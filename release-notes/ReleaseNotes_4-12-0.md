
# xTuple Release Notes

## Version 4.12.0-alpha - November, 2018

These are the release notes for the 4.12.0-alpha xTuple ERP release.
Thanks to all who contributed to make this release possible, including
Cordeck Building Solutions, Larry Cartee, Alfredo Martinez, Scott Zuke, 
Steven Buttgereit, Jim Wirt, Wes Baker, and Joel White.  See below for
 more information about [deploying this release](#deployment-notes).

### Summary

A large number of features and bug fixes have been added to the application since the 4.11.3 release. Our focus has been on enhancing the capabilities of CRM.

Of particular interest are the following:

- Recurring Sales Orders
- Bulk replacement and other improvements to contacts screen
- Address search functionality
- Document characteristics and other document tab enhancements
- A number of bug fixes and feature work were contributed by the community members named above. Thank you!

### Features added in 4.12.0-alpha

- Prof. Services issue #[33735](http://www.xtuple.org/xtincident/view/bugs/33735) _Need to stop recording history on actual cost posting_
- Implemented issue #[3445](http://www.xtuple.org/xtincident/view/bugs/3445) _Add Work Order Operations by Work Center_
- Implemented issue #[9924](http://www.xtuple.org/xtincident/view/bugs/9924) _Trim White Space at Start and End of Text Entry Fields on update_
- Implemented issue #[10370](http://www.xtuple.org/xtincident/view/bugs/10370) _Need ability to Search Addresses_
- Implemented issue #[11094](http://www.xtuple.org/xtincident/view/bugs/11094) _Add a PO Cost Column to the Un-invoiced P/O Receipts and Return Report_
- Implemented issue #[11131](http://www.xtuple.org/xtincident/view/bugs/11131) _Add CSV support to Export Data Functionality and call application to open resulting CSV file._
- Implemented issue #[11525](http://www.xtuple.org/xtincident/view/bugs/11525) _Configure Encryption window should have a key creation editor_
- Implemented issue #[11967](http://www.xtuple.org/xtincident/view/bugs/11967) _Cloud users need a way to set their timezone in relation to wherever the server lives._
- Implemented issue #[14260](http://www.xtuple.org/xtincident/view/bugs/14260) _Opportunity list does not allow you to filter by name_
- Implemented issue #[22233](http://www.xtuple.org/xtincident/view/bugs/22233) _SO Shipping notes auto copying to PO notes for linked POs_
- Implemented issue #[23330](http://www.xtuple.org/xtincident/view/bugs/23330) _Increase the Order setting in Characteristics._
- Implemented issue #[25092](http://www.xtuple.org/xtincident/view/bugs/25092) _Document Tab Enhancements_
- Implemented issue #[25779](http://www.xtuple.org/xtincident/view/bugs/25779) _Allow Cash Receipt screen to remain open after save_
- Implemented issue #[27709](http://www.xtuple.org/xtincident/view/bugs/27709) _Altering Customer Number in ERP when account is created by xTupleCommerce_
- Implemented issue #[29289](http://www.xtuple.org/xtincident/view/bugs/29289) _Need to edit line numbers in BOMs_
- Implemented issue #[29457](http://www.xtuple.org/xtincident/view/bugs/29457) _Add coitem_id, invcitem_id and invchead_id to cohist table where applicable_
- Implemented issue #[30503](http://www.xtuple.org/xtincident/view/bugs/30503) _CRM -- Need tool to cleanse Contacts (list hygiene)_
- Implemented issue #[30861](http://www.xtuple.org/xtincident/view/bugs/30861) _Detail on AP Misc Vr for Landed Costs_
- Implemented issue #[30866](http://www.xtuple.org/xtincident/view/bugs/30866) _Landed Cost Cross reference document identification_
- Implemented issue #[33430](http://www.xtuple.org/xtincident/view/bugs/33430) _Receive PO from Open PO list_
- Implemented issue #[33551](http://www.xtuple.org/xtincident/view/bugs/33551) _Add Documents and Characteristics to the Item Group window in core_
- Implemented issue #[33786](http://www.xtuple.org/xtincident/view/bugs/33786) _Add multi-select to billing approvals_

### Bug fixes in 4.12.0-alpha

- Fixed issue #[6171](http://www.xtuple.org/xtincident/view/bugs/6171) _While creating a new Return Authorization it is possible to enter the expired date prior to the created date_
- Fixed issue #[10146](http://www.xtuple.org/xtincident/view/bugs/10146) _No privileges are required to perform some transactions_
- Fixed issue #[13995](http://www.xtuple.org/xtincident/view/bugs/13995) _Can't resize post operations screen_
- Fixed issue #[16877](http://www.xtuple.org/xtincident/view/bugs/16877) _Print from Print Preview does nothing_
- Fixed issue #[17052](http://www.xtuple.org/xtincident/view/bugs/17052) _Vendor Type Pattern_
- Fixed issue #[18464](http://www.xtuple.org/xtincident/view/bugs/18464) _non - functional field in api view_
- Fixed issue #[21356](http://www.xtuple.org/xtincident/view/bugs/21356) _Broken summarizedBOM Functions_
- Fixed issue #[22377](http://www.xtuple.org/xtincident/view/bugs/22377) _It is possible to create duplicate Item Sources_
- Fixed issue #[24325](http://www.xtuple.org/xtincident/view/bugs/24325) _Item source can be created with 'Inventory / Vendor UOM Ratio' field value as zero_
- Fixed issue #[24368](http://www.xtuple.org/xtincident/view/bugs/24368) _Cannot Scroll Down on View Customer Characteristics_
- Fixed issue #[24514](http://www.xtuple.org/xtincident/view/bugs/24514) _Item Source requires a Vendor Item Number in order to save._
- Fixed issue #[25111](http://www.xtuple.org/xtincident/view/bugs/25111) _Can't find where to change default ship-to name on PO_
- Fixed issue #[25322](http://www.xtuple.org/xtincident/view/bugs/25322) _AR statement problem_
- Fixed issue #[26036](http://www.xtuple.org/xtincident/view/bugs/26036) _Application crashes on selecting to attach an image to an 'Employee'_
- Fixed issue #[26195](http://www.xtuple.org/xtincident/view/bugs/26195) _LotserialseqCluster does not contain "New" action_
- Fixed issue #[29162](http://www.xtuple.org/xtincident/view/bugs/29162) _'Use Alt.Label' checkbox is in enabled mode even after 'Show Subtotal' checkbox is disabled in 'Financial Report Group' screen_
- Fixed issue #[29272](http://www.xtuple.org/xtincident/view/bugs/29272) _Lot/Serial integrity not maintained through Transfer Order_
- Fixed issue #[29417](http://www.xtuple.org/xtincident/view/bugs/29417) _api.itemcost and api.itemsourceprice do not default currency_
- Fixed issue #[29591](http://www.xtuple.org/xtincident/view/bugs/29591) _The `usr` view is slow on databases with lots of `usrpref` records_
- Fixed issue #[30473](http://www.xtuple.org/xtincident/view/bugs/30473) _Problem with saving invoice number after prompt_
- Fixed issue #[30500](http://www.xtuple.org/xtincident/view/bugs/30500) _Unclear sales order status: no lines_
- Fixed issue #[30893](http://www.xtuple.org/xtincident/view/bugs/30893) _api.site view _INSERT rule attempts invalid coalesce on tax_zone field_
- Fixed issue #[30897](http://www.xtuple.org/xtincident/view/bugs/30897) _double click on pricing schedule opens in view mode vs. edit mode_
- Fixed issue #[31164](http://www.xtuple.org/xtincident/view/bugs/31164) _Checkbox Settings Reverting_
- Fixed issue #[31459](http://www.xtuple.org/xtincident/view/bugs/31459) _Escape value string in MetaSQL js PEG parser_
- Fixed issue #[31691](http://www.xtuple.org/xtincident/view/bugs/31691) _Bank rec do not populate_
- Fixed issue #[31801](http://www.xtuple.org/xtincident/view/bugs/31801) _missing field on api.invoiceline_
- Fixed issue #[31856](http://www.xtuple.org/xtincident/view/bugs/31856) _Copy Item not copying default locations_
- Fixed issue #[31857](http://www.xtuple.org/xtincident/view/bugs/31857) _Std Journal Entry - post requires note - but note is disabled_
- Fixed issue #[31858](http://www.xtuple.org/xtincident/view/bugs/31858) _Auto FIscal year creator fail_
- Fixed issue #[31859](http://www.xtuple.org/xtincident/view/bugs/31859) _‘Error Deleting Purchase Order’ error occurs while cancelling a Purchase Order at the time of  creation._
- Fixed issue #[32021](http://www.xtuple.org/xtincident/view/bugs/32021) _Desktop Login screen missing information_
- Fixed issue #[32113](http://www.xtuple.org/xtincident/view/bugs/32113) _Cannot post checks from the AP workbench_
- Fixed issue #[32197](http://www.xtuple.org/xtincident/view/bugs/32197) _Mixed UOM Price Schedule/Sales Order Pricing Issues_
- Fixed issue #[32262](http://www.xtuple.org/xtincident/view/bugs/32262) _Sales credit return on 0 cost_
- Fixed issue #[32304](http://www.xtuple.org/xtincident/view/bugs/32304) _Printed Sales order doesn't show the correct information_
- Fixed issue #[32307](http://www.xtuple.org/xtincident/view/bugs/32307) _Inventory history shows cost updates when no change_
- Fixed issue #[32322](http://www.xtuple.org/xtincident/view/bugs/32322) _‘View Allocations...’ & ‘View Orders’ context menu options are not working for the MPS Details._
- Fixed issue #[32336](http://www.xtuple.org/xtincident/view/bugs/32336) _Upside down sorting arrow_
- Fixed issue #[32343](http://www.xtuple.org/xtincident/view/bugs/32343) _Inventory transactions can result in orphaned Sales Reservations_
- Fixed issue #[32371](http://www.xtuple.org/xtincident/view/bugs/32371) _Log In Field issue_
- Fixed issue #[32453](http://www.xtuple.org/xtincident/view/bugs/32453) _Supply Order Issue with SO_
- Fixed issue #[32601](http://www.xtuple.org/xtincident/view/bugs/32601) _Accounting Payables "widget" crashes xTuple_
- Fixed issue #[32648](http://www.xtuple.org/xtincident/view/bugs/32648) _SO Ship To is not always retained( Sales Order Srops Shipto_id when Shipto has not State set and zip is 9999)_
- Fixed issue #[32676](http://www.xtuple.org/xtincident/view/bugs/32676) _Invoice duplicate ( item alias assigned to more than one customer causes Duplicate items on Invoice Form)_
- Fixed issue #[32734](http://www.xtuple.org/xtincident/view/bugs/32734) _DLineEdit returning passing timestamp to metasql_
- Fixed issue #[32748](http://www.xtuple.org/xtincident/view/bugs/32748) _Location not showing up on pick list_
- Fixed issue #[32770](http://www.xtuple.org/xtincident/view/bugs/32770) _Pricing schedule by Customer Report_
- Fixed issue #[32788](http://www.xtuple.org/xtincident/view/bugs/32788) _dspProcess SQL syntax error (really type error)_
- Fixed issue #[32827](http://www.xtuple.org/xtincident/view/bugs/32827) _Price values in ‘Preview’ mode of ‘Item Sources Prices’ screen are displayed incorrectly_
- Fixed issue #[32842](http://www.xtuple.org/xtincident/view/bugs/32842) _In ‘Shipment by Shipment’ screen, attempting to query shipment number displays error._
- Fixed issue #[32855](http://www.xtuple.org/xtincident/view/bugs/32855) _Translation problem_
- Fixed issue #[32856](http://www.xtuple.org/xtincident/view/bugs/32856) _Cannot set language to english_
- Fixed issue #[32858](http://www.xtuple.org/xtincident/view/bugs/32858) _Cash receipt table field is not consistent_
- Fixed issue #[32897](http://www.xtuple.org/xtincident/view/bugs/32897) _New incident history dialog can show up blank in older databases_
- Fixed issue #[32903](http://www.xtuple.org/xtincident/view/bugs/32903) _void posted check fails for multicurrency on AP checks_
- Fixed issue #[32908](http://www.xtuple.org/xtincident/view/bugs/32908) _Issue material to WO - BATCH - Serial Control item 0 on hand entire batch process stops_
- Fixed issue #[32927](http://www.xtuple.org/xtincident/view/bugs/32927) _Invoice printing issues_
- Fixed issue #[32947](http://www.xtuple.org/xtincident/view/bugs/32947) _Bank Reconciliation Report - bug in totaling query_
- Fixed issue #[32948](http://www.xtuple.org/xtincident/view/bugs/32948) _Sales Order Not Creating Work Orders after first line_
- Fixed issue #[32950](http://www.xtuple.org/xtincident/view/bugs/32950) _Erroneous SQL error when posting top-level WO scrap (4.11.2)_
- Fixed issue #[32956](http://www.xtuple.org/xtincident/view/bugs/32956) _As of Available QOH in Inventory Availability not working_
- Fixed issue #[33000](http://www.xtuple.org/xtincident/view/bugs/33000) _itemCharPrice() performance is slow for xTupleCommerce Product list queries with several items that have various characteristic pricing_
- Fixed issue #[33100](http://www.xtuple.org/xtincident/view/bugs/33100) _Create workOrder checkbox not working in salesOrderItem Window_
- Fixed issue #[33103](http://www.xtuple.org/xtincident/view/bugs/33103) _fundstype table has old "Master Card" fundstype_name from 4.10 database that was updated to "MasterCard" in 4.11_
- Fixed issue #[33104](http://www.xtuple.org/xtincident/view/bugs/33104) _‘Site’ column is displayed twice in ‘Employees’ screen._
- Fixed issue #[33122](http://www.xtuple.org/xtincident/view/bugs/33122) _Return lot tracked stock from W/O on large DB very slow_
- Fixed issue #[33194](http://www.xtuple.org/xtincident/view/bugs/33194) _Item Copy not copying user defined costs._
- Fixed issue #[33214](http://www.xtuple.org/xtincident/view/bugs/33214) _4.11.3 Viewing sales order fails intermittently_
- Fixed issue #[33218](http://www.xtuple.org/xtincident/view/bugs/33218) _Landed Costs - Incorrect element display_
- Fixed issue #[33229](http://www.xtuple.org/xtincident/view/bugs/33229) _Advanced commissions creates a voucher that cannot be posted_
- Fixed issue #[33238](http://www.xtuple.org/xtincident/view/bugs/33238) _Possible to receive items into inactive item sites_
- Fixed issue #[33242](http://www.xtuple.org/xtincident/view/bugs/33242) _XM.Invoice is missing Shipping info column on Postbooks databases_
- Fixed issue #[33254](http://www.xtuple.org/xtincident/view/bugs/33254) _shipheadbeforetrigger performance issue_
- Fixed issue #[33262](http://www.xtuple.org/xtincident/view/bugs/33262) _Sales Order Payment/Document # Field Not Clearing Upon Saving_
- Fixed issue #[33271](http://www.xtuple.org/xtincident/view/bugs/33271) _Puts current date in Started Date in a project_
- Fixed issue #[33279](http://www.xtuple.org/xtincident/view/bugs/33279) _4.11 incompatible with lot serial_
- Fixed issue #[33298](http://www.xtuple.org/xtincident/view/bugs/33298) _WO associated to SO closes automatically when the invoice in created_
- Fixed issue #[33431](http://www.xtuple.org/xtincident/view/bugs/33431) _Inconsistencies with Inability to delete electronically transmitted check_
- Fixed issue #[33447](http://www.xtuple.org/xtincident/view/bugs/33447) _Project Completed date set to current day automatically._
- Fixed issue #[33448](http://www.xtuple.org/xtincident/view/bugs/33448) _Contact Email Addresses problem with capital letters_
- Fixed issue #[33466](http://www.xtuple.org/xtincident/view/bugs/33466) _widget _wocharView does not edit or delete_
- Fixed issue #[33500](http://www.xtuple.org/xtincident/view/bugs/33500) _mis spelled column name in function_
- Fixed issue #[33518](http://www.xtuple.org/xtincident/view/bugs/33518) _Documents Tab no longer on Item Group window_
- Fixed issue #[33563](http://www.xtuple.org/xtincident/view/bugs/33563) _Cannot void sales credit with miscellaneous line item_
- Fixed issue #[33565](http://www.xtuple.org/xtincident/view/bugs/33565) _Possible to edit posted sales credit_
- Fixed issue #[33596](http://www.xtuple.org/xtincident/view/bugs/33596) _WO screens take excessive time to resolve._
- Fixed issue #[33633](http://www.xtuple.org/xtincident/view/bugs/33633) _Bank Rec shows outstanding transactions too far into the future_
- Fixed issue #[33639](http://www.xtuple.org/xtincident/view/bugs/33639) _Bank rec Account list has all bank accounts listed_
- Fixed issue #[33714](http://www.xtuple.org/xtincident/view/bugs/33714) _Configured Item errors on sales order items_
- Fixed issue #[33723](http://www.xtuple.org/xtincident/view/bugs/33723) _Discovery Doc fails to load after 33240 xt.ordhead clause_
- Fixed issue #[33730](http://www.xtuple.org/xtincident/view/bugs/33730) _SO in project miscalculates pricing schedule_
- Fixed issue #[33734](http://www.xtuple.org/xtincident/view/bugs/33734) _Report does not honor screen filter_
- Fixed issue #[33736](http://www.xtuple.org/xtincident/view/bugs/33736) _Only One Lot/Serial displayed when Receipting Transfer Orders with multiple item lots_
- Fixed issue #[33754](http://www.xtuple.org/xtincident/view/bugs/33754) _Can't print pick list for transfer orders after upgrade_
- Fixed issue #[33759](http://www.xtuple.org/xtincident/view/bugs/33759) _Supply Order not generated if it is the same as line 2_
- Fixed issue #[33812](http://www.xtuple.org/xtincident/view/bugs/33812) _TO receipts to not record lot serial detail in inventory history_
- Fixed issue #[33833](http://www.xtuple.org/xtincident/view/bugs/33833) _trying to change the Scheduled Date_
- Fixed issue #[33855](http://www.xtuple.org/xtincident/view/bugs/33855) _Pricing schedule not working for annual items?_
- Fixed issue #[33858](http://www.xtuple.org/xtincident/view/bugs/33858) _Purchase Order Open Causes Extraneous Search Box to Open_
- Fixed issue #[33879](http://www.xtuple.org/xtincident/view/bugs/33879) _Lot/Serial item with sequence enabled overrides ability to receipt correct lot on Return Authorisations_
- Fixed issue #[33936](http://www.xtuple.org/xtincident/view/bugs/33936) _Item Cost by Class Code Report Different On-screen than Printed_
- Fixed issue #[34022](http://www.xtuple.org/xtincident/view/bugs/34022) _vendor api view_
- Fixed issue #[34114](http://www.xtuple.org/xtincident/view/bugs/34114) _api.bom view is empty after upgrade to 4.11.3_


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

## Deployment Notes

If you are running version 4.4.0 or later of xTuple ERP, you will only need to apply
one updater package to upgrade to the latest release. The new updater packages are
designed to bring you all the way up to their version, no matter
what version (>= 4.4.0!) that you're on.
See [the FAQ on xTupleU](https://xtupleuniversity.xtuple.com/library/faqs?field_subject_tid=23&field_role_tid=All&title=upgra&sort_by=value&sort_order=DESC&items_per_page=25)
if you have problems.

If you are upgrading from PostBooks to any of the other editions, you simply need to run the installation package for that edition. This will upgrade both your xTuple ERP version _and_ edition. There is a special package for upgrading the Manufacturing Edition to Enterprise Edition.

NOTE FOR DISTRIBUTION EDITION CUSTOMERS: The xwd package no longer
exists as a separate entity. All the functionality that was contained
in the xwd package is now included in the single "distribution" upgrade
or install package.

To be verbose about all of this:

-   postbooks-upgrade-4.12.0Alpha.gz
    upgrades a PostBooks database from anywhere >= 4.4.0 to 4.12.0-alpha
-   distribution-upgrade-4.12.0Alpha.gz
    upgrades the core (i.e. inventory) and
    distribution code (i.e. xwd) to 4.12.0-alpha
-   distribution-install-4.12.0Alpha.gz
    does a one-time install of tables, etc. for core and distribution at 4.12.0-alpha
-   manufacturing-upgrade-4.12.0Alpha.gz
    upgrades the core and manufacturing code to 4.12.0-alpha
-   manufacturing-install-4.12.0Alpha.gz
    does a one-time install of tables, etc. for core and manufacturing at 4.12.0-alpha
-   enterprise-upgrade-4.12.0Alpha.gz
    upgrades the core, distribution, and manufacturing code to 4.12.0-alpha
-   enterprise-install-4.12.0Alpha.gz
    does a one-time install of tables, etc. for core, distribution,
    and manufacturing at 4.12.0-alpha

PLEASE NOTE: Other packages, such as Advanced Commissions and Fixed
Assets, are currently on their own release schedule and should
be installed as before.
