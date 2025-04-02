<!DOCTYPE html>
<html lang="ar">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>شراء متابعين إنستجرام</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            background-color: #fafafa;
            color: #262626;
        }
        .container {
            max-width: 400px;
            margin: auto;
            padding: 20px;
            background: white;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }
        .price {
            font-size: 20px;
            color: #ff4500;
        }
        button {
            background: #ff4500;
            color: white;
            border: none;
            padding: 10px;
            cursor: pointer;
            font-size: 18px;
            border-radius: 5px;
        }
        button:hover {
            background: #e63900;
        }
        #barcode {
            display: none;
            margin-top: 20px;
        }
    </style>
</head>
<body>
    <div class="container">
        <h2>شراء متابعين إنستجرام</h2>
        <label for="followers">اختر عدد المتابعين:</label>
        <input type="number" id="followers" min="100" max="1000" step="100" value="100">
        <p class="price">السعر: <span id="price">0.50</span>$</p>
        <button onclick="showBarcode()">شراء الآن</button>
        <img id="barcode" src="qr_code_image.png" alt="باركود الدفع">
    </div>
    
    <script>
        function updatePrice() {
            let followers = document.getElementById("followers").value;
            let price = (followers / 100) * 0.50;
            document.getElementById("price").innerText = price.toFixed(2);
        }
        
        function showBarcode() {
            document.getElementById("barcode").style.display = "block";
        }
        
        document.getElementById("followers").addEventListener("input", updatePrice);
    </script>
</body>
</html>
