Release Notes
xTuple ERP
Version 4.1.0
September 11, 2013
----------------------------------

This is the final release of version 4.1.0. Thanks to all in the
community who made this release possible! You will find several 
new features and bug fixes in this release. One note: The 
automatic update feature for the Desktop client has been removed 
from 4.1.0. It will be reintroduced in a future xTuple release.

Information about compatibility issues related to this software
version can be found on the xTuple Compatibility Matrix at the 
following address: www.xtuple.org/compatibility-matrix.

----------------------------------

The following features and bug fixes have been added to the
applications since 4.1.0RC. Additional detail for each item 
listed below may be found on our community website under the Issue 
Tracker.

Bug Fixes:

* Expired registration key crashes the application on login [20098]
* Selecting to open a "Time Clock Summary" screen displays "Could 
Not Create Form" error dialog [20508]
* "Production Time Clock By Employee" screen does not filters the 
production time clock entries according to the selected Employee 
[20509]
* It is not possible to create a new Work Order time clock entry 
from "Production Time Clock By Work Order" screen [20510]
* Fold username to lowercase [20702]
* Remove non-usable P/O reservations code [20772]
* Unable to change the bank account of a sales order set in the 
"Cash" section under the "Payment" tab [20779]
* Disallow mismatched client versions option is not honored [20811]
* Time Clock Summary form is missing [20916]
* Shifts are being duplicated [20917]

----------------------------------

The following features and bug fixes have been added to the
applications since 4.1.0Beta2. Additional detail for each item 
listed below may be found on our community website under the Issue 
Tracker.

New Features:

* Time and Attendance (19018)
* Substitute items on a sales order [19354]
* Add "Titles" to Customer List [20578]
* Checks and Cash payment from the CC payment tab in Sales Order 
Entry [20621]
* Create SO Link PO (adjust qty for PO) [20628]
* Item analyzation [20663]

Bug Fixes:

* Item Master Sorting is not working properly [16914]
* Selecting to add a Bill of Material to a new item generates a 
DB log error [17345]
* Set all get...id() stored procedures Volatitlity to STABLE 
[17998]
* Contact screen proportionality has changed [18689]
* Inconsistent behavior of "Close" button on Sales order screen 
[18875]
* Add owner to api.contact view [19344]
* Saving Filters with Class Code Matching Quantifiers Crashes 
xTuple [19346]
* Costs not handled consistently on Quote and Sales Order [19751]
* Change Sales Order header to show profit margin based on the 
"long 30" calculation [20001]
* Expose Sales Order Item Unit Cost for visibility and editability 
[20003]
* Revert the Sales Order Item Markup/Discount behavior to Discount 
only [20005]
* AR Statement cannot be emailed via EDI [20222]
* Duplicate Pricing Schedule Assignment does not display error 
[20346]
* Blank "BOM Item Actual Cost" screen is displayed on selecting to 
edit a costing element of a Bill Of Materials Item [20427]
* Check Register [20442]
* BOL 3.8.4 -> 4.0.3 Upgrade [20464]
* It is not possible to create a size zone with same details in 
different sites [20482]
* It possible to Clock-In a blank operation from "Time Clock" 
screen [20507]
* Text overlap in "Post Production" screen [20511]
* Employee Code is not displayed in Production Time clock By Work 
Order screen [20512]
* External Catalog Cross warehouse item creation [20533]
* Documents are lost when converting an iQuote to an Open Sales 
Order [20564]
* 4.0.5: "MaintainRegistrationKey" privilege is not available in 
Postbooks Empty database [20580]
* Running Availability Screen (inconsistant) [20588]
* Inventory, Utlility, Update Reoder Levels [20594]
* Batch Pack List Screen ( add Pick List Batch screen) [20598]
* The "purchaseOrder" dialog is displayed  irrelevantly on 
selecting to create a Purchase Order [20602]
* Pricing Schedules using scheduled date [20606]
* Sort sequence on Pick tickets/Packlist [20607]
* Sales Reservations report in PostBooks db [20619]
* Irrelevant behavior is observed in "Adjust Inventory Value" 
screen [20633]
* PO items do not worklike SO items during PO entry [20665]
* Vendor label is missing in "Attach a Document" screen [20670]
* Selecting to print "A/P Applications" screen does not displays 
"Doc#" label [20700]

