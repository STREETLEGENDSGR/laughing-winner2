street-legends-gr/
│
├── index.html
├── style.css
├── script.js
│
├── assets/
│   ├── logo.png
│   ├── hero-r35.jpg
│   ├── gallery1.jpg
│   ├── gallery2.jpg
│   └── gallery3.jpg
│
└── pages/
    ├── events.html
    ├── gallery.html
    ├── members.html
    └── shop.html
<!DOCTYPE html>
<html lang="el">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Street Legends GR</title>

<link rel="stylesheet" href="style.css">

<link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@400;700&display=swap" rel="stylesheet">
</head>

<body>

<header>
<div class="logo">
STREET LEGENDS GR
</div>

<nav>
<a href="#">Αρχική</a>
<a href="#">Events</a>
<a href="#">Gallery</a>
<a href="#">Members</a>
<a href="#">Shop</a>
</nav>

<div class="auth">
<button>Σύνδεση</button>
<button class="gold">Εγγραφή</button>
</div>
</header>

<section class="hero">

<div class="overlay">

<h1>STREET LEGENDS GR</h1>

<p>
Η μεγαλύτερη ελληνική automotive κοινότητα.
</p>

<a href="#" class="cta">
ΔΗΛΩΣΗ ΣΥΜΜΕΤΟΧΗΣ
</a>

</div>

</section>

<section class="event-box">

<h2>Επόμενη Συνάντηση</h2>

<p>17/07/2026</p>
<p>18:00</p>
<p>Αττική</p>

</section>

<section class="featured">

<h2>Featured Cars</h2>

<div class="cars">

<div class="card">
<img src="assets/gallery1.jpg">
<h3>Nissan R35 GTR</h3>
</div>

<div class="card">
<img src="assets/gallery2.jpg">
<h3>BMW M4</h3>
</div>

<div class="card">
<img src="assets/gallery3.jpg">
<h3>Toyota Supra</h3>
</div>

</div>

</section>

<footer>

<p>© 2026 Street Legends GR</p>

</footer>

<script src="script.js"></script>

</body>
</html>
*{
margin:0;
padding:0;
box-sizing:border-box;
font-family:'Orbitron',sans-serif;
}

body{
background:#0b0b0b;
color:white;
overflow-x:hidden;
}

header{
position:fixed;
top:0;
left:0;
width:100%;
padding:20px 60px;
display:flex;
justify-content:space-between;
align-items:center;
background:rgba(0,0,0,.7);
backdrop-filter:blur(10px);
z-index:1000;
border-bottom:1px solid rgba(255,215,0,.2);
}

.logo{
font-size:28px;
font-weight:700;
color:#FFD700;
text-shadow:0 0 20px #FFD700;
}

nav{
display:flex;
gap:25px;
}

nav a{
text-decoration:none;
color:white;
font-size:15px;
transition:.3s;
}

nav a:hover{
color:#FFD700;
}

.auth{
display:flex;
gap:10px;
}

.auth button{
padding:10px 18px;
border:none;
cursor:pointer;
border-radius:8px;
font-weight:600;
}

.auth .gold{
background:#FFD700;
color:black;
}

.hero{
height:100vh;
background:url('assets/hero-r35.jpg') center center/cover;
display:flex;
align-items:center;
justify-content:center;
text-align:center;
position:relative;
}

.overlay{
position:absolute;
width:100%;
height:100%;
background:rgba(0,0,0,.55);
display:flex;
flex-direction:column;
justify-content:center;
align-items:center;
}

.hero h1{
font-size:70px;
color:#FFD700;
text-shadow:0 0 35px #FFD700;
margin-bottom:20px;
}

.hero p{
font-size:20px;
max-width:700px;
margin-bottom:35px;
}

.cta{
padding:18px 40px;
background:#FFD700;
color:black;
font-weight:bold;
text-decoration:none;
border-radius:10px;
transition:.3s;
}

.cta:hover{
transform:scale(1.08);
box-shadow:0 0 30px #FFD700;
}

.event-box{
width:90%;
max-width:900px;
margin:80px auto;
padding:40px;
background:#141414;
border:1px solid #FFD700;
border-radius:20px;
text-align:center;
box-shadow:0 0 20px rgba(255,215,0,.15);
}

.event-box h2{
color:#FFD700;
margin-bottom:20px;
font-size:32px;
}

.event-box p{
margin:10px 0;
font-size:18px;
}

.featured{
padding:80px 50px;
}

.featured h2{
text-align:center;
font-size:42px;
margin-bottom:50px;
color:#FFD700;
}

.cars{
display:grid;
grid-template-columns:repeat(auto-fit,minmax(300px,1fr));
gap:30px;
}

.card{
background:#111;
border-radius:20px;
overflow:hidden;
transition:.4s;
border:1px solid rgba(255,215,0,.2);
}

.card:hover{
transform:translateY(-10px);
box-shadow:0 0 30px rgba(255,215,0,.35);
}

.card img{
width:100%;
height:250px;
object-fit:cover;
}

.card h3{
padding:20px;
text-align:center;
color:#FFD700;
}

