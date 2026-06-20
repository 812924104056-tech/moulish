
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Thank You ❤️</title>

<style>
*{
margin:0;
padding:0;
box-sizing:border-box;
font-family:'Poppins',sans-serif;
}

body{
height:100vh;
display:flex;
justify-content:center;
align-items:center;
background:linear-gradient(135deg,#ff758c,#ff7eb3,#ffd6e8);
overflow:hidden;
}

.container{
text-align:center;
color:white;
z-index:2;
}

.gift{
font-size:110px;
animation:shake 1s infinite;
cursor:pointer;
}

@keyframes shake{
0%{transform:rotate(0);}
25%{transform:rotate(8deg);}
50%{transform:rotate(-8deg);}
75%{transform:rotate(8deg);}
100%{transform:rotate(0);}
}

button{
margin-top:20px;
padding:14px 35px;
border:none;
border-radius:40px;
font-size:18px;
cursor:pointer;
background:white;
color:#ff4f81;
font-weight:bold;
transition:.3s;
}

button:hover{
transform:scale(1.1);
}

.card{
display:none;
margin-top:30px;
padding:30px;
width:380px;
background:rgba(255,255,255,.18);
backdrop-filter:blur(15px);
border-radius:20px;
box-shadow:0 0 30px rgba(255,255,255,.4);
animation:fade 1.5s;
}

@keyframes fade{
from{
opacity:0;
transform:scale(.6);
}
to{
opacity:1;
transform:scale(1);
}
}

h2{
margin-bottom:15px;
}

p{
font-size:18px;
line-height:1.8;
}

.heart{
position:absolute;
font-size:22px;
animation:float 7s linear infinite;
color:white;
}

@keyframes float{
0%{
transform:translateY(100vh);
opacity:0;
}
20%{
opacity:1;
}
100%{
transform:translateY(-120vh);
opacity:0;
}
}
</style>
</head>

<body>

<div class="container">

<div class="gift">🎁</div>

<button onclick="openGift()">Open Gift ❤️</button>

<div class="card" id="card">

<h2>✨ Thank You ✨</h2>

<p>
Dear Friend,<br><br>

Thank you for making my birthday extra special. ❤️<br><br>

Your wishes brought a smile to my face and happiness to my heart.<br><br>

Life becomes more beautiful with friends like you.<br><br>

Thank you for your support, care, and wonderful friendship.<br><br>

🤍 Forever Grateful 🤍<br><br>

<b>— Moulishwaran</b>

</p>

</div>

</div>

<script>

function openGift(){
document.getElementById("card").style.display="block";

for(let i=0;i<80;i++){

let heart=document.createElement("div");
heart.innerHTML="❤";
heart.className="heart";

heart.style.left=Math.random()*100+"vw";
heart.style.animationDuration=(Math.random()*4+3)+"s";
heart.style.fontSize=(Math.random()*25+15)+"px";

document.body.appendChild(heart);

setTimeout(()=>{
heart.remove();
},7000);

}
}

</script>

</body>
</html>
