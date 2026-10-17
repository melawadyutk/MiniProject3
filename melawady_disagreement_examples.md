# Disagreement Examples — melawady & mjohn326

Parties: **melawady** (Marwan Elawady) and **mjohn326** (Makenzie Johnson).
Between us there were 100 records (5 fields × 10 projects each way). 7 disagreed before discussion; all 7 were resolved.

## Example 1 — mattjj/pyhsmm (HasRecovered)
- **Owner:** mjohn326 · **Validator:** melawady
- **Author value:** Yes · **Validator value:** No
- **Evidence:** The only commit after the 2022-11..2024-12 gap is PR #121, *"docs: add warning message in the README"* (merged by mattjj on 2025-01-25). The README now opens with *"⚠️ Warning: this package is not maintained anymore ⚠️"*. The other 2025 rows in the WoC data are PR merge refs, not new development.
- **Discussion:** New commits after a gap usually mean recovery. Here the only new commit retires the project instead of reviving it.
- **Resolution:** **ValidatorKept** (No). mjohn326 agreed with the evidence.

## Example 2 — elfi-dev/elfi (HasRecovered)
- **Owner:** mjohn326 · **Validator:** melawady
- **Author value:** No · **Validator value:** Yes
- **Evidence:** 1,132 commits follow the 2019-06..2019-10 gap. Henri Pesonen resumed on 2019-11-15 (*"Enabling BOLFI-fit using only initial evidence points"*, PR #309), and the project stayed active until 2025-05.
- **Discussion:** The author's note ("the work was coming to a close") described the slowdown before the gap, not what happened after it. The commit counts settled the question.
- **Resolution:** **ValidatorKept** (Yes). mjohn326 agreed with the evidence.

## Example 3 — elfi-dev/elfi (ActivityPattern)
- **Owner:** mjohn326 · **Validator:** melawady
- **Author value:** steady · **Validator value:** declining
- **Evidence:** Yearly commits: 1,102 (2016), 789, 374, 105 (2019), 170, 351, 286, 170, 81, 11 (2025).
- **Discussion:** mjohn326 agreed but pointed out that the series could be read both ways: a steep drop in 2016–2019, then a fairly steady low level. We kept *declining* because it describes the long-term trend from start to finish.
- **Resolution:** **ValidatorKept** (declining), with the "steady low level after 2019" note recorded in the comments.

## Example 4 — mummer4/mummer (ActivityPattern)
- **Owner:** melawady · **Validator:** mjohn326
- **Author value:** irregular · **Validator value:** seasonal
- **Evidence:** mjohn326 saw an uptick around the fall in most years. Counting commits by month of the year, October has the most (73).
- **Discussion:** melawady had read the yearly counts as irregular (120, 79, 54, 17, 10, 59, 4, ...). After discussion he accepted the repeating fall uptick. "Seasonal" is not a category in the coding guide, so we recorded it as *cyclical*, which covers patterns that repeat at fixed intervals.
- **Resolution:** **ValidatorKept**, recorded as cyclical.

## Other disagreements (all ValidatorKept)
| Project | Field | Owner | Validator | Final |
|---|---|---|---|---|
| CARTAvis/carta-frontend | ActivityPattern | Steady | Declining | declining: commits fell from a 2,654 peak in 2021 to about 1,200–1,400 per year |
| pytorch/audio | ActivityPattern | irregular | declining | declining: 3,592 commits in 2021 down to 635 in 2024, still well below the peak after the 2025 rebound |
| nmslib/nmslib | RecentThemes | Other:Bug fixes | Bug fixes:Documentation updates | Bug fixes:Documentation updates: recent work is mostly test fixes plus README and build-config updates |
