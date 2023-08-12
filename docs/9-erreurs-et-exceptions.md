### **Gestion des Erreurs et Exceptions**

La gestion des erreurs est essentielle pour tout programmeur. En Python, les erreurs peuvent être traitées efficacement à l'aide du mécanisme d'exceptions.

#### **Comprendre les Erreurs et Exceptions**

- **Erreur**: Il s'agit d'un problème dans le code qui empêche le programme de s'exécuter.

- **Exception**: Une fois que le programme est en cours d'exécution, s'il rencontre une situation qu'il ne sait pas comment gérer, il génère une exception.

#### **Blocs Try, Except et Finally**

- **Bloc `try`**: Le code susceptible de générer une exception est placé dans le bloc `try`.

- **Bloc `except`**: Si une exception est générée dans le bloc `try`, le contrôle est immédiatement transféré au bloc `except`, où l'exception peut être traitée.

- **Bloc `finally`**: Il est exécuté quel que soit le résultat des blocs `try` et `except`, généralement utilisé pour effectuer des opérations de nettoyage.

Exemple:
```python
try:
    resultat = 10 / 0
except ZeroDivisionError:
    print("Division par zéro!")
finally:
    print("Ce code s'exécute quoi qu'il arrive.")
```

Dans l'exemple ci-dessus, le bloc `try` génère une exception `ZeroDivisionError`, le contrôle est donc transféré au bloc `except`, et après cela, le bloc `finally` est exécuté.

#### **Exceptions Personnalisées**

Vous pouvez définir vos propres exceptions en Python. Ces exceptions doivent être dérivées, directement ou indirectement, de la classe `Exception`.

Exemple:

```python
class ValeurTropHaute(Exception):
    pass

class ValeurTropBasse(Exception):
    pass

nombre = 10

try:
    entree = int(input("Entrez un nombre: "))
    if entree > nombre:
        raise ValeurTropHaute
    elif entree < nombre:
        raise ValeurTropBasse
except ValeurTropHaute:
    print("Cette valeur est trop haute!")
except ValeurTropBasse:
    print("Cette valeur est trop basse!")
```

Dans cet exemple, nous avons créé deux exceptions personnalisées, `ValeurTropHaute` et `ValeurTropBasse`. Si l'utilisateur entre un nombre trop élevé ou trop bas, l'exception appropriée est levée à l'aide du mot-clé `raise`.

 