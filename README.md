# Figma Wireframes — Claude Code Skill

A [Claude Code](https://claude.ai/code) skill that creates or refines low-fidelity wireframes directly in Figma from a page-level brief. Focuses on structure, hierarchy, and user flows rather than visual design.

## What It Does

- Walks you through a 7-step guided intake to capture context, content, audience, and requirements
- Creates wireframes directly in Figma using Figma MCP tools
- Builds with components from your published design system library

## Requirements

- [Claude Code](https://claude.ai/code)
- [Figma MCP server](https://github.com/nichochar/figma-mcp) connected in Claude Code

## Installation

Copy the `.claude/skills/` folder into your project:

```bash
# Clone this repo
git clone https://github.com/hlee-lee/figma-wireframes.git

# Copy the skill into your project
cp -r figma-wireframes/.claude/skills/figma-wireframes your-project/.claude/skills/
```

Your project should look like:

```
your-project/
└── .claude/
    └── skills/
        └── figma-wireframes/
            └── SKILL.md
```

## Usage

In Claude Code:

```
/figma-wireframes [brief or screen request]
```

## License

MIT
