Настало время прокачать вашу свежеустановленную ОС (Kubuntu)!

Запускаем Терминал при помощи клавиатурной комбинации Ctrl-Alt-T и вставляем в него при помощи клавиатурной комбинации Ctrl-Shift-V строку. После вставки текста вводим Y и Enter.

Локализуем ОС:

sudo apt install aspell-ru language-pack-kde-ru language-pack-ru language-pack-ru-base myspell-ru language-pack-gnome-ru-base language-pack-gnome-ru firefox-locale-ru libreoffice-l10n-ru language-pack-gnome-ru-base language-pack-gnome-ru

Подключение партнёров Ubuntu:

sudo software-properties-qt

В открывшемся окне установить флажки:

![GitHub Logo](https://github.com/rurewa/Education/blob/main/UbuntuPumping/images/Partners.png)

Настройка раскладки клавиатуры. В Параметрах системы открыть пункт:

![GitHub Logo](https://github.com/rurewa/Education/blob/main/UbuntuPumping/images/key.png)

Обновить ОС:

sudo apt list --upgradable -a && sudo apt update && sudo apt full-upgrade

Приложение для камеры и звукозаписи:

sudo apt update && sudo apt install guvcview gnome-sound-recorder gnome-clocks

Мессенджер Skype:

sudo snap install skype --classic

Программа видеоконференций ZOOM:

sudo snap install zoom-client

Telegram - отличный мессенжер!

sudo snap install telegram-desktop

Простой блокнот:

sudo apt update && sudo apt install mousepad

Читалка формата DJVI:

sudo apt update && sudo apt install djview4

Набор архиваторов:

sudo apt update && sudo apt install rar unrar p7zip-full arj

Простая рисовалка в духе Paint.net:

sudo snap install pinta

Поддержка Java (необходима для некоторых программ. Во время установки браузер лучше закрыть!):

sudo apt update && sudo apt install default-jre default-jdk

Диагностика и мониторинг ОС:

sudo apt-get update && sudo apt-get install stacer -y

Скриншотер (их много, но этот один из лучших):

sudo apt update && sudo apt install flameshot

Инструменты разработчика C++:

sudo apt update && sudo apt install build-essential git ghex gdb lldb micro

Для создания схем и разводки печатных плат KiCAD EDA:

sudo add-apt-repository --yes ppa:kicad/kicad-5.1-releases && sudo apt update && sudo apt install --install-recommends kicad kicad-demos && sudo apt install kicad-locale-ru

Подробнее о дополнениях к KiCADhttps://progmatikus.livejournal.com/323678.html

Набор необходимых и полезных утилит:sudo apt update && sudo apt install mc gdebi htop tree mesa-utils sl lm-sensors neofetch winbind wget curl ppa-purge inxi recoll net-tools xclip xsel xdotool

Информация об оборудовании:

sudo apt update && sudo apt install inxi

После того, как всё успешно установилось, перезагружаем ОС командой reboot в терминале!

Если вам недостаточно имеющихся приложений, то посетите эту страницу для поиска и установки нужной вам программы:

https://progmatikus.livejournal.com/55550.html

Так же много приложений можно найти сдесь:

https://snapcraft.io/store

Ещё много приложений в Ubuntu Story:

![GitHub Logo](https://github.com/rurewa/Education/blob/main/UbuntuPumping/images/Soft.png)