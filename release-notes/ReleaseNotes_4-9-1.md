# xTuple Release Notes
## Version 4.9.1 * September, 2015

These are the release notes for the 4.9.1 xTuple ERP release.  Thanks
to all who contributed to make this release possible.  For more
information about [deploying this release](#deployment-notes),
please see below.

**Note:** You will need the plv8 extension to PostgreSQL to upgrade
and use this release.  See our
[github wiki](https://github.com/xtuple/xtuple/wiki/Installing-PLv8) for
more information on how to install plv8 and a
[blog post](https://www.xtuple.org/blog/gmoskowitz/enabling-technologies-plv8-49)
describing plv8 and why we introduced this new dependency.

### Bug fixes

The xTuple ERP 4.9.1 release fixes a number of bugs in the xTuple ERP desktop
application.

#### Desktop Application

- Fixed
  issue #[22850](http://www.xtuple.org/xtincident/view/bugs/22850)
  _Mac 4.3 Nav Issue - Right Clicking on docked icon no longer shows open windows_
- Fixed
  issue #[24866](http://www.xtuple.org/xtincident/view/bugs/24866)
  _Lot/Serial Document Links not visible on linked Document_
- Fixed
  issue #[24926](http://www.xtuple.org/xtincident/view/bugs/24926)
  _desktop extensions should not set search_path_
- Fixed
  issue #[25286](http://www.xtuple.org/xtincident/view/bugs/25286)
  _*Make system messages non-modal_
- Fixed
  issue #[25561](http://www.xtuple.org/xtincident/view/bugs/25561)
  _*Routing revision not working_
- Fixed
  issue #[25656](http://www.xtuple.org/xtincident/view/bugs/25656)
  _there are at least two different potype tables_
- Fixed
  issue #[25706](http://www.xtuple.org/xtincident/view/bugs/25706)
  _apply applock class to ordercluster_
- Fixed
  issue #[25723](http://www.xtuple.org/xtincident/view/bugs/25723)
  _*itemipsprice function does not accommodate legacy data properly_
- Fixed
  issue #[25815](http://www.xtuple.org/xtincident/view/bugs/25815)
  _*AR- Discount cause out of balance_
- Fixed
  issue #[25898](http://www.xtuple.org/xtincident/view/bugs/25898)
  _Error when saving quick entries_
- Fixed
  issue #[25928](http://www.xtuple.org/xtincident/view/bugs/25928)
  _Opening a Purchase Order from Open Purchase Orders list slow_
- Fixed
  issue #[25934](http://www.xtuple.org/xtincident/view/bugs/25934)
  _*Cash Receipt Funds Type_
- Fixed
  issue #[26048](http://www.xtuple.org/xtincident/view/bugs/26048)
  _Edit URL Document Association brings up Empty File edit window_
- Fixed
  issue #[26130](http://www.xtuple.org/xtincident/view/bugs/26130)
  _PR in sales order entry_
- Fixed
  issue #[26148](http://www.xtuple.org/xtincident/view/bugs/26148)
  _*Purchase Order line items do not display until the entry screen is closed_
- Fixed
  issue #[26191](http://www.xtuple.org/xtincident/view/bugs/26191)
  _Error when applying Credits in Payables Workbench_
- Fixed
  issue #[26212](http://www.xtuple.org/xtincident/view/bugs/26212)
  _*Char setup screen_
- Fixed
  issue #[26229](http://www.xtuple.org/xtincident/view/bugs/26229)
  _*ShipTo Name field issue_
- Fixed
  issue #[26230](http://www.xtuple.org/xtincident/view/bugs/26230)
  _*getSoScheddate function_
- Fixed
  issue #[26247](http://www.xtuple.org/xtincident/view/bugs/26247)
  _Transfer Orders have no Returned Qty - overstates Shipped Qty_
- Fixed
  issue #[26258](http://www.xtuple.org/xtincident/view/bugs/26258)
  _*Customer Workbench_
- Fixed
  issue #[26266](http://www.xtuple.org/xtincident/view/bugs/26266)
  _481 to 490 Upgrade Breaks CRM Account Characteristics_
- Fixed
  issue #[26269](http://www.xtuple.org/xtincident/view/bugs/26269)
  _4.9.0 User Interface (UI) Issues_
- Fixed
  issue #[26277](http://www.xtuple.org/xtincident/view/bugs/26277)
  _Item number on an invoice can be changed even when related to a shipment._
- Fixed
  issue #[26279](http://www.xtuple.org/xtincident/view/bugs/26279)
  _New document associations disabled_
- Fixed
  issue #[26283](http://www.xtuple.org/xtincident/view/bugs/26283)
  _*Scrap on WO Screen_
- Fixed
  issue #[26302](http://www.xtuple.org/xtincident/view/bugs/26302)
  _Cannot create new comment type_
- Fixed
  issue #[26313](http://www.xtuple.org/xtincident/view/bugs/26313)
  _*Files attached to sales orders "missing" after upgrade_
- Fixed
  issue #[26319](http://www.xtuple.org/xtincident/view/bugs/26319)
  _Purchase Order does not honour Item Site Can Purchase setting_
- Fixed
  issue #[26338](http://www.xtuple.org/xtincident/view/bugs/26338)
  _Incorrect Outstanding Balance displayed on Invoices when Credit Allocated_
- Fixed
  issue #[26431](http://www.xtuple.org/xtincident/view/bugs/26431)
  _*Unable to attach Docs to Closed SOs_

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
