# arysusgaming

<html lang="en">
<head>
    
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ary Sus Gaming</title>
    <style>
        /* General Body and Page Styling */
        body {
            margin: 0;
            font-family: Arial, sans-serif;
            background-color: #1a1a1a; /* Dark background for the body */
            color: white; /* Light text for contrast */
            background-color: #121212;
        }

        /* Homepage & Hall of Fame Container */
        .container {
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            text-align: center;
            height: 100vh;
            color: white;
        }

        /* Background Image Settings */
        .homepage, .halloffame, .games {
            background-size: cover;
            background-position: center;
            width: 100%;
            height: 100vh;
            display: none; /* Hide initially */
            opacity: 0;
            transition: opacity 0.5s ease;
            background-color: rgba(0, 0, 0, 0.7); /* Dark semi-transparent background for better contrast */
        }

        /* Show active page */
        .active {
            display: block;
            opacity: 1;
        }

        /* Heading Styling */
        h1 {
            font-size: 4rem;
            margin: 0;
            padding: 20px;
            text-shadow: 2px 2px 8px rgba(0, 0, 0, 0.6);
            color: #fff; /* Light heading color */
            cursor: pointer; /* Add cursor pointer to indicate it's clickable */
        }

        /* Paragraph Styling */
        p {
            font-size: 1.5rem;
            margin-bottom: 20px;
            text-shadow: 1px 1px 6px rgba(0, 0, 0, 0.5);
            color: #ddd; /* Lighter paragraph color */
        }

        /* Button Styling */
        .button {
            background-color: #444444; /* Dark button background */
            padding: 15px 30px;
            font-size: 1.2rem;
            text-decoration: none;
            color: white; /* Light text color */
            border-radius: 10px;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.3);
            transition: background-color 0.3s ease;
            margin: 10px;
        }

        .button:hover {
            background-color: #666666; /* Darker hover effect */
        }

        /* Hall of Fame List Styling */
        ul {
            list-style-type: none;
            padding: 0;
        }

        ul li {
            font-size: 1.5rem;
            padding: 5px 0;
            text-shadow: 1px 1px 6px rgba(0, 0, 0, 0.5);
        }

        /* Games Page Styling */
        .games-container {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 20px;
            padding: 20px;
        }

        .game {
            background-color: rgba(255, 255, 255, 0.1); /* Semi-transparent dark background for games */
            padding: 10px;
            border-radius: 10px;
            text-align: center;
            width: 200px;
            color: white;
        }

        .game:hover {
            padding: 12px;
            border-radius: 12px;
            width: 225px;
        }
    </style>
</head>
<body>

    <!-- Homepage Content -->
    <div class="homepage active" style="background-image: url('your-background-image.jpg');">
        <div class="container">
            <h1 onclick="changeTabTitle()">Ary Sus Gaming</h1> <!-- Add the onclick event here -->
            <p>Welcome to Ary Sus Gaming, your ultimate gaming destination!</p>
            <a href="#" class="button" onclick="showHallOfFame()">Hall of Fame</a>
            <a href="#" class="button" onclick="showGamesPage()">Games</a>
        </div>
    </div>

    <!-- Hall of Fame Page (hidden initially) -->
    <div id="halloffame" class="halloffame" style="background-image: url('your-background-image.jpg');">
        <div class="container">
            <h1>Hall of Fame</h1>
            <p>Creators of this website:</p>
            <ul>
                <li>Exofiend</li>
                <li>Ary</li>
                <li>Mally</li>
            </ul>
            <p>Working on it...</p>
            <a href="#" class="button" onclick="goBack()">Back to Home</a>
        </div>
    </div>

    <!-- Games Page (hidden initially) -->
    <div id="games" class="games" style="background-image: url('your-background-image.jpg');">
        <div class="container">
            <h1>Games</h1>
            <p>Check out some cool games below!</p>
            <div class="games-container">
                <!-- Game 1 -->
                <div class="game">
                    <h2>MSG</h2>
                    <a href="https://msg1.pages.dev"><img src="https://msg1.pages.dev/IMGS/MSG.png" alt="Mally's Sussy Gaming" title="Game 1" width="150px" height="150px"></a>
                    <p>Mally's Sussy Gaming</p>
                </div>
                <!-- Game 2 -->
                <div class="game">
                    <h2>GAME ZONE</h2>
                    <a href="https://gameszone.pages.dev" title="Game Zone"><img src="https://gameszone.pages.dev/IMGS/Logo.png" alt="Game Zone Logo" width="150px" height="150px"></a>
                    <p>THIS IS GAME ZONE.</p>
                </div>
                <!-- Game 3 -->
                <div class="game">
                    <h2>Game 3</h2>
                    <a href="https://www.example.com" title="Game 3"><img src="https://www.example.com/image.jpg" alt="Game 3" width="150px" height="150px"></a>
                    <p>Game description or details here.</p>
                </div>
            </div>
            <a href="#" class="button" onclick="goBackToHome()">Back to Home</a>
        </div>
    </div>

    <script>
        // Function to change the title of the tab when the heading is clicked
        function changeTabTitle() {
            document.title = "about blank"; // Change the title of the tab
        }

        // Function to show Hall of Fame page
        function showHallOfFame() {
            document.querySelector('.homepage').classList.remove('active');
            document.querySelector('.halloffame').classList.add('active');
        }

        // Function to show Games page
        function showGamesPage() {
            document.querySelector('.homepage').classList.remove('active');
            document.querySelector('.games').classList.add('active');
        }

        // Function to go back to homepage from Hall of Fame
        function goBack() {
            document.querySelector('.halloffame').classList.remove('active');
            document.querySelector('.homepage').classList.add('active');
        }

        // Function to go back to homepage from Games page
        function goBackToHome() {
            document.querySelector('.games').classList.remove('active');
            document.querySelector('.homepage').classList.add('active');
        }
    </script>

</body>
</html>
