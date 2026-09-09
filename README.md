# Kōtuku Agent Kit

This kit makes it easy to add AI agent support to any project that depends on Tiri and the Kōtuku framework for
development. The alternative method is to checkout the Kōtuku repository and then store your project(s) in a
`projects` sub-folder of the main repo. Although this will work well, it adds substantial overhead that may be
excessive, hence the need for this kit.

## Repository installation

Mount this repository at `.agents` so Codex discovers `.agents/skills` automatically:

```bash
git submodule add https://github.com/kotuku-group/kotuku-agent-kit.git .agents
git submodule update --init
```

Keep project-specific build, test, and deployment rules in the consuming repository's `AGENTS.md`. The reusable
Tiri and Kōtuku guidance belongs here.

## Included skills

- `tiri-programming`: Tiri syntax, semantics, conventions, execution, and an on-demand reference manual.
- `flute-testing`: Flute test design, registration, execution, and coverage guidance.
- `kotuku-api`: On-demand generated Kōtuku module and class API documentation.

## Documentation sources

The skills are authored and maintained in this repository. They are not copied or generated from the Kōtuku SDK.

On first use, `tiri-programming` and `kotuku-api` check for their respective documentation and download it from the
repository declared by each skill. Downloaded directories are ignored by Git and their exact source revisions are
recorded locally.

The focused wiki guides remain a bundled snapshot whose source revision is recorded in `versions.json`. Refresh it
from a committed Kōtuku wiki tree with:

```bash
origo scripts/sync_references.tiri sdk=/path/to/kotuku --log-warning
```

The synchronization script exports Git `HEAD`, so uncommitted working-copy changes are never included. It does not
modify any skill instructions or downloaded documentation.

Validate the bundle after changing it:

```bash
origo scripts/verify_kit.tiri --log-warning
```

## Plugin use

The `.codex-plugin/plugin.json` manifest makes this repository installable as a Codex plugin. Repository submodules
remain the preferred installation for projects that need a reviewable, project-pinned documentation version.
