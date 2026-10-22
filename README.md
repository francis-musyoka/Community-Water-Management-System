# Community Water Management System — Documentation

Business requirements and workflows for a multi-organization water management platform. It serves community water schemes, county governments, water service providers, and property managers that supply water and bill customers by meter.

Kituasi Project is used throughout as a worked example only. Rules that differ between organizations, such as tariffs, penalties, and disconnection, are documented as organization settings.

## Where to start

- [Home](docs/index.md): purpose, who the platform serves, main capabilities
- [Requirements overview](docs/requirements/overview.md): platform structure, organization types, roles, and links to every requirement area
- [Workflows](docs/workflows/): step-by-step processes such as onboarding, registration, meter reading, and payments
- [System architecture](docs/architecture/system-architecture.md): technical decisions still open

## Repository layout

```text
docs/
  index.md          Home page
  requirements/     Capabilities and business rules (numbered requirements)
  workflows/        Processes from the user's point of view
  architecture/     Technical design decisions
  development/      Setup and maintenance instructions
mkdocs.yml          Site configuration and navigation
```

## Preview the documentation site

The docs are built with [MkDocs Material](https://squidfunk.github.io/mkdocs-material/).

```bash
python3 -m venv ~/.venvs/mkdocs
~/.venvs/mkdocs/bin/pip install -r requirements.txt
~/.venvs/mkdocs/bin/mkdocs serve
```

Then open `http://127.0.0.1:8000`. To build a static site into `site/` (not committed):

```bash
~/.venvs/mkdocs/bin/mkdocs build --strict
```

## Contributing

- Each requirement page ends with **Questions to confirm**. Answering these is the most useful contribution.
- When a question is answered, move the answer into the page and remove the question.
- Add new pages to the `nav` section of `mkdocs.yml`.
- Do not add passwords, API keys, M-Pesa credentials, or real customer data.
