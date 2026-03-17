# ParishPro Meta

This is the central documentation and project management hub for ParishPro.
If you are new to the project, start here before touching any code.

## What Is ParishPro

ParishPro is a free, open-source volunteer scheduling platform built for
Catholic parishes. It automates the process of scheduling ministers across
ministries and liturgies, replacing manual spreadsheet-based workflows with
a clean, role-based web application.

Licensed under AGPL v3 - free for any parish to self-host and configure.
Modifications must remain open source.

## Repository Structure

The ParishPro project is split across three repositories under the
[parishpro-app](https://github.com/parishpro-app) organization:

| Repo | Purpose |
|------|---------|
| [meta](https://github.com/parishpro-app/meta) | You are here - documentation, architecture, planning |
| [parishpro-web](https://github.com/parishpro-app/parishpro-web) | Frontend application |
| [parishpro-api](https://github.com/parishpro-app/parishpro-api) | Backend API |

This is a decoupled architecture. The frontend and backend are independent
deployments that communicate over HTTP. The backend is designed to be
internally modular, organized by domain (scheduling, auth, communications,
etc.) rather than by technical layer.

## Project Status

We are currently in the pre-development planning phase. No code is being
written yet. The following planning documents must be completed before
development begins:

- [ ] Research and select open source license
- [ ] Write Project Charter
- [ ] Write Use Case Document
- [ ] Write User Stories Backlog
- [ ] Write System Architecture Document
- [ ] Write Database Schema and Data Dictionary
- [ ] Write API Specification
- [ ] Write Scheduling Algorithm Specification
- [ ] Create UI/UX Wireframes
- [ ] Write Security Plan
- [ ] Write Test Plan

Track progress on the [Pre-Development Planning milestone](https://github.com/parishpro-app/meta/milestone/1).

## Documentation

Finalized planning documents live in the `/docs` folder of this repo:

| Document | Description |
|----------|-------------|
| Coming soon | Documents will be added as they are completed |

## Architecture Overview

ParishPro uses a decoupled architecture:

- **Frontend** - browser-based single page application
- **Backend** - stateless REST API, horizontally scalable
- **Deployment** - self-hosted via Docker

The tech stack is currently being evaluated. Decisions will be documented
in the System Architecture Document when finalized.

## How To Contribute

### Finding Work

All tasks are tracked on the [ParishPro Development project board](https://github.com/orgs/parishpro-app/projects/1).

- Issues labeled `good first issue` are ideal starting points
- Issues labeled `help wanted` are actively seeking contributors
- Filter by `frontend`, `backend`, `design`, or `documentation` to find
  work that matches your skills

### Workflow

1. Find an issue on the project board you want to work on
2. Comment on the issue to let others know you are picking it up
3. Fork the relevant repository
4. Create a branch named `issue-{number}-short-description`
5. Do the work
6. Submit a pull request referencing the issue number
7. A maintainer will review and merge

### Documentation Contributions

Planning documents are authored in Google Drive and converted to markdown
once finalized. If you want to contribute to a planning document, comment
on the relevant issue and the maintainer will share the working draft.

### Questions and Discussion

Join us on [Discord](https://discord.gg/DubATk2PKq) for project discussion,
questions, and coordination.

## Deployment

ParishPro is self-hosted. Parishes download the code and run it on their
own infrastructure. Docker support will be provided to make setup as
straightforward as possible. Detailed deployment documentation will be
added when the project reaches that stage.

## Maintainers

- [@destingollamudi](https://github.com/destingollamudi) - Project Lead

## License

[AGPL v3](LICENSE)
