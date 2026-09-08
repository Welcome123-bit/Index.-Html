<!DOCTYPE html>
<html>
<head>
    <title>SpaceGuard</title>

    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 30px;
            background: #0b1020;
            color: white;
        }

        h1 {
            font-size: 40px;
        }

        .subtitle {
            color: #aab3c5;
        }

        .dashboard {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 20px;
            margin-top: 30px;
        }

        .card {
            background: #171e33;
            padding: 25px;
            border-radius: 15px;
        }

        .card h2 {
            margin-top: 0;
        }

        .value {
            font-size: 28px;
            font-weight: bold;
        }

        button {
            padding: 12px 20px;
            border: none;
            border-radius: 8px;
            cursor: pointer;
            font-size: 16px;
        }
    </style>
</head>

<body>

    <h1>🚀 SpaceGuard</h1>

    <p class="subtitle">
        Space Weather Intelligence Dashboard
    </p>

    <div class="dashboard">

        <div class="card">
            <h2>☀️ Solar Activity</h2>
            <p class="value" id="solarActivity">Loading...</p>
        </div>

        <div class="card">
            <h2>🌍 Geomagnetic Activity</h2>
            <p class="value" id="geomagnetic">Loading...</p>
        </div>

        <div class="card">
            <h2>🛰️ Space Environment</h2>
            <p class="value" id="spaceEnvironment">Loading...</p>
        </div>

        <div class="card">
            <h2>⚠️ Current Risk</h2>
            <p class="value" id="risk">Calculating...</p>
        </div>

    </div>

    <br>

    <button onclick="checkStatus()">Check SpaceGuard</button>

    <script>

        function checkStatus() {

            document.getElementById("solarActivity").innerText =
                "Monitoring";

            document.getElementById("geomagnetic").innerText =
                "Monitoring";

            document.getElementById("spaceEnvironment").innerText =
                "Monitoring";

            document.getElementById("risk").innerText =
                "Analyzing...";
        }

    </script>

</body>
</html><!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>SpaceGuard</title>

    <style>
        * {
            box-sizing: border-box;
        }

        body {
            margin: 0;
            font-family: Arial, sans-serif;
            background: #080d1c;
            color: white;
        }

        header {
            padding: 30px;
            border-bottom: 1px solid #202943;
        }

        header h1 {
            margin: 0;
            font-size: 38px;
        }

        header p {
            margin-top: 8px;
            color: #9da8c0;
        }

        main {
            max-width: 1200px;
            margin: auto;
            padding: 30px;
        }

        .status {
            display: flex;
            align-items: center;
            gap: 10px;
            margin-bottom: 25px;
            color: #aeb8cc;
        }

        .dot {
            width: 10px;
            height: 10px;
            background: #35d07f;
            border-radius: 50%;
        }

        .dashboard {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 20px;
        }

        .card {
            background: #141b30;
            border: 1px solid #252e48;
            border-radius: 18px;
            padding: 25px;
            min-height: 170px;
        }

        .card h2 {
            margin-top: 0;
            font-size: 20px;
        }

        .value {
            font-size: 30px;
            font-weight: bold;
            margin-top: 25px;
        }

        .description {
            color: #9da8c0;
            line-height: 1.5;
        }

        .risk {
            border: 1px solid #6d5a20;
        }

        .risk .value {
            color: #ffd35a;
        }

        button {
            margin-top: 25px;
            padding: 13px 22px;
            border: none;
            border-radius: 10px;
            background: #ffffff;
            color: #080d1c;
            font-size: 16px;
            font-weight: bold;
            cursor: pointer;
        }

        button:hover {
            opacity: 0.85;
        }

        footer {
            text-align: center;
            padding: 30px;
            color: #68738b;
            font-size: 14px;
        }

        @media (max-width: 700px) {
            .dashboard {
                grid-template-columns: 1fr;
            }

            header h1 {
                font-size: 30px;
            }

            main {
                padding: 20px;
            }
        }
    </style>
</head>

<body>

    <header>
        <h1>🚀 SpaceGuard</h1>
        <p>Space Weather Intelligence Dashboard</p>
    </header>

    <main>

        <div class="status">
            <div class="dot"></div>
            <span>SpaceGuard is online</span>
        </div>

        <div class="dashboard">

            <div class="card">
                <h2>☀️ Solar Activity</h2>

                <p class="description">
                    Monitoring activity coming from the Sun.
                </p>

                <div class="value" id="solarActivity">
                    Waiting for data
                </div>
            </div>

            <div class="card">
                <h2>🌍 Geomagnetic Activity</h2>

                <p class="description">
                    Monitoring disturbances in Earth's magnetic field.
                </p>

                <div class="value" id="geomagnetic">
                    Waiting for data
                </div>
            </div>

            <div class="card">
                <h2>🛰️ Space Environment</h2>

                <p class="description">
                    Monitoring conditions that can affect spacecraft.
                </p>

                <div class="value" id="spaceEnvironment">
                    Waiting for data
                </div>
            </div>

            <div class="card risk">
                <h2>⚠️ Current Risk</h2>

                <p class="description">
                    SpaceGuard's current assessment.
                </p>

                <div class="value" id="risk">
                    Not calculated
                </div>
            </div>

        </div>

        <button onclick="checkStatus()">
            Check SpaceGuard
        </button>

    </main>

    <footer>
        SpaceGuard — NASA Space Apps Project
    </footer>

    <script>

        function checkStatus() {

            document.getElementById("solarActivity").innerText =
                "Monitoring";

            document.getElementById("geomagnetic").innerText =
                "Monitoring";

            document.getElementById("spaceEnvironment").innerText =
                "Monitoring";

            document.getElementById("risk").innerText =
                "Analyzing...";

        }

    </script>

</body>
</html>
