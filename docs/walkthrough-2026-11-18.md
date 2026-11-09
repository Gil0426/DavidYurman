# Nov 18 walkthrough: David Yurman PD dashboard

**When:** Wednesday, Nov 18, 2026, 12:30 pm ET, 30 minutes
**Who:** Gabrielle Miller, Paloma Baillie, Monique Matthews, Gil Oliveira
**Goal:** show what changed since Nov 5, confirm two definitions, and agree on one process fix so the Design column fills in.

Suggested order for 30 minutes: 5 min what changed · 15 min walk the Overview and Turnover with one season selected (2027 Womens February) · 10 min the three findings and two questions.

## What changed since Nov 5

| Nov 5 ask | Status |
|---|---|
| Overview reads the Master Board, not PLM | Done. The only PLM value the Overview reads is STATUS = Design Cancelled, to exclude cancelled styles. |
| Styles in scope = styles on the Master Board | Done. 1,599 across 13 active seasons, cancelled excluded. |
| Season pipeline stages: Design → Concept → CAD → Complete | Done. Every style starts in Design and moves as a team picks it up or signs it off. Costing excluded (runs in parallel). |
| Count + % of season on every segment | Done, everywhere. |
| Team progress: 5 columns, each from its own board | Done. Design, Concepts, CAD on the first row; Costing and PD Turnover centered below. |
| Delay finder tabled; season Gantt in its place | Done. Delay finder hidden, not deleted. |
| Designers tab from the Design Log | Done, with a caveat (finding 1 below). |
| Stats / Turnover: show sample + production, Concepts-style bars, on-time % | Done, from the Master Board columns Gabrielle pointed at. |
| CAD: rename Total, list seasons under iterations | Done. |
| Drill-downs show product description | Done. |
| Monday links fixed (were 401) | Done. |
| PDF export | Done. Export PDF button in the top bar, wordmark header, landscape. |
| Costing tab | Built, from the Design Costing Log. |
| Gemstones tab | Built from the Gemstones HJ Log, pending Monique's confirmation the team still uses it. |
| Year-over-year view | Not yet. After this round. |

## Three data findings

These are about the boards, not the app. Each one changes what a number on the dashboard can mean.

### 1. The Design Log isn't tied to styles

Of 204 tasks on the Design Log, 2 are linked to a Master Board item and none have the SKU/STYLE No. filled in. Many task names are ideas, not styles ("Labradorite Bead NL", "X Collection"); some carry a style number in the name ("CR5749 - HJ LIBERTY RING").

What this means: the Designers tab reports designer workload accurately (tasks, queue time, weeks per task). It can't report *which styles are with which designer* per season until tasks are tied to styles. The Overview handles this by treating Design as the starting stage for every style, so the pipeline is still right; it's the per-designer view that's limited.

The app already matches a task to a style three ways: the Master Board link, the SKU column, or a style number at the start of the task name. Any one of them works. The "unmatched" link on the Designers tile lists the tasks that have none.

### 2. The Master Board and PLM don't agree on how many styles a season has

2027 Womens February: 470 on the Master Board, 371 in PLM. 2027 Womens September: 441 vs 616. Two seasons exist in PLM but not on the Master Board. Some of this is scope (the Master Board is "styles in our working world"), some is the PLM → monday sync issue Monique is chasing with Molly.

What this means: Overview numbers will never match a PLM report. Answer when asked: "the Overview counts what's on your Master Board; PLM counts everything in PLM."

### 3. The same season is spelled two ways on the Master Board

"2027- Womens February" (391 styles) and "2027- WOMENS FEBRUARY" (79). The app matches both, but any monday filter or dashboard the team builds won't. A one-time cleanup, or a formula column, fixes it.

Smaller note: only about 7% of styles have a concept project, so the Concepts column is mostly "no item." Worth a yes/no on whether that matches how the Concepts team works.

## Two questions for Gabrielle

1. **Concepts coverage.** About 7% of styles in scope have a concept project. Does that match reality (Concepts handles a subset), or are projects missing their link to the Master Board?
2. **How should designers tie a task to a style?** Pick one habit for the team: link the Master Board item, fill in SKU/STYLE No., or start the task name with the style number. The app accepts all three; the team just needs to do one consistently. Once they do, the Design column and the "With Designers" tile fill in on their own.

## Open items on DY's side (from Nov 5)

- Monique: gemstones board owner (Kenneth); PLM → monday sync (Molly).
- Gabrielle: what the CAD tab's top KPI row should show; per-team deadlines (needed before the delay finder can come back).

## After this call

- Year-over-year view (CAD iterations trend, on-time trend by season).
- Delay finder, rebuilt against team deadlines once DY provides them.
- Any drill-down column changes from walking the pop-outs together.
