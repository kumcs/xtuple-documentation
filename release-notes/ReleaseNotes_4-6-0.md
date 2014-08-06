## xTuple Release Notes  
##### Version 4.6.0 Final * August 5, 2014  

These are the release notes for the 4.6.0 Final Release. Thanks to all who contributed to make this release possible.
For more information about [deploying this release](#deployment-notes), please see below.

### Features and bugfixes

The following features and bug fixes have been added to the application since the 4.5.0 release. 
Additional detail for each item listed below may be found on our [community website](http://www.xtuple.org).

##### Web/Mobile Application

- Fixed 
  issue #[21966](http://www.xtuple.org/xtincident/view/bugs/21966) 
  _Sales Analysis appears when bi extension is not enabled_ 
- Fixed 
  issue #[24104](http://www.xtuple.org/xtincident/view/bugs/24104) 
  _npm extension bugs_ 
- Fixed 
  issue #[24202](http://www.xtuple.org/xtincident/view/bugs/24202) 
  _Web Client Broken in Chrome latest!_ 
- Fixed 
  issue #[23966](http://www.xtuple.org/xtincident/view/bugs/23966) 
  _notify popup disappears on window resize_ 
- Implemented 
  issue #[22996](http://www.xtuple.org/xtincident/view/bugs/22996) 
  _signature capture_ 
  [![Signature Capture](https://i.vimeocdn.com/video/483976760_600x336.jpg)](http://player.vimeo.com/video/102056940)
- Implemented 
  issue #[23796](http://www.xtuple.org/xtincident/view/bugs/23796) 
  _Export grid list to csv_ 
- Implemented 
  issue #[23897](http://www.xtuple.org/xtincident/view/bugs/23897) 
  _Show charts based on privileges_ 
- Implemented 
  issue #[24073](http://www.xtuple.org/xtincident/view/bugs/24073) 
  _haxTuple: update ice cream tutorial_ 
- Implemented 
  issue #[23962](http://www.xtuple.org/xtincident/view/bugs/23962) 
  _css in extensions_ 


##### Desktop Application
- Fixed 
  issue #[20422](http://www.xtuple.org/xtincident/view/bugs/20422) 
  _*Observation:- 'Reason' list is not available on 'Lost Sale' screen for the cancellation of a sales  order line item_
- Fixed 
  issue #[23861](http://www.xtuple.org/xtincident/view/bugs/23861) 
  _*Cash Effective date out of range_ 
- Fixed 
  issue #[23873](http://www.xtuple.org/xtincident/view/bugs/23873) 
  _AP Memo on cancel can leave document in apopen table_ 
- Fixed 
  issue #[23877](http://www.xtuple.org/xtincident/view/bugs/23877) 
  _Clear out top level material costs_ 
- Fixed 
  issue #[24111](http://www.xtuple.org/xtincident/view/bugs/24111) 
  _Net Unit Price and price UOM in SO for AVG cost items_ 
- Fixed 
  issue #[24144](http://www.xtuple.org/xtincident/view/bugs/24144) 
  _GL Transaction remains unposted after balancing_ 
- Fixed 
  issue #[24177](http://www.xtuple.org/xtincident/view/bugs/24177) 
  _*orderActivityByProject metasql error_ 
- Fixed 
  issue #[24187](http://www.xtuple.org/xtincident/view/bugs/24187) 
  _No mulit select in PO requests_ 
- Fixed 
  issue #[24194](http://www.xtuple.org/xtincident/view/bugs/24194)
  _*Documents widgets not show Invoice_ 
- Fixed 
  issue #[24154](http://www.xtuple.org/xtincident/view/bugs/24154) 
  _*Kits generate linked POs when added to an SO_ 
- Fixed 
  issue #[24199](http://www.xtuple.org/xtincident/view/bugs/24199) 
  _*Bank Reconciliation process and Bank Reconciliation History report include deleted GL entries_ 
- Fixed 
  issue #[24230](http://www.xtuple.org/xtincident/view/bugs/24230) 
  _*Calculation at the bottom of the bank reconciliation history is opposite of what it should be_ 
- Fixed 
  issue #[24233](http://www.xtuple.org/xtincident/view/bugs/24233) 
  _* It is not possible to create a pricing schedule for 'Mark up by Product Category'_ 
- Fixed 
  issue #[24249](http://www.xtuple.org/xtincident/view/bugs/24249) 
  _*Issue with viewing Sales History cost_ 
- Fixed 
  issue #[24269](http://www.xtuple.org/xtincident/view/bugs/24269) 
  _quick item entry itemsite selection_ 
- Implemented 
  issue #[23878](http://www.xtuple.org/xtincident/view/bugs/23878) 
  _combine bank rec functions_ 
- Implemented 
  issue #[23254](http://www.xtuple.org/xtincident/view/bugs/23254) 
  _Add the ability to enter an alternate exchange rate on a Cash Receipt_ 


### Deployment Notes

We've lately revised the
naming conventions and the behavior of our core updater packages.
Our overall goal is to simplify the process of installing and
upgrading xTuple ERP databases.

Just as was true for the 4.4.1 release, you will only need to apply
one updater package to upgrade to 4.6.0--that is, assuming you are
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

    postbooks-upgrade-460.gz will:
    upgrade a PostBooks database from anywhere >= 4.4.0 to 4.6.0

    manufacturing-upgrade-460.gz will:
    upgrade the standard/dist (i.e., inventory code) to 4.6.0
    upgrade the manufacturing code to 4.6.0

    manufacturing-install-460.gz will:
    do a one-time install of tables, etc. for standard (i.e., inventory code) at 4.6.0
    upgrade the standard/dist (i.e., inventory code) to 4.6.0
    do a one-time install of tables, etc. for manufacturing at 4.6.0
    upgrade the manufacturing code to 4.6.0

    distribution-upgrade-460.gz will:
    upgrade the standard/ist (i.e., inventory code) to 4.6.0
    upgrade the distribution (i.e., xwd code) to 4.6.0

    distribution-install-460.gz will:
    do a one-time install of tables, etc. for standard (i.e., inventory code) at 4.6.0
    upgrade the standard/dist (i.e., inventory code) to 4.6.0
    do a one-time install of tables etc for distribution at 4.6.0
    upgrade the distribution (i.e., xwd code) to 4.6.0

PLEASE NOTE: Other packages, such as Advanced Commissions and Fixed 
Assets, are currently remaining on their own release schedule and should 
be installed as before. 
