---
title: Python pour l'Analyse de Données
---

Le monde des données est vaste et en constante évolution. Python, grâce à sa simplicité et sa flexibilité, est devenu l'outil privilégié des analystes. Découvrons comment Pandas et NumPy nous aident à naviguer dans ce monde.

#### **Introduction à Pandas et NumPy** 📚

Pandas, construit sur NumPy, est la pierre angulaire de l'analyse de données avec Python. Alors que NumPy est axé sur les tableaux numériques, Pandas étend cette capacité pour traiter des données plus complexes et structurées.

**Installation**:

```bash
pip install pandas numpy
```

#### **Découverte de Pandas** 🐼

Pandas introduit le concept de DataFrame, qui est essentiellement un tableau 2D avec des étiquettes.

**Chargement d'un fichier CSV**:

```python
df = pd.read_csv('mon_fichier.csv')
print(df.head())  # Affiche les 5 premières lignes
```

**Sélection de colonnes et de lignes spécifiques**:

```python
ages = df['Ages']
alice_data = df[df['Noms'] == 'Alice']
```

#### **NumPy à la rescousse** ⚙️

NumPy est essentiel pour les opérations numériques complexes.

**Création d'un tableau 2D**:

```python
matrix = np.array([[1, 2, 3], [4, 5, 6], [7, 8, 9]])
print(matrix)
```

**Opérations mathématiques**:

```python
print(np.mean(array))  # Calculer la moyenne
print(np.median(array))  # Médiane
```

#### **Nettoyage et Transformation des Données** 🧹

La qualité des données est essentielle pour une bonne analyse.

**Remplacement des valeurs manquantes**:

Au lieu de simplement supprimer les données manquantes, nous pouvons les imputer :

```python
df['Ages'].fillna(df['Ages'].mean(), inplace=True)  # Remplacer par la moyenne
```

**Transformation des données**:

Par exemple, convertir une colonne de chaînes de caractères en catégories numériques:

```python
df['Ville_Cat'] = df['Ville'].astype('category').cat.codes
```

#### **Visualisation avec Pandas et Matplotlib** 📉

La visualisation est essentielle pour comprendre vos données.

```bash
pip install matplotlib seaborn
```

```python
import seaborn as sns

# Histogramme
df['Ages'].hist(edgecolor='black')

# Diagramme de dispersion
df.plot(kind='scatter', x='Ages', y='Ville_Cat')

sns.pairplot(df, hue='Ville')  # Matrice de dispersion avec Seaborn
```

#### **Exploitation avancée des données avec GroupBy** 🔄

Pandas permet de regrouper des données de manière intuitive.

```python
grouped = df.groupby('Ville')
print(grouped.mean())  # Moyenne d'âge par ville
```

#### **Conclusion** 🚀

Python, avec Pandas et NumPy, est une puissante combinaison pour l'analyse de données. Ce guide offre un aperçu, mais l'univers des données est vaste. Pour maîtriser ces outils, il est essentiel de s'immerger dans des projets réels, de pratiquer continuellement et d'explorer les richesses de la documentation officielle.