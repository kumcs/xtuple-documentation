Release Notes
xTuple ERP
Version 4.1.0Beta2
June 5, 2013
----------------------------------

This is the second beta release of version 4.1.0. You will find
mostly bug fixes in this release. If you are beta testing, we
are eager to hear feedback on the new auto-update feature for
the xTuple Desktop client. This feature was added for 4.1.0. Let 
us know what you think! As always, we welcome your feedback. But 
please do not use beta software in production.

Information about compatibility issues related to this software
version can be found on the xTuple Compatibility Matrix at the 
following address: www.xtuple.org/compatibility-matrix.
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