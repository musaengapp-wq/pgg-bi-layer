# PGG Business Intelligence Layer — Build Task

## Overview
Build three modules for PGG's Business Intelligence layer. These are frontend-only demos (like the existing PGG MVP at /tmp/pgg-demo) — single HTML files with inline CSS/JS. Professional design matching the Cedar Hope report style (navy/gold theme).

## Design System
- Navy: #1a2744
- Gold: #c9a84c  
- Light gold: #f5ecd7
- Red: #c0392b (alerts/warnings)
- Green: #27ae60 (positive)
- Orange: #e67e22 (medium risk)
- Font: Segoe UI / system fonts
- Mobile responsive

---

## MODULE 1: Financial Health Dashboard (financial-health.html)

A real-time financial dashboard for care providers.

### Sections:
1. **Revenue Overview** — monthly revenue bar chart (last 12 months), YoY growth %, total revenue
2. **Client Concentration** — pie chart of revenue by commissioner/council, HHI score with traffic light (Green <1500, Amber 1500-2500, Red >2500)
3. **Payroll Ratio** — gauge showing payroll as % of revenue. Benchmark line at 65%. Red zone above 70%.
4. **Cash Position** — current bank balance, invoiced but unpaid, factored amount, net cash position
5. **Aged Debtors** — table with traffic lights: current, 30 days, 60 days, 90+ days
6. **Monthly Profit Trend** — line chart, rolling 12 months, with average line
7. **Per-Property P&L** — table showing each property: revenue, staff cost, rent, other costs, profit, margin %
8. **Void Rate** — percentage of empty beds per property, with occupancy target line
9. **Key Metrics Cards** — Revenue per occupied bed/week, Staff cost per occupied bed, Average placement duration

### Alert System (sidebar or top banner):
- Payroll exceeds 70% → amber
- Single commissioner >40% revenue → red
- Cash below 2 months operating costs → red  
- Void rate >15% → amber
- Aged debt >90 days → red

### Demo Data:
Use Cedar Hope's actual figures where available:
- Revenue: £1.7M, monthly ~£130-140k
- Payroll: 75%
- West Berkshire: 48%
- Properties: Southcote Lane x2, Hamilton Road, Basingstoke Road, Fairlawn Green, Pentland Close
- Create realistic monthly variation (not flat lines)

---

## MODULE 2: Acquisition Analysis Engine (acquisition-analysis.html)

An automated due diligence tool — what we did manually for Cedar Hope, but as a structured interface.

### Sections:
1. **Deal Summary Card** — target company, asking price, seller, buyer, completion date, deal multiple
2. **Financial Performance Table** — 5 years of turnover, profit, margin, corp tax (like our Cedar Hope table)
3. **Monthly vs Annual Comparison** — shows monthly run rate vs reported annual (catches the £7.6k vs £319k discrepancy)
4. **Revenue Concentration Analysis** — HHI calculator, top commissioners, concentration risk rating
5. **Balance Sheet Snapshot** — assets, liabilities, intercompany, director's loan, factoring
6. **Risk Matrix** — traffic light table of all identified risks (like our 10 key findings)
7. **Valuation Calculator** — input profit figure, select multiple range (2x-6x), shows valuation range. Toggle between best year, 3-year avg, run rate.
8. **Deal Structure Builder** — sliders for completion %, deferred %, earnout %. Shows amounts based on total price.
9. **Fix Cost Calculator** — list of fixes with editable costs, shows total investment, annual savings, payback period
10. **Questions Generator** — checklist of standard DD questions, ticked/unticked, exportable

### Demo Data:
Pre-populated with Cedar Hope data as the example case.

---

## MODULE 3: Operational Intelligence (ops-intelligence.html)

Ongoing monitoring dashboard for post-acquisition or retained clients.

### Sections:
1. **Staff Overview** — total headcount, permanent vs agency split, staff turnover rate (last 12 months)
2. **Staff Utilisation** — hours worked per property per week, agency hours %, overtime hours
3. **Placement Dashboard** — active placements, new this month, ended this month, average duration, breakdown reasons (pie chart)
4. **Compliance Score** — per property compliance rating based on: contact notes up to date, incidents resolved, training current, support plans reviewed
5. **Contact Notes Monitor** — total this month, flagged (no contact 7+ days = RED, attempted but no actual 14 days = safeguarding trigger)
6. **Incident Tracker** — open incidents, average time to resolve, severity breakdown
7. **Training Matrix** — staff training completion %, overdue items flagged red
8. **Cost per Occupied Bed** — the killer metric. By property. Weekly. Broken down: staff, rent, utilities, other.
9. **Placement Retention Curve** — line chart showing how long placements last (months), with industry benchmark overlay

### Demo Data:
Create realistic care provider data — 6 properties, ~30 service users, ~40 staff members.

---

## Technical Notes:
- Each module = single self-contained HTML file (CSS + JS inline)
- Use Chart.js via CDN for charts (https://cdn.jsdelivr.net/npm/chart.js)
- All interactive — clickable cards, expandable sections, hover tooltips
- Print-friendly (PDF export via browser print)
- NO backend — all demo data hardcoded
- Professional quality — this will be shown to potential clients

## Output:
Save all three files to this directory:
- /Users/matthewwilliams/.openclaw/workspace/pgg-bi-layer/financial-health.html
- /Users/matthewwilliams/.openclaw/workspace/pgg-bi-layer/acquisition-analysis.html  
- /Users/matthewwilliams/.openclaw/workspace/pgg-bi-layer/ops-intelligence.html

When completely finished, run this command to notify:
openclaw system event --text "Done: All 3 PGG Business Intelligence modules built — Financial Health, Acquisition Analysis, Ops Intelligence. Check /Users/matthewwilliams/.openclaw/workspace/pgg-bi-layer/" --mode now
