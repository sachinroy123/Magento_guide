# Magento_guide


https://docs.magento.com/user-guide/catalog/product-types.html
@Sachin read this blog to understand the different types of products in Magento 2.

Unlock 11 Necessary Design Patterns for Every Magento 2 Developer
https://bsscommerce.com/confluence/magento-2-design-patterns/


Magento 2 Create View: Block, Layouts, Templates
https://www.mageplaza.com/magento-2-module-development/view-block-layout-template-magento-2.html

Model and resouce models
https://www.codilar.com/magento-2-models-resource-models-and-collections

css
https://devdocs.magento.com/guides/v2.4/frontend-dev-guide/css-topics/css-themes.html


CRUD
https://dolphinwebsolution.com/how-to-perform-crud-operation-with-a-custom-module-in-magento-2


ORDER IMAGE..
http://vijaymrami.blogspot.com/2020/10/how-to-display-product-image-in-backend.html

template override 
https://www.mageplaza.com/devdocs/overriding-native-template-file-magento-2.html#new-method

difference checker...
https://www.diffchecker.com/diff

Search thoughout module ----
grep -r "table-order-items shipment" vendor/magento/module-sales

how to check class 

                  <?php   
                      print_r(get_class($block));
                      die();
                  ?>

---- SETUP MODULE TABLE ------
setup_module // all the module store in this table...

/**
 * Cysque Software.
 *
 * @category  Cysque
 * @package   Cysque_AdminLoginAsCustomer
 * @author    Cysque Software
 * @copyright Copyright © Cysque Software (https://cysque.com)
 * @license   https://store.cysque.com/terms-conditions
 */
 
 show the errors and warning....
 
 ../magento-coding-standard/vendor/bin/phpcs --standard=Magento2 app/code/Cysque/OrderItemImage/
 
../magento-coding-standard/vendor/bin/phpcs -n --standard=Magento2 app/code/Cysque/OrderItemImage/

removing white space 
../magento-coding-standard/vendor/bin/phpcbf  --standard=Magento2 app/code/Cysque/OrderItemImage/

permission 🚱
sudo chmod -R 777 var/;
sudo chmod -R 777 pub/;
sudo chmod -R 777 generated/;

