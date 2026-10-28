# Vibe App Prompt: David Yurman Product Development Reporting

Paste everything below the line into monday Vibe. Upload `brand/david-yurman-wordmark-black.png`
and `brand/david-yurman-wordmark-white.png` as the logo assets.

---

## What to build

Build a reporting app for **David Yurman Product Development**. It answers two questions:

1. **Season view:** For each season (for example F27), where is every style in the development process, and is the season on track?
2. **Team view:** For each team, how much work is in queue, in work, and complete, how long it takes, and how much of it is on time?

The people using it are PD leadership and team leads. They need to see where the bottlenecks are and, when a style is late, **which stage caused the delay**.

## Data sources (monday boards)

Use the boards already connected to this app. Before building anything, inspect each connected board's columns and map them to the fields below. Tell me the mapping you chose, and ask me if a field is ambiguous or missing. Don't use mock data unless a board is empty.

**Styles / Projects board** (one item per style). Find:
- Season (F27, S27, etc.)
- Current Stage: Design → Concepts → Concepts CAD → Wax → CAD → Gemstones → Costing → Turned Over (T/O)
- One status column per team with the values In Queue / In Work / Complete
- Designer (people) and CAD Designer (people)
- For each stage: the date it entered the queue, the date work started, and the date it finished
- CAD Iterations (number)
- Turnover Due Date and Turnover Actual Date

**Seasons board** (one item per season). Find the deadlines per season:
- Design Finalization Deadline, Concepts Submission Deadline, CAD Submission Deadline, Turnover Deadline
- If there's no Seasons board, ask me for these deadlines per season and store them in the app's settings.

**Gemstones board** (one item per stone, linked to a style). Find:
- Season, Out Type (QC / Repolish / Cert), Date Sent Out, Date Due Back, Date Returned

Rules for the numbers:
- **"Weeks in X"** = (finish date − start date) ÷ 7, rounded to one decimal. "Weeks in X queue" uses the queue-entry date and the work-start date. If a style is still open, measure up to today.
- **"On time"** = the style was submitted to (or finished) the stage on or before that season's deadline.
- **"% of season"** = that count divided by the total number of styles in the season.

## Global layout

- A top bar with the David Yurman wordmark on the left. Filters for **Season** (multi-select, defaults to all active seasons), **Team**, and **Person**.
- Tabs: **Overview · Designers · Concepts · Concepts CAD · Wax · CAD · Gemstones · Costing · Stats / Turnover**
- Every chart and KPI responds to the filters. Clicking a number or bar opens a drill-down table of the styles behind it, with a link to each monday item.

## Tab 1: Overview (full scope)

- **Team progress per season:** a stacked bar for each team and season showing In Queue / In Work / Complete.
- **Season pipeline (holistic view):** for each season, a horizontal funnel or stacked bar showing how many styles are in each stage (for example, "F27: 12 in Design, 8 in Concepts, 20 in CAD…").
- **Lifecycle snapshot / delay finder:** a table of late styles. For each one, show a mini stage-by-stage timeline with the time spent in each stage. Highlight the stage that ran longest compared with that stage's season average, and label it "Primary delay."

## Tab 2: Designers

- Number of projects per designer, by season.
- In Queue / In Work / Complete per designer.
- Average weeks in Design and weeks in the Design queue (per designer and per season).
- Number and % of projects submitted to Design on time (before the Design Finalization Deadline).
- An on-time flag for each style in a table.
- **Gantt chart:** X axis is time, Y axis is season. One bar per season, from the date the first style entered Design to the date the last style completed Design, so you can see where seasons overlap.

## Tab 3: Concepts

- Number and % of the season submitted to Concepts on time.
- Average weeks in Concepts.

## Tab 4: Concepts CAD

- Number of projects in each queue (In Queue / In Work / Complete).
- Number of Concept CADs per season.

## Tab 5: Wax

- Number of projects in each queue.
- Number of waxes per season.

## Tab 6: CAD

- Total CAD iterations per style, shown as a table plus a histogram of the distribution.
- Weeks in CAD, split into in work and in the CAD queue.
- Number and % of the season currently in CAD, as a live snapshot.
- Number and % of the season submitted to CAD on time.
- Number and % of the season that went through CAD.
- **Gantt chart:** season start in CAD to season complete in CAD, showing overlap (same format as the Designers tab).

## Tab 7: Gemstones

- Number of stones out for QC / Repolish / Cert, per season.
- Average days out per stone, by out type.
- Stones on time vs. late, per season.

## Tab 8: Costing

- Number and % of the season in Costing right now, complete vs. not complete.
- Average weeks in the Costing queue.

## Tab 9: Stats / Turnover

- On time vs. outstanding turnover (T/O) per season, as of today.
- **Gantt chart:** from the date each season started to the date the season was fully turned over, showing season overlap.

## Branding (exact, from the official DY 2026 template; do not invent a style)

**Logo:** the uploaded "DAVID YURMAN" wordmark. Use the black version on light backgrounds and the white version on black. Don't recreate the logo in a font.

**Fonts:**
- Headlines, page titles, and KPI numbers: **Garamond Regular**. Use the stack `Garamond, "EB Garamond", "Cormorant Garamond", serif`.
- All other text (labels, tables, body copy): **Helvetica Light**, with Helvetica Regular for emphasis. Use the stack `"Helvetica Neue", Helvetica, Arial, sans-serif` at weight 300, and 400 for emphasis.
- Section labels are small and quiet, like the template's sub-captions. Use sentence case and lots of white space.

**Colors:** use only these. No blues, greens, oranges, or default chart palettes.
- Primary (warm neutrals): `#F2EBE5` (blush/cream), `#BAA08B` (taupe), `#CDB9A8` (sand), `#DED1C4` (light sand)
- Secondary (greys): `#000000` (black), `#595959` (charcoal), `#D0D0D0` (light grey)
- Background: white `#FFFFFF`. Cards are white with a hairline `#D0D0D0` border, or filled with `#F2EBE5`. No heavy shadows and no rounded "bubbly" corners. Keep corners square or nearly square (2px at most).
- Text: `#000000` for headlines, `#595959` for body text and labels.

**Chart color mapping** (use it the same way everywhere):
- Complete / On time: `#BAA08B`
- In Work: `#CDB9A8`
- In Queue: `#DED1C4`
- Not started / no data: `#D0D0D0`
- **Late / Outstanding / Primary delay: `#000000`, with a text label ("LATE")**. Don't use red. Lateness reads as solid black against the soft neutrals.
- If a chart needs more than 4 series (for example, pipeline stages), go in this order: `#000000`, `#595959`, `#BAA08B`, `#CDB9A8`, `#DED1C4`, `#D0D0D0`, `#F2EBE5`.

The overall feel should be a luxury jewelry brand: editorial, minimal, calm, with thin rules between sections like the template's divider lines. Don't use emoji or playful icons.

## Build approach

Build the Overview tab and the global filters first, wired to live board data. Then add the team tabs one at a time. If a column I referenced doesn't exist, show an empty state that says which column is missing rather than making up data.
