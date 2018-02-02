
# xTuple Release Notes

## Version 4.11.3 - ?????, 2018

These are the release notes for the 4.11.3 xTuple ERP release.
Thanks to all who contributed to make this release possible,
including Cordeck Building Solutions, Alfredo Martinez,
and Scott Zuke.
See below for more information about
[deploying this release](#deployment-notes).

### Summary

A handful of features have been added and a number of bugs fixed since the 4.11.2 release. Our focus has been on xTupleCommerce infrastructure and enhancing the capabilities of CRM.

Of particular interest are the following:

- ???


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
