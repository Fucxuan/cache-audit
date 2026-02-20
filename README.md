# cache-audit — Prompt Caching Skill for Claude Code

A Claude Code skill that audits your setup against the 6 prompt caching rules from Anthropic's engineering team. Returns a scored report with specific fixes.

## Why This Exists

Prompt caching is what makes Claude Code affordable at scale. A high cache hit rate reduces costs and latency dramatically — but it's surprisingly easy to break without knowing it.

The Anthropic team runs alerts on cache hit rates and treats drops as incidents. This skill brings the same discipline to your personal setup.

## What It Checks

| Rule | What breaks it |
|------|---------------|
| 1. Ordering | Dynamic data (timestamps, git status) in the system prompt |
| 2. Message injection | Editing the system prompt mid-session instead of using `<system-reminder>` tags |
| 3. Tool stability | Adding/removing tools mid-conversation |
| 4. Model switching | Switching models in the same conversation thread |
| 5. Dynamic content size | Injecting thousands of tokens of dynamic data per session |
| 6. Fork safety | Compaction/subagent calls that don't share the parent's prefix |

## Installation

### Global (applies to all projects)

```bash
mkdir -p ~/.claude/skills
curl -o ~/.claude/skills/cache-audit.md https://raw.githubusercontent.com/ussumant/cache-audit/main/cache-audit.md
```

### Per-project

```bash
mkdir -p .claude/skills
curl -o .claude/skills/cache-audit.md https://raw.githubusercontent.com/ussumant/cache-audit/main/cache-audit.md
```

Then restart your Claude Code session for the skill to register.

## Usage

```
/cache-audit
```

or say: `"audit my caching"` / `"check my cache setup"`

### Example Output

```
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
  PROMPT CACHE AUDIT
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Score: 5/6

✅  Rule 1 — Ordering: PASS
✅  Rule 2 — Message injection: PASS
✅  Rule 3 — Tool stability: PASS
✅  Rule 4 — Model switching: PASS
⚠️  Rule 5 — Dynamic content size: WARNING
    → Git status is 40k chars. Recommend trimming.
✅  Rule 6 — Fork safety: PASS

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
  TOP FIX
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Git status injects 40k chars per session. Update .gitignore
to stop listing untracked noise files.
```

## Background

Based on Thariq Shihipar's thread ["Lessons from Building Claude Code: Prompt Caching Is Everything"](https://x.com/trq212).

Key insight: prompt caching works by prefix matching. Any change to the prefix — tool order, system prompt edit, model switch — invalidates everything after it. Design your entire harness around keeping the prefix stable.

## Requirements

- [Claude Code](https://docs.anthropic.com/en/docs/claude-code) installed
- No other dependencies — single markdown file

## License

MIT
