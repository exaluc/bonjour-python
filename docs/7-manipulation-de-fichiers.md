### **Manipulation de Fichiers**

En Python, la manipulation de fichiers est facile. Vous pouvez lire et écrire des fichiers texte, des CSV, des JSON et même des XML.

#### **Lire et Écrire des Fichiers**

- **Ouvrir un fichier**: Utilisez la fonction `open()`. Par défaut, le fichier est ouvert en mode lecture ('r').

  ```python
  f = open("mon_fichier.txt", "r")
  ```

- **Lire un fichier**: 

  - `read()`: Pour lire le contenu complet.

  ```python
  contenu = f.read()
  ```

  - `readline()`: Pour lire une ligne.

  ```python
  premiere_ligne = f.readline()
  ```

  - `readlines()`: Pour lire toutes les lignes dans une liste.

  ```python
  toutes_les_lignes = f.readlines()
  ```

- **Écrire dans un fichier**: Ouvrez le fichier en mode écriture ('w'). Attention, cela écrasera le contenu existant.

```python
f = open("mon_fichier.txt", "w")
f.write("Bonjour!")
```

- **Fermer un fichier**: Il est essentiel de fermer un fichier après l'avoir utilisé.

```python
f.close()
```

- **Utiliser `with`**: Cette méthode est préférée car elle ferme automatiquement le fichier une fois le bloc de code sous-jacent exécuté.

```python
with open("mon_fichier.txt", "r") as f:
    contenu = f.read()
```

#### **Gestion des données CSV, JSON et XML**

- **CSV (Comma-Separated Values)**:

  Python a un module intégré `csv` pour gérer les fichiers CSV.

  - Lire un CSV:

    ```python
    import csv
    
    with open('mon_fichier.csv', mode ='r')as file:
        csvFile = csv.reader(file)
        for line in csvFile:
            print(line)
    ```

  - Écrire dans un CSV:

  ```python
  with open('mon_fichier.csv', mode ='w')as file:
      writer = csv.writer(file)
      writer.writerow(["nom", "age"])
      writer.writerow(["Jean", 30])
  ```

- **JSON (JavaScript Object Notation)**:

  Le module `json` permet d'encoder et de décoder des données JSON.

  - Lire un JSON:

  ```python
  import json
  
  with open('mon_fichier.json', 'r') as file:
      donnees = json.load(file)
  ```

  - Écrire dans un JSON:

  ```python
  donnees = {"nom": "Jean", "age": 30}
  
  with open('mon_fichier.json', 'w') as file:
      json.dump(donnees, file)
  ```

- **XML (eXtensible Markup Language)**:

  Le module `xml.etree.ElementTree` est souvent utilisé pour parcourir et modifier des fichiers XML.

  - Lire un XML:

  ```python
  import xml.etree.ElementTree as ET
  
  tree = ET.parse('mon_fichier.xml')
  root = tree.getroot()
  
  for elem in root:
      print(elem.tag, elem.attrib)
  ```

  - Écrire dans un XML est un peu plus complexe. Vous créez des éléments, les ajoutez à l'arbre, puis sauvegardez l'arbre.

 