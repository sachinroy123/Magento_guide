for error reporting 
  -> go to app
       ->boostrap.php
       
                   error_reporting(E_ALL);
                    ini_set('display_errors', 1);
                    
 
 
 * After that Set default to developer mode 
   for that you have to follow these steps 
   open terminal on root directory------
   mage2->
      ->   sudo chmod -R 777 .
      ->   sudo f generated/metadata/* generated/code/*
      ->    bin/magento deploy:mode:set developer
