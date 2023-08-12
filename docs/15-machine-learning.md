### 15. **Python pour l'Apprentissage Automatique (Machine Learning)**

---

Python est un choix de premier ordre pour l'apprentissage automatique, principalement en raison des bibliothèques puissantes qu'il propose. L'une des bibliothèques les plus appréciées pour cela est Scikit-learn. Dans cet article, nous allons découvrir cette bibliothèque et mettre en œuvre certains des algorithmes de machine learning fondamentaux.

#### **Introduction à Scikit-learn**

Scikit-learn est une bibliothèque pour l'apprentissage automatique en Python. Elle fournit des outils simples et efficaces pour l'analyse de données et la modélisation, avec des implémentations pour une grande variété d'algorithmes.

**Installation**:

```bash
pip install scikit-learn
```

#### **Découverte de Scikit-learn**:

La force de Scikit-learn réside dans son interface cohérente. La plupart du temps, vous allez:
- Charger vos données
- Préparer vos données
- Choisir un modèle
- Entraîner le modèle
- Évaluer le modèle
- Répéter si nécessaire

#### **Mise en œuvre d'algorithmes de base en Machine Learning**:

**1. Régression Linéaire**:

C'est l'un des algorithmes les plus simples. Il est utilisé pour prédire une valeur numérique.

```python
from sklearn.linear_model import LinearRegression
from sklearn.model_selection import train_test_split
from sklearn.metrics import mean_squared_error
import numpy as np

# Simulons quelques données
X = 2 * np.random.rand(100, 1)
y = 4 + 3 * X + np.random.randn(100, 1)

X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2)

model = LinearRegression()
model.fit(X_train, y_train)
y_pred = model.predict(X_test)

mse = mean_squared_error(y_test, y_pred)
print(f"Erreur quadratique moyenne : {mse:.2f}")
```

**2. Classification avec le K plus proches voisins (KNN)**:

Le KNN est un algorithme non paramétrique utilisé pour la classification et la régression.

```python
from sklearn.datasets import load_iris
from sklearn.neighbors import KNeighborsClassifier
from sklearn.model_selection import train_test_split
from sklearn.metrics import accuracy_score

iris = load_iris()
X_train, X_test, y_train, y_test = train_test_split(iris.data, iris.target, test_size=0.2)

knn = KNeighborsClassifier(n_neighbors=3)
knn.fit(X_train, y_train)
y_pred = knn.predict(X_test)

accuracy = accuracy_score(y_test, y_pred)
print(f"Précision du modèle : {accuracy*100:.2f}%")
```

 