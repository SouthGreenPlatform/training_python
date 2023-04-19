# Les variables 

## typage

_Variable_  : zone de mémoire dans laquelle on stocke une valeurUne variable a un nom \(ensemble de lettres\, chiffres et \_\)

On déclare une variable en initialisant :  _x = 2_ On peut changer sa valeur avec une affectation :  _x = x \+ 3_

Python donne automatiquement un type a chaque variable en fonction de sa nature

_w = 1_ 				⇒ type  _int_  \(nombre entier\) integer

_x = 3\.2_ 			⇒ type  _float_  \(nombre flottant\) float

_y = "hello"_ 	⇒ type  _str_  \(chaîne de caractères\)

_z = True_ 			⇒ type  _bool_  \(booléen\) boolean

## Manipulation

Sur les nombres : opérateurs mathématiques de base _\+	\-	\*	/	\*\*_  \(puissance\)		 _%_  \(modulo\)

Sur les chaînes de caractères : _\+_ 	concaténation _\*_ 	répétition

_type\(ma\_variable\)_  donne le type de la variable

__Pas de conversion automatique \! \(str \+ int ⇒ erreur\) ex :__  _ "Bonjour" \+ 10_

Solution:

Conversion :  _int\(\)_ \,  _float\(\)_ \,  _str\(\)_

## Nommage

Un nom de variable ne peut pas commencer par un chiffre\.

Éviter de commencer avec un \_

Les noms de variables sont  _sensibles à la case_  \(test ≠ TEST\)

Utiliser la convention snake\_case \(sauf noms de classes\)

_ma\_longue\_variable = 3_

<span style="color:#000000">Ne pas utiliser un </span>  <span style="color:#4F81BD"> __mot réservé__ </span>  <span style="color:#000000"> comme nom \(</span>  <span style="color:#9BBB59">print</span>  <span style="color:#000000">\, </span>  <span style="color:#93C47D">range</span>  <span style="color:#000000">\, </span>  <span style="color:#9BBB59">from</span>  <span style="color:#000000">\, </span>  <span style="color:#9BBB59">for</span>  <span style="color:#000000">\, …\)</span>

<span style="color:#000000"> __Donnez des noms explicites à vos variables \!__ </span>

<span style="color:#9BBB59">longueur\_seq</span>  <span style="color:#000000"> plutôt que </span>  <span style="color:#9BBB59">l</span>
