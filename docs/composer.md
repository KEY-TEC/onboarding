# Composer
## Installation mit Composer
```
fin rc --image=docksal/cli:2.13-php7.4 composer create-project drupal/recommended-project PROJECT_NAME
```
### Composer Pitfals.
#### Patches über composer
```
fin exec composer require cweagans/composer-patches
```
``` 
        "patches": {
            "drupal/core": {
                "Fix broken theme suggestions for views.": "https://www.drupal.org/files/issues/2020-11-23/2118743-190.patch"
            }
        },
``` 
#### Client side libraries
``` 
fin exec composer require oomphinc/composer-installers-extender
``` 
  ```
  "repositories": {
    "asset-packagist": {
      "type": "composer",
      "url": "https://asset-packagist.org"
    },
   
    "drupal": {
      "type": "composer",
      "url": "https://packages.drupal.org/8"
    },
  },
```
  ```
  "installer-types": [
    "bower-asset",
    "npm-asset",
    "test"
],
        
```
```
"web/libraries/{$name}": [
    "type:drupal-library",
    "type:npm-asset",
    "type:bower-asset"
],
```
