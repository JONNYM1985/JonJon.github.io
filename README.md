<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Jon Jon and Friends</title>

<style>

*{
margin:0;
padding:0;
box-sizing:border-box;
font-family:Arial, Helvetica, sans-serif;
}

body{
background:#07030f;
color:white;
overflow-x:hidden;
}

/* animated glow background */

body::before{
content:"";
position:fixed;
width:200%;
height:200%;
background:
radial-gradient(circle at 20% 30%, #6a00ff22, transparent),
radial-gradient(circle at 80% 60%, #ff00ff22, transparent),
radial-gradient(circle at 50% 80%, #3b00ff22, transparent);
animation:bgmove 25s infinite linear;
z-index:-2;
}

@keyframes bgmove{
0%{transform:translate(0,0)}
50%{transform:translate(-20%, -10%)}
100%{transform:translate(0,0)}
}

canvas{
position:fixed;
top:0;
left:0;
z-index:-1;
}

/* header */

header{
text-align:center;
padding:110px 20px 80px;
}

h1{
font-size:4rem;
letter-spacing:3px;
text-shadow:0 0 25px #a855ff;
}

.tagline{
margin-top:15px;
color:#ccc;
font-style:italic;
}

/* container */

.container{
max-width:1000px;
margin:auto;
padding:30px;
}

/* cards */

.card{
background:rgba(255,255,255,0.05);
border:1px solid rgba(255,255,255,0.08);
backdrop-filter:blur(12px);
padding:35px;
border-radius:18px;
margin-bottom:25px;
transition:0.35s;
}

.card:hover{
transform:translateY(-8px);
box-shadow:0 0 25px rgba(160,70,255,0.35);
}

h2{
margin-bottom:15px;
color:#d8b4ff;
}

/* join button */

.join{
display:inline-block;
margin-top:20px;
padding:16px 32px;
font-size:1.1rem;
background:linear-gradient(90deg,#7c3aed,#a855f7);
border-radius:12px;
text-decoration:none;
color:white;
font-weight:bold;
transition:0.3s;
}

.join:hover{
transform:scale(1.1);
box-shadow:0 0 20px #a855ff;
}

/* playlist */

audio{
width:100%;
margin-top:15px;
}

/* footer */

footer{
text-align:center;
padding:40px;
color:#999;
}

</style>
</head>

<body>

<canvas id="stars"></canvas>

<header>

<h1>Jon Jon and Friends</h1>

<p class="tagline">
"Welcome to the party, we don't want it to end."
</p>

</header>

<div class="container">

<div class="card">

<h2>The Community</h2>

<p>
This is a space for the real ones. Inspired by the legends and the music that gets us through it all,
Jon Jon and Friends is a community built for good music, late-night world hopping, and genuine vibes.
</p>

<br>

<p>
Whether you're here to talk about life, blast some music, or explore worlds without drama —
you're home.
</p>

</div>

<div class="card">

<h2>The OVO Connection</h2>

<p>
From late-night vibes to emotional tracks, the playlist never stops.
If you're here for the music, the memories, and the energy — you're in the right place.
</p>

<br>

<p>
"Just hold on, we're going home."
</p>

</div>

<div class="card">

<h2>Group Vitals</h2>

<p><b>The Vibe:</b> 100% Chill & Melodic</p>
<p><b>The Goal:</b> Linking up and making memories</p>
<p><b>The Code:</b> 999 — turning negativity into something positive</p>

</div>

<div class="card">

<h2>Group Playlist</h2>

<audio controls>
<source src="music.mp3" type="audio/mpeg">
</audio>

<p style="color:#aaa;margin-top:10px;">
Add your favorite track to the site to play it here.
</p>

</div>

<div class="card">

<h2>Join Our VRChat Group</h2>

<p>
Click the button below to open the official group page and join the community.
</p>

<a class="join"
href="https://vrchat.com/home/group/grp_e6ecca5a-828b-4706-9c23-db1723469436"
target="_blank">

Join Jon Jon and Friends on VRChat

</a>

</div>

</div>

<footer>

Positive vibes only • Legends never die

</footer>

<script>

/* star animation */

const canvas = document.getElementById("stars")
const ctx = canvas.getContext("2d")

canvas.width = window.innerWidth
canvas.height = window.innerHeight

let stars=[]

for(let i=0;i<220;i++){
stars.push({
x:Math.random()*canvas.width,
y:Math.random()*canvas.height,
size:Math.random()*2,
speed:Math.random()*0.4
})
}

function animate(){

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

requestAnimationFrame(animate)

}

animate()

</script>

</body>
</html>
