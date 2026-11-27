# Free AI skills and prompts I actually use

Free Claude Code skills and prompts from my Instagram ([@official_arnavkapoor](https://www.instagram.com/official_arnavkapoor/)).

| What | Link |
|---|---|
| **AI teaches you AI**: a master prompt that interviews you and builds you a custom AI course (ChatGPT or Claude) | [prompts/ai-course.md](prompts/ai-course.md) |
| **check**: a Claude Code skill that makes Claude check its own work before it says "done" | [check/SKILL.md](check/SKILL.md) |

## check: makes Claude check its own work before it says "done"

Claude runs it, looks at it, compares it to what you asked, and fixes what's wrong, before it hands anything back.

**Install (30 seconds):**
1. Download [`check/SKILL.md`](check/SKILL.md).
2. Put it at `~/.claude/skills/check/SKILL.md` (make the folders if they don't exist).
3. Restart Claude Code. It now uses the skill on its own at the end of a task, or you can type `/check`.

Or paste this into your terminal:
```bash
mkdir -p ~/.claude/skills/check && curl -fsSL https://raw.githubusercontent.com/arnavkpr798-a11y/claude-skills/main/check/SKILL.md -o ~/.claude/skills/check/SKILL.md
```

Why it works: Boris Cherny, who created Claude Code, says giving Claude a way to verify its own work gives "2-3x the quality of the final result" ([his X thread, 3 Jan 2026](https://x.com/bcherny/status/2007179832300581177)).

More skills coming. Follow on Instagram for the next one.
