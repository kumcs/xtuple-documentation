Release Notes
xTuple ERP
Version 4.3.0 Beta
November 20, 2013
----------------------------------

These are the release notes for the 4.3.0 Beta Release. Thanks
to all who contributed to make this release possible. As always, 
we welcome feedback from beta testers, but please do not use beta 
software in production.

Here's an overview of notable new features in this release, several
of which were made possible by the FeatureMob2 crowd-sourcing
campaign:

Auto-updating Desktop client
  * At log in, the client checks to see if the client version matches 
    the serverVersion metric
  * If the two do not match, a new client matching the serverVersion 
    will download if desired
  * Available for ServerVersion 4.3.0 Beta and newer

Blanket Purchase Orders
  * Contract-based purchasing

Finance Charges
  * Assess finance charges on overdue invoices

Undo Bank Reconciliations
  * New flexibility to correct bank rec errors

Lot reservations
  * Manually reserve lot quantities to Sales Orders

A/R and A/P Workbenches
  * Multiple usability enhancements 

As always, please review the xTuple Compatibility Matrix before
upgrading: http://www.xtuple.org/compatibility-matrix.

----------------------------------

The following features and bug fixes have been added to the
applications since the 4.2.0 release. Additional detail for
each item listed below may be found on our community
website (www.xtuple.org).

New Features:

* Undo Bank Reconciliations [8891]
* Customer Prices by Item [9405]
* Add "Open Customer Master" to right-click on A/R Workbench 
[16055]
* Add right-click to see source Voucher on AP Workbench [16366]
* Add "Void" option to right-click on AP Workbench, Payables 
tab [17852]
* Finance charges [20104]
* Local currency on order backlog [20147]
* Omnibus - Improvements to AP Workbench [20279]
* Right-click on AR Workbench to open Customer [20281]
* Blanket PO based on Contracts [20861]
* Manual Lot Reservations to SO [21098]
* Add Sales Order totals and Quote Totals to xWD 2.1Alpha 
[21319]
* Add Incidents to Projects and Project Activities [21561]

Bug Fixes:

* Make updates more automatic [5837]
* Error voiding multi-currency check [19634]
* Recurring creation utility bug [20277]
* Project Task List is displaying incorrect dates [21312]
* Reimplement the Project Copy action using standard 
methodology [21693]
* "Create Item Source" dialog is displayed irrelevantly on 
selecting to save the blank "Purchase Order Item" screen [21718]
* Unable to Override Price for a supply order during SOE [21737]
* Linked POs [21753]
* Shipto General Notes do not populate sales orders [21779]
* Inside sales rep CHAR not being passed to the Invoice( xWD 2.1) 
[21822]
* MRP Exceptions [21829]
* Work Order Project Not being updated [21835]
* New gap filling SO function replaces SO numbering when quotes 
are involved [21850]
* openPurchaseOrder Screen [21886]
