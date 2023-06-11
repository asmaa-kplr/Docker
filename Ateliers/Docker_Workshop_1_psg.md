# Gestion d'images et de conteneurs Docker

Dans cet exercice, nous allons découvrir comment utiliser l'image Docker de PostgreSQL pour configurer et exécuter rapidement une base de données PostgreSQL.  
En suivant les étapes fournies, vous apprendrez comment télécharger l'image Docker de PostgreSQL, créer un conteneur, vérifier son fonctionnement et vous connecter à la base de données PostgreSQL. 

# 1. Télécharger l'image Docker de PostgreSQL

Avec Docker, vous pouvez soit créer ou posséder vos propres images, soit utiliser des images provenant du dépôt. Dans ce cas, étant donné que vous utilisez une image Docker de PostgreSQL, vous pouvez la récupérer depuis Docker Hub en utilisant la commande suivante :

```
docker pull postgres
```

![image](https://github.com/asmaa-kplr/Docker/assets/123757632/9a5cd7b8-20dc-4426-ad56-b966a4886b65)

# 2. Vérifier les images Docker installées

Une fois que l'image Docker de PostgreSQL a été récupérée depuis Docker Hub, vous pouvez vérifier l'image en utilisant la commande suivante :

```
docker images
```
![image](https://github.com/asmaa-kplr/Docker/assets/123757632/b793f054-03a3-44e0-b02a-a07825601104)

# 3. Exécuter le conteneur Docker PostgreSQL

Maintenant que vous avez l'image Docker de PostgreSQL sur votre machine, vous pouvez démarrer le conteneur. Comme mentionné précédemment, un conteneur est une instance d'une image Docker. Pour démarrer le conteneur PostgreSQL, vous devez fournir à Docker quelques paramètres, qui sont expliqués ci-dessous :

–name : le nom du conteneur PostgreSQL.
-d    : Cela lance le conteneur en mode détaché, ce qui signifie qu'il s'exécutera en arrière-plan.

```
docker run --name postgres_cont -e POSTGRES_PASSWORD:passwored -d -e 5432:5432 postgres
```

![image](https://github.com/asmaa-kplr/Docker/assets/123757632/b2b0341f-79a0-47d6-9c11-92a46cf9cc70)

# 4. Afficher les conteneurs en cours 

Afficher les conteneurs actuellement en cours d'exécution.

```
docker ps 
```

![image](https://github.com/asmaa-kplr/Docker/assets/123757632/675349c8-1b05-438d-83c4-d495d72dd263)

En exécutant la commande "docker ps" sans aucun argument supplémentaire, seuls les conteneurs en cours d'exécution seront affichés. 

# 5. Afficher tous les conteneurs 

Afficher tous les conteneurs présents sur votre machine, qu'ils soient en cours d'exécution ou arrêtés. 

```
docker ps -a
```

![image](https://github.com/asmaa-kplr/Docker/assets/123757632/7ff0b033-e931-40ac-942e-974491114401)

# 5. Exécuter une session interactive de shell  

A l'intérieur d'un conteneur nommé "pgsql-dev". Cela vous permet d'accéder à l'environnement du conteneur et d'interagir avec celui-ci en exécutant des commandes dans le shell.

```
docker exec -it <container-id> bash
```
![image](https://github.com/asmaa-kplr/Docker/assets/123757632/d1c52439-593f-4e6b-9902-e1bab4f00231)

# 6. Connecter a postgres 

```
psql -U postgres
```
![image](https://github.com/asmaa-kplr/Docker/assets/123757632/6897d657-6867-4bee-a6ca-158fc315b0ce)

# 7. Exécuter des commandes PostgreSQL

```
\l
```

![image](https://github.com/asmaa-kplr/Docker/assets/123757632/7c371b46-d71c-4e4c-bf83-d56f0b1c5fbd)

# 8. Quitter Postgres 

```
exit
```

# 9. Quitter le conteneur

```
exit
```

# 10 . Afficher les conteneurs en cours 

```
docker ps
```
![image](https://github.com/asmaa-kplr/Docker/assets/123757632/b5faff1a-fe95-4a0c-8104-d931c981314d)

# 11 . Arreter le conteneur de l'image postgres 
```
docker stop <ID_conteneur> 
```
![image](https://github.com/asmaa-kplr/Docker/assets/123757632/3861619e-3d84-4a7a-8760-ff3e31af0ef5)

