<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>TREATS Bakery | Kimberley CBD</title>

<!-- Google Fonts -->
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600&family=Lobster&display=swap" rel="stylesheet">

<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: 'Poppins', sans-serif;
    background: #fff5f8;
    color: #333;
    scroll-behavior: smooth;
}

/* HEADER */
header {
    position: absolute;
    width: 100%;
    padding: 20px 40px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    z-index: 100;
}

.logo {
    font-family: 'Lobster', cursive;
    font-size: 2.8rem;
    color: #fff;
    letter-spacing: 2px;
    text-shadow: 3px 3px 10px rgba(0,0,0,0.4);
}

nav a {
    color: white;
    text-decoration: none;
    margin-left: 25px;
    font-weight: 500;
    transition: 0.3s;
}

nav a:hover {
    color: #ffe066;
}

.mobile-menu {
    display: none;
    font-size: 1.8rem;
    color: white;
    cursor: pointer;
}

/* HERO SECTION */
.hero {
    height: 100vh;
    background: 
        linear-gradient(rgba(255, 105, 180, 0.6), rgba(255, 140, 0, 0.6)),
        url('https://images.unsplash.com/photo-1509440159596-0249088772ff');
    background-size: cover;
    background-position: center;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    text-align: center;
    color: white;
    padding: 20px;
}

.hero h1 {
    font-family: 'Lobster', cursive;
    font-size: 4rem;
    margin-bottom: 20px;
    text-shadow: 4px 4px 15px rgba(0,0,0,0.5);
}

.hero p {
    font-size: 1.2rem;
    max-width: 650px;
    margin-bottom: 30px;
}

.btn {
    padding: 14px 30px;
    background: #ffe066;
    color: #d63384;
    border-radius: 30px;
    text-decoration: none;
    font-weight: 600;
    transition: 0.3s;
}

.btn:hover {
    background: white;
    transform: scale(1.05);
}

/* SECTIONS */
section {
    padding: 70px 20px;
    text-align: center;
}

.section-title {
    font-size: 2.2rem;
    margin-bottom: 40px;
    color: #d63384;
}

.grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 25px;
    max-width: 1100px;
    margin: auto;
}

.card {
    background: white;
    padding: 25px;
    border-radius: 20px;
    box-shadow: 0 8px 20px rgba(0,0,0,0.08);
    transition: 0.3s;
}

.card:hover {
    transform: translateY(-8px);
}

.card h3 {
    color: #ff6f61;
    margin-bottom: 10px;
}

/* FOOTER */
footer {
    background: linear-gradient(90deg, #ff6f61, #d63384);
    color: white;
    padding: 20px;
    text-align: center;
}

/* MOBILE */
@media(max-width: 768px) {

    nav {
        display: none;
        flex-direction: column;
        background: rgba(0,0,0,0.8);
        position: absolute;
        top: 80px;
        right: 0;
        width: 200px;
        padding: 20px;
    }

    nav.active {
        display: flex;
    }

    nav a {
        margin: 10px 0;
    }

    .mobile-menu {
        display: block;
    }

    .hero h1 {
        font-size: 2.8rem;
    }
}
</style>
</head>

<body>

<header>
    <div class="logo">TREATS 🍰</div>
    <div class="mobile-menu" onclick="toggleMenu()">☰</div>
    <nav id="nav">
        <a href="#about">About</a>
        <a href="#menu">Menu</a>
        <a href="#contact">Contact</a>
    </nav>
</header>

<section class="hero">
    <h1>TREATS</h1>
    <p>Freshly baked sweet and savoury delights in Kimberley CBD. 
    Affordable, unique, and made with love for families, schools and events.</p>
    <a href="#contact" class="btn">Order Now</a>
</section>

<section id="about">
    <h2 class="section-title">Why Choose Us?</h2>
    <div class="grid">
        <div class="card">
            <h3>Affordable Quality</h3>
            <p>High-quality sweet and savoury goods at accessible prices.</p>
        </div>
        <div class="card">
            <h3>Unique Local Flavours</h3>
            <p>Special recipes inspired by Kimberley tastes.</p>
        </div>
        <div class="card">
            <h3>Mobile Stalls</h3>
            <p>Quick access in the CBD for busy lifestyles.</p>
        </div>
        <div class="card">
            <h3>Custom Events</h3>
            <p>Perfect for birthdays, school functions and corporate events.</p>
        </div>
    </div>
</section>

<section id="menu">
    <h2 class="section-title">Our Offerings</h2>
    <div class="grid">
        <div class="card">
            <h3>Sweet Treats 🍩</h3>
            <p>Cakes, cupcakes, cookies and pastries.</p>
        </div>
        <div class="card">
            <h3>Savoury Bakes 🥧</h3>
            <p>Pies, quiches, breads and sandwiches.</p>
        </div>
        <div class="card">
            <h3>Bulk Orders 🎉</h3>
            <p>Supplying schools, events and businesses.</p>
        </div>
    </div>
</section>

<section id="contact">
    <h2 class="section-title">Contact Us</h2>
    <p>📍 Kimberley CBD</p>
    <p>📞 084-943-0677</p>
    <p>📧 info@treatsbakery.co.za</p>
    <a href="#" class="btn">Place an Order</a>
</section>

<footer>
    <p>© 2026 TREATS Bakery | Baked Fresh Daily</p>
</footer>

<script>
function toggleMenu() {
    document.getElementById("nav").classList.toggle("active");
}
</script>

</body>
</html>
