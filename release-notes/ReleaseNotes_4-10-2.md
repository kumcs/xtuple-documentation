# xTuple Release Notes

## Version 4.10.2 - August, 2017

These are the release notes for the 4.10.2 xTuple ERP patch release.
Thanks to all who contributed to make this release possible. See below for more information about
[deploying this release](#deployment-notes).

### Summary

A number of bugs have been fixed since the 4.10.1 release.

**Note:** You will need PostgreSQL 9.3, 9.4, 9.5, or 9.6 to use this release,
with the following two PostgreSQL extensions:

- plv8 -
  See our
  [github wiki](https://github.com/xtuple/xtuple/wiki/Installing-PLv8) for
  more information on how to install plv8 and a
  [blog post](https://www.xtuple.org/blog/gmoskowitz/enabling-technologies-plv8-49)
  describing plv8 and why we introduced this dependency.
- ossp-uuid -
  If you built PostgreSQL from source code, might have to
  rebuild it. Make sure to include the `--with-ossp-uuid` option for
  the `configure` command. See
  [our instructions for building PostgreSQL](https://github.com/xtuple/qt-client/wiki/Desktop-Development-Environment-Setup#get-and-install-postgresql)
  for details.

These need to be installed on the database server, not client machines.


### Bug fixes

- Fixed issue #[24452](http://www.xtuple.org/xtincident/view/bugs/24452) _Display widget parameters vulnerable to SQL Injection_
- Fixed issue #[29027](http://www.xtuple.org/xtincident/view/bugs/29027) _'Item group' screen is displayed behind 'List Item Groups' screen when opened from 'Inventory Buffer Status by Item Group scree_
- Fixed issue #[29216](http://www.xtuple.org/xtincident/view/bugs/29216) _Bug in copyproject PL/pgSQL function causes failure on copying project_
- Fixed issue #[29304](http://www.xtuple.org/xtincident/view/bugs/29304) _Packing List Batch allows the addition of orders that do not display_
- Fixed issue #[29384](http://www.xtuple.org/xtincident/view/bugs/29384) _Application is crashed on clicking cancel button in 'Sales Order' screen_
- Fixed issue #[29385](http://www.xtuple.org/xtincident/view/bugs/29385) _Omnibus: Filters are disappeared when minimizing and maximizing 'Quantities on Hand' screen._
- Fixed issue #[29391](http://www.xtuple.org/xtincident/view/bugs/29391) _divide by 0 error in Slow Moving Inventory By Classcode metasql for 0 qoh_
- Fixed issue #[29510](http://www.xtuple.org/xtincident/view/bugs/29510) _Editing Discount on Credit Memo Apply changes apply amount_
- Fixed issue #[29512](http://www.xtuple.org/xtincident/view/bugs/29512) _Parameter Widget Saved filters are not remembered_
- Fixed issue #[29720](http://www.xtuple.org/xtincident/view/bugs/29720) _""Update Inventory"" checkbox on Credit Memo item ignores interfaceToGL metric_
- Fixed issue #[29796](http://www.xtuple.org/xtincident/view/bugs/29796) _Multiple Qty to Reserve popups on manually reserving multiple Lot/Location inventory_
- Fixed issue #[29885](http://www.xtuple.org/xtincident/view/bugs/29885) _Aging report wrong_
- Fixed issue #[29907](http://www.xtuple.org/xtincident/view/bugs/29907) _Wrong Check Number Printed and Updated_
- Fixed issue #[29938](http://www.xtuple.org/xtincident/view/bugs/29938) _Display won't open on Windows if a script adds a large amount of options to the parameter widget_
- Fixed issue #[30008](http://www.xtuple.org/xtincident/view/bugs/30008) _Incorrectly assign owner to vendor when usernames are close_
- Fixed issue #[30114](http://www.xtuple.org/xtincident/view/bugs/30114) _Error posting cash receipts_
- Fixed issue #[30134](http://www.xtuple.org/xtincident/view/bugs/30134) _Issue to Ship Line Item Right Click Menu Shows Reservation Items for Transfer Orders_
- Fixed issue #[30183](http://www.xtuple.org/xtincident/view/bugs/30183) _npm install failes with npm ERR! 404 'types/node' is not in the npm registry._
- Fixed issue #[30230](http://www.xtuple.org/xtincident/view/bugs/30230) _report design won't open_
- Fixed issue #[30237](http://www.xtuple.org/xtincident/view/bugs/30237) _411B List Price Not Recorded in ERP When Price Schedule Discount is Applied to List Price_
- Fixed issue #[30252](http://www.xtuple.org/xtincident/view/bugs/30252) _Price Schedules linked to exclusive items do not calculate price_
- Fixed issue #[30363](http://www.xtuple.org/xtincident/view/bugs/30363) _Documents attached to vouchers missing_
- Fixed issue #[30547](http://www.xtuple.org/xtincident/view/bugs/30547) _411 Main Top Menu Window Sector Fails_
- Fixed issue #[30606](http://www.xtuple.org/xtincident/view/bugs/30606) _4.11.0RC: Missing Triangle Expansion In Cash Receipts TAB_
- Fixed issue #[30700](http://www.xtuple.org/xtincident/view/bugs/30700) _SQL attached to add missing charuse rows for configured items_


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
Assets, remain on their own release schedules and should
be installed as before.
