# HomeBase

**A private, local-first home management app for homeowners.**

HomeBase keeps everything about your property in one place — appliances, maintenance schedules, documents, finances, contractors, and more. All data lives on your device. No accounts. No subscriptions. No telemetry.

---

## Features

### Property
- Store and edit full property details — address, home type, year built, square footage, purchase price and date
- Upload a photo of your home shown on the dashboard
- Manage multiple properties from one app (primary residence, rental, vacation home)

### Appliances & Systems
- Inventory of every appliance and system with make, model, serial number, and warranty expiry
- Filter size and change interval reminders
- Purchase price and installation date tracking

### Maintenance
- Task list with due dates and flexible recurrence (monthly, quarterly, semi-annual, annual)
- Completion history with cost and notes per completion
- Overdue badge in the sidebar when tasks are past due
- Weather-aware nudges — get prompted for seasonal maintenance based on local forecast

### Document Vault
- Upload and organize PDFs, images, and other files (insurance policies, permits, warranties, deeds)
- Expiry date tracking with dashboard alerts for documents expiring within 90 days
- Categorized storage (Insurance, Legal/Permits, Warranty, Manual/Specs, etc.)

### Contractors
- Contact book for every trade — HVAC, plumbing, roofing, electrical, and more
- Per-contractor job history with dates, descriptions, and costs
- "Would use again" flag to remember who you trust

### Projects
- Home improvement project log with start/end dates and total cost
- Capital improvement flagging for CPA tax basis documentation
- Permit tracking
- Project-linked document attachments

### Finances
- **Mortgage** — Loan terms, current balance, interest rate, payment tracking, refinance history
- **Property Tax** — Annual assessed value and tax records by year
- **Insurance** — Policy details, premium, coverage amounts, agent contact, claims history
- **HOA** — Association details, fee history, payment ledger, special assessment tracking
- **Utilities** — Monthly bills for electric, gas, water, internet with trend charts
- **Annual Financial Report** — Full-year summary of all home-related spending
- **Tax Basis Report** — Capital improvements summary formatted for CPA review

### Structure & Exterior
- **Rooms** — Floor plan inventory with dimensions, ceiling height, and finish/material tracking
- **Structural Components** — Roof, foundation, siding, windows, insulation — condition, age, useful life, service log
- **Exterior Features** — Deck, driveway, fencing, irrigation — condition and service history

### Emergency Preparedness
- Emergency contact list (neighbors, plumbers, electricians, HOA)
- Shutoff guide with optional photo — water main, gas, electrical panel

### Tools
- **Full-text search** — Cmd+K / Ctrl+K finds appliances, tasks, documents, contractors, and rooms across all records
- **Data export** — Export everything as a ZIP archive for backup or migration
- **Multi-property support** — Manage multiple homes from a single app

---

## Privacy

HomeBase stores all data in a SQLite database on your local machine. There are no cloud services, no analytics, no error reporting, and no network calls except optional weather lookups for maintenance nudges (Open-Meteo, open-source and privacy-respecting) and optional Google Calendar / Google Drive integrations that require explicit user authorization.

---

## Installation

Download the latest installer from the [Releases](../../releases) page.

| Platform | Installer |
|----------|-----------|
| macOS    | `.dmg`    |
| Windows  | `.msi` or `.exe` |

**Windows:** WebView2 is required. It is included on Windows 11 and most up-to-date Windows 10 installations. The installer will download it automatically if missing.

---

## License

© 2026 David Jacobus. All rights reserved.

HomeBase is proprietary software. Downloading and using the application does not grant any rights to the source code.
