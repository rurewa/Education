Версия документа 0.1 alpha
## Прокачка Lubuntu

### В процессе установки Lubuntu следует выбрать английский язык:

![GitHub Logo](images/)

![GitHub Logo](images/)


### Локализация Lubuntu

**Локализуем qt и gtk (после установки компьютер перезагрузится):**

`sudo apt install -y aspell-ru language-pack-kde-ru language-pack-ru language-pack-ru-base myspell-ru language-pack-gnome-ru-base language-pack-gnome-ru firefox-locale-ru libreoffice-l10n-ru language-pack-gnome-ru-base language-pack-gnome-ru && reboot`

![GitHub Logo](images/)

![GitHub Logo](images/)

**Подключение партнёров Ubuntu:**

`sudo software-properties-qt`

**Обновить ОС:**

`sudo apt list --upgradable -a && sudo apt update && sudo apt full-upgrade -y`

**Переключение раскладки клавиатуры:**

`sudo dpkg-reconfigure keyboard-configuration && reboot`

**Установить браузер Vivaldi:**

https://vivaldi.com/download/

