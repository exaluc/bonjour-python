---
title: Les bases
---

#### **Syntaxe et Structure** ✍️

Python, reconnu pour sa lisibilité et sa simplicité, se distingue par sa syntaxe. Pour une initiation réussie, voici les éléments clés :

- **Indentation:** En Python, l'indentation (espaces ou tabulations) est primordiale pour délimiter des blocs de code. Traditionnellement, on utilise quatre espaces pour chaque niveau d'indentation. ⬅️

```python
for i in range(3):
    if i == 2:
        print(f"{i} est égal à 2.")
    else:
        print(f"{i} n'est pas égal à 2.")
```

- **Commentaires:** Le symbole `#` introduit un commentaire. Ils sont parfaits pour documenter et clarifier votre code. 💡

```python
# Voici une fonction d'accueil
def dire_bonjour():
    print("Bonjour tout le monde!")  # Et voilà un autre commentaire !
```

- **Instructions de fin:** En Python, la simplicité prime : oubliez les points-virgules en fin d'instruction. Chaque nouvelle ligne équivaut à une nouvelle instruction. 📜

#### **Variables et Types de Données** 🔢

- **Déclaration de variables:** Pas besoin de définir le type de la variable en amont. Une simple affectation suffit. 🔄

```python
prenom = "Alice"
nombre = 42
```

- **Types de données courants:** 📌
    - **Entiers (`int`):** Comme le `7`. Exemple: `x = 10`
    - **Flottants (`float`):** Avec des décimales, comme `5.7`. Exemple: `y = 5.7`
    - **Chaînes de caractères (`str`):** Pour le texte. Exemple: `z = "Python est génial!"`
    - **Listes:** Collections modifiables. Exemple: `ma_liste = [10, "Python", 5.5]`
    - **Dictionnaires:** Avec des paires clé-valeur. Exemple: `mon_dico = {"langage": "Python", "version": 3.9}`

- **Typage dynamique:** Une variable peut changer de type à la volée. 🔄

```python
a = 10         # Ici, `a` est un entier
a = "dix"      # Là, `a` est une chaîne
```

#### **Opérateurs de base** ➕

- **Opérateurs arithmétiques:** Pour les opérations mathématiques.
    - Addition: `3 + 4  # Résultat: 7`
    - Soustraction: `7 - 3  # Résultat: 4`
    - Multiplication: `4 * 3  # Résultat: 12`
    - ... et d'autres que vous avez déjà énumérés.

- **Opérateurs de comparaison:** Ils renvoient `True` ou `False`.
    - Égal à: `4 == 4  # True`
    - Différent de: `4 != 5  # True`
    - ... et d'autres que vous avez déjà mentionnés.

- **Opérateurs logiques:** Pour combiner des conditions. 
    - ET logique: `True and False  # Résultat: False`
    - OU logique: `True or False  # Résultat: True`
    - NON logique: `not True  # Résultat: False`
