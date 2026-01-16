# Install_QtCreator_Ubuntu
## Установка и настройка QtCreator из архива на Ubuntu с добавлением ярлыка в панель задач
### Скачиваем QtCreator 16.0.2
```
wget https://github.com/stimandrew/Install_QtCreator_Ubuntu/releases/download/v1.0.0/qtcreator-linux-x64-16.0.2.deb
```
### Устанавливаем зависимости
```
sudo apt install libxcb-cursor0 libdouble-conversion3
```
### Устанавливаем  QtCreator 16.0.2
```
sudo dpkg -i qtcreator-linux-x64-16.0.2.deb
```
### Создаем файл `qtcreator.desktop`
```
sudo nano /usr/share/applications/qtcreator.desktop
```
### Добавляем следующее содержимое
```
[Desktop Entry]
Version=1.0
Name=Qt Creator 16.0.2
Comment=Qt Creator IDE
Exec=/opt/qt-creator/bin/qtcreator
Icon=/opt/qt-creator/share/icons/hicolor/256x256/apps/QtProject-qtcreator.png
Terminal=false
Type=Application
Categories=Development;IDE;Qt;
Keywords=Qt;IDE;C++;Development;
StartupNotify=true
MimeType=text/x-c++src;text/x-c++hdr;text/x-xsrc;application/x-designer;application/vnd.qt.qmakeprofile;application/vnd.qt.xml.resource;
```
### Делаем файл исполняемым
```
sudo chmod +x /usr/share/applications/qtcreator.desktop
```
