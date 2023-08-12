### **Travailler avec des Bases de Données en Python**

#### **SQLite et Python**

SQLite est une base de données relationnelle intégrée à Python. Il n'est pas nécessaire d'installer de modules externes pour l'utiliser.

Exemple d'utilisation de SQLite en Python:

```python
import sqlite3

# Se connecter à une base de données (ou la créer si elle n'existe pas)
connexion = sqlite3.connect('ma_base_de_donnees.db')

# Créer une table
curseur = connexion.cursor()
curseur.execute("""
CREATE TABLE IF NOT EXISTS utilisateurs (
    id INTEGER PRIMARY KEY,
    nom TEXT,
    age INTEGER
)
""")

# Insérer des données
curseur.execute("INSERT INTO utilisateurs (nom, age) VALUES (?, ?)", ("Alice", 30))

# Valider les modifications
connexion.commit()

# Fermer la connexion
connexion.close()
```

#### **Introduction aux Requêtes SQL en Python**

On peut exécuter n'importe quelle requête SQL en Python grâce au module `sqlite3`:

```python
connexion = sqlite3.connect('ma_base_de_donnees.db')
curseur = connexion.cursor()

# Sélectionner des données
curseur.execute("SELECT * FROM utilisateurs")
utilisateurs = curseur.fetchall()

for utilisateur in utilisateurs:
    print(utilisateur)

connexion.close()
```

#### **ORMs comme SQLAlchemy**

Un ORM (Object-Relational Mapping) permet de travailler avec des bases de données en utilisant la POO. SQLAlchemy est l'un des ORM les plus populaires en Python.

Exemple basique d'utilisation de SQLAlchemy:

```python
from sqlalchemy import create_engine, Column, Integer, String, Sequence
from sqlalchemy.ext.declarative import declarative_base
from sqlalchemy.orm import sessionmaker

Base = declarative_base()

class Utilisateur(Base):
    __tablename__ = 'utilisateurs'
    id = Column(Integer, Sequence('utilisateur_id_seq'), primary_key=True)
    nom = Column(String(50))
    age = Column(Integer)

# Connecter à la base de données
engine = create_engine('sqlite:///ma_base_de_donnees.db')
Base.metadata.create_all(engine)

# Créer une session
Session = sessionmaker(bind=engine)
session = Session()

# Ajouter un utilisateur
nouvel_utilisateur = Utilisateur(nom='Bob', age=40)
session.add(nouvel_utilisateur)
session.commit()

# Récupérer des utilisateurs
utilisateurs = session.query(Utilisateur).all()
for utilisateur in utilisateurs:
    print(utilisateur.nom, utilisateur.age)
```

---

Travailler avec des bases de données en Python est assez direct grâce aux modules intégrés et aux puissantes bibliothèques tierces disponibles.

 