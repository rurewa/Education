### Установка всех компонентов LAMP:

`sudo apt update && sudo apt install lamp-server^`

### Доустанавливаем необходимые компоненты:

`sudo apt install php libapache2-mod-php php-mysql php-opcache php-xml php-gd php-mbstring php-curl php-xmlrpc php-intl php-soap php-zip`

**Настройка сервера Apache2**

`systemctl status apache2`

`sudo systemctl start apache2`

`sudo systemctl enable apache2`

`apache2 -v`

### Oткрыть TCP-порт 80 и сохранить настройки:

`sudo iptables -I INPUT -p tcp --dport 80 -j ACCEPT && sudo apt update && sudo apt install iptables-persistent`

**Если вы используете брандмауэр UFW, выполните эту команду, чтобы открыть TCP-порт 80**

`sudo ufw allow http`

### Назначение прав на каталог с локальным сайтом:

`sudo chown www-data:www-data /var/www/html/ -R`

`sudo apache2ctl -t`

*будет ~ такой вывод:*

`AH00558: apache2: Could not reliably determine the server's fully qualified domain name, using 127.0.0.1. Set the 'ServerName' directive globally to suppress this messag

Syntax OK`

### Отредактируем конфигурационный файл:

`sudo nano /etc/apache2/conf-available/servername.conf`

*В открывшемся тектовом файле вставляем (Ctrl-Shift-V) это:*

`ServerName localhost`

*Сохраняем с помощью комбинации Ctrl-O и выходим из редактора по Ctrl-X*

### Ативировать конфигурационный файл:

`sudo a2enconf servername.conf`

`sudo systemctl reload apache2`

`sudo apache2ctl -t`

**Если хотите сложный пароль, то введите это (но для себя не советую, т.к. этот сервер будет ипользоваться только локально)**

`sudo mysql_secure_installation`

### Проверяем работу установленного Apache2:

http://localhost/index.html

**должна открыться веб-страница с информацией по версии Apache2**

### Диагностика установки LAMP: 

**Проверка версий установленных mysql и php:**

`mysql --version && php --version`

### Создаём файл проверки php:

`sudo nano /var/www/html/info.php`

*В открывшемся тектовом файле вставляем (Ctrl-Shift-V) это:*

`<?php
 phpinfo();
?>`

*Сохраняем с помощью комбинации Ctrl-O и выходим из редактора по Ctrl-X*

**Проверяем в браузере по адресу:**

http://localhost/info.php

**должна открыться веб-страница с информацией по версии PHP**

### Настрока php.ini

`sudo sed -i "s/memory_limit = .*/memory_limit = 512M/" /etc/php/7.4/apache2/php.ini`

`sudo sed -i "s/upload_max_filesize = .*/upload_max_filesize = 256M/" /etc/php/7.4/apache2/php.ini`

`sudo sed -i "s/post_max_size = .*/post_max_size = 256M/" /etc/php/7.4/apache2/php.ini`

`sudo sed -i "s/output_buffering = .*/output_buffering = Off/" /etc/php/7.4/apache2/php.ini`

`sudo sed -i "s/max_execution_time = .*/max_execution_time = 300/" /etc/php/7.4/apache2/php.ini`

`sudo sed -i "s/;date.timezone.*/date.timezone = UTC/" /etc/php/7.4/apache2/php.ini`

`sudo systemctl restart apache2`

### Установка phpmyadmin:

`sudo apt update && sudo apt install phpmyadmin`

**В появившемся окне Пробелом выбираем apache2, Tab-ом переключаемся между кнопками**

**В появившемся окне выбрать настройку с помощью dbconfig-common. Введите простой пароль**

### Диагностика сервера баз данных MySQL:

`sudo service mysql status`

**при запуске вы увидите зеленый активный статус**

### Создание нового пользователя test для phpmyadmin:

`sudo mysql -u root -p`

`CREATE USER 'test'@'localhost' IDENTIFIED BY 'пароль';`

`GRANT ALL PRIVILEGES ON *.* TO 'test'@'localhost';`

`FLUSH PRIVILEGES;`

**При помощи первых двух команд был создан новый пользователь с именем test, ему был присвоен пароль и предоставлены все возможные привилегии (такие как создание, удаление, редактирование баз данных, таблиц и т.д.). Третья команда обновляет заданные ранее привилегии.**

**чтобы выйти из режима sql нужно ввести команду**

`exit`

**Войти в интерфейс phpMyAdmin:**

http://localhost/phpmyadmin/

**в phpMyAdmin нужно создать новую и пустую базу данных (меню Базы данных)**

## Установка Joomla

## Загрузите дистрибутив Joomla с сайта:

https://downloads.joomla.org/

**распаковываем архив с Joomla в нужную папку**

`sudo unzip ~/Загрузки/Joomla_4.0.4-Stable-Full_Package.zip -d /var/www/html`

**удаляем тестовый файл, чтобы открылась страница установки Joomla:**

`sudo rm /var/www/html/index.html`

**Открываем в браузере страницу с адресом http://localhost**

**Указываем имя и логин администратора сайта (придумайте простое имя, типа admin)**

**Пароль не менее 12-и символов**

**На следующей странице указываем имя test и пароль базы данных**

**Если установка успешна, то необходимо удалить установочный каталог:**

`sudo rm -rf /var/www/html/installation/`

### Подробней про установку LAMP и Joomla:

https://linuxhostsupport.com/blog/how-to-install-joomla-3-9-on-ubuntu-20-04/

https://routerus.com/how-to-install-joomla-with-apache-on-ubuntu-18-04/

### Установка Joomla

https://joomlaportal.ru/russian-joomla

### Установка WordPress

https://ru.wordpress.org/download/#download-install