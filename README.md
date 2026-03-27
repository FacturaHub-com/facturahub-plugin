# FacturaHub — Claude Code Plugin

> Run your entire business from Claude. Invoices, expenses, tasks, financial reports and e-invoicing — all by talking to your AI.

[![Claude Code Plugin](https://img.shields.io/badge/Claude_Code-Plugin-7C3AED?style=for-the-badge&logo=data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMjQiIGhlaWdodD0iMjQiIHZpZXdCb3g9IjAgMCAyNCAyNCIgZmlsbD0ibm9uZSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj48cGF0aCBkPSJNMTIgMkM2LjQ4IDIgMiA2LjQ4IDIgMTJzNC40OCAxMCAxMCAxMCAxMC00LjQ4IDEwLTEwUzE3LjUyIDIgMTIgMnoiIGZpbGw9IiNmZmYiLz48L3N2Zz4=)](https://facturahub.com)
[![MCP Tools](https://img.shields.io/badge/MCP_Tools-46-10B981?style=for-the-badge)](https://facturahub.com)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](LICENSE)

## What is FacturaHub?

FacturaHub is a **Model Context Protocol (MCP) plugin** for Claude Code that turns your AI into a full business management assistant. Instead of switching between apps, just talk to Claude:

- *"Invoice Acme Corp for €2,500"*
- *"Log yesterday's €50 hosting expense"*
- *"Show me my P&L for Q1"*
- *"Assign the deploy task to Lucas, urgent"*

**46 MCP tools** handle invoicing, expenses, clients, tasks, financial reports, e-invoicing (Spain, Mexico, Colombia, Panama) and Business Memory — all from your terminal.

## Quick Install

### 1. Get your API key

Sign up free at [facturahub.com](https://facturahub.com/register) and copy your API key from the dashboard.

### 2. Set your API key

```bash
export FACTURAHUB_API_KEY=your-api-key-here
```

Add it to your `~/.zshrc` or `~/.bashrc` to persist across sessions.

### 3. Install the plugin

```bash
claude /plugin marketplace add Santy1422/facturahub-plugin
claude /plugin install facturahub@facturahub
```

That's it. Start talking to Claude about your business.

## Skills Included

| Skill | Command | What it does |
|-------|---------|-------------|
| Invoice | `/facturahub:invoice` | Create and send invoices conversationally |
| Expense | `/facturahub:expense` | Log business expenses with auto-categorization |
| Report | `/facturahub:report` | Generate P&L, tax, VAT, cash flow and income reports |
| Task | `/facturahub:task` | Create, assign, complete and manage tasks |
| Setup | `/facturahub:setup` | Configure your API key and verify connection |

## All 46 MCP Tools

### Invoicing & Clients
- `create_invoice` — Create invoices with automatic client creation
- `list_invoices` / `get_invoice` — View and search invoices
- `send_invoice` — Send invoices by email
- `mark_paid` — Mark invoices as paid
- `duplicate_invoice` — Duplicate existing invoices
- `download_pdf` — Generate professional PDF invoices
- `create_client` / `list_clients` — Manage your client database

### Expenses & Financial Reports
- `register_expense` / `delete_expense` — Track business expenses
- `get_profit_loss` — Profit & Loss statements
- `get_tax_summary` — Tax obligations by period
- `get_vat_balance` — VAT collected vs paid
- `get_income_summary` — Revenue breakdown
- `get_cashflow` — Cash flow analysis over time

### E-Invoicing (Electronic Invoicing)
**Spain (Verifactu/AEAT)**
- `validate_invoice_spain` — Validate NIF/CIF
- `generate_verifactu_qr` — AEAT verification QR codes
- `convert_to_facturae` — Facturae 3.2.2 XML
- `submit_to_hacienda` — Submit to Spanish tax authority

**Mexico (CFDI 4.0/SAT)**
- `validate_invoice_mexico` — Validate RFC
- `stamp_cfdi` — PAC stamping for SAT
- `convert_to_cfdi` — CFDI 4.0 XML generation

**Colombia (DIAN/UBL)**
- `validate_invoice_colombia` — Validate NIT
- `submit_to_dian` — Submit to DIAN
- `convert_to_ubl_dian` — UBL 2.1 XML

**Panama (DGI)**
- `validate_invoice_panama` — Validate RUC and ITBMS
- `submit_to_dgi` — Submit to DGI

### Task Management
- `create_task` / `list_tasks` / `get_my_tasks` — Create and view tasks
- `get_task_overview` — Task dashboard by status
- `assign_task` / `move_task` / `update_task` — Manage tasks
- `complete_task` / `delete_task` — Complete or remove tasks

### Business Memory (AI learns your business)
- `get_business_context` — Retrieve business knowledge
- `save_business_context` — Record business facts
- `remove_business_context` — Remove outdated info
- `save_business_summary` — Update executive summary

### Profile & Utilities
- `get_profile` / `update_profile` — Account settings
- `send_reminder` — Overdue invoice reminders
- `get_context` — Financial dashboard summary

## Alternative Setup Methods

### npx installer (Claude Desktop + Claude Code)

If you use Claude Desktop or prefer the npx approach:

```bash
npx -y facturahub setup --api-key=YOUR_API_KEY
```

This auto-detects Claude Desktop and Claude Code and configures both.

### Manual JSON config

Add this to your Claude Desktop or Claude Code config file:

```json
{
  "mcpServers": {
    "facturahub": {
      "command": "npx",
      "args": ["-y", "facturahub@latest"],
      "env": {
        "FACTURAHUB_API_KEY": "your-api-key",
        "FACTURAHUB_API_URL": "https://api.facturahub.com"
      }
    }
  }
}
```

**Config file locations:**
- Claude Desktop (Mac): `~/Library/Application Support/Claude/claude_desktop_config.json`
- Claude Desktop (Windows): `%APPDATA%\Claude\claude_desktop_config.json`
- Claude Code: `~/.claude/settings.json`

## Supported Countries

FacturaHub works in **20+ countries** with localized tax rates, currencies and e-invoicing:

🇪🇸 Spain · 🇲🇽 Mexico · 🇦🇷 Argentina · 🇨🇴 Colombia · 🇨🇱 Chile · 🇵🇪 Peru · 🇺🇾 Uruguay · 🇵🇦 Panama · 🇨🇷 Costa Rica · 🇪🇨 Ecuador · 🇩🇴 Dominican Republic · 🇧🇷 Brazil · 🇺🇸 United States · 🇬🇧 United Kingdom · 🇩🇪 Germany · 🇫🇷 France · 🇮🇹 Italy · 🇵🇹 Portugal · 🇳🇱 Netherlands

## Pricing

| Plan | Price | Includes |
|------|-------|----------|
| **Free** | $0/month | 5 invoices/month, expenses, clients, PDF, reports |
| **Solo** | $9/month | Unlimited everything, Business Memory, 46 MCP tools |
| **Pro** | $29/month | E-invoicing, API access, priority support |

Start free at [facturahub.com](https://facturahub.com/register).

## Links

- [Website](https://facturahub.com)
- [Documentation](https://facturahub.com/features/invoicing)
- [Pricing](https://facturahub.com/pricing)
- [npm package](https://www.npmjs.com/package/facturahub)

## Keywords

claude code plugin, mcp server, model context protocol, invoicing ai, ai accounting, freelancer invoicing, facturacion electronica, factura electronica, verifactu, cfdi, business management ai, claude desktop plugin, expense tracker ai, ai bookkeeping, saas invoicing, facturahub

## License

MIT
