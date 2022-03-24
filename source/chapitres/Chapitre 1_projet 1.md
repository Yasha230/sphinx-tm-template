# Projet 1: Commander le drone avec le clavier d'ordinateur

## Intoduction au projet

Maintenant que nous avons les installations de base faite, nous pouvons aborder le premier projet. Ce projet consiste à diriger le TELLO drone avec le clavier de l'ordinateur, le but étant de se familiarise avec l'éditeur Pycharm ainsi qu'avec le drone que nous utiliserons tout au long de ce tutoriel. Les commandes que nous utiliserons dans cette partie sont les commandes de base pour le mouvement du drone. Nous les lierons donc au touches du clavier, ce qui nous donnera la possibilité de contrôler le drone comme l'on contrôlerai un avatar dans un jeux vidéo.  

## Notions et outils utilisés

### Mouvement d'un drone

Un drone peut se déplacer de haut en bas ainsi que dans 3 directions différentes.
Le mouvement d'un drone se fait par les quatres hélices attaché à des moteurs. Pour un mouvement vertical, le drone s'appluie sur les rotors. En utilisant leurs rotors, les drones contrent la force gravitationelle exercé sur eux pour permettre de faire du surplace. De la même façon, pour monter, le drone exerce plus de force que celle de gravité et pour descendre, le drone exerce moins de force.  
Pour du vol stationnaire, deux de quatre rotors se déplacent dans le sens des aiguilles d'une montre, et les deux autre dans le sens contraire des aiguilles d'une montre. Ceci permet d'équilibrer l'élan latérale du drone. Pour éviter de déséquilibrer son mouvement vertical, les deux autres hélices augementent leur rotation. 
Le même principe s'applique au déplacement vers l'avant et vers l'arrière: les rotors doivent appliquer une poussée totu en veillant à ce que la rotation des rotors maintienne l'équilibre du drone.
Dans ce projet ce sera donc ces vitesses de rotors que nous influencerons.

```{image}figures/ Mouvement diagram.png
:alt: shéma des mouvements
```

### Modules

Lorsque l'on écrit des programmes plus conséquents, nous voulons diviser notre programme en plusieurs fichier pour faciliter la maintenace, ou quand l'on va appeller une fonction à plusieures reprises, pour éviter à avoir à la copier à chaque reprise.
Pour cela, Python permet de créer des **modules**, qui placent des définitions dans un fichier qui peuvent ensuite être utilisé dans un script ou dans une instance interactive de l'interpréteur. Les définitions d'un **module** peuvent être importées dans d'autres modules ou dans le module principal.

### Pygame
L'un des outil pricipale utilisé dans ce premier projet est Pygame. Pygame est un ensemble de modules utilisé sur plusieurs plateformes différentes pour créer des jeux vidéos en python. Pygame nous servira comme intermédiaire entre les saisies du clavier si seront transformés en commandes que comprendra le code pour ensuite contrôler le drone. Cela nous permettra d'utiliser le clavier d'un ordinateur pour contrôler le drone, comme l'on ferai dans un jeux vidéo.

## Projet - Code
