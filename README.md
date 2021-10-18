# Les Bases de Deep Learning 
Dans cette formation, nous allons apprendre les concepts de bases de Deep Learning et les calcules scientifiques

## Perceptron
### Définition

Le perceptron est l'unité de base des réseaux de neurones. Il s'agit d'un modèle de classification binaire, capable de séparer linearement 2 classes de points

![perceptron](images/1.png)

### Exemple

Imaginer qu'on ait deux types de plantes( toxique: y = 1 et non-toxique y = 0).

![perceptron](images/2.png)

Si un jour, on decide de mesurer les longueurs de ces plantes (x1 et x2) .

![perceptron](images/3.png)

En répresentant les résultat un graphique, on constate que ces plantes régroupées en séparées en deux classes ou groupes. 
On peut donc développer un modèle capable de prédire à quelle classe appartient une future plante en se basant sur cette droite appélé la frontière de décision.

![perceptron](images/4.png)

### Modèle Lineare
Pour développer ce modèle, il va falloir l'équation de cette droite.

Pour ça, nous allons développer un modèle lineaire en fournissant nos variables x1 et x2 à un neurones en multipliant chaque entrer du neurones par un poids w dans ce neurone, on va  également faire passer un coefficient complementaire b qu'on appelle le biais.

![perceptron](images/5.png)

De retour sur notre graphique, on peut colorer les régions où cette fonction nous retourne une valeur positive z>0 et les régions où elle nous retourne une valeur négative z<0.

![perceptron](images/6.png)

### Reglage des paramètre
Du coup pour prédire à quelle classe appartient une plante il va falloir  régler les paramètre w et b de façon à mieux séparer nos deux classes.

![perceptron](images/7.png)

![perceptron](images/8.png)

C'est ainsi que fonction un perceptron, le premier neurone de l'histoire de Deep Learning.

## Amélioration
Pour améliorer ce modèle, il sera mieu d'accompagner chaque prédiction d'une probabilité. Plus une plante sera éloingnée de la frontière de décision plus il sera évident qu'elle appartienne à sa classe.

![perceptron](images/9.png)

## Fonction d'activation

![perceptron](images/10.png) 

![perceptron](images/11.png)

![perceptron](images/12.png)

## Fonction sigmoïde

Cette fonction qui permet d'effectuer cette action est appélée la fonction **sigmoïde(Logistique)**.

Cette permet de convertir la sortie z en une probabilité a(z)

![perceptron](images/13.png)

## Par exemple 

![perceptron](images/14.png)

![perceptron](images/15.png)

## La loi de Bernoulli
![perceptron](images/16.png)

![perceptron](images/17.png)

## Résumé

Pour résumer tout ce qu'on vient de voir, tout ce qui se trouve à l'intérieur d'un réseau de neurone (z = w1 * x1 + w2 * x2 + b), suivi d'une fonction d'activation a(z) = 1 / 1 + e<sup>-z</sup> qui nous retourne une probabilité suivant la loi de Bernoulli.

![perceptron](images/18.png)

## Fonction Coût (MAXIUM DE VRAISEMBLANCE)
En machine Learning une fonction coût(Loss Function), c'est une fonction qui permet de quantifier les **erreurs effctuées** par un modèle. 

Dans notre cas, c'est une fonction qui calcule la différence entre y réelle et y_pred de notre modèle.

![perceptron](images/19.png)
