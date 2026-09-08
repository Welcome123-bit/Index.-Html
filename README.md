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
</html>
