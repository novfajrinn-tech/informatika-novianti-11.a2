<!DOCTYPE html>  <html lang="id">  
<head>  
<meta charset="UTF-8">  
<meta name="viewport" content="width=device-width, initial-scale=1.0">  <title>NOVV CINEMA</title>  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">  <style>  
/* TIKET BIOSKOP ESTETIK */  
  
.ticket{  
  
background:linear-gradient(180deg,#ffffff,#f3f3f3);  
  
color:#111;  
  
border-radius:25px;  
  
padding:25px;  
  
margin-top:25px;  
  
text-align:center;  
  
position:relative;  
  
overflow:hidden;  
  
box-shadow:0 10px 30px rgba(0,0,0,0.4);  
  
border:3px dashed #e50914;  
  
animation:fadeTicket 0.4s ease;  
}  
  
/* LUBANG SAMPING */  
  
.ticket::before,  
.ticket::after{  
  
content:"";  
  
position:absolute;  
  
width:35px;  
height:35px;  
  
background:#111;  
  
border-radius:50%;  
  
top:50%;  
  
transform:translateY(-50%);  
}  
  
.ticket::before{  
left:-18px;  
}  
  
.ticket::after{  
right:-18px;  
}  
  
/* JUDUL */  
  
.ticket h2{  
  
font-size:28px;  
  
margin-bottom:10px;  
  
color:#e50914;  
  
font-weight:800;  
  
letter-spacing:1px;  
}  
  
/* TEXT */  
  
.ticket p{  
  
margin:7px 0;  
  
font-size:15px;  
  
font-weight:500;  
}  
  
/* GARIS */  
  
.ticket-line{  
  
height:2px;  
  
background:repeating-linear-gradient(  
to right,  
#ccc 0 10px,  
transparent 10px 20px  
);  
  
margin:16px 0;  
}  
  
/* BARCODE */  
  
.barcode{  
  
margin-top:20px;  
  
font-size:34px;  
  
letter-spacing:5px;  
  
font-weight:900;  
  
color:#000;  
}  
  
/* ANIMASI */  
  
@keyframes fadeTicket{  
  
from{  
transform:scale(0.8);  
opacity:0;  
}  
  
to{  
transform:scale(1);  
opacity:1;  
}  
  
}  
  
  
*{  
margin:0;  
padding:0;  
box-sizing:border-box;  
font-family:'Poppins',sans-serif;  
}  
  
body{  
background:#0f0f0f;  
color:white;  
overflow-x:hidden;  
}  
  
/* LOGIN */  
  
#login{  
position:fixed;  
inset:0;  
background:#000;  
display:flex;  
flex-direction:column;  
justify-content:center;  
align-items:center;  
gap:12px;  
z-index:9999;  
backdrop-filter:blur(10px);
animation:fadeTicket .5s ease;
}  
  
#login h2{  
color:white;  
}  
  
#login input{  
padding:12px;  
width:230px;  
border:none;  
border-radius:10px;  
outline:none;  
}  
  
#login button{  
padding:12px 20px;  
background:#e50914;  
color:white;  
border:none;  
border-radius:10px;  
cursor:pointer;  
}  
  
/* NAVBAR */  
  
nav{  
position:fixed;  
top:0;  
left:0;  
width:100%;  
height:60px;  
  
display:flex;  
justify-content:space-between;  
align-items:center;  
  
padding:0 15px;  
  
background:rgba(0,0,0,0.95);  
  
z-index:1000;  
}  
  
.logo{  
font-size:35px;  
font-weight:800;  
color:#e50914;  
}  
  
.navbtn{  
background:#222;  
color:white;  
border:none;  
padding:8px 14px;  
border-radius:10px;  
cursor:pointer;  
}  
  
/* MOVIE */  
  
.section{  
padding:80px 15px;  
}  
  
.title{  
margin:20px 0 10px;  
font-size:24px;  
font-weight:700;  
color:#aaa;  
}  
  
.row{  
display:flex;  
gap:12px;  
overflow-x:auto;  
padding-bottom:5px;  
}  
  
.row::-webkit-scrollbar{  
display:none;  
}  
  
.card{  
min-width:190px;  
width:190px;  
height:290px;  
  
border-radius:18px;  
  
overflow:hidden;  
  
position:relative;  
  
cursor:pointer;  
  
flex-shrink:0;  
  
background:#222;  
  
transition:0.3s;  
}  
  
.card:hover{  
transform:scale(1.05);  
}  
  
.card img{  
width:100%;  
height:100%;  
object-fit:cover;  
display:block;  
}  
  
