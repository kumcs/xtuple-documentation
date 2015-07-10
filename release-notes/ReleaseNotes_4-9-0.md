# xTuple Release Notes
## Version 4.9.0 * July 13, 2015

These are the release notes for the 4.9.0 xTuple ERP release.  Thanks
to all who contributed to make this release possible.  For more
information about [deploying this release](#deployment-notes),
please see below.

**Note:** You will need the PL/v8 extension to PostgreSQL to upgrade
and use this release.  See our
[github wiki](https://github.com/xtuple/xtuple/wiki/Installing-PLv8) for
more information.

### Features and bug fixes

The following features and bug fixes have been added to the application
since the 4.9.0RC release (see below).

The primary theme of this release is improvement to Mobile Inventory
and to general desktop client quality. Note that a number of very
old issues have been marked as Fixed or Implemented. Much of this
is the result of reviewing the open bug and feature lists for work
that had already been done while addressing other issues.

#### Mobile Web Application

- Fixed
  issue #[24980](http://www.xtuple.org/xtincident/view/bugs/24980)
  _*After shipping an order it sits on the 'Ship Shipment' screen_
- Implemented
  issue #[25438](http://www.xtuple.org/xtincident/view/bugs/25438)
  _Add a checkbox in Setup to enable workflow trigger functionality_
- Fixed
  issue #[25924](http://www.xtuple.org/xtincident/view/bugs/25924)
  _Print on Save fails_
- Fixed
  issue #[26001](http://www.xtuple.org/xtincident/view/bugs/26001)
  _Don't create workflow in mobile if TriggerWorkflow enabled_
- Fixed
  issue #[26014](http://www.xtuple.org/xtincident/view/bugs/26014)
  _Transaction list item's status reads "O" instead of "F"_
- Implemented
  issue #[26015](http://www.xtuple.org/xtincident/view/bugs/26015)
  _Ship Order tap from Activity List goes to Issue to Shipping list - should go to Ship Order workspace_
- Fixed
  issue #[26016](http://www.xtuple.org/xtincident/view/bugs/26016)
  _Printing (route) error on print: "isError: true"_
- Implemented
  issue #[26017](http://www.xtuple.org/xtincident/view/bugs/26017)
  _First panel often gets in the way of UI flow. Look into "auto collapse" as a patch for this bad mobile UI design_
- Fixed
  issue #[26018](http://www.xtuple.org/xtincident/view/bugs/26018)
  _Print to printer failing on malformed rptrender print params_
- Implemented
  issue #[26025](http://www.xtuple.org/xtincident/view/bugs/26025)
  _Disable multi select on small mobile device lists_
- Fixed
  issue #[26027](http://www.xtuple.org/xtincident/view/bugs/26027)
  _Transaction list captureBarcode bugs_
- Fixed
  issue #[26033](http://www.xtuple.org/xtincident/view/bugs/26033)
  _Post Receipt does not close workflow item_
- Fixed
  issue #[26100](http://www.xtuple.org/xtincident/view/bugs/26100)
  _Enter Receipt - scanning/receiving does not update status from "In Truck" to "Fulfilled"_

#### Desktop Application

- Fixed
  issue #[13368](http://www.xtuple.org/xtincident/view/bugs/13368)
  _*Inconsistent behavior is observed for RA with disposition set to 'Service'_
- Fixed
  issue #[15457](http://www.xtuple.org/xtincident/view/bugs/15457)
  _*Special characters import-export_
- No Change Required
  issue #[17206](http://www.xtuple.org/xtincident/view/bugs/17206)
  _installer tries to run postgresql-9.1.2-1-linux-x64.run on 64-bit linux machines but can't_
- No Change Required
  issue #[17568](http://www.xtuple.org/xtincident/view/bugs/17568)
  _*xTuple Installer: It is not possible to re-install PostgreSQL component using xTuple installer_
- Implemented
  issue #[17857](http://www.xtuple.org/xtincident/view/bugs/17857)
  _Installer version of issue 17842 - force country/state agreement_
- No Change Required
  issue #[19124](http://www.xtuple.org/xtincident/view/bugs/19124)
  _*Observation: Selecting to uninstall the xTuple components using xTuple uninstaller doesn't uninstall the PostgreSQL_
- Fixed
  issue #[24727](http://www.xtuple.org/xtincident/view/bugs/24727)
  _audit sources for blind inserts_
- Fixed
  issue #[24866](http://www.xtuple.org/xtincident/view/bugs/24866)
  _Lot/Serial Document Links not visible on linked Document_
- Fixed
  issue #[25825](http://www.xtuple.org/xtincident/view/bugs/25825)
  _Distribution:It is not possible to delete a recurring enabled TO-DO_
- Fixed
  issue #[25889](http://www.xtuple.org/xtincident/view/bugs/25889)
  _*Insufficient Privileges dialog is displayed on selecting to click on 'Wo Schedule By Class Code'_
- Fixed
  issue #[25903](http://www.xtuple.org/xtincident/view/bugs/25903)
  _Focus on Misc. Distribution screen changes, not ideal for multiple order entries_
- Fixed
  issue #[25905](http://www.xtuple.org/xtincident/view/bugs/25905)
  _Clicking on the history tab and item availability tab in the Item Workbench queries all history, all items_
- Duplicate
  issue #[25926](http://www.xtuple.org/xtincident/view/bugs/25926)
  _*Sales History costs off by a factor of unit convesrsion_
- Fixed
  issue #[25933](http://www.xtuple.org/xtincident/view/bugs/25933)
  _NEW.cohead_shiptoname Is set to default ship to when using Free Form_
- Fixed
  issue #[25944](http://www.xtuple.org/xtincident/view/bugs/25944)
  _AR out of balance when the exchange rate is changed and then the CD is applied_
- Fixed
  issue #[25952](http://www.xtuple.org/xtincident/view/bugs/25952)
  _*Sales Order Item Focus in 4.9.0RC_
- Implemented
  issue #[25954](http://www.xtuple.org/xtincident/view/bugs/25954)
  _4.9.0 install: Installing PLv8 returns ./install_plv8.sh: line 37: PGVER: command not found_
- Fixed
  issue #[25962](http://www.xtuple.org/xtincident/view/bugs/25962)
  _Post Operations not Working for Work Orders in Edit Mode_
- Fixed
  issue #[25970](http://www.xtuple.org/xtincident/view/bugs/25970)
  _PO line item freight miscalculated causing PO Liability to be unbalanced_
- Fixed
  issue #[26021](http://www.xtuple.org/xtincident/view/bugs/26021)
  _*Inserting image in header and saving to database generates an error._
- Fixed
  issue #[26028](http://www.xtuple.org/xtincident/view/bugs/26028)
  _*DB log error is displayed on selecting to query 'Partially Shipped Orders' screen irrelevantly_
- Fixed
  issue #[26064](http://www.xtuple.org/xtincident/view/bugs/26064)
  _*image upload fails on macs_
- Fixed
  issue #[26091](http://www.xtuple.org/xtincident/view/bugs/26091)
  _Selecting a Reg Mgmt DocType with a Documents Tab Attach crashes the Qt Client_
- Fixed
  issue #[26132](http://www.xtuple.org/xtincident/view/bugs/26132)
  _comment-source associations are broken_
- Duplicate
  issue #[4121](http://www.xtuple.org/xtincident/view/bugs/4121)
  _Post PO_
- Implemented
  issue #[4126](http://www.xtuple.org/xtincident/view/bugs/4126)
  _Purchase Requisition for non-inventory items (and unscheduled inventory items)_
- Duplicate
  issue #[4127](http://www.xtuple.org/xtincident/view/bugs/4127)
  _Purchase Requisition for non-inventory items (and unscheduled inventory items)_
- Implemented
  issue #[4128](http://www.xtuple.org/xtincident/view/bugs/4128)
  _Prior Period Adjustments_
- No Change Required
  issue #[4131](http://www.xtuple.org/xtincident/view/bugs/4131)
  _Reject Codes_
- Duplicate
  issue #[4133](http://www.xtuple.org/xtincident/view/bugs/4133)
  _Copy PO_
- Implemented
  issue #[4134](http://www.xtuple.org/xtincident/view/bugs/4134)
  _Print PO_
- Implemented
  issue #[4137](http://www.xtuple.org/xtincident/view/bugs/4137)
  _Terms Code_
- Implemented
  issue #[4138](http://www.xtuple.org/xtincident/view/bugs/4138)
  _Vendor Search_
- Implemented
  issue #[4143](http://www.xtuple.org/xtincident/view/bugs/4143)
  _Vendor Maintenance_
- Implemented
  issue #[4144](http://www.xtuple.org/xtincident/view/bugs/4144)
  _Report_
- Implemented
  issue #[4145](http://www.xtuple.org/xtincident/view/bugs/4145)
  _Adjustment Types_
- Implemented
  issue #[4149](http://www.xtuple.org/xtincident/view/bugs/4149)
  _Unposted Transactions_
- Implemented
  issue #[4150](http://www.xtuple.org/xtincident/view/bugs/4150)
  _Trial Balance_
- Implemented
  issue #[4152](http://www.xtuple.org/xtincident/view/bugs/4152)
  _Out of Balance Posting_
- No Change Required
  issue #[4155](http://www.xtuple.org/xtincident/view/bugs/4155)
  _Sub-system posting_
- No Change Required
  issue #[4158](http://www.xtuple.org/xtincident/view/bugs/4158)
  _Journal Entries_
- No Change Required
  issue #[4159](http://www.xtuple.org/xtincident/view/bugs/4159)
  _Journal Entries_
- Implemented
  issue #[4162](http://www.xtuple.org/xtincident/view/bugs/4162)
  _RMA Processing_
- Duplicate
  issue #[4166](http://www.xtuple.org/xtincident/view/bugs/4166)
  _Customer Deposit_
- No Change Required
  issue #[4167](http://www.xtuple.org/xtincident/view/bugs/4167)
  _Cash Receipts_
- Implemented
  issue #[4168](http://www.xtuple.org/xtincident/view/bugs/4168)
  _Cash Receipts_
- Implemented
  issue #[4169](http://www.xtuple.org/xtincident/view/bugs/4169)
  _Cash Receipts_
- Implemented
  issue #[4170](http://www.xtuple.org/xtincident/view/bugs/4170)
  _Invoice Entry_
- Implemented
  issue #[4171](http://www.xtuple.org/xtincident/view/bugs/4171)
  _Invoice Creation_
- Implemented
  issue #[4176](http://www.xtuple.org/xtincident/view/bugs/4176)
  _Manual/Miscellaneous Payment Processing_
- Implemented
  issue #[4178](http://www.xtuple.org/xtincident/view/bugs/4178)
  _Payment Processing_
- Implemented
  issue #[4183](http://www.xtuple.org/xtincident/view/bugs/4183)
  _Post Vouchers_
- Duplicate
  issue #[4195](http://www.xtuple.org/xtincident/view/bugs/4195)
  _Edit posted POs_
- Duplicate
  issue #[4196](http://www.xtuple.org/xtincident/view/bugs/4196)
  _Edit posted POs_
- Implemented
  issue #[4199](http://www.xtuple.org/xtincident/view/bugs/4199)
  _Vendor Maintenance_
- Implemented
  issue #[4201](http://www.xtuple.org/xtincident/view/bugs/4201)
  _Vendor Maintenance_

## Version 4.9.0RC * June 5, 2015

These are the release notes for the 4.9.0 Release Candidate.
Thanks to all who contributed to make this release possible.
For more information about [deploying this release](#deployment-notes), please see below.

**Note:** You will need the PL/v8 extension to PostgreSQL to upgrade and use
this release.  See our
[github wiki](https://github.com/xtuple/xtuple/wiki/Installing-PLv8)
for more information.

### Features and bug fixes

The following features and bug fixes have been added to the application since the 4.9.0Beta release (see below).

- Fixed
  issue #[19160](http://www.xtuple.org/xtincident/view/bugs/19160)
  _*OnHand qty changing if we modified a transaction dated prior to the freeze_
- Fixed
  issue #[21311](http://www.xtuple.org/xtincident/view/bugs/21311)
  _Activity Report is missing Order information_
- Implemented
  issue #[23905](http://www.xtuple.org/xtincident/view/bugs/23905)
  _*prompt user on startup if no current fiscal or accounting period_
- Implemented
  issue #[24508](http://www.xtuple.org/xtincident/view/bugs/24508)
  _*Missing Info in Reference Guide_
- Fixed
  issue #[24663](http://www.xtuple.org/xtincident/view/bugs/24663)
  _When creating a BOM system allows Job costed Parts to be added to BOM_
- Implemented
  issue #[24892](http://www.xtuple.org/xtincident/view/bugs/24892)
  _*multiple item sites available with Advance item search_
- Implemented
  issue #[25151](http://www.xtuple.org/xtincident/view/bugs/25151)
  _In Quickstart Database Default Company and Business Unit to Off (unchecked)_
- Fixed
  issue #[25392](http://www.xtuple.org/xtincident/view/bugs/25392)
  _Disable ability to manually update trial balance_
- Implemented
  issue #[25433](http://www.xtuple.org/xtincident/view/bugs/25433)
  _Add readme file to client zips_
- Fixed
  issue #[25477](http://www.xtuple.org/xtincident/view/bugs/25477)
  _Catch missing curl.exe error for credit card processing_
- Fixed
  issue #[25511](http://www.xtuple.org/xtincident/view/bugs/25511)
  _*Text overlap observed in 'Sales setup' screen_
- Fixed
  issue #[25553](http://www.xtuple.org/xtincident/view/bugs/25553)
  _Incredible Shrinking Windows_
- Fixed
  issue #[25665](http://www.xtuple.org/xtincident/view/bugs/25665)
  _*Work order material return_
- Fixed
  issue #[25685](http://www.xtuple.org/xtincident/view/bugs/25685)
  _*Sales history report errors_
- Fixed
  issue #[25701](http://www.xtuple.org/xtincident/view/bugs/25701)
  _Bank account screen refers to checks, not payments_
- Fixed
  issue #[25711](http://www.xtuple.org/xtincident/view/bugs/25711)
  _*api.quote references wrong sequence for quote number_
- Fixed
  issue #[25719](http://www.xtuple.org/xtincident/view/bugs/25719)
  _*Unable to edit the customer data from Customer Workbench screen_
- Fixed
  issue #[25725](http://www.xtuple.org/xtincident/view/bugs/25725)
  _*Sales Reservations are not Released When Backorders are Disallowed_
- Fixed
  issue #[25727](http://www.xtuple.org/xtincident/view/bugs/25727)
  _Sales rep not cleared when ship to cleared_
- Fixed
  issue #[25728](http://www.xtuple.org/xtincident/view/bugs/25728)
  _Able to delete UOM conversion with history_
- Fixed
  issue #[25729](http://www.xtuple.org/xtincident/view/bugs/25729)
  _Cannot make a UOM conversion inactive for future orders once there is history_
- Implemented
  issue #[25741](http://www.xtuple.org/xtincident/view/bugs/25741)
  _allow extensions to add their own characteristic associations_
- Fixed
  issue #[25765](http://www.xtuple.org/xtincident/view/bugs/25765)
  _*Payment can be applied to closed SOs_
- Fixed
  issue #[25769](http://www.xtuple.org/xtincident/view/bugs/25769)
  _*User is allowed to edit/delete the item source price in view mode of an 'Item source'_
- Fixed
  issue #[25777](http://www.xtuple.org/xtincident/view/bugs/25777)
  _*Unable to convert quote into sales order_
- Fixed
  issue #[25827](http://www.xtuple.org/xtincident/view/bugs/25827)
  _Routing throughput calculations are incorrect for alternate production units_
- Fixed
  issue #[25834](http://www.xtuple.org/xtincident/view/bugs/25834)
  _*Coping an Item allows a user to add an inactive item to a BOM_
- Fixed
  issue #[25836](http://www.xtuple.org/xtincident/view/bugs/25836)
  _Bank Reconciliation uses insufficient decimal places for alternate currencies_
- Fixed
  issue #[25838](http://www.xtuple.org/xtincident/view/bugs/25838)
  _New unassigned account should default to liability type_
- Implemented
  issue #[25850](http://www.xtuple.org/xtincident/view/bugs/25850)
  _Add Vendor Number column to Item Sources List screen_
- Implemented
  issue #[25851](http://www.xtuple.org/xtincident/view/bugs/25851)
  _Add description to Role and User screens_
- Fixed
  issue #[25871](http://www.xtuple.org/xtincident/view/bugs/25871)
  _*City and Postal Code do not appear on reports if no State selected_
- Fixed
  issue #[25897](http://www.xtuple.org/xtincident/view/bugs/25897)
  _Scheduled date does not save in closed sales orders_
- Fixed
  issue #[22242](http://www.xtuple.org/xtincident/view/bugs/22242)
  _Add support to print Work Order travellers_
- Fixed
  issue #[25852](http://www.xtuple.org/xtincident/view/bugs/25852)
  _Changes to workflow_inheritsource function has broken Quality extension_

## Version 4.9.0Beta * May 5, 2015

These are the release notes for the 4.9.0 Beta Release.

### Features and bug fixes

The following features and bug fixes have been added to the application since the 4.8.1 release.
Additional detail for each item listed below may be found on our [community website](http://www.xtuple.org).

#### Mobile Web Application

xtuple.org issues:

- Implemented
  issue #[21664](http://www.xtuple.org/xtincident/view/bugs/21664)
  _Implement Cash Receipt_
- Implemented
  issue #[22244](http://www.xtuple.org/xtincident/view/bugs/22244)
  _Refactor many-to-many document associations_
- Fixed
  issue #[23034](http://www.xtuple.org/xtincident/view/bugs/23034)
  _Mobile creates duplicate indexes on uuid column_
- Implemented
  issue #[23298](http://www.xtuple.org/xtincident/view/bugs/23298)
  _Improve toolbar icons on phone_
- Fixed
  issue #[24534](http://www.xtuple.org/xtincident/view/bugs/24534)
  _xtattend function taclockin_
- Fixed
  issue #[24535](http://www.xtuple.org/xtincident/view/bugs/24535)
  _xtattend function taclockout_
- Fixed
  issue #[25298](http://www.xtuple.org/xtincident/view/bugs/25298)
  _Metric table sequence is incorrect on a fresh 4.9 build_
- Fixed
  issue #[25680](http://www.xtuple.org/xtincident/view/bugs/25680)
  _*Unable to load the mobile application on to a database_

GitHub issues:

- Fixed
  issue [#2264](https://github.com/xtuple/xtuple/issues/2264)
  _Transaction Containers/Lists and Search should be draggable bug_
- Implemented
  issue [#2235](https://github.com/xtuple/xtuple/issues/2235)
  _Remove unnecessary attributes in Transaction Lists_
- Implemented
  issue [#2234](https://github.com/xtuple/xtuple/issues/2234)
  _Transaction Lists should dynamically reorder_
- Implemented
  issue [#2233](https://github.com/xtuple/xtuple/issues/2233)
  _Add scanned variables concept to transaction lists_
- Implemented
  issue [#2232](https://github.com/xtuple/xtuple/issues/2232)
  _Make the (key) icon bigger on the Activity List_
- Fixed
  issue [#2226](https://github.com/xtuple/xtuple/issues/2226)
  _Issue/Return Material list action 'Return Line' does not work_
- Fixed
  issue [#2215](https://github.com/xtuple/xtuple/issues/2215)
  _Barcode scans should report errors_
- Fixed
  issue [#2214](https://github.com/xtuple/xtuple/issues/2214)
  _Color code Issue to Shipping Item List lines based on Stock Status_
- Fixed
  issue [#2213](https://github.com/xtuple/xtuple/issues/2213)
  _Issue to Shipping Item List should show best FIFO location to go to to pick an item_
- Implemented
  issue [#2208](https://github.com/xtuple/xtuple/issues/2208)
  _Scanning a lot barcode distributes qty 1 to lot as well_
- Fixed
  issue [#2207](https://github.com/xtuple/xtuple/issues/2207)
  _Activity list should auto refresh, or update/refresh as activity status changes bug_
- Implemented
  issue [#2205](https://github.com/xtuple/xtuple/issues/2205)
  _Distribution detail should be sorted by FIFO_
- Implemented
  issue [#2204](https://github.com/xtuple/xtuple/issues/2204)
  _Add QOH to Issue to Shipping (line item list + workspace)_
- Implemented
  issue [#2201](https://github.com/xtuple/xtuple/issues/2201)
  _Rename 'Trace' to 'Lot'_
- Fixed
  issue [#2200](https://github.com/xtuple/xtuple/issues/2200)
  _Printing to Browser failing after adding a printer bug_
- Fixed
  issue [#2189](https://github.com/xtuple/xtuple/issues/2189)
  _Issue Material list needs header and correction of item text overflow_
- Fixed
  issue [#2187](https://github.com/xtuple/xtuple/issues/2187)
  _Switch Mobile Report printing to use the OpenRPT route_
- Implemented
  issue [#2185](https://github.com/xtuple/xtuple/issues/2185)
  _Workflow Activites - Reassign User should allow text searching_
- Fixed
  issue [#2181](https://github.com/xtuple/xtuple/issues/2181)
  _Return Material Return button disabled_
- Fixed
  issue [#2025](https://github.com/xtuple/xtuple/issues/2025)
  _REST Issue To Shipping (Serialized) never responds_
- Fixed
  issue [#1982](https://github.com/xtuple/xtuple/issues/1982)
  _support UPC-A barcode formatting_


#### Desktop Application

- Implemented
  issue #[4876](http://www.xtuple.org/xtincident/view/bugs/4876)
  _Manual payment / manual check / EFT payment entry_
- Implemented
  issue #[6664](http://www.xtuple.org/xtincident/view/bugs/6664)
  _AR Aging Grid/Report do not match._
- Implemented
  issue #[11473](http://www.xtuple.org/xtincident/view/bugs/11473)
  _enhanced checking account "debit" transaction processing_
- Implemented
  issue #[11559](http://www.xtuple.org/xtincident/view/bugs/11559)
  _Need a method for manual purchase order requests_
- Implemented
  issue #[12336](http://www.xtuple.org/xtincident/view/bugs/12336)
  _SO Hold Permission_
- Fixed
  issue #[16680](http://www.xtuple.org/xtincident/view/bugs/16680)
  _*'Non-Working Day Entered' dialog is displayed irrelevantly on selecting to view a Work order_
- Implemented
  issue #[16970](http://www.xtuple.org/xtincident/view/bugs/16970)
  _*a/p needs manual checks_
- Fixed
  issue #[17257](http://www.xtuple.org/xtincident/view/bugs/17257)
  _*Incorrect behavior is observed on posting an invoice for a foreign customer_
- Fixed
  issue #[17494](http://www.xtuple.org/xtincident/view/bugs/17494)
  _*Observation: Selecting 'Apply to Balance' in the Cash Receipt screen generates DB log error_
- Fixed
  issue #[18047](http://www.xtuple.org/xtincident/view/bugs/18047)
  _*error when re-print invoices_
- Fixed
  issue #[18979](http://www.xtuple.org/xtincident/view/bugs/18979)
  _It is not possible to change the purchase order quantity from 'Quick Entry' tab_
- Fixed
  issue #[20364](http://www.xtuple.org/xtincident/view/bugs/20364)
  _*Uninformative dialog is displayed on selecting 'Issue Line' button for a Job Costing type Sales order line item_
- Fixed
  issue #[20382](http://www.xtuple.org/xtincident/view/bugs/20382)
  _*'Non-Working Date Entered' dialog is displayed multiple times_
- Reopened
  issue #[20480](http://www.xtuple.org/xtincident/view/bugs/20480)
  _*Add Qty and Weight Summary Totals to Purchase Order footer_
- Duplicate
  issue #[20502](http://www.xtuple.org/xtincident/view/bugs/20502)
  _Bank Rec History screen: Date Range drop-down is too small_
- Fixed
  issue #[20770](http://www.xtuple.org/xtincident/view/bugs/20770)
  _Different Miscellaneous Distribution defaults when adding Vendors_
- Fixed
  issue #[20809](http://www.xtuple.org/xtincident/view/bugs/20809)
  _*Freight Amount calculated for a sales order is not carried to its shipment_
- Fixed
  issue #[20857](http://www.xtuple.org/xtincident/view/bugs/20857)
  _Quick Entry for PO_
- Fixed
  issue #[20982](http://www.xtuple.org/xtincident/view/bugs/20982)
  _Function getunassignedaccntid() looks for non-existent metric and transaction fails_
- Implemented
  issue #[21596](http://www.xtuple.org/xtincident/view/bugs/21596)
  _*post documents in single step_
- Implemented
  issue #[21642](http://www.xtuple.org/xtincident/view/bugs/21642)
  _Sales Type Needs to be Accessible in Sales Reports/Screens_
- Fixed
  issue #[21921](http://www.xtuple.org/xtincident/view/bugs/21921)
  _*Tax report Issues_
- Fixed
  issue #[21922](http://www.xtuple.org/xtincident/view/bugs/21922)
  _*AR Open Item Report - applications display issue_
- Fixed
  issue #[21929](http://www.xtuple.org/xtincident/view/bugs/21929)
  _*Race Condition in SoNumber_
- Fixed
  issue #[22597](http://www.xtuple.org/xtincident/view/bugs/22597)
  _Distribution edition should include standard commission reports_
- Fixed
  issue #[22635](http://www.xtuple.org/xtincident/view/bugs/22635)
  _Issue with quote number generation when quotes are set to use sales order number_
- Implemented
  issue #[22800](http://www.xtuple.org/xtincident/view/bugs/22800)
  _Add ShipCharge and preferredSite default setting_
- Fixed
  issue #[22886](http://www.xtuple.org/xtincident/view/bugs/22886)
  _Contact Merge Not Working in 4.3 (Dogfood)_
- Fixed
  issue #[22909](http://www.xtuple.org/xtincident/view/bugs/22909)
  _*Selecting to convert quote of a purchase type item to invoice generates an irrelevant system message_
- Fixed
  issue #[23017](http://www.xtuple.org/xtincident/view/bugs/23017)
  _can't post TE sheet - only happens with one sheet_
- Fixed
  issue #[23055](http://www.xtuple.org/xtincident/view/bugs/23055)
  _*PostgreSQL 9.3: It is not possible to delete a recurring enabled TO-DO_
- Fixed
  issue #[23220](http://www.xtuple.org/xtincident/view/bugs/23220)
  _*Can't delete Employee "Mfgadmin"_
- Implemented
  issue #[23478](http://www.xtuple.org/xtincident/view/bugs/23478)
  _develop new method for building .gz packages_
- Fixed
  issue #[23492](http://www.xtuple.org/xtincident/view/bugs/23492)
  _possible to select a voucher with distributions to a company different from the bank account company_
- Fixed
  issue #[23668](http://www.xtuple.org/xtincident/view/bugs/23668)
  _*VAT problems with misc invoice payable_
- Fixed
  issue #[23771](http://www.xtuple.org/xtincident/view/bugs/23771)
  _*Unable to Modify Customer #_
- Fixed
  issue #[23779](http://www.xtuple.org/xtincident/view/bugs/23779)
  _*customer addresses displayed next to phone fields_
- Fixed
  issue #[23885](http://www.xtuple.org/xtincident/view/bugs/23885)
  _Credit card on sales order - new error with UUID mismatch_
- Implemented
  issue #[23904](http://www.xtuple.org/xtincident/view/bugs/23904)
  _*wizard / rapid creation of fiscal period and accounting periods_
- Fixed
  issue #[24151](http://www.xtuple.org/xtincident/view/bugs/24151)
  _*PO Quick Entry Issues_
- Implemented
  issue #[24213](http://www.xtuple.org/xtincident/view/bugs/24213)
  _need a version number comparison/compatibility function_
- Implemented
  issue #[24240](http://www.xtuple.org/xtincident/view/bugs/24240)
  _Better capture of lot number in Transfer Orders_
- Fixed
  issue #[24327](http://www.xtuple.org/xtincident/view/bugs/24327)
  _*User is able to duplicate an item sources using 'Copy' option_
- Fixed
  issue #[24335](http://www.xtuple.org/xtincident/view/bugs/24335)
  _*Can no longer print forms from xTuple Qt client_
- Fixed
  issue #[24408](http://www.xtuple.org/xtincident/view/bugs/24408)
  _Change PO due date in quick entry_
- Implemented
  issue #[24443](http://www.xtuple.org/xtincident/view/bugs/24443)
  _*Item History report for perishable items_
- Fixed
  issue #[24495](http://www.xtuple.org/xtincident/view/bugs/24495)
  _*open purchase orders missing release date_
- Fixed
  issue #[24587](http://www.xtuple.org/xtincident/view/bugs/24587)
  _*'Margin' and 'Margin %' are incorrectly calculated for invoice in foreign currency_
- Fixed
  issue #[24589](http://www.xtuple.org/xtincident/view/bugs/24589)
  _*Next Sales order number is not updated on selecting to convert a quote with sales order numbering_
- Fixed
  issue #[24608](http://www.xtuple.org/xtincident/view/bugs/24608)
  _Credit card charge approved but not completed_
- Fixed
  issue #[24616](http://www.xtuple.org/xtincident/view/bugs/24616)
  _*Upgrade scripts fail if custom searchpath specified_
- Fixed
  issue #[24642](http://www.xtuple.org/xtincident/view/bugs/24642)
  _*Order# in sales order screen is incremented irrelevantly_
- Duplicate
  issue #[24688](http://www.xtuple.org/xtincident/view/bugs/24688)
  _*PO Quick order entry error_
- Fixed
  issue #[24717](http://www.xtuple.org/xtincident/view/bugs/24717)
  _*Problem with Assignment of Sales Order Numbers_
- Fixed
  issue #[24805](http://www.xtuple.org/xtincident/view/bugs/24805)
  _*Gapless numbering not working as expected_
- Implemented
  issue #[24853](http://www.xtuple.org/xtincident/view/bugs/24853)
  _Add Class Code to Sales History Search Filter_
- Fixed
  issue #[24907](http://www.xtuple.org/xtincident/view/bugs/24907)
  _Characteristics options list throws error when adding options_
- Fixed
  issue #[24910](http://www.xtuple.org/xtincident/view/bugs/24910)
  _Function postmisccount() does not check inputs for null values_
- Implemented
  issue #[24940](http://www.xtuple.org/xtincident/view/bugs/24940)
  _*Dissallow and alert when multiple users are on the same record_
- Fixed
  issue #[24953](http://www.xtuple.org/xtincident/view/bugs/24953)
  _*xtuple 470 issue: vendor search columns not displaying main address values_
- Fixed
  issue #[25003](http://www.xtuple.org/xtincident/view/bugs/25003)
  _*currency chooser obscures amount field_
- Fixed
  issue #[25013](http://www.xtuple.org/xtincident/view/bugs/25013)
  _*Site in Return Auth. Line Items_
- Fixed
  issue #[25035](http://www.xtuple.org/xtincident/view/bugs/25035)
  _*Cannot create WO through SO in Projects_
- Fixed
  issue #[25072](http://www.xtuple.org/xtincident/view/bugs/25072)
  _*Purchased xTuple licenses are consumed by non xTuple DB connections_
- Implemented
  issue #[25140](http://www.xtuple.org/xtincident/view/bugs/25140)
  _Copy quote from customer/prospect to a new quote_
- Fixed
  issue #[25165](http://www.xtuple.org/xtincident/view/bugs/25165)
  _*Irrelevant system message is displayed on selecting to create a new Purchase order when Order # Generation is set to 'Manual'_
- Implemented
  issue #[25187](http://www.xtuple.org/xtincident/view/bugs/25187)
  _Improve sales order item entry with manual refresh order lines option_
- Fixed
  issue #[25189](http://www.xtuple.org/xtincident/view/bugs/25189)
  _Remove admin@xtuple.com from database templates_
- Won't Fix
  issue #[25194](http://www.xtuple.org/xtincident/view/bugs/25194)
  _Financial report display column is blank for layout: YTD % of Group_
- Fixed
  issue #[25195](http://www.xtuple.org/xtincident/view/bugs/25195)
  _Close loophole in forward updating of accounts_
- Fixed
  issue #[25222](http://www.xtuple.org/xtincident/view/bugs/25222)
  _Characteristic value won't accept alphanumeric_
- Implemented
  issue #[25240](http://www.xtuple.org/xtincident/view/bugs/25240)
  _purchase type in Qt_
- Fixed
  issue #[25254](http://www.xtuple.org/xtincident/view/bugs/25254)
  _*The Credit Memo Doc # field in 4.8.0 will not accept a 10 digit number_
- Fixed
  issue #[25257](http://www.xtuple.org/xtincident/view/bugs/25257)
  _*Ship to address_
- Fixed
  issue #[25258](http://www.xtuple.org/xtincident/view/bugs/25258)
  _*Update All Prices window pops up and is creating issues for us_
- Fixed
  issue #[25259](http://www.xtuple.org/xtincident/view/bugs/25259)
  _*A good portion of our daily sales are displaying with a 100% profit margin_
- Fixed
  issue #[25289](http://www.xtuple.org/xtincident/view/bugs/25289)
  _*Need Active column in CRM Accounts screen_
- Fixed
  issue #[25291](http://www.xtuple.org/xtincident/view/bugs/25291)
  _Db error editing CRM account in dfood_
- Fixed
  issue #[25293](http://www.xtuple.org/xtincident/view/bugs/25293)
  _Voiding invoice does not reopen sales order_
- Fixed
  issue #[25311](http://www.xtuple.org/xtincident/view/bugs/25311)
  _Make a better client mismatch message_
- Won't Fix
  issue #[25313](http://www.xtuple.org/xtincident/view/bugs/25313)
  _Make the guiclient zip a self-extracting file_
- Fixed
  issue #[25315](http://www.xtuple.org/xtincident/view/bugs/25315)
  _*Relocating SO Reserved Inventoty (public.unreservelocationqty bug)_
- Won't Fix
  issue #[25319](http://www.xtuple.org/xtincident/view/bugs/25319)
  _*Can still add files to SOs as Documents while viewing SOs_
- Fixed
  issue #[25345](http://www.xtuple.org/xtincident/view/bugs/25345)
  _Characteristics should be listed in alphabetical order for ease of use_
- Fixed
  issue #[25350](http://www.xtuple.org/xtincident/view/bugs/25350)
  _Expired license message is wrong for PostBooks_
- Fixed
  issue #[25355](http://www.xtuple.org/xtincident/view/bugs/25355)
  _*Error upon posting misc. production for item using tooling_
- Fixed
  issue #[25358](http://www.xtuple.org/xtincident/view/bugs/25358)
  _GL Account widget will display the account as a null string if any defined GL account does not conform to the way the ledger accounts are configured_
- Fixed
  issue #[25366](http://www.xtuple.org/xtincident/view/bugs/25366)
  _dspWoSchedule.js in xtmfg is using column index to extract data, and the columns have changed_
- Fixed
  issue #[25377](http://www.xtuple.org/xtincident/view/bugs/25377)
  _Possible to delete account used in sales category_
- Fixed
  issue #[25384](http://www.xtuple.org/xtincident/view/bugs/25384)
  _Fix for division by zero problem in public views saleshistorymisc  and saleshistory_
- Fixed
  issue #[25411](http://www.xtuple.org/xtincident/view/bugs/25411)
  _Bookings screen will show a characteristic column but will not display the values for the rows_
- Fixed
  issue #[25414](http://www.xtuple.org/xtincident/view/bugs/25414)
  _ImplodeWO function creates db log error when labor exists_
- Fixed
  issue #[25424](http://www.xtuple.org/xtincident/view/bugs/25424)
  _*Auto Order Numbers_
- Fixed
  issue #[25436](http://www.xtuple.org/xtincident/view/bugs/25436)
  _*PostBooks: Qty Total is not displayed in print report of Earned Commissions screen_
- Implemented
  issue #[25451](http://www.xtuple.org/xtincident/view/bugs/25451)
  _Add Account Type filters to Account List_
- Fixed
  issue #[25455](http://www.xtuple.org/xtincident/view/bugs/25455)
  _Voucher Item: Close check box remains unehcked after total qty is vouchered_
- Fixed
  issue #[25458](http://www.xtuple.org/xtincident/view/bugs/25458)
  _Function releasePR not correctly setting poitem_order_type and poitem_order_id_
- Fixed
  issue #[25471](http://www.xtuple.org/xtincident/view/bugs/25471)
  _Unclear Inside Rep error message when creating Sales orders_
- Implemented
  issue #[25486](http://www.xtuple.org/xtincident/view/bugs/25486)
  _Add Chart of Account filters_
- Fixed
  issue #[25489](http://www.xtuple.org/xtincident/view/bugs/25489)
  _*Ship to Number does not keep Overriding Number_
- Fixed
  issue #[25493](http://www.xtuple.org/xtincident/view/bugs/25493)
  _*BOM Item selection offers items with no BOM_
- Fixed
  issue #[25500](http://www.xtuple.org/xtincident/view/bugs/25500)
  _New column in location is not supported by API_
- Implemented
  issue #[25509](http://www.xtuple.org/xtincident/view/bugs/25509)
  _Add Privilege description to Maintain Roles screen_
- Fixed
  issue #[25521](http://www.xtuple.org/xtincident/view/bugs/25521)
  _*Selecting to print the filtered 'Chart of Accounts' screen prints the all accounts list irrelevantly_
- Fixed
  issue #[25527](http://www.xtuple.org/xtincident/view/bugs/25527)
  _*Vendors in list twice_
- Duplicate
  issue #[25530](http://www.xtuple.org/xtincident/view/bugs/25530)
  _*auto-creation of fiscal years and accounting periods_
- Fixed
  issue #[25588](http://www.xtuple.org/xtincident/view/bugs/25588)
  _*REST API total & subtotal reflect cancelled items_
- Fixed
  issue #[25600](http://www.xtuple.org/xtincident/view/bugs/25600)
  _Omnibus: Transfer Order Bugs_
- Fixed
  issue #[25612](http://www.xtuple.org/xtincident/view/bugs/25612)
  _S/O Sale Type defaults to first alphabetical type_
- Fixed
  issue #[25614](http://www.xtuple.org/xtincident/view/bugs/25614)
  _*Site Error on Credit Memo_
- Fixed
  issue #[25630](http://www.xtuple.org/xtincident/view/bugs/25630)
  _*Unable to build the masterref database from xTuple repositories_
- Fixed
  issue #[25633](http://www.xtuple.org/xtincident/view/bugs/25633)
  _mac nightly build raises 'invalid connection option' error when logging in_
- Fixed
  issue #[25652](http://www.xtuple.org/xtincident/view/bugs/25652)
  _*Product Category dropdown in item record is too short_
- Fixed
  issue #[25653](http://www.xtuple.org/xtincident/view/bugs/25653)
  _*Planner Code dropdown menu too short_
- Fixed
  issue #[25654](http://www.xtuple.org/xtincident/view/bugs/25654)
  _*Cost Category dropdown menu too short_
- Fixed
  issue #[25662](http://www.xtuple.org/xtincident/view/bugs/25662)
  _*'NEW' button is not functional_
- Implemented
  issue #[25664](http://www.xtuple.org/xtincident/view/bugs/25664)
  _application should complain if it connects to an unsupported version of the database server_
- Implemented
  issue #[25676](http://www.xtuple.org/xtincident/view/bugs/25676)
  _encapsulate reporting in the applock api_
- Implemented
  issue #[25702](http://www.xtuple.org/xtincident/view/bugs/25702)
  _Add Location filtering to Distribute Stock screen_
- Fixed
  issue #[25703](http://www.xtuple.org/xtincident/view/bugs/25703)
  _api.employee needs a left join for currsymbol_
- Implemented
  issue #[25704](http://www.xtuple.org/xtincident/view/bugs/25704)
  _Add Zone filter to Locations screen_
- Implemented
  issue #[25705](http://www.xtuple.org/xtincident/view/bugs/25705)
  _allow extensions to add their own document associations_
- Implemented
  issue #[25707](http://www.xtuple.org/xtincident/view/bugs/25707)
  _Add Comments to Bill of Materials header_
- Fixed
  issue #[25734](http://www.xtuple.org/xtincident/view/bugs/25734)
  _*PO Pulls wrong "ShipToName"_
- Fixed
  issue #[25736](http://www.xtuple.org/xtincident/view/bugs/25736)
  _*Unable to build the masterref database from xTuple repositories_
- Fixed
  issue #[25744](http://www.xtuple.org/xtincident/view/bugs/25744)
  _Ship To defaults to Recently added, cannot change back_
- Fixed
  issue #[25757](http://www.xtuple.org/xtincident/view/bugs/25757)
  _*Omnibus: Unable to create any record_
- Fixed
  issue #[25760](http://www.xtuple.org/xtincident/view/bugs/25760)
  _* Linux: Unable to  Log In into xTuple Qt 4 build_

## Deployment Notes

We've lately revised the
naming conventions and the behavior of our core updater packages.
Our overall goal is to simplify the process of installing and
upgrading xTuple ERP databases.

Just as was true for the 4.4.1 release, you will only need to apply
one updater package to upgrade to 4.9.0Beta--that is, assuming you are
already running on at least 4.4.0. The new updater packages are
designed to bring you all the way up to their version, no matter
what version (>= 4.4.0!) that you're on.

In 4.5.0 we went a step further: not only will a single package take
you through every *version* of the app, it will also install all the
constituent parts of your edition. Before now, if you wanted to do an
upgrade to the Manufacturing Edition, you would have needed to perform
the standard/dist upgrade and then the manufacturing upgrade. Not any
more. With the new process, only one upgrade package is needed for the
entire upgrade. No more upgrading the core and then upgrading the
related packages. Everything is upgraded all at once.

NOTE FOR DISTRIBUTION EDITION CUSTOMERS: The xwd package no longer
exists as a separate entity. All the functionality that was contained
in the xwd package is now included in the single "distribution" upgrade
or install package.

To be verbose about all of this:

    postbooks-upgrade-490Beta.gz will:
    upgrade a PostBooks database from anywhere >= 4.4.0 to 4.9.0Beta

    manufacturing-upgrade-490Beta.gz will:
    upgrade the standard/dist (i.e., inventory code) to 4.9.0Beta
    upgrade the manufacturing code to 4.9.0Beta

    manufacturing-install-490Beta.gz will:
    do a one-time install of tables, etc. for standard (i.e., inventory code) at 4.9.0Beta
    upgrade the standard/dist (i.e., inventory code) to 4.9.0Beta
    do a one-time install of tables, etc. for manufacturing at 4.9.0Beta
    upgrade the manufacturing code to 4.9.0Beta

    distribution-upgrade-490Beta.gz will:
    upgrade the standard/ist (i.e., inventory code) to 4.9.0Beta
    upgrade the distribution (i.e., xwd code) to 4.9.0Beta

    distribution-install-490Beta.gz will:
    do a one-time install of tables, etc. for standard (i.e., inventory code) at 4.9.0Beta
    upgrade the standard/dist (i.e., inventory code) to 4.9.0Beta
    do a one-time install of tables etc for distribution at 4.9.0Beta
    upgrade the distribution (i.e., xwd code) to 4.9.0Beta

PLEASE NOTE: Other packages, such as Advanced Commissions and Fixed
Assets, are currently remaining on their own release schedule and should
be installed as before.
