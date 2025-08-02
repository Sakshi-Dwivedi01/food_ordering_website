<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Gourmet Express - Food Delivery</title>
    <style>
        /* Global Styles */
        :root {
            --primary: #ff6b6b;
            --secondary: #4ecdc4;
            --dark: #292f36;
            --light: #f7fff7;
            --accent: #ffd166;
            --shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            background-color: var(--light);
            color: var(--dark);
            line-height: 1.6;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* Header */
        header {
            background-color: white;
            box-shadow: var(--shadow);
            position: sticky;
            top: 0;
            z-index: 100;
        }

        .navbar {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 1.5rem 0;
        }

        .logo {
            display: flex;
            align-items: center;
            font-size: 1.8rem;
            font-weight: 700;
            color: var(--primary);
        }

        .logo img {
            margin-right: 10px;
        }

        .nav-links {
            display: flex;
            gap: 2rem;
        }

        .nav-links a {
            text-decoration: none;
            color: var(--dark);
            font-weight: 500;
            transition: color 0.3s;
        }

        .nav-links a:hover {
            color: var(--primary);
        }

        .cart-btn {
            background-color: var(--primary);
            color: white;
            border: none;
            padding: 0.5rem 1rem;
            border-radius: 5px;
            display: flex;
            align-items: center;
            gap: 5px;
            cursor: pointer;
            transition: background-color 0.3s;
        }

        .cart-btn:hover {
            background-color: #ff5252;
        }

        .cart-count {
            background-color: var(--dark);
            color: white;
            border-radius: 50%;
            width: 20px;
            height: 20px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 0.7rem;
        }

        /* Hero Section */
        .hero {
            background: linear-gradient(rgba(0, 0, 0, 0.4), rgba(0, 0, 0, 0.4)), 
                        url('https://placehold.co/1200x500');
            background-size: cover;
            background-position: center;
            height: 400px;
            display: flex;
            align-items: center;
            color: white;
            margin-bottom: 2rem;
        }

        .hero-content {
            max-width: 600px;
        }

        .hero h1 {
            font-size: 2.5rem;
            margin-bottom: 1rem;
        }

        .hero p {
            font-size: 1.1rem;
            margin-bottom: 1.5rem;
        }

        .search-bar {
            display: flex;
            width: 100%;
        }

        .search-bar input {
            flex: 1;
            padding: 1rem;
            border: none;
            border-radius: 5px 0 0 5px;
            font-size: 1rem;
        }

        .search-bar button {
            background-color: var(--primary);
            color: white;
            border: none;
            padding: 0 1.5rem;
            border-radius: 0 5px 5px 0;
            cursor: pointer;
            transition: background-color 0.3s;
        }

        .search-bar button:hover {
            background-color: #ff5252;
        }

        /* Restaurant Grid */
        .section-title {
            font-size: 1.8rem;
            margin-bottom: 1.5rem;
            position: relative;
        }

        .section-title::after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 70px;
            height: 3px;
            background-color: var(--primary);
        }

        .restaurant-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
            gap: 2rem;
            margin-bottom: 3rem;
        }

        .restaurant-card {
            background-color: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: var(--shadow);
            transition: transform 0.3s;
        }

        .restaurant-card:hover {
            transform: translateY(-5px);
        }

        .restaurant-img {
            width: 100%;
            height: 180px;
            object-fit: cover;
        }

        .restaurant-info {
            padding: 1.2rem;
        }

        .restaurant-name {
            font-size: 1.2rem;
            margin-bottom: 0.5rem;
        }

        .restaurant-cuisine {
            color: #666;
            font-size: 0.9rem;
            margin-bottom: 1rem;
        }

        .restaurant-footer {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .rating {
            background-color: var(--accent);
            color: #333;
            padding: 0.2rem 0.5rem;
            border-radius: 5px;
            font-weight: 600;
            font-size: 0.9rem;
        }

        .delivery-time {
            font-size: 0.9rem;
            color: #666;
        }

        /* Menu Section */
        .menu-section {
            display: none;
            margin-top: 2rem;
        }

        .menu-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 1.5rem;
        }

        .back-btn {
            background-color: var(--dark);
            color: white;
            border: none;
            padding: 0.5rem 1rem;
            border-radius: 5px;
            cursor: pointer;
            transition: background-color 0.3s;
        }

        .back-btn:hover {
            background-color: #1a1f24;
        }

        .menu-categories {
            display: flex;
            gap: 1rem;
            margin-bottom: 2rem;
            overflow-x: auto;
            padding-bottom: 1rem;
        }

        .category-btn {
            background-color: white;
            border: 1px solid #ddd;
            padding: 0.5rem 1rem;
            border-radius: 20px;
            cursor: pointer;
            transition: all 0.3s;
        }

        .category-btn.active {
            background-color: var(--primary);
            color: white;
            border-color: var(--primary);
        }

        .menu-items {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
            gap: 1.5rem;
        }

        .menu-item {
            background-color: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: var(--shadow);
            transition: transform 0.3s;
        }

        .menu-item:hover {
            transform: translateY(-5px);
        }

        .menu-item-img {
            width: 100%;
            height: 180px;
            object-fit: cover;
        }

        .menu-item-info {
            padding: 1.2rem;
        }

        .menu-item-name {
            font-size: 1.1rem;
            margin-bottom: 0.5rem;
        }

        .menu-item-desc {
            color: #666;
            font-size: 0.9rem;
            margin-bottom: 1rem;
        }

        .menu-item-footer {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .menu-item-price {
            font-weight: 700;
            color: var(--primary);
        }

        .add-to-cart {
            background-color: var(--primary);
            color: white;
            border: none;
            padding: 0.5rem 1rem;
            border-radius: 5px;
            cursor: pointer;
            transition: background-color 0.3s;
        }

        .add-to-cart:hover {
            background-color: #ff5252;
        }

        /* Cart Sidebar */
        .cart-overlay {
            position: fixed;
            top: 0;
            right: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.5);
            z-index: 1000;
            display: none;
            opacity: 0;
            transition: opacity 0.3s;
        }

        .cart-sidebar {
            position: fixed;
            top: 0;
            right: -400px;
            width: 400px;
            height: 100%;
            background-color: white;
            z-index: 1001;
            transition: right 0.3s;
            display: flex;
            flex-direction: column;
        }

        .cart-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 1.5rem;
            border-bottom: 1px solid #ddd;
        }

        .cart-title {
            font-size: 1.5rem;
            font-weight: 600;
        }

        .close-cart {
            background: none;
            border: none;
            font-size: 1.5rem;
            cursor: pointer;
            color: #666;
        }

        .cart-items {
            flex: 1;
            overflow-y: auto;
            padding: 1.5rem;
        }

        .cart-item {
            display: flex;
            margin-bottom: 1rem;
            padding-bottom: 1rem;
            border-bottom: 1px solid #eee;
        }

        .cart-item-img {
            width: 80px;
            height: 80px;
            object-fit: cover;
            border-radius: 5px;
            margin-right: 1rem;
        }

        .cart-item-info {
            flex: 1;
        }

        .cart-item-name {
            font-weight: 600;
            margin-bottom: 0.3rem;
        }

        .cart-item-price {
            color: var(--primary);
            font-weight: 600;
            margin-bottom: 0.5rem;
        }

        .cart-item-qty {
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }

        .qty-btn {
            background-color: #eee;
            border: none;
            width: 25px;
            height: 25px;
            border-radius: 50%;
            cursor: pointer;
        }

        .remove-item {
            background: none;
            border: none;
            color: #ff6b6b;
            font-weight: 600;
            margin-top: 0.5rem;
            cursor: pointer;
        }

        .cart-summary {
            padding: 1.5rem;
            border-top: 1px solid #ddd;
        }

        .cart-totals {
            display: flex;
            flex-direction: column;
            gap: 0.5rem;
            margin-bottom: 1.5rem;
        }

        .cart-total-row {
            display: flex;
            justify-content: space-between;
        }

        .cart-total-label {
            font-weight: 600;
        }

        .cart-total-value {
            font-weight: 600;
            color: var(--primary);
        }

        .checkout-btn {
            width: 100%;
            padding: 1rem;
            background-color: var(--primary);
            color: white;
            border: none;
            border-radius: 5px;
            font-weight: 600;
            cursor: pointer;
            transition: background-color 0.3s;
        }

        .checkout-btn:hover {
            background-color: #ff5252;
        }

        /* Checkout Form */
        .checkout-form {
            display: none;
            background-color: white;
            padding: 2rem;
            border-radius: 10px;
            box-shadow: var(--shadow);
            max-width: 600px;
            margin: 2rem auto;
        }

        .form-group {
            margin-bottom: 1.5rem;
        }

        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: 600;
        }

        .form-group input, 
        .form-group textarea, 
        .form-group select {
            width: 100%;
            padding: 0.8rem;
            border: 1px solid #ddd;
            border-radius: 5px;
            font-size: 1rem;
        }

        .form-group textarea {
            height: 100px;
            resize: vertical;
        }

        .form-actions {
            display: flex;
            justify-content: space-between;
            margin-top: 2rem;
        }

        .form-btn {
            padding: 0.8rem 1.5rem;
            border-radius: 5px;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s;
        }

        .back-to-cart {
            background-color: #eee;
            border: none;
        }

        .place-order {
            background-color: var(--primary);
            color: white;
            border: none;
        }

        /* Order Confirmation */
        .order-confirmation {
            display: none;
            text-align: center;
            padding: 2rem;
        }

        .confirmation-icon {
            font-size: 4rem;
            color: var(--primary);
            margin-bottom: 1.5rem;
        }

        .confirmation-title {
            font-size: 2rem;
            margin-bottom: 1rem;
        }

        .confirmation-message {
            font-size: 1.1rem;
            margin-bottom: 2rem;
        }

        .back-to-home {
            padding: 1rem 2rem;
            background-color: var(--primary);
            color: white;
            border: none;
            border-radius: 5px;
            font-weight: 600;
            cursor: pointer;
            transition: background-color 0.3s;
        }

        .back-to-home:hover {
            background-color: #ff5252;
        }

        /* Responsive Styles */
        @media (max-width: 768px) {
            .navbar {
                flex-direction: column;
                gap: 1rem;
            }

            .nav-links {
                gap: 1rem;
            }

            .hero {
                height: 300px;
            }

            .hero h1 {
                font-size: 2rem;
            }

            .cart-sidebar {
                width: 100%;
                right: -100%;
            }

            .menu-items {
                grid-template-columns: repeat(auto-fill, minmax(240px, 1fr));
            }

            .checkout-form {
                padding: 1.5rem;
            }
        }

        @media (max-width: 480px) {
            .nav-links {
                flex-direction: column;
                align-items: center;
            }

            .hero {
                height: 250px;
            }

            .hero h1 {
                font-size: 1.8rem;
            }

            .menu-items {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container">
            <nav class="navbar">
                <div class="logo">
                    <img src="https://placehold.co/40x40" alt="Gourmet Express logo with fork and spoon crossed" />
                    <span>Jiva Cafe and Restaurant</span>
                </div>
                <div class="nav-links">
                    <a href="#home">Home</a>
                    <a href="#restaurants">Restaurants</a>
                    <a href="#offers">Offers</a>
                    <a href="#contact">Contact</a>
                    <button class="cart-btn" id="cartBtn">
                        Cart <span class="cart-count" id="cartCount">0</span>
                    </button>
                </div>
            </nav>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero" id="home">
        <div class="container">
            <div class="hero-content">
                <h1>Delicious food delivered to your door</h1>
                <p>Order from your favorite local restaurants with just a few clicks.</p>
                <div class="search-bar">
                    <input type="text" placeholder="Search for restaurants or dishes..." id="searchInput">
                    <button id="searchBtn">Search</button>
                </div>
            </div>
        </div>
    </section>

    <!-- Restaurants Section -->
    <section class="container" id="restaurants">
        <h2 class="section-title">Popular Restaurants</h2>
        <div class="restaurant-grid" id="restaurantGrid">
            <!-- Restaurant cards will be dynamically inserted here -->
        </div>
    </section>

    <!-- Menu Section (Hidden by default) -->
    <section class="container menu-section" id="menuSection">
        <div class="menu-header">
            <button class="back-btn" id="backBtn">Back to Restaurants</button>
            <h2 class="section-title" id="menuTitle">Restaurant Menu</h2>
        </div>
        <div class="menu-categories" id="menuCategories">
            <!-- Category buttons will be inserted here -->
        </div>
        <div class="menu-items" id="menuItems">
            <!-- Menu items will be inserted here -->
        </div>
    </section>

    <!-- Cart Sidebar -->
    <div class="cart-overlay" id="cartOverlay"></div>
    <div class="cart-sidebar" id="cartSidebar">
        <div class="cart-header">
            <h3 class="cart-title">Your Cart</h3>
            <button class="close-cart" id="closeCart">&times;</button>
        </div>
        <div class="cart-items" id="cartItems">
            <!-- Cart items will be inserted here -->
            <div class="empty-cart-message">Your cart is empty</div>
        </div>
        <div class="cart-summary">
            <div class="cart-totals">
                <div class="cart-total-row">
                    <span class="cart-total-label">Subtotal</span>
                    <span class="cart-total-value" id="cartSubtotal">$0.00</span>
                </div>
                <div class="cart-total-row">
                    <span class="cart-total-label">Delivery Fee</span>
                    <span class="cart-total-value" id="deliveryFee">$3.99</span>
                </div>
                <div class="cart-total-row">
                    <span class="cart-total-label">Total</span>
                    <span class="cart-total-value" id="cartTotal">$3.99</span>
                </div>
            </div>
            <button class="checkout-btn" id="checkoutBtn">Proceed to Checkout</button>
        </div>
    </div>

    <!-- Checkout Form -->
    <div class="container checkout-form" id="checkoutForm">
        <h2 class="section-title">Checkout</h2>
        <form id="orderForm">
            <div class="form-group">
                <label for="name">Full Name</label>
                <input type="text" id="name" required>
            </div>
            <div class="form-group">
                <label for="email">Email</label>
                <input type="email" id="email" required>
            </div>
            <div class="form-group">
                <label for="phone">Phone Number</label>
                <input type="tel" id="phone" required>
            </div>
            <div class="form-group">
                <label for="address">Delivery Address</label>
                <textarea id="address" required></textarea>
            </div>
            <div class="form-group">
                <label for="payment">Payment Method</label>
                <select id="payment" required>
                    <option value="">Select payment method</option>
                    <option value="cash">Cash on Delivery</option>
                    <option value="card">Credit/Debit Card</option>
                    <option value="paypal">PayPal</option>
                </select>
            </div>
            <div class="form-group">
                <label for="notes">Delivery Instructions (Optional)</label>
                <textarea id="notes" placeholder="Any special instructions for delivery..."></textarea>
            </div>
            <div class="form-actions">
                <button type="button" class="form-btn back-to-cart" id="backToCart">Back to Cart</button>
                <button type="submit" class="form-btn place-order" id="placeOrder">Place Order</button>
            </div>
        </form>
    </div>

    <!-- Order Confirmation -->
    <div class="container order-confirmation" id="orderConfirmation">
        <div class="confirmation-icon">✓</div>
        <h2 class="confirmation-title">Order Confirmed!</h2>
        <p class="confirmation-message">Thank you for your order! Your food will be prepared and delivered soon.</p>
        <button class="back-to-home" id="backToHome">Back to Home</button>
    </div>

    <script>
        // Sample data for restaurants and menus
        const restaurants = [
            {
                id: 1,
                name: "Pizzeria Napoli",
                cuisine: "Italian",
                rating: 4.8,
                deliveryTime: "30-40 min",
                image: "https://placehold.co/600x400",
                categories: ["Pizzas", "Pastas", "Salads", "Desserts"],
                menuItems: [
                    {
                        id: 101,
                        name: "Margherita Pizza",
                        description: "Classic pizza with tomato sauce, mozzarella and basil",
                        price: 12.99,
                        category: "Pizzas",
                        image: "https://placehold.co/300x200"
                    },
                    {
                        id: 102,
                        name: "Pepperoni Pizza",
                        description: "Traditional pizza with spicy pepperoni and mozzarella",
                        price: 14.99,
                        category: "Pizzas",
                        image: "https://placehold.co/300x200"
                    },
                    {
                        id: 103,
                        name: "Spaghetti Carbonara",
                        description: "Authentic Italian pasta with eggs, cheese, pancetta and pepper",
                        price: 11.99,
                        category: "Pastas",
                        image: "https://placehold.co/300x200"
                    },
                    {
                        id: 104,
                        name: "Caprese Salad",
                        description: "Fresh mozzarella, tomatoes and basil drizzled with balsamic glaze",
                        price: 8.99,
                        category: "Salads",
                        image: "https://placehold.co/300x200"
                    },
                    {
                        id: 105,
                        name: "Tiramisu",
                        description: "Classic Italian dessert with layers of coffee-soaked ladyfingers",
                        price: 6.99,
                        category: "Desserts",
                        image: "https://placehold.co/300x200"
                    }
                ]
            },
            {
                id: 2,
                name: "Burger Barn",
                cuisine: "American",
                rating: 4.5,
                deliveryTime: "25-35 min",
                image: "https://placehold.co/600x400",
                categories: ["Burgers", "Sides", "Drinks", "Desserts"],
                menuItems: [
                    {
                        id: 201,
                        name: "Classic Cheeseburger",
                        description: "Juicy beef patty with American cheese, lettuce and special sauce",
                        price: 9.99,
                        category: "Burgers",
                        image: "https://placehold.co/300x200"
                    },
                    {
                        id: 202,
                        name: "Bacon BBQ Burger",
                        description: "Angus beef with crispy bacon, cheddar and BBQ sauce",
                        price: 11.99,
                        category: "Burgers",
                        image: "https://placehold.co/300x200"
                    },
                    {
                        id: 203,
                        name: "French Fries",
                        description: "Crispy golden fries with sea salt",
                        price: 3.99,
                        category: "Sides",
                        image: "https://placehold.co/300x200"
                    },
                    {
                        id: 204,
                        name: "Onion Rings",
                        description: "Beer-battered onion rings with ranch dressing",
                        price: 4.99,
                        category: "Sides",
                        image: "https://placehold.co/300x200"
                    },
                    {
                        id: 205,
                        name: "Chocolate Milkshake",
                        description: "Creamy milkshake with real chocolate",
                        price: 5.99,
                        category: "Drinks",
                        image: "https://placehold.co/300x200"
                    }
                ]
            },
            {
                id: 3,
                name: "Sushi Palace",
                cuisine: "Japanese",
                rating: 4.7,
                deliveryTime: "35-45 min",
                image: "https://placehold.co/600x400",
                categories: ["Sushi Rolls", "Nigiri", "Appetizers", "Drinks"],
                menuItems: [
                    {
                        id: 301,
                        name: "California Roll",
                        description: "Classic roll with crab, avocado and cucumber",
                        price: 8.99,
                        category: "Sushi Rolls",
                        image: "https://placehold.co/300x200"
                    },
                    {
                        id: 302,
                        name: "Spicy Tuna Roll",
                        description: "Fresh tuna with spicy mayo and scallions",
                        price: 10.99,
                        category: "Sushi Rolls",
                        image: "https://placehold.co/300x200"
                    },
                    {
                        id: 303,
                        name: "Salmon Nigiri",
                        description: "Fresh salmon slices over pressed rice",
                        price: 6.99,
                        category: "Nigiri",
                        image: "https://placehold.co/300x200"
                    },
                    {
                        id: 304,
                        name: "Miso Soup",
                        description: "Traditional Japanese soup with tofu and seaweed",
                        price: 3.99,
                        category: "Appetizers",
                        image: "https://placehold.co/300x200"
                    },
                    {
                        id: 305,
                        name: "Green Tea",
                        description: "Traditional Japanese green tea",
                        price: 2.99,
                        category: "Drinks",
                        image: "https://placehold.co/300x200"
                    }
                ]
            },
            {
                id: 4,
                name: "Taco Fiesta",
                cuisine: "Mexican",
                rating: 4.6,
                deliveryTime: "20-30 min",
                image: "https://placehold.co/600x400",
                categories: ["Tacos", "Burritos", "Quesadillas", "Drinks"],
                menuItems: [
                    {
                        id: 401,
                        name: "Street Tacos",
                        description: "Three corn tortillas with choice of meat, cilantro and onions",
                        price: 9.99,
                        category: "Tacos",
                        image: "https://placehold.co/300x200"
                    },
                    {
                        id: 402,
                        name: "Carne Asada Burrito",
                        description: "Large flour tortilla with grilled steak, rice, beans and salsa",
                        price: 12.99,
                        category: "Burritos",
                        image: "https://placehold.co/300x200"
                    },
                    {
                        id: 403,
                        name: "Cheese Quesadilla",
                        description: "Grilled flour tortilla with melted cheese",
                        price: 7.99,
                        category: "Quesadillas",
                        image: "https://placehold.co/300x200"
                    },
                    {
                        id: 404,
                        name: "Guacamole",
                        description: "Freshly made guacamole with tortilla chips",
                        price: 6.99,
                        category: "Appetizers",
                        image: "https://placehold.co/300x200"
                    },
                    {
                        id: 405,
                        name: "Margarita",
                        description: "Classic lime margarita with salt rim",
                        price: 8.99,
                        category: "Drinks",
                        image: "https://placehold.co/300x200"
                    }
                ]
            }
        ];

        // Shopping cart
        let cart = [];
        
        // DOM elements
        const restaurantGrid = document.getElementById('restaurantGrid');
        const menuSection = document.getElementById('menuSection');
        const menuTitle = document.getElementById('menuTitle');
        const menuCategories = document.getElementById('menuCategories');
        const menuItems = document.getElementById('menuItems');
        const cartBtn = document.getElementById('cartBtn');
        const cartCount = document.getElementById('cartCount');
        const cartOverlay = document.getElementById('cartOverlay');
        const cartSidebar = document.getElementById('cartSidebar');
        const closeCartBtn = document.getElementById('closeCart');
        const cartItemsEl = document.getElementById('cartItems');
        const cartSubtotal = document.getElementById('cartSubtotal');
        const cartTotal = document.getElementById('cartTotal');
        const checkoutBtn = document.getElementById('checkoutBtn');
        const checkoutForm = document.getElementById('checkoutForm');
        const orderForm = document.getElementById('orderForm');
        const orderConfirmation = document.getElementById('orderConfirmation');
        const backBtn = document.getElementById('backBtn');
        const backToCartBtn = document.getElementById('backToCart');
        const backToHomeBtn = document.getElementById('backToHome');
        const searchInput = document.getElementById('searchInput');
        const searchBtn = document.getElementById('searchBtn');

        // Display restaurants on page load
        function displayRestaurants() {
            restaurantGrid.innerHTML = '';
            restaurants.forEach(restaurant => {
                const restaurantCard = document.createElement('div');
                restaurantCard.className = 'restaurant-card';
                restaurantCard.innerHTML = `
                    <img src="${restaurant.image}" alt="${restaurant.name} - ${restaurant.cuisine} restaurant" class="restaurant-img">
                    <div class="restaurant-info">
                        <h3 class="restaurant-name">${restaurant.name}</h3>
                        <p class="restaurant-cuisine">${restaurant.cuisine}</p>
                        <div class="restaurant-footer">
                            <span class="rating">★ ${restaurant.rating}</span>
                            <span class="delivery-time">${restaurant.deliveryTime}</span>
                        </div>
                    </div>
                `;
                restaurantCard.addEventListener('click', () => showMenu(restaurant));
                restaurantGrid.appendChild(restaurantCard);
            });
        }

        // Show menu for selected restaurant
        function showMenu(restaurant) {
            menuTitle.textContent = restaurant.name;
            menuCategories.innerHTML = '';
            menuItems.innerHTML = '';
            
            // Display category buttons
            restaurant.categories.forEach(category => {
                const categoryBtn = document.createElement('button');
                categoryBtn.className = 'category-btn';
                categoryBtn.textContent = category;
                categoryBtn.addEventListener('click', () => filterMenuItems(restaurant.menuItems, category));
                menuCategories.appendChild(categoryBtn);
            });
            
            // Set first category as active and show menu items
            const firstCategory = restaurant.categories[0];
            const firstCategoryBtn = menuCategories.querySelector('.category-btn');
            firstCategoryBtn.classList.add('active');
            filterMenuItems(restaurant.menuItems, firstCategory);
            
            // Hide restaurants and show menu
            document.getElementById('restaurants').style.display = 'none';
            menuSection.style.display = 'block';
        }

        // Filter menu items by category
        function filterMenuItems(items, category) {
            const filteredItems = items.filter(item => item.category === category);
            displayMenuItems(filteredItems);
            
            // Update active category button
            const categoryButtons = document.querySelectorAll('.category-btn');
            categoryButtons.forEach(btn => {
                btn.classList.remove('active');
                if (btn.textContent === category) {
                    btn.classList.add('active');
                }
            });
        }

        // Display menu items
        function displayMenuItems(items) {
            menuItems.innerHTML = '';
            items.forEach(item => {
                const menuItem = document.createElement('div');
                menuItem.className = 'menu-item';
                menuItem.innerHTML = `
                    <img src="${item.image}" alt="${item.name}" class="menu-item-img">
                    <div class="menu-item-info">
                        <h3 class="menu-item-name">${item.name}</h3>
                        <p class="menu-item-desc">${item.description}</p>
                        <div class="menu-item-footer">
                            <span class="menu-item-price">$${item.price.toFixed(2)}</span>
                            <button class="add-to-cart" data-id="${item.id}" data-name="${item.name}" data-price="${item.price}" data-image="${item.image}">Add to Cart</button>
                        </div>
                    </div>
                `;
                menuItems.appendChild(menuItem);
            });
            
            // Add event listeners to add-to-cart buttons
            document.querySelectorAll('.add-to-cart').forEach(button => {
                button.addEventListener('click', addToCart);
            });
        }

        // Back to restaurants view
        function backToRestaurants() {
            menuSection.style.display = 'none';
            document.getElementById('restaurants').style.display = 'block';
        }

        // Add item to cart
        function addToCart(e) {
            const id = parseInt(e.target.getAttribute('data-id'));
            const name = e.target.getAttribute('data-name');
            const price = parseFloat(e.target.getAttribute('data-price'));
            const image = e.target.getAttribute('data-image');
            
            // Check if item already in cart
            const existingItem = cart.find(item => item.id === id);
            
            if (existingItem) {
                existingItem.quantity += 1;
            } else {
                cart.push({
                    id,
                    name,
                    price,
                    image,
                    quantity: 1
                });
            }
            
            updateCart();
            
            // Provide visual feedback
            const button = e.target;
            button.textContent = 'Added!';
            setTimeout(() => {
                button.textContent = 'Add to Cart';
            }, 1000);
        }

        // Update cart display
        function updateCart() {
            cartCount.textContent = cart.reduce((sum, item) => sum + item.quantity, 0);
            
            cartItemsEl.innerHTML = '';
            
            if (cart.length === 0) {
                cartItemsEl.innerHTML = '<div class="empty-cart-message">Your cart is empty</div>';
                cartSubtotal.textContent = '$0.00';
                cartTotal.textContent = '$3.99';
                checkoutBtn.disabled = true;
                return;
            }
            
            checkoutBtn.disabled = false;
            
            cart.forEach(item => {
                const cartItem = document.createElement('div');
                cartItem.className = 'cart-item';
                cartItem.innerHTML = `
                    <img src="${item.image}" alt="${item.name}" class="cart-item-img">
                    <div class="cart-item-info">
                        <h4 class="cart-item-name">${item.name}</h4>
                        <div class="cart-item-price">$${(item.price * item.quantity).toFixed(2)}</div>
                        <div class="cart-item-qty">
                            <button class="qty-btn minus" data-id="${item.id}">-</button>
                            <span class="quantity">${item.quantity}</span>
                            <button class="qty-btn plus" data-id="${item.id}">+</button>
                        </div>
                        <button class="remove-item" data-id="${item.id}">Remove</button>
                    </div>
                `;
                cartItemsEl.appendChild(cartItem);
            });
            
            // Calculate subtotal
            const subtotal = cart.reduce((sum, item) => sum + (item.price * item.quantity), 0);
            cartSubtotal.textContent = `$${subtotal.toFixed(2)}`;
            
            // Calculate total (subtotal + delivery fee)
            const total = subtotal + 3.99;
            cartTotal.textContent = `$${total.toFixed(2)}`;
            
            // Add event listeners to quantity and remove buttons
            document.querySelectorAll('.minus').forEach(button => {
                button.addEventListener('click', decreaseQuantity);
            });
            
            document.querySelectorAll('.plus').forEach(button => {
                button.addEventListener('click', increaseQuantity);
            });
            
            document.querySelectorAll('.remove-item').forEach(button => {
                button.addEventListener('click', removeItem);
            });
        }

        // Decrease item quantity
        function decreaseQuantity(e) {
            const id = parseInt(e.target.getAttribute('data-id'));
            const item = cart.find(item => item.id === id);
            
            if (item.quantity > 1) {
                item.quantity -= 1;
            } else {
                // Remove item if quantity would become 0
                cart = cart.filter(item => item.id !== id);
            }
            
            updateCart();
        }

        // Increase item quantity
        function increaseQuantity(e) {
            const id = parseInt(e.target.getAttribute('data-id'));
            const item = cart.find(item => item.id === id);
            item.quantity += 1;
            updateCart();
        }

        // Remove item from cart
        function removeItem(e) {
            const id = parseInt(e.target.getAttribute('data-id'));
            cart = cart.filter(item => item.id !== id);
            updateCart();
        }

        // Toggle cart sidebar
        function toggleCart() {
            if (cartSidebar.style.right === '0px') {
                cartSidebar.style.right = '-400px';
                setTimeout(() => {
                    cartOverlay.style.display = 'none';
                    cartOverlay.style.opacity = '0';
                }, 300);
            } else {
                cartOverlay.style.display = 'block';
                setTimeout(() => {
                    cartOverlay.style.opacity = '1';
                    cartSidebar.style.right = '0px';
                }, 10);
            }
        }

        // Show checkout form
        function showCheckout() {
            toggleCart();
            checkoutForm.style.display = 'block';
            menuSection.style.display = 'none';
            document.getElementById('restaurants').style.display = 'none';
        }

        // Back to cart from checkout
        function backToCartFromCheckout() {
            checkoutForm.style.display = 'none';
            toggleCart();
            backToRestaurants();
        }

        // Place order
        function placeOrder(e) {
            e.preventDefault();
            
            // Get form values
            const name = document.getElementById('name').value;
            const email = document.getElementById('email').value;
            const phone = document.getElementById('phone').value;
            const address = document.getElementById('address').value;
            const payment = document.getElementById('payment').value;
            const notes = document.getElementById('notes').value;
            
            // In a real app, you would send this data to a server
            console.log('Order placed:', {
                customer: { name, email, phone, address, notes },
                paymentMethod: payment,
                items: cart,
                total: parseFloat(cartTotal.textContent.substring(1))
            });
            
            // Show confirmation and clear cart
            checkoutForm.style.display = 'none';
            orderConfirmation.style.display = 'block';
            cart = [];
            updateCart();
        }

        // Back to home from confirmation
        function backToHome() {
            orderConfirmation.style.display = 'none';
            backToRestaurants();
        }

        // Search functionality
        function searchRestaurants() {
            const searchTerm = searchInput.value.toLowerCase();
            
            if (searchTerm.trim() === '') {
                displayRestaurants();
                return;
            }
            
            const filteredRestaurants = restaurants.filter(restaurant => {
                return (
                    restaurant.name.toLowerCase().includes(searchTerm) ||
                    restaurant.cuisine.toLowerCase().includes(searchTerm) ||
                    restaurant.menuItems.some(item => 
                        item.name.toLowerCase().includes(searchTerm) ||
                        item.description.toLowerCase().includes(searchTerm)
                    )
                );
            });
            
            restaurantGrid.innerHTML = '';
            if (filteredRestaurants.length === 0) {
                restaurantGrid.innerHTML = '<p class="no-results">No restaurants or dishes found matching your search.</p>';
            } else {
                filteredRestaurants.forEach(restaurant => {
                    const restaurantCard = document.createElement('div');
                    restaurantCard.className = 'restaurant-card';
                    restaurantCard.innerHTML = `
                        <img src="${restaurant.image}" alt="${restaurant.name} - ${restaurant.cuisine} restaurant" class="restaurant-img">
                        <div class="restaurant-info">
                            <h3 class="restaurant-name">${restaurant.name}</h3>
                            <p class="restaurant-cuisine">${restaurant.cuisine}</p>
                            <div class="restaurant-footer">
                                <span class="rating">★ ${restaurant.rating}</span>
                                <span class="delivery-time">${restaurant.deliveryTime}</span>
                            </div>
                        </div>
                    `;
                    restaurantCard.addEventListener('click', () => showMenu(restaurant));
                    restaurantGrid.appendChild(restaurantCard);
                });
            }
        }

        // Event listeners
        cartBtn.addEventListener('click', toggleCart);
        closeCartBtn.addEventListener('click', toggleCart);
        cartOverlay.addEventListener('click', toggleCart);
        checkoutBtn.addEventListener('click', showCheckout);
        backBtn.addEventListener('click', backToRestaurants);
        backToCartBtn.addEventListener('click', backToCartFromCheckout);
        backToHomeBtn.addEventListener('click', backToHome);
        orderForm.addEventListener('submit', placeOrder);
        searchBtn.addEventListener('click', searchRestaurants);
        
        // Initialize the page
        displayRestaurants();
    </script>
</body>
</html>
