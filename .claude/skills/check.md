# /check

Run the full pre-commit validation suite (tests + static analysis + linting).

## Instructions

1. Run `make pre_commit/run` from the project root
2. This executes: tests → ShellCheck → editorconfig-checker
3. Report results for each step
4. If any step fails, identify the specific issues and suggest fixes
