Change Log
OpenMFG
Version 2.0.1
December 11, 2006
==================================



The following features and bug fixes have been added to the application 
since the release of version 2.0.0:


New features:

* Added ability to copy posted Purchase Orders from PO|Displays|P/O 
History, effectively enabling users to create template POs 
* Added ability to edit posted Purchase Orders from List Unposted 
Purchase Orders screen. This new functionality permits users to add 
Line Items to posted POs, change prices, and more.
* Added RECEIVE ALL option to SR|Receiving|Enter Receipt
* Added new error checking to prevent users from posting transactions 
into closed Accounting Periods for Accounts marked to disallow this 
practice
* Added distribution date field to the Check Register so users may 
specify when they want a posted Check to be voided
* Added SO configuration options for handling the recalculation of 
Item Prices on Sales Orders when Order quantities are changed
* Added ability to customize column header text when displaying or 
printing Financial Reports
* Added ability to customize the text used for Group subtotals when 
displaying or printing Financial Reports
* Added support to OpenRPT for new label size: CILS ALP1-9200-1
* Updated Project Management display "Order Activity by Project" 
to calculate Profit/Loss 
* Added System Events for CRM
* Added new CRM display "Incidents by CRM Account" 
* Added Country table for use by the CRM Address cluster
* Added Item Price lookup on Credit Memo Item screen for scenarios 
when Credit Memo has no Apply-To document

Bug Fixes:

* Fixed issue where Tax was not being automatically recalculated 
after Invoices were edited
* Fixed issue where Tax on Invoices was being calculated for the 
total, not just the taxable subtotal 
* Fixed issue where Sales Orders could be deleted in multi-user 
environment after Line Items had been shipped
* Fixed issue where Vouchers selected for payment could have Credit 
Memos applied to them
* Fixed issues with report definition layouts and font sizes related 
to Qt 4 conversion
* Prevented users from posting a $0 amount when applying AR Credit 
Memos to open Invoices
* Prevented users from issuing stock to Shipping for canceled Line 
Items 
* Enabled Document # information to be passed as Reference 
information in G/L displays and reports when posting Misc. Production
* Fixed issue where CRM Account Name and Number were not being 
passed to new Customer masters
* Modified accounting of PO Clearing to honor Account balance at 
the time of receipt; this change ensures the PO Clearing Account will 
balance properly in scenario where Standard Costs are changed after 
receipt, but before vouchering
* Fixed issue where forecast requirements were being generated for 
expired components on a Planning Item's Bill of Materials 
* Fixed issue with "Selected Module" filter not working properly 
in several G/L displays
* Fixed issue where Ship Date and Invoice Date were being reversed 
on the Invoice Information screen
* Fixed issue where negative values could not be entered in the 
Opening and Ending Balance fields of the Bank Reconciliation screen
* Added Difference and Custom column support when displaying 
Financial Reports
* Fixed issue where Doc Type was not being passed to the G/L displays 
when entering multiple Simple Journal Entries without closing the 
entry screen 
* Fixed Item Cluster to support drag-and-drop functionality
* Added index to improve performance when scanning UPC barcodes 
into Issue Stock to Shipping screen
* Added index to improve performance when "Create and Print Invoices" 
option is selected on Ship Order screen 
* Added index to improve delays occasionally experienced after 
selecting the NEW button on the Sales Order Line Items tab
* Added index to improve performance when selecting the ISSUE ALL 
BALANCE button on the Issue Stock to Shipping screen
* Fixed issue with landscape orientation preference not being 
honored for multi-print reports under Mac
* Fixed issues with Running Availability report not matching displayed
information 
* Expanded allowable number of characters for To-Do Item sequence 
numbers 
* Made Notes on Customer Information Workbench read-only
* Fixed misaligned column on Sales Order Credit Memo screen
* Added Time Fence parameter to I/M utility "Create Item Sites by 
Class Code"
* Fixed issue with CANCEL button giving wrong error message on 
Incident screen
* Fixed issue with specific Warehouse not working on "P/O Items 
by Buffer Status" report definition
* Fixed issue with wrong report printing from "W/O Operation Buffer
Status by Work Center" display
* Removed error message generated incorrectly when canceling out of
an existing Incident
* Fixed issue with selected Warehouse filter not working properly
when printing "P/O Items by Buffer Status" display
