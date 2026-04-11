Current Work Delivery Framework is located in `work_delivery` folder.

New Work Delivery Framework (in progress) is located in `work_delivery_framework` folder.

## Encoding Guardrails

- Preserve Markdown and text files as UTF-8 without BOM.
- Prefer `apply_patch` for documentation edits so encoding and punctuation are preserved.
- Avoid bulk rewrite commands for text files unless they explicitly write UTF-8 and are needed for a specific fix.

## Session Digests

`session_digests/` contains past conversations, decisions, context, and issues in LoreSpec format, generated via the `extract-a-lore-md` skill. When creating a LORE or session digest, link it to related session digests when relevant, but only if no explicit trail is provided.
