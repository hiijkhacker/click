# Q19 & Q25 – Client Information using Flask Headers

**File: `headers.py`**
```python
from flask import Flask, request

app = Flask(__name__)

@app.route("/")
def client_info():
    user_agent = request.headers.get("User-Agent")
    host = request.headers.get("Host")
    accept = request.headers.get("Accept")
    return f"""
    <h2>Client Information</h2>
    <p><b>User-Agent:</b> {user_agent}</p>
    <p><b>Host:</b> {host}</p>
    <p><b>Accept:</b> {accept}</p>
    """

if __name__ == "__main__":
    app.run(debug=True)
```

Install Flask with `python -m pip install flask`, run `python headers.py`, and open `http://127.0.0.1:5000`.
