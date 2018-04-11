Change Log
OpenMFG
Version 1.2.0
August 22, 2005
==================================



The following list includes all the features and bug fixes added to 
the application since the release of version 1.1.5. Each feature and
bug fix is listed beneath the minor release where it first appeared:



OpenMFG - 1.2.0-Final
======================

New Features:


* Enhanced Ship Vias to provide improved shipment tracking with links 
to selected shipping company websites.
* Added ability to add Freight by PO Line Item, including ability to
to Voucher and also correct PO Line Item Freight. 
* Added two S/O Displays: Quote Lookup by Item & Customer.
* Added date ranges to S/O Display/Report Sales Order Lookup by Item.
* Modified P/O Display/Report Items by Vendor to allow selection by 
internal P/O number.
* Renamed "Account Numbers" in G/L | Master Information to "Chart of 
Accounts."
* Enabled alternate A/R Account Assignments when entering Cash Receipts 
or Miscellaneous A/R Credit Memos.
* Expanded Search for Customer functionality in S/O | Master Information.
* Enabled batching of Cash Receipts to enhance Bank Reconciliations.
* Added ability to specify default selling Item Site on Customer master. 
* Enabled Sales Order Item notes to transfer to associated Work Order.


Bug Fixes:


* Fixed error with Correct Receiving information not populating in P/O |
Vouchers | Uninvoiced Receipts.
* Fixed problem with improper posting of unapplied Cash Receipts.
* Removed the following unused fields from PO Item screen: Vendor Qty. 
Ordered and Vendor Unit Price.
* Moved Update Credit Status by Customer" to S/O | Utilities.
* Fixed problem tabbing to EDI Cc: field.
* Fixed problem so Standard Operations fields accept values < 1.00.
* Fixed problem with display on Fixed Assets in Balance Sheet display.
* Fixed problem with "Copy to Ship-to" button on SO header screen.
* Prevented Financial Layout from allowing duplicate Account Numbers by
default.
* Fixed problem with Lot/Serial control when posting negative Miscellaneous 
Production.
* Fixed Batch Manager issue when submitting Actual Cost updates.
* Fixed rounding error in Discount % field on SO Item screen.
* Enabled consolidation of Billing Selections made on same day.


OpenMFG - 1.2.0RC1 
====================

New features:


* Expanded EDI export functionality, including support for customizable 
EDI Forms and both email and ftp transmission methods.
* Added "Cc:" field to EDI tab on Customer master.
* Enabled auto-updating of Actual Costs for purchased Items at Post 
Vouchers. NOTE: This is the new default behavior and is not configurable.
* Added Order interval parameter to Item Site, allowing for grouping of 
MRP Orders.
* Changed titles of Create Planned Replenishment Order screens to "Run 
MRP".
* Added Indented BOM option to Pending Availability tab on Sales Order 
Item  screen.
* Added ability to add Freight by Line Item on Purchase Order Item screen.
* Added Pricing Schedule Assignment by Customer Ship-To.
* Added ability to take Price Discounts based on payment Terms specified 
on Voucher. Discounts may be applied when Voucher is selected for payment. 
* Added Discount Account option to A/P Account Assignments for handling 
payment Discounts.
* Added date criteria on Select Payments screen.
* Added option on S/R|Shipping|Issue Stock to Shipping to disallow issuance 
of stock if Inventory is below order quantity.
* Added error checking for receiving above Purchase Order quantity.
* Added privilege removing ability of user to edit Unit Price at Sales 
Order Item.
* Added privilege restricting ability to edit Select Order for Billing.
* Added privilege restricting ability to assign Customer Type on Customer 
master.
* Added privilege to prevent certain users from viewing Uninvoiced Receipts.
* Added Notes information in several G/L displays.
* Added more window closing options under Window menu.
* Added procedure ensuring a user name is associated with every transaction 
to hit the G/L.
* Added new G/L Display: Daily Invoice G/L Transactions.
* Enabled ability to assign same Lot# to all Line Items on a received PO.
* Added ability to assign a non-default Prepaid Account when entering Misc. 
A/R Credit and Debit Memos.
* Added Prepaid and A/R Account options to Sales Categories.
* Added SUBMIT button to Post Invoices screen.
* Added Expense Categories option to Miscellaneous Vouchers.
* Added Reason Code option at Line Item level for S/O Credit Memos.
* Added ability to search for ranges of Journal numbers in G/L|Displays|G/L 
Series.
* Added additional CTRL-S functionality when searching Customer 
information.


