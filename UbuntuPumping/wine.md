## Установка и настройка Wine в Ubuntu 20.04

### Меняем архитектуру устанавливаемых Windows-приложений:

sudo dpkg --add-architecture i386 && sudo apt update

### Скачиваем ключ репозитория и добавляем его в систему:

wget -nc https://dl.winehq.org/wine-builds/winehq.key && sudo apt-key add winehq.key

### Добавляем репозиторий:

sudo add-apt-repository 'deb https://dl.winehq.org/wine-builds/ubuntu/ focal main' && sudo apt update

### Устанавливаем сам wine:

sudo apt install --install-recommends winehq-devel winetricks ; rm -R ~/.wine && env WINEPREFIX=~/.wine WINEARCH=win32 winecfg

### Прокачиваем Wine:

winetricks --force -q d3dcompiler_47 vcrun2015 corefonts dotnet45 dotnet472

### Запускаем конфигуратор Wine и выбираем в нём Windows 7/10

![GitHub Logo](images/winecfg.png)

### Перезагрузите компьютер!










