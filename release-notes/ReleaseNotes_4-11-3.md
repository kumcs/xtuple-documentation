
# xTuple Release Notes

## Version 4.11.3 - ?????, 2018

These are the release notes for the 4.11.3 xTuple ERP release.
Thanks to all who contributed to make this release possible, including
Cordeck Building Solutions, Larry Cartee, Bernard LeJour, Alfredo
Martinez, and Scott Zuke.  See below for more information about
[deploying this release](#deployment-notes).

### Summary

A handful of features have been added and a number of bugs fixed since the 4.11.2 release. Our focus has been on xTupleCommerce infrastructure and enhancing the capabilities of CRM.

Of particular interst are the following:

- Problems opening CRM accounts, opportunities, projects, etc. using the widget menu (▼) have been fixed
- The effects of changing shared addresses have been clarified, which should simplify CRM usage
- A number of bug fixes and feature work were contributed by the community members named above. Thank you!

### Features

- Features issue #[31441](http://www.xtuple.org/xtincident/view/bugs/31441) _Add MIME type information for the File to the file table_
- Features issue #[32100](http://www.xtuple.org/xtincident/view/bugs/32100) _Prodiem Stage Question - Need clarification about Account Warnings and Credit Limits_
- Features issue #[32568](http://www.xtuple.org/xtincident/view/bugs/32568) _New Artina Check Format_

### Bug fixes
- Fixed issue #[26163](http://www.xtuple.org/xtincident/view/bugs/26163) _Unable to add line items to a transfer order from Quick Entry tab_
- Fixed issue #[27306](http://www.xtuple.org/xtincident/view/bugs/27306) _Credit card Cash Receipt half-fails when Accounting Period isn't defined, then fake posts_
- Fixed issue #[29071](http://www.xtuple.org/xtincident/view/bugs/29071) _fixSerial Cannot access temporary tables of other sessions_
- Fixed issue #[29181](http://www.xtuple.org/xtincident/view/bugs/29181) _CRM -- error in Merge Accounts_
- Fixed issue #[29747](http://www.xtuple.org/xtincident/view/bugs/29747) _sales order line item quantity is updated though the line item quantity changes are not saved on Sales Order screen._
- Fixed issue #[30309](http://www.xtuple.org/xtincident/view/bugs/30309) _Purchases clearing incorrect posting on voucher_
- Fixed issue #[30464](http://www.xtuple.org/xtincident/view/bugs/30464) _‘Processing Errors’ dialog is displayed while creating recurring items for Incidents._
- Fixed issue #[30694](http://www.xtuple.org/xtincident/view/bugs/30694) _CRM -- Emphasize the scale of impact when applying address changes ""to all""_
- Fixed issue #[30893](http://www.xtuple.org/xtincident/view/bugs/30893) _api.site view \_INSERT rule attempts invalid coalesce on tax_zone field_
- Fixed issue #[31676](http://www.xtuple.org/xtincident/view/bugs/31676) _script toolbox and a number of qt constants, enums, and flags are not exposed to widget scripting_
- Fixed issue #[31721](http://www.xtuple.org/xtincident/view/bugs/31721) _Unable to create ‘Invoice Item Characteristics’ in Invoice Item screen while creating new Misc. invoice_
- Fixed issue #[31733](http://www.xtuple.org/xtincident/view/bugs/31733) _Completed tasks are still visible in task list_
- Fixed issue #[31761](http://www.xtuple.org/xtincident/view/bugs/31761) _‘Update’ button functionality is not working in ‘Forward Update Accounts’ screen._
- Fixed issue #[31822](http://www.xtuple.org/xtincident/view/bugs/31822) _‘Error Retrieving Information’  is displayed while fetching the records for default filter as ‘Lot Sale’ characterstic type._
- Fixed issue #[31834](http://www.xtuple.org/xtincident/view/bugs/31834) _New quote is created without shipTo selected even shipTo is set in the session_
- Fixed issue #[31879](http://www.xtuple.org/xtincident/view/bugs/31879) _‘Error deleting group’ dialog is displayed on clicking upon ‘Cancel’ button and roles are created in 'List Roles' screen._
- Fixed issue #[31915](http://www.xtuple.org/xtincident/view/bugs/31915) _Unposted Cash Receipt from Declined CC Transaction_
- Fixed issue #[31916](http://www.xtuple.org/xtincident/view/bugs/31916) _User is able to add comments under ‘ Remarks’ tab of ‘Item Master’ tab in ‘Item Availability Workbench’ screen._
- Fixed issue #[31922](http://www.xtuple.org/xtincident/view/bugs/31922) _catCostList screen has Byte Mark in 4.11.2_
- Fixed issue #[31936](http://www.xtuple.org/xtincident/view/bugs/31936) _A/P History on Vendor workbench shows history from all vendors_
- Fixed issue #[31946](http://www.xtuple.org/xtincident/view/bugs/31946) _‘Prod. Cat.’ column values starting text is missing in Preview mode of ‘Capacity UOMs by Product Category’ screen_
- Fixed issue #[31967](http://www.xtuple.org/xtincident/view/bugs/31967) _To-Do Item alarm functionality is not working_
- Fixed issue #[31993](http://www.xtuple.org/xtincident/view/bugs/31993) _‘Sales Order’ & ‘Quote’ windows are displayed without window titles and window size is not fit to the screen._
- Fixed issue #[31996](http://www.xtuple.org/xtincident/view/bugs/31996) _While closing a new account without saving, ‘Error deleting the initial Account record’ error is being displayed._
- Fixed issue #[32011](http://www.xtuple.org/xtincident/view/bugs/32011) _Opportunities - Cannot attach Prospect Quotes_
- Fixed issue #[32022](http://www.xtuple.org/xtincident/view/bugs/32022) _View Item Master_
- Fixed issue #[32037](http://www.xtuple.org/xtincident/view/bugs/32037) _‘Contact’ filter functionality is not working in ‘Projects’ screen._
- Fixed issue #[32054](http://www.xtuple.org/xtincident/view/bugs/32054) _Account combo box in Contact screen isn't functioning (4.11.2 testing)_
- Fixed issue #[32116](http://www.xtuple.org/xtincident/view/bugs/32116) _buildinvbal() excludes transactions on the last day of the month_
- Fixed issue #[32121](http://www.xtuple.org/xtincident/view/bugs/32121) _Bank rec do not clear tax_
- Fixed issue #[32135](http://www.xtuple.org/xtincident/view/bugs/32135) _Credit in closed period_
- Fixed issue #[32177](http://www.xtuple.org/xtincident/view/bugs/32177) _Testing DF 4.11.2 - right click account and click open - not opening window_
- Fixed issue #[32190](http://www.xtuple.org/xtincident/view/bugs/32190) _SO that exceeds credit limit should save on credit hold_
- Fixed issue #[32265](http://www.xtuple.org/xtincident/view/bugs/32265) _Quote displays wrong information when opened by two people_
- Fixed issue #[32297](http://www.xtuple.org/xtincident/view/bugs/32297) _Need metric for default freeform billto in core_
- Fixed issue #[32320](http://www.xtuple.org/xtincident/view/bugs/32320) _Current Purchase Order item quantity value is not displayed in ‘Change P/O Item Quantity’ window._
- Fixed issue #[32351](http://www.xtuple.org/xtincident/view/bugs/32351) _error deleting contact_
- Fixed issue #[32468](http://www.xtuple.org/xtincident/view/bugs/32468) _New CRM locks aren't working properly_
- Fixed issue #[32496](http://www.xtuple.org/xtincident/view/bugs/32496) _mfg script for item list_
- Fixed issue #[32526](http://www.xtuple.org/xtincident/view/bugs/32526) _Voiding of Cash Receipt/Customer Deposit Yields Unbalanced/Incorrect Ledger Transactions_
- Fixed issue #[32534](http://www.xtuple.org/xtincident/view/bugs/32534) _Entering new PostBooks License Key at ""Expired Key"" Login pop-up does not also update database_
- Fixed issue #[32550](http://www.xtuple.org/xtincident/view/bugs/32550) _`ccbank_ccbank_ccard_type_check` prevents upgrades once `B` for ACH Bank Account is added_
- Fixed issue #[32629](http://www.xtuple.org/xtincident/view/bugs/32629) _Process/Locks Manager not nesting properly_



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

### Features added in 4.11.3

- Features issue #[?????](http://www.xtuple.org/xtincident/view/bugs/?????) _?????_

### Bug fixes in 4.11.3

- Fixed issue #[??????](http://www.xtuple.org/xtincident/view/bugs/??????) _??????_

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
