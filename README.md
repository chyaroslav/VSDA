# VSDA



# Common

```
sudo apt update
sudo apt upgrade -y

sudo apt install docker.io -y
```
Создать каталог программы и БД
```
sudo mkdir -p /data/vsda/db
```


## PostgreSQL - база данных
Запуск БД PostgreSQL скрипты инициализации запускаются из текущего каталога
```
sudo docker run --name pg -p 5432:5432 -e POSTGRES_USER=vsda -e POSTGRES_PASSWORD=VSDA22pwd -e POSTGRES_DB=vsdadb -d -v "$(pwd)":/docker-entrypoint-initdb.d -e PGDATA=/var/lib/postgresql/data/pgdata -d -v "/data/vsda/db":/var/lib/postgresql/data postgres

```

```
