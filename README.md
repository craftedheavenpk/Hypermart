<!DOCTYPE html>
<html lang="en" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Hypermart | Premium Household & Grocery Store Lahore</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        martPrimary: '#047857',
                        martDark: '#064e3b',
                        martAccent: '#f59e0b',
                    }
                }
            }
        }
    </script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&family=Playfair+Display:wght@600;700&display=swap" rel="stylesheet">
    <style>
        body { font-family: 'Poppins', sans-serif; }
        .brand-font { font-family: 'Playfair Display', serif; }
    </style>
</head>
<body class="bg-slate-900 text-slate-100 min-h-screen flex flex-col">

    <!-- Top Announcement Bar -->
    <div class="bg-martDark text-emerald-300 text-xs py-2 px-4 text-center border-b border-emerald-900">
        <i class="fa-solid fa-truck-fast mr-2"></i> Fast Home Delivery across Lahore | Same-Day Delivery Available! | WhatsApp: 03034812714
    </div>

    <!-- Header / Navbar -->
    <header class="sticky top-0 z-40 bg-slate-900/95 backdrop-blur-md border-b border-slate-800 shadow-md">
        <div class="max-w-7xl mx-auto px-4 py-3 flex items-center justify-between">
            
            <!-- Hamburger & Logo -->
            <div class="flex items-center space-x-3">
                <button onclick="toggleSideMenu()" class="text-emerald-400 text-xl p-1 focus:outline-none md:hidden">
                    <i class="fa-solid fa-bars"></i>
                </button>
                <a href="#" class="flex items-center space-x-2">
                    <div class="w-10 h-10 rounded-full bg-gradient-to-tr from-emerald-600 to-emerald-400 flex items-center justify-center shadow-lg">
                        <i class="fa-solid fa-basket-shopping text-white text-lg"></i>
                    </div>
                    <div>
                        <span class="text-xl font-bold tracking-wider brand-font text-white block leading-none">Hypermart</span>
                        <span class="text-[10px] text-emerald-400 tracking-widest uppercase font-medium">Gulberg III, Lahore</span>
                    </div>
                </a>
            </div>

            <!-- Desktop Nav Links -->
            <nav class="hidden md:flex items-center space-x-6 font-medium text-sm">
                <a href="#home" class="hover:text-emerald-400 transition">Home</a>
                <a href="#products" class="hover:text-emerald-400 transition">All Products</a>
                <a href="#about" class="hover:text-emerald-400 transition">About Us</a>
                <a href="#contact" class="hover:text-emerald-400 transition">Contact</a>
            </nav>

            <!-- Cart / Bucket Button -->
            <div class="flex items-center space-x-3">
                <button onclick="toggleCart()" class="relative bg-emerald-600 hover:bg-emerald-500 text-white px-4 py-2 rounded-full font-medium text-sm flex items-center shadow transition">
                    <i class="fa-solid fa-bag-shopping mr-2"></i>
                    <span class="hidden sm:inline">Bucket</span>
                    <span id="cart-count" class="absolute -top-1.5 -right-1.5 bg-red-500 text-white text-xs w-5 h-5 rounded-full flex items-center justify-center font-bold shadow">0</span>
                </button>
            </div>
        </div>
    </header>

    <!-- Side Menu Drawer for Mobile -->
    <div id="sideMenu" class="fixed inset-0 z-50 bg-black/70 backdrop-blur-sm hidden transition-opacity">
        <div class="bg-slate-900 w-72 h-full p-6 flex flex-col justify-between shadow-2xl border-r border-slate-800 transform -translate-x-full transition-transform duration-300" id="sideMenuPanel">
            <div>
                <div class="flex items-center justify-between mb-8">
                    <div class="flex items-center space-x-2">
                        <div class="w-8 h-8 rounded-full bg-emerald-600 flex items-center justify-center">
                            <i class="fa-solid fa-basket-shopping text-white text-sm"></i>
                        </div>
                        <span class="font-bold text-lg brand-font text-white">Hypermart</span>
                    </div>
                    <button onclick="toggleSideMenu()" class="text-slate-400 hover:text-white text-xl">
                        <i class="fa-solid fa-xmark"></i>
                    </button>
                </div>
                <nav class="flex flex-col space-y-4 font-medium">
                    <a href="#home" onclick="toggleSideMenu()" class="flex items-center space-x-3 text-slate-300 hover:text-emerald-400 py-2 border-b border-slate-800"><i class="fa-solid fa-house w-6 text-emerald-500"></i> <span>Home</span></a>
                    <a href="#products" onclick="toggleSideMenu()" class="flex items-center space-x-3 text-slate-300 hover:text-emerald-400 py-2 border-b border-slate-800"><i class="fa-solid fa-boxes-stacked w-6 text-emerald-500"></i> <span>Products & Groceries</span></a>
                    <a href="#about" onclick="toggleSideMenu()" class="flex items-center space-x-3 text-slate-300 hover:text-emerald-400 py-2 border-b border-slate-800"><i class="fa-solid fa-circle-info w-6 text-emerald-500"></i> <span>About Us</span></a>
                    <a href="#contact" onclick="toggleSideMenu()" class="flex items-center space-x-3 text-slate-300 hover:text-emerald-400 py-2 border-b border-slate-800"><i class="fa-solid fa-phone w-6 text-emerald-500"></i> <span>Contact & WhatsApp</span></a>
                </nav>
            </div>
            <div class="text-xs text-slate-500 text-center py-4 border-t border-slate-800">
                <p>© 2026 Hypermart Lahore</p>
                <p class="mt-1">Order via WhatsApp: 03034812714</p>
            </div>
        </div>
    </div>

    <!-- Hero Section -->
    <section id="home" class="relative bg-gradient-to-r from-slate-950 via-emerald-950 to-slate-900 py-12 px-4 text-center border-b border-slate-800">
        <div class="max-w-4xl mx-auto">
            <span class="inline-block bg-emerald-900/60 text-emerald-300 text-xs font-semibold px-4 py-1.5 rounded-full mb-4 border border-emerald-700/50">
                <i class="fa-solid fa-star text-amber-400 mr-1.5"></i> Lahore's Trusted Household & Grocery Mart
            </span>
            <h1 class="text-3xl sm:text-5xl font-extrabold tracking-tight text-white mb-4 brand-font">
                Everything You Need for Your <span class="text-transparent bg-clip-text bg-gradient-to-r from-emerald-400 to-amber-300">Home & Kitchen</span>
            </h1>
            <p class="text-slate-300 text-sm sm:text-base max-w-2xl mx-auto mb-8 leading-relaxed">
                Explore premium quality food items, masalas, cooking oils, ghee, nuts, biscuits, personal care, smart home accessories, stationery, and daily essentials delivered right to your doorstep.
            </p>
            <div class="flex flex-wrap justify-center gap-4">
                <a href="#products" class="bg-emerald-600 hover:bg-emerald-500 text-white font-medium px-6 py-3 rounded-xl shadow-lg transition flex items-center">
                    <i class="fa-solid fa-bag-shopping mr-2"></i> Shop All Products
                </a>
                <a href="https://wa.me/923034812714?text=Hello%20Hypermart,%20I%20want%20to%20place%20an%20order." target="_blank" class="bg-emerald-700/50 hover:bg-emerald-700 text-emerald-200 border border-emerald-600 font-medium px-6 py-3 rounded-xl transition flex items-center">
                    <i class="fa-brands fa-whatsapp text-lg mr-2 text-emerald-400"></i> Direct WhatsApp Order
                </a>
            </div>
        </div>
    </section>

    <!-- Main Products Section -->
    <section id="products" class="max-w-7xl mx-auto px-4 py-10 flex-grow w-full">
        
        <!-- Section Header & Sorting/Filtering Controls -->
        <div class="flex flex-col md:flex-row md:items-center justify-between gap-4 mb-8 bg-slate-800/50 p-4 rounded-2xl border border-slate-700">
            <div>
                <h2 class="text-2xl font-bold text-white brand-font">Our Product Catalog</h2>
                <p class="text-xs text-slate-400 mt-0.5">Select items, add to bucket, and checkout directly via WhatsApp.</p>
            </div>

            <!-- Sorting & Search Controls -->
            <div class="flex flex-wrap items-center gap-3">
                <div class="relative flex-grow sm:flex-grow-0">
                    <input type="text" id="searchInput" oninput="filterProducts()" placeholder="Search items..." class="bg-slate-900 border border-slate-700 text-sm text-white rounded-xl px-4 py-2 pl-9 focus:outline-none focus:border-emerald-500 w-full sm:w-56">
                    <i class="fa-solid fa-magnifying-glass absolute left-3 top-3 text-slate-400 text-xs"></i>
                </div>
                <select id="sortSelect" onchange="filterProducts()" class="bg-slate-900 border border-slate-700 text-sm text-white rounded-xl px-4 py-2 focus:outline-none focus:border-emerald-500">
                    <option value="default">Sort by: Default</option>
                    <option value="low-high">Price: Low to High</option>
                    <option value="high-low">Price: High to Low</option>
                    <option value="name">Name: A to Z</option>
                </select>
            </div>
        </div>

        <!-- Categories Filter Pills -->
        <div class="flex items-center gap-2 overflow-x-auto pb-4 mb-6 no-scrollbar">
            <button onclick="setCategory('All')" class="cat-btn active-cat bg-emerald-600 text-white px-4 py-2 rounded-xl text-xs font-semibold whitespace-nowrap transition shadow">All Items</button>
            <button onclick="setCategory('Food & Staples')" class="cat-btn bg-slate-800 text-slate-300 hover:bg-slate-700 px-4 py-2 rounded-xl text-xs font-semibold whitespace-nowrap transition border border-slate-700">Food & Staples</button>
            <button onclick="setCategory('Masala & Oils')" class="cat-btn bg-slate-800 text-slate-300 hover:bg-slate-700 px-4 py-2 rounded-xl text-xs font-semibold whitespace-nowrap transition border border-slate-700">Masala & Oils</button>
            <button onclick="setCategory('Nuts & Snacks')" class="cat-btn bg-slate-800 text-slate-300 hover:bg-slate-700 px-4 py-2 rounded-xl text-xs font-semibold whitespace-nowrap transition border border-slate-700">Nuts & Biscuits</button>
            <button onclick="setCategory('Personal Care')" class="cat-btn bg-slate-800 text-slate-300 hover:bg-slate-700 px-4 py-2 rounded-xl text-xs font-semibold whitespace-nowrap transition border border-slate-700">Personal Care</button>
            <button onclick="setCategory('Smart Accessories')" class="cat-btn bg-slate-800 text-slate-300 hover:bg-slate-700 px-4 py-2 rounded-xl text-xs font-semibold whitespace-nowrap transition border border-slate-700">Smart Accessories</button>
            <button onclick="setCategory('Stationery')" class="cat-btn bg-slate-800 text-slate-300 hover:bg-slate-700 px-4 py-2 rounded-xl text-xs font-semibold whitespace-nowrap transition border border-slate-700">Stationery</button>
        </div>

        <!-- Products Grid: STRICTLY 2 Products per Row on mobile & responsive up to 4 on desktop -->
        <div id="products-grid" class="grid grid-cols-2 lg:grid-cols-4 gap-4 sm:gap-6">
            <!-- Dynamically populated by JS -->
        </div>
    </section>

    <!-- About Section -->
    <section id="about" class="bg-slate-800/40 border-t border-b border-slate-800 py-12 px-4 my-10">
        <div class="max-w-4xl mx-auto text-center">
            <h2 class="text-3xl font-bold text-white mb-4 brand-font">About Hypermart</h2>
            <p class="text-slate-300 text-sm sm:text-base leading-relaxed mb-6">
                Hypermart is Lahore's premier neighborhood shopping destination located in Gulberg III. We pride ourselves on providing 100% genuine household goods, fresh grocery staples, pure cooking oils, authentic masalas, snacks, stationery, and modern home accessories under one roof at unbeatable prices with doorstep delivery.
            </p>
            <div class="grid grid-cols-1 sm:grid-cols-3 gap-4 text-left">
                <div class="bg-slate-900 p-4 rounded-xl border border-slate-800">
                    <i class="fa-solid fa-shield-check text-emerald-400 text-xl mb-2"></i>
                    <h3 class="font-bold text-white text-sm mb-1">100% Quality Assured</h3>
                    <p class="text-xs text-slate-400">Verified branded and premium organic household products.</p>
                </div>
                <div class="bg-slate-900 p-4 rounded-xl border border-slate-800">
                    <i class="fa-solid fa-bolt text-amber-400 text-xl mb-2"></i>
                    <h3 class="font-bold text-white text-sm mb-1">Same-Day Lahore Delivery</h3>
                    <p class="text-xs text-slate-400">Quick dispatch across Lahore within hours of order placement.</p>
                </div>
                <div class="bg-slate-900 p-4 rounded-xl border border-slate-800">
                    <i class="fa-solid fa-wallet text-emerald-400 text-xl mb-2"></i>
                    <h3 class="font-bold text-white text-sm mb-1">Easy WhatsApp Checkout</h3>
                    <p class="text-xs text-slate-400">Seamless ordering via WhatsApp with JazzCash/EasyPaisa support.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact & Payment Section -->
    <section id="contact" class="max-w-4xl mx-auto px-4 py-8 mb-12 w-full text-center">
        <h2 class="text-2xl font-bold text-white mb-4 brand-font">Contact & Payment Information</h2>
        <div class="bg-slate-800/50 p-6 rounded-2xl border border-slate-700 inline-block w-full max-w-xl text-left">
            <div class="space-y-3 text-sm text-slate-300">
                <p><i class="fa-solid fa-location-dot text-emerald-400 w-6"></i> <strong>Location:</strong> Main Boulevard, Gulberg III, Lahore</p>
                <p><i class="fa-solid fa-phone text-emerald-400 w-6"></i> <strong>WhatsApp Helpline:</strong> 03034812714</p>
                <p><i class="fa-solid fa-credit-card text-emerald-400 w-6"></i> <strong>JazzCash / EasyPaisa:</strong> 03034812714</p>
                <p><i class="fa-solid fa-clock text-emerald-400 w-6"></i> <strong>Timings:</strong> 9:00 AM – 10:00 PM (Monday to Sunday)</p>
            </div>
        </div>
    </section>

    <!-- Cart / Bucket Drawer Overlay -->
    <div id="cartDrawer" class="fixed inset-0 z-50 bg-black/70 backdrop-blur-sm hidden flex justify-end transition-opacity">
        <div class="bg-slate-900 w-full max-w-md h-full p-5 flex flex-col justify-between shadow-2xl border-l border-slate-800 transform translate-x-full transition-transform duration-300" id="cartPanel">
            <div>
                <div class="flex items-center justify-between pb-4 border-b border-slate-800">
                    <div class="flex items-center space-x-2">
                        <i class="fa-solid fa-bag-shopping text-emerald-400 text-lg"></i>
                        <h3 class="font-bold text-lg text-white brand-font">Your Shopping Bucket</h3>
                    </div>
                    <button onclick="toggleCart()" class="text-slate-400 hover:text-white text-xl">
                        <i class="fa-solid fa-xmark"></i>
                    </button>
                </div>

                <!-- Cart Items List -->
                <div id="cart-items" class="py-4 space-y-3 overflow-y-auto max-h-[calc(100vh-280px)]">
                    <p class="text-slate-500 text-center py-8 text-sm">Your bucket is currently empty.</p>
                </div>
            </div>

            <!-- Cart Footer & WhatsApp Checkout -->
            <div class="pt-4 border-t border-slate-800">
                <div class="flex justify-between items-center mb-4 text-base font-bold text-white">
                    <span>Total Amount:</span>
                    <span id="cart-total" class="text-emerald-400">Rs. 0</span>
                </div>
                <button onclick="checkoutWhatsApp()" class="w-full bg-emerald-600 hover:bg-emerald-500 text-white font-semibold py-3 rounded-xl shadow-lg transition flex items-center justify-center space-x-2">
                    <i class="fa-brands fa-whatsapp text-lg"></i>
                    <span>Checkout via WhatsApp</span>
                </button>
                <p class="text-[11px] text-slate-500 text-center mt-2">Payments accepted via Cash on Delivery, JazzCash & EasyPaisa (03034812714).</p>
            </div>
        </div>
    </div>

    <!-- Footer -->
    <footer class="bg-slate-950 border-t border-slate-800 py-8 px-4 text-center text-xs text-slate-500">
        <div class="max-w-7xl mx-auto flex flex-col sm:flex-row items-center justify-between gap-4">
            <div class="flex items-center space-x-2">
                <div class="w-7 h-7 rounded-full bg-emerald-600 flex items-center justify-center">
                    <i class="fa-solid fa-basket-shopping text-white text-xs"></i>
                </div>
                <span class="font-bold text-white brand-font text-sm">Hypermart</span>
            </div>
            <p>© 2026 Hypermart Lahore. All rights reserved.</p>
            <div class="flex space-x-4 text-slate-400">
                <a href="https://wa.me/923034812714" target="_blank" class="hover:text-emerald-400"><i class="fa-brands fa-whatsapp text-base"></i></a>
                <a href="#home" class="hover:text-emerald-400"><i class="fa-solid fa-arrow-up text-base"></i></a>
            </div>
        </div>
    </footer>

    <!-- JavaScript Application Logic -->
    <script>
        const products = [
            {
                id: 1,
                name: "Super Basmati Rice (5kg)",
                category: "Food & Staples",
                price: 2450,
                image: "https://images.unsplash.com/photo-1586201375761-83865001e31c?auto=format&fit=crop&w=500&q=80",
                desc: "Aged long-grain aromatic basmati rice. Fluffy texture and delightful fragrance for biryani and daily meals."
            },
            {
                id: 2,
                name: "Fine Iodized Salt (800g)",
                category: "Food & Staples",
                price: 90,
                image: "https://images.unsplash.com/photo-1518110992383-2557ec1d8738?auto=format&fit=crop&w=500&q=80",
                desc: "Pure vacuum-evaporated iodized table salt. Essential for everyday cooking with clean taste and fine grain."
            },
            {
                id: 3,
                name: "Premium Wheat Flour / Atta (10kg)",
                category: "Food & Staples",
                price: 1350,
                image: "https://images.unsplash.com/photo-1509440159596-0249088772ff?auto=format&fit=crop&w=500&q=80",
                desc: "Stone-ground whole wheat flour rich in fiber. Perfect for soft, fluffy rotis and parathas for the family."
            },
            {
                id: 4,
                name: "Pure Corn / Maize Flour (1kg)",
                category: "Food & Staples",
                price: 220,
                image: "https://images.unsplash.com/photo-1556742049-0a67d553c295?auto=format&fit=crop&w=500&q=80",
                desc: "Finely milled yellow maize flour. Ideal for traditional makki ki roti, baking, and thickening gravies."
            },
            {
                id: 5,
                name: "Special Biryani Masala (50g)",
                category: "Masala & Oils",
                price: 140,
                image: "https://images.unsplash.com/photo-1596040033229-a9821ebd058d?auto=format&fit=crop&w=500&q=80",
                desc: "Authentic blend of handpicked aromatic spices. Gives restaurant-style flavor and color to your homemade biryani."
            },
            {
                id: 6,
                name: "Pure Cooking Oil (1 Litre Pouch)",
                category: "Masala & Oils",
                price: 520,
                image: "https://images.unsplash.com/photo-1474979266404-7eaacbcd87c5?auto=format&fit=crop&w=500&q=80",
                desc: "Vitamin-enriched high quality cooking oil. Light on stomach, ideal for frying, baking, and daily cooking."
            },
            {
                id: 7,
                name: "Desi Banaspati Ghee (1kg)",
                category: "Masala & Oils",
                price: 590,
                image: "https://images.unsplash.com/photo-1632778149955-e80f8ceca2e8?auto=format&fit=crop&w=500&q=80",
                desc: "Rich buttery aroma and traditional taste. Perfect for preparing sweets, parathas, and flavorful daily dishes."
            },
            {
                id: 8,
                name: "Mixed Roasted Nuts & Almonds Pack (250g)",
                category: "Nuts & Snacks",
                price: 750,
                image: "https://images.unsplash.com/photo-1536256263959-770b48d82b0a?auto=format&fit=crop&w=500&q=80",
                desc: "Crunchy premium mix of almonds, cashews, and walnuts. High protein energizing snack for all age groups."
            },
            {
                id: 9,
                name: "Crispy Tea Biscuits Box (Family Pack)",
                category: "Nuts & Snacks",
                price: 280,
                image: "https://images.unsplash.com/photo-1558961363-fa8fdf82db35?auto=format&fit=crop&w=500&q=80",
                desc: "Delightful golden-baked tea biscuits. Crisp, sweet, and the ultimate companion for your evening chai."
            },
            {
                id: 10,
                name: "Herbal Bath Soap (Pack of 3)",
                category: "Personal Care",
                price: 360,
                image: "https://images.unsplash.com/photo-1600857544200-b2f666a9a2ec?auto=format&fit=crop&w=500&q=80",
                desc: "Enriched with natural extracts and moisturizers. Gently cleanses skin while keeping it soft and fragrant."
            },
            {
                id: 11,
                name: "Anti-Dandruff Herbal Shampoo (400ml)",
                category: "Personal Care",
                price: 650,
                image: "https://images.unsplash.com/photo-1535585209827-a15fcdbc4c2d?auto=format&fit=crop&w=500&q=80",
                desc: "Deep nourishment formula that removes dandruff and strengthens roots. Leaves hair silky and shiny."
            },
            {
                id: 12,
                name: "Smart LED Desk Lamp with USB Charger",
                category: "Smart Accessories",
                price: 1250,
                image: "https://images.unsplash.com/photo-1534447677768-be436bb09401?auto=format&fit=crop&w=500&q=80",
                desc: "Eye-friendly touch-controlled LED lamp with adjustable brightness levels and built-in phone charging port."
            },
            {
                id: 13,
                name: "Portable Mini USB Desk Fan",
                category: "Smart Accessories",
                price: 890,
                image: "https://images.unsplash.com/photo-1585771724684-38269d6639fd?auto=format&fit=crop&w=500&q=80",
                desc: "Compact, quiet, and powerful USB-powered cooling fan. Ideal for study desks, offices, and bedside tables."
            },
            {
                id: 14,
                name: "Student Notebook & Ballpoint Pen Set",
                category: "Stationery",
                price: 320,
                image: "https://images.unsplash.com/photo-1583485088034-697b5bc54ccd?auto=format&fit=crop&w=500&q=80",
                desc: "High quality ruled pages notebook with smooth gel pens. Perfect for school, office meetings, and notes."
            }
        ];

        let cart = [];
        let currentCategory = 'All';

        function renderProducts() {
            const grid = document.getElementById('products-grid');
            const searchVal = document.getElementById('searchInput').value.toLowerCase();
            const sortVal = document.getElementById('sortSelect').value;

            let filtered = products.filter(p => {
                let matchesCat = currentCategory === 'All' || p.category === currentCategory;
                let matchesSearch = p.name.toLowerCase().includes(searchVal) || p.desc.toLowerCase().includes(searchVal);
                return matchesCat && matchesSearch;
            });

            if (sortVal === 'low-high') {
                filtered.sort((a, b) => a.price - b.price);
            } else if (sortVal === 'high-low') {
                filtered.sort((a, b) => b.price - a.price);
            } else if (sortVal === 'name') {
                filtered.sort((a, b) => a.name.localeCompare(b.name));
            }

            if (filtered.length === 0) {
                grid.innerHTML = `<div class="col-span-2 lg:col-span-4 text-center py-12 text-slate-400"><p>No products found matching your search.</p></div>`;
                return;
            }

            grid.innerHTML = filtered.map(p => `
                <div class="bg-slate-800/80 rounded-2xl border border-slate-700 overflow-hidden flex flex-col justify-between shadow-md hover:border-emerald-500/50 transition">
                    <div>
                        <div class="relative h-40 sm:h-48 overflow-hidden bg-slate-900">
                            <img src="${p.image}" alt="${p.name}" class="w-full h-full object-cover hover:scale-105 transition duration-300">
                            <span class="absolute top-2 left-2 bg-emerald-950/90 text-emerald-300 text-[10px] font-semibold px-2.5 py-1 rounded-full border border-emerald-800">${p.category}</span>
                        </div>
                        <div class="p-3 sm:p-4">
                            <h3 class="font-bold text-sm sm:text-base text-white mb-1 line-clamp-1">${p.name}</h3>
                            <p class="text-xs text-slate-300 line-clamp-3 mb-3 leading-relaxed">${p.desc}</p>
                        </div>
                    </div>
                    <div class="p-3 sm:p-4 pt-0 flex items-center justify-between border-t border-slate-700/50 mt-auto">
                        <span class="font-bold text-emerald-400 text-sm sm:text-base">Rs. ${p.price}</span>
                        <button onclick="addToCart(${p.id})" class="bg-emerald-600 hover:bg-emerald-500 text-white text-xs font-semibold px-3 py-2 rounded-xl transition flex items-center shadow">
                            <i class="fa-solid fa-plus mr-1"></i> Add
                        </button>
                    </div>
                </div>
            `).join('');
        }

        function setCategory(cat) {
            currentCategory = cat;
            document.querySelectorAll('.cat-btn').forEach(btn => {
                if (btn.innerText.includes(cat) || (cat === 'All' && btn.innerText.includes('All'))) {
                    btn.className = "cat-btn active-cat bg-emerald-600 text-white px-4 py-2 rounded-xl text-xs font-semibold whitespace-nowrap transition shadow";
                } else {
                    btn.className = "cat-btn bg-slate-800 text-slate-300 hover:bg-slate-700 px-4 py-2 rounded-xl text-xs font-semibold whitespace-nowrap transition border border-slate-700";
                }
            });
            renderProducts();
        }

        function filterProducts() {
            renderProducts();
        }

        function toggleSideMenu() {
            const menu = document.getElementById('sideMenu');
            const panel = document.getElementById('sideMenuPanel');
            if (menu.classList.contains('hidden')) {
                menu.classList.remove('hidden');
                setTimeout(() => panel.classList.remove('-translate-x-full'), 10);
            } else {
                panel.classList.add('-translate-x-full');
                setTimeout(() => menu.classList.add('hidden'), 300);
            }
        }

        function toggleCart() {
            const drawer = document.getElementById('cartDrawer');
            const panel = document.getElementById('cartPanel');
            if (drawer.classList.contains('hidden')) {
                drawer.classList.remove('hidden');
                setTimeout(() => panel.classList.remove('translate-x-full'), 10);
            } else {
                panel.classList.add('translate-x-full');
                setTimeout(() => drawer.classList.add('hidden'), 300);
            }
        }

        function addToCart(id) {
            const product = products.find(p => p.id === id);
            const existing = cart.find(item => item.id === id);
            if (existing) {
                existing.qty++;
            } else {
                cart.push({ ...product, qty: 1 });
            }
            updateCartUI();
            toggleCart();
        }

        function changeQty(id, delta) {
            const item = cart.find(i => i.id === id);
            if (item) {
                item.qty += delta;
                if (item.qty <= 0) {
                    cart = cart.filter(i => i.id !== id);
                }
            }
            updateCartUI();
        }

        function updateCartUI() {
            const countEl = document.getElementById('cart-count');
            const itemsEl = document.getElementById('cart-items');
            const totalEl = document.getElementById('cart-total');

            const totalCount = cart.reduce((sum, item) => sum + item.qty, 0);
            countEl.innerText = totalCount;

            if (cart.length === 0) {
                itemsEl.innerHTML = `<p class="text-slate-500 text-center py-8 text-sm">Your bucket is currently empty.</p>`;
                totalEl.innerText = "Rs. 0";
                return;
            }

            let totalPrice = 0;
            itemsEl.innerHTML = cart.map(item => {
                totalPrice += item.price * item.qty;
                return `
                    <div class="flex items-center justify-between bg-slate-800 p-3 rounded-xl border border-slate-700 text-sm">
                        <div class="flex-grow pr-2">
                            <h4 class="font-semibold text-white text-xs line-clamp-1">${item.name}</h4>
                            <p class="text-emerald-400 text-xs">Rs. ${item.price} x ${item.qty}</p>
                        </div>
                        <div class="flex items-center space-x-2">
                            <button onclick="changeQty(${item.id}, -1)" class="bg-slate-700 text-white w-6 h-6 rounded-lg flex items-center justify-center hover:bg-slate-600">-</button>
                            <span class="text-xs font-bold text-white">${item.qty}</span>
                            <button onclick="changeQty(${item.id}, 1)" class="bg-slate-700 text-white w-6 h-6 rounded-lg flex items-center justify-center hover:bg-slate-600">+</button>
                        </div>
                    </div>
                `;
            }).join('');

            totalEl.innerText = `Rs. ${totalPrice}`;
        }

        function checkoutWhatsApp() {
            if (cart.length === 0) {
                alert("Your bucket is empty! Please add items before checking out.");
                return;
            }

            let message = "Hello Hypermart, I want to place an order:%0A%0A";
            let total = 0;

            cart.forEach((item, index) => {
                let sub = item.price * item.qty;
                total += sub;
                message += `${index + 1}. ${item.name} (Qty: ${item.qty}) - Rs. ${sub}%0A`;
            });

            message += `%0A*Total Bill: Rs. ${total}*%0A%0APayment Method: JazzCash / EasyPaisa / Cash on Delivery%0ADelivery Address: [Please provide your Lahore address here]`;

            const whatsappUrl = `https://wa.me/923034812714?text=${message}`;
            window.open(whatsappUrl, '_blank');
        }

        // Initialize Products on Load
        window.onload = renderProducts;
    </script>
</body>
</html>
