# Love-
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Happy Valentine's Day - From Rishabh</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Dancing+Script:wght@700&family=Poppins:wght@400;600;800&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Poppins', sans-serif;
            overflow: hidden;
            transition: background-color 1.5s ease;
        }
        
        .font-romantic {
            font-family: 'Dancing Script', cursive;
        }
        
        /* Gift Box Animations */
        @keyframes float {
            0%, 100% { transform: translateY(0px); }
            50% { transform: translateY(-20px); }
        }
        
        @keyframes shake {
            0%, 100% { transform: rotate(0deg); }
            25% { transform: rotate(-5deg); }
            75% { transform: rotate(5deg); }
        }
        
        @keyframes popOpen {
            0% { transform: scale(1); }
            50% { transform: scale(1.1); }
            100% { transform: scale(0) rotate(720deg); opacity: 0; }
        }
        
        .gift-float {
            animation: float 3s ease-in-out infinite;
        }
        
        .gift-shake {
            animation: shake 0.5s ease-in-out infinite;
        }
        
        .gift-pop {
            animation: popOpen 0.8s ease-in-out forwards;
        }
        
        /* Heart Particles */
        @keyframes floatUp {
            0% { transform: translateY(100vh) scale(0); opacity: 0; }
            10% { opacity: 1; }
            90% { opacity: 1; }
            100% { transform: translateY(-100vh) scale(1.5); opacity: 0; }
        }
        
        .heart-particle {
            position: absolute;
            color: #ff6b9d;
            font-size: 24px;
            animation: floatUp 4s linear infinite;
            pointer-events: none;
        }
        
        /* Button Escape Animation */
        @keyframes escape {
            0% { transform: translate(0, 0); }
            25% { transform: translate(50px, -30px); }
            50% { transform: translate(-30px, 50px); }
            75% { transform: translate(40px, 40px); }
            100% { transform: translate(-50px, -20px); }
        }
        
        .btn-escape {
            animation: escape 0.3s ease-in-out;
        }
        
        /* Glow Effects */
        .glow-text {
            text-shadow: 0 0 20px rgba(255, 107, 157, 0.8), 0 0 40px rgba(255, 107, 157, 0.4);
        }
        
        .btn-glow {
            box-shadow: 0 0 20px rgba(255, 107, 157, 0.6);
            transition: all 0.3s ease;
        }
        
        .btn-glow:hover {
            box-shadow: 0 0 30px rgba(255, 107, 157, 0.9);
            transform: scale(1.05);
        }
        
        /* Background Transition */
        .bg-yellow-theme {
            background: linear-gradient(135deg, #fef3c7 0%, #fde68a 50%, #fcd34d 100%);
        }
        
        .bg-pink-theme {
            background: linear-gradient(135deg, #fce7f3 0%, #fbcfe8 50%, #f9a8d4 100%);
        }
        
        /* Hidden/Visible States */
        .hidden-custom {
            display: none !important;
        }
        
        .fade-in {
            animation: fadeIn 1s ease-in forwards;
        }
        
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        /* Sparkle Animation */
        @keyframes sparkle {
            0%, 100% { transform: scale(0) rotate(0deg); opacity: 0; }
            50% { transform: scale(1) rotate(180deg); opacity: 1; }
        }
        
        .sparkle {
            position: absolute;
            width: 20px;
            height: 20px;
            background: white;
            clip-path: polygon(50% 0%, 61% 35%, 98% 35%, 68% 57%, 79% 91%, 50% 70%, 21% 91%, 32% 57%, 2% 35%, 39% 35%);
            animation: sparkle 2s ease-in-out infinite;
        }
    </style>
</head>
<body class="bg-yellow-theme h-screen w-screen flex items-center justify-center relative">

    <!-- Floating Hearts Background -->
    <div id="hearts-container" class="absolute inset-0 overflow-hidden pointer-events-none"></div>

    <!-- GIFT SCENE -->
    <div id="gift-scene" class="text-center z-10 cursor-pointer transition-all duration-500">
        <div class="gift-float" id="gift-box">
            <!-- Gift Box SVG -->
            <svg width="200" height="200" viewBox="0 0 200 200" class="mx-auto drop-shadow-2xl">
                <!-- Box Base -->
                <rect x="20" y="80" width="160" height="100" fill="#ff6b6b" rx="10"/>
                <rect x="20" y="80" width="160" height="20" fill="#ee5a5a" rx="5"/>
                <!-- Vertical Ribbon -->
                <rect x="85" y="80" width="30" height="100" fill="#ffd93d"/>
                <!-- Horizontal Ribbon -->
                <rect x="20" y="115" width="160" height="20" fill="#ffd93d"/>
                <!-- Lid -->
                <rect x="10" y="50" width="180" height="40" fill="#ff8585" rx="8"/>
                <rect x="85" y="50" width="30" height="40" fill="#ffed4e"/>
                <!-- Bow -->
                <path d="M100 50 Q70 20 50 40 Q30 60 60 70 Q80 80 100 50" fill="#ff4757"/>
                <path d="M100 50 Q130 20 150 40 Q170 60 140 70 Q120 80 100 50" fill="#ff4757"/>
                <circle cx="100" cy="50" r="15" fill="#ff3344"/>
            </svg>
            <p class="mt-6 text-2xl text-gray-700 font-semibold animate-pulse">Tap to Open Your Gift! 🎁</p>
        </div>
    </div>

    <!-- QUESTION SCENE -->
    <div id="question-scene" class="hidden-custom text-center z-10 max-w-lg px-6">
        <div class="bg-white/80 backdrop-blur-lg rounded-3xl p-8 shadow-2xl border-4 border-pink-300">
            <h1 class="text-4xl md:text-5xl font-romantic text-pink-600 mb-8 glow-text">
                Will You Be My Valentine Or my life patner miss Sandhya
            </h1>
            
            <div class="flex gap-6 justify-center items-center relative h-32">
                <button id="yes-btn" class="bg-gradient-to-r from-pink-500 to-rose-500 text-white px-8 py-4 rounded-full text-xl font-bold btn-glow transform transition hover:scale-110">
                    Yes! 💝
                </button>
                
                <button id="no-btn" class="bg-gray-400 text-white px-8 py-4 rounded-full text-xl font-bold transition-all duration-200 hover:bg-gray-500 relative">
                    No 💔
                </button>
            </div>
            
            <p class="mt-6 text-gray-600 text-sm italic">Choose wisely... (I am extermly sorry take a heart from me 😊)</p>
        </div>
    </div>

    <!-- SUCCESS SCENE -->
    <div id="success-scene" class="hidden-custom text-center z-10">
        <div class="fade-in">
            <h1 class="text-6xl md:text-8xl font-romantic text-pink-600 mb-4 glow-text">
                Thankyou bebe choosing me i promise i will be the best patner of your life promise my princess
            </h1>
            <h2 class="text-3xl md:text-4xl text-pink-500 font-semibold mb-8">
                My Baby! 💕
            </h2>
            <div class="text-8xl animate-bounce">🌹💖🌹</div>
            <p class="mt-8 text-xl text-pink-700 font-medium">From Rishabh with Love</p>
        </div>
    </div>

    <script>
        // Elements
        const giftScene = document.getElementById('gift-scene');
        const giftBox = document.getElementById('gift-box');
        const questionScene = document.getElementById('question-scene');
        const successScene = document.getElementById('success-scene');
        const yesBtn = document.getElementById('yes-btn');
        const noBtn = document.getElementById('no-btn');
        const body = document.body;
        const heartsContainer = document.getElementById('hearts-container');

        // Create floating hearts
        function createHeart() {
            const heart = document.createElement('div');
            heart.className = 'heart-particle';
            heart.innerHTML = '💖';
            heart.style.left = Math.random() * 100 + '%';
            heart.style.animationDuration = (Math.random() * 3 + 3) + 's';
            heart.style.animationDelay = Math.random() * 2 + 's';
            heartsContainer.appendChild(heart);
            
            setTimeout(() => heart.remove(), 6000);
        }

        setInterval(createHeart, 300);

        // Gift Box Interaction
        giftScene.addEventListener('click', function() {
            giftBox.classList.remove('gift-float');
            giftBox.classList.add('gift-pop');
            
            // Create explosion of hearts
            for(let i = 0; i < 20; i++) {
                setTimeout(createHeart, i * 50);
            }
            
            setTimeout(() => {
                giftScene.classList.add('hidden-custom');
                questionScene.classList.remove('hidden-custom');
                questionScene.classList.add('fade-in');
            }, 800);
        });

        // Hover effects for gift
        giftScene.addEventListener('mouseenter', () => {
            if(!giftBox.classList.contains('gift-pop')) {
                giftBox.classList.add('gift-shake');
            }
        });

        giftScene.addEventListener('mouseleave', () => {
            giftBox.classList.remove('gift-shake');
        });

        // Yes Button - Success!
        yesBtn.addEventListener('click', function() {
            // Change background from yellow to pink
            body.classList.remove('bg-yellow-theme');
            body.classList.add('bg-pink-theme');
            
            // Transition scenes
            questionScene.classList.add('hidden-custom');
            successScene.classList.remove('hidden-custom');
            
            // Massive heart explosion
            for(let i = 0; i < 50; i++) {
                setTimeout(createHeart, i * 30);
            }
            
            // Create sparkles
            for(let i = 0; i < 10; i++) {
                const sparkle = document.createElement('div');
                sparkle.className = 'sparkle';
                sparkle.style.left = Math.random() * 100 + '%';
                sparkle.style.top = Math.random() * 100 + '%';
                sparkle.style.animationDelay = Math.random() * 2 + 's';
                document.body.appendChild(sparkle);
            }
        });

        // No Button - Run away!
        noBtn.addEventListener('mouseover', function() {
            moveButton();
        });

        noBtn.addEventListener('click', function(e) {
            e.preventDefault();
            moveButton();
        });

        function moveButton() {
            const container = questionScene.querySelector('.bg-white\\/80');
            const containerRect = container.getBoundingClientRect();
            const btnRect = noBtn.getBoundingClientRect();
            
            // Calculate random position within container bounds
            const maxX = containerRect.width - btnRect.width - 40;
            const maxY = containerRect.height - btnRect.height - 40;
            
            const randomX = Math.random() * maxX - (maxX/2);
            const randomY = Math.random() * maxY - (maxY/2);
            
            noBtn.style.transform = `translate(${randomX}px, ${randomY}px)`;
            noBtn.style.transition = 'transform 0.3s cubic-bezier(0.68, -0.55, 0.265, 1.55)';
            
            // Add shake effect
            noBtn.classList.add('btn-escape');
            setTimeout(() => noBtn.classList.remove('btn-escape'), 300);
        }

        // Touch support for mobile
        noBtn.addEventListener('touchstart', function(e) {
            e.preventDefault();
            moveButton();
        });
    </script>
</body>
</html>



