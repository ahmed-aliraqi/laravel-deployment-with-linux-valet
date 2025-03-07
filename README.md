# Laravel Development Guide

## Install Redis
https://redis.io/docs/getting-started/installation/install-redis-on-linux

## # add php repository 
```
sudo add-apt-repository ppa:ondrej/php

sudo apt update

sudo apt upgrade
```
## # Install php (7.1, 7.2, 7.3, 7.4, 8.0, 8.1, 8.2, 8.3 and 8.4)
```bash
sudo apt install -y unzip php7.1 php7.1-fpm php7.1-mbstring php7.1-cli php7.1-xml php7.1-bcmath php7.1-intl php7.1-sqlite3 php7.1-zip php7.1-mysql php7.1-gd php7.1-curl php7.1-pgsql php7.1-imagick php7.1-dom php7.1-mongodb php7.1-redis

sudo apt install -y unzip php7.2 php7.2-fpm php7.2-mbstring php7.2-cli php7.2-xml php7.2-bcmath php7.2-intl php7.2-sqlite3 php7.2-zip php7.2-mysql php7.2-gd php7.2-curl php7.2-pgsql php7.2-imagick php7.2-dom php7.2-mongodb php7.2-redis

sudo apt install -y unzip php7.3 php7.3-fpm php7.3-mbstring php7.3-cli php7.3-xml php7.3-bcmath php7.3-intl php7.3-sqlite3 php7.3-zip php7.3-mysql php7.3-gd php7.3-curl php7.3-pgsql php7.3-imagick php7.3-dom php7.3-mongodb php7.3-redis

sudo apt install -y unzip php7.4 php7.4-fpm php7.4-mbstring php7.4-cli php7.4-xml php7.4-bcmath php7.4-intl php7.4-sqlite3 php7.4-zip php7.4-mysql php7.4-gd php7.4-curl php7.4-pgsql php7.4-imagick php7.4-dom php7.4-mongodb php7.4-redis

sudo apt install -y unzip php8.0 php8.0-fpm php8.0-mbstring php8.0-cli php8.0-xml php8.0-bcmath php8.0-intl php8.0-sqlite3 php8.0-zip php8.0-mysql php8.0-gd php8.0-curl php8.0-pgsql php8.0-imagick php8.0-dom php8.0-mongodb php8.0-redis

sudo apt install -y unzip php8.1 php8.1-fpm php8.1-mbstring php8.1-cli php8.1-xml php8.1-bcmath php8.1-intl php8.1-sqlite3 php8.1-zip php8.1-mysql php8.1-gd php8.1-curl php8.1-pgsql php8.1-imagick php8.1-dom php8.1-mongodb php8.1-redis

sudo apt install -y unzip php8.2 php8.2-fpm php8.2-mbstring php8.2-cli php8.2-xml php8.2-bcmath php8.2-intl php8.2-sqlite3 php8.2-zip php8.2-mysql php8.2-gd php8.2-curl php8.2-pgsql php8.2-imagick php8.2-dom php8.2-mongodb php8.2-redis

sudo apt install -y unzip php8.3 php8.3-fpm php8.3-mbstring php8.3-cli php8.3-xml php8.3-bcmath php8.3-intl php8.3-sqlite3 php8.3-zip php8.3-mysql php8.3-gd php8.3-curl php8.3-pgsql php8.3-imagick php8.3-dom php8.3-mongodb php8.3-redis

sudo apt install -y unzip php8.4 php8.4-fpm php8.4-mbstring php8.4-cli php8.4-xml php8.4-bcmath php8.4-intl php8.4-sqlite3 php8.4-zip php8.4-mysql php8.4-gd php8.4-curl php8.4-pgsql php8.4-imagick php8.4-dom php8.4-mongodb php8.4-redis
```

## # Install mysql 8
```bash
sudo apt-get install mysql-server

sudo mysql_secure_installation
```
```
Validate Password Plugin ==> press no
Remove anonymous users? yes
Disallow root login remotely? yes
Remove test database and access to it? yes
Reload privilege tables now? yes
```
### Change mysql root password
```bash
sudo mysql -u root

ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY '';
EXIT;

sudo service mysql restart
```

### Install Valet For Linux
- Install OS Packages:
```bash
sudo apt-get install -y network-manager libnss3-tools jq xsel
```
- Install Valet Globally Via Composer CLI
```bash
composer global require cpriego/valet-linux
```
> Make sure to place Composer's system-wide vendor bin directory in your `$PATH`
- The `park` Command
  - Create a new directory on your machine by running something like `mkdir ~/Sites`. Next, `cd ~/Sites` and run `valet park`. This command will register your current working directory as a path that Valet should search for sites.
  - Next, create a new Laravel site within this directory: `laravel new blog`.
  - Open `http://blog.test` in your browser.



### Display PHP Info In Your Browser

```bash
mkdir ~/phpinfo && echo '<?php phpinfo();' > ~/phpinfo/index.php && cd ~/phpinfo && valet link
```
> Then go to `phpinfo.test` to see your current php version


### Switch between php versions use the following command:

##### PHP 7.1
```bash
valet use 7.1
```

##### PHP 7.2
```bash
valet use 7.2
```

##### PHP 7.3
```bash
valet use 7.3
```

##### PHP 7.4
```bash
valet use 7.4
```

##### PHP 8.0
```bash
valet use 8.0
```

##### PHP 8.1

```bash
valet use 8.1
```

##### PHP 8.2

```bash
valet use 8.2
```

##### PHP 8.3

```bash
valet use 8.3
```

