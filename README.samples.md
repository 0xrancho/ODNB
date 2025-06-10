# Sample Customer Datasets

This folder contains preloaded CSVs used for testing, demos, and UI development. These files simulate real customer data and should conform to the expected schema for each industry and tactic.

---

## Naming Convention

Use this pattern:
`<industry>_<goal>_<tactic>.csv`

Examples:
- `hvac_winback_reactivation.csv`
- `retail_expand_bundle.csv`
- `plumbing_advocate_referral.csv`

---

## File Guidelines

Each CSV should:
- Have a header row
- Include all **required meta fields** listed in `schema_definitions/`
- Be under ~5000 rows for performance
- Use realistic, anonymized data

---

## Current Samples

| File | Description |
|------|-------------|
| `american_water.csv` | SMB service dataset for winback scenarios |
| `blue_mountain_it.csv` | IT services dataset with contract metadata |

