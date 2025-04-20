<!DOCTYPE html>
<html>
<head>
  <title>Simple Interest Calculator</title>
</head>
<body>
  <h2>Simple Interest Calculator</h2>
  <label>Principal:</label><input id="principal"><br>
  <label>Rate (%):</label><input id="rate"><br>
  <label>Time (years):</label><input id="time"><br>
  <button onclick="calc()">Calculate</button>
  <p id="result"></p>

  <script>
    function calc() {
      const P = parseFloat(document.getElementById("principal").value);
      const R = parseFloat(document.getElementById("rate").value);
      const T = parseFloat(document.getElementById("time").value);
      const SI = (P * R * T) / 100;
      document.getElementById("result").innerText = "Simple Interest: RM " + SI.toFixed(2);
    }
  </script>
</body>
</html>
