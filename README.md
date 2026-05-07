# llm-playground

Throwaway space for unstructured CLI sandboxing. Nothing here is tracked. If something in `notes.md` starts looking like a real pattern, promote it to a tracked experiment in [llm-testing](https://github.com/jordanmamroud/llm-testing).

## Layout

- `CLAUDE.md` — open Claude Code from this repo root
- `AGENTS.md` — for Codex CLI
- `notes.md` — one-liner observations as you go

Both files live at the root. Claude reads `CLAUDE.md`, Codex reads `AGENTS.md` — they don't interfere. If you later want multiple playgrounds (e.g., `claude-vanilla/` vs `claude-with-rules/`), add subfolders then.

## Stripped context checklist

For sandboxes to actually be stripped:

1. No parent dir should contain a `CLAUDE.md` / `AGENTS.md`. `~/GitHub/llm-playground/` is fine — `~/GitHub/` has none.
2. Strip your global `~/.claude/CLAUDE.md` if you want a truly clean baseline.
3. Disable plugins/skills that auto-inject context if you want minimal harness behavior.
