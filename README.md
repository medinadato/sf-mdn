sf-mdn
======

# MDN Symfony

    Base for new projects using symfony

## Virtual Host
    <VirtualHost *:80>
        ServerName local.sf-mdn
        DocumentRoot "/var/www/sf-mdn/web"

        <Directory "/var/www/sf-mdn/web">
                SetEnv APPLICATION_ENV "development"
                Options Indexes Multiviews FollowSymLinks
                AllowOverride All
                Order allow,deny
                Allow from all

                RewriteEngine On
                RewriteCond %{REQUEST_FILENAME} !-f
                RewriteRule !\.(js|ico|gif|jpg|png|css|htm|html|txt|mp3)$ index.php
        </Directory>
    </VirtualHost>