<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Jewellery Billing</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: #f5f5f5;
      padding: 20px;
    }
    .bill {
      max-width: 700px;
      margin: auto;
      background: #fff;
      padding: 20px;
      border-radius: 10px;
      box-shadow: 0 0 10px rgba(0,0,0,0.1);
    }
    h2 {
      text-align: center;
      margin-bottom: 20px;
    }
    .row {
      display: flex;
      gap: 10px;
      margin-bottom: 12px;
      flex-wrap: wrap;
    }
    .row input {
      flex: 1;
      padding: 10px;
      border: 1px solid #ccc;
      border-radius: 5px;
    }
    button {
      padding: 10px 16px;
      border: none;
      background: #c48f1d;
      color: white;
      border-radius: 5px;
      cursor: pointer;
    }
    .result {
      margin-top: 20px;
      background: #f9f9f9;
      padding: 15px;
      border-radius: 8px;
      line-height: 1.8;
    }
  </style>
</head>
<body>
  <div class="bill">
    <h2>Jewellery Billing</h2>

    <div class="row">
      <input type="text" id="customerName" placeholder="Customer Name" />
      <input type="text" id="itemName" placeholder="Item Name" />
    </div>

    <div class="row">
      <input type="number" id="weightKg" placeholder="Weight (kg)" step="0.001" />
      <input type="number" id="pricePerKg" placeholder="Price per Kg" step="0.01" />
    </div>

    <div class="row">
      <input type="number" id="makingCharge" placeholder="Making Charge" step="0.01" value="0" />
      <input type="number" id="taxPercent" placeholder="Tax %" step="0.01" value="0" />
    </div>

    <button onclick="calculateBill()">Calculate Bill</button>

    <div class="result" id="result"></div>
  </div>

  <script>
    function calculateBill() {
      const customerName = document.getElementById("customerName").value || "N/A";
      const itemName = document.getElementById("itemName").value || "Jewellery Item";
      const weightKg = parseFloat(document.getElementById("weightKg").value) || 0;
      const pricePerKg = parseFloat(document.getElementById("pricePerKg").value) || 0;
      const makingCharge = parseFloat(document.getElementById("makingCharge").value) || 0;
      const taxPercent = parseFloat(document.getElementById("taxPercent").value) || 0;

      const baseAmount = weightKg * pricePerKg;
      const subtotal = baseAmount + makingCharge;
      const taxAmount = (subtotal * taxPercent) / 100;
      const total = subtotal + taxAmount;

      document.getElementById("result").innerHTML = `
        <strong>Customer:</strong> ${customerName}<br>
        <strong>Item:</strong> ${itemName}<br>
        <strong>Weight:</strong> ${weightKg.toFixed(3)} kg<br>
        <strong>Rate:</strong> ${pricePerKg.toFixed(2)} per kg<br>
        <strong>Base Amount:</strong> ${baseAmount.toFixed(2)}<br>
        <strong>Making Charge:</strong> ${makingCharge.toFixed(2)}<br>
        <strong>Subtotal:</strong> ${subtotal.toFixed(2)}<br>
        <strong>Tax (${taxPercent}%):</strong> ${taxAmount.toFixed(2)}<br>
        <strong>Total Bill:</strong> ${total.toFixed(2)}
      `;
    }
  </script>
</body>
</html>
