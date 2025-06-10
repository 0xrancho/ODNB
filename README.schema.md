# Schema Definitions for Customer Data

This folder defines the expected structure of CSV files per industry and tactic. Each schema lists:

- Required metadata fields
- Optional but helpful fields
- Formatting expectations
- Example values
- Data type (string, number, date, etc.)

---

## File Naming

Use the format:
`<industry>.schema.yaml`

Examples:
- `hvac.schema.yaml`
- `retail.schema.yaml`
- `it_services.schema.yaml`

You can also define goal-specific schemas if needed:
- `winback_generic.schema.yaml`
- `expand_services.schema.yaml`

---

## Example Fields

| Field Name         | Type   | Required | Description                        |
|--------------------|--------|----------|------------------------------------|
| `CustomerID`       | string | ✅        | Unique identifier                  |
| `LastPurchaseDate` | date   | ✅        | For recency / intent scoring       |
| `TotalSpend`       | number | ✅        | For ROI modeling                   |
| `CSATScore`        | number | optional | If available, used in intent logic |
| `ZipCode`          | string | optional | Helps infer region or market type  |
| `PlanTier`         | string | optional | For upsell and advocacy segments   |

---

## How It’s Used

When a CSV is uploaded, the system:
1. Checks for a matching schema
2. Maps each column
3. Flags missing fields
4. Passes valid fields into segment logic and prompt stacks

