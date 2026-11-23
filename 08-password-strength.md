# Q10 – Password Strength Validator

**File: `password.html`**
```html
<!DOCTYPE html>
<html>
<head>
<style>

<PARSED TEXT FOR PAGE: 12 / 22>
.weak { color: red; font-weight: bold; }
.moderate { color: orange; font-weight: bold; }
.strong { color: green; font-weight: bold; }
</style>
</head>
<body>
<h2>Research Lab Login</h2>
<input type="password" id="pwd" placeholder="Enter password">
<button onclick="checkStrength()">Validate</button>
<p id="result"></p>
<script>
function checkStrength() {
var pwd = document.getElementById("pwd").value;
var hasUpper = /[A-Z]/.test(pwd);
var hasLower = /[a-z]/.test(pwd);
var hasDigit = /[0-9]/.test(pwd);
var hasSpecial = /[^A-Za-z0-9]/.test(pwd);
var longEnough = pwd.length >= 8;
var score = hasUpper + hasLower + hasDigit + hasSpecial + longEnough;
var label, cls;
if (score <= 2) { label = "Weak"; cls = "weak"; }
else if (score <= 4) { label = "Moderate"; cls = "moderate"; }
else { label = "Strong"; cls = "strong"; }
var result = document.getElementById("result");
result.textContent = label;
result.className = cls;
}
</script>
</body>

<PARSED TEXT FOR PAGE: 13 / 22>
</html>
```

