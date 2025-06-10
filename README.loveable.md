# ODNB / Loveable Frontend Specs

This directory defines the frontend logic and UX flows for the **Big Loud Shirt** (DTC/Retail) demo tool, built using [Lovable.dev](https://lovable.dev). It powers the segment exploration interface and interaction flow.

## 🔁 Flow Overview

Lovable uses a YAML config to orchestrate multi-step chat experiences. This tool guides users through selecting a business goal, tactic, and dataset — then returns actionable insights and GTM strategies.

---

## 🧩 Files

### `context_page.md`
Defines the first screen logic:
- User selects:
  - Business Goal (Winback, Expand, Advocate)
  - Agent (e.g. Reactivation Email, Discount Offer)
  - Dataset (CSV from upload or preset sample)

Auto-generates a prompt to query segments.

---

### `insights_page.md`
Defines the second screen:
- Loads the GPT_BIN sunburst visualization
- Allows drill-down to segments
- Displays:
  - Segment Summary
  - Best-Fit Tactics
  - Example Messaging
  - Campaign Targets
  - Estimated Reach

---

### `flow_config.yaml`
Lovable workflow configuration:
- Page order
- Event triggers
- GPT input/output fields
- Component behavior and visual hierarchy

---

## 💡 Usage Notes

- This flow is optimized for mid-market retail brands and DTC operators using uploaded CSVs.
- Built to be repurposed for `apps/odnb` (SMB Services) by swapping prompt stacks and segment visuals.
- All prompts are generated using metadata from `engine/` and schema definitions in `data/schema_definitions/`.

---

## 📍To Do
- Implement visual component references for charts and sliders
- Add support for `segment bookmarks` and `campaign queue`

