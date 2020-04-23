# COMPTE-RENDU DU PROJET DE DÉVELOPPEMENT D’UN LANGAGE SPÉCIFIQUE POUR DES ANIMATIONS GRAPHIQUES SIMPLES

#### Auteur : Nicolas LE BRENNE

Objectif: Développer un interpreteur de script agissant sur des éléments graphiques.


### Exercice 1: Prise en main de la couche graphique

La prise en main de la couche graphique a permis de comprendre les bases du fonctionnement des objets GSpace et GRect.
Cette partie préparatoire a notamment donné lieu à la découverte des méthodes suivantes:


* Définition de la taille de l'objet robi: setDimension
* Position de l'objet robi via les coordonnées de son coin supérieur gauche: setPosition
* Définition de la couleur des objets robi et space: setColor
* La supension temporaire des actions objets via la méthode sleep


D'autres méthodes seront étudiées dans les exercices suivants.

La difficulté de cet exercice a tenu à l'adaptation automatique à la dimension de la fenêtre lors du parcours de robi au sein de la fenêtre space.

Le problème a été résolu en utilisant les méthodes getWidth() et getHeigth() qui permettaient d'ajuster paramétres de parcours des boucles for.

Mon choix de programmation s'est orienté sur l'utilisation de 4 boucles for consécutives. Il aurait cependant pu être judicieux de les imbriquer. En revanche, il aurait fallu prendre garde à ce que l'objet robi ne rebrousse pas chemin lors des ajustements de fenêtre.

![Résultat](https://i.gyazo.com/7f23d53ebb13e34a2e0bb0b5060763e4.gif)

### Exercice 2: Première version d'un interpréteur de script



