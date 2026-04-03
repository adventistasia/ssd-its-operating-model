# ITS Operating Model MCP Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Build a repo-local Codex plugin named `its-operating-model-mcp` that installs and manages its own clone of the ITS Operating Model repository, serves authoritative documents through MCP, checks once per day for upstream updates on first use, and provides a manual update command.

**Architecture:** Use a repo-local plugin under `plugins/its-operating-model-mcp/` with a required `.codex-plugin/plugin.json`, a `.mcp.json` MCP registration file, and a small TypeScript codebase. Separate plugin metadata, config persistence, repository lifecycle management, document routing, and MCP/CLI entrypoints so setup, update checks, and retrieval stay testable.

**Tech Stack:** TypeScript, Node.js, npm, MCP stdio server, Git CLI, Vitest

---

## File Structure

### Create

- `.agents/plugins/marketplace.json`
- `plugins/its-operating-model-mcp/.codex-plugin/plugin.json`
- `plugins/its-operating-model-mcp/.mcp.json`
- `plugins/its-operating-model-mcp/package.json`
- `plugins/its-operating-model-mcp/tsconfig.json`
- `plugins/its-operating-model-mcp/README.md`
- `plugins/its-operating-model-mcp/skills/update-managed-repo/SKILL.md`
- `plugins/its-operating-model-mcp/src/constants.ts`
- `plugins/its-operating-model-mcp/src/config.ts`
- `plugins/its-operating-model-mcp/src/git.ts`
- `plugins/its-operating-model-mcp/src/repo-manager.ts`
- `plugins/its-operating-model-mcp/src/documents.ts`
- `plugins/its-operating-model-mcp/src/server.ts`
- `plugins/its-operating-model-mcp/src/cli.ts`
- `plugins/its-operating-model-mcp/tests/config.test.ts`
- `plugins/its-operating-model-mcp/tests/repo-manager.test.ts`
- `plugins/its-operating-model-mcp/tests/documents.test.ts`

### Modify

- `.gitignore`

## Task 1: Scaffold the plugin package

**Files:**
- Create: `.agents/plugins/marketplace.json`
- Create: `plugins/its-operating-model-mcp/.codex-plugin/plugin.json`
- Create: `plugins/its-operating-model-mcp/.mcp.json`
- Create: `plugins/its-operating-model-mcp/package.json`
- Create: `plugins/its-operating-model-mcp/tsconfig.json`
- Create: `plugins/its-operating-model-mcp/README.md`
- Modify: `.gitignore`

- [ ] **Step 1: Write the failing scaffold test**

```ts
import { describe, expect, it } from "vitest";
import { existsSync, readFileSync } from "node:fs";
import { resolve } from "node:path";

describe("plugin scaffold", () => {
  it("declares the Codex plugin manifest and MCP config", () => {
    const root = resolve(process.cwd(), "plugins/its-operating-model-mcp");
    expect(existsSync(resolve(root, ".codex-plugin/plugin.json"))).toBe(true);
    expect(existsSync(resolve(root, ".mcp.json"))).toBe(true);
    const pluginJson = JSON.parse(readFileSync(resolve(root, ".codex-plugin/plugin.json"), "utf8"));
    expect(pluginJson.name).toBe("its-operating-model-mcp");
    expect(pluginJson.mcpServers).toBe("./.mcp.json");
  });
});
```

- [ ] **Step 2: Run test to verify it fails**

Run: `npm test -- --run tests/config.test.ts`
Expected: FAIL with missing manifest/config files

- [ ] **Step 3: Add the minimal scaffold**

```json
// .agents/plugins/marketplace.json
{"name":"local-repo-plugins","interface":{"displayName":"Local Repo Plugins"},"plugins":[{"name":"its-operating-model-mcp","source":{"source":"local","path":"./plugins/its-operating-model-mcp"},"policy":{"installation":"AVAILABLE","authentication":"ON_INSTALL"},"category":"Productivity"}]}
```

