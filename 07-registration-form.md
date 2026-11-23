# Q9 – Cyber Security Workshop Registration Form

**File: `register.html`**
```html
<!DOCTYPE html>
<html>
<head>
<title>Cyber Security Awareness Registration</title>
<link rel="stylesheet" href="style.css">
</head>
<body>
<form class="reg-form">
<h2>Cyber Security Workshop Registration</h2>
<label>Full Name</label>
<input type="text" name="fullname" required>
<label>Email</label>
<input type="email" name="email" required>
<label>Mobile Number</label>
<input type="tel" name="mobile" pattern="[0-9]{10}" required>
<label>Organization/Department</label>
<input type="text" name="org">
<label>Course/Workshop</label>
<select name="course">
<option>Web Security Basics</option>
<option>Ethical Hacking</option>
<option>Network Security</option>
</select>
<label>Experience Level</label>
<input type="radio" name="exp" value="Beginner"> Beginner
<input type="radio" name="exp" value="Intermediate"> Intermediate
<input type="radio" name="exp" value="Advanced"> Advanced

<PARSED TEXT FOR PAGE: 10 / 22>
<label>Areas of Interest</label>
<input type="checkbox" name="interest" value="Web"> Web Security
<input type="checkbox" name="interest" value="Network"> Network Security
<input type="checkbox" name="interest" value="Cloud"> Cloud Security
<label>Profile Photo</label>
<input type="file" name="photo" accept="image/*">
<label>Comments</label>
<textarea name="comments" rows="4"></textarea>
<div class="btn-row">
<button type="submit">Submit</button>
<button type="reset">Reset</button>
</div>
</form>
</body>
</html>
```
**File: `style.css`**
```css
body {
font-family: 'Segoe UI', sans-serif;
background: #f4f6f8;
}
.reg-form {
max-width: 450px; margin: 40px auto; background: #fff;
padding: 25px 30px; border-radius: 12px;

<PARSED TEXT FOR PAGE: 11 / 22>
box-shadow: 0 4px 15px rgba(0,0,0,0.1);
}
.reg-form h2 { color: #1b263b; text-align: center; }
.reg-form label {
display: block; margin-top: 12px; font-weight: 600; color: #333;
}
.reg-form input, .reg-form select, .reg-form textarea {
width: 100%; padding: 8px; margin-top: 4px;
border: 1px solid #ccc; border-radius: 6px;
box-sizing: border-box;
}
.reg-form input:focus, .reg-form textarea:focus {
border-color: #00b4d8; outline: none;
box-shadow: 0 0 5px rgba(0,180,216,0.4);
}
.btn-row { margin-top: 18px; display: flex; gap: 10px; }
.btn-row button {
flex: 1; padding: 10px; border: none; border-radius: 6px;
cursor: pointer; background: #00b4d8; color: #fff;
}
.btn-row button:hover { background: #0096c7; }
@media (max-width: 500px) {
.reg-form { margin: 20px 10px; padding: 15px; }
}
```

Save both files in the same folder and open `register.html`.
