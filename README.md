# SQLCommandLine

## How to Install MySQL on Ubuntu and CentOS
If you don't have MySQL installed on your droplet, you can quickly download it.<br>
``sudo apt-get install mysql-server``<br>

## How to Access the MySQL shell
Once you have MySQL installed on your droplet, you can access the MySQL shell by typing the following command into terminal:<br>
``mysql -u root -p``<br>

### while starting sql problem on linux and Kali (through Socket)
Please run these command<br>
``ps -A|grep mysql``<br>
``sudo pkill mysql``<br>
``ps -A|grep mysqld``<br>
``sudo pkill mysqld``<br>
``service mysql restart``<br>
``mysql -u root -p``<br>

## Show All USERS
``SELECT * FROM mysql.user;``<br>

## Create USER
``CREATE USER 'widget_cms'@'localhost' IDENTIFIED BY 'mypass'``<br>

## Show Database
`` SHOW DATABASES;``
