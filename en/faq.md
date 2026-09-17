# Frequently asked questions

[← Back to contents](README.md)

### What is Abrak?

A cloud ERP platform built on Odoo and localized for Iran: the Jalali calendar, a
right-to-left Persian interface, Rial payment and hosting on servers inside the country.

### Is Abrak a fork of Odoo?

No. It runs the real Odoo 19 core. Abrak's modules sit on top of it rather than
replacing it, so upstream Odoo updates reach you and general Odoo knowledge applies to
your system.

### How does pricing work?

Per internal user, not per app. The standard plan gives access to every app. Customers
and portal users are not counted. See [Pricing](pricing.md).

### Is the trial really free? Does it need a card?

Yes, and no card is required. You get full access to every app and decide at the end of
the seven days.

### How long does setup take?

A few minutes. A dedicated workspace is provisioned on your own subdomain. Nothing is
installed on your computer.

### Where is my data stored?

On servers inside Iran, with daily backups and a dedicated database per tenant.
See [Hosting & data](hosting-and-data.md).

### If I leave, can I take my data?

Yes. The database is standard PostgreSQL running the standard Odoo schema, not a closed
proprietary format.

### How is this different from installing Odoo myself?

A bare Odoo install needs a server, an administrator and ongoing maintenance, and it
has no Jalali calendar, no Rial payment and no compliance with Moadian or Iranian
labour law. Abrak delivers the same open-source core, ready to use.

### Does it work with the Moadian system?

Yes — electronic invoices are submitted to the tax portal from inside Odoo, with status
tracking. See [Iran localization](iran-localization.md).

### What about Sayad cheques and statutory ledgers?

Supported: cheques recorded with their Sayad identifier, cheque books, automatic journal
entries, day book and general ledger on Solar Hijri dates, Article 169 and VAT returns.

### Does it calculate payroll and insurance?

Yes, following the annual Ministry of Labour rulings, with the monthly insurance list
and the DBF export for the social-insurance portal.

### I have a WooCommerce store. Do I have to migrate?

Not necessarily. The WooCommerce connector syncs products, stock, prices and orders in
both directions and your store stays where it is. See [Integrations](integrations.md).

### How does AI connect to my data?

Through the MCP server, using an API key bound to one specific Odoo user. The assistant
sees no more than that user can, and the key carries a scope, a rate limit and an audit
log.

### Is support free?

Bronze support — a first response within 24 working hours — is included with every
subscription. Faster tiers are bought separately. See [Pricing](pricing.md).

### Which languages are supported?

The interface is Persian and English. This documentation is published in Persian,
English, Arabic and Pashto.

### Another question?

<https://abrak.org/contactus> · `admin@abrak.org`
