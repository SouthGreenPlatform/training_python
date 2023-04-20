## Pratique 7

### Exercice A

Créer un programme python `exo7_a.py` qui créer un dictionnaire associant à chaque base de l'ADN la chaine "purinique" (C et G) ou "pyrimidinique" (A et T) selon la base :
puis qui demande à l'utilisateur (fonction `input()`) d'entrer une base, 
et enfin qui affiche si la base entrée par l'utilisateur est purinique ou pyrimidique.

### Exercice B

En utilisant un dictionnaire et la fonction `in` (clef in dictionnaire), créer un programme python `exo7_b.py` qui stocke dans un dictionnaire le nombre d’occurrences de chaque acide aminé de la séquence `AGWPSGGASAGLAILWGASAIMPGALW`, puis afficher ce dictionnaire.  
    
Votre programme doit afficher :  

```python
{'P': 2, 'I': 2, 'W': 3, 'G': 6, 'L': 3, 'A': 7, 'M': 1, 'S': 3}
```

### Exercice C

Voila un dictionnaire faisant correspondre à chaque espèce la longueur de son génome : 

```
dico_espece = {'Escherichia coli':3.6,'Homo sapiens':3200,'Saccharomyces cerevisae':12,'Arabidopsis thaliana':125}
```

Créer un programme python `exo7_c.py` dans lequel vous créez ce dictionnaire et qui permet d'afficher le nom de l'organisme possédant le plus grand génome.

### Exercice D

Le fichier [sequences_especes.tsv](../../data/files/sequences_especes.tsv) est un fichier tabulé (2 colonnes séparées par des tabulations) contenant un identifiant de séquence dans la première colonne, et l’espèce associée dans la secondes colonne. 
```
Homo sapiens    27292
Saccharomyces cerevisiae S288C  850883
Homo sapiens    55226
Mus musculus    19791
```

Créez un script `exo7_d.py` qui lit ce fichier et, à l’aide d’un dictionnaire, écrit un fichier de sortie qui contient le nom d’une espèce précédé d’un dièze sur une ligne puis tous les identifiants de séquence associés à cette espèce sur les lignes suivantes.

```
# Homo sapiens
27292
55226
....
# Saccharomyces cerevisiae S288C
850883
....
```