# PHP

###### install apache and php and mysql :
  1. install apache :`sudo apt-get update` && `sudo apt-get install apache2`
    - test apache :  `sudo apache2ctl configtest`
      - for fix problem in not found server 127.0.0.1 : open `sudo nano /etc/apache2/apache2.conf` and write that`ServerName 127.0.0.1` in end of *apache2.conf*
    - for restart the apache `sudo systemctl restart apache2`  or `sudo apachectl restart`
  2. install mysql :`sudo apt-get install mysql-server`
  3. insatll php :`sudo apt-get install php libapache2-mod-php php-mcrypt php-mysql`
    - for advance in apache : open file.php at the first time :`sudo nano /etc/apache2/mods-enabled/dir.conf` and delete *index.php* then write *index.php* before *index.html* then `sudo systemctl restart apache2`
  4. install phpmyadmin :`sudo apt-get install phpmyadmin`
    - add phpmyadmin in apache :
      `sudo nano /etc/apache2/apache2.conf` then Add at the bottom >> `Include /etc/phpmyadmin/apache.conf` then `sudo apachectl restart`
