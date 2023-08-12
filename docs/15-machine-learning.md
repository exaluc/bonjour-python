---
title: Apprentissage Automatique (Machine Learning)
---

Dans l'univers moderne du big data, Python s'impose comme une référence dans l'apprentissage automatique grâce à des bibliothèques robustes comme Scikit-learn. Ce guide explorera les nuances de Scikit-learn et sa capacité à modéliser des phénomènes complexes à partir de données.

#### **Introduction à Scikit-learn** 📘

Scikit-learn est un pilier de la modélisation en Python, offrant une interface intuitive pour divers algorithmes, des pré-traitements aux méthodes d'évaluation.

**Installation**:

```bash
pip install scikit-learn
```

#### **Préparation des Données avec Scikit-learn** ⚙️

Avant toute modélisation, il est crucial de préparer les données. Scikit-learn propose des outils pour cela.

**Standardisation**:

La mise à l'échelle des données est souvent nécessaire pour que certains algorithmes fonctionnent correctement.

```python
from sklearn.preprocessing import StandardScaler

scaler = StandardScaler()
X_train_scaled = scaler.fit_transform(X_train)
X_test_scaled = scaler.transform(X_test)
```

**Encodage de variables catégorielles**:

```python
from sklearn.preprocessing import OneHotEncoder

encoder = OneHotEncoder()
X_encoded = encoder.fit_transform(X_categorical).toarray()
```

#### **Modélisation avec Scikit-learn** 🛠️


Les algorithmes sont l'âme de la machine learning, et Scikit-learn en propose une multitude.

**3. Machines à Vecteurs de Support (SVM)**:

Les SVM sont puissants pour la classification et la régression.

```python
from sklearn.svm import SVC
from sklearn.metrics import classification_report

svm = SVC(kernel='linear')
svm.fit(X_train_scaled, y_train)
y_pred = svm.predict(X_test_scaled)

print(classification_report(y_test, y_pred))
```

**4. Arbres de décision**:

Ils permettent une classification ou une régression basée sur une structure d'arbre.

```python
from sklearn.tree import DecisionTreeClassifier

tree = DecisionTreeClassifier()
tree.fit(X_train, y_train)
y_pred = tree.predict(X_test)

accuracy = accuracy_score(y_test, y_pred)
print(f"Précision de l'arbre de décision : {accuracy*100:.2f}%")
```

#### **Évaluation et Optimisation des Modèles** 🎯

Il ne suffit pas d'entraîner un modèle; il faut l'évaluer et l'optimiser.

**Validation croisée**:

Permet d'évaluer les performances d'un modèle de manière robuste.

```python
from sklearn.model_selection import cross_val_score

scores = cross_val_score(tree, X_train, y_train, cv=5)
print(f"Scores de validation croisée: {scores}")
print(f"Moyenne: {scores.mean():.2f}")
```

**Recherche par grille (Grid Search)**:

Optimise les hyperparamètres d'un modèle.

```python
from sklearn.model_selection import GridSearchCV

param_grid = {
    'n_neighbors': [3, 5, 11, 19],
    'weights': ['uniform', 'distance'],
    'metric': ['euclidean', 'manhattan']
}

grid_search = GridSearchCV(KNeighborsClassifier(), param_grid, cv=5)
grid_search.fit(X_train, y_train)
```

#### **Conclusion** 🌟

Scikit-learn est un trésor pour quiconque s'intéresse au machine learning en Python. Son éventail d'outils, allant du pré-traitement à l'évaluation, en fait un incontournable. Bien que ce guide couvre les bases, la maîtrise de Scikit-learn nécessite une exploration approfondie et une pratique régulière. N'hésitez pas à plonger dans la documentation officielle pour une exploration plus détaillée!