## Полезные приложения для Ubuntu 20.04 (64) на все случаи жизни

### Мультимедиа (видео и звук)

**VLC - мощный медиа плеер**

```
sudo snap install vlc
```

#### Vokoscreen - простая и удобная программа для записи видео с экрана

```
sudo snap install vokoscreen-ng
```

### Графика и дизайн

#### VariCAD - проводник 3D / 2D CAD. Открывает основные коммерческие cad форматы

**Официальная страница загрузки**

```
https://www.varicad.com/en/home/products/download/
```

#### Простая программа просмотра и обработки изображений Nomacs

```
sudo apt update && sudo apt install -y nomacs
```

#### XnViewMP (XnView Multi Platform) — продвинутый менеджер изображений для Linux

**Официальная страница загрузки:**

```
http://www.xnview.com/en/xnviewmp/#downloads
```

**или установить в терминале Ubuntu**

```
flatpak install -y flathub com.xnview.XnViewMP
```

#### Gimp - полноценный редактор графики

```
sudo apt update && sudo apt install -y gimp gimp-gmic gimp-gap gimp-data-extras gimp-dcraw abr2gbr
```

#### Inkscape - полноценный редактор векторной графики

```
sudo add-apt-repository -y ppa:inkscape.dev/stable && sudo apt update && sudo apt install -y inkscape ink-generator create-resources pstoedit
```

#### Krita - свободный и бесплатный графический растовый редактор в духе Adobe Photoshop

```
sudo add-apt-repository -y ppa:kritalime/ppa && sudo apt update && sudo apt install -y krita krita-l10n
```

### Офис и планирование

#### GitKraken - клиент для git репозитория (Github). Условно-бесплатная версия

```
sudo snap install gitkraken --classic
```

#### CherryTree - записная книжка иерархической структуры с базовыми возможностями

```
sudo add-apt-repository -y ppa:giuspen/ppa && sudo apt update && sudo apt install -y cherrytree
```

#### PDF Split and Merge -- очень простая, удобная в использовании, свободная утилита с открытым кодом для разделения и объединения pdf-файлов. Она имеет простой графический интерфейс, позволяющий пользователю объединять и разделять pdf-файлы

```
sudo apt update && sudo apt install -y pdfsam
```

#### Master PDF Editor - программа, которая позволяет сделать с PDF-документом что угодно. В варианте FREE имеет ограничения

**Официальная страница загрузки:**

```
https://code-industry.ru/downloads/
```

#### Установка отечественных офисных программ (такое себе, но может кому-то понадобится)

**Р7 Офис**

##### Получение дистрибутива по запросу на сайте:

```
https://support.r7-office.ru/hc/ru
```

**подготовка к установке дистрибутива**

```
sudo apt install libpangox-1.0-0 libgtkglext1
```

**установка загруженного дистрибутива**

```
dpkg -i r7-office.deb
```

```
sudo cp homelicense.lickey /etc/r7-office/license/
```

#### Мой Офис

```
https://myoffice.ru/
```
 
### 3D моделирование

#### Sweet Home 3D - программа для дизайна интерьера в Ubuntu

```
sudo snap install sweethome3d-homedesign --edge
```

### Разработка

#### Visual Studio Code — редактор исходного кода, разработанный Microsoft для Windows, Linux и macOS. Позиционируется как «лёгкий» редактор кода для кроссплатформенной разработки

```
sudo snap install code --classic
```

### Системные утилиты

#### Stacer - программа диагностики и обслуживания операционной системы и установленных приложений Ubuntu

```
sudo apt-get update && sudo apt-get install -y stacer
```
#### Bottles - менеджер установки Windows программ в Linux

```
flatpak install -y flathub com.usebottles.bottles && flatpak override --user --filesystem="/home/user" com.usebottles.bottles
```


### Рабочий стол

#### Файловый менеджер в стиле Total Commander и поддержкой его плагинов

```
sudo apt update && sudo apt install -y doublecmd-gtk
```

#### Забавный симулятор хакерского консольного интерфейса

```
sudo apt update && sudo apt install -y hollywood
```

### Виртуализация

```
sudo apt update && sudo apt install -y virtualbox virtualbox-ext-pack
```

### Интернет

### Образование и разработка

#### Colobot - игра, в которой можно научиться программированию на C-подобном языке

```
sudo apt update && sudo apt install -y colobot
```

#### Stellarium — это свободный планетарий для Вашего компьютера с открытым исходным кодом. Он отображает реалистичное небо в 3D таким, каким Вы видите его невооружённым глазом, в бинокль или телескоп.

```
sudo add-apt-repository -y ppa:stellarium/stellarium-releases && sudo apt update && sudo apt install -y stellarium
```

### Сеть

#### Установка qBittorrent - торрент менеджера

```
flatpak install -y flathub org.qbittorrent.qBittorrent
```

#### Установка и подключение Google Диска

**Установка:**

```
sudo add-apt-repository -y ppa:alessandro-strada/ppa && sudo apt-get update && sudo apt-get install -y google-drive-ocamlfuse
```

**Использование**

**Выполнить команду создания новой папки и настройки её для синхронизиронизации с Google диск:**

*Откроется браузер с предложением разрешить программе предоставить доступ к Google. На всё нужно согласиться!*

```
mkdir ~/GoogleDrive && google-drive-ocamlfuse GoogleDrive/
```

**Через некоторое время в командной строке появится это сообщение:**

Access token retrieved correctly.

**Это значит, что всё ОК!**

**Всё! Можно открыть эту папку в обычном Проводнике**

**Для закрепления результата необходимо прописать команду google-drive-ocamlfuse GoogleDrive/ в автозагрузку**

#### Установка и подключение Яндекс-диска

**Иснтрукция на официальном сайте**

```
https://yandex.ru/support/disk-desktop-linux/start.html
```

**Основы работы с ydisk в консоле**

**Установка и настройка в Ubuntu:**

```
echo "deb http://repo.yandex.ru/yandex-disk/deb/ stable main" | sudo tee -a /etc/apt/sources.list.d/yandex-disk.list > /dev/null && wget http://repo.yandex.ru/yandex-disk/YANDEX-DISK-KEY.GPG -O- | sudo apt-key add - && sudo apt-get update && sudo apt-get install -y yandex-disk
```

**Команды управления**

*первоначальная настройка программы*

```
yandex-disk setup
```

`yandex-disk token rurewa` - *идентификация (не обязательно, если сделан setup)*
`yandex-disk start -d ydisk` - *определение папки для синхронизации (не обязательно, если сделан setup)*
`yandex-disk status -d ydisk` - *показать статус синхронизации (при запущенном демоне синхронизация осуществляется автоматически) (не обязательно, если сделан setup)*

### Игры

#### Open Arena - 3D стрелялка

```
sudo flatpak install -y flathub ws.openarena.OpenArena
```