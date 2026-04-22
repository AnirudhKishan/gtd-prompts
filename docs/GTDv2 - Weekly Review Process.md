# GTDv2 --- Weekly Review Process

Operationalizes: "GTDv2 - Philosophies, Rationales and Principles.md"

Goal: maintain a trustworthy attention system with minimal cognitive
load.

------------------------------------------------------------------------

# Lists

    In
    Overflow
    Active Projects
    Waiting-For
    Maybe
    Cold Storage

## Meaning of Lists

**In** → capture bucket, unclarified inputs

**Overflow** → projects that want to be Active this cycle but are blocked only by the WIP cap. Same appetite as Active; only capacity differs. Soft target ~10. No next actions.

**Active Projects** → projects I have chosen to drive this cycle. Hard cap ≤ 5. Only list that earns next actions.

**Waiting-For** → projects blocked on external input (a reply, a decision, someone else's work). No next actions — the ball is not in my court.

**Maybe** → not on radar this cycle. Covers both fresh ideas and projects I have stepped back from. Includes "if time permits" items. Soft target ~25; push stale items to Cold Storage when noisy.

**Cold Storage** → ideas I don't want to delete but don't want to see. Archive. Uncapped.

------------------------------------------------------------------------

# Key Design Decisions

## 1. Single Commitment Boundary

Only **Active Projects** implies a current-cycle commitment to drive.

Crossing this boundary means:

-   project consumes WIP capacity (of 5)
-   project may receive next actions

Invariant:

> No Active Project → No Next Action

Overflow, Waiting-For, Maybe, and Cold Storage are all safe parking zones — none earns next actions.

## 2. Capacity and Appetite Are Separate

Overflow exists because appetite (wanting to drive) and capacity (slot in Active) are distinct. When appetite exceeds capacity, the excess belongs in Overflow, not Maybe. Forcing accountable projects into Maybe is what causes Active to drift into a wishlist.

Membership test for Overflow: *"Would I take an Active slot for this right now if one opened?"* — yes only. "If time permits" items do not belong in Overflow; they belong in Maybe.

## 3. One Maybe List, Not Many

Previous versions used multiple horizon lists (Review Cycle / Month /
Year / Someday) to manage attention distance. This created graduated
classification decisions on every item during review — the primary
source of friction.

**Cold Storage** — not more horizons — is the right noise filter.
When Maybe feels long, push items you don't want to see to Cold Storage.
This is a binary "do I want to keep seeing this?" decision, not a
distance judgment.

## 4. The Recurring 4-Way Question

A single question governs any transition out of Active or out of Waiting-For:

> "What should happen to this now?"

- Still wants Active, just squeezed out / re-opened → **Overflow**
- Blocked on someone or something external → **Waiting-For**
- No longer on radar this cycle → **Maybe**
- Done / obsolete → **delete**

No default. The same four outcomes apply whether the trigger is deactivation, a swap, or a Waiting-For item becoming unblocked. The recurring pattern is intentional — it keeps the system legible.

## 5. Local Decisions During Review

Each step asks one simple question. Do not compare across lists —
except in Step 5b, where starred items may be weighed against Active
Projects for swaps.

## 6. Activation Decisions Are Isolated

Promotion to **Active Projects** happens only in Step 5.

Purpose:

-   prevent earlier steps from becoming global prioritization
-   keep most review decisions local and mechanical

## 7. Dead Items Are Deleted

Dead means deleted from the system entirely.

Cold Storage is for items that are **not dead** but that you don't want
to see. Items that are truly done, cancelled, or irrelevant are removed.

------------------------------------------------------------------------

# Weekly Review

Steps 1, 2, and 5a are essential.\
Steps 3, 4, 5b, and 6 are skippable.

If In is empty, Active already reflects reality, and Active is already at cap, the review can be two minutes.

------------------------------------------------------------------------

## Step 1 --- Empty In (essential)

Goal: empty capture.

For each item in In, ask: **"What is this?"**

Trash → delete\
Reference → file it\
Blocked on someone/something external → **Waiting-For**\
Already driving it this cycle and Active has room (< 5) → **Active Projects**\
Want to drive it this cycle but Active is full → **Overflow**\
Everything else → **Maybe**

Default is **Maybe**. Direct placement in Active, Overflow, or Waiting-For is allowed when the answer is obvious — not to force classification.

No next actions here. No deliberation. Just park it.

------------------------------------------------------------------------

## Step 2 --- Gut-Check Active and Overflow (essential)

Cap: Active Projects ≤ 5. Overflow soft target ~10.

Walk Active Projects first. For each project, ask: **"Am I still driving this?"**

Yes → keep\
No → apply the **4-way question**:
  - Still wants Active, just squeezed out → **Overflow**
  - Blocked on external → **Waiting-For**
  - Not on radar this cycle → **Maybe**
  - Dead → **delete from the system**

If a project moves out of Active, clear its next actions (the invariant requires it).

Then walk Overflow. For each project, ask: **"Does this still want Active this cycle?"**

Yes → keep in Overflow\
No → apply the 4-way question (minus Overflow as a destination, since it's already leaving).

Don't deliberate. If you hesitate, keep it. You can drop it next week.

------------------------------------------------------------------------

## Step 3 --- Waiting-For Skim (skippable)

Goal: detect unblocks and stale waits.

This step is not individual-item deliberation — it's pattern recognition across external state. Before starting, check inboxes and threads for replies, decisions, or external movements.

For each Waiting-For item, ask: **"Is this still actually waiting?"**

Still blocked → leave it\
Unblocked → apply the **4-way question**:
  - Ready to drive and Active has room → **Active Projects**
  - Ready to drive but Active is full → **Overflow**
  - No longer want to drive this cycle → **Maybe**
  - Dead / obsolete → **delete**

Also watch for items that have been waiting too long and need a chase.

------------------------------------------------------------------------

## Step 4 --- Skim Maybe (skippable)

**Don't review every item.** Skim the list.

Three questions:

1.  "Anything here that's dead?" → **delete from the system**
2.  "Anything I don't want to see but it's not dead?" → **Cold Storage**
3.  "Anything here that's calling to me?" → **star / flag it** for Step 5b

If nothing jumps out, move on.

------------------------------------------------------------------------

## Step 5 --- Activate

Step 5 has two phases. 5a is essential whenever Active < 5; 5b is skippable.

### Step 5a --- Refill Active from Overflow (essential when Active < 5)

If Active is below cap, fill it — this is the whole point of Overflow.

Pull from Overflow first. For each slot available, ask: **"Which of these is ready to drive now?"**

Move chosen items to Active. This is mechanical, not deliberative — Overflow items have already passed the appetite test.

If Overflow is empty and slots remain, starred Maybe items from Step 4 may fill them.

If no starred items exist and slots still remain, leave Active below cap. Capacity is not obligation.

### Step 5b --- Swap (skippable)

Only if Active is at cap and you starred something in Step 4 that feels hotter than something currently Active.

For each starred item, ask: **"Do I want to commit to this right now, at the cost of displacing something Active?"**

Activation should feel like **"finally"** not "maybe."
Not sure → leave it in Maybe. It will be there next week.

If yes: swap. Apply the **4-way question** to the displaced Active item:
  - Still wants Active → **Overflow**
  - Blocked externally → **Waiting-For**
  - No longer on radar this cycle → **Maybe**
  - Dead → **delete**

This is the one moment in the review where comparing across lists is appropriate.

After activation decisions, **clear the stars/flags** on any items staying in Maybe. Stars are temporary markers for this step only — they should not carry over to next week.

------------------------------------------------------------------------

## Step 6 --- Cold Storage Skim (quarterly, or whenever curiosity strikes)

There is no schedule for this step. It exists only if you want it.

> "Anything worth reviving?"

Move to Maybe if yes. Otherwise ignore.

------------------------------------------------------------------------

# Exit Ramps

-   Steps 1, 2, and 5a are essential. Steps 3, 4, 5b, and 6 are skippable.
-   If you only complete Steps 1 and 2, you have done a useful review.
-   Completion is optional. Safety is required.

------------------------------------------------------------------------

# WIP Limits

Active Projects ≤ 5 (hard cap)\
Overflow → soft target ~10 (if larger, appetite is probably inflated — some items are really Maybe)\
Waiting-For → uncapped (but skim for stale waits)\
Maybe → soft target ~25 (push stale items to Cold Storage when noisy)\
Cold Storage → uncapped

------------------------------------------------------------------------

# Migration from Previous System

1.  Previous Active (≤ 10) splits into new Active (≤ 5) + Overflow.
    For each previous Active item, ask the membership question:
    -   Currently driving this cycle → stays in new **Active** (up to 5)
    -   Wants Active but didn't make the cut → **Overflow**
    -   Blocked externally → **Waiting-For**
    -   Not really on radar this cycle → **Maybe**
2.  Previous Maybe stays in Maybe. No re-sorting needed.
3.  Previous Cold Storage stays in Cold Storage.
4.  Create the new **Overflow** and **Waiting-For** lists in the task app.
5.  Strip next actions from anything that is not now in Active.
