
<html lang="hu">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>MidnightSMP</title>
<style>
*{box-sizing:border-box;margin:0;padding:0}
body{font-family:Inter,Arial,sans-serif;background:linear-gradient(180deg,#050b2e,#020617);color:white;overflow-x:hidden;}
nav{display:flex;justify-content:space-between;align-items:center;padding:20px 50px;background:rgba(5,11,46,.85);backdrop-filter:blur(10px)}
nav a{color:#cfe7ff;text-decoration:none;margin-left:24px;font-weight:600;cursor:pointer;transition:.3s}
nav a:hover{color:#fff;text-shadow:0 0 12px #3b82f6}
.btn{padding:14px 28px;border-radius:16px;background:#2563eb;color:white;font-weight:700;text-decoration:none;box-shadow:0 0 25px rgba(37,99,235,.8);transition:.3s}
.btn:hover{box-shadow:0 0 45px rgba(37,99,235,1)}
section{display:block;opacity:0;position:absolute;top:80px;left:0;width:100%;padding:60px 20px;text-align:center;pointer-events:none;transition:opacity .5s ease, transform .5s ease}
section.active{opacity:1;transform:translateY(0);pointer-events:auto;position:relative;}
h1{margin-bottom:10px;font-size:2.8rem}
h2{margin:30px 0 15px}
p{opacity:.85;margin-bottom:20px}
.status{margin-top:10px;opacity:.85}
.grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(220px,1fr));gap:30px;max-width:1000px;margin:30px auto}
.card{background:rgba(255,255,255,.06);padding:25px;border-radius:22px;text-align:center;box-shadow:0 0 25px rgba(59,130,246,.35);transition:.3s}
.card:hover{transform:translateY(-5px);box-shadow:0 0 45px rgba(59,130,246,.8)}
.icon{font-size:70px;margin-bottom:10px}
.member img{width:90px;border-radius:16px;box-shadow:0 0 20px #2563eb}
footer{text-align:center;padding:40px;opacity:.6}
@media(max-width:800px){nav{flex-direction:column;gap:10px} .grid{grid-template-columns:repeat(auto-fit,minmax(180px,1fr))}}
</style>
</head>
<body>

<nav>
<b>🌙 MidnightSMP</b>
<div>
<a onclick="show('home')">Főoldal</a>
<a onclick="show('videos')">Videók</a>
<a onclick="show('members')">Tagok</a>
<a class="btn" href="https://www.youtube.com/@midnightsmpgang">Csatornánk</a>
<a class="btn" href="https://dsc.gg/midnightsmp">Csatlakozás</a>
</div>
</nav>

<section id="home" class="active">
<h1>🌙 MidnightSMP</h1>
<h2>MidnightSMP — hivatalos oldal</h2>
<p>Csatlakozz az élményhez: építés, kaland és kreativitás egy modern, barátságos Minecraft SMP szerveren.</p>
<a class="btn" onclick="show('videos')">Videók megtekintése</a>
<a class="btn" onclick="show('members')" style="margin-left:15px;">Tagok megismerése</a>
<div class="status">🟢 Szerver státusz: <b>Online</b></div>
<h2>Kiemelt videó</h2>
<div class="grid">
  <div class="card"><div class="icon">❔</div><p>YouTube klipek és stream részletek</p></div>
</div>
<h2>Legújabb videók</h2>
<div class="grid">
  <div class="card"><div class="icon">❔</div><b>MidnightSMP – Nyitás</b><p>hamarosan</p></div>
  <div class="card"><div class="icon">❔</div><b>MidnightSMP – PvP</b><p>hamarosan</p></div>
  <div class="card"><div class="icon">❔</div><b>MidnightSMP – Káosz</b><p>hamarosan</p></div>
</div>
<h2>Csapatunk</h2>
<div class="grid">
  <div class="card member"><img src="https://mc-heads.net/avatar/Beniwadraxx/100"><b>Beniwadraxx</b><br><small>Tulaj</small></div>
  <div class="card member"><img src="https://mc-heads.net/avatar/Cigulass/100"><b>Cigulass</b><br><small>Tulaj</small></div>
  <div class="card member"><img src="https://mc-heads.net/avatar/BatyiTeam/100"><b>BatyiTeam</b><br><small>Szerver alapító</small></div>
</div>
</section>

<section id="videos">
<h1>Videók</h1>
<p>Legfrissebb streamek és klipek</p>
<div class="grid">
  <div class="card"><div class="icon">❔</div><b>MidnightSMP – Nyitás</b><p>hamarosan</p></div>
  <div class="card"><div class="icon">❔</div><b>MidnightSMP – PvP</b><p>hamarosan</p></div>
  <div class="card"><div class="icon">❔</div><b>MidnightSMP – Káosz</b><p>hamarosan</p></div>
</div>
</section>

<section id="members">
<h1>Tagok</h1>
<p>Ismerd meg a csapatot</p>
<div class="grid">
  <div class="card member"><img src="https://mc-heads.net/avatar/Beniwadraxx/100"><b>Beniwadraxx</b></div>
  <div class="card member"><img src="https://mc-heads.net/avatar/Cigulass/100"><b>Cigulass</b></div>
  <div class="card member"><img src="https://mc-heads.net/avatar/BatyiTeam/100"><b>BatyiTeam</b></div>
</div>
</section>

<footer>
© 2025 MidnightSMP<br>
Created By: Beniwadraxx
</footer>

<script>
let currentSection = 'home';
function show(id){
  if(currentSection===id) return;
  const prev = document.getElementById(currentSection);
  const next = document.getElementById(id);
  prev.style.opacity = 0;
  prev.style.transform = 'translateY(20px)';
  setTimeout(()=>{
    prev.classList.remove('active');
    prev.style.transform='translateY(0)';
    next.classList.add('active');
    next.style.opacity = 0;
    next.style.transform = 'translateY(20px)';
    setTimeout(()=>{
      next.style.opacity=1;
      next.style.transform='translateY(0)';
    },50);
  },500);
  currentSection = id;
  window.scrollTo(0,0);
}
</script>

</body>
</html>