```json
// plugins/its-operating-model-mcp/.codex-plugin/plugin.json
{"name":"its-operating-model-mcp","version":"0.1.0","description":"Managed ITS Operating Model MCP plugin","author":{"name":"SSD ITS","email":"its@example.org","url":"https://github.com/adventistasia"},"homepage":"https://github.com/adventistasia/ssd-its-operating-model","repository":"https://github.com/adventistasia/ssd-its-operating-model","license":"MIT","keywords":["mcp","its","operating-model"],"skills":"./skills/","mcpServers":"./.mcp.json","interface":{"displayName":"ITS Operating Model MCP","shortDescription":"Managed local access to ITS operating model documents","longDescription":"Installs and manages a local ITS Operating Model clone and serves authoritative docs through MCP.","developerName":"SSD ITS","category":"Productivity","capabilities":["Interactive","Read","Write"],"websiteURL":"https://github.com/adventistasia/ssd-its-operating-model","privacyPolicyURL":"https://github.com/adventistasia/ssd-its-operating-model","termsOfServiceURL":"https://github.com/adventistasia/ssd-its-operating-model","defaultPrompt":["Open the ITS Operating Model start-here guide.","Find the right deliverable specification for this stage.","Check whether the managed ITS repo has updates."],"brandColor":"#1F5F8B"}}
```

```json
// plugins/its-operating-model-mcp/.mcp.json
{"mcpServers":{"its-operating-model":{"command":"node","args":["./dist/server.js"]}}}
```

```json
// plugins/its-operating-model-mcp/package.json
{"name":"its-operating-model-mcp","version":"0.1.0","private":true,"type":"module","scripts":{"build":"tsc -p tsconfig.json","test":"vitest run","setup:repo":"node ./dist/cli.js setup","check-updates":"node ./dist/cli.js check-updates","update-repo":"node ./dist/cli.js update-repo","start:mcp":"node ./dist/server.js"},"dependencies":{"@modelcontextprotocol/sdk":"^1.10.0","zod":"^3.24.2"},"devDependencies":{"@types/node":"^22.14.0","typescript":"^5.8.3","vitest":"^3.1.1"}}
```

```json
// plugins/its-operating-model-mcp/tsconfig.json
{"compilerOptions":{"target":"ES2022","module":"NodeNext","moduleResolution":"NodeNext","outDir":"./dist","rootDir":"./src","strict":true,"esModuleInterop":true,"skipLibCheck":true,"types":["node"]},"include":["src/**/*.ts"]}
```

```gitignore
# .gitignore
.obsidian/
plugins/its-operating-model-mcp/dist/
plugins/its-operating-model-mcp/.runtime/
```

- [ ] **Step 4: Run test to verify it passes**

Run: `npm test -- --run tests/config.test.ts`
Expected: PASS

- [ ] **Step 5: Commit**

```bash
git add .agents/plugins/marketplace.json .gitignore plugins/its-operating-model-mcp
git commit -m "feat: scaffold ITS operating model MCP plugin"
```

## Task 2: Add config persistence and repo constants

**Files:**
- Create: `plugins/its-operating-model-mcp/src/constants.ts`
- Create: `plugins/its-operating-model-mcp/src/config.ts`
- Modify: `plugins/its-operating-model-mcp/tests/config.test.ts`

- [ ] **Step 1: Write the failing config tests**

```ts
import { afterEach, describe, expect, it } from "vitest";
import { mkdtempSync, rmSync } from "node:fs";
import { tmpdir } from "node:os";
import { join } from "node:path";
import { CONFIG_FILE_NAME, DEFAULT_REPO_BRANCH, DEFAULT_REPO_URL, getDefaultManagedRepoPath, loadPluginConfig, savePluginConfig } from "../src/config";

describe("config persistence", () => {
  const roots: string[] = [];
  afterEach(() => roots.splice(0).forEach((root) => rmSync(root, { recursive: true, force: true })));
  it("returns defaults before setup completes", () => {
    const root = mkdtempSync(join(tmpdir(), "its-mcp-"));
    roots.push(root);
    const config = loadPluginConfig(root);
    expect(config.setupCompleted).toBe(false);
    expect(config.repoUrl).toBe(DEFAULT_REPO_URL);
    expect(config.trackedBranch).toBe(DEFAULT_REPO_BRANCH);
    expect(config.repoPath).toBe(getDefaultManagedRepoPath(root));
  });
  it("round-trips saved config values", () => {
    const root = mkdtempSync(join(tmpdir(), "its-mcp-"));
    roots.push(root);
    savePluginConfig(root, { setupCompleted: true, repoUrl: DEFAULT_REPO_URL, trackedBranch: DEFAULT_REPO_BRANCH, repoPath: join(root, "managed-repo"), lastUpdateCheckDate: "2026-04-03", lastSeenLocalCommit: "abc123", lastSeenRemoteCommit: "def456" });
    const config = loadPluginConfig(root);
    expect(config.lastUpdateCheckDate).toBe("2026-04-03");
    expect(config.lastSeenLocalCommit).toBe("abc123");
    expect(config.lastSeenRemoteCommit).toBe("def456");
    expect(CONFIG_FILE_NAME).toBe("config.json");
  });
});
```

