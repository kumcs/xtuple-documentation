Release Notes
xTuple ERP
Version 4.4.1
May 16, 2014
----------------------------------

These are the release notes for the 4.4.1 Patch Release. Thanks
to all who contributed to make this release possible.

PLEASE NOTE: Beginning with version 4.4.1, we have introduced a 
new naming convention for our upgrade and installation files. The 
new convention stems from our unified build process, which now 
supports both Desktop and Mobile Web installations. In 4.4.1, you 
will see the following new file naming conventions:

OLD				NEW
pb440to441.gz		pb441.gz
dist440to441.gz		dist441.gz
xtmfg-440to441.gz		xtmfg_update441.gz

To summarize:
PostBooks 440 to 441 = pb441.gz
Distribution 440 to 441= dist441.gz
Manufacturing/Enterprise 440 to 441 = dist441.gz & xtmfg_update441.gz

It should also be noted that these upgrades will NOT run on any 
database prior to version 4.4.0. You will need to upgrade to AT LEAST 
4.4.0 before trying to run the new 4.4.1 patch upgrade packages.

ALSO: Mobile-enabled databases are not supported through the 
traditional Desktop update process. Anyone upgrading a mobile-enabled 
database should follow the process described here:

https://github.com/xtuple/xtuple/wiki/Upgrading  

As always, please review the xTuple Compatibility Matrix before
upgrading: http://www.xtuple.org/compatibility-matrix.

----------------------------------

The following features and bug fixes have been added to the
applications since the 4.4.0 release. Additional detail for
each item listed below may be found on our community
website (www.xtuple.org).

Features:
* AP CM's should display as negative in Payables tab on AP 
workbench [22495]

Bug Fixes:
* Return W/O materials default wrong sign on disassembly [19059]
* Cannot set values of characteristics [22372]
* Summary of Sales History does not show negative amounts [22634]
* Used at operation not copying over in new copy item utility 
[22655]
* Backlog reporting grouping incorrect [22676]
* Production Time Clock by Work Order [22921]
* Purge closed work orders [23070]
* Planned Orders not being generated [23097]
* Error on costed indented BOM of an inactive revision [23114]
* Copying project does not correctly copy Project Type [23143]
* Favorites in xWD [23157]
* PO for Grd entered items in 4.4 [23158]
* api.physinvcount processes quantities for Kit item types 
[23164]
* Selecting to unreserve stock from a sales order line item 
displays a system message [23174]
* Customer Group not working [23181]
* Weight calculation in Sales Order List screen [23246]
* Item Group Parent select list in empty when adding a new group 
[23273]
* Deleting an Item Group doesn't remove it from it's parent group 
[23275]
* Transform incomplete does not transform lot serial 
characteristics package [23276]
* Item site problem when creating a new item and copying it from 
an existing item [23284]
* Drop Ship - PO creation issue [23287]
* Drop ship item source price not displaying on sales order 
[23292]
* Lot control return behavior [23306]
* Developer certificate missing on 4.4.0 Mac client [23320]
* Bug return to line items after first order entered [23345]
* coitem trigger does not honor stock flag [23346]
* Partial issue of non-fractional job costed items [23372]
* Error in 4.4.0 adding SO's to Packing List Batch [23409]
* Margin calculation in salesOrderItem List metaSQL [23415]
* calcsalesorderamt(integer, text) margin percent calculation 
[23416]
* Manufacturing empty database: It is not possible to create a 
Work Order [23465]
* Correctly set serverVersion on desktop and database in new 
paradigm [23479]
* PostBooks: It is not possible to issue material batch/item for 
a work order [23482]
* It is not possible to issue stock to a Transfer Order [23483]
* It is not possible to create receipt for Return Authorizations 
[23485]
