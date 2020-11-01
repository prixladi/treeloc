# Treeloc


Application to support data opening
about woody plants using an open formal
standard. [OFN](https://opendata.gov.cz/otev%C5%99en%C3%A9-form%C3%A1ln%C3%AD-normy:start).

The application was created during the fulfillment of the  [bachelor's thesis](https://dspace.cvut.cz/handle/10467/88708). 

Application frontend - [Treeloc Frontend](https://github.com/prixladi/treeloc-frontend).

Application backend - [Treeloc Backend](https://github.com/prixladi/treeloc-backend).

# Launching the project

## Docker (docker-compose)

Download new images using `docker-compose pull`

Start the project using `docker-compose up`

---

### Frontend 

Frontend service should be running on port **80**.

---

### Api

Api service should be running on port **4545**.

---
### Loader

Loader service should be running on port **4546**.

---

### MongoDb

MongoDb container should be running on port **27017**.

---

Port mapping for all service can be changed in the **./docker-compose.yml**.

[docker-compose documentation.](https://docs.docker.com/compose/)

# Proměnné prostředí
Environment variables can be changed in the **./docker-compose.yml**.

## Api service

|Name|Optional|Description|
|---|---|---|
|MONGO_URL|no|MongoDB address|
|MONGO_DATABASE_NAME|no|MongoDB Database name|

## Loader service

|Name|Optional|Description|
|---|---|---|
|MONGO_URL|no|MongoDB address|
|MONGO_DATABASE_NAME|no|MongoDB Database name|
|LOADER_INTERVAL|no|Dataset download interval \[s\]|
|DISCOVERY_INTERVAL|no|DISCOVERY_URL call interval \[s\]|
|DISCOVERY_URL|no|Address of discovery endpoint|
|REMOVE_OLD|no|Flag true/false whether to clear all data after start|

## Frontend

|Name|Optional|Description|
|---|---|---|
|API_URL|ano| **Api** Service address|
|LOADER_URL|ano| **Loader** Service address|
