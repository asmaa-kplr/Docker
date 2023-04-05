# Premiers pas avec Docker
## Premier conteneur

- Selon la documentation Docker, il est recommandé de tester le bon fonctionnement du moteur Docker en démarrant le conteneur "hello-world" qui affiche un message dans le terminal.

```
docker run **
```

- Observer les conteneurs en cours d’exécution

```
docker container **
```

Avec cette commande on ne voit aucun conteneur en cours d’exécution. Le conteneur se termine dès que la commande par défaut du conteneur a été exécutée.

- Afficher les conteneurs terminés 

```
docker container **
```

- Afficher ensuite les images docker présentes sur la machine

```
docker ** ** 
```

- Supprimer l’image 'hello-world' , qui ne sera pas utile pour la suite

```
docker ** **
```

- La suppression de l'image n'est pas possible actuellement car elle est toujours référencée par un conteneur.

Il est donc nécessaire de commencer par supprimer le conteneur

```
docker ** ** 
```
Puis resupprimer l'image

```
docker ** ** 
```