- [ ] **Step 2: Run test to verify it fails**

Run: `npm test -- --run tests/config.test.ts`
Expected: FAIL with missing `../src/config`

- [ ] **Step 3: Write the implementation**

```ts
// constants.ts
export const PLUGIN_NAME = "its-operating-model-mcp";
export const DEFAULT_REPO_URL = "https://github.com/adventistasia/ssd-its-operating-model";
export const DEFAULT_REPO_BRANCH = "main";
export const CONFIG_DIR_NAME = ".runtime";
export const CONFIG_FILE_NAME = "config.json";
export const REQUIRED_DOCS = ["README.md","its_operating_model.md","its_work_management_model.md","work_delivery/work_delivery_framework.md","work_delivery/deliverable_specifications_index.md"] as const;
```

```ts
// config.ts
import { existsSync, mkdirSync, readFileSync, writeFileSync } from "node:fs";
import { join } from "node:path";
import { CONFIG_DIR_NAME, CONFIG_FILE_NAME, DEFAULT_REPO_BRANCH, DEFAULT_REPO_URL } from "./constants";
export { CONFIG_FILE_NAME, DEFAULT_REPO_BRANCH, DEFAULT_REPO_URL } from "./constants";
export type PluginConfig = { setupCompleted: boolean; repoUrl: string; trackedBranch: string; repoPath: string; lastUpdateCheckDate?: string; lastSeenLocalCommit?: string; lastSeenRemoteCommit?: string; };
export function getConfigDir(root: string): string { return join(root, CONFIG_DIR_NAME); }
export function getConfigPath(root: string): string { return join(getConfigDir(root), CONFIG_FILE_NAME); }
export function getDefaultManagedRepoPath(root: string): string { return join(getConfigDir(root), "ssd-its-operating-model"); }
export function loadPluginConfig(root: string): PluginConfig { const path = getConfigPath(root); if (!existsSync(path)) { return { setupCompleted: false, repoUrl: DEFAULT_REPO_URL, trackedBranch: DEFAULT_REPO_BRANCH, repoPath: getDefaultManagedRepoPath(root) }; } return JSON.parse(readFileSync(path, "utf8")) as PluginConfig; }
export function savePluginConfig(root: string, config: PluginConfig): void { mkdirSync(getConfigDir(root), { recursive: true }); writeFileSync(getConfigPath(root), JSON.stringify(config, null, 2)); }
```

- [ ] **Step 4: Run test to verify it passes**

Run: `npm test -- --run tests/config.test.ts`
Expected: PASS

- [ ] **Step 5: Commit**

```bash
git add plugins/its-operating-model-mcp/src/constants.ts plugins/its-operating-model-mcp/src/config.ts plugins/its-operating-model-mcp/tests/config.test.ts
git commit -m "feat: add MCP plugin config persistence"
```

## Task 3: Implement managed clone install and update logic

**Files:**
- Create: `plugins/its-operating-model-mcp/src/git.ts`
- Create: `plugins/its-operating-model-mcp/src/repo-manager.ts`
- Create: `plugins/its-operating-model-mcp/tests/repo-manager.test.ts`

- [ ] **Step 1: Write the failing repo-manager tests**

