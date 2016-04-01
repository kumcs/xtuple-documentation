# xTuple Release Notes
## Version 4.10.0Beta * April, 2016

These are the release notes for the 4.10.0Beta xTuple ERP release.
Thanks to all who contributed to make this release possible, including
a number of feature sponsors.
See below for more information about [deploying this release](#deployment-notes).

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

**Note:** You will need PostgreSQL 9.3 or 9.4 to use this release
with the following two PostgreSQL extensions:

- plv8 
  See our
  [github wiki](https://github.com/xtuple/xtuple/wiki/Installing-PLv8) for
  more information on how to install plv8 and a
  [blog post](https://www.xtuple.org/blog/gmoskowitz/enabling-technologies-plv8-49)
  describing plv8 and why we introduced this new dependency.
- ossp-uuid
  If you built PostgreSQL from source code, might have to
  rebuild it. Make sure to include the `--with-ossp-uuid` option for
  the `configure` command. See
  [our instructions for building PostgreSQL](https://github.com/xtuple/qt-client/wiki/Desktop-Development-Environment-Setup#get-and-install-postgresql)
  for details.

These need to be installed on the database server, not client machines.

#### Features

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

#### Bug fixes

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
- Fixed issue $[26675](http://www.xtuple.org/xtincident/view/bugs/26675)
  _Random contact on PO shipto_


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
