<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>TREATS Bakery | Kimberley CBD</title>
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">

<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Poppins', sans-serif;
}

body {
    background: #fff8f0;
    color: #333;
    scroll-behavior: smooth;
}

header {
    background: linear-gradient(135deg, #ff7b54, #ffb26b);
    color: white;
    padding: 20px 40px;
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.logo {
    font-size: 1.8rem;
    font-weight: 700;
}

nav a {
    color: white;
    text-decoration: none;
    margin-left: 20px;
    font-weight: 500;
}

nav a:hover {
    text-decoration: underline;
}

.hero {
    text-align: center;
    padding: 80px 20px;
    background: #fff;
}

.hero h1 {
    font-size: 2.5rem;
    color: #ff7b54;
}

.hero p {
    margin-top: 20px;
    font-size: 1.1rem;
    max-width: 600px;
    margin-left: auto;
    margin-right: auto;
}

.btn {
    display: inline-block;
    margin-top: 30px;
    padding: 12px 25px;
    background: #ff7b54;
    color: white;
    border-radius: 25px;
    text-decoration: none;
    font-weight: 600;
    transition: 0.3s;
}

.btn:hover {
    background: #ff5722;
}

section {
    padding: 60px 20px;
    text-align: center;
}

.section-title {
    font-size: 2rem;
    margin-bottom: 30px;
    color: #ff7b54;
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
    border-radius: 15px;
    box-shadow: 0 5px 15px rgba(0,0,0,0.08);
    transition: 0.3s;
}

.card:hover {
    transform: translateY(-5px);
}

.card h3 {
    color: #ff7b54;
    margin-bottom: 10px;
}

.footer {
    background: #ff7b54;
    color: white;
    padding: 20px;
    text-align: center;
}

.mobile-menu {
    display: none;
    font-size: 1.5rem;
    cursor: pointer;
}

@media(max-width: 768px) {
    nav {
        display: none;
        flex-direction: column;
        background: #ff7b54;
        position: absolute;
        top: 70px;
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
        <a href="#customers">Customers</a>
        <a href="#contact">Contact</a>
    </nav>
</header>

<section class="hero">
    <h1>Fresh. Affordable. Delicious.</h1>
    <p>Serving Kimberley CBD with high-quality sweet and savoury treats made with love. 
       Quick service, unique flavours, and convenient mobile stalls for busy lifestyles.</p>
    <a href="#contact" class="btn">Order Now</a>
</section>

<section id="about">
    <h2 class="section-title">Why Choose TREATS?</h2>
    <div class="grid">
        <div class="card">
            <h3>Affordable Quality</h3>
            <p>Freshly baked sweet and savoury goods at prices families and schools can afford.</p>
        </div>
        <div class="card">
            <h3>Unique Local Flavours</h3>
            <p>Special recipes inspired by Kimberley’s tastes and preferences.</p>
        </div>
        <div class="card">
            <h3>Convenient Access</h3>
            <p>Storefront in CBD plus mobile stalls for quick and easy purchases.</p>
        </div>
        <div class="card">
            <h3>Experienced Baker</h3>
            <p>Highly skilled baker with proven experience and strong community ties.</p>
        </div>
    </div>
</section>

<section id="menu" style="background:#fff;">
    <h2 class="section-title">Our Offerings</h2>
    <div class="grid">
        <div class="card">
            <h3>Sweet Treats</h3>
            <p>Cakes, cupcakes, cookies, pastries and more.</p>
        </div>
        <div class="card">
            <h3>Savoury Goods</h3>
            <p>Pies, quiches, sandwiches and freshly baked breads.</p>
        </div>
        <div class="card">
            <h3>Custom Event Orders</h3>
            <p>Perfect for birthdays, school events and corporate functions.</p>
        </div>
        <div class="card">
            <h3>Business & School Supply</h3>
            <p>Bulk supply options for local businesses and schools.</p>
        </div>
    </div>
</section>

<section id="customers">
    <h2 class="section-title">Who We Serve</h2>
    <div class="grid">
        <div class="card">
            <h3>Families</h3>
        </div>
        <div class="card">
            <h3>Event Planners</h3>
        </div>
        <div class="card">
            <h3>Local Residents</h3>
        </div>
        <div class="card">
            <h3>Schools</h3>
        </div>
    </div>
</section>

<section id="contact" style="background:#fff;">
    <h2 class="section-title">Contact Us</h2>
    <p>📍 Kimberley CBD</p>
    <p>📱 Call/WhatsApp: 000-000-0000</p>
    <p>📧 Email: info@treatsbakery.co.za</p>
    <a href="#" class="btn">Place an Order</a>
</section>

<footer class="footer">
    <p>© 2026 TREATS Bakery | Freshly Baked in Kimberley</p>
</footer>

<script>
function toggleMenu() {
    document.getElementById("nav").classList.toggle("active");
}
</script>

</body>
</html>
