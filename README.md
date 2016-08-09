# htaccess sample for WordPress

## Installation

1. Go in your website directory and run `curl -O https://raw.githubusercontent.com/wp-globalis-tools/wpg-htaccess/master/wpg-htaccess .htaccess`
2. Find / Replace `<WP_SITE_DIR>` with your site root directory
3. Flush WordPress permalinks : `wp rewrite structure "/%postname%/" && wp rewrite flush --hard`

## Examples

1. Development environment: `sed -i "s,<WP_SITE_DIR>,/foo/my_project,g" .htaccess`
2. Production environment: `sed -i "s,<WP_SITE_DIR>,/,g" .htaccess`

## Note

Depending on your wp-cli configuration, flushing permalinks in command line could require some extra settings.
We recommand to add 2 lines to your project wp-cli configuration file, before the flush operation :
```
echo "apache_modules:" >> wp-cli.local.yml
echo "  - mod_rewrite" >> wp-cli.local.yml
```

## Further explanations

Many things were taken from [roots/wp-h5bp-htaccess](https://github.com/roots/wp-h5bp-htaccess) project. Please read it for a complete htaccess optimization understanding.