```ts
import { describe, expect, it, vi } from "vitest";
import { REQUIRED_DOCS } from "../src/constants";
import { checkForDailyUpdates, createManagedRepo, validateManagedRepo } from "../src/repo-manager";

describe("repo manager", () => {
  it("validates required authoritative files", () => {
    const exists = vi.fn((file: string) => REQUIRED_DOCS.includes(file as never));
    expect(validateManagedRepo("C:/managed/repo", exists)).toEqual({ ok: true, missing: [] });
  });
  it("skips update fetch after daily check is recorded", async () => {
    const fetchRemote = vi.fn();
    const result = await checkForDailyUpdates({ setupCompleted: true, repoUrl: "https://github.com/adventistasia/ssd-its-operating-model", trackedBranch: "main", repoPath: "C:/managed/repo", lastUpdateCheckDate: "2026-04-03", lastSeenLocalCommit: "local-1", lastSeenRemoteCommit: "remote-1" }, "2026-04-03", fetchRemote);
    expect(result.status).toBe("skipped");
    expect(fetchRemote).not.toHaveBeenCalled();
  });
  it("clones the managed repo during setup", async () => {
    const cloneRepo = vi.fn().mockResolvedValue("local-commit");
    const result = await createManagedRepo({ setupCompleted: false, repoUrl: "https://github.com/adventistasia/ssd-its-operating-model", trackedBranch: "main", repoPath: "C:/managed/repo" }, cloneRepo, () => ({ ok: true, missing: [] }));
    expect(cloneRepo).toHaveBeenCalledWith("https://github.com/adventistasia/ssd-its-operating-model", "main", "C:/managed/repo");
    expect(result.setupCompleted).toBe(true);
  });
});
```

- [ ] **Step 2: Run test to verify it fails**

Run: `npm test -- --run tests/repo-manager.test.ts`
Expected: FAIL with missing `../src/repo-manager`

- [ ] **Step 3: Write the implementation**

```ts
// git.ts
import { execFile } from "node:child_process";
function runGit(args: string[], cwd?: string): Promise<string> { return new Promise((resolve, reject) => execFile("git", args, { cwd }, (error, stdout, stderr) => error ? reject(new Error(stderr || error.message)) : resolve(stdout.trim()))); }
export function cloneRepo(repoUrl: string, branch: string, targetPath: string): Promise<string> { return runGit(["clone","--branch",branch,repoUrl,targetPath]).then(() => runGit(["rev-parse","HEAD"], targetPath)); }
export function fetchRemote(targetPath: string): Promise<void> { return runGit(["fetch","origin","--quiet"], targetPath).then(() => undefined); }
export function getHeadCommit(targetPath: string): Promise<string> { return runGit(["rev-parse","HEAD"], targetPath); }
export function getRemoteCommit(targetPath: string, branch: string): Promise<string> { return runGit(["rev-parse",`origin/${branch}`], targetPath); }
export function pullFastForward(targetPath: string, branch: string): Promise<string> { return runGit(["pull","--ff-only","origin",branch], targetPath).then(() => runGit(["rev-parse","HEAD"], targetPath)); }
```

```ts
// repo-manager.ts
import { existsSync } from "node:fs";
import { join } from "node:path";
import { PluginConfig } from "./config";
import { REQUIRED_DOCS } from "./constants";
import { cloneRepo, fetchRemote, getHeadCommit, getRemoteCommit, pullFastForward } from "./git";
export type ValidationResult = { ok: boolean; missing: string[] };
export function validateManagedRepo(repoPath: string, fileExists: (path: string) => boolean = (path) => existsSync(join(repoPath, path))): ValidationResult { const missing = REQUIRED_DOCS.filter((path) => !fileExists(path)); return { ok: missing.length === 0, missing: [...missing] }; }
export async function createManagedRepo(config: PluginConfig, clone = cloneRepo, validate = validateManagedRepo): Promise<PluginConfig> { const localCommit = await clone(config.repoUrl, config.trackedBranch, config.repoPath); const validation = validate(config.repoPath); if (!validation.ok) throw new Error(`Managed repo is missing required files: ${validation.missing.join(", ")}`); return { ...config, setupCompleted: true, lastSeenLocalCommit: localCommit, lastSeenRemoteCommit: localCommit }; }
export async function checkForDailyUpdates(config: PluginConfig, currentDate: string, fetch = async (repoPath: string, branch: string) => { await fetchRemote(repoPath); return { localCommit: await getHeadCommit(repoPath), remoteCommit: await getRemoteCommit(repoPath, branch) }; }): Promise<{ status: "skipped" | "up-to-date" | "update-available"; config: PluginConfig; }> { if (config.lastUpdateCheckDate === currentDate) return { status: "skipped", config }; const { localCommit, remoteCommit } = await fetch(config.repoPath, config.trackedBranch); const nextConfig = { ...config, lastUpdateCheckDate: currentDate, lastSeenLocalCommit: localCommit, lastSeenRemoteCommit: remoteCommit }; return { status: localCommit === remoteCommit ? "up-to-date" : "update-available", config: nextConfig }; }
export async function applyRepoUpdate(config: PluginConfig): Promise<PluginConfig> { const updatedCommit = await pullFastForward(config.repoPath, config.trackedBranch); return { ...config, lastSeenLocalCommit: updatedCommit, lastSeenRemoteCommit: updatedCommit }; }
```

