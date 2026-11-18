# Agent Skills

Reusable workflows for AI agents. Each skill has one source folder using the [Agent Skills standard](https://agentskills.io/specification).

| Skill | What it does |
|---|---|
| [Industrial Feasibility Study (طرح توجیهی)](skills/industrial-feasibility-study/SKILL.md) | Reviews, prepares, and updates industrial feasibility studies. It can assess investment, check financial assumptions, and prepare an investor brief. |

## Install a skill

Download or clone this collection. Copy the entire folder `skills/industrial-feasibility-study` into the skill directory used by your agent in the **project where you want to use it**. Keep `SKILL.md` and `references/` together.

| Agent | Project directory | Documentation |
|---|---|---|
| Codex | `.agents/skills/` | [Codex skills](https://learn.chatgpt.com/docs/build-skills) |
| Claude Code | `.claude/skills/` | [Claude Code skills](https://code.claude.com/docs/en/skills) |
| Cursor | `.cursor/skills/` | [Cursor skills](https://prod.cursor.com/docs/skills) |
| Gemini CLI | `.gemini/skills/` | [Gemini CLI skills](https://geminicli.com/docs/cli/skills/) |
| GitHub Copilot | `.github/skills/` | [GitHub Copilot skills](https://docs.github.com/en/copilot/concepts/customizations/agent-skills) |

The resulting path ends with `industrial-feasibility-study/SKILL.md`. Choose a single discovery path when one agent watches multiple paths. The optional `agents/openai.yaml` file supplies a display label in Codex. The workflow uses the Markdown files and relative references on every platform.

If your agent has no native skill loader, attach `SKILL.md`, the relevant files from `references/`, and any project input. Ask the agent to follow the workflow in `SKILL.md`. If the agent can read a workspace, you can give it those paths instead.

## Try it

> Use industrial-feasibility-study to review this feasibility report for an investor meeting. Reconcile the figures you can reproduce, flag the unclear assumptions, and prioritize questions with the evidence needed to answer each one.

ورودی می‌تواند گزارش موجود، فایل مدل مالی یا شرح اولیه طرح باشد. برای گزارش فارسی، درخواستت را فارسی بنویس و در صورت نیاز فرمت خروجی را مشخص کن.

The text workflow has no required plugin, API key, or script. PDF inspection, fresh research and spreadsheet generation depend on the host's tools. The skill specifies how to proceed when those tools are unavailable.

## Contribute

Keep each skill in its own `skills/<id>/` directory using the [Agent Skills specification](https://agentskills.io/specification). Update the catalogue above and include a short example prompt. In your pull request, state which agents you tried and what happened. Use synthetic or permission-cleared examples. Keep private reports, credentials, personal paths, and internal notes out of the public repository.

The collection is available under the [MIT License](LICENSE). Preserve the license notice when redistributing a skill.
