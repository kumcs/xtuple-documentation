
# xTuple Release Notes

## Version 4.11.0 - August, 2017

These are the release notes for the 4.11.0 xTuple ERP release.
Thanks to all who contributed to make this release possible, including
[Daniel Pocock](https://forums.xtuple.com/u/pocock),
[Scott Moore](https://forums.xtuple.com/u/discountscott),
and [Steven Buttgereit](https://forums.xtuple.com/u/sbuttgereit496).
See below for more information about
[deploying this release](#deployment-notes).

### Summary

A large number of features and bug fixes have been added to the
application since the 4.10.1 release. Our focus has been on improving
the desktop client and preparing for upcoming xTupleCommerce features.

Of particular interest are the following:

- Completed support for Landed Cost
- Continued improvements in desktop client support for the Quality extension
- Continued improvements in desktop client support of the workflow engine
- Simplified reversal of A/R application
- Continued performance improvements
- Rudimentary (undocumented) widget scripting (issue #[28225](http://www.xtuple.org/xtincident/view/bugs/28225) WIP)

**Note:** See the xTuple ERP [Compatibility Matrix](https://xtupleuniversity.xtuple.com/library/articles/compatibility-matrix).
You will need the following two PostgreSQL extensions:

- plv8 -
  See our
  [github wiki](https://github.com/xtuple/xtuple/wiki/Installing-PLv8) for
  more information on how to install plv8 and a
  [blog post](https://www.xtuple.org/blog/gmoskowitz/enabling-technologies-plv8-49)
  describing plv8 and why we introduced this new dependency.
- ossp-uuid -
  If you built PostgreSQL from source code, you may have to
  rebuild it. Make sure to include the `--with-ossp-uuid` option for
  the `configure` command. See
  [our instructions for building PostgreSQL](https://github.com/xtuple/qt-client/wiki/Desktop-Development-Environment-Setup#get-and-install-postgresql)
  for details.

These need to be installed on the database server, not client machines.

### Bug fixes in 4.11.0

- Fixed issue #[27781](http://www.xtuple.org/xtincident/view/bugs/27781) _Schedule button available on "Create Recurring Items" utility despite Connect not installed_
- Fixed issue #[29612](http://www.xtuple.org/xtincident/view/bugs/29612) _crm account clusters for Sales Reps throw database error on List or Search_
- Fixed issue #[30465](http://www.xtuple.org/xtincident/view/bugs/30465) _'Create' button is not enabled when 'Create Recurring Items' window is opened having 'Invoice' option selected._
- Fixed issue #[30582](http://www.xtuple.org/xtincident/view/bugs/30582) _411 RA Slowness_
- Fixed issue #[30589](http://www.xtuple.org/xtincident/view/bugs/30589) _[qt-client] MetaSQL list defaults grade column to hidden_
- Fixed issue #[30600](http://www.xtuple.org/xtincident/view/bugs/30600) _4.11.0RC: Relocate Inventory screen issue_
- Fixed issue #[30663](http://www.xtuple.org/xtincident/view/bugs/30663) _Node.js database connections loose js_init'd search path_
- Fixed issue #[30675](http://www.xtuple.org/xtincident/view/bugs/30675) _REGRESSION:‘Price/Inv. Ratio’ field text is not aligned properly with the label name._
- Fixed issue #[30676](http://www.xtuple.org/xtincident/view/bugs/30676) _REGRESSION: ‘Pricing Schedule’ screen is opened twice when double clicking on a schedule in ‘Pricing Schedule’ screen._
- Fixed issue #[30681](http://www.xtuple.org/xtincident/view/bugs/30681) _Updater generates error due to flaw in createpackageschema(text,text)_
- Fixed issue #[30718](http://www.xtuple.org/xtincident/view/bugs/30718) _Orphaned itemlocdist records prevent upgrade to 4.11.0Beta or later_

## Version 4.11.0RC - July, 2017

These are the release notes for the 4.11.0RC xTuple ERP release.
Thanks to all who contributed to make this release possible, including
[Daniel Pocock](https://forums.xtuple.com/u/pocock),
[Scott Moore](https://forums.xtuple.com/u/discountscott),
and [Steven Buttgereit](https://forums.xtuple.com/u/sbuttgereit496).
See below for more information about
[deploying this release](#deployment-notes).

### Summary

A large number of features and bug fixes have been added to the
application since the 4.10.1 release. Our focus has been on improving
the desktop client and preparing for upcoming xTupleCommerce features.

Of particular interest are the following:

- Completed support for Landed Cost
- Continued improvements in desktop client support for the Quality extension
- Simplified reversal of A/R application
- Continued performance improvements
- Rudimentary (undocumented) widget scripting (issue #[28225](http://www.xtuple.org/xtincident/view/bugs/28225) WIP)

**Note:** See the xTuple ERP [Compatibility Matrix](https://xtupleuniversity.xtuple.com/library/articles/compatibility-matrix).
You will need the following two PostgreSQL extensions:

- plv8 -
  See our
  [github wiki](https://github.com/xtuple/xtuple/wiki/Installing-PLv8) for
  more information on how to install plv8 and a
  [blog post](https://www.xtuple.org/blog/gmoskowitz/enabling-technologies-plv8-49)
  describing plv8 and why we introduced this new dependency.
- ossp-uuid -
  If you built PostgreSQL from source code, you may have to
  rebuild it. Make sure to include the `--with-ossp-uuid` option for
  the `configure` command. See
  [our instructions for building PostgreSQL](https://github.com/xtuple/qt-client/wiki/Desktop-Development-Environment-Setup#get-and-install-postgresql)
  for details.

These need to be installed on the database server, not client machines.

### Features added in 4.11.0RC

- Features issue #[25491](http://www.xtuple.org/xtincident/view/bugs/25491) _Check Amount (Pre Discount)_
- Features issue #[25861](http://www.xtuple.org/xtincident/view/bugs/25861) _Add handling of Quality Tests when source document deleted/cancelled_
- Features issue #[28349](http://www.xtuple.org/xtincident/view/bugs/28349) _Make script-extensible implementation of VirtualCluster and VirtualClusterLineEdit_
- Features issue #[29702](http://www.xtuple.org/xtincident/view/bugs/29702) _Create Item Taxation template_
- Features issue #[30175](http://www.xtuple.org/xtincident/view/bugs/30175) _Add Customer Type as a search option with list_
- Features issue #[30322](http://www.xtuple.org/xtincident/view/bugs/30322) _Quote Items need to support sub-line items for Discount Pricing feature._

### Bug fixes in 4.11.0RC

- Fixed issue #[22868](http://www.xtuple.org/xtincident/view/bugs/22868) _Locking issues on transactions_
- Fixed issue #[26057](http://www.xtuple.org/xtincident/view/bugs/26057) _SQL Error when creating Quality Tests_
- Fixed issue #[26348](http://www.xtuple.org/xtincident/view/bugs/26348) _DB log error is displayed on selecting to print Order Activity By Project list from Project screen_
- Fixed issue #[26880](http://www.xtuple.org/xtincident/view/bugs/26880) _Cannot delete vendor commodity codes_
- Fixed issue #[27330](http://www.xtuple.org/xtincident/view/bugs/27330) _User is able to save operation Type with blank spaces_
- Fixed issue #[27708](http://www.xtuple.org/xtincident/view/bugs/27708) _Costing warning appears multiple times on releasing P/R_
- Fixed issue #[28020](http://www.xtuple.org/xtincident/view/bugs/28020) _Print Report for 'List Site Locations' is not displayed all Site Locations information_
- Fixed issue #[28089](http://www.xtuple.org/xtincident/view/bugs/28089) _Deleted Sales Order Items when CC payment applied_
- Fixed issue #[28622](http://www.xtuple.org/xtincident/view/bugs/28622) _Received DropShip PO linked to deleted SO_
- Fixed issue #[29224](http://www.xtuple.org/xtincident/view/bugs/29224) _Can't Migrate to 4.10 - avg costing and negative inventory problems after upgrade_
- Fixed issue #[29225](http://www.xtuple.org/xtincident/view/bugs/29225) _Vendor AP History does not display detail when AP Item is void_
- Fixed issue #[29233](http://www.xtuple.org/xtincident/view/bugs/29233) _Site Transfer does not respect Lot/Serial in all situations_
- Fixed issue #[29285](http://www.xtuple.org/xtincident/view/bugs/29285) _User can view pricing schedules even though ViewPricingSchedules privilege is not assigned_
- Fixed issue #[29304](http://www.xtuple.org/xtincident/view/bugs/29304) _Packing List Batch allows the addition of orders that do not display_
- Fixed issue #[29317](http://www.xtuple.org/xtincident/view/bugs/29317) _Db log error is observed instead of alert box in 'General Ledger Transactions' screen_
- Fixed issue #[29409](http://www.xtuple.org/xtincident/view/bugs/29409) _Purchase Requistion by Item - disabled Item Number when creating new PR_
- Fixed issue #[29435](http://www.xtuple.org/xtincident/view/bugs/29435) _'Description' column is not being updated in 'Relationships' tab of 'Item' screen._
- Fixed issue #[29694](http://www.xtuple.org/xtincident/view/bugs/29694) _xTupleCommerce: Change DB ShipVia Code for Fedex_
- Fixed issue #[29720](http://www.xtuple.org/xtincident/view/bugs/29720) _""Update Inventory"" checkbox on Credit Memo item ignores interfaceToGL metric_
- Fixed issue #[29772](http://www.xtuple.org/xtincident/view/bugs/29772) _'New' button is in enabled mode under 'Quotes' tab in 'Prospect' screen when creating New prospect._
- Fixed issue #[29860](http://www.xtuple.org/xtincident/view/bugs/29860) _*Quality Reports for US Letter_
- Fixed issue #[29872](http://www.xtuple.org/xtincident/view/bugs/29872) _*Database error is displayed on clicking 'OK' button in 'Data Missing' dialog box of 'Quality Plan' screen._
- Fixed issue #[29907](http://www.xtuple.org/xtincident/view/bugs/29907) _Wrong Check Number Printed and Updated_
- Fixed issue #[29931](http://www.xtuple.org/xtincident/view/bugs/29931) _A user with a . in their username is unable to copy financial reports_
- Fixed issue #[29960](http://www.xtuple.org/xtincident/view/bugs/29960) _Inactive Items still show up under pricing by customer type_
- Fixed issue #[30005](http://www.xtuple.org/xtincident/view/bugs/30005) _Size of List Price field in Item screen_
- Fixed issue #[30008](http://www.xtuple.org/xtincident/view/bugs/30008) _Incorrectly assign owner to vendor when usernames are close_
- Fixed issue #[30018](http://www.xtuple.org/xtincident/view/bugs/30018) _Work Order Material Requirements Not Being Updated with WO Changes_
- Fixed issue #[30041](http://www.xtuple.org/xtincident/view/bugs/30041) _cannot change due date on PO from PR_
- Fixed issue #[30083](http://www.xtuple.org/xtincident/view/bugs/30083) _'PurchaseVendorRelation' dependency error is displayed when tried to do buildapp on Manufacturing Empty database_
- Fixed issue #[30090](http://www.xtuple.org/xtincident/view/bugs/30090) _Unused Purchased Items not filtering inactive items_
- Fixed issue #[30111](http://www.xtuple.org/xtincident/view/bugs/30111) _Detailed Inventory History by Lot/Serial# Pattern must be ALL CAPS_
- Fixed issue #[30114](http://www.xtuple.org/xtincident/view/bugs/30114) _Error posting cash receipts_
- Fixed issue #[30133](http://www.xtuple.org/xtincident/view/bugs/30133) _Create Lot/Serial Form Fails to Properly Eval Fractional/Non-Fractional Entry_
- Fixed issue #[30134](http://www.xtuple.org/xtincident/view/bugs/30134) _Issue to Ship Line Item Right Click Menu Shows Reservation Items for Transfer Orders_
- Fixed issue #[30138](http://www.xtuple.org/xtincident/view/bugs/30138) _'SSL error' dialog is displayed when credit card settings are saved in credit card setup configuration screen_
- Fixed issue #[30157](http://www.xtuple.org/xtincident/view/bugs/30157) _Post dated AR Cash receipts display issue_
- Fixed issue #[30158](http://www.xtuple.org/xtincident/view/bugs/30158) _workflow module not working_
- Fixed issue #[30161](http://www.xtuple.org/xtincident/view/bugs/30161) _Able to create duplicate 'Purchase Type' in 'Purchase Types' screen._
- Fixed issue #[30166](http://www.xtuple.org/xtincident/view/bugs/30166) _[qt-client] createLotSerial.cpp tries to look up expiration/warranty using incorrect ids_
- Fixed issue #[30171](http://www.xtuple.org/xtincident/view/bugs/30171) _xt.ver error due to unexpected trigger order in web-enabled databases_
- Fixed issue #[30183](http://www.xtuple.org/xtincident/view/bugs/30183) _npm install failes with npm ERR! 404 'types/node' is not in the npm registry._
- Fixed issue #[30183](http://www.xtuple.org/xtincident/view/bugs/30183) _npm install fails with npm ERR! 404 'types/node' is not in the npm registry._
- Fixed issue #[30185](http://www.xtuple.org/xtincident/view/bugs/30185) _Issues with blank UPC codes when Unique Barcode setting is active_
- Fixed issue #[30186](http://www.xtuple.org/xtincident/view/bugs/30186) _disable triggers when updating schema_
- Fixed issue #[30214](http://www.xtuple.org/xtincident/view/bugs/30214) _upgrading to 4.11.0-beta with existing xt.potype gets dependency errors_
- Fixed issue #[30216](http://www.xtuple.org/xtincident/view/bugs/30216) _[qt-client] Itemsites with Control Method set to ""None"" show up on Inventory Availability report_
- Fixed issue #[30224](http://www.xtuple.org/xtincident/view/bugs/30224) _Workflow package missing description and version_
- Fixed issue #[30230](http://www.xtuple.org/xtincident/view/bugs/30230) _report design won't open_
- Fixed issue #[30237](http://www.xtuple.org/xtincident/view/bugs/30237) _411B List Price Not Recorded in ERP When Price Schedule Discount is Applied to List Price_
- Fixed issue #[30250](http://www.xtuple.org/xtincident/view/bugs/30250) _Critical Error alert is displayed on clicking 'New' button in 'Workflow' screen._
- Fixed issue #[30251](http://www.xtuple.org/xtincident/view/bugs/30251) _'Error' dialog box is displayed on adding a 'Available Successors:' in 'On Completion' tab of 'Workflow step' screen_
- Fixed issue #[30252](http://www.xtuple.org/xtincident/view/bugs/30252) _Price Schedules linked to exclusive items do not calculate price_
- Fixed issue #[30299](http://www.xtuple.org/xtincident/view/bugs/30299) _Able to ship the sales order for multiple times._
- Fixed issue #[30301](http://www.xtuple.org/xtincident/view/bugs/30301) _'Failed post List' error dialog is displayed while posting the Invoice for sales order._
- Fixed issue #[30363](http://www.xtuple.org/xtincident/view/bugs/30363) _Documents attached to vouchers missing_
- Fixed issue #[30378](http://www.xtuple.org/xtincident/view/bugs/30378) _Characteristic Value Choices Are Not Sequenced in Search_
- Fixed issue #[30422](http://www.xtuple.org/xtincident/view/bugs/30422) _unable to delete 'WH1' & 'WH2' item sites from 'Item screen when a new item is created by copying 'YTRUCK1'_
- Fixed issue #[30424](http://www.xtuple.org/xtincident/view/bugs/30424) _Bank Reconciliation Very Slow_
- Fixed issue #[30434](http://www.xtuple.org/xtincident/view/bugs/30434) _In ‘User Account Information’ screen, ‘Employee’ label name is not visible properly._
- Fixed issue #[30437](http://www.xtuple.org/xtincident/view/bugs/30437) _Attach Quality Plan/Test Doc causes client to crash_
- Fixed issue #[30439](http://www.xtuple.org/xtincident/view/bugs/30439) _Bom revision changes not captured correctly on comments_
- Fixed issue #[30456](http://www.xtuple.org/xtincident/view/bugs/30456) _*‘Error Issuing Item’ dialog is  displayed when issuing the sales order for both  ‘Lot’ & ‘Serial’ items._
- Fixed issue #[30463](http://www.xtuple.org/xtincident/view/bugs/30463) _On entering ‘Vendor:’ in ‘Buy Card’ screen, purchase history of vendor part number is not displayed by default._
- Fixed issue #[30466](http://www.xtuple.org/xtincident/view/bugs/30466) _Database Log Error is displayed after editing the Incident Recurring details and Incidents list is also not updated_
- Fixed issue #[30469](http://www.xtuple.org/xtincident/view/bugs/30469) _Post Operation when the user / server in different timezone:  wooperpost - wrong date and time_
- Fixed issue #[30471](http://www.xtuple.org/xtincident/view/bugs/30471) _*Quality tests are not created when doing partial post production with sampling frequency ‘Last Item’._
- Fixed issue #[30472](http://www.xtuple.org/xtincident/view/bugs/30472) _Existing Vendors payment information is displayed in ‘Checks’ screen under ‘Accounting’ tab of new vendor screen._
- Fixed issue #[30482](http://www.xtuple.org/xtincident/view/bugs/30482) _Logged in user who is not a ‘Purchasing Agent’ is displayed as ‘Purchasing Agent’ in Purchase Order screen._
- Fixed issue #[30486](http://www.xtuple.org/xtincident/view/bugs/30486) _deleteitemlocdist(integer) Performance is terrible_
- Fixed issue #[30494](http://www.xtuple.org/xtincident/view/bugs/30494) _4.11 beta - certain items unable to save bar code_
- Fixed issue #[30512](http://www.xtuple.org/xtincident/view/bugs/30512) _ ‘Error Receiving P/O Line Items’ is displayed while receiving the Return Authorization._
- Fixed issue #[30517](http://www.xtuple.org/xtincident/view/bugs/30517) _System does not use conversions when changing the quantity of a sales order item tied to a generated purchase order item_
- Fixed issue #[30524](http://www.xtuple.org/xtincident/view/bugs/30524) _REGRESSION: Database error is displayed while creating ‘Time’ Worksheet._
- Fixed issue #[30528](http://www.xtuple.org/xtincident/view/bugs/30528) _REGRESSION: On activating 'Pending' Revision of Location Controlled Item, error message is being displayed._
- Fixed issue #[30537](http://www.xtuple.org/xtincident/view/bugs/30537) _REGRESSION: ‘Error Occurred’ dialog is displayed while creating recurring Invoice in PostBooks edition_
- Fixed issue #[30547](http://www.xtuple.org/xtincident/view/bugs/30547) _411 Main Top Menu Window Sector Fails_
- Fixed issue #[30575](http://www.xtuple.org/xtincident/view/bugs/30575) _Customer widget has numerous issues_

## Version 4.11.0Beta - May, 2017

These are the release notes for the 4.11.0Beta xTuple ERP release.
Thanks to all who contributed to make this release possible. See below for more information about
[deploying this release](#deployment-notes).

### Summary

A large number of features and bug fixes have been added to the
application since the 4.10.1 release. Our focus has been on improving
the desktop client and preparing for upcoming xTupleCommerce features.

Of particular interest are the following:

- Completed support for Landed Cost
- Continued improvements in desktop client support for the Quality extension
- Simplified reversal of A/R application
- Continued performance improvements
- Rudimentary (undocumented) widget scripting (issue #[28225](http://www.xtuple.org/xtincident/view/bugs/28225) WIP)

**Note:** See the xTuple ERP [Compatibility Matrix](https://xtupleuniversity.xtuple.com/library/articles/compatibility-matrix).
You will need the following two PostgreSQL extensions:

- plv8 -
  See our
  [github wiki](https://github.com/xtuple/xtuple/wiki/Installing-PLv8) for
  more information on how to install plv8 and a
  [blog post](https://www.xtuple.org/blog/gmoskowitz/enabling-technologies-plv8-49)
  describing plv8 and why we introduced this new dependency.
- ossp-uuid -
  If you built PostgreSQL from source code, you may have to
  rebuild it. Make sure to include the `--with-ossp-uuid` option for
  the `configure` command. See
  [our instructions for building PostgreSQL](https://github.com/xtuple/qt-client/wiki/Desktop-Development-Environment-Setup#get-and-install-postgresql)
  for details.

These need to be installed on the database server, not client machines.

### Features

- Features issue #[2295](http://www.xtuple.org/xtincident/view/bugs/2295) _Copy Item Site when Copy Item Master_
- Features issue #[2903](http://www.xtuple.org/xtincident/view/bugs/2903) _Add POST option on Enter Cash Receipts_
- Features issue #[9241](http://www.xtuple.org/xtincident/view/bugs/9241) _Improve performance by caching lists for xcombobox_
- Features issue #[9757](http://www.xtuple.org/xtincident/view/bugs/9757) _Add a "Search" field to List Open Sales Order screen_
- Features issue #[18333](http://www.xtuple.org/xtincident/view/bugs/18333) _Order Sales Backlog on Scheduled Date_
- Features issue #[20113](http://www.xtuple.org/xtincident/view/bugs/20113) _Landed cost_
- Features issue #[26367](http://www.xtuple.org/xtincident/view/bugs/26367) _Add ability to "unallocate" Credit Memos_
- Features issue #[26390](http://www.xtuple.org/xtincident/view/bugs/26390) _Landed Cost_
- Features issue #[26765](http://www.xtuple.org/xtincident/view/bugs/26765) _Distribution of header freight to voucher lines costing elements_
- Features issue #[26924](http://www.xtuple.org/xtincident/view/bugs/26924) _updates for Catcost Windows_
- Features issue #[27164](http://www.xtuple.org/xtincident/view/bugs/27164) _Move workflow tables into core_
- Features issue #[27308](http://www.xtuple.org/xtincident/view/bugs/27308) _PAIN - Selecting Open Sales Order from Open Sales Orders redundant queries running_
- Features issue #[28101](http://www.xtuple.org/xtincident/view/bugs/28101) _Add xTuple as a vendor in the reference dbs_
- Features issue #[28298](http://www.xtuple.org/xtincident/view/bugs/28298) _Repeated ach batch numbers_
- Features issue #[28578](http://www.xtuple.org/xtincident/view/bugs/28578) _Add search by SO# to Param Widget and Search in toolbar on dspSalesOrders screen_
- Features issue #[28594](http://www.xtuple.org/xtincident/view/bugs/28594) _Submission Proposal: Make PL/pgSQL function public.adjustInvValue accept optional doc number_
- Features issue #[28606](http://www.xtuple.org/xtincident/view/bugs/28606) _Add Numeric option to Characteristics Type_
- Features issue #[28640](http://www.xtuple.org/xtincident/view/bugs/28640) _Better sorting on Incident Workbench_
- Features issue #[28699](http://www.xtuple.org/xtincident/view/bugs/28699) _Display indicator of Shipto Active / Inactive Status_
- Features issue #[28730](http://www.xtuple.org/xtincident/view/bugs/28730) _Add WIP value to work order schedule_
- Features issue #[28763](http://www.xtuple.org/xtincident/view/bugs/28763) _Expose guiErrorCheck to script_
- Features issue #[28773](http://www.xtuple.org/xtincident/view/bugs/28773) _Customer PO# Needed on Open Receivables Report_
- Features issue #[28799](http://www.xtuple.org/xtincident/view/bugs/28799) _Need to record a Work Order Close Date_
- Features issue #[28817](http://www.xtuple.org/xtincident/view/bugs/28817) _Reason Code on Sales Credit_
- Features issue #[28859](http://www.xtuple.org/xtincident/view/bugs/28859) _Add Filters to Unapplied Credit Memos screen_
- Features issue #[28882](http://www.xtuple.org/xtincident/view/bugs/28882) _add tax to poitem api_
- Features issue #[28925](http://www.xtuple.org/xtincident/view/bugs/28925) _API view for vendor comments_
- Features issue #[28962](http://www.xtuple.org/xtincident/view/bugs/28962) _Add AP Payment On Hold comment_
- Features issue #[29284](http://www.xtuple.org/xtincident/view/bugs/29284) _Make "Start Date" on Customer/Sales tab configurable_
- Features issue #[29303](http://www.xtuple.org/xtincident/view/bugs/29303) _Add reverse application feature to the core_
- Features issue #[29602](http://www.xtuple.org/xtincident/view/bugs/29602) _Reporting needed for Return Authorisations_
- Features issue #[29882](http://www.xtuple.org/xtincident/view/bugs/29882) _Make menu preferences available to user accounts and role screens_

### Bug fixes

- Fixed issue #[9200](http://www.xtuple.org/xtincident/view/bugs/9200) _Application inserting a prefix to Company ID_
- Fixed issue #[12189](http://www.xtuple.org/xtincident/view/bugs/12189) _Issue additional stock right click option opens behind screen._
- Fixed issue #[16967](http://www.xtuple.org/xtincident/view/bugs/16967) _High Frequency Recurring Jobs need to increment on now() + INTERVAL_
- Fixed issue #[19902](http://www.xtuple.org/xtincident/view/bugs/19902) _Error message only partially translatable_
- Fixed issue #[25077](http://www.xtuple.org/xtincident/view/bugs/25077) _Margin and Margin % are displaying incorrectly in the Unposted Invoice and Invoice windows_
- Fixed issue #[25224](http://www.xtuple.org/xtincident/view/bugs/25224) _Sales Order Item Entry Speed Issues_
- Fixed issue #[26373](http://www.xtuple.org/xtincident/view/bugs/26373) _Irrelevant behavior is observed on selecting to create a Return Authorization when 'Return Auth. #Generation' set to 'Manual'_
- Fixed issue #[26416](http://www.xtuple.org/xtincident/view/bugs/26416) _Qt Designer raises database errors from applock.cpp when loading the xTuple widgets library_
- Fixed issue #[26716](http://www.xtuple.org/xtincident/view/bugs/26716) _SO $$$ balance is showing payment due even though the SO is paid in full_
- Fixed issue #[27500](http://www.xtuple.org/xtincident/view/bugs/27500) _Sales History_
- Fixed issue #[28020](http://www.xtuple.org/xtincident/view/bugs/28020) _Print Report for 'List Site Locations' is not displayed all Site Locations information_
- Fixed issue #[28136](http://www.xtuple.org/xtincident/view/bugs/28136) _Error turning on AS OF qty on hand_
- Fixed issue #[28170](http://www.xtuple.org/xtincident/view/bugs/28170) _Constrain missing bankrecitem_
- Fixed issue #[28304](http://www.xtuple.org/xtincident/view/bugs/28304) _New project field misaligned on cash receipt_
- Fixed issue #[28418](http://www.xtuple.org/xtincident/view/bugs/28418) _'Cust.Type' is displayed as 'Undefined' by default in 'Return Authorization' screen._
- Fixed issue #[28512](http://www.xtuple.org/xtincident/view/bugs/28512) _INACTIVE SHIP TO APPEAR_
- Fixed issue #[28536](http://www.xtuple.org/xtincident/view/bugs/28536) _Multi-Level Trace not working_
- Fixed issue #[28546](http://www.xtuple.org/xtincident/view/bugs/28546) _WIP value disappear when deleting Work Order_
- Fixed issue #[28564](http://www.xtuple.org/xtincident/view/bugs/28564) _Non-inventory items appear on inventory reports_
- Fixed issue #[28568](http://www.xtuple.org/xtincident/view/bugs/28568) _Inactive item available for selection on Pricing Schedule Item screen_
- Fixed issue #[28584](http://www.xtuple.org/xtincident/view/bugs/28584) _Payables screen on vendor workbench needs query option_
- Fixed issue #[28585](http://www.xtuple.org/xtincident/view/bugs/28585) _Default customer credit status needed_
- Fixed issue #[28589](http://www.xtuple.org/xtincident/view/bugs/28589) _New credit limit check does not prevent shipping_
- Fixed issue #[28611](http://www.xtuple.org/xtincident/view/bugs/28611) _Journals listed under 'Eligible Sources' pane are disappeared on enabling 'Preview Posting' checkbox in 'Post Journals' screen._
- Fixed issue #[28631](http://www.xtuple.org/xtincident/view/bugs/28631) _Slow moving inventory report contains empty group box_
- Fixed issue #[28633](http://www.xtuple.org/xtincident/view/bugs/28633) _Confusion over short code abbreviations for funds type Other and Other Credit Card_
- Fixed issue #[28669](http://www.xtuple.org/xtincident/view/bugs/28669) _Able to create purchase order linked to sales order for an item which is not having standard cost._
- Fixed issue #[28697](http://www.xtuple.org/xtincident/view/bugs/28697) _Unable to delete item sites in PostBooks edition._
- Fixed issue #[28706](http://www.xtuple.org/xtincident/view/bugs/28706) _'Error Saving Credit Memo Information' dialog is displayed multiple times for customer say 'XTRM' in 'Sales Credit' screen_
- Fixed issue #[28718](http://www.xtuple.org/xtincident/view/bugs/28718) _Cannot Delete a credit card._
- Fixed issue #[28719](http://www.xtuple.org/xtincident/view/bugs/28719) _Item Description is missing from available columns in material req' report_
- Fixed issue #[28721](http://www.xtuple.org/xtincident/view/bugs/28721) _'Work Order' screen is displayed behind the 'Work Order History by W/O Number' screen while editing from Work Order History Scre_
- Fixed issue #[28723](http://www.xtuple.org/xtincident/view/bugs/28723) _"Release..." label implies a further dialog box, but none exists_
- Fixed issue #[28742](http://www.xtuple.org/xtincident/view/bugs/28742) _Update init.sql to support PostgreSQL 9.5+_
- Fixed issue #[28743](http://www.xtuple.org/xtincident/view/bugs/28743) _Workflow can be enabled in 2 places (but should not be)_
- Fixed issue #[28747](http://www.xtuple.org/xtincident/view/bugs/28747) _Unable to build masterref databases from xTuple repositories on 4_11_x branch._
- Fixed issue #[28748](http://www.xtuple.org/xtincident/view/bugs/28748) _Able to select 'Credit by' as 'None' when 'Dispostion' is selected as 'Credit' in 'Return Authorization' screen_
- Fixed issue #[28753](http://www.xtuple.org/xtincident/view/bugs/28753) _Search for Vendor" screen has duplicate column "Vendor Type_
- Fixed issue #[28766](http://www.xtuple.org/xtincident/view/bugs/28766) _Pricing schedule site selector is confusing_
- Fixed issue #[28769](http://www.xtuple.org/xtincident/view/bugs/28769) _You can add a job costed item as a component on a WO_
- Fixed issue #[28780](http://www.xtuple.org/xtincident/view/bugs/28780) _CI failure for 410RC due to workflow issues_
- Fixed issue #[28807](http://www.xtuple.org/xtincident/view/bugs/28807) _roundlocale handles rounding non-fractional quantities incorrectly_
- Fixed issue #[28812](http://www.xtuple.org/xtincident/view/bugs/28812) _Workflow Activities menu item grays out after it has been clicked_
- Fixed issue #[28840](http://www.xtuple.org/xtincident/view/bugs/28840) _External column on COA displaying incorrect value_
- Fixed issue #[28861](http://www.xtuple.org/xtincident/view/bugs/28861) _Invalid error message is displayed when saving RA with Credit/Ship as '[no default]' and Credit By as '[no default]'._
- Fixed issue #[28877](http://www.xtuple.org/xtincident/view/bugs/28877) _Item Source screen shows phantom row under prices when editing item source without any itemsrcp rows_
- Fixed issue #[28889](http://www.xtuple.org/xtincident/view/bugs/28889) _Display class windows with search bar only assign "Return" key shortcut and not "Enter"_
- Fixed issue #[28906](http://www.xtuple.org/xtincident/view/bugs/28906) _‘One or more items cant be issued due to insufficient inventory’ dialog is displayed on issuing materials with enough QoH_
- Fixed issue #[28907](http://www.xtuple.org/xtincident/view/bugs/28907) _Able to issue materials even though QOH of the regular type item is zero._
- Fixed issue #[28919](http://www.xtuple.org/xtincident/view/bugs/28919) _XCheckBox remembered non-forgetful state populates after initial window load, causing duplicate work_
- Fixed issue #[28932](http://www.xtuple.org/xtincident/view/bugs/28932) _New foreign key constraint on bankrecitem causes error on new Bank Reconciliations_
- Fixed issue #[28934](http://www.xtuple.org/xtincident/view/bugs/28934) _'Select' button is in enable mode even though 'Customer#' is not provided in 'Invoices' screen._
- Fixed issue #[28963](http://www.xtuple.org/xtincident/view/bugs/28963) _BOM Item specific costs do not impact cost of MFG item for user defined costing element_
- Fixed issue #[28966](http://www.xtuple.org/xtincident/view/bugs/28966) _Some mobile client "Setup" lists are not translated_
- Fixed issue #[28969](http://www.xtuple.org/xtincident/view/bugs/28969) _All items inventory information is displayed in 'Inventory Availability' screen when opened from 'Item Sites' screen for an item_
- Fixed issue #[28972](http://www.xtuple.org/xtincident/view/bugs/28972) _“Uses of the Contact” contact tab shouldn't be available while creating a new contact_
- Fixed issue #[28976](http://www.xtuple.org/xtincident/view/bugs/28976) _'Post button' should be in disable mode when 'Quick Relocate Lot' screen is opened_
- Fixed issue #[28994](http://www.xtuple.org/xtincident/view/bugs/28994) _Can delete reference item used on invoice_
- Fixed issue #[29007](http://www.xtuple.org/xtincident/view/bugs/29007) _Value of A/P Workbench drop down selector does not reset_
- Fixed issue #[29012](http://www.xtuple.org/xtincident/view/bugs/29012) _Buttons(Edit/View/Print/Copy) are enabled after removing non existing BOM from 'Search for:' field   in Bills of Materials_
- Fixed issue #[29025](http://www.xtuple.org/xtincident/view/bugs/29025) _All date filters are displayed by default with current date when 'Projects' screen is opened._
- Fixed issue #[29027](http://www.xtuple.org/xtincident/view/bugs/29027) _'Item group' screen is displayed behind 'List Item Groups' screen when opened from 'Inventory Buffer Status by Item Group scree_
- Fixed issue #[29044](http://www.xtuple.org/xtincident/view/bugs/29044) _All sites item sources are displayed in print report of 'Item Sources' when one site filter is selected_
- Fixed issue #[29053](http://www.xtuple.org/xtincident/view/bugs/29053) _View Supply Order shows no data in view mode_
- Fixed issue #[29074](http://www.xtuple.org/xtincident/view/bugs/29074) _Purchase order description wrong_
- Fixed issue #[29110](http://www.xtuple.org/xtincident/view/bugs/29110) _Disallow changing item site control method to "None" when qty exists_
- Fixed issue #[29119](http://www.xtuple.org/xtincident/view/bugs/29119) _Inactive item sites showing in relocate transaction list_
- Fixed issue #[29129](http://www.xtuple.org/xtincident/view/bugs/29129) _Nuisance Error on BOM Where Used_
- Fixed issue #[29130](http://www.xtuple.org/xtincident/view/bugs/29130) _Impossible to edit UOM vendor conversion on poitem line edit_
- Fixed issue #[29185](http://www.xtuple.org/xtincident/view/bugs/29185) _Open Sales Order window errors when Site Filter is applied_
- Fixed issue #[29216](http://www.xtuple.org/xtincident/view/bugs/29216) _Bug in copyproject PL/pgSQL function causes failure on copying project_
- Fixed issue #[29257](http://www.xtuple.org/xtincident/view/bugs/29257) _CPAL in private-extensions_
- Fixed issue #[29274](http://www.xtuple.org/xtincident/view/bugs/29274) _Purchase Order Item tax type setting not saved on new_
- Fixed issue #[29315](http://www.xtuple.org/xtincident/view/bugs/29315) _Standard Journal Total field Size_
- Fixed issue #[29359](http://www.xtuple.org/xtincident/view/bugs/29359) _itemsite api view needs to default order group to 1_
- Fixed issue #[29384](http://www.xtuple.org/xtincident/view/bugs/29384) _Application is crashed on clicking cancel button in 'Sales Order' screen_
- Fixed issue #[29391](http://www.xtuple.org/xtincident/view/bugs/29391) _divide by 0 error in Slow Moving Inventory By Classcode metasql for 0 qoh_
- Fixed issue #[29510](http://www.xtuple.org/xtincident/view/bugs/29510) _Editing Discount on Credit Memo Apply changes apply amount_
- Fixed issue #[29591](http://www.xtuple.org/xtincident/view/bugs/29591) _The `usr` view is slow on databases with lots of `usrpref` records_
- Fixed issue #[29592](http://www.xtuple.org/xtincident/view/bugs/29592) _Missing Item Label Report_
- Fixed issue #[29594](http://www.xtuple.org/xtincident/view/bugs/29594) _Post Operation - Operation Combobox does not display correctly if description is missing_
- Fixed issue #[29608](http://www.xtuple.org/xtincident/view/bugs/29608) _Tax Assignment screen: checkboxes enabled in View mode_
- Fixed issue #[29788](http://www.xtuple.org/xtincident/view/bugs/29788) _Distributing Inventory Extremely slow_
- Fixed issue #[29796](http://www.xtuple.org/xtincident/view/bugs/29796) _Multiple Qty to Reserve popups on manually reserving multiple Lot/Location inventory_
- Fixed issue #[29827](http://www.xtuple.org/xtincident/view/bugs/29827) _Demo Database: Item Characteristics are not copied to Sales Order Line Items when the Line Item is created_
- Fixed issue #[29885](http://www.xtuple.org/xtincident/view/bugs/29885) _Aging report wrong_
- Fixed issue #[29907](http://www.xtuple.org/xtincident/view/bugs/29907) _Wrong Check Number Printed and Updated_
- Fixed issue #[29911](http://www.xtuple.org/xtincident/view/bugs/29911) _commercialcore-install.sql is empty in packages_
- Fixed issue #[29938](http://www.xtuple.org/xtincident/view/bugs/29938) _Display won't open on Windows if a script adds a large amount of options to the parameter widget_
- Fixed issue #[29979](http://www.xtuple.org/xtincident/view/bugs/29979) _Shop Floor Workbench screen title should be reverted_
- Fixed issue #[30022](http://www.xtuple.org/xtincident/view/bugs/30022) _Poor Item Source visibility is causing duplicate sources_

## Deployment Notes

If you are running version 4.4.0 or later of xTuple ERP, you will only need to apply
one updater package to upgrade to the latest release. The new updater packages are
designed to bring you all the way up to their version, no matter
what version (>= 4.4.0!) that you're on.

If you are upgrading from PostBooks to any of the other editions, you simply need to run the installation package for that edition. This will upgrade both your xTuple ERP version _and_ edition. There is a special package for upgrading the Manufacturing Edition to Enterprise Edition.

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
