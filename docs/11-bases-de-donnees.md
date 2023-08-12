---
title: Travailler avec des Bases de Données en Python
---

#### **SQLite et Python** 📁

SQLite est une base de données relationnelle légère qui ne nécessite pas de serveur séparé pour fonctionner. C'est une excellente option pour les applications légères, les prototypes ou les applications de bureau.

1. **Création et Connexion à la base de données**:

```python
import sqlite3

connexion = sqlite3.connect('ma_base_de_donnees.db')
```

2. **Manipulation de Tables**:

```python
curseur = connexion.cursor()
curseur.execute("""
CREATE TABLE IF NOT EXISTS utilisateurs (
    id INTEGER PRIMARY KEY,
    nom TEXT NOT NULL,
    age INTEGER
)
""")
```

3. **Insertion de données**:

```python
curseur.execute("INSERT INTO utilisateurs (nom, age) VALUES (?, ?)", ("Alice", 30))
connexion.commit()
```

4. **Mise à jour de données**:

```python
curseur.execute("UPDATE utilisateurs SET age = ? WHERE nom = ?", (31, "Alice"))
connexion.commit()
```

5. **Suppression de données**:

```python
curseur.execute("DELETE FROM utilisateurs WHERE nom = ?", ("Alice",))
connexion.commit()
```

#### **Requêtes SQL avancées en Python** 🧐

1. **Filtrage**:

```python
curseur.execute("SELECT * FROM utilisateurs WHERE age > 25")
utilisateurs_majeurs = curseur.fetchall()
```

2. **Tri**:

```python
curseur.execute("SELECT * FROM utilisateurs ORDER BY age DESC")
utilisateurs_ordonnes = curseur.fetchall()
```

3. **Jointures**:

Si nous avons une autre table, disons `commandes`, nous pouvons lier les données entre les tables.

```python
curseur.execute("""
SELECT u.nom, c.produit 
FROM utilisateurs u 
JOIN commandes c ON u.id = c.id_utilisateur
""")
resultat_jointure = curseur.fetchall()
```

#### **ORMs: SQLAlchemy** 🔄

SQLAlchemy est un ORM qui permet de traduire les opérations avec la base de données en commandes Python.

1. **Modélisation**:

Avec SQLAlchemy, chaque table est représentée par une classe.

```python
from sqlalchemy import create_engine, Column, Integer, String
from sqlalchemy.ext.declarative import declarative_base

Base = declarative_base()

class Utilisateur(Base):
    __tablename__ = 'utilisateurs'
    id = Column(Integer, primary_key=True)
    nom = Column(String)
    age = Column(Integer)
```

2. **Création et Manipulation de la base de données**:

```python
engine = create_engine('sqlite:///ma_base_de_donnees.db')
Base.metadata.create_all(engine)

from sqlalchemy.orm import sessionmaker
Session = sessionmaker(bind=engine)
session = Session()
```

3. **Opérations CRUD**:

- Création:

```python
bob = Utilisateur(nom="Bob", age=35)
session.add(bob)
session.commit()
```

- Lecture:

```python
utilisateurs = session.query(Utilisateur).filter(Utilisateur.age > 25).all()
```

- Mise à jour:

```python
utilisateur = session.query(Utilisateur).filter(Utilisateur.nom == "Bob").first()
utilisateur.age = 36
session.commit()
```

- Suppression:

```python
session.delete(utilisateur)
session.commit()
```

---

Travailler avec des bases de données est un élément essentiel pour de nombreuses applications Python, que ce soit pour stocker des données locales ou pour interagir avec des bases de données externes. La facilité d'utilisation et la flexibilité offertes par Python dans ce domaine le rendent particulièrement attrayant pour le développement de bases de données. 📚👩‍💻👨‍💻🌐