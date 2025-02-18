# Assignment User Stories

   1. The module needs to be compatible with Magento v2.4.6.
   2. Users should experience functional address validation while adding addresses from both the My Account page and during the checkout process.
   3. Auto-complete suggestions for Canadian and US addresses should be available to users.
    
# Developer Guide

1. Create an account with Smarty Streets, so that you can use the API keys for the integration. Click [here](https://www.smarty.com) to create a free account.
2. Start below services from Smarty Streets as free trial - 'US Address Verification, Core Edition, Cloud License' and 'US Address Autocomplete, Pro Edition, Cloud License'.
3. Follow the below mentioned module documentation for further details.

# Pyxl_SmartyStreets
Using the SmartyStreet SDK this module offers address validation and autocomplete for customer addresses. 
The validation is performed when a customer adds/edits their address from the Customer Dashboard
as well as in the checkout process.

This module requires valid API credentials for SmartyStreets. 
You can find their pricing options [here](https://smartystreets.com/pricing).  

## Getting Started
To install this module run the following.

If you **don't** have Pyxl_Core installed already run this first:

    composer config repositories.pyxl-core git https://github.com/thinkpyxl/magento2-Pyxl_Core.git
    composer require pyxl/core:^1.0.0
    bin/magento module:enable Pyxl_Core
    
Then require this package:

    composer config repositories.pyxl-smartystreets git https://github.com/thinkpyxl/magento2-Pyxl_SmartyStreets.git
    composer require pyxl/module-smartystreets:^1.0.13
    bin/magento module:enable Pyxl_SmartyStreets
    bin/magento setup:upgrade
    bin/magento cache:clean 
    
    
## Settings  
Navigate to **Stores** -> **Configuration** -> **Pyxl** ->  **SmartyStreets**

There are two features you can manage. 

Under **Validation** you can enable/disable the address validation feature and provide your Auth Token and ID.

Under **Autocomplete** you can enable/disable the autocomplete feature and include your website key. 

## Documentation
SmartyStreets PHP SDK Documentation can be found [here](https://smartystreets.com/docs/sdk/php)
SmartyStreets Javascript SDK Documentation can be found [here](https://smartystreets.com/docs/sdk/javascript)

## TODO
* Implement International capabilities for autocomplete
* Provide better handling and user experience if more than one candidate is returned in back-end validation.
* Include billing address form on checkout in autocomplete component
* Refactor some of the code to clean up duplicate efforts  

## Authors
* Joel Rainwater
