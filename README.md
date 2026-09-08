<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>SpaceGuard</title>

    <style>
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        body {
            font-family: Arial, sans-serif;
            background: #050816;
            color: white;
            min-height: 100vh;
        }

        header {
            text-align: center;
            padding: 40px 20px 25px;
        }

        header h1 {
            font-size: 42px;
            margin-bottom: 10px;
        }

        header p {
            color: #9ca8c7;
            font-size: 17px;
        }

        .container {
            width: 90%;
            max-width: 1100px;
            margin: auto;
        }

        .dashboard {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 20px;
            margin-top: 25px;
        }

        .card {
            background: #0d1328;
            border: 1px solid #202b4d;
            border-radius: 18px;
            padding: 25px;
            min-height: 150px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.25);
        }

        .card h2 {
            font-size: 20px;
            margin-bottom: 20px;
        }

        .value {
            font-size: 30px;
            font-weight: bold;
        }

        .description {
            margin-top: 10px;
            color: #8e9bbd;
            font-size: 14px;
        }

        .button-container {
            text-align: center;
            margin: 35px 0;
        }

        button {
            background: #2563eb;
            color: white;
            border: none;
            padding: 15px 30px;
            border-radius: 12px;
            font-size: 16px;
            cursor: pointer;
        }

        button:hover {
            background: #1d4ed8;
        }

        footer {
            text-align: center;
            padding: 30px;
            color: #687493;
            font-size: 13px;
        }

        @media (max-width: 700px) {
            header h1 {
                font-size: 32px;
            }

            .dashboard {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>

<body>

    <header>
        <h1>🚀 SpaceGuard</h1>
        <p>Space Weather Intelligence Dashboard</p>
    </header>

    <main class="container">

        <section class="dashboard">

            <div class="card">
                <h2>☀️ Solar Activity</h2>
                <div class="value" id="solarActivity">
                    Loading...
                </div>
                <div class="description">
                    Latest solar flux measurement
                </div>
            </div>

            <div class="card">
                <h2>🌍 Geomagnetic Activity</h2>
                <div class="value" id="geomagnetic">
                    Loading...
                </div>
                <div class="description">
                    Latest planetary K-index
                </div>
            </div>

            <div class="card">
                <h2>🛰️ Space Environment</h2>
                <div class="value" id="spaceEnvironment">
                    Loading...
                </div>
                <div class="description">
                    Current space-weather environment
                </div>
            </div>

            <div class="card">
                <h2>⚠️ Current Risk</h2>
                <div class="value" id="risk">
                    Analyzing...
                </div>
                <div class="description">
                    Educational SpaceGuard risk assessment
                </div>
            </div>

        </section>

        <div class="button-container">
            <button onclick="checkStatus()">
                Check SpaceGuard
            </button>
        </div>

    </main>

    <footer>
        SpaceGuard uses public space-weather data.
        <br>
        Not an official NASA forecast.
    </footer>

    <script src="script.js"></script>

</body>
</html>
