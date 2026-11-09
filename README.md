# HTML communication skill

Create polished, accessible static HTML explanations, reports, diagrams, prototypes, and similar artifacts using an offline gallery of 20 example structures.

## Install

For user-wide discovery by an Agent Skills-compatible tool, run:

```bash
mkdir -p ~/.agents/skills
git clone git@github.com:Sanjay-R/html-effectiveness.git \
  ~/.agents/skills/html-communication
```

For a project-only installation, run the same commands from your project directory, replacing `~/.agents/skills` with `.agents/skills`. Restart or reload your agent to discover the skill. Follow your tool's installation instructions if it uses another location; approve the project skill if your tool requires project trust. Remove or update any older skill with the same name: Pi keeps the first one it discovers.

## Use with an agent

Ask the agent, for example:

> Create a single-page interactive HTML explanation of this implementation plan.

For a file-aware agent without skill discovery, provide the path explicitly:

> Read `/path/to/html-communication-skill/SKILL.md` and follow its instructions. Create an interactive HTML explanation of this implementation plan.

To request a collection instead of the default single page:

> Create a linked multi-page HTML report covering the findings and recommendations.

Browse `templates/index.html` locally to see the gallery. Generated artifacts require no build system or remote assets.

## Source and updates

The templates originate from [html-effectiveness](https://github.com/ThariqS/html-effectiveness), licensed under Apache-2.0. See [UPSTREAM.md](UPSTREAM.md) for the snapshot and modifications. When updating, compare with the recorded upstream commit, retain copyright and license notices, update the commit reference, and validate the local gallery and skill instructions.