### **Fonctions**

Les fonctions sont des blocs de code réutilisables qui effectuent une tâche spécifique. En Python, il existe des fonctions intégrées, et vous pouvez également définir vos propres fonctions.

#### **Définition et Appel de Fonctions**

- **Définir une fonction** avec le mot-clé `def` suivi du nom de la fonction et des parenthèses `()`:

```python
def ma_fonction():
    print("Bonjour depuis ma fonction!")
```

- **Appel de la fonction** en utilisant son nom suivi de parenthèses:

```python
ma_fonction()  # Affiche: "Bonjour depuis ma fonction!"
```

- **Paramètres:** Une fonction peut accepter des valeurs, appelées paramètres, qui affectent son comportement:

```python
def saluer(nom):
    print(f"Bonjour, {nom}!")
    
saluer("Lucian")  # Affiche: "Bonjour, Lucian!"
```

- **Retour de valeur:** Une fonction peut renvoyer une valeur à l'aide du mot-clé `return`:

```python
def additionner(x, y):
    return x + y

resultat = additionner(3, 4)  # resultat vaut 7
```

#### **Fonctions Lambda**

Une fonction lambda est une petite fonction anonyme qui peut avoir un nombre quelconque de paramètres, mais ne peut avoir qu'une seule expression.

```python
carre = lambda x: x**2
print(carre(5))  # Affiche: 25
```

#### **Fonctions Intégrées**

Python fournit de nombreuses fonctions intégrées qui sont toujours disponibles. Voici quelques exemples courants:

- **`print()`**: Affiche des messages ou des variables:

```python
print("Bonjour!")
```

- **`len()`**: Renvoie la longueur d'un objet, comme une liste ou une chaîne:

```python
longueur = len("Python")  # longueur vaut 6
```

- **`type()`**: Renvoie le type d'un objet:

```python
typ = type(123)  # typ vaut <class 'int'>
```

- **`str()`, `int()`, `float()`**: Convertissent des valeurs en chaîne de caractères, entier ou nombre à virgule flottante respectivement:

```python
nombre = str(123)  # nombre vaut "123"
```

- **`list()`, `tuple()`, `dict()`, `set()`**: Convertissent des valeurs en liste, tuple, dictionnaire ou ensemble respectivement.

Il existe de nombreuses autres fonctions intégrées en Python, et elles sont conçues pour faciliter et accélérer votre codage.

 