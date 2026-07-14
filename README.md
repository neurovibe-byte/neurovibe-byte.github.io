<!DOCTYPE html>

<html class="dark" lang="en"><head>
<meta charset="utf-8"/>
<meta content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no" name="viewport"/>
<title>KICKS.DRP | The Drop</title>
<!-- Telegram Web Apps SDK -->
<script src="https://telegram.org/js/telegram-web-app.js"></script>
<script src="https://cdn.tailwindcss.com?plugins=forms,container-queries"></script>
<link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@300;400;500;600;700&amp;family=Inter:wght@300;400;500;600;700&amp;display=swap" rel="stylesheet"/>
<link href="https://fonts.googleapis.com/css2?family=Material+Symbols+Outlined:wght,FILL@100..700,0..1&amp;display=swap" rel="stylesheet"/>
<link href="https://fonts.googleapis.com/css2?family=Material+Symbols+Outlined:wght,FILL@100..700,0..1&amp;display=swap" rel="stylesheet"/>
<script id="tailwind-config">
        tailwind.config = {
            darkMode: "class",
            theme: {
                extend: {
                    "colors": {
                        "primary-fixed": "#c3f400",
                        "on-error-container": "#ffdad6",
                        "primary": "#ffffff",
                        "on-secondary-fixed": "#1c1b1b",
                        "on-primary-fixed": "#161e00",
                        "on-surface": "#e2e2e2",
                        "inverse-on-surface": "#2f3131",
                        "surface-container-high": "#282a2b",
                        "inverse-surface": "#e2e2e2",
                        "surface-container-highest": "#333535",
                        "secondary": "#c8c6c5",
                        "on-secondary": "#313030",
                        "surface-variant": "#333535",
                        "tertiary-fixed": "#e5e2e1",
                        "on-secondary-fixed-variant": "#474746",
                        "surface-bright": "#37393a",
                        "on-secondary-container": "#b7b5b4",
                        "on-error": "#690005",
                        "tertiary-container": "#e5e2e1",
                        "primary-fixed-dim": "#abd600",
                        "on-surface-variant": "#c4c9ac",
                        "surface-container": "#1e2020",
                        "tertiary-fixed-dim": "#c9c6c5",
                        "secondary-fixed": "#e5e2e1",
                        "tertiary": "#ffffff",
                        "inverse-primary": "#506600",
                        "surface-tint": "#abd600",
                        "secondary-fixed-dim": "#c8c6c5",
                        "outline": "#8e9379",
                        "error-container": "#93000a",
                        "outline-variant": "#444933",
                        "background": "#121414",
                        "primary-container": "#c3f400",
                        "surface-container-lowest": "#0c0f0f",
                        "on-primary": "#283500",
                        "on-tertiary-fixed-variant": "#474646",
                        "surface": "#121414",
                        "on-tertiary": "#313030",
                        "secondary-container": "#474746",
                        "on-background": "#e2e2e2",
                        "surface-dim": "#121414",
                        "on-primary-fixed-variant": "#3c4d00",
                        "surface-container-low": "#1a1c1c",
                        "on-primary-container": "#556d00",
                        "error": "#ffb4ab",
                        "on-tertiary-fixed": "#1c1b1b",
                        "on-tertiary-container": "#656464"
                    },
                    "borderRadius": {
                        "DEFAULT": "0.25rem",
                        "lg": "0.5rem",
                        "xl": "0.75rem",
                        "full": "9999px"
                    },
                    "spacing": {
                        "gutter": "12px",
                        "stack-gap": "16px",
                        "container-margin": "20px",
                        "section-gap": "32px"
                    },
                    "fontFamily": {
                        "headline-lg-mobile": ["Space Grotesk"],
                        "headline-xl": ["Space Grotesk"],
                        "body-md": ["Inter"],
                        "label-sm": ["Inter"],
                        "label-bold": ["Space Grotesk"],
                        "headline-lg": ["Space Grotesk"]
                    },
                    "fontSize": {
                        "headline-lg-mobile": ["28px", { "lineHeight": "32px", "fontWeight": "700" }],
                        "headline-xl": ["40px", { "lineHeight": "44px", "letterSpacing": "-0.04em", "fontWeight": "700" }],
                        "body-md": ["16px", { "lineHeight": "24px", "fontWeight": "400" }],
                        "label-sm": ["12px", { "lineHeight": "16px", "fontWeight": "500" }],
                        "label-bold": ["14px", { "lineHeight": "18px", "fontWeight": "600" }],
                        "headline-lg": ["32px", { "lineHeight": "36px", "letterSpacing": "-0.02em", "fontWeight": "700" }]
                    }
                },
            },
        }
    </script>
