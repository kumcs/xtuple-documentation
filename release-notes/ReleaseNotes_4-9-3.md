# xTuple Release Notes
## Version 4.9.3 * February, 2016

These are the release notes for the 4.9.3 xTuple ERP release.  Thanks
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

The xTuple ERP 4.9.3 release fixes a number of bugs in the xTuple ERP desktop
application.

#### Desktop Application
- Fixed
  issue #[26190](http://www.xtuple.org/xtincident/view/bugs/26190)
  _Cannot create new Fiscal Periods_

- Fixed
  issue #[16636](http://www.xtuple.org/xtincident/view/bugs/16636)
  _*Selecting to 'View Transactions' for a Project account from Trial Balances screen displays irrelevant details_
- Fixed
  issue #[16649](http://www.xtuple.org/xtincident/view/bugs/16649)
  _License key loophole_
- Fixed
  issue #[25441](http://www.xtuple.org/xtincident/view/bugs/25441)
  _ItemSite API view is very slow_
- Fixed
  issue #[25576](http://www.xtuple.org/xtincident/view/bugs/25576)
  _*after database connection lost, desktop client must be restarted_
- Fixed
  issue #[25620](http://www.xtuple.org/xtincident/view/bugs/25620)
  _*poreject_recv_id not populated_
- Fixed
  issue #[25697](http://www.xtuple.org/xtincident/view/bugs/25697)
  _Login Screen Database Name Cursor Jumps_
- Fixed
  issue #[25698](http://www.xtuple.org/xtincident/view/bugs/25698)
  _*MAC QT5: Unable to close the WorkOrder_
- Fixed
  issue #[25919](http://www.xtuple.org/xtincident/view/bugs/25919)
  _*Can't search Vendor Item Number_
- Fixed
  issue #[25947](http://www.xtuple.org/xtincident/view/bugs/25947)
  _*Registration Key is not handled properly_
- Fixed
  issue #[26084](http://www.xtuple.org/xtincident/view/bugs/26084)
  _*Unable to attach a documents to a new Opportunity_
- Fixed
  issue #[26121](http://www.xtuple.org/xtincident/view/bugs/26121)
  _*Value column does not use locale in printed QOH Report_
- Fixed
  issue #[26228](http://www.xtuple.org/xtincident/view/bugs/26228)
  _there is no good way to install xtmfg into a distribution database_
- Fixed
  issue #[26334](http://www.xtuple.org/xtincident/view/bugs/26334)
  _License manager down_
- Fixed
  issue #[26376](http://www.xtuple.org/xtincident/view/bugs/26376)
  _*Unsaved Sales Order Line Items are being displayed under 'Line Items' tab of a Sales Order_
- Fixed
  issue #[26391](http://www.xtuple.org/xtincident/view/bugs/26391)
  _Document Assignment is orphaned if Sales Order is cancelled or deleted_
- Fixed
  issue #[26421](http://www.xtuple.org/xtincident/view/bugs/26421)
  _Netable calculation causing issues with MPS schedule_
- Fixed
  issue #[26437](http://www.xtuple.org/xtincident/view/bugs/26437)
  _*User is able to create a Sales order even after revoking 'Maintain sales order' privilege_
- Fixed
  issue #[26485](http://www.xtuple.org/xtincident/view/bugs/26485)
  _Able to change currency after Credit Memo has posted to the GL_
- Fixed
  issue #[26505](http://www.xtuple.org/xtincident/view/bugs/26505)
  _*4.9.0 Urgent Issue: Ship Order Bug with the Return & Enter Key_
- Fixed
  issue #[26528](http://www.xtuple.org/xtincident/view/bugs/26528)
  _'Unit Price UOM' is not being updated automatically in 'Item' screen_
- Fixed
  issue #[26606](http://www.xtuple.org/xtincident/view/bugs/26606)
  _*Omnibus: Unable to add a new image in any screen from 'Documents' section_
