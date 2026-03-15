# Task: Merge 3 BI Modules Into One App

## What exists
Three standalone HTML files in this directory:
- financial-health.html
- acquisition-analysis.html  
- ops-intelligence.html

## What to build
Create a single `index.html` that combines all three modules into one professional app with:

### Navigation
- Fixed sidebar or top nav bar with the 3 module tabs
- Active state highlighting on current module
- Smooth transitions between modules (no page reload — use JS to show/hide sections)
- PGG branding: "Beacon — Business Intelligence" at the top

### Layout
- Dashboard-style layout
- Sidebar nav (left) with icons + labels for each module
- Main content area (right) shows the active module
- Top bar with: logo/brand, current module name, notification bell icon
- Footer: "Pillar Governance Group — Beacon BI"

### Design
- Same navy/gold theme (#1a2744, #c9a84c)
- Professional, clean, modern
- Mobile responsive — sidebar collapses to hamburger on mobile
- All charts and interactivity from the original modules preserved

### Module Names in Nav
1. 🏠 Overview (home dashboard with key metrics from all modules)
2. 📊 Financial Health
3. 🔍 Acquisition Analysis  
4. ⚙️ Operational Intelligence
5. 👥 Recruitment & Workforce — vacancy tracker, agency vs permanent, DBS expiry alerts, training matrix, staff retention, visa status tracker, recruitment pipeline
6. 🤝 Commissioner Relations — revenue per council, contract renewal dates, rate history, referral pipeline, LA relationship scoring, tender tracker
7. 🏠 Property Management — lease expiry tracker, rent vs revenue per property, maintenance requests, occupancy rates, utility costs, compliance certs (fire/gas/electrical)
8. 📋 Service User Journey — referral to placement timeline, support plan progress, outcome measurement, placement breakdown early warning, move-on tracker
9. 🛡️ Regulatory Dashboard — CQC inspection readiness score, Ofsted compliance, policy review schedule, Supported Housing Act checklist, audit trail

### Extra
- The Overview/home tab shows summary cards pulling key metrics from ALL modules
- Keep everything in ONE index.html file (inline CSS/JS)
- Chart.js via CDN

## Output
Save as: /Users/matthewwilliams/.openclaw/workspace/pgg-bi-layer/index.html

When finished run:
openclaw system event --text "Done: BI modules merged into single app with nav tabs at /Users/matthewwilliams/.openclaw/workspace/pgg-bi-layer/index.html" --mode now
