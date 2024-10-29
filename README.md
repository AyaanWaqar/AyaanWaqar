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

        <!-- Project 4 -->
        <div class="project-card">
            <a href="https://github.com/AyaanWaqar/FingerPrintDoorLock" target="_blank">
                <img src="project4.jpg" alt="Project 4">
                <div class="project-card-content">
                    <h3>FingerPrint DoorLock</h3>
                    <p>A lock developed using a fingerprint sensor, servo motor and LCD.</p>
                </div>
            </a>
        </div>

        <!-- Project 5 -->
        <div class="project-card">
            <a href="https://github.com/AyaanWaqar/BluetoothRC" target="_blank">
                <img src="project5.jpeg" alt="Project 5">
                <div class="project-card-content">
                    <h3>Bluetooth Controlled RC Car</h3>
                    <p>An RC car controlled via a bluetooth module.</p>
                </div>
            </a>
        </div>

        <!-- Project 6 -->
        <div class="project-card">
            <a href="https://github.com/AyaanWaqar/LCDWork" target="_blank">
                <img src="project6.jpg" alt="Project 6">
                <div class="project-card-content">
                    <h3>LCD Projects</h3>
                    <p>The use of LCDs in various operations.</p>
                </div>
            </a>
        </div>

        <!-- Project 7 -->
        <div class="project-card">
            <a href="https://github.com/AyaanWaqar/RelayModules" target="_blank">
                <img src="Project7.jpg" alt="Project 7">
                <div class="project-card-content">
                    <h3>Relay Module</h3>
                    <p>The use of relay switches to allow high voltage components to be used with arduino</p>
                </div>
            </a>
        </div>

        <!-- Project 8 -->
        <div class="project-card">
            <a href="https://github.com/AyaanWaqar/TempSensor" target="_blank">
                <img src="project8.jpeg" alt="Project 8">
                <div class="project-card-content">
                    <h3>MLX Temperature Sensor</h3>
                    <p>The use of temperature sensors to input farenhiet and celcius readings</p>
                </div>
            </a>
        </div>

        <!-- Project 9 -->
        <div class="project-card">
            <a href="https://github.com/AyaanWaqar/HardCodeRc" target="_blank">
                <img src="project9.jpeg" alt="Project 9">
                <div class="project-card-content">
                    <h3>Hard Coded RC car</h3>
                    <p>Hard Coding a car to complete specific timed trials.</p>
                </div>
            </a>
        </div>

        <!-- Project 10 -->
        <div class="project-card">
            <a href="https://github.com/AyaanWaqar/SoundSensor" target="_blank">
                <img src="project10.jpeg" alt="Project 10">
                <div class="project-card-content">
                    <h3>Sound Detection</h3>
                    <p>Detecting a clap to switch lights on and off.</p>
                </div>
            </a>
        </div>

        <!-- Project 11 -->
        <div class="project-card">
            <a href="https://github.com/AyaanWaqar/LineFollowingRc" target="_blank">
                <img src="project11.jpeg" alt="Project 11">
                <div class="project-card-content">
                    <h3>Line Following RC Car</h3>
                    <p>Created a line following RC car using numerous IR sensors.</p>
                </div>
            </a>
        </div>

        <!-- Project 12 -->
        <div class="project-card">
            <a href="https://github.com/AyaanWaqar/BluetoothComponents" target="_blank">
                <img src="project12.jpeg" alt="Project 12">
                <div class="project-card-content">
                    <h3>Bluetooth with Components</h3>
                    <p>The use of Bluetooth to manipulate various components.</p>
                </div>
            </a>
        </div>

        <!-- Project 13 -->
        <div class="project-card">
            <a href="https://github.com/AyaanWaqar/ServoMotor" target="_blank">
                <img src="project13.jpeg" alt="Project 13">
                <div class="project-card-content">
                    <h3>Servo Motor Use</h3>
                    <p>The use of a servo motor in various projects.</p>
                </div>
            </a>
        </div>

        <!-- Project 14 -->
        <div class="project-card">
            <a href="https://github.com/AyaanWaqar/MotionSensor" target="_blank">
                <img src="project14.jpeg" alt="Project 14">
                <
