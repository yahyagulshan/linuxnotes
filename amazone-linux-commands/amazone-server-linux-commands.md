### install mysql 
---

- *wget https://repo.mysql.com/yum/mysql-5.7-community/el/6/x86_64/mysql-community-devel-5.7.38-1.el6.x86_64.rpm*
- *rpm --import https://repo.mysql.com/RPM-GPG-KEY-mysql-2022*
- *sudo yum install mysql-community-server*
- *sudo systemctl start mysqld.service*
- *sudo grep 'temporary password' /var/log/mysqld.log*

- *CREATE DATABASE test2_db DEFAULT CHARACTER SET utf8 COLLATE utf8_unicode_ci;*
- *CREATE USER 'test2_user'@'%' IDENTIFIED BY '123sklHDJD3444';*
- *GRANT ALL PRIVILEGES ON test2_db.* TO 'test2_user'@'%';*

---
### install apache on amazon linux

- *sudo yum install httpd*
---
### install wordpress

- *wget http://wordpress.org/latest.tar.gz*
- *tar -xzvf latest.tar.gz*
- *mv *.* ..*
- *cd wordpress/*
- *mv wp-config-sample.php wp-config.php*
- *vi wp-config.php (here change the db configuration)*
- *service httpd restart*

---
### install php new version

- *sudo yum install amazon-linux-extras*
- *sudo  amazon-linux-extras | grep php*
- *sudo amazon-linux-extras enable php7.4*
- *yum install php-cli php-pdo php-fpm php-json php-mysqln*
- *php --version*
- *service httpd restart*
