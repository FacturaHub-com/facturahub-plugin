---
name: invoice
description: Create and send invoices. Use when the user wants to invoice a client, create a bill, or send a factura.
---

Help the user create an invoice using the `create_invoice` tool.

Ask for the minimum information needed:
- **Client name** (or company) — if the client already exists, use their ID
- **Amount** or line items (description + amount for each)
- **Currency** (default to the user's profile currency)

Use `list_clients` first to check if the client already exists. If not, `create_invoice` will create the client automatically.

After creating the invoice, offer to:
- Send it by email with `send_invoice`
- Download the PDF with `download_pdf`
- Duplicate it later with `duplicate_invoice`

Keep it conversational. The user should be able to say "$ARGUMENTS" and get an invoice created with minimal back-and-forth.
