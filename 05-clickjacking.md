# Q5 & Q11 – Clickjacking Local Demo

**File: `victim.html`**
```html
<!DOCTYPE html>
<html>
<body style="text-align:center; margin-top:100px;">
<button style="padding:15px 30px; font-size:18px;"
onclick="alert('Demo button clicked!')">
Click Demo Button

<PARSED TEXT FOR PAGE: 7 / 22>
</button>
</body>
</html>
```
**File: `clickjack_demo.html`**
```html
<!DOCTYPE html>
<html>
<body>
<h2>Click here to see the demo</h2>
<div style="position:relative; width:250px; height:70px;">
<button style="position:absolute; top:0; left:0; width:250px;
height:70px; font-size:18px;">
CLAIM DEMO
</button>
<iframe src="victim.html"
style="position:absolute; top:-95px; left:-10px; width:250px;
height:160px; opacity:0.0001; z-index:2;">
</iframe>
</div>
</body>
</html>
```

Keep both files in one folder. This is a local demo using a harmless alert button. Example defensive header: `Content-Security-Policy: frame-ancestors 'none';`.
