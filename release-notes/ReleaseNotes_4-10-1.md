# xTuple Release Notes

## Version 4.10.1 - March, 2017

These are the release notes for the 4.10.1 xTupl ERP release.
Thanks to all who contributed to make this release possible. See below for more information about
[deploying this release](#deployment-notes).

### Summary

A number of bugs have been fixed since the 4.10.0 release.

**Note:** You will need PostgreSQL 9.3, 9.4, or 9.5 to use this release,
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


### Bug fixes

- Addressed issue #[29190](http://www.xtuple.org/xtincident/view/bugs/29190) _Update key in PostBooks databases_
- Addressed issue #[27709](http://www.xtuple.org/xtincident/view/bugs/27709) _Altering Customer Number in ERP when account is created by xTupleCommerce_
- Fixed issue #[23812](http://www.xtuple.org/xtincident/view/bugs/23812) _Customer P/Ns copying incorrectly from Adv Item Search to Order/Quote_
- Fixed issue #[27450](http://www.xtuple.org/xtincident/view/bugs/27450) _'Select Number' dialog is displayed in Vendor WorkBench screen irrelevantly_
- Fixed issue #[27705](http://www.xtuple.org/xtincident/view/bugs/27705) _Possible confusion over where characteristics can be used_
- Fixed issue #[27812](http://www.xtuple.org/xtincident/view/bugs/27812) _Qt5 Lin/Win client windows open with banner off screen_
- Fixed issue #[28597](http://www.xtuple.org/xtincident/view/bugs/28597) _Error AP Credit Memo application_
- Fixed issue #[28627](http://www.xtuple.org/xtincident/view/bugs/28627) _“Ship Via” field on vendors isn't a dropdown_
- Fixed issue #[28653](http://www.xtuple.org/xtincident/view/bugs/28653) _Validation of BOM screen occurring during ""Cancel""_
- Fixed issue #[28746](http://www.xtuple.org/xtincident/view/bugs/28746) _Cannot issue material batch to WO_
- Fixed issue #[28800](http://www.xtuple.org/xtincident/view/bugs/28800) _Lot Serial Characteristics Issue_
- Fixed issue #[28839](http://www.xtuple.org/xtincident/view/bugs/28839) _Sub. type code displaying incorrect value on COA_
- Fixed issue #[28868](http://www.xtuple.org/xtincident/view/bugs/28868) _Cash receipt in differing currency does not work correctly_
- Fixed issue #[28899](http://www.xtuple.org/xtincident/view/bugs/28899) _Able to select Standard cost although turned off in Inventory Setup_
- Fixed issue #[28903](http://www.xtuple.org/xtincident/view/bugs/28903) _Workflow activities not displayed in 'Workflow Activities' screen for purchase order when it is released at time of creation_
- Fixed issue #[28905](http://www.xtuple.org/xtincident/view/bugs/28905) _'Cannot save work order' dialog is displayed while trying to open any work order which has priority set to other than '1'._
- Fixed issue #[28906](http://www.xtuple.org/xtincident/view/bugs/28906) _‘One or more items cant be issued due to insufficient inventory’ dialog is displayed on issuing materials with enough QoH_
- Fixed issue #[28907](http://www.xtuple.org/xtincident/view/bugs/28907) _Able to issue materials even though QOH of the regular type item is zero._
- Fixed issue #[28908](http://www.xtuple.org/xtincident/view/bugs/28908) _No warning message is displayed when issuing average costing item having qoh as zero._
- Fixed issue #[28952](http://www.xtuple.org/xtincident/view/bugs/28952) _Mac version of 4.10.0 final desktop client is unsigned_
- Fixed issue #[29022](http://www.xtuple.org/xtincident/view/bugs/29022) _“On Order” item availability is incorrect when creating a new SO line_
- Fixed issue #[29058](http://www.xtuple.org/xtincident/view/bugs/29058) _Checks not printing after 4.10 upgrade_
- Fixed issue #[29076](http://www.xtuple.org/xtincident/view/bugs/29076) _Item characteristics duplicated when quote converted_
- Fixed issue #[29137](http://www.xtuple.org/xtincident/view/bugs/29137) _Reports defs' grade > 0 for core report def aftern migration and in ref DB_
- Fixed issue #[29173](http://www.xtuple.org/xtincident/view/bugs/29173) _GL Transactions report_
- Fixed issue #[29226](http://www.xtuple.org/xtincident/view/bugs/29226) _Mistake on postcashreceipt function_
- Fixed issue #[29238](http://www.xtuple.org/xtincident/view/bugs/29238) _DB log error is displayed on editing a line item in 'Purchase Order' screen._
- Fixed issue #[29251](http://www.xtuple.org/xtincident/view/bugs/29251) _Credit Card Receipt error - decimal precision_
- Fixed issue #[29330](http://www.xtuple.org/xtincident/view/bugs/29330) _Ledger Control Values Incorrect_
- Fixed issue #[29358](http://www.xtuple.org/xtincident/view/bugs/29358) _pg_restore reports errors when refreshing xtdash materialized views_
- Fixed issue #[29361](http://www.xtuple.org/xtincident/view/bugs/29361) _Error Voiding an Invoice_
- Fixed issue #[29408](http://www.xtuple.org/xtincident/view/bugs/29408) _itemsite_value is not updated if standard cost is deleted._
- Fixed issue #[29444](http://www.xtuple.org/xtincident/view/bugs/29444) _Web-enabled Extensions cannot install the ""foundation-database/manifest.js""_
- Fixed issue #[29497](http://www.xtuple.org/xtincident/view/bugs/29497) _XT.Data.fetch default ORDER BY gets base table primary key column, not ORM view primary key column_
- Fixed issue #[29532](http://www.xtuple.org/xtincident/view/bugs/29532) _AR Memo Base Equ does not change_
- Fixed issue #[29550](http://www.xtuple.org/xtincident/view/bugs/29550) _Financial Report error_
- Fixed issue #[29619](http://www.xtuple.org/xtincident/view/bugs/29619) _xtdash Materialized Views dropped when updating database to 4.11.0Beta_
- Fixed issue #[29633](http://www.xtuple.org/xtincident/view/bugs/29633) _New MasterCard BIN_


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
