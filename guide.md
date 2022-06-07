Helper ->Data.php

use Magento\Framework\View\Element\Block\ArgumentInterface;

class Data extends AbstractHelper implements ArgumentInterface
{
 ......
}

layout file ...
    <body>
        <referenceBlock name="item_price">
            <action method="setTemplate">
                <argument name="template" xsi:type="string">Cysque_OrderItemImage::email/items/price/row.phtml</argument>

            </action>
            <arguments>
                <argument name="cysque_helper" xsi:type="object">Cysque\OrderItemImage\Helper</argument>
                </arguments>
        </referenceBlock>
    </body>





item.phtml

<?php

$helper = $block->getData('cysque_helper');

?>

-------------------------for getting system.xml value ------------- 
https://www.mageplaza.com/magento-2-module-development/create-system-xml-configuration-magento-2.html#42-create-a-helper-file-standard


Create file: app/code/Mageplaza/HelloWorld/Helper/Data.php

<?php

namespace Mageplaza\HelloWorld\Helper;

use Magento\Framework\App\Helper\AbstractHelper;
use Magento\Store\Model\ScopeInterface;

class Data extends AbstractHelper
{
// hellowordl -> section id ,
//  general    -> group id ,
//   enable    -> field id ,

	const XML_PATH_HELLOWORLD = 'helloworld/';

	public function getConfigValue($field, $storeId = null)
	{
		return $this->scopeConfig->getValue(
			$field, ScopeInterface::SCOPE_STORE, $storeId
		);
	}

	public function getGeneralConfig($code, $storeId = null)
	{

		return $this->getConfigValue(self::XML_PATH_HELLOWORLD .'general/'. $code, $storeId);
	}

}
