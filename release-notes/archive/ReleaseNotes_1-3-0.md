Change Log
OpenMFG
Version 1.3.0
February 9, 2006
==================================



The following list includes all the features and bug fixes added to 
the application since the release of version 1.2.0. Each feature and
bug fix is listed beneath the minor release where it first appeared:



OpenMFG - 1.3.0-Final
======================

New Features:


* Updated Help Files to coincide with 1.3.0 release
* Replaced S/O Module user privilege "RestrictSelectOrderEditing" with 
new privilege "AllowSelectOrderEditing" to make privilege logic more 
intuitive and consistent. The database upgrade package will 
automatically replace the former privilege with the new privilege so 
there will be no impact on existing users.
* Added Account Type column to Chart of Accounts master list
* Enabled display of full Subaccount Type names on Account Number 
master
* Renamed A/R Cash Receipts display/report to "Cash Receipts by 
Customer"



Bug fixes:

* Fixed issue in S/O display/report "Partially Shipped Orders" where 
backlog amounts were not being calculated correctly if stock was issued 
to Shipping using a Bar Code scanner
* Enabled disabling of Miscellaneous Charges interface on Quote Line
Item screen if S/O Module is configured to hide this interface
* Fixed issue with material usage variance reporting to enable 
reporting on all materials, regardless of issue type, in W/O Module 
displays/reports




OpenMFG - 1.3.0RC1 
====================

New features:


* Added templates for Balance Sheet, Income Statement, and Statement 
of Cash Flows to List Financial Reports. Existing installations will
receive these templates automatically during the upgrade process. The
templates will also be added to the empty.sql database.
* Added new A/R|Deposits Register display/report
* Added new A/R|Open Items display/report
* Added running total/balance to A/P|Check Register display/report
 


Bug Fixes:


* Fixed inconsistencies in Trial Balance display/report
* Fixed issue where offsetting G/L series entries using same Account 
Number for same amounts were being summed instead of being displayed
separately in the G/L
* Fixed issues with beginning/ending balance information not forward-
updating appropriately into next period when closing previous period
* Fixed issues on S/O|Displays|Partially Shipped Orders related to 
"Show Prices" option and alignment of Total at bottom of screen
* Dropped Shipping Warehouse requirement when viewing parent Sales 
Order information from W/O|Displays|Work Order Schedule by Planner 
Code
* Fixed issue with multiple line description/notes information getting 
garbled in G/L|Displays|Summarized G/L Transactions
* Fixed issue with multiple Purchase Order headers being created for 
same Vendor in certain scenario when creating POs from I/M Availability 
displays
* Added comma to amounts displayed in Difference column of Trial 
Balance display
* Fixed issue Actual Cost updates not being handled properly when 
vouchering Items where Inventory/Vendor ratio not 1:1
* Enabled NEW button on Comments tab of S/O|Display|Customer Information
* Resized Vendor master and Customer master screens
* Fixed permissions issue preventing certain users from performing Cost 
updates
* Prevented users from being able to select an amount of $0 for payment
* Fixed issue related to the "Manual" Order Number creation in Configure 
P/O



OpenMFG - 1.3.0Beta3
====================

New features:


* Made it possible to run MRP using the Batch Manager
* Added ability to assign names to Accounting Periods 
* Created G/L utility to forward-update multiple Accounts at once 
* Added new custom column to Financial Reporting Engine, with ability to
customize the column name when viewing Financial Reports



Bug Fixes:


* Fixed issue with Inventory Availability displays/reports not 
recognizing Inventory/Vendor UOM ratios
* Fixed issue with MRP not recognizing Inventory/Vendor UOM ratios
* Fixed error in Fiscal Year close routine where Year-End Equity Account 
balance was not being recalculated automatically if Fiscal Year was 
closed, reopened, and then closed again
* Renamed location-tracking column header in Inventory History displays/
reports
* Fixed color-coding of Availability in I/M|Displays|Inventory 
Availability by Source Vendor
* Fixed issue with Zones not saving properly on Warehouse Location master
* Fixed issue with List Open Sales Order not updating properly
* Prevented CLEAR button on Quote header from incrementing Quote Number
* Fixed errors when attempting to override Purchase Order Numbers when 
creating a PO from a Purchase Request
* Allowed Items having Item Type = "Reference" to be sold
* Enabled Sales Order Number to be recognized after hitting ENTER button
on S/R|Forms|Print Shipping Form
* Fixed issue with Document Number not populating in Inventory History 
displays after a Miscellaneous Adjustment for a Multiple Location Control 
(MLC) Item
* Fixed issue with Country code information in Bill-To and Ship-To 
Addresses not correctly populating the Invoice report



OpenMFG - 1.3.0Beta2
====================

