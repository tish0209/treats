<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>TREATS Bakery | Kimberley CBD</title>

<link href="https://fonts.googleapis.com/css2?family=Lobster&family=Playfair+Display:wght@600&family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">

<style>
*{margin:0;padding:0;box-sizing:border-box;}
body{
font-family:'Poppins',sans-serif;
background:linear-gradient(to right,#ffe0f5,#fff3b0);
color:#444;
}

/* HEADER */
header{
background:#ff69b4;
padding:15px 30px;
display:flex;
justify-content:space-between;
align-items:center;
color:white;
}

.logo{
font-family:'Lobster',cursive;
font-size:2.8rem;
}

/* HERO */
.hero{
background:url('https://images.unsplash.com/photo-1555507036-ab1f4038808a');
background-size:cover;
background-position:center;
padding:100px 20px;
text-align:center;
color:white;
}

.hero h1{
font-family:'Lobster',cursive;
font-size:4rem;
margin-bottom:20px;
text-shadow:2px 2px 10px rgba(0,0,0,0.5);
}

/* SECTION */
section{
padding:60px 20px;
text-align:center;
}

.section-title{
font-family:'Playfair Display',serif;
font-size:2.3rem;
margin-bottom:30px;
color:#ff1493;
}

.grid{
display:grid;
grid-template-columns:repeat(auto-fit,minmax(250px,1fr));
gap:20px;
max-width:1100px;
margin:auto;
}

.card{
background:white;
padding:20px;
border-radius:20px;
box-shadow:0 10px 20px rgba(0,0,0,0.1);
transition:0.3s;
}

.card:hover{
transform:scale(1.05);
}

.price{
color:#ff1493;
font-weight:bold;
}

button{
background:#ff69b4;
color:white;
border:none;
padding:8px 15px;
border-radius:20px;
cursor:pointer;
margin-top:8px;
}

button:hover{
background:#ff1493;
}

/* CART */
.cart{
background:white;
max-width:500px;
margin:20px auto;
padding:20px;
border-radius:20px;
box-shadow:0 10px 20px rgba(0,0,0,0.1);
}

.cart h3{
margin-bottom:10px;
}

.total{
font-weight:bold;
margin-top:10px;
color:#ff1493;
}

/* DELIVERY */
select{
padding:10px;
margin-top:10px;
border-radius:10px;
}

/* INSTAGRAM */
.instagram{
display:flex;
justify-content:center;
gap:15px;
flex-wrap:wrap;
}

.instagram img{
width:120px;
height:120px;
border-radius:15px;
object-fit:cover;
}

/* FOOTER */
footer{
background:#ff69b4;
color:white;
padding:20px;
text-align:center;
margin-top:40px;
}

@media(max-width:768px){
.hero h1{font-size:2.5rem;}
}
</style>
</head>

<body>

<header>
<div class="logo">TREATS 🍰</div>
</header>

<section class="hero">
<h1>Order Your Favourite Treats 💕</h1>
</section>

<section>
<h2 class="section-title">Our Menu</h2>
<div class="grid" id="menu"></div>
</section>

<div class="cart">
<h3>🛒 Your Cart</h3>
<ul id="cart-items"></ul>
<p class="total">Total: R<span id="total">0</span></p>

<label>Delivery Option:</label><br>
<select id="delivery">
<option value="0">Pickup (Free)</option>
<option value="20">Local Delivery (+R20)</option>
</select>

<br><br>
<button onclick="sendWhatsApp()">Order via WhatsApp</button>
</div>

<section>
<h2 class="section-title">Follow Us On Instagram 📸</h2>
<div class="instagram">
<img src="https://images.unsplash.com/photo-1608198093002-ad4e005484ec">
<img src="https://images.unsplash.com/photo-1509440159596-0249088772ff">
<img src="https://images.unsplash.com/photo-1587241321921-91a834d6d191">
</div>
</section>

<footer>
© 2026 TREATS Bakery | Kimberley CBD 💕
</footer>

<script>
const products = [
{name:"Cookies",price:7},
{name:"Doughnuts",price:15},
{name:"Scones",price:15},
{name:"Mini Cakes",price:30},
{name:"Chocolate Eclairs",price:18},
{name:"Malva Pudding",price:28},
{name:"Bread",price:16},
{name:"Fat Cakes",price:8},
{name:"Croissants",price:12},
{name:"Samosas",price:10},
{name:"Puff Pastries",price:10}
];

let cart = [];

const menuDiv = document.getElementById("menu");

products.forEach(product=>{
let card = document.createElement("div");
card.classList.add("card");
card.innerHTML = `
<h3>${product.name}</h3>
<p class="price">R${product.price}</p>
<button onclick="addToCart('${product.name}',${product.price})">Add to Cart</button>
`;
menuDiv.appendChild(card);
});

function addToCart(name,price){
cart.push({name,price});
renderCart();
}

function renderCart(){
let list = document.getElementById("cart-items");
list.innerHTML="";
let total=0;

cart.forEach(item=>{
let li=document.createElement("li");
li.textContent=`${item.name} - R${item.price}`;
list.appendChild(li);
total+=item.price;
});

let deliveryCost=parseInt(document.getElementById("delivery").value);
total+=deliveryCost;

document.getElementById("total").textContent=total;
}

document.getElementById("delivery").addEventListener("change",renderCart);

function sendWhatsApp(){
if(cart.length===0){
alert("Your cart is empty 🛒");
return;
}
let message="Hello TREATS! I'd like to order:%0A";
cart.forEach(item=>{
message+=`${item.name} - R${item.price}%0A`;
});
message+=`Total: R${document.getElementById("total").textContent}`;

window.open(`https://wa.me/0849430677?text=${message}`);
}
</script>

</body>
</html>
