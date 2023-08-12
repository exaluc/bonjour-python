---
title: Fonctions
---

Les fonctions sont des outils essentiels en programmation, permettant d'encapsuler du code pour des tâches spécifiques. Python regorge de fonctions prêtes à l'emploi, mais vous avez aussi la liberté de créer les vôtres.

#### **Définition et Appel de Fonctions** 📝

- **Définir une fonction** se fait avec le mot-clé `def`. Pensez-y comme à une recette que vous pouvez suivre encore et encore 🍪:

```python
def ma_fonction():
    print("Salut! C'est moi, ta fonction!")
```

- **Pour utiliser la recette (fonction)**, il suffit de l'appeler par son nom:

```python
ma_fonction()  # Affiche: "Salut! C'est moi, ta fonction!"
```

- **Paramètres:** Pensez aux paramètres comme aux ingrédients d'une recette. Ils changent le résultat final 🍰:

```python
def cafe(ingredient):
    print(f"Voici votre café avec {ingredient}!")
    
cafe("du lait")  # Affiche: "Voici votre café avec du lait!"
```

- **Retour de valeur:** Parfois, une fonction doit vous donner quelque chose en retour 🎁:

```python
def multiplier(x, y):
    return x * y

double = multiplier(3, 2)  # double vaut 6
```

#### **Fonctions Lambda** ⚡

Les fonctions lambda sont comme des raccourcis. Rapides et efficaces pour de petites tâches:

```python
inverse = lambda x: 1/x
print(inverse(2))  # Affiche: 0.5
```

#### **Fonctions Intégrées** 🔧

Python est comme une boîte à outils géante avec toutes sortes d'outils préfabriqués:

- **`print()`**: Votre outil pour envoyer des messages:

```python
print("Salut, monde!")  # 🌍
```

- **`len()`**: Mesurez tout ce qui est mesurable, comme les chaînes de caractères:

```python
taille = len("Chat")  # taille vaut 4 🐱
```

- **`type()`**: Quel genre d'outil avez-vous là?

```python
typ = type(True)  # typ vaut <class 'bool'> 🚦
```

- **Conversions**: Transformer un outil en un autre:

```python
texte = str(456)  # texte vaut "456" 📜
sequence = list("abc")  # sequence vaut ['a', 'b', 'c'] 📋
```

- **Créations**: Fabriquer des structures de données:

```python
mon_set = set([1, 1, 2, 3])  # mon_set vaut {1, 2, 3} 🧱
```

Pensez aux fonctions intégrées comme à des amis qui sont toujours là pour vous aider ! 😊