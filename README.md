# pscomposergs
###7 The composer.json file
compoer.json
```
{
  "name":"",
  "require":{
    "php",">5.6",
    "pear/text_password":"^1.2"
  },
  "require-dev":{
    "phpunit/phpunit":"*"
  }
}
```
update, nodev
```
composer install --no-dev
composer update
```
###8
```
composer show  //all installed packages
```

###9 The composer.lock
```
composer show -t
```

###10 Find packages
```
composer require //then type pak name
```
## Composer Scripts
###16 Composer events
```
{
  "scripts":{
    "post-update-cmd":"Vendor\\Class::method",
    "post-package-install":["Vendor\\Class::method"],
    "post-install-cmd":[
      "Vendor\\Class::method",
      "phpunit -c app/"
    ]
  }
}
```

###17 Custom Commands
```
{
  "scripts":{
    "clearCache":"rm -rf cache/*",
    "test":[
      "@clearCache",
      "phpunit"
    ]
  }
}
```
run
```
composer test
```
