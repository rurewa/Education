## Настало время прокачать вашу свежеустановленную ОС (Kubuntu)!

### Подключение партнёров Ubuntu:

`sudo software-properties-qt`

### В открывшемся окне установить флажки:

![GitHub Logo](images/Partners.png)

### Запускаем Терминал при помощи клавиатурной комбинации Ctrl-Alt-T и вставляем в него при помощи клавиатурной комбинации Ctrl-Shift-V строку. После вставки текста вводим Y и Enter.

### Обновить ОС:

`sudo apt list --upgradable -a && sudo apt update && sudo apt full-upgrade -y && reboot`

*Эта команда обновит и перезагрузит ОС.*

### Локализуем ОС:

`sudo apt install -y aspell-ru language-pack-kde-ru language-pack-ru language-pack-ru-base myspell-ru language-pack-gnome-ru-base language-pack-gnome-ru firefox-locale-ru libreoffice-l10n-ru language-pack-gnome-ru-base language-pack-gnome-ru`

### Настройка раскладки клавиатуры. В Параметрах системы открыть пункт:

![GitHub Logo](images/key.png)

### Установить приложения (открыть ссылку):

https://github.com/rurewa/Education/blob/main/UbuntuPumping/SoftInstall.md