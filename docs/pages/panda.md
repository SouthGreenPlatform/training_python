# Panda 

__Tous les exemples de ce cours pour la partie __  <span style="color:#6B9F25">pandas</span>  __ ont été pris du cours de python de Patrick Fuchs et Pierre Poulain \!\! __  _[https://python\.sdv\.univ\-paris\-diderot\.fr/17\_modules\_interet\_bioinfo/\#174\-module\-pandas](https://python.sdv.univ-paris-diderot.fr/17_modules_interet_bioinfo/#174-module-pandas)_  __ __

## Series

Une `Serie` correspond à un vecteur à une dimension

__Syntaxe__

```python
>>> import pandas as pd
>>> s = pd.Series([10, 20, 30, 40], index = ['a', 'b', 'c', 'd'])
>>> s
a    10
b    20
c    30
d    40
dtype: int64
```

Chaque élément de la série de données possède une étiquette qui permet d'appeler les éléments :  

```python
>>> s[0]
10
>>> s["a"]
10
```

on peut extraire plusieurs éléments, par leurs indices ou leurs étiquettes :  

```python
>>> s[[1, 3]]
b    20
d    40
dtype: int64
```

```python
>>> s[["b", "d"]]
b    20
d    40
dtype: int64
```

Les étiquettes permettent de modifier et d'ajouter des éléments :  

```python
>>> s["c"] = 300
>>> s["z"] = 50
>>> s
a     10
b     20
c    300
d     40
z     50
dtype: int64
```

on peut filtrer une partie de la series :  

```python
>>> s[s>30]
c    300
d     40
z     50
dtype: int64
```

et même combiner plusieurs critères de sélection :  

```python
>>> s[(s>20) & (s<100)]
d    40
z    50
dtype: int64
```

## Dataframe

Une `Dataframe` correspondent à un tableaux à deux dimensions avec des étiquettes pour nommer les lignes et les colonnes.

### Création 

Voici comment créer un dataframe avec pandas à partir de données fournies comme liste de lignes :
```python
>>> df = pd.DataFrame(columns=["a", "b", "c", "d"],
...                   index=["chat", "singe", "souris"],
...                   data=[np.arange(10, 14),
...                         np.arange(20, 24),
...                         np.arange(30, 34)])
>>> df
         a   b   c   d
chat    10  11  12  13
singe   20  21  22  23
souris  30  31  32  33
```

Le même dataframe peut aussi être créé à partir des valeurs fournies en colonnes sous la forme d'un dictionnaire :

```python
>>> data = {"a": np.arange(10, 40, 10),
...         "b": np.arange(11, 40, 10),
...         "c": np.arange(12, 40, 10),
...         "d": np.arange(13, 40, 10)}
>>> df = pd.DataFrame(data)
>>> df.index = ["chat", "singe", "souris"]
>>> df
         a   b   c   d
chat    10  11  12  13
singe   20  21  22  23
souris  30  31  32  33
```

### Création à partir d'un csv

Une fonctionnalité très intéressante de pandas est d'ouvrir très facilement un fichier au format .csv :

```python
>>> import pandas as pd
>>> df = pd.read_csv("mon_fichier.csv")

>>> df = pd.read_csv("mon_fichier.csv", index_col="ID")
>>> df.head()
>>> df.shape

# quel est le type de c/colonne
>>> df.dtypes 
```


### Pratique 11 : importer un fichier csv et le explorer

Jupyter notebook

Créer un programme python  `exo-pandas-explo.py`  qui prenne en input le fichier suivant:

[https://python.sdv.univ-paris-diderot.fr/data-files/transferrin_report.csv
](https://python.sdv.univ-paris-diderot.fr/data-files/transferrin_report.csv)

Lire le fichier avec  `pd.read_csv` et calculer quelques statistiques descriptives pour les données numériques avec la méthode `.describe()`.

La colonne "Source" contient des chaînes de caractères, on peut rapidement déterminer le nombre de protéines pour chaque organisme 


### Dataframe Proprietés

Les dimensions d'un dataframe sont données par l'attribut `.shape` :

```python
>>> df.shape l'attribut
(3, 4)
```

La méthode `.head(n)` renvoie les n premières lignes du dataframe (par défaut, n vaut 5) :

```python
>>> df.head(2)
```

L'attribut `.columns` renvoie le nom des colonnes et permet aussi de renommer les colonnes 

```python
>>> df.columns
Index(['a', 'b', 'c', 'd'], dtype='object')
>>> df.columns = ["Paris", "Lyon", "Nantes", "Pau"]
>>> df
        Paris  Lyon  Nantes  Pau
chat       10    11      12   13
singe      20    21      22   23
souris     30    31      32   33
```

### Dataframe Sélection

#### Sélection de colonnes

On peut sélectionner une colonne par son étiquette :

```python
>>> df["Lyon"]
chat      11
singe     21
souris    31
```

ou plusieurs colonnes en même temps :

```python
>>> df[["Lyon", "Pau"]]
        Lyon  Pau
chat      11   13
singe     21   23
souris    31   33
```

#### Sélection de lignes

Pour sélectionner une ligne, il faut utiliser l'instruction .loc() et l'étiquette de la ligne :  

```python
>>> df.loc["singe"]
Paris     20
Lyon      21
Nantes    22
Pau       23
Name: singe, dtype: int64
```

Ici aussi, on peut sélectionner plusieurs lignes :

```python
>>> df.loc[["singe", "chat"]]
       Paris  Lyon  Nantes  Pau
singe     20    21      22   23
chat      10    11      12   13
```

Enfin, on peut aussi sélectionner des lignes avec l'instruction .iloc et l'indice de la ligne (la première ligne ayant l'indice 0) :  

```python
>>> df.iloc[1]
Paris     20
Lyon      21
Nantes    22
Pau       23
Name: singe, dtype: int64

>>> df.iloc[[1,0]]
       Paris  Lyon  Nantes  Pau
singe     20    21      22   23
chat      10    11      12   13
```

On peut également utiliser les tranches (comme pour les listes) : 

```python
>>> df.iloc[0:2]
       Paris  Lyon  Nantes  Pau
chat      10    11      12   13
singe     20    21      22   23
```

#### Sélection de lignes ET colonnes

On peut combiner les deux types de sélection (en ligne et en colonne):
```python
>>> df.loc["souris", "Pau"]
33
>>> df.loc[["singe", "souris"], ['Nantes', 'Lyon']]
        Nantes  Lyon
singe       22    21
souris      32    31
```

#### Sélection par condition

Sélectionnons maintenant toutes les lignes pour lesquelles les effectifs à Pau sont > à 15

```python
>>> df[ df["Pau"]>15 ]
```

De cette sélection, on ne souhaite garder que les valeurs pour Lyon :

```python
>>> df[ df["Pau"]>15 ]["Lyon"]
```

On peut aussi combiner plusieurs conditions avec & pour l'opérateur et :

```python
>>> df[ (df["Pau"]>15) & (df["Lyon"]>25) ]
```

et | pour l'opérateur ou :

```python
>>> df[ (df["Pau"]>15) | (df["Lyon"]>25) ]
```

### Pratique 12 : Statistiques par groupe

Créer un programme python `exo-pandas-stats.py` qui prenne en input le fichier `transferrin_report.csv` et qui calcule la taille et la masse moléculaire moyennes des transferrines.

* explorer les fonctions `.groupby()` et `.mean()` pour le faire

* Calculer la valeur minimale et maximale de la longueur et de la masse moléculaire
explore les fonctions  `.pivot_table()`

### Combinaison de dataframes

Combinaison de dataframes

df1 
```python
         Lyon  Paris
chat      10      3
singe     23     15
souris    17     20
```

df2 
```python
          Nantes  Strasbourg
chat         3           5
souris       9          10
lapin       14           8
```

pour concatener les deux df

```python
>>>pd.concat([df1, df2])
```

pour les concatener mais en mettant en commun les lignes des deux df

```python
>>> pd.concat([df1, df2], axis=1)
```

conserver que les lignes communes aux deux dataframes

```python
>>> pd.concat([df1, df2], axis=1, join="inner")
```

### Pratique 13 : Concatener

Créer un programme python exo-pandas-concatener.py qui cree les deux df :  

df1 
```python
         Lyon  Paris
chat      10      3
singe     23     15
souris    17     20
```

df2
```python 
          Nantes  Strasbourg
chat         3           5
souris       9          10
lapin       14           8
```

et qui les concatene ! 

