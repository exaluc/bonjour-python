---
title: Développement Web avec Python
---

Découvrir le monde du développement web en Python, c'est comme entrer dans une boutique remplie de différentes étagères, chacune offrant un outil adapté à une tâche spécifique. Plongeons dans ce monde fascinant !

#### **Flask : Le Micro-Framework** 🌱

**Présentation** : Flask est comme un bloc Lego de base sur lequel vous pouvez construire ce que vous voulez. Il offre une simplicité et une flexibilité inégalées pour démarrer rapidement.

**Installation** :
```bash
pip install Flask
```

**Exemple basique** :
```python
from flask import Flask, render_template
app = Flask(__name__)

@app.route('/')
def accueil():
    return "Salut avec Flask!"
```

**Utilisation de templates** : Flask s'intègre facilement avec le moteur de template Jinja2.
Créez un dossier `templates` et ajoutez un fichier `accueil.html` avec le contenu suivant :
```html
<h1>Bienvenue sur mon site Flask</h1>
<p>{{ message }}</p>
```
Puis, modifiez votre route pour renvoyer ce template :
```python
@app.route('/')
def accueil():
    return render_template("accueil.html", message="Salut encore avec Flask!")
```

---

#### **Django : Le Titan** 🏛️

**Présentation** : Imaginez un château avec tout ce dont vous avez besoin à l'intérieur. C'est Django, une forteresse pour votre application web, riche en fonctionnalités.

**Installation** :
```bash
pip install django
```

**Démarrage rapide** :
- Création d'un projet et d'une app :
```bash
django-admin startproject monprojet
cd monprojet
python manage.py startapp monapp
```

**Configuration** :
Pour intégrer `monapp`, ajoutez-le à `INSTALLED_APPS` dans `monprojet/settings.py` :
```python
INSTALLED_APPS = [
    ...
    'monapp',
]
```

**Exemple de modèle** : Dans `monapp/models.py` :
```python
from django.db import models

class Article(models.Model):
    titre = models.CharField(max_length=100)
    contenu = models.TextField()
```

Après avoir défini votre modèle, n'oubliez pas de faire une migration :
```bash
python manage.py makemigrations
python manage.py migrate
```

---

#### **FastAPI : La fusée** 🚀

**Présentation** : Si Flask est un bloc Lego et Django un château, FastAPI est comme une fusée. Il vous emmène là où vous devez aller, et vite !

**Installation** :
```bash
pip install fastapi[all] uvicorn
```

**Documentation automatique** : L'une des meilleures caractéristiques de FastAPI est qu'il génère une documentation interactive (Swagger UI) pour votre API. Une fois votre application lancée, accédez à `http://localhost:8000/docs`.

**Exemple avec Pydantic** :
FastAPI utilise Pydantic pour la validation des données :
```python
from fastapi import FastAPI
from pydantic import BaseModel

app = FastAPI()

class Article(BaseModel):
    titre: str
    contenu: str

@app.post("/articles/")
async def create_article(article: Article):
    return {"titre": article.titre, "contenu": article.contenu}
```

---

**Conclusion** :

En matière de développement web en Python, il existe un framework pour chaque besoin. Flask pour la flexibilité, Django pour sa richesse, et FastAPI pour la rapidité et la modernité. Votre projet déterminera le meilleur choix ! 💼🔧🖥️