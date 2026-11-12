# 🐝 Is the Bee Network Working?
### Measuring the impact of bus franchising on punctuality in Greater Manchester

**Status:** 🟡 In progress (started November 2026)
**Author:** Aryan Dhawan · MSc Business Analytics, University of Manchester

---

## The question
Between September 2023 and January 2025, Greater Manchester brought its buses
under public control in three stages (tranches), creating the Bee Network.
TfGM reports that punctuality has improved. But a headline percentage can't
tell us *why*. Was it franchising, or seasonality, roadworks, weather, events,
or a change in which routes are being measured?

**This project asks: how much of the change in bus punctuality is actually
caused by franchising?**

## Why it matters
Other English city regions are considering bus franchising. An honest answer
about whether it works in Manchester has real value for policy decisions.

## Rollout timeline (the natural experiment)
| Tranche | Areas | Joined the Bee Network |
|---|---|---|
| T1 | Bolton, Wigan, parts of Salford, Bury & Manchester | 24 Sep 2023 |
| T2 | Oldham, Rochdale, parts of Bury, Salford & north Manchester | 24 Mar 2024 |
| T3 | Stockport, Tameside, Trafford, rest of Manchester & Salford | 5 Jan 2025 |

Because areas joined at different times, each later tranche can act as a
comparison group for the earlier ones.

## Approach
1. **Is it real?** Define punctuality, check data quality, and separate
   genuine change from normal week-to-week variation and seasonality
2. **Where?** Break performance down by tranche, day and time period
3. **Why?** Separate internal causes (operations, timetables, drivers) from
   external ones (roadworks, weather, events)
4. **So what?** Estimate the franchising effect and write recommendations
   for a transport decision-maker

## Hypotheses
<!-- Written by me before looking at the data -->
- H1: I believe franchising improved bus punctuality, because TfGM now controls timetables and can hold operators to performance targets. If true, each tranche’s punctuality will rise after its joining date, by more than in the same weeks a year earlier.
It’s wrong if tranches that hadn’t joined yet improved by the same amount at the same time. That would mean something city wide caused it, not franchising.

- H2: I believe T2 is less punctual than T1 because its operator has more cancelled or missing trips (staff or bus shortages).
If true, T2 will show lower “operated km” than T1 in the same weeks, and punctuality will be worst in the weeks when operated km is lowest.
It’s wrong if T2’s operated km is as high as T1’s. Then the buses are running, so the problem lies elsewhere (most likely the roads).

- H3: I believe the timetable changes improved punctuality mainly by giving buses more scheduled time, not by making journeys faster.
If true, punctuality jumps soon after 27 Oct 2024, and the new timetables show longer scheduled journey times than the old ones.
It’s wrong if scheduled journey times stayed the same or got shorter and punctuality still improved. That would mean the buses really did get faster.

## Data sources
- TfGM weekly Bee Network bus punctuality reports (tfgm.com)
- *Exact definition of "on time" to be confirmed from TfGM documentation*

## Repository structure
data/
raw/ ← data exactly as collected, never edited
processed/ ← cleaned data ready for analysis
notebooks/ ← exploration and analysis, numbered in order
src/ ← reusable Python code
docs/
decision_log.md ← every analytical decision and why I made it

## Progress log
- **Nov 2026:** Project defined, repository created

## Tools
Python · pandas · DuckDB · SQL · Streamlit · LLM-assisted text classification

