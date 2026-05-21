# AI Usage Log

**Team:** Nemesis
**Product:** Nemesis — Selling tool for handmade creators

This file is updated every time AI-generated output is used in the project. It is audited at Checkpoint 3.

---

## Entry Format
Date: YYYY-MM-DD
Story: [Story ID] — [Story summary]
Tool: [Tool name]
Task: [What the AI was asked to generate or assist with]
Prompt summary: [Brief description of the prompt used]
Files changed: [List of files the AI output touched]
Result: Accepted / Modified / Discarded
Review notes: [What was checked. What was changed from AI output. Any errors or hallucinations caught.]
Reviewer: [Name]

---

## Log Entries

---
Date: 2026-05-21
Story: Lab 10 — Growth modeling deliverables
Tool: Claude (Anthropic)
Task: Build the six-month growth projection spreadsheet — team had identified acquisition channels and discussed assumptions; AI generated the full Excel model
Prompt summary: Given our 3 acquisition channels (Instagram/TikTok Organic, Craft Community Seeding, Referral Program) and product context (handmade creator selling tool, Georgian market), generate a formula-driven growth_projection.xlsx with 3 tabs (Inputs, Calculations, Outputs), 6-month cohort model, worst/expected/best scenario toggle, CAC and LTV per channel, cumulative retained users chart, and stress test
Files changed: 04-gtm/financials/growth_projection.xlsx
Result: Modified
Review notes: AI generated the full spreadsheet structure and all formulas. Channel selection verified by team against interview findings from Weeks 3–4 — Instagram/TikTok and craft communities confirmed as correct channels for Georgian handmade sellers. Conversion rate assumptions (4–12% signup, 20–50% D30 retention) cross-checked against industry benchmarks cited in unit-economics.md. ARPU set to $0 worst case reflecting MVP is currently free. Channel spend figures ($0 Instagram organic, $50 community seeding, $30 referral) confirmed as realistic for team budget. AI had no knowledge of our specific user research so team validated all assumptions against actual interview data before accepting.
Reviewer: Tamar Vatcharadze

