#### Passage d'arguments

Exemples

_note1 = input\("Donner une note : "\)_

_note2 = input\("Donner une note : "\)_

_note3 = input\("Donner une note : "\)_

_moy = \(int\(note1\)\+int\(note3\)\+int\(note2\)\)/3_

_print \("La moyenne est "\,moy\)_

<span style="color:#000000">On souhaite passer ces valeurs en argument au programme</span>

Exemples

_liste\_animaux = \['vache'\,'souris'\,'levure'\,'bacterie'\]_

_for nom in listeAnimaux:_

_print\(nom\)_

<span style="color:#000000">On souhaite passer ces valeurs en argument au programme</span>

Jusqu'à présent\, on utilise des données fixes ou demandées à l'utilisateur avec  __input\(\)__

On veut passer des  _arguments/paramètres_  au programme

pour permettre l'exécution du programme avec  _différentes données_  sans avoir à modifier le script

pour  _éviter l'interaction avec l'utilisateur_

_python3 exo3\.py 15 17 8_

<span style="color:#000000">Script qui attend les arguments</span>

<span style="color:#000000">argument du programme</span>

<span style="color:#000000">\(obligatoire ou avec valeur par default\)</span>

Récupérer les valeurs passées en argument au programme :Utilisation de la liste  _sys\.argv_  du module sys \( _import sys_ \)

_sys\.argv\[0\] _ ⇒ nom du programme

_sys\.argv\[1\]\.\.\.sys\.argv\[n\] _ ⇒ valeurs des arguments

__Exemple pour la commande __  _python exo3\.py 15 17 8_

_sys\.argv\[0\] = "exo3\.py"_

_sys\.argv\[1\] = "15"_

_sys\.argv\[2\] = "17"_

_sys\.argv\[3\] = "8"_

Vérifier qu'on a le  _bon nombre d'arguments _ = taille de  _sys\.argv_

Si on a 3 arguments\, alors  _len\(sys\.argv\) == 4_

__Si on a pas le bon nombre\, quitter le programme :__

_sys\.exit\(\)_  __sortie normale__

_sys\.exit\("Message d'erreur"\)_  __sortie avec erreur \(met le code d'erreur du shell à 1\)__