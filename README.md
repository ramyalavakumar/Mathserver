# Ex.05 Design a Website for Server Side Processing
## Date:08-10-2025

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

<!DOCTYPE html>
<html>
<head>
    <title>Power Calculation</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 40px;
        }
        input[type="text"], input[type="submit"] {
            padding: 8px;
            margin: 8px 0;
            width: 200px;
        }
        .result {
            margin-top: 20px;
            font-weight: bold;
        }
        .error {
            color: red;
            margin-top: 20px;
        }
    </style>
</head>
<body>

    <h2>Calculate Power (P = I² × R)</h2>

    <form method="POST">
        {% csrf_token %}
        
        <label for="current">Current (I in Amps):</label><br>
        <input type="text" id="current" name="current" placeholder="Enter current"><br>

        <label for="resistance">Resistance (R in Ohms):</label><br>
        <input type="text" id="resistance" name="resistance" placeholder="Enter resistance"><br>

        <input type="submit" value="Calculate Power">
    </form>

    {% if power %}
        <div class="result">
            Power = {{ power }} Watts
        </div>
    {% endif %}

    {% if error %}
        <div class="error">
            Error: {{ error }}
        </div>
    {% endif %}

</body>
</html>


## SERVER SIDE PROCESSING:
<img width="1064" height="581" alt="Screenshot 2025-10-13 181719" src="https://github.com/user-attachments/assets/bd10ae32-8954-4ece-83f8-ce0a5ba6d258" />


## HOMEPAGE:
![Uploading Screenshot 2025-11-19 183517.png…]()


## RESULT:
The program for performing server side processing is completed successfully.
