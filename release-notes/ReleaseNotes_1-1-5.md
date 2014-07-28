Change Log
OpenMFG
Version 1.1.5
February 25, 2005
==================================



The following features and bug fixes have been added to the application 
since the release of version 1.1.4:


New features:


* Added right-click menu option to Voucher Item enabling user to view P/O
  Item information.
* Modified S/R|Shipping|Issue Stock to Shipping to use darker shade of
  green for future ship date shipments. 


Bug Fixes:


* Fixed P/D|Costing|Maintain Actual Costs to disallow entry of negative
  Actual Costs (#3152).
* Fixed problem with correspondence address data not saving properly on the
  Customer master (#3119).
* Fixed problem where A/P Check could be posted multiple times (#3124).
* Fixed problem with printed flag not clearing on A/P Check (#3125).
* Added error message if posting Vouchers when none available to post (#2804).
* Modified S/O|Item Pricing|Pricing Schedule Assignments to say "N/A" in
  Customer Type column in cases when a specific, single Customer is specified
  (#3123).
* Fixed problem with S/O|Master Information|Customer Form Assignments not 
  handling Quote forms correctly (#3199).
* Fixed problem with Ship-To Address not displaying correctly before Customer
  record is saved.
* Fixed problem with second line descriptions not appearing on the S/O Item
  screen (#3057).
* Fixed rounding error on Customer Information display.
* Fixed problem with S/A displays miscalculating Invoice amounts (#3208).
* Fixed multiple application focus problems (#3101, #3193, #3131).
* Fixed intermittent crash problem on Windows 98 machines (#3200).
* Fixed crash problem in M/S|Planned Orders|Delete Planned Order (#3206).
* Enabled inclusion of meaningful content into the "Subject" line of emails 
  sent by the Batch Manager (#3107).
* Fixed problem with Batch Manager printing duplicate jobs under certain
  circumstances (#3201).
* Fixed focus problem on Sales Order header after SAVE AND ADD TO PACKING LIST
  BATCH button is selected (#3212).
* Added error message preventing posting of unbalanced G/L Series entry 
  (#3156).
* Fixed Invoice screen to include Ship-To browse button in edit mode (#3181).
* Added message to S/R|Shipping|Issue Stock to Shipping to prevent the
  distribution of MLC Items having insufficient QOH (#3195).
* Fixed problem with availability information not being displayed correctly
  for manufactured sold Items (#3105).
* Fixed problem with duplicate columns appearing in S/O|Displays|Summarized 
  Backlog by Warehouse when "Show Prices and Costs" option selected (#3220).
* Fixed problem with Sales total not appearing in S/O|Displays|Summarized 
  Backlog by Warehouse (#3219).
* Moved Total function to bottom of S/O|Displays|Summarized Backlog by 
  Warehouse screen (#3222).
* Fixed sort order problem on S/O|Displays|Summarized Backlog by Warehouse
  (#3218).