<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Professora Tabuada (1–15)</title>
  <style>
    :root{
      --bg:#0f172a;          /* fundo escuro */
      --panel:#0b1220;       /* painel */
      --text:#e5e7eb;        /* texto */
      --muted:#94a3b8;       /* texto fraco */
      --primary:#22d3ee;     /* ciano */
      --ok:#34d399;          /* verde */
      --bad:#fb7185;         /* rosa */
      --warn:#f59e0b;        /* âmbar */
    }
    *{box-sizing:border-box}
    html,body{height:100%}
    body{
      margin:0; font-family: system-ui, -apple-system, Segoe UI, Roboto, Ubuntu, Cantarell, Noto Sans, Arial;
      color:var(--text);
      background: radial-gradient(1400px 900px at 70% -10%, #0b1220 10%, var(--bg) 60%) fixed;
      overflow:hidden;
    }

    /* ===== CENÁRIO ===== */
    .scene{
      position:relative; width:100%; height:100%;
      display:grid; place-items:center;
    }
    .bg{
      position:absolute; inset:0; object-fit:cover; width:100%; height:100%; filter: blur(2px) brightness(.7);
    }
    .bg.fallback{ background:
      radial-gradient(1200px 800px at 20% 10%, rgba(34,211,238,.2), transparent 60%),
      linear-gradient(180deg, rgba(255,255,255,.02), rgba(255,255,255,.01));
    }
    .overlay{ position:absolute; inset:0; background: linear-gradient(180deg, rgba(0,0,0,.25), rgba(0,0,0,.45)); }

    /* ===== PROFESSORA ===== */
    .teacher{
      position:absolute; left: clamp(8px, 4vw, 48px); bottom: clamp(8px, 5vh, 64px);
      width: min(34vw, 360px); aspect-ratio: 3/4; display:flex; align-items:flex-end; justify-content:center;
      pointer-events:none; user-select:none;
    }
    .teacher img{ width:100%; height:auto; border-radius: 18px; box-shadow: 0 20px 60px rgba(0,0,0,.45); opacity:.85}
    .talking{ animation: bounce 1.2s ease-in-out infinite; }
    @keyframes bounce{ 0%,100%{ transform: translateY(0)} 50%{ transform: translateY(-4px)} }

    /* ===== PAINEL ===== */
    .panel{
      position:relative; z-index:2; width:min(920px, 95vw);
      background: linear-gradient(180deg, rgba(255,255,255,.06), rgba(255,255,255,.03));
      border:1px solid rgba(255,255,255,.12); border-radius:24px; padding:18px 18px 14px; backdrop-filter: blur(6px);
      box-shadow: 0 10px 40px rgba(0,0,0,.35);
    }
    header{ display:flex; align-items:center; justify-content:space-between; gap:12px; margin-bottom:8px }
    .title{ font-weight:900; letter-spacing:.3px; font-size: clamp(18px, 2.4vw, 28px); }
    .badge{ font-size:12px; color: var(--muted); border:1px solid rgba(255,255,255,.14); padding:6px 10px; border-radius:999px }

    .question{ display:flex; align-items:center; justify-content:center; text-align:center; min-height:108px; border-radius:16px; font-weight:900; letter-spacing:.6px; font-size: clamp(28px, 5vw, 64px);
      background: linear-gradient(180deg, rgba(34,211,238,.1), rgba(34,211,238,.03)); border:1px dashed rgba(34,211,238,.35); }

    .row{ display:flex; gap:10px; align-items:center; flex-wrap:wrap }
    .row + .row{ margin-top:10px }

    input[type=number]{
      width: 170px; padding: 12px 14px; border-radius: 14px; background: var(--panel); color: var(--text);
      border:1px solid rgba(255,255,255,.16); font-size: 18px; outline:none;
    }
    input[type=number]:focus{ border-color: var(--primary); box-shadow: 0 0 0 4px rgba(34,211,238,.15) }

    button{ padding: 12px 16px; border-radius: 14px; border:1px solid rgba(255,255,255,.16); background: var(--panel); color:var(--text); font-weight:800; cursor:pointer }
    button.primary{ background: linear-gradient(180deg, #22d3ee, #0891b2); border:none; color:#001e26 }
    button.ghost{ background: transparent }
    button:disabled{ opacity:.6; cursor:not-allowed }

    .feedback{ min-height:28px; font-weight:800; letter-spacing:.2px }
    .ok{ color: var(--ok) }
    .bad{ color: var(--bad) }
    .hint{ color: var(--warn) }

    .chips{ display:flex; gap:8px; flex-wrap:wrap }
    .chip{ font-size:12px; color: var(--muted); border:1px solid rgba(255,255,255,.14); padding:6px 10px; border-radius:999px }

    .stats{ display:grid; grid-template-columns: repeat(3, 1fr); gap:8px }
    .stat{ background: rgba(255,255,255,.05); border:1px solid rgba(255,255,255,.1); border-radius:16px; text-align:center; padding:10px }
    .stat .big{ font-size:26px; font-weight:900 }

    .footer{ margin-top:8px; text-align:center; color:var(--muted); font-size:12px }

    @media (max-width: 820px){ .teacher{ width:min(44vw, 280px) } }
  </style>
</head>
<body>
  <div class="scene">
    <!-- Coloque um arquivo "cenario.jpg" na mesma pasta para virar o fundo -->
    <img class="bg" id="bgImg" src="Fundo.png" alt="Cenário (sala de aula)">
    <div class="bg fallback" id="bgFallback"></div>
    <div class="overlay"></div>

    <!-- Professora (duas imagens: boca fechada e aberta) -->
    <div class="teacher">
      <!-- Coloque os arquivos: professora-fechada.png e professora-aberta.png -->
      <img id="professora" src="Professora1.png" alt="Professora" data-mouth="closed">
    </div>

    <!-- Painel da aplicação -->
    <div class="panel">
      <header>
        <div class="title">👩🏻‍🏫 Professora Falante da Tabuada <span style="opacity:.75">(2–15)</span></div>
        <div class="badge" id="voiceState">🔈 Voz: desligada</div>
      </header>

      <div class="question" id="pergunta">Clique em Começar</div>

      <div class="row" style="margin-top:12px">
        <input id="resposta" type="number" placeholder="Digite aqui" disabled>
        <button class="primary" id="btnVerificar" disabled>Verificar</button>
        <button class="ghost" id="btnPular" disabled>Pular</button>
        <button class="ghost" id="btnOuvir" title="Repetir a pergunta" disabled>🔊 Ouvir</button>
      </div>

      <div class="feedback" id="feedback"></div>

      <div class="row" style="justify-content:space-between; margin-top:4px">
        <div class="chips">
          <span class="chip">Tabuadas: 2–15</span>
          <span class="chip">Multiplicadores: 0–12</span>
        </div>
        <div class="row">
          <button id="btnVoz" class="ghost">Ativar voz</button>
          <button id="btnReset" class="ghost">Reset</button>
          <button id="btnStart" class="primary">Começar</button>
        </div>
      </div>

      <div class="stats" style="margin-top:12px">
        <div class="stat"><div class="big" id="sAcertos">0</div><small>Acertos</small></div>
        <div class="stat"><div class="big" id="sSequencia">0</div><small>Sequência</small></div>
        <div class="stat"><div class="big" id="sTempo">—</div><small>Tempo</small></div>
      </div>

      <div class="footer">Dicas: <b>Enter</b> verifica · <b>Espaço</b> pula </div>
    </div>
  </div>

  <script>
    // ========= ELEMENTOS =========
    const $ = (sel)=>document.querySelector(sel);
    const el = {
      pergunta: $('#pergunta'), resposta: $('#resposta'), btnVerificar: $('#btnVerificar'), btnPular: $('#btnPular'), btnStart: $('#btnStart'),
      feedback: $('#feedback'), sAcertos: $('#sAcertos'), sSequencia: $('#sSequencia'), sTempo: $('#sTempo'),
      btnVoz: $('#btnVoz'), voiceState: $('#voiceState'), btnOuvir: $('#btnOuvir'), btnReset: $('#btnReset'),
      prof: $('#professora'), bgImg: $('#bgImg'), bgFallback: $('#bgFallback')
    };

    // Esconde fallback se a imagem de fundo carregar
    el.bgImg.addEventListener('load', ()=>{ el.bgFallback.style.display='none'; });
    el.bgImg.addEventListener('error', ()=>{ el.bgFallback.style.display='block'; });

    // ========= ESTADO =========
    const state = {
      a: null, b: null,
      acertos: 0, sequencia: 0, startTime: 0, timerId: null,
      vozAtiva: false,
      talkingTimer: null, // intervalo para abrir/fechar boca
    };

    // ========= UTIL =========
    function randInt(min, max){ // inclusive
      return Math.floor(Math.random() * (max - min + 1)) + min;
    }

    function setFeedback(texto, kind){
      el.feedback.className = 'feedback ' + (kind || '');
      el.feedback.textContent = texto || '';
    }

    // ========= PERGUNTAS =========
    function novaPergunta(){
      state.a = randInt(2,15);
      state.b = randInt(0,12);
      el.pergunta.textContent = `${state.a} × ${state.b} = ?`;
      el.resposta.value = '';
      el.resposta.focus();
      setFeedback('','');
      if(state.vozAtiva) falar(`Quanto é ${state.a} vezes ${state.b}?`);
    }

    function verificar(){
      const val = Number(el.resposta.value.trim());
      const certo = state.a * state.b;
      if(val === certo){
        state.acertos++; state.sequencia++;
        el.sAcertos.textContent = state.acertos; el.sSequencia.textContent = state.sequencia;
        setFeedback(`✔ Boa! ${state.a} × ${state.b} = ${certo}.`, 'ok');
        if(state.vozAtiva) falar(`Acertou..! ${state.a} vezes ${state.b} é ${certo}.`);
        setTimeout(novaPergunta, 500);
      } else {
        state.sequencia = 0; el.sSequencia.textContent = 0;
        setFeedback(`✖ Ops! Tente novamente…`, 'bad');
        if(state.vozAtiva) falar(`Opsss, Tente novamente...`);
        el.resposta.select();
      }
    }

    function pular(){
      setFeedback('↪ Pulou. Vamos pra próxima.', 'hint');
      if(state.vozAtiva) falar('Pulou. Próxima pergunta.');
      novaPergunta();
    }

    function start(){
      state.acertos = 0; state.sequencia = 0; el.sAcertos.textContent = 0; el.sSequencia.textContent = 0;
      state.startTime = performance.now();
      clearInterval(state.timerId);
      state.timerId = setInterval(()=>{
        const secs = Math.round((performance.now() - state.startTime)/100)/10; // 0.1s
        el.sTempo.textContent = secs + 's';
      }, 200);

      el.resposta.disabled = false; el.btnVerificar.disabled = false; el.btnPular.disabled = false; el.btnOuvir.disabled = false;
      novaPergunta();
    }

    function resetAll(){
      clearInterval(state.timerId); el.sTempo.textContent = '—';
      el.resposta.value = ''; el.resposta.disabled = true; el.btnVerificar.disabled = true; el.btnPular.disabled = true; el.btnOuvir.disabled = true;
      state.acertos = 0; state.sequencia = 0; el.sAcertos.textContent = 0; el.sSequencia.textContent = 0;
      setFeedback('', ''); el.pergunta.textContent = 'Clique em Começar';
    }

    // ========= FALA + ANIMAÇÃO DE BOCA =========
    function startTalking(){
      // animação simples: alterna boca aberta/fechada a cada 120ms enquanto fala
      stopTalking();
      el.prof.classList.add('talking');
      state.talkingTimer = setInterval(()=>{
        const isOpen = el.prof.dataset.mouth === 'open';
        el.prof.dataset.mouth = isOpen ? 'closed' : 'open';
        updateMouth();
      }, 120);
    }

    function stopTalking(){
      if(state.talkingTimer){ clearInterval(state.talkingTimer); state.talkingTimer = null; }
      el.prof.dataset.mouth = 'closed';
      el.prof.classList.remove('talking');
      updateMouth();
    }

    function updateMouth(){
      const openSrc = 'professora-aberta.png';
      const closedSrc = 'professora-fechada.png';
      el.prof.src = (el.prof.dataset.mouth === 'open') ? openSrc : closedSrc;
    }

    function falar(texto){
      try{
        if(window.speechSynthesis.speaking) window.speechSynthesis.cancel();
        const msg = new SpeechSynthesisUtterance(texto);
        msg.lang = 'pt-BR';
        msg.rate = 1; // velocidade
        msg.pitch = 1; // tom
        msg.onstart = startTalking;
        msg.onend = stopTalking;
        msg.onerror = stopTalking;
        window.speechSynthesis.speak(msg);
      }catch(e){ console.warn('Speech falhou', e); }
    }

    // ========= VOZ ON/OFF =========
    function toggleVoz(){
      state.vozAtiva = !state.vozAtiva;
      el.voiceState.textContent = state.vozAtiva ? '🔊 Voz: ligada' : '🔈 Voz: desligada';
      el.btnVoz.textContent = state.vozAtiva ? 'Desativar voz' : 'Ativar voz';
      if(state.vozAtiva && el.pergunta.textContent.includes('×')){
        falar(`Quanto é ${state.a} vezes ${state.b}?`);
      } else if(!state.vozAtiva){
        if(window.speechSynthesis.speaking) window.speechSynthesis.cancel();
        stopTalking();
      }
    }

    // ========= EVENTOS =========
    el.btnStart.addEventListener('click', start);
    el.btnVerificar.addEventListener('click', verificar);
    el.btnPular.addEventListener('click', pular);
    el.btnOuvir.addEventListener('click', ()=>{ if(state.vozAtiva) falar(`Quanto é ${state.a} vezes ${state.b}?`); });
    el.btnVoz.addEventListener('click', toggleVoz);
    el.btnReset.addEventListener('click', resetAll);

    // Enter = verificar | Espaço = pular
    document.addEventListener('keydown', (e)=>{
      if(el.btnVerificar.disabled) return;
      if(e.key === 'Enter'){ verificar(); }
      else if(e.key === ' '){ e.preventDefault(); pular(); }
    });

    // Se usuário clicar na professora e a voz estiver ativa, repetir a pergunta
    el.prof.addEventListener('click', ()=>{ if(state.vozAtiva && !el.btnVerificar.disabled) falar(`Quanto é ${state.a} vezes ${state.b}?`); });

    // Estado inicial
    resetAll();
  </script>
</body>
</html>
