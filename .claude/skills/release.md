# /release

Prepare a new release of create-pr.

## Arguments

- `$ARGS` — the new version number (e.g. `0.11.0`). If not provided, ask the user.

## Instructions

1. Read the current version from `CREATE_PR_VERSION` in the `create-pr` file
2. If no version argument was provided, look at commits since the last release to suggest a version bump (breaking → major, feat → minor, fix → patch), then ask the user to confirm
3. Update `CREATE_PR_VERSION` in `create-pr` to the new version
4. Update `CHANGELOG.md`: add a new section for the version with a summary of commits since the last release (use `git log` to gather them)
5. Run `./build.sh` to generate `bin/create-pr` and `bin/checksum`
6. Run `lib/bashunit tests` to verify nothing is broken
7. Report the summary and remind the user to:
   - Commit the changes with `release: <version>`
   - Create a GitHub release at https://github.com/Chemaclass/create-pr/releases/new
   - Attach `bin/create-pr` and `bin/checksum` to the release
