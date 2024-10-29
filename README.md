<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ayaan Waqar</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
            margin: 0;
            padding: 0;
            color: #333;
        }
        .header {
            background-color: #007bff;
            color: white;
            padding: 1em 0;
            text-align: center;
        }
        .container {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            padding: 2em;
        }
        .project-card {
            background-color: white;
            border: 1px solid #ddd;
            border-radius: 8px;
            width: 300px;
            margin: 1em;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            text-align: center;
        }
        .project-card img {
            width: 100px;
            height: 100px;
            margin: 1em auto;
            display: block;
            transition: transform 0.3s ease;
        }
        .project-card img:hover {
            transform: scale(1.1); /* Slight zoom on hover */
        }
        .project-card h3 {
            margin: 0.5em 0;
        }
        .project-card p {
            padding: 0 1em 1em;
        }
    </style>
</head>
<body>
    <div class="header">
        <h1>Ayaan Waqar's Projects</h1>
    </div>
    <div class="container">
        <!-- Project 1 -->
        <div class="project-card">
            <a href="https://github.com/username/epilet-repo" target="_blank">
                <img src="Project1.jpg" alt="Project 1">
            </a>
            <h3>The Epilet</h3>
            <p>A band for epilepsy patients that allows tonic-clonic seizure detection and alerts.</p>
        </div>

        <!-- Project 2 -->
        <div class="project-card">
            <a href="https://github.com/AyaanWaqar/Obstacle-Avoiding-RCcars" target="_blank">
                <img src="project2.jpg" alt="Project 2">
            </a>
            <h3>Autonomous Car</h3>
            <p>A brief description of Project 2. Explain the purpose and technology used.</p>
        </div>

        <!-- Project 3 -->
        <div class="project-card">
            <a href="https://github.com/username/project3-repo" target="_blank">
                <img src="project3.jpg" alt="Project 3">
            </a>
            <h3>Project Title 3</h3>
            <p>A brief description of Project 3. Explain the purpose and technology used.</p>
        </div>

        <!-- Add more projects as needed -->
    </div>
</body>
</html>

