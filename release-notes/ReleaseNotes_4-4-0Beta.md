Release Notes
xTuple ERP
Version 4.4.0 Beta
February 24, 2014
----------------------------------

These are the release notes for the 4.4.0 Beta Release. Thanks
to all who contributed to make this release possible. As always, 
we welcome feedback from beta testers, but please do not use beta 
software in production.

As always, please review the xTuple Compatibility Matrix before
upgrading: http://www.xtuple.org/compatibility-matrix.

----------------------------------

The following features and bug fixes have been added to the
applications since the 4.3.0 release. Additional detail for
each item listed below may be found on our community
website (www.xtuple.org).

New Features:

* Finance charges [20104]
* Issue reservations only [20988]
* Add missing support for multi-site processing to shipping sub 
system [21943]
* Display margin and margin % on Invoice [22456]
* Configurable SOE Part #1 [22602]
* Add current server port to the Desktop Client window title [22614]

Bug Fixes:

* JOB Work Orders [20806]
* project type widget on project screen defaults one from list 
[22211]
* Selecting to cancel the transfer order resets the Order # to zero 
irrelevantly [22301]
* Enter a manual item cost during an Adjustment Transaction [22419]
* Drop Ship PO Ship To Address insufficient [22444]
* PostBooks: DB log error is generated on selecting to query the 
"Open Sales Orders" screen [22474]
* Duplicate check numbers [22501]
* Quick relocate does not handle multiple items with the same lot 
number [22530]
* Relocating reserved items silently breaks the reservation [22536]
* line item price for configured item changes after edit [22541]
* Reopening closed SO line in Edit mode results in postgres 
retaining lock on the SO [22544]
* Can't add a line item to credit memo [22564]
* Voiding a check in 4.2.0 causes the replacement check to include 
"Credits Applied" incorrectly [22582]
* Changing cost category for an active item can cause issues with 
GL [22587]
* Sales orders created from quotes don't automatically create work 
orders [22589]
* Wrong Customer Price passed to coitem from return authorization 
[22609]
* Sales Order "Total" value is not displayed in "Open Sales Order 
screen" for a sales order with zero (0.00) tax amount [22646]
* Used at operation not copying over in new copy item utility [22655]
* Irrelevant system message is displayed on selecting to cancel a 
Quote creation [22670]
* Update api.account table [22688]
* Cannot delete sales order line items when reservations enabled 
[22716]
* Create index for ls_number to minimize problem with createLotSerial 
[22748]