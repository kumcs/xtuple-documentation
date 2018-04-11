
# xTuple Release Notes

## Version 4.11.1 - October, 2017

These are the release notes for the 4.11.1 xTuple ERP release.
Thanks to all who contributed to make this release possible,
including Verlin Nooner and Scott Zuke.
See below for more information about
[deploying this release](#deployment-notes).

### Summary

A handful of features and lots of bug fixes have been added to the
application since the 4.11.0 release. Our focus has been on improving
overall quality and functionality.

Of particular interest are the following:

- Fixes to the autocompleter bugs
- Improvements in CSVImp 0.6.0
  - Importing images and other files
  - Update and Append

CSVImp 0.6.0 will be released with and bundled into xTuple ERP 4.11.1.

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

### Features added in 4.11.1

- Features issue #[5043](http://www.xtuple.org/xtincident/view/bugs/5043) _Right Click to View Characteristics for P/R_
- Features issue #[19111](http://www.xtuple.org/xtincident/view/bugs/19111) _Add support for item characteristics to misc. invoice_
- Features issue #[29526](http://www.xtuple.org/xtincident/view/bugs/29526) _distribution catalog - would like to be able to double click and edit or view a catcost item_
- Features issue #[29873](http://www.xtuple.org/xtincident/view/bugs/29873) _Prompt for GL posting date when voiding posted invoice_
- Features issue #[29880](http://www.xtuple.org/xtincident/view/bugs/29880) _Need utility for loading images into ERP database_
- Features issue #[30854](http://www.xtuple.org/xtincident/view/bugs/30854) _Expose the dispatch service XM.SalesOrder.addPayment() to the REST API._

### Bug fixes in 4.11.1

- Fixed issue #[14206](http://www.xtuple.org/xtincident/view/bugs/14206) _Observation: No label is displayed for date field in the 'Credit Card Transaction Information' screen_
- Fixed issue #[16185](http://www.xtuple.org/xtincident/view/bugs/16185) _invalid pricing schedule assignment patterns disrupt editing sales orders_
- Fixed issue #[16275](http://www.xtuple.org/xtincident/view/bugs/16275) _Incorrect site is displayed on selecting to post Miscellaneous Production from 'Inventory Availability' screen_
- Fixed issue #[17127](http://www.xtuple.org/xtincident/view/bugs/17127) _Alarm Date not enabled_
- Fixed issue #[17680](http://www.xtuple.org/xtincident/view/bugs/17680) _Irrelevant behavior is observed for Account creation when CRM Account # generation is set to 'Automatic'_
- Fixed issue #[19021](http://www.xtuple.org/xtincident/view/bugs/19021) _inconsistency in RAs (receiving site)_
- Fixed issue #[19378](http://www.xtuple.org/xtincident/view/bugs/19378) _duplicate database indexes_
- Fixed issue #[20717](http://www.xtuple.org/xtincident/view/bugs/20717) _Irrelevant behaviour is observed in Customer Groups screen_
- Fixed issue #[21869](http://www.xtuple.org/xtincident/view/bugs/21869) _XML Import - Ship To incorrectly selected_
- Fixed issue #[24362](http://www.xtuple.org/xtincident/view/bugs/24362) _xWDSPA: Selecting to change the SPA number from 'N/A' to any displays Database Error irrelevantly_
- Fixed issue #[24425](http://www.xtuple.org/xtincident/view/bugs/24425) _Item Alias Behavior in Sales Order_
- Fixed issue #[25421](http://www.xtuple.org/xtincident/view/bugs/25421) _Trade Service LOD file changes Price UOM_
- Fixed issue #[25682](http://www.xtuple.org/xtincident/view/bugs/25682) _Edit option missing from purchase request menu_
- Fixed issue #[26127](http://www.xtuple.org/xtincident/view/bugs/26127) _Alias not selected for SO showing in customer part field_
- Fixed issue #[26158](http://www.xtuple.org/xtincident/view/bugs/26158) _Identical alias for different item cannot be selected_
- Fixed issue #[27331](http://www.xtuple.org/xtincident/view/bugs/27331) _System does not honor the characteristics created in 'Sales' setup_
- Fixed issue #[27513](http://www.xtuple.org/xtincident/view/bugs/27513) _Possible to make changes to order being edited by another user_
- Fixed issue #[27538](http://www.xtuple.org/xtincident/view/bugs/27538) _Irrelevant behavior is observed when clicking 'cancel' button on 'Incident' screen_
- Fixed issue #[27555](http://www.xtuple.org/xtincident/view/bugs/27555) _[postbooks] ""May use the full application"" visible when it is the only option_
- Fixed issue #[27772](http://www.xtuple.org/xtincident/view/bugs/27772) _many displays are hard to open or extend with scripting_
- Fixed issue #[27860](http://www.xtuple.org/xtincident/view/bugs/27860) _Disabling a package schema should disable triggers on public tables_
- Fixed issue #[28159](http://www.xtuple.org/xtincident/view/bugs/28159) _PO Litem Characteristics cannot be added to a PO line Item_
- Fixed issue #[28276](http://www.xtuple.org/xtincident/view/bugs/28276) _invcitem_updateinv column allows nulls_
- Fixed issue #[28370](http://www.xtuple.org/xtincident/view/bugs/28370) _'Standard', 'Actual' fields are not properly aligned in 'Item List Price' screen_
- Fixed issue #[28548](http://www.xtuple.org/xtincident/view/bugs/28548) _Ship-via does not populate on Invoice_
- Fixed issue #[28625](http://www.xtuple.org/xtincident/view/bugs/28625) _Inventory Availability screen does not support multiple filter parameters (fix attached)_
- Fixed issue #[29026](http://www.xtuple.org/xtincident/view/bugs/29026) _'Standard Oper.' field name is displayed instead of 'Standard Operation' in 'Work Order Operation' screen_
- Fixed issue #[29164](http://www.xtuple.org/xtincident/view/bugs/29164) _Able to save Financial report group with blank names in Financial Report screen._
- Fixed issue #[29166](http://www.xtuple.org/xtincident/view/bugs/29166) _'Edit' Button is not functional in 'Column Layout' screen._
- Fixed issue #[29222](http://www.xtuple.org/xtincident/view/bugs/29222) _AP Multi-Currency Posting Issue_
- Fixed issue #[29234](http://www.xtuple.org/xtincident/view/bugs/29234) _Allowed entry of non numeric causes termination of sql_
- Fixed issue #[29248](http://www.xtuple.org/xtincident/view/bugs/29248) _api.bom creates multiple active revisions_
- Fixed issue #[29291](http://www.xtuple.org/xtincident/view/bugs/29291) _No error message when trying to delete payment terms used only on a PO_
- Fixed issue #[29342](http://www.xtuple.org/xtincident/view/bugs/29342) _Using the 'X' object to cancel on Contact screen leaves record_
- Fixed issue #[29363](http://www.xtuple.org/xtincident/view/bugs/29363) _Able to enter item details in 'Purchase Order Item' screen though 'Site Can Purchase This Item' check box is disabled for item_
- Fixed issue #[29385](http://www.xtuple.org/xtincident/view/bugs/29385) _Omnibus: Filters are disappeared when minimizing and maximizing 'Quantities on Hand' screen._
- Fixed issue #[29523](http://www.xtuple.org/xtincident/view/bugs/29523) _Transaction block error while trying to update roles_
- Fixed issue #[29701](http://www.xtuple.org/xtincident/view/bugs/29701) _xTupleCommerce: CBUMP bumper in demodb has no list price, yet is marked as sellable._
- Fixed issue #[29808](http://www.xtuple.org/xtincident/view/bugs/29808) _'Lot/Serial' tab is in disable mode after removing the item number in 'Return Authorization Item' screen_
- Fixed issue #[29996](http://www.xtuple.org/xtincident/view/bugs/29996) _'Select button' is enabled without selecting Bank Account in 'Select Bank Account' dialog box in 'Approve Payments' screen._
- Fixed issue #[30012](http://www.xtuple.org/xtincident/view/bugs/30012) _Sales Order Item Tab Order Changed_
- Fixed issue #[30094](http://www.xtuple.org/xtincident/view/bugs/30094) _Preferred selling site on ship-to address not honored_
- Fixed issue #[30189](http://www.xtuple.org/xtincident/view/bugs/30189) _'Due date' field is not refreshed on changing Terms in 'Miscellaneous Voucher' screen_
- Fixed issue #[30315](http://www.xtuple.org/xtincident/view/bugs/30315) _Reversed invoice indicator needs work_
- Fixed issue #[30391](http://www.xtuple.org/xtincident/view/bugs/30391) _Sales Order form items list incorrectly assumes that Customer PN Item Aliases will be unique_
- Fixed issue #[30469](http://www.xtuple.org/xtincident/view/bugs/30469) _Post Operation when the user / server in different timezone:  wooperpost - wrong date and time_
- Fixed issue #[30591](http://www.xtuple.org/xtincident/view/bugs/30591) _[xtuple] Detail query in Items report incorrectly inner joins on prodcat_id and item_price_uom_id_
- Fixed issue #[30595](http://www.xtuple.org/xtincident/view/bugs/30595) _4.11 Nordic: Numeric Keypad ""ENTER"" Key does not affect POST in distribute Window_
- Fixed issue #[30603](http://www.xtuple.org/xtincident/view/bugs/30603) _Drill down on Summarized Sales History report Error_
- Fixed issue #[30607](http://www.xtuple.org/xtincident/view/bugs/30607) _Voiding a check in local currency fails_
- Fixed issue #[30628](http://www.xtuple.org/xtincident/view/bugs/30628) _ParameterWidget/XComboBox reports wrong value when ""null"" (scripting)_
- Fixed issue #[30636](http://www.xtuple.org/xtincident/view/bugs/30636) _Inventory zone report uses location comment instead of ARBL naming convention_
- Fixed issue #[30663](http://www.xtuple.org/xtincident/view/bugs/30663) _Node.js database connections lose js_init's search path_
- Fixed issue #[30677](http://www.xtuple.org/xtincident/view/bugs/30677) _calcsalesorderamt_
- Fixed issue #[30679](http://www.xtuple.org/xtincident/view/bugs/30679) _Merge / Purge Utility cannot be used by more than one person at a time_
- Fixed issue #[30685](http://www.xtuple.org/xtincident/view/bugs/30685) _Tab entry changed on misc. distribution screen_
- Fixed issue #[30689](http://www.xtuple.org/xtincident/view/bugs/30689) _Extra space is observed in between the fields in ‘Item List Prices’ screen._
- Fixed issue #[30693](http://www.xtuple.org/xtincident/view/bugs/30693) _Accounting Periods_
- Fixed issue #[30703](http://www.xtuple.org/xtincident/view/bugs/30703) _Freight breakdown value is incorrectly displayed in ‘Freight Breakdown’ when return authorization disposition is ‘Replace’._
- Fixed issue #[30708](http://www.xtuple.org/xtincident/view/bugs/30708) _XComboBox removeItem method leaves object in an inconsistent state (scripting)_
- Fixed issue #[30721](http://www.xtuple.org/xtincident/view/bugs/30721) _Unable to do buildapp on masterref database_
- Fixed issue #[30781](http://www.xtuple.org/xtincident/view/bugs/30781) _Item Number List Widget misbehaving on Mac 4.11_
- Fixed issue #[30788](http://www.xtuple.org/xtincident/view/bugs/30788) _WO Lead Time not being added_
- Fixed issue #[30796](http://www.xtuple.org/xtincident/view/bugs/30796) _RA Item Notes don't follow SO_
- Fixed issue #[30802](http://www.xtuple.org/xtincident/view/bugs/30802) _‘Error Saving Item Information’ dialog is displayed when sales order ‘line item’ is created in Distribution Empty Database_
- Fixed issue #[30813](http://www.xtuple.org/xtincident/view/bugs/30813) _View Transaction Link on Trial Balance Report_
- Fixed issue #[30822](http://www.xtuple.org/xtincident/view/bugs/30822) _Received qty does not consider returns_
- Fixed issue #[30851](http://www.xtuple.org/xtincident/view/bugs/30851) _cannot disable an extension if it contains a trigger with a mixed-case name_
- Fixed issue #[30852](http://www.xtuple.org/xtincident/view/bugs/30852) _Cannot view voucher item screen_
- Fixed issue #[30864](http://www.xtuple.org/xtincident/view/bugs/30864) _Landed Cost Distribution creates erros in Maintain Item Cost_
- Fixed issue #[30867](http://www.xtuple.org/xtincident/view/bugs/30867) _‘Error Posting Transaction’ dialog is displayed while posting a transaction in Enterprise and Distribution Editions_
- Fixed issue #[30898](http://www.xtuple.org/xtincident/view/bugs/30898) _Selection of GL account from dropdown not honored_
- Fixed issue #[30901](http://www.xtuple.org/xtincident/view/bugs/30901) _Price UOM not working as expected_
- Fixed issue #[30903](http://www.xtuple.org/xtincident/view/bugs/30903) _‘Error enabling package’ dialog is displayed while disabling ‘xt’ package in ‘List Packages’ screen._
- Fixed issue #[30943](http://www.xtuple.org/xtincident/view/bugs/30943) _Freight Distribution error on AP-PO Vouchering version 4.11.0_
- Fixed issue #[30945](http://www.xtuple.org/xtincident/view/bugs/30945) _Converting multiple unrelated UOMs does not work_
- Fixed issue #[30947](http://www.xtuple.org/xtincident/view/bugs/30947) _api.customer view balance_method not compatible between select and insert/update_
- Fixed issue #[30950](http://www.xtuple.org/xtincident/view/bugs/30950) _Customer name not transferring to linked work order_
- Fixed issue #[30958](http://www.xtuple.org/xtincident/view/bugs/30958) _Constraint on Rev table doesn't allow ""S"" status_
- Fixed issue #[31002](http://www.xtuple.org/xtincident/view/bugs/31002) _Vendor Records are not Saved_
- Fixed issue #[31017](http://www.xtuple.org/xtincident/view/bugs/31017) _Multicompany sync login screen does not support enhanced authentication_

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

-   postbooks-upgrade-4.11.1.gz
    upgrades a PostBooks database from anywhere >= 4.4.0 to 4.11.1
-   distribution-upgrade-4.11.1.gz
    upgrades the core (i.e. inventory) and
    distribution code (i.e. xwd) to 4.11.1
-   distribution-install-4.11.1.gz
    does a one-time install of tables, etc. for core and distribution at 4.11.1
-   manufacturing-upgrade-4.11.1.gz
    upgrades the core and manufacturing code to 4.11.1
-   manufacturing-install-4.11.1.gz
    does a one-time install of tables, etc. for core and manufacturing at 4.11.1
-   enterprise-upgrade-4.11.1.gz
    upgrades the core, distribution, and manufacturing code to 4.11.1
-   enterprise-install-4.11.1.gz
    does a one-time install of tables, etc. for core, distribution,
    and manufacturing at 4.11.1

PLEASE NOTE: Other packages, such as Advanced Commissions and Fixed
Assets, are currently on their own release schedule and should
be installed as before.
