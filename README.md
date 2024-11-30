<!DOCTYPE html>
<html lang="tr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Silah ve Geri Sayım</title>
    <style>
        #gun, #countdown, #message {
            display: none;
        }
    </style>
</head>
<body>
    <a href="#" onclick="showGun(); return false;">Linke Tıklayın</a>

    <div id="gun">
        <img src="silah_resmi.jpg" alt="Silah" width="300">
    </div>

    <div id="countdown"></div>
    <div id="message"></div>

    <script>
        function showGun() {
            document.getElementById('gun').style.display = 'block';
            setTimeout(startCountdown, 1000);
        }

        function startCountdown() {
            let countdown = 10;
            document.getElementById('countdown').style.display = 'block';
            let countdownElement = document.getElementById('countdown');
            countdownElement.innerHTML = countdown;

            let interval = setInterval(function() {
                countdown--;
                countdownElement.innerHTML = countdown;
                if (countdown <= 0) {
                    clearInterval(interval);
                    showMessage();
                }
            }, 1000);
        }

        function showMessage() {
            document.getElementById('countdown').style.display = 'none';
            document.getElementById('message').style.display = 'block';
            document.getElementById('message').innerHTML = "Beni PUBG'den ekle oynayalım! 61418521170";
        }
    </script>
</body>
</html>
