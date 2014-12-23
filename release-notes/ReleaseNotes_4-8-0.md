## xTuple Release Notes
##### Version 4.8.0 Final * December 23, 2014

These are the release notes for the 4.8.0 Final Release. Thanks to all who contributed to make this release possible.
For more information about [deploying this release](#deployment-notes), please see below.

### Features and bug fixes

The following features and bug fixes have been added to the application since the 4.7.0 release.
Additional detail for each item listed below may be found on our [community website](http://www.xtuple.org).


##### Desktop Application

 - Implemented
   issue #[17145](http://www.xtuple.org/xtincident/view/bugs/17145)
   _*Add the ability to post "checks" without printing_
 - Implemented
   issue #[24314](http://www.xtuple.org/xtincident/view/bugs/24314)
   _Add "Item Pattern" to parameter widget in Sales History_
 - Implemented
   issue #[24532](http://www.xtuple.org/xtincident/view/bugs/24532)
   _*Improve Sales Order Line Item Entry_
 - Implemented
   issue #[24769](http://www.xtuple.org/xtincident/view/bugs/24769)
   _Add a generic signal interface for scripting_
 - Implemented
   issue #[25114](http://www.xtuple.org/xtincident/view/bugs/25114)
   _Total Amount on Opportunity List View_
 - Fixed
   issue #[17261](http://www.xtuple.org/xtincident/view/bugs/17261)
   _Invoice Register preview and print blank_
 - Fixed
   issue #[22081](http://www.xtuple.org/xtincident/view/bugs/22081)
   _Open AP voucher which we cannot wipe off by paying check or applying a credit_
 - Fixed
   issue #[23119](http://www.xtuple.org/xtincident/view/bugs/23119)
   _Invoice doubling issue_
 - Fixed
   issue #[23510](http://www.xtuple.org/xtincident/view/bugs/23510)
   _Problem with miscellaneous vouchers_
 - Fixed
   issue #[23574](http://www.xtuple.org/xtincident/view/bugs/23574)
   _*'Add' buttons is active under 'Roles' tab in the 'User Account Information screen' when no role is selected_
 - Fixed
   issue #[23639](http://www.xtuple.org/xtincident/view/bugs/23639)
   _Barcode scanning into Post Operation screen_
 - Fixed
   issue #[24191](http://www.xtuple.org/xtincident/view/bugs/24191)
   _*Sales Order characteristics not being added to automatically-generated Purchase Orders_
 - Fixed
   issue #[24356](http://www.xtuple.org/xtincident/view/bugs/24356)
   _RMA's post unit price to actual cost when RMA is Received_
 - Fixed
   issue #[24381](http://www.xtuple.org/xtincident/view/bugs/24381)
   _*Ship-To Address searching takes too long to return a value_
 - Fixed
   issue #[24421](http://www.xtuple.org/xtincident/view/bugs/24421)
   _*Sales order number reused after order is deleted_
 - Fixed
   issue #[24469](http://www.xtuple.org/xtincident/view/bugs/24469)
   _xt.lock problems persisting_
 - Fixed
   issue #[24482](http://www.xtuple.org/xtincident/view/bugs/24482)
   _*UOM Conversion Panel_
 - Fixed
   issue #[24512](http://www.xtuple.org/xtincident/view/bugs/24512)
   _*No warning dialog is displayed on selecting to save 'Billing Approvals' with -ve Total	_
 - Fixed
   issue #[24588](http://www.xtuple.org/xtincident/view/bugs/24588)
   _*'Issue Line'/'Issue All' buttons are not working on 'Issue to Shipping' screen_
 - Fixed
   issue #[24627](http://www.xtuple.org/xtincident/view/bugs/24627)
   _*next/previous buttons iterate over canceled line items_
 - Fixed
   issue #[24687](http://www.xtuple.org/xtincident/view/bugs/24687)
   _*Sale Price disappears from RA_
 - Fixed
   issue #[24694](http://www.xtuple.org/xtincident/view/bugs/24694)
   _Unable to issue individual material item to work order from work order screen_
 - Fixed
   issue #[24698](http://www.xtuple.org/xtincident/view/bugs/24698)
   _Sales History does not reflect PO cost_
 - Fixed
   issue #[24702](http://www.xtuple.org/xtincident/view/bugs/24702)
   _*Copy Item does not maintain Target Item description and item_id properly_
 - Fixed
   issue #[24740](http://www.xtuple.org/xtincident/view/bugs/24740)
   _*'A Stored Procedure failed ..' dialog is displayed on Selecting to reserve zero(0.00) quantity from a lot_
 - Fixed
   issue #[24745](http://www.xtuple.org/xtincident/view/bugs/24745)
   _*Irrelevant behavior is observed in 'Routing' tab of 'Copy Item' screen_
 - Fixed
   issue #[24746](http://www.xtuple.org/xtincident/view/bugs/24746)
   _*Duplication of SalesType is allowed_
 - Fixed
   issue #[24750](http://www.xtuple.org/xtincident/view/bugs/24750)
   _*Item Copy not copying all data_
 - Fixed
   issue #[24756](http://www.xtuple.org/xtincident/view/bugs/24756)
   _*Insert to api.contact fails to save new address record_
 - Fixed
   issue #[24760](http://www.xtuple.org/xtincident/view/bugs/24760)
   _*Actual Cost Issue_
 - Fixed
   issue #[24761](http://www.xtuple.org/xtincident/view/bugs/24761)
   _*Item Prices are not updated on 'Copy Item' screen on selecting to uncheck 'Rollup Prices'_
 - Fixed
   issue #[24781](http://www.xtuple.org/xtincident/view/bugs/24781)
   _*Pricing Schedule Overlapping in Error_
 - Fixed
   issue #[24791](http://www.xtuple.org/xtincident/view/bugs/24791)
   _Cannot view posted misc check details_
 - Fixed
   issue #[24795](http://www.xtuple.org/xtincident/view/bugs/24795)
   _AVG costing with zero qtyonhand does not revert to STD costing with xwdspa_
 - Fixed
   issue #[24802](http://www.xtuple.org/xtincident/view/bugs/24802)
   _*Blank columns are observed in 'Count Tag Edit List' screen_
 - Fixed
   issue #[24823](http://www.xtuple.org/xtincident/view/bugs/24823)
   _*Priority Level_
 - Fixed
   issue #[24831](http://www.xtuple.org/xtincident/view/bugs/24831)
   _*Accounts Payable vouchers_
 - Fixed
   issue #[24834](http://www.xtuple.org/xtincident/view/bugs/24834)
   _*Permission error when creating new prospect/customer_
 - Fixed
   issue #[24839](http://www.xtuple.org/xtincident/view/bugs/24839)
   _*Exchange rate in bank rec don't work right_
 - Fixed
   issue #[24846](http://www.xtuple.org/xtincident/view/bugs/24846)
   _*Error with cash base taxation_
 - Fixed
   issue #[24848](http://www.xtuple.org/xtincident/view/bugs/24848)
   _Check detail may print unrelated vouchers on check stub_
 - Fixed
   issue #[24850](http://www.xtuple.org/xtincident/view/bugs/24850)
   _*Cannot create CRM account without MaintainUsers privilege_
 - Fixed
   issue #[24872](http://www.xtuple.org/xtincident/view/bugs/24872)
   _*Error distributing to default location using Issue to Shipping screen_
 - Fixed
   issue #[24878](http://www.xtuple.org/xtincident/view/bugs/24878)
   _*Error upon entering line qty for SO line item with Item Availability Workbench open_
 - Fixed
   issue #[24882](http://www.xtuple.org/xtincident/view/bugs/24882)
   _*Unapplied A/R Credit Mem - Screen dif from Print_
 - Fixed
   issue #[24885](http://www.xtuple.org/xtincident/view/bugs/24885)
   _*AR out of balance_
 - Fixed
   issue #[24887](http://www.xtuple.org/xtincident/view/bugs/24887)
   _*Inventory receiving adds to order to Packing List Batch without reserving inventory_
 - Fixed
   issue #[24898](http://www.xtuple.org/xtincident/view/bugs/24898)
   _*dup work orders_
 - Fixed
   issue #[24902](http://www.xtuple.org/xtincident/view/bugs/24902)
   _*Void invoice using alternate accnt_
 - Fixed
   issue #[24909](http://www.xtuple.org/xtincident/view/bugs/24909)
   _void voucher does not work on multi-select_
 - Fixed
   issue #[24914](http://www.xtuple.org/xtincident/view/bugs/24914)
   _*470 Issue: Summarized Sales total don't match_
 - Fixed
   issue #[24958](http://www.xtuple.org/xtincident/view/bugs/24958)
   _*Sales Order Line Item Edit : Reserve & Save should not be hidden_
 - Fixed
   issue #[24959](http://www.xtuple.org/xtincident/view/bugs/24959)
   _*Bypass reserve and save Pop Up Window_
 - Fixed
   issue #[24963](http://www.xtuple.org/xtincident/view/bugs/24963)
   _itemsite trigger for reorderlevels_
 - Fixed
   issue #[24964](http://www.xtuple.org/xtincident/view/bugs/24964)
   _*Unit cost on converted quote displayed incorrectly_
 - Fixed
   issue #[24996](http://www.xtuple.org/xtincident/view/bugs/24996)
   _*Request Profit % on Brief Sales History Report_
 - Fixed
   issue #[25022](http://www.xtuple.org/xtincident/view/bugs/25022)
   _*Omnibus: Cursor defaults to 'Transaction Date' irrelevantly_
 - Fixed
   issue #[25026](http://www.xtuple.org/xtincident/view/bugs/25026)
   _*Non-Netable' column values are not displayed in print report of 'Quantities on Hand'_
 - Fixed
   issue #[25034](http://www.xtuple.org/xtincident/view/bugs/25034)
   _*QOH not Displaying in the Advanced Item Search_
 - Fixed
   issue #[25043](http://www.xtuple.org/xtincident/view/bugs/25043)
   _*Available QOH not showing in line tab, quote window_
 - Fixed
   issue #[25046](http://www.xtuple.org/xtincident/view/bugs/25046)
   _Wrong values when returning same item on two lines_
 - Fixed
   issue #[25049](http://www.xtuple.org/xtincident/view/bugs/25049)
   _Discrepancy in privileges to maintain a customer_
 - Fixed
   issue #[25058](http://www.xtuple.org/xtincident/view/bugs/25058)
   _*Totals not displaying for all quotes in the Quotes window_
 - Fixed
   issue #[25077](http://www.xtuple.org/xtincident/view/bugs/25077)
   _*Margin and Margin % are displaying incorrectly in the Unposted Invoice and Invoice windows_
 - Fixed
   issue #[25097](http://www.xtuple.org/xtincident/view/bugs/25097)
   _SO Print on Save defaults to Cancel, not OK/Print_
 - Fixed
   issue #[25109](http://www.xtuple.org/xtincident/view/bugs/25109)
   _*Irrelevant behavior is observed in Customer Workbench screen_
 - Fixed
   issue #[25116](http://www.xtuple.org/xtincident/view/bugs/25116)
   _*Characteristic values not displaying in the Open Sales Orders Window_
 - Fixed
   issue #[25118](http://www.xtuple.org/xtincident/view/bugs/25118)
   _*Using new Security Roles not Working_
 - Fixed
   issue #[25130](http://www.xtuple.org/xtincident/view/bugs/25130)
   _*Selecting to copy the sales order doesn't copy the Sales Order characteristics_
 - Fixed
   issue #[25141](http://www.xtuple.org/xtincident/view/bugs/25141)
   _*Postgre 9.1, 9.2 :User is not allowed to create a work order on mfgdemo,mfg empty data bases_
 - Fixed
   issue #[25142](http://www.xtuple.org/xtincident/view/bugs/25142)
   _4.7.0 dist and mfg quickstart dbs missing account assigments_


### Deployment Notes

We've lately revised the
naming conventions and the behavior of our core updater packages.
Our overall goal is to simplify the process of installing and
upgrading xTuple ERP databases.

Just as was true for the 4.4.1 release, you will only need to apply
one updater package to upgrade to 4.7.0--that is, assuming you are
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

    postbooks-upgrade-470.gz will:
    upgrade a PostBooks database from anywhere >= 4.4.0 to 4.7.0

    manufacturing-upgrade-470.gz will:
    upgrade the standard/dist (i.e., inventory code) to 4.7.0
    upgrade the manufacturing code to 4.7.0

    manufacturing-install-470.gz will:
    do a one-time install of tables, etc. for standard (i.e., inventory code) at 4.7.0
    upgrade the standard/dist (i.e., inventory code) to 4.7.0
    do a one-time install of tables, etc. for manufacturing at 4.7.0
    upgrade the manufacturing code to 4.7.0

    distribution-upgrade-470.gz will:
    upgrade the standard/ist (i.e., inventory code) to 4.7.0
    upgrade the distribution (i.e., xwd code) to 4.7.0

    distribution-install-470.gz will:
    do a one-time install of tables, etc. for standard (i.e., inventory code) at 4.7.0
    upgrade the standard/dist (i.e., inventory code) to 4.7.0
    do a one-time install of tables etc for distribution at 4.7.0
    upgrade the distribution (i.e., xwd code) to 4.7.0

PLEASE NOTE: Other packages, such as Advanced Commissions and Fixed
Assets, are currently remaining on their own release schedule and should
be installed as before.
