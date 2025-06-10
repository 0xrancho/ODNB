# Testing & Validation

This folder contains basic tests and sanity checks for ODNB and Big Loud Shirt outputs.

The goal is to ensure:
- Uploaded data matches expected schemas
- Prompt stacks generate usable, accurate output
- Segment logic produces clear, interpretable results

---

## Test Types

### ✅ Output Sanity Checks
- Run goal/tactic prompts with sample data
- Validate:
  - Segment record count
  - Messaging relevance
  - Correct variable interpolation

### 📊 Schema Conformance
- Ensure each sample CSV matches its schema
- Check required fields exist
- Detect formatting issues (e.g., date/time)

### 🧠 Strategy Prompt Regression
- Run saved prompts periodically
- Compare output before/after updates

---

## Suggested Files

- `test_sample_outputs.md`
- `validate_csv_schema.py`
- `segment_card_regression.md`
