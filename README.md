# doctor-codebase

A Claude Code skill that maps how an unfamiliar codebase works. It classifies
the codebase type, traces data flows, scans for architectural smells, and ends
with a risk profile that states what was not explored.

Derived from [quicksilversurfer/codebase-explorer](https://github.com/quicksilversurfer/codebase-explorer).
See NOTICE.md for the pinned commit and the list of changes.

## Install

Run inside a Claude Code session, as two separate prompts:

    /plugin marketplace add berzileux/doctor-codebase
    /plugin install doctor-codebase@doctor-codebase
    
Uninstall

    /plugin uninstall doctor-codebase@doctor-codebase
    /plugin marketplace remove doctor-codebase
    
Disable the plugin, enable it when needed

    /plugin disable doctor-codebase@doctor-codebase
    /plugin enable doctor-codebase@doctor-codebase

## Use

The skill loads when your request matches its description. Examples:

- "Explore this codebase"
- "I inherited this code, onboard me"
- "Audit this system's architecture"

If the plugin namespace is needed, the skill name is `doctor-codebase:doctor-codebase`.

## What it does

1. Detects the archetype (frontend, backend API, pipeline, library, IaC, CLI, ML).
2. Maps I/O boundaries, hard limits, implicit contracts, and git activity.
3. Traces 3 to 5 vertical slices using the strategy for that archetype.
4. Scans for architectural smells.
5. Writes a risk profile and lists what was not explored.

## Safety notes

- The skill is pure Markdown. It contains no scripts and no network calls.
- Its instructions use read-only commands such as `git log`, `git status` and `ls`.
- Generated maps describe what the model believes the code does. Spot-check
  data flows against the code before you rely on them.
- Read SKILL.md before you run it in a session with permissions skipped.
  Run such sessions only in a sandbox with no production credentials.

## Layout

    .claude-plugin/
      marketplace.json
      plugin.json
    skills/
      doctor-codebase/
        SKILL.md
        references/
    NOTICE.md
    README.md

## Uninstall

    /plugin uninstall doctor-codebase@doctor-codebase