- [ ] **Step 4: Run test to verify it passes**

Run: `npm test -- --run tests/repo-manager.test.ts`
Expected: PASS

- [ ] **Step 5: Commit**

```bash
git add plugins/its-operating-model-mcp/src/git.ts plugins/its-operating-model-mcp/src/repo-manager.ts plugins/its-operating-model-mcp/tests/repo-manager.test.ts
git commit -m "feat: add managed repo install and update logic"
```

## Task 4: Implement authoritative document routing

**Files:**
- Create: `plugins/its-operating-model-mcp/src/documents.ts`
- Create: `plugins/its-operating-model-mcp/tests/documents.test.ts`

- [ ] **Step 1: Write the failing document-routing tests**

```ts
import { describe, expect, it } from "vitest";
import { getDocumentByName, getStageGuidance } from "../src/documents";

describe("document routing", () => {
  it("maps start-here requests to README", () => expect(getDocumentByName("get_start_here")?.relativePath).toBe("README.md"));
  it("maps stage 1 requests to the work assessment process", () => expect(getStageGuidance("stage 1")?.relativePath).toBe("work_delivery/work_assessment/work_assessment_process.md"));
  it("maps small governed work to the work brief specification", () => expect(getStageGuidance("small governed work")?.relativePath).toBe("work_delivery/work_brief/work_brief_specification.md"));
});
```

- [ ] **Step 2: Run test to verify it fails**

Run: `npm test -- --run tests/documents.test.ts`
Expected: FAIL with missing `../src/documents`

- [ ] **Step 3: Write the implementation**

```ts
export type DocumentRecord = { name: string; relativePath: string; title: string };
const DOCUMENTS: Record<string, DocumentRecord> = {
  get_start_here: { name: "get_start_here", relativePath: "README.md", title: "Start Here" },
  get_operating_model: { name: "get_operating_model", relativePath: "its_operating_model.md", title: "ITS Operating Model" },
  get_work_management_model: { name: "get_work_management_model", relativePath: "its_work_management_model.md", title: "ITS Work Management Model" },
  get_work_delivery_framework: { name: "get_work_delivery_framework", relativePath: "work_delivery/work_delivery_framework.md", title: "Work Delivery Framework" },
  get_deliverable_specifications_index: { name: "get_deliverable_specifications_index", relativePath: "work_delivery/deliverable_specifications_index.md", title: "Deliverable Specifications Index" },
  get_standard_deliverables_guide: { name: "get_standard_deliverables_guide", relativePath: "work_delivery/standard_deliverables_guide.md", title: "Standard Deliverables Guide" },
};
const STAGE_GUIDANCE = [
  { match: /\bstage 1\b|\bassess|\bassessment\b/i, doc: { name: "work_assessment_process", relativePath: "work_delivery/work_assessment/work_assessment_process.md", title: "Work Assessment Process" } },
  { match: /\bsmall governed work\b|\bwork brief\b/i, doc: { name: "work_brief_specification", relativePath: "work_delivery/work_brief/work_brief_specification.md", title: "Work Brief Specification" } },
  { match: /\binitiative\b|\bformal baseline\b/i, doc: { name: "initiative_definition_document_specification", relativePath: "work_delivery/governance_and_control_deliverables/initiative_definition_document_specification.md", title: "Initiative Definition Document Specification" } },
];
export function getDocumentByName(name: string): DocumentRecord | undefined { return DOCUMENTS[name]; }
export function getStageGuidance(stageOrIntent: string): DocumentRecord | undefined { return STAGE_GUIDANCE.find(({ match }) => match.test(stageOrIntent))?.doc; }
```

- [ ] **Step 4: Run test to verify it passes**