.overlay{  
position:absolute;  
bottom:0;  
width:100%;  
padding:14px;  
font-size:15px;  
font-weight:700;  
background:linear-gradient(to top,#000,transparent);  
  
}  
  
/* MODAL */  
  
.modal{  
position:fixed;  
inset:0;  
  
background:rgba(0,0,0,0.92);  
  
display:none;  
  
justify-content:flex-start;  
align-items:center;  
  
overflow-y:auto;  
  
padding:80px 10px 20px;  
  
z-index:999;  
}  
  
/* BOX */  
  
.box{  
width:100%;  
max-width:520px;  
margin:auto;  
  
background:#141414;  
  
padding:15px;  
  
border-radius:18px;  
  
overflow:hidden;  
}  
  
/* SCREEN */  
  
.screen{  
height:42px;  
  
background:linear-gradient(to right,#444,#999,#444);  
  
border-radius:8px;  
  
text-align:center;  
  
line-height:42px;  
  
font-size:12px;  
  
font-weight:bold;  
  
margin-top:12px;  
margin-bottom:18px;  
  
color:black;  
}  
  
/* SEATS */  
  
.seats{  
  
display:grid;  
  
grid-template-columns:repeat(13, 38px);  
  
gap:6px;  
  
justify-content:flex-start;  
  
overflow-x:auto;  
overflow-y:hidden;  
  
padding:5px 10px 15px;  
  
width:100%;  
}  
  
/* SEAT */  
  
.seat{  
  
width:38px;  
height:38px;  
  
background:#1f1f1f;  
  
font-size:10px;  
font-weight:600;  
  
display:flex;  
align-items:center;  
justify-content:center;  
  
border-radius:8px;  
  
cursor:pointer;  
  
flex-shrink:0;  
  
white-space:nowrap;  
}  
  
.seat.active{  
background:#e50914;  
}  
  
.seat.sold{  
background:#555;  
cursor:not-allowed;  
}  
  
.seat.aisle{  
visibility:hidden;  
}  
  
/* TOTAL */  
  
#total{  
margin-top:10px;  
margin-bottom:10px;  
}  
  
/*NOVV DELICIOUS*/  
  
.snack-list{  
padding:5px 0;  
}  
  
.snack-card{  
  
display:flex;  
align-items:center;  
  
background:#111;  
  
padding:10px;  
  
border-radius:14px;  
  
margin-bottom:12px;  
}  
  
.snack-img{  
width:65px;  
height:65px;  
border-radius:12px;  
object-fit:cover;  
}  
  
.snack-info{  
flex:1;  
margin-left:10px;  
}  
  
.snack-title{  
font-size:13px;  
font-weight:700;  
}  
  
.snack-desc{  
font-size:11px;  
color:#aaa;  
}  
  
.snack-price{  
font-size:12px;  
font-weight:bold;  
margin-top:3px;  
}  
  
.snack-btn{  
  
background:#0a84ff;  
  
border:none;  
  
padding:8px 12px;  
  
border-radius:20px;  
  
color:white;  
  
font-size:11px;  
  
cursor:pointer;  
}  
  
.snack-btn.active{  
background:#16a34a;  
}  
  
/* HISTORY */  
  
#historyPanel{  
  
display:none;  
  
position:fixed;  
inset:0;  
  
background:#111;  
  
padding:20px;  
  
overflow:auto;  
  
z-index:9999;  
}  
  
.history-card{  
  
padding:12px;  
  
background:#1a1a1a;  
  
margin:12px 0;  
  
border-radius:12px;  
}  
  
/* BUTTON */  
  
.buybtn{  
  
width:100%;  
  
margin-top:10px;  
  
padding:12px;  
  
border:none;  
  
border-radius:10px;  
  
font-weight:bold;  
  
cursor:pointer;  
}  
  