<style>
        body {
            background-color: #0A0A0A;
            color: #e2e2e2;
            -webkit-tap-highlight-color: transparent;
            overflow-x: hidden;
        }
        .glass-card {
            background: rgba(26, 26, 26, 0.6);
            backdrop-filter: blur(12px);
            border: 1px solid rgba(255, 255, 255, 0.1);
        }
        .neon-glow {
            box-shadow: 0 0 15px rgba(195, 244, 0, 0.4);
        }
        .hide-scrollbar::-webkit-scrollbar {
            display: none;
        }
        .hide-scrollbar {
            -ms-overflow-style: none;
            scrollbar-width: none;
        }
        .material-symbols-outlined {
            font-variation-settings: 'FILL' 0, 'wght' 400, 'GRAD' 0, 'opsz' 24;
        }
    </style>
</head>
<body class="font-body-md text-body-md antialiased">
<!-- Header / TopAppBar -->
<nav class="fixed top-0 w-full z-50 bg-surface/60 backdrop-blur-xl border-b border-white/10 shadow-[0_20px_40px_rgba(0,0,0,0.6)] flex justify-between items-center px-container-margin h-16">
<div class="flex items-center gap-3 active:scale-95 transition-transform duration-200">
<img alt="KICKS.DRP Logo" class="w-10 h-10 rounded-full object-cover border border-primary-fixed/30" src="https://lh3.googleusercontent.com/aida-public/AB6AXuAKSQN53mFRKsEGrHMcdhUWEG93Nu732jh7kUv3SB16ep1PRuvMAljgiY38Ccmhi6h5bMgAvJlpHpNC8nXxmp5eew-jz8wcMyT-C4uXfa3Nsb8ClIYEkMrr8yMVznhg2xgHAtYgwWjqzjCM7gznjpVu7swqP2jEBGLQ4F683ZCyq8999d0LtWvBEli91oExzWV67ztMwEB31QtMhvmKdwNGM0Y0t7HCaaGasumfbpOnNjnblrAPlszIEXajeSNQICSpI1_q0xn5i1JU"/>
<span class="font-headline-lg-mobile text-headline-lg-mobile text-primary-fixed">DRP</span>
</div>
<div class="relative active:scale-95 transition-transform duration-200">
<span class="material-symbols-outlined text-primary-fixed text-2xl">shopping_cart</span>
<span class="absolute -top-1 -right-1 bg-primary-fixed text-on-primary-fixed text-[10px] font-bold w-4 h-4 flex items-center justify-center rounded-full">3</span>
</div>
</nav>
<main class="pt-20 pb-32 px-container-margin space-y-section-gap">
<!-- Hero Search & Welcome -->
<section class="space-y-4">
<div class="space-y-1">
<h2 class="font-headline-xl text-headline-xl">THE <span class="text-primary-fixed">DROP</span></h2>
<p class="text-on-surface-variant font-label-sm text-label-sm">CURATED GRAILS &amp; EXCLUSIVE RELEASES</p>
</div>
<div class="relative">
<span class="material-symbols-outlined absolute left-4 top-1/2 -translate-y-1/2 text-on-surface-variant">search</span>
<input class="w-full bg-surface-container-low border border-white/5 rounded-xl py-4 pl-12 pr-4 focus:border-primary-fixed focus:ring-0 transition-colors text-on-surface outline-none" placeholder="Search styles, brands..." type="text"/>
</div>
</section>
<!-- Hot Drops Carousel -->
<section class="space-y-4 -mx-container-margin">
<div class="px-container-margin flex justify-between items-end">
<h3 class="font-label-bold text-label-bold uppercase tracking-widest text-primary-fixed">Hot Drops</h3>
<span class="text-on-surface-variant text-[10px] font-bold uppercase tracking-tighter">View All</span>
</div>
<div class="flex overflow-x-auto gap-stack-gap px-container-margin pb-4 hide-scrollbar snap-x">
<!-- Jordan 1 -->
<div class="snap-center shrink-0 w-72 glass-card rounded-2xl overflow-hidden relative group">
<div class="absolute top-4 left-4 z-10">
<span class="bg-primary-fixed text-on-primary-fixed px-3 py-1 rounded-full text-[10px] font-bold uppercase">Limited</span>
</div>
<div class="h-48 overflow-hidden">
<img class="w-full h-full object-cover group-hover:scale-110 transition-transform duration-700" data-alt="A professional studio product shot of the Air Jordan 1 High 'Chicago' sneakers against a pitch black background. The lighting is cinematic, highlighting the vibrant red and clean white leather panels. The iconic silhouette is positioned at a dynamic 45-degree angle. High-end streetwear photography style with a premium glassmorphism aesthetic." src="https://lh3.googleusercontent.com/aida-public/AB6AXuBPU-LVX10yf6yYVn6OL5SNYnOIHetMPddgrz2X1Yf5vfA0LwQA4UZB07YPNr2mJYyAeqTCAuFppGNrfo7b3J5I8EpF8DfEUYpdUacr5htZdM5CcCvIYY1u9n9jPokeYJjGZqtrv1SzjVZVO0Ua5v5lTF_bs1ph2decEWe22VqS-nb67-yrtXMiBvsI6wKccsszC52zjq5rGVsLtE0J7bbETXVX6B28MMl_ISmH4TApUtlxD5KCqv0c8b513H9Vst-J-ROs7FnidMpy"/>
</div>
<div class="p-4 space-y-2">
<p class="text-on-surface-variant text-[10px] uppercase font-bold">Jordan Brand</p>
<h4 class="font-label-bold text-label-bold">AJ1 High 'Lost &amp; Found'</h4>
<p class="text-primary-fixed font-headline-lg-mobile text-xl">$485.00</p>
</div>
</div>
<!-- Yeezy -->
<div class="snap-center shrink-0 w-72 glass-card rounded-2xl overflow-hidden relative group">
<div class="h-48 overflow-hidden">
<img class="w-full h-full object-cover group-hover:scale-110 transition-transform duration-700" data-alt="Close-up creative product photography of Adidas Yeezy Boost 350 V2 'Carbon Beluga' sneakers. The intricate primeknit texture is highly detailed under soft neon lime studio lighting. The shoe is floating in a dark minimalist void. Elite digital boutique visual style with deep charcoal tones and sharp highlights." src="https://lh3.googleusercontent.com/aida-public/AB6AXuC6NYGsb5OvD4TW5FEmc2fVCLrJofQo2CRjOE8GPUkisvxu8AIcvG7z4kkh9H91ZB7pqgWOcp0ntz8WFcIUj_wxLgfc7pZ0N5caiFf12HYD46UAt04D0nGxfRFgzh6uo2YwnUzjI0RzIoscBsuxdWiDWbIwkLeeJaoIwzcaxjxAL3Q2lLWz9nXSVh3zrBLJOgsMkir6INShYbOJDFyyoZs4i9lVLWAtVRCmHecj-pSw1TAcUQBBMKGkNDZTKjqhXLxiIWG2_tirosjZ"/>
</div>
<div class="p-4 space-y-2">
<p class="text-on-surface-variant text-[10px] uppercase font-bold">Adidas</p>
<h4 class="font-label-bold text-label-bold">Yeezy 350 V2 'Carbon'</h4>
<p class="text-primary-fixed font-headline-lg-mobile text-xl">$260.00</p>
</div>
</div>
<!-- Dunk -->
<div class="snap-center shrink-0 w-72 glass-card rounded-2xl overflow-hidden relative group">
<div class="h-48 overflow-hidden">
<img class="w-full h-full object-cover group-hover:scale-110 transition-transform duration-700" data-alt="A high-end sneaker photography shot of Nike Dunk Low 'Panda' black and white colorway. The shoes are set on a reflective dark acrylic surface, creating a mirror effect. The lighting is cold and crisp, emphasizing the contrast of the leather. Streetwear culture aesthetic with a premium dark mode UI feel." src="https://lh3.googleusercontent.com/aida-public/AB6AXuB033vW83zVKWL1gqQjyl6jHzK0sx8CXa7IMPmfSNNzjl4vxeIXyJLyPRMj4HOLv8AwNh2hFZ3L1TaLOz-JoyIRtZDh44pyfD-lkVz2taS97UaZbgq8iy60BJfol3UKYa2eV0THzqbWl5nfO8pv8elpAUmScJBvpEQmqzxiAu7UgRBMG_966NMQ9GrWjiDzxbM09TkXZoF0qlSOXU3qnfJ8KxWlDRgIDruEU8j4Uloa130GBvu7ROXPfqN0iPbaaWDxUdpHr94kmxA-"/>
</div>
<div class="p-4 space-y-2">
<p class="text-on-surface-variant text-[10px] uppercase font-bold">Nike</p>
<h4 class="font-label-bold text-label-bold">Dunk Low 'Panda'</h4>
<p class="text-primary-fixed font-headline-lg-mobile text-xl">$185.00</p>
</div>
</div>
</div>
</section>
<!-- Filters -->
<section class="flex gap-3 overflow-x-auto hide-scrollbar">
<button class="px-6 py-2 rounded-full bg-primary-fixed text-on-primary-fixed font-label-bold text-label-sm neon-glow whitespace-nowrap">All</button>
<button class="px-6 py-2 rounded-full glass-card text-on-surface font-label-bold text-label-sm whitespace-nowrap hover:border-primary-fixed/50 transition-colors">Nike</button>
<button class="px-6 py-2 rounded-full glass-card text-on-surface font-label-bold text-label-sm whitespace-nowrap hover:border-primary-fixed/50 transition-colors">Jordan</button>
<button class="px-6 py-2 rounded-full glass-card text-on-surface font-label-bold text-label-sm whitespace-nowrap hover:border-primary-fixed/50 transition-colors">Adidas</button>
<button class="px-6 py-2 rounded-full glass-card text-on-surface font-label-bold text-label-sm whitespace-nowrap hover:border-primary-fixed/50 transition-colors">New Balance</button>
</section>
<!-- Product Grid -->
<section class="grid grid-cols-2 gap-4 pb-12">
<!-- Product 1 -->
<div class="glass-card rounded-2xl p-3 flex flex-col space-y-3 relative group active:scale-95 transition-transform duration-200">
<div class="aspect-square rounded-xl overflow-hidden bg-surface-container-low">
<img class="w-full h-full object-cover group-hover:scale-110 transition-transform duration-500" data-alt="An atmospheric studio shot of a Nike Air Max Plus sneaker in a vibrant sunset colorway. The sneaker is isolated on a dark, textured gray background. Volumetric lighting casts long, soft shadows. High-resolution commercial fashion photography with neon accents for an elite digital store." src="https://lh3.googleusercontent.com/aida-public/AB6AXuDFRN-NlBuUWUljFUpMCP8ezD42a-LhdOhDIOYBznH1LvWGCpmqQ4ITp8RTtpRHiK1p3fQ4-lLscAcP2nVkYWrP7JjQ12v-1W1Oeo15rEMuCL1VNteNxynjiUECvZce6P2EA6St6t-QV_58lwJjc-kISuzugzOg2vTL2Z_V6FbZP2KP8Wm54WZ-pW2PRxPUMke9rdZTqEHvsgHLzSu2OZciWwYE_-0SSIpOGraueYRY4el8qDIkgWbMY42LCGLwe3j1-s-vHsk_SAVT"/>
</div>
<div class="space-y-1">
<h5 class="text-on-surface-variant text-[10px] uppercase font-bold">Nike</h5>
<p class="font-label-bold text-label-sm truncate">Air Max Plus 'Sunset'</p>
<div class="flex justify-between items-center">
<span class="text-primary-fixed font-bold">$190</span>
<button class="bg-primary-fixed text-on-primary-fixed w-8 h-8 rounded-lg flex items-center justify-center hover:scale-110 active:scale-90 transition-all">
<span class="material-symbols-outlined text-xl">add</span>
</button>
</div>
</div>
</div>
<!-- Product 2 -->
<div class="glass-card rounded-2xl p-3 flex flex-col space-y-3 relative group active:scale-95 transition-transform duration-200">
<div class="aspect-square rounded-xl overflow-hidden bg-surface-container-low">
<img class="w-full h-full object-cover group-hover:scale-110 transition-transform duration-500" data-alt="Luxury fashion photography of a Jordan 4 'Military Black' sneaker. The shoe is positioned vertically on its heel on a black mirrored surface. Soft purple and blue rim lighting creates a cyber-fashion vibe. Deep charcoal color palette with high-key contrast highlights." src="https://lh3.googleusercontent.com/aida-public/AB6AXuDLDP0qL2eHBhKZxJKC70YYwXgLd1jSbsoU5cnQReojVoB2fO8efMxbwMdBA4XB64pMbr9oL7PhdNIsfj_pkl2usF1U2NJE_DirS9pipvHyRSiIMqhWNHOnvZ4PA3l6ooAvJFugl6mRnLMjw6r66ppHD-2ALt9lL92o95OTXYGFPwpwEjaI17wvZqoQZNrmSHeivX0WFLA_x_RfzMF3sOWZHOtAhb-gc5ARKtc-gYtRhNQO0UNGygtwIJjKM1ER1cWCz1A94vJg0iN9"/>
</div>
<div class="space-y-1">
<h5 class="text-on-surface-variant text-[10px] uppercase font-bold">Jordan</h5>
<p class="font-label-bold text-label-sm truncate">AJ4 'Military Black'</p>
<div class="flex justify-between items-center">
<span class="text-primary-fixed font-bold">$410</span>
<button class="bg-primary-fixed text-on-primary-fixed w-8 h-8 rounded-lg flex items-center justify-center hover:scale-110 active:scale-90 transition-all">
<span class="material-symbols-outlined text-xl">add</span>
</button>
</div>
</div>
</div>
<!-- Product 3 -->
<div class="glass-card rounded-2xl p-3 flex flex-col space-y-3 relative group active:scale-95 transition-transform duration-200">
<div class="aspect-square rounded-xl overflow-hidden bg-surface-container-low">
<img class="w-full h-full object-cover group-hover:scale-110 transition-transform duration-500" data-alt="Studio photography of a New Balance 550 'White Green' vintage basketball sneaker. The lighting is warm and retro-inspired, emphasizing the cream and forest green tones. The setting is a minimalist studio with industrial textures. Premium aesthetic for an underground fashion boutique." src="https://lh3.googleusercontent.com/aida-public/AB6AXuDCkjT5eJRursiL2re-66655QMjbzIyIV5ckOQzz6p04nUW630MJjeffpE00VReJJU80vyj-SUuG_k7s180wD7mDqj0pZ-1pJnvGpi2_XwN8H1FXOS2f24jckiFpFeXhdcyG61D3T-1HgYKe1CgJou5qRUJ130oMueu3IGXfVaUFwq6F8pVhmIcK9rO2urEo4vxLiOONGTKpU9zrabHyIVmUG4ZPxE3eOInEQSDIYSOqvzTgoY1BQwmzHOIriuO3RcHdbFnGBs5xmoP"/>
</div>
<div class="space-y-1">
<h5 class="text-on-surface-variant text-[10px] uppercase font-bold">New Balance</h5>
<p class="font-label-bold text-label-sm truncate">NB 550 Vintage Green</p>
<div class="flex justify-between items-center">
<span class="text-primary-fixed font-bold">$145</span>
<button class="bg-primary-fixed text-on-primary-fixed w-8 h-8 rounded-lg flex items-center justify-center hover:scale-110 active:scale-90 transition-all">
<span class="material-symbols-outlined text-xl">add</span>
</button>
</div>
</div>
</div>
<!-- Product 4 -->
<div class="glass-card rounded-2xl p-3 flex flex-col space-y-3 relative group active:scale-95 transition-transform duration-200">
<div class="aspect-square rounded-xl overflow-hidden bg-surface-container-low relative">
<div class="absolute top-2 right-2 bg-red-600 text-white text-[8px] font-black px-2 py-1 rounded italic uppercase">Sold Out</div>
<img class="w-full h-full object-cover opacity-50 grayscale" data-alt="Experimental fashion photography of a Nike x Off-White Terra Forma sneaker. The complex, chunky silhouette is highlighted by sharp, high-key white lighting against a deep obsidian black backdrop. The mood is avant-garde and technologically aggressive. Elite streetwear digital experience aesthetic." src="https://lh3.googleusercontent.com/aida-public/AB6AXuCBPltsl_N5Gq1efKwNhL4-mwcZMx-y26KWrTmCwaD4yUfZtHCI97mAYTNhLd90K-XA3mbmKpnUzOmfBzsMCV6lWwzHaxTzHu2VwgiKCB9YE4DyX5DDtDxvzOVkdnJBjdnDaxT7NwIPlknaPKdJtY_62nhaYc8xt-YNIaISy5nRf95-TCouV4MwugDPhqTxyKGCPPFxzk5X0Owb0n3NUVI8aWtDy6-ldQhM-pTD64yGyy3D7Ps4K8ykOGpLSW5d_hdMxrC7EZK-FWsH"/>
</div>
<div class="space-y-1">
<h5 class="text-on-surface-variant text-[10px] uppercase font-bold">Off-White</h5>
<p class="font-label-bold text-label-sm truncate">Terra Forma 'Volt'</p>
<div class="flex justify-between items-center">
<span class="text-on-surface-variant font-bold">$210</span>
<button class="bg-surface-container-highest text-on-surface-variant w-8 h-8 rounded-lg flex items-center justify-center opacity-50 cursor-not-allowed" disabled="">
<span class="material-symbols-outlined text-xl">close</span>
</button>
</div>
</div>
</div>
</section>
</main>
<!-- Bottom Navigation Shell -->
<div class="fixed bottom-4 left-container-margin right-container-margin rounded-full z-50 bg-surface-container/60 backdrop-blur-xl border border-white/10 shadow-[0_20px_40px_rgba(0,0,0,0.6)] flex justify-around items-center h-16 px-gutter">
<!-- Active Tab: storefront -->
<a class="flex flex-col items-center justify-center bg-primary-fixed text-on-primary-fixed rounded-full w-12 h-12 shadow-[0_0_15px_rgba(195,244,0,0.4)] active:scale-90 transition-all duration-300 ease-out" href="#">
<span class="material-symbols-outlined" style="font-variation-settings: 'FILL' 1;">storefront</span>
</a>
<a class="flex flex-col items-center justify-center text-on-surface-variant w-12 h-12 hover:text-primary-fixed active:scale-90 transition-all duration-300 ease-out" href="#">
<span class="material-symbols-outlined">favorite</span>
</a>
<a class="flex flex-col items-center justify-center text-on-surface-variant w-12 h-12 hover:text-primary-fixed active:scale-90 transition-all duration-300 ease-out" href="#">
<span class="material-symbols-outlined">package_2</span>
</a>
<a class="flex flex-col items-center justify-center text-on-surface-variant w-12 h-12 hover:text-primary-fixed active:scale-90 transition-all duration-300 ease-out" href="#">
<span class="material-symbols-outlined">person</span>
</a>
</div>
<!-- Background Atmospheric Effect -->
<div class="fixed inset-0 pointer-events-none -z-10">
<div class="absolute top-[-10%] right-[-10%] w-[500px] h-[500px] bg-primary-fixed/5 rounded-full blur-[120px]"></div>
<div class="absolute bottom-[20%] left-[-20%] w-[400px] h-[400px] bg-primary-fixed/5 rounded-full blur-[100px]"></div>
</div>
<script>
        // Micro-interactions for buttons and tabs
        document.querySelectorAll('button, a').forEach(el => {
            el.addEventListener('touchstart', () => {
                el.style.transform = 'scale(0.95)';
            });
            el.addEventListener('touchend', () => {
                el.style.transform = '';
            });
        });

        // Simple horizontal scroll detection for active drop indicator
        const carousel = document.querySelector('.overflow-x-auto');
        carousel.addEventListener('scroll', () => {
            // Can implement progress indicators here if needed
        });
        
        // Initialize Telegram Web App
        window.Telegram.WebApp.ready();
        window.Telegram.WebApp.expand();
    </script>
</body></html>
