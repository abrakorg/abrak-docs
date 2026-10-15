# Getting started with the Services & Projects package

[← Back to contents](README.md) · [General getting started](getting-started.md)

The Abrak Services & Projects package is built for engineering consultancies, software houses, contractor firms, technical service agencies, and project-driven teams. It includes **12 integrated apps** covering project management, timesheets, field dispatch, ticketing, digital documentation, and recurring billing:

- **Project** (`project`)
- **Timesheets** (`timesheet_grid`)
- **Helpdesk** (`helpdesk`)
- **Field Service** (`industry_fsm`)
- **Sales** (`sale_management`)
- **CRM** (`crm`)
- **Subscriptions** (`sale_subscription`)
- **Documents** (`documents`)
- **Sign** (`sign`)
- **Knowledge** (`knowledge`)
- **Iranian Accounting** (`abrak_ir_accounting`)
- **Moadian Tax Gateway** (`abrak_odoo_moadian_pro`)

Below are the first 5 concrete steps to configure your project workflows, log team timesheets, dispatch field service technicians with electronic signatures, manage helpdesk SLAs, and issue recurring invoices.

---

## Step 1: Set up project workflows, milestones, and task boards

**Apps:** Project (`project`)  
**Menu path:** `Project → Configuration → Projects`

Organize client deliverables and team workloads:

1. Under `Project → Configuration → Projects`, click **New** to create a client engagement (e.g., Client Alpha System Implementation).
2. Configure pipeline stages on the Kanban view (e.g., Backlog, In Progress, Review, Completed).
3. Enable **Timesheets** and **Milestones** in project settings.
4. Add project tasks with assigned owners, Solar Hijri deadlines, and Planned Hours estimates.

> **Measurable outcome:** An active project is visible on the Kanban board with decomposed work breakdown tasks, deadlines, and assigned team members.

---

## Step 2: Log and validate team timesheets

**Apps:** Timesheets (`timesheet_grid`)  
**Menu path:** `Timesheets → My Timesheets`

Capture billable client hours and engineer activities:

1. Team members working on tasks can trigger the **Start Timer** widget directly within task cards for live duration tracking.
2. At the end of a shift or assignment, the timer is stopped and descriptive work notes are logged.
3. In the **Grid View**, project managers review aggregate weekly hours and click **Validate** to approve submissions.
4. Approved timesheets link directly to sales orders for accurate billing.

> **Measurable outcome:** Weekly timesheet entries are formally approved by project managers, with hours accurately allocated per project and task.

---

## Step 3: Dispatch field service technicians with on-site digital signatures

**Apps:** Field Service (`industry_fsm`) and Sign (`sign`)  
**Menu path:** `Field Service → My Tasks`

Manage on-site installations, repairs, and technical visits:

1. In the **Field Service** app, dispatch tasks are scheduled with client site addresses and contact details.
2. Field technicians view assigned work orders on mobile or tablet browsers and tap **Start**.
3. During the on-site visit, technicians record replacement parts consumed and additional services performed.
4. Tap **Sign** to hand the mobile device to the client to capture their legal digital signature.
5. The signed service delivery report is generated as an immutable PDF and stored in the **Documents** app (`documents`).

> **Measurable outcome:** The on-site intervention report is finalized with GPS timestamps, parts consumed, and the client's verified digital signature.

---

## Step 4: Configure Helpdesk support teams, SLAs, and Knowledge bases

**Apps:** Helpdesk (`helpdesk`) and Knowledge (`knowledge`)  
**Menu path:** `Helpdesk → Tickets`

Deliver post-implementation support adhering to contracted service levels:

1. Under `Helpdesk → Configuration → Helpdesk Teams`, set up support channels (email alias, web portal form, or live chat).
2. Define **SLA Policies** (e.g., First Response within 2 hours, Urgent Resolution within 8 hours).
3. Author standard operating articles in the **Knowledge** app (`knowledge`) for rapid one-click canned replies.
4. Support agents receive incoming tickets, resolve issues, and trigger automatic customer satisfaction surveys.

> **Measurable outcome:** Customer tickets are tracked against strict SLA countdown clocks, with resolution times logged in operational performance dashboards.

---

## Step 5: Automate recurring subscriptions and issue Moadian tax invoices

**Apps:** Subscriptions (`sale_subscription`), Iranian Accounting (`abrak_ir_accounting`), and Moadian (`abrak_odoo_moadian_pro`)  
**Menu path:** `Subscriptions → Subscriptions` and `Accounting → Customers → Invoices`

Convert delivered services and ongoing maintenance contracts into revenue:

1. In the Subscriptions module, establish recurring service contracts (monthly retainer or annual maintenance) with automated renewal cycles.
2. For time-and-materials projects, generate invoices directly from verified timesheet hours.
3. Confirm invoices in Iranian Accounting to generate general ledger entries in Rials.
4. Under the **Moadian** tab, click **Send to Tax Portal** to transmit digitally signed electronic invoices to the national tax registry.

> **Measurable outcome:** Invoices are automatically generated on contract schedule, accounting entries are posted, and valid 22-digit fiscal tax IDs are retrieved.

---

## Next steps

- [App catalogue](apps.md) — explore document management, collaboration, and CRM tools
- [Integrations](integrations.md) — connect VoIP telephony, SMS gateways, and AI/MCP
- [Pricing](pricing.md) — check internal user rates and support plans
