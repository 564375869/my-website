<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <meta name="description" content="Discover stylish and affordable fashion at CS Store. Shop jackets, dresses, hoodies, and more." />
  <title>CS Store - Fashion for All</title>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css" />
  <style>
    html {
      scroll-behavior: smooth;
    }

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: 'Segoe UI', sans-serif;
    }

    body {
      background-color: #f8f8f8;
      color: #333;
    }

    nav {
      background-color: #fff;
      padding: 15px 30px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      box-shadow: 0 2px 5px rgba(0,0,0,0.1);
      position: sticky;
      top: 0;
      z-index: 1000;
    }

    .nav-logo {
      display: flex;
      align-items: center;
    }

    .nav-logo img {
      width: 50px;
      height: 50px;
      margin-right: 10px;
      border-radius: 50%;
    }

    .nav-logo span {
      font-size: 1.5rem;
      font-weight: bold;
      color: #333;
    }

    .nav-links {
      display: flex;
      gap: 25px;
      align-items: center;
    }

    .nav-links a, .nav-links i {
      text-decoration: none;
      color: #333;
      font-weight: 500;
      font-size: 1rem;
      transition: color 0.3s;
    }

    .nav-links a:hover, .nav-links i:hover {
      color: #ff6b6b;
    }

    .menu-toggle {
      display: none;
      font-size: 24px;
      cursor: pointer;
    }

    @media (max-width: 768px) {
      .nav-links {
        display: none;
        flex-direction: column;
        background-color: white;
        position: absolute;
        top: 70px;
        right: 30px;
        padding: 15px;
        box-shadow: 0 4px 8px rgba(0,0,0,0.1);
      }

      .nav-links.active {
        display: flex;
      }

      .menu-toggle {
        display: block;
      }
    }

    .banner {
      background-image: url('blob:https://picsart.com/31282aeb-9309-4c13-ab08-12f38e69a3d0');
      background-size: cover;
      background-position: center;
      height: 80vh;
      display: flex;
      align-items: center;
      justify-content: center;
      position: relative;
      color: white;
      text-align: center;
      padding: 20px;
    }

    .banner::after {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      height: 100%;
      width: 100%;
      background-color: rgba(0, 0, 0, 0.5);
    }

    .banner-content {
      position: relative;
      z-index: 1;
    }

    .banner-logo {
      width: 100px;
      margin-bottom: 20px;
      border-radius: 10px;
      box-shadow: 0 4px 8px rgba(0,0,0,0.4);
    }

    .banner h1 {
      font-size: 3rem;
      margin-bottom: 15px;
    }

    .banner p {
      font-size: 1.3rem;
      margin-bottom: 25px;
    }

    .banner button {
      padding: 12px 25px;
      font-size: 1rem;
      background-color: #ff6b6b;
      color: white;
      border: none;
      border-radius: 5px;
      cursor: pointer;
      transition: background 0.3s;
    }

    .banner button:hover {
      background-color: #e05252;
    }

    .products {
      padding: 60px 20px;
      text-align: center;
    }

    .products h2 {
      font-size: 2.5rem;
      margin-bottom: 40px;
    }

    .product-grid {
      display: flex;
      justify-content: center;
      flex-wrap: wrap;
      gap: 30px;
    }

    .product-card {
      background: white;
      padding: 15px;
      width: 220px;
      border-radius: 8px;
      box-shadow: 0 4px 10px rgba(0,0,0,0.1);
      transition: transform 0.3s;
    }

    .product-card:hover {
      transform: translateY(-5px);
    }

    .product-card img {
      width: 100%;
      border-radius: 6px;
    }

    .product-card h3 {
      margin: 10px 0 5px;
      font-size: 1.2rem;
    }

    .product-card p {
      color: #ff6b6b;
      font-weight: bold;
      margin-bottom: 10px;
    }

    .buy-btn {
      background-color: #333;
      color: white;
      border: none;
      padding: 8px 15px;
      border-radius: 4px;
      cursor: pointer;
      transition: background-color 0.3s;
    }

    .buy-btn:hover {
      background-color: #ff6b6b;
    }

    .contact {
      padding: 60px 20px;
      background-color: #fff;
      text-align: center;
    }

    .contact h2 {
      font-size: 2.5rem;
      margin-bottom: 20px;
    }

    .contact p {
      font-size: 1.2rem;
      margin-bottom: 15px;
    }

    .testimonials {
      background-color: #f2f2f2;
      padding: 50px 20px;
      text-align: center;
    }

    .testimonial-grid {
      display: flex;
      flex-direction: column;
      gap: 20px;
      max-width: 600px;
      margin: auto;
    }

    .testimonial {
      background: white;
      padding: 20px;
      border-radius: 8px;
      box-shadow: 0 4px 10px rgba(0,0,0,0.1);
    }

    footer {
      background-color: #222;
      color: white;
      text-align: center;
      padding: 20px;
    }

    /* WhatsApp floating chat */
    .whatsapp-float {
      position: fixed;
      bottom: 25px;
      right: 25px;
      z-index: 1001;
    }

    .whatsapp-button {
      background-color: #25D366;
      border-radius: 50%;
      width: 60px;
      height: 60px;
      display: flex;
      justify-content: center;
      align-items: center;
      box-shadow: 0 4px 12px rgba(0, 0, 0, 0.2);
      cursor: pointer;
    }

    .whatsapp-button i {
      color: white;
      font-size: 28px;
    }

    .chat-popup {
      display: none;
      position: fixed;
      bottom: 95px;
      right: 25px;
      width: 280px;
      background: white;
      border-radius: 8px;
      box-shadow: 0 8px 20px rgba(0,0,0,0.2);
      padding: 15px;
    }

    .chat-popup.active {
      display: block;
    }

    .chat-popup h4 {
      margin-bottom: 10px;
    }

    .chat-popup p {
      font-size: 0.9rem;
      margin-bottom: 15px;
    }

    .chat-popup a {
      display: inline-block;
      background-color: #25D366;
      color: white;
      text-decoration: none;
      padding: 8px 15px;
      border-radius: 5px;
      font-weight: bold;
    }
  </style>
