# Sync Skills

Fetch the latest skill files from each source repo on GitHub and update this repo.

For each skill below, fetch the SKILL.md and all files inside references/ using the GitHub API (via `gh api`), then overwrite the local copies in this repo. Commit the changes with a message listing which skills were updated and what changed.

## Sources

| Skill | Repo | Path |
|-------|------|------|
| rem-cli | github.com/BRO3886/rem | `skills/rem-cli/` |
| ical-cli | github.com/BRO3886/ical | `skills/cal-cli/` |
| healthsync | github.com/BRO3886/healthsync | `cmd/skills/healthsync/` |

## Steps

1. For each skill, use `gh api repos/BRO3886/<repo>/contents/<path>/SKILL.md` to fetch SKILL.md (decode base64 content field)
2. List files under `references/` using `gh api repos/BRO3886/<repo>/contents/<path>/references` and fetch each one
3. Overwrite the local files in `<skill-name>/SKILL.md` and `<skill-name>/references/<file>`
4. Show a diff of what changed
5. Commit with message: `chore: sync skills from upstream (<skill> vX.Y.Z, ...)`
