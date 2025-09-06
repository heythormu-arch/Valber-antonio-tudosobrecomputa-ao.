<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <title>STUDIO V TECH</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: 'Segoe UI', sans-serif;
      background: linear-gradient(120deg, #0f0f0f, #1a1a1a);
      color: white;
      height: 100vh;
      overflow: hidden;
    }

    .container {
      text-align: center;
      padding-top: 100px;
      animation: fadeIn 2s ease-in-out forwards;
    }

    .logo {
      font-size: 4em;
      font-weight: bold;
      color: #0ff;
      text-shadow: 0 0 10px #0ff, 0 0 20px #0ff, 0 0 40px #0ff;
      animation: glow 2s infinite;
    }

    .subtitle {
      font-size: 1.2em;
      margin-top: 10px;
      color: #aaa;
      animation: fadeIn 3s ease-in-out forwards;
    }

    .creator {
      margin-top: 40px;
      font-size: 1em;
      color: #888;
      font-style: italic;
      animation: fadeIn 3.5s ease-in-out forwards;
    }

    @keyframes glow {
      0%, 100% {
        text-shadow: 0 0 10px #0ff, 0 0 20px #0ff;
      }
      50% {
        text-shadow: 0 0 30px #0ff, 0 0 60px #0ff;
      }
    }

    @keyframes fadeIn {
      0% { opacity: 0; transform: translateY(20px); }
      100% { opacity: 1; transform: translateY(0); }
    }

    button {
      margin-top: 50px;
      padding: 15px 40px;
      font-size: 1.5em;
      background-color: #0ff;
      border: none;
      color: #111;
      font-weight: bold;
      border-radius: 8px;
      cursor: pointer;
      transition: background 0.3s, transform 0.2s;
      animation: fadeIn 4s ease-in-out forwards;
    }

    button:hover {
      background-color: #00cccc;
      transform: scale(1.05);
    }

    #ad-section {
      display: none;
      padding: 50px;
      animation: fadeIn 2s ease-in-out forwards;
    }

    .scrolling-text {
      width: 100%;
      white-space: nowrap;
      overflow: hidden;
      box-sizing: border-box;
      border-top: 2px solid #0ff;
      border-bottom: 2px solid #0ff;
      margin-top: 30px;
    }

    .scrolling-text p {
      display: inline-block;
      padding-left: 100%;
      animation: scroll-left 15s linear infinite;
      font-size: 1.5em;
      color: #0ff;
    }

    @keyframes scroll-left {
      0% {
        transform: translateX(0%);
      }
      100% {
        transform: translateX(-100%);
      }
    }

    .highlight {
      color: #00ffff;
      font-weight: bold;
    }

    .ad-text {
      font-size: 1.8em;
      text-align: center;
      margin-top: 20px;
      color: #0ff;
      animation: fadeIn 3s ease-in-out forwards;
    }

    .thumbs-up {
      font-size: 3em;
      color: #0ff;
      margin-top: 20px;
    }

    .thank-you {
      display: none;
      font-size: 2em;
      color: #0ff;
      text-align: center;
      margin-top: 50px;
      animation: fadeIn 3s ease-in-out forwards;
    }

  </style>
</head>
<body>

  <div class="container" id="intro">
    <div class="logo">STUDIO V TECH</div>
    <div class="subtitle">Assistência Técnica de Confiança</div>
    <div class="creator">Criado por Valber • Tel: 16 93300 4123</div>
    <button onclick="mostrarPropaganda()">ENTRAR</button>
  </div>

  <div id="ad-section">
    <div class="ad-text">🚀 Seu PC com Problemas? A <span class="highlight">STUDIO V TECH</span> resolve!</div>

    <div class="scrolling-text">
      <p>🛠️ Formatação Profissional • 💻 Troca de Placa-Mãe • ⚙️ Instalação de Windows • 🔌 Limpeza e Montagem • 🧠 Diagnóstico Técnico • Tudo com garantia e confiança! 🚀</p>
    </div>

    <div class="ad-text" style="margin-top: 40px;">
      💡 Chame o especialista, chame <span class="highlight">Valber</span>!
    </div>

    <div class="thumbs-up">👍</div>
  </div>

  <div class="thank-you" id="thank-you">
    Obrigado por nos dar essa atenção! 🙏
  </div>

  <script>
    function mostrarPropaganda() {
      document.getElementById("intro").style.display = "none";
      document.getElementById("ad-section").style.display = "block";

      // Depois de 19 segundos, esconder a propaganda e mostrar a mensagem de agradecimento
      setTimeout(function() {
        document.getElementById("ad-section").style.display = "none";
        document.getElementById("thank-you").style.display = "block";
      }, 19000); // 19 segundos
    }
  </script>

</body>
</html>
