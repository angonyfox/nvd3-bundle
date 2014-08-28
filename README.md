Bundle for using NVD3 (https://github.com/novus/nvd3.git) with symfony

Installation
------------

1. Add bundle as a dependency to the composer.json

``` json
{
    "require": {
        "pandora/nvd3-bundle": "dev-master"
    }
}
```
2. Run "composer update"
3. Make sure to enable PandoraNVD3Bundle and SpBowerBundle in AppKernel.php .
``` php
public function registerBundles()
{
    $bundles = array(
        // ...
        new Pandora\NVD3Bundle\PandoraNVD3Bundle(),
        new Sp\BowerBundle\SpBowerBundle(),
    );
}
```
4. Update app/config/config.yml
``` yml
# app/config/config.yml
sp_bower:
    bundles:
        PandoraNVD3Bundle: ~
```
5. Install bower dependencies
```
app/console sp:bower:install
```
6. Install asset
```
app/console assets:install --symlink
```
