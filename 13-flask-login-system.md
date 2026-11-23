# Q20 – Login System using HTML and Flask

**File: `templates/login.html`**
```html
<!DOCTYPE html>
<html>
<body>
<h2>Login</h2>
<form action="/login" method="POST">
Username: <input type="text" name="username"><br><br>
Password: <input type="password" name="password"><br><br>
<button type="submit">Login</button>
</form>
</body>
</html>
```
**File: `app.py`**
```python
from flask import Flask, request, render_template

app = Flask(__name__)

@app.route("/")
def home():
    return render_template("login.html")

@app.route("/login", methods=["POST"])
def login():
    username = request.form.get("username")
    password = request.form.get("password")

    if username == "admin" and password == "12345":
        return "Login successful!"
    else:
        return "Invalid username or password."

if __name__ == "__main__":
    app.run(debug=True)
```

Install Flask and run `python app.py`. Demo credentials: `admin` / `12345`.
