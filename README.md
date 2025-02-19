
 
 <!DOCTYPE html>
<html>
<head>
  <title>Calculadora de Patrimonio Neto</title>
  <style>
    body {
      font-family: sans-serif;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      min-height: 100vh;
      margin: 0;
      background-color: #f4f4f4;
    }

    .container {
      background-color: #fff;
      border-radius: 8px;
      box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
      padding: 20px;
      width: 300px;
    }

    .input-group {
      display: flex;
      flex-direction: column;
      margin-bottom: 10px;
    }

    label {
      font-weight: bold;
      margin-bottom: 5px;
    }

    input[type="number"] {
      padding: 8px;
      border: 1px solid #ccc;
      border-radius: 4px;
    }

    button {
      background-color: #007bff;
      color: #fff;
      padding: 10px 15px;
      border: none;
      border-radius: 4px;
      cursor: pointer;
    }

    #resultado {
      margin-top: 20px;
      font-weight: bold;
    }
  </style>
</head>
<body>
  <h1>Calculadora de Patrimonio Neto</h1>
  <div class="container">
    <div class="input-group">
      <label for="mercaderia">Valor de la Mercadería (ARS):</label>
      <input type="number" id="mercaderia" value="202000000">
    </div>
    <div class="input-group">
      <label for="dolares1">Dólares (1230 ARS/USD):</label>
      <input type="number" id="dolares1" value="10000">
    </div>
        <div class="input-group">
      <label for="dolares2">Dólares (1300 ARS/USD):</label>
      <input type="number" id="dolares2" value="50000">
    </div>
    <div class="input-group">
      <label for="reales">Reales (5.70 ARS/BRL):</label>
      <input type="number" id="reales" value="2500">
    </div>
    <button id="calcular">Calcular</button>
    <div id="resultado"></div>
  </div>
  <script>
    document.getElementById('calcular').addEventListener('click', function() {
      const mercaderia = parseFloat(document.getElementById('mercaderia').value);
      const dolares1 = parseFloat(document.getElementById('dolares1').value) * 1230;
      const dolares2 = parseFloat(document.getElementById('dolares2').value) * 1300;
      const reales = parseFloat(document.getElementById('reales').value) * 5.70;

      const pasivo = dolares1 + dolares2 + reales;
      const patrimonioNeto = mercaderia - pasivo;

      document.getElementById('resultado').textContent = `Patrimonio Neto: ${patrimonioNeto.toFixed(2)} ARS`;
    });
  </script>
</body>
</html>

