# claude-skills

Working rules I bind Claude Code to.

## Contents

| File | What it is |
|---|---|
| [`you-work-for-me.md`](you-work-for-me.md) | **Only Plan A**: how Claude works for me. I am the boss. Every task goes all the way to a verified result, and nothing comes back to me as a chore. Inspired by *The Devil Wears Prada*. |

## Use it

**With the `manifesto` plugin** from [ryzhakar/claude-skills](https://github.com/ryzhakar/claude-skills): save the file locally, then add it to `.manifestos.yaml` in your project. It is then bound at session start, after compaction, and in every subagent.

```yaml
you:
  - name: you-work-for-me
    purpose: working relationship
    source: /absolute/path/to/you-work-for-me.md
subagents:
  other:
    - name: you-work-for-me
      purpose: working relationship
      source: /absolute/path/to/you-work-for-me.md
```

**Without the plugin**: save the file as `~/.claude/manifestos/you-work-for-me.md`, then add one line to `~/.claude/CLAUDE.md`:

```markdown
Read `~/.claude/manifestos/you-work-for-me.md` in full at session start and follow it.
```

Swap "Vic" in the text for your own name.
