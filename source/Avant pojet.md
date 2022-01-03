# Mise en place

## Espace de travail

Pour les projects qui suivent, les codes seront écrit en langage de programation Python3 et l'editeur utilisé sera Pycharm community.

## Installations de base

La première chose qu'il nous faud pour commencer à programmer le drone est la bibliothèque du TELLO drone. Pour cela, il nous faut télécharger le "pakage" depluis l'onglet "File" sous "settings".

```{figure} figures/image 1.JPG

```
Ensuite nous devons selectionner notre et le "interperteurs". Nous allons ajouter la bibliothèque faite pour le drone que nous allons utiliser, qui a le nom de: djitellopy.
Une fois que l'installation est faite nous allons pouvoir importer la bibliothèque du drone ainsi que celle du temps.

```python
from djitellopy import tello
from time import sleep
```
Ensuite pour se connecter au Tello drone, il faut créer un "objet" Tello, le nommer et le connecter.

```python
dragonfly = tello.Tello()
dragonfly.connect()
```
