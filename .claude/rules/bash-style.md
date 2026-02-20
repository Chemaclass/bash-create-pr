# Bash coding style

When writing or modifying bash code in this project:

- Always start scripts with `#!/bin/bash` and `set -euo pipefail`
- Use `local` for all variables inside functions
- Use `declare -r` for constants
- Quote all variable expansions: `"$var"` not `$var`
- Use `$(command)` instead of backticks
- Use `[[ ]]` instead of `[ ]` for conditionals
- Use `printf` over `echo` for formatted output
- Namespace functions with file prefix: functions in `src/pr_title.sh` should be named `pr_title::*` or `pr_title`
- Use `readonly` or `declare -r` for constants that should not change
- Default values with `${VAR:-default}`
- Error output to stderr: `echo "error" >&2`
- Use `error_and_exit` helper for fatal errors (defined in `src/helpers.sh`)
