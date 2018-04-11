### xTuple Release Notes
##### Version 4.8.1 Patch Release * January 23, 2015

These are the release notes for the 4.8.1 Final Release. Thanks to all who contributed to make this release possible.
For more information about [deploying this release](#deployment-notes), please see below.

### Features and bug fixes

The following features and bug fixes have been added to the application since the 4.8.0 release.
Additional detail for each item listed below may be found on our [community website](http://www.xtuple.org).


##### Desktop Application

 - Fixed
   issue #[21298](http://www.xtuple.org/xtincident/view/bugs/21298)
   _Project List Report: Project Type displays Undefined when 'MaintainProjectTypes' privilege is not assigned_
 - Fixed
   issue #[23639](http://www.xtuple.org/xtincident/view/bugs/23639)
   _Barcode scanning into Post Operation screen_
 - Fixed
   issue #[24953](http://www.xtuple.org/xtincident/view/bugs/24953)
   _*xtuple 470 issue: vendor search columns not displaying main address values_
 - Fixed
   issue #[25124](http://www.xtuple.org/xtincident/view/bugs/25124)
   _*Unknown Debit Memos are displaying on our Checks_
 - Fixed
   issue #[25163](http://www.xtuple.org/xtincident/view/bugs/25163)
   _Print payment screen not functional_
 - Fixed
   issue #[25186](http://www.xtuple.org/xtincident/view/bugs/25186)
   _*W/O History Lost_
 - Fixed
   issue #[25199](http://www.xtuple.org/xtincident/view/bugs/25199)
   _Work Order returns of Lot Controlled items_
 - Fixed
   issue #[25206](http://www.xtuple.org/xtincident/view/bugs/25206)
   _*Can't reconcile payments_
 - Fixed
   issue #[25218](http://www.xtuple.org/xtincident/view/bugs/25218)
   _Standard Journal Entry Notes Not Saved_
 - Fixed
   issue #[25266](http://www.xtuple.org/xtincident/view/bugs/25266)
   _*Deleting a Count Tag deletes QOH of item_
 - Fixed
   issue #[25300](http://www.xtuple.org/xtincident/view/bugs/25300)
   _* DB log error is generated on selecting to query 'Vendors' screen_
 - Fixed
   issue #[25301](http://www.xtuple.org/xtincident/view/bugs/25301)
   _*'Processing Error' dialog is displayed on selecting to close a Work Order from 'Post Production' screen_

   ### Deployment Notes

We've lately revised the
naming conventions and the behavior of our core updater packages.
Our overall goal is to simplify the process of installing and
upgrading xTuple ERP databases.

Just as was true for the 4.4.1 release, you will only need to apply
one updater package to upgrade to 4.8.1--that is, assuming you are
already running on at least 4.4.0. The new updater packages are
designed to bring you all the way up to their version, no matter
what version (>= 4.4.0!) that you're on.

In 4.5.0 we went a step further: not only will a single package take
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

    postbooks-upgrade-481.gz will:
    upgrade a PostBooks database from anywhere >= 4.4.0 to 4.8.1

    manufacturing-upgrade-481.gz will:
    upgrade the standard/dist (i.e., inventory code) to 4.8.1
    upgrade the manufacturing code to 4.8.1

    manufacturing-install-481.gz will:
    do a one-time install of tables, etc. for standard (i.e., inventory code) at 4.8.1
    upgrade the standard/dist (i.e., inventory code) to 4.8.1
    do a one-time install of tables, etc. for manufacturing at 4.8.1
    upgrade the manufacturing code to 4.8.1

    distribution-upgrade-481.gz will:
    upgrade the standard/ist (i.e., inventory code) to 4.8.1
    upgrade the distribution (i.e., xwd code) to 4.8.1

    distribution-install-481.gz will:
    do a one-time install of tables, etc. for standard (i.e., inventory code) at 4.8.1
    upgrade the standard/dist (i.e., inventory code) to 4.8.1
    do a one-time install of tables etc for distribution at 4.8.1
    upgrade the distribution (i.e., xwd code) to 4.8.1

PLEASE NOTE: Other packages, such as Advanced Commissions and Fixed
Assets, are currently remaining on their own release schedule and should
be installed as before.
