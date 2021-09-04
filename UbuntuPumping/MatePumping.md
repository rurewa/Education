## Прокачка Ubuntu Mate

### Запускаем Терминал при помощи клавиатурной комбинации Ctrl-Alt-T и вставляем в него при помощи клавиатурной комбинации Ctrl-Shift-V строку. 

*После вставки текста вводим Y и нажимаем Enter:*

sudo apt list --upgradable -a && sudo apt update && sudo apt full-upgrade && reboot

*Эта команда обновит и перезагрузит ОС.*

### После перезагрузки устанавливаем необходимые мультимедийные кодеки и шрифты (во время выполнения этой установки браузер лучше закрыть!):

sudo apt update && sudo apt install ubuntu-restricted-extras ttf-dejavu-core

### Появится такое окно:

![GitHub Logo](images/image3.png)

*В процессе установки программа задаёт пользователю вопросы, на которые нужно отвечать утвердительно (Y/Да), используя TAB и стрелки для перемещения и Enter.*

![GitHub Logo](images/image5.png)

![GitHub Logo](images/image7.png)

### Далее по списку:

### Приложения для камеры и звукозаписи:

sudo apt update && sudo apt install guvcview gnome-sound-recorder gnome-clocks

### Программа для работы с веб-камерой:

sudo apt update && sudo apt install guvcview

### Gifex - GIF запись с экрана в Linux

sudo snap install gifex

### Программа для загрузки видео с таких сайтов (YouTube etc.):

sudo snap install video-downloader

### TeamViewer для Linux для удалённого доступа и поддержки через Интернет:

http://www.teamviewer.com/ru/download/linux.aspx

### Chrome - бесплатный браузер от Google:

https://www.google.com/chrome/?brand=BNSD&gclid=CjwKCAiAgc-ABhA7EiwAjev-j2sRh3XMEOwm0w0IMz4yaun4a7DWtWNpFLsql89MDn-fvJiHRwbSwxoC-X4QAvD_BwE&gclsrc=aw.ds

### Gimp - полноценный редактор графики:

sudo apt update && sudo apt install gimp gimp-gmic gimp-gap gimp-data-extras gimp-dcraw abr2gbr

### Pinta - простая рисовалка в духе Paint.net:

sudo snap install pinta

### Программа видеоконференций ZOOM:

sudo snap install zoom-client

### Telegram - отличный мессенжер!

sudo snap install telegram-desktop

### Читалка формата DJVI:

sudo apt update && sudo apt install djview4

### Набор архиваторов:

sudo apt update && sudo apt install rar unrar p7zip-full arj

### Простая рисовалка в духе Paint.net:

sudo snap install pinta

### FreeCAD - 2D/3D решение для любителей и инженеров с начальной поддержкой формата dwg (Autocad):

sudo snap install freecad

### Leocad - проектрирование Lego:

sudo snap install leocad --classic

### Gcompris - набор развивающих игр:

sudo snap install gcompris --classic

### Развивающая игра Сети:

sudo apt update && sudo apt install knetwalk

### Arduino для Ubuntu 14/16/18 (32/64 bit):

mkdir Programs && cd Programs && wget https://downloads.arduino.cc/arduino-1.8.15-linux64.tar.xz && tar -xvf arduino-1.8.15-linux64.tar.xz && cd arduino-1.8.15 && sudo ./install.sh

*Чтобы программный код загружался в контроллер, нужно добавить текущего пользователя в группы dialout и tty:*

sudo gpasswd -a myuser tty && sudo gpasswd -a myuser dialout && sudo gpasswd -a myuser plugdev

*Где myuser - это имя пользователя вашей ОС.*

*Установить необходимое для работы с платами компоненты можно командой:*

sudo apt-get install gcc-avr binutils-avr gdb-avr avr-libc avrdude

### Поддержка Java (необходима для некоторых программ. Во время установки браузер лучше закрыть!):

sudo apt update && sudo apt install default-jre default-jdk

### Скриншотер (их много, но этот один из лучших):

sudo apt update && sudo apt install flameshot

### Инструменты разработчика C++:

sudo apt update && sudo apt install build-essential git ghex gdb lldb

### Для создания схем и разводки печатных плат KiCAD EDA:

sudo add-apt-repository --yes ppa:kicad/kicad-5.1-releases && sudo apt update && sudo apt install --install-recommends kicad kicad-demos kicad-locale-ru

Подробнее о дополнениях к KiCAD

### Scratch Desktop 3.6 for Ubuntu Linux:

sudo snap install scratux

### Fritzing - программный комплекс начального уровня для проектирования электронных устройств. Полезен в учебных целях:

sudo apt update && sudo apt install fritzing fritzing-data fritzing-parts

### Geany - это мощный, стабильный и легкий текстовый редактор для программистов:

sudo apt update && sudo apt install geany geany-plugins

### Dia - приложение для рисования структурированных диаграмм

sudo apt update && sudo apt install dia

### Tilix - тайловый (многооконный) терминал:

sudo add-apt-repository ppa:webupd8team/terminix && sudo apt-get update && sudo apt install tilix

### Micro - свободный текстовый редактор для консоли:

cd Загрузки && wget https://github.com/zyedidia/micro/releases/download/v2.0.10/micro-2.0.10-amd64.deb && sudo apt update && sudo dpkg -i micro-2.0.10-amd64.deb && sudo apt update

### Набор необходимых и полезных утилит:

sudo apt update && sudo apt install mc gdebi htop tree mesa-utils sl lm-sensors neofetch winbind wget curl ppa-purge inxi recoll net-tools xclip xsel arp-scan

### SimulIDE - простой и бесплатный симулятор электрических цепей:

wget https://launchpad.net/simulide/0.4.15/0.4.15-sr1/+download/simulide_0.4.15-SR1.AppImage && chmod a+x simulide_0.4.15-SR1.AppImage

### OpenShot - простой в управлении и мощный по возможностям видеоредактор:

sudo add-apt-repository ppa:openshot.developers/ppa && sudo apt update && sudo apt install openshot-qt

### Audacity - простой в управлении и мощный по возможностям аудиоредактор:

sudo add-apt-repository ppa:ubuntuhandbook1/audacity && sudo apt update && sudo apt install audacity

### OBS Studio - бесплатное программное обеспечение с открытым исходным кодом для записи видео и потокового вещания:

sudo add-apt-repository ppa:obsproject/obs-studio && sudo apt update && sudo apt install ffmpeg obs-studio

### Информация об оборудовании:

sudo apt update && sudo apt install inxi

*запуск этой программы в Терминале:*

inxi -Fs

### Поддержка snap и flatpack в Центре Приложений

sudo apt update && sudo apt install gnome-software gnome-software-plugin-snap gnome-software-plugin-flatpak

### Дополнительные темы значков для LibreOffice 7

sudo apt update && sudo apt install libreoffice-style-breeze libreoffice-style-tango libreoffice-style-sifr

### Дополнительная локализация приложений (запустить команду в Терминале):

gnome-language-selector 

*В открывшемся окне нажмите "Установить"*

![mateLang](images/mateLang.png)

### Установить переключение клавиатуры на другой язык (запустить команду в Терминале):

mate-keyboard-properties

*В открывшемся окне выполните это:*

![mateLang](images/mateKey1.png)

![mateLang](images/mateKey2.png) 

### Перезагрузите компьютер.

## Всё готово!