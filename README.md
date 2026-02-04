<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>System Diagnostic: User 'Divyanshu'</title>
    <style>
        body {
            background-color: #0d0221;
            color: #fff;
            font-family: 'Comic Sans MS', cursive, sans-serif;
            display: flex;
            align-items: center;
            justify-content: center;
            height: 100vh;
            margin: 0;
            overflow: hidden;
            text-align: center;
        }

        #setup, #finale, #call-screen {
            background: rgba(255, 255, 255, 0.1);
            padding: 25px;
            border-radius: 20px;
            backdrop-filter: blur(10px);
            border: 2px solid #e94560;
            width: 320px;
            box-shadow: 0 0 30px rgba(233, 69, 96, 0.5);
        }

        #finale, #call-screen { display: none; }

        .pfp {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            border: 5px solid #ff00ff;
            margin-bottom: 15px;
            object-fit: cover;
        }

        .meter { height: 15px; background: #222; border-radius: 10px; margin: 15px 0; overflow: hidden; }
        .fill { height: 100%; width: 0%; background: linear-gradient(90deg, #ff00ff, #00ffff); transition: width 0.2s; }

        button {
            padding: 12px 20px;
            border-radius: 10px;
            border: none;
            cursor: pointer;
            font-weight: bold;
            margin-top: 10px;
            width: 100%;
        }

        #yesBtn { background: #e94560; color: white; }
        #noBtn { background: #444; color: #888; position: absolute; transition: 0.1s; }
        .call-btn { background: #2ecc71; color: white; animation: shake 0.5s infinite; }

        @keyframes shake {
            0% { transform: rotate(0deg); }
            25% { transform: rotate(5deg); }
            75% { transform: rotate(-5deg); }
            100% { transform: rotate(0deg); }
        }

        .incoming-pfp { width: 100px; height: 100px; border-radius: 50%; background: #555; display: inline-block; margin-bottom: 20px; font-size: 50px; line-height: 100px; }
    </style>
</head>
<body>

    <audio id="bgMusic" loop><source src="funny_song.mp3" type="audio/mpeg"></audio>

    <div id="setup">
        <h2 style="color: #ff00ff;">GF SHORTAGE! ⚠️</h2>
        <p>Detected: No girlfriend found for Divyanshu. Initiating Friend-to-GF conversion...</p>
        <div class="meter"><div class="fill" id="meter"></div></div>
        <div style="height: 100px; position: relative;">
            <button id="yesBtn" onclick="finishPrank()">ACCEPT UPGRADE 💅</button>
            <button id="noBtn" onmouseover="dodge()">STAY SINGLE</button>
        </div>
    </div>

    <div id="finale">
        <img src="divyanshu.jpg" class="pfp" alt="Divyanshu">
        <h2 style="color: #00ff00;">CONVERSION SUCCESS!</h2>
        <p>Divyanshu, you are now officially under my protection. Maintenance fees apply.</p>
        <button class="call-btn" onclick="triggerCall()">CALL YOUR BOYFRIEND</button>
    </div>

    <div id="call-screen">
        <div class="incoming-pfp">🧔🏻‍♂️</div>
        <h2>Incoming Call...</h2>
        <h1 style="color: #2ecc71;">MY BELOVED BF ❤️</h1>
        <p>00:03</p>
        <div style="display: flex; justify-content: space-around; margin-top: 30px;">
            <div style="background: #e74c3c; width: 60px; height: 60px; border-radius: 50%; line-height: 60px; font-size: 30px;">📵</div>
            <div style="background: #2ecc71; width: 60px; height: 60px; border-radius: 50%; line-height: 60px; font-size: 30px;">📞</div>
        </div>
        <button onclick="location.reload()" style="background:none; border: 1px solid #555; color: #555; margin-top: 40px;">End Prank</button>
    </div>

    <script>
        function dodge() {
            const btn = document.getElementById('noBtn');
            btn.style.left = Math.random() * 200 + 'px';
            btn.style.top = Math.random() * 300 + 'px';
            btn.style.position = 'fixed';
            let meter = document.getElementById('meter');
            let currentWidth = parseInt(meter.style.width) || 0;
            if(currentWidth < 100) meter.style.width = (currentWidth + 10) + '%';
        }

        function finishPrank() {
            document.getElementById('bgMusic').play();
            document.getElementById('setup').style.display = 'none';
            document.getElementById('finale').style.display = 'block';
        }

        function triggerCall() {
            document.getElementById('finale').style.display = 'none';
            document.getElementById('call-screen').style.display = 'block';
            if (navigator.vibrate) navigator.vibrate([500, 200, 500, 200, 500]);
        }
    </script>
</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>System Diagnostic: User 'Divyanshu'</title>
    <style>
        body {
            background-color: #0d0221;
            color: #fff;
            font-family: 'Comic Sans MS', cursive, sans-serif;
            display: flex;
            align-items: center;
            justify-content: center;
            height: 100vh;
            margin: 0;
            overflow: hidden;
            text-align: center;
        }

        #setup, #finale, #call-screen {
            background: rgba(255, 255, 255, 0.1);
            padding: 25px;
            border-radius: 20px;
            backdrop-filter: blur(10px);
            border: 2px solid #e94560;
            width: 320px;
            box-shadow: 0 0 30px rgba(233, 69, 96, 0.5);
        }

        #finale, #call-screen { display: none; }

        .pfp {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            border: 5px solid #ff00ff;
            margin-bottom: 15px;
            object-fit: cover;
        }

        .meter { height: 15px; background: #222; border-radius: 10px; margin: 15px 0; overflow: hidden; }
        .fill { height: 100%; width: 0%; background: linear-gradient(90deg, #ff00ff, #00ffff); transition: width 0.2s; }

        button {
            padding: 12px 20px;
            border-radius: 10px;
            border: none;
            cursor: pointer;
            font-weight: bold;
            margin-top: 10px;
            width: 100%;
        }

        #yesBtn { background: #e94560; color: white; }
        #noBtn { background: #444; color: #888; position: absolute; transition: 0.1s; }
        .call-btn { background: #2ecc71; color: white; animation: shake 0.5s infinite; }

        @keyframes shake {
            0% { transform: rotate(0deg); }
            25% { transform: rotate(5deg); }
            75% { transform: rotate(-5deg); }
            100% { transform: rotate(0deg); }
        }

        .incoming-pfp { width: 100px; height: 100px; border-radius: 50%; background: #555; display: inline-block; margin-bottom: 20px; font-size: 50px; line-height: 100px; }
    </style>
</head>
<body>

    <audio id="bgMusic" loop><source src="funny_song.mp3" type="audio/mpeg"></audio>

    <div id="setup">
        <h2 style="color: #ff00ff;">GF SHORTAGE! ⚠️</h2>
        <p>Detected: No girlfriend found for Divyanshu. Initiating Friend-to-GF conversion...</p>
        <div class="meter"><div class="fill" id="meter"></div></div>
        <div style="height: 100px; position: relative;">
            <button id="yesBtn" onclick="finishPrank()">ACCEPT UPGRADE 💅</button>
            <button id="noBtn" onmouseover="dodge()">STAY SINGLE</button>
        </div>
    </div>

    <div id="finale">
        <img src="divyanshu.jpg" class="pfp" alt="Divyanshu">
        <h2 style="color: #00ff00;">CONVERSION SUCCESS!</h2>
        <p>Divyanshu, you are now officially under my protection. Maintenance fees apply.</p>
        <button class="call-btn" onclick="triggerCall()">CALL YOUR BOYFRIEND</button>
    </div>

    <div id="call-screen">
        <div class="incoming-pfp">🧔🏻‍♂️</div>
        <h2>Incoming Call...</h2>
        <h1 style="color: #2ecc71;">MY BELOVED BF ❤️</h1>
        <p>00:03</p>
        <div style="display: flex; justify-content: space-around; margin-top: 30px;">
            <div style="background: #e74c3c; width: 60px; height: 60px; border-radius: 50%; line-height: 60px; font-size: 30px;">📵</div>
            <div style="background: #2ecc71; width: 60px; height: 60px; border-radius: 50%; line-height: 60px; font-size: 30px;">📞</div>
        </div>
        <button onclick="location.reload()" style="background:none; border: 1px solid #555; color: #555; margin-top: 40px;">End Prank</button>
    </div>

    <script>
        function dodge() {
            const btn = document.getElementById('noBtn');
            btn.style.left = Math.random() * 200 + 'px';
            btn.style.top = Math.random() * 300 + 'px';
            btn.style.position = 'fixed';
            let meter = document.getElementById('meter');
            let currentWidth = parseInt(meter.style.width) || 0;
            if(currentWidth < 100) meter.style.width = (currentWidth + 10) + '%';
        }

        function finishPrank() {
            document.getElementById('bgMusic').play();
            document.getElementById('setup').style.display = 'none';
            document.getElementById('finale').style.display = 'block';
        }

        function triggerCall() {
            document.getElementById('finale').style.display = 'none';
            document.getElementById('call-screen').style.display = 'block';
            if (navigator.vibrate) navigator.vibrate([500, 200, 500, 200, 500]);
        }
    </script>
</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>System Diagnostic: User 'Divyanshu'</title>
    <style>
        body {
            background-color: #0d0221;
            color: #fff;
            font-family: 'Comic Sans MS', cursive, sans-serif;
            display: flex;
            align-items: center;
            justify-content: center;
            height: 100vh;
            margin: 0;
            overflow: hidden;
            text-align: center;
        }

        #setup, #finale, #call-screen {
            background: rgba(255, 255, 255, 0.1);
            padding: 25px;
            border-radius: 20px;
            backdrop-filter: blur(10px);
            border: 2px solid #e94560;
            width: 320px;
            box-shadow: 0 0 30px rgba(233, 69, 96, 0.5);
        }

        #finale, #call-screen { display: none; }

        .pfp {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            border: 5px solid #ff00ff;
            margin-bottom: 15px;
            object-fit: cover;
        }

        .meter { height: 15px; background: #222; border-radius: 10px; margin: 15px 0; overflow: hidden; }
        .fill { height: 100%; width: 0%; background: linear-gradient(90deg, #ff00ff, #00ffff); transition: width 0.2s; }

        button {
            padding: 12px 20px;
            border-radius: 10px;
            border: none;
            cursor: pointer;
            font-weight: bold;
            margin-top: 10px;
            width: 100%;
        }

        #yesBtn { background: #e94560; color: white; }
        #noBtn { background: #444; color: #888; position: absolute; transition: 0.1s; }
        .call-btn { background: #2ecc71; color: white; animation: shake 0.5s infinite; }

        @keyframes shake {
            0% { transform: rotate(0deg); }
            25% { transform: rotate(5deg); }
            75% { transform: rotate(-5deg); }
            100% { transform: rotate(0deg); }
        }

        .incoming-pfp { width: 100px; height: 100px; border-radius: 50%; background: #555; display: inline-block; margin-bottom: 20px; font-size: 50px; line-height: 100px; }
    </style>
</head>
<body>

    <audio id="bgMusic" loop><source src="funny_song.mp3" type="audio/mpeg"></audio>

    <div id="setup">
        <h2 style="color: #ff00ff;">GF SHORTAGE! ⚠️</h2>
        <p>Detected: No girlfriend found for Divyanshu. Initiating Friend-to-GF conversion...</p>
        <div class="meter"><div class="fill" id="meter"></div></div>
        <div style="height: 100px; position: relative;">
            <button id="yesBtn" onclick="finishPrank()">ACCEPT UPGRADE 💅</button>
            <button id="noBtn" onmouseover="dodge()">STAY SINGLE</button>
        </div>
    </div>

    <div id="finale">
        <img src="divyanshu.jpg" class="pfp" alt="Divyanshu">
        <h2 style="color: #00ff00;">CONVERSION SUCCESS!</h2>
        <p>Divyanshu, you are now officially under my protection. Maintenance fees apply.</p>
        <button class="call-btn" onclick="triggerCall()">CALL YOUR BOYFRIEND</button>
    </div>

    <div id="call-screen">
        <div class="incoming-pfp">🧔🏻‍♂️</div>
        <h2>Incoming Call...</h2>
        <h1 style="color: #2ecc71;">MY BELOVED BF ❤️</h1>
        <p>00:03</p>
        <div style="display: flex; justify-content: space-around; margin-top: 30px;">
            <div style="background: #e74c3c; width: 60px; height: 60px; border-radius: 50%; line-height: 60px; font-size: 30px;">📵</div>
            <div style="background: #2ecc71; width: 60px; height: 60px; border-radius: 50%; line-height: 60px; font-size: 30px;">📞</div>
        </div>
        <button onclick="location.reload()" style="background:none; border: 1px solid #555; color: #555; margin-top: 40px;">End Prank</button>
    </div>

    <script>
        function dodge() {
            const btn = document.getElementById('noBtn');
            btn.style.left = Math.random() * 200 + 'px';
            btn.style.top = Math.random() * 300 + 'px';
            btn.style.position = 'fixed';
            let meter = document.getElementById('meter');
            let currentWidth = parseInt(meter.style.width) || 0;
            if(currentWidth < 100) meter.style.width = (currentWidth + 10) + '%';
        }

        function finishPrank() {
            document.getElementById('bgMusic').play();
            document.getElementById('setup').style.display = 'none';
            document.getElementById('finale').style.display = 'block';
        }

        function triggerCall() {
            document.getElementById('finale').style.display = 'none';
            document.getElementById('call-screen').style.display = 'block';
            if (navigator.vibrate) navigator.vibrate([500, 200, 500, 200, 500]);
        }
    </script>
</body>
</html>
