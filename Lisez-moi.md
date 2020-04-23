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

![Résultat](https://i.gyazo.com/ca6f038e823dbae2bae8da4630bcb1f7.gif)

### Exercice 2: Première version d'un interpréteur de script

Cette seconde partie a portée sur l'analyse d'un script par interpréteur de commande. Ce script était de la forme:

 <center>(script (s1 s2 s3 s4))</center>
 
 Cette S-expression est saisie en tant qu'objet ExprList, en somme un tableau. Chaque terme de ce tableau est accessible via la methode get(index) puis est casté en string (pour s1 et s2). 
 
 Les termes suivants sont les arguments de s2 et seront castés soit en string soit en entier selon la nature de la fonction s2.
 
 L'exercice 2 revient donc principalement au découpage de la S-expression afin d'en extraire les données relatives aux changements graphiques.
 
 La limite de ce problème tient au fait que le nombre de possibilités de script est limité par le nombre de type d'objets et de fonctions définis dans notre code.
 
 ### Exercice 3: Introduction des commandes
 
 
