# 5@8Bot

Pour t'assurer de rester assez "hydraté" et nourris durant les *5@8*, tu as décidé de [modifier une Roomba™](https://www.youtube.com/watch?v=Brf02tdtQGo&t=30s) pour qu’elle te rende service en allant chercher des boissons 🍺 et de la pizza 🍕 pour toi et tes amis. Pour ce faire, ce petit bot doit aller chercher les jetons de la personne en question, aller chercher l'item qu'elle veut et aller lui porter. Ce processus doit être répété par la suite pour la personne suivante. 

### 📈 Votre objectif

Sachant que trois heures c'est un temps très limité pour pouvoir bien profiter de ton 5@8, le bot doit prendre le chemin le plus optimal entre ses objectifs.

### 🕵🏼‍♂️ Explication

Ton bot va prendre en entrée une carte des lieux qui ressemble à ceci: 

```
#####
#A B#
#   #
#  P#
#   #
#@ 1#
#####
``` 
où
 `A, B, … Z \ P` représente les personnes voulant des breuvages,
 `1, 2, … 9` représente les bars où sont fournis les brevages,
 `P` représente l'endroit où aller chercher la pizza et
 `@` represente la position initiale du robot.

Ton bot prendra aussi en entrée une série d'ordres:
 ```
 AB
 BF
 AF
 AP
 ```
où la première colonne représente la personne voulant l'item, et la deuxième colonne est soit `B` pour bière, `F` pour liqueur ou `P` pour pizza.

Roomba™ étant un très simple robot, peut seulement prendre et agir dans quatre directions: Up `U`, Down `D`, Left `L` or Right `R`. Le robot peut aussi prendre les jetons de quelqu'un `T`, prendre de la pizza `P` du point de vente, prendre de  la liqueur `F` ou de la bière `B` du bar ou donner un item à quelqu'un `G`. Pour faire une action, le bot doit être où l'action à lieu. Par exemple, pour prendre les jetons de `A`, le bot doit se placer à `(1,1)` (prenant en compte que `(0, 0)` est le coin en haut à gauche).

### 💻 Interaction avec la plateforme

Ton bot doit afficher les actions qu'il a effectuées, avec chaque ordre sur une ligne séparée. Par exemple,  la bonne sortie pour la map et les ordres ci-dessus est:  

```
UUUUTDDDDRRBUUUULLG
RRTDDDDFUUUUG
LLTDDDDRRFUUUULLG
TDDRRPUULLG
```
Le *flag* sera la concatenation des chemins pour [education](https://github.com/jactymilena/CSGames2023SelectionPublic/blob/main/5@8-bot/education.txt), [science](https://github.com/jactymilena/CSGames2023SelectionPublic/blob/main/5@8-bot/genie.txt), [genie](https://github.com/jactymilena/CSGames2023SelectionPublic/blob/main/5@8-bot/sciences.txt), en ordre, soumis à un algorithme de hachage MD5 et suivant le format `JDIS-{CONTENT_GOES_HERE}`.

Par exemple, si les chemins sont `UTDBG`, `DTUBG`, `LTRBG`, alors le *flag* sera `JDIS-{fa244afb7adcabbab6021fb9f1ef8e4e}`

**⚠️WARNING !!!⚠️**  
Pour être sûr que votre robot indique le bon chemin, veuillez utiliser la [*Distance de Manhattan*](https://en.wikipedia.org/wiki/Taxicab_geometry) et considérer les directions dans l'ordre suivant: `U`, `D`, `L`, `R`[.](https://www.youtube.com/watch?v=NKbI6dpY-yo)

Sinon, votre robot pourrait trouver un chemin égal mais incorrect.

Bonne chance ! 💙
