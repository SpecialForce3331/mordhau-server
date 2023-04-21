1) Запускаем docker-compose-updater, ждем пока отработает скрипт обновления и завершится процесс
2) Запускаем docker-compose, ждем пока игра запустится, после чего останавливаем.
3) Копируем Mordhau/Saved/Config/LinuxServer/Game.ini и Mordhau/Saved/Config/LinuxServer/Engine.ini в корневую папку игры.
4) Добавляем в Game.ini
```
MapRotation=HRD_Camp
MapRotation=HRD_Grad
MapRotation=HRD_MountainPeak
MapRotation=HRD_Taiga

MaxSlots=6
ServerName=SudorootServer

AdminPassword=123qwe
Admins=76561198021320101
```
5) Добавляем в Engine.ini
```
[/Script/EngineSettings.GameMapsSettings]
ServerDefaultMap=/Game/Mordhau/Maps/DuelCamp/HRD_Camp
```
6) Выставляем права на .ini файлы 666
7) Запускаем повторно docker-compose и радуемся жизни.