Un __dictionnaire__ est une structure de données qui contient une collection __non ordonnée__ (pas d'indice) de __couples clé/valeur__ (pouvant être de types différents)

## Dictionnaires

__Déclarer__ un dictionnaire

```python
dico = {cle1: valeur1, cle2: valeur2, …}
dico_vide = {}
```

On __accède aux valeurs__ d'un dictionnaire par ses clés

```python
dico[cle]
```

Liste des __clés__ d'un dictionnaire : `dico.keys()`  
Liste des __valeurs__ d'un dictionnaire : `dico.values()`  
Liste des __couples clé/valeur__ d'un dictionnaire : `dico.items()`  

!!! note
    Les liste retourné se comportent presque comme des listes mais n'en sont pas tout à fait. On peut obtenir une vraie liste en faisant : 
    `list(dico.keys())`

```python
for cle, valeur in dico.items():
	print(f"La clé {cle} contient {valeur}")
```

__Longueur__ (nb. de couples) d'un dictionnaire

```python
len(dico)
```

!!! note 
    `len` fonctionne sur beaucoup de types qui ont une longueur : `str`, `list`, `tuple`, `dict`, `set`, `range`… 

__Tester l'existence__ d'une clé
```python
if cle in dico		#retourne True si la clé existe
```

__Modifier une valeur__ ou __Ajouter un couple__ (selon si la clé existe ou pas)
```python
dico[cle] = valeur
```

__Supprimer__ un couple
```python
del dico[cle]
```

__Vider__ un dictionnaire
```python
dico.clear()
```

--8<-- "pages/pratiques/pratique7.md"