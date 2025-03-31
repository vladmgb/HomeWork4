# Решение к домашнему заданию к [занятию 4](https://github.com/netology-code/virtd-homeworks/blob/shvirtd-1/05-virt-03-docker-intro/)

## Задача 1
 Ссылка на образ в [dockerhub](https://hub.docker.com/repository/docker/vladmgb/custom-nginx/general)

## Задача 2
Cкриншоты консоли к задаче 2

![Cкриншоты консоли к задаче 2](https://github.com/user-attachments/assets/7c811767-d0ff-4d62-b62b-7d83be779a91)


## Задача 3
Cкриншоты команд и их выводы к задаче 3

![task_3_1](https://github.com/user-attachments/assets/1aba91da-70be-408f-aa1c-43fd8c631aa8)


![task_3_2](https://github.com/user-attachments/assets/cfa24f12-bdd4-4f46-8733-cd0d679d0b16)

## Задача 4
Cкриншоты команд и их выводы к задаче 4

![task_4](https://github.com/user-attachments/assets/c7b46109-d739-432f-ae9c-981cbf904d20)


## Задача 5
Cкриншоты команд и их выводы к задаче 5

![task_5_1](https://github.com/user-attachments/assets/21217ee6-c937-4375-955a-a414f9b4b4a0)

Был запущен файл compose.yaml, т.к. из документации следует, что если оба файла присутствуют, то  файл compose.yaml имеет предпочтение.

Добавил в compose.yaml секцию include с docker-compose.yaml, чтобы запустились оба контейнера.

![task_5_2](https://github.com/user-attachments/assets/17a32978-1c39-4b24-8bdb-57fb5d758912)

Скриншот от поля "AppArmorProfile" до "Driver" из Portainer

![task_5_4](https://github.com/user-attachments/assets/86a1a103-6e8b-4b28-8ee7-24d6cb11b841)

Cкриншот portainer c задеплоенным компоузом
![task_5_5](https://github.com/user-attachments/assets/2de9ce26-07af-442b-9b6b-ee137f751a19)

Команды и вывод
![task_5_6](https://github.com/user-attachments/assets/4ff5be12-dd65-442f-a45d-ed9614f6faf5)


Файл compose.yaml

```
  version: "3"
  include:
    - docker-compose.yaml
  services:
    portainer:
      image: portainer/portainer-ce:latest
      volumes:
        - /var/run/docker.sock:/var/run/docker.sock
      restart: unless-stopped
      ports:
        - "9000:9000"
```

