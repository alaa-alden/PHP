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
###### virtual host :
  1. change path the website
      - create virtual sites :`sudo cp '/etc/apache2/sites-available/000-default.conf' /etc/apache2/sites-available/file.conf`
      - write in file.conf :`ServerAdmin info@winners.com`&&`ServerName winners.com`&&`ServerAlias www.winners.com`
      - in the same path for winners.com.conf
        - enable the file configure `sudo a2ensite new file.conf`
        - disable the file configure `sudo a2dissite old file.conf`
      - restart apache :    `sudo service apache2 restart`
  2. change name in url :
      - give any ip address that connection with the PC to  the virtual host by : for know what ip address maybe gave `ifconfig`  then `sudo nano /etc/hosts` then add `ip name `

  **so maybe create many website on the PC**
