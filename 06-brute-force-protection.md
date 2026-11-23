# Q6 – Brute-Force Protection using Flask

**File: `app.py`**
```python
from flask import Flask, request
from time import time

app = Flask(__name__)
failed_attempts = {}

MAX_ATTEMPTS = 5
LOCKOUT_SECONDS = 60

@app.route("/login", methods=["POST"])
def login():
    ip = request.remote_addr
    count, last_time = failed_attempts.get(ip, [0, 0])

    if count >= MAX_ATTEMPTS and time() - last_time < LOCKOUT_SECONDS:
        return "Too many failed attempts. Try again later.", 429

    username = request.form.get("username")
    password = request.form.get("password")

    if username == "admin" and password == "12345":
        failed_attempts.pop(ip, None)
        return "Login successful!"
    else:
        failed_attempts[ip] = [count + 1, time()]
        return "Invalid credentials", 401

if __name__ == "__main__":
    app.run(debug=True)
```

Install Flask with `python -m pip install flask`. The in-memory counter is a lab demonstration.
