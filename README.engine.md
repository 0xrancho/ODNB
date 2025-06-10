ODNB / Engine Directory

This directory contains the core logic for customer segmentation, tactic prompting, scoring heuristics, and go-to-market strategy inference. It powers all ODNB apps through modular, swappable components.

📁 Structure

segments/

Contains reusable logic for defining and filtering customer segments based on input CSV data.

Example: "Lapsed but High LTV", "Active but Low Engagement"

May include YAML rule files or Python-based filters

prompts/

Houses all LLM prompt templates organized by goal and tactic.

Naming: goal_tactic_prompt.md

Example: winback_discount_prompt.md

scoring/

Implements heuristic scoring logic for each customer row.

Examples: Churn risk, buyer intent, engagement readiness

Can be YAML rules, Python scripts, or mixed-methods

strategies/

Defines playbooks that combine prompts, segment logic, and campaign triggers.

Example: "Winback Playbook" or "Seasonal Upsell Push"

🧠 Usage Notes

All apps read from these modules based on selected goal + tactic

Prompt stack logic assumes alignment with schema definitions in /data/schema_definitions/

Output is fed into UI components and Lovable frontend flows

🛠 Next Tasks

Add winback_reactivation_prompt.md and initial playbook

Build baseline scoring script for churn + intent

Refactor segment logic into JSONPath-style filter expressions
