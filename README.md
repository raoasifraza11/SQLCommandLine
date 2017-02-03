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


## Create Database
``CREATE DATABASE IF NOT EXISTS widget_db``

## GRANT Privilegs
``GRANT ALL ON widget_db.* TO 'widget_cms'@'localhost'``<br>

## FLUSH
``FLUSH PRIVILEGES``<br>

## SHOW GRANTS FOR USER
``SHOW GRANTS FOR 'widget_cms'@'localhost'``<br>
``Grants for widget_cms@localhost  ``<br>
``GRANT USAGE ON *.* TO 'widget'@'localhost' IDENTIFIED BY PASSWORD '*6C8989366EAF75BB670AD8EA7A7FC1176A95CEF4'``<br>
``GRANT ALL PRIVILEGES ON `foo`.* TO 'admin'@'localhost'``<br>


## DROP USER
``DROP USER 'widget_cms'@'localhost'``

## DROP DATABASE
``DROP DATABASE IF EXISTS widget_db``

## USE DATABASE
``Use widegt_db;``

## Create Table
``CREATE TABLE admin (
      id INT(11) NOT NULL AUTO_INCREMENT,
      username varchar(50) NOT NULL,
      hash_password varchar(60) NOT NULL,
      primary key (id)
      );``
      
      