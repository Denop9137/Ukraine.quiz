<!DOCTYPE html>
<html lang="uk">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Тест на тему "Мама"</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            line-height: 1.6;
            margin: 0;
            padding: 0;
            background-color: #f4f4f4;
        }
        .container {
            max-width: 800px;
            margin: 20px auto;
            background: #fff;
            padding: 20px;
            border-radius: 5px;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
        }
        h1 {
            text-align: center;
            color: #333;
        }
        .question {
            margin-bottom: 20px;
        }
        .question h2 {
            font-size: 18px;
            margin-bottom: 10px;
        }
        .answers {
            list-style: none;
            padding: 0;
        }
        .answers li {
            margin-bottom: 10px;
        }
        button {
            display: block;
            margin: 20px auto;
            padding: 10px 20px;
            font-size: 16px;
            background-color: #007BFF;
            color: #fff;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
        button:hover {
            background-color: #0056b3;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Тест на тему "Мама"</h1>
        
        <div class="question">
            <h2>1. Який день року відзначається як День матері в Україні?</h2>
            <ul class="answers">
                <li><input type="radio" name="q1" id="q1a" value="Друге неділю травня"> <label for="q1a">Друге неділю травня</label></li>
                <li><input type="radio" name="q1" id="q1b" value="8 березня"> <label for="q1b">8 березня</label></li>
                <li><input type="radio" name="q1" id="q1c" value="1 червня"> <label for="q1c">1 червня</label></li>
                <li><input type="radio" name="q1" id="q1d" value="25 грудня"> <label for="q1d">25 грудня</label></li>
            </ul>
        </div>

        <div class="question">
            <h2>2. Як називається найбільш відома картина Рафаеля, присвячена образу матері?</h2>
            <ul class="answers">
                <li><input type="radio" name="q2" id="q2a" value="Сікстинська мадонна"> <label for="q2a">Сікстинська мадонна</label></li>
                <li><input type="radio" name="q2" id="q2b" value="Мона Ліза"> <label for="q2b">Мона Ліза</label></li>
                <li><input type="radio" name="q2" id="q2c" value="Дама з горностаєм"> <label for="q2c">Дама з горностаєм</label></li>
                <li><input type="radio" name="q2" id="q2d" value="Таємна вечеря"> <label for="q2d">Таємна вечеря</label></li>
            </ul>
        </div>

        <div class="question">
            <h2>3. Як називається пісня Назарія Яремчука, присвячена матері?</h2>
            <ul class="answers">
                <li><input type="radio" name="q3" id="q3a" value="Червона рута"> <label for="q3a">Червона рута</label></li>
                <li><input type="radio" name="q3" id="q3b" value="Рідна мати моя"> <label for="q3b">Рідна мати моя</label></li>
                <li><input type="radio" name="q3" id="q3c" value="Гуцулка Ксеня"> <label for="q3c">Гуцулка Ксеня</label></li>
                <li><input type="radio" name="q3" id="q3d" value="Водограй"> <label for="q3d">Водограй</label></li>
            </ul>
        </div>

        <button onclick="checkAnswers()">Перевірити відповіді</button>
        
        <p id="result" style="text-align: center; font-size: 18px; color: green; font-weight: bold;"></p>
    </div>

    <script>
        function checkAnswers() {
            let score = 0;
            if (document.querySelector('input[name="q1"]:checked')?.value === "Друге неділю травня") score++;
            if (document.querySelector('input[name="q2"]:checked')?.value === "Сікстинська мадонна") score++;
            if (document.querySelector('input[name="q3"]:checked')?.value === "Рідна мати моя") score++;
            
            document.getElementById('result').textContent = `Ваш результат: ${score}/3`;
        }
    </script>
</body>
</html>
