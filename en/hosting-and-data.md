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

## Ownership and portability

Your data is yours. Abrak is built on the open-source Odoo core rather than a closed
proprietary format, so another Odoo instance can read your export. If you decide to go
elsewhere, that is a condition of sale, not a favour.

## Hosting tiers

From shared hosting to a dedicated VPS. Which one fits depends on user count, data
volume and whether you need dedicated resources.

<https://abrak.org/hosting>

## Self-hosting

If you would rather run it yourself, Abrak's commercial modules are sold separately. In
that case upgrades, backups and monitoring are yours to run.

<https://abrak.org/apps>

## Security

- HTTPS enforced, with HSTS
- tenants isolated on their own subdomain
- standard Odoo access control (groups, record rules, model access rights)
- vulnerability reports: `admin@abrak.org` — see [SECURITY.md](../SECURITY.md)
