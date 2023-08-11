### 14. **Python pour l'Analyse de Données**

---

Python est un outil puissant pour l'analyse de données, notamment grâce à des bibliothèques comme Pandas et NumPy. Plongeons dans cet univers captivant.

#### **Introduction à Pandas et NumPy**

Pandas est une bibliothèque de manipulation de données de haut niveau, construite sur la bibliothèque NumPy. Alors que NumPy est idéal pour travailler avec des tableaux de données homogènes, Pandas est conçu pour travailler avec des tableaux hétérogènes, souvent représentés sous forme de tableaux (ou DataFrames).

**Installation**:

```bash
pip install pandas numpy
```

#### **Découverte de Pandas**:

**Création d'un DataFrame simple**:

```python
import pandas as pd

data = {
    'Noms': ['Alice', 'Bob', 'Charlie'],
    'Âges': [25, 30, 35],
    'Ville': ['Paris', 'Lyon', 'Marseille']
}

df = pd.DataFrame(data)
print(df)
```

#### **Manipulation avec NumPy**:

NumPy est la bibliothèque de base pour la manipulation numérique en Python. Elle fournit des objets pour manipuler des tableaux de données de n'importe quel type.

```python
import numpy as np

array = np.array([1, 2, 3, 4, 5])
print(array)
```

#### **Nettoyage, Transformation et Visualisation des Données**:

Les données réelles sont souvent désordonnées. Pandas offre une variété d'outils pour traiter ces problèmes.

**Exemple de nettoyage**:

Supposons que nous ayons des données avec des valeurs manquantes:

```python
data = {
    'Noms': ['Alice', 'Bob', 'Charlie', 'David'],
    'Âges': [25, np.nan, 35, 40],
    'Ville': ['Paris', 'Lyon', 'Marseille', np.nan]
}

df = pd.DataFrame(data)
print(df)

# Supprimer les lignes avec des NaN
df_cleaned = df.dropna()
print(df_cleaned)
```

**Transformation**:

Supposons que vous vouliez ajouter 5 ans à chaque âge:

```python
df['Âges'] = df['Âges'].apply(lambda x: x + 5 if not np.isnan(x) else x)
print(df)
```

**Visualisation**:

Pour visualiser les données, nous pouvons utiliser la bibliothèque Matplotlib:

```bash
pip install matplotlib
```

```python
import matplotlib.pyplot as plt

ages = df['Âges'].dropna().tolist()
names = df['Noms'].tolist()

plt.bar(names, ages)
plt.xlabel('Noms')
plt.ylabel('Âges')
plt.title('Âge des personnes')
plt.show()
```

#### **Conclusion**:

Pandas et NumPy sont des outils essentiels pour toute personne souhaitant effectuer une analyse de données avec Python. Ce tutoriel offre une introduction, mais les possibilités offertes par ces bibliothèques sont immenses. Pour devenir vraiment compétent, il est recommandé de pratiquer régulièrement et de consulter la documentation officielle.


[🔙 Retour au README principal](./readme.md)