# Dikuuu<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>To My Cutieee 💖</title>
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;600&display=swap" rel="stylesheet">
<style>
body{
    margin:0;
    font-family:'Poppins', sans-serif;
    background: linear-gradient(135deg,#ffd6e8,#e0c3fc);
    overflow-x:hidden;
    text-align:center;
    color:#fff;
}
section{
    padding:60px 20px;
}
h1{
    font-size:40px;
}
button{
    padding:12px 25px;
    border:none;
    border-radius:30px;
    background:#ff4f81;
    color:white;
    font-size:16px;
    cursor:pointer;
    transition:0.3s;
}
button:hover{
    transform:scale(1.1);
    background:#ff2e6a;
}
.card{
    background:rgba(255,255,255,0.2);
    backdrop-filter:blur(10px);
    margin:15px;
    padding:20px;
    border-radius:15px;
    display:inline-block;
    width:250px;
}
.gallery img{
    width:150px;
    border-radius:15px;
    margin:10px;
    transition:0.4s;
}
.gallery img:hover{
    transform:scale(1.1);
}
footer{
    padding:20px;
    font-size:14px;
}
.heart{
    position:fixed;
    color:#ff4f81;
    font-size:20px;
    animation: float 6s linear infinite;
}
@keyframes float{
    0%{transform:translateY(100vh);}
    100%{transform:translateY(-10vh);}
}
.modal{
    display:none;
    position:fixed;
    top:0;left:0;
    width:100%;height:100%;
    background:rgba(0,0,0,0.7);
    justify-content:center;
    align-items:center;
}
.modal-content{
    background:white;
    color:#ff4f81;
    padding:30px;
    border-radius:15px;
}
</style>
</head>
<body>

<section>
<h1>Happy Valentine’s Day, Cutieee ❤️</h1>
<p>You are my today and all of my tomorrows.</p>
<button onclick="showSurprise()">Click for a Surprise 💌</button>
</section>

<section>
<h2>💖 A Message For You 💖</h2>
<p id="typing"></p>
</section>

<section>
<h2>📸 Our Memories</h2>
<div class="gallery">
<img src="https://via.placeholder.com/150" alt="">
<img src="https://via.placeholder.com/150" alt="">
<img src="https://via.placeholder.com/150" alt="">
</div>
</section>

<section>
<h2>🌸 Reasons I Love You</h2>
<div class="card">Your cute smile 😊</div>
<div class="card">Your caring heart 💗</div>
<div class="card">Your beautiful eyes ✨</div>
<div class="card">The way you say my name 💕</div>
</section>

<div class="modal" id="modal">
<div class="modal-content">
<h2>Will you be my Valentine forever, Cutieee? 💍❤️</h2>
<button onclick="yesLove()">YES 💖</button>
<button onclick="closeModal()">OF COURSE 😘</button>
</div>
</div>

<footer>
Made with ❤️ by Your Forever Person
</footer>

<script>
// Typing Effect
let text = "Cutieee, you are the most beautiful part of my life. Every moment with you feels magical. I am so lucky to call you mine. ❤️";
let i = 0;
function typing(){
    if(i < text.length){
        document.getElementById("typing").innerHTML += text.charAt(i);
        i++;
        setTimeout(typing,50);
    }
}
typing();

// Floating Hearts
setInterval(()=>{
    let heart = document.createElement("div");
    heart.classList.add("heart");
    heart.innerHTML="❤️";
    heart.style.left=Math.random()*100+"vw";
    heart.style.fontSize=Math.random()*20+10+"px";
    document.body.appendChild(heart);
    setTimeout(()=>heart.remove(),6000);
},500);

// Modal
function showSurprise(){
    document.getElementById("modal").style.display="flex";
}
function closeModal(){
    document.getElementById("modal").style.display="none";
}
function yesLove(){
    alert("Yayyy! I Love You Forever Cutieee 💖💖💖");
}
</script>

</body>
</html>
