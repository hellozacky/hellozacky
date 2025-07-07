<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Pixel Art GitHub Profile</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        /* Pixel art styling */
        .pixel {
            image-rendering: pixelated;
            image-rendering: -moz-crisp-edges;
            image-rendering: crisp-edges;
        }
        
        /* Animal animations */
        @keyframes walk {
            0% { transform: translateX(0); }
            100% { transform: translateX(100%); }
        }
        
        @keyframes float {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-10px); }
        }
        
        @keyframes bounce {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-15px); }
        }
        
        .walking {
            animation: walk 15s linear infinite;
        }
        
        .floating {
            animation: float 3s ease-in-out infinite;
        }
        
        .bouncing {
            animation: bounce 2s ease-in-out infinite;
        }
        
        /* Pixel art animals */
        .pixel-cat {
            width: 32px;
            height: 32px;
            background-image: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 32 32"><rect width="32" height="32" fill="%23FF9966"/><rect x="8" y="8" width="4" height="4" fill="%23000"/><rect x="20" y="8" width="4" height="4" fill="%23000"/><rect x="12" y="16" width="8" height="4" fill="%23000"/><rect x="8" y="20" width="4" height="4" fill="%23000"/><rect x="20" y="20" width="4" height="4" fill="%23000"/></svg>');
        }
        
        .pixel-dog {
            width: 32px;
            height: 32px;
            background-image: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 32 32"><rect width="32" height="32" fill="%23CC9966"/><rect x="8" y="8" width="4" height="4" fill="%23000"/><rect x="20" y="8" width="4" height="4" fill="%23000"/><rect x="12" y="16" width="8" height="4" fill="%23000"/><rect x="6" y="20" width="6" height="4" fill="%23000"/><rect x="20" y="20" width="6" height="4" fill="%23000"/></svg>');
        }
        
        .pixel-bird {
            width: 32px;
            height: 32px;
            background-image: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 32 32"><rect width="32" height="32" fill="%23FFCC66"/><rect x="12" y="8" width="8" height="4" fill="%23000"/><rect x="8" y="12" width="4" height="4" fill="%23000"/><rect x="20" y="12" width="4" height="4" fill="%23000"/><rect x="12" y="16" width="8" height="4" fill="%23000"/><rect x="16" y="20" width="4" height="8" fill="%23000"/></svg>');
        }
        
        /* Pixel art borders */
        .pixel-border {
            border: 4px solid #000;
            box-shadow: 4px 4px 0 rgba(0,0,0,0.3);
            position: relative;
        }
        
        .pixel-border::before {
            content: "";
            position: absolute;
            top: -8px;
            left: -8px;
            right: -8px;
            bottom: -8px;
            border: 4px solid #000;
            z-index: -1;
        }
        
        /* Responsive adjustments */
        @media (max-width: 768px) {
            .walking {
                animation-duration: 20s;
            }
        }
    </style>
