<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Jornada do Meu Aniversário</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            background-color: #f4f4f9;
            margin: 0;
            padding: 20px;
        }
        h1, h2 {
            color: #4CAF50;
        }
        p {
            font-size: 18px;
            color: #333;
            margin: 20px 0;
        }
        iframe {
            width: 100%;
            max-width: 720px;
            height: 405px;
            border: none;
            border-radius: 15px;
            margin: 20px 0;
        }
        button {
            padding: 15px 30px;
            font-size: 16px;
            background-color: #4CAF50;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
        button:hover {
            background-color: #45a049;
        }
        #senha-container, #conteudo, #localizacao {
            display: none;
        }
        input[type="text"] {
            padding: 10px;
            font-size: 16px;
            border: 1px solid #ccc;
            border-radius: 5px;
            margin-right: 10px;
        }
    </style>
    <script>
        function iniciarJornada() {
            document.querySelector('#senha-container').style.display = 'block';
        }

        function verificarSenha() {
            const senha = document.querySelector('#senha').value;
            if (senha === "0802") {
                document.querySelector('#senha-container').style.display = 'none';
                document.querySelector('#conteudo').style.display = 'block';
            } else {
                alert("Senha incorreta. Tente novamente.");
            }
        }

        function verificarResposta() {
            const resposta = document.querySelector('#resposta').value.toLowerCase();
            if (resposta === "sofia") {
                document.querySelector('#misterio').style.display = 'none';
                document.querySelector('#localizacao').style.display = 'block';
            } else {
                alert("Resposta incorreta. Tente novamente.");
            }
        }
    </script>
</head>
<body>
    <h1>Jornada do Meu Aniversário</h1>
    <button onclick="iniciarJornada()">Iniciar Jornada</button>
    
    <div id="senha-container">
        <h2>Digite a senha para continuar:</h2>
        <input type="text" id="senha">
        <button onclick="verificarSenha()">Entrar</button>
    </div>

    <div id="conteudo">
        <h2>Mensagem Especial</h2>
        <p>Você é uma pessoa incrível e essencial na vida de todos nós. Cada momento ao seu lado é único e especial. Esperamos que essa jornada traga alegria e muitas memórias inesquecíveis. 💖</p>
        
        <iframe src="https://www.youtube.com/embed/OMPVAZIs_sE" allowfullscreen></iframe>
        
        <div id="misterio">
            <h2>Hora do Mistério</h2>
            <p>Em cada nota, uma lembrança,<br>
               Cantamos juntos, como uma dança.<br>
               Uma canção que nos faz sorrir,<br>
               Nosso amor, ela faz sentir.</p>
            <input type="text" id="resposta">
            <button onclick="verificarResposta()">Responder</button>
        </div>

        <div id="localizacao">
            <h2>Parabéns! Você acertou!</h2>
            <p>Mande uma mensagem para Eni chamando ela de <strong>Tia</strong></p>
        </div>
    </div>
</body>
</html>
