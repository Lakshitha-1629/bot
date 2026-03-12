<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>NoMercy-MD Cyber Control Panel</title>
<link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@500;700&display=swap" rel="stylesheet">

<style>

body{
margin:0;
background:black;
font-family:'Orbitron', monospace;
color:#00ffea;
overflow-x:hidden;
}

/* MATRIX BACKGROUND */

canvas{
position:fixed;
top:0;
left:0;
width:100%;
height:100%;
z-index:-1;
}

/* HEADER */

header{
text-align:center;
padding:60px 20px;
}

header h1{
font-size:60px;
color:#ff0000;
text-shadow:0 0 10px red,0 0 30px red;
animation:glitch 1s infinite;
}

@keyframes glitch{
0%{text-shadow:2px 0 red,-2px 0 blue;}
25%{text-shadow:-2px 2px red,2px -2px blue;}
50%{text-shadow:2px -2px red,-2px 2px blue;}
75%{text-shadow:-2px 0 red,2px 0 blue;}
100%{text-shadow:2px 0 red,-2px 0 blue;}
}

header p{
color:#00ffee;
font-size:18px;
}

/* LOGO */

.logo{
width:180px;
margin-bottom:20px;
animation:float 3s infinite ease-in-out;
}

@keyframes float{
0%{transform:translateY(0)}
50%{transform:translateY(-12px)}
100%{transform:translateY(0)}
}

/* PANELS */

.container{
width:90%;
max-width:800px;
margin:auto;
}

.panel{
background:rgba(0,0,0,0.85);
border:2px solid #00ffee;
box-shadow:0 0 20px #00ffee;
padding:30px;
margin:25px 0;
border-radius:10px;
transition:0.3s;
}

.panel:hover{
box-shadow:0 0 30px #ff00ff;
}

.title{
font-size:26px;
margin-bottom:15px;
color:#00ffee;
}

.text{
font-size:18px;
margin:6px 0;
}

/* BUTTONS */

.btn{
display:inline-block;
margin-top:15px;
padding:12px 25px;
background:#00ffee;
color:black;
border:none;
border-radius:5px;
font-weight:bold;
cursor:pointer;
box-shadow:0 0 10px #00ffee;
transition:0.3s;
}

.btn:hover{
background:red;
color:white;
transform:scale(1.1);
box-shadow:0 0 20px red;
}

/* WARNING */

.warning{
color:red;
font-size:20px;
text-shadow:0 0 10px red;
}

/* FOOTER */

footer{
text-align:center;
padding:40px;
color:#aaa;
text-shadow:0 0 10px cyan;
}

</style>
</head>

<body>

<canvas id="matrix"></canvas>

<header>

<img src="https://github.com/Lakshitha-1629/bot/blob/main/logo/NoMercy.png?raw=true" class="logo">

<h1>NoMercy-MD</h1>

<p>Cyber Hacker Control System</p>

</header>


<div class="container">

<div class="panel">

<div class="title">🤖 BOT INFORMATION</div>

<div class="text">Bot Name : <b>NoMercy-MD</b></div>

<div class="text">Version : <b>V1</b></div>

<div class="text">Team : <b>Out Of Metrix</b></div>

</div>


<div class="panel">

<div class="title">👑 OWNER INFORMATION</div>

<div class="text">Owner Name : <b>Lakshitha</b></div>

<div class="text">Access : <b>Owner Only</b></div>

<button class="btn">Owner Menu</button>

</div>


<div class="panel">

<div class="title">⚡ BOT FEATURES</div>

<div class="text">Bug Menu</div>

<div class="text">Download Menu</div>

<div class="text">Main Menu</div>

<div class="text">Free Fire Hacks (Coming Soon)</div>

<button class="btn">View Commands</button>

</div>


<div class="panel">

<div class="title">🌐 WEBSITE</div>

<div class="text">Official Website : Coming Soon</div>

<button class="btn">Visit Website</button>

</div>


<div class="panel">

<div class="title">⚠ SYSTEM STATUS</div>

<div class="warning">💀 SYSTEM LOCKED</div>

<div class="warning">⚡ PUBLIC ACCESS : COMING SOON</div>

</div>

</div>


<footer>

⚡ Powered by NoMercy-MD | Out Of Metrix Cyber Team ⚡

</footer>


<script>

const canvas=document.getElementById("matrix");

const ctx=canvas.getContext("2d");

canvas.height=window.innerHeight;

canvas.width=window.innerWidth;

const letters="ABCDEFGHIJKLMNOPQRSTUVWXYZ123456789@#$%^&*";

const fontSize=14;

const columns=canvas.width/fontSize;

const drops=[];

for(let i=0;i<columns;i++) drops[i]=1;

function draw(){

ctx.fillStyle="rgba(0,0,0,0.05)";

ctx.fillRect(0,0,canvas.width,canvas.height);

ctx.fillStyle="#0f0";

ctx.font=fontSize+"px monospace";

for(let i=0;i<drops.length;i++){

const text=letters[Math.floor(Math.random()*letters.length)];

ctx.fillText(text,i*fontSize,drops[i]*fontSize);

if(drops[i]*fontSize>canvas.height && Math.random()>0.975)

drops[i]=0;

drops[i]++;

}

}

setInterval(draw,50);

</script>

</body>
</html>
