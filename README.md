<!DOCTYPE html>
<html>
<head>

<title>Jon Jon and Friends</title>

<style>

body{
margin:0;
font-family:Arial;
color:white;
text-align:center;
background:linear-gradient(#0a0018,#1b0033,#050010);
overflow-x:hidden;
}

/* galaxy background */

canvas{
position:fixed;
top:0;
left:0;
z-index:-1;
}

/* neon logo */

.logo{

font-size:110px;
font-weight:900;
margin-top:120px;

background:linear-gradient(90deg,#ff7aff,#a855f7,#7c3aed);
-webkit-background-clip:text;
color:transparent;

text-shadow:
0 0 20px #a855ff,
0 0 40px #a855ff,
0 0 90px #7c3aed;

}

/* tagline */

.tagline{
margin-top:15px;
color:#ccc;
font-style:italic;
}

/* join button */

.join{

display:inline-block;
margin-top:30px;
padding:18px 40px;

font-size:22px;
font-weight:bold;

background:linear-gradient(90deg,#7c3aed,#a855f7);
border-radius:12px;

text-decoration:none;
color:white;

}

.join:hover{
box-shadow:0 0 25px #a855ff;
}

/* sections */

.card{

background:rgba(255,255,255,0.05);
border-radius:20px;
padding:35px;
margin:60px auto;
width:80%;
max-width:1000px;

backdrop-filter:blur(10px);

}

/* members */

.members{
display:flex;
justify-content:center;
gap:20px;
flex-wrap:wrap;
}

.member{

background:rgba(255,255,255,0.07);
padding:20px;
border-radius:15px;
width:180px;

}

/* gallery */

.gallery{
display:grid;
grid-template-columns:repeat(auto-fit,minmax(200px,1fr));
gap:15px;
margin-top:20px;
}

.gallery img{
width:100%;
border-radius:10px;
}

iframe{
margin-top:20px;
border-radius:12px;
}

footer{
margin:80px 0;
color:#888;
}

</style>

</head>

<body>

<canvas id="stars"></canvas>

<!-- AUTOPLAY MUSIC -->

<audio autoplay loop muted id="music">
<source src="music.mp3" type="audio/mpeg">
</audio>

<script>
window.addEventListener("click", function(){
document.getElementById("music").muted=false;
});
</script>

<!-- LOGO -->

<div class="logo">
Jon Jon and Friends
</div>

<div class="tagline">
"Welcome to the party, we don't want it to end."
</div>

<!-- JOIN GROUP BUTTON -->

<a class="join"
href="https://vrchat.com/home/group/grp_e6ecca5a-828b-4706-9c23-db1723469436"
target="_blank">

JOIN THE VRCHAT GROUP

</a>

<!-- COMMUNITY -->

<div class="card">

<h2>The Community</h2>

<p>
Late night world hopping. Good music. Real conversations.
Jon Jon and Friends is a place for the real ones.
</p>

</div>

<!-- MEMBERS -->

<div class="card">

<h2>Members</h2>

<div class="members">

<div class="member">
<h3>Jon Jon</h3>
<p>Founder</p>
</div>

<div class="member">
<h3>Friends</h3>
<p>Community</p>
</div>

<div class="member">
<h3>Legends</h3>
<p>Active Members</p>
</div>

</div>

</div>

<!-- DRAKE MUSIC -->

<div class="card">

<h2>Drake Vibes</h2>

<iframe
src="https://open.spotify.com/embed/artist/3TVXtAsR1Inumwj472S9r4"
width="100%" height="200"
allow="autoplay; clipboard-write; encrypted-media;">
</iframe>

</div>

<!-- JUICE WRLD MUSIC -->

<div class="card">

<h2>Juice WRLD Energy</h2>

<iframe
src="https://open.spotify.com/embed/artist/4MCBfE4596Uoi2O4DtmEMz"
width="100%" height="200"
allow="autoplay; clipboard-write; encrypted-media;">
</iframe>

</div>

<!-- GALLERY -->

<div class="card">

<h2>VRChat Gallery</h2>

<div class="gallery">

<img src="https://images.unsplash.com/photo-1542751371-adc38448a05e">
<img src="https://images.unsplash.com/photo-1511512578047-dfb367046420">
<img src="https://images.unsplash.com/photo-1493711662062-fa541adb3fc8">
<img src="https://images.unsplash.com/photo-1550745165-9bc0b252726f">

</div>

</div>

<footer>

Positive vibes only • Legends never die

</footer>

<script>

/* galaxy stars */

const canvas = document.getElementById("stars")
const ctx = canvas.getContext("2d")

canvas.width = window.innerWidth
canvas.height = window.innerHeight

let stars=[]

for(let i=0;i<300;i++){

stars.push({

x:Math.random()*canvas.width,
y:Math.random()*canvas.height,
size:Math.random()*2,
speed:Math.random()*0.4

})

}

function draw(){

ctx.clearRect(0,0,canvas.width,canvas.height)

ctx.fillStyle="white"

stars.forEach(s=>{

s.y+=s.speed

if(s.y>canvas.height){
s.y=0
}

ctx.beginPath()
ctx.arc(s.x,s.y,s.size,0,Math.PI*2)
ctx.fill()

})

requestAnimationFrame(draw)

}

draw()

</script>

</body>
</html>
