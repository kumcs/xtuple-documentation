Changelog
OpenMFG
Version 2.1.0
May 30, 2007
==================================

The following features and bug fixes have been added to the application 
since the release of version 2.1.0-RC2:

New features:

* Added Incidents list to CRM Account screen 
* Added To-Dos tab to CRM Account master 
* Linked CRM Accounts to To-Dos 
* Added ability to see Invoice details on A/R Open Items by Customer 
display
* Added toolbar button for "Select Order for Billing" screen

Bug Fixes:

* Fixed issue where CRM Account changes weren't being propagated to 
the Customer master
* Fixed issue where S/O Line Item was showing wrong Tax Currency
* Fixed S/O Line Item Tax detail to use Order Currency not Tax 
Authority Currency
* Enabled adding To-Dos to existing Incidents
* Changed how bar codes are rendered to improve scanning
* Fixed issue where Freight Tax was not being shown in Tax detail 
until after Sales Order was saved
* Disabled "Qty. to Voucher" field on the Voucher Item screen to 
emphasize read-only usage
* Fixed Sales Order screen which was unnecessarily converting Order 
Tax Currency
* Fixed incorrect Tax Currency on Select Order for Billing screen
* Fixed improper forward-updating of Year End Equity Account
* Enabled shipping of $0 cost Items
* Enabled clearing of P/O Liability when P/O Line Items are marked as 
invoiced
* Fixed Print W/O Traveler screen to print Work Order labels for all 
released, exploded, and in-process Work Orders
* Fixed G/L Transactions display to show P/O detail when viewing a 
Voucher from right-click menu
* Fixed issue where $0 value P/O Liability transaction was posting to 
the G/L; should be hidden instead
* Enforced stricter implementation of implode/explode Work Order 
privileges
* Re-scaled OpenRPT toolbar buttons
* Fixed rounding inconsistency which could cause Invoices and A/R Open 
to disagree
* Fixed screen resizing issue on Configure W/O screen
* Prevented assignment of multiple default Ship-To Addresses
* Fixed issue where OpenRPT menus were not supported if using "Show 
windows as free-floating" preference
* Fixed image rendering issues for documents emailed through the Batch 
Manager (Mac version)
* Fixed error received when attempting to post multiple Vouchers from 
Unposted Vouchers list
* Fixed issue with Cash Receipt showing wrong Currency
* Enabled deletion of P/O Quick Entry Line Items
* Prevented scenario where Invoice screen could fail to update A/R 
open balances appropriately
* Removed unnecessary G/L impact when editing unposted Purchase Order 
Receipts
* Fixed screen resizing issue on A/P Aging screen
* Fixed screen resizing issue on Bank Reconciliation screen
* Enforced copying of Tax information when Sales Orders are copied
* Fixed error when posting Cash Receipt migrated from previous version
* Fixed incorrect Exchange Rate error at P/O Quick Entry
* Prevented incorrect duplicate Line Items on P/O Quick Entry screen
* Enforced display of preferred Warehouse on P/O Quick Entry screen
* Fixed incorrect P/O Liability amounts after posting rejected expense 
Items in multi-currency situation

PLEASE NOTE: The application-based help files have not been updated for
this release.

