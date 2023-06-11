# 

Dans cet exercice, nous allons découvrir comment utiliser l'image Docker de PostgreSQL pour configurer et exécuter rapidement une base de données PostgreSQL.  
En suivant les étapes fournies, vous apprendrez comment télécharger l'image Docker de PostgreSQL, créer un conteneur, vérifier son fonctionnement et vous connecter à la base de données PostgreSQL. 

# 1. Télécharger l'image Docker de PostgreSQL

Avec Docker, vous pouvez soit créer ou posséder vos propres images, soit utiliser des images provenant du dépôt. Dans ce cas, étant donné que vous utilisez une image Docker de PostgreSQL, vous pouvez la récupérer depuis Docker Hub en utilisant la commande suivante :

```
docker pull postgres
```

# 2. Vérifier les images Docker installées

Une fois que l'image Docker de PostgreSQL a été récupérée depuis Docker Hub, vous pouvez vérifier l'image en utilisant la commande suivante :

```
docker images
```

# 3. Exécuter le conteneur Docker PostgreSQL

Maintenant que vous avez l'image Docker de PostgreSQL sur votre machine, vous pouvez démarrer le conteneur. Comme mentionné précédemment, un conteneur est une instance d'une image Docker. Pour démarrer le conteneur PostgreSQL, vous devez fournir à Docker quelques paramètres, qui sont expliqués ci-dessous :

–name : le nom du conteneur PostgreSQL.
-d    : Cela lance le conteneur en mode détaché, ce qui signifie qu'il s'exécutera en arrière-plan.

```
docker run --name postgres_cont -d postgres
```

# 4. Afficher les conteneurs en cours 

Afficher les conteneurs actuellement en cours d'exécution.

```
docker ps
```

En exécutant la commande "docker ps" sans aucun argument supplémentaire, seuls les conteneurs en cours d'exécution seront affichés. 

# 5. Exécuter une session interactive de shell  

A l'intérieur d'un conteneur nommé "pgsql-dev". Cela vous permet d'accéder à l'environnement du conteneur et d'interagir avec celui-ci en exécutant des commandes dans le shell.



