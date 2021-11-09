### Установка всех компонентов LAMP:

`sudo apt update && sudo apt install lamp-server^`

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