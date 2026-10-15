# Getting started with the Retail package

[← Back to contents](README.md) · [General getting started](getting-started.md)

The Abrak Retail package is built for multi-location stores, retail shops, supermarkets, and businesses running physical and online sales channels. It includes **11 integrated apps**:

- **Point of Sale** (`point_of_sale`)
- **Inventory** (`stock`)
- **Purchase** (`purchase`)
- **Barcode** (`stock_barcode`)
- **Iranian POS & Payment** (`abrak_pos_iran`)
- **Iranian Accounting** (`abrak_ir_accounting`)
- **Moadian Tax Gateway** (`abrak_odoo_moadian_pro`)
- **Torob Connector** (`abrak_torob_connector`)
- **Abrak Delivery & Fleet** (`delivery_abrak`)
- **CRM** (`crm`)
- **Sales** (`sale_management`)

Below are the first 5 concrete steps to configure your inventory, register items, set up touch point-of-sale registers, connect payment terminals, and issue compliant tax invoices.

---

## Step 1: Configure inventory, products, and barcodes

**Apps:** Inventory (`stock`) and Barcode (`stock_barcode`)  
**Menu path:** `Inventory → Products → Products`

Enter your product hierarchy and catalog baseline:

1. Navigate to `Inventory → Configuration → Product Categories` and establish your category tree (e.g., Groceries, Cleaning Supplies, Electronics). Set your inventory valuation method to Average Cost (AVCO) or FIFO.
2. Under `Inventory → Products → Products`, click **New**.
3. Set the product type to **Storable Product** so stock moves are tracked.
4. Specify sales prices and cost prices in Rials.
5. In the Barcode field, scan or enter the standard barcode (EAN-13 or national product code).
6. Click **Update Quantity** to set starting stock on hand in your primary warehouse.

> **Measurable outcome:** Products exist in the catalog with prices, cost bases, active barcodes, and initial stock quantities visible in inventory cardex reports.

---

## Step 2: Configure Point of Sale and connect Iranian bank card readers

**Apps:** Point of Sale (`point_of_sale`) and Iranian POS (`abrak_pos_iran`)  
**Menu path:** `Point of Sale → Configuration → Settings`

Set up the retail touchscreen register and integrate physical card terminals (PC-POS):

1. Go to `Point of Sale → Configuration → Point of Sale`, and open your primary shop register or create a new one.
2. Under **Payment Methods**, enable Cash and Bank Card (Iranian POS).
3. In the Iranian POS settings (`abrak_pos_iran`), select the terminal protocol (Behpardakht, Saman Kish, Sadad, or Asan Pardakht) and provide the network IP or serial port to send payment amounts directly to the card terminal.
   > **Pilot:** the bank card-terminal connection (`abrak_pos_iran`) has so far been tested only with a simulator. Connecting a real bank terminal needs a contract and certificate from your payment service provider (PSP). Until then, record card payments manually in the POS.
4. Enable cashier barcode badge login and receipt printer options.

> **Measurable outcome:** Clicking **New Session** launches the touch POS interface with products loaded and the card terminal in a ready, listening state.

---

## Step 3: Complete your first register sale, print receipt, and auto-decrement stock

**Apps:** Point of Sale (`point_of_sale`) and Inventory (`stock`)  
**Menu path:** `Point of Sale → Open Session`

Execute an end-to-end checkout cycle on the sales floor:

1. On the touch register interface, scan the product barcode using a scanner or select it directly from the screen.
2. Click **Payment** and select the Bank Card payment method.
3. The exact total is pushed to the physical card terminal; the customer swipes and enters their PIN, completing the electronic payment.
4. Click **Validate** to generate the printed receipt featuring Solar Hijri dates and bank tracking references.
5. At the end of the work shift, click **Close Register** to balance physical receipts against system totals.

> **Measurable outcome:** A printed receipt is generated with Solar Hijri dates, accounting entries for cash/bank are posted, and stock quantities are automatically decremented from the warehouse.

---

## Step 4: Issue statutory electronic invoices to the Moadian tax portal

**Apps:** Iranian Accounting (`abrak_ir_accounting`) and Moadian Gateway (`abrak_odoo_moadian_pro`)  
**Menu path:** `Accounting → Customers → Invoices`

Issue fiscal invoices complying with Iranian tax authority regulations:

1. Create a customer invoice and select a company or individual with their National ID or Economic Code.
2. Add product lines; the system retrieves 13-digit national tax commodity codes and statutory VAT rates (10%) from product defaults.
3. Click **Confirm** to post accounting journal entries.
4. Open the **Moadian** tab and click **Send to Tax Portal**.
5. The gateway signs the fiscal data payload with the company's private cryptographic key and transmits it to the state portal.

> **Measurable outcome:** The invoice status updates to "Sent / Accepted" and receives a verified 22-digit unique fiscal Tax ID.

---

## Step 5: Connect the Torob marketplace feed and delivery fleet

**Apps:** Torob Connector (`abrak_torob_connector`) and Abrak Delivery (`delivery_abrak`)  
**Menu path:** `Settings → Torob Connector` and `Inventory → Configuration → Delivery Methods`

Expand external sales channels and manage parcel fulfilment:

1. In the Torob Connector settings, copy your signed product XML/JSON feed URL and register it on your Torob merchant dashboard for real-time price and stock sync.
2. Under `Inventory → Configuration → Delivery Methods`, set up shipping options (e.g., Express Courier, Iran Post, Tipax).
3. Define pricing rules based on parcel weight or order totals.
4. On validated sales deliveries, click **Print Shipping Label** to produce transport barcodes.

> **Measurable outcome:** The signed Torob feed is validated with live stock levels synced, and standard shipping labels with tracking numbers are generated for fulfilment.

---

## Next steps

- [App catalogue](apps.md) — explore all available business applications
- [Iran localization](iran-localization.md) — Sayad cheques and statutory reporting
- [Pricing](pricing.md) — review user tiers and subscription terms
