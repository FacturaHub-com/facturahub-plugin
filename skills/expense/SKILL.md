---
name: expense
description: Log business expenses. Use when the user mentions a purchase, cost, bill they paid, subscription, or business expense.
---

Help the user register an expense using the `register_expense` tool.

Extract from "$ARGUMENTS":
- **Description** — what was purchased
- **Amount** — how much it cost
- **Category** — infer from context (office, software, travel, meals, marketing, professional_services, utilities, other)
- **Date** — today if not specified

If the user provides a simple statement like "Paid €50 for hosting", extract all fields automatically and create the expense without asking unnecessary questions.

After registering, confirm the expense was logged with the amount and category.
