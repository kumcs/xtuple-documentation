Change Log
OpenMFG
Version 1.1.1
November 15, 2004
==================================



The following features and bug fixes have been added to the application 
since the release of version 1.1:


New features:


* Added "Disable Export Display Contents" option to Maintain User screen.
  This privilege can be used to block users from having access to the
  Export Contents functionality.

* Added new privileges to improve security in A/P and A/R Modules.

* Added VIEW DETAILS button to Invoice Information screen found in A/R |
  Displays | Invoice Information

* Added Subaccount Types to G/L | Master Information.



Bug Fixes:


* Fixed "May Overlap with Preceding Operation" flag on the BOO Item
  screen. If selected, Operation may begin at any time. If not selected,
  Operation may not begin until preceding Operation has completed.
* Fixed loopholes for users assigned no privileges.
* Fixed error where users could delete a WO Material Requirement issued
  to a Work Order.
* Fixed inconsistencies in Billing Selection process.
* Fixed print Pick List to include Work Orders having Released ("R")
  status* Made sort order parallel for Financial Layout and Preview Financial 
  Report.
* Fixed problem with Work Orders created from Sales Orders not being
  created in "Supplied at" Warehouses.
* Fixed problem with Asset and Expense Account Type values being reversed
  in Trial Balance report.
* Fixed problem where Items without a "Sold from" Item Site could be
  selected at Sales Order entry.
* Fixed problem with Location information not saving on Count Slips.
* Clarified error message at post Count Tags when improperly counted
  Lot/Serial or MLC Items exist.
* Fixed issue with "Before" qty. not displaying on Expense transaction
* Fixed problem with copy Pricing Schedule function.
* Fixed problem where system allowed Returns in excess of qty. Received.
* Prevented duplicate Item Sources.


