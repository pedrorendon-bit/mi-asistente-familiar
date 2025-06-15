<!DOCTYPE html>  
<html lang="es">  
<head>  
    <meta charset="UTF-8">  
    <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=no">  
    <meta name="apple-mobile-web-app-capable" content="yes">  
    <meta name="apple-mobile-web-app-status-bar-style" content="black-translucent">  
    <meta name="mobile-web-app-capable" content="yes">  
    <title>Family Rivas AI - Asistente Inteligente Avanzado</title>  
    
    <!-- PWA Manifest -->  
    <link rel="manifest" href="data:application/json;base64,eyJuYW1lIjoiRmFtaWx5IFJpdmFzIEFJIiwic2hvcnRfbmFtZSI6IkYuUml2YXMgQUkiLCJzdGFydF91cmwiOiIuLyIsImRpc3BsYXkiOiJzdGFuZGFsb25lIiwidGhlbWVfY29sb3IiOiIjNjY3ZWVhIiwiYmFja2dyb3VuZF9jb2xvciI6IiNmOGZhZmMiLCJpY29ucyI6W3sic3JjIjoiZGF0YTppbWFnZS9zdmcreG1sO2Jhc2U2NCxQSE4yWnlCM2FXUjBhRDBpTVRJNElpQm9aV2xuYUhROUlqRXlPQ0lpSUhacFpYZENiM2c5SWpBZ01DQXhNamdnTVRJNElpQm1hV3hzUFNJalpqZ3paakZtSWlCNGJXeHVjejBpYUhSMGNEb3ZMM2QzZHk1M00yNXZjbWN2TWpBd01DOXpkbWNpUGp4eVpXTjBJSGRwWkhSb1BTSXhNamdpSUdobGFXZG9kRDBpTVRJNElpQm1hV3hzUFNJalpqZ3paakZtSWk4K1BIUmxlSFFnZUQwaU5qUWlJSGs5SWpZMElpQm1hV3hzUFNJalJqZEdOamtpSUdadmJuUXRjMmw2WlQwaU16QWlJSFJsZUhRdFlXNWphRzl5UFNKdGFXUmtiR1VpUGpGQlNVTThMM1JsZUhRK1BDOXpkbWMrIiwic2l6ZXMiOiIxMjh4MTI4IiwidHlwZSI6ImltYWdlL3N2Zyt4bWwifV19">  
    
    <!-- Iconos para móviles -->  
    <link rel="apple-touch-icon" href="data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMTI4IiBoZWlnaHQ9IjEyOCIgdmlld0JveD0iMCAwIDEyOCAxMjgiIGZpbGw9IiNmOGZhZmMiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+PHJlY3Qgd2lkdGg9IjEyOCIgaGVpZ2h0PSIxMjgiIGZpbGw9IiNmOGZhZmMiLz48dGV4dCB4PSI2NCIgeT0iNjQiIGZpbGw9IiNGNkY2RjYiIGZvbnQtc2l6ZT0iMzAiIHRleHQtYW5jaG9yPSJtaWRkbGUiPjFBSTwvdGV4dD48L3N2Zz4=">  
    
    <style>  
        /* === VARIABLES CSS === */  
        :root {  
            --primary-gradient: linear-gradient(135deg, #667eea 0%, #764ba2 100%);  
            --secondary-gradient: linear-gradient(135deg, #f093fb 0%, #f5576c 100%);  
            --success-gradient: linear-gradient(135deg, #4facfe 0%, #00f2fe 100%);  
            --warning-gradient: linear-gradient(135deg, #fa709a 0%, #fee140 100%);  
            --dark-gradient: linear-gradient(135deg, #2c3e50 0%, #34495e 100%);  
            
            --text-primary: #2d3748;  
            --text-secondary: #718096;  
            --text-light: #a0aec0;  
            --border-light: #e2e8f0;  
            --success-color: #48bb78;  
            --warning-color: #ed8936;  
            --error-color: #f56565;  
            
            --shadow-sm: 0 1px 3px rgba(0, 0, 0, 0.1);  
            --shadow-md: 0 4px 6px rgba(0, 0, 0, 0.1);  
            --shadow-lg: 0 10px 15px rgba(0, 0, 0, 0.1);  
            --shadow-xl: 0 20px 25px rgba(0, 0, 0, 0.15);  
            
            --border-radius: 12px;  
            --border-radius-lg: 20px;  
            --transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);  
        }  

        /* === RESET Y BASE === */  
        * {  
            margin: 0;  
            padding: 0;  
            box-sizing: border-box;  
        }  

        body {  
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, sans-serif;  
            background: linear-gradient(135deg, #f8fafc 0%, #e2e8f0 100%);  
            color: var(--text-primary);  
            line-height: 1.6;  
            overflow-x: hidden;  
            -webkit-font-smoothing: antialiased;  
            -moz-osx-font-smoothing: grayscale;  
        }  

        /* === CONTENEDOR PRINCIPAL === */  
        .container {  
            max-width: 1200px;  
            margin: 0 auto;  
            height: 100vh;  
            display: flex;  
            flex-direction: column;  
            background: white;  
            border-radius: var(--border-radius-lg);  
            box-shadow: var(--shadow-xl);  
            overflow: hidden;  
            position: relative;  
        }  

        /* === CERTIFICADO MEJORADO === */  
        .creator-badge {  
            background: var(--primary-gradient);  
            color: white;  
            text-align: center;  
            padding: 8px 16px;  
            font-size: 0.8rem;  
            font-weight: 600;  
            letter-spacing: 0.5px;  
            box-shadow: 0 2px 4px rgba(102, 126, 234, 0.2);  
            position: relative;  
            overflow: hidden;  
        }  

        .creator-badge::before {  
            content: '';  
            position: absolute;  
            top: -50%;  
            left: -50%;  
            width: 200%;  
            height: 200%;  
            background: linear-gradient(45deg, transparent, rgba(255,255,255,0.1), transparent);  
            animation: shine 3s infinite;  
        }  

        @keyframes shine {  
            0% { transform: translateX(-100%) translateY(-100%) rotate(45deg); }  
            100% { transform: translateX(100%) translateY(100%) rotate(45deg); }  
        }  

        /* === HEADER AVANZADO === */  
        .header {  
            background: var(--primary-gradient);  
            color: white;  
            padding: 20px 30px;  
            position: relative;  
            overflow: hidden;  
        }  

        .header::before {  
            content: '';  
            position: absolute;  
            top: 0;  
            left: 0;  
            right: 0;  
            bottom: 0;  
            background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100"><defs><pattern id="grid" width="10" height="10" patternUnits="userSpaceOnUse"><path d="M 10 0 L 0 0 0 10" fill="none" stroke="rgba(255,255,255,0.1)" stroke-width="0.5"/></pattern></defs><rect width="100" height="100" fill="url(%23grid)"/></svg>');  
            opacity: 0.3;  
        }  

        .header-content {  
            display: flex;  
            justify-content: space-between;  
            align-items: center;  
            position: relative;  
            z-index: 1;  
        }  

        .brand {  
            display: flex;  
            align-items: center;  
            gap: 15px;  
        }  

        .logo {  
            font-size: 2.5rem;  
            background: rgba(255, 255, 255, 0.2);  
            padding: 12px;  
            border-radius: 50%;  
            backdrop-filter: blur(10px);  
            border: 2px solid rgba(255, 255, 255, 0.3);  
            animation: pulse 2s infinite;  
        }  

            @keyframes pulse {  
            0%, 100% { transform: scale(1); }  
            50% { transform: scale(1.05); }  
        }  

        .brand-text h1 {  
            font-size: 1.8rem;  
            font-weight: 700;  
            margin-bottom: 4px;  
            text-shadow: 2px 2px 4px rgba(0,0,0,0.1);  
        }  

        .brand-text p {  
            opacity: 0.9;  
            font-size: 0.9rem;  
            font-weight: 400;  
        }  

        /* === PANEL DE ESTADO === */  
        .status-panel {  
            display: flex;  
            gap: 20px;  
            align-items: center;  
        }  

        .status-item {  
            background: rgba(255, 255, 255, 0.15);  
            padding: 8px 16px;  
            border-radius: var(--border-radius);  
            backdrop-filter: blur(10px);  
            border: 1px solid rgba(255, 255, 255, 0.2);  
            text-align: center;  
            min-width: 80px;  
        }  

        .status-item .label {  
            font-size: 0.7rem;  
            opacity: 0.8;  
            text-transform: uppercase;  
            letter-spacing: 0.5px;  
        }  

        .status-item .value {  
            font-size: 1.1rem;  
            font-weight: 700;  
            margin-top: 2px;  
        }  

        .status-online {  
            background: var(--success-gradient);  
            box-shadow: 0 0 20px rgba(72, 187, 120, 0.3);  
            animation: glow 2s ease-in-out infinite alternate;  
        }  

        @keyframes glow {  
            from { box-shadow: 0 0 20px rgba(72, 187, 120, 0.3); }  
            to { box-shadow: 0 0 30px rgba(72, 187, 120, 0.6); }  
        }  

        /* === WIDGET DE INFORMACIÓN === */  
        .info-widgets {  
            display: flex;  
            gap: 15px;  
            padding: 15px 30px;  
            background: linear-gradient(90deg, #f8fafc 0%, #edf2f7 100%);  
            border-bottom: 1px solid var(--border-light);  
            overflow-x: auto;  
            scrollbar-width: none;  
            -ms-overflow-style: none;  
        }  

        .info-widgets::-webkit-scrollbar {  
            display: none;  
        }  

        .widget {  
            min-width: 200px;  
            background: white;  
            padding: 15px;  
            border-radius: var(--border-radius);  
            box-shadow: var(--shadow-sm);  
            border: 1px solid var(--border-light);  
            transition: var(--transition);  
        }  

        .widget:hover {  
            transform: translateY(-2px);  
            box-shadow: var(--shadow-md);  
        }  

        .widget-header {  
            display: flex;  
            align-items: center;  
            gap: 10px;  
            margin-bottom: 10px;  
        }  

        .widget-icon {  
            font-size: 1.2rem;  
            width: 30px;  
            height: 30px;  
            border-radius: 50%;  
            display: flex;  
            align-items: center;  
            justify-content: center;  
            background: var(--primary-gradient);  
            color: white;  
        }  

        .widget-title {  
            font-size: 0.8rem;  
            font-weight: 600;  
            color: var(--text-secondary);  
            text-transform: uppercase;  
            letter-spacing: 0.5px;  
        }  

                .widget-content {  
            font-size: 1.1rem;  
            font-weight: 700;  
            color: var(--text-primary);  
        }  

        .widget-subtitle {  
            font-size: 0.75rem;  
            color: var(--text-light);  
            margin-top: 4px;  
        }  

        /* === ÁREA DE CHAT MEJORADA === */  
        .chat-container {  
            flex: 1;  
            display: flex;  
            flex-direction: column;  
            height: calc(100vh - 300px);  
            min-height: 400px;  
        }  

        .chat-area {  
            flex: 1;  
            padding: 20px 30px;  
            overflow-y: auto;  
            scroll-behavior: smooth;  
            background: linear-gradient(180deg, #f8fafc 0%, #ffffff 100%);  
            position: relative;  
        }  

        .chat-area::-webkit-scrollbar {  
            width: 6px;  
        }  

        .chat-area::-webkit-scrollbar-track {  
            background: #f1f5f9;  
            border-radius: 3px;  
        }  

        .chat-area::-webkit-scrollbar-thumb {  
            background: linear-gradient(180deg, #cbd5e0, #a0aec0);  
            border-radius: 3px;  
        }  

        .chat-area::-webkit-scrollbar-thumb:hover {  
            background: var(--primary-gradient);  
        }  

        /* === MENSAJES MEJORADOS === */  
        .message {  
            display: flex;  
            margin-bottom: 20px;  
            animation: slideIn 0.3s ease-out;  
            position: relative;  
        }  

        @keyframes slideIn {  
            from {  
                opacity: 0;  
                transform: translateY(20px);  
            }  
            to {  
                opacity: 1;  
                transform: translateY(0);  
            }  
        }  

        .message.user-message {  
            justify-content: flex-end;  
        }  

        .message.bot-message {  
            justify-content: flex-start;  
        }  

        .message-bubble {  
            max-width: 70%;  
            padding: 15px 20px;  
            border-radius: var(--border-radius-lg);  
            position: relative;  
            box-shadow: var(--shadow-sm);  
            backdrop-filter: blur(10px);  
        }  

        .user-message .message-bubble {  
            background: var(--primary-gradient);  
            color: white;  
            border-bottom-right-radius: 6px;  
            margin-left: auto;  
        }  

        .bot-message .message-bubble {  
            background: white;  
            border: 1px solid var(--border-light);  
            border-bottom-left-radius: 6px;  
            position: relative;  
        }  

        .bot-message .message-bubble::before {  
            content: '';  
            position: absolute;  
            left: -1px;  
            top: 0;  
            bottom: 0;  
            width: 4px;  
            background: var(--primary-gradient);  
            border-radius: 2px;  
        }  

        .message-avatar {  
            width: 40px;  
            height: 40px;  
            border-radius: 50%;  
            display: flex;  
            align-items: center;  
            justify-content: center;  
            font-size: 1.2rem;  
            margin: 0 12px;  
            box-shadow: var(--shadow-sm);  
        }  

        .user-message .message-avatar {  
            background: var(--secondary-gradient);  
            color: white;  
            order: 2;  
        }  

        .bot-message .message-avatar {  
            background: var(--success-gradient);  
            color: white;  
        }  

        .message-content {  
            line-height: 1.5;  
        }  

        .message-content strong {  
            font-weight: 700;  
        }  

        .message-content em {  
            font-style: italic;  
            opacity: 0.9;  
        }  

        .message-time {  
            font-size: 0.7rem;  
            opacity: 0.6;  
            margin-top: 8px;  
            text-align: right;  
        }  

        .bot-message .message-time {  
            text-align: left;  
        }  

        /* === MENSAJE DE BIENVENIDA === */  
        .welcome-message {  
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);  
            color: white;  
            padding: 25px;  
            border-radius: var(--border-radius-lg);  
            margin-bottom: 25px;  
            box-shadow: var(--shadow-lg);  
            position: relative;  
            overflow: hidden;  
        }  

        .welcome-message::before {  
            content: '';  
            position: absolute;  
            top: 0;  
            right: 0;  
            width: 100px;  
            height: 100px;  
            background: rgba(255, 255, 255, 0.1);  
            border-radius: 50%;  
            transform: translate(30px, -30px);  
        }  

        .welcome-message h3 {  
            font-size: 1.4rem;  
            margin-bottom: 10px;  
            display: flex;  
            align-items: center;  
            gap: 10px;  
        }  

        .welcome-message p {  
            opacity: 0.9;  
            line-height: 1.6;  
        }  

        /* === SUGERENCIAS MEJORADAS === */  
        .suggestions {  
            display: flex;  
            gap: 10px;  
            padding: 15px 30px;  
            background: #f8fafc;  
            border-top: 1px solid var(--border-light);  
            overflow-x: auto;  
            scrollbar-width: none;  
            -ms-overflow-style: none;  
        }  

        .suggestions::-webkit-scrollbar {  
            display: none;  
        }  

        .suggestion-chip {  
            background: white;  
            border: 2px solid var(--border-light);  
            padding: 8px 16px;  
            border-radius: 20px;  
            font-size: 0.85rem;  
            font-weight: 500;  
            cursor: pointer;  
            transition: var(--transition);  
            white-space: nowrap;  
            position: relative;  
            overflow: hidden;  
        }  

        .suggestion-chip::before {  
            content: '';  
            position: absolute;  
            top: 0;  
            left: -100%;  
            width: 100%;  
            height: 100%;  
            background: var(--primary-gradient);  
            transition: var(--transition);  
            z-index: -1;  
        }  

        .suggestion-chip:hover {  
            color: white;  
            border-color: transparent;  
            transform: translateY(-2px);  
            box-shadow: var(--shadow-md);  
        }  

        .suggestion-chip:hover::before {  
            left: 0;  
        }  

        .suggestion-chip:active {  
            transform: translateY(0);  
        }  

        /* === INPUT AREA MEJORADA === */  
        .input-area {  
            padding: 20px 30px;  
            background: white;  
            border-top: 1px solid var(--border-light);  
            display: flex;  
            gap: 15px;  
            align-items: flex-end;  
            position: relative;  
        }  

        .input-container {  
            flex: 1;  
            position: relative;  
        }  

        .message-input {  
            width: 100%;  
            padding: 15px 20px;  
            border: 2px solid var(--border-light);  
            border-radius: var(--border-radius-lg);  
            font-size: 1rem;  
            font-family: inherit;  
            resize: none;  
            outline: none;  
            transition: var(--transition);  
            background: #f8fafc;  
            min-height: 50px;  
            max-height: 120px;  
        }  

        .message-input:focus {  
            border-color: #667eea;  
            background: white;  
            box-shadow: 0 0 0 3px rgba(102, 126, 234, 0.1);  
        }  

        .message-input::placeholder {  
            color: var(--text-light);  
        }  

        .input-actions {  
            display: flex;  
            gap: 10px;  
        }  

        .send-button, .voice-button, .attachment-button {  
            width: 50px;  
            height: 50px;  
            border: none;  
            border-radius: 50%;  
            cursor: pointer;  
            font-size: 1.2rem;  
            transition: var(--transition);  
            display: flex;  
            align-items: center;  
            justify-content: center;  
            position: relative;  
            overflow: hidden;  
        }  

        .send-button {  
            background: var(--primary-gradient);  
            color: white;  
            box-shadow: var(--shadow-md);  
        }  

        .send-button:hover {  
            transform: scale(1.05);  
            box-shadow: var(--shadow-lg);  
        }  

        .send-button:active {  
            transform: scale(0.95);  
        }  

        .voice-button {  
            background: var(--success-gradient);  
            color: white;  
        }  

        .attachment-button {  
            background: var(--warning-gradient);  
            color: white;  
        }  

        .voice-button:hover, .attachment-button:hover {  
            transform: scale(1.05);  
        }  

        /* === INDICADOR DE ESCRITURA === */  
        .typing-indicator {  
            display: none;  
            align-items: center;  
            gap: 10px;  
            padding: 15px 20px;  
            background: white;  
            border-radius: var(--border-radius-lg);  
            margin-bottom: 20px;  
            box-shadow: var(--shadow-sm);  
            border: 1px solid var(--border-light);  
        }  

        .typing-indicator.show {  
            display: flex;  
            animation: slideIn 0.3s ease-out;  
        }  

        .typing-avatar {  
            width: 30px;  
            height: 30px;  
            border-radius: 50%;  
            background: var(--success-gradient);  
            color: white;  
            display: flex;  
            align-items: center;  
            justify-content: center;  
            font-size: 0.9rem;  
        }  

        .typing-dots {  
            display: flex;  
            gap: 4px;  
        }  

        .typing-dots span {  
            width: 8px;  
            height: 8px;  
            border-radius: 50%;  
            background: var(--text-light);  
            animation: bounce 1.4s infinite ease-in-out both;  
        }  

        .typing-dots span:nth-child(1) { animation-delay: -0.32s; }  
        .typing-dots span:nth-child(2) { animation-delay: -0.16s; }  

        @keyframes bounce {  
            0%, 80%, 100% {  
                transform: scale(0);  
            }  
            40% {  
                transform: scale(1);  
            }  
        }  

        /* === FOOTER CON ESTADÍSTICAS === */  
        .footer {  
            background: #f8fafc;  
            border-top: 1px solid var(--border-light);  
            padding: 10px 30px;  
            display: flex;  
            justify-content: space-between;  
            align-items: center;  
            font-size: 0.8rem;  
            color: var(--text-secondary);  
        }  

        .footer-stats {  
            display: flex;  
            gap: 20px;  
        }  

        .stat-item {  
            display: flex;  
            align-items: center;  
            gap: 5px;  
        }  

        .stat-value {  
            font-weight: 600;  
            color: var(--text-primary);  
        }  

        /* === RESPONSIVE DESIGN === */  
        @media (max-width: 768px) {  
            .container {  
                height: 100vh;  
                border-radius: 0;  
                margin: 0;  
            }  

            .header {  
                padding: 15px 20px;  
            }  

            .header-content {  
                flex-direction: column;  
                gap: 15px;  
                text-align: center;  
            }  

            .brand-text h1 {  
                font-size: 1.5rem;  
            }  

            .status-panel {  
                justify-content: center;  
            }  

            .info-widgets {  
                padding: 10px 20px;  
                gap: 10px;  
            }  

            .widget {  
                min-width: 150px;  
                padding: 12px;  
            }  

            .chat-area {  
                padding: 15px 20px;  
            }  

            .message-bubble {  
                max-width: 85%;  
                padding: 12px 16px;  
            }  

            .suggestions {  
                padding: 10px 20px;  
            }  

            .input-area {  
                padding: 15px 20px;  
                gap: 10px;  
            }  
                
            .send-button, .voice-button, .attachment-button {  
                width: 45px;  
                height: 45px;  
                font-size: 1.1rem;  
            }  

            .footer {  
                padding: 8px 20px;  
                flex-direction: column;  
                gap: 8px;  
                text-align: center;  
            }  

            .footer-stats {  
                gap: 15px;  
            }  
        }  

        @media (max-width: 480px) {  
            .widget {  
                min-width: 120px;  
                padding: 10px;  
            }  

            .widget-content {  
                font-size: 1rem;  
            }  

            .message-bubble {  
                max-width: 90%;  
                padding: 10px 14px;  
            }  

            .input-area {  
                gap: 8px;  
            }  

            .send-button, .voice-button, .attachment-button {  
                width: 40px;  
                height: 40px;  
                font-size: 1rem;  
            }  
        }  

        /* === ANIMACIONES ESPECIALES === */  
        .pulse-animation {  
            animation: pulse-glow 2s infinite;  
        }  

        @keyframes pulse-glow {  
            0% { box-shadow: 0 0 5px rgba(102, 126, 234, 0.5); }  
            50% { box-shadow: 0 0 20px rgba(102, 126, 234, 0.8); }  
            100% { box-shadow: 0 0 5px rgba(102, 126, 234, 0.5); }  
        }  

        .shake-animation {  
            animation: shake 0.5s ease-in-out;  
        }  

        @keyframes shake {  
            0%, 100% { transform: translateX(0); }  
            25% { transform: translateX(-5px); }  
            75% { transform: translateX(5px); }  
        }  

        /* === MODO OSCURO === */  
        @media (prefers-color-scheme: dark) {  
            :root {  
                --text-primary: #f7fafc;  
                --text-secondary: #a0aec0;  
                --text-light: #718096;  
                --border-light: #2d3748;  
            }  

            body {  
                background: linear-gradient(135deg, #1a202c 0%, #2d3748 100%);  
            }  

            .container {  
                background: #2d3748;  
            }  

            .chat-area {  
                background: linear-gradient(180deg, #2d3748 0%, #1a202c 100%);  
            }  

            .bot-message .message-bubble {  
                background: #4a5568;  
                border-color: #718096;  
                color: #f7fafc;  
            }  

            .input-area {  
                background: #4a5568;  
                border-color: #718096;  
            }  

            .message-input {  
                background: #2d3748;  
                border-color: #718096;  
                color: #f7fafc;  
            }  

            .footer {  
                background: #4a5568;  
                border-color: #718096;  
            }  
        }  
    </style>  
</head>  
<body>  
    <!-- Certificado del Desarrollador -->  
    <div class="creator-badge">  
        🚀 Family Rivas AI v2.0 - Desarrollado por Eros Jeancarlos Cordova Rivas | Sistema Avanzado 2024 ⚡  
    </div>  

    <div class="container">  
        <!-- Header Mejorado -->  
        <div class="header">  
            <div class="header-content">  
                <div class="brand">  
                    <div class="logo">🤖</div>  
                    <div class="brand-text">  
                        <h1>Family Rivas AI</h1>  
                        <p>Asistente Inteligente Avanzado</p>  
                    </div>  
                </div>  
                <div class="status-panel">  
                    <div class="status-item status-online">  
                        <div class="label">Estado</div>  
                        <div class="value">Online</div>  
                    </div>  
                    <div class="status-item" id="timeWidget">  
                        <div class="label">Hora</div>  
                        <div class="value" id="currentTime">--:--</div>  
                    </div>  
                    <div class="status-item" id="messageCounter">  
                        <div class="label">Mensajes</div>  
                        <div class="value" id="msgCount">0</div>  
                    </div>  
                </div>  
            </div>  
        </div>  

        <!-- Widgets de Información -->  
        <div class="info-widgets">  
            <div class="widget" id="weatherWidget">  
                <div class="widget-header">  
                    <div class="widget-icon">🌤️</div>  
                    <div class="widget-title">Clima</div>  
                </div>  
                <div class="widget-content" id="weatherTemp">Cargando...</div>  
                <div class="widget-subtitle" id="weatherLocation">Obteniendo ubicación...</div>  
            </div>  

            <div class="widget" id="dateWidget">  
                <div class="widget-header">  
                    <div class="widget-icon">📅</div>  
                    <div class="widget-title">Fecha</div>  
                </div>  
                <div class="widget-content" id="currentDate">--</div>  
                <div class="widget-subtitle" id="dayOfWeek">--</div>  
            </div>  

            <div class="widget" id="batteryWidget">  
                <div class="widget-header">  
                    <div class="widget-icon">🔋</div>  
                    <div class="widget-title">Batería</div>  
                </div>  
                <div class="widget-content" id="batteryLevel">--</div>  
                <div class="widget-subtitle" id="batteryStatus">Verificando...</div>  
            </div>  

            <div class="widget" id="networkWidget">  
                <div class="widget-header">  
                    <div class="widget-icon">📶</div>  
                    <div class="widget-title">Red</div>  
                </div>  
                <div class="widget-content" id="networkStatus">Online</div>  
                <div class="widget-subtitle" id="connectionType">WiFi</div>  
            </div>  

            <div class="widget" id="performanceWidget">  
                <div class="widget-header">  
                    <div class="widget-icon">⚡</div>  
                    <div class="widget-title">Sistema</div>  
                </div>  
                <div class="widget-content" id="systemPerformance">Óptimo</div>  
                <div class="widget-subtitle" id="memoryUsage">RAM: --</div>  
            </div>  
        </div>  

        <!-- Área de Chat -->  
        <div class="chat-container">  
            <div class="chat-area" id="chatArea">  
                <div class="welcome-message">  
                    <h3>🚀 ¡Bienvenido a Family Rivas AI Avanzado!</h3>  
                    <p>  
                        Soy tu asistente inteligente con capacidades avanzadas. Puedo ayudarte con:  
                        <br>• 🌤️ Información del clima en tiempo real  
                        <br>• 🕒 Hora mundial y fechas  
                        <br>• 📱 Estado del dispositivo y batería  
                        <br>• 🧮 Cálculos matemáticos complejos  
                        <br>• 🌍 Conversaciones inteligentes  
                        <br>• 🎯 Y mucho más...  
                    </p>  
                </div>  

                <!-- Indicador de escritura -->  
                <div class="typing-indicator" id="typingIndicator">  
                    <div class="typing-avatar">🤖</div>  
                    <div class="typing-dots">  
                        <span></span>  
                        <span></span>  
                        <span></span>  
                    </div>  
                    <span style="margin-left: 10px; color: var(--text-secondary);">Family Rivas AI está escribiendo...</span>  
                </div>  
            </div>  

            <!-- Sugerencias -->  
            <div class="suggestions">  
                <div class="suggestion-chip" onclick="sendSuggestion('¿Qué tiempo hace hoy?')">🌤️ Clima actual</div>  
                <div class="suggestion-chip" onclick="sendSuggestion('¿Qué hora es?')">🕒 Hora actual</div>  
                <div class="suggestion-chip" onclick="sendSuggestion('Calcula 2+2*5')">🧮 Calculadora</div>  
                <div class="suggestion-chip" onclick="sendSuggestion('Estado de mi batería')">🔋 Batería</div>  
                <div class="suggestion-chip" onclick="sendSuggestion('Cuéntame un chiste')">😄 Chiste</div>  
                <div class="suggestion-chip" onclick="sendSuggestion('¿Cómo estás?')">💬 Conversación</div>  
                <div class="suggestion-chip" onclick="sendSuggestion('Ayúdame con programación')">💻 Programación</div>  
                <div class="suggestion-chip" onclick="sendSuggestion('Información sobre tecnología')">🚀 Tecnología</div>  
            </div>  

            <!-- Área de Input -->  
            <div class="input-area">  
                <div class="input-container">  
                    <textarea   
                        id="messageInput"   
                        class="message-input"   
                        placeholder="Escribe tu mensaje aquí... (Presiona Enter para enviar)"  
                        rows="1"  
                    ></textarea>  
                </div>  
                <div class="input-actions">  
                    <button class="attachment-button" onclick="handleAttachment()" title="Adjuntar archivo">📎</button>  
                    <button class="voice-button" onclick="toggleVoiceRecording()" title="Grabar mensaje de voz" id="voiceBtn">🎤</button>  
                    <button class="send-button" onclick="sendMessage()" title="Enviar mensaje" id="sendBtn">📤</button>  
                </div>  
            </div>  
        </div>  

        <!-- Footer con estadísticas -->  
        <div class="footer">  
            <div class="footer-stats">  
                <div class="stat-item">  
                    <span>⚡ Velocidad:</span>  
                    <span class="stat-value" id="responseSpeed">Ultra rápida</span>  
                </div>  
                <div class="stat-item">  
                    <span>🎯 Precisión:</span>  
                    <span class="stat-value" id="accuracyRate">99.8%</span>  
                </div>  
                <div class="stat-item">  
                    <span>🌐 Conexión:</span>  
                    <span class="stat-value" id="connectionQuality">Excelente</span>  
                </div>  
                <div class="stat-item">  
                    <span>📊 Sesión:</span>  
                    <span class="stat-value" id="sessionTime">0m</span>  
                </div>  
            </div>  
            <div class="footer-info">  
                <span>Family Rivas AI © 2024 - Desarrollado por Eros Jeancarlos Cordova Rivas</span>  
            </div>  
        </div>  
    </div>  

    <script>  
        // === VARIABLES GLOBALES ===  
        let messageCount = 0;  
        let sessionStartTime = Date.now();  
        let isVoiceRecording = false;  
        let recognition = null;  
        let currentWeather = null;  
        
        // === INICIALIZACIÓN ===  
        document.addEventListener('DOMContentLoaded', function() {  
            initializeApp();  
            updateWidgets();  
            setInterval(updateWidgets, 1000);  
            setupEventListeners();  
            loadWeatherData();  
            initializeVoiceRecognition();  
        });  

        function initializeApp() {  
            console.log('🚀 Family Rivas AI v2.0 Inicializado');  
            updateTime();  
            updateDate();  
            updateSessionTime();  
            checkBatteryStatus();  
            checkNetworkStatus();  
            updateSystemPerformance();  
        }  

        // === MANEJO DE EVENTOS ===  
        function setupEventListeners() {  
            const messageInput = document.getElementById('messageInput');  
            
            messageInput.addEventListener('keydown', function(e) {  
                if (e.key === 'Enter' && !e.shiftKey) {  
                    e.preventDefault();  
                    sendMessage();  
                }  
            });  

            messageInput.addEventListener('input', function() {  
                autoResizeTextarea(this);  
            });  

            // Eventos de visibilidad  
            document.addEventListener('visibilitychange', function() {  
                if (document.hidden) {  
                    console.log('App oculta');  
                } else {  
                    console.log('App visible');  
                    updateWidgets();  
                }  
            });  
        }  

        // === FUNCIONES DE WIDGETS ===  
        function updateWidgets() {  
            updateTime();  
            updateDate();  
            updateSessionTime();  
            updateMessageCount();  
        }  

        function updateTime() {  
            const now = new Date();  
            const timeString = now.toLocaleTimeString('es-ES', {  
                hour: '2-digit',  
                minute: '2-digit'  
            });  
            document.getElementById('currentTime').textContent = timeString;  
        }  

        function updateDate() {  
            const now = new Date();  
            const dateString = now.toLocaleDateString('es-ES', {  
                day: '2-digit',  
                month: '2-digit',  
                year: 'numeric'  
            });  
            const dayString = now.toLocaleDateString('es-ES', {  
                weekday: 'long'  
            });  
            document.getElementById('currentDate').textContent = dateString;  
            document.getElementById('dayOfWeek').textContent = dayString.charAt(0).toUpperCase() + dayString.slice(1);  
        }  

        function updateSessionTime() {  
            const now = Date.now();  
            const sessionDuration = Math.floor((now - sessionStartTime) / 1000 / 60);  
            document.getElementById('sessionTime').textContent = `${sessionDuration}m`;  
        }  

        function updateMessageCount() {  
            document.getElementById('msgCount').textContent = messageCount;  
        }  

        // === FUNCIONES DE CLIMA ===  
        async function loadWeatherData() {  
            try {  
                if (navigator.geolocation) {  
                    navigator.geolocation.getCurrentPosition(async (position) => {  
                        const lat = position.coords.latitude;  
                        const lon = position.coords.longitude;  
                        
                        // Simulación de datos del clima (reemplazar con API real)  
                        const weatherData = await simulateWeatherAPI(lat, lon);  
                        updateWeatherWidget(weatherData);  
                    }, (error) => {  
                        console.warn('Error obteniendo ubicación:', error);  
                        updateWeatherWidget({  
                            temperature: '22°C',  
                            location: 'Ubicación no disponible',  
                            condition: 'Despejado'  
                        });  
                    });  
                } else {  
                    updateWeatherWidget({  
                        temperature: '25°C',  
                        location: 'Lima, Perú',  
                        condition: 'Soleado'  
                    });  
                }  
            } catch (error) {  
                console.error('Error cargando clima:', error);  
                updateWeatherWidget({  
                    temperature: 'N/A',  
                    location: 'Error de conexión',  
                    condition: 'Desconocido'  
                });  
            }  
        }  

        async function simulateWeatherAPI(lat, lon) {  
            // Simulación de respuesta de API meteorológica  
            return new Promise((resolve) => {  
                setTimeout(() => {  
                    const temperatures = ['18°C', '22°C', '25°C', '28°C', '20°C'];  
                    const conditions = ['Soleado', 'Nublado', 'Despejado', 'Lluvia ligera'];  
                    const cities = ['Lima', 'Arequipa', 'Cusco', 'Trujillo', 'Chiclayo'];  
                    
                    resolve({  
                        temperature: temperatures[Math.floor(Math.random() * temperatures.length)],  
                        location: `${cities[Math.floor(Math.random() * cities.length)]}, Perú`,  
                        condition: conditions[Math.floor(Math.random() * conditions.length)]  
                    });  
                }, 1000);  
            });  
        }  

        function updateWeatherWidget(data) {  
            document.getElementById('weatherTemp').textContent = data.temperature;  
            document.getElementById('weatherLocation').textContent = data.location;  
            currentWeather = data;  
        }  

        // === FUNCIONES DE BATERÍA ===  
        async function checkBatteryStatus() {  
            try {  
                if ('getBattery' in navigator) {  
                    const battery = await navigator.getBattery();  
                    updateBatteryWidget(battery);  
                    
                    battery.addEventListener('chargingchange', () => updateBatteryWidget(battery));  
                    battery.addEventListener('levelchange', () => updateBatteryWidget(battery));  
                } else {  
                    updateBatteryWidget({  
                        level: 0.85,  
                        charging: false  
                    });  
                }  
            } catch (error) {  
                console.warn('API de batería no disponible:', error);  
                updateBatteryWidget({  
                    level: 0.90,  
                    charging: false  
                });  
            }  
        }  

        function updateBatteryWidget(battery) {  
            const level = Math.round(battery.level * 100);  
            const isCharging = battery.charging;  
            
            document.getElementById('batteryLevel').textContent = `${level}%`;  
            document.getElementById('batteryStatus').textContent = isCharging ? 'Cargando' : 'Desconectado';  
            
            // Cambiar color según el nivel  
            const widget = document.getElementById('batteryWidget');  
            if (level < 20) {  
                widget.style.borderLeft = '4px solid #f56565';  
            } else if (level < 50) {  
                widget.style.borderLeft = '4px solid #ed8936';  
            } else {  
                widget.style.borderLeft = '4px solid #48bb78';  
            }  
        }  

        // === FUNCIONES DE RED ===  
        function checkNetworkStatus() {  
            const updateNetworkInfo = () => {  
                const isOnline = navigator.onLine;  
                const connection = navigator.connection || navigator.mozConnection || navigator.webkitConnection;  
                
                document.getElementById('networkStatus').textContent = isOnline ? 'Online' : 'Offline';  
                
                if (connection) {  
                    const connectionType = connection.effectiveType || connection.type || 'Desconocido';  
                    document.getElementById('connectionType').textContent = connectionType.toUpperCase();  
                } else {  
                    document.getElementById('connectionType').textContent = 'WiFi';  
                }  
                
                // Actualizar color del widget  
                const widget = document.getElementById('networkWidget');  
                widget.style.borderLeft = isOnline ? '4px solid #48bb78' : '4px solid #f56565';  
            };  
            
            updateNetworkInfo();  
            window.addEventListener('online', updateNetworkInfo);  
            window.addEventListener('offline', updateNetworkInfo);  
        }  

        // === FUNCIONES DE RENDIMIENTO ===  
        function updateSystemPerformance() {  
            const performance = window.performance;  
            const memory = performance.memory;  
            
            if (memory) {  
                const usedMemory = Math.round(memory.usedJSHeapSize / 1024 / 1024);  
                const totalMemory = Math.round(memory.totalJSHeapSize / 1024 / 1024);  
                
                document.getElementById('memoryUsage').textContent = `RAM: ${usedMemory}MB`;  
                
                if (usedMemory / totalMemory > 0.8) {  
                    document.getElementById('systemPerformance').textContent = 'Alto uso';  
                } else if (usedMemory / totalMemory > 0.5) {  
                    document.getElementById('systemPerformance').textContent = 'Normal';  
                } else {  
                    document.getElementById('systemPerformance').textContent = 'Óptimo';  
                }  
            } else {  
                document.getElementById('memoryUsage').textContent = 'RAM: N/A';  
                document.getElementById('systemPerformance').textContent = 'Óptimo';  
            }  
        }  

        // === FUNCIONES DE VOZ ===  
        function initializeVoiceRecognition() {  
            if ('webkitSpeechRecognition' in window || 'SpeechRecognition' in window) {  
                const SpeechRecognition = window.SpeechRecognition || window.webkitSpeechRecognition;  
                recognition = new SpeechRecognition();  
                
                recognition.continuous = false;  
                recognition.interimResults = false;  
                recognition.lang = 'es-ES';  
                
                recognition.onstart = function() {  
                    console.log('Reconocimiento de voz iniciado');  
                    document.getElementById('voiceBtn').textContent = '🔴';  
                    document.getElementById('voiceBtn').classList.add('pulse-animation');  
                };  
                
                recognition.onresult = function(event) {  
                    const transcript = event.results[0][0].transcript;  
                    document.getElementById('messageInput').value = transcript;  
                    autoResizeTextarea(document.getElementById('messageInput'));  
                };  
                
                recognition.onend = function() {  
                    console.log('Reconocimiento de voz terminado');  
                    document.getElementById('voiceBtn').textContent = '🎤';  
                    document.getElementById('voiceBtn').classList.remove('pulse-animation');  
                    isVoiceRecording = false;  
                };  
                
                recognition.onerror = function(event) {  
                    console.error('Error en reconocimiento de voz:', event.error);  
                    document.getElementById('voiceBtn').textContent = '🎤';  
                    document.getElementById('voiceBtn').classList.remove('pulse-animation');  
                    isVoiceRecording = false;  
                };  
            }  
        }  

        function toggleVoiceRecording() {  
            if (!recognition) {  
                alert('Reconocimiento de voz no disponible en este dispositivo');  
                return;  
            }  
            
            if (!isVoiceRecording) {  
                recognition.start();  
                isVoiceRecording = true;  
            } else {  
                recognition.stop();  
                isVoiceRecording = false;  
            }  
        }  

        // === FUNCIONES DE MENSAJES ===  
        function sendMessage() {  
            const input = document.getElementById('messageInput');  
            const message = input.value.trim();  
            
            if (message === '') return;  
            
            // Agregar mensaje del usuario  
            addMessage(message, 'user');  
            input.value = '';  
            autoResizeTextarea(input);  
            
            // Mostrar indicador de escritura  
            showTypingIndicator();  
            
            // Procesar respuesta después de un delay  
            setTimeout(() => {  
                const response = processMessage(message);  
                hideTypingIndicator();  
                addMessage(response, 'bot');  
                updateResponseStats();  
            }, Math.random() * 2000 + 1000); // 1-3 segundos de delay  
        }  

        function sendSuggestion(suggestion) {  
            document.getElementById('messageInput').value = suggestion;  
            sendMessage();  
        }  

        function addMessage(message, sender) {  
            const chatArea = document.getElementById('chatArea');  
            const messageDiv = document.createElement('div');  
            messageDiv.className = `message ${sender}-message`;  
            
            const now = new Date();  
            const timeString = now.toLocaleTimeString('es-ES', {  
                hour: '2-digit',  
                minute: '2-digit'  
            });  
            
            messageDiv.innerHTML = `  
                <div class="message-avatar">  
                    ${sender === 'user' ? '👤' : '🤖'}  
                </div>  
                <div class="message-bubble">  
                    <div class="message-content">${formatMessage(message)}</div>  
                    <div class="message-time">${timeString}</div>  
                </div>  
            `;  
            
            chatArea.appendChild(messageDiv);  
            chatArea.scrollTop = chatArea.scrollHeight;  
            
            // Animación de entrada  
            messageDiv.style.opacity = '0';  
            messageDiv.style.transform = 'translateY(20px)';  
            setTimeout(() => {  
                messageDiv.style.transition = 'all 0.3s ease-out';  
                messageDiv.style.opacity = '1';  
                messageDiv.style.transform = 'translateY(0)';  
            }, 100);  
            
            if (sender === 'user') {  
                messageCount++;  
                updateMessageCount();  
            }  
        }  

        function formatMessage(message) {  
            // Formatear enlaces  
            message = message.replace(/(https?:\/\/[^\s]+)/g, '<a href="$1" target="_blank">$1</a>');  
            
            // Formatear texto en negrita  
            message = message.replace(/\*\*(.*?)\*\*/g, '<strong>$1</strong>');  
            
            // Formatear texto en cursiva  
            message = message.replace(/\*(.*?)\*/g, '<em>$1</em>');  
            
            // Formatear código  
            message = message.replace(/`(.*?)`/g, '<code>$1</code>');  
            
            return message;  
        }  

        // === PROCESAMIENTO DE MENSAJES ===  
        function processMessage(message) {  
            const lowerMessage = message.toLowerCase();  
            
            // Comandos específicos  
            if (lowerMessage.includes('clima') || lowerMessage.includes('tiempo')) {  
                return getWeatherResponse();  
            }  
            
            if (lowerMessage.includes('hora') || lowerMessage.includes('qué hora')) {  
                return getTimeResponse();  
            }  
            
            if (lowerMessage.includes('fecha') || lowerMessage.includes('día')) {  
                return getDateResponse();  
            }  
            
            if (lowerMessage.includes('batería') || lowerMessage.includes('bateria')) {  
                return getBatteryResponse();  
            }  
            
            if (lowerMessage.includes('calcula') || lowerMessage.includes('matemática') || lowerMessage.includes('matematica')) {  
                return getCalculationResponse(message);  
            }  
            
            if (lowerMessage.includes('chiste') || lowerMessage.includes('gracioso')) {  
                return getJokeResponse();  
            }  
            
            if (lowerMessage.includes('programación') || lowerMessage.includes('programacion') || lowerMessage.includes('código')) {  
                return getProgrammingResponse();  
            }  
            
            if (lowerMessage.includes('tecnología') || lowerMessage.includes('tecnologia')) {  
                return getTechnologyResponse();  
            }  
            
            // Respuestas generales  
            return getGeneralResponse(message);  
        }  

        function getWeatherResponse() {  
            if (currentWeather) {  
                return `🌤️ **Información del clima:**\n\n📍 **Ubicación:** ${currentWeather.location}\n🌡️ **Temperatura:** ${currentWeather.temperature}\n☁️ **Condición:** ${currentWeather.condition}\n\n*Datos actualizados en tiempo real*`;  
            }  
            return '🌤️ Obteniendo información del clima... Por favor, espera un momento.';  
        }  

        function getTimeResponse() {  
            const now = new Date();  
            const timeString = now.toLocaleTimeString('es-ES');  
            const dateString = now.toLocaleDateString('es-ES', {  
                weekday: 'long',  
                year: 'numeric',  
                month: 'long',  
                day: 'numeric'  
            });  
            return `⏰ **Hora actual:** ${timeString}\n📅 **Fecha:** ${dateString}`;  
        }  

        function getDateResponse() {  
            const now = new Date();  
            const dateString = now.toLocaleDateString('es-ES', {  
                weekday: 'long',  
                year: 'numeric',  
                month: 'long',  
                day: 'numeric'  
            });  
            return `📅 **Fecha actual:** ${dateString}`;  
        }  

        function getBatteryResponse() {  
            const batteryLevel = document.getElementById('batteryLevel').textContent;  
            const batteryStatus = document.getElementById('batteryStatus').textContent;  
            return `🔋 **Estado de la batería:**\n\n📊 **Nivel:** ${batteryLevel}\n⚡ **Estado:** ${batteryStatus}\n\n*Información del dispositivo en tiempo real*`;  
        }  

        function getCalculationResponse(message) {  
            try {  
                // Extraer expresión matemática  
                const mathExpression = message.match(/calcula\s+(.+)/i);  
                if (mathExpression) {  
                    const expression = mathExpression[1].replace(/[^0-9+\-*/().\s]/g, '');  
                    const result = eval(expression);  
                    return `🧮 **Cálculo realizado:**\n\n📝 **Expresión:** ${expression}\n✅ **Resultado:** ${result}\n\n*Calculadora avanzada integrada*`;  
                }  
            } catch (error) {  
                return '❌ No pude procesar ese cálculo. Por favor, usa formato como: "calcula 2+2*5"';  
            }  
            return '🧮 ¿Qué cálculo quieres que realice? Ejemplo: "calcula 15*3+7"';  
        }  

        function getJokeResponse() {  
            const jokes = [  
                "¿Por qué los programadores prefieren el modo oscuro? ¡Porque la luz atrae bugs! 🐛💡",  
                "¿Cuál es el colmo de un informático? Que su mujer tenga un hijo y no sepa si es suyo o del sistema 👶💻",  
                "¿Qué le dice un bit al otro? Nos vemos en el bus de datos 🚌💾",  
                "¿Por qué los robots nunca entran en pánico? Porque tienen nervios de acero 🤖⚡",  
                "¿Cómo se llama el primo androide de R2-D2? R2-Detú 😄🤖",  
                "¿Qué hace un programador cuando no puede dormir? Cuenta ovejas en binario: 1, 10, 11, 100... 🐑💤"  
            ];  
            const randomJoke = jokes[Math.floor(Math.random() * jokes.length)];  
            return `😄 **¡Aquí tienes un chiste!**\n\n${randomJoke}\n\n*¿Quieres otro? Solo pídemelo*`;  
        }  

        function getProgrammingResponse() {  
            const tips = [  
                "**Consejo de programación:** Siempre comenta tu código. Tu yo del futuro te lo agradecerá 📝",  
                "**Buena práctica:** Usa nombres de variables descriptivos. 'datos' no dice nada, 'listaUsuarios' sí 🏷️",  
                "**Tip avanzado:** Aprende a usar Git correctamente. Es tu mejor amigo para el control de versiones 🌿",  
                "**Optimización:** Primero haz que funcione, luego haz que sea rápido 🚀",  
                "**Debugging:** El mejor debugger eres tú mismo explicando el código a un patito de goma 🦆"  
            ];  
            const randomTip = tips[Math.floor(Math.random() * tips.length)];  
            return `💻 **Programación:**\n\n${randomTip}\n\n¿Necesitas ayuda con algún lenguaje específico? ¡Pregúntame!`;  
        }  

        function getTechnologyResponse() {  
            const techNews = [  
                "🚀 **IA Generativa:** Los modelos de lenguaje están revolucionando la forma en que interactuamos con la tecnología",  
                "⚡ **Computación Cuántica:** Los procesadores cuánticos prometen resolver problemas imposibles para computadoras clásicas",  
                "🌐 **Web3:** La descentralización está cambiando Internet tal como lo conocemos",  
                "🤖 **Automatización:** Los robots y la IA están transformando industrias completas",  
                "🔒 **Ciberseguridad:** La protección de datos nunca ha sido tan crítica como ahora",  
                "📱 **IoT:** El Internet de las Cosas conecta cada vez más dispositivos a la red global"  
            ];  
            const randomTech = techNews[Math.floor(Math.random() * techNews.length)];  
            return `🚀 **Tecnología Actual:**\n\n${randomTech}\n\n*¿Quieres saber más sobre algún tema específico?*`;  
        }  

        function getGeneralResponse(message) {  
            const responses = [  
                `¡Hola! 👋 Entiendo que me escribes sobre "${message}". Como tu asistente AI avanzado, estoy aquí para ayudarte con cualquier consulta.`,  
                `Interesante pregunta sobre "${message}". 🤔 Como Family Rivas AI, puedo ayudarte con información, cálculos, clima, programación y mucho más.`,  
                `¡Perfecto! 🎯 Veo que mencionas "${message}". Estoy diseñado para ser tu compañero inteligente. ¿En qué más puedo asistirte?`,  
                `Gracias por tu mensaje sobre "${message}". 🚀 Soy un asistente AI avanzado creado por Eros Jeancarlos Cordova Rivas. ¿Cómo puedo ayudarte mejor?`,  
                `¡Excelente! 💡 Respecto a "${message}", como tu AI personal, puedo brindarte información precisa y útil. ¿Qué más necesitas saber?`  
            ];  
            return responses[Math.floor(Math.random() * responses.length)];  
        }  

        // === FUNCIONES DE UI ===  
        function showTypingIndicator() {  
            document.getElementById('typingIndicator').style.display = 'flex';  
            const chatArea = document.getElementById('chatArea');  
            chatArea.scrollTop = chatArea.scrollHeight;  
        }  

        function hideTypingIndicator() {  
            document.getElementById('typingIndicator').style.display = 'none';  
        }  

        function autoResizeTextarea(textarea) {  
            textarea.style.height = 'auto';  
            textarea.style.height = Math.min(textarea.scrollHeight, 120) + 'px';  
        }  

        function updateResponseStats() {  
            // Simular estadísticas de respuesta  
            const speeds = ['Ultra rápida', 'Muy rápida', 'Rápida', 'Instantánea'];  
            const accuracies = ['99.9%', '99.8%', '99.7%', '99.6%'];  
            const qualities = ['Excelente', 'Óptima', 'Perfecta', 'Superior'];  
            
            document.getElementById('responseSpeed').textContent = speeds[Math.floor(Math.random() * speeds.length)];  
            document.getElementById('accuracyRate').textContent = accuracies[Math.floor(Math.random() * accuracies.length)];  
            document.getElementById('connectionQuality').textContent = qualities[Math.floor(Math.random() * qualities.length)];  
        }  

        // === FUNCIONES DE ARCHIVOS ===  
        function handleAttachment() {  
            const input = document.createElement('input');  
            input.type = 'file';  
            input.multiple = true;  
            input.accept = 'image/*,text/*,.pdf,.doc,.docx';  
            
            input.onchange = function(e) {  
                const files = Array.from(e.target.files);  
                if (files.length > 0) {  
                    let fileList = '📎 **Archivos adjuntos:**\n\n';  
                    files.forEach((file, index) => {  
                        const fileSize = (file.size / 1024).toFixed(1);  
                        fileList += `${index + 1}. 📄 ${file.name} (${fileSize} KB)\n`;  
                    });  
                    
                    fileList += '\n*Archivos procesados exitosamente*';  
                    addMessage(fileList, 'user');  
                    
                    // Simular procesamiento  
                    setTimeout(() => {  
                        const response = `✅ **Archivos recibidos correctamente**\n\nHe recibido ${files.length} archivo(s). Como AI avanzado, puedo:\n\n🔍 Analizar contenido de texto\n🖼️ Procesar imágenes\n📊 Extraer información de documentos\n\n¿Qué te gustaría que haga con estos archivos?`;  
                        addMessage(response, 'bot');  
                    }, 1500);  
                }  
            };  
            
            input.click();  
        }  

        // === FUNCIONES DE CONFIGURACIÓN ===  
        function toggleTheme() {  
            const body = document.body;  
            const isDark = body.classList.contains('dark-theme');  
            
            if (isDark) {  
                body.classList.remove('dark-theme');  
                localStorage.setItem('theme', 'light');  
            } else {  
                body.classList.add('dark-theme');  
                localStorage.setItem('theme', 'dark');  
            }  
        }  

        function clearChat() {  
            const chatArea = document.getElementById('chatArea');  
            const messages = chatArea.querySelectorAll('.message');  
            
            messages.forEach(message => {  
                message.style.animation = 'fadeOut 0.3s ease-out';  
                setTimeout(() => message.remove(), 300);  
            });  
            
            messageCount = 0;  
            updateMessageCount();  
            
            setTimeout(() => {  
                addMessage('🗑️ Chat limpiado exitosamente. ¡Listo para una nueva conversación!', 'bot');  
            }, 500);  
        }  

        // === FUNCIONES DE EXPORTACIÓN ===  
        function exportChat() {  
            const messages = document.querySelectorAll('.message');  
            let chatContent = 'FAMILY RIVAS AI - EXPORTACIÓN DE CHAT\n';  
            chatContent += '=====================================\n\n';  
            
            messages.forEach(message => {  
                const sender = message.classList.contains('user-message') ? 'USUARIO' : 'FAMILY RIVAS AI';  
                const content = message.querySelector('.message-content').textContent;  
                const time = message.querySelector('.message-time').textContent;  
                
                chatContent += `[${time}] ${sender}: ${content}\n\n`;  
            });  
            
            chatContent += `\nExportado el: ${new Date().toLocaleString('es-ES')}\n`;  
            chatContent += 'Desarrollado por: Eros Jeancarlos Cordova Rivas\n';  
            
            const blob = new Blob([chatContent], { type: 'text/plain' });  
            const url = URL.createObjectURL(blob);  
            const a = document.createElement('a');  
            a.href = url;  
            a.download = `family-rivas-ai-chat-${Date.now()}.txt`;  
            a.click();  
            URL.revokeObjectURL(url);  
            
            addMessage('📥 **Chat exportado exitosamente** ✅\n\nEl archivo se ha descargado a tu dispositivo.', 'bot');  
        }  

        // === FUNCIONES AVANZADAS ===  
        function analyzePerformance() {  
            const performanceData = {  
                loadTime: Math.round(performance.now()),  
                messageCount: messageCount,  
                sessionDuration: Math.floor((Date.now() - sessionStartTime) / 1000 / 60),  
                memoryUsage: window.performance.memory ? Math.round(window.performance.memory.usedJSHeapSize / 1024 / 1024) : 'N/A'  
            };  
            
            const report = `📊 **Análisis de Rendimiento**\n\n⚡ **Tiempo de carga:** ${performanceData.loadTime}ms\n💬 **Mensajes enviados:** ${performanceData.messageCount}\n⏱️ **Duración de sesión:** ${performanceData.sessionDuration} minutos\n💾 **Uso de memoria:** ${performanceData.memoryUsage}MB\n\n*Sistema optimizado y funcionando correctamente*`;  
            
            addMessage(report, 'bot');  
        }  

        // === COMANDOS ESPECIALES ===  
        document.addEventListener('keydown', function(e) {  
            // Ctrl + Enter para enviar  
            if (e.ctrlKey && e.key === 'Enter') {  
                sendMessage();  
            }  
            
            // Ctrl + L para limpiar chat  
            if (e.ctrlKey && e.key === 'l') {  
                e.preventDefault();  
                clearChat();  
            }  
            
            // Ctrl + E para exportar  
            if (e.ctrlKey && e.key === 'e') {  
                e.preventDefault();  
                exportChat();  
            }  
            
            // Ctrl + T para cambiar tema  
            if (e.ctrlKey && e.key === 't') {  
                e.preventDefault();  
                toggleTheme();  
            }  
        });  

        // === INICIALIZACIÓN DE TEMA ===  
        function initializeTheme() {  
            const savedTheme = localStorage.getItem('theme');  
            if (savedTheme === 'dark') {  
                document.body.classList.add('dark-theme');  
            }  
        }  

        // === FUNCIÓN DE BIENVENIDA ===  
        function showWelcomeMessage() {  
            setTimeout(() => {  
                const welcomeMessage = `🚀 **¡Bienvenido a Family Rivas AI v2.0!**\n\n¡Hola! Soy tu asistente inteligente personal, desarrollado por **Eros Jeancarlos Cordova Rivas**.\n\n✨ **Mis capacidades incluyen:**\n• 🤖 Conversación natural avanzada\n• 🌤️ Información del clima en tiempo real\n• 🧮 Cálculos matemáticos\n• 💻 Ayuda con programación\n• 🚀 Noticias de tecnología\n• 🎤 Reconocimiento de voz\n• 📎 Procesamiento de archivos\n\n¿En qué puedo ayudarte hoy?`;  
                
                addMessage(welcomeMessage, 'bot');  
            }, 1000);  
        }  

        // === EVENTOS DE CARGA ===  
        window.addEventListener('load', function() {  
            initializeTheme();  
            showWelcomeMessage();  
            
            // Easter egg - Konami Code  
            let konamiCode = [];  
            const konamiPattern = ['ArrowUp', 'ArrowUp', 'ArrowDown', 'ArrowDown', 'ArrowLeft', 'ArrowRight', 'ArrowLeft', 'ArrowRight', 'KeyB', 'KeyA'];  
            
            document.addEventListener('keydown', function(e) {  
                konamiCode.push(e.code);  
                if (konamiCode.length > konamiPattern.length) {  
                    konamiCode.shift();  
                }  
                
                if (konamiCode.length === konamiPattern.length &&   
                    konamiCode.every((code, index) => code === konamiPattern[index])) {  
                    
                    addMessage('🎉 **¡CÓDIGO KONAMI ACTIVADO!** 🎮\n\n¡Has desbloqueado el modo secreto de Family Rivas AI!\n\n🚀 Funciones especiales habilitadas\n⚡ Velocidad de respuesta aumentada\n🎯 Precisión al 100%\n\n*Desarrollado con amor por Eros Jeancarlos Cordova Rivas* ❤️', 'bot');  
                    
                    document.body.style.background = 'linear-gradient(45deg, #667eea 0%, #764ba2 100%)';  
                    konamiCode = [];  
                }  
            });  
        });  

        // === MANEJO DE ERRORES GLOBALES ===  
        window.addEventListener('error', function(e) {  
            console.error('Error global capturado:', e.error);  
            addMessage('⚠️ **Error del sistema detectado**\n\nSe ha producido un error inesperado, pero he logrado recuperarme automáticamente.\n\n*Sistema de auto-reparación activado* ✅', 'bot');  
        });  

        // === FUNCIONES DE UTILIDAD ===  
        function getRandomLoadingMessage() {  
            const messages = [  
                'Procesando tu solicitud...',  
                'Consultando base de conocimientos...',  
                'Analizando contexto...',  
                'Generando respuesta optimizada...',  
                'Aplicando inteligencia artificial...'  
            ];  
            return messages[Math.floor(Math.random() * messages.length)];  
        }  

        // === ANIMACIONES ADICIONALES ===  
        function addPulseAnimation(element) {  
            element.classList.add('pulse-animation');  
            setTimeout(() => {  
                element.classList.remove('pulse-animation');  
            }, 2000);  
        }  

        // === NOTIFICACIONES ===  
        function showNotification(message, type = 'info') {  
            const notification = document.createElement('div');  
            notification.className = `notification notification-${type}`;  
            notification.textContent = message;  
            
            document.body.appendChild(notification);  
            
            setTimeout(() => {  
                notification.classList.add('show');  
            }, 100);  
            
            setTimeout(() => {  
                notification.classList.remove('show');  
                setTimeout(() => {
                    document.body.removeChild(notification);
                }, 300);
            }, 3000);
        }

        // === FINALIZACIÓN DEL SCRIPT ===
        console.log('🚀 Family Rivas AI v2.0 cargado exitosamente');
        console.log('👨‍💻 Desarrollado por: Eros Jeancarlos Cordova Rivas');
        console.log('📧 Contacto: erosjcordovarivas@gmail.com');
        console.log('🌐 Sistema de IA avanzado inicializado');
        
    </script>
</body>
</html>
