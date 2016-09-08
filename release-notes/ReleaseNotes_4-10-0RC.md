# xTuple Release Notes

## Version 4.10.0RC - September, 2016

These are the release notes for the 4.10.0RC xTuple ERP release.
Thanks to all who contributed to make this release possible, including
a number of feature sponsors.
See below for more information about [deploying this release](#deployment-notes).

### Summary

A large number of features and bug fixes have been added to the
application since the 4.9.3 release. Our focus has been in improving
the desktop client with the following themes:

- Lay the groundwork for an ERP dashboards extension
- Implement Feature Mob 2 features
- Update technology infrastructure
- Improve desktop application performance

Of particular interest are the following features:

- Improved support for VAT, particularly with regard to
  purchasing and tax reporting
- Introduction of a simplified sales order entry window
- Introduction of List Price Schedules
- Increased availability of the Documents tab
- Password reset policies

The technology upgrades include Qt 5 for updated web and JavaScript
features, bug fixes, and performance improvements; PostgreSQL 9.3
for internal features; and ossp-uuid for standardized UUID assignment
and performance. We have increased scripting access to a number of
Qt 5 classes as well, including networking and web technologies,
JavaScript, and serial port control.

**Note:**
The fix for [bug 26903](http://www.xtuple.org/xtincident/view/bugs/26903)
changed the format of work order numbers. Previous versions of the
application displayed these as "12345-1" and "12345-12". Version
4.10.0Beta and later show these same work orders as "12345-001" and
"12345-012". This is a presentation-only change. However, some
auxiliary tables such as `invhist` store the work order number as
a text string. If you have any custom code that scans text columns
for work order numbers, you must either change your code or update
the data. We have written a utility extension to help update the
data. _This is a dangerous operation_ - it will rewrite history
tables and cannot be reverted easily. The extension is attached to
[issue 28286](http://www.xtuple.org/xtincident/view/bugs/28286) if
you decide to risk using it.

**Note:** You will need PostgreSQL 9.3 or 9.4 to use this release,
with the following two PostgreSQL extensions:

- plv8 -
  See our
  [github wiki](https://github.com/xtuple/xtuple/wiki/Installing-PLv8) for
  more information on how to install plv8 and a
  [blog post](https://www.xtuple.org/blog/gmoskowitz/enabling-technologies-plv8-49)
  describing plv8 and why we introduced this new dependency.
- ossp-uuid -
  If you built PostgreSQL from source code, might have to
  rebuild it. Make sure to include the `--with-ossp-uuid` option for
  the `configure` command. See
  [our instructions for building PostgreSQL](https://github.com/xtuple/qt-client/wiki/Desktop-Development-Environment-Setup#get-and-install-postgresql)
  for details.

These need to be installed on the database server, not client machines.

### Features

- Implemented issue #[22870](http://www.xtuple.org/xtincident/view/bugs/22870)
  _default fiscal year in Quickstart not suitable for everybody_
- Implemented issue #[28238](http://www.xtuple.org/xtincident/view/bugs/28238)
  _Move query in workOrder::sFillList() to MetaSQL_
- Implemented issue #[28260](http://www.xtuple.org/xtincident/view/bugs/28260)
  _Update workflow_inheritsource function in xt schema in core_
- Implemented issue #[28335](http://www.xtuple.org/xtincident/view/bugs/28335)
  _Expose qt-client, openrpt and Qt runtime versions to script_
- Implemented issue #[28345](http://www.xtuple.org/xtincident/view/bugs/28345)
  _Script access to QButtonGroup_
- Implemented issue #[28348](http://www.xtuple.org/xtincident/view/bugs/28348)
  _Add source_active_field to source table_
- Implemented issue #[28396](http://www.xtuple.org/xtincident/view/bugs/28396)
  _Sales Tax Assignment on Simplified Sales Order Requires additional and redundent set issues._
- Implemented issue #[28427](http://www.xtuple.org/xtincident/view/bugs/28427)
  _[qt-client] Add Item Group VirtualCluster_
- Implemented issue #[28494](http://www.xtuple.org/xtincident/view/bugs/28494)
  _[xtrental] Add comment types for Rental Items_

### Bug fixes

- Fixed issue #[19108](http://www.xtuple.org/xtincident/view/bugs/19108)
  _Extensions load in random order_
- Fixed issue #[19226](http://www.xtuple.org/xtincident/view/bugs/19226)
  _Print PO without Price_
- Fixed issue #[19925](http://www.xtuple.org/xtincident/view/bugs/19925)
  _Breeders don't work on Average cost_
- Fixed issue #[20393](http://www.xtuple.org/xtincident/view/bugs/20393)
  _Drill Down Results from FRE open behind_
- Fixed issue #[25602](http://www.xtuple.org/xtincident/view/bugs/25602)
  _Item Sources / Prices doesn't remember columns_
- Fixed issue #[25683](http://www.xtuple.org/xtincident/view/bugs/25683)
  _inactive sales reps appear in drop down_
- Fixed issue #[25928](http://www.xtuple.org/xtincident/view/bugs/25928)
  _Opening a Purchase Order from Open Purchase Orders list slow_
- Fixed issue #[25946](http://www.xtuple.org/xtincident/view/bugs/25946)
  _ 'Credit Card Processing Error' is displayed on selecting to charge a Foreign customer's sales order_
- Fixed issue #[26139](http://www.xtuple.org/xtincident/view/bugs/26139)
  _Misc receipts accounting treatment causes issues_
- Fixed issue #[26684](http://www.xtuple.org/xtincident/view/bugs/26684)
  _Need better way to correct aborted check printing_
- Fixed issue #[26716](http://www.xtuple.org/xtincident/view/bugs/26716)
  _SO $$$ balance is showing payment due even thought the SO is paid in full_
- Fixed issue #[26919](http://www.xtuple.org/xtincident/view/bugs/26919)
  _Irrelevant behavior is observed in 'Maintain Work Order Operations' screen_
- Fixed issue #[27761](http://www.xtuple.org/xtincident/view/bugs/27761)
  _Error with Unique characteristics_
- Fixed issue #[27914](http://www.xtuple.org/xtincident/view/bugs/27914)
  _Can't issue inventory in issue to shipping_
- Fixed issue #[28046](http://www.xtuple.org/xtincident/view/bugs/28046)
  _Sales Order and Simple Sales Order _CCAmount passed to Authorize.net can be in the wrong currency_
- Fixed issue #[28075](http://www.xtuple.org/xtincident/view/bugs/28075)
  _Rounding discrepancies on sales orders_
- Fixed issue #[28110](http://www.xtuple.org/xtincident/view/bugs/28110)
  _Incorrect display of Tax on AR memo's_
- Fixed issue #[28204](http://www.xtuple.org/xtincident/view/bugs/28204)
  _ 'DB log' error is displayed when navigate to 'Packing List Batch' screen_
- Fixed issue #[28209](http://www.xtuple.org/xtincident/view/bugs/28209)
  _Changing Sale Type does not generate new workflow._
- Fixed issue #[28213](http://www.xtuple.org/xtincident/view/bugs/28213)
  _Characteristics Corrupted_
- Fixed issue #[28214](http://www.xtuple.org/xtincident/view/bugs/28214)
  _Customer Billing Contact Lists Unrelated, No Checkbox_
- Fixed issue #[28215](http://www.xtuple.org/xtincident/view/bugs/28215)
  _Cust Characteristics Retained after Customer Type Changes_
- Fixed issue #[28217](http://www.xtuple.org/xtincident/view/bugs/28217)
  _Displaying all sales orders (even unrelated) AND Bill To Addresses on new accounts_
- Fixed issue #[28220](http://www.xtuple.org/xtincident/view/bugs/28220)
  _Work Order Screen - column Short shows incorrect value_
- Fixed issue #[28221](http://www.xtuple.org/xtincident/view/bugs/28221)
  _Error Importing Item Source Price_
- Fixed issue #[28236](http://www.xtuple.org/xtincident/view/bugs/28236)
  _Voiding Misc Check does not reverse tax_
- Fixed issue #[28249](http://www.xtuple.org/xtincident/view/bugs/28249)
  _api.itemsourceprice_
- Fixed issue #[28256](http://www.xtuple.org/xtincident/view/bugs/28256)
  _setUserPreference(text, text) stored procedure contains a typo_
- Fixed issue #[28257](http://www.xtuple.org/xtincident/view/bugs/28257)
  _Simplified Sales order Needs a ""Clear"" button_
- Fixed issue #[28264](http://www.xtuple.org/xtincident/view/bugs/28264)
  _quick item entry XWD_
- Fixed issue #[28270](http://www.xtuple.org/xtincident/view/bugs/28270)
  _Able to ship partially issued stock for kit type item when 'Accepts Partial Shipments' option is disabled on   'Customer' screen_
- Fixed issue #[28271](http://www.xtuple.org/xtincident/view/bugs/28271)
  _'Cannot Save Work Order' error dialog is displayed when tried to open work order with due date set to a non-working day_
- Fixed issue #[28278](http://www.xtuple.org/xtincident/view/bugs/28278)
  _Account numbers not printing on financial trend report_
- Fixed issue #[28280](http://www.xtuple.org/xtincident/view/bugs/28280)
  _voucherItem creates a Transaction Block when screen opens_
- Fixed issue #[28283](http://www.xtuple.org/xtincident/view/bugs/28283)
  _Text value on filter should be saved {example: Registration Source field}_
- Fixed issue #[28288](http://www.xtuple.org/xtincident/view/bugs/28288)
  _Unable to add line items to a sales order from 'QUICK ITEM ENTRY' in 'Sales Order' screen._
- Fixed issue #[28292](http://www.xtuple.org/xtincident/view/bugs/28292)
  _Remove ability to edit Posted AR Memo amount_
- Fixed issue #[28300](http://www.xtuple.org/xtincident/view/bugs/28300)
  _Name for operation report needs to be updated_
- Fixed issue #[28303](http://www.xtuple.org/xtincident/view/bugs/28303)
  _Profit Centres are still populated in Accounts after switching off_
- Fixed issue #[28317](http://www.xtuple.org/xtincident/view/bugs/28317)
  _Error entering exchange rates_
- Fixed issue #[28338](http://www.xtuple.org/xtincident/view/bugs/28338)
  _item source search box not visible on Windows 10_
- Fixed issue #[28350](http://www.xtuple.org/xtincident/view/bugs/28350)
  _Item Number Pattern Search does not include item alias_
- Fixed issue #[28359](http://www.xtuple.org/xtincident/view/bugs/28359)
  _Voiding AP Vouchers does not reflect on Tax History report_
- Fixed issue #[28361](http://www.xtuple.org/xtincident/view/bugs/28361)
  _Function releasePR does not populate pohead_fob_
- Fixed issue #[28368](http://www.xtuple.org/xtincident/view/bugs/28368)
  _Update Item Site lead time utility does not correctly order the Item Sites_
- Fixed issue #[28401](http://www.xtuple.org/xtincident/view/bugs/28401)
  _Sales Order Entry - Quick Sales Order Entry Blocking Error in 4.10 Beta 2_
- Fixed issue #[28408](http://www.xtuple.org/xtincident/view/bugs/28408)
  _getcompanyid() Function expects to return an INTEGER however the GL Company code is a TEXT field_
- Fixed issue #[28409](http://www.xtuple.org/xtincident/view/bugs/28409)
  _Unable to copy an item from 'Copy Item' screen._
- Fixed issue #[28410](http://www.xtuple.org/xtincident/view/bugs/28410)
  _averageprice function broken: Planned Revenue/Expenses by Planner Code display_
- Fixed issue #[28421](http://www.xtuple.org/xtincident/view/bugs/28421)
  _Length of Check number_
- Fixed issue #[28425](http://www.xtuple.org/xtincident/view/bugs/28425)
  _Return Authorisation Credit By Issue_
- Fixed issue #[28459](http://www.xtuple.org/xtincident/view/bugs/28459)
  _Unable to add Sales Order to packing list batch_
- Fixed issue #[28462](http://www.xtuple.org/xtincident/view/bugs/28462)
  _Simple Sales Order creates empty orphaned Sales Order after saving one order and closing the screen_
- Fixed issue #[28481](http://www.xtuple.org/xtincident/view/bugs/28481)
  _Customer Discount shows N/A when 100%_
- Fixed issue #[28490](http://www.xtuple.org/xtincident/view/bugs/28490)
  _Copy Production Plan results in date/timestamp casting problem_


## Version 4.10.0Beta2 - July, 2016

These are the release notes for the 4.10.0Beta2 xTuple ERP release.
Thanks to all who contributed to make this release possible, including
a number of feature sponsors.
See below for more information about [deploying this release](#deployment-notes).

### Summary

A large number of features and bug fixes have been added to the
application since the 4.9.3 release. Our focus has been in improving
the desktop client with the following themes:

- Lay the groundwork for an ERP dashboards extension
- Implement Feature Mob 2 features
- Update technology infrastructure
- Improve desktop application performance

Of particular interest are the following features:

- Improved support for VAT, particularly with regard to
  purchasing and tax reporting
- Introduction of a simplified sales order entry window
- Introduction of List Price Schedules
- Increased availability of the Documents tab
- Password reset policies

The technology upgrades include Qt 5 for updated web and JavaScript
features, bug fixes, and performance improvements; PostgreSQL 9.3
for internal features; and ossp-uuid for standardized UUID assignment
and performance. We have increased scripting access to a number of
Qt 5 classes as well, including networking and web technologies,
JavaScript, and serial port control.

**Note:** You will need PostgreSQL 9.3 or 9.4 to use this release,
with the following two PostgreSQL extensions:

- plv8 -
  See our
  [github wiki](https://github.com/xtuple/xtuple/wiki/Installing-PLv8) for
  more information on how to install plv8 and a
  [blog post](https://www.xtuple.org/blog/gmoskowitz/enabling-technologies-plv8-49)
  describing plv8 and why we introduced this new dependency.
- ossp-uuid -
  If you built PostgreSQL from source code, might have to
  rebuild it. Make sure to include the `--with-ossp-uuid` option for
  the `configure` command. See
  [our instructions for building PostgreSQL](https://github.com/xtuple/qt-client/wiki/Desktop-Development-Environment-Setup#get-and-install-postgresql)
  for details.

These need to be installed on the database server, not client machines.

### Features

- Implemented issue #[18335](http://www.xtuple.org/xtincident/view/bugs/18335)
  _Window size and position not being remembered_
- Implemented issue #[19787](http://www.xtuple.org/xtincident/view/bugs/19787)
  _Inactivate work ctrs and Operations_
- Implemented issue #[20423](http://www.xtuple.org/xtincident/view/bugs/20423)
  _Deactivate locations_
- Implemented issue #[24842](http://www.xtuple.org/xtincident/view/bugs/24842)
   _Cash flow not considered_
- Implemented issue #[25989](http://www.xtuple.org/xtincident/view/bugs/25989)
  _Journal inventory cost across Cost Cat G/L Accounts when it is change_
- Implemented issue #[26767](http://www.xtuple.org/xtincident/view/bugs/26767)
  _List Minus Discount Pricing_
- Implemented issue #[27357](http://www.xtuple.org/xtincident/view/bugs/27357)
  _Slow Moving Inventory Report should have a tolerance_
- Implemented issue #[27366](http://www.xtuple.org/xtincident/view/bugs/27366)
  _Add Work Order Specific characteristics_
- Implemented issue #[27477](http://www.xtuple.org/xtincident/view/bugs/27477)
  _Created and Modified Dates & Associated Triggers on every Table_
- Implemented issue #[27779](http://www.xtuple.org/xtincident/view/bugs/27779)
  _Modify ContactWidget to allow access to embedded AddressCluster_
- Implemented issue #[27847](http://www.xtuple.org/xtincident/view/bugs/27847)
  _List Pricing Schedule changes on Sales Order Item_
- Implemented issue #[27785](http://www.xtuple.org/xtincident/view/bugs/27785)
  _Add ledger control package to core_
- Implemented issue #[27789](http://www.xtuple.org/xtincident/view/bugs/27789)
  _Recall support for display lot serial history:ShipTo contact 
- Implemented issue #[27970](http://www.xtuple.org/xtincident/view/bugs/27970)
  _Add Additional group MRP Order Functionality_
- Implemented issue #[28032](http://www.xtuple.org/xtincident/view/bugs/28032)
  _Add correct tax handling for Misc Distributions on Cash Receipts_
- Implemented issue #[28041](http://www.xtuple.org/xtincident/view/bugs/28041)
  _Opportunity List Needs Create Date_
- Implemented issue #[28049](http://www.xtuple.org/xtincident/view/bugs/28049)
  _Add Customer Hold Status to Customer List_
- Implemented issue #[28068](http://www.xtuple.org/xtincident/view/bugs/28068)
  _Add Country to saleshistory view to facilitate dashboards_
- Implemented issue #[28134](http://www.xtuple.org/xtincident/view/bugs/28134)
  _Add Expand All/Collapse All actions to display class_
- Implemented issue #[28146](http://www.xtuple.org/xtincident/view/bugs/28146)
  _Add Project Tasks to ToDo Calendar screen_
- Implemented issue #[28188](http://www.xtuple.org/xtincident/view/bugs/28188)
  _Modify the Packing List Batch metasql to show only Open orders_

### Bug fixes

- Fixed issue #[16481](http://www.xtuple.org/xtincident/view/bugs/16481)
  _'Edit Customer' and 'View Customer' options on To-Do List Calendar
  are not functional_
- Fixed issue #[18003](http://www.xtuple.org/xtincident/view/bugs/18003)
  _Voiding an AP Voucher does not let you choose date and voiding posts
  at orig voucher date_
- Fixed issue #[22170](http://www.xtuple.org/xtincident/view/bugs/22170)
  _Application crash when copying xtreewidget data to the clipboard_
- Fixed issue #[24741](http://www.xtuple.org/xtincident/view/bugs/24741)
  _Irrelevant  behavior is observed in Reserve Stock to Order' screen
  for a Regular item on enabling 'Reserve by Location' groupbox_
- Fixed issue #[24742](http://www.xtuple.org/xtincident/view/bugs/24742)
  _'Valid Locations' widget is displayed on 'Reserve Stock to Order'
  screen irrelevantly, when 'Reserve by Location' is disabled_
- Fixed issue #[24866](http://www.xtuple.org/xtincident/view/bugs/24866)
  _Lot/Serial Document Links not visible on linked Document_
- Fixed issue #[25125](http://www.xtuple.org/xtincident/view/bugs/25125)
  _Temporary item not being cleared properly during copy operation_
- Fixed issue #[25167](http://www.xtuple.org/xtincident/view/bugs/25167)
  _Adding Account Very Slow_
- Fixed issue #[25402](http://www.xtuple.org/xtincident/view/bugs/25402)
  _roundlocale +1 error_
- Fixed issue #[25798](http://www.xtuple.org/xtincident/view/bugs/25798)
  _make linux auto-client-download detect and handle 64bit vs 32bit
  clients_
- Fixed issue #[25888](http://www.xtuple.org/xtincident/view/bugs/25888)
  _It is possible to deselect 'Company Id is a(n):' radio button_
- Fixed issue #[25928](http://www.xtuple.org/xtincident/view/bugs/25928)
  _Opening a Purchase Order from Open Purchase Orders list slow_
- Fixed issue #[25942](http://www.xtuple.org/xtincident/view/bugs/25942)
  _Unable to charge the sales order amount using a Credit Card_
- Fixed issue #[26156](http://www.xtuple.org/xtincident/view/bugs/26156)
  _Virtually impossible to investigate GL issues for transactions that
  ""wash""_
- Fixed issue #[26418](http://www.xtuple.org/xtincident/view/bugs/26418)
  _nonspecific password prompt is confusing_
- Fixed issue #[26756](http://www.xtuple.org/xtincident/view/bugs/26756)
  _Incident #10567 has reoccurred-cannot void foreign currency check_
- Fixed issue #[26802](http://www.xtuple.org/xtincident/view/bugs/26802)
  _Sales menu option renamed prematurely_
- Fixed issue #[27172](http://www.xtuple.org/xtincident/view/bugs/27172)
  _Irrelevant behavior is observed in 'Vendor' screen_
- Fixed issue #[27177](http://www.xtuple.org/xtincident/view/bugs/27177)
  _Column sorting not working on project activity screen_
- Fixed issue #[27345](http://www.xtuple.org/xtincident/view/bugs/27345)
  _'Item Number:' field is in enable mode without entering
  'Work Order#:' in 'Work Order Material Requirement' screen
  irrelevantly_
- Fixed issue #[27411](http://www.xtuple.org/xtincident/view/bugs/27411)
  _Irrelevant behavior is observed in 'User Account Information' screen_
- Fixed issue #[27417](http://www.xtuple.org/xtincident/view/bugs/27417)
  _User is not able to receive the line items from  'Enter Order
  Receipts' screen_
- Fixed issue #[27423](http://www.xtuple.org/xtincident/view/bugs/27423)
  _unexpected behavior from running pricing scripts_
- Fixed issue #[27469](http://www.xtuple.org/xtincident/view/bugs/27469)
  _'Non-Working Day Entered' dialog is displayed multiple times
  irrelevantly_
- Fixed issue #[27490](http://www.xtuple.org/xtincident/view/bugs/27490)
  _ User is able to save a profit center with spaces in 'List Profit
  Centers' screens irrelevantly_
- Fixed issue #[27544](http://www.xtuple.org/xtincident/view/bugs/27544)
  _Db log error is observed on scheduling Run MRP by Item_
- Fixed issue #[27581](http://www.xtuple.org/xtincident/view/bugs/27581)
  _XTUPLEAPPS Menu links require updates_
- Fixed issue #[27584](http://www.xtuple.org/xtincident/view/bugs/27584)
  _Time Phased Sales metasql out of sync_
- Fixed issue #[27585](http://www.xtuple.org/xtincident/view/bugs/27585)
  _ Irrelevant behavior is observed on selecting to post production
  from work order schedule screen_
- Fixed issue #[27592](http://www.xtuple.org/xtincident/view/bugs/27592)
  _need to support building with gcc6_
- Fixed issue #[27631](http://www.xtuple.org/xtincident/view/bugs/27631)
  _Not everything copies from Item Copy_
- Fixed issue #[27674](http://www.xtuple.org/xtincident/view/bugs/27674)
  _Max desire cost format_
- Fixed issue #[27691](http://www.xtuple.org/xtincident/view/bugs/27691)
  _Issue to WO allows multiple qty of same serial number_
- Fixed issue #[27692](http://www.xtuple.org/xtincident/view/bugs/27692)
  _Problem when component on work order multiple times_
- Fixed issue #[27716](http://www.xtuple.org/xtincident/view/bugs/27716)
  _Details missed when copying projects_
- Fixed issue #[27720](http://www.xtuple.org/xtincident/view/bugs/27720)
  _Unit price on woOperation screen in new mode only_
- Fixed issue #[27740](http://www.xtuple.org/xtincident/view/bugs/27740)
  _Add trigger at table level preventing base currency change_
- Fixed issue #[27743](http://www.xtuple.org/xtincident/view/bugs/27743)
  _Label missing on new currency comments_
- Fixed issue #[27751](http://www.xtuple.org/xtincident/view/bugs/27751)
  _Db log error is being displayed instead of prompt dialog when edited
  one of the standard operation to duplicate the other one._
- Fixed issue #[27762](http://www.xtuple.org/xtincident/view/bugs/27762)
  _Report Name mistake_
- Fixed issue #[27763](http://www.xtuple.org/xtincident/view/bugs/27763)
  _Cash Receipt by Customer Group does not support voiding receipts_
- Fixed issue #[27768](http://www.xtuple.org/xtincident/view/bugs/27768)
  _Dictionary files missing from the 4.10b binary package_
- Fixed issue #[27775](http://www.xtuple.org/xtincident/view/bugs/27775)
  _MetaSQL can cause broken report_
- Fixed issue #[27780](http://www.xtuple.org/xtincident/view/bugs/27780)
  _Convert PO Voucher list to metaSQL_
info: script/sql attached_
- Fixed issue #[27790](http://www.xtuple.org/xtincident/view/bugs/27790)
  _Problem opening WO from PO associated_
- Fixed issue #[27800](http://www.xtuple.org/xtincident/view/bugs/27800)
  _'Copy Project' screen gets closes on clicking 'OK' button in 'System
  Error' dialog box when the project name is duplicated.'_
- Fixed issue #[27802](http://www.xtuple.org/xtincident/view/bugs/27802)
  _Schedule option: unable to see/edit email address_
- Fixed issue #[27803](http://www.xtuple.org/xtincident/view/bugs/27803)
  _Import/Export screen: unable to enter email addresses_
- Fixed issue #[27807](http://www.xtuple.org/xtincident/view/bugs/27807)
  _Non-Inventory items on POs not displaying correctly_
- Fixed issue #[27813](http://www.xtuple.org/xtincident/view/bugs/27813)
  _Customer info missing on cash receipt misc. distribution_
- Fixed issue #[27814](http://www.xtuple.org/xtincident/view/bugs/27814)
  _Wrong Itemsite passed  to Reassign Lot/Serial # from item workbench_
- Fixed issue #[27820](http://www.xtuple.org/xtincident/view/bugs/27820)
  _Voided cash receipt still included in Base Amount Total_
- Fixed issue #[27824](http://www.xtuple.org/xtincident/view/bugs/27824)
  _Planned Order Search Pattern_
- Fixed issue #[27832](http://www.xtuple.org/xtincident/view/bugs/27832)
  _Ad hoc exchange rate comment not added to list_
- Fixed issue #[27836](http://www.xtuple.org/xtincident/view/bugs/27836)
  _Error Creating same Alias for different for different Accounts_
- Fixed issue #[27838](http://www.xtuple.org/xtincident/view/bugs/27838)
  _Alignment is not proper in 'Miscellaneous Voucher Distribution'
  screen_
- Fixed issue #[27839](http://www.xtuple.org/xtincident/view/bugs/27839)
  _'Set as Default' option is still in enabled mode for 'Item Sources'
  which already been set as default_
- Fixed issue #[27841](http://www.xtuple.org/xtincident/view/bugs/27841)
  _Update ABC Class error_
- Fixed issue #[27842](http://www.xtuple.org/xtincident/view/bugs/27842)
  _Update ABC Class only on Active Itemsites_
- Fixed issue #[27853](http://www.xtuple.org/xtincident/view/bugs/27853)
  _Can not view quote when viewing opportunity_
- Fixed issue #[27862](http://www.xtuple.org/xtincident/view/bugs/27862)
  _ 'New' button is enabled under 'Misc.Distributions' tab of 'Voucher'
  screen even though the order no is not provided._
- Fixed issue #[27867](http://www.xtuple.org/xtincident/view/bugs/27867)
  _Item Workbench Query Issue (replaces 25953?)_
- Fixed issue #[27877](http://www.xtuple.org/xtincident/view/bugs/27877)
  _DB log error is generated on running 'Run MRP Exceptions'_
- Fixed issue #[27887](http://www.xtuple.org/xtincident/view/bugs/27887)
  _Invalid rows are being added in 'Invoice Register' screen on
  selecting to click on 'Query' button without entering date range_
- Fixed issue #[27895](http://www.xtuple.org/xtincident/view/bugs/27895)
  _Item Alias_
- Fixed issue #[27901](http://www.xtuple.org/xtincident/view/bugs/27901)
  _ 'Select Number' dialog box is displayed instead it should display
  'Enter Vendor' dialog box in 'Vendor History' screen_
- Fixed issue #[27903](http://www.xtuple.org/xtincident/view/bugs/27903)
  _Without entering item in 'Assign Item to Planner Code' displays 'No
  Planner Code Selected' dialog instead of 'Enter Item Number'_
- Fixed issue #[27909](http://www.xtuple.org/xtincident/view/bugs/27909)
  _Unable to create a sales order for a customer and item with markup
  pricing schedule_
- Fixed issue #[27911](http://www.xtuple.org/xtincident/view/bugs/27911)
  _On entering one space in 'Class Code Pattern' field observed that
  class code gets reassigned unexpectedly'_
- Fixed issue #[27912](http://www.xtuple.org/xtincident/view/bugs/27912)
  _On clicking 'Replace' button without entering Replacement Item
  doesn't display userfriendly message and screen gets closed_
- Fixed issue #[27915](http://www.xtuple.org/xtincident/view/bugs/27915)
  _Description of an item is not properly aligned in 'List Item Images'
  screen_
- Fixed issue #[27919](http://www.xtuple.org/xtincident/view/bugs/27919)
  _Cant bill items with a kit that is not issued to shipping_
- Fixed issue #[27922](http://www.xtuple.org/xtincident/view/bugs/27922)
  _Manufacturing function returning incorrect values_
- Fixed issue #[27929](http://www.xtuple.org/xtincident/view/bugs/27929)
  _Unable to view firmed SO line item_
- Fixed issue #[27945](http://www.xtuple.org/xtincident/view/bugs/27945)
  _Item Site is not a Supplied at Site for WO_
- Fixed issue #[27958](http://www.xtuple.org/xtincident/view/bugs/27958)
  _'Issue Stock' itemcontextmenu option is in enable mode for line
  items in unreleased transfer orders_
- Fixed issue #[27964](http://www.xtuple.org/xtincident/view/bugs/27964)
  _Maintain Preferences without Permission_
- Fixed issue #[27965](http://www.xtuple.org/xtincident/view/bugs/27965)
  _Unable to select the 'Enable Shipping Interface from Transfer Order
  Screen' checkbox in Inventory setup screen_
- Fixed issue #[27975](http://www.xtuple.org/xtincident/view/bugs/27975)
  _Mac: Application is crashed on selecting to open any screen from
  'Menu bar' items while 'Loading..' message is displayed._
- Fixed issue #[27976](http://www.xtuple.org/xtincident/view/bugs/27976)
  _working day functionality does not extend to sub-assemblies_
- Fixed issue #[27987](http://www.xtuple.org/xtincident/view/bugs/27987)
  _Omnibus: Unable to save the changes for the images which are opened
  in Edit mode from 'Documents' tab in 'Sales Order' screen_
- Fixed issue #[27989](http://www.xtuple.org/xtincident/view/bugs/27989)
  _No alert is being displayed on clicking 'Expire' button without
  providing Item Number in 'Mass Expire Component Item' screen_
- Fixed issue #[28027](http://www.xtuple.org/xtincident/view/bugs/28027)
  _Incorrect & missing info on Tax Reports_
- Fixed issue #[28028](http://www.xtuple.org/xtincident/view/bugs/28028)
  _'New Owner' label is not aligned with the text box on 'Edit Owners'
  screen._
- Fixed issue #[28031](http://www.xtuple.org/xtincident/view/bugs/28031)
  _Changes to Return Authorization settings lost on save_
- Fixed issue #[28033](http://www.xtuple.org/xtincident/view/bugs/28033)
  _Right click on SO line when all lines' status CF: cannot re-open_
- Fixed issue #[28034](http://www.xtuple.org/xtincident/view/bugs/28034)
  _Dropship change of address on SO does not trigger a change on
  corresponding PO_
- Fixed issue #[28036](http://www.xtuple.org/xtincident/view/bugs/28036)
  _MetaSQL statement salesOrderItem-indentedbomavail.mql for Indented
  Availability on salesOrderItem using wrong column_
- Fixed issue #[28037](http://www.xtuple.org/xtincident/view/bugs/28037)
  _RMA return for SO line not yet invoiced has 0 cost when cost method
  average_
- Fixed issue #[28039](http://www.xtuple.org/xtincident/view/bugs/28039)
  _On demand MRP exceptions due to wrong data type_
- Fixed issue #[28055](http://www.xtuple.org/xtincident/view/bugs/28055)
  _issueallbalancetoshipping() bugfix_
- Fixed issue #[28057](http://www.xtuple.org/xtincident/view/bugs/28057)
  _Able to add miscellaneous distributions to a closed vouchers in
  'Voucher' screen_
- Fixed issue #[28058](http://www.xtuple.org/xtincident/view/bugs/28058)
  _Order shipment information is not auto-populated in 'Sales Order
  Status' screen when screen is opened from 'Open Sales Orders'_
- Fixed issue #[28061](http://www.xtuple.org/xtincident/view/bugs/28061)
  _Gapless Document Numbering_
- Fixed issue #[28069](http://www.xtuple.org/xtincident/view/bugs/28069)
  _Description of an item is not properly aligned in 'Create Item Cost'
  screen when screen is enlarged._
- Fixed issue #[28072](http://www.xtuple.org/xtincident/view/bugs/28072)
  _API.itemcomment imports (INSERTS) to Item Site not Item (one letter
  change)_
- Fixed issue #[28080](http://www.xtuple.org/xtincident/view/bugs/28080)
  _Copy Quote Item Costing_
- Fixed issue #[28081](http://www.xtuple.org/xtincident/view/bugs/28081)
  _Copy Sales Order Item Costing_
- Fixed issue #[28092](http://www.xtuple.org/xtincident/view/bugs/28092)
  _'Copy Planned Schedule' screen loses its focus from 'New Schedule
  Number' field_
- Fixed issue #[28098](http://www.xtuple.org/xtincident/view/bugs/28098)
  _Invalid data displayed_
- Fixed issue #[28108](http://www.xtuple.org/xtincident/view/bugs/28108)
  _coshist_promisedate does not populate when coitem_promdate exists_
- Fixed issue #[28113](http://www.xtuple.org/xtincident/view/bugs/28113)
  _Unable to copy Quote from 'Quotes' screen_
- Fixed issue #[28121](http://www.xtuple.org/xtincident/view/bugs/28121)
  _Change ""Delete Order"" to ""Remove Order"" on Packing List Batch_
- Fixed issue #[28132](http://www.xtuple.org/xtincident/view/bugs/28132)
  _'Edit Invoice Item' option is still in enabled mode for 'Invoices'
  which are already been posted in 'Order Activity by Project'_
- Fixed issue #[28156](http://www.xtuple.org/xtincident/view/bugs/28156)
  _User without permissions can edit projects_
- Fixed issue #[28161](http://www.xtuple.org/xtincident/view/bugs/28161)
  _'Edit Sales Order' option is in enable mode for a 'Sales order'
  which is already been closed  in  'Bookings' Screen_
- Fixed issue #[28178](http://www.xtuple.org/xtincident/view/bugs/28178)
  _Return Auths for Kit Items cannot be credited_
- Fixed issue #[28218](http://www.xtuple.org/xtincident/view/bugs/28218)
  _incident window should allow display and filtering on
  ""resolution""_"

## Version 4.10.0Beta - April, 2016

These are the release notes for the 4.10.0Beta xTuple ERP release.
Thanks to all who contributed to make this release possible, including
a number of feature sponsors.
See below for more information about [deploying this release](#deployment-notes).

### Summary

A large number of features and bug fixes have been added to the
application since the 4.9.3 release. Our focus has been in improving
the desktop client with the following themes:

- Lay the groundwork for an ERP dashboards extension
- Implement Feature Mob 2 features
- Update technology infrastructure
- Improve desktop application performance

Of particular interest are the following features:

- Improved support for VAT, particularly with regard to
  purchasing and tax reporting
- Introduction of a simplified sales order entry window
- Introduction of List Price Schedules
- Increased availability of the Documents tab
- Password reset policies

The technology upgrades include Qt 5 for updated web and JavaScript
features, bug fixes, and performance improvements; PostgreSQL 9.3
for internal features; and ossp-uuid for standardized UUID assignment
and performance. We have increased scripting access to a number of
Qt 5 classes as well, including networking and web technologies,
JavaScript, and serial port control.

**Note:** You will need PostgreSQL 9.3 or 9.4 to use this release,
with the following two PostgreSQL extensions:

- plv8 -
  See our
  [github wiki](https://github.com/xtuple/xtuple/wiki/Installing-PLv8) for
  more information on how to install plv8 and a
  [blog post](https://www.xtuple.org/blog/gmoskowitz/enabling-technologies-plv8-49)
  describing plv8 and why we introduced this new dependency.
- ossp-uuid -
  If you built PostgreSQL from source code, might have to
  rebuild it. Make sure to include the `--with-ossp-uuid` option for
  the `configure` command. See
  [our instructions for building PostgreSQL](https://github.com/xtuple/qt-client/wiki/Desktop-Development-Environment-Setup#get-and-install-postgresql)
  for details.

These need to be installed on the database server, not client machines.

### Features

- Implemented issue #[3569](http://www.xtuple.org/xtincident/view/bugs/3569)
  _Routing - Unable to Modify Instructions_
- Implemented issue #[7175](http://www.xtuple.org/xtincident/view/bugs/7175)
  _Allow Packing List Batch to filter out Holds and Future Scheduled Orders_
- Implemented issue #[9246](http://www.xtuple.org/xtincident/view/bugs/9246)
  _Correctly escape all SQL statements that have escaped characters in them_
- Implemented issue #[10577](http://www.xtuple.org/xtincident/view/bugs/10577)
  _Ability to set a form assignment keyed on Transfer Orders_
- Implemented issue #[11207](http://www.xtuple.org/xtincident/view/bugs/11207)
  _Port 1099 package into core (FM2)_
- Implemented issue #[11908](http://www.xtuple.org/xtincident/view/bugs/11908)
  _Vendor Purchase Order Notes do not flow to PO_
- Implemented issue #[12607](http://www.xtuple.org/xtincident/view/bugs/12607)
  _Ability to Reschedule PO (not line items)_
- Implemented issue #[14182](http://www.xtuple.org/xtincident/view/bugs/14182)
  _*Include standard changes in inventory history_
- Implemented issue #[15171](http://www.xtuple.org/xtincident/view/bugs/15171)
  _*Credit Holds in Sales Orders_
- Implemented issue #[17259](http://www.xtuple.org/xtincident/view/bugs/17259)
  _Move cashrcptbycustgrp to core_
- Implemented issue #[22824](http://www.xtuple.org/xtincident/view/bugs/22824)
  _update of pricing schedules_
- Implemented issue #[23027](http://www.xtuple.org/xtincident/view/bugs/23027)
  _Global UOM conversion_
- Implemented issue #[23152](http://www.xtuple.org/xtincident/view/bugs/23152)
  _privilege to restrict users from editing shared filters_
- Implemented issue #[23207](http://www.xtuple.org/xtincident/view/bugs/23207)
  _*Add filter to GL transaction for amount_
- Implemented issue #[24077](http://www.xtuple.org/xtincident/view/bugs/24077)
  _remove trailing whitespace with gitattributes_
- Implemented issue #[24158](http://www.xtuple.org/xtincident/view/bugs/24158)
  _*PO Return needs RMA/RGA code field_
- Implemented issue #[25127](http://www.xtuple.org/xtincident/view/bugs/25127)
  _Sales Types on opensalesorder-detail Screen also Backlog and bookings as well_
- Implemented issue #[25631](http://www.xtuple.org/xtincident/view/bugs/25631)
  _Payments feature request_
- Implemented issue #[25718](http://www.xtuple.org/xtincident/view/bugs/25718)
  _Add Employee Group filter to Employees List and Search_
- Implemented issue #[25810](http://www.xtuple.org/xtincident/view/bugs/25810)
  _Change to the xwd.convertcatalog and xwd.updatecatalog function_
- Implemented issue #[2583](http://www.xtuple.org/xtincident/view/bugs/2583)
  _Add ABC Class reporting_
- Implemented issue #[25907](http://www.xtuple.org/xtincident/view/bugs/25907)
  _Need user interface for "Generate mobile workflow from desktop orders"_
- Implemented issue #[25927](http://www.xtuple.org/xtincident/view/bugs/25927)
  _*Automate Closing RA Open Lines after credit is posted_
- Implemented issue #[26023](http://www.xtuple.org/xtincident/view/bugs/26023)
  _Add "Enable Database Workflow trigger" metric to qt-client_
- Implemented issue #[26038](http://www.xtuple.org/xtincident/view/bugs/26038)
  _expand CustomerSelector widget API to limit which options are presented_
- Implemented issue #[26216](http://www.xtuple.org/xtincident/view/bugs/26216)
  _catcost screens for catcost table_
- Implemented issue #[26223](http://www.xtuple.org/xtincident/view/bugs/26223)
  _Add Ship Zone and Sale Type to Item Pricing_
- Implemented issue #[26224](http://www.xtuple.org/xtincident/view/bugs/26224)
  _Add Reserved Qty to Item Availability and Running Availability screens_
- Implemented issue #[26246](http://www.xtuple.org/xtincident/view/bugs/26246)
  _Add Pack Date to Packing List Batch_
- Implemented issue #[26282](http://www.xtuple.org/xtincident/view/bugs/26282)
  _By pass Credit Hold if payment is taken for Cash Accounts_
- Implemented issue #[26366](http://www.xtuple.org/xtincident/view/bugs/26366)
  _Add "Print on Post" to Simple G/L Journal_
- Implemented issue #[26370](http://www.xtuple.org/xtincident/view/bugs/26370)
  _Issue All to Shipping stops at line with insufficient inventory_
- Implemented issue #[26375](http://www.xtuple.org/xtincident/view/bugs/26375)
  _*AR, AP Aging Reports in 4.9.x_
- Implemented issue #[26387](http://www.xtuple.org/xtincident/view/bugs/26387)
  _*Availability date in SOItem_
- Implemented issue #[26408](http://www.xtuple.org/xtincident/view/bugs/26408)
  _*Access Vendor A/P history from Payables work bench_
- Implemented issue #[26424](http://www.xtuple.org/xtincident/view/bugs/26424)
  _Revert Return document back to Credit Memo and add Misc Items_
- Implemented issue #[26498](http://www.xtuple.org/xtincident/view/bugs/26498)
  _Add avgcost() as a column on itemsite record on the item_
- Implemented issue #[26679](http://www.xtuple.org/xtincident/view/bugs/26679)
  _*Add SO# to Authorize.net_
- Implemented issue #[26693](http://www.xtuple.org/xtincident/view/bugs/26693)
  _VAT Taxation enhancements (FM2, replaces #20135)_
- Implemented issue #[26699](http://www.xtuple.org/xtincident/view/bugs/26699)
  _*Add Created By to filters_
- Implemented issue #[26767](http://www.xtuple.org/xtincident/view/bugs/26767)
  _*List Minus Discount Pricing_
- Implemented issue #[26832](http://www.xtuple.org/xtincident/view/bugs/26832)
  _*Have an option to one characteristic per module_
- Implemented issue #[26833](http://www.xtuple.org/xtincident/view/bugs/26833)
  _Create a simple sales order entry window as an alternative to
  the full-blown version_
- Implemented issue #[26840](http://www.xtuple.org/xtincident/view/bugs/26840)
  _*Slow Moving Inventory report does not give the option to display Posted Costs_
- Implemented issue #[26866](http://www.xtuple.org/xtincident/view/bugs/26866)
  _Add Documents Tab to Vendor master_
- Implemented issue #[26867](http://www.xtuple.org/xtincident/view/bugs/26867)
  _Add PO Item Non-Inventory items to PO List description_
- Implemented issue #[26950](http://www.xtuple.org/xtincident/view/bugs/26950)
  _Quantities on Hand by Zone screen_
- Implemented issue #[26951](http://www.xtuple.org/xtincident/view/bugs/26951)
  _Add Vendor Characteristics API View_
- Implemented issue #[26960](http://www.xtuple.org/xtincident/view/bugs/26960)
  _tweak lostSerial with set function to accept item_id and ls_id_
- Implemented issue #[26973](http://www.xtuple.org/xtincident/view/bugs/26973)
  _Convert AP Credit Memo sql to metaSQL_
- Implemented issue #[26995](http://www.xtuple.org/xtincident/view/bugs/26995)
  _Reverse Behavior on Miscellaneous AP Credit Memo (replaces 18174) (FM2)_
- Implemented issue #[26997](http://www.xtuple.org/xtincident/view/bugs/26997)
  _Purchasing PO search by customer Purchase Order (replaces 20143) (FM2)_
- Implemented issue #[26998](http://www.xtuple.org/xtincident/view/bugs/26998)
  _Make parent-child relationship in CRM meaningful (replaces 17846, FM2)_
- Implemented issue #[26999](http://www.xtuple.org/xtincident/view/bugs/26999)
  _Deposit when applying Credit Card payment on Sales Order (SO)
  (replaces 20141, FM2)_
- Implemented issue #[27000](http://www.xtuple.org/xtincident/view/bugs/27000)
  _Add "Column" to "Copy to Clipboard" right-click on table view
  (replaces 17543, FM2)_
- Implemented issue #[27056](http://www.xtuple.org/xtincident/view/bugs/27056)
  _*Enforce Password Reset Policy_
- Implemented issue #[27109](http://www.xtuple.org/xtincident/view/bugs/27109)
  _PAIN - calcsalesorderamt_
- Implemented issue #[27110](http://www.xtuple.org/xtincident/view/bugs/27110)
  _PAIN - redundant use of getSoStatus_
- Implemented issue #[27362](http://www.xtuple.org/xtincident/view/bugs/27362)
  _Add item type filter to item cost by classcode_
- Implemented issue #[27407](http://www.xtuple.org/xtincident/view/bugs/27407)
  _Move Webapp metrics to a Desktop setup screen_
- Implemented issue #[27418](http://www.xtuple.org/xtincident/view/bugs/27418)
  _Update Reorder Levels MetaSQL returns transit sites for update_

### Bug fixes

- Fixed issue #[10570](http://www.xtuple.org/xtincident/view/bugs/10570)
  _Sales Order Line Item UOM does not Update to match the Pricing
  Schedule UOM_
- Fixed issue #[17067](http://www.xtuple.org/xtincident/view/bugs/17067)
  _Print Shipping Forms window prints forms for sales orders but
  not for transfer orders_
- Fixed issue #[17699](http://www.xtuple.org/xtincident/view/bugs/17699)
  _*It is not possible to create a Transfer Order from 'Inventory
  History' screen_
- Fixed issue #[18310](http://www.xtuple.org/xtincident/view/bugs/18310)
  _*Irrelevant dialog is displayed on selecting to 'Save' a sales
  order line item opened in edit mode_
- Fixed issue #[21265](http://www.xtuple.org/xtincident/view/bugs/21265)
  _*Bank Rec Window sorts date and amount as text_
- Fixed issue #[22413](http://www.xtuple.org/xtincident/view/bugs/22413)
  _desktop client downloader leaves files behind if download fails_
- Fixed issue #[23006](http://www.xtuple.org/xtincident/view/bugs/23006)
  _*possible to post same serial # to 2 sites_
- Fixed issue #[23464](http://www.xtuple.org/xtincident/view/bugs/23464)
  _*Item Alias problems_
- Fixed issue #[23725](http://www.xtuple.org/xtincident/view/bugs/23725)
  _*Update actual cost and expired components_
- Fixed issue #[23893](http://www.xtuple.org/xtincident/view/bugs/23893)
  _*Selecting to print the 'Lost Sales' screen displays 'Report Not
  Found' dialog_
- Fixed issue #[25038](http://www.xtuple.org/xtincident/view/bugs/25038)
  _*Items approved for billing are doubling in the Approve Order
  for Billing Window_
- Fixed issue #[25402](http://www.xtuple.org/xtincident/view/bugs/25402)
  _*roundlocale +1 error_
- Fixed issue #[25565](http://www.xtuple.org/xtincident/view/bugs/25565)
  _AP Voucher does not allow tax calculation of freight_
- Fixed issue #[25587](http://www.xtuple.org/xtincident/view/bugs/25587)
  _*Partially Drop-Shipped Order_
- Fixed issue #[25667](http://www.xtuple.org/xtincident/view/bugs/25667)
  _Smooth Margin_
- Fixed issue #[25677](http://www.xtuple.org/xtincident/view/bugs/25677)
  _*Tax History Screen_
- Fixed issue #[25686](http://www.xtuple.org/xtincident/view/bugs/25686)
  _Error message about pDistDate displayed irrelevantly when
  attempting to post a standard journal to a non-existent period_
- Fixed issue #[25709](http://www.xtuple.org/xtincident/view/bugs/25709)
  _*Selecting to save a blank 'Purchase Type' displays irrelevant
  text in the dialog box_
- Fixed issue #[25720](http://www.xtuple.org/xtincident/view/bugs/25720)
  _*User is allowed to change the Scheduled date of a Quote in
  'View' mode_
- Fixed issue #[25733](http://www.xtuple.org/xtincident/view/bugs/25733)
  _*Quick Relocate Function Fails to Show Error on Relocate Failure_
- Fixed issue #[25848](http://www.xtuple.org/xtincident/view/bugs/25848)
  _*Item Alias API_
- Fixed issue #[25871](http://www.xtuple.org/xtincident/view/bugs/25871)
  _*City and Postal Code do not appear on reports if no State
  selected_
- Fixed issue #[25878](http://www.xtuple.org/xtincident/view/bugs/25878)
  _*Characteristic Input Mask and Validator not working for Lot/Serial
  input_
- Fixed issue #[25896](http://www.xtuple.org/xtincident/view/bugs/25896)
  _*Unable to add a characteristics to an 'Incident' on creation_
- Fixed issue #[25978](http://www.xtuple.org/xtincident/view/bugs/25978)
  _* 'Username' label is not available in 'General Ledger Transactions'
  print report_
- Fixed issue #[25979](http://www.xtuple.org/xtincident/view/bugs/25979)
  _*'Deleted' label is not available in 'General Ledger Transaction'
  print report from 2nd page_
- Fixed issue #[25985](http://www.xtuple.org/xtincident/view/bugs/25985)
  _When adding a new Work Order from a new Project, project # is
  not populated_
- Fixed issue #[25993](http://www.xtuple.org/xtincident/view/bugs/25993)
  _*DB log error is displayed irrelevantly on selecting to view
  Total Tax_
- Fixed issue #[26005](http://www.xtuple.org/xtincident/view/bugs/26005)
  _*Irrelevant behaviour is observed in 'Opportunities' screen_
- Fixed issue #[26030](http://www.xtuple.org/xtincident/view/bugs/26030)
  _*User is allowed to edit 'Ship To' details in view mode of
  customer screen_
- Fixed issue #[26034](http://www.xtuple.org/xtincident/view/bugs/26034)
  _*Delete SO when At Shipping_
- Fixed issue #[26070](http://www.xtuple.org/xtincident/view/bugs/26070)
  _*Incident status does not display in project activity window_
- Fixed issue #[26078](http://www.xtuple.org/xtincident/view/bugs/26078)
  _*Item Source visibility inconsistent_
- Fixed issue #[26085](http://www.xtuple.org/xtincident/view/bugs/26085)
  _Tweak postreceipts() to always concatenate order line for gl
  postings (fx attached)_
- Fixed issue #[26090](http://www.xtuple.org/xtincident/view/bugs/26090)
  _*Lower Qty ordered when atShipping already_
- Fixed issue #[26124](http://www.xtuple.org/xtincident/view/bugs/26124)
  _*Bank Adjustment should ensure date is part of valid fiscal
  period_
- Fixed issue #[26197](http://www.xtuple.org/xtincident/view/bugs/26197)
  _*Purchase Order Ship-To Name Field is NOT Changeable_
- Fixed issue #[26213](http://www.xtuple.org/xtincident/view/bugs/26213)
  _updating item with catalog_
- Fixed issue #[26226](http://www.xtuple.org/xtincident/view/bugs/26226)
  _*'Delete Unused'  button is not working properly in 'Purchase
  Types' screen_
- Fixed issue #[26231](http://www.xtuple.org/xtincident/view/bugs/26231)
  _*negative Quote total bars line item selection_
- Fixed issue #[26284](http://www.xtuple.org/xtincident/view/bugs/26284)
  _* 'Approve' button is in disable mode in 'Approve Payments'
  screen_
- Fixed issue #[26296](http://www.xtuple.org/xtincident/view/bugs/26296)
  _*Typo error on 'Time Phased Available Capacity by Work Center'
  screen_
- Fixed issue #[26297](http://www.xtuple.org/xtincident/view/bugs/26297)
  _*Unable to print 'MRP Detail' screen_
- Fixed issue #[26318](http://www.xtuple.org/xtincident/view/bugs/26318)
  _*Unrelease Open Purchase Order allowed on Right Click Contextual
  menu_
- Fixed issue #[26322](http://www.xtuple.org/xtincident/view/bugs/26322)
  _*Pick list report for Transfer Order is not available in Reports
  List_
- Fixed issue #[26330](http://www.xtuple.org/xtincident/view/bugs/26330)
  _*'?' Is displayed instead of 'Q' as the Parent Type of a work
  order created on selecting to convert a quote to Invoice_
- Fixed issue #[26346](http://www.xtuple.org/xtincident/view/bugs/26346)
  _*List Site Location Window not working in 4.9.0_
- Fixed issue #[26347](http://www.xtuple.org/xtincident/view/bugs/26347)
  _*'Manual Freight?' dialog box is being displayed on selecting
  to edit 'Quote' created for Foreign Customer_
- Fixed issue #[26361](http://www.xtuple.org/xtincident/view/bugs/26361)
  _*Db log error is generated on selecting to duplicate 'Opportunity
  Sources'_
- Fixed issue #[26362](http://www.xtuple.org/xtincident/view/bugs/26362)
  _*Irrelevant behaviour is observed on quering the 'Order Activity
  by Project' screen_
- Fixed issue #[26377](http://www.xtuple.org/xtincident/view/bugs/26377)
  _*'Cancel Item' button is in active mode on a stock issued 'Sales
  Order Item' screen created for 'Kit' type item_
- Fixed issue #[26389](http://www.xtuple.org/xtincident/view/bugs/26389)
  _New Line characters appearing in Payment (Check) notes field_
- Fixed issue #[26392](http://www.xtuple.org/xtincident/view/bugs/26392)
  _*'Customer #' field detials are not saved properly in a quote
  screen_
- Fixed issue #[26414](http://www.xtuple.org/xtincident/view/bugs/26414)
  _*Error in ship to number logic_
- Fixed issue #[26433](http://www.xtuple.org/xtincident/view/bugs/26433)
  _Transaction Date on Issue Stock to Shipping does not carry forward
  to Ship Order screen's Date Shipped field_
- Fixed issue #[26477](http://www.xtuple.org/xtincident/view/bugs/26477)
  _fixacl() raises warning about the pkghead table_
- Fixed issue #[26484](http://www.xtuple.org/xtincident/view/bugs/26484)
  _*User is allowed to convert an unsaved to Quote to a sales order_
- Fixed issue #[26490](http://www.xtuple.org/xtincident/view/bugs/26490)
  _*No space is observed for 'changeswill' text in 'Customer Saved'
  dialog_
- Fixed issue #[26622](http://www.xtuple.org/xtincident/view/bugs/26622)
  _*User is able to save a record with spaces in 'Employee' screen_
- Fixed issue #[26631](http://www.xtuple.org/xtincident/view/bugs/26631)
  _License user count is showing different values in different
  fields (replaces #26551)_
- Fixed issue #[26652](http://www.xtuple.org/xtincident/view/bugs/26652)
  _*No space is observed in between 'SelectOptions' dialog box in
  'Work Order Costing' screen_
- Fixed issue #[26653](http://www.xtuple.org/xtincident/view/bugs/26653)
  _* Db log error is displayed irrelevantly instead of 'user friendly
  message' in 'Project Types' screen_
- Fixed issue #[26654](http://www.xtuple.org/xtincident/view/bugs/26654)
  _*User is not able to select 'Project Types' in Project screen_
- Fixed issue #[26675](http://www.xtuple.org/xtincident/view/bugs/26675)
  _Random contact on PO shipto_
- Fixed issue #[26692](http://www.xtuple.org/xtincident/view/bugs/26692)
  _*User is able to create duplicate Pricing Schedule Assignments_
- Fixed issue #[26716](http://www.xtuple.org/xtincident/view/bugs/26716)
  _*SO $$$ balance is showing payment due even thought the SO is
  paid in full_
- Fixed issue #[26734](http://www.xtuple.org/xtincident/view/bugs/26734)
  _*Ship To ID Not Populated_
- Fixed issue #[26736](http://www.xtuple.org/xtincident/view/bugs/26736)
  _*No space is observed in between 'Classcode'  in the label name
  of 'W/O Buffer Status by Class Code' screen_
- Fixed issue #[26741](http://www.xtuple.org/xtincident/view/bugs/26741)
  _Item Site ABC class errors_
- Fixed issue #[26742](http://www.xtuple.org/xtincident/view/bugs/26742)
  _*Checkbox is not enabled by default in 'Accounting' tab in Vendor
  screen_
- Fixed issue #[26759](http://www.xtuple.org/xtincident/view/bugs/26759)
  _*'Discountable' option is not being disabled for tax code in
  'Miscellaneous Voucher Distribution' window_
- Fixed issue #[26777](http://www.xtuple.org/xtincident/view/bugs/26777)
  _*'Cash Receipt' screen loses its focus from 'Customer #:' field_
- Fixed issue #[26778](http://www.xtuple.org/xtincident/view/bugs/26778)
  _*'Quotes' screen is not being updated automatically_
- Fixed issue #[26794](http://www.xtuple.org/xtincident/view/bugs/26794)
  _*MRP creates planned orders that are fractional vendor UOM_
- Fixed issue #[26796](http://www.xtuple.org/xtincident/view/bugs/26796)
  _*'Setup' menu item is being displayed as 'xSetup' in Macintosh
  Environment_
- Fixed issue #[26804](http://www.xtuple.org/xtincident/view/bugs/26804)
  _*Pack date_
- Fixed issue #[26815](http://www.xtuple.org/xtincident/view/bugs/26815)
  _*'New' button is in enable mode in 'Maintain Item Costs' screen
  irrelevantly_
- Fixed issue #[26818](http://www.xtuple.org/xtincident/view/bugs/26818)
  _* Irrelevant behavior is observed in 'Role' screen_
- Fixed issue #[26822](http://www.xtuple.org/xtincident/view/bugs/26822)
  _*Error posting AP misc voucher_
- Fixed issue #[26823](http://www.xtuple.org/xtincident/view/bugs/26823)
  _*exceeding allowed concurrent license user_
- Fixed issue #[26824](http://www.xtuple.org/xtincident/view/bugs/26824)
  _*System does not check drop ship box for drop ship items if the
  Create Purchase Order box is cleared for a previous line item_
- Fixed issue #[26829](http://www.xtuple.org/xtincident/view/bugs/26829)
  _*'Vendor: Vendor #:' is displayed instead of 'Vendor#:' in 'Item
  Sources' dialog_
- Fixed issue #[26834](http://www.xtuple.org/xtincident/view/bugs/26834)
  _*The quantity info in the orders tab, sales order section of the
  item avail WB is innacurate_
- Fixed issue #[26836](http://www.xtuple.org/xtincident/view/bugs/26836)
  _*Db log error is generated on selecting to duplicate 'Project
  Types'_
- Fixed issue #[26837](http://www.xtuple.org/xtincident/view/bugs/26837)
  _* Irrelevant behavior is observed in 'Customer Prices' tab under
  'Item Availability Workbench' screen_
- Fixed issue #[26838](http://www.xtuple.org/xtincident/view/bugs/26838)
  _*Irrelevant dialog box is displayed in 'Item Availability
  Workbench' screen_
- Fixed issue #[26841](http://www.xtuple.org/xtincident/view/bugs/26841)
  _*blank line on the layout shipment by shipment_
- Fixed issue #[26846](http://www.xtuple.org/xtincident/view/bugs/26846)
  _*Line item entered after canceling item not saved_
- Fixed issue #[26847](http://www.xtuple.org/xtincident/view/bugs/26847)
  _*System allows changing sales order quantity for a job cost item
  without changing work order quantity, after it has been shipped_
- Fixed issue #[26848](http://www.xtuple.org/xtincident/view/bugs/26848)
  _RR Transaction type missing from Usage Statistics report_
- Fixed issue #[26850](http://www.xtuple.org/xtincident/view/bugs/26850)
  _*No space is observed for 'thedatabase' text in 'Database
  disconnected' dialog box_
- Fixed issue #[26882](http://www.xtuple.org/xtincident/view/bugs/26882)
  _*whereUsed details SQL Metaquery is incorrect_
- Fixed issue #[26888](http://www.xtuple.org/xtincident/view/bugs/26888)
  _*Error copying item with multiple location control set_
- Fixed issue #[26890](http://www.xtuple.org/xtincident/view/bugs/26890)
  _*xTuple is incorrectly setting Pick List status on Work Order
  Material Requirement dialog_
- Fixed issue #[26903](http://www.xtuple.org/xtincident/view/bugs/26903)
  _*Work Order # column on Work Order Schedule screen sorts in
  alphabetical order instead of numerical order_
- Fixed issue #[26904](http://www.xtuple.org/xtincident/view/bugs/26904)
  _*DB log error is displayed irrelevantly in 'Item' screen_
- Fixed issue #[26922](http://www.xtuple.org/xtincident/view/bugs/26922)
  _Changing an item to use job costing with open orders for that
  item can lead to unpredictable results_
- Fixed issue #[26926](http://www.xtuple.org/xtincident/view/bugs/26926)
  _* 'Prospects' screen is not being updated automatically_
- Fixed issue #[26933](http://www.xtuple.org/xtincident/view/bugs/26933)
  _* Irrelevant behavior is observed in 'Purchase Types' screen._
- Fixed issue #[26935](http://www.xtuple.org/xtincident/view/bugs/26935)
  _*'Issue Additional Stock to Order Line' doesn't populate with
  the order number in Maintain Shipping   Contents screen_
- Fixed issue #[26936](http://www.xtuple.org/xtincident/view/bugs/26936)
  _*new Cash Receipt does not handle Applications list properly
  when 'Customer #:'  is removed_
- Fixed issue #[26942](http://www.xtuple.org/xtincident/view/bugs/26942)
  _*Blank names are being displayed instead of 'Default' in Customer
  Form Assignment_
- Fixed issue #[26944](http://www.xtuple.org/xtincident/view/bugs/26944)
  _* Irrelevant dialog box name is displayed in 'Material Usage
  Variance by Work Order'_
- Fixed issue #[26945](http://www.xtuple.org/xtincident/view/bugs/26945)
  _*'Work Order' default filter is not being displayed on selecting
  to open 'Labor Variance By Work Order' screen_
- Fixed issue #[26947](http://www.xtuple.org/xtincident/view/bugs/26947)
  _*Irrelevant behavior is observed in 'Print Invoice' screen_
- Fixed issue #[26956](http://www.xtuple.org/xtincident/view/bugs/26956)
  _* Irrelevant dialog box name is displayed in  'Work Order History
  by W/O Number'_
- Fixed issue #[26957](http://www.xtuple.org/xtincident/view/bugs/26957)
  _* Irrelevant behavior is observed on 'Work Order Operations By
  Work Order' screen_
- Fixed issue #[26958](http://www.xtuple.org/xtincident/view/bugs/26958)
  _*On Selecting to query the screen irrelevant dialog box name is
  displayed in 'Single Level Bill of Materials' screen_
- Fixed issue #[26959](http://www.xtuple.org/xtincident/view/bugs/26959)
  _Purchased Job Costed items_
- Fixed issue #[26969](http://www.xtuple.org/xtincident/view/bugs/26969)
  _*Negative As Off QOH for average items_
- Fixed issue #[26975](http://www.xtuple.org/xtincident/view/bugs/26975)
  _*No spacing is observed in the error message of 'Cannot Save
  Sales Order' dialog_
- Fixed issue #[26977](http://www.xtuple.org/xtincident/view/bugs/26977)
  _*Item Attributes tab resizing not working_
- Fixed issue #[26981](http://www.xtuple.org/xtincident/view/bugs/26981)
  _*Transfer Order 'Line#' is not being updated properly in 'Transfer
  Order Item' screen_
- Fixed issue #[27007](http://www.xtuple.org/xtincident/view/bugs/27007)
  _confusing label on credit card account setup_
- Fixed issue #[27014](http://www.xtuple.org/xtincident/view/bugs/27014)
  _Cannot view open RA items by status_
- Fixed issue #[27015](http://www.xtuple.org/xtincident/view/bugs/27015)
  _*BOM Items with Issue Child W/O to Parent W/O at Receipt flag
  are not issued to parent._
- Fixed issue #[27040](http://www.xtuple.org/xtincident/view/bugs/27040)
  _*UOM conversion for subassembly order fails upon changing parent
  WO qty_
- Fixed issue #[27047](http://www.xtuple.org/xtincident/view/bugs/27047)
  _xwd hides SO More button for all unprivileged users_
- Fixed issue #[27055](http://www.xtuple.org/xtincident/view/bugs/27055)
  _"The QT Scroll Bug"_
- Fixed issue #[27057](http://www.xtuple.org/xtincident/view/bugs/27057)
  _*Service Orders_
- Fixed issue #[27068](http://www.xtuple.org/xtincident/view/bugs/27068)
  _*Unable to issue subassembly using UoM Conversion_
- Fixed issue #[27098](http://www.xtuple.org/xtincident/view/bugs/27098)
  _*User is able to save a record with spaces in 'Company Number'
  screen_
- Fixed issue #[27116](http://www.xtuple.org/xtincident/view/bugs/27116)
  _Closed projects showing up in lookup list_
- Fixed issue #[27144](http://www.xtuple.org/xtincident/view/bugs/27144)
  _*'Bills of materials' screen is not being updated properly_
- Fixed issue #[27158](http://www.xtuple.org/xtincident/view/bugs/27158)
  _Item Usage Statistics report missing some inventory transactions_
- Fixed issue #[27159](http://www.xtuple.org/xtincident/view/bugs/27159)
  _*No Item Groups are present in 'List Item Groups' screen
  irrelevantly_
- Fixed issue #[27167](http://www.xtuple.org/xtincident/view/bugs/27167)
  _*Supply orders planned at end of first MRP period_
- Fixed issue #[27178](http://www.xtuple.org/xtincident/view/bugs/27178)
  _*Irrelevant behavior is observed in Lot/Serial Sequences screen_
- Fixed issue #[27284](http://www.xtuple.org/xtincident/view/bugs/27284)
  _*Recall Orders to Shipping - Screen Hangs_
- Fixed issue #[27310](http://www.xtuple.org/xtincident/view/bugs/27310)
  _*Wrong order of steps for Post Production dialog_
- Fixed issue #[27314](http://www.xtuple.org/xtincident/view/bugs/27314)
  _itemcluster_
- Fixed issue #[27339](http://www.xtuple.org/xtincident/view/bugs/27339)
  _*Purchase Order Characteristics Not Saved_
- Fixed issue #[27348](http://www.xtuple.org/xtincident/view/bugs/27348)
  _Project Types menu item is in the wrong place_
- Fixed issue #[27353](http://www.xtuple.org/xtincident/view/bugs/27353)
  _*Purchase requests released in bulk ignore order minimum_
- Fixed issue #[27359](http://www.xtuple.org/xtincident/view/bugs/27359)
  _*Irrelevant behavior is observed in Vendor Catalog Conversion
  Configuration screen_
- Fixed issue #[27360](http://www.xtuple.org/xtincident/view/bugs/27360)
  _Project Type combobox does not populate for new Projects_
- Fixed issue #[27367](http://www.xtuple.org/xtincident/view/bugs/27367)
  _Project field called Notes - but called Description in Project
  List_
- Fixed issue #[27377](http://www.xtuple.org/xtincident/view/bugs/27377)
  _*WO auto issue date error_
- Fixed issue #[27383](http://www.xtuple.org/xtincident/view/bugs/27383)
  _*Multi-currency checks will not post_
- Fixed issue #[27405](http://www.xtuple.org/xtincident/view/bugs/27405)
  _*Deleting a Customer Group has no confirmation dialog box_
- Fixed issue #[27417](http://www.xtuple.org/xtincident/view/bugs/27417)
  _*User is not able to receive the line items from  'Enter Order
  Receipts' screen_
- Fixed issue #[27422](http://www.xtuple.org/xtincident/view/bugs/27422)
  _*Unable to convert external vendor catalog item irrelevantly_
- Fixed issue #[27430](http://www.xtuple.org/xtincident/view/bugs/27430)
  _*Inventory availability report hides non-usable information_
- Fixed issue #[27445](http://www.xtuple.org/xtincident/view/bugs/27445)
  _User defined cost on Average costed items not calculating
  correctly_
- Fixed issue #[27466](http://www.xtuple.org/xtincident/view/bugs/27466)
  _'No work week calendar found' dialog is being displayed twice
  in 'Quote' screen irrelevantly_
- Fixed issue #[27467](http://www.xtuple.org/xtincident/view/bugs/27467)
  _*'Non-Working Day Entered' dialog is displayed irrelevantly on
  selecting to view a Work order_
- Fixed issue #[27473](http://www.xtuple.org/xtincident/view/bugs/27473)
  _P/R Release does not copy Project to P/O Item_
- Fixed issue #[27478](http://www.xtuple.org/xtincident/view/bugs/27478)
  _Inconsistent Status text in Project API View_
- Fixed issue #[27485](http://www.xtuple.org/xtincident/view/bugs/27485)
  _*ItemSource column hiding error_
- Fixed issue #[27496](http://www.xtuple.org/xtincident/view/bugs/27496)
  _*Item Type filter on the Item List screen works incorrectly_
- Fixed issue #[27512](http://www.xtuple.org/xtincident/view/bugs/27512)
  _*Completed projects available to new sales orders, quotes, and
  purchase orders_
- Fixed issue #[27517](http://www.xtuple.org/xtincident/view/bugs/27517)
  _Serial Column integritry screen should ignore foreign tables_
- Fixed issue #[27524](http://www.xtuple.org/xtincident/view/bugs/27524)
  _Location Controlled inventory requires "W/O Issue" location
  default when shipping._
- Fixed issue #[27559](http://www.xtuple.org/xtincident/view/bugs/27559)
  _*Typo error is observed on 'Location' screen_
- Fixed issue #[27571](http://www.xtuple.org/xtincident/view/bugs/27571)
  _*Typing in Issue Stock dialog's Qty to Issue field does not work
  as expected for non-fractional items_
- Fixed issue #[27573](http://www.xtuple.org/xtincident/view/bugs/27573)
  _*When the "Sales Order Status" screen is first open the cursor
  is not in the order # field_
- Fixed issue #[27574](http://www.xtuple.org/xtincident/view/bugs/27574)
  _*When the "Post Production" screen is first open the cursor is
  not in the Qty. to Post field_
- Fixed issue #[27619](http://www.xtuple.org/xtincident/view/bugs/27619)
  _*Ubuntu: 'Notice' dialog box is opened behind the xtuple application
  irrelevantly_
- Fixed issue #[27633](http://www.xtuple.org/xtincident/view/bugs/27633)
  _Validators missing on characteristic_
- Fixed issue #[27635](http://www.xtuple.org/xtincident/view/bugs/27635)
  _*WOs created from SOs do not operate as expected._
- Fixed issue #[27643](http://www.xtuple.org/xtincident/view/bugs/27643)
  _*Authorize.net transaction ID issue_
- Fixed issue #[27646](http://www.xtuple.org/xtincident/view/bugs/27646)
  _Smooth Margin does not appear to test the Long30Markup metric_
- Fixed issue #[27659](http://www.xtuple.org/xtincident/view/bugs/27659)
  _*Time-Phase Planned Rev/Exp by Planner Code Error_
- Fixed issue #[27662](http://www.xtuple.org/xtincident/view/bugs/27662)
  _*Irrelevant behavior is observed on Approve payments screen_
- Fixed issue #[27681](http://www.xtuple.org/xtincident/view/bugs/27681)
  _*Check Numbers Wrong_
- Fixed issue #[27694](http://www.xtuple.org/xtincident/view/bugs/27694)
  _Issue to Shipping - Require Sufficient Inventory disabled and
  NOT checked_
- Fixed issue #[27700](http://www.xtuple.org/xtincident/view/bugs/27700)
  _User defined costs doubled when posting production_
- Fixed issue #[27728](http://www.xtuple.org/xtincident/view/bugs/27728)
  _project Type is not populating when Project window opened_


## Deployment Notes

We've lately revised the naming conventions and the behavior of our
core updater packages. Our overall goal is to simplify the process
of installing and upgrading xTuple ERP databases.

Just as was true for the 4.4.1 release, you will only need to apply
one updater package to upgrade to the latest release--that is, assuming you are
already running on at least 4.4.0. The new updater packages are
designed to bring you all the way up to their version, no matter
what version (>= 4.4.0!) that you're on.

Beginning with 4.5.0, we even went a step further: not only will a
single package take you through every *version* of the app, it will
also install all the constituent parts of your edition. Before now,
if you wanted to do an upgrade to the Manufacturing or Enterprise
Editions, you would have needed to perform the standard/dist upgrade
and then the manufacturing upgrade. Not any more. With the new process,
only one upgrade package is needed for the entire upgrade. No more
upgrading the core and then upgrading the related packages. Everything
is upgraded all at once.

NOTE FOR DISTRIBUTION EDITION CUSTOMERS: The xwd package no longer
exists as a separate entity. All the functionality that was contained
in the xwd package is now included in the single "distribution" upgrade
or install package.

To be verbose about all of this:

    postbooks-upgrade-491.gz will:
    upgrade a PostBooks database from anywhere >= 4.4.0 to 4.9.1

    distribution-upgrade-491.gz will:
    upgrade the standard/dist (i.e., inventory code) to 4.9.1
    upgrade the distribution (i.e., xwd code) to 4.9.1

    distribution-install-491.gz will:
    do a one-time install of tables, etc. for standard (i.e., inventory code) at 4.9.1
    do a one-time install of tables, etc. for distribution at 4.9.1

    manufacturing-upgrade-491.gz will:
    upgrade the standard/dist (i.e., inventory code) to 4.9.1
    upgrade the manufacturing code to 4.9.1

    manufacturing-install-491.gz will:
    do a one-time install of tables, etc. for standard (i.e., inventory code) at 4.9.1
    do a one-time install of tables, etc. for manufacturing at 4.9.1

    enterprise-upgrade-491.gz will:
    upgrade the standard/dist (i.e., inventory code) to 4.9.1
    upgrade the distribution (i.e., xwd code) to 4.9.1
    upgrade the manufacturing code to 4.9.1

    enterprise-install-491.gz will:
    do a one-time install of tables, etc. for standard (i.e., inventory code) at 4.9.1
    do a one-time install of tables, etc. for distribution at 4.9.1
    do a one-time install of tables, etc. for manufacturing at 4.9.1

PLEASE NOTE: Other packages, such as Advanced Commissions and Fixed
Assets, are currently remaining on their own release schedule and should
be installed as before.
