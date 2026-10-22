# Local development setup

## Status

**To be completed once the implementation stack and repository are known.** The project requirements PDF does not specify application dependencies or runtime requirements.

## Preview this documentation locally

If MkDocs Material is installed in the shared virtual environment at `~/.venvs/mkdocs`, run these commands from the root of this documentation project:

```bash
~/.venvs/mkdocs/bin/mkdocs serve
```

Then open `http://127.0.0.1:8000` in a browser. MkDocs reloads the preview when Markdown files are changed.

## Build the documentation site

```bash
~/.venvs/mkdocs/bin/mkdocs build
```

The generated static site is written to the `site/` directory by default.

## Application setup details to add

- Required language and runtime versions
- Dependency installation commands
- Environment variables and example configuration
- Database creation and migrations
- Development server and test commands
- Seed data and test accounts
- Deployment procedure

Do not add real passwords, API keys, M-Pesa secrets, or other credentials to the documentation repository.
