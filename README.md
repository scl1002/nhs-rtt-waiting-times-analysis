Beyond 18 Weeks: NHS RTT Waiting Times Dashboard

Power BI dashboard analysing NHS England Referral to Treatment (RTT) waiting times, April–September 2026.

Why this topic:
When I worked with post-operative patients, many had been referred on and were waiting to see a consultant. They often asked me how long the wait would be. Occasionally I saw patients whose symptoms were severe but who had not received timely, appropriate treatment. I wanted to use real data to understand how long patients actually wait and where the longest waits are concentrated.

Power BI features used
Power Query: data loading and cleaning
DAX: measures (total waiting, % over 18 weeks) and calculated columns (52–65 / 65–78 / 78+ week bands)
KPI cards, line chart, stacked bar chart, table
Report page tooltip: hover over a specialty to see its long-wait breakdown
Slicer: filter by NHS trust
Bookmarks: info button that opens a key findings panel
Edit interactions: keeps national KPIs fixed when other visuals are selected
Top N and visual-level filters

Data
NHS England RTT Waiting Times, April–September 2026. Analysis uses incomplete pathways (Part_2), the measure used for the 18-week standard.

Key findings (Sep 2026)
About 34% of patients had waited over 18 weeks, against a target of no more than 8%.
52+ week waits rose ~13% (≈201K → ≈227K) while the overall 18+ week backlog stayed flat.
Trauma & Orthopaedics has the most long waiters: about 1 in 5 of all 52+ week waits.
What I learned

The raw data needed careful validation. Summing all RTT part types, including the "Total" row and adding monthly snapshots together all inflated the figures several times over. I fixed these by filtering to Part_2, excluding the Total row and using the latest month for point-in-time figures.
