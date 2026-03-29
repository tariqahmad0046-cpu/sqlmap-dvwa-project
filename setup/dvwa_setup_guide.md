# DVWA Setup Guide

## Install DVWA
cd /var/www/html
sudo git clone https://github.com/digininja/DVWA.git

## Permissions
sudo chmod -R 777 DVWA

## Configure Database
cd DVWA/config
cp config.inc.php.dist config.inc.php

Edit:
- username = root
- password = (blank or your password)

## Restart services
sudo systemctl restart apache2
sudo systemctl restart mysql

## Open in browser
http://localhost/DVWA
