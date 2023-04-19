#### Manipulation des chaînes de caractères

_Découper_  une chaîne de caractères en  _liste d'éléments_ \, en utilisant un  _séparateur_  \(par défaut\, espaces  _et_  tabulations\)

_liste = chaine\.split\(separateur\)_

_animaux = "girafe tigre singe"_  _ma\_liste = animaux\.split\(\)_  _print\(ma\_liste\)_

=>  _\["girafe"\, "tigre"\, "singe"\]_

_Découper_  une chaîne de caractères en  _liste d'éléments_ \, en utilisant un  _séparateur_  \(par défaut\, espaces  _et_  tabulations\)

_liste = chaine\.split\(separateur\)_

_animaux = "girafe;tigre;singe"_  _ma\_liste = animaux\.split\(";"\)_  _print\(ma\_liste\)_

=>  _\["girafe"\, "tigre"\, "singe"\]_

Mettre en  _MAJUSCULE/minuscule_

_chaine\_majuscule = chaine\.upper\(\)_  _chaine\_mijuscule = chaine\.lower\(\)_  _chaine\_capitalisee = chaine\.capitalize\(\)_

<span style="color:#4F81BD"> __Convertir__ </span>  <span style="color:#000000"> une </span>  <span style="color:#4F81BD"> __liste de chaînes de caractères__ </span>  <span style="color:#000000"> en </span>  <span style="color:#4F81BD"> __une seule chaîne de caractères__ </span>

<span style="color:#9BBB59">chaine = "séparateur"\.join\(liste\)</span>

<span style="color:#9BBB59">liste = \["A"\, "T"\, "G"\, "CAAA"\]</span>  <span style="color:#9BBB59">seq1 = "\-"\.join\(liste\)</span>  <span style="color:#9BBB59">	</span>  <span style="color:#000000"> __=>__ </span>  <span style="color:#9BBB59"> "A\-T\-G\-CAA"</span>  <span style="color:#9BBB59">seq2 = ""\.join\(liste\)		</span>  <span style="color:#000000"> __=>__ </span>  <span style="color:#9BBB59"> "ATGCAA"</span>  <span style="color:#9BBB59">seq3 = " "\.join\(liste\)	</span>  <span style="color:#000000"> __=>__ </span>  <span style="color:#9BBB59"> "A T G CAA"</span>

_Supprimer certains caractères_  \(donnés dans une chaine de caractères\)  _des extrémités d'une chaîne de caractères_  \(par défaut : espaces\, tabulations et sauts de ligne\)

des deux côtés de la chaîne : _new\_chaine = chaine\.strip\(\)_ \(paramètres par défaut\)

a l'extrémité droite : _new\_chaine = chaine\.rstrip\("\.;"\)_ \(retirera les \. et les ;\)

a l'extrémité gauche _new\_chaine = chaine\.lstrip\(" \\t\\n"\)_ \(retirera les espaces\, les tabulations et les sauts de ligne\)