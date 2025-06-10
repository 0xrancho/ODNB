ODNB / Data Directory

This directory contains data files and schema definitions used by the ODNB segmentation engine. It supports both SMB Services and Retail/DTC apps by standardizing input formats and required metadata.

📁 Structure

sample_customers/

Sample CSV files used for testing, demos, and validation.

Each file should include clear headers and anonymized customer data

Recommended columns: CustomerID, LastPurchaseDate, EmailEngagement, Segment, LTV, etc.

schema_definitions/

YAML or JSON schemas that define:

Required fields for all customer datasets

Expected data types (e.g., date, numeric, categorical)

Optional fields that may influence prompt or scoring logic

CustomerID:
  type: string
LastPurchaseDate:
  type: date
LTV:
  type: number
Segment:
  type: string

🧪 Usage Notes

All engine modules in /engine/ read from these definitions

Lovable apps auto-suggest upload templates based on schema metadata

Scoring logic in /engine/scoring/ assumes fields defined here exist in input data

🔜 Coming Soon

Synthetic dataset generator

Schema validator for upload compatibility

CSV preview and pre-inference diagnostics
