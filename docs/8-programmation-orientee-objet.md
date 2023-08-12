---
title: Programmation Orientée Objet (POO)
---

La POO est une méthode de programmation qui traite des programmes comme des collections d'objets interagissant les uns avec les autres, plutôt que comme des séquences d'instructions à exécuter.

#### **Introduction à la POO** 🌟

La POO est née de la nécessité de gérer de grands programmes et de réduire leur complexité. Elle offre une manière structurée de représenter le monde réel dans un programme, en le décomposant en objets ayant des attributs (caractéristiques) et des méthodes (actions).

#### **Classes et Objets** 🏫

- **Classe**: Pensez à la classe comme à un plan. Il définit les attributs et les méthodes nécessaires pour créer un objet.

```python
class Animal:
    def __init__(self, espece, nom):
        self.espece = espece
        self.nom = nom
    
    def parler(self):
        print(f"Je suis un {self.espece} et je m'appelle {self.nom}.")
```

- **Objet**: L'objet est une instance de la classe, avec des valeurs réelles.

```python
chien = Animal("chien", "Buddy")
chien.parler()  # Affiche: "Je suis un chien et je m'appelle Buddy."
```

#### **Héritage et Polymorphisme** 🌲

- **Héritage**: Permet à une nouvelle classe d'hériter des propriétés et méthodes d'une classe existante.

```python
class Oiseau(Animal):
    def __init__(self, nom, peut_voler=True):
        super().__init__("oiseau", nom)
        self.peut_voler = peut_voler

    def voler(self):
        if self.peut_voler:
            print(f"{self.nom} vole dans le ciel!")
        else:
            print(f"{self.nom} ne peut pas voler.")
```

- **Polymorphisme**: Offre une interface unique pour des types différents, ce qui permet d'utiliser des objets de différentes classes de manière interchangeable.

```python
chat = Animal("chat", "Whiskers")

def presenter_animal(animal):
    animal.parler()

presenter_animal(chien)
presenter_animal(Oiseau("Polly"))
```

#### **Encapsulation et Abstraction** 📦

- **Encapsulation**: Cela permet de masquer les détails internes d'un objet, ne montrant que ce qui est nécessaire.

```python
class Banque:
    def __init__(self):
        self.__balance = 0

    def deposer(self, montant):
        self.__balance += montant
        print(f"Vous avez déposé {montant}€. Solde actuel: {self.__balance}€.")
    
    def retirer(self, montant):
        if montant > self.__balance:
            print("Solde insuffisant!")
        else:
            self.__balance -= montant
            print(f"Vous avez retiré {montant}€. Solde actuel: {self.__balance}€.")
```

- **Abstraction**: Il s'agit de créer un modèle simple qui retire les détails complexes. En utilisant l'abstraction, vous pouvez cacher la complexité et ne montrer que les fonctionnalités essentielles.

```python
class AppareilElectronique:
    def allumer(self):
        pass

    def eteindre(self):
        pass

# Ici, les méthodes exactes pour allumer/éteindre ne sont pas définies. Ce sera le travail des classes qui hériteront de cette classe.
```

---

La POO offre une approche solide et modulaire pour construire des programmes, faciliter leur maintenance et améliorer la réutilisabilité du code. C'est comme construire avec des LEGOs: chaque pièce (ou objet) a sa propre structure et fonctionnalité, et vous pouvez les combiner de manière créative pour créer quelque chose de grand! 🌆