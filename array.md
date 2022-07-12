       Array and Object-------
       
       https://bitbucket.org/vivekkumar_cysque/ccommerce/src/dev/app/code/Cysque/Themes/Model/Api/ThemeConfig.php
       
       
       $response = [
            'status' => 200,
            'message' => 'Success',
            'data' => []
        ];
        
        
         **
 * Undocumented function
 *
 * @return array
 */
    public function getCollectionData()
    {
        $isEnabled = $this->isEnabled();
        $applyFor  = $this->getApplyFor();
        $threshold = $this->getThreshold();
        $loadingType = $this->getLoadingType();
        $resizeWidth = $this->getResizeWidth();
        $resizeHeight = $this->getResizeHeight();
        $placeholderType = $this->getPlaceholderType();

        // $getIcon = $this->getIcon();
        // $mediaUrl = $this->getMediaUrl();
        
        
        $collection =[
            'data' =>[]
        ];

        $collection['data'] =[
        'isEnabled'  => $isEnabled,
        'applyFor' => $applyFor,
        'threshold' => $threshold,
        'loadingType'  => $loadingType,
        'resizeWidth'  => $resizeWidth,
        'resizeHeight' => $resizeHeight,
        'placeholderType'  => $placeholderType
        ];

        return $collection;
    }
}
