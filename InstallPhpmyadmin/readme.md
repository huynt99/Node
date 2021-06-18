# install phpmyadmin in nginx
sudo apt-get update
*** 
sudo mysql;
UNINSTALL COMPONENT "file://component_validate_password";
***

sudo apt install phpmyadmin
web server to reconfig auto -> <oke> hoặc ấn esc
dbconfig-common -> <yes>
password -> <ok>

sudo ln -s  /usr/share/phpmyadmin /var/www/html/phpmyadmin
sudo chmod 775 -R /usr/share/phpmyadmin/
sudo chown root:www-data -R /usr/share/phpmyadmin/

sudo nano /etc/nginx/sites-available/default
-> add index.php
-> xóa comment  location ~ \.php$ {} và location ~ /\.ht {}
sudo service nginx restart
