# Q1 & Q13 – HTML Injection Demo

**File: `vulnerable.html`**
```html
<!DOCTYPE html>
<html>
<body>
<h2>Feedback Form (Vulnerable)</h2>
<textarea id="comment" rows="4" cols="40"></textarea><br>
<button onclick="showComment()">Submit</button>
<div id="output"></div>
<script>
function showComment() {
var text = document.getElementById("comment").value;
document.getElementById("output").innerHTML = text;
}
</script>
</body>
</html>
```
**File: `fixed.html`** (the safe version uses `textContent` instead of `innerHTML`)
```html
<!DOCTYPE html>
<html>
<body>
<h2>Feedback Form (Vulnerable)</h2>
<textarea id="comment" rows="4" cols="40"></textarea><br>
<button onclick="showComment()">Submit</button>
<div id="output"></div>
<script>
function showComment() {
var text = document.getElementById("comment").value;
document.getElementById("output").textContent = text;
}
</script>
</body>
</html>
```

Run locally in a browser. In the vulnerable demo, HTML entered in the comment is rendered; the fixed demo displays it as text.
