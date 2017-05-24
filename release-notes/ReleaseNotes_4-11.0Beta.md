# xTuple Release Notes

## Version 4.10.1 - May, 2017

These are the release notes for the 4.11.0Beta xTuple ERP release.
Thanks to all who contributed to make this release possible. See below for more information about
[deploying this release](#deployment-notes).

### Summary

A large number of features and bug fixes have been added to the
application since the 4.10.0 release. Our focus has been on improving
the desktop client and preparing for upcoming xTupleCommerce features.

Of particular interest are the following:

- Completed support for Landed Cost
- Continued improvements in desktop client support for the Quality extension
- Simplified reversal of A/R application
- Continued performance improvements
- Rudimentary (undocumented) widget scripting (issue #[28225](http://www.xtuple.org/xtincident/view/bugs/28225) WIP)

**Note:** This release is compatible with PostgreSQL 9.3 through 9.6.
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
