# GTDv2 — Design Decisions

This document preserves the reasoning that produced the current GTDv2 list structure and review process. It is ADR-lite: one section per decision, capturing the problem, alternatives considered, choice, and rationale.

For the *what* (current system state), see:
- `GTDv2 - Philosophies, Rationales and Principles.md`
- `GTDv2 - Weekly Review Process.md`

This document is the *why*.

---

## Context

The previous system had four lists: **In**, **Active Projects**, **Maybe**, **Cold Storage**. Active Projects was defined as *"projects I am willing to carry mentally right now,"* WIP-capped at 10.

In practice, the label drifted. Active Projects became an aspirational top-10 list — a wishlist of things I'd *like* to be working on — rather than a description of what I was actually driving. Two coupled problems emerged:

1. **Dishonest label.** Items sat in Active without real engagement. The list stopped being trustworthy, which violates the non-negotiable *"I trust my system."*
2. **Arbitrary cap.** A 10-slot limit forced genuine accountabilities into Maybe, where they didn't belong. The system became incomplete as well as aspirational.

Root diagnosis: **Active Projects was doing two jobs at once** — it was both the *commitment boundary* (gates next actions) and the *WIP limiter* (manages cognitive load). Those two jobs legitimately need different sizing.

---

## Decisions

### D1. Split accountability from driving

**Problem:** One list cannot simultaneously be honest about everything I'm accountable for *and* be short enough to WIP-limit.

**Options considered:**
- **(A) Tag-based:** Keep one list, uncap it, use a `#focus` tag for the driving subset. Only tagged items earn next actions.
- **(B) New list upstream of Active:** Accountability list above Active; Active stays WIP-limited and earns next actions.
- **(C) New list downstream of Active:** Active stays aspirational; a new smaller list captures the driving subset.

**Chose: (B).**

**Rationale:** Tags rot more easily than list membership; (A) relies on discipline at every touch. (C) keeps the dishonest "Active = aspirational" label. (B) makes each list mean exactly one thing and keeps "Active" meaning the WIP-limited, next-action-bearing set — matching existing muscle memory.

---

### D2. Name the upstream list "Overflow"

**Problem:** What do we call the new list?

**Options considered:**
- **Commitments** — honest but falsely implies Active isn't a commitment (it is).
- **Roster** — neutral; sits alongside Active well; feels flat.
- **On Radar / Radar** — matches the framing "on radar this cycle"; slightly informal.
- **Carrying** — matches old Principle 5 language; awkward as a noun.
- **Watchlist / Standing Projects / Docket** — flavor variants of the above.
- **Overflow** — names the capacity constraint directly.

**Chose: Overflow.**

**Rationale:** The *reason* this list exists is that Active has a hard cap. Naming it after that constraint (a) makes the cap feel real every time you look at it, (b) is descriptive rather than pejorative (think "overflow parking," not "leftovers"), and (c) reinforces the WIP discipline. Roster was runner-up but flatter — it doesn't name the axis that distinguishes the list from Active.

**Rejected earlier but worth noting:** "Overflow" was initially rejected on psychological-safety grounds (sounded like a dumping ground). Revisiting, the concern was overblown: overflow is capacity language, not moral judgment.

---

### D3. Tightened Overflow definition — capacity, not accountability

**Problem:** Early framing had Overflow as "things I'm carrying but not driving." That admits too much: it would absorb "if time permits" items, paused projects, and passive accountabilities. Overflow would have become the new aspirational graveyard one level down.

**Decision:** Overflow membership requires both:
1. **Appetite** — I want to drive this this cycle.
2. **Blocked only by the cap** — if a slot opened, I'd take it.

Without (2), it's Maybe. Without (1), it's Maybe or Waiting-For. Accountability alone does not earn Overflow.

**Rationale:** The distinguishing axis between Active and Overflow is **capacity**, not accountability or effort. Both lists have the same appetite; Overflow is simply the queue. This keeps Overflow small (soft target ~10) and honest.

**Consequence:** The earlier intake rule ("already accountable → Overflow") was revised. New rule: default to Maybe; Overflow only when the item both wants Active and is blocked by the cap.

---

### D4. Waiting-For as a formal list

