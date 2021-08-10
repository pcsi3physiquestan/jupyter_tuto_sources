---
jupytext:
  encoding: '# -*- coding: utf-8 -*-'
  formats: ipynb,md:myst
  split_at_heading: true
  text_representation:
    extension: .md
    format_name: myst
    format_version: 0.13
    jupytext_version: 1.10.3
kernelspec:
  display_name: Python 3
  language: python
  name: python3
---

# Utilisation de Jupyter

Un notebook Jupyter est à la fois:
* Une application Web interactive dans laquelle on peut documenter, exécuter et partager du code (Python pour nous).
* Un document qui permet d'intégrer des cellules de textes et/ou d'équations et des cellules du code (Python).

C'est un outil très utile en séance de travaux pratiques (entre autre) puisqu'il permet d'associer un compte-rendu propre et ordonnée (grâce aux cellules de texte) et l'exploitation des données grâce aux méthodes numériques implémentées dans les cellules de code Python.

_Remarque : Ce document que vous lisez à l'heure actuelle est (ou a été créé à partir) d'un notebook._

Dans ce document, nous allons vous présenter ce qu'est un notebook et comment les ouvrir et les modifier avec une application locale.

## Un notebook : ca se présente comment ?

### Allure générale

Un notebook se présente comme un fichier d'extension .ipynb. Lorsqu'il est ouvert par l'application Jupyter notebook (cf. suite pour y accéder), elle se présente sous la forme suivante d'une suite de "**cellules**" de *texte* (au format Markdown) et *code* (Python - avec la partie affichée par le compilateur si la cellule a été executée).

On notera dans l'image du notebook ci-dessous un liseré bleu ou vert sur le côté gauche de la cellule *active* (qu'on édite ou qu'on veut exécuter).

```{figure} images/jupyternotebookallure_com.png
:name: allure
:align: center
Note Jupyter
```

***
### Les cellules de texte
Par défaut, les cellules de texte sont éditées au format "Markdown". La mise en forme se fait au moyen de notations simples : titre, liste ou formule mathématique.

_Vous ne devriez pas beaucoup modifier les zones de texte. Elles correspondront en général aux énonces._

***
### Les cellules de code

Les cellules de code sont interprétées comme du Python.

Pour exécuter le code, il faut appuyer sur **Shift + Entrée** ou sur le bouton **Exécuter** dans la barre d'outil en haut de la page.

```{figure} images/jupyternotebookoutil.png
:name: barre_out
:align: center
Barre d'outil
```

```{code-cell}
a = 1
b = 2
print(a + b)
```

````{attention} 
*Les cellules de code ne sont pas indépendantes. Quand vous exécutez une cellule, elle tient compte de toutes les cellules **qui ont été exécutées avant**.*

**Attention**, la compréhension des cellules ne se fait pas dans l'ordre du document mais dans l'ordre d'execution des cellules. Et si vous exécutez deux fois la même cellule, elle tiendra compte de la première exécution.

__On retiendra qu'il est important d'exécuter TOUTES les cellules de code DANS l'ORDRE du notebook.__
````

_A titre d'exemple, la cellule de code ci-dessous ne renvoie pas d'erreur __uniquement si la précédent a été exécutée.__ Et si on l'exécute plusieurs fois, on incrémente la variable `a` de 1._

```{code-cell}
a = a + 1
```

***
### La barre d'outil
```{figure} images/jupyternotebookoutil.png
:name: barre_outil
:align: center
Barre d'outil
```

La barre d'outil en haut regroupe les boutons les plus utiles. Dans l'ordre (en gras les plus utiles):

1. **Enregistrer le fichier** notebook (son nom est tout en haut, dans le cas montré tout en haut,le nom du fichier est `methodes_exp_partie_3.ipynb`). _Vous pouvez changer le nom du fichier en cliquant dessus en haut de la page._
2. **Ajouter une cellule après** : La cellule est par défaut une cellule de code. Elle est ajoutée après la cellule active.
3. Couper/Copier/Coller la cellule active
4. Déplacer la cellule active vers le haut ou vers le bas
5. **Executer la cellule active** _Identique à `Shift+Entrée`_
6. Arrêter le noyau : utile seulement si le temps d'exécution devient trop long _(exemple : boucle infinie !)_.
7. **Relancer le noyau** : permet de repartir de 0 dans la compilation. _Pensez à relancer l'éxecution des cellules précédentes !_
8. Relancer le noyau et exécuter toutes les cellules (dans l'ordre du document cette fois)
9. Changer le format de la cellule (permet de transformer une cellule de code en cellule Markdown par exemple)
10. Afficher la palette de commande : Elle regroupe toutes les commandes exécutables (comment supprimer une cellule par exemple).

*Remarque : Il existe des commandes clavier qui permettent de gagner en rapidité mais elles ne seront pas présentées pour ne pas alourdir la présentation. Ces commandes sont affichées dans la palette de commande à côté de la commande*.

***
## Un notebook : comment ça s'exécute ?
Il s'agit d'installer Python, Jupyter et les bibliothèques scientifiques utiles en physique (numpy, scipy, matplotlib...). La méthode proposée est d'installer __Anaconda__. Elle a [déjà été présentée](https://filedn.eu/l2bpHGgwv4dYLpu8bJBwYM7/Stan/Pyzo_Anaconda/Python_pyzo_insta_gen_auroraW/co/Python_Installation.html).

### Lancement de Jupyter notebook
Lancer le navigateur Anaconda. La [fenêtre s'ouvre](accueil)

```{figure} ./images/accueil_anaconda.png
:name: accueil
:align: center
Navigateur Anaconda
```
Il suffit de cliquer sur "Jupyter Notebook" pour lancer l'application. 

### Utilisation de Jupyter
Par défaut, _Jupyter notebook_ s'ouvrira sur votre répertoire personnel. Vous aurez une fenêtre comme ceci:

```{figure} ./images/jupytertree.png
:name: treejupyter
:align: center
Accueil Notebook Jupyter
```

* Vous pouvez naviguer entre les répertoires (comme `vitesse_son_2` sur l'image). __Il est vivement conseillé de créer un répertoire spécifique aux activités du cours/TP de physique__ (bouton `Nouveau` en haut à droite).
* Les notebooks sont les fichiers avec les extensions `.ipynb`. Il suffit de cliquer sur un fichier pour l'ouvrir.
* Vous pouvez aussi créer vos propres notebooks avec le bouton `Nouveau` (choisir `Python 3`)

