# MS Design Studio & Printing POS

Offline POS system built with HTML5, CSS3 and Vanilla JavaScript. Data is stored locally in the browser using localStorage, so the app can run without internet after the files are on the PC.

## Start
1. Extract the `MS-Design-POS` folder.
2. Open `index.html` in Chrome or Edge.
3. Login with:
   - Username: `admin`
   - Password: `admin123`

For best offline/local behavior, you can also serve the folder using any simple local web server, but the application is designed to work by opening the HTML directly.

## Features
- Login
- Dashboard statistics and sales chart
- Fast POS billing and automatic invoice numbers
- Paid, Unpaid and Advance billing statuses
- Cash, Card and Bank Transfer payment methods
- Advance payments automatically keep the remaining amount as outstanding/unpaid
- Product/service management
- Stock-controlled and non-stock service items
- Inventory stock in/out/adjustment
- Customer profiles, invoice history and outstanding credit
- Printing job/order workflow and status tracking
- Expense management
- Profit and sales reports with CSV export
- Printable invoices
- Business and invoice settings
- JSON backup and restore
- Global search
- Responsive desktop/tablet/mobile interface

## Data Storage
All data is stored under the browser localStorage key `msDesignPOS_v1`. Back up regularly from **Backup & Restore**.

## Notes
- Clearing browser/site data will remove local POS data unless it has been backed up.
- Demo product prices can be edited from Products & Services.
- Invoice printing uses the browser print dialog and supports A4; thermal output depends on the selected printer/paper size in Windows.

## Report improvements
- Outstanding / unpaid invoice amount
- Cost of unpaid sales
- Today's product cost
- Today's expenses and total daily cost
- Per-invoice unpaid customer cost and gross profit
- Daily sales, product cost, expenses, total cost, outstanding and net profit breakdown

## Reports update
- Daily report opens with today's date by default.
- Type a customer name/phone/ID in Reports to see all previous invoice history, including total quantity, total amount, cost, profit, paid and outstanding.
- Full printable report includes every customer and every invoice in the selected date range with item/quantity, total amount, cost, gross profit, paid and unpaid values.
- Customer summary groups totals by customer for easier end-of-day checking.

## Branding & Invoice Update
- Upload PNG/JPG/WebP business logo from Settings. Logo is saved offline in localStorage and included in JSON backups.
- Logo can be shown/hidden and appears in the sidebar and printable invoice.
- Advanced commercial invoice template with customer block, payment status badge, totals, outstanding balance and signature area.
- Separate A4 Invoice and 80mm Thermal Receipt print buttons.

## Balance Payment & Tax Number Update
- Customers with unpaid/advance invoices now show a **Balance Payment** button.
- A later payment is recorded separately with date, customer, amount, method, note, and invoice allocations.
- Payments are automatically applied to the **oldest outstanding invoice first**.
- Fully settled invoices change to **Paid**; partially settled invoices remain **Advance** with the remaining outstanding balance.
- Customer profiles include balance payment history, total sales, total cost, gross profit, total paid, and current outstanding balance.
- Reports include balance payments received, customer, paid amount, applied invoices, lifetime customer sales, cost, gross profit, and current balance.
- Settings now include a **Tax Number / TIN / VAT Number** field.
- The tax number appears on the professional invoice and printed reports.
- Backup/restore includes balance payment records and remains compatible with older backups that do not contain a payments section.

## New Sale - Old Balance Settlement

The New Sale screen now has a **Transaction Type** selector. Choose **Pay Old Balance**, select the customer, enter the payment and save/print. The payment is applied to the oldest outstanding invoices first. The normal sales invoice is replaced by a **Balance Settlement** printout showing the old invoice numbers, bill totals, cost, profit, amount paid now, and remaining balance. Reports record the payment on the actual payment date and show the affected old bills with their total, cost and gross profit.

## Administrator Accounts

- Admin 1 — Username: `admin` / Password: `admin123`
- Admin 2 — Username: `admin 2` / Password: `Qaz@@123`

Both administrator accounts can view reports and invoices, edit invoice payment/customer details, delete invoices, and delete balance-settlement payment records. Invoice deletion requires confirmation and returns stock-controlled sold quantities to stock. Deleting a balance settlement restores the applied outstanding balances to the affected old invoices.