New features:


* Added "Difference" and "Difference %" options to Financial 
Reporting Engine
* Modified forward-update and close Accounting Period
functionality to automatically clear beginning balances of
Revenue and Expense Accounts when the start of the next Period 
coincides with the start of a new Fiscal Year
* Added performance enhancements to improve processing time when 
running S/A|Time-Phased displays/reports
* Added performance enhancements to improve processing time when 
running MRP
* Renamed Accounting Year Period to "Fiscal Year"
* Added country code support in Customer and Vendor addresses
 


Bug Fixes:


* Modified Running Availability display to accurately consider 
Inventory/Vendor UOM ratios for existing Purchase Orders
* Enabled correct interpretation of Inventory/Vendor UOM ratios when 
releasing Purchase Requests to Purchase Orders using Item Sources
* Fixed problem with negative numbers appearing when shipped Items 
were recalled to Shipping
* Fixed problem where A/R applications were not displaying on A/R 
Credit Memos
* Fixed problem in Issue Stock to Shipping with barcode scanner 
functionality mishandling Sales Orders containing multiple Line Items 
of the same Item
* Fixed problem with Document Number not displaying in Inventory 
History displays
* Fixed problem with data alignment on Quote Line Item display
* Prevented users from creating Item Costs if no Costing Element is 
assigned
* Removed non-functioning PURGE button from S/R|Shipping|Recall Orders 
to Shipping
* Fixed problems with Purchase Order report definition
* Added logic to improve efficiency and accuracy when updating and 
posting Item Costs for All Class Codes
* Fixed incorrect calculation in "% of Group Total" portion of Financial 
Report Engine
* Revised Invoice report definition to display adjusted total due after 
Credit Memos applied
* Modified A/R history displays to use Due Date as opposed to Document 
Date
* Fixed commission value error on Customer master
* Modified the "formataddr" function to handle country codes, making 
country codes available to report definitions using the function
* Fixed unclear system error when copying a Financial Report
* Fixed problems with data not saving as expected on A/R and A/P Credit 
Memo and Debit Memo screens
* Fixed problem where Invoice was not being printed when selecting all 
three options at S/R|Ship Order
* Fixed problem where Credit Memos allocated to a Sales Order were not 
being released when Sales Order was deleted



OpenMFG - 1.3.0Beta1
====================

New features:


* Added ability to Issue Stock to Shipping from Sales Order screen
* Added functionality to prevent users from inadvertently ignoring
error messages when using barcodes to issue stock to Shipping
* Added A/R configuration option to hide APPLY TO BALANCE button when
entering Cash Receipts
* Added S/O configuration option to hide Misc. Charges and related fields
on Sales Order screen
* Modified Financial Report engine to allow for greater flexibility when
displaying percentage total calculations



Bug Fixes:


* Fixed pattern-recognition problem with Summarized Backlog by Warehouse
report
* Prevented ability to overpay an Invoice when entering Cash Receipts
* Improved safeguards to prevent users from deleting Vendors 
inadvertently



OpenMFG - 1.3.0Alpha
====================

New features:


* Added credit card encryption and online processing; currently 
  supports YourPay verification service
* Implemented two-step credit card process where cards may be 
  preauthorized and charged
* Added integration with UPS WorldShip
* Created new Financial Reports menu structure
* Added ability to PRINT Financial Reports
* Added ability to COPY Financial Reports 
* Enabled summarized financial reporting with "Hide Detail" option 
  on Financial Reports 
* Added ability to create/maintain Budgets by G/L Account
* Added ability to create Budget reports
* Added time-phased capability when previewing Financial Reports
* Added ability to suppress unwanted columns when previewing Financial 
  Reports
* Added % difference option to Financial Reports 
* Added warning when user attempts to DELETE a Financial Report
* Enabled Cash Flow reporting using Financial Reports
* Added right-click drill-down in G/L Transactions and Summarized 
  G/L Transactions displays
* Created new A/R Workbench where Cash Receipts, Credit Memos, and 
  Credit Card charges can be applied on one screen 
* Created Customer Service Workbench in S/O|Displays|Customer 
  Information
* Created Work Order Production Workbench in W/O|Displays|W/O Schedule 
  by Work Center
* Created A/P|Voucher Register display/report 
* Created A/R|Invoice Register display/report, replacing G/L|Daily 
  Invoice G/L Transactions  
* Added Credit Memo data to Invoice Register 
* Modified Trial Balance display/report to include Db/Cr balances, 
  differences, and totals
* Added Cash Receipts display/report 
* Added A/P Aging display/report
* Added A/R Aging display/report 
* Modified Bill of Operations and also Post Operations to allow for the 
  transfer of Work Order quantities to specifically-designated WIP 
  Locations (applies to MLC Items only)