</style>  </head>  <body>  <!-- LOGIN -->  <div id="login">  <h2>LOGIN NOVV CINEMA</h2>  <input id="user" placeholder="Username">  <button onclick="enter()">  
Masuk  
</button>  </div>  <!-- NAVBAR -->  <nav>  <div class="logo">  
NOVV CINEMA  
</div>  <button class="navbtn" onclick="openHistory()">  
History  
</button>  </nav>  <!-- MOVIES -->  <div class="section">  <div class="title">  
FILM ACTION  
</div>  <div class="row" id="action"></div>  <div class="title">  
FILM ROMANCE  
</div>  <div class="row" id="romance"></div>  <div class="title">  
FILM HOROR  
</div>  <div class="row" id="horror"></div>  </div>  <!-- MODAL -->  <div class="modal" id="modal">  <div class="box">  <h2 id="movieName"></h2>  <iframe id="trailer"  
width="100%"  
height="220"  
style="  
border:none;  
border-radius:14px;  
margin-top:12px;  
margin-bottom:15px;  
"  
allowfullscreen>  
</iframe>  <div class="screen">  
LAYAR BIOSKOP  
</div>  <div class="seats" id="seatBox"></div>  <h3 id="total">  
Total: Rp0  
</h3>  <h3 style="margin-top:10px;">  
🍿 NOVV DELICIOUS  
</h3>  <div class="snack-list">  <div class="snack-card">  <img class="snack-img"  
src="snack2.jpg">

<div class="snack-info">  <div class="snack-title">  
SALTED POPCORN  
</div>   <div class="snack-desc">  
Salty Goodness  
</div>  <div class="snack-price">  
Rp37.000  
</div>  </div>  <button class="snack-btn"  
onclick="addSnack(this,'Salted Popcorn',37000)">
PESAN
</button>

</div>  <div class="snack-card">  <img class="snack-img"  
src="snack1.jpg">

<div class="snack-info">  <div class="snack-title">  
SWEET POPCORN  
</div>  <div class="snack-desc">  
Yummy  
</div>  <div class="snack-price">  
Rp35.000  
</div>  </div>  <button class="snack-btn"  
onclick="addSnack(this,'Sweet Popcorn',35000)">
PESAN
</button>

</div>  
<!-- MINUMAN XXI -->  <div class="snack-card">  <img class="snack-img"  
src="drink1.jpg">

<div class="snack-info">  <div class="snack-title">  
COCA COLA 250ML  
</div>  <div class="snack-desc">  
Fresh Ice Drink  
</div>  <div class="snack-price">  
Rp28.000  
</div>  </div>  <button class="snack-btn"  
onclick="addSnack(this,'Coca Cola 250ML',28000)">
PESAN
</button>

</div>  <div class="snack-card">  <img class="snack-img"  
src="drink3.jpg">

<div class="snack-info">  <div class="snack-title">  
BROWN SUGAR MILK  
</div>  <div class="snack-desc">  
Sweet & Smooth Drink  
</div>  <div class="snack-price">  
Rp30.000  
</div>  </div>  <button class="snack-btn"  
onclick="addSnack(this,'Brown Sugar Milk',30000)">
PESAN
</button>

</div>  <div class="snack-card">  <img class="snack-img"  
src="drink4.jpg">

<div class="snack-info">  <div class="snack-title">  
MATCHA LATTE  
</div>  <div class="snack-desc">  
Premium NovvCinema Drink  
</div>  <div class="snack-price">  
Rp37.000  
</div>  </div>  <button class="snack-btn"  
onclick="addSnack(this,'Matcha Latte',37000)">
PESAN
</button>

</div>  </div>  <button class="buybtn"  
style="background:#e50914;color:white;"  
onclick="buy()">
BELI SEKARANG
</button>

<button class="buybtn"  
style="background:#333;color:white;"  
onclick="closeModal()">

CLOSE

</button>  </div>  </div>  <!-- HISTORY -->  <div id="historyPanel">  <h2>  
🎟 HISTORY TICKET  
</h2>  <div id="historyList"></div>  <button class="buybtn"  
style="background:#333;color:white;"  
onclick="closeHistory()">

CLOSE

</button>  
<div id="ticketPrint"></div>  </div>  <script>  
  
/* DATA */  
  
let user="";  
  
let selectedMovie="";  
  
let seats=[];  
  
let snacks=[];  
  
let soldSeats = JSON.parse(
localStorage.getItem("soldSeats") || "[]"
);
  
let tickets=JSON.parse(  
localStorage.getItem("tickets") || "[]"  
);  
  
/* LOGIN */  
  
function enter(){  
  
let u=document.getElementById("user").value;  
  
if(u.trim()!==""){  
  
user=u;  
  
document.getElementById("login").style.display="none";  
  
}  
  
}  
  
/* MOVIE DATA + FOTO SENDIRI */  
  
