# Q21 – Cookies using Flask

**File: `cookies.py`**
```python
from flask import Flask, request, make_response

app = Flask(__name__)

@app.route("/set")
def set_cookie():
    resp = make_response("Cookie set!")
    resp.set_cookie("username", "student123")
    return resp

@app.route("/get")
def get_cookie():
    username = request.cookies.get("username")
    return f"Stored username: {username}"

if __name__ == "__main__":
    app.run(debug=True)
```

Install Flask, run `python cookies.py`, open `/set` first and then `/get` at `http://127.0.0.1:5000`.
