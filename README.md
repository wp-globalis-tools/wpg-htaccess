# htaccess sample for WordPress

## Installation

1. Go in your website directory and run `curl -O https://raw.githubusercontent.com/wp-globalis-tools/wpg-htaccess/master/wpg-htaccess .htaccess`
2. Find / Replace `<WP_SITE_DIR>` with your site root directory

## Examples

1. Development environment: `sed -i "s,<WP_SITE_DIR>,/foo/my_project,g" .htaccess`
2. Production environment: `sed -i "s,<WP_SITE_DIR>,/,g" .htaccess`

## Further explanations

Many things were taken from [roots/wp-h5bp-htaccess](https://github.com/roots/wp-h5bp-htaccess) project. Please read it for a complete htaccess optimization understanding.
