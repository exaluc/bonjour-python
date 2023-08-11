### **Structures de Données**

#### **Listes et Compréhensions de Liste**

- **Listes:** Une liste est une collection ordonnée et modifiable d'éléments. Les éléments d'une liste peuvent être de n'importe quel type.

```python
ma_liste = [1, 2, 3, 4, "python", 3.14]
```

- **Accès aux éléments:** Vous pouvez accéder à un élément de la liste en utilisant son index.

```python
premier_element = ma_liste[0]  # Résultat: 1
dernier_element = ma_liste[-1]  # Résultat: 3.14
```

- **Modification de la liste:** Les listes sont mutables, ce qui signifie que vous pouvez modifier, ajouter ou supprimer des éléments.

```python
ma_liste[4] = "JAVA"
ma_liste.append(5)  # Ajoute 5 à la fin de la liste
```

- **Compréhensions de liste:** C'est une manière concise de créer des listes.

```python
carres = [x**2 for x in range(10)]  # [0, 1, 4, 9, 16, 25, 36, 49, 64, 81]
```

#### **Tuples**

- **Tuples:** Un tuple est une collection ordonnée et non modifiable d'éléments.

```python
mon_tuple = (1, 2, 3, "python", 3.14)
```

- **Accès aux éléments:** Semblable aux listes, mais gardez à l'esprit que les tuples sont immuables.

```python
premier_element = mon_tuple[0]  # Résultat: 1
```

#### **Dictionnaires**

- **Dictionnaires:** Une collection non ordonnée de paires clé-valeur.

```python
mon_dico = {
    "nom": "Jean",
    "age": 30,
    "ville": "Paris"
}
```

- **Accès et modification:** 

```python
nom = mon_dico["nom"]  # Résultat: "Jean"
mon_dico["age"] = 31   # Modifie l'âge à 31
```

- **Ajout et suppression de clés:**

```python
mon_dico["profession"] = "Ingénieur"
del mon_dico["ville"]
```

#### **Ensembles (Sets)**

- **Sets:** Une collection non ordonnée d'éléments uniques.

```python
mon_ensemble = {1, 2, 3, 4, 4, 5, 5}
```

Cela crée un ensemble avec les éléments `{1, 2, 3, 4, 5}` car les ensembles ne permettent pas les doublons.

- **Opérations courantes sur les ensembles:** union, intersection, différence.

```python
A = {1, 2, 3, 4}
B = {3, 4, 5, 6}
union = A | B          # {1, 2, 3, 4, 5, 6}
intersection = A & B   # {3, 4}
difference = A - B     # {1, 2}
```


[🔙 Retour au README principal](./readme.md)