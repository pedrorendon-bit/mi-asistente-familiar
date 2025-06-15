<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>🤖 Asistente Familiar IA</title>
    <style>
        * { margin: 0; padding: 0; box-sizing: border-box; }
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh; padding: 20px;
        }
        .container {
            max-width: 900px; margin: 0 auto; background: white;
            border-radius: 20px; overflow: hidden;
            box-shadow: 0 20px 40px rgba(0,0,0,0.15);
            height: 90vh; display: flex; flex-direction: column;
        }
        .header {
            background: linear-gradient(135deg, #4f46e5, #06b6d4);
            color: white; padding: 20px; text-align: center; position: relative;
        }
        .header h1 { font-size: 1.8rem; margin-bottom: 5px; }
        .header p { opacity: 0.9; font-size: 0.9rem; }
        .setup-btn {
            position: absolute; top: 15px; right: 15px;
            background: rgba(255,255,255,0.2); border: none;
            padding: 8px 15px; border-radius: 20px; color: white;
            cursor: pointer; font-size: 0.8rem;
        }
        .api-setup {
            background: linear-gradient(135deg, #fef3c7, #fde68a);
            padding: 20px; display: none;
        }
        .api-input {
            width: 100%; padding: 12px; border: 2px solid #f59e0b;
            border-radius: 10px; margin: 10px 0;
        }
        .save-btn {
            background: #10b981; color: white; border: none;
            padding: 12px 25px; border-radius: 25px; cursor: pointer;
        }
        .chat-area {
            flex: 1; overflow-y: auto; padding: 20px;
            background: #f8fafc;
        }
        .message {
            margin: 15px 0; display: flex; align-items: flex-start;
        }
        .message.user-message { justify-content: flex-end; }
        .avatar {
            width: 40px; height: 40px; border-radius: 50%;
            display: flex; align-items: center; justify-content: center;
            margin: 0 10px; font-size: 1.2rem;
        }
        .bot-message .avatar { background: #10b981; }
        .user-message .avatar { background: #f59e0b; }
        .content {
            max-width: 70%; padding: 15px 20px; border-radius: 20px;
            font-size: 0.95rem; line-height: 1.5;
        }
        .bot-message .content {
            background: #e2e8f0; color: #1e293b;
        }
        .user-message .content {
            background: #4f46e5; color: white;
        }
        .input-container {
            padding: 20px; background: white; display: flex; gap: 10px;
        }
        #message-input {
            flex: 1; padding: 15px 20px; border: 2px solid #e2e8f0;
            border-radius: 25px; font-size: 1rem;
        }
        #send-btn {
            background: #4f46e5; color: white; border: none;
            padding: 15px 25px; border-radius: 25px; cursor: pointer;
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="header">
            <h1>🤖 Asistente Familiar IA</h1>
            <p>Powered by OpenAI GPT-4</p>
            <button class="setup-btn" onclick="toggleSetup()">⚙️ Config</button>
        </div>
        
        <div id="api-setup" class="api-setup">
            <h3>🔑 Configurar OpenAI</h3>
            <input type="password" id="api-key" class="api-input" placeholder="Pega tu API Key aquí">
            <button onclick="saveAPI()" class="save-btn">✅ Guardar</button>
        </div>
        
        <div id="chat-area" class="chat-area">
            <div class="message bot-message">
                <div class="avatar">🤖</div>
                <div class="content">¡Hola! Configura tu API Key y podremos chatear.</div>
            </div>
        </div>
        
        <div class="input-container">
            <input type="text" id="message-input" placeholder="Escribe tu mensaje...">
            <button onclick="sendMessage()" id="send-btn">Enviar</button>
        </div>
    </div>

    <script>
        let apiKey = localStorage.getItem('openai_api_key');

        function toggleSetup() {
            const setup = document.getElementById('api-setup');
            setup.style.display = setup.style.display === 'none' ? 'block' : 'none';
        }

        function saveAPI() {
            const key = document.getElementById('api-key').value;
            if (key.startsWith('sk-')) {
                localStorage.setItem('openai_api_key', key);
                apiKey = key;
                document.getElementById('api-setup').style.display = 'none';
                addMessage('bot', '✅ API configurada! Ya puedes chatear.');
            } else {
                alert('❌ API Key inválida');
            }
        }

        function addMessage(type, text) {
            const chatArea = document.getElementById('chat-area');
            const messageDiv = document.createElement('div');
            messageDiv.className = `message ${type}-message`;
            messageDiv.innerHTML = `
                <div class="avatar">${type === 'bot' ? '🤖' : '👤'}</div>
                <div class="content">${text}</div>
            `;
            chatArea.appendChild(messageDiv);
            chatArea.scrollTop = chatArea.scrollHeight;
        }

        async function sendMessage() {
            const input = document.getElementById('message-input');
            const message = input.value.trim();
            
            if (!message) return;
            if (!apiKey) {
                alert('⚠️ Configura tu API Key primero');
                return;
            }

            addMessage('user', message);
            input.value = '';

            try {
                const response = await fetch('https://api.openai.com/v1/chat/completions', {
                    method: 'POST',
                    headers: {
                        'Content-Type': 'application/json',
                        'Authorization': `Bearer ${apiKey}`
                    },
                    body: JSON.stringify({
                        model: 'gpt-3.5-turbo',
                        messages: [{ role: 'user', content: message }],
                        max_tokens: 150
                    })
                });

                const data = await response.json();
                
                if (data.choices && data.choices[0]) {
                    addMessage('bot', data.choices[0].message.content);
                } else {
                    addMessage('bot', '❌ Error en la respuesta');
                }
            } catch (error) {
                addMessage('bot', '❌ Error de conexión');
            }
        }

        document.getElementById('message-input').addEventListener('keypress', function(e) {
            if (e.key === 'Enter') {
                sendMessage();
            }
        });
    </script>
</body>
</html>
