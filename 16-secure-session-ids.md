# Q23 – Secure Session IDs using Python secrets

**File: `q23.py`**
```python
import secrets

for i in range(5):
    session_id = secrets.token_hex(16)
    print(f"Session ID {i+1}: {session_id}")
```

Run `python q23.py`. Five random session IDs are printed.
