# Discovery call: David Yurman PD dashboard

**Date:** Thursday, Nov 5, 2026
**Attendees:** Gabrielle Miller (VP Women's Design & Ops), Paloma Baillie, Monique Matthews (Dir, Creative & Wholesale Tech), Gil Oliveira (CarbonWeb)
**Next meeting:** Wednesday, Nov 18, 12:30 pm ET, 30 min. Gabrielle is out the week of Nov 9. Weekly cadence after that.

## Headline

They like it ("so impressive," "I can't tell you how exciting this is"). The one structural problem is the data source: the Overview is built on PLM, and PLM statuses are not the statuses they care about. PLM status is the company-wide lifecycle (Concept / Development / Sample / Production). Their statuses are *which team has the style right now* (Design, Concepts, CAD, Costing). Those live on the team boards and roll up into the **Design Master Board**, which is the hub everything links to.

Gil didn't have access to the Master Board's mirrored columns before the call. Monique removed the restrictions during the call, and also granted Designer Log, Costing, and Concept Team Projects. Gemstones is pending.

## Decisions by section

### Overview

| Item | Decision |
|---|---|
| Data source | Swap from DYPLMAppData to the **Design Master Board**. Everything rolls up there. Only the PD Turnover column keeps using the PLM turnover date. |
| Styles in scope | Should mean "styles actively being worked on in design," from the Master Board, not everything in PLM. |
| Top KPI tiles | Revisit after the other tabs are done. Gabrielle: a number like "turned over on time" is only meaningful per season, so the summary row isn't useful without season context. Table the design of this row. |
| Season pipeline | Stages become **Design → Concept → CAD → Complete** (not PLM stages). Costing is excluded because it runs in parallel with everything. Each segment shows **count and % of the season** ("2 of 6 still with designers, 4 of 6 moved on"), not "% complete." |
| Team progress by season | Add **Concepts** and **Costing** columns (5 total: Design, Concepts, CAD, Costing, PD Turnover). Keep PD Turnover if it fits. Each column pulls from its own team's board. |
| Delay finder | **Table it** (hide, don't delete). 90% of their work is late, so a list of late styles isn't useful. Replace its spot with the **full-process Gantt** (designers → turned over, per season). Future: measure each team against its deadline; DY to provide deadlines. Gabrielle's idea: a "primary delay" column at the end of the Master Board per style. |
| Monique's idea | Mirror each tab's KPI row on the Overview. Gabrielle: only if season-scoped. Parked. |

### Designers tab

- Source: **Designer Log** board (Women's Design → Designers → Designer Log). Gil now has access.
- "On time" is not in PLM. Designers have a **deadline** and an **ETA** on their board; on time = ETA on or before deadline.
- PLM design sign-off date is fine to keep as a reference.

### Concepts, Concepts CAD, Wax tabs

- Approved as built. "Weeks in Concepts by season" was a highlight.
- Concepts CAD lives inside the Concepts board as its own tab, so the current source is correct.

### CAD tab

- Everything below the top KPI row is good.
- Top KPI row needs rethinking. "In CAD right now 67" next to "Submitted on time 120" and "Went through CAD 133" confused Gabrielle. She's taking it offline to decide what the top row should say.
- Rename the "Total" column in Weeks in CAD to **"Total weeks in CAD."**
- CAD iterations: add the **list of seasons it's pulling from** to the caption, so a reader can see "in 2026 things went through 18 times, in 2027 it's gone down."
- Fall 27 is the first season the CAD board was used in earnest. Earlier seasons will be thin.

### Stats / Turnover tab

Two sections, same layout as the Concepts stacked bars:

1. **Show sample turnover.** Only mainline seasons (names like "2027 Womens February / September") and only styles with **Wholesale** in their Channel column.
2. **Production turnover.** All seasons (mainline and premium), all channels.

Each row: a bar with turned over vs. pending turnover, then a column at the end with **"n (xx%)" on time**. Source: Master Board. Columns to use: "Target TO date for sampling," "Actual TO date for sampling," and the production equivalents (target / actual design sign-off area). Channel column exists on the Master Board (wholesale / retail / e-comm), near the front.

### Drill-downs (pop-outs)

- Include the **product description**, not just the style number. Nobody memorizes style numbers.
- The "open in monday" link returns a **401**. Fix the URL (it should point at the davidyurman-ensemble.monday.com board/item).
- Walk through every pop-out together once the boards are settled, to pick columns.

### Everything else

- **Year-over-year view** requested (e.g., 2027 through 2029, to see whether CAD iterations are trending down).
- **Season filter** add/remove works the way they want. Approved as is.
- **Export:** printable **PDF**, not Excel.
- **Gemstones:** Monique checking with Kenneth whether the team still uses the Gemstones High Jewelry Log after Chris left, and whether gemstones data is tracked in the costing log instead. The log Gil saw has no due-date column, only ETA.
- **PLM glitch:** styles sometimes exist in PLM but don't appear in monday. Monique following up with Molly. Reporting depends on this being fixed.
- **Costing:** Gil has access now; connect it.

## Action items

**Gil**
1. Connect Design Master Board, Designer Log, Costing to the Vibe app.
2. Rebuild Overview on the Master Board: season pipeline stages, team progress (5 columns), count + % everywhere.
3. Hide Delay finder; add full-process Gantt in its place.
4. Build Designers tab from Designer Log (deadline vs ETA).
5. Build Stats / Turnover (show sample + production) from the Master Board.
6. CAD tab: rename Total column, add seasons list to CAD iterations caption.
7. Drill-downs: add product description, fix the monday link.
8. PDF export.
9. Year-over-year view (lower priority).

**Monique**
- Confirm gemstones board / owner (Kenneth).
- PLM → monday sync glitch (Molly).

**Gabrielle**
- Decide what the CAD tab's top KPI row should show.
- Deadlines per team (needed before the delay finder can come back).

## Suggested build order for Nov 18

1. Connect the three boards and confirm which Master Board columns map to each stage (one Vibe message asking for a column mapping table first, then build).
2. Overview rebuild (pipeline + team progress + Gantt, hide delay finder).
3. Stats / Turnover.
4. Designers tab.
5. CAD tab cosmetics and drill-down fixes.
6. PDF export.
