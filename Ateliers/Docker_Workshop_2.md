# Construire des images Docker
## Premières images
Explorons maintenant une autre image célèbre : docker/whalesay.
Whalesay contient une adaptation du jeu Linux cowsay. Ce jeu a été initialement écrit en 1999 par Tony Monroe.

- Executer le conteneur comme suit :

```
docker run docker/whalesay cowsay bonjour
```

![image](https://user-images.githubusercontent.com/123757632/230111484-760ac882-5399-4bdd-8e62-1ace69b74bf3.png)

- Pour vérifier la popularité de l’image docker/whalesay et voir si de nombreuses images mettant en oeuvre des baleines parlantes existent , rechercher l' images spécifiques à travers le hub Docker. 

L’image docker docker/whalesay est un peu frustrante car elle exige à chaque exécution de préciser le message à afficher.

Nous aimerions que dans le cas où l’utilisateur ne donne aucune commande au moment de l’exécution du conteneur, un message par défaut soit affiché par la baleine.

Nous allons construire une nouvelle image pour cela à partir d 'un Dockerfile

Avant de créer une nouvelle image, il est important de créer un nouveau répertoire dans lequel seront stockés le Dockerfile ainsi que tous les fichiers permettant de créer l’image. Ce répertoire sera le contexte utilisé pour la création de l’image


