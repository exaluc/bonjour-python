### **Concepts Avancés en Python**

#### **Itérateurs et Générateurs**

- **Itérateurs**: En Python, un itérateur est un objet qui implémente les méthodes `__iter__()` et `__next__()`. Les itérateurs permettent aux objets d'être itérés (parcourus) en utilisant une boucle `for`.

```python
class MonIterateur:
    def __init__(self, max):
        self.max = max

    def __iter__(self):
        self.n = 0
        return self

    def __next__(self):
        if self.n <= self.max:
            result = 2 ** self.n
            self.n += 1
            return result
        else:
            raise StopIteration

mon_iter = MonIterateur(3)
for num in mon_iter:
    print(num)
```

- **Générateurs**: Les générateurs sont des fonctions qui retournent un objet qui peut être parcouru. Ils sont définis comme des fonctions normales, mais utilisent le mot-clé `yield` pour retourner des données.

```python
def mon_generateur(max):
    n = 0
    while n < max:
        yield 2 ** n
        n += 1

for num in mon_generateur(4):
    print(num)
```

#### **Décorateurs**

Les décorateurs sont une manière puissante de modifier ou d'étendre le comportement des fonctions ou des méthodes sans changer leur code source.

```python
def mon_decorateur(fonction):
    def wrapper():
        print("Quelque chose est exécuté avant la fonction.")
        fonction()
        print("Quelque chose est exécuté après la fonction.")
    return wrapper

@mon_decorateur
def dire_bonjour():
    print("Bonjour!")

dire_bonjour()
```

#### **Métaclasses**

Les métaclasses sont "des classes de classes". Elles définissent comment une classe se comporte. Une classe est en réalité une instance d'une métclasse.

```python
class MaMetaclasse(type):
    def __new__(cls, nom, bases, dct):
        dct['ajout'] = "Nouvel attribut ajouté"
        return super().__new__(cls, nom, bases, dct)

class MaClasse(metaclass=MaMetaclasse):
    pass

print(MaClasse.ajout)  # Affiche: "Nouvel attribut ajouté"
```

---

Ces concepts avancés en Python peuvent sembler déroutants au début, mais ils sont essentiels pour écrire du code Python efficace et modulaire, surtout dans des projets complexes ou des bibliothèques de code.

 