Change Log
OpenMFG
Version 1.2.0-RC1
July 21, 2005
==================================



The following features and bug fixes have been added to the application 
since the release of version 1.2.0-Beta2:



New features:


* Expanded EDI export functionality, including support for customizable EDI Forms
and both email and ftp transmission methods.
* Add "Cc:" field to EDI tab on Customer master.
* Enabled auto-updating of Actual Costs for purchased Items at Post Vouchers. NOTE: This
is the new default behavior and is not configurable.
* Added Order interval parameter to Item Site, allowing for grouping of MRP Orders.
* Changed titles of Create Planned Replenishment Order screens to "Run MRP".
* Added Indented BOM option to Pending Availability tab on Sales Order Item screen.
* Added ability to add Freight by Line Item on Purchase Order Item screen.
* Added Pricing Schedule Assignment by Customer Ship-To.
* Added ability to take Price Discounts based on payment Terms specified on Voucher.
Discounts may be applied when Voucher is selected for payment. 
* Added Discount Account option to A/P Account Assignments for handling payment
Discounts.
* Added date criteria on Select Payments screen.
* Added option on S/R|Shipping|Issue Stock to Shipping to disallow issuance of stock if 
Inventory is below order quantity.
* Added error checking for receiving above Purchase Order quantity.
* Added privilege removing ability of user to edit Unit Price at Sales Order Item.
* Added privilege restricting ability to edit Select Order for Billing.
* Added privilege restricting ability to assign Customer Type on Customer master.
* Added privilege to prevent certain users from viewing Uninvoiced Receipts.
* Added Notes information in several G/L displays.
* Added more window closing options under Window menu.
* Added procedure ensuring a user name is associated with every transaction to hit the
G/L.
* Added new G/L Display: Daily Invoice G/L Transactions.
* Enabled ability to assign same Lot# to all Line Items on a received PO.
* Added ability to assign a non-default Prepaid Account when entering Misc. A/R 
Credit and Debit Memos.
* Added Prepaid and A/R Account options to Sales Categories.
* Added SUBMIT button to Post Invoices screen.
* Added Expense Categories option to Miscellaneous Vouchers.
* Added Reason Code option at Line Item level for S/O Credit Memos.
* Added ability to search for ranges of Journal numbers in G/L|Displays|G/L Series.
* Added additional CTRL-S functionality when searching Customer information.



Bug Fixes:

* Fixed problem in MRP where past requirements were not being netted properly.
* Fixed MRP problem with fractional Planned Order quantity being generated.
* Fixed problems with Trial Balances.
* Fixed problem with debit/credit reversal on A/R Asset Account.
* Fixed focus problem in Financial Layout editor.
* Fixed billing problem where partially shipped Orders were being closed before full
Order quantity had been shipped.
* Corrected incorrect display of Order parameters in I/M Availability displays.
* Added Standard Journal History report definition.
* Added Daily Invoice G/L Transactions report definition.
* Enabled Packing List option on Print Traveler.
* Fixed problem with certain Sales Orders not deleting.
* Fixed problem with BOO screen not remaining open after saving.
* Removed non-functional "Send Advanced Shipping Notices" option from Customer Ship-To 
screen.