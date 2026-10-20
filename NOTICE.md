# NOTICE

This repository contains work derived from another project.

## Upstream

- Project: codebase-explorer
- Author: quicksilversurfer
- URL: https://github.com/quicksilversurfer/codebase-explorer
- Pinned commit: 3b7dbb25a01fddfc319e08603724f5e6294863bb
- License: the upstream README states "MIT". At the pinned commit the
  upstream repository contains no LICENSE file, so no copyright holder
  line or license text was available to copy. Confirm with the upstream
  author before publishing this repository publicly.

## Files derived from upstream

- skills/doctor-codebase/SKILL.md
- skills/doctor-codebase/references/advanced-techniques.md
- skills/doctor-codebase/references/documentation-templates.md
- skills/doctor-codebase/references/smell-catalog.md

## Changes made to the upstream files

1. SKILL.md frontmatter: `name` changed from `codebase-explorer` to `doctor-codebase`.
2. SKILL.md: top heading changed from "Codebase Explorer" to "Doctor Codebase".
3. SKILL.md: one attribution line added below that heading.
4. Files moved under `skills/doctor-codebase/` so the repo works as a Claude Code plugin.

All other text in the four files is unchanged from the pinned commit.

## Files added in this repository

- .claude-plugin/marketplace.json
- .claude-plugin/plugin.json
- README.md
- NOTICE.md

## Updating from upstream

1. Clone upstream into an empty folder and note the new commit hash.
2. Diff it against the files above. Read the diff.
3. Copy the accepted changes, re-apply the changes listed above, and update
   the pinned commit hash here and in SKILL.md.
