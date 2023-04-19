On peut vouloir appeler un programme extérieur depuis notre script et récupérer sa sortie

Module subprocess (`import subprocess`)

Commande à donner sous forme de __liste de chaînes de caractères__, chaque argument étant une nouvelle chaîne.

Ajouter l'option `stdout` pour capturer la sortie et `text` pour automatiquement la décoder (comme à l'ouverture d'un fichier).

Renvoie un objet `CompletedProcess`, la sortie est accessible sur l'argument `.stdout`.

```python 
import subprocess
commande = ["programme", "argument1", "argument2"...]
process = subprocess.run(
    	commande,
    	stdout=subprocess.PIPE,
    	text=True
)
print(process.stdout)
```

Arguments de subprocess utiles :  

* `stdout=subprocess.PIPE` : récupérer la sortie standard du programme

* `check=True` : génère une exception si le programme rencontre une erreur (code de sortie ≠ 0)

* `shell=True` : exécuter la commande dans un __shell__  
(pour utiliser les pipes | , les redirections >, …).  
Dans ce cas, la commande doit être une chaîne de caractères.

* `timeout=10` : définit un __délai d'exécution__, en secondes.Une erreur se produira si le programme dépasse ce délai.


Consultez la documentation !   
[https://docs.python.org/3/library/subprocess.html](https://docs.python.org/3/library/subprocess.html)
