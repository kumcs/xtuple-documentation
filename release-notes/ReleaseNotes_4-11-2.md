
# xTuple Release Notes

## Version 4.11.2 - November, 2017

These are the release notes for the 4.11.2 xTuple ERP release.
Thanks to all who contributed to make this release possible,
including our CRM enhancements sponsor,
Steven Buttgereit, Larry Cartee, Lee Gibson,
Chris Lappe, Scott Moore, Mike Oligny, and Scott Zuke.
See below for more information about
[deploying this release](#deployment-notes).

### Summary

A handful of features have been added and a number of bugs fixed since the 4.11.1 release. Our focus has been on xTupleCommerce infrastructure and enhancing the capabilities of CRM.

Of particular interest are the following:

- Sorting lists by multiple columns
- Expanding document attachment capabilities
- The ability to create prospects directly from contacts


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

### Features added in 4.11.2

- Features issue #[19555](http://www.xtuple.org/xtincident/view/bugs/19555) _Cannot Attach Quotes to Incidents (or anywhere on Document Tab)_
- Features issue #[29623](http://www.xtuple.org/xtincident/view/bugs/29623) _[qt-client] Add fiscal year filter to trial balance_
- Features issue #[29887](http://www.xtuple.org/xtincident/view/bugs/29887) _Add Shipto Parameter to SalesOrder_
- Features issue #[30092](http://www.xtuple.org/xtincident/view/bugs/30092) _DOCs on JE_
- Features issue #[30392](http://www.xtuple.org/xtincident/view/bugs/30392) _Miscellaneous Debit and Credit Memo's should not have account list filtered_
- Features issue #[31105](http://www.xtuple.org/xtincident/view/bugs/31105) _Default in Tax Type from Vendor on Misc Vouchers_
- Features issue #[31217](http://www.xtuple.org/xtincident/view/bugs/31217) _Need ability to create prospects from contacts_
- Features issue #[31245](http://www.xtuple.org/xtincident/view/bugs/31245) _Incidents don't properly preserve history with respect to notes changes_
- Features issue #[31445](http://www.xtuple.org/xtincident/view/bugs/31445) _The DocAttach dialog will need modifications to enhance its scriptability_
- Features issue #[31446](http://www.xtuple.org/xtincident/view/bugs/31446) _Exposed QMimeDatabase to scripting_
- Features issue #[31560](http://www.xtuple.org/xtincident/view/bugs/31560) _Support Multiple Column Order By on XTreeWidget_
- Features issue #[31636](http://www.xtuple.org/xtincident/view/bugs/31636) _support multi-select in CRM lists to process multiple objects_

### Bug fixes in 4.11.1

- Fixed issue #[18973](http://www.xtuple.org/xtincident/view/bugs/18973) _Key entered January dates not saved correctly using DD/MM/YY dates_
- Fixed issue #[19108](http://www.xtuple.org/xtincident/view/bugs/19108) _Extensions load in random order_
- Fixed issue #[23405](http://www.xtuple.org/xtincident/view/bugs/23405) _4.4 Icon not as fancy as 4.3_
- Fixed issue #[26635](http://www.xtuple.org/xtincident/view/bugs/26635) _Linux: Setup(sales) screen does not fit to the window (replaces #26568)_
- Fixed issue #[26730](http://www.xtuple.org/xtincident/view/bugs/26730) _use xt.lock lock_expire to get rid of old, orphaned locks_
- Fixed issue #[27917](http://www.xtuple.org/xtincident/view/bugs/27917) _Able to add comments to sales orderitem in view mode also._
- Fixed issue #[28019](http://www.xtuple.org/xtincident/view/bugs/28019) _Planner Code, Cost Category details are not being displayed in print report of 'Frozen Item Sites'_
- Fixed issue #[28952](http://www.xtuple.org/xtincident/view/bugs/28952) _Mac version of 4.10.0 final desktop client is unsigned_
- Fixed issue #[29316](http://www.xtuple.org/xtincident/view/bugs/29316) _Documents attached to incident are not being deleted from 'docass' table when incident is cancelled during its creation._
- Fixed issue #[29744](http://www.xtuple.org/xtincident/view/bugs/29744) _Bank Rec Date Issue_
- Fixed issue #[30519](http://www.xtuple.org/xtincident/view/bugs/30519) _coitem_listprice should include the charass_price for configured items._
- Fixed issue #[30592](http://www.xtuple.org/xtincident/view/bugs/30592) _No Foreign Key to link cashrcpt with ccpay_
- Fixed issue #[30729](http://www.xtuple.org/xtincident/view/bugs/30729) _RA with serial number broken_
- Fixed issue #[30799](http://www.xtuple.org/xtincident/view/bugs/30799) _Voiding AP Voucher - error in Tax History Report_
- Fixed issue #[30857](http://www.xtuple.org/xtincident/view/bugs/30857) _Vendor No. is grayed_
- Fixed issue #[30894](http://www.xtuple.org/xtincident/view/bugs/30894) _api.custshipto view select issue with no cust shipform_
- Fixed issue #[30895](http://www.xtuple.org/xtincident/view/bugs/30895) _‘Item Sites’ screen is displayed behind the ‘Accounting’ setup screen when it is opened from ‘Cost Categories’ in 'Accounting'_
- Fixed issue #[30908](http://www.xtuple.org/xtincident/view/bugs/30908) _lower level user defined cost posting to GL_
- Fixed issue #[30911](http://www.xtuple.org/xtincident/view/bugs/30911) _api.vendor behavior fails to automatically assign crm account numbers on insert_
- Fixed issue #[30913](http://www.xtuple.org/xtincident/view/bugs/30913) _Maintain/View privilege issues_
- Fixed issue #[30922](http://www.xtuple.org/xtincident/view/bugs/30922) _Sales configuration has a new field (4.11) that is not "hooked up" called Ordeer Start Date_
- Fixed issue #[30933](http://www.xtuple.org/xtincident/view/bugs/30933) _AP Credit Memo application field size issue_
- Fixed issue #[30948](http://www.xtuple.org/xtincident/view/bugs/30948) _Invoices should have comments_
- Fixed issue #[30992](http://www.xtuple.org/xtincident/view/bugs/30992) _Monitored Accounts don't display in xtdesktop 4.0.8_
- Fixed issue #[31007](http://www.xtuple.org/xtincident/view/bugs/31007) _Extended price column not totalling on backlog display_
- Fixed issue #[31061](http://www.xtuple.org/xtincident/view/bugs/31061) _desktop client does not (down)load extension translations properly from database_
- Fixed issue #[31065](http://www.xtuple.org/xtincident/view/bugs/31065) _Recurring Invoices which are posted have Edit options available_
- Fixed issue #[31118](http://www.xtuple.org/xtincident/view/bugs/31118) _4.11.1 upgrade breaks inventory availability report_
- Fixed issue #[31126](http://www.xtuple.org/xtincident/view/bugs/31126) _New Purchase Orders take almost a minute to open_
- Fixed issue #[31133](http://www.xtuple.org/xtincident/view/bugs/31133) _AR Workbench Customer Type Pattern Query Fails_
- Fixed issue #[31166](http://www.xtuple.org/xtincident/view/bugs/31166) _"Issue Batch" not working_
- Fixed issue #[31168](http://www.xtuple.org/xtincident/view/bugs/31168) _View Costing Detail reports repeated lines_
- Fixed issue #[31170](http://www.xtuple.org/xtincident/view/bugs/31170) _Work order routing and pick list do not show revision_
- Fixed issue #[31191](http://www.xtuple.org/xtincident/view/bugs/31191) _Can manually add a parent item as a child in a wo_
- Fixed issue #[31214](http://www.xtuple.org/xtincident/view/bugs/31214) _Unable to change Order Start Date on Customer Defaults_
- Fixed issue #[31227](http://www.xtuple.org/xtincident/view/bugs/31227) _Error in updating ‘From Site’ value in ‘Transfer Order Item’ screen while creating a new transfer order._
- Fixed issue #[31228](http://www.xtuple.org/xtincident/view/bugs/31228) _Order Number with matching pattern is not displayed correctly in ‘Vendor’ drop down_
- Fixed issue #[31229](http://www.xtuple.org/xtincident/view/bugs/31229) _Salesorder API view doesn't work without shipform_
- Fixed issue #[31264](http://www.xtuple.org/xtincident/view/bugs/31264) _pricing schedule problem_
- Fixed issue #[31271](http://www.xtuple.org/xtincident/view/bugs/31271) _Saving dates from scripts doesn't work correctly across DST_
- Fixed issue #[31278](http://www.xtuple.org/xtincident/view/bugs/31278) _Sales Credit - project field enabled in View mode_
- Fixed issue #[31284](http://www.xtuple.org/xtincident/view/bugs/31284) _Viewing a Sales Credit results in corrupted data in cmhead table_
- Fixed issue #[31298](http://www.xtuple.org/xtincident/view/bugs/31298) _Issue To Ship Not respecting UOM Conversion_
- Fixed issue #[31303](http://www.xtuple.org/xtincident/view/bugs/31303) _tabbing over an item in a list doesn't expose it to the keyboard_
- Fixed issue #[31304](http://www.xtuple.org/xtincident/view/bugs/31304) _Future posting date_
- Fixed issue #[31315](http://www.xtuple.org/xtincident/view/bugs/31315) _omnibus: embedded windows use default filter, not parent window filter_
- Fixed issue #[31331](http://www.xtuple.org/xtincident/view/bugs/31331) _Bank Rec Import Error_
- Fixed issue #[31455](http://www.xtuple.org/xtincident/view/bugs/31455) _Memory Leaks when opening C++ core dialogs from scripts_
- Fixed issue #[31459](http://www.xtuple.org/xtincident/view/bugs/31459) _Escape value string in MetaSQL js PEG parser_
- Fixed issue #[31460](http://www.xtuple.org/xtincident/view/bugs/31460) _Expose functions to scripting for paymentgateways_
- Fixed issue #[31475](http://www.xtuple.org/xtincident/view/bugs/31475) _In ‘Sales Order Lookup by Item’ screen, when Sales Order is opened in ‘View’ mode, able to cancel ‘Non shipped Sales Order line_
- Fixed issue #[31483](http://www.xtuple.org/xtincident/view/bugs/31483) _Error dialog is displayed when ‘Freight’ is entered instead of ‘Misc. Charge’ without credit account in 'Sales Credit' screen._
- Fixed issue #[31498](http://www.xtuple.org/xtincident/view/bugs/31498) _FRE shows inactive financial reports_
- Fixed issue #[31509](http://www.xtuple.org/xtincident/view/bugs/31509) _CSVImp can crash during import from within desktop client 4.11.x versions_
- Fixed issue #[31596](http://www.xtuple.org/xtincident/view/bugs/31596) _Relocate inventory: You cannot Relocate more inventory than is available_
- Fixed issue #[31600](http://www.xtuple.org/xtincident/view/bugs/31600) _Items Sources list count in ‘Preview’ mode is mismatch when compare with list in ‘Items Sources’ screen_
- Fixed issue #[31602](http://www.xtuple.org/xtincident/view/bugs/31602) _User is able to add ‘New PO’, when created contract is opened in ‘View’ mode from ‘Contract’ screen._
- Fixed issue #[31631](http://www.xtuple.org/xtincident/view/bugs/31631) _Says item on order in error_
- Fixed issue #[31673](http://www.xtuple.org/xtincident/view/bugs/31673) _‘Processing Error’ occurs while posting miscellaneous production._
- Fixed issue #[31679](http://www.xtuple.org/xtincident/view/bugs/31679) _‘Error Retrieving Shipment Information’ dialog occurs while returning the stock issued to shipping._
- Fixed issue #[31701](http://www.xtuple.org/xtincident/view/bugs/31701) _catCost screen Typo's_
- Fixed issue #[31709](http://www.xtuple.org/xtincident/view/bugs/31709) _User is unable to edit the ‘Prototype’ Type of comments by double clicking on it._

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
