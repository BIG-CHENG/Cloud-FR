# laravel
laravel

bug: access root ok, failed to route elsewhere (php artisan serve also ok)
solution: need overwrite
1. add overwirte in /etc/apache2/site_avaliable/000-default
        <Directory "/var/www/html/wwwai/public">
                Allowoverride All
        </Directory>

2. enable rewrite
sudo a2enmod rewrite
sudo service apache2 restart

3. (optional) add .htaccess
