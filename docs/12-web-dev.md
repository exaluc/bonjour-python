### **Développement Web avec Python**

Le développement web en Python est devenu de plus en plus populaire grâce à une variété de frameworks. Parmi eux, Flask, Django et FastAPI se démarquent par leur popularité et leur utilité. Examinons ces trois frameworks et découvrons comment les installer et les utiliser.

#### **Flask: Le Micro-Framework**

**Présentation**: Flask est un micro-framework léger, simple et extensible. Parfait pour les petites applications ou lorsque vous souhaitez une grande flexibilité.

**Installation**:
```bash
pip install Flask
```

**Exemple basique**:
```python
from flask import Flask
app = Flask(__name__)

@app.route('/')
def accueil():
    return "Salut avec Flask!"
```

**Démarrer l'application**: Exécutez votre script Python.
```bash
python nom_du_script.py
```
Accédez à `http://localhost:5000/` pour voir votre application.

---

#### **Django: Le Framework Haut-Niveau**

**Présentation**: Django est complet et suit le modèle "batteries-included". Il est idéal pour les grands projets ou lorsque vous voulez beaucoup de fonctionnalités intégrées.

**Installation**:
```bash
pip install django
```

**Création d'un nouveau projet**:
```bash
django-admin startproject nomduprojet
```

**Exemple basique**: 

Dans `nomduprojet/views.py`, ajoutez:
```python
from django.http import HttpResponse

def accueil(request):
    return HttpResponse("Salut avec Django!")
```

Ajoutez la route dans `nomduprojet/urls.py`:
```python
from django.urls import path
from . import views

urlpatterns = [
    path('', views.accueil, name='accueil'),
]
```

**Démarrer l'application**: 
```bash
cd nomduprojet
python manage.py runserver
```
Accédez à `http://localhost:8000/`.

---

#### **FastAPI: Le Nouveau Venu**

**Présentation**: FastAPI est moderne et basé sur des types standard, ce qui le rend rapide. Idéal pour des APIs modernes.

**Installation**:
```bash
pip install fastapi[all] uvicorn
```

**Exemple basique**:
```python
from fastapi import FastAPI

app = FastAPI()

@app.get("/")
def lire_racine():
    return {"Salut": "avec FastAPI"}
```

**Démarrer l'application**: 
```bash
uvicorn nom_du_script:app --reload
```
Accédez à `http://localhost:8000/`.

---

**Conclusion**:

Le choix du framework dépend des besoins de votre projet. Flask offre flexibilité, Django fournit une suite d'outils complète, et FastAPI est optimal pour les performances élevées et les APIs modernes.

 