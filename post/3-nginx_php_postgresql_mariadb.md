## 安装 nginx + php + postgresql + mariadb 

  ### 安装nginx+php 
```  
  sudo dnf install nginx php php-common php-fpm php-cli php-opcache php-pear php-pecl-mongodb php-pecl-apcu php-pecl-redis php-pecl-memcache php-pecl-memcached php-pecl-zip php-gd php-mbstring php-mcrypt php-xml php-pdo php-mysqlnd php-pgsql -y

  systemctl stop httpd.service
```
设置nginx和php-fpm随系统自动启动
```
  systemctl enable nginx.service php-fpm.service
```
修改nginx配置文件已支持php-fpm
```
  sudo vim /etc/nginx/nginx.conf
```
在http块中添加
```
  include /etc/nginx/conf.d/*.conf;
```
然后修改server配置指令，将php文件请求转发给php-fpm

启动nginx和php-fpm
```
  systemctl start nginx.service php-fpm.service
```
安装composer
```
php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"
php composer-setup.php
sudo mv composer.phar /usr/local/bin/composer
```
设置国内代理地址
```
composer config -g repo.packagist composer https://packagist.phpcomposer.com
```
  ### 安装 postgresql 
详细步骤 []: <https://www.postgresql.org/download/linux/redhat/>
```
sudo dnf install postgresql postgresql-server postgresql-contrib postgresql-devel
sudo postgresql-setup initdb -y
```
修改/var/lib/pgsql/data/pg_hba.conf和/var/lib/pgsql/data/postgresql.conf

修改postgres密码
```
sudo -u postgres psql
postgres=# ALTER USER postgres WITH PASSWORD 'pzzrudlf';
postgres=# \q
``` 
(linux系统postgres用户密码)
```
sudo passwd -d postgres
sudo passwd -u postgres 
```
### 安装 mariadb
```shell
sudo dnf install mariadb mariadb-server
/usr/bin/mysql_secure_installation
```

