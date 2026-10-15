# Getting started with the Manufacturing package

[← Back to contents](README.md) · [General getting started](getting-started.md)

The Abrak Manufacturing package is designed for production plants, industrial workshops, assembly facilities, and discrete manufacturing enterprises. It includes **14 specialized apps** spanning supply chain, MRP, quality control, maintenance, fixed assets, and statutory payroll:

- **Manufacturing / MRP** (`mrp`)
- **Product Lifecycle Management** (`mrp_plm`)
- **Quality Control** (`quality_control`)
- **Maintenance** (`maintenance`)
- **Inventory** (`stock`)
- **Purchase** (`purchase`)
- **Iranian Accounting** (`abrak_ir_accounting`)
- **Moadian Tax Gateway** (`abrak_odoo_moadian_pro`)
- **Fixed Assets** (`l10n_ir_asset`)
- **Employees / HR** (`hr`)
- **Attendance** (`hr_attendance`)
- **Iranian Payroll** (`l10n_ir_hr_payroll`)
- **Social Security Insurance** (`l10n_ir_sso_insurance`)
- **Sales** (`sale_management`)

Below are the first 5 concrete steps to configure work centers, set up Bills of Materials (BOM), define quality inspection points, execute manufacturing orders, and calculate true cost of goods manufactured.

---

## Step 1: Configure work centers and equipment maintenance schedules

**Apps:** Manufacturing (`mrp`) and Maintenance (`maintenance`)  
**Menu path:** `Manufacturing → Configuration → Work Centers`

Set up shop floor workstations, machinery, and cost overheads:

1. Under `Manufacturing → Configuration → Work Centers`, click **New** to define physical production stations (e.g., Cutting, Stamping, Assembly, Packaging).
2. Set working capacity, operational hours, and the **hourly costing rate (Cost per hour)** in Rials to account for machine depreciation and power overheads in finished goods valuation.
3. Open the **Maintenance** app (`Maintenance → Equipments`), register machinery, and assign each machine to its corresponding work center.
4. Schedule Preventive Maintenance (PM) intervals to avoid unexpected line downtime.

> **Measurable outcome:** Work centers are active with defined hourly operating cost rates, assigned machinery records, and preventive maintenance calendars.

---

## Step 2: Build Bills of Materials (BOM) and enable PLM versioning

**Apps:** Manufacturing (`mrp`) and Product Lifecycle Management (`mrp_plm`)  
**Menu path:** `Manufacturing → Products → Bills of Materials`

Specify components, quantities, and operational routings:

1. Navigate to `Manufacturing → Products → Bills of Materials` and create a BOM for your manufactured product.
2. In the **Components** tab, list all raw materials and consumable components required per unit (deducted from `stock`).
3. In the **Operations** tab, attach step-by-step routing instructions to specific work centers (e.g., 10 minutes at Cutting, 15 minutes at Assembly).
4. Use **PLM** to manage Engineering Change Orders (ECOs) whenever technical specifications or component formulations change, archiving historical versions with engineering approval logs.

> **Measurable outcome:** An approved Version 1.0 BOM is saved with bill of materials ratios, anticipated scrap percentages, and verified routing operations.

---

## Step 3: Establish Quality Control Points (QCP) on the shop floor

**Apps:** Quality Control (`quality_control`)  
**Menu path:** `Quality → Quality Control → Control Points`

Ensure strict compliance with quality criteria during manufacturing:

1. Go to `Quality → Control Points` and click **New**.
2. Select the trigger event: either upon incoming receipt of raw materials or during manufacturing operations at a specific work center.
3. Set the test type: Pass/Fail check, numerical measurement with min/max tolerance boundaries, or mandatory photo documentation.
4. Provide instructions and standard operating procedure notes for shop inspectors.

> **Measurable outcome:** A quality gate is enforced; shop floor operators cannot validate or complete work orders without completing and passing the quality check form.

---

## Step 4: Release and execute a Manufacturing Order (MO)

**Apps:** Manufacturing (`mrp`) and Inventory (`stock`)  
**Menu path:** `Manufacturing → Operations → Manufacturing Orders`

Execute a production run converting raw materials into finished stock:

1. In `Manufacturing Orders`, click **New**, select the product, and specify the target quantity. The BOM and routing automatically populate.
2. Click **Confirm** to check stock availability and reserve raw materials.
3. Click **Work Orders**, allowing operators to click **Start** at their workstation to track real-time labor duration.
4. Complete the required quality inspection check.
5. Once all steps finish, click **Produce All** to finalize the order.

> **Measurable outcome:** Raw materials are deducted from inventory, finished goods are added to product stock, and stock move records reflect physical movement.

---

## Step 5: Analyze unit cost and integrate shop floor payroll

**Apps:** Iranian Payroll (`l10n_ir_hr_payroll`) and Iranian Accounting (`abrak_ir_accounting`)  
**Menu path:** `Manufacturing → Reporting → Cost Analysis` and `Payroll → Payslips`

Measure production costs and account for direct labor and social insurance:

1. On the completed Manufacturing Order, click **Cost Analysis** to inspect the breakdown between raw material costs, machine overheads, and labor hours.
2. Track plant worker shifts and clock-in events through **Attendance** (`hr_attendance`).
3. Under `Payroll → Payslips`, compute monthly wages adhering to Ministry of Labour statutory wage bases, overtime, and housing allowances.
4. Export statutory DBF diskette files for Social Security Insurance (`l10n_ir_sso_insurance`) and record direct labor payroll journals into manufacturing work-in-progress (WIP) accounts.

> **Measurable outcome:** Accurate finished goods unit costs are established combining direct materials, direct labor, and machine overheads, seamlessly reflected in general ledger balance sheets.

---

## Next steps

- [App catalogue](apps.md) — review maintenance, quality, and supply apps
- [Iran localization](iran-localization.md) — statutory payroll and tax compliance
- [Pricing](pricing.md) — explore per-user plans and deployment options
