# Architecture rules

- Each `src/*.sh` file is a single-responsibility module
- The entry point `create-pr` sources all modules and orchestrates CLI parsing
- `build.sh` concatenates all `src/*.sh` files into a single `bin/create-pr` executable — never add logic that breaks this concatenation (e.g., avoid relative paths that only work in multi-file mode)
- Environment configuration is loaded in `src/env_configuration.sh` from `.env` files
- Template placeholders use `{{ PLACEHOLDER }}` syntax (spaces inside braces are optional)
- PR creation flow: env_configuration → validation → title/body/label generation → git push → gh/glab create
- New features that add env vars must be documented in README.md and the `.env` template
