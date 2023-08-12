---
title: Concepts Avancés
---

#### **Itérateurs et Générateurs** 🔁

- **Itérateurs**: Un itérateur est un objet qui produit les éléments à parcourir un à un. Vous avez probablement déjà utilisé `iter()` pour obtenir un itérateur à partir d'une liste ou d'une autre collection.

```python
iterateur = iter([1, 2, 3])
print(next(iterateur))  # Affiche: 1
```

- **Itération personnalisée**:

```python
class CompteARebours:
    def __init__(self, debut):
        self.debut = debut

    def __iter__(self):
        return self

    def __next__(self):
        if self.debut <= 0:
            raise StopIteration
        self.debut -= 1
        return self.debut + 1

for num in CompteARebours(3):
    print(num)
```

- **Générateurs**: Simples à utiliser, les générateurs sont des fonctions qui produisent une séquence de résultats plutôt que de renvoyer une valeur unique.

```python
def compte_a_rebours_gen(debut):
    while debut > 0:
        yield debut
        debut -= 1

for num in compte_a_rebours_gen(3):
    print(num)
```

#### **Compréhensions de Générateurs** 💡

Ce sont des expressions qui produisent un générateur.

```python
gen = (x**2 for x in range(3))
for val in gen:
    print(val)
```

#### **Décorateurs** ✨

Un décorateur est une fonction qui prend une autre fonction en argument, ajoute des fonctionnalités et renvoie la fonction.

- **Utilisation d'un décorateur pour logger**:

```python
def logger(fonction):
    def wrapper(*args, **kwargs):
        print(f"Exécution de la fonction {fonction.__name__}")
        return fonction(*args, **kwargs)
    return wrapper

@logger
def saluer(nom):
    print(f"Salut, {nom}!")

saluer("Alice")
```

#### **Métaclasses** 🛠

Une métclasse est une classe de classe. Les métaclasses contrôlent la création et l'initialisation des classes.

- **Utilisation d'une métclasse pour ajouter des attributs automatiquement**:

```python
class AttributAjouteMeta(type):
    def __init__(cls, nom, bases, dct):
        cls.attribut_ajoute = "Valeur ajoutée"
        super().__init__(nom, bases, dct)

class MaClasse(metaclass=AttributAjouteMeta):
    pass

print(MaClasse.attribut_ajoute)  # Affiche: "Valeur ajoutée"
```

#### **Context Managers et `with` Statement** 📂

Permet de gérer des ressources, comme les fichiers, de manière propre et efficace.

```python
with open('mon_fichier.txt', 'r') as fichier:
    for ligne in fichier:
        print(ligne, end="")
```

Avec les concepts avancés, vous pouvez écrire du code Python plus propre, plus efficace et plus Pythonique. Ces concepts peuvent sembler intimidants au début, mais une fois maîtrisés, ils peuvent être incroyablement puissants. Lancez-vous et explorez-les! 🚀📚