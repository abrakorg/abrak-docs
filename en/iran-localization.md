# Iran localization

[← Back to contents](README.md)

This is what separates Abrak from "Odoo with a Persian translation". Translation is the
easy part; matching the calendar and the law is not.

## The Jalali (Solar Hijri) calendar

Solar Hijri dates are not just a display format. In Abrak the calendar runs through:

- **Fiscal years and periods** — the year runs 1 Farvardin to 29 or 30 Esfand, not
  January to December.
- **Due dates** — cheques, invoices, instalments and reminders are stored and sorted on
  Solar Hijri dates.
- **Reports** — balance sheets, P&L and quarterly statutory reports close on Solar
  Hijri quarters.
- **Payroll** — the payroll period is a Solar Hijri month and worked days are counted
  on that basis.

Persian-Indic digits render and parse correctly in forms and reports.

### Solar Hijri dates in print and Excel

- **Printed reports (PDF)** — date and time print in Tehran time, even when the user has no time zone set in their profile. An event stored at 21:00 UTC on 20 March 2026 prints as 1 Farvardin 1405, 00:30.
- **Excel and CSV export** — in a normal export, every date or datetime column gets a Solar Hijri column next to it, titled "… (Shamsi)". The original Gregorian column stays so that sorting and filtering in Excel keep working.
- **Import-compatible export** — if you tick "import-compatible" and re-import the file into Abrak, no column is added and the file is the same as before.
- **Grouping** — group labels in a grouped export are Solar Hijri (for example "Dey 1378").

## Moadian (electronic invoicing)

Iran's tax authority requires electronic invoicing through the Moadian system. Abrak
submits invoices to the taxpayer portal from inside Odoo:

- obtain the fiscal memory ID from the portal and generate the signing key in Odoo
- complete buyer and product data to the system's requirements
- submit automatically or manually, with per-invoice status tracking
- handle type-one and type-two invoices separately

Submission deadlines and the Article 22 penalties are set in law and change. Read the
current figures on <https://abrak.org/moadian-odoo>, not from this page.

## Sayad cheques and Iranian accounting

- Incoming and outgoing cheques recorded with their Sayad identifier
- Cheque book, cheque status and automatic journal entries
- Statutory day book and general ledger on Solar Hijri dates
- Withholding tax and the Article 169 quarterly transaction report
- VAT returns
- Multi-column trial balance

## Payroll and social insurance

- Payslips following the annual Ministry of Labour rulings
- Payroll tax on that year's bracket table
- Employee and employer social insurance contributions
- The monthly insurance list and its **DBF export** for the state portal
- New-year bonus, severance, overtime and accrued leave

Tax tables and salary ceilings change every year and arrive with Abrak updates.

## Rial payment

Payment runs through an Iranian bank gateway — no international card, no FX cost.
Gateway fees and Shaparak settlement are posted to accounting and reconciled against
the bank statement.

## Where data lives

On servers inside Iran, with daily backups. See [Hosting & data](hosting-and-data.md).
