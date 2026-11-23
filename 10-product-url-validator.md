# Q15 – Product URL Validator

**File: `url.html`**
```html
<!DOCTYPE html>
<html>

<PARSED TEXT FOR PAGE: 15 / 22>
<body>
<h2>Product URL Validator</h2>
<input type="text" id="url" size="50" placeholder="Enter product URL">
<button onclick="validateUrl()">Check</button>
<p id="msg"></p>
<script>
function validateUrl() {
var url = document.getElementById("url").value.trim();
var msg = "";
if (url.indexOf("https://") !== 0) {
msg = "URL must start with https://";
} else if (url.indexOf("www.shopmart.com") === -1) {
msg = "URL must belong to www.shopmart.com";
} else if (/\s/.test(url) || /[<>]/.test(url)) {
msg = "URL contains spaces or invalid characters";
} else if (url.indexOf("/product/") === -1) {
msg = "URL must include a valid product path (/product/)";
} else {
msg = "Valid product URL";
}
document.getElementById("msg").textContent = msg;
}
</script>
</body>
</html>
```

