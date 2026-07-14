<!DOCTYPE html>
<html class="dark" lang="en">
<head>
    <meta charset="UTF-8"/>
    <meta content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no" name="viewport"/>
    <title>KICKS.DRP | The Drop</title>
    <script src="https://telegram.org/js/telegram-web-app.js"></script>
    <script src="https://cdn.tailwindcss.com?plugins=forms,container-queries"></script>
    <link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@300;400;500;600;700&family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet"/>
    <link href="https://fonts.googleapis.com/css2?family=Material+Symbols+Outlined:wght,FILL@100..700,0..1&display=swap" rel="stylesheet"/>
    <style>
        body { background-color: #121414; color: #e2e2e2; font-family: 'Inter', sans-serif; overflow-x: hidden; }
        .glass-card { background: rgba(26, 26, 26, 0.6); backdrop-filter: blur(12px); border: 1px solid rgba(255, 255, 255, 0.1); }
        .hide-scrollbar::-webkit-scrollbar { display: none; }
        .hidden { display: none; }
    </style>
</head>
<body class="antialiased">

<nav class="fixed top-0 w-full z-50 bg-surface/60 backdrop-blur-xl border-b border-white/10 flex justify-between items-center px-5 h-16">
    <div class="flex items-center gap-3">
        <span class="font-bold text-xl text-[#c3f400]">DRP</span>
    </div>
    <div class="relative" id="cart-icon">
        <span class="material-symbols-outlined text-[#c3f400] text-2xl">shopping_cart</span>
        <span id="cart-count" class="absolute -top-1 -right-1 bg-[#c3f400] text-black text-[10px] font-bold w-4 h-4 flex items-center justify-center rounded-full">0</span>
    </div>
</nav>

<main class="pt-20 pb-32 px-5">
    <!-- Store View -->
    <section id="view-store">
        <input id="search-input" class="w-full bg-[#1e2020] border border-white/5 rounded-xl py-4 pl-4 mb-6 text-white outline-none" placeholder="Search sneakers..."/>
        <div id="product-grid" class="grid grid-cols-2 gap-4">
            <!-- Products injected by JS -->
        </div>
    </section>

    <!-- Favorites View -->
    <section id="view-favorite" class="hidden">
        <h2 class="text-2xl font-bold mb-4">Favorites</h2>
        <div id="favorite-list" class="space-y-4"></div>
    </section>

    <!-- Cart/Box View -->
    <section id="view-cart" class="hidden">
        <h2 class="text-2xl font-bold mb-4">Your Cart</h2>
        <div id="cart-items" class="space-y-4"></div>
        <button id="checkout-btn" class="w-full mt-6 bg-[#c3f400] text-black font-bold py-4 rounded-xl">Checkout</button>
    </section>

    <!-- Profile View -->
    <section id="view-profile" class="hidden">
        <h2 class="text-2xl font-bold mb-4">Profile</h2>
        <div class="glass-card p-6 rounded-2xl">
            <p class="text-lg">User ID: <span id="user-id"></span></p>
            <p class="text-lg">Username: <span id="user-name"></span></p>
        </div>
    </section>
</main>

<div class="fixed bottom-0 w-full bg-[#121414]/90 backdrop-blur-xl border-t border-white/10 flex justify-around p-4">
    <button class="nav-btn" data-target="view-store"><span class="material-symbols-outlined">storefront</span></button>
    <button class="nav-btn" data-target="view-favorite"><span class="material-symbols-outlined">favorite</span></button>
    <button class="nav-btn" data-target="view-cart"><span class="material-symbols-outlined">package_2</span></button>
    <button class="nav-btn" data-target="view-profile"><span class="material-symbols-outlined">person</span></button>
</div>

<script>
    const products = [
        { id: 1, name: "AJ1 High 'Lost & Found'", brand: "Jordan", price: 485, img: "https://lh3.googleusercontent.com/aida-public/AB6AXuBPU-LVX10yf6yYVn6OL5SNYnOIHetMPddgrz2X1Yf5vfA0LwQA4UZB07YPNr2mJYyAeqTCAuFppGNrfo7b3J5I8EpF8DfEUYpdUacr5htZdM5CcCvIYY1u9n9jPokeYJjGZqtrv1SzjVZVO0Ua5v5lTF_bs1ph2decEWe22VqS-nb67-yrtXMiBvsI6wKccsszC52zjq5rGVsLtE0J7bbETXVX6B28MMl_ISmH4TApUtlxD5KCqv0c8b513H9Vst-J-ROs7FnidMpy" },
        { id: 2, name: "Yeezy 350 V2 'Carbon'", brand: "Adidas", price: 260, img: "https://lh3.googleusercontent.com/aida-public/AB6AXuC6NYGsb5OvD4TW5FEmc2fVCLrJofQo2CRjOE8GPUkisvxu8AIcvG7z4kkh9H91ZB7pqgWOcp0ntz8WFcIUj_wxLgfc7pZ0N5caiFf12HYD46UAt04D0nGxfRFgzh6uo2YwnUzjI0RzIoscBsuxdWiDWbIwkLeeJaoIwzcaxjxAL3Q2lLWz9nXSVh3zrBLJOgsMkir6INShYbOJDFyyoZs4i9lVLWAtVRCmHecj-pSw1TAcUQBBMKGkNDZTKjqhXLxiIWG2_tirosjZ" }
    ];

    let cart = JSON.parse(localStorage.getItem('cart')) || [];
    let favorites = JSON.parse(localStorage.getItem('favorites')) || [];

    function renderProducts() {
        const grid = document.getElementById('product-grid');
        grid.innerHTML = products.map(p => `
            <div class="glass-card rounded-2xl p-3 flex flex-col gap-2">
                <img src="${p.img}" class="aspect-square rounded-xl object-cover">
                <p class="text-xs uppercase">${p.brand}</p>
                <p class="font-bold text-sm">${p.name}</p>
                <div class="flex justify-between items-center">
                    <span class="text-[#c3f400] font-bold">$${p.price}</span>
                    <div>
                        <button onclick="toggleFav(${p.id})" class="material-symbols-outlined text-sm ${favorites.includes(p.id) ? 'text-red-500' : ''}">favorite</button>
                        <button onclick="addToCart(${p.id})" class="bg-[#c3f400] text-black w-8 h-8 rounded-lg">+</button>
                    </div>
                </div>
            </div>
        `).join('');
    }

    function addToCart(id) {
        cart.push(products.find(p => p.id === id));
        localStorage.setItem('cart', JSON.stringify(cart));
        updateCartCount();
        Telegram.WebApp.HapticFeedback.notificationOccurred('success');
    }

    function toggleFav(id) {
        if (favorites.includes(id)) favorites = favorites.filter(f => f !== id);
        else favorites.push(id);
        localStorage.setItem('favorites', JSON.stringify(favorites));
        renderProducts();
    }

    function updateCartCount() {
        document.getElementById('cart-count').textContent = cart.length;
    }

    // Navigation
    document.querySelectorAll('.nav-btn').forEach(btn => {
        btn.addEventListener('click', () => {
            document.querySelectorAll('main > section').forEach(s => s.classList.add('hidden'));
            document.getElementById(btn.dataset.target).classList.remove('hidden');
        });
    });

    // Profile init
    document.getElementById('user-id').textContent = Telegram.WebApp.initDataUnsafe.user?.id || 'N/A';
    document.getElementById('user-name').textContent = Telegram.WebApp.initDataUnsafe.user?.username || 'Guest';

    // Checkout
    document.getElementById('checkout-btn').addEventListener('click', () => {
        Telegram.WebApp.showPopup({ title: 'Payment', message: 'Proceed to payment?' });
    });

    renderProducts();
    updateCartCount();
    window.Telegram.WebApp.ready();
    window.Telegram.WebApp.expand();
</script>
</body>
</html>
