## Настало время прокачать вашу свежеустановленную ОС (Kubuntu)!

### Подключение партнёров Ubuntu:

`sudo software-properties-qt`

### Запускаем Терминал при помощи клавиатурной комбинации Ctrl-Alt-T и вставляем в него при помощи клавиатурной комбинации Ctrl-Shift-V строку. После вставки текста вводим Y и Enter.

### Локализуем ОС:

`sudo apt install -y aspell-ru language-pack-kde-ru language-pack-ru language-pack-ru-base myspell-ru language-pack-gnome-ru-base language-pack-gnome-ru firefox-locale-ru libreoffice-l10n-ru language-pack-gnome-ru-base language-pack-gnome-ru`

### В открывшемся окне установить флажки:

![GitHub Logo](images/Partners.png)

### Настройка раскладки клавиатуры. В Параметрах системы открыть пункт:

![GitHub Logo](images/key.png)

### Обновить ОС:

`sudo apt list --upgradable -a && sudo apt update && sudo apt full-upgrade && reboot -y`

### Установить приложения (открыть ссылку):

https://github.com/rurewa/Education/blob/main/UbuntuPumping/SoftInstall.md

### Информация об оборудовании с помощью Inxi:

*запуск этой программы в Терминале:*

`inxi -Fs`