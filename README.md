# Nginx configuration for running Shopware

This is an example configuration from running [Shopware](https://github.com/shopware/shopware) using
[nginx](http://nginx.org). Which is a high-performance non-blocking HTTP server.

This configuration is heavily inspired by [perusio's](https://github.com/perusio/drupal-with-nginx/) drupal-configuration.

## Warning
Please only use nginx if you know what you are doing. Shopware AG is not officially supporting nginx. 
Also note that Shopware will not run faster with nginx. A properly configured apache webserver is in most cases as fast as nginx.

## Compatibility
This configuration is tested with Shopware 5.1 or later.

## Installation

1. Move the old `/etc/nginx` directory to `/etc/nginx.old`.
2. Clone the git repository from github:

    ```
    git clone https://github.com/bcremer/shopware-with-nginx.git /etc/nginx
    ```
    
3. Setup the PHP-FPM upstream in `conf.d/upstream.conf`
4. Edit or copy the `sites-available/example.com.conf` configuration file to suit your requirements.
5. Enable your site configuration

    ```
    ln -s ../sites-available/example.com.conf /etc/nginx/sites-enabled/
    ```
    
6. Reload nginx
