# Work Delivery Framework v1

## 1. Purpose

This folder is the publishable `v1` operating pack derived from the canonical specification in `../work_delivery_framework_specification.md`.

Use this folder when you need the framework in a navigable, operational form with:

1. core framework guidance
2. artifact-level specifications
3. ready-to-use templates
4. machine-readable framework definitions

## 2. Canonical Source Rule

The canonical source of truth remains `../work_delivery_framework_specification.md`.

The files in this folder are derived operating artifacts. If any conflict is discovered, treat the canonical specification as authoritative and update this `v1` pack to match it.

## 3. Start Here

Read in this order:

1. `framework_overview.md`
2. `artifact_catalog.md`
3. `completeness_and_review_model.md`
4. the relevant file in `artifact_specifications/`
5. the matching template in `templates/`

## 4. Folder Map

| Path | Use it for |
| --- | --- |
| `framework_overview.md` | Scope, lifecycle, stages, gates, scaling, and operating model |
| `artifact_catalog.md` | Canonical artifacts, triggers, gate requirements, packaging rules |
| `completeness_and_review_model.md` | Completeness, AI sufficiency, review, blockers, and anti-bureaucracy controls |
| `artifact_specifications/` | Normative drafting and review specifications for each canonical artifact |
| `templates/` | Ready-to-use Markdown forms/templates |
| `machine_readable/` | YAML catalogs for AI and tooling consumption |
| `examples/` | Small example artifacts showing intended quality and structure |

## 5. Common Tasks

| If you need to... | Start here |
| --- | --- |
| Understand the framework lifecycle | `framework_overview.md` |
| Decide which artifacts are required | `artifact_catalog.md` |
| Judge whether an artifact or gate is complete | `completeness_and_review_model.md` |
| Draft a Project Brief | `artifact_specifications/initiative_definition_project_brief_specification.md` then `templates/initiative_definition_project_brief_template.md` |
| Draft a Decision Log or Open Items Register | the matching spec and template in their folders |
| Extract machine-readable framework objects | `machine_readable/` |

## 6. Design Principles

This `v1` pack is intentionally lean.

It is designed to:

1. preserve the framework's formal controls
2. reduce navigation friction for human teams
3. keep artifact names and identifiers stable for AI agents
4. avoid recreating the larger legacy taxonomy unless the canonical specification requires it

## 7. Important Usage Rules

1. Do not treat document presence as proof of completeness.
2. Do not proceed through a gate when mandatory pass conditions are not satisfied.
3. Do not leave uncontrolled placeholders such as `TBD` or `TBC` in required artifacts.
4. Record material decisions in the `Decision Log`.
5. Record unresolved blockers, risks, issues, assumptions, and dependencies in the `Open Items Register`.
6. Use the named template only when its trigger condition is true or when the artifact is always required.

## 8. Related File

The design note used to structure this pack is `v1_document_set_design.md`.
