<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Jon Jon and Friends</title>

<style>
/* Reset */
* { margin:0; padding:0; box-sizing:border-box; }

/* Body + Background */
body {
  font-family: Arial, sans-serif;
  background: linear-gradient(#0b0018,#1d0038,#050010);
  color: white;
  text-align: center;
  overflow-x: hidden;
}

/* Stars Canvas */
canvas#stars {
  position: fixed;
  top:0;
  left:0;
  width:100%;
  height:100%;
  z-index: -1;
}

/* Big Logo */
.logo {
  font-size: 100px;
  font-weight: 900;
  margin-top: 120px;
  letter-spacing: 5px;
  background: linear-gradient(90deg,#ff7aff,#a855f7,#7c3aed);
  -webkit-background-clip: text;
  color: transparent;
  text-shadow:
    0 0 20px #a855ff,
    0 0 40px #a855ff,
    0 0 80px #7c3aed;
}

/* Tagline */
.tagline {
  margin-top: 10px;
  font-style: italic;
  color: #ccc;
}

/* Join Button */
.join {
  display: inline-block;
  margin-top: 30px;
  padding: 18px 40px;
  font-size: 22px;
  font-weight: bold;
  background: linear-gradient(90deg,#7c3aed,#a855f7);
  border-radius: 12px;
  text-decoration: none;
  color: white;
  transition: 0.3s;
}
.join:hover { box-shadow:0 0 25px #a855ff; }

/* Cards */
.card {
  background: rgba(255,255,255,0.05);
  border-radius: 20px;
  padding: 35px;
  margin: 50px auto;
  width: 80%;
  max-width: 900px;
  backdrop-filter: blur(10px);
}
.card h2 { color:#d8b4ff; margin-bottom:15px; }
iframe { margin-top:20px; border-radius:12px; }

/* Footer */
footer { margin:60px 0; color:#888; }

</style>
</head>

<body>

<canvas id="stars"></canvas>

<!-- Autoplay Music -->
<audio autoplay loop muted id="music">
  <source src="music.mp3" type="audio/mpeg">
</audio>
<script>
window.addEventListener("click", () => {
  document.getElementById("music").muted = false;
});
</script>

<!-- Logo -->
<div class="logo">Jon Jon and Friends</div>
<div class="tagline">"Welcome to the party, we don't want it to end."</div>

<!-- Join VRChat Group -->
<a class="join" href="https://vrchat.com/home/group/grp_e6ecca5a-828b-4706-9c23-db1723469436" target="_blank">JOIN VRCHAT GROUP</a>

<!-- Community Card -->
<div class="card">
  <h2>The Community</h2>
  <p>A place for real ones. Late-night world hopping, good music, and genuine vibes.</p>
  <p>Positive vibes only. Legends never die.</p>
</div>

<!-- Vibe Card -->
<div class="card">
  <h2>The Vibe</h2>
  <p>100% Chill & Melodic</p>
  <p>Making memories together</p>
  <p>999 — turning negativity into something positive</p>
</div>

<!-- Drake Music -->
<div class="card">
  <h2>Drake Vibes</h2>
  <p>Late-night energy and melodic tracks.</p>
  <iframe src="https://open.spotify.com/embed/artist/3TVXtAsR1Inumwj472S9r4" width="100%" height="200" frameborder="0" allow="autoplay; clipboard-write; encrypted-media;"></iframe>
</div>

<!-- Juice WRLD Music -->
<div class="card">
  <h2>Juice WRLD Energy</h2>
  <p>Music that hits the soul.</p>
  <iframe src="https://open.spotify.com/embed/artist/4MCBfE4596Uoi2O4DtmEMz" width="100%" height="200" frameborder="0" allow="autoplay; clipboard-write; encrypted-media;"></iframe>
</div>

<footer>Jon Jon and Friends • VRChat Community</footer>

<script>
/* Stars Animation */
const canvas = document.getElementById("stars");
const ctx = canvas.getContext("2d");
canvas.width = window.innerWidth;
canvas.height = window.innerHeight;
let stars = [];
for(let i=0;i<200;i++){
  stars.push({x:Math.random()*canvas.width, y:Math.random()*canvas.height, size:Math.random()*2, speed:Math.random()*0.3});
}
function drawStars(){
  ctx.clearRect(0,0,canvas.width,canvas.height);
  ctx.fillStyle="white";
  stars.forEach(s=>{
    s.y += s.speed;
    if(s.y > canvas.height) s.y=0;
    ctx.beginPath();
    ctx.arc(s.x,s.y,s.size,0,Math.PI*2);
    ctx.fill();
  });
  requestAnimationFrame(drawStars);
}
drawStars();
</script>

</body>
</html>
