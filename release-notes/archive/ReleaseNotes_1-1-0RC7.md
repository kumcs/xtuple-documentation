Change Log
OpenMFG
Version 1.1RC7
August 26, 2004
==================================



The following features and bug fixes have been added to the application 
since the release of version 1.1RC6:


New features:


* Added greater traceability to the P/O process in the following ways: 
1. When a user is logged in, the P/O Agent will default to the 
logged-in user; 2. P/O Item changes are already recorded with comments 
listing the logged-in user in the P/O Items Comments area -- however, we 
have also added Comments functionality to the Change P/O Item Qty. screen.

* Added Tracking Number field to the Order Shipping process. With this
addition, Sales order Tracking Numbers may now be viewed in S/R | Displays 
| Shipments by Sales  Order. (Code submitted by Frank Parks of
EzBizPartner, Inc.)

* Enabled MOVE UP/MOVE DOWN buttons on Financial Layout utility.

* Added new user privilege to control access to maintenance of Uninvoiced
Receipts in P/O | Vouchers | Uninvoiced Receipts

* Disabled ability to edit Item Numbers

* Added new I/M Display/Report: Quantities on Hand by Item Group

* Returned Companies functionality to G/L | Master Information


Bug Fixes:


* Fixed problem with inability to transfer Lot/Serial qty. if not MLC
* Fixed issue with Restricted flag not working for Warehouse Locations
* Enabled deletion of Credit Memo Items
* Added logic in S/O Credit Memos to require inclusion of Customer Number
* Fixed REPLACE CHECK button on Check Run screen
* Fixed problem with P/O Item editing during P/O entry
* Fixed problem preventing users from changing their own password
* Enabled automatic screen refresh when G/L configuration changes made
* Fixed problem with negative numbers appearing in Trial Balances display
* Removed inactive Sales Reps from consideration at Sales Order entry
* Fixed Extended Costs total in S/A | Display | Sales History by Item
* Fixed S/O | Display | Partially Shipped Orders
* Fixed P/D | Displays | Indented Where Used & Indented BOM
* Removed CLOSE button from S/O Quote Line Items tab
* Fixed editing issue in A/P | Displays | Open Items by Vend. & Vend. Hist.
* Improved functionality of Pending Availability tab on S/O Item screen
* Required Tax field on Invoice to be numeric only
* Fixed Tax calculation error in A/R | Displays | Inv. Info. & Cust. Hist.
* Fixed issues when posting/updating Costs using Batch Manager
* Fixed issue with manual entry of Breeder Item # at W/O creation
* Fixed issue with create PRs from I/M | Displays | Inventory Availability
* Fixed issue with create PRs from M/S | Displays | Planned Orders by ...
* Fixed problem editing Credit Memo Items
* Removed 0 balance Items from A/R | Displays | Open Items by Cust.
* Disabled ability to assign Lot # to non-Lot-controlled qty.
* Added logic to require Expense Category for non-Inv. P/O Items
* Added logic to require Item # when entering P/O Item qty.
* Fixed screen refresh problem in P/D | Items | Search for Items
* Removed native Currency refs from Company master and G/L config
* Fixed inconsist printing issue in Customer Information report definition
