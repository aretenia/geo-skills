# Contributing

PRs welcome. This pack is meant to stay free, local-first, and honest.

## Ground rules

- **Free-first.** No skill should require a paid API to do its core job. If a third-party data source helps, mark it optional and make the skill degrade gracefully without it.
- **Cite your sources.** Research figures (correlation studies, benchmarks) must be attributed inline to the published study. Do not invent statistics.
- **No vendor lock-in.** Don't hardcode a specific paid tool as the only path.
- **Each skill is self-contained.** A skill should not reference another skill that is not shipped in this pack.

## Adding or editing a skill

Each skill lives in `skills/<name>/SKILL.md` with YAML frontmatter:

```yaml
---
name: your-skill
description: One clear sentence on what it does and when to use it.
---
```

Keep the opening section tight. Put long reference material in a `references/` subfolder.

## Before you open a PR

- Run the skill against a real URL and confirm it produces useful output.
- Make sure there are no references to skills outside this pack.
- Keep the writing plain. No marketing fluff.
