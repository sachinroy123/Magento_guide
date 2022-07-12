       Array and Object-------
       
       https://bitbucket.org/vivekkumar_cysque/ccommerce/src/dev/app/code/Cysque/Themes/Model/Api/ThemeConfig.php
       
       
       $response = [
            'status' => 200,
            'message' => 'Success',
            'data' => []
        ];
        
        
           public function getThemeConfigValues()
            {
          return [
            'enabled' => $this->helper->getThemeConfigValue('general', 'enabled'),
            'rtl' => $this->helper->getThemeConfigValue('general', 'rtl'),
            'header'=> [
                'logo' => $this->getThemeConfigImageUrl('header', 'header_logo'),
                'maxWidth' => $this->helper->getThemeConfigValue('header', 'logo_max_width'),
                'maxHeight' => $this->helper->getThemeConfigValue('header', 'logo_max_height'),
            ],
            'footer' => [
                'logo' => ($this->helper->getThemeConfigValue('footer', 'footer_logo'))?
                    $this->getThemeConfigImageUrl('footer', 'footer_logo') : '',
                'links' => $this->helper->getSerializeArray($this->helper->getThemeConfigValue('footer', 'footer_links')),
                'social' => $this->helper->getSerializeArray($this->helper->getThemeConfigValue('footer', 'social_media')),
                'paymentIcon' => ($this->helper->getThemeConfigValue('footer', 'enabled_payment_icon'))?
                    $this->getThemeConfigImageUrl('footer', 'payment_icon') : '',
            ],
