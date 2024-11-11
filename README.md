<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Site de Diversão</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            background-color: #f0f8ff;
        }
        
        .container {
            text-align: center;
        }
        
        h1 {
            font-size: 24px;
            margin-bottom: 10px;
        }
        
        p {
            font-size: 18px;
            color: #333;
        }
        
        input[type="text"] {
            padding: 10px;
            font-size: 16px;
            width: 200px;
        }
        
        button {
            padding: 10px 20px;
            font-size: 16px;
            margin-left: 10px;
            background-color: #4CAF50;
            color: white;
            border: none;
            cursor: pointer;
        }
        
        button:hover {
            background-color: #45a049;
        }
        
        #errorMessage {
            font-size: 16px;
            margin-top: 10px;
            color: red;
            display: none;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Bem-vindo ao site de Gabriel Ferreti</h1>
        <p>Se quiser dar algumas risadas, escreva "Diego" na caixa de mensagens abaixo.</p>

        <!-- Caixa de mensagem e botão enviar -->
        <div>
            <input type="text" id="messageBox" placeholder="Escreva aqui...">
            <button id="sendButton">Enviar</button>
        </div>

        <!-- Mensagem de erro -->
        <p id="errorMessage"></p>
    </div>

    <script>
        // Obter referências aos elementos HTML
        const messageBox = document.getElementById("messageBox");
        const errorMessage = document.getElementById("errorMessage");
        const sendButton = document.getElementById("sendButton");

        // Adicionar um evento de clique ao botão "Enviar"
        sendButton.addEventListener("click", function() {
            const message = messageBox.value.trim();

            // Verificar se a mensagem contém exatamente a palavra "Diego"
            if (message.toLowerCase() === "diego") {
                errorMessage.textContent = 'Esse nome não é permitido aqui, pois o correto é "Didi".';
                errorMessage.style.display = "block";
            } else if (message !== "") {
                errorMessage.style.display = "none";
                alert("Mensagem enviada: " + message);
            } else {
                errorMessage.textContent = "Por favor, escreva algo antes de enviar.";
                errorMessage.style.display = "block";
            }

            messageBox.value = ""; // Limpar a caixa de mensagens após enviar
        });
    </script>
</body>
</html>


<!---
Bieldosprompts/Bieldosprompts is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
