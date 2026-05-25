# HomeBase

**A private, local-first home management app for homeowners.**

HomeBase keeps everything about your property in one place — appliances, maintenance schedules, documents, finances, contractors, and more. All data lives on your device. No accounts. No subscriptions. No telemetry.

Built with [Tauri](https://tauri.app) (Rust + WebView), it runs natively on macOS and Windows as a small, fast desktop application backed by a local SQLite database.

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
- **Load / Clear test data** — Seed realistic sample data per property for evaluation, clear it when done

---

## Privacy

HomeBase stores all data in a SQLite database on your local machine. There are no cloud services, no analytics, no error reporting, and no network calls except optional weather lookups for maintenance nudges (Open-Meteo, open-source and privacy-respecting) and optional Google Calendar / Google Drive integrations that require explicit user authorization.

---

## Installation

Download the latest installer from the [Releases](../../releases) page.

| Platform | Installer |
|----------|-----------|
| macOS    | `.dmg`    |
| Windows  | `.msi` or `.exe` (NSIS) |

**Windows:** WebView2 is required. It is included on Windows 11 and most up-to-date Windows 10 installations. The installer will download it automatically if missing.

---

## Building from Source

### Prerequisites

- [Rust](https://rustup.rs) 1.77+
- [Node.js](https://nodejs.org) 20+
- Platform system libraries (see below)

**macOS**
```bash
xcode-select --install   # Xcode Command Line Tools
npm install
npm run tauri dev
```

**Linux (Ubuntu / Debian / WSL2)**
```bash
sudo apt update && sudo apt install -y \
  pkg-config build-essential libwebkit2gtk-4.1-dev \
  libssl-dev libgtk-3-dev libayatana-appindicator3-dev \
  librsvg2-dev
npm install
npm run tauri dev
```

**Windows (native — recommended)**

Open *Developer PowerShell for VS 2022*, then:
```powershell
npm install
npm run tauri dev
```

> Visual Studio Build Tools 2022 with the C++ workload must be installed before running `npm install`. See [CLAUDE.md](CLAUDE.md) for the full setup guide.

### Production build

```bash
npm run tauri build
```

Installers are written to `src-tauri/target/release/bundle/`.

---

## Tech Stack

| Layer | Technology |
|-------|-----------|
| Desktop shell | [Tauri 2](https://tauri.app) (Rust) |
| Frontend | React 18, TypeScript, Tailwind CSS |
| Data fetching | TanStack Query v5 |
| State | Zustand |
| Charts | Recharts |
| Database | SQLite via [rusqlite](https://github.com/rusqlite/rusqlite) |
| Migrations | [rusqlite_migration](https://github.com/cljoly/rusqlite_migration) |
| Build | Vite 8, esbuild/Terser |

---

## License

MIT — see [LICENSE](LICENSE) for details.