- Fixed
  issue #[26629](http://www.xtuple.org/xtincident/view/bugs/26629)
  _User is able to change base currency irrelevantly (replaces #26535)_
- Fixed
  issue #[26638](http://www.xtuple.org/xtincident/view/bugs/26638)
  _*Credit Card Refunds Processed Incorrectly_
- Fixed
  issue #[26643](http://www.xtuple.org/xtincident/view/bugs/26643)
  _Pending Availability with Multi Level BOM issue (replaces 25884)_
- Fixed
  issue #[26648](http://www.xtuple.org/xtincident/view/bugs/26648)
  _Error on issue inventory_
- Fixed
  issue #[26655](http://www.xtuple.org/xtincident/view/bugs/26655)
  _*Voucher uninvoiced column includes RA and other values_
- Fixed
  issue #[26659](http://www.xtuple.org/xtincident/view/bugs/26659)
  _*Discount Not Applying Correctly on Cash Receipt_
- Fixed
  issue #[26687](http://www.xtuple.org/xtincident/view/bugs/26687)
  _Reservation system miscalculates QOH for alternate UOM items_
- Fixed
  issue #[26691](http://www.xtuple.org/xtincident/view/bugs/26691)
  _*DB log error is generated on selecting to check 'Copy Routing' checkbox in 'Copy Item' screen_
- Fixed
  issue #[26696](http://www.xtuple.org/xtincident/view/bugs/26696)
  _*Shipped child item message on quotes_
- Fixed
  issue #[26705](http://www.xtuple.org/xtincident/view/bugs/26705)
  _Lot/Serial not passing to Receiving Site for T/Os_
- Fixed
  issue #[26757](http://www.xtuple.org/xtincident/view/bugs/26757)
  _P/O Returns with Purchase Price Variance are posting to the G/L incorrectly_
- Fixed
  issue #[26783](http://www.xtuple.org/xtincident/view/bugs/26783)
  _ccpayments lists payments twice if customer is in two customer groups_
- Fixed
  issue #[26844](http://www.xtuple.org/xtincident/view/bugs/26844)
  _Getting invalid registration key window 4.10.0-beta_
- Fixed
  issue #[26869](http://www.xtuple.org/xtincident/view/bugs/26869)
  _*AP application drill down issue_
- Fixed
  issue #[26887](http://www.xtuple.org/xtincident/view/bugs/26887)
  _Adding CRM element Relation in Documents causes duplicated lines_
- Fixed
  issue #[26961](http://www.xtuple.org/xtincident/view/bugs/26961)
  _*creating an accounting period fails: malformed array literal_
- Fixed
  issue #[26986](http://www.xtuple.org/xtincident/view/bugs/26986)
  _balancing inventory fails with constraint violations inserting NULLs in value columns_
- Fixed
  issue #[27105](http://www.xtuple.org/xtincident/view/bugs/27105)
  _Need a way to prioritize incidents numerically in addition to current alpha sort, for better project mgmt_
- Fixed
  issue #[27142](http://www.xtuple.org/xtincident/view/bugs/27142)
  _*Omnibus: Windows are getting shrinked irrelevantly_
- Fixed
  issue #[27156](http://www.xtuple.org/xtincident/view/bugs/27156)
  _*CC processing error when A.N is set to process card-present_
- Fixed
  issue #[27189](http://www.xtuple.org/xtincident/view/bugs/27189)
  _Lot Serial Tracking not allowing specific material assignment within Work Order_
- Fixed
  issue #[27205](http://www.xtuple.org/xtincident/view/bugs/27205)
  _*Error Creating new Accounting Periods_
- Fixed
  issue #[27230](http://www.xtuple.org/xtincident/view/bugs/27230)
  _*Costs Visible and Should Not Be_
- Fixed
  issue #[27282](http://www.xtuple.org/xtincident/view/bugs/27282)
  _PAIN - Customer form saves are rather long_
- Fixed
  issue #[27300](http://www.xtuple.org/xtincident/view/bugs/27300)
  _'Fiscal Year', 'Accounting Periods', and 'Exchange Rates' for current year are not being created in demo databases irrelevantly_
- Fixed
  issue #[27301](http://www.xtuple.org/xtincident/view/bugs/27301)
  _orderedbypo function does not include poitem_qty_returned_
- Fixed
  issue #[27305](http://www.xtuple.org/xtincident/view/bugs/27305)
  _*Tax not properly applied_
- Fixed
  issue #[27358](http://www.xtuple.org/xtincident/view/bugs/27358)
  _Characteristics no longer work on Projects List 4.9.1_

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
