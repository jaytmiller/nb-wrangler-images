# AGENTS.md

## Project

nb-wrangler-images defines and archives nb-wrangler specs and image assets used to
build images based on nb-wrangler defined environments.  Its purpose is to store
and act on nb-wrangler image definitions so it stores required inputs materials
and the GitHub Actions needed to curate or reinstall wrangler specs and produce
images on GHCR as a product.

Primary tooling: nb-wrangler tool and dependencies relatd to installing and testing
mamba/pip environments and orchestrating image builds and testing:

- nb-wrangler
- uv
- pip
- mamba
- micromamba
- C/C++ compiler chain, others as needed,
- Docker
- git
- make

## Non-negotiable rules

- Never read, print, commit, or modify secrets, `.env`, credentials, or private keys.
- Do not edit generated files: `dist/`, `build/`, `coverage/`, `docs/_build/`.
- Do not run destructive Docker commands (`docker system prune`, volume removal,
  compose down -v) without explicit approval.
- Preserve CPU-only execution unless a task explicitly requires GPU support.

## Commands

TBD - Makefile

## Architecture

- specs/<mission or e.g. webbinar>/nb-wrangler specs
- assets/<mission or e.g. webbinar>/small aux files for images
- .github/worklfows   image build and maintenance pipelines

## Change requirements

- Make the smallest change that solves the requested problem.
- Keep functions and methods simple and target SLOC within ~ 20 lines.
- Use nb-wrangler's nbw tool to accomplish relatd tasks in pipelines where supported.
- Ask before changing public APIs.

## Documentation
- README.md
- documentation under docs/