footer{
margin-top:80px;
padding:30px;
text-align:center;
background:#000;
border-top:1px solid rgba(255,215,0,.2);
}

footer p{
color:#888;
}

::-webkit-scrollbar{
width:8px;
}

::-webkit-scrollbar-track{
background:#0b0b0b;
}

::-webkit-scrollbar-thumb{
background:#FFD700;
border-radius:10px;
}

@media(max-width:768px){

header{
padding:15px 20px;
flex-direction:column;
gap:15px;
}

.hero h1{
font-size:40px;
}

.hero p{
font-size:16px;
padding:0 20px;
}

nav{
flex-wrap:wrap;
justify-content:center;
}

}
// Loading Screen

window.addEventListener("load", () => {

const loader = document.querySelector(".loader");

if(loader){
loader.classList.add("loader-hidden");
}

});

// Smooth Scroll

document.querySelectorAll('a[href^="#"]').forEach(anchor => {

anchor.addEventListener("click", function(e){

e.preventDefault();

const target = document.querySelector(this.getAttribute("href"));

if(target){

target.scrollIntoView({
behavior:"smooth"
});

}

});

});

// Navbar Effect

window.addEventListener("scroll", () => {

const header = document.querySelector("header");

if(window.scrollY > 50){

header.style.background = "rgba(0,0,0,0.95)";
header.style.boxShadow = "0 0 25px rgba(255,215,0,0.15)";

}else{

header.style.background = "rgba(0,0,0,0.7)";
header.style.boxShadow = "none";

}

});

// Countdown Event

const countdownDate = new Date("Jul 17, 2026 18:00:00").getTime();

const timer = setInterval(() => {

const now = new Date().getTime();

const distance = countdownDate - now;

const days = Math.floor(distance / (1000 * 60 * 60 * 24));

const hours = Math.floor(
(distance % (1000 * 60 * 60 * 24))
/
(1000 * 60 * 60)
);

const minutes = Math.floor(
(distance % (1000 * 60 * 60))
/
(1000 * 60)
);

const seconds = Math.floor(
(distance % (1000 * 60))
/
1000
);

const countdown = document.getElementById("countdown");

if(countdown){

countdown.innerHTML =
`${days} Ημέρες ${hours} Ώρες ${minutes} Λεπτά ${seconds} Δευτ.`;

}

if(distance < 0){

clearInterval(timer);

if(countdown){

countdown.innerHTML = "Η ΣΥΝΑΝΤΗΣΗ ΞΕΚΙΝΗΣΕ";

}

}

},1000);

// Reveal Animation

const observer = new IntersectionObserver(entries => {

entries.forEach(entry => {

if(entry.isIntersecting){

entry.target.classList.add("show");

}

});

});

document.querySelectorAll(".card,.event-box,.featured")
.forEach(el => observer.observe(el));

// Gallery Lightbox

const galleryImages = document.querySelectorAll(".card img");

galleryImages.forEach(image => {

image.addEventListener("click", () => {

const lightbox = document.createElement("div");

lightbox.id = "lightbox";

lightbox.innerHTML =
`<img src="${image.src}">`;

document.body.appendChild(lightbox);

lightbox.addEventListener("click", () => {

lightbox.remove();

});

});

});

// Hero Animation

const heroTitle = document.querySelector(".hero h1");

if(heroTitle){

setInterval(() => {

heroTitle.style.textShadow =
`0 0 ${20 + Math.random()*40}px #FFD700`;

},700);

}
<div id="countdown"></div>
<!DOCTYPE html>
<html lang="el">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Εγγραφή Μέλους | Street Legends GR</title>
<link rel="stylesheet" href="../style.css">
</head>

<body>

<section class="register-container">

<h1>Εγγραφή Μέλους</h1>

<form id="memberForm">

<input type="text"
placeholder="Ονοματεπώνυμο"
required>

<input type="email"
placeholder="Email"
required>

<input type="text"
placeholder="Αυτοκίνητο"
required>

<input type="file"
accept="image/*"
required>

<textarea
placeholder="Λίγα λόγια για το αυτοκίνητο">
</textarea>

<button type="submit">
ΥΠΟΒΟΛΗ
</button>

</form>

<div id="success"></div>

</section>

<script>
document
.getElementById("memberForm")
.addEventListener("submit",function(e){

e.preventDefault();

document.getElementById("success").innerHTML =
"✅ Η αίτησή σας καταχωρήθηκε.";

});
</script>

</body>
</html>
.register-container{
max-width:700px;
margin:150px auto;
padding:40px;
background:#111;
border:1px solid #FFD700;
border-radius:20px;
}

.register-container h1{
text-align:center;
color:#FFD700;
margin-bottom:30px;
}

.register-container form{
display:flex;
flex-direction:column;
gap:15px;
}

.register-container input,
.register-container textarea{
padding:15px;
background:#1a1a1a;
border:1px solid #333;
color:white;
border-radius:10px;
}

.register-container button{
padding:15px;
background:#FFD700;
border:none;
font-weight:bold;
cursor:pointer;
border-radius:10px;
}

#success{
margin-top:20px;
text-align:center;
color:#00ff66;
font-weight:bold;
}
