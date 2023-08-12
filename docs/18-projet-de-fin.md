---
title: Projet de Fin – API pour la Gestion Écologique avec ChatGPT et FastAPI
---

**Objectif**:
Créer une API qui permet aux utilisateurs de poser des questions sur les déchets et le recyclage, et d'obtenir des recommandations basées sur l'IA sur la façon de les traiter de manière écologique.

---

**Étape 1 : Configuration et Installation**

Assurez-vous d'avoir `pip` installé. Ensuite:

1. Installez FastAPI et Uvicorn:
```bash
pip install fastapi uvicorn
```

2. Installez OpenAI Python client:
```bash
pip install openai
```

**Étape 2 : Initialisation de FastAPI**

1. Créez un nouveau fichier `main.py`.
2. Initialisez votre application FastAPI:
```python
from fastapi import FastAPI, HTTPException

app = FastAPI()
```

**Étape 3 : Intégration de ChatGPT**

1. Configurez le client OpenAI avec votre clé API:

```python
import openai

openai.api_key = "YOUR_API_KEY"
```

2. Créez une route FastAPI pour poser des questions à ChatGPT:
```python
from pydantic import BaseModel

class Query(BaseModel):
    question: str

@app.post("/query/")
def get_answer(query: Query):
    try:
        response = openai.Completion.create(
            engine="davinci",
            prompt=query.question,
            max_tokens=150
        )
        return {"response": response.choices[0].text.strip()}
    except Exception as e:
        raise HTTPException(status_code=500, detail="Erreur interne du serveur.")
```

**Étape 4 : Exécuter l'API**

Exécutez votre API avec Uvicorn:
```bash
uvicorn main:app --reload
```

Votre serveur devrait maintenant tourner sur `http://127.0.0.1:8000/`

**Étape 5 : Test de l'API avec `curl`**

1. Ouvrez un terminal et exécutez la commande suivante:

```bash
curl -X 'POST' \
  'http://127.0.0.1:8000/query/' \
  -H 'accept: application/json' \
  -H 'Content-Type: application/json' \
  -d '{
  "question": "Comment puis-je recycler les bouteilles en plastique?"
}'
```

2. Vous devriez recevoir une réponse du serveur semblable à :

```json
{
  "response": "Les bouteilles en plastique peuvent être recyclées en les déposant dans le bac de recyclage approprié. Assurez-vous de les rincer et de retirer les étiquettes. Dans certaines régions, vous pouvez également les ramener en magasin pour obtenir un remboursement. Consultez les directives locales pour plus de détails."
}
```

---

**Clap de fin**:
Vous avez maintenant une API basique qui offre des réponses orientées sur la gestion écologique des déchets. Bien sûr, ce n'est qu'un début. Vous pouvez étendre cette base avec plus de fonctionnalités, comme une authentification, la prise en compte de la localisation de l'utilisateur pour des conseils spécifiques à sa région, etc.