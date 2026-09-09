# gway-agent

Codex-oriented agent assets for the gway ecosystem.

## Purpose

This repository is the shared home for reusable Codex and agent integration assets used across Arthexis projects.

- `skills/` — Codex skills, one directory per skill with `SKILL.md` as the entry point.
- `hooks/` — lifecycle and integration hooks.
- `tools/` — agent-facing utilities and tool definitions.
- `src/gway_agent/` — reusable Python support code shared by hooks and tools.

Keep product-specific behavior in the consuming repository unless it is broadly reusable across the gway ecosystem.

## Development

The project follows the shared `arthexis/ci-base` Python baseline. CI runs Ruff, pytest, package builds, and clean-install checks through the central reusable workflow.

Run the local quality checks with:

```console
bash .ci/quality.sh --check .
```

Apply safe Ruff fixes and formatting with:

```console
bash .ci/quality.sh --fix .
```

Validate the repository baseline with:

```console
python .ci/check_repo.py
```
