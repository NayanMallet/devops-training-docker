# devops-training-docker
Docker TP1 - Nayan Mallet

# Q3
### a. Récupérer l'image sur le docker hub (nginx)
```bash
docker image pull nginx
```
### b. Vérifier que vous disposez bien de l'image locale
```bash
docker images
```
```json
REPOSITORY   TAG       IMAGE ID       CREATED        SIZE
nginx        latest    42e917aaa1b5   6 weeks ago    280MB
```
### c. Créer un container pour servir la page html crée précédemment + montage entre chemin local et ceux du container 
```bash
docker run --name my_nginx -d -p 80:80 -v /Users/nayanmallet/Developer/DevOps/devops-training-docker/html:/usr/share/nginx/html nginx
```
### e. Commande pour supprimer le container
```bash
docker container rm my_nginx
```
### f. Commande pour servir le fichier
```bash
docker run --name my_nginx -d -p 80:80 nginx
docker cp /Users/nayanmallet/Developer/DevOps/devops-training-docker/html my_nginx:/usr/share/nginx
```
