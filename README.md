# Agent Skills

## Skills

| Skill | Purpose |
| --- | --- |
| [`apply-correction`](skills/apply-correction/) | Revise an artifact from the authoritative current state after corrections or changed requirements. |
| [`cognitive-rhythm-writing`](skills/cognitive-rhythm-writing/) | Improve the progression of explanatory long-form prose without manufacturing drama. |
| [`diagnose-problem`](skills/diagnose-problem/) | Establish the evidence-backed cause of a failure, regression, or unexpected result. |
| [`natural-japanese-writing`](skills/natural-japanese-writing/) | Write or revise Japanese while preserving meaning, expertise, voice, and context. |
| [`perform-safely`](skills/perform-safely/) | Handle destructive, external, sensitive, or hard-to-reverse actions safely. |
| [`place-knowledges`](skills/place-knowledges/) | Decide where knowledge from a change belongs before editing artifacts. |
| [`research-answer`](skills/research-answer/) | Research and synthesize evidence-backed answers to current or contested questions. |
| [`shape-actionable-output`](skills/shape-actionable-output/) | Present multi-step work and guidance so the next action is clear. |
| [`simplify-change`](skills/simplify-change/) | Prefer the smallest conventional change that satisfies the requirements. |
| [`test-design`](skills/test-design/) | Design and review tests around observable behavior and important boundaries. |
| [`write-commit-message`](skills/write-commit-message/) | Draft commit messages that explain a change's purpose and rationale. |

## Install a skill

With the [`skills` CLI](https://github.com/vercel-labs/skills), install one skill with:

```sh
bunx skills add https://github.com/halqme/skills --skill <skill-name>
```

Replace `<skill-name>` with a directory name from the table above.

## Repository layout

Each skill lives in `skills/<skill-name>/` and has a `SKILL.md` file. Some skills also include `references/` for supporting material or `evals/` for evaluation examples.

## Provenance and license

This collection was extracted from [my personal Pi extensions packages](https://github.com/halqme/pi-kit/tree/v1) and is maintained as a standalone set. The `natural-japanese-writing` references list additional sources.

The original material in this repository, including the Pi Kit-derived skills, is licensed under the [Apache License 2.0](LICENSE).