</head>
<body>

  <!-- Navbar -->
  <nav>
    <div class="nav-logo">
      <img src="https://media1.thehungryjpeg.com/thumbs2/ori_3808926_zdvdz8chwd9v6q0fxmat4dm9hgwyyvlptdew40qm_monogram-sc-logo-design.jpg" alt="SC Logo">
      <span>CS Store</span>
    </div>
    <div class="menu-toggle" onclick="toggleMenu()">☰</div>
    <div class="nav-links" id="navLinks">
      <a href="#">Home</a>
      <a href="#products">Shop</a>
      <a href="#contact">Contact</a>
    </div>
  </nav>

  <!-- Banner -->
  <header class="banner">
    <div class="banner-content">
      <img src="https://media1.thehungryjpeg.com/thumbs2/ori_3808926_zdvdz8chwd9v6q0fxmat4dm9hgwyyvlptdew40qm_monogram-sc-logo-design.jpg"
           alt="SC Store Logo"
           class="banner-logo" />
      <h1>Welcome to CS Store</h1>
      <p>Style That Speaks – Discover Your Look</p>
      <button onclick="scrollToProducts()">Shop Now</button>
    </div>
  </header>

  <!-- Products -->
  <main class="products" id="products">
    <h2>Featured Collection</h2>
    <div class="product-grid">
      <!-- Product Cards -->
      <div class="product-card">
        <img src="https://via.placeholder.com/220x280.png?text=Denim+Jacket" alt="Denim Jacket" loading="lazy">
        <h3>Denim Jacket</h3>
        <p>$59.99</p>
        <button class="buy-btn">Add to Cart</button>
      </div>
      <div class="product-card">
        <img src="https://via.placeholder.com/220x280.png?text=Summer+Dress" alt="Summer Dress" loading="lazy">
        <h3>Summer Dress</h3>
        <p>$45.00</p>
        <button class="buy-btn">Add to Cart</button>
      </div>
      <div class="product-card">
        <img src="https://via.placeholder.com/220x280.png?text=Casual+Shirt" alt="Casual Shirt" loading="lazy">
        <h3>Casual Shirt</h3>
        <p>$29.99</p>
        <button class="buy-btn">Add to Cart</button>
      </div>
      <div class="product-card">
        <img src="https://via.placeholder.com/220x280.png?text=Sports+Hoodie" alt="Sports Hoodie" loading="lazy">
        <h3>Sports Hoodie</h3>
        <p>$39.99</p>
        <button class="buy-btn">Add to Cart</button>
      </div>
    </div>
  </main>

  <!-- Testimonials -->
  <section class="testimonials">
    <h2>What Our Customers Say</h2>
    <div class="testimonial-grid">
      <div class="testimonial">
        <p>"Amazing quality and fast delivery!"</p>
        <span>- Sarah A.</span>
      </div>
      <div class="testimonial">
        <p>"Love the summer dress! Will shop again."</p>
        <span>- Jamal R.</span>
      </div>
    </div>
  </section>

  <!-- Contact Section -->
  <section class="contact" id="contact">
    <h2>Contact Us</h2>
    <p>Phone: 0335-9077447</p>
  </section>

  <!-- WhatsApp Floating Chat -->
  <div class="whatsapp-float">
    <div class="whatsapp-button" onclick="toggleChat()">
      <i class="fab fa-whatsapp"></i>
    </div>
    <div class="chat-popup" id="chatPopup">
      <h4>Need Help?</h4>
      <p>Chat with our team on WhatsApp.</p>
      <a href="https://wa.me/923359077447" target="_blank">Start Chat</a>
    </div>
  </div>

  <!-- Footer -->
  <footer>
    <p>&copy; 2025 CS Store. All rights reserved.</p>
  </footer>

  <!-- JS -->
  <script>
    function scrollToProducts() {
      document.getElementById('products').scrollIntoView({ behavior: 'smooth' });
    }

    function toggleMenu() {
      document.getElementById('navLinks').classList.toggle('active');
    }

    function toggleChat() {
      document.getElementById('chatPopup').classList.toggle('active');
    }
  </script>

</body>
</html>
