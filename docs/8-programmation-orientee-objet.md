### **Programmation Orientée Objet (POO)**

La POO est un paradigme de programmation qui repose sur l'idée de regrouper les données et les fonctions qui les manipulent en une seule unité appelée objet. En Python, la POO est facilitée par le concept de classes et d'objets.

#### **Introduction à la POO**

La Programmation Orientée Objet est basée sur des concepts qui cherchent à modulariser et organiser le code de manière plus intuitive et proche de la manière dont nous percevons le monde: en objets avec des propriétés (attributs) et des capacités (méthodes).

#### **Classes et Objets**

- **Classe**: Une classe est un blueprint ou un modèle pour créer des objets. Elle définit des attributs (variables) et des méthodes (fonctions).

```python
class Voiture:
    def __init__(self, marque, couleur):
        self.marque = marque
        self.couleur = couleur
    
    def klaxonner(self):
        print(f"{self.marque} dit: Klaxon!")
```

- **Objet**: Un objet est une instance d'une classe. C'est un exemplaire spécifique de la classe.

```python
ma_voiture = Voiture("Toyota", "rouge")
ma_voiture.klaxonner()  # Affiche: "Toyota dit: Klaxon!"
```

#### **Héritage et Polymorphisme**

- **Héritage**: C'est un mécanisme dans lequel une nouvelle classe est dérivée d'une classe existante. La nouvelle classe hérite des attributs et des méthodes de la classe de base.

```python
class VehiculeElectrique(Voiture):
    def __init__(self, marque, couleur, autonomie):
        super().__init__(marque, couleur)
        self.autonomie = autonomie

    def afficher_autonomie(self):
        print(f"Autonomie restante: {self.autonomie} km")
```

- **Polymorphisme**: C'est la capacité de prendre plusieurs formes. En POO, cela signifie que différentes classes peuvent être traitées comme des instances de la même classe grâce à l'héritage.

```python
def klaxonner_vehicule(vehicule):
    vehicule.klaxonner()

# Bien que les deux objets soient de types différents, ils peuvent être traités de la même manière grâce au polymorphisme.
klaxonner_vehicule(ma_voiture)
klaxonner_vehicule(VehiculeElectrique("Tesla", "noir", 500))
```

#### **Encapsulation et Abstraction**

- **Encapsulation**: C'est le regroupement des données (attributs) et des méthodes qui les manipulent en une seule unité (objet). Vous pouvez également restreindre l'accès aux attributs et méthodes en utilisant des modificateurs privés (`_` ou `__`).

```python
class ExempleEncapsulation:
    def __init__(self):
        self.public = "Je suis public!"
        self._protege = "Je suis protégé!"
        self.__prive = "Je suis privé!"
```

- **Abstraction**: Il s'agit de cacher la complexité réelle tout en exposant uniquement les parties essentielles. En POO, cela est réalisé en utilisant des classes et des objets.

 