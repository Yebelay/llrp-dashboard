# LLRP I — Field Monitoring Dashboard

**Project:** Making Groups Work for Women in Pastoral Communities  
**Org:** C4ED / World Bank · LLRP II · Somali Region, Ethiopia  
**Live Dashboard:** [https://Yebelay.github.io/llrp-dashboard](https://Yebelay.github.io/llrp-dashboard)

---

## 📊 What this dashboard shows

| KPI | Source |
|-----|--------|
| MSEs listed vs 360 target | MSE Member Listing CSV |
| Daily cumulative progress vs required pace | MSE Member Listing CSV |
| Team & enumerator performance | MSE Member Listing CSV |
| Treatment arm balance (Control / Human-led / Tech-based) | mse_v2.csv |
| Woreda & zone coverage (36 woredas) | mse_v2.csv |
| Spousal survey targets identified | MSE Member Listing CSV |

---

## 🚀 How to host on GitHub Pages (free)

### First time setup (5 minutes)

**Step 1 — Create a GitHub repository**
1. Go to [github.com](https://github.com) → Sign in → **New repository**
2. Name it: `llrp-dashboard`
3. Set to **Public** (required for free GitHub Pages)
4. Click **Create repository**

**Step 2 — Upload the files**
1. Click **Add file → Upload files**
2. Drag and drop both files:
   - `index.html`  ← the dashboard
   - `README.md`   ← this file
3. Click **Commit changes**

**Step 3 — Enable GitHub Pages**
1. Go to your repo → **Settings** tab
2. Scroll to **Pages** (left sidebar)
3. Under **Source**: select `Deploy from a branch`
4. Branch: `main` · Folder: `/ (root)`
5. Click **Save**
6. Wait 2–3 minutes → your link appears:  
   `https://Yebelay.github.io/llrp-dashboard`

**Step 4 — Share the link**
- Send `https://Yebelay.github.io/llrp-dashboard` to the World Bank client
- Works on any browser, any device, no login required

---

## 🔄 How to update the dashboard with new data

Each time you export new listing data from SurveyCTO:

**Step 1 — Re-run the Python script**
```bash
python3 build_dashboard.py
```
This regenerates `index.html` with updated numbers.

**Step 2 — Upload the new index.html to GitHub**
1. Go to your repo
2. Click `index.html` → **Edit** (pencil icon) → paste new content → **Commit**

OR use GitHub Desktop for drag-and-drop updates.

**The live link stays the same** — clients just refresh their browser.

---

## 📁 File structure

```
llrp-dashboard/
├── index.html          ← The complete dashboard (single file, no dependencies)
├── README.md           ← This file
└── data/               ← Optional: store raw CSVs here for reference
    ├── MSE_Member_Listing_WIDE.csv
    └── mse_v2.csv
```

---

## 📊 Power BI alternative

A Power BI data file (`LLRP_PowerBI_Data.xlsx`) is also provided with 6 clean flat tables:

| Sheet | Contents |
|-------|----------|
| `MSE_Summary` | One row per listed MSE with all field metadata |
| `MSE_Master_360` | All 360 MSEs with treatment arms, zones, teams |
| `Daily_Progress` | Day-by-day counts with cumulative and pace columns |
| `Team_Summary` | Aggregated team performance |
| `Woreda_Coverage` | Coverage status for all 36 woredas |
| `Treatment_Arms` | Arm balance: listed vs target |

**To use in Power BI Desktop:**
1. File → Get Data → Excel → select `LLRP_PowerBI_Data.xlsx`
2. Load all 6 tables
3. Create relationship: `MSE_Summary[MSE_ID]` → `MSE_Master_360[MSE_ID]`
4. Build visuals from the Instructions sheet inside the Excel file

---

## 📅 Data as of this version

- **Date:** 31-Mar-2026
- **MSEs listed:** 83 / 360 (23.1%)
- **Woredas started:** 10 / 36
- **Members listed:** 950
- **Spouse targets identified:** 94

---

## 📞 Contact

C4ED Research Team · [c4ed.org](https://c4ed.org)
