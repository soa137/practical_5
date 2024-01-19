# Общее описание проекта practical_5
## Выполнение программы на Python, которая выводит текущее время и дату в контейнере Docker
## Описание установки и настройки Docker и Docker Compose:
- Обновил индекс пакетов с помощью команды`sudo apt-get update
- Установил необходимые пакеты командой `sudo apt-get install ca-certificates curl gnupg
- Добавил официальный GPG-ключ в Docker командами 
sudo install -m 0755 -d /etc/apt/keyrings
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
sudo chmod a+r /etc/apt/keyrings/docker.gpg`
- Добавил репозиторий Docker в источники Apt командой `echo \
"deb [arch="$(dpkg --print-architecture)" signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
"$(. /etc/os-release && echo "$VERSION_CODENAME")" stable" | \
sudo tee /etc/apt/sources.list.d/docker.list > /dev/null`
- Обновил индекс пакетов`sudo apt-get update
- Установил последнюю версию командой `sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin`
- Проверил установку запуском тестового образа командой `sudo docker run hello-world`
- Создал группу docker командой `sudo groupadd docker`
- Добавил пользователя в группу docker командой `sudo usermod -aG docker soa
- Презагрузил систему и проверил, что команды docker теперь работают без sudo командой `docker run hello-world
- Загрузил и установил Docker Compose командой `sudo curl -L "https://github.com/docker/compose/releases/download/v2.24.1/docker-compose-linux-x86_64" -o /usr/local/bin/docker-compose
- Установил права на исполнение для файла docker-compose командой `sudo chmod +x /usr/local/bin/docker-compose
- Запустил команду, чтобы проверить версию Docker Compose docker-compose --version`