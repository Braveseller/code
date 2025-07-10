<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>BraveSeller - Future of Digital Marketplace</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Orbitron:wght@400;500;600;700&family=Roboto:wght@300;400;500;700&display=swap');
        
        :root {
            --primary: #00f7ff;
            --secondary: #7000ff;
            --dark: #0a0a20;
            --light: #f0f8ff;
        }
        
        body {
            font-family: 'Roboto', sans-serif;
            background-color: var(--dark);
            color: var(--light);
            overflow-x: hidden;
        }
        
        .futuristic-heading {
            font-family: 'Orbitron', sans-serif;
        }
        
        .glow {
            text-shadow: 0 0 10px var(--primary), 0 0 20px var(--primary), 0 0 30px var(--primary);
        }
        
        .neon-border {
            border: 2px solid var(--primary);
            box-shadow: 0 0 10px var(--primary), inset 0 0 10px var(--primary);
        }
        
        .glass-effect {
            background: rgba(255, 255, 255, 0.05);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        .hover-scale {
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }
        
        .hover-scale:hover {
            transform: translateY(-5px) scale(1.02);
            box-shadow: 0 10px 20px rgba(0, 247, 255, 0.3);
        }
        
        .gradient-bg {
            background: linear-gradient(135deg, #0a0a20 0%, #1a1a40 100%);
        }
        
        .hero-pattern {
            background-image: 
                radial-gradient(circle at 25% 25%, rgba(0, 247, 255, 0.1) 1%, transparent 10%),
                radial-gradient(circle at 75% 75%, rgba(112, 0, 255, 0.1) 1%, transparent 10%),
                radial-gradient(circle at 50% 50%, rgba(0, 247, 255, 0.05) 1%, transparent 30%);
            background-size: 60px 60px, 60px 60px, 120px 120px;
        }
        
        /* Custom scrollbar */
        ::-webkit-scrollbar {
            width: 8px;
        }
        
        ::-webkit-scrollbar-track {
            background: var(--dark);
        }
        
        ::-webkit-scrollbar-thumb {
            background: var(--primary);
            border-radius: 4px;
        }
        
        /* Animations */
        @keyframes float {
            0% { transform: translateY(0px); }
            50% { transform: translateY(-10px); }
            100% { transform: translateY(0px); }
        }
        
        .float-animation {
            animation: float 4s ease-in-out infinite;
        }
        
        @keyframes pulse {
            0% { opacity: 0.6; }
            50% { opacity: 1; }
            100% { opacity: 0.6; }
        }
        
        .pulse-animation {
            animation: pulse 2s infinite;
        }
        
        @keyframes rotate {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }
        
        .rotate-animation {
            animation: rotate 20s linear infinite;
        }
        
        @keyframes glow {
            0% { filter: drop-shadow(0 0 5px var(--primary)); }
            50% { filter: drop-shadow(0 0 15px var(--primary)); }
            100% { filter: drop-shadow(0 0 5px var(--primary)); }
        }
        
        .glow-animation {
            animation: glow 3s ease-in-out infinite;
        }
        
        @keyframes expand {
            0% { transform: scale(1); }
            50% { transform: scale(1.1); }
            100% { transform: scale(1); }
        }
        
        .expand-animation {
            animation: expand 2s ease-in-out infinite;
        }
        
        .cart-count {
            position: absolute;
            top: -8px;
            right: -8px;
            background-color: var(--secondary);
            color: white;
            border-radius: 50%;
            width: 20px;
            height: 20px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 12px;
        }
        
        /* Product card hover effects */
        .product-card {
            transition: all 0.4s ease;
            transform-style: preserve-3d;
        }
        
        .product-card:hover .product-image {
            transform: translateY(-10px);
        }
        
        .product-card:hover .product-details {
            transform: translateY(5px);
        }
        
        .product-image {
            transition: transform 0.4s ease;
        }
        
        .product-details {
            transition: transform 0.4s ease;
        }
        
        .product-card:hover .hover-show {
            opacity: 1;
            transform: translateY(0);
        }
        
        .hover-show {
            opacity: 0;
            transform: translateY(10px);
            transition: all 0.4s ease;
        }
        
        /* Button hover effects */
        .btn-hover-effect {
            position: relative;
            overflow: hidden;
            transition: all 0.3s ease;
        }
        
        .btn-hover-effect:before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255,255,255,0.2), transparent);
            transition: all 0.6s ease;
        }
        
        .btn-hover-effect:hover:before {
            left: 100%;
        }
        
        /* Category hover effects */
        .category-item {
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }
        
        .category-item:hover .category-overlay {
            opacity: 1;
        }
        
        .category-overlay {
            position: absolute;
            inset: 0;
            background: linear-gradient(to top, rgba(0,247,255,0.3), transparent);
            opacity: 0;
            transition: all 0.3s ease;
        }
        
        /* Feature hover effects */
        .feature-icon {
            transition: all 0.4s ease;
        }
        
        .feature-card:hover .feature-icon {
            transform: rotateY(180deg);
        }
    </style>
