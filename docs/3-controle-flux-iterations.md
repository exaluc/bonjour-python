---
title: Contrôle de flux et Itération
---

#### **Instructions conditionnelles (if, elif, else)** 🌐

La prise de décision est fondamentale en programmation. Les instructions conditionnelles vous permettent d'exécuter certains codes en fonction de la validité d'une ou plusieurs conditions.

- **if:** Il s'agit de la condition de base. Si la condition est vraie, le code sous cette condition s'exécute.

📝 **Exemple :**
```python
age = 18
if age >= 18:
    print("Vous êtes majeur!")
```
Dans cet exemple, le message "Vous êtes majeur!" s'affiche uniquement si `age` est supérieur ou égal à 18.

- **elif:** Utilisé pour ajouter d'autres conditions après un `if`. C'est une manière élégante d'écrire une série de conditions.

📝 **Exemple :**
```python
note = 85
if note >= 90:
    print("Excellent!")
elif 70 <= note < 90:
    print("Bien joué!")
```
Le message "Bien joué!" s'affichera ici car la note est de 85.

- **else:** Cette instruction capture tout ce qui n'a pas été capté par les conditions précédentes.

📝 **Exemple :**
```python
jour = "dimanche"
if jour == "samedi":
    print("C'est le week-end!")
else:
    print("Ce n'est pas samedi.")
```

#### **Boucles (for et while)** 🔄

L'une des forces de la programmation est de répéter des tâches. Les boucles permettent de réaliser ces répétitions efficacement.

- **for:** Parfait pour parcourir une séquence. Il répète un bloc pour chaque élément d'une séquence.

📝 **Exemple :**
```python
noms = ["Alice", "Bob", "Charlie"]
for nom in noms:
    print(f"Bonjour, {nom}!")
```
Chaque nom de la liste sera salué par un "Bonjour".

- **while:** Répète un bloc tant qu'une condition est vraie.

📝 **Exemple :**
```python
compteur = 3
while compteur > 0:
    print(f"Compte à rebours: {compteur}")
    compteur -= 1
```
La boucle affiche un compte à rebours de 3 à 1.

#### **Break, Continue, et Pass** ⏯

Vous souhaitez avoir un contrôle plus fin sur vos boucles? Voici trois outils pour cela.

- **break:** C'est l'équivalent d'un bouton d'arrêt. Il met fin à la boucle immédiatement.

📝 **Exemple :**
```python
for lettre in "Python":
    if lettre == "h":
        break
    print(lettre)
# Résultat : P, y, t
```

- **continue:** Pensez-y comme un bouton "avance rapide". Il saute le reste de l'itération en cours.

📝 **Exemple :**
```python
for lettre in "Python":
    if lettre == "h":
        continue
    print(lettre)
# Résultat : P, y, t, o, n
```

- **pass:** C'est essentiellement un espace réservé. Utile lorsque vous devez respecter une syntaxe, mais que vous n'avez rien à exécuter.

📝 **Exemple :**
```python
for lettre in "Python":
    if lettre == "h":
        pass
    print(lettre)
# Résultat : P, y, t, h, o, n
```
Le "h" est inclus dans le résultat car `pass` ne fait rien.