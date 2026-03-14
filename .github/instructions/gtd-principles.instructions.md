---
description: "Use when processing GTD inbox items, clarifying tasks, organizing projects into lists, or reviewing active projects and someday/maybe tiers"
---
# GTD Principles

## Core Philosophy

- **Clarify and Organize are separate steps.** Clarify turns raw inbox items into well-defined tasks. Organize routes them to the right lists. Doing both at once is overwhelming — always keep them apart.
- **Capture everything, decide later.** The inbox is a dumping ground. No filtering at capture time.
- **One inbox item at a time.** During clarify, process items sequentially. No batching, no skipping ahead.
- **Verb-first tasks.** Every task starts with an action verb. "Buy groceries" not "Groceries."
- **Caps keep the system honest.** Hard limits on active lists prevent overcommitment.

## Workstreams

Two fully separate workstreams. Each has its own complete set of lists.

| Workstream | Task App | Capture Sources |
|------------|----------|-----------------|
| **Work** | Microsoft To Do | Teams, Outlook |
| **Personal** | TickTick | WhatsApp, Gmail |

When the user doesn't specify a workstream, ask once before producing output.

## Lists (per workstream)

### Action lists
| List | Purpose | Cap |
|------|---------|-----|
| **In** | Raw captured items, unprocessed | — |
| **Active Projects** | Projects with a defined next action, actively being worked | 10 |
| **Waiting For** | Delegated or blocked — waiting on someone/something | — |
| **Calendar** | Date-specific actions or events | — |

### Non-action lists
| List | Purpose | Cap |
|------|---------|-----|
| **Reference** | Information to file, not act on | — |
| **Incubation** | Ideas that need to ruminate — not ready for action yet | — |

### Someday/Maybe tiers (closest → furthest)
| List | Purpose | Cap |
|------|---------|-----|
| **This week, maybe** | Might do this week | 10 |
| **This month, maybe** | Might do this month | 10 |
| **This year, maybe** | Might do this year | 10 |
| **Someday, maybe** | No timeline, just an idea worth keeping | — |

## Routing rules

During **Clarify**, classify each inbox item as one of:
- **Actionable** → will become a task (title + optional steps + optional notes)
- **Trash** → delete
- **Reference** → file it
- **Calendar** → date-specific, goes to calendar
- **Waiting For** → blocked on someone/something
- **Incubation** → needs to ruminate, not ready for action

During **Organize**, route actionable items:
1. If it fits in Active Projects (under cap) → add it
2. If Active Projects is full → propose what to demote or combine, then distribute overflow to someday/maybe tiers (respecting their caps, nearest tier first)

## Review cycle

- **Review cycle length:** Weekly
- **Daily scan:** Quick check of today's tasks and calendar. Flag blockers and stale items.
- **Weekly review:** Full pass through all lists for a workstream. Inbox zero check, project relevance, promote/demote across someday/maybe tiers, waiting-for follow-ups, incubation check, enforce all caps.

## Output format

- All task output is **copy-paste ready** — each piece in its own fenced code block for easy copying.
- Label the target app in output: `→ To Do` or `→ TickTick`.
- Group output by destination list when routing multiple items.