Run: `npm test -- --run tests/documents.test.ts`
Expected: PASS

- [ ] **Step 5: Commit**

```bash
git add plugins/its-operating-model-mcp/src/documents.ts plugins/its-operating-model-mcp/tests/documents.test.ts
git commit -m "feat: add stage-aware document routing"
```

## Task 5: Implement the MCP server and CLI entrypoints

**Files:**
- Create: `plugins/its-operating-model-mcp/src/cli.ts`
- Create: `plugins/its-operating-model-mcp/src/server.ts`
- Modify: `plugins/its-operating-model-mcp/package.json`

- [ ] **Step 1: Write the failing CLI helper tests**

```ts
import { describe, expect, it } from "vitest";
import { formatUpdateMessage, parseCliArgs } from "../src/cli";

describe("cli helpers", () => {
  it("parses the setup command", () => expect(parseCliArgs(["setup"])).toEqual({ command: "setup" }));
  it("formats an update-available prompt", () => expect(formatUpdateMessage({ status: "update-available", localCommit: "abc123", remoteCommit: "def456" })).toContain("Update available"));
});
```

- [ ] **Step 2: Run test to verify it fails**

Run: `npm test -- --run tests/repo-manager.test.ts`
Expected: FAIL with missing `../src/cli`

- [ ] **Step 3: Write the implementation**

```ts
// cli.ts
import { join } from "node:path";
import { loadPluginConfig, savePluginConfig } from "./config";
import { applyRepoUpdate, checkForDailyUpdates, createManagedRepo } from "./repo-manager";
export function parseCliArgs(args: string[]): { command: "setup" | "check-updates" | "update-repo" } { const [command] = args; if (command === "setup" || command === "check-updates" || command === "update-repo") return { command }; throw new Error(`Unsupported command: ${command ?? "undefined"}`); }
export function formatUpdateMessage(result: { status: "update-available" | "up-to-date"; localCommit: string; remoteCommit: string; }): string { return result.status === "up-to-date" ? `Managed repo is up to date at ${result.localCommit}.` : `Update available. Local ${result.localCommit} -> remote ${result.remoteCommit}. Run npm run update-repo to apply it.`; }
async function main(): Promise<void> { const { command } = parseCliArgs(process.argv.slice(2)); const pluginRoot = join(import.meta.dirname, ".."); let config = loadPluginConfig(pluginRoot); if (command === "setup") { config = await createManagedRepo(config); savePluginConfig(pluginRoot, config); console.log(`Managed repo installed at ${config.repoPath}`); return; } const today = new Date().toISOString().slice(0, 10); if (command === "check-updates") { const result = await checkForDailyUpdates(config, today); savePluginConfig(pluginRoot, result.config); if (result.status === "skipped") { console.log("Daily update check already completed today."); return; } console.log(formatUpdateMessage({ status: result.status === "update-available" ? "update-available" : "up-to-date", localCommit: result.config.lastSeenLocalCommit ?? "unknown", remoteCommit: result.config.lastSeenRemoteCommit ?? "unknown" })); return; } config = await applyRepoUpdate(config); savePluginConfig(pluginRoot, config); console.log(`Managed repo updated to ${config.lastSeenLocalCommit}`); }
void main();
```

```ts
// server.ts
import { readFileSync } from "node:fs";
import { join } from "node:path";
import { McpServer } from "@modelcontextprotocol/sdk/server/mcp.js";
import { StdioServerTransport } from "@modelcontextprotocol/sdk/server/stdio.js";
import { z } from "zod";
import { loadPluginConfig } from "./config";
import { getDocumentByName, getStageGuidance } from "./documents";
const server = new McpServer({ name: "its-operating-model", version: "0.1.0" });
function readManagedDocument(relativePath: string): string { const pluginRoot = join(import.meta.dirname, ".."); const config = loadPluginConfig(pluginRoot); return readFileSync(join(config.repoPath, relativePath), "utf8"); }
server.tool("get_document", { name: z.string() }, async ({ name }) => { const doc = getDocumentByName(name); return { content: [{ type: "text", text: doc ? `Source: ${doc.relativePath}\n\n${readManagedDocument(doc.relativePath)}` : `Unknown document: ${name}` }] }; });
server.tool("get_stage_guidance", { stage_or_intent: z.string() }, async ({ stage_or_intent }) => { const doc = getStageGuidance(stage_or_intent); return { content: [{ type: "text", text: doc ? `Source: ${doc.relativePath}\n\n${readManagedDocument(doc.relativePath)}` : "No stage guidance matched. Try a stage number, work brief, or initiative request." }] }; });
await server.connect(new StdioServerTransport());
```

