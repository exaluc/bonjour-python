---
title: APIs et Web Scraping
---

Dans notre voyage numérique, les API et le Web Scraping sont des outils inestimables pour débloquer des réservoirs d'informations en ligne. Allons plus loin dans notre compréhension avec des exemples avancés et professionnels.

### **1. Qu'est-ce qu'une API?** 🚪

Une API, ou Interface de Programmation d'Application, est comme une fenêtre sur un logiciel, permettant à d'autres logiciels d'y accéder et d'interagir avec lui. Elle définit la manière dont les requêtes sont traitées, les données accessibles, et leur format de sortie.

#### **API NVD (National Vulnerability Database)** 🛡️

NVD fournit une API pour accéder à des informations détaillées sur les CVE (Common Vulnerabilities and Exposures) liées à des failles de sécurité.

1. **Récupérer les détails d'un CVE spécifique**:

   ```python
   import requests

   CVE_ID = "CVE-2021-12345"
   URL_NVD = f"https://services.nvd.nist.gov/rest/json/cve/1.0/{CVE_ID}"

   response = requests.get(URL_NVD)

   if response.status_code == 200:
       cve_data = response.json()['result']['CVE_Items'][0]
       print(f"Détails pour {CVE_ID}: {cve_data['cve']['description']['description_data'][0]['value']}")
   ```

2. **Lister les CVE récents**:

   ```python
   URL_RECENT_CVE = "https://services.nvd.nist.gov/rest/json/cves/1.0?resultsPerPage=5"

   response = requests.get(URL_RECENT_CVE)
   if response.status_code == 200:
       cves = response.json()['result']['CVE_Items']
       for cve in cves:
           print(cve['cve']['CVE_data_meta']['ID'], ":", cve['cve']['description']['description_data'][0]['value'])
   ```

---

### **2. L'Art du Web Scraping** 🎨🕸️

Lorsqu'une API n'est pas disponible, le Web Scraping intervient pour extraire des données depuis une page web.

#### **Scraping avancé avec Beautiful Soup et Selenium** 🤖

Selenium est particulièrement utile pour interagir avec des pages dynamiques qui nécessitent une interaction utilisateur, comme le remplissage d'un formulaire.

**Exemple basique**:

```python
import requests
from bs4 import BeautifulSoup

URL = "https://www.openai.com/research/"
response = requests.get(URL)
soup = BeautifulSoup(response.content, "html.parser")
title = soup.title.text
print(title)
```

```python
from selenium import webdriver
from bs4 import BeautifulSoup

URL_DYNAMIC = "https://www.site-dynamique"
browser = webdriver.Chrome()
browser.get(URL_DYNAMIC)

# Interaction avec la page et extraction des données
element = browser.find_element_by_id("element_id")
element.send_keys("recherche")

# Récupération des données
html = browser.page_source
soup = BeautifulSoup(html, "html.parser")
results = soup.find_all("div", class_="result-class")

for result in results:
    print(result.text)

browser.close()
```

---

### **3. Explorons d'autres APIs professionnelles** 🎲

- **API REST Countries** 🌍: Fournit des informations sur les pays.

    ```python
    import requests

    URL_COUNTRIES = "https://restcountries.com/v3.1/all"
    response = requests.get(URL_COUNTRIES)
    countries = response.json()
    for country in countries[:5]:
        print(country['name']['common'])
    ```

- **API CoinGecko** 📊: Données sur les prix des cryptomonnaies.

    ```python
    import requests

    URL_CRYPTO = "https://api.coingecko.com/api/v3/coins/markets?vs_currency=usd&ids=bitcoin,ethereum&order=market_cap_desc&limit=5&sparkline=false"
    response = requests.get(URL_CRYPTO)
    cryptos = response.json()
    for crypto in cryptos:
        print(f"{crypto['name']} - {crypto['current_price']} USD")
    ```

---

### **Conclusion** 🎓

Avec une gamme d'APIs disponibles et les puissants outils de Web Scraping à notre disposition, l'accès à des informations utiles et pertinentes est plus facile que jamais. Cependant, utilisez ces outils avec prudence, en respectant les conditions d'utilisation et les droits d'accès.