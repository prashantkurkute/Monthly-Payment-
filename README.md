<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Monthly Payment Form</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: #e0f7fa;
      margin: 0;
      padding: 20px;
      display: flex;
      justify-content: center;
      align-items: center;
      min-height: 100vh;
    }

    .form-box {
      background: #ffffff;
      padding: 25px;
      border-radius: 10px;
      box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
      width: 100%;
      max-width: 400px;
    }

    h2 {
      text-align: center;
      color: #00796b;
      margin-bottom: 20px;
    }

    label {
      margin-top: 12px;
      display: block;
      color: #333;
      font-weight: bold;
    }

    input, select {
      width: 100%;
      padding: 10px;
      margin-top: 5px;
      border: 1px solid #ccc;
      border-radius: 6px;
      font-size: 16px;
    }

    button {
      width: 100%;
      margin-top: 20px;
      padding: 12px;
      background-color: #009688;
      color: white;
      border: none;
      border-radius: 6px;
      font-size: 16px;
      cursor: pointer;
    }

    button:hover {
      background-color: #00796b;
    }
  </style>
</head>
<body>
  <div class="form-box">
    <h2>Monthly Payment Form</h2>
    <form id="paymentForm">
      <label for="name">Name</label>
      <input type="text" id="name" required />

      <label for="toPay">To Pay Name</label>
      <input type="text" id="toPay" required />

      <label for="month">Select Month</label>
      <select id="month" required>
        <option value="">Select Month</option>
        <option>January</option><option>February</option><option>March</option>
        <option>April</option><option>May</option><option>June</option>
        <option>July</option><option>August</option><option>September</option>
        <option>October</option><option>November</option><option>December</option>
      </select>

      <label for="amount">Amount</label>
      <input type="number" id="amount" required />

      <button type="submit">Submit Payment</button>
    </form>
  </div>

  <script>
    document.getElementById('paymentForm').addEventListener('submit', function(e) {
      e.preventDefault();
      alert('Payment submitted for ' + document.getElementById('name').value);
      this.reset();
    });
  </script>
</body>
</html>
