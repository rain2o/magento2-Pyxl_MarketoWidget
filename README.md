# Marketo Widget
Provides a new Magento widget which can be used to embed a Marketo form inside CMS Pages and Blocks.

## Getting Started
To install this module run the following.

If you **don't** have Pyxl_Core installed already run this first:

    composer config repositories.pyxl-core git git@bitbucket.org:pyxlinc/pyxl-core-extension.git
    composer require pyxl/core:dev-master
    bin/magento module:enable Pyxl_Core
    
Then require this package:

    composer config repositories.pyxl-marketowidget git git@bitbucket.org:pyxlinc/pyxl_marketowidget.git
    composer require pyxl/marketo-widget:dev-master
    bin/magento module:enable Pyxl_MarketoWidget
    bin/magento setup:upgrade
    bin/magento cache:clean 
    
    
## Settings
You will need to setup a few settings before using these widgets. 
* Navigate to **Stores** -> **Configuration** -> **Pyxl** ->  **Marketo Settings**
* In *Base URL* insert the base URL for your subscription. This can typically be found in the embed code. 
* In *Munchkin ID* insert your subscription Munchkin ID. 

## Widget
To use the widget use the Insert Widget function on any CMS Block or Page and choose **Marketo Form**. In the popup
put the Form ID in the field and save. Your form should populate when testing (after clearing cache). 

## Authors
* Joel Rainwater
