# Getting started

[← Back to contents](README.md)

## The seven-day trial

Sign up at <https://abrak.org/start>. The first seven days are free, **no bank card
required**, with full access to every app — not a feature-limited edition and no locked
apps. At the end of the week you decide; until then you pay nothing and can cancel at
any time.

## Your workspace

After signup, a dedicated workspace is created on your own subdomain:

```
https://<your-name>.abrak.org
```

That workspace has **its own database**. Your records do not share a table with any
other customer. This is an architectural decision rather than a setting: isolation at
the database level is what makes a full export, a restore, or a migration out possible
without touching anyone else's data.

Provisioning takes a few minutes. Nothing is installed on your computer; everything
runs in the browser.

## The first three steps

1. **Pick your apps.** You do not need to enable all of them at once. Start with
   whatever hurts today — usually accounting or CRM — and add more later. The apps
   share one data model, so switching on Inventory in month three does not orphan the
   sales data from month one.

2. **Enter your baseline.** Company details, the Solar Hijri fiscal year, currency
   (Rial), your chart of accounts, and users. If you are coming from spreadsheets or a
   legacy package, the migration guides on <https://abrak.org/blog> walk through it.

3. **Add users.** Only **internal users** count towards your bill. Suppliers, customers
   and portal users are free.

## What counts as a user

This distinction affects your bill directly:

| User type | Access | Billed? |
|---|---|---|
| Internal user | The back office, every enabled app | Yes |
| Portal user | Only their own records — invoices, orders, tickets | No |
| Customer / supplier | The same portal | No |
| Website visitor | Public pages and the shop | No |

So a shop with 5 staff and 5,000 customers pays for 5 users.

## Getting help

- **Bronze support** is included with every subscription at no extra cost.
- Faster tiers are described on the [pricing page](pricing.md).
- For on-site deployment and team training: <https://abrak.org/services/deployment>

## Next

- [The app catalogue](apps.md) — see what is available
- [Iran localization](iran-localization.md) — if statutory compliance is your concern
- [Pricing](pricing.md) — before the trial ends
