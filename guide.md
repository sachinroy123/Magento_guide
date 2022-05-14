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
/**
 * Copyright © Magento, Inc. All rights reserved.
 * See COPYING.txt for license details.
 */

// phpcs:disable Magento2.Templates.ThisInTemplate

/** @var \Magento\Sales\Block\Order\Items $block */
$helper = $block->getData('cysque_helper');

?>
