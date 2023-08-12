---
title: Modules et Paquets
---

En programmation Python, un module est un fichier contenant des définitions et des instructions Python. Le fichier nommé `module.py` a le nom de module `module` que vous pouvez utiliser dans un script Python avec le mot-clé `import`. Un paquet est une manière d'organiser des modules connexes dans un répertoire.

#### **Qu'est-ce que sont les Modules et les Paquets?** 🧩

- **Modules 📄**: Un module est essentiellement un fichier contenant du code Python. Il peut définir des fonctions, des classes et des variables, et peut également inclure du code exécutable.

  Exemple: `mon_module.py`

- **Paquets 📁**: Un paquet est un moyen d'organiser plusieurs modules en un seul répertoire. Ce répertoire contient un fichier spécial appelé `__init__.py` pour indiquer à Python que le répertoire doit être traité comme un paquet.

  Structure d'un paquet:
  ```
  mon_paquet/
  ├─ __init__.py
  ├─ module1.py
  └─ module2.py
  ```

#### **Importer des Modules** 🔄

- **Importation d'un module**:
  ```python
  import mon_module
  ```
  Après cette importation, vous pouvez accéder aux fonctions ou variables définies dans `mon_module` avec `mon_module.nom_fonction`.

- **Alias lors de l'importation** 🏷:
  ```python
  import mon_module as mm
  ```

- **Importer des éléments spécifiques d'un module** ⚙:
  ```python
  from mon_module import ma_fonction
  ```

#### **Explorer la Bibliothèque Standard Python** 📚

La bibliothèque standard Python offre une collection impressionnante de modules prêts à l'emploi. Voici quelques modules couramment utilisés:

- **`math`** 🧮: Fonctions mathématiques.
  ```python
  import math
  angle = math.radians(180)  # Convertit les degrés en radians
  ```

- **`datetime`** ⏰: Manipulation des dates et des temps.
  ```python
  from datetime import timedelta
  une_semaine = timedelta(days=7)
  ```

- **`os`** 💽: Interaction avec le système d'exploitation.
  ```python
  import os
  liste_fichiers = os.listdir('.')  # Liste tous les fichiers du répertoire courant
  ```

- **`sys`** 🖥: Interagit avec l'interpréteur Python.
  ```python
  import sys
  version = sys.version  # Récupère la version de Python en cours d'exécution
  ```

- **`json`** 📜: Encodage et décodage du format JSON.
  ```python
  import json
  donnees = json.dumps({"nom": "Jean", "age": 30})  # Convertit un dictionnaire en chaîne JSON
  ```

- **`random`** 🎲: Génère des nombres aléatoires.
  ```python
  import random
  nombre = random.randint(1, 10)  # Génère un nombre aléatoire entre 1 et 10
  ```

Ces modules ne sont qu'un petit aperçu de ce que la bibliothèque standard a à offrir. Elle est vaste et couvre presque tous les domaines imaginables, faisant de Python un outil puissant dès l'installation.