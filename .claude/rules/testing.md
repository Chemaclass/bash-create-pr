# Testing rules

When writing or modifying tests:

- Test files go in `tests/unit/` mirroring `src/` structure
- E2E tests go in `tests/e2e/`
- Test function names: `function test_<module>_<behavior>()`
- Use `set_up()` for test setup (source files, export env vars)
- Available assertions: `assert_same`, `assert_equals`, `assert_not_equals`, `assert_contains`, `assert_not_contains`, `assert_empty`, `assert_not_empty`, `assert_exit_code`
- Data providers: add `# data_provider provider_name` comment above the test function, then define `function provider_name()` with `echo` lines for each test case
- Use `skip` to mark known-failing or WIP tests
- Run tests with `lib/bashunit tests` or `make test`
- Snapshot files go in `tests/unit/snapshots/`
- Always source the module under test in `set_up()` via `source "$CREATE_PR_ROOT_DIR/src/<module>.sh"`
