# xTuple Release Notes
## Version 4.9.2 * October, 2015

These are the release notes for the 4.9.2 xTuple ERP release.  Thanks
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

The xTuple ERP 4.9.2 release fixes a number of bugs in the xTuple ERP desktop
application.

#### Desktop Application
- Fixed
  issue #[26190](http://www.xtuple.org/xtincident/view/bugs/26190)
  _Cannot create new Fiscal Periods_
- Implemented
  issue #[26434](http://www.xtuple.org/xtincident/view/bugs/26434)
  _Authorize.Net Networking Change_
- Fixed
  issue #[26436](http://www.xtuple.org/xtincident/view/bugs/26436)
  _Authorize.net complaint During CC processing_
- Fixed
  issue #[26463](http://www.xtuple.org/xtincident/view/bugs/26463)
  _*Ship Order Screen Check Boxes_
- Fixed
  issue #[26513](http://www.xtuple.org/xtincident/view/bugs/26513)
  _Error converting quote in 4.9.1_
- Fixed
  issue #[26539](http://www.xtuple.org/xtincident/view/bugs/26539)
  _4.9.1 - Can't convert Propects to Customers_
- Fixed
  issue #[26552](http://www.xtuple.org/xtincident/view/bugs/26552)
  _New Project Opens with data_
- Fixed
  issue #[26588](http://www.xtuple.org/xtincident/view/bugs/26588)
  _xTuple Windows client performance (replaces #26561)_
- Fixed
  issue #[26601](http://www.xtuple.org/xtincident/view/bugs/26601)
  _*Fatal error on createLotSerial Screen (replaces #26560)_
- Fixed
  issue #[26610](http://www.xtuple.org/xtincident/view/bugs/26610)
  _*UOM Conversion error on Quote items_
- Fixed
  issue #[26623](http://www.xtuple.org/xtincident/view/bugs/26623)
  _490 Pop Up Warning CVV issue (replaces #26515)_

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
