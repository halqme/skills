# Standalone Agent Skills

A collection of reusable agent skills, maintained separately from [Pi Kit](https://github.com/halqme/pi-kit). The skills use the `SKILL.md` directory format and do not require Pi Kit's runtime extensions.

## Skills

| Skill | Purpose |
| --- | --- |
| [`apply-correction`](skills/apply-correction/) | Revise an artifact from the authoritative current state after corrections or changed requirements. |
| [`cognitive-rhythm-writing`](skills/cognitive-rhythm-writing/) | Improve the progression of explanatory long-form prose without manufacturing drama. |
| [`natural-japanese-writing`](skills/natural-japanese-writing/) | Write or revise Japanese while preserving meaning, expertise, voice, and context. |
| [`perform-safely`](skills/perform-safely/) | Handle destructive, external, sensitive, or hard-to-reverse actions safely. |
| [`place-knowledges`](skills/place-knowledges/) | Decide where knowledge from a change belongs before editing artifacts. |
| [`research-answer`](skills/research-answer/) | Research and synthesize evidence-backed answers to current or contested questions. |
| [`shape-actionable-output`](skills/shape-actionable-output/) | Present multi-step work and guidance so the next action is clear. |
| [`test-design`](skills/test-design/) | Design and review tests around observable behavior and important boundaries. |
| [`write-commit-message`](skills/write-commit-message/) | Draft commit messages that explain a change's purpose and rationale. |
| [`writing-skills`](skills/writing-skills/) | Design, create, evaluate, or improve agent skills. |

## Install a skill

With the [`skills` CLI](https://github.com/vercel-labs/skills), install one skill with:

```sh
bunx skills add https://github.com/halqme/skills --skill <skill-name>
```

Replace `<skill-name>` with a directory name from the table above.

## Repository layout

Each skill lives in `skills/<skill-name>/` and has a `SKILL.md` file. Some skills also include `references/` for supporting material or `evals/` for evaluation examples.

## Provenance and license

This collection was extracted from [Pi Kit](https://github.com/halqme/pi-kit) and is maintained as a standalone set. The four `writing-skills/references/` guides are adapted from the Agent Skills documentation. Each identifies its source page, the [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) license, and its Markdown conversion. The local `best-practices.md` copy also notes that its closing “Next steps” section is not included. The `natural-japanese-writing` references list additional sources.

The Agent Skills [README](https://github.com/agentskills/agentskills#license) distinguishes CC BY 4.0-licensed documentation from Apache 2.0-licensed code. Its [contribution policy](https://github.com/agentskills/agentskills/blob/main/CONTRIBUTING.md#license) assigns CC BY 4.0 to documentation, and [`docs/LICENSE`](https://github.com/agentskills/agentskills/blob/main/docs/LICENSE) contains that license. These four upstream guides are documentation in `docs/skill-creation/`, so their source text is treated as CC BY 4.0 material; redistribution must meet that license's attribution and modification-notice conditions.

The original material in this repository, including the Pi Kit-derived skills, is licensed under the [Apache License 2.0](LICENSE). The four third-party guides in `skills/writing-skills/references/` are excluded from Apache 2.0 and remain separately licensed under CC BY 4.0, as noted in each file.
