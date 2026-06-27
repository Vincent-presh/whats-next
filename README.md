# What's Next

`What's Next` helps agents decide the next best feature to build after a task is finished.

It turns product context into one clear follow-up move instead of a long, fuzzy backlog.

## What it is for

Use this repo when an agent needs to answer:

- what should we build next?
- which feature has the most leverage now?
- what is the smallest high-value next step?
- should this become a plan or a goal?

## Core idea

The skill looks at:

- current product state
- ideal product state
- user pain
- blocked dependencies
- effort and impact

Then it ranks the next few options and picks one move to make.

## Repo contents

- [SKILL.md](SKILL.md): Codex skill definition and workflow
- [CLAUDE.md](CLAUDE.md): Claude-friendly project instructions
- [.cursor/rules/whats-next.mdc](.cursor/rules/whats-next.mdc): Cursor rule version
- [references/decision-rubric.md](references/decision-rubric.md): simple ranking rubric

## How to use

### Codex

Codex reads [SKILL.md](SKILL.md). The skill is meant to be triggered after a task is done and the agent needs to decide the next best feature to build.

### Claude

Claude can use [CLAUDE.md](CLAUDE.md) as the lightweight instruction file for the same workflow.

### Cursor

Cursor can use [.cursor/rules/whats-next.mdc](.cursor/rules/whats-next.mdc) as the local rule file.

## Decision rule

Prefer the option that:

1. unlocks more work
1. removes a bottleneck
1. improves the core loop
1. is small enough to finish soon

Avoid building a long backlog when one clear next move exists.

## Example output

```text
Now: onboarding is working, but activation is weak.
Ideal: users reach value in the first session.
Next: fix the first-run setup step.
Why: it blocks activation and unlocks every later feature.
```

## Philosophy

This repo is meant to keep agents focused.

No giant roadmap.
No speculative padding.
No extra noise.

Just the next best thing to build.
