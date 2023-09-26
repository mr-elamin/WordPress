1- How to fix maximum upload and php memory limit issues in WordPress ?
Open .htaccess file and added the following into a newline at the end of the file.

php_value upload_max_filesize 256M
php_value post_max_size 256M
php_value memory_limit 256M

--------------------------------------------------

2- How to fix pfsense HAProxy Problem ?

open wp-config.php file and add the following right after <?php

<?php

// force SSL
$_SERVER['HTTPS']='on';

define('WP_HOME','http://your-website-here.net');
define('WP_SITEURL','www.your-website-here.net');


-----------------------------

3- For W3 Total Cache to discover Redis, it is necessary to fill in 
some variables in the mysite/wordpress/data/wp_config.php file, just before configuring the SQL database.

//
// redis config cache for total cache
//
define( 'W3TC_CONFIG_CACHE_ENGINE', 'redis');
define( 'W3TC_CONFIG_CACHE_REDIS_SERVERS', 'redis::6384' );
// optional redis settings
define( 'W3TC_CONFIG_CACHE_REDIS_PERSISTENT', true );
define( 'W3TC_CONFIG_CACHE_REDIS_DBID', 0 );
define( 'W3TC_CONFIG_CACHE_REDIS_PASSWORD', '' );



------------------------------------
phpmyadmin
login name root and password is MYSQL_ROOT_PASSWORD=database-root-password-here
server field should be left empty