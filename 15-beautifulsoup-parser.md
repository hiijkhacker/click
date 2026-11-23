# Q22 – Parse an HTML Page using BeautifulSoup

**File: `q22.py`**
```python
import requests
from bs4 import BeautifulSoup

url = "http://127.0.0.1:5000"
html = requests.get(url).text
soup = BeautifulSoup(html, "html.parser")

print("Title:", soup.title.string if soup.title else "No title")

print("\nHyperlinks:")
for link in soup.find_all("a"):
    print(link.get("href"))

print("\nForms:")
for form in soup.find_all("form"):
    print(form.get("action"), form.get("method"))

print("\nInput fields:")
for inp in soup.find_all("input"):
    print("name:", inp.get("name"), "| type:", inp.get("type"))
```

Install with `python -m pip install requests beautifulsoup4`. Start the Q20 Flask app in another terminal before running this parser.
