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

**Определяем гибритную связку:**

`lshw -short | grep -i  display`

**Определяем испульзуемый драйвер для дискретной видеокарты:**

`nvidia-detector`

**Устанавливаем переключатель видеокарт:**

`sudo apt install nvidia-prime`

**Переключаем на дискретную видеокарту:**

`sudo prime-select nvidia`

**Определить поддержку 3D:**

`glxinfo | grep OpenGL`

### Проверка работоспособности видеоподсистемы с помощью бенчмарков.

### Шестерёнки:

**устанавливаем:**

`sudo apt update && sudo apt install mesa-utils`

*запускаем в терминале:* 

`glxgears -info`

### Установка альтернативного Терминала по умолчанию

`sudo update-alternatives --config x-terminal-emulator`

**выбираем в появившемся меню нужные Терминал по порядку размещения, например 3**

### Решение проблемы с ошибкой Busybox

https://itisgood.ru/2020/08/07/kak-ispravit-oshibku-busybox-initramfs-na-ubuntu/
