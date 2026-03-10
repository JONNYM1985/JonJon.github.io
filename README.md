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
background:#05010a;
color:white;
overflow-x:hidden;
}

/* animated gradient background */

body::before{
content:"";
position:fixed;
width:200%;
height:200%;
background:radial-gradient(circle at 20% 30%, #6a00ff22, transparent),
radial-gradient(circle at 80% 70%, #ff00ff22, transparent),
radial-gradient(circle at 50% 50%, #0000ff22, transparent);
animation:movebg 20s infinite linear;
z-index:-2;
}

@keyframes movebg{
0%{transform:translate(0,0)}
50%{transform:translate(-20%, -10%)}
100%{transform:translate(0,0)}
}

/* stars */

canvas{
position:fixed;
top:0;
left:0;
z-index:-1;
}

/* header */

header{
text-align:center;
padding:100px 20px;
}

h1{
font-size:4rem;
letter-spacing:2px;
text-shadow:0 0 20px #a855ff;
}

.tagline{
margin-top:15px;
font-style:italic;
color:#cfcfcf;
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
backdrop-filter:blur(12px);
border:1px solid rgba(255,255,255,0.1);
padding:35px;
margin-bottom:25px;
border-radius:18px;
transition:0.4s;
}

.card:hover{
transform:translateY(-8px) scale(1.02);
box-shadow:0 0 30px rgba(170,80,255,0.3);
}

h2{
margin-bottom:15px;
color:#d8b4ff;
}

/* button */

.join{
display:inline-block;
margin-top:20px;
padding:14px 28px;
background:linear-gradient(90deg,#7c3aed,#a855f7);
border-radius:10px;
text-decoration:none;
color:white;
font-weight:bold;
transition:0.3s;
}

.join:hover{
transform:scale(1.1);
box-shadow:0 0 15px #a855ff;
}

/* music */

audio{
margin-top:15px;
width:100%;
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
Inspired by the legends and the music that gets us through it all,
Jon Jon and Friends is a place for late-night world hopping,
good music, and real conversations.
</p>

<br>

<p>
Whether you're exploring worlds, talking about life,
or just vibing, everyone here has a spot in the circle.
</p>

</div>

<div class="card">

<h2>The Vibe</h2>

<p><b>The Vibe:</b> 100% Chill & Melodic</p>
<p><b>The Goal:</b> Linking up and making memories</p>
<p><b>The Code:</b> 999 – turning negativity into something positive</p>

</div>

<div class="card">

<h2>Group Playlist</h2>

<audio controls>
<source src="music.mp3" type="audio/mpeg">
</audio>

<p style="margin-top:10px;color:#aaa;">
Upload your favorite track to play it here.
</p>

</div>

<div class="card">

<h2>Join the Circle</h2>

<p>
Positive vibes only. Legends never die.
</p>

<a class="join" href="#">
Join Us on VRChat
</a>

</div>

</div>

<footer>

Jon Jon and Friends • VRChat Community

</footer>

<script>

/* star background */

const canvas = document.getElementById("stars")
const ctx = canvas.getContext("2d")

canvas.width = window.innerWidth
canvas.height = window.innerHeight

let stars = []

for(let i=0;i<200;i++){
stars.push({
x:Math.random()*canvas.width,
y:Math.random()*canvas.height,
size:Math.random()*2,
speed:Math.random()*0.3
})
}

function animate(){

ctx.clearRect(0,0,canvas.width,canvas.height)

ctx.fillStyle="white"

stars.forEach(s=>{
s.y += s.speed

if(s.y > canvas.height){
s.y = 0
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
