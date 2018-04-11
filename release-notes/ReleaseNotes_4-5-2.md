Release Notes
xTuple ERP
Version 4.5.2
July 16, 2014
----------------------------------

These are the release notes for the 4.5.2 Patch Release. Thanks
to all who contributed to make this release possible.

With the release of 4.5.2, we continue the process of revising the
naming conventions and the behavior of our core updater packages.
Our overall goal is to simplify the process of installing and
upgrading xTuple ERP databases.

Just as was true for the 4.4.1 release, you will only need to apply
one updater package to upgrade to 4.5.2--that is, assuming you are
already running on at least 4.4.0. The new updater packages are
designed to bring you all the way up to their version, no matter
what version (>= 4.4.0!) that you're on.

In 4.5.0+ we've gone a step further: not only will a single package take
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

postbooks-upgrade-452.gz will:
upgrade a PostBooks database from anywhere >= 4.4.0 to 4.5.2

manufacturing-upgrade-452.gz will:
upgrade the standard/dist (i.e., inventory code) to 4.5.2
upgrade the manufacturing code to 4.5.2

manufacturing-install-452.gz will:
requires a PostBooks edition database >= 4.4.0
do a one-time install of tables, etc. for standard (i.e., inventory code) at 4.5.2
upgrade the standard/dist (i.e., inventory code) to 4.5.2
do a one-time install of tables, etc. for manufacturing at 4.5.2
upgrade the manufacturing code to 4.5.2

distribution-upgrade-452.gz will:
requires xwd package installed and at version >= 2.4.0
upgrade the standard/ist (i.e., inventory code) to 4.5.2
upgrade the distribution (i.e., xwd code) to 4.5.2

distribution-install-452.gz will:
requires a PostBooks edition database >= 4.4.0
do a one-time install of tables, etc. for standard (i.e., inventory code) at 4.5.2
upgrade the standard/dist (i.e., inventory code) to 4.5.2
do a one-time install of tables etc for distribution at 4.5.2
upgrade the distribution (i.e., xwd code) to 4.5.2

PLEASE NOTE: Other packages, such as Advanced Commissions and Fixed
Assets, are currently remaining on their own release schedule and should
be installed as before.

As always, please review the xTuple Compatibility Matrix before
upgrading: http://www.xtuple.org/compatibility-matrix.

----------------------------------

The following features and bug fixes have been added to the
applications since the 4.5.1 release. Additional detail for
each item listed below may be found on our community
website (www.xtuple.org).


Bug Fixes:

* Contract window throws dialog related connection errors [24033]
* Can Sub out Issued Items in W/O [24028]


