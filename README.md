Tp2 serveur
2023-07-04

Dans ce travail pratique, vous allez démontrer que vous avez installé un système de conteneurs
et que vous êtes capable de créer des conteneurs selon une description.

Section 1:
![VersionDockers](https://github.com/Thower56/Tp2_serveur/assets/112575794/3b4709f7-2c56-42cc-a34b-4da0b5d6d313)

Etape 1:
docker --version
docker container version

Etape 2:
docker network create mon_reseau

docker run -d --name apache --network mon_reseau httpd:alpine

docker run -d --name mongoDB --network mon_reseau -e MONGO_INITDB_ROOT_USERNAME=adminmongo -e MONGO_INITDB_ROOT_PASSWORD=EncoreUnAutreBD -v mongodb:/data/db mongo

docker network inspect mon_reseau

docker logs mongoDB | grep adminmongo

