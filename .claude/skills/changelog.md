# /changelog

Generate a changelog entry from recent commits.

## Instructions

1. Find the latest version tag or release commit using `git log --oneline --grep="release:"`
2. Gather all commits since that point with `git log --oneline`
3. Group commits by type (feat, fix, ref, docs, chore, test, etc.)
4. Format as a markdown changelog section following the existing style in `CHANGELOG.md`
5. Output the generated entry so the user can review it before adding to the file
