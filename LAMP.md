### Установка всех компонентов LAMP:

`sudo apt update && sudo apt install lamp-server^`

`apt install php libapache2-mod-php php-mysql php-opcache php-xml php-gd php-mbstring php-curl php-xmlrpc php-intl php-soap php-zip`

*Next, we will have to tweak some values in the PHP configuration file (php.ini). Open the PHP configuration file (/etc/php/7.4/apache2/php.ini) and modify the following values:*

`memory_limit – Minimum: 64M Recommended: 128M or higher
upload_max_filesize – Minimum: 30M
post_max_size – Minimum: 30M
max_execution_time: Recommended: 30
Save the php.ini file and restart the web server for the changes to take effect`

`systemctl status apache2`

`sudo systemctl start apache2`

`sudo systemctl enable apache2`

`apache2 -v`

### Если вы используете брандмауэр UFW, выполните эту команду, чтобы открыть TCP-порт 80.

`sudo iptables -I INPUT -p tcp --dport 80 -j ACCEPT`

`sudo ufw allow http`

### Назначение прав на каталог с локальным сайтом:

`sudo chown www-data:www-data /var/www/html/ -R`

`sudo apache2ctl -t`

*будет ~ такой вывод:*

AH00558: apache2: Could not reliably determine the server's fully qualified domain name, using 127.0.0.1. Set the 'ServerName' directive globally to suppress this messag

`sudo nano /etc/apache2/conf-available/servername.conf`

*В открывшемся тектовом файле вставляем это:*

`ServerName localhost`

### Ативировать конфигурационный файл:

`sudo a2enconf servername.conf`

`sudo systemctl reload apache2`

`sudo apache2ctl -t`

`sudo mysql_secure_installation`

### Проверяем работу установленного Apache2:

http://localhost/index.html

### Проверка версий установленных mysql и php:

`mysql --version && php --version`

### Создаём файл проверки php:

`sudo nano /var/www/html/info.php`

http://localhost/info.php

### Установка phpmyadmin:

`sudo apt update && sudo apt install phpmyadmin`

`sudo apt -y install php-mbstring`

### Создание нового пользователя phpmyadmin:

`sudo mysql -u root -p`

`CREATE USER 'test'@'localhost' IDENTIFIED BY 'пароль';``

`GRANT ALL PRIVILEGES ON *.* TO 'test'@'localhost';``

`FLUSH PRIVILEGES;``

**При помощи первых двух команд был создан новый пользователь с именем test, ему был присвоен пароль и предоставлены все возможные 
привилегии (такие как создание, удаление, редактирование баз данных, таблиц и т.д.). Третья команда обновляет заданные ранее привилегии.**

`чтобы выйти из режима sql нужно ввести команду exit`

*Войти в интерфейс phpMyAdmin:*

http://localhost/phpmyadmin/

### Установка Joomla