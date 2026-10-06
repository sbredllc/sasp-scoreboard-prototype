# SASP Scoreboard

A small, phone-friendly starter project for a SASP team and match-day scoring app.

## Try It

1. Open `index.html` in a modern browser such as Microsoft Edge or Chrome.
2. On first launch, choose **Create a team**. The **Join an existing team** option is marked **Coming soon** because online accounts and invitations are not part of this local prototype yet. Teams are saved only in this browser on this device.
3. Use the **Team Setup** menu screen to add or select a team and manage its members. Each profile requires a first and last name; preferred name and grade are optional. Graduation year is optional, with choices from 2027 through 2046. Member email/phone and parent/guardian name, email, and phone are also optional. Delete a team or member to archive it from active lists; restore archived entries from the corresponding Archived section. Archiving preserves historical matches and scores.
4. Open **Match Setup** to create an event in advance. Enter the event name and start date, with an optional end date, location, and notes, then select the stages and team members who will participate. Assign each participating shooter to an event-specific squad of up to four and choose that shooter's division, category when applicable, and firearm discipline. Classifications are selected per event and are not inferred from grade or graduation year. You can add squads and change assignments before saving, and arrange members differently for each event. Saved events appear below the setup form with their squads and classifications listed.
5. Use **Edit event** on a saved event card to change its name, dates, location, notes, stages, participating team members, and their squad/classification selections. Removing a shooter or stage permanently deletes its related strings and stage approvals for that event; the app confirms before deleting recorded strings.
6. On match day, open **Scoring** or select **Score this event** from its saved-event card. Choose the event to score; event dates, location, stages, and shooter count are shown above the scoring form. Events remain available for switching, and their scoring history stays separate.
7. Choose a shooter and one of the selected event's stages, enter the timer time, then mark each target Hit or Miss and record its shot-attempt count before saving the string. The run log below shows only the currently selected shooter and stage; changing either selection clears the timer entry and changes the visible log without deleting saved strings.
8. After all five strings for a stage have been scored, review the fastest-four subtotal and have the shooter select **Accept stage total**. Only accepted stage totals are included in the match total.
9. Open **Stage Layout** and select a stage from its dropdown to see its approximate stage diagram and a reference table of each target's lateral position, downrange distance, size, shape, and height.
10. Open **Stats** to select a team member, then filter their statistics by match and stage. Selecting **All matches** or **All stages** shows combined results with each match/stage kept as a separate table row.
11. Open **Schedule** to add or review team calendar events. Each schedule event needs a name and date; time, location, and notes are optional.

The stage choices are Exclamation, V, Go Fast, Focus, M, Speed Trap, In & Out, and Pop Quiz.
The **Stage Layout** screen includes an approximate diagram and dropdown-driven reference table for all eight stages. Lateral positions are approximate; verify the actual course setup at the range.
Each shooter records five strings per selected stage in each match. Based on the 2027 handbook, each missed bang target adds 3 seconds, missing the stop target records a 30-second string score, and hitting Pop Quiz's penalty target adds 8 seconds. String scores are capped at 30 seconds. After all five strings at a stage are scored, the shooter accepts that stage's subtotal. The subtotal is the sum of the four fastest strings; the match total adds accepted stage subtotals for the stages selected in that match. Match totals remain provisional until all selected stage totals have been accepted.

Each stage has an original, approximate top-down range guide based on the handbook and one Hit/Miss choice plus a shot-attempt count for every target on each string. All diagrams use the same scale for horizontal and downrange distances and are displayed at 80% of the card width. Plate sizes are drawn proportionally to their dimensions and enlarged by an additional 75% from the previous target size, retaining the prior visibility adjustments. Lateral target offsets remain approximate where exact measurements are not specified. The Exclamation guide places the four bang targets diagonally from front to back, with the stop plate far right at the same distance as the leftmost bang target. The Speed Trap guide places its farthest target straight downrange from the shooter box, with the outer targets at 30 ft and the two inner targets at 36 ft. The In & Out guide places the stop plate in the middle of its four bang targets. The Pop Quiz guide shows the two rear round targets partly behind the penalty plate, the stop plate in front of it, and the final two targets spread to either side in front. Attempt counts default to one; use zero when no shots were taken at a target. Attempts are informational and do not change the scoring penalty, which is applied once for each missed bang target. Confirm target positions and measurements against the actual course: the guide is not a survey drawing, and the handbook notes that target heights may vary by range.

