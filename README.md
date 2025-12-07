# [cite_start]🔎 Web Scraping y Conceptos Básicos de HTML [cite: 19]

[cite_start]Este repositorio contiene material de apoyo y ejemplos sobre la técnica de **Web Scraping** y los **conceptos fundamentales de HTML** necesarios para realizar la extracción de datos de forma automatizada[cite: 19].

[cite_start]El web scraping es una técnica para extraer datos de sitios web de forma automatizada[cite: 1].

---

## 🎯 ¿Qué es Web Scraping?

[cite_start]El Web Scraping es una técnica para extraer datos de sitios web de forma automatizada[cite: 1]. [cite_start]Esto se logra mediante el uso de scripts o herramientas que acceden a páginas web, recuperan su contenido (HTML, JSON, etc.), y lo procesan para obtener información útil[cite: 2].

### [cite_start]⚙️ ¿Cómo Funciona? [cite: 3]

El proceso de Web Scraping se realiza en los siguientes pasos:

1.  [cite_start]**Solicitudes (Requests):** El script envía una solicitud HTTP (GET, POST, etc.) al servidor del sitio web para obtener el contenido de la página[cite: 4].
2.  [cite_start]**Extracción (Parsing):** Se analiza el contenido recibido (generalmente en formato HTML o JSON) para identificar los elementos de interés[cite: 5].
3.  [cite_start]**Procesamiento:** Los datos extraídos se estructuran en el formato deseado (CSV, base de datos, etc.)[cite: 6].

---

## [cite_start]🛠️ Herramientas Comunes [cite: 7]

### [cite_start]🐍 Librerías de Python [cite: 8]

| Librería | Propósito Principal |
| :--- | :--- |
| **Requests** | [cite_start]Para enviar solicitudes HTTP [cite: 12] [cite_start]y descargar el contenido HTML de una página web[cite: 17]. |
| **Beautiful Soup** | [cite_start]Para extraer datos y navegar por estructuras HTML y XML[cite: 9]. [cite_start]Analiza y organiza el HTML para buscar y extraer datos específicos fácilmente[cite: 18]. |
| **Scrapy** | [cite_start]Un framework avanzado para web scraping[cite: 10]. |
| **Selenium** | [cite_start]Para interactuar con páginas web dinámicas[cite: 11]. |

### [cite_start]🖱️ Herramientas No Técnicas [cite: 13]

* [cite_start]Octoparse [cite: 14]
* [cite_start]ParseHub [cite: 15]

---

## 💻 Ejemplo de Código con Beautiful Soup

[cite_start]Este es un ejemplo sencillo que muestra cómo se utilizan las librerías `requests` y `BeautifulSoup` para obtener y analizar una página web[cite: 32]:

```python
from bs4 import BeautifulSoup [cite: 20]
import requests [cite: 21]

# Enviar solicitud a una página web [cite: 22]
url = "[https://almacennaturalmelipal.mitiendanube.com/index.html/](https://almacennaturalmelipal.mitiendanube.com/index.html/)" [cite: 23]
response = requests.get(url) [cite: 24]

# Analizar el contenido HTML [cite: 25]
soup = BeautifulSoup(response.text, 'html.parser') [cite: 26]

# Ejemplo de extracción: iterar sobre todos los títulos h1
# soup es una estructura de datos anidada [cite: 27]
for title in soup.find_all('h1'): [cite: 30]
    print(title.text) [cite: 31]
