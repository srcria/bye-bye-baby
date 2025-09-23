<!doctype html>
<html lang="pt-BR">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Bye Bye Baby — Preservativos</title>
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700&display=swap" rel="stylesheet">
<style>
:root{
  --bg:#0b0b0b;
  --panel:#0f0f12;
  --accent:#8a2be2;
  --accent-2:#5d28a6;
  --muted:#bdbdbd;
  --radius:14px;
}
*{box-sizing:border-box;}
html {scroll-behavior: smooth;}
body{margin:0;background:linear-gradient(180deg,var(--bg),#060606);color:#fff;font-family:'Inter',sans-serif;}
header{display:flex;align-items:center;justify-content:space-between;padding:18px 28px;position:sticky;top:0;backdrop-filter:blur(6px);z-index:20;background:transparent;}
.brand{display:flex;gap:12px;align-items:center;}
.logo img{width:48px;height:48px;border-radius:12px;object-fit:cover;}
nav a{color:var(--muted);text-decoration:none;margin-left:18px;font-weight:600;cursor:pointer;}
.carrinho{position:relative;cursor:pointer;font-size:24px;}
.carrinho span{position:absolute;top:-6px;right:-10px;background:var(--accent);color:#fff;border-radius:50%;padding:2px 6px;font-size:12px;}
.hero{padding:64px 28px;display:grid;grid-template-columns:1fr 380px;gap:28px;max-width:1200px;margin:0 auto;}
.card{background:linear-gradient(180deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01));border-radius:var(--radius);padding:28px;transition:all 0.3s ease;}
h1{font-size:34px;margin:0 0 12px;}
p.lead{color:var(--muted);margin:0 0 18px;}
.cta{display:flex;gap:12px;margin-top:18px;}
.btn{padding:12px 18px;border-radius:12px;border:0;font-weight:700;cursor:pointer;transition:0.2s;}
.btn:hover{opacity:0.85;}
.btn-primary{background:linear-gradient(90deg,var(--accent),var(--accent-2));color:#fff;}
.btn-ghost{background:transparent;border:1px solid rgba(255,255,255,0.06);color:var(--muted);}
.product-list{display:grid;grid-template-columns:repeat(auto-fill,minmax(220px,1fr));gap:18px;margin-top:16px;}
.product{background:linear-gradient(180deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01));padding:16px;border-radius:12px;}
.product .thumb{height:140px;border-radius:10px;background:linear-gradient(135deg,var(--accent),#1a1a1a);display:flex;align-items:center;justify-content:center;font-weight:700;}
.sabores-section{max-width:1100px;margin:34px auto;padding:0 18px;}
.sabores-card{background:var(--panel);border-radius:12px;padding:16px;margin-bottom:16px;transition:0.3s;cursor:pointer;display:flex;align-items:center;}
.sabores-card:hover{transform:scale(1.05);}
.sabores-card img{
  width:60px;
  height:60px;
  border-radius:8px;
  margin-right:10px;
  vertical-align:middle;
  object-fit:cover;
}
.shake{animation:shake 0.3s;}
@keyframes shake{
  0% {transform:translateX(0);}
  25% {transform:translateX(-5px);}
  50% {transform:translateX(5px);}
  75% {transform:translateX(-5px);}
  100% {transform:translateX(0);}
}
#carrinho-aba{position:fixed;top:64px;right:-320px;width:300px;height:80%;background:var(--panel);border-left:2px solid var(--accent);padding:16px;overflow-y:auto;transition:0.3s;z-index:25;}
#carrinho-aba.show{right:0;}
.carrinho-item{display:flex;justify-content:space-between;align-items:center;margin-bottom:12px;background:linear-gradient(180deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01));padding:10px;border-radius:10px;}
.carrinho-item span{margin:0 4px;}
.carrinho-item button{padding:4px 8px;border-radius:6px;border:none;background:var(--accent-2);color:#fff;cursor:pointer;}
footer{padding:28px;text-align:center;color:var(--muted);margin-top:36px;}
@media(max-width:880px){.hero{grid-template-columns:1fr;}nav a{margin-left:10px;font-size:14px}}
</style>
</head>
<body>

<header>
  <div class="brand">
    <div class="logo">
      <img src="c:\sites\logo.png.png" alt="Logo Bye Bye Baby">
    </div>
    <div>
      <div style="font-weight:700">Bye Bye Baby</div>
      <div style="font-size:12px;color:var(--muted);margin-top:2px">
        Preservativos — proteção e estilo
      </div>
    </div>
  </div>
  <nav>
    <a href="#produtos">Produtos</a>
    <a href="#sabores" onclick="shakeSabores()">Sabores</a>
    <a href="#sobre">Sobre</a>
    <a href="#contato">Contato</a>
  </nav>
  <div class="carrinho" onclick="toggleCarrinho()">
    🛒 <span id="totalCarrinho">0</span>
  </div>
</header>

<div id="carrinho-aba"></div>

<main>
<section class="hero">
  <div class="card">
    <h1><br>Bem-vindos à Bye Bye Baby</h1>
    <p class="lead">Proteção com atitude — design moderno, materiais de qualidade e variedade para todos os momentos.</p>
    <div class="cta">
      <button class="btn btn-primary" onclick="scrollSabores()">Confira os sabores</button>
      <button class="btn btn-ghost" onclick="scrollContato()">Fale com a equipe</button>
    </div>
  </div>
</section>

<!-- Produtos -->
<section id="produtos" class="hero">
  <aside class="card">
    <div class="product-list">
      <article class="product"><div class="thumb">Premium</div><h3>Bye Bye Baby — Premium</h3><p style="color:var(--muted)">Maior conforto, lubrificação premium.</p></article>
      <article class="product"><div class="thumb">Clássico</div><h3>Bye Bye Baby — Clássico</h3><p style="color:var(--muted)">Qualidade padrão.</p></article>
      <article class="product"><div class="thumb">Ultra</div><h3>Bye Bye Baby — Ultra-fino</h3><p style="color:var(--muted)">Sensação natural.</p></article>
    </div>
  </aside>
</section>

<!-- Sabores -->
<section id="sabores" class="sabores-section">
  <h2>Premium</h2>
  <div class="sabores-card" onclick="addCarrinho('Premium','Frutas Vermelhas & Champanhe')"><img src="c:\sites\embalagem.png.png" alt="Frutas Vermelhas & Champanhe"> Frutas Vermelhas & Champanhe</div>
  <div class="sabores-card" onclick="addCarrinho('Premium','Café Gourmet')"><img src="c:\sites\embalagem.png.png" alt="Café Gourmet"> Café Gourmet</div>
  <div class="sabores-card" onclick="addCarrinho('Premium','Maracujá & Pimenta Rosa')"><img src="c:\sites\embalagem.png.png" alt="Maracujá & Pimenta Rosa"> Maracujá & Pimenta Rosa (um toque picante e refinado)</div>

  <h2>Clássico</h2>
  <div class="sabores-card" onclick="addCarrinho('Clássico','Natural')"><img src="c:\sites\embalagem.png.png" alt="Natural"> Natural (sem sabor)</div>
  <div class="sabores-card" onclick="addCarrinho('Clássico','Morango')"><img src="c:\sites\embalagem.png.png" alt="Morango"> Morango</div>
  <div class="sabores-card" onclick="addCarrinho('Clássico','Chocolate ao Leite')"><img src="c:\sites\ChatGPT Image 23 de set. de 2025, 15_33_17.png" alt="Chocolate ao Leite"> Chocolate ao Leite (parceria garoto)</div>
  <div class="sabores-card" onclick="addCarrinho('Clássico','Chocolate meio amargo')"><img src="c:\sites\ChatGPT Image 23 de set. de 2025, 15_33_17.png" alt="Chocolate meio amargo"> Chocolate meio amargo (parceria garoto)</div>

  <h2>Ultra-fino</h2>
  <div class="sabores-card" onclick="addCarrinho('Ultra-fino','Jasmim')"><img src="c:\sites\embalagem.png.png" alt="Jasmim"> Jasmim (floral leve)</div>
  <div class="sabores-card" onclick="addCarrinho('Ultra-fino','Limão Siciliano')"><img src="c:\sites\embalagem.png.png" alt="Limão Siciliano"> Limão Siciliano</div>
  <div class="sabores-card" onclick="addCarrinho('Ultra-fino','Melancia Refrescante')"><img src="c:\sites\embalagem.png.png" alt="Melancia Refrescante"> Melancia Refrescante</div>
</section>


<!-- Sobre -->
<section id="sobre" style="max-width:1100px;margin:34px auto;padding:0 18px">
  <div class="card">
    <h2 style="margin-top:0">Sobre a Bye Bye Baby</h2>
    <p style="color:var(--muted);margin-top:6px">Somos um time jovem que acredita que proteção não precisa ser sem graça. Criamos embalagens modernas e campanhas descontraídas, com foco na segurança e respeito ao usuário.</p>
  </div>
</section>

<!-- Contato -->
<section id="contato" style="max-width:1100px;margin:24px auto;padding:0 18px">
  <div class="card">
    <h2 style="margin-top:0">Fale com a equipe</h2>
    <p style="color:var(--muted);margin-top:6px">Quer trocar ideias, pedir amostras ou colaborar? Manda um salve pra gente!</p>
    <form style="display:flex;flex-direction:column;gap:10px;margin-top:12px">
      <input placeholder="Nome" style="padding:10px;border-radius:10px;border:1px solid rgba(255,255,255,0.04);background:transparent;color:#fff">
      <input placeholder="E-mail" style="padding:10px;border-radius:10px;border:1px solid rgba(255,255,255,0.04);background:transparent;color:#fff">
      <textarea placeholder="Mensagem" rows="4" style="padding:10px;border-radius:10px;border:1px solid rgba(255,255,255,0.04);background:transparent;color:#fff"></textarea>
      <div style="display:flex;gap:8px">
        <button class="btn btn-primary" type="button">Enviar</button>
        <button class="btn btn-ghost" type="reset">Limpar</button>
      </div>
    </form>
  </div>
</section>

<footer>
  <div style="max-width:1100px;margin:0 auto;padding:0 18px">
    <div style="display:flex;justify-content:space-between;flex-wrap:wrap;gap:12px;align-items:center">
      <div>© Bye Bye Baby — 2025</div>
      <div style="color:var(--muted);font-size:13px">Feito por amigos. Use com responsabilidade.</div>
    </div>
  </div>
</footer>

<script>
let carrinho = {};
function addCarrinho(tipo, nome){
  const key = tipo + ' - ' + nome;
  if(carrinho[key]) carrinho[key]++;
  else carrinho[key]=1;
  updateCarrinho();
}

function updateCarrinho(){
  const aba = document.getElementById('carrinho-aba');
  aba.innerHTML = '';
  let total=0;
  for(const item in carrinho){
    total += carrinho[item];
    const div = document.createElement('div');
    div.className='carrinho-item';
    div.innerHTML=`<span>${item}</span>
      <div>
        <button onclick="menos('${item}')">-</button>
        <span>${carrinho[item]}</span>
        <button onclick="mais('${item}')">+</button>
      </div>`;
    aba.appendChild(div);
  }
  document.getElementById('totalCarrinho').textContent=total;
}

function mais(item){carrinho[item]++;updateCarrinho();}
function menos(item){carrinho[item]--; if(carrinho[item]<=0) delete carrinho[item]; updateCarrinho();}

function toggleCarrinho(){
  document.getElementById('carrinho-aba').classList.toggle('show');
}

function scrollSabores(){
  const section = document.getElementById('sabores');
  section.scrollIntoView({behavior:'smooth'});
  shakeSabores();
}

function scrollContato(){
  const section = document.getElementById('contato');
  section.scrollIntoView({behavior:'smooth'});
}

function shakeSabores(){
  const section = document.getElementById('sabores');
  section.classList.add('shake');
  setTimeout(()=>{section.classList.remove('shake');},300);
}
</script>

</body>
</html>
