[index.html.html](https://github.com/user-attachments/files/25173227/index.html.html)
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>O amor de Alexsander por Beatriz</title>
  <style>
    /* ===== Reset básico ===== */
    * { box-sizing: border-box; margin: 0; padding: 0; }
    html, body { height: 100%; }

    /* ===== Fundo romântico ===== */
    body {
      font-family: system-ui, -apple-system, Segoe UI, Roboto, Arial, sans-serif;
      color: #2b0b16;
      overflow-x: hidden;
      background: radial-gradient(circle at top left, #ffe1ec, transparent 55%),
                  radial-gradient(circle at bottom right, #ffd6e7, transparent 60%),
                  linear-gradient(135deg, #fff0f6, #ffe6f0);
    }

    /* ===== Layout ===== */
    .wrap {
      min-height: 100%;
      display: grid;
      place-items: center;
      padding: 32px 16px;
      position: relative;
    }

    .card {
      width: min(920px, 100%);
      background: rgba(255, 255, 255, 0.75);
      backdrop-filter: blur(10px);
      border: 1px solid rgba(255, 182, 193, 0.55);
      border-radius: 24px;
      box-shadow: 0 10px 40px rgba(99, 17, 46, 0.15);
      padding: 28px;
      position: relative;
      overflow: hidden;
    }

    .header {
      display: grid;
      gap: 10px;
      margin-bottom: 18px;
    }

    h1 {
      font-size: clamp(28px, 4vw, 44px);
      letter-spacing: -0.02em;
      line-height: 1.1;
    }

    .sub {
      font-size: clamp(14px, 1.8vw, 18px);
      opacity: 0.85;
      line-height: 1.5;
    }

    /* ===== Contador ===== */
    .meter {
      display: grid;
      gap: 12px;
      margin: 18px 0 20px;
      padding: 18px;
      border-radius: 18px;
      background: rgba(255, 230, 240, 0.65);
      border: 1px solid rgba(255, 182, 193, 0.45);
    }

    .meterTitle {
      display: flex;
      align-items: baseline;
      justify-content: space-between;
      gap: 12px;
      flex-wrap: wrap;
    }

    .meterTitle span {
      font-weight: 700;
    }

    .value {
      font-variant-numeric: tabular-nums;
      font-weight: 800;
      font-size: clamp(26px, 5vw, 52px);
      letter-spacing: 0.02em;
    }

    .note {
      opacity: 0.85;
      line-height: 1.45;
      font-size: 14px;
    }

    /* ===== Textos poéticos ===== */
    .poems {
      display: grid;
      grid-template-columns: 1fr;
      gap: 12px;
      margin-top: 10px;
    }

    .poem {
      border-left: 4px solid rgba(255, 105, 180, 0.6);
      padding: 12px 14px;
      border-radius: 12px;
      background: rgba(255, 255, 255, 0.55);
      animation: fadeUp 700ms ease both;
    }

    .poem strong { font-weight: 800; }

    /* ===== Botões ===== */
    .actions {
      display: flex;
      gap: 10px;
      flex-wrap: wrap;
      margin-top: 18px;
    }

    button {
      appearance: none;
      border: 0;
      cursor: pointer;
      padding: 12px 14px;
      border-radius: 14px;
      font-weight: 700;
      transition: transform 120ms ease, box-shadow 120ms ease, opacity 120ms ease;
    }

    .primary {
      background: linear-gradient(135deg, #ff4d8d, #ff77a9);
      color: white;
      box-shadow: 0 12px 25px rgba(255, 77, 141, 0.25);
    }

    .ghost {
      background: rgba(255, 255, 255, 0.65);
      border: 1px solid rgba(255, 77, 141, 0.25);
      color: #6b0f2a;
    }

    button:hover { transform: translateY(-1px); }
    button:active { transform: translateY(0px) scale(0.99); opacity: 0.95; }

    /* ===== Barra "infinita" simbólica ===== */
    .bar {
      height: 12px;
      width: 100%;
      border-radius: 999px;
      background: rgba(255, 255, 255, 0.65);
      border: 1px solid rgba(255, 182, 193, 0.45);
      overflow: hidden;
    }

    .bar > i {
      display: block;
      height: 100%;
      width: 45%;
      border-radius: 999px;
      background: linear-gradient(90deg, #ff4d8d, #ff8fbc, #ff4d8d);
      animation: move 1.2s linear infinite;
      filter: saturate(1.1);
    }

    /* ===== Corações flutuando ===== */
    .hearts {
      position: absolute;
      inset: 0;
      pointer-events: none;
      overflow: hidden;
    }

    .heart {
      position: absolute;
      bottom: -40px;
      font-size: 18px;
      opacity: 0.0;
      animation: floatUp linear forwards;
      text-shadow: 0 6px 18px rgba(255, 77, 141, 0.25);
    }

    /* ===== Animações ===== */
    @keyframes move {
      from { transform: translateX(-60%); }
      to   { transform: translateX(220%); }
    }

    @keyframes fadeUp {
      from { opacity: 0; transform: translateY(10px); }
      to   { opacity: 1; transform: translateY(0); }
    }

    @keyframes floatUp {
      0%   { transform: translateY(0) translateX(0) scale(0.9); opacity: 0; }
      10%  { opacity: 0.95; }
      100% { transform: translateY(-120vh) translateX(var(--drift)) scale(1.25); opacity: 0; }
    }

    /* ===== Rodapé ===== */
    .footer {
      margin-top: 18px;
      opacity: 0.75;
      font-size: 13px;
      line-height: 1.4;
    }

    /* ===== Responsivo ===== */
    @media (min-width: 720px) {
      .poems { grid-template-columns: 1fr 1fr; }
      .card { padding: 34px; }
    }
  </style>
</head>

<body>
  <div class="wrap">
    <div class="hearts" id="hearts"></div>

    <main class="card" aria-label="Declaração de amor">
      <header class="header">
        <h1>Beatriz o amor do Alexsander por você é tão grande que nem o medidor consegue acompanhar.</h1>
        <p class="sub">
          Um sentimento que não se mede — mas a gente tenta, só pra deixar registrado:
          isso aqui é infinito.
        </p>
      </header>

      <section class="meter" aria-label="Medidor simbólico de amor">
        <div class="meterTitle">
          <span>Medidor simbólico (cresce sem parar)</span>
          <small class="note" id="status">Rodando...</small>
        </div>

        <div class="value" id="loveValue">0</div>

        <div class="bar" aria-hidden="true"><i></i></div>

        <p class="note">
          Cada número é só um jeito de dizer a mesma coisa: <strong>Beatriz</strong>, você é prioridade,
          presença e paz — e o que o Alexsander sente por você só aumenta.
        </p>

        <div class="actions">
          <button class="primary" id="boostBtn">Acelerar o amor</button>
          <button class="ghost" id="pauseBtn">Pausar</button>
          <button class="ghost" id="messageBtn">Nova mensagem</button>
        </div>
      </section>

      <section class="poems" id="poems" aria-label="Mensagens românticas">
        <div class="poem"><strong>Beatriz</strong>, o amor aqui é escolha diária: eu escolho você.</div>
        <div class="poem">Quando penso em futuro, seu nome aparece primeiro.</div>
        <div class="poem">Meu coração reconhece o seu — como se já soubesse o caminho.</div>
        <div class="poem">O que eu sinto não cabe em palavras… então eu construí um site.</div>
      </section>

      <p class="footer">
        Dica: salve este arquivo como <strong>index.html</strong> e abra no navegador.
      </p>
    </main>
  </div>

  <script>
    // ====== Configurações do "contador infinito" ======
    const loveValueEl = document.getElementById("loveValue");
    const statusEl = document.getElementById("status");
    const poemsEl = document.getElementById("poems");

    const boostBtn = document.getElementById("boostBtn");
    const pauseBtn = document.getElementById("pauseBtn");
    const messageBtn = document.getElementById("messageBtn");

    let running = true;
    let love = 0;

    // Velocidade base (quantos incrementos por "tick")
    let speed = 1;

    // Usa BigInt pra não estourar rapidamente
    let loveBig = 0n;

    // Formata com separador de milhar no pt-BR
    function formatBigInt(n) {
      // Converte pra string e aplica separador manual pra suportar BigInt
      const s = n.toString();
      let out = "";
      let count = 0;
      for (let i = s.length - 1; i >= 0; i--) {
        out = s[i] + out;
        count++;
        if (count === 3 && i !== 0) {
          out = "." + out; // pt-BR usa ponto como separador de milhar
          count = 0;
        }
      }
      return out;
    }

    function tick() {
      if (running) {
        // Crescimento simbólico: a velocidade também cresce aos poucos
        // (vai ficando "mais infinito" com o tempo)
        const add = BigInt(speed);
        loveBig += add;

        // Aumenta a velocidade devagar (limite pra não travar)
        if (speed < 5000) speed += 1;

        loveValueEl.textContent = formatBigInt(loveBig);
      }
      requestAnimationFrame(tick);
    }

    // ====== Mensagens românticas randômicas ======
    const messages = [
      "Beatriz, eu te amo do jeito mais sério e mais leve ao mesmo tempo.",
      "Meu coração fica em paz quando é você.",
      "Você é meu pensamento bom repetido todo dia.",
      "Se amor tivesse endereço, o meu sempre daria em você.",
      "Eu não te amo só por hoje — eu te amo por tudo que vem depois.",
      "Você é a parte do meu mundo que faz sentido.",
      "O que eu sinto por você não diminui: amadurece e aumenta."
    ];

    function addMessage() {
      const msg = messages[Math.floor(Math.random() * messages.length)];
      const div = document.createElement("div");
      div.className = "poem";
      div.textContent = msg;
      poemsEl.prepend(div);

      // Limita a quantidade pra não ficar enorme
      const max = 8;
      while (poemsEl.children.length > max) {
        poemsEl.removeChild(poemsEl.lastElementChild);
      }
    }

    // ====== Corações flutuando ======
    const heartsWrap = document.getElementById("hearts");
    const heartChars = ["❤", "💗", "💖", "💘", "💕"];

    function spawnHeart() {
      const heart = document.createElement("div");
      heart.className = "heart";
      heart.textContent = heartChars[Math.floor(Math.random() * heartChars.length)];

      const left = Math.random() * 100;
      const size = 14 + Math.random() * 22;
      const duration = 4 + Math.random() * 4;

      heart.style.left = left + "vw";
      heart.style.fontSize = size + "px";
      heart.style.animationDuration = duration + "s";
      heart.style.setProperty("--drift", (Math.random() * 60 - 30) + "px");

      heartsWrap.appendChild(heart);

      // Remove depois pra não acumular elementos
      setTimeout(() => heart.remove(), duration * 1000);
    }

    // ====== Eventos ======
    boostBtn.addEventListener("click", () => {
      // "Acelera" forte, mas com limite
      speed = Math.min(speed + 250, 8000);
      statusEl.textContent = "Amor acelerado.";
      setTimeout(() => statusEl.textContent = running ? "Rodando..." : "Pausado.", 900);

      // Explosão de corações
      for (let i = 0; i < 18; i++) setTimeout(spawnHeart, i * 30);
    });

    pauseBtn.addEventListener("click", () => {
      running = !running;
      pauseBtn.textContent = running ? "Pausar" : "Continuar";
      statusEl.textContent = running ? "Rodando..." : "Pausado.";
    });

    messageBtn.addEventListener("click", () => {
      addMessage();
      for (let i = 0; i < 8; i++) setTimeout(spawnHeart, i * 40);
    });

    // ====== Inicialização ======
    // Começa com alguns corações
    for (let i = 0; i < 10; i++) setTimeout(spawnHeart, i * 120);

    // Spawn contínuo suave
    setInterval(() => {
      if (running) spawnHeart();
    }, 450);

    // Primeira mensagem extra
    setTimeout(addMessage, 800);

    // Inicia animação do contador
    tick();
  </script>
</body>
</html>

