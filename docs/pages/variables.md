# Les variables 

## typage

__Variable__ : zone de mémoire dans laquelle on stocke une valeurUne variable a un nom (ensemble de lettres, chiffres et _)

On déclare une variable en initialisant : `x = 2`  
On peut changer sa valeur avec une affectation : `x = x + 3`

Python donne automatiquement un type a chaque variable en fonction de sa nature : 

* `w = 1`				⇒ type `int` (nombre entier) integer
* `x = 3.2`			    ⇒ type `float` (nombre flottant) float
* `y = "hello"`	        ⇒ type `str` (chaîne de caractères)
* `z = True`			⇒ type `bool` (booléen) boolean

## Manipulation

* Sur les nombres : opérateurs mathématiques de base  

    * `+`
    * `-`	
    * `*`	
    * `/`	
    * `**` (puissance)		
    * `%` (modulo)

* Sur les chaînes de caractères :
    * `+`	concaténation
    * `*`	répétition

`type(ma_variable)` donne le type de la variable

!!! warning
    Pas de conversion automatique ! (str + int ⇒ erreur)   
    ex : `"Bonjour" + 10`=> erreur  
    Solution:   
        => Conversion : `int()`, `float()`, `str()`


## Nommage

* Un nom de variable ne peut pas commencer par un chiffre. 
Éviter de commencer avec un `_`

* Les noms de variables sont __sensibles à la case__ (test ≠ TEST)
Utiliser la convention snake_case (sauf noms de classes)
`ma_longue_variable = 3`

* Ne pas utiliser un __mot réservé__ comme nom (`print`, `range`, `from`, `for`, …)

* __Donnez des noms explicites à vos variables !__  
`longueur_seq` plutôt que `l`
