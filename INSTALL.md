# Installing ML Coach

> **Для людей:** этот файл написан для AI-агента. Просто отправь агенту фразу из [README](README.md#установка). Агент скачает репозиторий и скопирует одну папку со скиллом в нужное место, больше он ничего не запускает и не меняет.
>
> **For humans:** this file is meant for an AI agent. Just send your agent the phrase from the [README](README.en.md#install). It downloads the repo and copies one skill folder into place, nothing else is run or changed.

---

## Instructions for the agent

The user asked you to install the **ML Coach** skill from https://github.com/vincere-mori/ml-engineer-roadmap. It is a plain prompt skill: a `SKILL.md` file plus three markdown reference files. It contains no scripts.

Follow the steps for the agent you are. Tell the user what you are about to do before running commands. Talk to the user in their language.

### If you are Claude Code

Run in the shell:

```bash
claude plugin marketplace add vincere-mori/ml-engineer-roadmap
claude plugin install ml-roadmap@ml-engineer-roadmap
```

If the `claude` command is not available in the shell, use the fallback below with the target directory `~/.claude/skills/ml-coach`.

### If you are Codex

Use the fallback below with the target directory `~/.agents/skills/ml-coach`.

### Any other agent that supports `SKILL.md` skills

Use the fallback below with your own user-level skills directory. If you are not sure where it is, ask the user instead of guessing.

### Fallback: copy the skill folder

1. Clone the repo into a temporary directory:
   ```bash
   git clone --depth 1 https://github.com/vincere-mori/ml-engineer-roadmap.git <tmp>/ml-engineer-roadmap
   ```
   If `git` is not available, download these four files instead and keep the same folder structure:
   - `https://raw.githubusercontent.com/vincere-mori/ml-engineer-roadmap/main/plugins/ml-roadmap/skills/ml-coach/SKILL.md`
   - `https://raw.githubusercontent.com/vincere-mori/ml-engineer-roadmap/main/plugins/ml-roadmap/skills/ml-coach/references/roadmap.md`
   - `https://raw.githubusercontent.com/vincere-mori/ml-engineer-roadmap/main/plugins/ml-roadmap/skills/ml-coach/references/questions.md`
   - `https://raw.githubusercontent.com/vincere-mori/ml-engineer-roadmap/main/plugins/ml-roadmap/skills/ml-coach/references/interview.md`
2. Copy the folder `plugins/ml-roadmap/skills/ml-coach` to the target directory, so that the result is `<target>/SKILL.md` and `<target>/references/*.md`. Create parent directories if needed. On Windows `~` is the user profile folder (`%USERPROFILE%`).
3. If the target directory already exists, it is an older version of the skill: replace it.
4. Delete the temporary clone.

### After installing

Tell the user, in their language:

- the skill is installed and where;
- they may need to restart the agent session for it to show up;
- how to use it: just ask, for example "Check my ML level", "Run an ML system design mock interview, Middle level", "Quiz me on gradient boosting", "Make a study plan to get an internship by June". In Claude Code it can also be called with `/ml-roadmap:ml-coach`.

Do not start a session with the skill unless the user asks.
