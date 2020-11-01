# Treeloc

Aplikace pro podporu otevírání dat o dřevinách pomocí [OFN](https://opendata.gov.cz/otev%C5%99en%C3%A9-form%C3%A1ln%C3%AD-normy:start).

Aplikace vznikla v rámci [Baklářské práce](https://dspace.cvut.cz/handle/10467/88708). 

Frontend aplikace - [Treeloc Frontend](https://github.com/prixladi/treeloc-frontend).

Backend aplikace - [Treeloc Backend](https://github.com/prixladi/treeloc-backend).

# Demo aplikace

Demo aplikace běží na https://treeloc.azurewebsites.net/.

# Spuštění projektu

## Docker (docker-compose)

Stažení nových imagů pomocí `docker-compose pull`

Spuštění projektu pomocí `docker-compose up`

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
|REMOVE_OLD|ano|Příznak true/false zda se po spuštění mají smazat všechna data|

## Frontend

|Název|Povinná|Popis|
|---|---|---|
|API_URL|ano|Adresa **Api** služby|
|LOADER_URL|ano|Adresa **Loader** služby|
