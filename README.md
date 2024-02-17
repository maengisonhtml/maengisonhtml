<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>GCash Simulator</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f0f0f0;
        }
        .container {
            max-width: 600px;
            margin: 50px auto;
            background-color: #fff;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }
        input[type="text"] {
            width: calc(100% - 20px);
            padding: 10px;
            margin: 10px 0;
            border: 1px solid #ccc;
            border-radius: 5px;
        }
        input[type="submit"] {
            width: 100%;
            padding: 10px;
            background-color: #007bff;
            color: #fff;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
        input[type="submit"]:hover {
            background-color: #0056b3;
        }
    </style>
</head>
<body>
    <div class="container">
        <h2>GCash Simulator</h2>
        <form id="gcashForm">
            <input type="text" id="amount" placeholder="Enter Amount">
            <input type="text" id="receiver" placeholder="Enter Receiver">
            <input type="submit" value="Send Money">
        </form>
    </div>
    <script>
        document.getElementById('gcashForm').addEventListener('submit', function(e) {
            e.preventDefault();
            const amount = document.getElementById('amount').value;
            const receiver = document.getElementById('receiver').value;
            if (amount && receiver) {
                alert(`Sent PHP ${amount} to ${receiver} successfully!`);
            } else {
                alert('Please fill in all fields.');
            }
        });
    </script>
</body>
</html>
