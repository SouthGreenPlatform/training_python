## Entrées/sorties en console

Afficher du texte et des variables :  _print\(\)_

_nom = “Sebastien"_  _print\("Bonjour"\, nom\)_ \(print ajoute un espace entre les éléments automatiquement\. Modifiable avec le paramètre "sep"\)

Récupérer une information saisie par l'utilisateur :  _input\(\)_

_nom = input\("Quel est votre nom ? "\)_

## Entrées/sorties > Affichage formaté

_Formatage_  : Intégrer des variables dans une chaîne de caractères\, en contrôlant la manière dont elles s'affichent

_Fonction format\(\)_  _valeur = 34\.67644_  _print\("La valeur est \{\} \!"\.format\(valeur\)\)_

_f\-strings_ Même syntaxe que format\, affiche les variables sans avoir à les passer en paramètre _valeur = 34\.67644_  _print\(f"La valeur est \{valeur\} \!"\)_  _print\(f"La valeur arrondi est \{valeur:\.2f\} \!"\)_

<span style="color:#999999"> _\(opérateur % : ancienne syntaxe\)_ </span>

<span style="color:#FFFFFF"> __\!   Python >= 3\.6__ </span>