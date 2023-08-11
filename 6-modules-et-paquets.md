### **Modules et Paquets**

Dans la programmation Python, un module est un fichier contenant des définitions et des instructions Python. Le fichier nommé `module.py` a le nom de module `module` que vous pouvez utiliser dans un script Python avec le mot-clé `import`. Un paquet est une manière d'organiser des modules connexes dans un répertoire.

#### **Qu'est-ce que sont les Modules et les Paquets?**

- **Modules**: Un module est essentiellement un fichier contenant du code Python. Il peut définir des fonctions, des classes et des variables, et peut également inclure du code exécutable.

  Exemple: `mon_module.py`

- **Paquets**: Un paquet est un moyen d'organiser plusieurs modules en un seul répertoire. Ce répertoire contient un fichier spécial appelé `__init__.py` (qui peut être vide) pour indiquer à Python que le répertoire doit être traité comme un paquet ou un module.

  Structure d'un paquet:
  ```
  mon_paquet/
  ├─ __init__.py
  ├─ module1.py
  └─ module2.py
  ```

#### **Importer des Modules**

- **Importation d'un module**: Pour utiliser un module, vous devez l'importer à l'aide du mot-clé `import`.

```python
import mon_module
```

Après cette importation, vous pouvez accéder aux fonctions ou variables définies dans `mon_module` en utilisant `mon_module.nom_fonction` ou `mon_module.nom_variable`.

- **Alias lors de l'importation**: Vous pouvez donner un alias au module lors de l'importation pour simplifier ou clarifier le code.

```python
import mon_module as mm
```

- **Importer des éléments spécifiques d'un module**: Vous pouvez importer des éléments spécifiques d'un module plutôt que le module entier.

```python
from mon_module import ma_fonction
```

#### **Explorer la Bibliothèque Standard Python**

La bibliothèque standard Python est une vaste collection de modules qui sont inclus avec Python et fournissent des fonctionnalités essentielles, allant de l'accès au système d'exploitation aux outils de programmation web.

Voici quelques modules couramment utilisés:

- **`math`**: Fournit des fonctions mathématiques.

```python
import math
racine_carree = math.sqrt(16)  # 4.0
```

- **`datetime`**: Pour manipuler les dates et les temps.

```python
from datetime import datetime
maintenant = datetime.now()
```

- **`os`**: Fournit des fonctions pour interagir avec le système d'exploitation.

```python
import os
rep_courant = os.getcwd()  # Renvoie le répertoire courant
```

- **`sys`**: Accède à certaines variables utilisées ou maintenues par l'interpréteur et aux fonctions qui interagissent fortement avec l'interpréteur.

```python
import sys
sys.exit()  # Quitte l'interpréteur Python
```

- **`json`**: Pour encoder et décoder le format JSON.

```python
import json
donnees = json.loads('{"nom": "Jean", "age": 30}')
```

C'est une petite fraction de la bibliothèque standard. Elle est vaste et couvre de nombreux domaines, rendant Python puissant et polyvalent dès l'installation.


[🔙 Retour au README principal](./readme.md)