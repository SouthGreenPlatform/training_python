Écrire vos propres fonctions vous permet de __rendre un bloc de code réutilisable__ depuis n'importe où dans votre script, __autant de fois que nécessaire__.

Avantages :
* au lieu de copier coller : on modifie la fonction, cela change le comportement partout où elle est appelée
* lisibilité

## Syntaxe

```python
def nom_de_la_fonction(argument_1, argument2):
	# instructions…
	return valeur_de_retour
```

!!! Note
    les variables déclarées dans la fonction ne sont pas accessibles depuis l'extérieur (sauf la valeur de retour)
    ```python
    def fonction():
    	x = 3
    print(x)	   # Erreur !!
    ```

--8<-- "pages/pratiques/pratique10.md"