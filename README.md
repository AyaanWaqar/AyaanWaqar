<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ayaan Waqar - Projects</title>
    <style>
        /* Basic Reset */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: Arial, sans-serif;
            background-color: #292828;
            color: #fff;
            display: flex;
            flex-direction: column;
            align-items: center;
            padding: 20px;
        }

        /* Header and Profile Section */
        .header {
            text-align: center;
            margin-bottom: 2em;
        }

        .header h1 {
            font-size: 2.5em;
            color: #fff;
            margin-bottom: 0.5em;
        }

        .header p {
            font-size: 1.2em;
            color: #aaa;
            max-width: 600px;
            margin: 0 auto;
        }

        /* Projects Container */
        .container {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 20px;
            width: 100%;
            max-width: 1200px;
        }

        /* Project Card Styling */
        .project-card {
            background-color: #1a1a1a;
            border-radius: 8px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.3);
            overflow: hidden;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        .project-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 6px 15px rgba(0, 0, 0, 0.5);
        }

        .project-card img {
            width: 100%;
            height: auto;
            display: block;
        }

        .project-card-content {
            padding: 15px;
            text-align: center;
        }

        .project-card h3 {
            font-size: 1.4em;
            color: #fff;
            margin-bottom: 0.5em;
        }

        .project-card p {
            font-size: 1em;
            color: #ccc;
        }

        /* Responsive Styling */
        @media (max-width: 600px) {
            .header h1 {
                font-size: 2em;
            }

            .header p {
                font-size: 1em;
            }
        }
    </style>
</head>
<body>
    <div class="header">
        <h1>Ayaan Waqar</h1>
        <p>Welcome to my project portfolio. Here you'll find some of the projects I've been working on, including RC cars, sensors, IoT devices, and more, each built to push boundaries and explore possibilities in technology.</p>
    </div>

    <div class="container">
        <!-- Project 1 -->
        <div class="project-card">
            <a href="https://github.com/username/epilet-repo" target="_blank">
                <img src="Project1.jpg" alt="Project 1">
                <div class="project-card-content">
                    <h3>The Epilet</h3>
                    <p>A band for epilepsy patients that allows tonic-clonic seizure detection and alerts.</p>
                </div>
            </a>
        </div>

        <!-- Project 2 -->
        <div class="project-card">
            <a href="https://github.com/AyaanWaqar/Obstacle-Avoiding-RCcars" target="_blank">
                <img src="project2.jpg" alt="Project 2">
                <div class="project-card-content">
                    <h3>Autonomous Car</h3>
                    <p>RC car developed using UltraSonic Sensor to maneuver around obstacles.</p>
                </div>
            </a>
        </div>

        <!-- Project 3 -->
        <div class="project-card">
            <a href="https://github.com/AyaanWaqar/DiabeticFoot" target="_blank">
                <img src="project3.jpg" alt="Project 3">
                <div class="project-card-content">
                    <h3>Diabetic Foot Analyzer</h3>
                    <p>A device developed for diabetic patients.</p>
                </div>
            </a>
        </div>

        <!-- Add more project cards in the same format -->

        <!-- Project 16 (Example for the last project) -->
        <div class="project-card">
            <a href="https://github.com/AyaanWaqar/LEDs" target="_blank">
                <img src="project16.jpg" alt="Project 16">
                <div class="project-card-content">
                    <h3>LEDs</h3>
                    <p>Starting from the basics with LEDs and advancing to more complex projects.</p>
                </div>
            </a>
        </div>
    </div>
</body>
</html>
