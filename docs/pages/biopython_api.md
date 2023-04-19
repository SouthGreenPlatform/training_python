## Récupérer des Séquences

Interroger les bases de données et télécharger des séquences
Ici on s'intéresse au BDD du NCBI (ex portail Entrez)

```python
from Bio import Entrez
```

__Important__ : préciser un email (conditions d'utilisation du NCBI)

```python
Entrez.email = "votre@email.fr"
```

1. __Effectuer une requête__ sur une base de données

    ```python
    fic_XML = Entrez.esearch(db=nom_db, term=requete, …)
    ```

    Renvoie le résultat sous la forme d'un fichier XML ouvert

2. __Parser le résultat__ dans un dictionnaire

    ```python
    dic_resultat = Entrez.read(fic_XML)
    ```

    Identifiants des séquences : `dico_resultat["IdList"]`

3. __Télécharger les séquences__ à partir des identifiants

    ```python
    fic_sequences = Entrez.efetch(
        db=nom_db,
        id=dic_resultat["IdList"],
        rettype=format
    )
    ```

    Renvoie un objet fichier ouvert, à lire avec SeqIO.read() ou SeqIO.parse().

4. Penser à __fermer les fichiers__ une fois qu'on a fini

    ```python
    fic_XML.close()
    fic_sequences.close()
    ```


## Documentation

Quelques liens utiles pour utiliser Biopython

* Cookbook : tutoriaux sur les différents composants  
[https://biopython\.org/DIST/docs/tutorial/Tutorial\.html](https://biopython.org/DIST/docs/tutorial/Tutorial.html)  
[https://biopython\.org/wiki/Category%3ACookbook](https://biopython.org/wiki/Category:Cookbook)

* API documentation : documentation complète de tous les objets et fonctions  
[http://biopython\.org/DIST/docs/api/](http://biopython.org/DIST/docs/api/)

* Un article/tutoriel en français  
[https://connect\.ed\-diamond\.com/GNU\-Linux\-Magazine/GLMFHS\-073/La\-bioinformatique\-avec\-Biopython](https://connect.ed-diamond.com/GNU-Linux-Magazine/GLMFHS-073/La-bioinformatique-avec-Biopython)


--8<-- "pages/pratiques/pratique9.md"