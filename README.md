# BMI-Calculator
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>BMI Calculator</title>
</head>
<body>
  <h2>BMI Calculator</h2>
  <label>Height (meters): <input type="number" id="height"></label><br><br>
  <label>Weight (kg): <input type="number" id="weight"></label><br><br>
  <button onclick="calculateBMI()">Calculate</button>
  <p id="result"></p>

  <script>
    function calculateBMI() {
      let h = document.getElementById("height").value;
      let w = document.getElementById("weight").value;
      if(h && w){
        let bmi = w / (h * h);
        document.getElementById("result").innerText = "Your BMI is: " + bmi.toFixed(2);
      } else {
        document.getElementById("result").innerText = "Please enter values!";
      }
    }
  </script>
</body>
</html>
