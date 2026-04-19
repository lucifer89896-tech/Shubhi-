# Shubhi-
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Happy Birthday Shubhi ❤️</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Dancing+Script:wght@400;700&family=Poppins:wght@300;400;600&display=swap');
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Poppins', sans-serif;
            background: linear-gradient(135deg, #ffeef8 0%, #fff1f9 50%, #fff8fd 100%);
            min-height: 100vh;
            overflow-x: hidden;
            position: relative;
        }

        /* Clouds Background */
        .clouds {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 200px;
            z-index: 1;
            pointer-events: none;
        }

        .cloud {
            position: absolute;
            font-size: clamp(2rem, 4vw, 4rem);
            opacity: 0.8;
            animation: drift 20s infinite linear;
        }

        .cloud:nth-child(1) { top: 20px; left: -10%; animation-delay: 0s; }
        .cloud:nth-child(2) { top: 50px; left: -20%; font-size: clamp(1.5rem, 3vw, 3rem); animation-delay: 5s; }
        .cloud:nth-child(3) { top: 80px; left: -15%; animation-delay: 10s; }
        .cloud:nth-child(4) { top: 40px; left: -25%; font-size: clamp(2.5rem, 5vw, 5rem); animation-delay: 15s; }
        .cloud:nth-child(5) { top: 100px; left: -30%; font-size: clamp(1.8rem, 3.5vw, 3.5rem); animation-delay: 2s; }

        @keyframes drift {
            0% { transform: translateX(-20%) translateY(0px); }
            50% { transform: translateX(110%) translateY(-10px); }
            100% { transform: translateX(120%) translateY(0px); }
        }

        .page {
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            padding: 20px;
            text-align: center;
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            opacity: 0;
            transform: translateY(50px);
            transition: all 0.8s ease;
            z-index: 2;
        }

        .page.active {
            opacity: 1;
            transform: translateY(0);
        }

        .page.hidden {
            display: none;
        }

        h1 {
            font-family: 'Dancing Script', cursive;
            font-size: clamp(3rem, 8vw, 6rem);
            color: #ff6b9d;
            margin-bottom: 1rem;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.1);
            z-index: 3;
            position: relative;
        }

        h2 {
            font-family: 'Dancing Script', cursive;
            font-size: clamp(2.5rem, 6vw, 4rem);
            color: #ff1493;
            margin-bottom: 2rem;
            text-shadow: 1px 1px 2px rgba(0,0,0,0.1);
        }

        .content {
            max-width: 800px;
            line-height: 1.8;
            font-size: clamp(1.1rem, 3vw, 1.4rem);
            color: #333;
            margin-bottom: 3rem;
            padding: 0 20px;
        }

        /* First Page Content */
        .birthday-content {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 2rem;
        }

        /* Cake Styles */
        .cake-container {
            margin: 1rem 0;
            perspective: 1000px;
        }

        .cake {
            font-size: 4rem;
            animation: bounce 2s infinite;
        }

        .candle {
            display: inline-block;
            margin: 0 5px;
            animation: flicker 1.5s infinite alternate;
        }

        .candle.flame-1 { color: #ff6b35; }
        .candle.flame-2 { color: #ff8c42; }
        .candle.flame-3 { color: #ffa500; }
        .candle.flame-4 { color: #ff6b35; }

        .cake-base {
            font-size: 3rem;
            background: linear-gradient(45deg, #ff69b4, #ff1493);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            margin-top: 10px;
            text-shadow: none;
        }

        /* Kitty Animation */
        .kitty-container {
            font-size: clamp(3rem, 6vw, 5rem);
            margin: 1rem 0;
        }

        .kitty {
            animation: kittyDance 0.6s infinite;
            display: inline-block;
        }

        .kitty-idle {
            animation: none;
        }

        @keyframes kittyDance {
            0%, 100% { transform: rotate(-10deg) scale(1); }
            25% { transform: rotate(10deg) scale(1.1); }
            50% { transform: rotate(-5deg) scale(1.05); }
            75% { transform: rotate(5deg) scale(1.1); }
        }

        /* Party Popper Animation */
        .party-popper {
            font-size: 3rem;
            margin: 1rem 0;
            cursor: pointer;
            transition: transform 0.3s ease;
            padding: 15px 30px;
            background: linear-gradient(135deg, #ff6b9d, #ff1493);
            border-radius: 50px;
            color: #000;
            font-weight: 600;
            box-shadow: 0 8px 25px rgba(255, 107, 157, 0.4);
        }

        .party-popper:hover {
            transform: scale(1.1);
        }

        .sprinkles {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: 1000;
        }

        .sprinkle {
            position: absolute;
            font-size: 1.5rem;
            pointer-events: none;
            animation: fall linear infinite;
        }

        @keyframes fall {
            0% {
                transform: translateY(-100vh) rotate(0deg);
                opacity: 1;
            }
            100% {
                transform: translateY(100vh) rotate(360deg);
                opacity: 0;
            }
        }

        /* Next Button */
        .next-btn {
            background: linear-gradient(135deg, #ff69b4, #ff1493);
            color: #000;
            border: none;
            padding: 18px 40px;
            font-size: 1.3rem;
            font-weight: 600;
            border-radius: 50px;
            cursor: pointer;
            box-shadow: 0 10px 30px rgba(255, 105, 180, 0.4);
            transition: all 0.3s ease;
            font-family: 'Poppins', sans-serif;
            text-transform: uppercase;
            letter-spacing: 1px;
            position: relative;
            overflow: hidden;
        }

        .next-btn::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255,255,255,0.4), transparent);
            transition: left 0.5s;
        }

        .next-btn:hover::before {
            left: 100%;
        }

        .next-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 15px 40px rgba(255, 105, 180, 0.6);
        }

        /* Final Page Balloons */
        .balloons-container {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: 10;
        }

        .balloon {
            position: absolute;
            font-size: clamp(2rem, 5vw, 4rem);
            animation: float 8s infinite ease-in-out;
        }

        @keyframes float {
            0% {
                transform: translateY(100vh) scale(0);
                opacity: 0;
            }
            10% {
                opacity: 1;
            }
            90% {
                opacity: 1;
            }
            100% {
                transform: translateY(-100px) scale(1);
                opacity: 0;
            }
        }

        .heart {
            color: #ff69b4;
            text-shadow: 0 0 20px rgba(255, 105, 180, 0.8);
        }

        .final-message {
            font-family: 'Dancing Script', cursive;
            font-size: clamp(3rem, 10vw, 6rem);
            color: #ff1493;
            text-shadow: 2px 2px 10px rgba(255, 105, 180, 0.5);
            z-index: 20;
            position: relative;
        }

        /* Animations */
        @keyframes bounce {
            0%, 20%, 50%, 80%, 100% { transform: translateY(0); }
            40% { transform: translateY(-20px); }
            60% { transform: translateY(-10px); }
        }

        @keyframes flicker {
            0%, 100% { text-shadow: 0 0 5px currentColor; }
            50% { text-shadow: 0 0 20px currentColor, 0 0 30px currentColor; }
        }

        /* Responsive */
        @media (max-width: 768px) {
            .birthday-content {
                gap: 1rem;
            }
            
            .content {
                padding: 0 10px;
            }
        }
    </style>
</head>
<body>
    <!-- Clouds -->
    <div class="clouds">
        <div class="cloud">☁️☁️☁️</div>
        <div class="cloud">☁️☁️</div>
        <div class="cloud">☁️☁️☁️☁️</div>
        <div class="cloud">☁️☁️☁️</div>
        <div class="cloud">☁️☁️</div>
    </div>

    <!-- Page 1: Happy Birthday -->
    <div id="page1" class="page active">
        <h1>Happy Birthday Shubhi</h1>
        
        <div class="birthday-content">
            <div class="kitty-container">
                <div class="kitty kitty-idle" id="kitty">😻</div>
            </div>

            <div class="cake-container">
                <div class="cake" id="cake">
                    <div class="candle flame-1">🕯️</div>
                    <div class="candle flame-2">🕯️</div>
                    <div class="candle flame-3">🕯️</div>
                    <div class="candle flame-4">🕯️</div>
                </div>
                <div class="cake-base">🎂</div>
            </div>

            <div class="party-popper" onclick="blowPopper()">🎉 BLEW 🎉</div>
            <div class="sprinkles" id="sprinkles1"></div>
        </div>
        
        <button class="next-btn" onclick="nextPage()">Next</button>
    </div>

    <!-- Page 2: Our Journey -->
    <div id="page2" class="page">
        <h2>Our Journey</h2>
        <div class="content">
            You know, when I saw you first time, I just felt something for you, and I know at that time that it was not possible, but I had in my mind that I will make it possible, and if my love is true, the God will make it possible, and I think it is, and here we are, on a journey together to be life partners forever. 
            <br><br>
            And, you know, I just love how you are. I don't want to change you. I don't want to restrict you from doing anything. I just want you to achieve success in your life, and I want that we spend this life together, living happily and becoming a great couple and great parents also. 
            <br><br>
            And I don't know how to define you, what I feel, but what I feel is so real, so pure for you that it's just beyond your imagination. 
            <br><br>
            <strong>And at the last, I can say all is: I love you.</strong>
        </div>
        <button class="next-btn" onclick="nextPage()">Next</button>
    </div>

    <!-- Page 3: You Are Perfect (NEW) -->
    <div id="page3" class="page">
        <h2>You Are Perfect</h2>
        <div class="content">
            I know you doubt yourself sometimes, but I wish you could see yourself through my eyes. Then you would truly realize how beautiful and cute you are.
            <br><br>
            Whenever I look into your eyes, they are just so beautiful like the ocean and I always get lost in them. Your cheeks are simply adorable, and that little blush on them makes you the cutest in the world. Your lips are cute too, but honestly, your whole face is just very, very pretty and of course, your personality the way you are it makes you even more special. 
            <br><br>
            You are such a charming, beautiful, and pretty girl. So please, never doubt yourself.
            <br><br>
            <strong>And once again, I love you. ❤️</strong>
        </div>
        <button class="next-btn" onclick="nextPage()">Next</button>
    </div>

    <!-- Page 4: Final Love Message -->
    <div id="page4" class="page" style="background: #fff;">
        <div class="balloons-container" id="balloons"></div>
        <div class="final-message">I Love You Shubhi 💕</div>
    </div>

    <script>
        let currentPage = 1;
        const totalPages = 4;

        function nextPage() {
            const current = document.getElementById(`page${currentPage}`);
            current.classList.remove('active');
            currentPage++;
            
            if (currentPage <= totalPages) {
                const next = document.getElementById(`page${currentPage}`);
                next.classList.add('active');
                
                // Start balloons on final page
                if (currentPage === 4) {
                    startBalloons();
                }
            }
        }

        function blowPopper() {
            // Animate kitty
            const kitty = document.getElementById('kitty');
            kitty.classList.remove('kitty-idle');
            kitty.classList.add('kitty');
            
            // Animate cake more vigorously
            const cake = document.getElementById('cake');
            cake.style.animation = 'bounce 0.5s infinite';
            
            // Party popper sprinkles
            const sprinkles = document.getElementById('sprinkles1');
            sprinkles.innerHTML = '';
            
            for (let i = 0; i < 50; i++) {
                setTimeout(() => {
                    createSprinkle(sprinkles);
                }, i * 50);
            }
            
            // Reset animations after 3 seconds
            setTimeout(() => {
                kitty.classList.add('kitty-idle');
                kitty.classList.remove('kitty');
                cake.style.animation = 'bounce 2s infinite';
            }, 3000);
        }

        function createSprinkle(container) {
            const sprinkle = document.createElement('div');
            const emojis = ['🎉', '✨', '⭐', '💖', '🌟', '🎊', '💫', '🎈', '💕', '🌈'];
            sprinkle.innerHTML = emojis[Math.floor(Math.random() * emojis.length)];
            sprinkle.className = 'sprinkle';
            
            sprinkle.style.left = Math.random() * 100 + '%';
            sprinkle.style.animationDuration = (Math.random() * 3 + 2) + 's';
            sprinkle.style.animationDelay = Math.random() * 2 + 's';
            
            container.appendChild(sprinkle);
            
            setTimeout(() => {
                sprinkle.remove();
            }, 5000);
        }

        function startBalloons() {
            const container = document.getElementById('balloons');
            setInterval(() => {
                const balloon = document.createElement('div');
                balloon.className = 'balloon heart';
                balloon.innerHTML = '💖';
                balloon.style.left = Math.random() * 100 + '%';
                balloon.style.animationDuration = (Math.random() * 4 + 6) + 's';
                balloon.style.fontSize = (Math.random() * 2 + 2) + 'rem';
                container.appendChild(balloon);
                
                setTimeout(() => {
                    balloon.remove();
                }, 10000);
            }, 300);
        }

        // Prevent scrolling
        window.addEventListener('scroll', () => {
            window.scrollTo(0, 0);
        });
    </script>
</body>
</html>
```