Bug Fixes:


* Fixed problem in MRP where past requirements were not being netted 
properly.
* Fixed MRP problem with fractional Planned Order quantity being generated.
* Fixed problems with Trial Balances.
* Fixed problem with debit/credit reversal on A/R Asset Account.
* Fixed focus problem in Financial Layout editor.
* Fixed billing problem where partially shipped Orders were being closed 
before full Order quantity had been shipped.
* Corrected incorrect display of Order parameters in I/M Availability 
displays.
* Added Standard Journal History report definition.
* Added Daily Invoice G/L Transactions report definition.
* Enabled Packing List option on Print Traveler.
* Fixed problem with certain Sales Orders not deleting.
* Fixed problem with BOO screen not remaining open after saving.
* Removed non-functional "Send Advanced Shipping Notices" option from 
Customer Ship-To screen.


OpenMFG - 1.2.0Beta2
====================

New features:


* Added numbering to Standard Journals.
* Added Standard Journal history display/report.
* Added ability to reverse Standard Journal and Series Journal entries 
through a contextual right-click menu.
* Added G/L configuration option to make the Notes field required for all 
manual journal (G/L) entries.
* Added Distribution Date to Series Journal Entry.
* Added reason codes under A/R|Master Information for linkage to both S/O 
Credit Memos and Misc. AR Credit Memos.
* Added Db/Cr sense to Adjustment Type for Bank Reconciliation.
* Consolidated Shipping/Invoicing functions on Ship order screen.
* Added Notes option on Enter PO Receipt screen.
* Added error checking to prevent receiving above PO qty.
* Added ability to print Packing Lists in batch mode by Ship Via.
* Added ability to print Invoices in batch mode by Ship Via.
* Implemented encrypted client/server connections using secure tunnel.
* Duplicated Cost Category and Expense Category under A/P|Master 
Information.
* Added date of last operation information on S/O|Displays|Sales Order 
Status.
* Modified Sales Order header to indicate if Order is converted Quote.
* Renamed POST buttons to CREATE INVOICE on Billing Selection screens.
* Added S/O configuration option enabling "SAVE AND ADD TO PACKING LIST" 
button to be visible always on Sales Order, regardless of Order status.
* Added S/O configuration option to leave "Select Order for Billing" on 
by default on the Ship Order screen.
* Enabled alphanumeric Ship-Tos.
* Modified CTRL-S lookups so data is sorted by number.
* Added User Preference option to map ellipses to either search or list.
* Added option to Print Work Order Labels when printing a W/O Traveler.
* Added "At Shipping" column in S/O|Displays|Inventory Availability by 
Sales Order.
* Added Customer Type information to Sales Order header


Bug Fixes:


