# Temperature_Converter
#HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Temperature Converter</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div id="container">
        <h1>Temperature Converter</h1>
        <label for="celsius">Enter Temperature in Celsius:</label>
        <input type="number" id="celsius" placeholder="Enter temperature">
        <button onclick="convertTemperature()">Convert</button>

        <div id="result">
            <p><strong>Fahrenheit:</strong> <span id="fahrenheit"></span> °F</p>
            <p><strong>Kelvin:</strong> <span id="kelvin"></span> K</p>
        </div>
    </div>
    <script src="script.js"></script>
</body>
</html>

#CSS

body {
    font-family: Arial, sans-serif;
    text-align: center;
}

#container {
    margin: 50px auto;
    width: 300px;
    border: 1px solid #ccc;
    padding: 20px;
    background-color: #f4f4f4;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

h1 {
    color: #333;
}

#result {
    margin-top: 20px;
}


#JS


function convertTemperature() {
    const celsiusInput = document.getElementById("celsius").value;
    const celsius = parseFloat(celsiusInput);

    if (!isNaN(celsius)) {
        const fahrenheit = (celsius * 9/5) + 32;
        const kelvin = celsius + 273.15;

        document.getElementById("fahrenheit").textContent = fahrenheit.toFixed(2);
        document.getElementById("kelvin").textContent = kelvin.toFixed(2);
    } else {
        alert("Please enter a valid temperature in Celsius.");
    }
}

