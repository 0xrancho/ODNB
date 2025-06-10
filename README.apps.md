ODNB / Apps Directory

This folder contains the user-facing interfaces for ODNB. Each subfolder represents a standalone app built for a specific industry or use case.

📁 Structure

odnb/

The SMB Services interface:

Tailored for local service businesses (e.g., HVAC, Landscaping, Home Repair)

Focuses on Customer Winback, Reactivation, and Upsell

Output segments based on behavior, timing, and inferred lifecycle stage

big-loud-shirt/

The Retail & DTC demo tool:

Optimized for mid-market eCommerce and retail brands

Uses uploaded CSVs and category-level metadata

Integrates sunburst visualizations and persona-based segment drilldowns

🛠 Implementation Notes

Both apps share logic from the engine/ directory

Frontend flows for Big Loud Shirt are defined in /lovable/

Each app will load from the same schema definition and scoring engine

Eventually both can connect to hosted GPT endpoints or run inference locally

🧠 Usage Guidance

Add app-specific logic and overrides within each folder (e.g., custom tactics, prompt tweaks)

For testing segment strategies, clone either app and point to different sample CSVs

UI components should be pulled from /ui-components/ whenever possible

