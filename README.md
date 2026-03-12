<!DOCTYPE html>

<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width,initial-scale=1.0">
<title>Jon Jon and Friends</title>

<style>

body{
margin:0;
font-family:Arial, Helvetica, sans-serif;
background:#050010;
color:white;
text-align:center;
overflow-x:hidden;
}

/* STAR SKY */

canvas{
position:fixed;
top:0;
left:0;
z-index:-1;
}

/* PALM TREES */

.palm-left,.palm-right{
position:fixed;
bottom:0;
width:260px;
opacity:.35;
pointer-events:none;
}

.palm-left{left:0;}
.palm-right{right:0;transform:scaleX(-1);}

/* LOGO */

.logo{

margin-top:130px;
font-size:90px;
font-weight:900;

background:linear-gradient(90deg,#ff7aff,#a855f7,#7c3aed);
-webkit-background-clip:text;
color:transparent;

text-shadow:
0 0 20px #a855ff,
0 0 60px #7c3aed;

}

.tagline{
margin-top:10px;
color:#bbb;
font-style:italic;
}

/* JOIN BUTTON */

.join{

display:inline-block;
margin-top:30px;
padding:18px 45px;

font-size:22px;
font-weight:bold;

background:linear-gradient(90deg,#7c3aed,#a855f7);
border-radius:12px;
color:white;
text-decoration:none;

}

.join:hover{
box-shadow:0 0 20px #a855ff;
}

/* MEMBER COUNTER */

.counter{
margin-top:30px;
font-size:28px;
color:#c7b7ff;
}

/* CARDS */

.card{

background:rgba(0,0,0,.55);
border-radius:20px;
padding:40px;
margin:70px auto;
width:85%;
max-width:900px;

}

/* MEMBERS */

.members{
display:flex;
flex-wrap:wrap;
justify-content:center;
gap:20px;
}

.member{
background:rgba(255,255,255,.05);
padding:20px;
border-radius:14px;
width:170px;
}

/* GALLERY */

.gallery{
display:grid;
grid-template-columns:repeat(auto-fit,minmax(200px,1fr));
gap:15px;
margin-top:25px;
}

.gallery img{
width:100%;
border-radius:10px;
}

footer{
margin:90px 0;
color:#999;
}

</style>

</head>

<body>

<canvas id="stars"></canvas>

<img class="palm-left" src="https://i.imgur.com/ZcLLrkY.png">
<img class="palm-right" src="https://i.imgur.com/ZcLLrkY.png">

<audio autoplay muted loop id="music">
<source src="music.mp3" type="audio/mpeg">
</audio>

<script>
window.addEventListener("click",()=>{
document.getElementById("music").muted=false
})
</script>

<div class="logo">
Jon Jon and Friends
</div>

<div class="tagline">
"Welcome to the party — we don't want it to end."
</div>

<a class="join"
href="https://vrchat.com/home/group/grp_e6ecca5a-828b-4706-9c23-db1723469436"
target="_blank">

JOIN THE VRCHAT GROUP

</a>

<div class="counter">
Members: <span id="memberCount">Loading...</span>
</div>

<div class="card">

<h2>The Community</h2>

<p>
Late night VRChat world hopping, music, and good conversations.
Jon Jon and Friends is a chill space for everyone.
</p>

</div>

<div class="card">

<h2>Members</h2>

<div class="members">

<div class="member">
<h3>Jon Jon</h3>
Founder
</div>

<div class="member">
<h3>Friends</h3>
Community
</div>

<div class="member">
<h3>Legends</h3>
Active Members
</div>

</div>

</div>

<div class="card">

<h2>VRChat Moments</h2>

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

/* STARS */

const canvas=document.getElementById("stars")
const ctx=canvas.getContext("2d")

canvas.width=window.innerWidth
canvas.height=window.innerHeight

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

if(s.y>canvas.height)s.y=0

ctx.beginPath()
ctx.arc(s.x,s.y,s.size,0,Math.PI*2)
ctx.fill()

})

requestAnimationFrame(draw)

}

draw()

/* VRCHAT MEMBER COUNT */

async function getMembers(){

try{

let res=await fetch("https://api.allorigins.win/raw?url=https://vrchat.com/api/1/groups/grp_e6ecca5a-828b-4706-9c23-db1723469436")
let data=await res.json()

document.getElementById("memberCount").innerText=data.memberCount

}catch{

document.getElementById("memberCount").innerText="Unavailable"

}

}

getMembers()
setInterval(getMembers,60000)

</script>

</body>
</html>
