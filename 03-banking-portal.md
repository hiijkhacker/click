# Q3 – Online Banking Portal (JavaScript)

**File: `banking.html`**
```html
<!DOCTYPE html>
<html>
<head><title>Online Banking Portal</title></head>
<body onload="showSecurityAlert()">
<h2 id="welcome"></h2>
<p id="details"></p>
<script>
var customerName = "Rahul Sharma";
var accountType = "Savings";
var accountBalance = 54230.75;
document.getElementById("welcome").textContent =
"Welcome to Online Banking, " + customerName + "!";
document.getElementById("details").innerHTML =
"Account Type: " + accountType + "<br>Balance: Rs. " + accountBalance;
function showSecurityAlert() {
alert("Never share your OTP or PIN with anyone.");
}
</script>
</body>
</html>
```

