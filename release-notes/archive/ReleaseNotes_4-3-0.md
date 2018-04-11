Release Notes
xTuple ERP
Version 4.3.0
February 18, 2014
----------------------------------

These are the release notes for the 4.3.0 Final Release. Thanks
to all who contributed to make this release possible. 

Please note that beginning with version 4.3, xTuple ERP is now 
available in a dedicated commercial package for wholesale distributors.
The Distribution Edition replaces the former Standard Edition, which 
will be retired, and includes the following additional features:

  * Integration of third party pricing services including Trade Service
  * Browse and search the full Trade Service catalog (Electrical, 
    Plumbing, HVAC, Industrial)
  * One-click conversion from catalog to sellable Item including Vendor 
    and pricing setup
  * And much more....(see xtuple.com/wholesale-distribution) for the full list

Standard Edition customers should contact xTuple for special offers to 
upgrade to either the Distribution or Manufacturing Edition of xTuple ERP.

Existing Manufacturing and Enterprise edition customers should note that 
upgrade files formerly prefixed with "std-" will now be prefixed with 
"xtdist-" going forward. For example, the upgrade file to move from 4.2 to 
4.3 is named "xtdist42xto430.gz".

The 4.3.0 release introduces a number of new features, several of which 
were made possible by the FeatureMob2 crowd-sourcing campaign. Here's an 
overview of notable new features in 4.3.0:

Auto-updating Desktop client
  * At log in, the client checks to see if the client version matches 
    the serverVersion metric
  * If the two do not match, a new client matching the serverVersion 
    will download if desired
  * Available for ServerVersion 4.3.0 Beta and newer

Blanket Purchase Orders
  * Contract-based purchasing

Undo Bank Reconciliations
  * New flexibility to correct bank rec errors

Lot reservations
  * Manually reserve lot quantities to Sales Orders

A/R and A/P Workbenches
  * Multiple usability enhancements

As always, please review the xTuple Compatibility Matrix before
upgrading: http://www.xtuple.org/compatibility-matrix.

----------------------------------

The following features and bug fixes have been added to the
applications since the 4.3.0 RC release. Additional detail for
each item listed below may be found on our community
website (www.xtuple.org).

New Features:
* Order Markup % [22039]

Bug Fixes:

* Weight display issues [21742]
* New gap filling SO function replaces SO numbering when quotes 
are involved [21850]
* GL Series Report has SQL error in 4.2 [21858]
* Change shipto address after items issued to shipping causes 
error [21977]
* Problems with createLotSerial.cpp [22114]
* Blanket PO items not shown on MRP Exceptions report [22140]
* ItemAvailabilityWorkbench script error [22154]
* Vendor UOM misaligned [22187]
* Inventory > Utilities > Adjust avg. cost value allows a user 
with only "ViewCost" privilege to modify inventory value [22189]
* "Uses Purchase Orders" setting causing false warnings [22206]
* No longer able to edit closed SO [22245]
* Irrelevant behavior is observed on selecting 'Rollup Prices' 
check box in 'Sales Order Item' screen [22254]
* Unable to delete Work Order Material Requirement from 'W/O 
Materials and Operations' widget of 'Sales Order Item' screen 
[22257]
* Can't return PO [22269]
* dspSalesHistory do not include Misc Invoices [22278]
* List Sales Orders Report not filtering [22283]
* Can not update 4.2 to 4.3RC with web client installed [22289]
* SYSTEM/UTILITIES/Maintain CSV Atlas is no longer a menu option 
[22307]
* It is possible to create a return authorization with blank 
Customer# in the Header information tab [22332]
* Products setup - BOO and BOM active/substitute - can do both 
but field suggests this is only possible on BOOs [22360]
* Total Qty. Per should equal” no longer accepts a value on 
BOM screen [22363]
* Editing S/O and clicking on Close button results in data loss 
[22380]
* quickRelocateLot screen should stay open after post [22404]


----------------------------------

The following features and bug fixes have been added to the
applications since the 4.3.0 Beta release. Additional detail for
each item listed below may be found on our community
website (www.xtuple.org).

New Features:
* Add ability to release PO from Contract Screen [22141]
* Customer name on header of sales order and quotes [21799]
* SO item notes pass to PO [22121]
* Login screen - extend list of recent entries to more than 5 [16518]
* Manual Lot Reservations to SO [21098]
* enhancements to Item Groups for external websites [22087]

Bug Fixes:

* Freight tax [21794]
* Notes to comments feature broken after upgrade [21952]
* It is not possible  to issue stock to a released Transfer Order [21950]
* Copy Item should insert current price [21954]
* View Financial Report window doesn't remember size anymore [21975]
* System error on PO screen [22139]
* When Sales Order creates a Project - Project should default more information [21307]
* W/O Bug when Check Rollup Prices [21941]
* Error voiding multi-currency check [19634]
* 4.2 standard cannot edit work order quantity [22002]
* SO rolling up prices on Job items for Work orders [22120]
* unrelease po privilege missing from upgrade [22113]
* Blanket PO tweaks [21953]
* PostBooks :It is not possible to create a sales order [21964]
* It is not possible to create an item source to an item [21951]
* work order due dates [21969]
* It is not possible to create a Purchase Order [21995]


----------------------------------
Release Notes
xTuple ERP
Version 4.3.0 Beta
November 20, 2013
----------------------------------
The following features and bug fixes have been added to the
applications since the 4.2.0 release. Additional detail for
each item listed below may be found on our community
website (www.xtuple.org).

New Features:

* Undo Bank Reconciliations [8891]
* Customer Prices by Item [9405]
* Add "Open Customer Master" to right-click on A/R Workbench 
[16055]
* Add right-click to see source Voucher on AP Workbench [16366]
* Add "Void" option to right-click on AP Workbench, Payables 
tab [17852]
* Finance charges [20104]
* Local currency on order backlog [20147]
* Omnibus - Improvements to AP Workbench [20279]
* Right-click on AR Workbench to open Customer [20281]
* Blanket PO based on Contracts [20861]
* Manual Lot Reservations to SO [21098]
* Add Sales Order totals and Quote Totals to xWD 2.1Alpha 
[21319]
* Add Incidents to Projects and Project Activities [21561]

Bug Fixes:

* Make updates more automatic [5837]
* Error voiding multi-currency check [19634]
* Recurring creation utility bug [20277]
* Project Task List is displaying incorrect dates [21312]
* Reimplement the Project Copy action using standard 
methodology [21693]
* "Create Item Source" dialog is displayed irrelevantly on 
selecting to save the blank "Purchase Order Item" screen [21718]
* Unable to Override Price for a supply order during SOE [21737]
* Linked POs [21753]
* Shipto General Notes do not populate sales orders [21779]
* Inside sales rep CHAR not being passed to the Invoice( xWD 2.1) 
[21822]
* MRP Exceptions [21829]
* Work Order Project Not being updated [21835]
* New gap filling SO function replaces SO numbering when quotes 
are involved [21850]
* openPurchaseOrder Screen [21886]