const data={  
  
action:[  
  
{  
  
name:"THE TOMORROW WAR",  
img:"baik1.jpg",  
trailer:"https://www.youtube.com/embed/LnIbOiskSdc?autoplay=1"  
},  
  
{  
name:"NO TIME TO DIE",  
img:"baik2.jpg",  
trailer:"https://www.youtube.com/embed/BIhNsAtPbPI?si=Y5dOOp14PgfBto6r"  
},  
  
  
{  
name:"OUTSIDE THE WIRE",  
img:"baik3.jpg",  
trailer:"https://www.youtube.com/embed/u8ZsUivELbs?si=ekxPGX6qp2qu-9oI"  
},  
  
{  
name:"THE MATRIX RESURRECTIONS",  
img:"baik4.jpg",  
trailer:"https://www.youtube.com/embed/AD_8i1xRyTA?si=QrLvj0wA0bu1OPpo"  
},  
  
{  
name:"13 BOM DI JAKARTA",  
img:"baik5.jpg",  
trailer:"https://www.youtube.com/embed/AdjedKX9nas?si=ztPIPOcMncF7tKd7"  
}  
  
],  
  
romance:[  
  
{  
name:"HABIBIE & AIUNUN 3",  
img:"fajrin1.jpg",  
trailer:"https://youtube.com/embed/CIP0esJ6MMs?si=ufVxDK1sFzz-_bBp"  
},  
  
{  
name:"ANANTA",  
img:"fajrin2.jpg",  
trailer:"https://youtube.com/embed/1Re0nOo8b0M?si=3YZpZF04dprk4-Jr"  
},  
  
{  
name:"MATT & MOU",  
img:"fajrin3.jpg",  
trailer:"https://youtube.com/embed/vw_IgWC65mM?si=UkilLAf3Yjm8B7ih"  
},  
  
{  
name:"PAST LIVES",  
img:"fajrin4.jpg",  
trailer:"https://youtube.com/embed/kA244xewjcI?si=o4xueUZqlDKfdlgO"  
},  
  
{  
name:"LOVE AGAIN",  
img:"fajrin5.jpg",  
trailer:"https://youtube.com/embed/CQDXtD2HJAs?si=3iRHBAVjzKqflL5t"  
},  
  
],  
  
horror:[  
  
{  
name:"KUASA GELAP",  
img:"triass1.jpg",  
trailer:"https://youtube.com/embed/sMkUS1wqr8Q?si=PLVjqBPkjhhHIXdF"  
},  
  
{  
name:"SUMALA",  
img:"triass2.jpg",  
trailer:"https://youtube.com/embed/aMaMeKHH6iM?si=mhh3Jw9aLfdidFH6"  
},  
  
{  
name:"PEREWANGAN",  
img:"triass3.png",  
trailer:"https://youtube.com/embed/LS3Cz0b14mc?si=z7X3CiLK2m3O24n2"  
},  
  
{   
name:"THE CONJURING LAST RITES",  
img:"triass4.jpg",  
trailer:"https://youtube.com/embed/bMgfsdYoEEo?si=SIrEsRhF6P_9siJR"  
},  
  
{  
name:"SEWU DINO",  
img:"triass5.jpg",  
trailer:"https://youtube.com/embed/12sXNFbQa6I?si=ZIzhdCe4GevHAIEj"  
},  
]  
  
};  
  
/* LOAD MOVIES */  
  
function load(){  
  
createMovie("action",data.action);  
  
createMovie("romance",data.romance);  
  
createMovie("horror",data.horror);  
  
}  
  
function createMovie(id,list){  
  
let box=document.getElementById(id);  
  
list.forEach(movie=>{  
  
let card=document.createElement("div");  
  
card.className="card";  
  
card.innerHTML=`  
  
<img src="${movie.img}">  
  
<div class="overlay">  
${movie.name}  
</div>  
  
`;  
  
card.onclick=()=>openMovie(movie);  
  
box.appendChild(card);  
  
});  
  
}  
  
load();  
  
/* OPEN MOVIE */  
  
function openMovie(movie){  
  
selectedMovie=movie.name;  
  
seats=[];  
  
snacks=[];  
  
document.getElementById("movieName").innerText=  
movie.name;  
  
document.getElementById("trailer").src=  
movie.trailer;  
  
document.getElementById("modal").style.display=  
"flex";  
  
loadSeats();  
  
update();  
  
}  
  
/* LOAD SEATS */  
  
