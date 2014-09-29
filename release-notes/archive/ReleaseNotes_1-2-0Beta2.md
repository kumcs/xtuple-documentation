Change Log
OpenMFG
Version 1.2.0-Beta2
June 10, 2005
==================================



The following features and bug fixes have been added to the application 
since the release of version 1.2.0-Beta1:



New features:


* Added numbering to Standard Journals.
* Added Standard Journal history display/report.
* Added ability to reverse Standard Journal and Series Journal entries through a 
contextual right-click menu.
* Added G/L configuration option to make the Notes field required for all manual 
journal (G/L) entries.
* Added Distribution Date to Series Journal Entry.
* Added reason codes under A/R|Master Information for linkage to both S/O Credit
Memos and Misc. AR Credit Memos.
* Added Db/Cr sense to Adjustment Type for Bank Reconciliation.
* Consolidated Shipping/Invoicing functions on Ship order screen.
* Added Notes option on Enter PO Receipt screen.
* Added error checking to prevent receiving above PO qty.
* Added ability to print Packing Lists in batch mode by Ship Via.
* Added ability to print Invoices in batch mode by Ship Via.
* Implemented encrypted client/server connections using secure tunnel.
* Duplicated Cost Category and Expense Category under A/P|Master Information.
* Added date of last operation information on S/O|Displays|Sales Order Status.
* Modified Sales Order header to indicate if Order is converted Quote.
* Renamed POST buttons to CREATE INVOICE on Billing Selection screens.
* Added S/O configuration option enabling "SAVE AND ADD TO PACKING LIST" button 
to be visible always on Sales Order, regardless of Order status.
* Added S/O configuration option to leave "Select Order for Billing" on by default
on the Ship Order screen.
* Enabled alphanumeric Ship-Tos.
* Modified CTRL-S lookups so data is sorted by number.
* Added User Preference option to map ellipses to either search or list.
* Added option to Print Work Order Labels when printing a W/O Traveler.
* Added "At Shipping" column in S/O|Displays|Inventory Availability by Sales
Order.
* Added Customer Type information to Sales Order header


Bug Fixes:

* Fixed error with incorrect updating of W/O Material Variances.
* Fixed problem with 'Apply to Balance' calculation for A/R Misc. Credit Memos.
* Implemented Inventory/Vendor UOM ratio for PO Receiving conversions.
* Fixed problem with Ship Via not saving on Ship-To.
* Renamed Cost Category 'Labor and Overhead Clearing' to 'Labor and Overhead Costs.'
* Added missing Check Register report.
* Added subtotal to 'Other Income' section of Income Statement.
* Increased decimal precision for Lot assignments.
* Fixed problem preventing scrap of full qty. issued to Work Order.
* Fixed problem with profit and loss not displaying on Income Statement display.
* Fixed issue with 'SAVE' in Sales Order Header always incrementing Order number.
* Improved spacing of 'At Shipping' column on Issue Stock to Shipping screen.
* Improved implementation of PostARDocuments privilege.
* Fixed problem with extraneous data left from SO entry after crash.
* Fixed problem with Expense Accounts not displaying on Income Statement display.
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














