Release Notes
xTuple ERP
Version 4.5.1
June 30, 2014
----------------------------------

These are the release notes for the 4.5.1 Patch Release. Thanks
to all who contributed to make this release possible.

With the release of 4.5.1, we continue the process of revising the
naming conventions and the behavior of our core updater packages.
Our overall goal is to simplify the process of installing and
upgrading xTuple ERP databases.

Just as was true for the 4.4.1 release, you will only need to apply
one updater package to upgrade to 4.5.1--that is, assuming you are
already running on at least 4.4.0. The new updater packages are
designed to bring you all the way up to their version, no matter 
what version (>= 4.4.0!) that you're on.

In 4.5.0 we've gone a step further: not only will a single package take
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

postbooks-upgrade-451.gz will:
upgrade a PostBooks database from anywhere >= 4.4.0 to 4.5.1

manufacturing-upgrade-451.gz will:
upgrade the standard/dist (i.e., inventory code) to 4.5.1
upgrade the manufacturing code to 4.5.1

manufacturing-install-451.gz will:
requires a PostBooks edition database >= 4.4.0
do a one-time install of tables, etc. for standard (i.e., inventory code) at 4.5.1
upgrade the standard/dist (i.e., inventory code) to 4.5.1
do a one-time install of tables, etc. for manufacturing at 4.5.1
upgrade the manufacturing code to 4.5.1

distribution-upgrade-451.gz will:
requires xwd package installed and at version >= 2.4.0
upgrade the standard/ist (i.e., inventory code) to 4.5.1
upgrade the distribution (i.e., xwd code) to 4.5.1

distribution-install-451.gz will:
requires a PostBooks edition database >= 4.4.0
do a one-time install of tables, etc. for standard (i.e., inventory code) at 4.5.1
upgrade the standard/dist (i.e., inventory code) to 4.5.1
do a one-time install of tables etc for distribution at 4.5.1
upgrade the distribution (i.e., xwd code) to 4.5.1

PLEASE NOTE: Other packages, such as Advanced Commissions and Fixed 
Assets, are currently remaining on their own release schedule and should 
be installed as before.

As always, please review the xTuple Compatibility Matrix before
upgrading: http://www.xtuple.org/compatibility-matrix.

----------------------------------

The following features and bug fixes have been added to the
applications since the 4.5.0 release. Additional detail for
each item listed below may be found on our community
website (www.xtuple.org).

Features:

* Authorize.net Test server using incorrect URL [13748]
* Update of pricing schedules [22824]
* Allow capture of credit card charges from external pre-authorized 
sources [23937]

Bug Fixes:

* Financial Report Writer is very slow [7155]
* App-based help files not being updated [20210]
* Observation: "Reason" list is not available on "Lost Sale" screen 
for the cancellation of a sales  order line item [20422]
* Item Costs by Class Code report showing inactive items [21570]
* Project Type filter not working in desktop client [23223]
* Selecting to view in-active Bill of Material Item displays blank 
"Item Number" field [23487]
* Bill To Infromation on Prospect Quote cannot edited [23534]
* Correcting receiving can leave value and no QOH [23658]
* Item Label printing with the wrong alias [23811]
* Voiding posted CR of type Visa didn't take money out of checking 
acct [23829]
* importpricesvc function [23839]
* Qty on Hand shows inaccurate total quantities in the Advanced Item 
Search [23843]
* Customer Favorites are not accessible from a Quote [23845]
* Cash Effective date out of range [23861]
* Date filter does not work on "Lost Sales" screen [23892]
* Bank Reconciliation Calculation Problem [23903]
* Margin Issues in 4.5 [23920]
* Project activity subform not nesting properly for quotes [23958]
* Incident can not be created from project view [23959]
* Can add inactive item to order using Quick Item Entry [23961]
* Copy Item BOM Quantity Per cannot go below 1.00 [23973]
* DB log error is generated on selecting to "Save" credit card setup 
[23976]
* Error when printing financial reports [24005]