Scoring rules are based on the 2027 handbook (scoring on page 17; stage diagrams on pages 28–35).

The prototype saves its data in browser storage on the current device. It does not use an account, sync data between devices, support joining an online team, encrypt contact details, or provide backups. Only enter member or parent/guardian contact information when appropriate consent has been obtained. Clearing browser data can remove saved entries.

Each shooter in the current match has a summary tab with all five string times for every selected stage, stage totals and acceptance status, shot-attempt counts, target hits and misses, target hit rate, accepted-stage count, and match total. Hit rate is based on marked target outcomes, not individual shots. Average scored string time is also shown; old records without attempt counts are identified as unavailable rather than inferred.

The **Stats** screen provides shooter, match, and stage dropdowns, aggregate performance metrics, and a match-by-stage table with string times, stage totals, approval status, attempts, hits, misses, and hit rate.

The **Schedule** screen keeps dated events scoped to the selected team and displays them chronologically. Removing a schedule event removes that event from the saved team schedule.

## Scoring Note

This prototype calculates each competitor's stage score as the sum of their four fastest scored strings out of five, using target penalties listed above. The shooter accepts the completed stage total, and the match total sums accepted stage scores across the stages selected for that match. It remains provisional until every selected stage total is accepted. It does not calculate official match or team results or other procedural penalties. Confirm the full scoring rules and competition workflow before using results for an event.

Data saved before teams were added is migrated into a team containing the existing roster and matches. Data saved before match setup was added is migrated into a single match containing the existing team roster and all stages. Strings saved before target-by-target scoring and stage acceptance were added remain visible, but they do not count toward totals until re-entered with target results and the shooter accepts the stage total.

## Current Scope

- Create and switch between teams.
- Archive and restore teams while preserving their members, matches, and scores.
- Add team members, with names, preferred name, grade, and optional member/parent-guardian contact details; archive and restore members while preserving match history.
- Record an optional member graduation year from 2027 through 2046.
- Create events in advance with dates, location, notes, selected stages, and participating team members.
- Assign participating members to event-specific squads of up to four; squad membership can differ from event to event.
- Record each shooter's event-specific division (Rookie, Intermediate, Senior, College, or Open), applicable category (Intermediate Entry Level/Advanced or Senior Junior Varsity/Varsity), and firearm discipline (RFI, RFO, CFI, CFO, 1911, Rimfire Revolver Iron Sight, Ultimate, or PCC).
- Edit saved event details, stage selections, and participating team members.
- Score previously created events separately from Match Setup, switching among saved events without mixing their score records.
- Review target positions and dimensions for each stage in the Stage Layout dropdown and reference table.
- Add, review, and remove team schedule events with dates, optional times, locations, and notes.
- Filter each team member's statistics by match and stage.
- Record up to five strings per competitor for each stage.
- Mark each target Hit or Miss once per string and record its shot attempts.
- Have the shooter accept each completed stage total before it counts toward the match total.
- Apply the listed target penalties when calculating string times.
- See stage subtotals based on the four fastest strings and match totals from accepted stages.
- Review per-shooter stage and match statistics in each shooter's summary tab.
- Remove recorded strings.
- Keep the current data in browser storage.

Deleting a team or member archives it instead of permanently erasing it. Archived teams disappear from the active team selector; their members, matches, and scores remain saved, and restoring the team makes its history accessible again. Archived members are excluded when creating future matches. They remain visible in any existing match they participated in, with past strings and scores retained; new strings cannot be recorded for an archived member. Use the **Archived teams** and **Archived team members** sections in Team setup to restore entries. Each archived entry can also be permanently deleted. Permanent deletion requires confirmation and erases that team's members, matches, and related scores, or the member's match entries and scores; it cannot be undone.

This is an early prototype, not a production scoring system.
