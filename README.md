# shift-innovatie.github.io
# 4. Maak basis HTML-bestanden
cat > index.html <<'EOF'
<!doctype html>
<html lang="nl">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Shift Innovatie — Home</title>
  <link rel="stylesheet" href="css/style.css">
</head>
<body>
  <header class="site-header">
    <div class="container">
      <h1>Shift Innovatie</h1>
      <nav>
        <a href="index.html">Home</a>
        <a href="about.html">Over</a>
        <a href="blog/">Blog</a>
        <a href="contact.html">Contact</a>
      </nav>
    </div>
  </header>

  <main class="container">
    <section class="hero">
      <h2>Jonge denkers, Slimme oplossing!</h2>
      <p>Wij helpen startups en innovators met strategie, financiering en marktintroductie.</p>
    </section>

    <section class="content">
      <article>
        <h3>Onze diensten</h3>
        <p>— Innovatiestrategie<br>— Subsidies en investeringen<br>— Groei en opschaling</p>
      </article>
    </section>
  </main>

  <footer class="site-footer">
    <div class="container">
      <p>© <span id="jaar"></span> Shift Innovatie</p>
    </div>
  </footer>

  <script>
    document.getElementById('jaar').textContent = new Date().getFullYear();
  </script>
</body>
</html>
EOF

# 5. About-pagina
cat > about.html <<'EOF'
<!doctype html>
<html lang="nl">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Over ons — Shift Innovatie</title>
  <link rel="stylesheet" href="css/style.css">
</head>
<body>
  <header class="site-header">
    <div class="container">
      <h1>Over ons</h1>
      <nav>
        <a href="index.html">Home</a>
        <a href="about.html">Over</a>
        <a href="blog/">Blog</a>
        <a href="contact.html">Contact</a>
      </nav>
    </div>
  </header>

  <main class="container">
    <h2>Over Shift Innovatie</h2>
    <p>Shift Innovatie begeleidt ondernemers bij het realiseren van groei door innovatie, financiering en marktstrategie.</p>
  </main>

  <footer class="site-footer">
    <div class="container"><p>© <span id="jaar"></span> Shift Innovatie</p></div>
  </footer>
  <script>document.getElementById('jaar').textContent = new Date().getFullYear();</script>
</body>
</html>
EOF

# 6. Contact-pagina
cat > contact.html <<'EOF'
<!doctype html>
<html lang="nl">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Contact — Shift Innovatie</title>
  <link rel="stylesheet" href="css/style.css">
</head>
<body>
  <header class="site-header">
    <div class="container">
      <h1>Contact</h1>
      <nav>
        <a href="index.html">Home</a>
        <a href="about.html">Over</a>
        <a href="blog/">Blog</a>
        <a href="contact.html">Contact</a>
      </nav>
    </div>
  </header>

  <main class="container">
    <h2>Neem contact op</h2>
    <p>Mail: <a href="mailto:info@shift-innovatie.nl">info@shift-innovatie.nl</a></p>
    <p>Telefoon: +31 (0)6 123 456 78</p>
  </main>

  <footer class="site-footer">
    <div class="container"><p>© <span id="jaar"></span> Shift Innovatie</p></div>
  </footer>
  <script>document.getElementById('jaar').textContent = new Date().getFullYear();</script>
</body>
</html>
EOF

# 7. Eenvoudige CSS
cat > css/style.css <<'EOF'
:root{ --accent:#0077b6; --bg:#fff; --text:#222 }
body{ font-family:system-ui,-apple-system,Roboto,"Segoe UI",sans-serif; margin:0; color:var(--text); background:var(--bg) }
.container{ max-width:960px; margin:0 auto; padding:1rem }
.site-header{ background:#f8f9fa; border-bottom:1px solid #e0e0e0; }
.site-header h1{ display:inline-block; margin:0 }
.site-header nav{ float:right; }
.site-header nav a{ margin-left:1rem; color:var(--accent); text-decoration:none; }
.site-header nav a:hover{ text-decoration:underline; }
.hero{ padding:2rem 0; }
.site-footer{ background:#f1f1f1; text-align:center; padding:1rem 0; margin-top:2rem; font-size:0.9rem }
EOF

# 8. Eerste blogpagina
mkdir blog
cat > blog/index.html <<'EOF'
<!doctype html>
<html lang="nl">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Blog — Shift Innovatie</title>
  <link rel="stylesheet" href="../css/style.css">
</head>
<body>
  <header class="site-header">
    <div class="container">
      <h1>Blog</h1>
      <nav>
        <a href="../index.html">Home</a>
        <a href="../about.html">Over</a>
        <a href="../blog/">Blog</a>
        <a href="../contact.html">Contact</a>
      </nav>
    </div>
  </header>

  <main class="container">
    <h2>Laatste artikelen</h2>
    <ul>
      <li><a href="eerste-post.html">Onze eerste post</a> — 3 november 2025</li>
    </ul>
  </main>

  <footer class="site-footer">
    <div class="container"><p>© <span id="jaar"></span> Shift Innovatie</p></div>
  </footer>
  <script>document.getElementById('jaar').textContent = new Date().getFullYear();</script>
</body>
</html>
EOF

cat > blog/eerste-post.html <<'EOF'
<!doctype html>
<html lang="nl">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Onze eerste post — Shift Innovatie</title>
  <link rel="stylesheet" href="../css/style.css">
</head>
<body>
  <header class="site-header">
    <div class="container">
      <h1>Onze eerste post</h1>
      <nav>
        <a href="../index.html">Home</a>
        <a href="../about.html">Over</a>
        <a href="../blog/">Blog</a>
        <a href="../contact.html">Contact</a>
      </nav>
    </div>
  </header>

  <main class="container">
    <h2>Welkom op onze blog</h2>
    <p>Dit is een testbericht om te zien hoe onze blogpagina's eruitzien op GitHub Pages.</p>
  </main>

  <footer class="site-footer">
    <div class="container"><p>© <span id="jaar"></span> Shift Innovatie</p></div>
  </footer>
  <script>document.getElementById('jaar').textContent = new Date().getFullYear();</script>
</body>
</html>
EOF

# 9. Voeg bestanden toe, commit en push
git add .
git commit -m "Initial website upload for GitHub Pages"
git branch -M main
git push -u origin main
