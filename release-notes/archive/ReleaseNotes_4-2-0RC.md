Release Notes
xTuple ERP
Version 4.2.0 RC
October 3, 2013
----------------------------------

These are the release notes for the 4.2.0 Release Candidate (RC). 
Thanks to all who contributed to make this release possible.

As always, please review the xTuple Compatibility Matrix before
upgrading: http://www.xtuple.org/compatibility-matrix.

----------------------------------

The following features and bug fixes have been added to the
applications since the 4.2.0 Beta release. Additional detail for
each item listed below may be found on our community
website (www.xtuple.org).

New Features:

* Collection of features related to Alternate Routings [20437]
* Add item_prodweight to salesOrder Item Tab [20626]
* New Report: Show items that were just received that have demand 
[21000]
* Changes to "long 30" calculation in 4.2 Alpha [21056]

Bug Fixes:

* Work Order Detail Report [10925]
* It is possible to create a Sales order for an itemsite with no 
work week defined [16898]
* Transaction dump when creating a Pricing Schedule item [17797]
* Error in calculation of available allocatable amount of a 
customer deposit [17934]
* Misleading changelog in sales order [18355]
* Able to create a recursive BOM [18740]
* Bad tab order on Expense Category form [18741]
* Bad tab order on "Sales Category" form [18742]
* Print Purchase Order Form screen doesn't get refreshed after 
printing [18941]
* Unable to Issue Uncontrolled Material to a TO [19009]
* Costing error when voiding [19351]
* Wrong field name in Item source [20028]
* No Error message is displayed on selecting to add a line item 
without entering the schedule date [20357]
* Selecting to save the line item of a sales order selected for 
billing displays irrelevant dialog [20407]
* Privilege Issue viewing Inactive Revisions [20426]
* Void check on unposted bankrec [20557]
* "Update Price?" dialog is displayed irrelevantly on selecting to 
edit a characteristic value of a sales order line item [20712]
* Selecting to add an employee to blank Employee group screen 
generates db log error [20722]
* Irrelevant behavior is observed in sales order screen [20810]
* Observation: Sales Order Acknowledgement does not displays 
Currency symbol [20825]
* Incorrect behavior is observed in sales order item screen [20862]
* Qty field is blank in the print report of "Purchase Order 
Delivery Date Variance by Vendor" screen [20914]
* Incorrect port is used when selecting recent on log in screen 
[20971]
* Need to update copyright on login screen [20976]
* Label on shifts display does not match spec [20980]
* Adding a credit card will not let you save without a State field 
[21017]
* Summarized Time Clock entries are not displayed in "Time Clock 
Summary" Screen [21029]
* Observation: It is not possible to select multiple quote line 
items in Quote screen [21033]
* Severe Performance Issue when Applying AR Cash [21064]
* Keep Purchase Request list open [21065]
* Tax Credit [21073]
* It is not possible to create a Work Order for a job costing item 
[21074]
* Issue Material by Item screen does not immediately update [21136]
* Odd behavior in filters on Work Order Schedule [21140]
* Window sizes going haywire [21141]
* Credit Memo Application posting to incorrect account [21154]
* Accounts Payable Reports no longer available [21159]
* Planned Order Notes not saving [21169]
* Selecting to delete a parent CRM account displays incorrect 
error message [21199]
* Sticky Button in Post Production [21228]
* Opportunity stage created with "Mark Opportunity inactive at 
this Stage" checkbox checked is not functional [21241]
* Default Location misbehavior [21258]
* Auto-issue drives serial number quantities negative [21267]
* Bank Reconcilation Report issues [21269]
* Countries list is not available in CRM setups to set a default 
country for Addresses [21286]
* "Could Not Create Form" dialog is displayed irrelevantly on 
selecting to copy an item [21287]
* DB log error is displayed on selecting to Clock-In a work order 
from Time clock screen [21288]
* DB log error is generated on selecting to create a sales order 
for a manufacturing item [21290]
* Project List Report Section Total is 0.00 [21296]
* GL Transactions display includes deleted GL transactions in 
calculation of beginning balance [21300]
* Window menu items are inactive [21303]
* Filter on Project Type does not return a list [21304]
* New Project displays bad text on Additional Summary [21305]
* Project Activities should be active by default [21309]
* Clicking on Activity Project to create a task gives database 
error [21310]
* Project New is missing option for Quote [21313]
* Drop ship in Sales order entry [21321]
* No Way To activate a BOM revision [21329]
* SO: subsequent SO lines 0 price [21337]
* Sales Credit Memo Close Button [21340]
* Omnibus: It is not possible to delete an order created from a 
Project screen [21348]
* "Debug" error dialog is displayed irrelevantly on selecting to 
view the Sales Order line item [21349]
* Application crashes on selecting to Exit the MetaSQL Editor 
screen [21357]
* Possible to enter clock out time earlier than clock in time 
[21364]
* Print Report of "Employees" screen doesn't honor the filters 
selected [21376]
* Selecting to edit a sales order line item created with a job 
costing item displays irrelevant system message [21380]
* Permission denied for sequence tatc_tatc_id_seq [21386]
* Copy item function is not copying bom items [21388]
* Sales Order Item Inventory BOM screen not refreshing after 
Item is copied [21389]
* Work Order Operation times not showing in Time Clock reports 
[21410]
* Item bar code incorrectly substituted [21469]
* "Immediate Transfer to Site" check box is not functional in 
"Post Miscellaneous Production" screen [21492]
* Cannot select Site when creating or editing a Pricing Schedule 
[21499]
* Irrelevant behavior is observed on selecting to duplicate the 
Roles [21513]
* Overhead time not posting [21560]
* Time Clock Summary missing totaltime [21569]
* Client Launch is very slow in Windows x64 [21607]


