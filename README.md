# Stalk-Market-Prediction

Brief About Stock Market 
Data analysis makes use of historical trading volumes, stock prices, and economic indicators.
✅ AI & Machine Learning: Methods such as Random Forests, LSTMs, and Linear Regression forecast patterns.
Sentiment analysis looks at financial reports, social media, and news to gauge the mood of the market.
✅ Risk Assessment: Determines investment opportunities, risks, and market volatility.

Use and Advantages:  Enhances investment plans by spotting lucrative patterns; 📊 Lowers risks with in-the-moment forecasts and notifications. 📈 Automated Trading: Without human involvement, trades can be executed by AI-driven models.
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Stock Market Prediction</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Poppins', sans-serif;
        }

        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background: url('https://source.unsplash.com/1600x900/?stocks,market,finance') no-repeat center center/cover;
        }

        .container {
            width: 90%;
            max-width: 500px;
            text-align: center;
            background: rgba(0, 0, 0, 0.8);
            padding: 30px;
            border-radius: 15px;
            box-shadow: 0px 4px 15px rgba(0, 0, 0, 0.3);
            color: blue;
        }

        /* Welcome Screen */
        .welcome-screen {
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            animation: fadeIn 1s ease-in-out;
        }

        .welcome-screen img {
            width: 150px;
            margin: 20px 0;
            border-radius: 10px;
            box-shadow: 0px 4px 10px rgba(255, 255, 255, 0.3);
            animation: pulse 1.5s infinite alternate;
        }

        .welcome-screen h1 {
            font-size: 24px;
            margin-bottom: 10px;
        }

        .welcome-screen p {
            font-size: 16px;
            margin-bottom: 20px;
        }

        .welcome-screen button {
            padding: 12px 25px;
            font-size: 18px;
            border: none;
            border-radius: 8px;
            background: linear-gradient(135deg, #ff9800, #ff5722);
            color: white;
            cursor: pointer;
            transition: all 0.3s;
        }

        .welcome-screen button:hover {
            background: linear-gradient(135deg, #ff5722, #e64a19);
            transform: scale(1.05);
        }

        /* Main App Screen */
        .main-screen {
            display: none;
            flex-direction: column;
            align-items: center;
        }

        .main-screen img {
            width: 120px;
            margin-bottom: 15px;
            border-radius: 10px;
            box-shadow: 0px 4px 10px rgba(255, 255, 255, 0.3);
        }

        input {
            width: 80%;
            padding: 12px;
            border-radius: 5px;
            border: none;
            margin-top: 15px;
            text-align: center;
            font-size: 16px;
        }

        .main-screen button {
            padding: 12px 25px;
            font-size: 18px;
            border: none;
            border-radius: 8px;
            background: #00c853;
            color: white;
            cursor: pointer;
            transition: 0.3s;
            margin-top: 15px;
        }

        .main-screen button:hover {
            background: #009624;
        }

        #prediction {
            margin-top: 15px;
            font-size: 18px;
            font-weight: bold;
            background: rgba(255, 255, 255, 0.2);
            padding: 10px;
            border-radius: 10px;
        }

        /* Animations */
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(-10px); }
            to { opacity: 1; transform: translateY(0); }
        }

        @keyframes pulse {
            0% { transform: scale(1); }
            100% { transform: scale(1.05); }
        }
    </style>
</head>
<body>

    <div class="container">
        <!-- Welcome Page -->
        <div class="welcome-screen" id="welcomeScreen">
            <h1>🚀 Welcome to Stock Market Prediction 📈</h1>
            <img src="https://cdn-icons-png.flaticon.com/512/3135/3135715.png" alt="User Icon">
            <p>Discover market trends and predictions in an easy and interactive way!</p>
            <button onclick="showMainScreen()">Go</button>
        </div>

        <!-- Main App Page -->
        <div class="main-screen" id="mainScreen">
            <h1>📊 Stock Market Prediction</h1>
            <img src="https://source.unsplash.com/200x200/?stocks,graph" alt="Stock Image">
            <input type="text" id="stockSymbol" placeholder="Enter Stock Symbol">
            <button onclick="predictStock()">Predict</button>
            <p id="prediction"></p>
        </div>
    </div>

    <script>
        function showMainScreen() {
            document.getElementById("welcomeScreen").style.display = "none";
            document.getElementById("mainScreen").style.display = "flex";
        }

        function predictStock() {
            let stockSymbol = document.getElementById("stockSymbol").value;
            let predictionText = document.getElementById("prediction");

            if (stockSymbol.trim() === "") {
                predictionText.innerHTML = "⚠ Please enter a stock symbol!";
                predictionText.style.color = "red";
                return;
            }

            let randomPrediction = Math.random() > 0.5 ? "Stock is expected to go up 📈" : "Stock might go down 📉";
            predictionText.innerHTML = Prediction for ${stockSymbol.toUpperCase()}: ${randomPrediction};
            predictionText.style.color = "white";
        }
    </script>

</body>
</html>