- [ ] **Step 4: Run tests to verify they pass**

Run: `npm test -- --run tests/repo-manager.test.ts tests/documents.test.ts`
Expected: PASS

- [ ] **Step 5: Build the plugin**

Run: `npm run build`
Expected: PASS with `dist/cli.js` and `dist/server.js`

- [ ] **Step 6: Commit**

```bash
git add plugins/its-operating-model-mcp/src/cli.ts plugins/its-operating-model-mcp/src/server.ts plugins/its-operating-model-mcp/package.json
git commit -m "feat: add MCP server and CLI commands"
```

## Task 6: Add the manual update skill and final usage docs

**Files:**
- Create: `plugins/its-operating-model-mcp/skills/update-managed-repo/SKILL.md`
- Modify: `plugins/its-operating-model-mcp/README.md`

- [ ] **Step 1: Write the failing skill-presence test**

```ts
import { describe, expect, it } from "vitest";
import { existsSync, readFileSync } from "node:fs";
import { resolve } from "node:path";

describe("manual update skill", () => {
  it("documents the managed update workflow", () => {
    const skillPath = resolve(process.cwd(), "plugins/its-operating-model-mcp/skills/update-managed-repo/SKILL.md");
    expect(existsSync(skillPath)).toBe(true);
    expect(readFileSync(skillPath, "utf8")).toContain("npm run update-repo");
  });
});
```

- [ ] **Step 2: Run test to verify it fails**

Run: `npm test -- --run tests/documents.test.ts`
Expected: FAIL because the skill file does not exist yet

- [ ] **Step 3: Write the skill and README**

```md
---
name: update-managed-repo
description: Refresh the plugin-managed ITS Operating Model clone after confirming that the user wants to apply available upstream updates.
---

# Update Managed Repo

1. Run `npm run check-updates` from the plugin root.
2. If no updates are available, tell the user the managed repository is already current.
3. If updates are available, ask whether to apply them now.
4. Only after confirmation, run `npm run update-repo`.
5. Report the new managed revision and remind the user that authoritative content may have changed.
```

```md
# ITS Operating Model MCP

This plugin manages a local clone of the ITS Operating Model repository and serves authoritative documents through MCP.

## Setup

1. `npm install`
2. `npm run build`
3. `npm run setup:repo`

## Commands

- `npm run check-updates`
- `npm run update-repo`
- `npm run start:mcp`

## Managed update policy

The plugin checks for upstream changes once per day on first use and tells the user when updates are available.
It does not apply updates automatically.
```

- [ ] **Step 4: Run tests to verify they pass**

Run: `npm test -- --run tests/documents.test.ts`
Expected: PASS

- [ ] **Step 5: Commit**

```bash
git add plugins/its-operating-model-mcp/skills/update-managed-repo/SKILL.md plugins/its-operating-model-mcp/README.md plugins/its-operating-model-mcp/tests/documents.test.ts
git commit -m "docs: add managed repo update skill and usage notes"
```

## Task 7: Verify the full flow

**Files:**
- Modify: `plugins/its-operating-model-mcp/package.json`

- [ ] **Step 1: Add a verify script**

```json
{"scripts":{"verify":"npm run test && npm run build"}}
```

- [ ] **Step 2: Run automated verification**

Run: `npm run verify`
Expected: PASS with Vitest and TypeScript build green

- [ ] **Step 3: Run setup and update commands**

Run: `npm run setup:repo`
Expected: PASS with `Managed repo installed at <plugin-root>/.runtime/ssd-its-operating-model`

Run: `npm run check-updates`
Expected: PASS with either `Managed repo is up to date` or `Update available`

- [ ] **Step 4: Start the MCP server**

Run: `npm run start:mcp`
Expected: PASS with the process waiting for stdio MCP requests and no startup errors

- [ ] **Step 5: Commit**

```bash
git add plugins/its-operating-model-mcp/package.json
git commit -m "chore: verify ITS operating model MCP plugin"
```
