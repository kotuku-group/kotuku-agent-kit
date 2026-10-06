# Kōtuku Agent Kit

This kit makes it easy to add AI agent support to any project that depends on Tiri and the Kōtuku framework for development. The alternative method is to checkout the Kōtuku repository and then store your project(s) in a `projects` sub-folder of the main repo. Either strategy will work well, but the latter adds substantial overhead that may be excessive, hence the need for this kit.

## Repository installation

From the root of your project folder, mount this repository at `.agents` so Codex and Claude discover `.agents/skills` automatically:

```bash
git submodule add https://github.com/kotuku-group/kotuku-agent-kit.git .agents
git submodule update --init
mkdir -p .claude && ln -s ../.agents/skills .claude/skills
```

## Included skills

- `tiri-programming`: Tiri syntax, semantics, conventions, execution, and an on-demand reference manual.
- `flute-testing`: Flute test design, registration, execution, and coverage guidance.
- `kotuku-api`: On-demand generated Kōtuku module and class API documentation.

## Documentation sources

On first use, `tiri-programming` and `kotuku-api` download the exact commit declared by each source file. Downloaded directories are ignored by Git; `.source.json` files record their provenance, and a cache is replaced automatically when it does not match the configured repository, path, and revision. To publish a documentation update, change the relevant pinned revision, validate the kit, and increment the plugin version.

Validate the bundle after changing it:

```bash
origo scripts/verify_kit.tiri --log-warning
```

## Plugin use

The `.codex-plugin/plugin.json` manifest makes this repository installable as a Codex plugin. Repository submodules remain the preferred installation for projects that need a reviewable, project-pinned documentation version.
