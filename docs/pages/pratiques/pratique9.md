# Pratique 9

## Exercice A

Créer un programme python `exo9_a.py` qui permet de récupérer dans la banque de données Protein du NCBI les séquences du gène SRY (`SRY [gene]`) de l'homme (`Homo sapiens[Orgn]`) et qui crée un fichier résultat avec les séquences au format Genbank (option `rettype="gb"` de la fonction `efetch()`). Vous limiterez votre recherche aux 10 premières entrées de la banque (option `retmax` de la fonction `esearch()`).

## Exercice B

Créer un programme python `exo9_b.py` qui permet de faire la même chose que le programme précédent mais qui fait en sorte que le nom de la banque de données du NCBI, le nom du gène et de l'organisme, ainsi que le nom de fichier résultat soient donnés en argument à votre programme.

## Exercice C

Créer un programme python `exo9_c.py` qui à partir de 15 séquences d'un gène (donné par l'utilisateur en argument) récupérées sur une banque du NCBI  (donnée par l'utilisateur en argument) affiche à l'écran pour chaque séquence : « séquence nom_sequence de longueur lg_sequence »

Par exemple voilà l'affichage pour les 3 premières séquences récupérées pour le gène SRY dans la banque Protein du NCBI :  
```
sequence EDW99052 de longueur 530
sequence EDL09053 de longueur 395
sequence EAX02769 de longueur 204
```