Voila une séquence au format fasta [sequence1.fa](../../data/files/sequence1.fa)

```
>gi|374429558|ref|NR_046237.1| Rattus norvegicus 18S ribosomal RNA (Rn18s), ribosomal RNA
TACCTGGTTGATCCTGCCAGTAGCATATGCTTGTCTCAAAGATTAAGCCATGCATGTCTAAGTACGCACG
GCCGGTACAGTGAAACTGCGAATGGCTCATTAAATCAGTTATGGTTCCTTTGGTCGCTCGCTCCTCTCCT
ACTTGGATAACTGTGGTAATTCTAGAGCTAATACATGCCGACGGGCGCTGACCCCCCTTCCCGTGGGGGG
AACGCGTGCATTTATCAGATCAAAACCAACCCGGTCAGCCCCCTCCCGGCTCCGGCCGGGGGTCGGGCGC
CGGCGGCTTTGGTGACTCTAGATAACCTCGGGCCGATCGCACGTCCCCGTGGCGGCGACGACCCATTCGA
```

* Créer un programme python `exo6_a.py` qui permet de lire le fichier `sequence1.fa` (dont le nom est passé en argument) contenant la séquence au format fasta et qui affiche cette séquence

* Créer un programme python `exo6_b.py` qui permet de lire un fichier (dont le nom est passé en argument) contenant la séquence au format fasta et qui affiche les résidus de la séquence écrits en minuscule (pas l’en-tête fasta ">....").
    
    Exemple d'affichage :
    ```
    tacctggttgatcctgccagtagcatatgcttgtctcaaagattaagccatgcatgtctaagtacgcacg
    gccggtacagtgaaactgcgaatggctcattaaatcagttatggttcctttggtcgctcgctcctctcct
    acttggataactgtggtaattctagagctaatacatgccgacgggcgctgaccccccttcccgtgggggga
    ...
    ```

* Créer un programme python `exo6_c.py` qui permet de lire un fichier (dont le nom est passé en argument) contenant la séquence au format fasta et qui affiche une ligne sur 2 de la séquence fasta : ligne 1 puis 3 puis 5 …  
    Exemple d'affichage :
    ```
    >gi|374429558|ref|NR_046237.1| Rattus norvegicus 18S ribosomal RNA (Rn18s)
    GCCGGTACAGTGAAACTGCGAATGGCTCATTAAATCAGTTATGGTTCCTTTGGTCGCTCGCTCCTCTCCT
    AACGCGTGCATTTATCAGATCAAAACCAACCCGGTCAGCCCCCTCCCGGCTCCGGCCGGGGGTCGGGCGC
    ```

Details de l’en-tête d'une séquence au format fasta (sequence1.fasta)
```
>gi|374429558|ref|NR_046237.1| Rattus norvegicus 18S ribosomal RNA (Rn18s)
```

* Créer un programme python `exo6_d.py` qui permet de lire un fichier (passé en argument) contenant plusieurs séquences au format fasta et qui affiche les en-têtes de ces séquences.
* Modifier le programme précédent `exo6_d.py` pour qu'il crée un fichier résultat ne contenant que les en-têtes des séquences fasta (en plus de l'affichage). Le nom du fichier résultat sera passé en argument.

    Exemple de fichier résultat :  
    ```
    >gi|374429558|ref|NR_046237.1| Rattus norvegicus 18S ribosomal RNA (Rn18s)
    >gi|374429558|ref|NR_046237.1| Rattus norvegicus 18S ribosomal RNA (Rn18s)
    >gi|374429558|ref|NR_046237.1| Rattus norvegicus 18S ribosomal RNA (Rn18s)
    >gi|374429558|ref|NR_046237.1| Rattus norvegicus 18S ribosomal RNA (Rn18s)
    ```

* Créer un programme python `exo6_e.py` qui permet de lire un fichier (passé en argument) contenant plusieurs séquences au format fasta et qui crée un fichier résultat (passé en argument) qui devra contenir uniquement le numéro gi et le numéro d'accession de chaque séquence du fichier d'entrée.

    Exemple de fichier résultat : 
    ``` 
    seq 1 => num gi : 374429558, num accession : NR_046237.1
    seq 2 => num gi : 374429558, num accession : NR_046237.1
    seq 3 => num gi : 374429558, num accession : NR_046237.1
    ```

* Créer un programme `exo6_f.py` qui prend en argument un fichier tabulé contenant 2 colonnes numériques et écrit un nouveau fichier tabulé en sortie contenant les 2 colonnes originales et une 3ème colonne contenant leur somme.  
Les noms des fichiers d’entrée et de sortie doivent être pris en argument.  
La première ligne du fichier tabulé est un en-tête, il faut juste ajouter le nom de la colonne supplémentaire `Somme`.  
Un fichier d’entrée d’exemple [fichier_tabule.tsv](../../data/files/fichier_tabulate.tsv) est disponible dans les données du cours.

    Exemple d'entrée :
    ```             				
    Valeur_1		Valeur_2		
    5				10
    3				22
    ```

    Exemple de sortie :
    ```
    Valeur_1		Valeur_2		Somme
    5				10				15
    3				22				25
    ```
