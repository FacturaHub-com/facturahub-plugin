---
name: report
description: Generate financial reports. Use when the user asks about profits, losses, taxes, VAT, cash flow, income, or financial summary.
---

Generate the appropriate financial report based on "$ARGUMENTS".

Available reports:
- **P&L / Profit & Loss**: Use `get_profit_loss` — shows income vs expenses
- **Tax summary**: Use `get_tax_summary` — tax obligations by period
- **VAT balance**: Use `get_vat_balance` — VAT collected vs paid
- **Income summary**: Use `get_income_summary` — revenue breakdown
- **Cash flow**: Use `get_cashflow` — money in vs money out over time
- **General overview**: Use `get_context` — dashboard-style summary

If the user doesn't specify which report, start with `get_context` for a general overview, then suggest specific reports based on what they might need.

Present numbers clearly with currency formatting. Highlight key insights (e.g., "Your expenses are 40% higher than last month").
