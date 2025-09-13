# zltkjenya.github.io
<!doctype html>
<html lang="en">
<head>
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>Simple HTML Page</title>
<style>
:root{ --bg:#f7fafc; --card:#ffffff; --accent:#2563eb; --muted:#6b7280; }
body{ font-family:Inter, system-ui, -apple-system,Segoe UI, Roboto, "Helvetica Neue", Arial; margin:0; background:var(--bg); color:#111827; }
.container{ max-width:900px; margin:48px auto; padding:24px; }
header{ display:flex; align-items:center; justify-content:space-between; gap:16px; }
h1{ margin:0; font-size:1.5rem; }
nav a{ margin-left:12px; text-decoration:none; color:var(--muted); font-size:0.95rem }
.card{ background:var(--card); border-radius:12px; padding:18px; box-shadow:0 6px 18px rgba(16,24,40,0.06); }
.actions{ margin-top:16px; display:flex; gap:8px }
button{ border:0; padding:10px 14px; border-radius:8px; cursor:pointer; font-weight:600 }
.btn-primary{ background:var(--accent); color:#fff }
.btn-ghost{ background:transparent; color:var(--muted) }
footer{ margin-top:28px; text-align:center; color:var(--muted); font-size:0.9rem }
pre{ background:#0f172a; color:#e6eef8; padding:12px; border-radius:8px; overflow:auto }
</style>
</head>
<body>
<div class="container">
<header>
<h1>My Simple Page</h1>
<nav>
<a href="#">Home</a>
<a href="#about">About</a>
<a href="#contact">Contact</a>
</nav>
</header>

<main style="margin-top:18px">
<section class="card">
<h2 id="welcome">Welcome!</h2>
<p style="color:var(--muted)">This is a minimal HTML page with a bit of styling and a small script. Use it as a starter template.</p>
<div class="actions">
<button class="btn-primary" id="greetBtn">Greet me</button>
<button class="btn-ghost" id="showCode">Show HTML sample</button>
</div>
<div id="output" style="margin-top:14px"></div>
</section>

<section class="card" style="margin-top:18px">
<h3 id="about">About this page</h3>
<p style="color:var(--muted)">Built with semantic HTML, a tiny CSS block, and a few lines of JavaScript that demonstrate interactivity without frameworks.</p>
</section>

<section class="card" style="margin-top:18px">
<h3 id="contact">Contact</h3>
<p style="color:var(--muted)">Want changes? Edit the HTML directly or ask me to customize it for you.</p>
<pre id="codePreview" style="display:none">&lt;!-- example: put your snippet here --&gt;&#10;&lt;p&gt;Hello world&lt;/p&gt;</pre>
</section>
</main>

<footer>
<small>Generated: <span id="now"></span></small>
</footer>
</div>

<script>
document.getElementById('now').textContent = new Date().toLocaleString();
document.getElementById('greetBtn').addEventListener('click', function(){
const out = document.getElementById('output');
out.innerHTML = '<strong>Hello!</strong> Nice to meet you. \n' +
'Try the "Show HTML sample" button to reveal a small snippet.';
});

document.getElementById('showCode').addEventListener('click', function(){
const pre = document.getElementById('codePreview');
pre.style.display = pre.style.display === 'none' ? 'block' : 'none';
});
</script>
</body>
</html>