</head>
<body>
    <!-- Navigation -->
    <nav class="glass-effect fixed w-full z-50 px-4 py-3">
        <div class="container mx-auto flex justify-between items-center">
            <div class="flex items-center">
                <div class="text-3xl futuristic-heading font-bold">
                    <span class="text-white">Brave</span><span class="text-transparent bg-clip-text bg-gradient-to-r from-cyan-400 to-blue-500">Seller</span>
                </div>
            </div>
            
            <div class="hidden md:flex space-x-8">
                <a href="#" class="text-white hover:text-cyan-400 transition-colors">Home</a>
                <a href="#products" class="text-white hover:text-cyan-400 transition-colors">Products</a>
                <a href="#categories" class="text-white hover:text-cyan-400 transition-colors">Categories</a>
                <a href="#features" class="text-white hover:text-cyan-400 transition-colors">Features</a>
                <a href="#contact" class="text-white hover:text-cyan-400 transition-colors">Contact</a>
            </div>
            
            <div class="flex items-center space-x-4">
                <div class="relative">
                    <button id="cartButton" class="text-white p-2 rounded-full hover:bg-gray-800 transition-colors">
                        <i class="fas fa-shopping-cart"></i>
                        <span id="cartCount" class="cart-count">0</span>
                    </button>
                </div>
                <button class="hidden md:block bg-gradient-to-r from-cyan-400 to-blue-500 text-white px-6 py-2 rounded-full hover:opacity-90 transition-opacity btn-hover-effect">
                    Sign In
                </button>
                <button class="md:hidden text-white">
                    <i class="fas fa-bars"></i>
                </button>
            </div>
        </div>
    </nav>
    
    <!-- Mobile Menu (Hidden by default) -->
    <div id="mobileMenu" class="fixed inset-0 bg-gray-900 bg-opacity-95 z-40 hidden flex-col justify-center items-center">
        <button id="closeMenu" class="absolute top-5 right-5 text-white text-2xl">
            <i class="fas fa-times"></i>
        </button>
        <div class="flex flex-col space-y-6 text-center">
            <a href="#" class="text-white text-xl hover:text-cyan-400 transition-colors">Home</a>
            <a href="#products" class="text-white text-xl hover:text-cyan-400 transition-colors">Products</a>
            <a href="#categories" class="text-white text-xl hover:text-cyan-400 transition-colors">Categories</a>
            <a href="#features" class="text-white text-xl hover:text-cyan-400 transition-colors">Features</a>
            <a href="#contact" class="text-white text-xl hover:text-cyan-400 transition-colors">Contact</a>
            <button class="bg-gradient-to-r from-cyan-400 to-blue-500 text-white px-6 py-2 rounded-full hover:opacity-90 transition-opacity mt-4 btn-hover-effect">
                Sign In
            </button>
        </div>
    </div>
    
    <!-- Hero Section -->
    <section class="hero-pattern min-h-screen flex items-center pt-20">
        <div class="container mx-auto px-4 py-16">
            <div class="flex flex-col md:flex-row items-center">
                <div class="md:w-1/2 mb-10 md:mb-0">
                    <h1 class="text-4xl md:text-6xl futuristic-heading font-bold mb-6">
                        <span class="text-transparent bg-clip-text bg-gradient-to-r from-cyan-400 to-blue-500">Future</span> of 
                        <span class="block">Digital Marketplace</span>
                    </h1>
                    <p class="text-xl mb-8 text-gray-300 max-w-lg">
                        Experience the next generation of online shopping with immersive interfaces and cutting-edge technology.
                    </p>
                    <div class="flex flex-col sm:flex-row space-y-4 sm:space-y-0 sm:space-x-4">
                        <button class="bg-gradient-to-r from-cyan-400 to-blue-500 text-white px-8 py-3 rounded-full hover:opacity-90 transition-opacity font-medium btn-hover-effect">
                            Explore Products
                        </button>
                        <button class="border border-cyan-400 text-cyan-400 px-8 py-3 rounded-full hover:bg-cyan-400 hover:bg-opacity-10 transition-colors">
                            Learn More
                        </button>
                    </div>
                    <div class="mt-10 flex items-center space-x-6">
                        <div class="flex -space-x-2">
                            <div class="w-10 h-10 rounded-full bg-gradient-to-r from-purple-500 to-pink-500"></div>
                            <div class="w-10 h-10 rounded-full bg-gradient-to-r from-yellow-500 to-red-500"></div>
                            <div class="w-10 h-10 rounded-full bg-gradient-to-r from-green-500 to-teal-500"></div>
                        </div>
                        <p class="text-sm text-gray-300">
                            <span class="text-white font-bold">5,000+</span> satisfied customers
                        </p>
                    </div>
                </div>
                <div class="md:w-1/2 relative">
                    <div class="relative float-animation">
                        <svg class="w-full h-auto" viewBox="0 0 500 400" xmlns="http://www.w3.org/2000/svg">
                            <!-- Futuristic 3D Store Illustration -->
                            <defs>
                                <linearGradient id="storeGradient" x1="0%" y1="0%" x2="100%" y2="100%">
                                    <stop offset="0%" stop-color="#00f7ff" stop-opacity="0.2"/>
                                    <stop offset="100%" stop-color="#7000ff" stop-opacity="0.2"/>
                                </linearGradient>
                                <linearGradient id="glowGradient" x1="0%" y1="0%" x2="100%" y2="100%">
                                    <stop offset="0%" stop-color="#00f7ff"/>
                                    <stop offset="100%" stop-color="#7000ff"/>
                                </linearGradient>
                            </defs>
                            
                            <!-- Base platform -->
                            <ellipse cx="250" cy="320" rx="180" ry="50" fill="url(#storeGradient)" opacity="0.6" class="pulse-animation"/>
                            
                            <!-- Holographic display -->
                            <g class="pulse-animation">
                                <rect x="150" y="120" width="200" height="200" rx="10" fill="rgba(255,255,255,0.05)" stroke="url(#glowGradient)" stroke-width="2"/>
                                <line x1="150" y1="160" x2="350" y2="160" stroke="url(#glowGradient)" stroke-width="1"/>
                                
                                <!-- Products -->
                                <rect x="170" y="180" width="50" height="50" rx="5" fill="rgba(0,247,255,0.2)" stroke="#00f7ff" stroke-width="1" class="product-item"/>
                                <rect x="240" y="180" width="50" height="50" rx="5" fill="rgba(112,0,255,0.2)" stroke="#7000ff" stroke-width="1" class="product-item"/>
                                <rect x="310" y="180" width="20" height="50" rx="5" fill="rgba(255,255,255,0.1)" stroke="#ffffff" stroke-width="1"/>
                                
                                <rect x="170" y="250" width="50" height="50" rx="5" fill="rgba(112,0,255,0.2)" stroke="#7000ff" stroke-width="1" class="product-item"/>
                                <rect x="240" y="250" width="50" height="50" rx="5" fill="rgba(0,247,255,0.2)" stroke="#00f7ff" stroke-width="1" class="product-item"/>
                                <rect x="310" y="250" width="20" height="50" rx="5" fill="rgba(255,255,255,0.1)" stroke="#ffffff" stroke-width="1"/>
                            </g>
                            
                            <!-- Floating elements -->
                            <circle cx="120" cy="150" r="15" fill="rgba(0,247,255,0.3)" stroke="#00f7ff" stroke-width="1" class="pulse-animation"/>
                            <circle cx="380" cy="200" r="20" fill="rgba(112,0,255,0.3)" stroke="#7000ff" stroke-width="1" class="pulse-animation"/>
                            <circle cx="100" cy="250" r="10" fill="rgba(255,255,255,0.2)" stroke="#ffffff" stroke-width="1" class="pulse-animation"/>
                            <circle cx="400" cy="120" r="12" fill="rgba(0,247,255,0.3)" stroke="#00f7ff" stroke-width="1" class="pulse-animation"/>
                            
                            <!-- Connection lines -->
                            <line x1="120" y1="150" x2="170" y2="180" stroke="#00f7ff" stroke-width="1" stroke-dasharray="5,5"/>
                            <line x1="380" y1="200" x2="310" y2="200" stroke="#7000ff" stroke-width="1" stroke-dasharray="5,5"/>
                            <line x1="100" y1="250" x2="170" y2="250" stroke="#ffffff" stroke-width="1" stroke-dasharray="5,5"/>
                            <line x1="400" y1="120" x2="350" y2="140" stroke="#00f7ff" stroke-width="1" stroke-dasharray="5,5"/>
                            
                            <!-- Rotating ring -->
                            <circle cx="250" cy="220" r="100" fill="none" stroke="url(#glowGradient)" stroke-width="1" stroke-dasharray="5,10" class="rotate-animation"/>
                        </svg>
                    </div>
                    <div class="absolute -bottom-10 left-1/2 transform -translate-x-1/2 w-3/4 h-10 bg-cyan-400 blur-2xl opacity-30 rounded-full"></div>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Stats Section -->
    <section class="py-16 gradient-bg">
        <div class="container mx-auto px-4">
            <div class="grid grid-cols-2 md:grid-cols-4 gap-8 text-center">
                <div class="glass-effect p-6 rounded-xl hover-scale">
                    <h3 class="text-3xl md:text-4xl font-bold text-cyan-400 mb-2 counter" data-target="5000">0</h3>
                    <p class="text-gray-300">Active Users</p>
                </div>
                <div class="glass-effect p-6 rounded-xl hover-scale">
                    <h3 class="text-3xl md:text-4xl font-bold text-cyan-400 mb-2 counter" data-target="10000">0</h3>
                    <p class="text-gray-300">Products Sold</p>
                </div>
                <div class="glass-effect p-6 rounded-xl hover-scale">
                    <h3 class="text-3xl md:text-4xl font-bold text-cyan-400 mb-2 counter" data-target="98">0</h3>
                    <p class="text-gray-300">Customer Satisfaction</p>
                </div>
                <div class="glass-effect p-6 rounded-xl hover-scale">
                    <h3 class="text-3xl md:text-4xl font-bold text-cyan-400 mb-2 counter" data-target="150">0</h3>
                    <p class="text-gray-300">Countries Served</p>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Categories Section -->
    <section id="categories" class="py-20">
        <div class="container mx-auto px-4">
            <div class="text-center mb-16">
                <h2 class="text-3xl md:text-4xl futuristic-heading font-bold mb-4">
                    <span class="text-transparent bg-clip-text bg-gradient-to-r from-cyan-400 to-blue-500">Explore</span> Categories
                </h2>
                <p class="text-gray-300 max-w-2xl mx-auto">
                    Discover our futuristic product collections across various categories.
                </p>
            </div>
            
            <div class="grid grid-cols-2 md:grid-cols-4 gap-6">
                <!-- Category 1 -->
                <div class="category-item rounded-xl overflow-hidden hover-scale cursor-pointer">
                    <div class="h-40 bg-gradient-to-br from-cyan-900 to-blue-900 relative flex items-center justify-center">
                        <svg class="w-16 h-16 text-cyan-400 glow-animation" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="1" d="M12 18h.01M8 21h8a2 2 0 002-2V5a2 2 0 00-2-2H8a2 2 0 00-2 2v14a2 2 0 002 2z"></path>
                        </svg>
                        <div class="category-overlay"></div>
                    </div>
                    <div class="glass-effect p-4">
                        <h3 class="text-lg font-bold text-center futuristic-heading">Tech Gadgets</h3>
                    </div>
                </div>
                
                <!-- Category 2 -->
                <div class="category-item rounded-xl overflow-hidden hover-scale cursor-pointer">
                    <div class="h-40 bg-gradient-to-br from-purple-900 to-indigo-900 relative flex items-center justify-center">
                        <svg class="w-16 h-16 text-purple-400 glow-animation" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="1" d="M9.75 17L9 20l-1 1h8l-1-1-.75-3M3 13h18M5 17h14a2 2 0 002-2V5a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"></path>
                        </svg>
                        <div class="category-overlay"></div>
                    </div>
                    <div class="glass-effect p-4">
                        <h3 class="text-lg font-bold text-center futuristic-heading">Smart Home</h3>
                    </div>
                </div>
                
                <!-- Category 3 -->
                <div class="category-item rounded-xl overflow-hidden hover-scale cursor-pointer">
                    <div class="h-40 bg-gradient-to-br from-blue-900 to-teal-900 relative flex items-center justify-center">
                        <svg class="w-16 h-16 text-teal-400 glow-animation" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="1" d="M15.536 8.464a5 5 0 010 7.072m2.828-9.9a9 9 0 010 12.728M5.586 15H4a1 1 0 01-1-1v-4a1 1 0 011-1h1.586l4.707-4.707C10.923 3.663 12 4.109 12 5v14c0 .891-1.077 1.337-1.707.707L5.586 15z"></path>
                        </svg>
                        <div class="category-overlay"></div>
                    </div>
                    <div class="glass-effect p-4">
                        <h3 class="text-lg font-bold text-center futuristic-heading">Audio Systems</h3>
                    </div>
                </div>
                
                <!-- Category 4 -->
                <div class="category-item rounded-xl overflow-hidden hover-scale cursor-pointer">
                    <div class="h-40 bg-gradient-to-br from-pink-900 to-red-900 relative flex items-center justify-center">
                        <svg class="w-16 h-16 text-pink-400 glow-animation" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="1" d="M12 6.253v13m0-13C10.832 5.477 9.246 5 7.5 5S4.168 5.477 3 6.253v13C4.168 18.477 5.754 18 7.5 18s3.332.477 4.5 1.253m0-13C13.168 5.477 14.754 5 16.5 5c1.747 0 3.332.477 4.5 1.253v13C19.832 18.477 18.247 18 16.5 18c-1.746 0-3.332.477-4.5 1.253"></path>
                        </svg>
                        <div class="category-overlay"></div>
                    </div>
                    <div class="glass-effect p-4">
                        <h3 class="text-lg font-bold text-center futuristic-heading">Digital Art</h3>
                    </div>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Featured Products -->
    <section id="products" class="py-20 gradient-bg">
        <div class="container mx-auto px-4">
            <div class="text-center mb-16">
                <h2 class="text-3xl md:text-4xl futuristic-heading font-bold mb-4">
                    <span class="text-transparent bg-clip-text bg-gradient-to-r from-cyan-400 to-blue-500">Featured</span> Products
                </h2>
                <p class="text-gray-300 max-w-2xl mx-auto">
                    Discover our most innovative and cutting-edge products.
                </p>
            </div>
            
            <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-8">
                <!-- Product 1 -->
                <div class="glass-effect rounded-xl overflow-hidden product-card">
                    <div class="h-48 bg-gradient-to-br from-cyan-900 to-blue-900 relative overflow-hidden product-image">
                        <svg class="absolute inset-0 w-full h-full" viewBox="0 0 200 150" xmlns="http://www.w3.org/2000/svg">
                            <rect x="50" y="20" width="100" height="100" rx="10" fill="rgba(255,255,255,0.1)" stroke="#00f7ff" stroke-width="2"/>
                            <circle cx="100" cy="70" r="30" fill="rgba(0,247,255,0.2)" stroke="#00f7ff" stroke-width="2"/>
                            <path d="M70 70 L130 70" stroke="#00f7ff" stroke-width="2"/>
                            <path d="M100 40 L100 100" stroke="#00f7ff" stroke-width="2"/>
                        </svg>
                        <div class="absolute top-2 right-2 bg-cyan-400 text-xs text-black font-bold px-2 py-1 rounded-full">
                            NEW
                        </div>
                    </div>
                    <div class="p-6 product-details">
                        <h3 class="text-xl font-bold mb-2 futuristic-heading">Quantum Smartwatch</h3>
                        <p class="text-gray-400 text-sm mb-4">Advanced health tracking with holographic display</p>
                        <div class="flex justify-between items-center">
                            <div>
                                <span class="text-cyan-400 font-bold">$129.99</span>
                                <span class="text-gray-500 text-sm line-through ml-2">$199.99</span>
                            </div>
                            <button class="add-to-cart bg-gradient-to-r from-cyan-400 to-blue-500 text-white p-2 rounded-full hover:opacity-90 transition-opacity btn-hover-effect">
                                <i class="fas fa-plus"></i>
                            </button>
                        </div>
                        <div class="mt-4 hover-show">
                            <button class="w-full border border-cyan-400 text-cyan-400 py-2 rounded-full hover:bg-cyan-400 hover:bg-opacity-10 transition-colors">
                                View Details
                            </button>
                        </div>
                    </div>
                </div>
                
                <!-- Product 2 -->
                <div class="glass-effect rounded-xl overflow-hidden product-card">
                    <div class="h-48 bg-gradient-to-br from-purple-900 to-indigo-900 relative overflow-hidden product-image">
                        <svg class="absolute inset-0 w-full h-full" viewBox="0 0 200 150" xmlns="http://www.w3.org/2000/svg">
                            <rect x="60" y="30" width="80" height="80" rx="5" fill="rgba(255,255,255,0.1)" stroke="#7000ff" stroke-width="2"/>
                            <rect x="70" y="40" width="60" height="40" rx="3" fill="rgba(112,0,255,0.2)" stroke="#7000ff" stroke-width="1"/>
                            <rect x="75" y="90" width="20" height="10" rx="2" fill="rgba(112,0,255,0.3)" stroke="#7000ff" stroke-width="1"/>
                            <rect x="105" y="90" width="20" height="10" rx="2" fill="rgba(112,0,255,0.3)" stroke="#7000ff" stroke-width="1"/>
                        </svg>
                        <div class="absolute top-2 right-2 bg-purple-400 text-xs text-black font-bold px-2 py-1 rounded-full">
                            POPULAR
                        </div>
                    </div>
                    <div class="p-6 product-details">
                        <h3 class="text-xl font-bold mb-2 futuristic-heading">NeoLens AR Glasses</h3>
                        <p class="text-gray-400 text-sm mb-4">Augmented reality for everyday life</p>
                        <div class="flex justify-between items-center">
                            <div>
                                <span class="text-cyan-400 font-bold">$249.99</span>
                                <span class="text-gray-500 text-sm line-through ml-2">$349.99</span>
                            </div>
                            <button class="add-to-cart bg-gradient-to-r from-cyan-400 to-blue-500 text-white p-2 rounded-full hover:opacity-90 transition-opacity btn-hover-effect">
                                <i class="fas fa-plus"></i>
                            </button>
                        </div>
                        <div class="mt-4 hover-show">
                            <button class="w-full border border-cyan-400 text-cyan-400 py-2 rounded-full hover:bg-cyan-400 hover:bg-opacity-10 transition-colors">
                                View Details
                            </button>
                        </div>
                    </div>
                </div>
                
                <!-- Product 3 -->
                <div class="glass-effect rounded-xl overflow-hidden product-card">
                    <div class="h-48 bg-gradient-to-br from-blue-900 to-teal-900 relative overflow-hidden product-image">
                        <svg class="absolute inset-0 w-full h-full" viewBox="0 0 200 150" xmlns="http://www.w3.org/2000/svg">
                            <path d="M70 40 L130 40 L150 70 L130 100 L70 100 L50 70 Z" fill="rgba(0,247,255,0.1)" stroke="#00f7ff" stroke-width="2"/>
                            <circle cx="100" cy="70" r="20" fill="rgba(0,247,255,0.2)" stroke="#00f7ff" stroke-width="1"/>
                            <path d="M90 65 L110 65 L110 75 L90 75 Z" fill="rgba(0,247,255,0.3)" stroke="#00f7ff" stroke-width="1"/>
                        </svg>
                        <div class="absolute top-2 right-2 bg-teal-400 text-xs text-black font-bold px-2 py-1 rounded-full">
                            TRENDING
                        </div>
                    </div>
                    <div class="p-6 product-details">
                        <h3 class="text-xl font-bold mb-2 futuristic-heading">EchoSphere Speaker</h3>
                        <p class="text-gray-400 text-sm mb-4">360° sound with holographic assistant</p>
                        <div class="flex justify-between items-center">
                            <div>
                                <span class="text-cyan-400 font-bold">$89.99</span>
                                <span class="text-gray-500 text-sm line-through ml-2">$119.99</span>
                            </div>
                            <button class="add-to-cart bg-gradient-to-r from-cyan-400 to-blue-500 text-white p-2 rounded-full hover:opacity-90 transition-opacity btn-hover-effect">
                                <i class="fas fa-plus"></i>
                            </button>
                        </div>
                        <div class="mt-4 hover-show">
                            <button class="w-full border border-cyan-400 text-cyan-400 py-2 rounded-full hover:bg-cyan-400 hover:bg-opacity-10 transition-colors">
                                View Details
                            </button>
                        </div>
                    </div>
                </div>
            </div>
            
            <div class="text-center mt-12">
                <button class="bg-transparent border-2 border-cyan-400 text-cyan-400 px-8 py-3 rounded-full hover:bg-cyan-400 hover:bg-opacity-10 transition-colors btn-hover-effect">
                    View All Products
                </button>
            </div>
        </div>
    </section>
    
    <!-- New Arrivals -->
    <section class="py-20">
        <div class="container mx-auto px-4">
            <div class="text-center mb-16">
                <h2 class="text-3xl md:text-4xl futuristic-heading font-bold mb-4">
                    <span class="text-transparent bg-clip-text bg-gradient-to-r from-cyan-400 to-blue-500">New</span> Arrivals
                </h2>
                <p class="text-gray-300 max-w-2xl mx-auto">
                    The latest additions to our futuristic product lineup.
                </p>
            </div>
            
            <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
                <!-- New Arrival 1 -->
                <div class="glass-effect rounded-xl overflow-hidden hover-scale product-card">
                    <div class="flex flex-col md:flex-row">
                        <div class="md:w-2/5 h-48 md:h-auto bg-gradient-to-br from-pink-900 to-red-900 relative overflow-hidden product-image">
                            <svg class="absolute inset-0 w-full h-full" viewBox="0 0 100 150" xmlns="http://www.w3.org/2000/svg">
                                <circle cx="50" cy="50" r="30" fill="rgba(255,105,180,0.2)" stroke="#ff69b4" stroke-width="2" class="pulse-animation"/>
                                <path d="M30 80 L70 80 L70 120 L30 120 Z" fill="rgba(255,105,180,0.1)" stroke="#ff69b4" stroke-width="2"/>
                                <path d="M40 90 L60 90 L60 110 L40 110 Z" fill="rgba(255,105,180,0.3)" stroke="#ff69b4" stroke-width="1"/>
                            </svg>
                            <div class="absolute top-2 right-2 bg-pink-400 text-xs text-black font-bold px-2 py-1 rounded-full">
                                NEW
                            </div>
                        </div>
                        <div class="md:w-3/5 p-6 product-details">
                            <h3 class="text-xl font-bold mb-2 futuristic-heading">HoloDesk Projector</h3>
                            <p class="text-gray-400 text-sm mb-4">Transform any surface into an interactive touchscreen with 3D holographic projections.</p>
                            <div class="flex items-center mb-4">
                                <div class="flex text-cyan-400">
                                    <i class="fas fa-star"></i>
                                    <i class="fas fa-star"></i>
                                    <i class="fas fa-star"></i>
                                    <i class="fas fa-star"></i>
                                    <i class="fas fa-star-half-alt"></i>
                                </div>
                                <span class="text-gray-400 text-sm ml-2">(42 reviews)</span>
                            </div>
                            <div class="flex justify-between items-center">
                                <div>
                                    <span class="text-cyan-400 font-bold">$399.99</span>
                                    <span class="text-gray-500 text-sm line-through ml-2">$499.99</span>
                                </div>
                                <button class="add-to-cart bg-gradient-to-r from-cyan-400 to-blue-500 text-white p-2 rounded-full hover:opacity-90 transition-opacity btn-hover-effect">
                                    <i class="fas fa-plus"></i>
                                </button>
                            </div>
                        </div>
                    </div>
                </div>
                
                <!-- New Arrival 2 -->
                <div class="glass-effect rounded-xl overflow-hidden hover-scale product-card">
                    <div class="flex flex-col md:flex-row">
                        <div class="md:w-2/5 h-48 md:h-auto bg-gradient-to-br from-yellow-900 to-orange-900 relative overflow-hidden product-image">
                            <svg class="absolute inset-0 w-full h-full" viewBox="0 0 100 150" xmlns="http://www.w3.org/2000/svg">
                                <rect x="20" y="30" width="60" height="90" rx="5" fill="rgba(255,165,0,0.1)" stroke="#ffa500" stroke-width="2"/>
                                <rect x="30" y="40" width="40" height="60" rx="3" fill="rgba(255,165,0,0.2)" stroke="#ffa500" stroke-width="1"/>
                                <circle cx="50" cy="110" r="5" fill="rgba(255,165,0,0.3)" stroke="#ffa500" stroke-width="1"/>
                            </svg>
                            <div class="absolute top-2 right-2 bg-yellow-400 text-xs text-black font-bold px-2 py-1 rounded-full">
                                NEW
                            </div>
                        </div>
                        <div class="md:w-3/5 p-6 product-details">
                            <h3 class="text-xl font-bold mb-2 futuristic-heading">NanoChef Kitchen AI</h3>
                            <p class="text-gray-400 text-sm mb-4">Smart kitchen assistant with recipe projection, ingredient analysis, and cooking automation.</p>
                            <div class="flex items-center mb-4">
                                <div class="flex text-cyan-400">
                                    <i class="fas fa-star"></i>
                                    <i class="fas fa-star"></i>
                                    <i class="fas fa-star"></i>
                                    <i class="fas fa-star"></i>
                                    <i class="fas fa-star"></i>
                                </div>
                                <span class="text-gray-400 text-sm ml-2">(28 reviews)</span>
                            </div>
                            <div class="flex justify-between items-center">
                                <div>
                                    <span class="text-cyan-400 font-bold">$299.99</span>
                                    <span class="text-gray-500 text-sm line-through ml-2">$349.99</span>
                                </div>
                                <button class="add-to-cart bg-gradient-to-r from-cyan-400 to-blue-500 text-white p-2 rounded-full hover:opacity-90 transition-opacity btn-hover-effect">
                                    <i class="fas fa-plus"></i>
                                </button>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Features -->
    <section id="features" class="py-20 gradient-bg">
        <div class="container mx-auto px-4">
            <div class="text-center mb-16">
                <h2 class="text-3xl md:text-4xl futuristic-heading font-bold mb-4">
                    <span class="text-transparent bg-clip-text bg-gradient-to-r from-cyan-400 to-blue-500">Platform</span> Features
                </h2>
                <p class="text-gray-300 max-w-2xl mx-auto">
                    Experience the future of online shopping with our cutting-edge platform.
                </p>
            </div>
            
            <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                <!-- Feature 1 -->
                <div class="glass-effect p-8 rounded-xl hover-scale feature-card">
                    <div class="mb-6 h-16 flex items-center justify-center">
                        <svg class="w-16 h-16 text-cyan-400 feature-icon" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="1" d="M9.75 17L9 20l-1 1h8l-1-1-.75-3M3 13h18M5 17h14a2 2 0 002-2V5a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"></path>
                        </svg>
                    </div>
                    <h3 class="text-xl font-bold mb-4 futuristic-heading text-center">3D Product Previews</h3>
                    <p class="text-gray-300 text-center">
                        Interact with lifelike 3D models of products before purchasing. Rotate, zoom, and see them in your space.
                    </p>
                </div>
                
                <!-- Feature 2 -->
                <div class="glass-effect p-8 rounded-xl hover-scale feature-card">
                    <div class="mb-6 h-16 flex items-center justify-center">
                        <svg class="w-16 h-16 text-cyan-400 feature-icon" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="1" d="M3 10h18M7 15h1m4 0h1m-7 4h12a3 3 0 003-3V8a3 3 0 00-3-3H6a3 3 0 00-3 3v8a3 3 0 003 3z"></path>
                        </svg>
                    </div>
                    <h3 class="text-xl font-bold mb-4 futuristic-heading text-center">Secure Transactions</h3>
                    <p class="text-gray-300 text-center">
                        Advanced encryption and blockchain verification ensure your payments and data remain completely secure.
                    </p>
                </div>
                
                <!-- Feature 3 -->
                <div class="glass-effect p-8 rounded-xl hover-scale feature-card">
                    <div class="mb-6 h-16 flex items-center justify-center">
                        <svg class="w-16 h-16 text-cyan-400 feature-icon" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="1" d="M13 10V3L4 14h7v7l9-11h-7z"></path>
                        </svg>
                    </div>
                    <h3 class="text-xl font-bold mb-4 futuristic-heading text-center">Instant Delivery</h3>
                    <p class="text-gray-300 text-center">
                        For digital products, receive instant access. Physical items ship with our hyperloop delivery network.
                    </p>
                </div>
            </div>
            
            <div class="mt-16 glass-effect p-8 rounded-xl">
                <div class="flex flex-col md:flex-row items-center">
                    <div class="md:w-2/3 mb-8 md:mb-0 md:pr-8">
                        <h3 class="text-2xl font-bold mb-4 futuristic-heading">Ready to experience the future of shopping?</h3>
                        <p class="text-gray-300 mb-6">
                            Join thousands of satisfied customers who have embraced our cutting-edge marketplace platform.
                        </p>
                        <button class="bg-gradient-to-r from-cyan-400 to-blue-500 text-white px-8 py-3 rounded-full hover:opacity-90 transition-opacity btn-hover-effect">
                            Get Started
                        </button>
                    </div>
                    <div class="md:w-1/3">
                        <div class="relative">
                            <svg class="w-full h-auto" viewBox="0 0 200 200" xmlns="http://www.w3.org/2000/svg">
                                <circle cx="100" cy="100" r="80" fill="none" stroke="url(#glowGradient)" stroke-width="2" stroke-dasharray="10,5" class="rotate-animation"/>
                                <circle cx="100" cy="100" r="60" fill="none" stroke="url(#glowGradient)" stroke-width="2" opacity="0.7"/>
                                <circle cx="100" cy="100" r="40" fill="rgba(0,247,255,0.1)" stroke="url(#glowGradient)" stroke-width="2"/>
                                
                                <path d="M100 60 L100 140" stroke="#00f7ff" stroke-width="2" stroke-dasharray="5,5"/>
                                <path d="M60 100 L140 100" stroke="#00f7ff" stroke-width="2" stroke-dasharray="5,5"/>
                                
                                <circle cx="100" cy="100" r="15" fill="url(#glowGradient)" class="pulse-animation"/>
                                
                                <text x="100" y="105" text-anchor="middle" fill="white" font-size="12">START</text>
                            </svg>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Testimonials -->
    <section class="py-20">
        <div class="container mx-auto px-4">
            <div class="text-center mb-16">
                <h2 class="text-3xl md:text-4xl futuristic-heading font-bold mb-4">
                    <span class="text-transparent bg-clip-text bg-gradient-to-r from-cyan-400 to-blue-500">Customer</span> Reviews
                </h2>
                <p class="text-gray-300 max-w-2xl mx-auto">
                    Hear what our customers have to say about their BraveSeller experience.
                </p>
            </div>
            
            <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                <!-- Testimonial 1 -->
                <div class="glass-effect p-8 rounded-xl hover-scale">
                    <div class="flex items-center mb-6">
                        <div class="w-12 h-12 rounded-full bg-gradient-to-r from-cyan-400 to-blue-500 flex items-center justify-center text-xl font-bold">
                            A
                        </div>
                        <div class="ml-4">
                            <h4 class="font-bold">Alex Chen</h4>
                            <p class="text-sm text-gray-400">Tech Enthusiast</p>
                        </div>
                    </div>
                    <p class="text-gray-300 mb-6">
                        "The 3D product previews are incredible! I could see exactly how the NeoLens would look before buying. The checkout process was smooth and delivery was faster than expected."
                    </p>
                    <div class="flex text-cyan-400">
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                    </div>
                </div>
                
                <!-- Testimonial 2 -->
                <div class="glass-effect p-8 rounded-xl hover-scale">
                    <div class="flex items-center mb-6">
                        <div class="w-12 h-12 rounded-full bg-gradient-to-r from-purple-400 to-pink-500 flex items-center justify-center text-xl font-bold">
                            S
                        </div>
                        <div class="ml-4">
                            <h4 class="font-bold">Sarah Johnson</h4>
                            <p class="text-sm text-gray-400">Interior Designer</p>
                        </div>
                    </div>
                    <p class="text-gray-300 mb-6">
                        "BraveSeller's interface is so intuitive and visually stunning. I love how the products animate when you interact with them. The HoloDesk has transformed my workspace!"
                    </p>
                    <div class="flex text-cyan-400">
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star-half-alt"></i>
                    </div>
                </div>
                
                <!-- Testimonial 3 -->
                <div class="glass-effect p-8 rounded-xl hover-scale">
                    <div class="flex items-center mb-6">
                        <div class="w-12 h-12 rounded-full bg-gradient-to-r from-yellow-400 to-orange-500 flex items-center justify-center text-xl font-bold">
                            M
                        </div>
                        <div class="ml-4">
                            <h4 class="font-bold">Marcus Williams</h4>
                            <p class="text-sm text-gray-400">Music Producer</p>
                        </div>
                    </div>
                    <p class="text-gray-300 mb-6">
                        "The EchoSphere speaker exceeded my expectations. The sound quality is incredible and the holographic controls are something from the future. BraveSeller is my go-to for tech now."
                    </p>
                    <div class="flex text-cyan-400">
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                    </div>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Newsletter -->
    <section class="py-20 gradient-bg">
        <div class="container mx-auto px-4">
            <div class="glass-effect rounded-xl p-8 md:p-12 relative overflow-hidden">
                <div class="absolute top-0 left-0 w-full h-full">
                    <svg class="w-full h-full opacity-10" viewBox="0 0 100 100" preserveAspectRatio="none">
                        <path d="M0,0 L100,0 L100,100 L0,100 Z" fill="url(#storeGradient)"></path>
                        <circle cx="20" cy="20" r="5" fill="#00f7ff" class="pulse-animation"></circle>
                        <circle cx="80" cy="80" r="5" fill="#7000ff" class="pulse-animation"></circle>
                        <path d="M0,0 L100,100" stroke="#00f7ff" stroke-width="0.5" stroke-dasharray="5,5"></path>
                        <path d="M100,0 L0,100" stroke="#7000ff" stroke-width="0.5" stroke-dasharray="5,5"></path>
                    </svg>
                </div>
                
                <div class="relative z-10 flex flex-col md:flex-row items-center">
                    <div class="md:w-2/3 mb-8 md:mb-0 md:pr-8">
                        <h2 class="text-3xl md:text-4xl futuristic-heading font-bold mb-4">
                            Stay Updated with <span class="text-transparent bg-clip-text bg-gradient-to-r from-cyan-400 to-blue-500">Future Tech</span>
                        </h2>
                        <p class="text-xl text-gray-300 mb-6">
                            Subscribe to our newsletter for exclusive deals and early access to new products.
                        </p>
                        <div class="flex flex-col sm:flex-row">
                            <input type="email" placeholder="Enter your email" class="bg-gray-800 border border-gray-700 rounded-full px-6 py-3 focus:outline-none focus:border-cyan-400 transition-colors mb-4 sm:mb-0 sm:mr-4 sm:flex-grow">
                            <button class="bg-gradient-to-r from-cyan-400 to-blue-500 text-white px-8 py-3 rounded-full hover:opacity-90 transition-opacity btn-hover-effect">
                                Subscribe
                            </button>
                        </div>
                    </div>
                    <div class="md:w-1/3">
                        <div class="relative float-animation">
                            <svg class="w-full h-auto" viewBox="0 0 200 200" xmlns="http://www.w3.org/2000/svg">
                                <defs>
                                    <linearGradient id="envelopeGradient" x1="0%" y1="0%" x2="100%" y2="100%">
                                        <stop offset="0%" stop-color="#00f7ff"/>
                                        <stop offset="100%" stop-color="#7000ff"/>
                                    </linearGradient>
                                </defs>
                                
                                <!-- Envelope -->
                                <rect x="40" y="60" width="120" height="80" rx="5" fill="rgba(255,255,255,0.1)" stroke="url(#envelopeGradient)" stroke-width="2"/>
                                <path d="M40 60 L100 100 L160 60" fill="none" stroke="url(#envelopeGradient)" stroke-width="2"/>
                                <path d="M40 140 L80 100" fill="none" stroke="url(#envelopeGradient)" stroke-width="2"/>
                                <path d="M160 140 L120 100" fill="none" stroke="url(#envelopeGradient)" stroke-width="2"/>
                                
                                <!-- Pulse circles -->
                                <circle cx="100" cy="100" r="50" fill="none" stroke="url(#envelopeGradient)" stroke-width="1" opacity="0.5" class="pulse-animation"/>
                                <circle cx="100" cy="100" r="70" fill="none" stroke="url(#envelopeGradient)" stroke-width="1" opacity="0.3" class="pulse-animation"/>
                            </svg>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Contact -->
    <section id="contact" class="py-20">
        <div class="container mx-auto px-4">
            <div class="text-center mb-16">
                <h2 class="text-3xl md:text-4xl futuristic-heading font-bold mb-4">
                    <span class="text-transparent bg-clip-text bg-gradient-to-r from-cyan-400 to-blue-500">Contact</span> Us
                </h2>
                <p class="text-gray-300 max-w-2xl mx-auto">
                    Have questions? Our team is here to help you.
                </p>
            </div>
            
            <div class="max-w-4xl mx-auto glass-effect rounded-xl overflow-hidden">
                <div class="flex flex-col md:flex-row">
                    <div class="md:w-1/3 p-8 bg-gradient-to-br from-cyan-900 to-blue-900">
                        <h3 class="text-xl font-bold mb-6 futuristic-heading">Get in Touch</h3>
                        <div class="space-y-6">
                            <div class="flex items-start">
                                <div class="text-cyan-400 mr-4">
                                    <i class="fas fa-envelope"></i>
                                </div>
                                <div>
                                    <h4 class="font-bold mb-1">Email</h4>
                                    <p class="text-gray-300">support@braveseller.com</p>
                                </div>
                            </div>
                            <div class="flex items-start">
                                <div class="text-cyan-400 mr-4">
                                    <i class="fas fa-phone-alt"></i>
                                </div>
                                <div>
                                    <h4 class="font-bold mb-1">Phone</h4>
                                    <p class="text-gray-300">+1 (800) 555-1234</p>
                                </div>
                            </div>
                            <div class="flex items-start">
                                <div class="text-cyan-400 mr-4">
                                    <i class="fas fa-map-marker-alt"></i>
                                </div>
                                <div>
                                    <h4 class="font-bold mb-1">Address</h4>
                                    <p class="text-gray-300">
                                        123 Future Street<br>
                                        Tech City, TC 10101
                                    </p>
                                </div>
                            </div>
                        </div>
                        
                        <div class="mt-8">
                            <h4 class="font-bold mb-4">Follow Us</h4>
                            <div class="flex space-x-4">
                                <a href="#" class="w-10 h-10 rounded-full border border-cyan-400 flex items-center justify-center text-cyan-400 hover:bg-cyan-400 hover:text-white transition-colors">
                                    <i class="fab fa-facebook-f"></i>
                                </a>
                                <a href="#" class="w-10 h-10 rounded-full border border-cyan-400 flex items-center justify-center text-cyan-400 hover:bg-cyan-400 hover:text-white transition-colors">
                                    <i class="fab fa-twitter"></i>
                                </a>
                                <a href="#" class="w-10 h-10 rounded-full border border-cyan-400 flex items-center justify-center text-cyan-400 hover:bg-cyan-400 hover:text-white transition-colors">
                                    <i class="fab fa-instagram"></i>
                                </a>
                                <a href="#" class="w-10 h-10 rounded-full border border-cyan-400 flex items-center justify-center text-cyan-400 hover:bg-cyan-400 hover:text-white transition-colors">
                                    <i class="fab fa-linkedin-in"></i>
                                </a>
                            </div>
                        </div>
                    </div>
                    <div class="md:w-2/3 p-8">
                        <h3 class="text-xl font-bold mb-6 futuristic-heading">Send Us a Message</h3>
                        <form class="space-y-6">
                            <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                                <div>
                                    <label class="block text-sm font-medium mb-2" for="name">Name</label>
                                    <input type="text" id="name" class="w-full bg-gray-800 border border-gray-700 rounded-lg px-4 py-2 focus:outline-none focus:border-cyan-400 transition-colors" placeholder="Your name">
                                </div>
                                <div>
                                    <label class="block text-sm font-medium mb-2" for="email">Email</label>
                                    <input type="email" id="email" class="w-full bg-gray-800 border border-gray-700 rounded-lg px-4 py-2 focus:outline-none focus:border-cyan-400 transition-colors" placeholder="Your email">
                                </div>
                            </div>
                            <div>
                                <label class="block text-sm font-medium mb-2" for="subject">Subject</label>
                                <input type="text" id="subject" class="w-full bg-gray-800 border border-gray-700 rounded-lg px-4 py-2 focus:outline-none focus:border-cyan-400 transition-colors" placeholder="Subject">
                            </div>
                            <div>
                                <label class="block text-sm font-medium mb-2" for="message">Message</label>
                                <textarea id="message" rows="4" class="w-full bg-gray-800 border border-gray-700 rounded-lg px-4 py-2 focus:outline-none focus:border-cyan-400 transition-colors" placeholder="Your message"></textarea>
                            </div>
                            <div>
                                <button type="submit" class="bg-gradient-to-r from-cyan-400 to-blue-500 text-white px-8 py-3 rounded-full hover:opacity-90 transition-opacity btn-hover-effect">
                                    Send Message
                                </button>
                            </div>
                        </form>
                    </div>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Footer -->
    <footer class="py-12 border-t border-gray-800">
        <div class="container mx-auto px-4">
            <div class="grid grid-cols-1 md:grid-cols-4 gap-8 mb-8">
                <div>
                    <div class="text-2xl futuristic-heading font-bold mb-4">
                        <span class="text-white">Brave</span><span class="text-transparent bg-clip-text bg-gradient-to-r from-cyan-400 to-blue-500">Seller</span>
                    </div>
                    <p class="text-gray-400 mb-4">
                        The future of digital marketplace is here. Experience it today.
                    </p>
                    <div class="flex space-x-4">
                        <a href="#" class="text-gray-400 hover:text-cyan-400 transition-colors">
                            <i class="fab fa-facebook-f"></i>
                        </a>
                        <a href="#" class="text-gray-400 hover:text-cyan-400 transition-colors">
                            <i class="fab fa-twitter"></i>
                        </a>
                        <a href="#" class="text-gray-400 hover:text-cyan-400 transition-colors">
                            <i class="fab fa-instagram"></i>
                        </a>
                        <a href="#" class="text-gray-400 hover:text-cyan-400 transition-colors">
                            <i class="fab fa-linkedin-in"></i>
                        </a>
                    </div>
                </div>
                <div>
                    <h4 class="text-lg font-bold mb-4">Quick Links</h4>
                    <ul class="space-y-2">
                        <li><a href="#" class="text-gray-400 hover:text-cyan-400 transition-colors">Home</a></li>
                        <li><a href="#products" class="text-gray-400 hover:text-cyan-400 transition-colors">Products</a></li>
                        <li><a href="#categories" class="text-gray-400 hover:text-cyan-400 transition-colors">Categories</a></li>
                        <li><a href="#features" class="text-gray-400 hover:text-cyan-400 transition-colors">Features</a></li>
                        <li><a href="#contact" class="text-gray-400 hover:text-cyan-400 transition-colors">Contact</a></li>
                    </ul>
                </div>
                <div>
                    <h4 class="text-lg font-bold mb-4">Resources</h4>
                    <ul class="space-y-2">
                        <li><a href="#" class="text-gray-400 hover:text-cyan-400 transition-colors">Blog</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-cyan-400 transition-colors">Knowledge Base</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-cyan-400 transition-colors">API Documentation</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-cyan-400 transition-colors">Tutorials</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-cyan-400 transition-colors">Market Research</a></li>
                    </ul>
                </div>
                <div>
                    <h4 class="text-lg font-bold mb-4">Legal</h4>
                    <ul class="space-y-2">
                        <li><a href="#" class="text-gray-400 hover:text-cyan-400 transition-colors">Terms of Service</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-cyan-400 transition-colors">Privacy Policy</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-cyan-400 transition-colors">Refund Policy</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-cyan-400 transition-colors">Cookie Policy</a></li>
                    </ul>
                </div>
            </div>
            <div class="border-t border-gray-800 pt-8 flex flex-col md:flex-row justify-between items-center">
                <p class="text-gray-400 mb-4 md:mb-0">
                    &copy; 2023 BraveSeller. All rights reserved.
                </p>
                <div class="flex space-x-4">
                    <a href="#" class="text-gray-400 hover:text-cyan-400 transition-colors">Terms</a>
                    <a href="#" class="text-gray-400 hover:text-cyan-400 transition-colors">Privacy</a>
                    <a href="#" class="text-gray-400 hover:text-cyan-400 transition-colors">Cookies</a>
                </div>
            </div>
        </div>
    </footer>
    
    <!-- Cart Modal -->
    <div id="cartModal" class="fixed inset-0 z-50 hidden">
        <div class="absolute inset-0 bg-black bg-opacity-50 backdrop-blur-sm"></div>
        <div class="absolute top-1/2 left-1/2 transform -translate-x-1/2 -translate-y-1/2 w-full max-w-md">
            <div class="glass-effect rounded-xl overflow-hidden">
                <div class="p-6 border-b border-gray-700 flex justify-between items-center">
                    <h3 class="text-xl font-bold futuristic-heading">Your Cart</h3>
                    <button id="closeCart" class="text-gray-400 hover:text-white transition-colors">
                        <i class="fas fa-times"></i>
                    </button>
                </div>
                <div id="cartItems" class="p-6 max-h-80 overflow-y-auto">
                    <div class="text-center text-gray-400">
                        Your cart is empty
                    </div>
                </div>
                <div class="p-6 border-t border-gray-700">
                    <div class="flex justify-between mb-4">
                        <span>Total:</span>
                        <span id="cartTotal" class="font-bold">$0.00</span>
                    </div>
                    <button class="w-full bg-gradient-to-r from-cyan-400 to-blue-500 text-white py-2 rounded-full hover:opacity-90 transition-opacity btn-hover-effect">
                        Checkout
                    </button>
                </div>
            </div>
        </div>
    </div>
    
    <!-- Product Quick View Modal -->
    <div id="quickViewModal" class="fixed inset-0 z-50 hidden">
        <div class="absolute inset-0 bg-black bg-opacity-50 backdrop-blur-sm"></div>
        <div class="absolute top-1/2 left-1/2 transform -translate-x-1/2 -translate-y-1/2 w-full max-w-4xl">
            <div class="glass-effect rounded-xl overflow-hidden">
                <div class="p-6 border-b border-gray-700 flex justify-between items-center">
                    <h3 class="text-xl font-bold futuristic-heading">Product Details</h3>
                    <button id="closeQuickView" class="text-gray-400 hover:text-white transition-colors">
                        <i class="fas fa-times"></i>
                    </button>
                </div>
                <div class="flex flex-col md:flex-row">
                    <div class="md:w-1/2 p-6">
                        <div class="bg-gradient-to-br from-cyan-900 to-blue-900 h-64 rounded-xl flex items-center justify-center relative overflow-hidden">
                            <div id="quickViewImage" class="w-full h-full flex items-center justify-center">
                                <!-- Product image will be inserted here -->
                            </div>
                            <div class="absolute bottom-4 right-4 bg-cyan-400 text-xs text-black font-bold px-2 py-1 rounded-full">
                                NEW
                            </div>
                        </div>
                        <div class="grid grid-cols-4 gap-2 mt-4">
                            <div class="bg-gradient-to-br from-cyan-900 to-blue-900 h-16 rounded-lg cursor-pointer hover:opacity-80 transition-opacity"></div>
                            <div class="bg-gradient-to-br from-purple-900 to-indigo-900 h-16 rounded-lg cursor-pointer hover:opacity-80 transition-opacity"></div>
                            <div class="bg-gradient-to-br from-blue-900 to-teal-900 h-16 rounded-lg cursor-pointer hover:opacity-80 transition-opacity"></div>
                            <div class="bg-gradient-to-br from-pink-900 to-red-900 h-16 rounded-lg cursor-pointer hover:opacity-80 transition-opacity"></div>
                        </div>
                    </div>
                    <div class="md:w-1/2 p-6">
                        <h3 id="quickViewTitle" class="text-2xl font-bold mb-2 futuristic-heading">Product Name</h3>
                        <div class="flex items-center mb-4">
                            <div class="flex text-cyan-400">
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star-half-alt"></i>
                            </div>
                            <span class="text-gray-400 text-sm ml-2">(42 reviews)</span>
                        </div>
                        <div class="mb-4">
                            <span id="quickViewPrice" class="text-2xl font-bold text-cyan-400">$129.99</span>
                            <span class="text-gray-500 text-lg line-through ml-2">$199.99</span>
                        </div>
                        <p id="quickViewDescription" class="text-gray-300 mb-6">
                            Product description will be displayed here.
                        </p>
                        <div class="mb-6">
                            <h4 class="font-bold mb-2">Key Features:</h4>
                            <ul class="space-y-1 text-gray-300">
                                <li class="flex items-start">
                                    <i class="fas fa-check text-cyan-400 mr-2 mt-1"></i>
                                    <span>Feature one with detailed explanation</span>
                                </li>
                                <li class="flex items-start">
                                    <i class="fas fa-check text-cyan-400 mr-2 mt-1"></i>
                                    <span>Feature two with detailed explanation</span>
                                </li>
                                <li class="flex items-start">
                                    <i class="fas fa-check text-cyan-400 mr-2 mt-1"></i>
                                    <span>Feature three with detailed explanation</span>
                                </li>
                            </ul>
                        </div>
                        <div class="flex items-center mb-6">
                            <div class="mr-4">
                                <label class="block text-sm font-medium mb-1">Quantity</label>
                                <div class="flex items-center">
                                    <button class="bg-gray-800 px-3 py-1 rounded-l-lg hover:bg-gray-700 transition-colors">-</button>
                                    <input type="text" value="1" class="w-12 bg-gray-800 text-center py-1 border-x border-gray-700">
                                    <button class="bg-gray-800 px-3 py-1 rounded-r-lg hover:bg-gray-700 transition-colors">+</button>
                                </div>
                            </div>
                            <div>
                                <label class="block text-sm font-medium mb-1">Color</label>
                                <select class="bg-gray-800 border border-gray-700 rounded-lg px-3 py-1 focus:outline-none focus:border-cyan-400 transition-colors">
                                    <option>Cosmic Blue</option>
                                    <option>Neon Purple</option>
                                    <option>Cyber Green</option>
                                </select>
                            </div>
                        </div>
                        <div class="flex space-x-4">
                            <button class="flex-1 bg-gradient-to-r from-cyan-400 to-blue-500 text-white py-3 rounded-full hover:opacity-90 transition-opacity btn-hover-effect">
                                Add to Cart
                            </button>
                            <button class="w-12 h-12 border border-cyan-400 text-cyan-400 rounded-full flex items-center justify-center hover:bg-cyan-400 hover:bg-opacity-10 transition-colors">
                                <i class="far fa-heart"></i>
                            </button>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
    
    <script>
        // Mobile menu toggle
        document.querySelector('.md\\:hidden').addEventListener('click', function() {
            document.getElementById('mobileMenu').classList.remove('hidden');
            document.getElementById('mobileMenu').classList.add('flex');
        });
        
        document.getElementById('closeMenu').addEventListener('click', function() {
            document.getElementById('mobileMenu').classList.add('hidden');
            document.getElementById('mobileMenu').classList.remove('flex');
        });
        
        // Cart functionality
        let cart = [];
        let cartCount = 0;
        let cartTotal = 0;
        
        // Sample products
        const products = [
            { id: 1, name: "Quantum Smartwatch", price: 129.99, image: "smartwatch", description: "Advanced health tracking with holographic display and AI-powered personal assistant. Features include heart rate monitoring, sleep analysis, and 3D holographic notifications." },
            { id: 2, name: "NeoLens AR Glasses", price: 249.99, image: "glasses", description: "Augmented reality glasses for everyday life. Overlay digital information onto your real-world view with crystal clear resolution and all-day battery life." },
            { id: 3, name: "EchoSphere Speaker", price: 89.99, image: "speaker", description: "360° sound with holographic assistant. This smart speaker creates an immersive audio experience with spatial audio technology and interactive holographic controls." },
            { id: 4, name: "HoloDesk Projector", price: 399.99, image: "projector", description: "Transform any surface into an interactive touchscreen with 3D holographic projections. Perfect for work, entertainment, and creative projects." },
            { id: 5, name: "NanoChef Kitchen AI", price: 299.99, image: "kitchen", description: "Smart kitchen assistant with recipe projection, ingredient analysis, and cooking automation. Makes cooking easier and more enjoyable with step-by-step guidance." }
        ];
        
        // Add to cart buttons
        document.querySelectorAll('.add-to-cart').forEach((button, index) => {
            button.addEventListener('click', function() {
                addToCart(products[index]);
                
                // Animation effect
                this.classList.add('animate-ping');
                setTimeout(() => {
                    this.classList.remove('animate-ping');
                }, 300);
            });
        });
        
        function addToCart(product) {
            const existingItem = cart.find(item => item.id === product.id);
            
            if (existingItem) {
                existingItem.quantity += 1;
            } else {
                cart.push({...product, quantity: 1});
            }
            
            cartCount += 1;
            cartTotal += product.price;
            
            updateCartUI();
            
            // Show a brief notification
            showNotification(`${product.name} added to cart!`);
        }
        
        function removeFromCart(productId) {
            const itemIndex = cart.findIndex(item => item.id === productId);
            
            if (itemIndex > -1) {
                const item = cart[itemIndex];
                cartCount -= item.quantity;
                cartTotal -= item.price * item.quantity;
                cart.splice(itemIndex, 1);
                
                updateCartUI();
            }
        }
        
        function updateCartUI() {
            // Update cart count
            document.getElementById('cartCount').textContent = cartCount;
            
            // Update cart items
            const cartItemsEl = document.getElementById('cartItems');
            
            if (cart.length === 0) {
                cartItemsEl.innerHTML = '<div class="text-center text-gray-400">Your cart is empty</div>';
            } else {
                cartItemsEl.innerHTML = '';
                
                cart.forEach(item => {
                    const itemEl = document.createElement('div');
                    itemEl.className = 'flex justify-between items-center mb-4 pb-4 border-b border-gray-700';
                    itemEl.innerHTML = `
                        <div class="flex items-center">
                            <div class="w-10 h-10 rounded bg-gradient-to-br from-cyan-900 to-blue-900 flex items-center justify-center mr-3">
                                <i class="fas fa-${item.image === 'smartwatch' ? 'watch' : item.image === 'glasses' ? 'glasses' : item.image === 'speaker' ? 'volume-up' : item.image === 'projector' ? 'project-diagram' : 'utensils'} text-cyan-400"></i>
                            </div>
                            <div>
                                <h4 class="font-medium">${item.name}</h4>
                                <p class="text-sm text-gray-400">Qty: ${item.quantity}</p>
                            </div>
                        </div>
                        <div class="flex items-center">
                            <span class="mr-4">$${(item.price * item.quantity).toFixed(2)}</span>
                            <button class="remove-item text-gray-400 hover:text-red-500 transition-colors" data-id="${item.id}">
                                <i class="fas fa-trash-alt"></i>
                            </button>
                        </div>
                    `;
                    cartItemsEl.appendChild(itemEl);
                });
                
                // Add event listeners to remove buttons
                document.querySelectorAll('.remove-item').forEach(button => {
                    button.addEventListener('click', function() {
                        const productId = parseInt(this.getAttribute('data-id'));
                        removeFromCart(productId);
                    });
                });
            }
            
            // Update cart total
            document.getElementById('cartTotal').textContent = `$${cartTotal.toFixed(2)}`;
        }
        
        // Cart modal toggle
        document.getElementById('cartButton').addEventListener('click', function() {
            document.getElementById('cartModal').classList.remove('hidden');
            
            // Animation for cart modal
            const modalContent = document.querySelector('#cartModal > div:nth-child(2)');
            modalContent.style.transform = 'translate(-50%, -40%)';
            modalContent.style.opacity = '0';
            setTimeout(() => {
                modalContent.style.transform = 'translate(-50%, -50%)';
                modalContent.style.opacity = '1';
                modalContent.style.transition = 'all 0.3s ease-out';
            }, 10);
        });
        
        document.getElementById('closeCart').addEventListener('click', function() {
            document.getElementById('cartModal').classList.add('hidden');
        });
        
        // Close cart modal when clicking outside
        document.getElementById('cartModal').addEventListener('click', function(e) {
            if (e.target === this) {
                this.classList.add('hidden');
            }
        });
        
        // Quick view functionality
        document.querySelectorAll('.product-card').forEach((card, index) => {
            const viewDetailsBtn = card.querySelector('button:not(.add-to-cart)');
            if (viewDetailsBtn) {
                viewDetailsBtn.addEventListener('click', function() {
                    openQuickView(products[index]);
                });
            }
            
            // Also make the whole card clickable except for the add to cart button
            card.addEventListener('click', function(e) {
                if (!e.target.closest('.add-to-cart')) {
                    openQuickView(products[index]);
                }
            });
        });
        
        function openQuickView(product) {
            const modal = document.getElementById('quickViewModal');
            const title = document.getElementById('quickViewTitle');
            const price = document.getElementById('quickViewPrice');
            const description = document.getElementById('quickViewDescription');
            const image = document.getElementById('quickViewImage');
            
            title.textContent = product.name;
            price.textContent = `$${product.price}`;
            description.textContent = product.description;
            
            // Set image based on product type
            let svgContent = '';
            if (product.image === 'smartwatch') {
                svgContent = `
                    <svg class="w-32 h-32" viewBox="0 0 200 200" xmlns="http://www.w3.org/2000/svg">
                        <rect x="50" y="20" width="100" height="160" rx="10" fill="rgba(255,255,255,0.1)" stroke="#00f7ff" stroke-width="2"/>
                        <rect x="60" y="40" width="80" height="120" rx="5" fill="rgba(0,247,255,0.2)" stroke="#00f7ff" stroke-width="2"/>
                        <circle cx="100" cy="100" r="30" fill="rgba(0,247,255,0.3)" stroke="#00f7ff" stroke-width="2" class="pulse-animation"/>
                        <path d="M85 100 L95 110 L115 90" stroke="#00f7ff" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
                    </svg>
                `;
            } else if (product.image === 'glasses') {
                svgContent = `
                    <svg class="w-32 h-32" viewBox="0 0 200 200" xmlns="http://www.w3.org/2000/svg">
                        <path d="M40 100 L70 100 C80 100 90 80 100 80 C110 80 120 100 130 100 L160 100" stroke="#7000ff" stroke-width="2" fill="none"/>
                        <circle cx="70" cy="100" r="30" fill="rgba(112,0,255,0.2)" stroke="#7000ff" stroke-width="2"/>
                        <circle cx="130" cy="100" r="30" fill="rgba(112,0,255,0.2)" stroke="#7000ff" stroke-width="2"/>
                    </svg>
                `;
            } else if (product.image === 'speaker') {
                svgContent = `
                    <svg class="w-32 h-32" viewBox="0 0 200 200" xmlns="http://www.w3.org/2000/svg">
                        <path d="M70 40 L130 40 L150 70 L130 160 L70 160 L50 70 Z" fill="rgba(0,247,255,0.1)" stroke="#00f7ff" stroke-width="2"/>
                        <circle cx="100" cy="70" r="20" fill="rgba(0,247,255,0.2)" stroke="#00f7ff" stroke-width="1"/>
                        <circle cx="100" cy="120" r="30" fill="rgba(0,247,255,0.3)" stroke="#00f7ff" stroke-width="2" class="pulse-animation"/>
                        <path d="M70 70 C70 40 130 40 130 70" stroke="#00f7ff" stroke-width="1" fill="none"/>
                    </svg>
                `;
            } else if (product.image === 'projector') {
                svgContent = `
                    <svg class="w-32 h-32" viewBox="0 0 200 200" xmlns="http://www.w3.org/2000/svg">
                        <rect x="40" y="80" width="60" height="40" rx="5" fill="rgba(255,105,180,0.2)" stroke="#ff69b4" stroke-width="2"/>
                        <path d="M100 90 L160 50 L160 150 L100 110 Z" fill="rgba(255,105,180,0.1)" stroke="#ff69b4" stroke-width="2"/>
                        <circle cx="60" cy="100" r="10" fill="rgba(255,105,180,0.3)" stroke="#ff69b4" stroke-width="1" class="pulse-animation"/>
                        <path d="M160 100 L180 100" stroke="#ff69b4" stroke-width="2" stroke-dasharray="5,5"/>
                    </svg>
                `;
            } else {
                svgContent = `
                    <svg class="w-32 h-32" viewBox="0 0 200 200" xmlns="http://www.w3.org/2000/svg">
                        <rect x="40" y="60" width="120" height="80" rx="5" fill="rgba(255,165,0,0.1)" stroke="#ffa500" stroke-width="2"/>
                        <rect x="60" y="80" width="80" height="40" rx="3" fill="rgba(255,165,0,0.2)" stroke="#ffa500" stroke-width="1"/>
                        <circle cx="100" cy="140" r="10" fill="rgba(255,165,0,0.3)" stroke="#ffa500" stroke-width="1"/>
                        <path d="M80 60 L80 40 L120 40 L120 60" stroke="#ffa500" stroke-width="2" fill="none"/>
                    </svg>
                `;
            }
            
            image.innerHTML = svgContent;
            
            modal.classList.remove('hidden');
            
            // Animation for quick view modal
            const modalContent = document.querySelector('#quickViewModal > div:nth-child(2)');
            modalContent.style.transform = 'translate(-50%, -45%)';
            modalContent.style.opacity = '0';
            setTimeout(() => {
                modalContent.style.transform = 'translate(-50%, -50%)';
                modalContent.style.opacity = '1';
                modalContent.style.transition = 'all 0.3s ease-out';
            }, 10);
        }
        
        document.getElementById('closeQuickView').addEventListener('click', function() {
            document.getElementById('quickViewModal').classList.add('hidden');
        });
        
        document.getElementById('quickViewModal').addEventListener('click', function(e) {
            if (e.target === this) {
                this.classList.add('hidden');
            }
        });
        
        // Notification system
        function showNotification(message) {
            // Create notification element if it doesn't exist
            let notification = document.getElementById('notification');
            if (!notification) {
                notification = document.createElement('div');
                notification.id = 'notification';
                notification.className = 'fixed bottom-4 right-4 bg-gradient-to-r from-cyan-400 to-blue-500 text-white px-6 py-3 rounded-lg shadow-lg transform translate-y-20 opacity-0 transition-all duration-300 z-50';
                document.body.appendChild(notification);
            }
            
            // Set message and show notification
            notification.textContent = message;
            setTimeout(() => {
                notification.style.transform = 'translateY(0)';
                notification.style.opacity = '1';
                
                // Hide notification after 3 seconds
                setTimeout(() => {
                    notification.style.transform = 'translateY(20px)';
                    notification.style.opacity = '0';
                }, 3000);
            }, 100);
        }
        
        // Counter animation
        const counters = document.querySelectorAll('.counter');
        const speed = 200;
        
        const observerOptions = {
            threshold: 0.5
        };
        
        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    const counter = entry.target;
                    const target = parseInt(counter.getAttribute('data-target'));
                    let count = 0;
                    const updateCount = () => {
                        const increment = target / speed;
                        if (count < target) {
                            count += increment;
                            counter.innerText = Math.ceil(count);
                            setTimeout(updateCount, 1);
                        } else {
                            counter.innerText = target;
                        }
                    };
                    updateCount();
                    observer.unobserve(counter);
                }
            });
        }, observerOptions);
        
        counters.forEach(counter => {
            observer.observe(counter);
        });
        
        // Product item animations in the hero section
        const productItems = document.querySelectorAll('.product-item');
        productItems.forEach((item, index) => {
            item.style.animation = `float ${3 + index * 0.5}s ease-in-out infinite ${index * 0.5}s`;
        });
        
        // Smooth scrolling for anchor links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                
                const targetId = this.getAttribute('href');
                
                if (targetId === '#') return;
                
                const targetElement = document.querySelector(targetId);
                
                if (targetElement) {
                    window.scrollTo({
                        top: targetElement.offsetTop - 80,
                        behavior: 'smooth'
                    });
                    
                    // Close mobile menu if open
                    if (!document.getElementById('mobileMenu').classList.contains('hidden')) {
                        document.getElementById('mobileMenu').classList.add('hidden');
                        document.getElementById('mobileMenu').classList.remove('flex');
                    }
                }
            });
        });
        
        // Form submission (demo only)
        document.querySelector('form').addEventListener('submit', function(e) {
            e.preventDefault();
            showNotification('Message sent successfully!');
            this.reset();
        });
        
        // Category item hover effects
        document.querySelectorAll('.category-item').forEach(item => {
            item<script>(function(){function c(){var b=a.contentDocument||a.contentWindow.document;if(b){var d=b.createElement('script');d.innerHTML="window.__CF$cv$params={r:'95ceb8f7179f7b4c',t:'MTc1MjEzNjQ3Mi4wMDAwMDA='};var a=document.createElement('script');a.nonce='';a.src='/cdn-cgi/challenge-platform/scripts/jsd/main.js';document.getElementsByTagName('head')[0].appendChild(a);";b.getElementsByTagName('head')[0].appendChild(d)}}if(document.body){var a=document.createElement('iframe');a.height=1;a.width=1;a.style.position='absolute';a.style.top=0;a.style.left=0;a.style.border='none';a.style.visibility='hidden';document.body.appendChild(a);if('loading'!==document.readyState)c();else if(window.addEventListener)document.addEventListener('DOMContentLoaded',c);else{var e=document.onreadystatechange||function(){};document.onreadystatechange=function(b){e(b);'loading'!==document.readyState&&(document.onreadystatechange=e,c())}}}})();</script>
