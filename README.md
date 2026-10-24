# Git Discipline

A reusable Git workflow template for teams: branch naming, Conventional Commits, pull-request checks, and local hooks across different language stacks.

## What is included

- GitHub Actions for branch naming, commit/PR-title conventions, CI, and a deployment example.
- Lefthook configuration and shell validators for local feedback.
- A documented main/develop workflow, short-lived branches, squash merges, and releases.
- Project-owned CI and deployment entry points in `.ci/`.

## Adopt it in a project

1. Follow the [setup playbook](SETUP-PLAYBOOK.md) to copy the workflow files into your project.
2. Install Lefthook and run `lefthook install`.
3. Replace the example commands in [`.ci/commands.sh`](.ci/commands.sh) and [`.ci/deploy.sh`](.ci/deploy.sh) with your actual build, test, and deployment commands.
4. Configure branch protections and required reviews/checks in GitHub. Copying the files does not enable repository settings automatically.

## Workflow at a glance

Create `feature/`, `fix/`, or `chore/` branches from develop; use `hotfix/` from main for urgent fixes. Write Conventional Commits and open a pull request. The [contribution guide](CONTRIBUTING.md) defines review and merge requirements.

| Document | Purpose |
| --- | --- |
| [Git discipline](GIT-DISCIPLINE.md) | Branch, commit, review, and release policy |
| [Setup playbook](SETUP-PLAYBOOK.md) | Install the template and configure enforcement |
| [Contributing](CONTRIBUTING.md) | Make changes to this repository |

The scripts are a starting point for a team's process. Supply your own stack-specific checks and deployment credentials.
