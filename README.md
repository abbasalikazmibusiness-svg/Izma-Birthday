# Izma-Birthday
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Happy 18th IZMA</title>

<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@500;600;700&family=Poppins:wght@300;400;500&display=swap" rel="stylesheet">

<style>
*{margin:0;padding:0;box-sizing:border-box;}
body{
  background:#000;
  font-family:'Poppins',sans-serif;
  color:white;
  overflow-x:hidden;
}

/* ================= PREMIUM LOADER ================= */

.loader{
  position:fixed;
  width:100%;
  height:100vh;
  background:#000;
  display:flex;
  align-items:center;
  justify-content:center;
  flex-direction:column;
  z-index:9999;
  overflow:hidden;
  transition:1.2s ease;
}

.loader.hidden{
  opacity:0;
  pointer-events:none;
}

/* moving light sweep background */
.loader::before{
  content:"";
  position:absolute;
  width:200%;
  height:200%;
  background:radial-gradient(circle at center, rgba(255,105,180,.15), transparent 60%);
  animation:rotateGlow 6s linear infinite;
}

@keyframes rotateGlow{
  from{transform:rotate(0deg);}
  to{transform:rotate(360deg);}
}

/* shimmer particles */
.spark{
  position:absolute;
  width:3px;
  height:3px;
  background:#ff99cc;
  border-radius:50%;
  opacity:.6;
  animation:sparkle 3s infinite ease-in-out;
}

@keyframes sparkle{
  0%,100%{opacity:.2; transform:scale(1);}
  50%{opacity:1; transform:scale(1.8);}
}

/* elegant loading text */
.loader h2{
  font-family:'Playfair Display',serif;
  font-size:26px;
  letter-spacing:3px;
  background:linear-gradient(90deg,#ff4da6,#fff,#ff99cc);
  -webkit-background-clip:text;
  -webkit-text-fill-color:transparent;
  animation:textGlow 2s ease-in-out infinite alternate;
  z-index:2;
}

@keyframes textGlow{
  from{filter:drop-shadow(0 0 10px #ff4da6);}
  to{filter:drop-shadow(0 0 25px #ff99cc);}
}

.loader p{
  margin-top:15px;
  font-size:13px;
  opacity:.6;
  letter-spacing:2px;
  z-index:2;
}

/* ================= REST OF PAGE (UNCHANGED STYLE) ================= */

.hero{
  text-align:center;
  padding:90px 20px 40px;
  opacity:0;
  animation:fadeIn 2s forwards;
  animation-delay:2.8s;
}

@keyframes fadeIn{to{opacity:1;}}

.hero h1{
  font-family:'Playfair Display',serif;
  font-size:10vw;
  background:linear-gradient(120deg,#ff4da6,#fff,#ff99cc);
  -webkit-background-clip:text;
  -webkit-text-fill-color:transparent;
  animation:glow 3s infinite alternate;
}

@keyframes glow{
  from{filter:drop-shadow(0 0 10px #ff4da6);}
  to{filter:drop-shadow(0 0 30px #ff99cc);}
}

.hero h3{margin-top:10px;font-weight:300;opacity:.7;}

.note{
  max-width:750px;
  margin:50px auto;
  padding:40px;
  border-radius:25px;
  background:linear-gradient(145deg,rgba(255,255,255,.12),rgba(255,255,255,.03));
  border:1px solid rgba(255,255,255,.25);
  box-shadow:0 30px 80px rgba(255,0,120,.3);
  backdrop-filter:blur(35px);
  text-align:center;
  line-height:1.8;
  opacity:0;
  animation:fadeIn 2s forwards;
  animation-delay:3.2s;
}

.note h2{
  font-family:'Playfair Display',serif;
  margin-bottom:20px;
  font-size:5vw;
  background:linear-gradient(120deg,#ff4da6,#ffffff,#ff99cc);
  -webkit-background-clip:text;
  -webkit-text-fill-color:transparent;
}

.signature{
  margin-top:35px;
  font-family:'Playfair Display',serif;
  font-style:italic;
  font-size:20px;
  letter-spacing:1px;
  opacity:.9;
  color:#ff99cc;
  text-shadow:0 0 15px rgba(255,105,180,.6);
}

.cards{
  max-width:900px;
  margin:70px auto;
  display:grid;
  grid-template-columns:repeat(auto-fit,minmax(260px,1fr));
  gap:30px;
  padding:0 20px;
  opacity:0;
  animation:fadeIn 2s forwards;
  animation-delay:3.6s;
}

.card{
  background:linear-gradient(145deg,rgba(255,255,255,.08),rgba(255,255,255,.03));
  border:1px solid rgba(255,255,255,.2);
  padding:30px;
  border-radius:20px;
  transition:.5s;
  backdrop-filter:blur(25px);
}

.card:hover{
  transform:translateY(-12px);
  box-shadow:0 25px 70px rgba(255,0,120,.4);
}

.card h4{margin-bottom:12px;color:#ff99cc;font-weight:500;}
.card p{font-size:14px;opacity:.85;}

@media(max-width:768px){
  .hero h1{font-size:14vw;}
  .note h2{font-size:8vw;}
}
</style>
</head>
<body>

<!-- PREMIUM LOADER -->
<div class="loader" id="loader">
  <h2>For Someone Truly Special</h2>
  <p>Please wait...</p>
</div>

<!-- spark particles -->
<script>
for(let i=0;i<25;i++){
  let s=document.createElement("div");
  s.className="spark";
  s.style.left=Math.random()*100+"vw";
  s.style.top=Math.random()*100+"vh";
  s.style.animationDelay=Math.random()*3+"s";
  document.querySelector(".loader").appendChild(s);
}
</script>

<!-- MUSIC -->
<audio autoplay loop>
  <source src="https://www2.cs.uic.edu/~i101/SoundFiles/HappyBirthday.mid" type="audio/midi">
</audio>

<div class="hero">
  <h1>Happy 18th Birthday IZMA 🤍</h1>
  <h3>Welcome to Adulthood</h3>
</div>

<div class="note">
  <h2>A Little Note For You 💗</h2>
  <p>
    Today is not just about turning 18.
    It’s about celebrating the beautiful soul you have become.
    Your kindness, strength, and light make this world brighter.
    <br><br>
    This new chapter will bring dreams, courage,
    and countless opportunities to shine.
    Never forget how deeply you are loved.
    <br><br>
    Happy 18th Birthday. This is just the beginning. 💖
  </p>

  <div class="signature">
    This is from your Abbas Bhayya 🤍
  </div>
</div>

<div class="cards">
  <div class="card"><h4>Your Innocent Little Smile</h4><p>The way your tiny smile could brighten the whole room.</p></div>
  <div class="card"><h4>Our Random Late Night Talks</h4><p>The laughs and secrets we shared.</p></div>
  <div class="card"><h4>Your First Big Dream</h4><p>The moment you started believing in yourself.</p></div>
  <div class="card"><h4>The Strong Version of You</h4><p>You handled life quietly but bravely.</p></div>
  <div class="card"><h4>Your Caring Heart</h4><p>You always care deeply for the people you love.</p></div>
  <div class="card"><h4>The Glow You Carry</h4><p>There’s something special about you that keeps growing.</p></div>
</div>

<script>
window.addEventListener("load",()=>{
  setTimeout(()=>{
    document.getElementById("loader").classList.add("hidden");
  },2500);
});
</script>

</body>
</html>
