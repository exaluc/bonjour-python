---
title: Manipulation de Fichiers
---

En Python, travailler avec des fichiers est un jeu d'enfant! Que ce soit des fichiers texte, des CSV, des JSON, ou des XML, Python vous a couvert.

#### **Lire et Écrire des Fichiers** 📄

- **Ouvrir un fichier** 🚪: Utilisez la fonction `open()`. Par défaut, le fichier est ouvert en mode lecture ('r').

  ```python
  f = open("mon_fichier.txt", "r")
  ```

- **Lire un fichier** 📖:

  - `read()`: Pour absorber l'intégralité du fichier.

  ```python
  contenu = f.read()
  print(contenu)
  ```

  - `readline()`: Si vous voulez juste un petit goût, soit une ligne.

  ```python
  premiere_ligne = f.readline()
  print(premiere_ligne)
  ```

  - `readlines()`: Pour dévorer toutes les lignes sous forme de liste.

  ```python
  toutes_les_lignes = f.readlines()
  for ligne in toutes_les_lignes:
      print(ligne)
  ```

- **Écrire dans un fichier** ✍️: Ouvrez le fichier en mode écriture ('w'). Prenez garde, cela pourrait remplacer ce qui existait déjà!

```python
f = open("mon_fichier.txt", "w")
f.write("Bonjour, monde!")
```

- **Fermer un fichier** 🔐: C'est comme éteindre la lumière en quittant une pièce. C'est une bonne pratique!

```python
f.close()
```

- **Utiliser `with`** 🤝: Elle est la meilleure amie des programmeurs. Elle prend soin du fichier et le ferme automatiquement pour vous.

```python
with open("mon_fichier.txt", "r") as f:
    contenu = f.read()
    print(contenu)
```

#### **Jongler avec les données CSV, JSON et XML** 🔄

- **CSV (Comma-Separated Values)** 📋:

  Python possède une boîte à outils intégrée nommée `csv`.

  - Lire un CSV 📜:

    ```python
    import csv
    
    with open('mon_fichier.csv', mode ='r')as fichier:
        lecteur_csv = csv.reader(fichier)
        for ligne in lecteur_csv:
            print(", ".join(ligne))
    ```

  - Écrire dans un CSV 🖊:

    ```python
    donnees = [["nom", "age"], ["Jean", 30], ["Marie", 25]]

    with open('mon_fichier.csv', mode ='w')as fichier:
        ecrivain = csv.writer(fichier)
        ecrivain.writerows(donnees)
    ```

- **JSON (JavaScript Object Notation)** 🧬:

  Avec le module `json`, transformer des objets Python en JSON et vice versa est un jeu d'enfant.

  - Lire un JSON 🧐:

    ```python
    import json
  
    with open('mon_fichier.json', 'r') as fichier:
        donnees = json.load(fichier)
        print(donnees)
    ```

  - Écrire dans un JSON 🎨:

    ```python
    personne = {"nom": "Jean", "age": 30, "ville": "Paris"}
  
    with open('mon_fichier.json', 'w') as fichier:
        json.dump(personne, fichier, indent=4)
    ```

- **XML (eXtensible Markup Language)** 🌐:

  `xml.etree.ElementTree` est comme votre GPS pour naviguer à travers les fichiers XML.

  - Lire un XML 🗺:

    ```python
    import xml.etree.ElementTree as ET
  
    arbre = ET.parse('mon_fichier.xml')
    racine = arbre.getroot()
  
    for elem in racine:
        print(elem.tag, "-", elem.text)
    ```

  - Écrire dans un XML 🏗:

    ```python
    import xml.etree.ElementTree as ET
    
    racine = ET.Element("personnes")
    personne = ET.SubElement(racine, "personne", attrib={"id": "1"})
    ET.SubElement(personne, "nom").text = "Jean"
    ET.SubElement(personne, "age").text = "30"
    
    arbre = ET.ElementTree(racine)
    arbre.write("mon_fichier.xml")
    ```

Voilà une plongée enrichie dans la manipulation de fichiers avec Python!