Current Work Delivery Framework is located in `work_delivery` folder.

New Work Delivery Framework (in progress) is located in `work_delivery_framework` folder.

## Project Control Folder (this repo as a project)

Use `_project_control/` for repo-level planning and tracking artifacts (this is *not* framework content).

**Canonical locations**
- Open Items Register: `_project_control/open_items_register.md`
- Specs / design docs: `_project_control/specs/`
- Implementation plans: `_project_control/plans/`
- Reports / status / reviews: `_project_control/reports/`
- Findings (audit/review findings): `_project_control/findings/`

**Naming guidance**
- Prefer `YYYY-MM-DD-<artifact-type>-<short-slug>.md` for specs, plans, findings, and reports.
- Prefer `RAID-###` entry IDs inside `_project_control/open_items_register.md`.

**Superpowers location override**
- Save specs to: `_project_control/specs/` (do not use `docs/superpowers/specs/`)
- Save plans to: `_project_control/plans/` (do not use `docs/superpowers/plans/`)

## Encoding Guardrails

- Preserve Markdown and text files as UTF-8 without BOM.
- Prefer `apply_patch` for documentation edits so encoding and punctuation are preserved.
- Avoid bulk rewrite commands for text files unless they explicitly write UTF-8 and are needed for a specific fix.

## Session Digests

`_project_control/session_digests/` contains past conversations, decisions, context, and issues in LoreSpec format, generated via the `extract-a-lore-md` skill. When creating a LORE or session digest, link it to related session digests when relevant, but only if no explicit trail is provided.
