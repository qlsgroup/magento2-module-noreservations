# No Reservations Magento 2 Module

Magento 2.3 introduced [MSI](https://github.com/magento/inventory) which was a complete overhaul of its inventory management system enabling use of multiple source inventories. A new concept introduced in MSI is [reservations](https://devdocs.magento.com/guides/v2.3/inventory/reservations.html). When combined with an ERP system which is the source of truth for stock data these reservations can be problematic if the ERP is updating Magento with levels of salable stock rather than physical stock on hand. see [this github issue](https://github.com/magento/inventory/issues/2269)

This module attempts to get around some of these issues by doing the following:

* Stopping any reservations being persisted to the database.
* No deductions on Shipping because QLS manages this. 

We are basically reverting to a behaviour more like Magento 2.2 where stock qty is also the saleable qty. 

Originally make by [8 Wire Digital](https://www.8wiredigital.co.nz/)
Copied by [QLS](https://www.qls.nl/)