# Trishu-s-birthday-
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Happy Birthday Trishu</title>
    <style>
        * { margin: 0; padding: 0; box-sizing: border-box; }
        body, html { width: 100%; height: 100%; font-family: 'Segoe UI', sans-serif; overflow: hidden; }
        #startScreen, #mainContent, #letterScreen, #galleryScreen { position: absolute; width: 100%; height: 100%; display: none; justify-content: center; align-items: center; text-align: center; }

        /* Start screen */
        #startScreen { background-color: black; color: pink; display: flex; flex-direction: column; }
        #startBtn { padding: 15px 30px; font-size: 20px; border: 2px solid pink; background: transparent; color: pink; cursor: pointer; border-radius: 10px; }

        /* Main birthday screen */
        #mainContent { background-color: #ffe6f0; color: #ff3399; flex-direction: column; display: flex; }
        #startLoveBtn { padding: 15px 30px; font-size: 20px; border: none; background: #ff99cc; color: white; cursor: pointer; border-radius: 10px; margin-top: 20px; }

        /* Letter Screen */
        #letterScreen { background-color: #fff0f5; color: #ff3399; flex-direction: column; display: flex; padding: 20px; }
        .handwritten { font-family: 'Brush Script MT', cursive; font-size: 22px; white-space: pre-line; color: #cc0066; }

        /* Gallery Screen */
        #galleryScreen { background-color: #ffe6f0; color: #ff3399; flex-direction: column; display: flex; }
        .gallery img { width: 200px; height: auto; margin: 10px; border-radius: 10px; }

        /* Feedback */
        #feedbackBox { margin-top: 20px; }
        textarea { width: 80%; height: 100px; border: 2px solid #ff3399; border-radius: 10px; padding: 10px; font-size: 16px; }
        #sendBtn { margin-top: 10px; padding: 10px 20px; background: #ff3399; color: white; border: none; border-radius: 5px; cursor: pointer; }

        /* Petals animation */
        .petal {
            position: fixed;
            top: -50px;
            background: pink;
            border-radius: 50%;
            opacity: 0.8;
            width: 15px;
            height: 15px;
            animation: fall linear infinite;
        }

        @keyframes fall {
            0% { transform: translateY(0) rotate(0); }
            100% { transform: translateY(100vh) rotate(360deg); }
        }

    </style>
</head>
<body>

    <!-- Start Screen -->
    <div id="startScreen">
        <h1 style="color:white; font-size: 24px;">Loading...</h1>
        <button id="startBtn" style="display:none;">Click to Start</button>
    </div>

    <!-- Main Birthday Content -->
    <div id="mainContent">
        <h1>Happy Birthday Dear Trishu</h1>
        <button id="startLoveBtn">Kya Hum Shuru Karein?</button>
    </div>

    <!-- Handwritten Letter Screen -->
    <div id="letterScreen">
        <h2 style="margin-bottom: 20px;">Dear Special One</h2>
        <p class="handwritten">
            Aap mere liye sabse khaas ho,  
            bhale hi ap mujse baat karo yaa na karo...  
            aap jese bhi ho dil ke bahut paas hoo...  
            i know aapki life me bhut problems hai  
            but me aapke saath hamesha rahunga,  
            hum aapko rote hue nahi dekhh sakte,  
            isliye aapna khyaal rakha karo.  
            I always love you more than my limits...
        </p>
        <button id="openGalleryBtn">Next</button>
    </div>

    <!-- Gallery Screen -->
    <div id="galleryScreen">
        <h2>Our Special Memories</h2>
        <div class="gallery">
            <img src="https://via.placeholder.com/200?text=Photo+1" alt="Photo 1">
            <img src="https://via.placeholder.com/200?text=Photo+2" alt="Photo 2">
            <img src="https://via.placeholder.com/200?text=Photo+3" alt="Photo 3">
        </div>
        <div id="feedbackBox">
            <textarea placeholder="Jaan, agar aapko kuch kehna hai toh yahan likh sakti ho."></textarea><br>
            <button id="sendBtn">Send</button>
        </div>
    </div>

    <!-- Petals Animation -->
    <script>
        function createPetal() {
            const petal = document.createElement('div');
            petal.classList.add('petal');
            petal.style.left = Math.random() * 100 + "vw";
            petal.style.animationDuration = (Math.random() * 3 + 2) + "s";
            document.body.appendChild(petal);

            setTimeout(() => {
                petal.remove();
            }, 5000);
        }

        setInterval(createPetal, 300);

        // Screen transitions
        window.onload = function() {
            const startScreen = document.getElementById('startScreen');
            const startBtn = document.getElementById('startBtn');
            const mainContent = document.getElementById('mainContent');
            const startLoveBtn = document.getElementById('startLoveBtn');
            const letterScreen = document.getElementById('letterScreen');
            const openGalleryBtn = document.getElementById('openGalleryBtn');
            const galleryScreen = document.getElementById('galleryScreen');
            const sendBtn = document.getElementById('sendBtn');

            startScreen.style.display = 'flex';
            setTimeout(() => {
                startScreen.querySelector('h1').style.display = 'none';
                startBtn.style.display = 'block';
            }, 3000);

            startBtn.onclick = () => {
                startScreen.style.display = 'none';
                mainContent.style.display = 'flex';
            }

            startLoveBtn.onclick = () => {
                mainContent.style.display = 'none';
                letterScreen.style.display = 'flex';
            }

            openGalleryBtn.onclick = () => {
                letterScreen.style.display = 'none';
                galleryScreen.style.display = 'flex';
            }

            sendBtn.onclick = () => {
                alert("Thank you so much jaan, I love you so much 😘😘😘");
            }
        }
    </script>

    <!-- Background Music Placeholder -->
    <!-- <audio src="your-music-file.mp3" autoplay loop></audio> -->

</body>
</html>
