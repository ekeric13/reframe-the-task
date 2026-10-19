# Reframe the Task Skill

Challenge a familiar approach, clarify the intended outcome, and recommend a better solution with selective interviewing.

A cross-harness skill for Codex, Claude Code, and other Agent Skills-compatible tools. The skill is in [`reframe-the-task/`](./reframe-the-task/SKILL.md).

Use it when you know the domain but suspect there is a better solution than the current approach. It identifies the intended outcome, tests assumptions, and compares concrete alternatives, including keeping the current solution.

It reads available context first and asks one consequential question at a time only when the answer could change the recommendation. It stops interviewing when it can make a useful recommendation. Ask for a rewritten prompt, advice, or execution; a bare invocation explores and recommends.

## Install With skills.sh

Authenticate to GitHub with an account that can read this private repository before installing.

```bash
npx skills@latest add ekeric13/reframe-the-task
```

## Install For Codex

From a local clone:

```bash
mkdir -p ~/.codex/skills/reframe-the-task
rsync -a reframe-the-task/ ~/.codex/skills/reframe-the-task/
```

Start a new session and invoke it:

```text
Use $reframe-the-task to challenge my current approach, ask only consequential questions, and recommend a better solution before implementing anything.
```

## Install For Claude Code As A Plugin

```text
/plugin marketplace add https://github.com/ekeric13/reframe-the-task
/plugin install reframe-the-task@reframe-the-task
```

Invoke the namespaced skill with `/reframe-the-task:reframe-the-task`.

## Install For Claude Code As A Personal Skill

```bash
mkdir -p ~/.claude/skills/reframe-the-task
rsync -a reframe-the-task/ ~/.claude/skills/reframe-the-task/
```

Then use `/reframe-the-task`.

## Verify The Skill

```bash
python3 ~/.codex/skills/.system/skill-creator/scripts/quick_validate.py ./reframe-the-task
```

## Inspiration

Inspired by Felix Rieseberg's [How to be more ambitious: A tutorial for humans with models](https://felixrieseberg.com/how-to-be-more-ambitious-a-tutorial-for-humans-with-models/).
