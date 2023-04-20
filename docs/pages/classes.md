## Un type spécifique : les classes/objets

Les __classes__ sont les principaux outils de la __programmation orientée objet__.

Une __classe__ peut comporter :  
* Des variables, appelées __attributs__
* Des fonctions, appelées __méthodes__

Une __instance__ d'une __classe__ est un __objet__  

On peut appeler les attributs d'un objet en utilisant le `.` : 
```python
objet.attribut = 4	# objet.méthode()
```

```python
chaine = "Bonjour"
```
la variable `chaine` est en réalité une instance de la classe `str`.

!!! Important
    Tous les types en python sont des objets

## Examiner les objets / Obtenir de l’aide sur ...

`help(obj)` : Affiche la documentation. Fonctionne sur les modules, les objets et les fonctions.  
Raccourci sur IPython : `?obj`  
 
`dir(obj)` : retourne la liste des attributs et méthodes de la classe de l’objet 

```python
>>> dir("")
[ 'capitalize', 'casefold', 'center', 'count', 'encode', 'endswith', 'expandtabs', 'find', 'format',
 'format_map', 'index', 'isalnum', 'isalpha', 'isascii', 'isdecimal', 'isdigit', 'isidentifier', 'islower',
 'isnumeric', 'isprintable', 'isspace', 'istitle', 'isupper', 'join', 'ljust', 'lower', 'lstrip', 'maketrans',
 'partition', 'replace', 'rfind', 'rindex', 'rjust', 'rpartition', 'rsplit', 'rstrip', 'split', 'splitlines', 'startswith',
 'strip', 'swapcase', 'title', 'translate', 'upper', 'zfill']
```