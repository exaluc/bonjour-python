---
title: Structures de Données
---

#### **Listes et Compréhensions de Liste** 📜

- **Listes:** Une liste est une collection ordonnée et modifiable. Les éléments peuvent varier en type. 👍

```python
ma_liste = [1, 2, 3, 4, "python", 3.14]
```

- **Accès aux éléments:** Les indices font le lien ! 🎯

```python
premier_element = ma_liste[0]  # Résultat: 1
cinquieme_element = ma_liste[4]  # Résultat: "python"
```

- **Modification de la liste:** La mutabilité des listes offre une grande flexibilité. 🔄

```python
ma_liste[4] = "JAVA"  # Remplacer "python" par "JAVA"
ma_liste.extend([7,8])  # Ajouter plusieurs éléments en une fois
```

- **Compréhensions de liste:** Une manière élégante et rapide de générer des listes. ✨

```python
impairs = [x for x in range(10) if x % 2 != 0]  # [1, 3, 5, 7, 9]
```

#### **Tuples** 🔒

- **Tuples:** Similaires aux listes, mais immuables. Idéaux pour des données constantes. 🛑

```python
jours_semaine = ("Lundi", "Mardi", "Mercredi", "Jeudi", "Vendredi", "Samedi", "Dimanche")
```

- **Accès aux éléments:** Comme pour les listes, mais sans modification possible. 

```python
jour1 = jours_semaine[0]  # Résultat: "Lundi"
```

#### **Dictionnaires** 🔑

- **Dictionnaires:** Paires clé-valeur pour un stockage organisé et efficace. 📔

```python
personne = {
    "prénom": "Jean",
    "nom": "Dupont",
    "âge": 30,
    "hobbies": ["lecture", "cinéma", "randonnée"]
}
```

- **Accès et modification:** Grâce aux clés, c'est un jeu d'enfant ! 🎲

```python
nom = personne["nom"]  # Résultat: "Dupont"
personne["hobbies"].append("natation")  # Ajout d'un hobby
```

- **Méthodes utiles:** Les dictionnaires ont de nombreuses méthodes pour faciliter la vie. 🧰

```python
cles = personne.keys()  # Renvoie toutes les clés
valeurs = personne.values()  # Renvoie toutes les valeurs
```

#### **Ensembles (Sets)** 🔗

- **Sets:** Collections d'éléments uniques. Parfait pour éliminer les doublons ! 🚫

```python
nombres = {1, 2, 3, 3, 4, 4, 5}  # Résultat: {1, 2, 3, 4, 5}
```

- **Opérations courantes:** Les sets sont idéaux pour les opérations mathématiques.

```python
A = {1, 2, 3, 4}
B = {3, 4, 5, 6}
seulement_A = A.difference(B)  # {1, 2}
```

---

**Conseils pratiques:** 🚀

- Pour des données fixes et immuables, préférez les tuples.
- Pour stocker des paires clé-valeur, utilisez les dictionnaires.
- Si vous devez éliminer des doublons d'une liste, convertissez-la en set, puis à nouveau en liste.
- Les compréhensions de liste sont puissantes, utilisez-les pour rendre votre code plus pythonique.