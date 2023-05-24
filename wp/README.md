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

# Replace the table prefix in wp-config.php
nano wp-config.php
# $table_prefix  = 'wp_910009_';
# Verify the table prefix
wp db prefix

# Install composer packages
composer install

# Check the remote configuration can be correctly displayed
composer show:config:prod

# Install the website locally.
# It is required to import a fresh database dump and will be overriden by the import:prod command. 
wp core install --url=http://localhost:8533 --title="My WP" --admin_user=admin --admin_password=password --admin_email=ad@m.in (http://--admin_email=ad@m.in/)

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

# Adjust .env variables for possible wp-starter plugin based.
cd wp-content/plugins/rdv-connector
cp .env.example .env
php artisan key:generate

# Run the server
cd -
wp server --port=8255
```
