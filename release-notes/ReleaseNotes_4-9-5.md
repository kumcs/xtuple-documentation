# xTuple Release Notes
## Version 4.9.5 - April, 2016

These are the release notes for the 4.9.5 xTuple ERP release.
Thanks to all who contributed to make this release possible.
For more information about [deploying this release](#deployment-notes),
please see below.

**Note:** You will need the plv8 extension to PostgreSQL to upgrade
and use this release.  See our
[github wiki](https://github.com/xtuple/xtuple/wiki/Installing-PLv8) for
more information on how to install plv8 and a
[blog post](https://www.xtuple.org/blog/gmoskowitz/enabling-technologies-plv8-49)
describing plv8 and why we introduced this new dependency.

### Feature
- Implemented in REST API
  _Add dispatch function/service to save credit cards over the REST API._

### Bug fixes

The xTuple ERP 4.9.5 release fixes a few bugs in the xTuple ERP desktop
application. In addition there are minor changes to the REST API to
support upcoming xTupleCommerce changes.

- Fixed
  issue #[26654](http://www.xtuple.org/xtincident/view/bugs/26654) _User is not able to select 'Project Types' in Project screen_
- Fixed
  issue #[27434](http://www.xtuple.org/xtincident/view/bugs/27434) _ACH block count incorrect_
- Fixed
  issue #[27643](http://www.xtuple.org/xtincident/view/bugs/27643) _Authorize.net transaction ID issue_
- Fixed
  issue #[27728](http://www.xtuple.org/xtincident/view/bugs/27728) _project Type is not populating when Project window opened_
- Fixed
  issue #[27840](http://www.xtuple.org/xtincident/view/bugs/27840) _Attached incident appears to be duplicate but isn't_
- Fixed in REST API
  _Remove shipto_id requirement from favorites._


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

    postbooks-upgrade-495.gz will:
    upgrade a PostBooks database from anywhere >= 4.4.0 to 4.9.5

    distribution-upgrade-495.gz will:
    upgrade the standard/dist (i.e., inventory code) to 4.9.5
    upgrade the distribution (i.e., xwd code) to 4.9.5

    distribution-install-495.gz will:
    do a one-time install of tables, etc. for standard (i.e., inventory code) at 4.9.5
    do a one-time install of tables, etc. for distribution at 4.9.5

    manufacturing-upgrade-495.gz will:
    upgrade the standard/dist (i.e., inventory code) to 4.9.5
    upgrade the manufacturing code to 4.9.5

    manufacturing-install-495.gz will:
    do a one-time install of tables, etc. for standard (i.e., inventory code) at 4.9.5
    do a one-time install of tables, etc. for manufacturing at 4.9.5

    enterprise-upgrade-495.gz will:
    upgrade the standard/dist (i.e., inventory code) to 4.9.5
    upgrade the distribution (i.e., xwd code) to 4.9.5
    upgrade the manufacturing code to 4.9.5

    enterprise-install-495.gz will:
    do a one-time install of tables, etc. for standard (i.e., inventory code) at 4.9.5
    do a one-time install of tables, etc. for distribution at 4.9.5
    do a one-time install of tables, etc. for manufacturing at 4.9.5

PLEASE NOTE: Other packages, such as Advanced Commissions and Fixed
Assets, are currently remaining on their own release schedule and should
be installed as before.
