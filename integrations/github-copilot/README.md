# GitHub Copilot Integration

The Agency works with GitHub Copilot out of the box. No conversion needed —
agents use the existing `.md` + YAML frontmatter format.

## Prerequisites

- [GitHub Copilot](https://github.com/features/copilot) subscription (Individual, Business, or Enterprise)
- [GitHub Copilot CLI](https://docs.github.com/en/copilot/github-copilot-in-the-cli/about-github-copilot-in-the-cli) **or** [VS Code](https://code.visualstudio.com/) / any JetBrains IDE with the Copilot extension

## Local Setup

### Step 1 — Clone the repo

```bash
git clone https://github.com/msitarzewski/agency-agents.git
cd agency-agents
```

### Step 2 — Install agents

```bash
./scripts/install.sh --tool copilot
```

This copies all agent `.md` files into `~/.github/agents/`.

### Step 3 — Confirm the install

```bash
ls ~/.github/agents | head
```

You should see files like `engineering-frontend-developer.md`,
`engineering-backend-architect.md`, etc.

### Step 4 — Activate an agent

Open a GitHub Copilot Chat session (VS Code, JetBrains, or CLI) and reference
any agent by name:

```
Use the Frontend Developer agent to review this React component.
```

```
Activate the Reality Checker and verify this feature is production-ready.
```

```
Use the Backend Architect agent to design a REST API for user authentication.
```

Copilot will load the matching agent's persona and instructions automatically.

## Manual Install (single category)

If you only want a specific division instead of the full roster:

```bash
mkdir -p ~/.github/agents
cp /path/to/agency-agents/engineering/*.md ~/.github/agents/
```

Replace `engineering` with any division folder (`design`, `marketing`,
`testing`, `sales`, etc.).

## Available Agent Divisions

| Division | Folder |
|---|---|
| Engineering | `engineering/` |
| Design | `design/` |
| Marketing | `marketing/` |
| Sales | `sales/` |
| Testing | `testing/` |
| Product | `product/` |
| Project Management | `project-management/` |
| Support | `support/` |
| Paid Media | `paid-media/` |
| Spatial Computing | `spatial-computing/` |
| Specialized | `specialized/` |

## Agent Directory

Agents are organized into divisions. See the [main README](../../README.md) for
the full current roster.
