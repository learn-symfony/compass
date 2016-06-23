# php Compass

this is a library extends scssphp package with compass stylesheets

 * A script that checks out Compass and extracts the SCSS
 * A PHP class that hooks into a instance of `scssc` from scssphp. This script
   updates the import path and adds built in functions required my Compass

Compass' SCSS is checked into this repository, so you only need to run the
extract script if you are updating the version of Compass that is included.

##Installation
```
composer require eugene-matvejev/compass
```
##Usage
```
<?php
   require "vendor/autoload.php";

   $scss = new scssc();
   new scss_compass($scss);

   echo $scss->compile('
       @import "compass";

       .shadow {
            @include box-shadow(10px 10px 8px red);
       }
   ');
```

##resources:
 * http://compass-style.org/
 * http://leafo.net/scssphp/

