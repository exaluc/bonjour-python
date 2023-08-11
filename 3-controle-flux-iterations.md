### **Contrôle de flux et Itération**

#### **Instructions conditionnelles (if, elif, else)**

Les instructions conditionnelles permettent d'exécuter certaines portions de code en fonction de la vérité d'une condition.

- **if:** exécute un bloc de code si la condition est vraie.

```python
if condition:
    # code à exécuter si la condition est vraie
```

- **elif:** ajoute une condition supplémentaire après un `if`. 

```python
if condition1:
    # code pour condition1
elif condition2:
    # code pour condition2
```

- **else:** exécute un bloc de code si aucune des conditions précédentes n'est vraie.

```python
if condition:
    # code pour condition
else:
    # code à exécuter si la condition est fausse
```

#### **Boucles (for et while)**

Les boucles permettent de répéter l'exécution d'un bloc de code.

- **for:** exécute un bloc de code pour chaque élément d'une séquence.

```python
for variable in séquence:
    # code à exécuter pour chaque élément
```

Exemple avec une liste:

```python
for num in [1, 2, 3, 4]:
    print(num)
```

- **while:** exécute un bloc de code tant qu'une condition est vraie.

```python
while condition:
    # code à exécuter tant que la condition est vraie
```

Exemple:

```python
compteur = 0
while compteur < 5:
    print(compteur)
    compteur += 1
```

#### **Break, Continue, et Pass**

Ces instructions sont utilisées pour modifier le comportement normal d'une boucle.

- **break:** termine la boucle courante.

```python
for num in [1, 2, 3, 4]:
    if num == 3:
        break
    print(num)
# Résultat : 1, 2
```

- **continue:** passe à l'itération suivante de la boucle, en sautant le reste du code de l'itération courante.

```python
for num in [1, 2, 3, 4]:
    if num == 3:
        continue
    print(num)
# Résultat : 1, 2, 4
```

- **pass:** une instruction vide, qui ne fait rien. Elle peut être utilisée comme un espace réservé lorsque une instruction est requise par la syntaxe, mais aucune action n'est nécessaire.

```python
for num in [1, 2, 3, 4]:
    if num == 3:
        pass
    print(num)
# Résultat : 1, 2, 3, 4
```


[🔙 Retour au README principal](./readme.md)