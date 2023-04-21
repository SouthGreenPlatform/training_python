## Découper

__Découper__ une chaîne de caractères en __liste d'éléments__ (par défaut, espaces **et** tabulations)

```python
liste = chaine.split(separateur)
animaux = "girafe tigre singe"
ma_liste = animaux.split()
print(ma_liste)
>>> ["girafe", "tigre", "singe"]
```

__Découper__ une chaîne de caractères en __liste d'éléments__, en utilisant un __séparateur__ e.g. `;`

```python
liste = chaine.split(separateur)
animaux = "girafe;tigre;singe"
ma_liste = animaux.split(";")
print(ma_liste)
>>> ["girafe", "tigre", "singe"]
```

## Majuscule/minuscule

Mettre en __MAJUSCULE/minuscule__
```python
chaine_majuscule = chaine.upper()
chaine_mijuscule = chaine.lower()
chaine_capitalisee = chaine.capitalize()
```

## Convertir

Convertir une liste de chaînes de caractères en une seule chaîne de caractères

```python
chaine = "séparateur".join(liste)
liste = ["A", "T", "G", "CAAA"]
seq1 = "-".join(liste)	#=> "A-T-G-CAA"
seq2 = "".join(liste)	#=> "ATGCAA"
seq3 = " ".join(liste)	#=> "A T G CAA"
```

## Supprimer

__Supprimer certains caractères__ (donnés dans une chaine de caractères) __des extrémités d'une chaîne de caractères__ (par défaut : espaces, tabulations et sauts de ligne)

* des deux côtés de la chaîne (paramètres par défaut):  
```python
new_chaine = chaine.strip()
```

* a l'extrémité droite (retirera les `.` et les `;`):  
```python
new_chaine = chaine.rstrip(".;")
```

* a l'extrémité gauche (retirera les espaces, les tabulations et les sauts de ligne): 
```python
new_chaine = chaine.lstrip(" \t\n")
```