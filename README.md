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

The GTD system definition lives in `docs/`:

| Document | Purpose |
|----------|---------|
| GTDv2 - Philosophies, Rationales and Principles | Core philosophy, principles, and design axioms |
| GTDv2 - Weekly Review Process | Lists, review steps, WIP limits, exit ramps |
| GTDv2 - Design Decisions | Decision log: why the system is shaped the way it is (alternatives considered, rationales) |

## File structure

```
.github/
  agents/
    gtd-review.agent.md              # GTD Review Buddy (weekly review coach)
docs/
  GTDv2 - Philosophies, ...md        # System principles
  GTDv2 - Weekly Review Process.md   # Review process definition
  GTDv2 - Design Decisions.md        # Decision log / rationale
README.md                            # This file
```
