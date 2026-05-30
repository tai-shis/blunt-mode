# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Purpose

Claude Code plugin that activates blunt, direct communication mode. Strips social padding and sycophancy, challenges assumptions, prioritizes correctness.

## Structure

```
.claude-plugin/
  plugin.json        # plugin manifest
  marketplace.json   # marketplace metadata
skills/blunt-mode/
  SKILL.md           # skill definition injected into context on invocation
```

## Plugin Architecture

Discovered via `.claude-plugin/plugin.json`. The `skills` array points to skill directories containing `SKILL.md` with YAML frontmatter (`name`, `description`, `license`) and the instruction body.

The `description` field in frontmatter controls when the harness auto-triggers the skill — write it as trigger conditions, not a summary.

## Skill Design

`SKILL.md` is injected verbatim into context on invocation. Keep it instruction-focused. No narrative, no examples, no meta-commentary.
