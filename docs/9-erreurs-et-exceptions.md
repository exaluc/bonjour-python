---
title: Gestion des Erreurs et Exceptions
---

La robustesse d'un programme réside souvent dans sa capacité à gérer les imprévus. Python fournit des outils puissants pour traiter et anticiper les erreurs à travers le mécanisme d'exceptions.

#### **Comprendre les Erreurs et Exceptions** 💡

- **Erreur (Bug)**: Il s'agit d'un défaut dans le code. Par exemple, une variable non définie.
  
- **Exception**: C'est un événement qui se produit pendant l'exécution du programme et qui interrompt le flux normal d'instructions.

#### **Blocs Try, Except, Else et Finally** 🛑

- **Bloc `try`**: Contient le code susceptible de générer une exception.
  
- **Bloc `except`**: Gère l'exception si elle est levée dans le bloc `try`.
  
- **Bloc `else`**: Ce bloc est exécuté si aucune exception n'est levée dans le bloc `try`.
  
- **Bloc `finally`**: Exécuté toujours à la fin, qu'une exception soit levée ou non.

```python
try:
    resultat = int(input("Entrez un nombre: ")) / 2
except ValueError:
    print("Veuillez entrer un nombre valide!")
else:
    print(f"La moitié de votre nombre est {resultat}.")
finally:
    print("Merci d'avoir participé!")
```

#### **Types courants d'Exceptions** 📌

Python possède de nombreuses exceptions intégrées comme:

- `ValueError`: Lorsqu'une fonction reçoit un argument de valeur correcte mais de type inapproprié.
- `TypeError`: Lorsque une opération est appliquée au type inapproprié.
- `FileNotFoundError`: Lorsqu'un fichier ou un répertoire est demandé mais n'existe pas.

#### **Levée d'Exceptions** 🚀

Le mot-clé `raise` permet de lancer une exception spécifique, ce qui peut être utile pour signaler des erreurs dans votre propre code.

```python
age = int(input("Quel est votre âge? "))
if age < 0:
    raise ValueError("L'âge ne peut pas être négatif!")
```

#### **Assertions** ⛔

Les assertions sont un outil de débogage, elles testent une condition et déclenchent une exception si la condition est fausse.

```python
age = int(input("Entrez votre âge: "))
assert age >= 0, "L'âge ne peut pas être négatif!"
```

#### **Exceptions Personnalisées** 🎨

La création d'exceptions personnalisées peut aider à clarifier votre code et à traiter des cas spécifiques.

```python
class AgeNegatif(Exception):
    """Exception levée pour un âge négatif."""
    pass

age = int(input("Entrez votre âge: "))
if age < 0:
    raise AgeNegatif("L'âge ne peut pas être négatif!")
```

---

La gestion des erreurs est essentielle pour la robustesse d'un programme. La capacité de prévoir, gérer et communiquer les erreurs rend un programme plus fiable et plus convivial.