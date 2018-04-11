Change Log
OpenMFG
Version 1.2.0-Beta1
May 18, 2005
==================================



The following features and bug fixes have been added to the application 
since the release of version 1.2.0-alpha:



New features:


* Added Standard Journal History display.
* Added ability to reverse Standard Journal and Standard Journal Group
postings. Reversing entries can be made from the relevant Post screens
and also from the right-click menus in G/L|Displays|Standard Journal
History, G/L|Displays|G/L Series.
* Added configuration option in System|Configure G/L to make Notes
required for Journal entries if desired.
* Added Search for Document capability on Cash Receipts screen.
* Improved ability to find and load language files used when translating
OpenMFG screens into other languages.
* Add requirement to Bank Reconciliation requiring a difference of '0'
before users may post a reconciliation (#3277).
* Added ability to search for Item Aliases generically, instead of by
exact match (#3305).


Bug Fixes:

* Fixed problem causing error message when posting Count Tags by Class
Code (#3309).
* Fixed rounding error for Work Order qty. having more than 4 places of
decimal precision (#3273).
* Fixed problem with View Work Order option in contextual menu of Item
Allocations screen (#3298). 
* Prevented closed Sales Order Items from being selected for billing 
(#3303).
* Fixed problem with Notes not saving on Standard Journal entries (#3285)
* Made default print qty. = 1 when printing Pick Lists (#3226).
* Fixed problem with Document # not saving on Bill of Operations (BOO) header
(#3205).
* Removed non-functional "Allow Pull Through" flag on BOO Item screen (#3066).
* Fixed problem with printing of multiple Count Tag Edit List pages from the display screen (#3304).



PLEASE NOTE: The application-based help files have been updated to fix the
navigation errors discovered in the 1.2.0Alpha release.


