**Установка Linux Lite подробно описана тут:**

https://web-shpargalka.ru/linux-lite-sistemnye-trebovanija.php

## Настраиваем Linux Lite v 5.6

### Открываем окно настроек:

![GitHub Logo](images/LinuxLiteStart.png)

#### Отключаем скринсервер и засыпание монитора

![GitHub Logo](images/LinuxLiteScreenSave.png)

![GitHub Logo](images/LinuxLiteScreenSave1.png)

![GitHub Logo](images/LinuxLiteScreenSave2.png)

![GitHub Logo](images/LinuxLiteScreenSave3.png)

![GitHub Logo](images/LinuxLiteScreenSave4.png)

![GitHub Logo](images/LinuxLiteScreenSave5.png)

![GitHub Logo](images/LinuxLiteScreenSave6.png)

#### Локализуем всю систему:

![GitHub Logo](images/LinuxLiteLang.png)

![GitHub Logo](images/LinuxLiteLang1.png)

**Программа попросит вас загрузить обновления языков, нужно согласиться**

#### Настраиваем раскладку клавиатуры:

![GitHub Logo](images/LinuxLiteKeyboard.png)

![GitHub Logo](images/LinuxLiteKeyboard1.png)

#### Настройка нижней панели:

![GitHub Logo](images/LinuxLitePanelLang.png)

![GitHub Logo](images/LinuxLitePanelLang1.png)

![GitHub Logo](images/LinuxLiteLang2.png)

![GitHub Logo](images/LinuxLitePanelLang2.png)

### Настройка источников приложений:

![GitHub Logo](images/LinuxLiteSoftPartners.png)

![GitHub Logo](images/LinuxLiteSoftUpdate.png)

**Запускаем Терминал при помощи клавиатурной комбинации Ctrl-Alt-T и вставляем в него при помощи клавиатурной комбинации Ctrl-Shift-V строку. **

*После вставки текста вводим Y и нажимаем Enter:*

`sudo apt list --upgradable -a && sudo apt update && sudo apt full-upgrade -y && reboot`

*Эта команда обновит и перезагрузит ОС.*

**Установить ядро 5.11**

`sudo apt install --install-recommends linux-generic-hwe-20.04`

### Установить приложения (открыть ссылку):

https://github.com/rurewa/Education/blob/main/UbuntuPumping/SoftInstall.md