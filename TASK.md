# TASK: Add Per-Property P&L Comparison to BI Layer

## What to build
Add a new section to `financial-health.html` called "Per-Property P&L Comparison". This is a table/dashboard showing:

1. **Property comparison table** with columns:
   - Property Name (e.g. "114 Southcote Lane", "56 Hamilton Road")
   - Beds/Units
   - Occupancy % 
   - Monthly Revenue
   - Monthly Staff Costs
   - Monthly Rent/Lease
   - Monthly Other Costs
   - Monthly Net Profit
   - Profit Margin %
   - RAG status (Red/Amber/Green based on margin)

2. Use demo data for 6 properties (use Cedar Hope property names):
   - 114 Southcote Lane (5 bed, profitable)
   - 146 Southcote Lane (3 bed, break-even)
   - 56 Hamilton Road (4 bed, profitable)
   - Basingstoke Road (5 bed, loss-making)
   - Fairlawn Green (5 bed, profitable)
   - Pentland Close (4 bed, loss-making - RI rated)

3. **Summary bar at top** showing:
   - Total monthly revenue across all properties
   - Total monthly costs
   - Total net profit
   - Number of profitable vs loss-making properties

4. **Style it to match** the existing BI Layer design (navy/gold PGG theme, same fonts, same card styling)

5. Add it as a section within financial-health.html, not a separate page

## Rules
- Keep it frontend only (HTML/CSS/JS inline)
- Demo data hardcoded
- Make the table responsive
- Commit when done with message "Add per-property P&L comparison to Financial module"
- Push to GitHub
