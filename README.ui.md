# UI Components

This folder stores or documents visual components used across ODNB apps. These components help users explore data and configure segment outputs without technical skill.

---

## Current Components

### 🎯 GPT_BIN Slider
- Adjusts segment size based on likelihood to convert or match the goal/tactic.
- Range: 1–5 or 1–10
- Interacts directly with the sunburst chart to filter visible segments.

### 🌟 Buyer Intent Star Graph
- Visualizes buyer intent using 5-point star ratings.
- Used to sub-segment users within a selected segment.
- Combines fields like recency, CSAT, spend, etc.

### 🌞 Sunburst Segment Viewer
- Hierarchical visualization of segment breakdown (e.g. by region, category, BIN).
- Clicking a wedge generates a strategy card.
- Supports multi-layer filters.

### 🎛 Refinement Filters
- Optional toggles/sliders for:
  - Region / Location
  - Product or Service Category
  - Churn Risk
  - Campaign Performance History

---

## Format

- `.py` if building Streamlit/Plotly components
- `.jsx` or `.tsx` for React versions
- `.md` descriptions if prototyping UI in natural language or Lovable

