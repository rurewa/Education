## Прокачка Linux Mint

### Установить переключение клавиатуры на другой язык:

![GitHub Logo](images/mint_key1.png)

![GitHub Logo](images/mint_key2.png)

![GitHub Logo](images/mint_key3.png)

### Отключить засыпание компьютера:

![GitHub Logo](images/mint_savepower1.png)

![GitHub Logo](images/mint_savepower2.png)

### Отключить скринсервер

![GitHub Logo](images/mint_screen1.png)

![GitHub Logo](images/mint_screen1.png)

### Добавляем источники обновлений:

![GitHub Logo](images/image5.png)![GitHub Logo](images/mint_soft_origin1.png)

![GitHub Logo](images/image5.png)![GitHub Logo](images/mint_soft_origin2.png)

### Запускаем Терминал при помощи клавиатурной комбинации Ctrl-Alt-T и вставляем в него при помощи клавиатурной комбинации Ctrl-Shift-V строку. 

*После вставки текста вводим Y и нажимаем Enter:*

`sudo apt list --upgradable -a && sudo apt update && sudo apt full-upgrade -y && reboot`

*Эта команда обновит и перезагрузит ОС.*

### Включаем поддержку Snap:

`sudo rm /etc/apt/preferences.d/nosnap.pref && sudo apt update && sudo apt install -y snapd`

### Установить приложения (открыть ссылку):

https://github.com/rurewa/Education/blob/main/UbuntuPumping/SoftInstall.md

*После установки всех приложений выполните унструкции ниже*

### Установка терминала Tilix по умолчанию:

![GitHub Logo](images/MintTilix.png)

![GitHub Logo](images/MateTilix2.png)

### Информация об оборудовании с помощью Inxi:

*запуск этой программы в Терминале:*

`inxi -Fs`

### Перезагрузите компьютер.

## Всё готово!