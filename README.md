<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    
    <style>
        body, html {
            margin: 0;
            padding: 0;
            height: 100%;
            width: 100%;
            font-family: Arial, sans-serif;
        }
        body {
            background: url('https://images7.alphacoders.com/658/658741.jpg') no-repeat center center fixed;
            background-size: cover;
            display: flex;
            justify-content: center;
            align-items: center;
            color: white;
            text-align: center;
            padding-top: 260px;
        }
        .navbar {
            background-color: rgba(0, 0, 0, 0.7);
            padding: 10px;
            text-align: center;
            position: fixed;
            width: 100%;
            top: 0;
            left: 0;
            z-index: 1000;
        }
        .navbar a {
            color: white;
            text-decoration: none;
            margin: 0 15px;
            font-size: 18px;
            cursor: pointer;
        }
        .container {
            background-color: rgba(255, 255, 255, 0.8);
            margin: 50px auto;
            padding: 20px;
            max-width: 800px;
            text-align: center;
            border-radius: 10px;
        }
        img {
            max-width: 100%;
            height: auto;
            border-radius: 10px;
            margin-top: 20px;
            max-height: 400px;
        }
        h1 {
            margin-top: 0;
            color: #ff69b4;
        }
        .script-box {
            background-color: rgba(255, 182, 193, 0.8);
            padding: 20px;
            border-radius: 10px;
            margin-top: 20px;
            text-align: center;
        }
        .script-box h2 {
            color: #ff69b4;
        }
        .script-box pre {
            background-color: rgba(255, 255, 255, 0.8);
            border-radius: 10px;
            padding: 10px;
            color: #000;
            font-family: monospace;
            display: inline-block;
            overflow-wrap: break-word;
            max-width: 100%;
        }
        .script-buttons {
            margin-top: 10px;
        }
        .script-buttons button {
            background-color: #ff69b4;
            border: none;
            color: white;
            padding: 10px 20px;
            margin: 5px;
            border-radius: 5px;
            cursor: pointer;
        }
        .search-container {
            margin-top: 20px;
            text-align: center;
        }
        .search-container input[type="text"] {
            padding: 10px;
            border: 2px solid #ff69b4;
            border-radius: 20px;
            width: 60%;
            max-width: 500px;
            outline: none;
            color: #333;
        }
        .search-container input[type="text"]::placeholder {
            color: #ff69b4;
        }
        .script-section {
            display: none;
        }
    </style>
</head>
<body>
    <div class="navbar">
        <a href="#" onclick="showSection('all')">Everything</a>
        <a href="#" onclick="showSection('universal')">Universal</a>
        <a href="https://discord.gg/dXBeFrZC" target="_blank">Discord</a>
        <a href="https://youtu.be/6CBp4qylX6I?si=6_RVSADRDymxqsRq" target="_blank">YouTube</a>
        <a href="#" onclick="sortScripts('new')">New</a>
        <a href="#" onclick="sortScripts('old')">Old</a>
    </div>
    <div class="container">
        <h1>Welcome to nogamenolife's scripts</h1>
        <p>nogamenolife is the best anime</p>
        <div class="search-container">
            <input type="text" placeholder="search scripts... [ID Game] or [Name Game]">
        </div>
        <img src="https://c4.wallpaperflare.com/wallpaper/807/606/524/no-game-no-life-shiro-no-game-no-life-anime-wallpaper-preview.jpg" alt="Sample Image">
        <div id="all" class="script-section">
            <div class="script-box">
                <h2>UPDATE Speed + InfJump</h2>
                <pre>loadstring(game:HttpGet("https://raw.githubusercontent.com/nogamenoIife/fly-script/main/fly%20script"))()</pre>
                <div class="script-buttons">
                    <button onclick="copyToClipboard('loadstring(game:HttpGet(&quot;https://raw.githubusercontent.com/nogamenoIife/fly-script/main/fly%20script&quot;))()')">COPY</button>
                    <button>SHARE</button>
                    <button>REPORT</button>
                    <button>Go to Game</button>
                </div>
            </div>
        </div>
        <div id="universal" class="script-section">
            <div class="script-box">
                <h2>Universal Script Example</h2>
                <pre>loadstring(game:HttpGet("https://example.com/universal-script"))()</pre>
                <div class="script-buttons">
                    <button onclick="copyToClipboard('loadstring(game:HttpGet(&quot;https://example.com/universal-script&quot;))()')">COPY</button>
                    <button>SHARE</button>
                    <button>REPORT</button>
                    <button>Go to Game</button>
                </div>
            </div>
        </div>
        <!-- Add more sections and scripts as needed -->
    </div>
    <script>
        function showSection(sectionId) {
            const sections = document.querySelectorAll('.script-section');
            sections.forEach(section => {
                section.style.display = 'none';
            });
            document.getElementById(sectionId).style.display = 'block';
        }

        function copyToClipboard(str) {
            navigator.clipboard.writeText(str).then(function() {
                alert('Copied to clipboard!');
            }, function(err) {
                console.error('Could not copy text: ', err);
            });
        }

        function sortScripts(order) {
            // Implement sorting functionality based on 'new' or 'old'
            alert(`Sorting scripts by ${order}`);
        }

        // Show the "Everything" section by default
        showSection('all');
    </script>
</body>
</html>
