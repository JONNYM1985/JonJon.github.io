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
background:#050505;
color:white;
overflow-x:hidden;
}

canvas{
position:fixed;
top:0;
left:0;
z-index:-1;
}

header{
text-align:center;
padding:80px 20px;
}

h1{
font-size:3.5rem;
letter-spacing:2px;
}

.tagline{
color:#bbb;
margin-top:10px;
font-style:italic;
}

.container{
max-width:900px;
margin:auto;
padding:30px;
}

.card{
background:rgba(20,20,20,0.8);
padding:30px;
border-radius:15px;
margin-bottom:25px;
backdrop-filter:blur(10px);
transition:0.3s;
}

.card:hover{
transform:scale(1.03);
}

h2{
margin-bottom:15px;
}

.join-btn{
display:inline-block;
margin-top:15px;
padding:12px 25px;
background:#6a00ff;
border-radius:8px;
text-decoration:none;
color:white;
font-weight:bold;
}

.join-btn:hover{
background:#8a2cff;
}

.music-player{
text-align:center;
}

footer{
text-align:center;
padding:25px;
color:#777;
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
Whether you're here to talk about life, blast music, or explore VRChat without the extra drama,
you're home. Everyone deserves a spot in the circle.
</p>

</div>

<div class="card">

<h2>The Vibe</h2>

<p><b>The Vibe:</b> 100% Chill & Melodic</p>
<p><b>The Goal:</b> Linking up and making memories</p>
<p><b>The Code:</b> 999 — turning negativity into something positive</p>

</div>

<div class="card music-player">

<h2>Group Playlist</h2>

<audio controls>
<source src="music.mp3" type="audio/mpeg">
</audio>

<p style="margin-top:10px;color:#aaa;">
Upload your favorite track to the site to play it here.
</p>

</div>

<div class="card">

<h2>Join the Crew</h2>

<p>
Positive vibes only. Legends never die.
</p>

<br>

<a class="join-btn" href="#">
Join Us on VRChat
</a>

</div>

</div>

<footer>

Jon Jon and Friends • VRChat Community

</footer>

<script>

const canvas=document.getElementById("stars")
const ctx=canvas.getContext("2d")

canvas.width=window.innerWidth
canvas.height=window.innerHeight

let stars=[]

for(let i=0;i<200;i++){

stars.push({
x:Math.random()*canvas.width,
y:Math.random()*canvas.height,
size:Math.random()*2
})

}

function draw(){

ctx.clearRect(0,0,canvas.width,canvas.height)

ctx.fillStyle="white"

stars.forEach(s=>{

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