----------------------------------
Release Notes
xTuple ERP
Version 4.2.0 Beta
September 5, 2013
----------------------------------

These are the release notes for the 4.2.0 Beta Release. Thanks
to all who contributed to make this release possible.

As always, please review the xTuple Compatibility Matrix before
upgrading: http://www.xtuple.org/compatibility-matrix.

----------------------------------

The following features and bug fixes have been added to the
applications since the 4.2.0 Alpha release. Additional detail for
each item listed below may be found on our community
website (www.xtuple.org).

New Features:

* Characteristics on Sales Orders/Invoices/Purchase Orders [19168]
* Enhancements to Project (babylon) [19836]
* Change PO Status from Released to Unreleased [20597]
* Embedded Lot/Serial Characteristics [20860]
* Add Alias to Item Widget type-ahead search [20986]
* Attach documents on PO--cannot attach after PO is closed [20996]
* Add PO lookup functionality [20997]
* Cash payment tab - add Order total and balance on the screen 
[21001]
* For Job Items, allow modification of WO on SO Item screen [21095]

Bug Fixes:

* Mac client will crash when ssl enabled [20220]
* It is not possible to create a new Work Order time clock entry from 
Production Time Clock By Work Order screen [20510]
*  Irrelevant behavior is observed in Post Miscellaneous Production 
screen [20925]
* Window Sizing Problems Everywhere [20935]
* Linking POs to SOs [20948]
* Missing Privs for Time and Attendance [20967]
* Change global.pri search paths for openrpt and csvimp to support 
git submodules [20975]
* Quick Item Bulder [21003]
* PO and SO's magnifying glass [21006]
* Can not create inventory settings for a new item [21013]
* No warning when creating new user [21027]
* Selecting to Query the Purchase Order list screen displays a System 
message [21050]
* Purchase Requests are not closed on selecting to convert them to a 
Purchase order [21052]
* Distorted text is displayed in the Copy Item screen [21053]
* Incident does not display correct user on an edit [21068]
* AP Open Document has no unique link to General ledger [21072]
* API Account Return Rule has error returning Parent Account [21109]

----------------------------------
Release Notes
xTuple ERP
Version 4.2.0Alpha
August 1, 2013
----------------------------------

These are the release notes for the 4.2.0 Alpha Release. Thanks
to all who contributed to make this release possible.

As always, please review the xTuple Compatibility Matrix before
upgrading: http://www.xtuple.org/compatibility-matrix.

----------------------------------

The following features and bug fixes have been added to the
applications since the 4.1.0 release. Additional detail for
each item listed below may be found on our community
website (www.xtuple.org).

New Features:

* WorkOrder Detail Report [10925]
* Document Tab everywhere the Comment tab is [11304]
* Expose QToolButton to scripting [18198]
* Support negative offsets on date input [18245]
* New PO Access from the Vendor Workbench [18551]
* Enhanced Copy Item [19623]
* Change PO Status from Released to Unreleased [20597]
* Credits taken on Check Stubs in AP [20600]
* Quote do not generate log [20616
* Item Alias, sales order entry, customer PN [20618]
* Advanced item Search as default search option [20620]
* Add PO number to the top of the purchase order screen [20630]
* Item Workbench enhancements [20649]
* Add fields to variuos screens [20660]
* Add fields to running availabilty and or workbench [20661]

Bug Fixes:

* Focus Policy incorrect displayed with designer [10259]
* Mac: Omnibus: Selecting to cancel/save a new item creation from 
"Item Number" magnifying filter crashes the application [20499]
* Void AP Invoice incorrect C/M Doc Date [20561]
* AP Aging Application or Aging FX error [20636]
* PO items do not worklike SO items during PO entry [20665]
* Sales Reservation Utility [20733]
* Irrelevant behavior is observed in sales order screen [20810]
* vcard changes to xtreewidget cause invalid date conversion [20838]
* Selecting to synchronize companies crashes the application [20859]
* Selecting to print "Items" screen with "Product Category Pattern" 
filter generates db log error [20877]
* Cannot reprioritize W/Os after being released [20894]
* Qty field is blank in the print report of "Purchase Order Delivery 
Date Variance by Vendor" screen [20914]
* Irrelevant behavior is observed in "Post Miscellaneous Production" 
screen [20925]
* Selecting to open "Inventory Availability by Sales Order" screen 
displays "No Sales Order Selected" dialog irrelevantly [20926]
* Error when attempting to reserve quantities on sales order [20964]
