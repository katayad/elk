## Сборка & Запуск:

В CRM/
```
sudo docker-compose build
sudo docker-compose up
```

### Запуск в фоновом режиме и остановка
```
sudo docker-compose up -d
sudo docker-compose down
```

### Доступ к терминалу на контейнере (обычно не нужно)
```
sudo docker exec -it int_serv bash
sudo docker exec -it database bash
```

## Установка:

### Проект:

```
git clone git@gitlab.com:SNMsoft/CRM.git
```

### Docker:

```
sudo apt-get update
sudo apt-get install apt-transport-https ca-certificates curl software-properties-common
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"

sudo apt-get update
sudo apt-get install docker-ce

sudo pip install docker-compose
```

### gitlab Runner


Установка:
```
curl -L https://packages.gitlab.com/install/repositories/runner/gitlab-ci-multi-runner/script.deb.sh | sudo bash
sudo apt-get install gitlab-ci-multi-runner
```

Регистрация:
```
sudo gitlab-runner register
```
https://gitlab.com, docker, alpine:latest

```
/etc/gitlab-runner/config.toml
```
privileged = true
