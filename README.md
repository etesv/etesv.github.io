<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Shreya Collections - Exquisite Jewelry</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:wght@300;400;600;700&family=Montserrat:wght@300;400;500;600&display=swap" rel="stylesheet">
    <style>
        :root {
            --gold: #D4AF37;
            --dark-gold: #B8941E;
            --cream: #FAF7F2;
            --dark: #1a1a1a;
            --gray: #6B6B6B;
            --light-gray: #E8E8E8;
            --white: #FFFFFF;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Montserrat', sans-serif;
            background-color: var(--cream);
            color: var(--dark);
            line-height: 1.6;
            overflow-x: hidden;
        }

        /* Header & Navigation */
        header {
            position: fixed;
            top: 0;
            width: 100%;
            background: rgba(250, 247, 242, 0.95);
            backdrop-filter: blur(10px);
            z-index: 1000;
            border-bottom: 1px solid rgba(212, 175, 55, 0.2);
            animation: slideDown 0.6s ease;
        }

        @keyframes slideDown {
            from {
                transform: translateY(-100%);
                opacity: 0;
            }
            to {
                transform: translateY(0);
                opacity: 1;
            }
        }

        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 1.5rem 5%;
            max-width: 1400px;
            margin: 0 auto;
        }

        .logo {
            font-family: 'Cormorant Garamond', serif;
            font-size: 2rem;
            font-weight: 700;
            color: var(--dark);
            letter-spacing: 2px;
            position: relative;
        }

        .logo::after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 40px;
            height: 2px;
            background: var(--gold);
        }

        .nav-links {
            display: flex;
            gap: 2.5rem;
            list-style: none;
            align-items: center;
        }

        .nav-links a {
            text-decoration: none;
            color: var(--dark);
            font-weight: 400;
            font-size: 0.9rem;
            letter-spacing: 1px;
            text-transform: uppercase;
            transition: color 0.3s;
            position: relative;
        }

        .nav-links a::after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 0;
            height: 1px;
            background: var(--gold);
            transition: width 0.3s;
        }

        .nav-links a:hover::after {
            width: 100%;
        }

        .nav-links a:hover {
            color: var(--gold);
        }

        .cart-icon {
            cursor: pointer;
            position: relative;
        }

        .cart-count {
            position: absolute;
            top: -8px;
            right: -8px;
            background: var(--gold);
            color: var(--white);
            border-radius: 50%;
            width: 20px;
            height: 20px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 0.7rem;
            font-weight: 600;
        }

        /* Hero Section */
        .hero {
            margin-top: 80px;
            height: 90vh;
            background: linear-gradient(135deg, rgba(212, 175, 55, 0.1) 0%, rgba(250, 247, 242, 1) 100%);
            display: flex;
            align-items: center;
            justify-content: center;
            position: relative;
            overflow: hidden;
        }

        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            right: 0;
            width: 50%;
            height: 100%;
            background: url('data:image/svg+xml,<svg width="100" height="100" xmlns="http://www.w3.org/2000/svg"><defs><pattern id="grid" width="50" height="50" patternUnits="userSpaceOnUse"><path d="M 50 0 L 0 0 0 50" fill="none" stroke="rgba(212,175,55,0.1)" stroke-width="0.5"/></pattern></defs><rect width="100" height="100" fill="url(%23grid)"/></svg>');
            opacity: 0.3;
        }

        .hero-content {
            text-align: center;
            max-width: 800px;
            padding: 0 2rem;
            animation: fadeInUp 1s ease;
            z-index: 1;
        }

        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .hero h1 {
            font-family: 'Cormorant Garamond', serif;
            font-size: 5rem;
            font-weight: 300;
            color: var(--dark);
            margin-bottom: 1rem;
            line-height: 1.2;
            letter-spacing: 3px;
        }

        .hero h1 span {
            font-weight: 700;
            color: var(--gold);
            display: block;
        }

        .hero p {
            font-size: 1.1rem;
            color: var(--gray);
            margin-bottom: 2.5rem;
            letter-spacing: 1px;
        }

        .btn-primary {
            display: inline-block;
            padding: 1rem 3rem;
            background: var(--gold);
            color: var(--white);
            text-decoration: none;
            font-weight: 500;
            letter-spacing: 2px;
            text-transform: uppercase;
            transition: all 0.3s;
            border: 2px solid var(--gold);
            cursor: pointer;
            font-size: 0.9rem;
        }

        .btn-primary:hover {
            background: transparent;
            color: var(--gold);
            transform: translateY(-2px);
            box-shadow: 0 10px 30px rgba(212, 175, 55, 0.3);
        }

        /* Category Section */
        .categories {
            padding: 6rem 5%;
            max-width: 1400px;
            margin: 0 auto;
        }

        .section-title {
            text-align: center;
            margin-bottom: 4rem;
        }

        .section-title h2 {
            font-family: 'Cormorant Garamond', serif;
            font-size: 3rem;
            font-weight: 600;
            color: var(--dark);
            margin-bottom: 1rem;
            letter-spacing: 2px;
        }

        .section-title p {
            color: var(--gray);
            font-size: 1rem;
            letter-spacing: 1px;
        }

        .category-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }

        .category-card {
            position: relative;
            height: 400px;
            overflow: hidden;
            cursor: pointer;
            border: 1px solid var(--light-gray);
            transition: transform 0.5s;
        }

        .category-card:hover {
            transform: translateY(-10px);
        }

        .category-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(to bottom, transparent 0%, rgba(26, 26, 26, 0.7) 100%);
            z-index: 1;
            transition: opacity 0.3s;
        }

        .category-card:hover::before {
            opacity: 0.9;
        }

        .category-img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s;
        }

        .category-card:hover .category-img {
            transform: scale(1.1);
        }

        .category-info {
            position: absolute;
            bottom: 0;
            left: 0;
            right: 0;
            padding: 2rem;
            z-index: 2;
            color: var(--white);
        }

        .category-info h3 {
            font-family: 'Cormorant Garamond', serif;
            font-size: 2rem;
            margin-bottom: 0.5rem;
            letter-spacing: 2px;
        }

        .category-info p {
            font-size: 0.9rem;
            opacity: 0.9;
        }

        /* Products Section */
        .products {
            padding: 6rem 5%;
            background: var(--white);
        }

        .product-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
            gap: 3rem;
            max-width: 1400px;
            margin: 0 auto;
        }

        .product-card {
            background: var(--cream);
            border: 1px solid var(--light-gray);
            transition: all 0.4s;
            position: relative;
            overflow: hidden;
            opacity: 0;
            animation: fadeIn 0.6s forwards;
        }

        @keyframes fadeIn {
            to {
                opacity: 1;
            }
        }

        .product-card:nth-child(1) { animation-delay: 0.1s; }
        .product-card:nth-child(2) { animation-delay: 0.2s; }
        .product-card:nth-child(3) { animation-delay: 0.3s; }
        .product-card:nth-child(4) { animation-delay: 0.4s; }
        .product-card:nth-child(5) { animation-delay: 0.5s; }
        .product-card:nth-child(6) { animation-delay: 0.6s; }

        .product-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 40px rgba(0, 0, 0, 0.1);
        }

        .product-image {
            width: 100%;
            height: 350px;
            background: var(--white);
            display: flex;
            align-items: center;
            justify-content: center;
            overflow: hidden;
            position: relative;
        }

        .product-image img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s;
        }

        .product-card:hover .product-image img {
            transform: scale(1.05);
        }

        .product-badge {
            position: absolute;
            top: 15px;
            right: 15px;
            background: var(--gold);
            color: var(--white);
            padding: 0.4rem 1rem;
            font-size: 0.75rem;
            font-weight: 600;
            letter-spacing: 1px;
            text-transform: uppercase;
        }

        .product-info {
            padding: 1.5rem;
        }

        .product-info h3 {
            font-family: 'Cormorant Garamond', serif;
            font-size: 1.5rem;
            margin-bottom: 0.5rem;
            color: var(--dark);
            font-weight: 600;
        }

        .product-info p {
            color: var(--gray);
            font-size: 0.9rem;
            margin-bottom: 1rem;
        }

        .product-price {
            display: flex;
            align-items: center;
            justify-content: space-between;
            margin-bottom: 1rem;
        }

        .price {
            font-size: 1.5rem;
            font-weight: 600;
            color: var(--gold);
            font-family: 'Cormorant Garamond', serif;
        }

        .old-price {
            text-decoration: line-through;
            color: var(--gray);
            font-size: 1rem;
            margin-left: 0.5rem;
        }

        .btn-add-cart {
            width: 100%;
            padding: 1rem;
            background: var(--dark);
            color: var(--white);
            border: 2px solid var(--dark);
            cursor: pointer;
            font-weight: 500;
            letter-spacing: 1px;
            text-transform: uppercase;
            transition: all 0.3s;
            font-size: 0.85rem;
        }

        .btn-add-cart:hover {
            background: transparent;
            color: var(--dark);
        }

        /* Features Section */
        .features {
            padding: 6rem 5%;
            background: var(--cream);
        }

        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 3rem;
            max-width: 1400px;
            margin: 0 auto;
        }

        .feature-item {
            text-align: center;
            padding: 2rem;
        }

        .feature-icon {
            font-size: 3rem;
            color: var(--gold);
            margin-bottom: 1rem;
        }

        .feature-item h3 {
            font-family: 'Cormorant Garamond', serif;
            font-size: 1.5rem;
            margin-bottom: 0.5rem;
            color: var(--dark);
        }

        .feature-item p {
            color: var(--gray);
            font-size: 0.9rem;
        }

        /* Newsletter */
        .newsletter {
            padding: 5rem 5%;
            background: var(--dark);
            color: var(--white);
            text-align: center;
        }

        .newsletter h2 {
            font-family: 'Cormorant Garamond', serif;
            font-size: 2.5rem;
            margin-bottom: 1rem;
            letter-spacing: 2px;
        }

        .newsletter p {
            margin-bottom: 2rem;
            opacity: 0.9;
        }

        .newsletter-form {
            display: flex;
            max-width: 600px;
            margin: 0 auto;
            gap: 1rem;
        }

        .newsletter-form input {
            flex: 1;
            padding: 1rem 1.5rem;
            border: 2px solid var(--gold);
            background: transparent;
            color: var(--white);
            font-size: 1rem;
            outline: none;
        }

        .newsletter-form input::placeholder {
            color: rgba(255, 255, 255, 0.6);
        }

        .newsletter-form button {
            padding: 1rem 2.5rem;
            background: var(--gold);
            border: 2px solid var(--gold);
            color: var(--white);
            cursor: pointer;
            font-weight: 600;
            letter-spacing: 1px;
            text-transform: uppercase;
            transition: all 0.3s;
        }

        .newsletter-form button:hover {
            background: transparent;
            color: var(--gold);
        }

        /* Footer */
        footer {
            background: var(--dark);
            color: var(--white);
            padding: 4rem 5% 2rem;
        }

        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 3rem;
            max-width: 1400px;
            margin: 0 auto 3rem;
        }

        .footer-section h3 {
            font-family: 'Cormorant Garamond', serif;
            font-size: 1.5rem;
            margin-bottom: 1.5rem;
            color: var(--gold);
        }

        .footer-section ul {
            list-style: none;
        }

        .footer-section ul li {
            margin-bottom: 0.8rem;
        }

        .footer-section ul li a {
            color: rgba(255, 255, 255, 0.8);
            text-decoration: none;
            transition: color 0.3s;
            font-size: 0.9rem;
        }

        .footer-section ul li a:hover {
            color: var(--gold);
        }

        .footer-bottom {
            text-align: center;
            padding-top: 2rem;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            color: rgba(255, 255, 255, 0.6);
            font-size: 0.9rem;
        }

        /* Cart Modal */
        .cart-modal {
            display: none;
            position: fixed;
            top: 0;
            right: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.7);
            z-index: 2000;
        }

        .cart-modal.active {
            display: block;
            animation: fadeIn 0.3s;
        }

        .cart-content {
            position: absolute;
            top: 0;
            right: 0;
            width: 450px;
            height: 100%;
            background: var(--white);
            padding: 2rem;
            overflow-y: auto;
            animation: slideInRight 0.4s;
        }

        @keyframes slideInRight {
            from {
                transform: translateX(100%);
            }
            to {
                transform: translateX(0);
            }
        }

        .cart-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 2rem;
            padding-bottom: 1rem;
            border-bottom: 2px solid var(--light-gray);
        }

        .cart-header h2 {
            font-family: 'Cormorant Garamond', serif;
            font-size: 2rem;
            color: var(--dark);
        }

        .close-cart {
            font-size: 2rem;
            cursor: pointer;
            color: var(--dark);
            border: none;
            background: none;
        }

        .cart-items {
            margin-bottom: 2rem;
        }

        .cart-item {
            display: flex;
            gap: 1rem;
            margin-bottom: 1.5rem;
            padding-bottom: 1.5rem;
            border-bottom: 1px solid var(--light-gray);
        }

        .cart-item img {
            width: 80px;
            height: 80px;
            object-fit: cover;
        }

        .cart-item-info {
            flex: 1;
        }

        .cart-item-info h4 {
            font-family: 'Cormorant Garamond', serif;
            font-size: 1.1rem;
            margin-bottom: 0.3rem;
        }

        .cart-item-price {
            color: var(--gold);
            font-weight: 600;
        }

        .remove-item {
            color: var(--gray);
            cursor: pointer;
            font-size: 0.85rem;
            text-decoration: underline;
            border: none;
            background: none;
            padding: 0;
        }

        .cart-total {
            margin-top: 2rem;
            padding-top: 1rem;
            border-top: 2px solid var(--dark);
        }

        .cart-total h3 {
            display: flex;
            justify-content: space-between;
            font-family: 'Cormorant Garamond', serif;
            font-size: 1.8rem;
            margin-bottom: 1.5rem;
        }

        .btn-checkout {
            width: 100%;
            padding: 1.2rem;
            background: var(--gold);
            color: var(--white);
            border: none;
            cursor: pointer;
            font-weight: 600;
            letter-spacing: 2px;
            text-transform: uppercase;
            transition: all 0.3s;
            font-size: 1rem;
        }

        .btn-checkout:hover {
            background: var(--dark-gold);
            transform: translateY(-2px);
            box-shadow: 0 10px 30px rgba(212, 175, 55, 0.3);
        }

        .empty-cart {
            text-align: center;
            padding: 3rem 0;
            color: var(--gray);
        }

        /* Responsive */
        @media (max-width: 768px) {
            .nav-links {
                gap: 1rem;
            }

            .nav-links a {
                font-size: 0.8rem;
            }

            .hero h1 {
                font-size: 3rem;
            }

            .hero p {
                font-size: 1rem;
            }

            .section-title h2 {
                font-size: 2rem;
            }

            .product-grid {
                grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
                gap: 2rem;
            }

            .cart-content {
                width: 100%;
            }

            .newsletter-form {
                flex-direction: column;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <nav>
            <div class="logo">SHREYA</div>
            <ul class="nav-links">
                <li><a href="#home">Home</a></li>
                <li><a href="#categories">Collections</a></li>
                <li><a href="#products">Shop</a></li>
                <li><a href="#about">About</a></li>
                <li class="cart-icon" onclick="toggleCart()">
                    🛍️
                    <span class="cart-count">0</span>
                </li>
            </ul>
        </nav>
    </header>

    <!-- Hero Section -->
    <section class="hero" id="home">
        <div class="hero-content">
            <h1>
                Timeless Elegance
                <span>Crafted for You</span>
            </h1>
            <p>Discover exquisite handcrafted jewelry that tells your story</p>
            <a href="#products" class="btn-primary">Explore Collection</a>
        </div>
    </section>

    <!-- Categories Section -->
    <section class="categories" id="categories">
        <div class="section-title">
            <h2>Our Collections</h2>
            <p>Explore our curated selection of fine jewelry</p>
        </div>
        <div class="category-grid">
            <div class="category-card">
                <img src="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='400' height='400'%3E%3Crect fill='%23f5e6d3' width='400' height='400'/%3E%3Ctext x='50%25' y='50%25' dominant-baseline='middle' text-anchor='middle' font-family='serif' font-size='24' fill='%23D4AF37'%3ENecklaces%3C/text%3E%3C/svg%3E" alt="Necklaces" class="category-img">
                <div class="category-info">
                    <h3>Necklaces</h3>
                    <p>Statement pieces that captivate</p>
                </div>
            </div>
            <div class="category-card">
                <img src="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='400' height='400'%3E%3Crect fill='%23e8d4c0' width='400' height='400'/%3E%3Ctext x='50%25' y='50%25' dominant-baseline='middle' text-anchor='middle' font-family='serif' font-size='24' fill='%23D4AF37'%3ERings%3C/text%3E%3C/svg%3E" alt="Rings" class="category-img">
                <div class="category-info">
                    <h3>Rings</h3>
                    <p>Symbols of eternal beauty</p>
                </div>
            </div>
            <div class="category-card">
                <img src="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='400' height='400'%3E%3Crect fill='%23dcc7b0' width='400' height='400'/%3E%3Ctext x='50%25' y='50%25' dominant-baseline='middle' text-anchor='middle' font-family='serif' font-size='24' fill='%23D4AF37'%3EEarrings%3C/text%3E%3C/svg%3E" alt="Earrings" class="category-img">
                <div class="category-info">
                    <h3>Earrings</h3>
                    <p>Elegance in every detail</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Products Section -->
    <section class="products" id="products">
        <div class="section-title">
            <h2>Featured Collection</h2>
            <p>Handpicked pieces for the discerning connoisseur</p>
        </div>
        <div class="product-grid" id="productGrid">
            <!-- Products will be dynamically loaded -->
        </div>
    </section>

    <!-- Features Section -->
    <section class="features" id="about">
        <div class="features-grid">
            <div class="feature-item">
                <div class="feature-icon">✨</div>
                <h3>Premium Quality</h3>
                <p>Each piece crafted with finest materials and exceptional attention to detail</p>
            </div>
            <div class="feature-item">
                <div class="feature-icon">🚚</div>
                <h3>Free Shipping</h3>
                <p>Complimentary delivery on all orders above ₹5,000</p>
            </div>
            <div class="feature-item">
                <div class="feature-icon">🔒</div>
                <h3>Secure Payment</h3>
                <p>Safe and encrypted transactions for your peace of mind</p>
            </div>
            <div class="feature-item">
                <div class="feature-icon">💎</div>
                <h3>Lifetime Warranty</h3>
                <p>Comprehensive coverage on all our jewelry pieces</p>
            </div>
        </div>
    </section>

    <!-- Newsletter Section -->
    <section class="newsletter">
        <h2>Join Our Exclusive Circle</h2>
        <p>Be the first to discover new collections and receive special offers</p>
        <form class="newsletter-form" onsubmit="subscribeNewsletter(event)">
            <input type="email" placeholder="Enter your email address" required>
            <button type="submit">Subscribe</button>
        </form>
    </section>

    <!-- Footer -->
    <footer>
        <div class="footer-content">
            <div class="footer-section">
                <h3>Shreya Collections</h3>
                <p>Crafting timeless elegance since 2010. Each piece tells a story of artistry, passion, and unparalleled beauty.</p>
            </div>
            <div class="footer-section">
                <h3>Quick Links</h3>
                <ul>
                    <li><a href="#home">Home</a></li>
                    <li><a href="#categories">Collections</a></li>
                    <li><a href="#products">Shop</a></li>
                    <li><a href="#about">About Us</a></li>
                </ul>
            </div>
            <div class="footer-section">
                <h3>Customer Care</h3>
                <ul>
                    <li><a href="#">Contact Us</a></li>
                    <li><a href="#">Shipping Info</a></li>
                    <li><a href="#">Returns</a></li>
                    <li><a href="#">Size Guide</a></li>
                </ul>
            </div>
            <div class="footer-section">
                <h3>Connect With Us</h3>
                <ul>
                    <li><a href="#">Instagram</a></li>
                    <li><a href="#">Facebook</a></li>
                    <li><a href="#">Pinterest</a></li>
                    <li><a href="#">Twitter</a></li>
                </ul>
            </div>
        </div>
        <div class="footer-bottom">
            <p>&copy; 2024 Shreya Collections. All rights reserved. Crafted with ♥</p>
        </div>
    </footer>

    <!-- Cart Modal -->
    <div class="cart-modal" id="cartModal" onclick="closeCartOnOutside(event)">
        <div class="cart-content" onclick="event.stopPropagation()">
            <div class="cart-header">
                <h2>Shopping Bag</h2>
                <button class="close-cart" onclick="toggleCart()">&times;</button>
            </div>
            <div class="cart-items" id="cartItems">
                <div class="empty-cart">
                    <p>Your shopping bag is empty</p>
                </div>
            </div>
            <div class="cart-total" id="cartTotal" style="display: none;">
                <h3>
                    <span>Total:</span>
                    <span id="totalAmount">₹0</span>
                </h3>
                <button class="btn-checkout" onclick="checkout()">Proceed to Checkout</button>
            </div>
        </div>
    </div>

    <script>
        // Product Data
        const products = [
            {
                id: 1,
                name: "Diamond Solitaire Ring",
                description: "18K white gold with 1ct diamond",
                price: 45000,
                oldPrice: 52000,
                image: "data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='400' height='400'%3E%3Crect fill='%23ffffff' width='400' height='400'/%3E%3Ccircle cx='200' cy='200' r='80' fill='none' stroke='%23D4AF37' stroke-width='3'/%3E%3Cpolygon points='200,140 220,180 180,180' fill='%23D4AF37'/%3E%3Ctext x='50%25' y='85%25' dominant-baseline='middle' text-anchor='middle' font-family='serif' font-size='16' fill='%23666'%3EDiamond Ring%3C/text%3E%3C/svg%3E",
                badge: "Bestseller"
            },
            {
                id: 2,
                name: "Pearl Drop Earrings",
                description: "Freshwater pearls in gold setting",
                price: 12500,
                oldPrice: null,
                image: "data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='400' height='400'%3E%3Crect fill='%23ffffff' width='400' height='400'/%3E%3Ccircle cx='200' cy='180' r='30' fill='%23f5f5f5' stroke='%23D4AF37' stroke-width='2'/%3E%3Cline x1='200' y1='150' x2='200' y2='120' stroke='%23D4AF37' stroke-width='2'/%3E%3Ctext x='50%25' y='85%25' dominant-baseline='middle' text-anchor='middle' font-family='serif' font-size='16' fill='%23666'%3EPearl Earrings%3C/text%3E%3C/svg%3E",
                badge: null
            },
            {
                id: 3,
                name: "Gold Chain Necklace",
                description: "22K gold delicate chain",
                price: 35000,
                oldPrice: 38000,
                image: "data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='400' height='400'%3E%3Crect fill='%23ffffff' width='400' height='400'/%3E%3Cellipse cx='200' cy='200' rx='100' ry='120' fill='none' stroke='%23D4AF37' stroke-width='4'/%3E%3Ctext x='50%25' y='85%25' dominant-baseline='middle' text-anchor='middle' font-family='serif' font-size='16' fill='%23666'%3EGold Necklace%3C/text%3E%3C/svg%3E",
                badge: "New"
            },
            {
                id: 4,
                name: "Emerald Pendant Set",
                description: "Natural emerald with gold chain",
                price: 28000,
                oldPrice: null,
                image: "data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='400' height='400'%3E%3Crect fill='%23ffffff' width='400' height='400'/%3E%3Crect x='175' y='180' width='50' height='50' fill='%2350C878' stroke='%23D4AF37' stroke-width='2'/%3E%3Cline x1='200' y1='180' x2='200' y2='140' stroke='%23D4AF37' stroke-width='2'/%3E%3Ctext x='50%25' y='85%25' dominant-baseline='middle' text-anchor='middle' font-family='serif' font-size='16' fill='%23666'%3EEmerald Pendant%3C/text%3E%3C/svg%3E",
                badge: null
            },
            {
                id: 5,
                name: "Ruby Studded Bangles",
                description: "Pair of gold bangles with rubies",
                price: 42000,
                oldPrice: 48000,
                image: "data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='400' height='400'%3E%3Crect fill='%23ffffff' width='400' height='400'/%3E%3Ccircle cx='200' cy='200' r='90' fill='none' stroke='%23D4AF37' stroke-width='8'/%3E%3Ccircle cx='200' cy='140' r='8' fill='%23E0115F'/%3E%3Ccircle cx='260' cy='200' r='8' fill='%23E0115F'/%3E%3Ctext x='50%25' y='85%25' dominant-baseline='middle' text-anchor='middle' font-family='serif' font-size='16' fill='%23666'%3ERuby Bangles%3C/text%3E%3C/svg%3E",
                badge: "Sale"
            },
            {
                id: 6,
                name: "Platinum Band Ring",
                description: "Classic platinum wedding band",
                price: 32000,
                oldPrice: null,
                image: "data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='400' height='400'%3E%3Crect fill='%23ffffff' width='400' height='400'/%3E%3Ccircle cx='200' cy='200' r='80' fill='none' stroke='%23D4AF37' stroke-width='6'/%3E%3Ctext x='50%25' y='85%25' dominant-baseline='middle' text-anchor='middle' font-family='serif' font-size='16' fill='%23666'%3EPlatinum Band%3C/text%3E%3C/svg%3E",
                badge: null
            }
        ];

        // Cart state
        let cart = [];

        // Initialize products
        function initProducts() {
            const productGrid = document.getElementById('productGrid');
            productGrid.innerHTML = products.map(product => `
                <div class="product-card">
                    <div class="product-image">
                        <img src="${product.image}" alt="${product.name}">
                        ${product.badge ? `<div class="product-badge">${product.badge}</div>` : ''}
                    </div>
                    <div class="product-info">
                        <h3>${product.name}</h3>
                        <p>${product.description}</p>
                        <div class="product-price">
                            <div>
                                <span class="price">₹${product.price.toLocaleString()}</span>
                                ${product.oldPrice ? `<span class="old-price">₹${product.oldPrice.toLocaleString()}</span>` : ''}
                            </div>
                        </div>
                        <button class="btn-add-cart" onclick="addToCart(${product.id})">Add to Cart</button>
                    </div>
                </div>
            `).join('');
        }

        // Add to cart
        function addToCart(productId) {
            const product = products.find(p => p.id === productId);
            const existingItem = cart.find(item => item.id === productId);
            
            if (existingItem) {
                existingItem.quantity++;
            } else {
                cart.push({ ...product, quantity: 1 });
            }
            
            updateCart();
            showNotification('Added to cart!');
        }

        // Remove from cart
        function removeFromCart(productId) {
            cart = cart.filter(item => item.id !== productId);
            updateCart();
        }

        // Update cart display
        function updateCart() {
            const cartCount = document.querySelector('.cart-count');
            const cartItems = document.getElementById('cartItems');
            const cartTotal = document.getElementById('cartTotal');
            const totalAmount = document.getElementById('totalAmount');
            
            const totalItems = cart.reduce((sum, item) => sum + item.quantity, 0);
            cartCount.textContent = totalItems;
            
            if (cart.length === 0) {
                cartItems.innerHTML = '<div class="empty-cart"><p>Your shopping bag is empty</p></div>';
                cartTotal.style.display = 'none';
            } else {
                const total = cart.reduce((sum, item) => sum + (item.price * item.quantity), 0);
                
                cartItems.innerHTML = cart.map(item => `
                    <div class="cart-item">
                        <img src="${item.image}" alt="${item.name}">
                        <div class="cart-item-info">
                            <h4>${item.name}</h4>
                            <p class="cart-item-price">₹${item.price.toLocaleString()} × ${item.quantity}</p>
                            <button class="remove-item" onclick="removeFromCart(${item.id})">Remove</button>
                        </div>
                    </div>
                `).join('');
                
                totalAmount.textContent = `₹${total.toLocaleString()}`;
                cartTotal.style.display = 'block';
            }
        }

        // Toggle cart
        function toggleCart() {
            const cartModal = document.getElementById('cartModal');
            cartModal.classList.toggle('active');
        }

        // Close cart when clicking outside
        function closeCartOnOutside(event) {
            if (event.target.id === 'cartModal') {
                toggleCart();
            }
        }

        // Checkout
        function checkout() {
            if (cart.length === 0) {
                alert('Your cart is empty!');
                return;
            }
            alert('Thank you for shopping with Shreya Collections! Proceeding to checkout...');
            // Here you would integrate with a payment gateway
        }

        // Newsletter subscription
        function subscribeNewsletter(event) {
            event.preventDefault();
            const email = event.target.querySelector('input').value;
            alert(`Thank you for subscribing! We'll send updates to ${email}`);
            event.target.reset();
        }

        // Show notification
        function showNotification(message) {
            const notification = document.createElement('div');
            notification.style.cssText = `
                position: fixed;
                bottom: 30px;
                right: 30px;
                background: var(--gold);
                color: var(--white);
                padding: 1rem 2rem;
                border-radius: 5px;
                font-weight: 600;
                z-index: 3000;
                animation: slideInUp 0.3s ease;
            `;
            notification.textContent = message;
            document.body.appendChild(notification);
            
            setTimeout(() => {
                notification.style.animation = 'fadeOut 0.3s ease';
                setTimeout(() => notification.remove(), 300);
            }, 2000);
        }

        // Smooth scrolling
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({ behavior: 'smooth', block: 'start' });
                }
            });
        });

        // Initialize on load
        window.addEventListener('load', initProducts);
    </script>
</body>
</html>
