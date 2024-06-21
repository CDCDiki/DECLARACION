<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>¿Quieres ser mi novia? 😅😰💦</title>
    <style>
        body, html {
            height: 100%;
            margin: 0;
            font-family: Arial, sans-serif;
            text-align: center;
            color: white;
            text-shadow: 2px 2px 4px #000000;
            overflow: hidden;
            background-image: url('https://img.freepik.com/foto-gratis/pareja-anime-enamorada_23-2151103337.jpg');
            background-size: cover;
            background-position: center;
        }
        .container {
            position: relative;
            z-index: 1;
            background: rgba(0, 0, 0, 0.5);
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            height: 100vh;
        }
        h1 {
            font-size: 2.5em;
            color: #ff69b4;
        }
        button {
            padding: 10px 20px;
            margin: 10px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-size: 1em;
        }
        #yesBtn {
            background-color: #32cd32;
            color: white;
            margin-right: 10px;
        }
        #noBtn {
            background-color: #ff6347;
            color: white;
            position: absolute;
            top: 20px;
            left: 150px; /* Posición inicial al lado del botón Sí */
        }
        p {
            font-size: 1.2em;
            display: none;
            margin-top: 20px;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>¿Quieres ser mi novia? 😅😰💦</h1>
        <button id="yesBtn">Sí</button>
        <button id="noBtn">No</button>
        <p id="message"></p>
    </div>

    <script>
        document.getElementById('yesBtn').onclick = function() {
            document.getElementById('message').innerText = "¡Gracias! ¡Me haces muy feliz! 💕😊";
            document.getElementById('message').style.display = 'block';
        };

        document.getElementById('noBtn').onclick = function() {
            const messages = [
                "Por favor, di que sí. 🙏❤️",
                "No te imaginas cuánto me harías feliz. 💖",
                "¿Estás segura? ¡Seremos una pareja genial! 😘",
                "Piénsalo bien, seremos muy felices juntos. 😊",
                "¡Te prometo que no te arrepentirás! 💕",
                "Eres muy especial para mí. 😍",
                "¡Dale una oportunidad al amor! 💓"
            ];
            let messageIndex = Math.floor(Math.random() * messages.length);
            document.getElementById('message').innerText = messages[messageIndex];
            document.getElementById('message').style.display = 'block';

            // Mover el botón No a otra posición aleatoria
            let container = document.querySelector('.container');
            let containerRect = container.getBoundingClientRect();
            let newX = Math.random() * (containerRect.width - 100);
            let newY = Math.random() * (containerRect.height - 100);
            document.getElementById('noBtn').style.left = `${newX}px`;
            document.getElementById('noBtn').style.top = `${newY}px`;
        };
    </script>
</body>
</html>
