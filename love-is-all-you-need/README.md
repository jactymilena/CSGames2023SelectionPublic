# Love is all you need

Avec les récents événements politiques, Twitter ressent un sentiment de haine toujours plus grand sur sa plateforme. Comme nous vivons dans un monde dystopique où la censure est acceptée, Twitter a décidé de "nettoyer" sa plateforme des discours haineux.

### 📈 Votre objectif

Dans un premier temps, ils ont engagé des travailleurs du [Mechanical Turk](https://www.mturk.com/) pour étiqueter les tweets comme positifs ou négatifs. Mais, avec la chute de leurs [actions](https://www.marketwatch.com/story/twitter-shares-slide-16-after-fake-account-purge-new-rules-in-europe-2018-07-27), ils ont dû réduire leurs dépenses et faire appel à des stagiaires en informatique (non rémunérés) pour construire un modèle d'apprentissage automatique permettant de prédire si un tweet est positif ou négatif.

### 🕵🏼‍♂️ Explication

`Data/train_data.csv` contient  les tweets et `Data/train_labels.csv` contient les *labels* qui leur sont associés. `Data/test_data.csv` contient les tweet n'ayant pas de *label*.

```
https://i.redd.it/xc3q9bc2xr311.jpg - Whenever I look at this I laugh  Haha.
```
Sa catégorie est `1`

ou un autre:

```
@BryanPerson we'll definitely have an iPhone Audioboo chat at #iabc09. I'll be doing mine, too 
```
ayant aussi une catégorie de `1`

### 💻 Interaction avec la plateforme

Un [starter pack](https://github.com/jactymilena/CSGames2023SelectionPublic/blob/main/love-is-all-you-need/stater_pack.zip) vous est fourni. Pour `entrainer` votre modèle et `prédire` les catégories, vous devez coder les fonctions appropriés dans `model.py`. Vous pouvez regarder `solver.py` pour voir comment les données sont générées et validées, mais *NE PAS MODIFIER CE FICHIER*.

`train` prend l'ensemble des données d'apprentissage (*dataset*) `X` and *labels* `Y`
`predict`  prend votre `model` et tous les tweets `X` à prédire

Pour entraîner votre modèle et ensuite faire des prédictions, exécutez `python solver.py`. Vous devrez ensuite copier le contenu de `Data/predictions.json` dans le solveur de la plate-forme, dans une impression console. Le contenu devrait ressembler à quelque chose comme `print('["0", "1"...]')`

Une précision de 70% vous donnera quelques points tandis qu'une précision de 75% et plus vous donnera tous les points.

#### Requirements

`Python 3` et `numpy` sont nécessaires pour exécuter `solver.py`. Vous pouvez utiliser la bibliothèque de votre choix pour construire et entraîner votre modèle tant que vous ne modifiez pas les signatures des fonctions.

#### Tips

Vous pouvez supposer que les tweets sont i.i.d et qu'il y a une chance égale qu'un tweet soit dans la catégorie `0` ou `1`. Par conséquent, un classificateur aléatoire, qui produit `0` avec 50% de chance et `1` avec 50% de chance, vous donnera une précision de 50%. 

Si votre précision est inférieure à 50 %, vous pouvez supposer que votre approche n'est pas très bonne et ne vaudra aucun point. Une solution simple qui permet d'obtenir une précision d'environ 70 % est [l'estimation du maximum de vraisemblance](https://en.wikipedia.org/wiki/Maximum_likelihood_estimation).

Bonne chance ! 💙

P.S. : Toute référence politique date d'un temps où Trump était encore au pouvoir.