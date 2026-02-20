# Test Runner Agent

Run the project test suite and report results.

## Tools

Bash, Read, Grep

## Instructions

1. Run the full test suite with `lib/bashunit tests` from the project root `/Users/chema/Code/Chemaclass/create-pr`
2. If tests fail, read the failing test file and the corresponding source file to understand the failure
3. Report which tests passed and which failed, with clear failure details
4. If asked to run static analysis, also run `make sa` (ShellCheck)
5. If asked to run linting, also run `make lint` (editorconfig-checker)
6. If asked to run everything, run `make pre_commit/run`
