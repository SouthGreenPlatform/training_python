
## Listes

_Liste_  : structure de données contenant une série de valeurs ordonnées \(possiblement de types différents\)

_ma\_liste = \[1\, "deux"\, 3\.0\]_

_ma\_liste\_vide = \[\]_

<span style="color:#000000">Appeler les éléments d'une liste</span>

_ma\_liste\[0\]_  <span style="color:#000000">	premier élément de la liste</span>  _ma\_liste\[1\]_  <span style="color:#000000">	second élément de la liste</span>

<span style="color:#FF0000"> __Attention : Les index commencent à 0 \! __ </span>

#### Listes

<span style="color:#000000">i\,j = positions dans la liste		x = valeur</span>

__Récupérer la longueur d'une liste __ :

_len\(ma\_liste\)_

Prendre une tranche d'une liste :

_ma\_liste\[i:j\]_ 	⇒ éléments de l'indice i à l'indice j\-1

_ma\_liste\[i:\]_ 	⇒ tous les éléments à partir de l'indice i

_ma\_liste\[:j\]_ 	⇒ tous les éléments jusqu'à l'indice j\-1

_ma\_liste\[:\-1\]_ 	⇒ tous les éléments sauf le dernier

_ma\_liste\[\-1\]_ 	⇒ dernier élément

Concaténer des listes

_liste\_1 \+ liste\_2_

<span style="color:#000000">i\,j = positions dans la liste		x = valeur</span>

Ajouter un élément à la fin d'une liste _ma\_liste\.append\(x\)_

Remplacer la valeur d'un élément à une position déterminée _ma\_liste\[i\] = x_

Insérer un élément à une position déterminée _ma\_liste\.insert\(i\, x\)_

<span style="color:#000000">i\,j = positions dans la liste		x = valeur</span>

Trier une liste en place	 _ma\_liste\.sort\(\)_

Créer une copie triée d'une liste	 _liste\_triee = sorted\(ma\_liste\)_

Inverser une liste	 _ma\_liste\.reverse\(\)_

Supprimer un élément d'une liste	 _del ma\_liste\[i\]_  _	ma\_liste\.remove\(x\)_ 	\(ne retire que la première occurrence de x\)

Compter le nombre d'occurrences de x dans une liste	 _ma\_liste\.count\(x\)_

<span style="color:#000000">i\,j = positions dans la liste		x = valeur</span>

Tester si un élément appartient ou pas à une liste _if x in ma\_liste:_  _if x not in ma\_liste:_

_Attention_  : toutes les recherches par valeur dans la listesont en O\(n\)= de  _plus en plus lentes_  au fur et à mesure que la taille de la liste augmente

Une chaîne de caractères est une  _liste non modifiable_  _sequence = "ATGGCAT"_  _sequence\[2\]_ 				=> "G"

On peut créer une liste modifiable à partir de la chaîne _liste\_sequence = list\(sequence\)_

_Listes de listes_

_liste = \[\[1\, 2\, 3\]\, \[4\, 5\, 6\]\]_  _liste\[0\]_ 				=> \[1\, 2\, 3\] _liste\[0\]\[0\]_ 		=> 1 _liste\[1\]\[2\]_ 		=> 6