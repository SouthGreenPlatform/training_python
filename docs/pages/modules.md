
Python met à disposition des __modules__ qui contiennent des __fonctions souvent utilisées__ ou pour __interagir__ avec le __système__ 

!!! note
    modules = bibliothèques/librairies

Utilisation d'un module :  

* __Installer__ le module si il n'est pas dans la librairie standard 
```python
python3 –m pip install
```

* __Importer__ le module en début de programme
```python
import nom_module
```

* Appeler un objet/une fonction d'un module
```python
nom_module.fonction()
```

* Aide sur un module
```python 
help(nom_module) # 	sur IPython : ?nom_module
```

Quelques modules de la librairie standard utiles :

* `math` : fonctions et constantes mathématiques de base (sin, cos, exp, pi…)
* `random` : génération de l'aléatoire (nombres, choix…)
* `sys` : passage d'argument, gestion de l'entrée/sortie standard…
* `os` : dialogue avec le système d'exploitation (système de fichiers, variables d'environnement…)
* `subprocess` : lancer d'autre programmes à partir de Python
* `re` : utilisation des expressions régulières
* `csv`, `json` : lecture et écriture des formats éponymes
* `pathlib` : gestion des chemins des fichiers et repertoires 

!!! note
    Tous les modules de la librairie standard et leur documentation :  
    https://docs.python.org/3/library/index.html
