Настало время прокачать вашу свежеустановленную ОС!

![GitHub Logo](https://github.com/rurewa/Education/blob/main/UbuntuPumping/images/image12.png)

Выбираем Программы и обновления

![GitHub Logo](https://github.com/rurewa/Education/blob/main/UbuntuPumping/images/image1.png)

Устанавливаем флажки Партнёры Canonical

В соседней вкладке этого же окна уставливаем так, как на картинке:

![GitHub Logo](https://github.com/rurewa/Education/blob/main/UbuntuPumping/images/update_gui.png)

Запускаем Терминал при помощи клавиатурной комбинации Ctrl-Alt-T и вставляем в него при помощи клавиатурной комбинации Ctrl-Shift-V строку. После вставки текста вводим Y и Enter:

sudo apt list --upgradable -a && sudo apt update && sudo apt full-upgrade && reboot
Эта команда обновит и перезагрузит ОС.

Появится такое окно:

![GitHub Logo](https://github.com/rurewa/Education/blob/main/UbuntuPumping/images/image3.png)

После перезагрузки устанавливаем необходимые мультимедийные кодеки и шрифты (во время выполнения этой установки браузер лучше закрыть!):

sudo apt update && sudo apt install ubuntu-restricted-extras ttf-dejavu-core

В процессе установки программа задаёт пользователю вопросы, на которые нужно отвечать утвердительно (Yes), используя TAB и стрелки для перемещения и Enter.

![GitHub Logo](https://github.com/rurewa/Education/blob/main/UbuntuPumping/images/image5.png)


![GitHub Logo](https://github.com/rurewa/Education/blob/main/UbuntuPumping/images/image7.png)


Далее по списку:

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

Подробнее о дополнениях к KiCAD

https://progmatikus.livejournal.com/323678.html

Набор необходимых и полезных утилит:

sudo apt update && sudo apt install mc gdebi htop tree mesa-utils sl lm-sensors neofetch winbind wget curl ppa-purge inxi recoll net-tools xclip xsel

Настройки ОС:

sudo apt update && sudo apt install gnome-tweak-tool gnome-shell-extensions xdotool gconf-editor

Информация об оборудовании:

sudo apt update && sudo apt install inxi

Некоторые программы не поспевают за изменениями Ubuntu и некорректно попадают в трей. Исправить это можно установкой дополнения по ссылке:

https://extensions.gnome.org/extension/1503/tray-icons/

Установка русского языка и раскладки

Запусти настройки языка ОС:

![GitHub Logo](https://github.com/rurewa/Education/blob/main/UbuntuPumping/images/image2.png)

И обнови язык, соглашаясь на всё!

Настрой переключение языков на клавиатуре через Alt-Shift:

![GitHub Logo](https://github.com/rurewa/Education/blob/main/UbuntuPumping/images/image4.png)

![GitHub Logo](https://github.com/rurewa/Education/blob/main/UbuntuPumping/images/image9.png)

![GitHub Logo](https://github.com/rurewa/Education/blob/main/UbuntuPumping/images/image8.png)

Не закрывайте главное окно дополнительных настроек, выполнив:

![GitHub Logo](https://github.com/rurewa/Education/blob/main/UbuntuPumping/images/image10.png)

![GitHub Logo](https://github.com/rurewa/Education/blob/main/UbuntuPumping/images/image11.png)

![GitHub Logo](https://github.com/rurewa/Education/blob/main/UbuntuPumping/images/image6.png)

![GitHub Logo](https://github.com/rurewa/Education/blob/main/UbuntuPumping/images/addons_Gnome.png)

После того, как всё успешно установилось, перезагружаем ОС командой reboot в терминале!

Некоторые рекомендации относительно настройки ОС после прокачки:

Переместить значок Dash вверх/влево (команду выполнить в Терминале):

gsettings set org.gnome.shell.extensions.dash-to-dock show-apps-at-top true

![GitHub Logo](https://github.com/rurewa/Education/blob/main/UbuntuPumping/images/dash.png)

Приложений может оказаться много, и, чтобы легче ориентироваться в них, сгруппируйте их следующим образом:

![GitHub Logo](https://github.com/rurewa/Education/blob/main/UbuntuPumping/images/dash_show.png)

Если вам недостаточно имеющихся приложений, то посетите эту страницу для поиска и установки нужной вам программы:

https://progmatikus.livejournal.com/55550.html

Так же много приложений можно найти сдесь:

https://snapcraft.io/store

а установить приложения с сайта можно как на картинке:

![GitHub Logo](https://github.com/rurewa/Education/blob/main/UbuntuPumping/images/app_install_snap.png)

Ещё много приложений в Ubuntu Story:

![GitHub Logo](https://github.com/rurewa/Education/blob/main/UbuntuPumping/images/Find_Ubuntu_Store.png)
