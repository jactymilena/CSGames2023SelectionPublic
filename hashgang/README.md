# Hashgang

Yuh, ooh, brr, brr  
Hash gang, ohh

### 📈 Votre objectif

Votre quête mon seigneur, si toutefois vous l'acceptez, sera de rassembler chaque ainé des 2000 hashs. Quatres grandes familles constituent votre royaume.

### 🕵🏼‍♂️ Explication 

Vous recevrez un [fichier contenant 2000 hashs](https://github.com/jactymilena/CSGames2023SelectionPublic/blob/main/hashgang/hashes.txt) issues de 4 algorithmes différents.

**MD5**: Un octet d'une valeur aléatoire.  
**SHA1**: Une `string` de 4 caractères avec cet alphabet: `abc`  
**SHA256**: Une `string` de 3 caractères avec cet alphabet: `abcdefghijklmnopqrstuvwxyz`  
**SHA3_512**: Une `string` de 6 caractères (commençant par `0x`) avec cet alphabet: `0123456789abcdef`  

La réponse est la concaténation du premier caractère de chaque message hashé, en ordre. Dans le cas de MD5, il s'agit du nombre (si on a hashé l'octet 234, on concatène 234 à la réponse. Si c'est 5, on concatène 5).

#### Exemple
**Données hashées**
```
'salut'
50       <- le caractère 50 et non la string '50'
'patate douce'
```

**Sortie**
```
s50p
```

### 💻 Interaction avec la plateforme

Ce défi doit être fait sur vos postes en local. Afin de le résoudre, il faut afficher la réponse trouvée sur la plateforme de défis. 