* Fixed error with incorrect updating of W/O Material Variances.
* Fixed problem with 'Apply to Balance' calculation for A/R Misc. Credit 
Memos.
* Implemented Inventory/Vendor UOM ratio for PO Receiving conversions.
* Fixed problem with Ship Via not saving on Ship-To.
* Renamed Cost Category 'Labor and Overhead Clearing' to 'Labor and 
Overhead Costs.'
* Added missing Check Register report.
* Added subtotal to 'Other Income' section of Income Statement.
* Increased decimal precision for Lot assignments.
* Fixed problem preventing scrap of full qty. issued to Work Order.
* Fixed problem with profit and loss not displaying on Income Statement 
display.
* Fixed issue with 'SAVE' in Sales Order Header always incrementing Order 
number.
* Improved spacing of 'At Shipping' column on Issue Stock to Shipping 
screen.
* Improved implementation of PostARDocuments privilege.
* Fixed problem with extraneous data left from SO entry after crash.
* Fixed problem with Expense Accounts not displaying on Income Statement 
display.
* Enabled printing of BOM for purchased items.
* Prevented MRP from creating Planned Orders for Inactive Items.
* Fixed problem when updating price of SO Line Item.
* Fixed updating of Sales Order Pack Date.
* Fixed odd focus shift on Bank Reconciliation screen.
* Fixed multiple miscellaneous errors on the Income Statement display.
* Enabled Reference # posting with Voucher.
* Fixed reversed transaction detail on Inventory Transaction screen.
* Enabled editing of Invoice Ship-To.
* Enabled editing of Invoice Bill-To.
* Enabled editing of Sales Order Ship-To.
* Added Supplying Warehouse requirement at PO Item.
* Fixed problem with Summarized BOM display.
* Fixed problem with unclear values in Purchase Price Variance displays.
* Enabled Serial # printing on Invoice.


OpenMFG - 1.2.0Beta1
====================

New features:


* Added Standard Journal History display.
* Added ability to reverse Standard Journal and Standard Journal Group
postings. Reversing entries can be made from the relevant Post screens
and also from the right-click menus in G/L|Displays|Standard Journal
History, G/L|Displays|G/L Series.
* Added configuration option in System|Configure G/L to make Notes
required for Journal entries if desired.
* Added Search for Document capability on Cash Receipts screen.
* Improved ability to find and load language files used when translating
OpenMFG screens into other languages.
* Add requirement to Bank Reconciliation requiring a difference of '0'
before users may post a reconciliation.
* Added ability to search for Item Aliases generically, instead of by
exact match.


Bug Fixes:


* Fixed problem causing error message when posting Count Tags by Class
Code.
* Fixed rounding error for Work Order qty. having more than 4 places of
decimal precision.
* Fixed problem with View Work Order option in contextual menu of Item
Allocations screen. 
* Prevented closed Sales Order Items from being selected for billing.
* Fixed problem with Notes not saving on Standard Journal entries.
* Made default print qty. = 1 when printing Pick Lists.
* Fixed problem with Document # not saving on Bill of Operations (BOO) 
header.
* Removed non-functional "Allow Pull Through" flag on BOO Item screen.
* Fixed problem with printing of multiple Count Tag Edit List pages from 
the display screen.


OpenMFG - 1.2.0Alpha
====================

New features:


* Added Bank Reconciliation functionality in G/L|Bank Reconciliation.
* Added a Check Register in AP|Displays/Reports.
* Added the following financial displays/reports in G/L|Financial Reports: 
Balance Sheet and Income Statement.
* Improved the Financial Layout tool to include subtotals and totals.
* Enhanced Tax Codes to support three levels of Tax Rates.
* Added links for viewing Tax details on all relevant billing screens 
(e.g., Invoice, Credit Memo, etc.).
* Added Accounting Year Periods in G/L|Master Information to facilitate
year-end closings.
* Updated G/L configuration to allow for assignment of year-end closing
Account in System|Configure Modules|Configure G/L


OpenMFG - 1.1.7 (Limited Release)
====================

New features:


* Added Enhanced Authentication security functionality.


Bug Fixes:


* Fixed rounding error when distributing fractional quantities requiring
more than 2 places of decimal precision.


OpenMFG - 1.1.6 (Limited Release)
====================


New features:


* Removed multiple print dialogs when printing Check Runs; also added 
functionality to review Check Runs when printing errors occur.  
* Added "Running Availability" option to following P/O Displays: PO
Items by Date, PO Items by Item, PO Items by Vendor (Ref. Frank 
Parks).


Bug Fixes:


* Fixed problem with Tax calculations being off by one penny in certain
situations.

