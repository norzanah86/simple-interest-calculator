<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Simple Interest Calculator</title>
  <style>
    body {
      font-family: 'Segoe UI', sans-serif;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      height: 100vh;
      margin: 0;
      background: #f9f9f9;
    }

    .calculator {
      background: white;
      padding: 20px 30px;
      border-radius: 15px;
      box-shadow: 0 5px 20px rgba(0, 0, 0, 0.1);
      max-width: 400px;
      width: 100%;
    }

    h2 {
      margin-top: 0;
      color: #333;
      text-align: center;
    }

    label {
      display: block;
      margin-top: 10px;
      font-weight: bold;
      color: #555;
    }

    input {
      width: 100%;
      padding: 10px;
      margin-top: 5px;
      border: 1px solid #ccc;
      border-radius: 8px;
      box-sizing: border-box;
    }

    button {
      margin-top: 20px;
      width: 100%;
      padding: 10px;
      background-color: #0077cc;
      color: white;
      font-weight: bold;
      border: none;
      border-radius: 8px;
      cursor: pointer;
      transition: background-color 0.3s;
    }

    button:hover {
      background-color: #005fa3;
    }

    #result {
      margin-top: 15px;
      font-size: 1.1em;
      text-align: center;
      color: #007700;
    }
  </style>
</head>
<body>
  <div class="calculator">
    <h2>Simple Interest Calculator</h2>

    <label for="principal">Principal (RM):</label>
    <input type="number" id="principal" placeholder="e.g. 1000" />

    <label for="rate">Rate (% per year):</label>
    <input type="number" id="rate" placeholder="e.g. 5" />

    <label for="time">Time (years):</label>
    <input type="number" id="time" placeholder="e.g. 2" />

    <button onclick="calculateSI()">Calculate</button>
    <p id="result"></p>
  </div>

  <script>
    function calculateSI() {
      const p = parseFloat(document.getElementById("principal").value);
      const r = parseFloat(document.getElementById("rate").value);
      const t = parseFloat(document.getElementById("time").value);

      if (isNaN(p) || isNaN(r) || isNaN(t)) {
        document.getElementById("result").innerText = "Please fill in all fields.";
        return;
      }

      const si = (p * r * t) / 100;
      document.getElementById("result").innerText = "Simple Interest: RM " + si.toFixed(2);
    }
  </script>
</body>
</html>
