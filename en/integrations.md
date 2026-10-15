# Integrations

[← Back to contents](README.md)

## Online stores

### WooCommerce

Two-way sync between Odoo and one or more WooCommerce stores:

- products, stock, prices and orders in both directions
- automatic attribute and value mapping (colour, size), with manual pins for awkward names
- a sync queue showing each job's status and retry count
- a conflict policy for when both sides changed the same record

Step-by-step guide: <https://abrak.org/woocommerce-odoo>

### Torob

A signed official product feed from Odoo to torob.com — prices and stock update
automatically instead of by hand in a spreadsheet.

Guide: <https://abrak.org/torob-odoo>

### Instagram

Instagram Shopping does not work in Iran. The practical alternative:

- automatic product publishing from Odoo to Instagram
- product codes and a bio link that carry the visitor to a cart
- automated replies to direct messages and comments, with real funnel measurement

Guide: <https://abrak.org/instagram-shop-odoo>

## Communications

### SMS

SMS from a **Rial wallet** on a licensed domestic gateway, with no separate operator
contract. Usable from marketing automation, due-date reminders and order notifications.

<https://abrak.org/sms>

### Cloud telephony

- click-to-dial from inside CRM
- automatic call logging against the customer record
- dedicated numbers and landline service
- fax and video conferencing

Packages: <https://abrak.org/shop>

## AI

### AI gateway

Language-model access paid from a **Rial wallet**, behind an **OpenAI-compatible API** —
code written for OpenAI works by changing the base URL.

<https://abrak.org/ai>

### MCP server

MCP (Model Context Protocol) lets an AI assistant reach live system data — "what is the
stock in the Tehran warehouse", "raise the invoice for this order".

The controls Abrak puts around it:

- an API key bound to a specific Odoo user — the assistant never sees more than that
  user can
- scope, rate limit and allowed models set per key
- a tool sandbox to test before connecting a real client
- change confirmation and an audit log

Before handing a key to an assistant, read the MCP key security checklist on
<https://abrak.org/blog>.

Guide: <https://abrak.org/mcp-odoo>

## Shipping

Shipping cost calculated from destination province and parcel weight, across postal,
Tipax and courier rates. Public calculator, no signup:
<https://abrak.org/shipping/calculator>

## Attendance

Clock-in by GPS geofence, rotating QR code or messenger, wired directly into labour-law
payroll calculation.

<https://abrak.org/hr-attendance-odoo>

## Signed webhooks

Odoo's native "Send Webhook Notification" server action (usable from Automation Rules) has, on Abrak, a "webhook signing key" visible to system admins only. With a key set, every POST carries three headers:

- `X-Abrak-Event-Id`: unique per call; deduplicate on it.
- `X-Abrak-Timestamp`: Unix seconds.
- `X-Abrak-Signature: sha256=<hex>`: HMAC-SHA256 with the key over the bytes `"<timestamp>." + <raw body>`.

Receivers recompute the signature over the raw body, compare in constant time and reject calls older than about 5 minutes. Without a key, Odoo's native behaviour is unchanged.

```python
import hmac, hashlib, time

def verify(secret: str, headers: dict, raw_body: bytes, max_age=300) -> bool:
    ts = headers.get("X-Abrak-Timestamp", "")
    sig = headers.get("X-Abrak-Signature", "")
    if not ts.isdigit() or abs(time.time() - int(ts)) > max_age:
        return False
    expected = "sha256=" + hmac.new(secret.encode(), ts.encode() + b"." + raw_body,
                                    hashlib.sha256).hexdigest()
    return hmac.compare_digest(expected, sig)
```
