
## Pratique 2: les test

* Créer un programme python exo2.py qui affiche la moyenne de 3 notes données par l'utilisateur.

Voici le code python3 pour demander 3 valeurs à l'utilisateur qui seront stockées dans les variables note1\, note2\, note3

```python
note1 = input\("Donner une note : "\)
note2 = input\("Donner une note : "\)
note3 = input\("Donner une note : "\)
```

!!! warning
    les variables `note1`, `note2`, `note3` sont de type  __chaîne de caractère __ (`str`)

* Modifier ensuite le programme afin qu'il affiche : 

    "ajourné" si la moyenne est inférieure à 10  
    "passable" si la moyenne est supérieure ou égale à 10  
    "assez bien" si la moyenne est supérieure ou égale à 12
    "bien" si la moyenne est supérieure ou égale à 14  
    "très bien" si la moyenne est supérieure ou égale à 16  

!!! tips
    Écrire l’algorithme en commentaire par exemple:
    ```python  
    # on demande a l'utilisateur de rentrer 3 notes qu'on sauvegarde dans 3 variables
    # on doit convertir les valeurs car la fonction input retourne des str()
    ```