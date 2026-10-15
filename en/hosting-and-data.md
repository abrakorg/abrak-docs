# Hosting and data

[← Back to contents](README.md)

## Where data lives

On servers **inside Iran**. That is a practical choice rather than a slogan: reliable
access without depending on a foreign service, and alignment with the data-residency
requirements Iranian organisations face.

## A dedicated database

Every tenant gets its own PostgreSQL database. That means:

- your records never share a table with another customer
- restoring your backup affects nobody else
- a full export is a standard PostgreSQL operation, not a project

This differs from the shared-table multi-tenancy many cloud services run on, and the
difference shows up precisely when you want to leave.

## Backups

Automatic daily backups. For a restore, or an off-schedule copy, ask support.

## Backup restore on request

In the customer panel (`/my/apps`, backup card) every completed backup has a "request restore" button, with an optional reason. The request goes to Abrak operations; an operator approves and runs it. You are notified when the request is received and when it is done or rejected.

Before restoring, a safety backup of the current database is taken automatically, so the restore itself can be undone. Logins are paused during the restore and re-enabled after a health check; a suspended service stays suspended.

## Storage alerts

Database and file storage are measured every hour. At 90 % and 100 % of the resource package limit, the account admin and the business email receive an email (also noted in the account history) with a link to upgrade the resource package and a link to contact support. No SMS is sent. Each level is announced once and re-arms if usage drops below 70 %.

## Ownership and portability

Your data is yours. Abrak is built on the open-source Odoo core rather than a closed
proprietary format, so another Odoo instance can read your export. If you decide to go
elsewhere, that is a condition of sale, not a favour.

## Hosting tiers

From shared hosting to a dedicated VPS. Which one fits depends on user count, data
volume and whether you need dedicated resources.

The tiers open for purchase are always the ones listed on the hosting page and at
signup. When a tier is withdrawn from sale, only new customers stop seeing it: the
service you already have is never suspended, moved or downgraded, and its renewals
and support continue.

<https://abrak.org/hosting>

- For services with their own database, you can connect your own domain with an automatic certificate: [Custom domain](custom-domain.md).

## Self-hosting

If you would rather run it yourself, Abrak's commercial modules are sold separately. In
that case upgrades, backups and monitoring are yours to run.

<https://abrak.org/apps>

## Security

- HTTPS enforced, with HSTS
- tenants isolated on their own subdomain
- standard Odoo access control (groups, record rules, model access rights)
- Support agents enter without your password, for a limited time: [Secure support access](support-access.md).
- vulnerability reports: `admin@abrak.org` — see [SECURITY.md](../SECURITY.md)

