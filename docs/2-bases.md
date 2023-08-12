### **Les bases de Python**

#### **Syntaxe et Structure**

Python est reconnu pour sa lisibilité et sa clarté. Voici quelques éléments clés de la syntaxe de Python:

- **Indentation:** Contrairement à de nombreux autres langages, Python utilise l'indentation (des espaces ou des tabulations) pour délimiter les blocs de code. Il est courant d'utiliser 4 espaces pour chaque niveau d'indentation.

```python
if True:
    print("L'indentation est correcte!")
```

- **Commentaires:** En Python, tout ce qui suit le symbole `#` sur une ligne est considéré comme un commentaire et n'est pas exécuté.

```python
# Ceci est un commentaire
print("Ceci n'est pas un commentaire")  # Mais ceci est un commentaire aussi!
```

- **Instructions de fin:** Contrairement à certains autres langages, Python n'utilise pas de point-virgule (`;`) à la fin des instructions. Chaque instruction est généralement sur une nouvelle ligne.

#### **Variables et Types de Données**

- **Déclaration de variables:** En Python, les variables ne nécessitent pas de déclaration explicite. Vous pouvez directement assigner une valeur à une variable.

```python
nom = "Jean"
age = 30
```

- **Types de données courants:**

    - **Entiers (`int`):** `x = 5`
    - **Flottants (`float`):** `y = 3.14`
    - **Chaînes de caractères (`str`):** `z = "Bonjour"`
    - **Listes:** `ma_liste = [1, 2, 3, 4]`
    - **Dictionnaires:** `mon_dico = {"clé": "valeur", "nom": "Jean"}`

- **Type dynamique:** Python est un langage à typage dynamique, ce qui signifie que le type d'une variable est déterminé à l'exécution et peut être modifié.

```python
x = 5          # x est un int
x = "Python"   # Maintenant, x est un str
```

#### **Opérateurs de base**

- **Opérateurs arithmétiques:**
    - Addition: `x + y`
    - Soustraction: `x - y`
    - Multiplication: `x * y`
    - Division: `x / y`
    - Division entière: `x // y`
    - Modulo (reste de la division): `x % y`
    - Puissance: `x ** y`

- **Opérateurs de comparaison:**
    - Égal à: `x == y`
    - Différent de: `x != y`
    - Plus grand que: `x > y`
    - Moins grand que: `x < y`
    - Plus grand ou égal à: `x >= y`
    - Moins grand ou égal à: `x <= y`

- **Opérateurs logiques:**
    - ET logique: `x and y`
    - OU logique: `x or y`
    - NON logique: `not x`

 