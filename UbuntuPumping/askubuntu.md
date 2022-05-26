## Драйвера видеокарт

**ссылка на мануал с описанием**

https://losst.ru/kak-posmotret-videokartu-v-linux

**Сначала проверим все доступые пропиетарные драйвера для вашей системы**

`sudo ubuntu-drivers autoinstall`

**обновим имеющиеся...**

`sudo apt-cache policy linux-firmware && sudo apt install linux-firmware`

**Узнать производителя и название видеокарты:**

`sudo update-pciids && lspci | grep -E "VGA|3D"`

**Получить подробную информацию по видеокарте:**

`sudo lshw -c video`

**или:**

`sudo apt install mesa-utils`

**или объём видеопамяти:**

`glxinfo -B`

**Видеодрайвер:**

`sudo lshw -c video | grep driver`

### В случаес с гибритной графикой

**Определяем интегрированную видеокарту:**

`lspci -nn | grep -E 'VGA|Display'`

**Определяем дискретную видеокарту:**

`glxinfo -B`

**Определяем гибридную связку:**

`lshw -short | grep -i  display`

**Определяем испульзуемый драйвер для дискретной видеокарты:**

`nvidia-detector`

**Устанавливаем переключатель видеокарт:**

`sudo apt install nvidia-prime`

**Переключаем на дискретную видеокарту:**

`sudo prime-select nvidia`

**Настроить видеокарту с помощью графической утилиты:**

`sudo nvidia-settings`

**Смотреть состояние видеокарты:**

`nvidia-smi`

**Почитать дополнительно:**

https://linuxize.com/post/how-to-nvidia-drivers-on-ubuntu-20-04/

**Определить поддержку 3D:**

`glxinfo | grep OpenGL`

### Проверка работоспособности видеоподсистемы с помощью бенчмарков.

### Шестерёнки:

**устанавливаем:**

`sudo apt update && sudo apt install mesa-utils`

*запускаем в терминале:* 

`glxgears -info`

### Если возникли проблемы с разрешением экрана на внешнем мониторе

https://linuxnow.ru/view.php?id=103

### Если драйвер nvidia не устанавливется (ошибка установки), то устанавливаем из этого ppa:

https://launchpad.net/~kelebek333/+archive/ubuntu/nvidia-legacy

### Установка альтернативного Терминала по умолчанию

`sudo update-alternatives --config x-terminal-emulator`

**выбираем в появившемся меню нужные Терминалы по номеру размещения, например 3**

### Обслуживание ОС

**Очистка кеши и удаление ненужных пакетов apt**

`sudo apt autoclean && sudo apt autoremove`

**попробовать исправить битые пакеты**

`sudo apt -f install`

**попробовать исправить битые пакеты**

`sudo dpkg --configure -a`

`sudo apt upgrade --fix-missing && sudo apt update`

`sudo apt --fix-broken install && sudo apt update`

** Переустановить LibreOffice**

`sudo apt-get install --reinstall libreoffice libreoffice-core`

**Очистка кеша flatpak:**

`flatpak uninstall --unused && sudo rm -rfv /var/tmp/flatpak-cache-*`

### Решение проблемы с ошибкой Busybox

https://itisgood.ru/2020/08/07/kak-ispravit-oshibku-busybox-initramfs-na-ubuntu/

### Решения проблем с WiFi

**Если после устновки Linux на базе Ubuntu WiFi не заработал, или работает плохо, обновите стек ядра Linux:**

`sudo apt install --install-recommends linux-generic-hwe-20.04`

#### Диагностика неисправностей с WiFi

**Проверьте пинг:**

`ping ya.ru`

**Определить установленный модуль WiFi:**

`lspci -knn | egrep 'Eth|Net'`

**Если у вас  RTL8188 (этими чипами часто комплектуются TP-LINK), то выполните это:**

`cd ~ ; git clone https://github.com/aircrack-ng/rtl8188eus && cd rtl8188eus/ && echo 'blacklist r8188eu'|sudo tee -a '/etc/modprobe.d/realtek.conf' &&  make && sudo make install`