</head>
<body class="bg-purple-100 min-h-screen p-4">
    <div class="max-w-4xl mx-auto">
        <!-- Pixel art header -->
        <div class="pixel-border bg-yellow-200 p-6 mb-8 relative overflow-hidden">
            <div class="flex flex-col md:flex-row items-center">
                <div class="w-32 h-32 bg-blue-200 pixel-border mb-4 md:mb-0 md:mr-6 flex items-center justify-center">
                    <div class="w-24 h-24 bg-red-200 pixel"></div>
                </div>
                <div class="flex-1">
                    <h1 class="text-3xl font-bold mb-2 text-gray-800">PixelPaws</h1>
                    <p class="text-gray-700 mb-4">🐾 Pixel art enthusiast & animal lover 🐾</p>
                    <div class="flex space-x-2">
                        <span class="px-3 py-1 bg-green-200 text-gray-800 pixel-border text-sm">JavaScript</span>
                        <span class="px-3 py-1 bg-blue-200 text-gray-800 pixel-border text-sm">HTML/CSS</span>
                        <span class="px-3 py-1 bg-pink-200 text-gray-800 pixel-border text-sm">Pixel Art</span>
                    </div>
                </div>
            </div>
            
            <!-- Animated animals -->
            <div class="absolute top-4 left-0 w-full h-full pointer-events-none">
                <div class="pixel-cat walking absolute top-1/4 left-0"></div>
                <div class="pixel-dog walking absolute top-1/2 left-0" style="animation-delay: 3s;"></div>
                <div class="pixel-bird floating absolute top-1/3 right-10"></div>
                <div class="pixel-cat bouncing absolute bottom-10 right-20" style="animation: bounce 1.5s ease-in-out infinite;"></div>
            </div>
        </div>
        
        <!-- About section -->
        <div class="pixel-border bg-white p-6 mb-8">
            <h2 class="text-2xl font-bold mb-4 text-gray-800 border-b-2 border-gray-300 pb-2">👋 About Me</h2>
            <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                <div>
                    <p class="text-gray-700 mb-4">Hello! I'm a pixel art creator who loves bringing cute animals to life through code and pixels.</p>
                    <p class="text-gray-700 mb-4">When I'm not crafting tiny creatures, you can find me exploring game development or contributing to open source projects.</p>
                    <div class="flex items-center mb-4">
                        <span class="w-4 h-4 bg-red-500 mr-2"></span>
                        <span class="text-gray-700">Currently working on: Pixel Pet Simulator</span>
                    </div>
                    <div class="flex items-center">
                        <span class="w-4 h-4 bg-blue-500 mr-2"></span>
                        <span class="text-gray-700">Learning: Advanced animation techniques</span>
                    </div>
                </div>
                <div class="flex items-center justify-center">
                    <div class="w-48 h-48 bg-gray-100 pixel-border relative overflow-hidden">
                        <!-- Pixel art scene -->
                        <div class="absolute bottom-0 w-full h-8 bg-green-300"></div>
                        <div class="absolute bottom-8 left-8 w-16 h-16 bg-blue-300"></div>
                        <div class="absolute bottom-8 right-8 w-8 h-8 bg-yellow-300"></div>
                        <div class="pixel-cat absolute bottom-8 left-1/2 transform -translate-x-1/2"></div>
                        <div class="pixel-bird absolute top-8 right-8 floating"></div>
                    </div>
                </div>
            </div>
        </div>
        
        <!-- Projects section -->
        <div class="pixel-border bg-white p-6 mb-8">
            <h2 class="text-2xl font-bold mb-4 text-gray-800 border-b-2 border-gray-300 pb-2">🛠️ Projects</h2>
            <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                <div class="pixel-border bg-blue-50 p-4 relative overflow-hidden h-40">
                    <h3 class="font-bold text-lg mb-2">Pixel Pets</h3>
                    <p class="text-gray-700 text-sm mb-2">Adopt and care for pixel art animals</p>
                    <div class="absolute bottom-2 right-2">
                        <div class="pixel-dog bouncing"></div>
                    </div>
                    <div class="absolute top-2 right-2 flex space-x-1">
                        <span class="text-xs bg-blue-200 px-2 py-1 pixel-border">JavaScript</span>
                    </div>
                </div>
                <div class="pixel-border bg-green-50 p-4 relative overflow-hidden h-40">
                    <h3 class="font-bold text-lg mb-2">Animal Crossing</h3>
                    <p class="text-gray-700 text-sm mb-2">Pixel art animals crossing the screen</p>
                    <div class="absolute bottom-2 right-2">
                        <div class="pixel-cat"></div>
                    </div>
                    <div class="absolute top-2 right-2 flex space-x-1">
                        <span class="text-xs bg-green-200 px-2 py-1 pixel-border">CSS</span>
                    </div>
                </div>
                <div class="pixel-border bg-yellow-50 p-4 relative overflow-hidden h-40">
                    <h3 class="font-bold text-lg mb-2">Pixel Zoo</h3>
                    <p class="text-gray-700 text-sm mb-2">Collection of pixel art animals</p>
                    <div class="absolute bottom-2 right-2">
                        <div class="pixel-bird floating"></div>
                    </div>
                    <div class="absolute top-2 right-2 flex space-x-1">
                        <span class="text-xs bg-yellow-200 px-2 py-1 pixel-border">HTML</span>
                    </div>
                </div>
                <div class="pixel-border bg-pink-50 p-4 relative overflow-hidden h-40">
                    <h3 class="font-bold text-lg mb-2">Animal Animator</h3>
                    <p class="text-gray-700 text-sm mb-2">Tool for creating pixel art animations</p>
                    <div class="absolute bottom-2 right-2 flex space-x-2">
                        <div class="pixel-cat"></div>
                        <div class="pixel-dog"></div>
                    </div>
                    <div class="absolute top-2 right-2 flex space-x-1">
                        <span class="text-xs bg-pink-200 px-2 py-1 pixel-border">Canvas</span>
                    </div>
                </div>
            </div>
        </div>
        
        <!-- Stats section -->
        <div class="pixel-border bg-white p-6 mb-8">
            <h2 class="text-2xl font-bold mb-4 text-gray-800 border-b-2 border-gray-300 pb-2">📊 GitHub Stats</h2>
            <div class="grid grid-cols-2 md:grid-cols-4 gap-4 text-center">
                <div class="pixel-border bg-red-100 p-4">
                    <div class="text-3xl font-bold">42</div>
                    <div class="text-sm">Repositories</div>
                </div>
                <div class="pixel-border bg-blue-100 p-4">
                    <div class="text-3xl font-bold">128</div>
                    <div class="text-sm">Commits</div>
                </div>
                <div class="pixel-border bg-green-100 p-4">
                    <div class="text-3xl font-bold">24</div>
                    <div class="text-sm">Followers</div>
                </div>
                <div class="pixel-border bg-yellow-100 p-4">
                    <div class="text-3xl font-bold">12</div>
                    <div class="text-sm">Following</div>
                </div>
            </div>
        </div>
        
        <!-- Footer with social links -->
        <div class="pixel-border bg-gray-800 p-6">
            <h2 class="text-2xl font-bold mb-4 text-white border-b-2 border-gray-500 pb-2">🌐 Connect</h2>
            <div class="flex flex-wrap justify-center gap-4">
                <a href="#" class="px-4 py-2 bg-blue-500 text-white pixel-border hover:bg-blue-600 transition">Twitter</a>
                <a href="#" class="px-4 py-2 bg-purple-500 text-white pixel-border hover:bg-purple-600 transition">Instagram</a>
                <a href="#" class="px-4 py-2 bg-gray-500 text-white pixel-border hover:bg-gray-600 transition">GitHub</a>
                <a href="#" class="px-4 py-2 bg-red-500 text-white pixel-border hover:bg-red-600 transition">YouTube</a>
            </div>
            <div class="mt-6 text-center text-gray-400 text-sm">
                <p>Made with ❤️ and pixels</p>
            </div>
        </div>
    </div>
</body>
</html>
