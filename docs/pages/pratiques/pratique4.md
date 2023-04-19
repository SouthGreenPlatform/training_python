* Créer un programme python `exo4_a.py` qui à partir de la séquence nucléique `TCTGTTAACCATCCACTTCG` (chaîne de caractères)
 crée sa séquence complémentaire inverse, puis l'affiche.

* Créer un programme python `exo4_b.py` qui compte le nombre de chacune des bases (A, T, G, C) présente dans la séquence nucléique `TCTGTTAACCATCCACTTCG`, puis qui affiche ces nombres. Vous ferez une version qui utilise la fonction count() des listes et une autre version qui ne l'utilise pas.

* Créer un programme python `exo4_c.py` qui vérifie si la sous-séquence `ATG` (codon start) est présente dans la séquence nucléique `TCTGTTATGACCATCCACTTCG`, puis affiche "oui" ou "non" en fonction du résultat. Par la suite, modifier le programme pour qu'il affiche également la position de la sous-séquence "ATG" si elle est présente.

* Reprendre l'un des programmes `exo4_a.py`, `exo4_b.py` ou `exo4_c.py` et faire en sorte qu'il fonctionne pour plusieurs séquences (les séquences seront stockées dans une liste et chacune des séquences sera analysée)

    Exemple : 
    ```python    
    seq1= "ATGCGTAGTCGT"
    seq2= "AGGTTCGTATG"
    mesSeq = [seq1,seq2]
    ```