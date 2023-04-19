#### Fichiers

Souvent en bioinfo\, on doit  _lire ou écrire des fichiers_

<span style="color:#000000">Ouvrir un fichier :</span>  _fd = open\("nom\_du\_fichier"\, "mode d'ouverture"\)_

__Modes d'ouverture :__

_"r"_  __ pour __  _lecture_

_"w"_  __ pour __  _écriture_  __\, __  _écrase_  __ le fichier si il existe déjà__

_"a"_  __ pour __  _écriture_  __\, __  _ajoute_  __ à la fin du fichier si il existe déjà__

_"x"_  __ pour __  _écriture_  __\, __  _échoue_  __ si le fichier existe déjà__

<span style="color:#000000">Python traite les fichiers comme des fichiers texte par défaut \(encodage utf\-8\)</span>

Souvent en bioinfo\, on doit  _lire ou écrire des fichiers_

<span style="color:#000000">Ouvrir un fichier :</span>  _fd = open\("nom\_du\_fichier"\, "mode d'ouverture"\)_

_fd_  __ est un objet représentant le fichier ouvert sur lequel on peut appeler des fonctions pour manipuler le fichier__

__Une fois les manipulations finies\, on doit impérativement __  _fermer le fichier_  __ \!__

_fd = open\("fichier\.txt"\, "r"\)_  <span style="color:#B7B7B7">\# ici instructions utilisant le fichier…</span>  _fd\.close\(\)_  <span style="color:#B7B7B7">\# ici on ne peut plus utiliser fd</span>

#### Fichiers > Lecture

_Lecture_  du fichier \(fichier ouvert en mode  _"r"_ \)

Le fichier a un curseur qui avance à chaque opération de lecture\.

<span style="color:#000000">Lire tout le fichier comme chaîne de caractères</span>  _chaine = fd\.read\(\)_

<span style="color:#000000">Lire n caractères du fichier comme chaîne de caractères</span>  _chaine = fd\.read\(n\)_

<span style="color:#000000">Lire une ligne du fichier comme chaîne de caractères</span>  _ligne = fd\.readline\(\)_

<span style="color:#000000">Lire toutes les lignes du fichier dans une liste</span>  _lignes = fd\.readlines\(\)_

<span style="color:#000000">Pour revenir au début </span>  <span style="color:#000000">: </span>  _fd\.seek\(0\)_

<span style="color:#4F81BD"> __Lecture__ </span>  <span style="color:#000000"> du fichier </span>  <span style="color:#000000">\(fichier ouvert en mode </span>  <span style="color:#9BBB59">"r"</span>  <span style="color:#000000">\)</span>

Lire le fichier  _ligne par ligne_  avec une  _boucle_  _for ligne in fd:_  _	print\(ligne\)_

\(Équivalent d'une boucle utilisant  _fd\.readline\(\)_ \)

La boucle utilise le curseur du fichier de la même manière que les autres fonctions \!

<span style="color:#F79646"> __Attention :__ </span>  <span style="color:#000000"> Les lignes lues par </span>  <span style="color:#9BBB59">readline\(\)</span>  <span style="color:#000000">\, </span>  <span style="color:#9BBB59">readlines\(\)</span>  <span style="color:#000000"> </span>  <span style="color:#000000">et la boucle </span>  <span style="color:#9BBB59">for</span>  <span style="color:#000000"> </span>  <span style="color:#000000">contiennent les sauts de ligne \(</span>  <span style="color:#9BBB59">"\\n"</span>  <span style="color:#000000">\)\. </span>

#### Fichiers > Écriture

_Écriture_  dans un fichier \(fichier ouvert en mode  _"w"_ \,  _"a" _ ou _ "x"_ \)

__Écrire une chaîne de caractères__  _fd\.write\(chaine\)_  _Attention :_  <span style="color:#000000"> n'ajoute pas automatiquement le saut de ligne \(</span>  _"\\n"_  <span style="color:#000000">\)</span>

__Écrire plusieurs lignes \(liste de chaînes de caractère\)__  _fd\.writelines\(liste\)_  _Attention :_  __ n'ajoute pas non plus les sauts de ligne \(__  _"\\n"_  __\)__

#### Fichiers

Ouverture du fichier avec  _with_  :  _fermeture automatique_

_fd = open\("fichier\.txt"\, "r"\)_  _print\(fd\.read\(\)\)_  _fd\.close\(\)_

<span style="color:#000000">Fichier fermé automatiquement :</span>

<span style="color:#000000">A la fin du bloc</span>

<span style="color:#000000">En cas d'erreur dans le bloc</span>

_with open\("fichier\.txt"\, "r"\) as fd:_

_	print\(fd\.read\(\)\)_

_print\("ici\, le fichier a été fermé automatiquement"\)_