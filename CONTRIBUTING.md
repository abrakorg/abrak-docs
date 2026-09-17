# Contributing

## What belongs here

This repository is documentation. Corrections, clearer explanations, missing steps and
translation fixes are all welcome. Product bugs belong in support, not here — write to
**admin@abrak.org** or use the contact form at <https://abrak.org/contactus>.

## Languages

The tree holds four editions:

| Directory | Language |
|---|---|
| `fa/` | فارسی — the source of truth |
| `en/` | English |
| `ar/` | العربية |
| `ps/` | پښتو |

A change to a fact (a price, a limit, a deadline) should land in Persian **and** in
every edition that repeats it, in the same pull request. A change that only fixes the
wording of one edition does not need the others.

## Writing rules

- Write what the product actually does today. If something is planned, say so.
- Keep the right-to-left editions right-to-left: do not replace Persian, Arabic or
  Pashto characters with look-alikes, and keep the zero-width non-joiner where the
  language needs it.
- Link to the live page on <https://abrak.org> rather than restating a price or a
  legal deadline that changes.
- One idea per paragraph. No marketing copy.

## Pull requests

Describe what changed and why in plain language. If you are fixing a fact, say where
you verified it.
