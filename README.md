## magento-additional-pricing
** This adds additional pricing in PDP and Category pages

## Install
* download the zip file.
* Add it in root/app/code
* go to terminal root and type 
*`bin/magento module:enable F8_Pricing`

* `php bin/magento setup:upgrade && php bin/magento cache:flush && php bin/magento cache:clean`
* `php bin/magento indexer:reindex`
* `php bin/magento setup:di:compile`
* `php bin/magento setup:static-content:deploy -f`


* before install make sure this stuff is sorted out.
 
Please create the following 2 attributes in the products page in the 
* price_per_m2 = you can set it to text field if this is gonna be just to show the price.
* category_m2_price = make this attribute a yes/no enable/disbale attribute  



* Check this file

 This code to be added in this file in the theme or 
 extend it in the them and add this code 
 above the getPrice function to call the 
 second price in the category .

 After adding this code remove this file in this module

* This file = F8/Pricing/view/frontend/templates/product/list.phtml
