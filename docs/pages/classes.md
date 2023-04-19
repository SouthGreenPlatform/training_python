## Un type spécifique : les classes/objets

Les  _classes_  sont les principaux outils de la  _programmation orientée objet_ \.

Une  _classe_  peut comporter :

Des variables\, appelées  _attributs_

Des fonctions\, appelées  _méthodes_

Une  _instance_  d'une  _classe_  est un  _objet_

On peut appeler les  _attributs_  d'un objet en utilisant le \. : _objet\.attribut = 4					objet\.méthode\(\)_

_chaine_  =  _"Bonjour"_

la variable  _chaine_  est en réalité une instance de la classe  _str\. _

<span style="color:#FF0000"> __Tous les types en python sont des objets__ </span>

<span style="color:#000000">\# création de l’instance ‘</span>  __une\_cerise’ de la classe Cerise\(\)__

<span style="color:#000000">une\_cerise = Cerise\(\) </span>

<span style="color:#000000">\# exemple d’attributs</span>

__une\_cerise\.couleur = rouge__

__une\_cerise\.taille = 2__

__\# exemple d’une methode__

__une\_cerise\.enlever\_noyau\(\)__

## Examiner les objets / Obtenir de l’aide sur ...

_help\(obj\)_  : Affiche la documentation\. Fonctionne sur les modules\, les objets et les fonctions\.Raccourci sur IPython :  _?obj_

_dir\(obj\) _ : retourne la liste des attributs et méthodes de la classe de l’objet

<span style="color:#000000">>>> dir\(""\)</span>

<span style="color:#000000">\[ 'capitalize'\, 'casefold'\, 'center'\, 'count'\, 'encode'\, 'endswith'\, 'expandtabs'\, 'find'\, 'format'\,</span>

<span style="color:#000000"> 'format\_map'\, 'index'\, 'isalnum'\, 'isalpha'\, 'isascii'\, 'isdecimal'\, 'isdigit'\, 'isidentifier'\, 'islower'\,</span>

<span style="color:#000000"> 'isnumeric'\, 'isprintable'\, 'isspace'\, 'istitle'\, 'isupper'\, 'join'\, 'ljust'\, 'lower'\, 'lstrip'\, 'maketrans'\,</span>

<span style="color:#000000"> 'partition'\, 'replace'\, 'rfind'\, 'rindex'\, 'rjust'\, 'rpartition'\, 'rsplit'\, 'rstrip'\, 'split'\, 'splitlines'\, 'startswith'\,</span>

<span style="color:#000000"> 'strip'\, 'swapcase'\, 'title'\, 'translate'\, 'upper'\, 'zfill'\]</span>