----------------------------------

The following features and bug fixes have been added to the
applications since 4.1.0Beta. Additional detail for each item 
listed below may be found on our community website under the Issue 
Tracker.

New Features:

* Replace "List Cost" naming with "Wholesale Price" [20002]

Bug Fixes:

* Currency exchange rate window does not handle localized numerics 
properly [10418]
* Delete posted invoice before saving [18630]
* Inventory update should be disabled if no item site [20043]
* Running Availability print does not print all information [20153]
* Picking List SO with Locations report not showing reserved qty 
[20174]
* API Price Schedule Item Error [20223]
* Pricing Schedules [20263]
* Recurring creation utility bug [20277]
* Site to Site transfer of fractional amount of item not set as 
fractional [20287]
* Cost for newly created item [20299]
* Error running MRP with exceptions: poitem_soitem_id does not 
exist [20308]
* Irrelevant behavior is observed on selected to post the receipt 
for a PO line item [20337]
* G/LSeries Report & filter [20376]
* deleteitemcost(integer,integer) function uses SELECT where it 
should use PERFORM [20381]
* Selecting to copy a Drop Ship quote does not creates drop ship 
enabled quote [20390]
* It is possible to create duplicate records for site zone [20403]
* Re-opening a quote doesn't shows the Override Price of a quote 
item [20417]
* Make sure new installer does two-letter state abbreviations 
[20432]

----------------------------------

The following features and bug fixes have been added to the
applications since 4.0.3. Additional detail for each item listed 
below may be found on our community website under the Issue 
Tracker.

New Features:

* Make updates more automatic	[5837]
* Substitute items on a sales order	[19354]
* New API for entering Physical Inventory Counts [19388]

Bug Fixes:

* Freight amount is calculated incorrectly for a sales order with 
multiple shipments [17525]
* Postbooks Demo: Selecting to purge invoices generates DB log 
error [17779]
* Selecting to post a cash receipt displays a system message 
[18623]
* DB log error is generated on selecting to query "Update 
Reorder Level by Item" screen [18678]
* Irrelavent behaviour is observed in "User Information" screen 
[18705]
* Observation: Incorrect Net unit price is populated in Purchase 
Order item screen [18755]
* DB log error is generated on selecting to query the "Return 
Authorization Workbench" screen [18934]
* Irrelevent dialog is displayed on selecting to print Sale 
Types [18975]
* Unable to print "Contracts" screen [18995]
* API item view missing fields [19317]
* API requires custinfo_shipform in order to display data [19339]
* Only Show Shortages [19421]
* Trial Balance Out of Balance [19583]
* Item "Maximum Desired Cost" value not converted to local 
currency when comparing to PO Unit Price [19600]
* "purgeSalesOrders" does not exist on login after 38xto400 std 
update [19602]
* It is not possible to copy an already copied Locale [19618]
* DB log error is generated on selecting to print a Sales Order 
created for a foreign customer [19639]
* api.itemsourceprice does not include newly added public.itemsrcp 
columns [19651]
* Profit Margin doesn't recalculate [19694]
* Convert Quote to Order/Convert Quote to Invoice [19728]
* Substitute items salesOrderItem Screen [19729]
* List cost does not show in local currency [19756]
* Performance issue with Master Schedule display after migrating 
to 3.8.4 and new cloud [19961]
* View public.usr, locales, roundqty() affect performance of 
cloud db's with more users [19971]
* Return Authorization automatic numbering problem [20013]