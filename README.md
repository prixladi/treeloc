# Treeloc Backend

# Spuštění projektu

## Docker (docker-compose)

Spuštění projektu pomocí `docker-compose up`

Vytvoření nových imagů a spuštění projektu pomocí `docker-compose up --build`

---

### Frontend 

Služba poběží na portu **80**.

---

### Api

Služba poběží na portu **4545**.

---
### Loader

Služba poběží na portu **4546**.

---

### MongoDb

Kontejner s databází poběží na portu **27017**.

---

Mapování portů pro všechny služby se dá změnit v souboru **./docker-compose.yml**.

[Dokumentace docker-compose.](https://docs.docker.com/compose/)

# Proměnné prostředí
Proměnné prostředí se dají změnit v souboru **./docker-compose.yml**.

## Api service

|Název|Povinná|Popis|
|---|---|---|
|MONGO_URL|ano|Adresa Mongo databáze|
|MONGO_DATABASE_NAME|ano|Název Mongo databáze|

## Loader service

|Název|Povinná|Popis|
|---|---|---|
|MONGO_URL|ano|Adresa Mongo databáze|
|MONGO_DATABASE_NAME|ano|Název Mongo databáze|
|LOADER_INTERVAL|ano|Interval stahovaní datasetů ve vteřinách|
|DISCOVERY_INTERVAL|ano|Interval volání DISCOVERY_URL ve vteřinách|
|DISCOVERY_URL|ano|Adresa která vrací adresy datasetů|

## Frontend

|Název|Povinná|Popis|
|---|---|---|
|API_URL|ano|Adresa **Api** služby|
|LOADER_URL|ano|Adresa **Loader** služby|