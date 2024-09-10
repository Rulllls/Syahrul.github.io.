# Syahrul.github.io.

<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Kalkulator Fahri Babi</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: #f4f4f4;
        }
        #kalkulator {
            background: white;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }
        input[type="text"] {
            width: 100%;
            padding: 10px;
            margin-bottom: 10px;
            border: 1px solid #ccc;
            border-radius: 5px;
        }
        button {
            width: 23%;
            padding: 10px;
            margin: 5px;
            border: none;
            border-radius: 5px;
            background-color: #007bff;
            color: white;
            cursor: pointer;
        }
        button:hover {
            background-color: #0056b3;
        }
    </style>
</head>
<body>
    <div id="kalkulator">
        <h2>Kalkulator Fahri Anjing</h2>
        <input type="text" id="angka1" placeholder="Angka Pertama">
        <input type="text" id="angka2" placeholder="Angka Kedua">
        <input type="text" id="hasil" placeholder="Hasil" readonly>
        <div>
            <button onclick="hitung('+')">Tambah</button>
            <button onclick="hitung('-')">Kurang</button>
            <button onclick="hitung('*')">Kali</button>
            <button onclick="hitung('/')">Bagi</button>
        </div>
    </div>

    <script>
        function hitung(operasi) {
            var angka1 = parseFloat(document.getElementById('angka1').value);
            var angka2 = parseFloat(document.getElementById('angka2').value);
            var hasil;

            switch (operasi) {
                case '+':
                    hasil = angka1 + angka2;
                    break;
                case '-':
                    hasil = angka1 - angka2;
                    break;
                case '*':
                    hasil = angka1 * angka2;
                    break;
                case '/':
                    hasil = angka1 / angka2;
                    break;
                default:
                    hasil = 'Error';
            }

            document.getElementById('hasil').value = hasil;
        }
    </script>
</body>
</html>
