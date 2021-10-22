## Драйвера видеокарт

https://losst.ru/kak-posmotret-videokartu-v-linux

**Узнать производителя и название видеокарты:**

sudo update-pciids && lspci | grep -E "VGA|3D"

**Получить подробную информацию по видеокарте:**

sudo lshw -c video

**или:**

sudo apt install mesa-utils

**или объём видеопамяти:**

glxinfo -B

**Видеодрайвер:**

sudo lshw -c video | grep driver

### В случаес с гибритной графикой

**Определяем интегрированную видеокарту:**

lspci -nn | grep -E 'VGA|Display'

**Определяем дискретную видеокарту:**

glxinfo -B

**Определяем гибритную связку:**

lshw -short | grep -i  display

**Определяем испульзуемый драйвер для дискретной видеокарты:**

nvidia-detector

**Устанавливаем переключатель видеокарт:**

sudo apt install nvidia-prime

**Переключаем на дискретную видеокарту:**

sudo prime-select nvidia

**Определить поддержку 3D:**

glxinfo | grep OpenGL

### Проверка работоспособности видеоподсистемы с помощью бенчмарков.

### Шестерёнки:

**устанавливаем:**

sudo apt update && sudo apt install mesa-utils

*запускаем в терминале:* 

glxgears -info
