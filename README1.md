# Домашнее задание к занятию "`Оркестрация кластером Docker контейнеров на примере Docker Swarm`" - `Первушин Дмитрий`

### Задача 1

Создайте ваш первый Docker Swarm-кластер в Яндекс Облаке. Документация swarm: https://docs.docker.com/engine/reference/commandline/swarm_init/

1. Создайте 3 облачные виртуальные машины в одной сети.
2. Установите docker на каждую ВМ.
3. Создайте swarm-кластер из 1 мастера и 2-х рабочих нод.
4. Проверьте список нод командой:
```
docker node ls
```

### Решение 1

Создал кластер командой
```
docker swarm init --advertise-addr 10.128.0.27
```

Присоединил рабочие ноды командой
```
docker swarm join --token SWMTKN-1-2kc0z8dr8ivfok8ctskllnn9kc5hx2fjvoxs5sdyl0mpgld4k9-8qdg83vnbdercnfz9t1c7y89x 10.128.0.27:2377
```

Прикладываю скриншоты
![Task1](https://github.com/Divan4eg/docker-hw/blob/main/img/13.png)

![Task1](https://github.com/Divan4eg/docker-hw/blob/main/img/14.png)
