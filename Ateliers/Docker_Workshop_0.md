# Commandes de base de Docker

Cet exercice vous a permis de pratiquer les commandes de base de Docker, y compris la vérification de la version de Docker, 
l'affichage des conteneurs en cours d'exécution, la gestion des images Docker, le téléchargement d'une image depuis un registre, 
et la suppression d'une image de votre machine.

## 1. Afficher la version de Docker installée

```
docker --version
```

## 2. Afficher la liste des conteneurs en cours d'exécution. Au début, vous ne devriez voir aucun conteneur actif

```
docker ps
```

## 3. Afficher la liste des images Docker disponibles sur votre machine. Initialement, vous ne devriez avoir aucune image dans la liste.

```
docker images
```

## 4. Télécharger l'image "hello-world" depuis le Docker Hub. Cela vous permettra de tester rapidement Docker avec une image simple.

```
docker pull hello-world
```

## 5. Vérifiez à nouveau les images Docker disponibles. Vous devriez maintenant voir l'image "hello-world" récemment téléchargée dans la liste.

```
docker images
```

## 6. Supprimer l'image "hello-world" de votre machine. 

```
docker rmi hello-world
```

## 7. Vérifiez une dernière fois la liste des images Docker. L'image "hello-world" devrait maintenant être supprimée de la liste.

```
docker images 
```
