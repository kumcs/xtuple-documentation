Change Log
OpenMFG
Version 2.0.2
January 8, 2007
==================================



The following features and bug fixes have been added to the application 
since the release of version 2.0.1:


New Features:

* Added Shipment Numbers to uniquely identify individual shipments
* Modified several screens in the S/R Module (e.g., S/R|Displays|
Shipments by Date) to support Shipment Numbers
* Modified standard Packing List report definition to support 
Shipment Numbers (NOTE: Any custom Packing List report definitions 
will need to be upgraded to take advantage of the new Shipment 
Numbers functionality.)
* Added S/O Pick List option to Customer Form Assignments to allow
possibility for distinction between S/O Pick List and S/O Packing
List
* Added ability to back-out unposted Sales Order Invoices; deleting 
these Invoices now returns them to the Billing Selections list
* Added link between coship and invcitem tables; now, when posting 
a Billing Selection, the application will populate a value in 
coship_invcitem_id that links a shipment line to an Invoice Item 
line
* Added S/R privilege to prevent non-privileged users from recalling 
Sales Orders to Shipping if the Orders have been invoiced
* Added column to Sales Order Status display showing qty. invoiced

Bug Fixes:

* Fixed issue preventing conversion of Quotes
* Fixed issue with fonts not printing as expected on Mac
* Fixed issue where Quotes were not being cleared effectively
* Fixed issue with Customer discount Price not being transferred 
correctly from Sales Order Item to Invoice Item
* Fixed issue preventing Warehouse Locations from being added
* Fixed issue in vouchering where Vendor UOM conversions were not 
being honored correctly
* Fixed issue in Correct Receiving where Vendor UOM conversions 
were not being honored correctly
* Fixed Correct Receiving to prompt for Location when handling MLC 
Items
* Fixed Correct Receiving to handle Lot/Serial Items correctly
* Improved wording of error message in scenario where user attempts
to double-post a Voucher
* Tightened functionality surrounding the recall of Sales Orders 
to Shipping to reduce possibility for errors
* Added flexibility to billing cycle (i.e., ability to back-out 
unposted Invoices) to reduce possibility for errors
* Fixed issue with incorrect posting of Work Order Operation 
corrections
* Fixed issue where Locations having QOH = 0 were not being 
displayed when distributing MLC or Lot/Serial qty. 
* Fixed issue where posting Count Tags having qty. = 0 was not 
eliminating Lot qty. located in Item Site
* Added support for additional decimal places to Reassign Lot/Serial 
# screen 
* Fixed issue with Billing Selections not being removed properly in 
scenario where user CANCELS selection before saving it
* Fixed issue in MRP Detail display where firmed Availability was 
not being properly projected into future periods 
* Prevented users from driving Inventory qty. negative on Relocate 
Inventory screen
* Improved wording of error message requiring Count Slips when 
counting Item Sites having MLC and/or Lot/Serial qty. 
* Added error checking to help ensure Item Costs are updated 
accurately when Item Types are changed 
* Fixed issue causing error message to be shown when printing Credit 
Memos 
* Fixed issue causing error message to be shown when printing 
Invoices
* Fixed issue with data not printing in Costed Single Level Bill of 
Materials report
* Improved error checking when applying A/P Credit Memos to reduce 
errors
* Fixed error in upgrade packages for users running PostgreSQL 8.2 
(NOTE: OpenMFG is tested and supported on PostgreSQL 8.1)
* Fixed issue with Customer records not being deleted correctly 
when managing CRM Accounts
* Fixed issue causing error messages to be shown when creating 
new Customer Accounts
* Fixed screen resizing issue on Buffer Status by Planner Code 
screen
* Fixed TAB order issue on Cash Receipts screen
* Improved detail checking when viewing Work Order information in 
right-click menus of Inventory History displays
* Fixed screen resizing issue on Planned Orders by Item display
* Fixed issue with extraneous dispatch of CRM Event Notifications
* Improved handling when user attempts to enter duplicate To-Do 
name
* Fixed issue where NEW button was not active on Task List if no 
Tasks displayed
* Fixed issue when viewing CC transactions from right-click menu 
in Detailed Inventory History by Location display
* Fixed issue related to scanning Item bar codes on Issue Stock to 
Shipping screen; scan now returns each Line Item, as expected
* Fixed Item Group filter in Buffer Management displays
* Added "Exit OpenMFG" option back to System menu
* Fixed issue with freight values not being displayed properly when 
shipping Orders via UPS WorldShip
* Fixed problem on Windows preventing page ranges from printing 
correctly
