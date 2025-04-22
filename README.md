# Chatbot-Mario-
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>Chatbot - Mario Javier Chumbez</title>
  <style>
    body { font-family: Arial; background: #f2f2f2; margin: 0; padding: 20px; }
    .chat-container { background: #fff; padding: 20px; border-radius: 8px; width: 100%; max-width: 480px; margin: auto; box-shadow: 0 0 10px rgba(0,0,0,0.1); }
    .bot { background-color: #e0f0ff; padding: 10px; margin: 10px 0; border-radius: 8px; }
    .user { background-color: #d1ffd1; padding: 10px; margin: 10px 0; border-radius: 8px; text-align: right; }
    button { margin: 5px; padding: 8px 16px; border: none; border-radius: 4px; cursor: pointer; }
    .btn-option { background-color: #0077cc; color: #fff; }
  </style>
</head>
<body>
  <div class="chat-container" id="chat">
    <div class="bot">Hola, soy Mario Javier Chumbez. ¿En qué puedo ayudarte hoy?</div>
    <button class="btn-option" onclick="show('experiencia')">Ver experiencia profesional</button>
    <button class="btn-option" onclick="show('logros')">Conocer logros</button>
    <button class="btn-option" onclick="show('cv')">Descargar mi CV</button>
    <button class="btn-option" onclick="show('agenda')">Agendar una reunión</button>
  </div>

  <script>
    function show(option) {
      const chat = document.getElementById('chat');
      let response = document.createElement('div');
      response.classList.add('user');
      response.textContent = option.charAt(0).toUpperCase() + option.slice(1);
      chat.appendChild(response);

      let botReply = document.createElement('div');
      botReply.classList.add('bot');

      if (option === 'experiencia') {
        botReply.textContent = "Coordino vendors en CrediScotia. También trabajé en Scotiacontacto y Grupo El Comercio, liderando equipos de ventas y estrategias comerciales.";
      } else if (option === 'logros') {
        botReply.textContent = "Logros: Logramos aumentar +40% productividad en el ultimo año, reducimos la rotación en 18%, funnel de ventas implementado con mejor visibilidad de indicadores para la toma de decisiones, A nivel personal la empresa familiar sigue dando trabajo a mas peruanos .";
      } else if (option === 'cv') {
        botReply.innerHTML = 'Puedes descargar mi CV aquí: <a href="CV_Editable_Mario_Chumbez.docx" target="_blank">Descargar CV</a>';
      } else if (option === 'agenda') {
        botReply.innerHTML = 'Agenda una llamada conmigo aquí: <a href="https://calendly.com/tulink" target="_blank">Calendly</javierchumbez> o contáctame por <a href="https://wa.me/51992085196">WhatsApp</a>';
      }

      chat.appendChild(botReply);
    }
  </script>
</body>
</html>