**Problem:** Under the tightened Overflow definition, projects blocked on external input have nowhere coherent to live. They're not being driven (so not Active), they don't want to be driven right now (so not Overflow — the ball isn't in my court), and Maybe is wrong (I haven't stepped back; I'm just waiting).

**Decision:** Add **Waiting-For** as an explicit list. Standard GTD category, now formally in the system.

**Rationale:** Conflating Waiting-For with Maybe loses the unblock signal. Waiting-For has its own review cadence (pattern-recognition across external state, not per-item deliberation) which is why it earns its own step in the review.

---

### D5. The 4-way deactivation question, with no default

**Problem:** When a project leaves Active, where does it go?

**Options considered:**
- Always → Maybe (previous system).
- Always → Overflow (assume still on radar).
- Three-way with Overflow default.
- 4-way with no default.

**Chose: 4-way, no default.**

> "What should happen to this now?"
> - Still wants Active, squeezed out → **Overflow**
> - Blocked externally → **Waiting-For**
> - Not on radar this cycle → **Maybe**
> - Dead → **delete**

**Rationale:** Defaulting to Overflow re-creates the original problem one layer down — Overflow becomes a wishlist. Defaulting to Maybe is dishonest when the project really is still competing for a slot. The four outcomes are genuinely distinct; the question has to be asked each time. The cost is one question per deactivation, which is low.

---

### D6. Recurring 4-way pattern for unblocking too

**Problem:** When a Waiting-For item becomes unblocked, where does it go?

**Decision:** Apply the **same 4-way question**. Ready to drive + Active has room → Active. Ready to drive + Active full → Overflow. No longer want this cycle → Maybe. Obsolete → delete.

**Rationale:** Reusing the same question for both deactivation and unblocking is a good code smell — it signals the mental model is coherent. One pattern, multiple triggers. Easier to internalize, easier to coach.

---

### D7. Active cap = 5 (down from 10), Overflow soft target ~10

**Problem:** With Overflow absorbing the "wants Active but didn't make the cut" items, the Active cap should reflect genuine driving capacity, not a padded ceiling.

**Decision:** Active ≤ 5 (hard cap). Overflow soft target ~10.

**Rationale:** 10 was the old "aspirational" cap. The actual number of projects a person can genuinely drive in parallel is smaller — 5 is tight but honest. Overflow at ~10 means if you have more than ~15 projects *actively competing for driving capacity*, either the cap is too tight or your appetite is inflated (some Overflow items are really Maybe in disguise). Either way it's a useful signal.

---

### D8. Step 5 split — mandatory refill + skippable swap

**Problem:** With Active dropping to 5 and Step 2 likely to shrink it further during gut-check, Active will often end the review below cap. That's fine — unless the user's intent was to be at cap. The old single Step 4 conflated "refill an empty slot" (low-deliberation) with "swap a current driver for a hotter item" (high-deliberation).

**Decision:** Split into:
- **Step 5a — Refill** (essential when Active < 5). Pull from Overflow first, then starred Maybe. Mechanical.
- **Step 5b — Swap** (skippable). Compare starred Maybe against Active. High-deliberation.

**Rationale:** Refilling from Overflow is not a heavy decision — Overflow items have already passed the appetite test in D3. Swapping, by contrast, requires displacing a current driver. Separating them lets the essential part stay light and the optional part keep its exit ramp.

---

### D9. Overflow-first activation (not equal weighting with starred Maybe)

**Problem:** When Active has room and both Overflow items and starred Maybe items want in, who goes first?

**Decision:** **Overflow first**, starred Maybe fills remaining slots only if Overflow is exhausted.

**Rationale:** Overflow is the queue — items have waited their turn for capacity. Starred Maybe is the "surprise candidate." Letting Maybe jump the queue would undermine the purpose of Overflow.

---

### D10. Maybe retains its name; no rename

**Problem:** Under the new shape, Maybe holds two kinds of items: fresh ideas that haven't been committed to, and previously-committed items that are no longer on radar. Does "Maybe" still fit?

**Options considered:** Parked, Backburner, Shelf, Later, Incubator.

**Chose: Keep "Maybe".**

**Rationale:** (a) Classical GTD vocabulary has value — familiar, professional. (b) Every alternative fits one of the two cases better than the other; none is cleanly superior. (c) Redefinition to *"not on radar this cycle"* is a one-sentence change; renaming cascades through docs and agent prompts.

---

## Principles That Emerged

Distilled from the decisions above, now canonicalized in `GTDv2 - Philosophies, Rationales and Principles.md`:

- **Active = what I am driving this cycle.** (Not "willing to carry mentally" in the abstract.)
- **Capacity and appetite are separate axes.** Both together → Active. Appetite without capacity → Overflow. Neither → Maybe.
- **The recurring 4-way question** is the canonical transition for any project leaving Active or Waiting-For.
- **Overflow is not a wishlist.** Membership requires both appetite *and* willingness to take an open slot.

---

## Notes for Future Revisions

- If Overflow consistently blows past ~10, either Active cap is too tight or appetite is inflated. Don't just raise the cap — interrogate the appetite first.
- If Waiting-For rots (items forgotten, replies missed), the weekly skim isn't enough; consider an external cadence (e.g., a separate "did anyone reply?" check).
- If Maybe balloons past ~25 consistently, consider either a more aggressive Cold Storage push or the reference-system migration mentioned in `Backlog.md`.
