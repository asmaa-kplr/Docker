# Premiers pas avec Docker
## Premier conteneur

- Selon la documentation Docker, il est recommandé de tester le bon fonctionnement du moteur Docker en démarrant le conteneur "hello-world" qui affiche un message dans le terminal.

```
docker run hello-world
```

![image](https://user-images.githubusercontent.com/123757632/230086152-916f29e7-2d6a-4832-9a8d-e0dd04356279.png)

Lors de l'exécution de la commande "docker run hello-world": 
- Docker recherche localement une image nommée "hello-world:latest".
- Si l'image n'est pas trouvée localement, Docker la télécharge depuis la bibliothèque Docker Hub et la stocke localement. 
- Ensuite, Docker crée un nouveau conteneur à partir de cette image et exécute l'exécutable qui affiche le message "Hello from Docker!". 
- Enfin, Docker transmet la sortie du conteneur au client Docker qui l'affiche sur le terminal. 

Ce résultat indique que l'installation de Docker semble fonctionner correctement et fournit des informations supplémentaires sur le fonctionnement de Docker.

Il fournit également des suggestions pour continuer à utiliser Docker et des liens vers des ressources supplémentaires pour en savoir plus sur Docker.

- Observer les conteneurs en cours d’exécution

```
docker container ls
```
![image](https://user-images.githubusercontent.com/123757632/230089228-1913e849-6cb6-49d8-a207-227e1e675be7.png)

Avec cette commande on ne voit aucun conteneur en cours d’exécution. Le conteneur se termine dès que la commande par défaut du conteneur a été exécutée.

- Afficher les conteneurs terminés 

```
docker container ls -a
```

![image](https://user-images.githubusercontent.com/123757632/230090096-24177243-aaf1-4671-b130-3fb6821f649d.png)


- Afficher ensuite les images docker présentes sur la machine

```
docker images
```

![image](https://user-images.githubusercontent.com/123757632/230090445-9dc246ae-b575-488c-b59e-757afd1a21de.png)

- Supprimer l’image 'hello-world' , qui ne sera pas utile pour la suite

```
docker rmi <Id-image>
```

La suppression de l'image n'est pas possible actuellement car elle est toujours référencée par un conteneur.

Il est donc nécessaire de commencer par supprimer le conteneur

```
docker rm <Id-conteneur>
```
Puis resupprimer l'image

```
docker rmi <Id-image>
```
