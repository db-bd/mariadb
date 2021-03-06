## Mariadb Windows Portable Install Alongside MySQL
* Download Maria DB from [downloads.mariadb.org](https://downloads.mariadb.org/)
* Extract Maria DB e.g ` D:\Database\Mariadb `
* From bin directory run command
```sh
mysql_install_db.exe
```
* This will create a my.ini in ` data ` directory
* Again from bin directory
```sh
 mysqld --console
```
* This is hold terminal in running mode of ` mysqld `
* Again from bin
```sh
mysql -uroot
```
* Create a user ` admin `
```sh
CREATE USER admin@localhost IDENTIFIED BY 'nopass';
```
* Make MariaDB Service
```sh
mysqld --install-manual MariaDB
```

* If we want to install `MariaDB` alongside `MySQL` then Change `MySQL` Default port `3306` to `3360`
```sh
mysqld --install-manual MariaDB --port=3360
```

* Start Stop MariaDB Service
```sh
net start MariaDB [aka mariadb]
net stop MariaDB  [aka mariadb]
```
* Connect & version check
```sh
mysql -uadmin -pnopass
SHOW VARIABLES LIKE '%version%'
```