function loadSeats(){  
  
let box=document.getElementById("seatBox");  
  
box.innerHTML="";  
  
let rows="ABCDEFGHIJ";  
  
for(let i=0;i<10;i++){  
  
for(let j=1;j<=12;j++){  
  
if(j===7){  
  let gap=document.createElement("div");  
  gap.className="seat aisle";  
  box.appendChild(gap);  
  continue;  
}  
  
let id=rows[i]+j;  
  
let seat=document.createElement("div");  
  
seat.className="seat";  
  
seat.innerText=id;  
  
if(soldSeats.includes(id)){  
seat.classList.add("sold");  
}  
  
seat.onclick=()=>{  
  
if(seat.classList.contains("sold")) return;  
  
seat.classList.toggle("active");  
  
if(seats.includes(id)){  
  
seats=seats.filter(x=>x!==id);  
  
}else{  
  
seats.push(id);  
  
}  
  
update();  
  
};  
  
box.appendChild(seat);  
  
}  
  
}  
  
}  
  
/* SNACK */  
  
function addSnack(el,name,price){  
  
el.classList.toggle("active");  
  
let index=snacks.findIndex(  
s=>s.name===name  
);  
  
if(index>-1){  
  
snacks.splice(index,1);  
  
}else{  
  
snacks.push({  
name,  
price  
});  
  
}  
  
update();  
  
}  
  
/* UPDATE */  
  
function update(){  
  
let total=  
(seats.length*35000)+  
snacks.reduce((a,b)=>a+b.price,0);  
  
document.getElementById("total").innerText=  
"Total: Rp"+total;  
  
}  
  
/* BUY */  
  
function buy(){  
  
if(seats.length===0){  
  
alert("Pilih kursi dulu!");  
  
return;  
  
}  
  
let total=  
(seats.length*35000)+  
snacks.reduce((a,b)=>a+b.price,0);  
  
let ticketID="NOVV-"+Date.now();  
  
let ticket={  
  
id:ticketID,  
  
movie:selectedMovie,  
  
seats,  
  
snacks,  
  
user,  
total  
  
};  
  
tickets.push(ticket);  
soldSeats = soldSeats.concat(seats);  
  
localStorage.setItem(  
"tickets",  
JSON.stringify(tickets)  
);  
  
  
/* TAMPILKAN TIKET */  
  
document.getElementById("ticketPrint").innerHTML=`  
  
<div class="ticket">  
  
<h2>🎬 NOVV CINEMA</h2>  
  
<div class="ticket-line"></div>  
  
<p><b>ID Ticket:</b></p>  
<p>${ticket.id}</p>  
  
<div class="ticket-line"></div>  
  
<p><b>Movie:</b></p>  
<p>${ticket.movie}</p>  
  
<div class="ticket-line"></div>  
  
<p><b>Seats:</b></p>  
<p>${ticket.seats.join(", ")}</p>  
  
<div class="ticket-line"></div>  
  
<p><b>Snacks:</b></p>  
<p>  
${ticket.snacks.length > 0  
? ticket.snacks.map(s=>s.name).join(", ")  
: "Tidak ada"}  
</p>  
  
<div class="ticket-line"></div>  
  
<p><b>Total:</b></p>  
<p>Rp${ticket.total}</p>  
  
<div class="ticket-line"></div>  
  
<p><b>Atas Nama:</b></p>  
<p>${ticket.user}</p>  
  
<div class="barcode">  
||||| |||| ||| ||  
</div>  
  
</div>  
  
`;  
  
document.getElementById("historyPanel").style.display="block";  
  openHistory();
closeModal();  
  
}  
  
  
/* HISTORY */  
  
function openHistory(){  
  
let box=document.getElementById("historyList");  
  
box.innerHTML="";  
  
tickets.forEach((t,i)=>{  
  
box.innerHTML+=`  
  
<div class="history-card">  
  
<b>${t.movie}</b>  
  
<br><br>  
  
Seats:  
${t.seats.join(", ")}  
  
<br><br>  
  
User:  
${t.user}  
  
<br><br>  
  
<button onclick="deleteTicket(${i})"  
style="  
background:#e50914;  
border:none;  
padding:8px 12px;  
color:white;  
border-radius:8px;  
cursor:pointer;  
">  
  
Delete  
  
</button>  
  
</div>  
  
`;  
  
});  
  
document.getElementById("historyPanel").style.display="block";  
  
}  
  
/* DELETE */  
  
function deleteTicket(i){  
  
tickets.splice(i,1);  
  
localStorage.setItem(  
"tickets",  
JSON.stringify(tickets)  
);  
  
openHistory();  
  
}  
  
/* CLOSE */  
  
function closeHistory(){  
  
document.getElementById("historyPanel").style.display="none";  
  
}  
  
function closeModal(){  
  
document.getElementById("modal").style.display="none";  
  
document.getElementById("trailer").src="";  
  
}  
  
</script>  </body>  
</html>