* Added ability to identify individual users who performed set up and/or 
  run when Work Order Operations or Production is posted
* Enhanced options on W/O|Displays|W/O Operations by Work Center
* Enabled Credit Memo applications at point of SO entry 
* Added multiple new statuses for Sales Orders, leading to better Order 
  tracking
* Added originating Quote Number to Sales Order header if Sales Order 
  is a converted Quote 
* Added S/O|Sales Order Lookup by Customer Type display
* Added Restricted Locations tab to Item Site master 
* Added special hotkeys for Mac
* Improved Location tracking in I/M|Inventory History by Item/Planner 
  Code 
* Modified behavior of "Print Packing List" on S/R Ship Order screen to 
  show quantity as having been shipped prior to printing the Packing List
* Added System|S/O Config for Invoice date source 
* Added functionality to prevent users from opening the same window twice 
* Enabled EDI interface when running Reprint Invoices 
* Created S/O|Sales Orders By Customer PO Lookup display
* Added right-click option in W/O|W/O Schedule displays to view parent 
  Sales Orders, when applicable
* Added "Ship Complete" option to Sales Order header to prevent the 
  shipment of Orders which are not complete
* Added "Shipment Value" informational display to Ship Order screen 
* Added CLEAR button to Sales Order header 
* Added W/O|Open Work Orders with Parent Sales Orders display/report
* Enabled behind-the-scenes linkages between Purchase Requests and their 
  parent Work Orders
* Enabled ability to edit the G/L Account when entering A/P Debit and 
  Credit Memos 
* Added ability to do multiple selects on A/P|Payments|Select Payments 
* Added Invoice Number to A/P|Select Payments and Selected Payments screens 
* Changed default behavior to keep the following screens open to facilitate 
  batch entry: Voucher, Misc. Voucher, A/R Credit Memo, and Series G/L 
  Journal Entry
* Added ability to navigate between Sales Order Items 
* Added functionality to prevent multiple users from editing the same Sales 
  Order at the same time
* Added "Maximum Order Quantity" to Item Site Order Parameters options; 
  currently applies only when MRP is run
* Added ability to Issue Stock to Shipping by UPC code



Bug fixes:


* Fixed error when Correcting Production Posting for Work Orders having 
  quantity > 999
* Fixed permissions issue so users without Customer Master privileges 
  cannot access Customer Master from Print Invoice screen 
* Tightened permissions to prevent unprivileged users from viewing Sales 
  Order information in certain situations 
* Updated Sales Order Item Pending Availability tab to conform to 
  system-wide allocations standard 
* Fixed "Release Order" option in right-click menu of Running Availability 
  screen affecting purchased Items 
* Fixed tabbing problem in SO|Orders|Print Packing List
* Enabled SAVE AND ADD TO PACKING LIST BATCH button so that it is accessible 
  when editing a Sales Order
* Fixed problem with Quotes not appearing on List Quotes screen if Quote 
  contained no Quote Items 
* Adjusted sizing of Sales Order screen to accommodate longer Account Number 
  segments
* Fixed reversed dates in W/O|W/O History by W/O Number display 
* Fixed problem causing error message when adding/editing an MLC Item Site 
  where all locations are restricted 
* Renamed Sales Order Item Warehouse to "Shipping Warehouse" and Sales Order 
  header Warehouse to "Warehouse"
* Renamed the Ship Date on the Sales Order header to "Scheduled Date"
* Improved screen layout of Item Site Order Parameter options
* Fixed problem where Credit Memos were not recognizing the corresponding 
  Ship-To
* Fixed problem in S/R|Displays|Shipments by Sales Order/by Date where 
  Sales Order Items were shown as being "Shipped," when in fact they were 
  "At Shipping" 
* Fixed problem where some payments were incorrectly showing $0 balance on 
  A/P|Payments|Select Payments
* Fixed problem with printed status not updating on List Unposted Invoices 
  when printing Invoices by Ship Via
* Fixed problem with A/P Open Items having $0 balance not being closed 
* Fixed rounding error in Purchase Order Line Item screen
* Fixed problem where P/O Freight was not automatically filling in when 
  receiving P/O Items
* Enabled S/A displays/reports to recognize $0 Credit Memos 
* Enlarged sizing of Account Number segments on G/L|Master Information|Chart 
  of Accounts
* Fixed problem where Tax Exempt ID Number was not displaying in the Customer 
  master screen 
* Fixed problem to prevent Standard Journal Items from being saved without 
  an Account
* Fixed mis-labeled column header in Running Availability display
* Fixed problem where Sales Tax was not calculating properly when more than 
  one item was invoiced 
* Added description information when printing Warehouse Locations master list
