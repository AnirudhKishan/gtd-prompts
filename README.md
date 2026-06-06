# GTD Copilot Workspace

Personal GTD system definition and coaching agents, powered by GitHub Copilot in VS Code.

## Setup

1. Clone this repo
2. Open the folder in VS Code
3. Make sure GitHub Copilot Chat is enabled

## Workstreams

| Workstream | Task App | Capture Sources |
|------------|----------|-----------------|
| **Work** | Microsoft To Do | Teams, Outlook |
| **Personal** | TickTick | WhatsApp, Gmail |

Lists (In, Overflow, Active Projects, Waiting-For, Maybe, Cold Storage) live in the task apps above — not in this repo.

## Agents

Select from the agent picker in Copilot Chat:

| Agent | What it does |
|-------|--------------|
| **GTD Review Buddy** | Walks you through the GTDv2 weekly review, one step at a time. Conversational coach — no task pasting required. |

## Docs

The GTD system definition lives in my Obsidian vault (single source of truth), under `50 Systems/Task Management/`:

| Note | Purpose |
|----------|---------|
| GTD System | Overview and index |
| GTD Principles | Core philosophy, principles, and design axioms |
| GTD Weekly Review | Lists, review steps, WIP limits, exit ramps |
| GTD Design Decisions | Decision log: why the system is shaped the way it is (alternatives considered, rationales) |
| GTD Backlog | Open improvements to the system |

## File structure

```
.github/
  agents/
    gtd-review.agent.md              # GTD Review Buddy (weekly review coach)
README.md                            # This file
```

The system definition now lives in the Obsidian vault under `50 Systems/Task Management/`.
