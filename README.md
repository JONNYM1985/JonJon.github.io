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
overflow-x:hidden;

/* CITY NIGHT BACKGROUND */

background-image:
linear-gradient(rgba(5,0,16,0.7),rgba(5,0,16,0.9)),
url("https://images.unsplash.com/photo-1477959858617-67f85cf4f1df");

background-size:cover;
background-attachment:fixed;
background-position:center;

}

/* star canvas */

canvas{
position:fixed;
top:0;
left:0;
z-index:-1;
}

/* logo */

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

.tagline{
margin-top:10px;
color:#ddd;
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

background:rgba(0,0,0,0.55);
border-radius:20px;
padding:40px;
margin:70px auto;
width:85%;
max-width:1000px;

backdrop-filter:blur(10px);

}

/* artist images */

.artist{

display:flex;
flex-wrap:wrap;
justify-content:center;
gap:30px;
margin-top:25px;

}

.artist img{

width:220px;
border-radius:15px;

box-shadow:0 0 20px rgba(168,85,247,0.6);

}

iframe{
margin-top:20px;
border-radius:12px;
}

footer{
margin:80px 0;
color:#aaa;
}

/* palm decoration */

.palms{

position:fixed;
bottom:0;
width:100%;
pointer-events:none;

}

.palms img{

width:100%;
opacity:.35;

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
window.addEventListener("click",function(){
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

<!-- ARTISTS -->

<div class="card">

<h2>Community Vibes</h2>

<div class="artist">

<img src="https://upload.wikimedia.org/wikipedia/commons/3/3e/Juice_WRLD_2018.png">

<img src="https://upload.wikimedia.org/wikipedia/commons/9/90/Drake_2016.png">

</div>

</div>

<!-- MUSIC -->

<div class="card">

<h2>Drake Vibes</h2>

<iframe
src="https://open.spotify.com/embed/artist/3TVXtAsR1Inumwj472S9r4"
width="100%" height="200"
allow="autoplay; clipboard-write; encrypted-media;">
</iframe>

</div>

<div class="card">

<h2>Juice WRLD Energy</h2>

<iframe
src="https://open.spotify.com/embed/artist/4MCBfE4596Uoi2O4DtmEMz"
width="100%" height="200"
allow="autoplay; clipboard-write; encrypted-media;">
</iframe>

</div>

<footer>

Positive vibes only • Legends never die

</footer>

<!-- PALM TREE OVERLAY -->

<div class="palms">

<img src="https://i.imgur.com/3ZQ3Z6K.png">

</div>

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
