#### Dictionnaires

Un  _dictionnaire_  est une structure de données qui contient une  _collection non ordonnée_  \(pas d'indice\) de  _couples clé/valeur_  \(pouvant être de types différents\)

_Déclaration_  _dico = \{cle1: valeur1\, cle2: valeur2\, …\}_  _dico\_vide = \{\}_

On  _accède aux valeurs_  d'un dictionnaire par ses clés _dico\[cle\]_

Liste\* des  _clés_  d'un dictionnaire :  _dico\.keys\(\)_

Liste\* des  _valeurs_  d'un dictionnaire :  _dico\.values\(\)_

Liste\* des  _couples clé/valeur_  d'un dictionnaire :  _dico\.items\(\)_

_for cle\, valeur in dico\.items\(\):_  _	print\(f"La clé \{cle\} contient \{valeur\}"\)_

<span style="color:#000000">\* se comportent presque comme des listes mais n'en sont pas tout à fait\. On peut obtenir une vraie liste en faisant : </span>

_list\(dico\.keys\(\)\)_

_Longueur_  \(nb\. de couples\) d'un dictionnaire _len\(dico\)_ note :  _len_  fonctionne sur beaucoup de types qui ont une longueur :  _str_ \, _ list_ \, _ tuple_ \, _ dict_ \, _ set_ \, _ range_ …

<span style="color:#4F81BD"> __Tester l'existence__ </span>  <span style="color:#000000"> d'une clé</span>  <span style="color:#9BBB59">if cle in dico		</span>  <span style="color:#000000">retourne </span>  <span style="color:#93C47D"> __True__ </span>  <span style="color:#000000"> si la clé existe</span>

<span style="color:#4F81BD"> __Modifier une valeur__ </span>  <span style="color:#000000"> ou </span>  <span style="color:#4F81BD"> __Ajouter un couple__ </span>  <span style="color:#000000">\(selon si la clé existe ou pas\)</span>  <span style="color:#9BBB59">dico\[cle\] = valeur</span>

<span style="color:#4F81BD"> __Supprimer __ </span>  <span style="color:#000000">un couple</span>  <span style="color:#9BBB59">del dico\[cle\]</span>

<span style="color:#4F81BD"> __Vider __ </span>  <span style="color:#000000">un dictionnaire</span>  <span style="color:#9BBB59">dico\.clear\(\)</span>