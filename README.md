# Ex.05 Design a Website for Server Side Processing


## AIM:
 To design a website to calculate the power of a lamp filament in an incandescent bulb in the server side. 


## FORMULA:
P = I<sup>2</sup>R
<br> P --> Power (in watts)
<br> I --> Intensity
<br> R --> Resistance

## DESIGN STEPS:

### Step 1:
Clone the repository from GitHub.

### Step 2:
Create Django Admin project.

### Step 3:
Create a New App under the Django Admin project.

### Step 4:
Create python programs for views and urls to perform server side processing.

### Step 5:
Create a HTML file to implement form based input and output.

### Step 6:
Publish the website in the given URL.

## PROGRAM :
NAME : BALASUBRAMANIAM L
ROLL NO:24901213
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Lamp Filament Power Calculator</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            max-width: 600px;
            margin: 40px auto;
            padding: 20px;
            background-color: #f5f5f5;
        }
        .calculator {
            background-color: white;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 2px 4px rgba(0,0,0,0.1);
        }
        .input-group {
            margin-bottom: 15px;
        }
        label {
            display: block;
            margin-bottom: 5px;
            font-weight: bold;
        }
        input {
            width: 100%;
            padding: 8px;
            border: 1px solid #ddd;
            border-radius: 4px;
            margin-bottom: 10px;
        }
        button {
            background-color: #4CAF50;
            color: white;
            padding: 10px 15px;
            border: none;
            border-radius: 4px;
            cursor: pointer;
            width: 100%;
        }
        button:hover {
            background-color: #45a049;
        }
        #result {
            margin-top: 20px;
            padding: 10px;
            border-radius: 4px;
            background-color: #e8f5e9;
            display: none;
        }
        .formula {
            background-color: #f8f9fa;
            padding: 10px;
            border-radius: 4px;
            margin-bottom: 20px;
            text-align: center;
        }
    </style>
</head>
<body>
    <div class="calculator">
        <h1>Lamp Filament Power Calculator</h1>
        
        <div class="formula">
            <p>Formula: P = I² × R</p>
            <p>Where P = Power (watts), I = Current (amperes), R = Resistance (ohms)</p>
        </div>

        <div class="input-group">
            <label for="current">Current (I) in amperes:</label>
            <input type="number" id="current" step="0.01" required>
        </div>

        <div class="input-group">
            <label for="resistance">Resistance (R) in ohms:</label>
            <input type="number" id="resistance" step="0.01" required>
        </div>

        <button onclick="calculatePower()">Calculate Power</button>

        <div id="result"></div>
    </div>

    <script>
        function calculatePower() {
            // Get input values
            const current = parseFloat(document.getElementById('current').value);
            const resistance = parseFloat(document.getElementById('resistance').value);
            
            // Validate inputs
            if (isNaN(current) || isNaN(resistance)) {
                alert('Please enter valid numbers for both current and resistance');
                return;
            }
            
            // Calculate power using P = I²R
            const power = current * current * resistance;
            
            // Display result
            const resultDiv = document.getElementById('result');
            resultDiv.style.display = 'block';
            resultDiv.innerHTML = `
                <h3>Results:</h3>
                <p>Current (I): ${current} A</p>
                <p>Resistance (R): ${resistance} Ω</p>
                <p>Power (P): ${power.toFixed(2)} watts</p>
            `;
        }
    </script>
</body>
</html>

```


## SERVER SIDE PROCESSING:


## HOMEPAGE:
![image](https://github.com/user-attachments/assets/b2696a12-faad-4e23-93c7-653ed7521863)



## RESULT:
The program for performing server side processing is completed successfully.
