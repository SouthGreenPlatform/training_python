#### Boucles

On peut avoir besoin de répéter une action \(un bloc de code\) plusieurs fois

Exemples:

Afficher chaque élément d'une liste

Tant que vous n'aurez pas compris les boucles\, je rééexpliquerai

Pour cela on va " _boucler_ "\.

Deux structure itératives :  _Pour_  \(for\) et  _Tant que_  \(while\)

#### Boucles > while (TANT QUE)

_Tant que_  la condition est vraie\, le bloc de code est exécuté

<span style="color:#000000">expression conditionnelle \(comme les if\)</span>

_while condition:_

_	instruction_

_	\.\.\._

<span style="color:#000000">bloc de code qui sera exécuté tant que la condition est vraie</span>

<span style="color:#000000">Le bloc d'instructions doit </span>  _modifier la valeur de l'expression conditionnelle_  <span style="color:#000000">\, sinon boucle infinie \!</span>

<span style="color:#000000">\(rappel : </span>  <span style="color:#000000"> __CTRL\+C__ </span>  <span style="color:#000000"> pour arrêter un programme bloqué dans une boucle infinie\)</span>

<span style="color:#000000">expression conditionnelle \(dépend de i\)</span>

_i = 1_  _while i <= 4:_

_	print\(i\)_

_	i = i \+ 1_

<span style="color:#000000">modification de la valeur de i</span>  __⇒ modification de la valeur de l'expression conditionnelle__

#### Boucles > for (POUR)

_Pour chaque élément_  d'un itérable\, exécuter un bloc de code

\(une liste est un exemple d'itérable\)

<span style="color:#000000">variable qui contiendra chaque élément</span>

_for_  _ element _  _in_  _ iterable:_

_	instruction_  _	…_

<span style="color:#000000">itérable \(ex\. liste\) duquel les éléments seront tirés</span>

<span style="color:#000000">bloc de code \(indenté\) qui sera exécuté une fois pour chaque élément</span>

_animaux = \["Lion"\, "Chèvre"\, "Vache"\]_

_for animal in animaux:_

_	print\(animal\)_

Astuce : avoir en même temps la position et la valeur de l'élément

_for position\, element in enumerate\(iterable\):_  _	print\(f"Position \{position\} : \{element\}"\)_

_Attention :_  Ne pas modifier la liste sur laquelle on boucle \!

Si on veut itérer sur un nombre croissant\, on peut utiliser  _range_  :

_range\(fin\)		_  <span style="color:#000000">Entiers de 0 à fin \- 1</span>  _range\(début\, fin\)	_  <span style="color:#000000">Entiers de début à fin \- 1</span>  _range\(début\, fin\, pas\)	_  <span style="color:#000000">Entiers de début à fin \- 1 tous les pas</span>

<span style="color:#000000">Exemple : nombres pairs entre 2 et 12</span>

_for i in range\(2\, 14\, 2\):_  _	print\(i\)_

#### Boucles > Interruptions

Deux instructions qui permettent  _d'interrompre une boucle prématurément_  :

_continue_  arrête l'exécution de l'itération en cours et  _passe à l'itération suivante_

=> utile si on veut ignorer une variable particulière et passer directement à la suivante

_break_  arrête l'exécution de l'itération en cours et  _sort de la boucle_

<span style="color:#000000">=> utile par exemple si on cherche quelque chose et qu'on l'a trouvé</span>

_ma\_liste = \["machin"\, "truc"\, "chose"\]_

_for element in ma\_liste:_

_if element == "truc":_

_	continue_

_print\(element\)_

_print\("fini"\)_

_ma\_liste = \["machin"\, "truc"\, "chose"\]_

_for element in ma\_liste:_

_if element == "truc":_

_	print\(element\)_

_	break_

_print\("fini"\)_