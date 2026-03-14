# GTD Copilot Workspace

Personal GTD workflow powered by GitHub Copilot prompts in VS Code. Clarify inbox items, organize them into lists, and run reviews — all through chat.

## Setup

1. Clone this repo
2. Open the folder in VS Code
3. Make sure GitHub Copilot Chat is enabled

## Workstreams

| Workstream | Task App | Capture Sources |
|------------|----------|-----------------|
| **Work** | Microsoft To Do | Teams, Outlook |
| **Personal** | TickTick | WhatsApp, Gmail |

Each workstream has its own full set of GTD lists. Prompts ask which workstream you're working in (or infer from context).

## Prompts

Type `/` in Copilot Chat to access these:

| Prompt | When to use |
|--------|-------------|
| `/clarify` | Process one inbox item into an actionable task |
| `/organize` | Route clarified items to the right lists, enforce caps |
| `/review` | Daily scan or full weekly review |

### Typical flow

1. **Clarify** — Run `/clarify` for each item in your inbox. One at a time.
2. **Organize** — Run `/organize` with your clarified items + current Active Projects list.
3. **Review** — Run `/review` for a daily check-in or full weekly review.

## Sync

This is a git repo. To stay in sync across machines:

- `git pull` before starting a GTD session
- `git commit` + `git push` after making changes to prompts or principles

## File structure

```
.github/
  instructions/
    gtd-principles.instructions.md   # Your GTD system definition (read by Copilot)
  prompts/
    clarify.prompt.md                 # /clarify
    organize.prompt.md                # /organize
    review.prompt.md                  # /review
README.md                            # This file (read by you)
```
