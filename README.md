<!DOCTYPE html>  
<html lang="es">  
<head>  
    <meta charset="UTF-8">  
    <meta name="viewport" content="width=device-width, initial-scale=1.0">  
    <title>🤖 Family Rivas AI - Asistente Inteligente</title>  
    <style>  
        :root {  
            --primary-gradient: linear-gradient(135deg, #667eea 0%, #764ba2 100%);  
            --secondary-gradient: linear-gradient(135deg, #f093fb 0%, #f5576c 100%);  
            --accent-gradient: linear-gradient(135deg, #4facfe 0%, #00f2fe 100%);  
            --success-color: #10b981;  
            --warning-color: #f59e0b;  
            --danger-color: #ef4444;  
            --text-primary: #1f2937;  
            --text-secondary: #6b7280;  
            --bg-light: #f8fafc;  
            --bg-card: #ffffff;  
            --border-light: #e5e7eb;  
            --shadow-sm: 0 1px 2px rgba(0, 0, 0, 0.05);  
            --shadow-md: 0 4px 6px rgba(0, 0, 0, 0.1);  
            --shadow-lg: 0 10px 15px rgba(0, 0, 0, 0.1);  
            --shadow-xl: 0 20px 25px rgba(0, 0, 0, 0.1);  
        }  

        * {   
            margin: 0;   
            padding: 0;   
            box-sizing: border-box;   
        }  
        
        body {  
            font-family: 'Inter', 'Segoe UI', system-ui, sans-serif;  
            background: var(--primary-gradient);  
            min-height: 100vh;  
            padding: 10px;  
            color: var(--text-primary);  
            line-height: 1.6;  
        }  

        .container {  
            max-width: 1200px;  
            margin: 0 auto;  
            background: var(--bg-card);  
            border-radius: 24px;  
            overflow: hidden;  
            box-shadow: var(--shadow-xl);  
            height: 95vh;  
            display: flex;  
            flex-direction: column;  
            position: relative;  
        }  

        .creator-badge {  
            position: absolute;  
            top: 10px;  
            left: 50%;  
            transform: translateX(-50%);  
            background: rgba(255,215,0,0.9);  
            color: #1f2937;  
            padding: 8px 16px;  
            border-radius: 20px;  
            font-size: 0.75rem;  
            font-weight: 600;  
            backdrop-filter: blur(10px);  
            border: 2px solid rgba(255,255,255,0.3);  
            z-index: 10;  
            box-shadow: var(--shadow-md);  
        }  

        .header {  
            background: linear-gradient(135deg, #667eea, #764ba2, #4facfe);  
            background-size: 200% 200%;  
            animation: gradientShift 8s ease infinite;  
            color: white;  
            padding: 25px 30px;  
            position: relative;  
            overflow: hidden;  
        }  

        @keyframes gradientShift {  
            0% { background-position: 0% 50%; }  
            50% { background-position: 100% 50%; }  
            100% { background-position: 0% 50%; }  
        }  

        .header-content {  
            display: flex;  
            justify-content: space-between;  
            align-items: center;  
            position: relative;  
            z-index: 2;  
        }  

        .brand {  
            display: flex;  
            align-items: center;  
            gap: 15px;  
        }  

        .logo {  
            width: 60px;  
            height: 60px;  
            background: rgba(255,255,255,0.2);  
            border-radius: 50%;  
            display: flex;  
            align-items: center;  
            justify-content: center;  
            font-size: 24px;  
            backdrop-filter: blur(10px);  
            border: 2px solid rgba(255,255,255,0.3);  
        }  

        .brand-info h1 {  
            font-size: 1.8rem;  
            font-weight: 700;  
            margin-bottom: 5px;  
            text-shadow: 2px 2px 4px rgba(0,0,0,0.3);  
        }  

        .brand-info .tagline {  
            font-size: 0.9rem;  
            opacity: 0.9;  
            font-weight: 400;  
        }  

        .header-stats {  
            display: flex;  
            flex-direction: column;  
            align-items: flex-end;  
            gap: 8px;  
        }  

        .status-badge {  
            background: rgba(16, 185, 129, 0.9);  
            padding: 6px 12px;  
            border-radius: 20px;  
            font-size: 0.8rem;  
            font-weight: 600;  
            display: flex;  
            align-items: center;  
            gap: 6px;  
            backdrop-filter: blur(10px);  
        }  

        .stats-counter {  
            background: rgba(255,255,255,0.2);  
            padding: 6px 12px;  
            border-radius: 15px;  
            font-size: 0.8rem;  
            backdrop-filter: blur(10px);  
        }  

        .chat-container {  
            flex: 1;  
            display: flex;  
            flex-direction: column;  
            overflow: hidden;  
        }  

        .chat-area {  
            flex: 1;  
            overflow-y: auto;  
            padding: 25px;  
            background: linear-gradient(145deg, #f8fafc, #e2e8f0);  
            position: relative;  
        }  

        .chat-area::-webkit-scrollbar {  
            width: 6px;  
        }  

        .chat-area::-webkit-scrollbar-track {  
            background: #f1f5f9;  
        }  

        .chat-area::-webkit-scrollbar-thumb {  
            background: #cbd5e1;  
            border-radius: 3px;  
        }  

        .message {  
            margin: 20px 0;  
            display: flex;  
            align-items: flex-start;  
            animation: messageSlide 0.6s cubic-bezier(0.4, 0, 0.2, 1);  
        }  

        @keyframes messageSlide {  
            from {   
                opacity: 0;   
                transform: translateY(20px) scale(0.95);  
            }  
            to {   
                opacity: 1;   
                transform: translateY(0) scale(1);  
            }  
        }  

        .user-message {   
            justify-content: flex-end;   
        }  

        .avatar {  
            width: 50px;  
            height: 50px;  
            border-radius: 50%;  
            display: flex;  
            align-items: center;  
            justify-content: center;  
            margin: 0 15px;  
            font-size: 20px;  
            box-shadow: var(--shadow-md);  
            flex-shrink: 0;  
            position: relative;  
        }  

        .bot-message .avatar {  
            background: var(--primary-gradient);  
            color: white;  
        }  

        .user-message .avatar {  
            background: var(--secondary-gradient);  
            color: white;  
        }  

        .avatar::after {  
            content: '';  
            position: absolute;  
            bottom: -2px;  
            right: -2px;  
            width: 16px;  
            height: 16px;  
            background: var(--success-color);  
            border-radius: 50%;  
            border: 2px solid white;  
        }  

        .content {  
            max-width: 70%;  
            padding: 20px 24px;  
            border-radius: 20px;  
            line-height: 1.7;  
            font-size: 0.95rem;  
            box-shadow: var(--shadow-md);  
            position: relative;  
            word-wrap: break-word;  
        }  

        .bot-message .content {  
            background: linear-gradient(135deg, #e0f2fe, #f3e5f5);  
            border-bottom-left-radius: 8px;  
        }  

        .user-message .content {  
            background: linear-gradient(135deg, #fef3c7, #fed7aa);  
            border-bottom-right-radius: 8px;  
        }  

        .content::before {  
            content: '';  
            position: absolute;  
            width: 0;  
            height: 0;  
        }  

        .bot-message .content::before {  
            left: -8px;  
            top: 20px;  
            border-top: 8px solid transparent;  
            border-bottom: 8px solid transparent;  
            border-right: 8px solid #e0f2fe;  
        }  

        .user-message .content::before {  
            right: -8px;  
            top: 20px;  
            border-top: 8px solid transparent;  
            border-bottom: 8px solid transparent;  
            border-left: 8px solid #fef3c7;  
        }  

        .typing {  
            display: none;  
            align-items: flex-start;  
            margin: 20px 0;  
            animation: typingPulse 1.5s infinite;  
        }  

        @keyframes typingPulse {  
            0%, 100% { opacity: 0.7; }  
            50% { opacity: 1; }  
        }  

        .input-area {  
            padding: 25px;  
            background: linear-gradient(135deg, #ffffff, #f8fafc);  
            border-top: 1px solid var(--border-light);  
            box-shadow: 0 -4px 6px rgba(0, 0, 0, 0.05);  
        }  

        .input-container {  
            display: flex;  
            gap: 15px;  
            align-items: center;  
            background: white;  
            border-radius: 25px;  
            padding: 12px 20px;  
            border: 2px solid #e5e7eb;  
            transition: all 0.3s ease;  
            box-shadow: var(--shadow-sm);  
        }  

        .input-container:focus-within {  
            border-color: #667eea;  
            box-shadow: 0 0 0 3px rgba(102, 126, 234, 0.1);  
            transform: translateY(-2px);  
        }  

        #message-input {  
            flex: 1;  
            border: none;  
            outline: none;  
            font-size: 1rem;  
            padding: 8px 0;  
            background: transparent;  
            color: var(--text-primary);  
        }  

        #message-input::placeholder {  
            color: var(--text-secondary);  
        }  

        .btn {  
            border: none;  
            border-radius: 50px;  
            padding: 12px 24px;  
            font-weight: 600;  
            cursor: pointer;  
            transition: all 0.3s ease;  
            font-size: 0.9rem;  
            display: flex;  
            align-items: center;  
            gap: 8px;  
        }  

        .btn-primary {  
            background: var(--primary-gradient);  
            color: white;  
            box-shadow: var(--shadow-md);  
        }  

        .btn-primary:hover {  
            transform: translateY(-2px);  
            box-shadow: var(--shadow-lg);  
        }  

        .suggestions {  
            display: flex;  
            gap: 10px;  
            margin-bottom: 15px;  
            flex-wrap: wrap;  
        }  

        .suggestion-chip {  
            background: rgba(102, 126, 234, 0.1);  
            color: #667eea;  
            padding: 8px 16px;  
            border-radius: 20px;  
            font-size: 0.85rem;  
            cursor: pointer;  
            transition: all 0.3s ease;  
            border: 1px solid rgba(102, 126, 234, 0.2);  
        }  

        .suggestion-chip:hover {  
            background: rgba(102, 126, 234, 0.15);  
            transform: translateY(-2px);  
        }  

        /* RESPONSIVE */  
        @media (max-width: 768px) {  
            .container { height: 100vh; border-radius: 0; }  
            .header-content { flex-direction: column; gap: 15px; }  
            .content { max-width: 85%; }  
            .creator-badge { font-size: 0.7rem; padding: 6px 12px; }  
        }  
    </style>  
</head>  
<body>  
    <div class="container">  
        <!-- Certificado del Creador -->  
        <div class="creator-badge">  
            🏆 Creado por Eros Jeancarlos Cordova Rivas - Desarrollador Certificado  
        </div>  

        <!-- Header -->  
        <div class="header">  
            <div class="header-content">  
                <div class="brand">  
                    <div class="logo">🤖</div>  
                    <div class="brand-info">  
                        <h1>Family Rivas AI</h1>  
                        <div class="tagline">Asistente Inteligente con IA Avanzada</div>  
                    </div>  
                </div>  
                <div class="header-stats">  
                    <div class="status-badge">  
                        <span>🟢</span> En línea  
                    </div class="stats-counter">  
                        <span id="message-count">0</span> mensajes procesados  
                    </div>  
                </div>  
            </div>  
        </div>  

        <!-- Chat Container -->  
        <div class="chat-container">  
            <div class="chat-area" id="chat-area">  
                <!-- Mensaje de bienvenida -->  
                <div class="message bot-message">  
                    <div class="avatar">🤖</div>  
                    <div class="content">  
                        <strong>¡Hola! 👋 Soy Family Rivas AI</strong><br>  
                        Soy tu asistente inteligente personal creado por <strong>Eros Jeancarlos Cordova Rivas</strong>.   
                        Puedo ayudarte con:  
                        <ul style="margin: 10px 0; padding-left: 20px;">  
                            <li>🧮 Matemáticas y cálculos complejos</li>  
                            <li>📝 Escritura y corrección de textos</li>  
                            <li>🔍 Búsqueda de información</li>  
                            <li>💡 Resolución de problemas</li>  
                            <li>🎯 Análisis y recomendaciones</li>  
                        </ul>  
                        ¿En qué puedo ayudarte hoy?  
                    </div>  
                </div>  

                <!-- Indicador de escritura -->  
                <div class="typing" id="typing-indicator">  
                    <div class="avatar">🤖</div>  
                    <div class="content">  
                        IA Rivas está escribiendo<span class="typing-dots">...</span>  
                    </div>  
                </div>  
            </div>  

            <!-- Área de entrada -->  
            <div class="input-area">  
                <!-- Sugerencias rápidas -->  
                <div class="suggestions">  
                    <div class="suggestion-chip" onclick="sendSuggestion('¿Cómo puedes ayudarme?')">  
                        ❓ ¿Cómo puedes ayudarme?  
                    </div>  
                    <div class="suggestion-chip" onclick="sendSuggestion('Resuelve esta ecuación: 2x + 5 = 15')">  
                        🧮 Resolver ecuación  
                    </div>  
                    <div class="suggestion-chip" onclick="sendSuggestion('Corrige este texto')">  
                        📝 Corregir texto  
                    </div>  
                    <div class="suggestion-chip" onclick="sendSuggestion('Explícame sobre IA')">  
                        🤖 Sobre IA  
                    </div>  
                </div>  

                <!-- Input container -->  
                <div class="input-container">  
                    <input   
                        type="text"   
                        id="message-input"   
                        placeholder="Escribe tu mensaje aquí... (presiona Enter para enviar)"  
                        autocomplete="off"  
                    >  
                    <button class="btn btn-primary" onclick="sendMessage()">  
                        <span>📤</span> Enviar  
                    </button>  
                </div>  
            </div>  
        </div>  
    </div>  

    <script>  
        // === VARIABLES GLOBALES ===  
        let messageCount = 0;  
        const chatArea = document.getElementById('chat-area');  
        const messageInput = document.getElementById('message-input');  
        const typingIndicator = document.getElementById('typing-indicator');  
        const messageCountElement = document.getElementById('message-count');  

        // === FUNCIONES PRINCIPALES ===  
        function sendMessage() {  
            const message = messageInput.value.trim();  
            if (!message) return;  

            addUserMessage(message);  
            messageInput.value = '';  
            showTyping();  

            // Simular procesamiento de IA  
            setTimeout(() => {  
                hideTyping();  
                const response = generateAIResponse(message);  
                addBotMessage(response);  
                updateMessageCount();  
            }, Math.random() * 2000 + 1000); // Entre 1-3 segundos  
        }  

        function addUserMessage(message) {  
            const messageDiv = document.createElement('div');  
            messageDiv.className = 'message user-message';  
            messageDiv.innerHTML = `  
                <div class="avatar">👤</div>  
                <div class="content">${escapeHtml(message)}</div>  
            `;  
            chatArea.appendChild(messageDiv);  
            scrollToBottom();  
        }  

        function addBotMessage(message) {  
            const messageDiv = document.createElement('div');  
            messageDiv.className = 'message bot-message';  
            messageDiv.innerHTML = `  
                <div class="avatar">🤖</div>  
                <div class="content">${message}</div>  
            `;  
            chatArea.appendChild(messageDiv);  
            scrollToBottom();  
        }  

        function showTyping() {  
            typingIndicator.style.display = 'flex';  
            scrollToBottom();  
        }  

        function hideTyping() {  
            typingIndicator.style.display = 'none';  
        }  

        function scrollToBottom() {  
            chatArea.scrollTop = chatArea.scrollHeight;  
        }  

        function updateMessageCount() {  
            messageCount++;  
            messageCountElement.textContent = messageCount;  
        }  

        function sendSuggestion(suggestion) {  
            messageInput.value = suggestion;  
            sendMessage();  
        }  

        function escapeHtml(text) {  
            const div = document.createElement('div');  
            div.textContent = text;  
            return div.innerHTML;  
        }  

        // === GENERADOR DE RESPUESTAS DE IA ===  
        function generateAIResponse(userMessage) {  
            const message = userMessage.toLowerCase();  
            
            // Respuestas sobre el creador  
            if (message.includes('creador') || message.includes('quien te creo') || message.includes('eros')) {  
                return `  
                    <strong>👨‍💻 Sobre mi creador</strong><br>  
                    Fui creado por <strong>Eros Jeancarlos Cordova Rivas</strong>, un desarrollador apasionado por la inteligencia artificial y la tecnología.   
                    Él me diseñó para ser un asistente útil, inteligente y amigable.<br><br>  
                    <em>🏆 "La tecnología debe servir para mejorar la vida de las personas" - Eros J.C. Rivas</em>  
                `;  
            }  

            // Respuestas sobre capacidades  
            if (message.includes('que puedes hacer') || message.includes('ayudarme') || message.includes('capacidades')) {  
                return `  
                    <strong>🚀 Mis capacidades incluyen:</strong><br>  
                    <ul style="margin: 10px 0; padding-left: 20px;">  
                        <li>🧮 <strong>Matemáticas:</strong> Cálculos, ecuaciones, estadísticas</li>  
                        <li>📝 <strong>Escritura:</strong> Corrección, redacción, traducción</li>  
                        <li>🔍 <strong>Análisis:</strong> Datos, textos, patrones</li>  
                        <li>💡 <strong>Creatividad:</strong> Ideas, soluciones, brainstorming</li>  
                        <li>🎯 <strong>Consultoría:</strong> Recomendaciones personalizadas</li>  
                        <li>🤖 <strong>Conversación:</strong> Chat natural e inteligente</li>  
                    </ul>  
                    ¿Hay algo específico en lo que te gustaría que te ayude?  
                `;  
            }  

            // Matemáticas básicas  
            if (message.includes('resuelve') || message.includes('calcula') || message.includes('ecuación')) {  
                if (message.includes('2x + 5 = 15')) {  
                    return `  
                        <strong>🧮 Resolviendo la ecuación: 2x + 5 = 15</strong><br><br>  
                        <strong>Paso 1:</strong> Restar 5 de ambos lados<br>  
                        2x + 5 - 5 = 15 - 5<br>  
                        2x = 10<br><br>  
                        <strong>Paso 2:</strong> Dividir ambos lados por 2<br>  
                        2x ÷ 2 = 10 ÷ 2<br>  
                        x = 5<br><br>  
                        <strong>✅ Respuesta: x = 5</strong><br>  
                        <em>Verificación: 2(5) + 5 = 10 + 5 = 15 ✓</em>  
                    `;  
                }  
                return `  
                    <strong>🧮 Solucionador matemático activo</strong><br>  
                    Por favor, proporciona la ecuación o cálculo específico que quieres que resuelva.   
                    Puedo trabajar con:<br>  
                    • Ecuaciones lineales y cuadráticas<br>  
                    • Cálculos aritméticos<br>  
                    • Porcentajes y estadísticas<br>  
                    • Conversiones de unidades
                                    `;  
            }  

            // Corrección de texto  
            if (message.includes('corrige') || message.includes('revisa texto') || message.includes('gramática')) {  
                return `  
                    <strong>📝 Corrector de texto activado</strong><br>  
                    Por favor, comparte el texto que quieres que revise y corregiré:<br>  
                    • Ortografía y gramática<br>  
                    • Puntuación y estructura<br>  
                    • Estilo y claridad<br>  
                    • Sugerencias de mejora<br><br>  
                    <em>💡 Tip: Pega tu texto en el próximo mensaje y lo analizaré detalladamente.</em>  
                `;  
            }  

            // Sobre IA y tecnología  
            if (message.includes('ia') || message.includes('inteligencia artificial') || message.includes('tecnología')) {  
                return `  
                    <strong>🤖 Sobre Inteligencia Artificial</strong><br>  
                    La IA es una rama de la informática que busca crear sistemas capaces de realizar tareas que normalmente requieren inteligencia humana.<br><br>  
                    <strong>Tipos principales:</strong><br>  
                    • <strong>IA Débil:</strong> Especializada en tareas específicas (como yo)<br>  
                    • <strong>IA Fuerte:</strong> Inteligencia general artificial (aún en desarrollo)<br><br>  
                    <strong>Aplicaciones actuales:</strong><br>  
                    🚗 Vehículos autónomos | 🏥 Diagnóstico médico<br>  
                    💬 Asistentes virtuales | 🎮 Videojuegos<br>  
                    📊 Análisis de datos | 🎨 Arte generativo<br><br>  
                    <em>El futuro es prometedor y lleno de posibilidades.</em>  
                `;  
            }  

            // Saludos  
            if (message.includes('hola') || message.includes('buenos') || message.includes('buenas')) {  
                const greetings = [  
                    "¡Hola! 👋 Me alegra verte por aquí. ¿En qué puedo ayudarte hoy?",  
                    "¡Saludos! 🌟 Soy Family Rivas AI, listo para asistirte.",  
                    "¡Hola! 😊 ¿Qué aventura intelectual emprenderemos juntos hoy?",  
                    "¡Buen día! ☀️ Estoy aquí para hacer tu día más productivo."  
                ];  
                return greetings[Math.floor(Math.random() * greetings.length)];  
            }  

            // Despedidas  
            if (message.includes('adiós') || message.includes('bye') || message.includes('hasta luego')) {  
                const farewells = [  
                    "¡Hasta luego! 👋 Fue un placer ayudarte. Regresa cuando quieras.",  
                    "¡Adiós! 🌟 Espero haberte sido útil. ¡Que tengas un excelente día!",  
                    "¡Nos vemos pronto! 😊 Recuerda que siempre estaré aquí para ayudarte.",  
                    "¡Hasta la vista! 🚀 Gracias por usar Family Rivas AI."  
                ];  
                return farewells[Math.floor(Math.random() * farewells.length)];  
            }  

            // Preguntas sobre el tiempo  
            if (message.includes('tiempo') || message.includes('clima') || message.includes('temperatura')) {  
                return `  
                    <strong>🌤️ Información meteorológica</strong><br>  
                    Actualmente no tengo acceso a datos meteorológicos en tiempo real, pero puedo sugerirte:<br><br>  
                    📱 <strong>Apps recomendadas:</strong><br>  
                    • Weather.com | AccuWeather<br>  
                    • Weather Underground | Windy<br><br>  
                    🔍 <strong>Sitios web:</strong><br>  
                    • tiempo.com | eltiempo.es<br>  
                    • weather.gov (oficial)<br><br>  
                    <em>💡 En futuras actualizaciones podré acceder a datos meteorológicos en tiempo real.</em>  
                `;  
            }  

            // Preguntas sobre programación  
            if (message.includes('programar') || message.includes('código') || message.includes('javascript') || message.includes('html')) {  
                return `  
                    <strong>💻 Asistencia en programación</strong><br>  
                    ¡Perfecto! Puedo ayudarte con desarrollo web y programación:<br><br>  
                    <strong>Lenguajes que domino:</strong><br>  
                    🌐 HTML5, CSS3, JavaScript<br>  
                    ⚛️ React, Vue.js, Angular<br>  
                    🐍 Python, Java, C++<br>  
                    🗄️ SQL, MongoDB, Firebase<br><br>  
                    <strong>Puedo ayudarte con:</strong><br>  
                    • Debugging y corrección de errores<br>  
                    • Explicación de conceptos<br>  
                    • Optimización de código<br>  
                    • Buenas prácticas<br><br>  
                    ¿Qué proyecto estás desarrollando?  
                `;  
            }  

            // Respuestas motivacionales  
            if (message.includes('motivación') || message.includes('inspiración') || message.includes('triste')) {  
                const motivational = [  
                    `<strong>💪 ¡Ánimo!</strong><br>Recuerda que cada desafío es una oportunidad de crecimiento. <em>"El éxito no es final, el fracaso no es fatal: es el coraje de continuar lo que cuenta."</em> - Winston Churchill`,  
                    `<strong>🌟 Inspiración del día</strong><br>Eres más fuerte de lo que crees y más capaz de lo que imaginas. <em>"El único modo de hacer un gran trabajo es amar lo que haces."</em> - Steve Jobs`,  
                    `<strong>🚀 Mensaje motivacional</strong><br>Cada pequeño paso cuenta en el camino hacia tus metas. <em>"No importa qué tan lento vayas, siempre y cuando no te detengas."</em> - Confucio`  
                ];  
                return motivational[Math.floor(Math.random() * motivational.length)];  
            }  

            // Respuesta por defecto con IA generativa  
            const defaultResponses = [  
                `<strong>🤔 Interesante pregunta</strong><br>Déjame procesar tu consulta: "${userMessage}"<br><br>Aunque soy una IA avanzada, siempre estoy aprendiendo. ¿Podrías ser más específico sobre lo que necesitas? Esto me ayudará a darte una respuesta más precisa y útil.`,  
                
                `<strong>💭 Analizando tu mensaje</strong><br>He procesado: "${userMessage}"<br><br>Para brindarte la mejor asistencia posible, me gustaría entender mejor tu necesidad. ¿Podrías proporcionar más contexto o detalles específicos?`,  
                
                `<strong>🔍 Procesando solicitud</strong><br>Tu mensaje: "${userMessage}"<br><br>Estoy aquí para ayudarte con cualquier tema. Si pudieras reformular tu pregunta o agregar más detalles, podré ofrecerte una respuesta más personalizada y útil.`,  
                
                `<strong>🎯 Enfocando respuesta</strong><br>Entiendo que preguntas sobre: "${userMessage}"<br><br>Mi objetivo es ser lo más útil posible. ¿Hay algún aspecto específico de este tema en el que te gustaría que me enfoque?`  
            ];  
            
            return defaultResponses[Math.floor(Math.random() * defaultResponses.length)];  
        }  

        // === EVENT LISTENERS ===  
        messageInput.addEventListener('keypress', function(e) {  
            if (e.key === 'Enter') {  
                sendMessage();  
            }  
        });  

        // Autoenfoque en el input al cargar  
        window.addEventListener('load', function() {  
            messageInput.focus();  
        });  

        // Animación de puntos en el indicador de escritura  
        setInterval(() => {  
            const dots = document.querySelector('.typing-dots');  
            if (dots) {  
                const currentDots = dots.textContent;  
                if (currentDots === '...') {  
                    dots.textContent = '.';  
                } else if (currentDots === '.') {  
                    dots.textContent = '..';  
                } else {  
                    dots.textContent = '...';  
                }  
            }  
        }, 500);  

        // === FUNCIONES ADICIONALES ===  
        // Limpiar chat (función oculta para desarrolladores)  
        function clearChat() {  
            const messages = chatArea.querySelectorAll('.message:not(:first-child)');  
            messages.forEach(msg => msg.remove());  
            messageCount = 0;  
            messageCountElement.textContent = '0';  
        }  

        // Estadísticas del chat  
        function getStats() {  
            console.log(`📊 Estadísticas Family Rivas AI:  
            💬 mensaje procesado: ${messageCount}  
            🕒 Sesión iniciada: ${new Date().toLocaleString()}  
            👨‍💻 Desarrollado por: Eros Jeancarlos Cordova Rivas  
            🤖 Versión: 1.0.0`);  
        }  

        // Modo desarrollador (teclas especiales)  
        document.addEventListener('keydown', function(e) {  
        // Ctrl + Shift + D = Estadísticas
            if (e.ctrlKey && e.shiftKey && e.key === 'D') {
                getStats();
            }
            
            // Ctrl + Shift + C = Limpiar chat
            if (e.ctrlKey && e.shiftKey && e.key === 'C') {
                if (confirm('¿Seguro que quieres limpiar el chat?')) {
                    clearChat();
                }
            }
        });

        // Mensaje de bienvenida del desarrollador en consola
        console.log(`
        🚀 Family Rivas AI - Asistente Inteligente
        ==========================================
        👨‍💻 Desarrollado por: Eros Jeancarlos Cordova Rivas
        🤖 Versión: 1.0.0
        📅 Fecha: ${new Date().toLocaleDateString()}
        
        💡 Atajos de teclado:
        • Enter: Enviar mensaje
        • Ctrl+Shift+D: Ver estadísticas
        • Ctrl+Shift+C: Limpiar chat
        
        🔗 Funciones disponibles:
        • sendMessage() - Enviar mensaje
        • clearChat() - Limpiar conversación
        • getStats() - Ver estadísticas
        
        ¡Gracias por usar Family Rivas AI! 🌟
        `);

        // Inicialización
        document.addEventListener('DOMContentLoaded', function() {
            // Mensaje de bienvenida personalizado
            setTimeout(() => {
                const welcomeMessages = [
                    "¡Sistema iniciado correctamente! 🟢",
                    "Conexión establecida con éxito ✅",
                    "IA Family Rivas lista para asistir 🤖"
                ];
                
                console.log(welcomeMessages[Math.floor(Math.random() * welcomeMessages.length)]);
            }, 1000);
        });
    </script>
</body>
</html>
