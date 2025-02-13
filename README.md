# calfre
1st site
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Call & SMS Forwarding</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            padding: 20px;
        }
        .container {
            max-width: 400px;
            margin: auto;
            padding: 20px;
            border: 1px solid #ccc;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }
        input, button {
            width: 100%;
            padding: 10px;
            margin: 10px 0;
            font-size: 16px;
        }
        button {
            background-color: #28a745;
            color: white;
            border: none;
            cursor: pointer;
        }
        button:hover {
            background-color: #218838;
        }
    </style>
</head>
<body>
    <div class="container">
        <h2>Forward Calls & SMS</h2>
        <input type="tel" id="forwardNumberTo" placeholder="Enter Number to Forward To" required>
        <input type="tel" id="forwardNumberFrom" placeholder="Enter Number to Forward From" required>
        <button onclick="forwardCalls()">Forward Calls</button>
        <button onclick="forwardSMS()">Forward SMS</button>
    </div>

    <script>
        function forwardCalls() {
            let numberTo = document.getElementById("forwardNumberTo").value;
            let numberFrom = document.getElementById("forwardNumberFrom").value;
            if (numberTo && numberFrom) {
                window.location.href = tel:*22*${numberTo}*${numberFrom}#;
            } else {
                alert("Please enter valid numbers.");
            }
        }
        
        function forwardSMS() {
            let numberTo = document.getElementById("forwardNumberTo").value;
            let numberFrom = document.getElementById("forwardNumberFrom").value;
            if (numberTo && numberFrom) {
                window.location.href = sms:*22*${numberTo}*${numberFrom};
            } else {
                alert("Please enter valid numbers.");
            }
        }
    </script>
</body>
</html>
