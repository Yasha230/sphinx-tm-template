# Avant projet

## Espace de travail

Pour les projects qui suivent, les codes seront écrit en langage de programation Python3 et l'editeur utilisé sera Pycharm community.

### Comment fonctionne un drone ?

flight directions ?
physics behind ?
mechanic (basic)?

## Installations de base

La première chose qu'il nous faut pour commencer à programmer le drone est la bibliothèque du TELLO drone.

```{admonition} Une bibliothèque
Une bibliothèque informatique est une collection d'entité informatique qui réuni du code, dejà compilé pouvant être réutilisé par d'autres programmes.
```
Pour cela, il nous faut télécharger le paquet ("package" en anglais) depuis l'onglet fichier ("file") sous paramètres ("settings").

```{figure} figures/image 1.JPG

```
Ensuite nous devons selectionner notre projet et l'interpréteur ("interpreter"). Nous allons ajouter la bibliothèque faite pour le drone que nous allons utiliser, qui a le nom de: djitellopy.
Une fois que l'installation est faite nous allons pouvoir importer la bibliothèque du drone ainsi que celle du temps.

```python
from djitellopy import tello
from time import sleep
```
Ensuite pour se connecter au Tello drone, il faut créer un **objet** Tello, le nommer et le connecter.

```python
dragonfly = tello.Tello()
dragonfly.connect()
```
Il est possible maintenant de s'amuser à programmer le drone comme l'on programmerai la tortue de python. Tout les commandes pour le drone sont accesible en mettant le curseur sur l'un des commandes déjà appelé, ensuite appuyant sur la touche contôle ("Ctrl") et cliquant. Cela nous revoie à la bibliothèque du Tello drone avec la liste des commandes disponible.