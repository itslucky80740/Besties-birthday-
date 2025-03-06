# Besties-birthday-
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Happiest Birthday Bacchu 💝🫶🏻</title>
    <style>
        body {
            text-align: center;
            background-color: #ffd6e5;
            font-family: 'Comic Sans MS', cursive, sans-serif;
            overflow: hidden;
        }

        h1 {
            color: #ff4d79;
            font-size: 50px;
            animation: glow 1.5s infinite alternate;
        }

        @keyframes glow {
            from { text-shadow: 0 0 10px #ff4d79, 0 0 20px #ff99b8; }
            to { text-shadow: 0 0 20px #ff99b8, 0 0 30px #ff4d79; }
        }

        #message {
            font-size: 22px;
            color: #ff007f;
            margin: 20px auto;
            width: 60%;
            background: #fff3f8;
            padding: 15px;
            border-radius: 15px;
            box-shadow: 0 0 10px #ff99b8;
        }

        .cute-animation {
            position: absolute;
            width: 50px;
            animation: float 5s infinite;
        }

        @keyframes float {
            0% { transform: translateY(0); }
            50% { transform: translateY(-20px); }
            100% { transform: translateY(0); }
        }

        .cake-container {
            margin-top: 50px;
            position: relative;
        }

        .cake {
            width: 200px;
        }

        .candle {
            width: 20px;
            position: absolute;
            top: -80px;
            left: 50%;
            transform: translateX(-50%);
        }

        .flame {
            width: 15px;
            position: absolute;
            top: -30px;
            left: 50%;
            transform: translateX(-50%);
            animation: flicker 0.5s infinite alternate;
        }

        @keyframes flicker {
            from { opacity: 1; transform: scale(1.1); }
            to { opacity: 0.8; transform: scale(1); }
        }

        #balloons {
            position: absolute;
            width: 100%;
            height: 100%;
            top: 0;
            left: 0;
            overflow: hidden;
            pointer-events: none;
        }

        .balloon {
            position: absolute;
            width: 40px;
            animation: rise 6s infinite;
        }

        @keyframes rise {
            from { transform: translateY(100vh); opacity: 1; }
            to { transform: translateY(-10vh); opacity: 0; }
        }
    </style>
</head>
<body>
    <h1>Happiest Birthday Bacchu 💝🫶🏻</h1>

    <div id="message">✨ Happy Birthday to the most wonderful, adorable, and kind-hearted person! May your life be filled with love, joy, and endless happiness! ✨</div>

    <div class="cake-container">
        <img src="https://i.imgur.com/O7bY8Yx.png" class="cake" alt="Birthday Cake">
        <img src="https://i.imgur.com/DPKpTPI.png" class="candle" alt="Candle">
        <img src="https://i.imgur.com/M1RJbHJ.png" class="flame" id="flame" alt="Flame">
    </div>

    <p>🎂 Blow out the candle by clicking on it! 🎂</p>

    <audio id="birthdaySong" loop>
        <source src="https://www.fesliyanstudios.com/play-mp3/387" type="audio/mpeg">
    </audio>

    <div id="balloons"></div>

    <script>
        document.body.addEventListener("click", function() {
            document.getElementById("birthdaySong").play();
        });

        document.getElementById("flame").addEventListener("click", function() {
            this.style.display = "none";
            alert("🎉 Yay! You blew out the candle! 🎉");
        });

        function createBalloon() {
            const balloon = document.createElement("img");
            balloon.src = "https://i.imgur.com/7dQm9Yj.png";
            balloon.classList.add("balloon");
            balloon.style.left = Math.random() * 100 + "vw";
            balloon.style.animationDuration = (Math.random() * 3 + 4) + "s";
            document.getElementById("balloons").appendChild(balloon);
            setTimeout(() => balloon.remove(), 6000);
        }

        setInterval(createBalloon, 800);
    </script>
</body>
</html>
