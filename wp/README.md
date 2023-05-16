# PLACEHOLDER

Wordpress website PLACEHOLDER

## Getting started

```shell
# Install the core
wp core download

# Configure the database
wp core config --dbhost=localhost --dbname=PLACEHOLDER --dbuser=root --dbpass=root

# Create the database
wp db create
wp db check

# This will create a wp-config.php
# replace the value
# $table_prefix  = 'wp_910009_';
# cat ~/sites/PLACEHOLDER.ch/wp-config.php
nano wp-config.php

# Make sure composer is used and install npm packages
composer install

# Check the remote configuration can be correctly displayed
composer show:config:prod

# Import the website
composer import:prod

# Install the plugins
# ls ~/sites/PLACEHOLDER.ch/wp-content/plugins
wp plugin install duplicate-post
wp plugin install honeypot
wp plugin install instant-images
wp plugin install woocommerce
wp plugin install wordpress-importer
wp plugin install wp-super-cache
# ...

# Remove the local themes and download the remote ones.
rm -rf wp-content/themes
rsync -av avgo_admin@avgo.ftp.infomaniak.com:~/sites/PLACEHOLDER.ch/wp-content/themes wp-content

# Run the server
composer dev
```
