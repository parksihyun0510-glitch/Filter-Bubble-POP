<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Filter Bubble Pop — Caixin</title>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link href="https://fonts.googleapis.com/css2?family=IBM+Plex+Mono:wght@400;500&family=Playfair+Display:wght@700&display=swap" rel="stylesheet">
  <style>
    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

    :root {
      --navy: #0B132B;
      --navy-2: #111d35;
      --gold: #C9A84C;
      --gold-lt: #E8C96A;
      --white: #F5F5F0;
      --muted: #8A8FA8;
      --danger: #E05555;
      --success: #4CAF82;
      --border: rgba(201,168,76,0.2);
    }

    body {
      background: var(--navy);
      color: var(--white);
      font-family: 'IBM Plex Mono', monospace;
      min-height: 100vh;
      display: flex;
      flex-direction: column;
      align-items: center;
      padding: 48px 24px 80px;
    }

    /* ── Header ── */
    .site-header { text-align: center; margin-bottom: 56px; }
    .brand { font-size: 11px; letter-spacing: 4px; color: var(--gold); margin-bottom: 14px; }
    .site-title {
      font-family: 'Playfair Display', serif;
      font-size: clamp(26px, 5vw, 42px);
      color: var(--white);
      line-height: 1.15;
      margin-bottom: 14px;
    }
    .site-subtitle {
      font-size: 11px;
      color: var(--muted);
      line-height: 1.8;
      max-width: 480px;
      margin: 0 auto;
    }
    .divider { width: 48px; height: 1px; background: var(--gold); margin: 28px auto 0; opacity: 0.4; }

    /* ── Main card ── */
    .card {
      width: 100%;
      max-width: 680px;
      background: var(--navy-2);
      border: 0.5px solid var(--border);
      border-radius: 18px;
      padding: 36px 40px 40px;
      display: flex;
      flex-direction: column;
      gap: 28px;
    }

    /* ── Bias Index panel ── */
    .bias-panel {
      background: rgba(224,85,85,0.08);
      border: 0.5px solid rgba(224,85,85,0.3);
      border-radius: 12px;
      padding: 18px 22px;
    }
    .bias-top {
      display: flex;
      align-items: flex-start;
      justify-content: space-between;
      margin-bottom: 14px;
    }
    .bias-kicker { font-size: 9px; letter-spacing: 3px; color: var(--danger); margin-bottom: 5px; }
    .bias-headline { font-size: 13px; color: var(--white); font-weight: 500; }
    .bias-value { font-size: 28px; font-weight: 500; color: var(--danger); line-height: 1; text-align: right; transition: color 0.5s; }
    .bias-value-label { font-size: 9px; color: var(--danger); letter-spacing: 1px; margin-top: 3px; transition: color 0.5s; }
    .bar-track { height: 5px; background: rgba(255,255,255,0.07); border-radius: 3px; overflow: hidden; }
    .bar-fill { height: 100%; border-radius: 3px; background: linear-gradient(90deg, var(--danger), var(--gold)); transition: width 0.6s cubic-bezier(.4,0,.2,1), background 0.5s; }
    .bar-scale { display: flex; justify-content: space-between; margin-top: 5px; }
    .bar-scale span { font-size: 8px; color: var(--muted); }

    /* ── Section label ── */
    .section-label { font-size: 9px; letter-spacing: 3px; color: var(--gold); border-bottom: 0.5px solid var(--border); padding-bottom: 10px; }

    /* ── Bubble field ── */
    .bubble-field {
      position: relative;
      min-height: 280px;
      display: flex;
      flex-wrap: wrap;
      align-items: flex-start;
      align-content: flex-start;
      gap: 14px;
      padding: 8px 0;
    }

    .empty-state {
      position: absolute;
      inset: 0;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      gap: 10px;
      opacity: 0;
      pointer-events: none;
      transition: opacity 0.5s ease;
    }
    .empty-state.visible { opacity: 1; }
    .empty-icon { font-size: 32px; opacity: 0.35; }
    .empty-text { font-size: 11px; color: var(--muted); text-align: center; line-height: 1.7; }

    /* ── Bubble ── */
    .bubble {
      position: relative;
      display: inline-flex;
      align-items: center;
      gap: 9px;
      padding: 11px 18px;
      /* fully pill-shaped */
      border-radius: 999px;
      font-size: 13px;
      font-weight: 500;
      cursor: default;
      user-select: none;
      border: 1px solid;
      transition: transform 0.2s cubic-bezier(.34,1.56,.64,1), box-shadow 0.2s ease;
      animation: floatIn 0.5s cubic-bezier(.22,1.5,.4,1) both;
      will-change: transform;
    }

    @keyframes floatIn {
      from { opacity: 0; transform: scale(0.4) translateY(10px); }
      to   { opacity: 1; transform: scale(1)   translateY(0);    }
    }

    .bubble:hover { transform: scale(1.08); }

    /* Size variants — all remain pill-shaped */
    .bubble.xl { font-size: 15px; padding: 13px 22px; }
    .bubble.lg { font-size: 13px; padding: 11px 18px; }
    .bubble.sm { font-size: 11px; padding: 8px  14px; }
    .bubble.xs { font-size: 10px; padding: 6px  12px; }

    /* Color variants */
    .bubble.gold   { background: rgba(201,168,76,0.12); border-color: rgba(201,168,76,0.5);  color: var(--gold-lt); }
    .bubble.teal   { background: rgba(0,194,168,0.10);  border-color: rgba(0,194,168,0.4);   color: #5DDECE; }
    .bubble.muted  { background: rgba(138,143,168,0.10);border-color: rgba(138,143,168,0.28);color: var(--muted); }
    .bubble.danger { background: rgba(224,85,85,0.10);  border-color: rgba(224,85,85,0.4);   color: #F08080; }
    .bubble.purple { background: rgba(150,100,220,0.10);border-color: rgba(150,100,220,0.4); color: #C8A0F0; }

    /* ── × button ── */
    .pop-btn {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      width: 20px;
      height: 20px;
      border-radius: 50%;
      background: rgba(224,85,85,0.15);
      border: 0.5px solid rgba(224,85,85,0.45);
      font-size: 11px;
      color: var(--danger);
      cursor: pointer;
      transition: background 0.15s, transform 0.15s;
      flex-shrink: 0;
      line-height: 1;
    }
    .pop-btn:hover { background: rgba(224,85,85,0.38); transform: scale(1.2); }

    /* ────────────────────────────────────
       POP ANIMATION — 3-phase burst
       1. quick inflate + slight wobble
       2. fast scale-up with rotation
       3. scatter shards + fade to zero
    ──────────────────────────────────── */
    @keyframes bubblePop {
      0%   { transform: scale(1)    rotate(0deg);   opacity: 1;   filter: brightness(1);   }
      12%  { transform: scale(1.18) rotate(-3deg);  opacity: 1;   filter: brightness(1.3); }
      24%  { transform: scale(1.05) rotate(3deg);   opacity: 1;   filter: brightness(1.5); }
      40%  { transform: scale(1.55) rotate(-2deg);  opacity: 0.85;filter: brightness(1.8); }
      60%  { transform: scale(2.1)  rotate(5deg);   opacity: 0.45;filter: brightness(2);   }
      80%  { transform: scale(2.8)  rotate(-4deg);  opacity: 0.15;filter: brightness(2.2); }
      100% { transform: scale(3.2)  rotate(2deg);   opacity: 0;   filter: brightness(2.5); }
    }

    /* particle fragments that fly outward */
    @keyframes shardFly {
      0%   { transform: translate(0,0) scale(1);   opacity: 0.9; }
      100% { transform: translate(var(--dx), var(--dy)) scale(0); opacity: 0; }
    }

    .popping {
      animation: bubblePop 0.48s cubic-bezier(.4,0,.6,1) forwards !important;
      pointer-events: none;
      overflow: visible;
      z-index: 10;
    }

    /* shard element */
    .shard {
      position: absolute;
      border-radius: 999px;
      pointer-events: none;
      animation: shardFly 0.5s ease-out forwards;
    }

    /* ── Restore / counter ── */
    .restore-row { display: flex; align-items: center; justify-content: space-between; flex-wrap: wrap; gap: 12px; }
    .popped-count { font-size: 10px; color: var(--muted); min-height: 18px; }
    .restore-btn {
      font-family: 'IBM Plex Mono', monospace;
      font-size: 10px;
      letter-spacing: 1px;
      color: var(--gold);
      background: rgba(201,168,76,0.08);
      border: 0.5px solid rgba(201,168,76,0.3);
      border-radius: 6px;
      padding: 7px 16px;
      cursor: pointer;
      transition: background 0.15s;
      display: none;
    }
    .restore-btn:hover { background: rgba(201,168,76,0.18); }

    .footnote { font-size: 9px; color: var(--muted); text-align: center; line-height: 1.8; opacity: 0.6; }
  </style>
</head>
<body>

  <header class="site-header">
    <p class="brand">財新 CAIXIN — IMC DEMO</p>
    <h1 class="site-title">Filter Bubble<br>Pop UI</h1>
    <p class="site-subtitle">
      Review the algorithmic topics you are currently over-exposed to.<br>
      Remove them one by one to restore your information balance.
    </p>
    <div class="divider"></div>
  </header>

  <main class="card">

    <div class="bias-panel">
      <div class="bias-top">
        <div>
          <p class="bias-kicker">ALGORITHM AUDIT</p>
          <p class="bias-headline">My Information Balance Index</p>
        </div>
        <div style="text-align:right">
          <div class="bias-value" id="biasValueNum">72</div>
          <div class="bias-value-label" id="biasValueLabel">% BIASED</div>
        </div>
      </div>
      <div class="bar-track">
        <div class="bar-fill" id="biasFill" style="width:72%"></div>
      </div>
      <div class="bar-scale">
        <span>Balanced — 0%</span>
        <span>100% — Heavily Biased</span>
      </div>
    </div>

    <div>
      <p class="section-label">ACTIVE TOPIC BUBBLES — CLICK × TO REMOVE</p>
    </div>

    <div class="bubble-field" id="bubbleField">
      <div class="empty-state" id="emptyState">
        <div class="empty-icon">✦</div>
        <p class="empty-text">
          All topic bubbles have been removed.<br>
          Information Balance Index: <strong style="color:var(--success)">Balanced</strong>
        </p>
      </div>
    </div>

    <div class="restore-row">
      <p class="popped-count" id="poppedCount"></p>
      <button class="restore-btn" id="restoreBtn" onclick="restoreAll()">↺ Restore all bubbles</button>
    </div>

  </main>

  <p class="footnote" style="margin-top:36px">
    This is a UI demonstration only. · Caixin IMC Campaign · 財新傳媒
  </p>

  <script>
    const BUBBLES = [
      { id:'b1',  label:'#Youth_Unemployment',  size:'xl', color:'gold',   weight:22, delay:0   },
      { id:'b2',  label:'#Real_Estate_Policy',  size:'lg', color:'teal',   weight:18, delay:60  },
      { id:'b3',  label:'#TechRegulation',      size:'lg', color:'gold',   weight:14, delay:120 },
      { id:'b4',  label:'#StockMarket',         size:'sm', color:'muted',  weight:8,  delay:180 },
      { id:'b5',  label:'#Inflation',           size:'lg', color:'danger', weight:16, delay:240 },
      { id:'b6',  label:'#GraduateJobs',        size:'xl', color:'purple', weight:20, delay:300 },
      { id:'b7',  label:'#FDI_Policy',          size:'sm', color:'muted',  weight:6,  delay:360 },
      { id:'b8',  label:'#USChinaTrade',        size:'lg', color:'teal',   weight:12, delay:420 },
      { id:'b9',  label:'#GDPGrowth',           size:'sm', color:'muted',  weight:5,  delay:480 },
      { id:'b10', label:'#CarbonPolicy',        size:'xs', color:'muted',  weight:4,  delay:540 },
    ];

    const BIAS_BASE = BUBBLES.reduce((s,b) => s + b.weight, 0);
    let poppedIds = new Set();

    /* colour map for shards */
    const SHARD_COLORS = {
      gold:   ['#C9A84C','#E8C96A','#fff8e0'],
      teal:   ['#00C2A8','#5DDECE','#a0f5e8'],
      muted:  ['#8A8FA8','#b0b4c8','#dde0ea'],
      danger: ['#E05555','#F08080','#ffd0d0'],
      purple: ['#9664DC','#C8A0F0','#ecdcff'],
    };

    function spawnShards(el, color) {
      const rect   = el.getBoundingClientRect();
      const field  = document.getElementById('bubbleField').getBoundingClientRect();
      const cx     = rect.left + rect.width  / 2 - field.left;
      const cy     = rect.top  + rect.height / 2 - field.top;
      const colors = SHARD_COLORS[color] || SHARD_COLORS.muted;
      const count  = 10;

      for (let i = 0; i < count; i++) {
        const angle  = (360 / count) * i + (Math.random() - 0.5) * 30;
        const dist   = 60 + Math.random() * 80;
        const rad    = angle * Math.PI / 180;
        const dx     = Math.cos(rad) * dist;
        const dy     = Math.sin(rad) * dist;
        const w      = 6  + Math.random() * 10;
        const h      = 5  + Math.random() * 8;
        const delay  = Math.random() * 60;
        const dur    = 420 + Math.random() * 120;
        const clr    = colors[Math.floor(Math.random() * colors.length)];

        const shard = document.createElement('div');
        shard.className = 'shard';
        shard.style.cssText = `
          left:${cx - w/2}px; top:${cy - h/2}px;
          width:${w}px; height:${h}px;
          background:${clr};
          opacity:0.85;
          --dx:${dx}px; --dy:${dy}px;
          animation-duration:${dur}ms;
          animation-delay:${delay}ms;
        `;
        document.getElementById('bubbleField').appendChild(shard);
        setTimeout(() => shard.remove(), dur + delay + 50);
      }
    }

    function renderBubbles() {
      const field = document.getElementById('bubbleField');
      field.querySelectorAll('.bubble').forEach(el => el.remove());

      BUBBLES.forEach(b => {
        if (poppedIds.has(b.id)) return;
        const el = document.createElement('div');
        el.className = `bubble ${b.size} ${b.color}`;
        el.id = b.id;
        el.style.animationDelay = b.delay + 'ms';
        el.innerHTML = `
          <span>${b.label}</span>
          <span class="pop-btn" title="Remove this topic" onclick="popBubble('${b.id}','${b.color}')">×</span>
        `;
        field.appendChild(el);
      });

      updateBiasDisplay();
      updateEmptyState();
      updateRestoreBtn();
    }

    function popBubble(id, color) {
      const el = document.getElementById(id);
      if (!el || el.classList.contains('popping')) return;

      /* spawn shards BEFORE the element starts scaling,
         so positions are still accurate */
      spawnShards(el, color);

      el.classList.add('popping');
      poppedIds.add(id);

      setTimeout(() => {
        el.remove();
        updateBiasDisplay();
        updateEmptyState();
        updateRestoreBtn();
        updatePoppedCount();
      }, 480);
    }

    function restoreAll() {
      poppedIds.clear();
      renderBubbles();
      document.getElementById('poppedCount').textContent = '';
    }

    function updateBiasDisplay() {
      const remaining = BUBBLES
        .filter(b => !poppedIds.has(b.id))
        .reduce((s,b) => s + b.weight, 0);
      const pct = Math.round((remaining / BIAS_BASE) * 100);

      document.getElementById('biasValueNum').textContent = pct;
      document.getElementById('biasFill').style.width = pct + '%';

      const numEl   = document.getElementById('biasValueNum');
      const labelEl = document.getElementById('biasValueLabel');
      const fillEl  = document.getElementById('biasFill');

      if (pct <= 20) {
        numEl.style.color = labelEl.style.color = 'var(--success)';
        labelEl.textContent = '% BALANCED';
        fillEl.style.background = 'linear-gradient(90deg,var(--success),#8BC34A)';
      } else if (pct <= 50) {
        numEl.style.color = labelEl.style.color = 'var(--gold)';
        labelEl.textContent = '% MODERATE';
        fillEl.style.background = 'linear-gradient(90deg,var(--gold),var(--gold-lt))';
      } else {
        numEl.style.color = labelEl.style.color = 'var(--danger)';
        labelEl.textContent = '% BIASED';
        fillEl.style.background = 'linear-gradient(90deg,var(--danger),var(--gold))';
      }
    }

    function updateEmptyState() {
      document.getElementById('emptyState')
        .classList.toggle('visible', poppedIds.size >= BUBBLES.length);
    }
    function updateRestoreBtn() {
      document.getElementById('restoreBtn').style.display =
        poppedIds.size > 0 ? 'inline-block' : 'none';
    }
    function updatePoppedCount() {
      const el = document.getElementById('poppedCount');
      el.textContent = poppedIds.size > 0 ? poppedIds.size + ' topic(s) removed' : '';
    }

    renderBubbles();
  </script>
</body>
</html>
