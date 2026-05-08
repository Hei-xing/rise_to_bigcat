<!DOCTYPE html>
<html lang="ja">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>RISE TO BIGCAT — LΩPARA</title>
<link href="https://fonts.googleapis.com/css2?family=Bebas+Neue&family=Orbitron:wght@700;900&family=Share+Tech+Mono&family=Rajdhani:wght@300;400;600;700&display=swap" rel="stylesheet">
<style>
* { margin:0; padding:0; box-sizing:border-box; }

:root {
  --white: #ffffff;
  --black: #080808;
  --gray:  #f0f0f0;
  --dim:   #999999;
  --accent:#0066ff;
}

html { scroll-behavior:smooth; }

body {
  background: #ffffff !important;
  color: var(--black);
  font-family: 'Rajdhani', sans-serif;
  min-height: 100vh;
  overflow-x: hidden;
}

/* ── コーナーマーカー（フライヤー四隅） ── */
.corner-mark {
  position: fixed;
  z-index: 100;
  pointer-events: none;
  width: 28px; height: 28px;
}
.corner-mark svg { width:100%;height:100%; }
.corner-mark.tl { top:12px;left:12px; }
.corner-mark.tr { top:12px;right:12px; }
.corner-mark.bl { bottom:12px;left:12px; }
.corner-mark.br { bottom:12px;right:12px; }

/* ── STATUS BAR ── */
.status-bar {
  position: relative; z-index: 10;
  display: flex; align-items: center; justify-content: space-between;
  padding: 10px 20px;
  border-bottom: 1px solid var(--black);
  font-family: 'Rajdhani', sans-serif;
  font-weight: 700;
  font-size: 13px; letter-spacing: 3px;
  color: var(--dim);
}
.status-center { display:flex;align-items:center;gap:6px; }
.status-dot { width:5px;height:5px;border-radius:50%;background:var(--black);animation:pulse 2s infinite; }
@keyframes pulse{0%,100%{opacity:1;}50%{opacity:0.25;}}
.status-dot:nth-child(2){animation-delay:.3s;}
.status-dot:nth-child(3){animation-delay:.6s;}

/* ── HERO ── */
.hero {
  position: relative; z-index: 1;
  padding: 32px 20px 28px;
  border-bottom: 1px solid var(--black);
}

/* フライヤー風 上部インフォ行 */
.hero-topbar {
  display: flex; justify-content: space-between; align-items: flex-start;
  margin-bottom: 28px;
  font-family: 'Rajdhani', sans-serif;
  font-weight: 600;
  font-size: 12px; letter-spacing: 2px; color: var(--dim);
  line-height: 1.8;
}
.hero-topbar-right { text-align: right; }

/* ブラケットフレーム */
.bracket-frame {
  position: relative;
  margin: 0 auto 4px;
  max-width: 720px;
  padding: 20px 24px;
}
.bracket-frame::before, .bracket-frame::after,
.bracket-frame .bf-bl, .bracket-frame .bf-br {
  content: '';
  position: absolute;
  width: 16px; height: 16px;
  border-color: var(--black);
  border-style: solid;
}
.bracket-frame::before { top:0;left:0;border-width:2px 0 0 2px; }
.bracket-frame::after  { top:0;right:0;border-width:2px 2px 0 0; }
.bracket-frame .bf-bl  { bottom:0;left:0;border-width:0 0 2px 2px; }
.bracket-frame .bf-br  { bottom:0;right:0;border-width:0 2px 2px 0; }

/* ── SVGロゴ ── */
.logo-wrap { width:100%;max-width:720px;margin:0 auto 4px; }
.logo-svg { width:100%;height:auto;overflow:visible; }

/* entername 風サブテキスト */
.logo-subtext {
  font-family: 'Rajdhani', sans-serif;
  font-weight: 600;
  text-align: center;
  font-size: 12px; letter-spacing: 6px;
  color: var(--dim);
  margin-bottom: 28px;
}

/* ── COUNTDOWN ── */
.hero-countdown {
  display: flex; flex-direction: column; align-items: center;
  border-top: 1px solid rgba(0,0,0,0.08);
  padding-top: 20px;
}
.hero-countdown-label {
  font-family: 'Rajdhani', sans-serif;
  font-weight: 600;
  font-size: 13px; letter-spacing: 2px;
  color: var(--dim); margin-bottom: 14px;
  white-space: nowrap;
}
.hero-countdown-display { display:inline-flex;align-items:flex-start; }
.hcd-unit { display:flex;flex-direction:column;align-items:center;padding:0 12px; }
.hcd-num {
  font-family: 'Orbitron', monospace;
  font-size: clamp(32px,7vw,60px); font-weight:900;
  color: var(--black); line-height:1;
}
.hcd-label { font-family:'Rajdhani',sans-serif;font-weight:600;font-size:11px;letter-spacing:2px;color:var(--dim);margin-top:4px; }
.hcd-sep {
  font-family: 'Orbitron', monospace;
  font-size: clamp(22px,5vw,42px); font-weight:900;
  color: var(--black); opacity:.2; padding-top:4px; line-height:1;
}

/* TICKET */
.ticket-btn {
  display: inline-block;
  margin-top: 22px; padding: 12px 52px;
  font-family: 'Bebas Neue', sans-serif;
  font-size: 20px; letter-spacing: 6px;
  color: var(--white);
  background: var(--black);
  text-decoration: none;
  border: 2px solid var(--black);
  transition: background .2s, color .2s;
  position: relative; overflow: hidden;
}
.ticket-btn::before {
  content: '';
  position: absolute; inset:0;
  background: linear-gradient(90deg,transparent,rgba(255,255,255,0.1),transparent);
  transform: translateX(-100%);
  transition: transform .4s;
}
.ticket-btn:hover { background: var(--white); color: var(--black); }
.ticket-btn:hover::before { transform: translateX(100%); }

/* ── DIVIDER ── */
.divider {
  position: relative; z-index:1;
  display: flex; align-items: center; gap: 12px;
  padding: 0 20px; margin: 0 0 24px;
}
.divider::before,.divider::after { content:'';flex:1;height:1px;background:var(--black);opacity:.12; }
.divider-text { font-family:'Rajdhani',sans-serif;font-weight:600;font-size:11px;letter-spacing:5px;color:var(--dim); }

/* ── INTRO ── */
.intro {
  position: relative; z-index:1;
  max-width: 640px; margin: 24px auto 36px;
  padding: 0 28px; text-align: center;
}
.intro-body { font-family:'Rajdhani',sans-serif;font-size:16px;line-height:2.1;color:rgba(0,0,0,0.6);font-weight:600; }
.intro-em { color: var(--black); font-weight:600; }

/* ── MISSION LOG ── */
.mission-log-header {
  position: relative; z-index:1;
  display: flex; align-items: center; justify-content: space-between;
  padding: 12px 20px;
  border-top: 1px solid var(--black);
  border-bottom: 1px solid rgba(0,0,0,0.1);
  margin-bottom: 0;
}
.mission-log-title {
  font-family: 'Bebas Neue', sans-serif;
  font-size: 18px; letter-spacing: 6px; color: var(--black);
}
.mission-log-hint { font-family:'Rajdhani',sans-serif;font-weight:600;font-size:11px;letter-spacing:3px;color:var(--dim); }

/* ── CODES GRID ── */
.codes {
  position: relative; z-index:1;
  display: grid; grid-template-columns: repeat(2,1fr);
  gap: 0;
  border-bottom: 1px solid var(--black);
}
.code-card {
  background: var(--white);
  padding: 14px 16px;
  display: flex; align-items: center; gap: 12px;
  cursor: pointer; position: relative; overflow: hidden;
  border-right: 1px solid rgba(0,0,0,0.08);
  border-bottom: 1px solid rgba(0,0,0,0.08);
  transition: background .2s;
}
.code-card:hover { background: var(--gray); }
.code-card::before {
  content:''; position:absolute;
  top:0;left:0;width:0;height:2px;
  background:var(--black);
  transition:width .25s;
}
.code-card:hover::before { width:100%; }

.code-card.omega {
  grid-column: 1/-1;
  background: var(--black);
  color: var(--white);
  border-right: none;
  border-bottom: none;
  padding: 20px 24px;
}
.code-card.omega::before { background:var(--white); }
.code-card.omega:hover { background: #111; }

.code-num-block { flex-shrink:0;text-align:center;width:52px;border-right:1px solid rgba(0,0,0,0.08);margin-right:4px;padding-right:8px; }
.code-num { font-family:'Rajdhani',sans-serif;font-size:10px;font-weight:700;color:var(--dim);letter-spacing:2px;display:block;line-height:1.3; }
.code-num-id {
  font-family:'Bebas Neue',sans-serif;
  font-size:28px;color:var(--black);display:block;line-height:1;
}
.code-card.omega .code-num { color:rgba(255,255,255,0.3); }
.code-card.omega .code-num-id { font-size:40px;color:rgba(255,255,255,0.9); }
.code-body { flex:1;min-width:0; }
.code-label {
  font-family:'Bebas Neue',sans-serif;
  font-size:18px;color:var(--black);letter-spacing:2px;margin-bottom:1px;
}
.code-card.omega .code-label { font-size:26px;color:var(--white); }
.code-kanji { font-family:'Rajdhani',sans-serif;font-weight:600;font-size:11px;color:var(--dim);letter-spacing:2px;margin-bottom:3px;text-transform:uppercase; }
.code-card.omega .code-kanji { color:rgba(255,255,255,0.3); }
.code-desc { font-family:'Rajdhani',sans-serif;font-size:13px;color:var(--dim);line-height:1.5;font-weight:600; }
.code-card.omega .code-desc { color:rgba(255,255,255,0.5);font-size:12px; }

/* ── SECRET FILES ── */
.secret-section { position:relative;z-index:1;padding:0 0 0; }
.secret-header {
  display:flex;align-items:center;justify-content:space-between;
  padding:12px 20px;
  border-top:1px solid rgba(0,0,0,0.1);
  border-bottom:1px solid rgba(0,0,0,0.06);
}
.secret-header-title { font-family:'Bebas Neue',sans-serif;font-size:18px;letter-spacing:6px;color:var(--black); }
.secret-header-sub { font-family:'Rajdhani',sans-serif;font-weight:600;font-size:12px;letter-spacing:2px;color:var(--dim); }
.secret-file-list { padding:0; }
.secret-file {
  display:flex;align-items:center;gap:16px;
  padding:12px 20px;
  border-bottom:1px solid rgba(0,0,0,0.06);
  transition:background .2s;cursor:default;
}
.secret-file:hover { background:var(--gray); }
.secret-lock { font-family:'Rajdhani',sans-serif;font-size:15px;color:rgba(0,0,0,0.2);flex-shrink:0;width:16px;text-align:center; }
.secret-fname { font-family:'Rajdhani',sans-serif;font-weight:600;font-size:14px;color:rgba(0,0,0,0.25);letter-spacing:2px;flex:1; }
.secret-tag { font-family:'Rajdhani',sans-serif;font-weight:700;font-size:11px;letter-spacing:2px;color:var(--dim);border:1px solid rgba(0,0,0,0.15);padding:2px 8px;flex-shrink:0; }
.secret-statusbar {
  display:flex;justify-content:space-between;
  padding:8px 20px;
  background:var(--gray);
  border-top:1px solid rgba(0,0,0,0.06);
  font-size:8px;letter-spacing:2px;color:var(--dim);
}
.secret-blink{animation:blink 1.2s step-end infinite;}
@keyframes blink{0%,100%{opacity:1;}50%{opacity:0;}}

/* ── MODAL ── */
.modal-overlay{position:fixed;inset:0;background:rgba(0,0,0,0.7);z-index:10000;display:flex;align-items:center;justify-content:center;padding:24px;opacity:0;pointer-events:none;transition:opacity .2s;backdrop-filter:blur(4px);}
.modal-overlay.open{opacity:1;pointer-events:all;}
.modal-box{background:var(--white);border-top:3px solid var(--black);max-width:480px;width:100%;max-height:88vh;overflow-y:auto;padding:36px 32px 32px;position:relative;transform:translateY(10px);transition:transform .2s;}
.modal-overlay.open .modal-box{transform:translateY(0);}
.modal-close{position:absolute;top:16px;right:16px;background:none;border:1px solid rgba(0,0,0,0.2);color:var(--dim);font-size:12px;width:28px;height:28px;cursor:pointer;display:flex;align-items:center;justify-content:center;font-family:'Rajdhani',sans-serif;font-weight:600;transition:border-color .2s,color .2s;}
.modal-close:hover{border-color:var(--black);color:var(--black);}
.modal-code-num{font-family:'Rajdhani',sans-serif;font-weight:600;font-size:12px;letter-spacing:4px;color:var(--dim);margin-bottom:8px;}
.modal-title{font-family:'Bebas Neue',sans-serif;font-size:34px;color:var(--black);letter-spacing:3px;margin-bottom:4px;}
.modal-sub{font-family:'Rajdhani',sans-serif;font-weight:600;font-size:12px;letter-spacing:2px;color:var(--dim);text-transform:uppercase;}
.modal-divider{height:1px;background:rgba(0,0,0,0.1);margin:16px 0;}
.modal-body{font-family:'Rajdhani',sans-serif;font-size:15px;color:rgba(0,0,0,0.65);line-height:1.9;font-weight:300;}
.modal-body strong{color:var(--black);font-weight:600;}
.mi-event-title{font-family:'Bebas Neue',sans-serif;font-size:18px;color:var(--black);letter-spacing:2px;margin-bottom:16px;}
.mi-row{display:flex;gap:12px;margin-bottom:10px;font-size:13px;line-height:1.7;}
.mi-label{font-family:'Rajdhani',sans-serif;font-weight:600;font-size:12px;letter-spacing:2px;color:var(--dim);flex-shrink:0;padding-top:2px;width:36px;}
.mi-val{color:rgba(0,0,0,0.75);}
.mi-note{font-family:'Rajdhani',sans-serif;font-weight:600;font-size:12px;color:var(--dim);display:block;margin-top:2px;}
.mi-section-title{font-family:'Rajdhani',sans-serif;font-weight:700;font-size:12px;letter-spacing:4px;color:var(--dim);margin:16px 0 10px;padding-bottom:6px;border-bottom:1px solid rgba(0,0,0,0.08);}
.mi-ticket{border-left:2px solid rgba(0,0,0,0.1);padding:6px 0 6px 12px;margin-bottom:8px;}
.mi-ticket.omega-t{border-left-color:var(--black);}
.mi-ticket.beta-t{border-left-color:rgba(0,0,0,0.35);}
.mi-ticket.alpha-t{border-left-color:rgba(0,0,0,0.15);}
.mi-ticket-name{font-family:'Bebas Neue',sans-serif;font-size:15px;color:var(--black);letter-spacing:1px;margin-bottom:2px;}
.mi-ticket-desc{font-family:'Rajdhani',sans-serif;font-weight:600;font-size:13px;color:var(--dim);line-height:1.6;}
.mi-price{color:var(--black);}
.mi-tag{font-family:'Rajdhani',sans-serif;font-weight:700;font-size:11px;background:rgba(0,0,0,0.05);color:var(--black);padding:1px 5px;border:1px solid rgba(0,0,0,0.2);vertical-align:middle;letter-spacing:1px;}
.mi-footnote{font-family:'Rajdhani',sans-serif;font-weight:600;font-size:12px;color:var(--dim);margin-top:12px;padding-top:8px;border-top:1px solid rgba(0,0,0,0.08);}

/* ── FOOTER ── */
.footer {
  position: relative; z-index:1;
  display: flex; align-items: center; justify-content: space-between;
  padding: 20px 20px;
  border-top: 2px solid var(--black);
}
.footer-logo { font-family:'Bebas Neue',sans-serif;font-size:22px;letter-spacing:6px;color:var(--black); }
.footer-sub { font-family:'Rajdhani',sans-serif;font-weight:600;font-size:11px;letter-spacing:2px;color:var(--dim);text-align:right;line-height:1.8; }



/* responsive */
@media(max-width:600px){
  .codes{grid-template-columns:1fr;}
  .code-card{border-right:none;}
  .hcd-unit{padding:0 8px;}
  .footer{flex-direction:column;gap:8px;text-align:center;}
  .footer-sub{text-align:center;}
}

.omega-char{font-family:'Orbitron',monospace!important;font-style:normal;}
</style>
</head>
<body>

<!-- コーナーマーカー -->
<div class="corner-mark tl"><svg viewBox="0 0 28 28"><path d="M0 28 L0 0 L28 0" fill="none" stroke="#080808" stroke-width="2"/></svg></div>
<div class="corner-mark tr"><svg viewBox="0 0 28 28"><path d="M28 28 L28 0 L0 0" fill="none" stroke="#080808" stroke-width="2"/></svg></div>
<div class="corner-mark bl"><svg viewBox="0 0 28 28"><path d="M0 0 L0 28 L28 28" fill="none" stroke="#080808" stroke-width="2"/></svg></div>
<div class="corner-mark br"><svg viewBox="0 0 28 28"><path d="M28 0 L28 28 L0 28" fill="none" stroke="#080808" stroke-width="2"/></svg></div>

<!-- STATUS BAR -->
<div class="status-bar">
  <span>L<span class="omega-char">Ω</span>PARA / 2026</span>
  <div class="status-center">
    <div class="status-dot"></div>
    <div class="status-dot"></div>
    <div class="status-dot"></div>
    <span>MISSION ACTIVE</span>
  </div>
  <span>RISE_TO_BIGCAT.exe</span>
</div>

<!-- HERO -->
<div class="hero">

  <div class="hero-topbar">
    <div>
      CITY ROCK IDOL<br>
      L<span class="omega-char">Ω</span>PARA
    </div>
    <div style="text-align:center;font-size:16px;opacity:0.15;">⊕</div>
    <div class="hero-topbar-right">
      心斎橋 BIGCAT<br>
      2026.10.13 TUE
    </div>
  </div>

  <!-- SVGロゴ -->
  <div class="logo-wrap">
    <div class="bracket-frame">
      <div class="bf-bl"></div>
      <div class="bf-br"></div>
      <svg class="logo-svg" viewBox="0 0 700 240" xmlns="http://www.w3.org/2000/svg">
        <defs>
          <!-- 黒インクグラデ（フライヤーの質感） -->
          <linearGradient id="ink-rt" x1="0" y1="0" x2="0" y2="1">
            <stop offset="0%"  stop-color="#1a1a1a"/>
            <stop offset="40%" stop-color="#080808"/>
            <stop offset="100%" stop-color="#000000"/>
          </linearGradient>
          <linearGradient id="ink-bc" x1="0" y1="0" x2="0" y2="1">
            <stop offset="0%"  stop-color="#2a2a2a"/>
            <stop offset="20%" stop-color="#0a0a0a"/>
            <stop offset="100%" stop-color="#000000"/>
          </linearGradient>
          <!-- ハイライト（エッジ光） -->
          <linearGradient id="edge-hi" x1="0" y1="0" x2="0" y2="1">
            <stop offset="0%"  stop-color="white" stop-opacity="0.3"/>
            <stop offset="30%" stop-color="white" stop-opacity="0"/>
          </linearGradient>
        </defs>

        <!-- RISE TO -->
        <!-- シャドウ -->
        <text x="350" y="80" text-anchor="middle"
          font-family="'Bebas Neue',sans-serif" font-size="78" letter-spacing="20"
          fill="rgba(0,0,0,0.08)"
          transform="translate(3,4) skewX(-6)">RISE TO</text>
        <!-- アウトライン -->
        <text x="350" y="80" text-anchor="middle"
          font-family="'Bebas Neue',sans-serif" font-size="78" letter-spacing="20"
          fill="none" stroke="#080808" stroke-width="3"
          transform="skewX(-6)">RISE TO</text>
        <!-- 本体 -->
        <text x="350" y="80" text-anchor="middle"
          font-family="'Bebas Neue',sans-serif" font-size="78" letter-spacing="20"
          fill="url(#ink-rt)" transform="skewX(-6)">RISE TO</text>
        <!-- エッジハイライト -->
        <text x="350" y="80" text-anchor="middle"
          font-family="'Bebas Neue',sans-serif" font-size="78" letter-spacing="20"
          fill="url(#edge-hi)" transform="skewX(-6)">RISE TO</text>

        <!-- BIGCAT -->
        <!-- シャドウ -->
        <text x="350" y="212" text-anchor="middle"
          font-family="'Bebas Neue',sans-serif" font-size="172" letter-spacing="0"
          fill="rgba(0,0,0,0.06)"
          transform="translate(4,5) skewX(-6)">BIGCAT</text>
        <!-- アウトライン -->
        <text x="350" y="212" text-anchor="middle"
          font-family="'Bebas Neue',sans-serif" font-size="172" letter-spacing="0"
          fill="none" stroke="#080808" stroke-width="4"
          transform="skewX(-6)">BIGCAT</text>
        <!-- 本体 -->
        <text x="350" y="212" text-anchor="middle"
          font-family="'Bebas Neue',sans-serif" font-size="172" letter-spacing="0"
          fill="url(#ink-bc)" transform="skewX(-6)">BIGCAT</text>
        <!-- エッジハイライト -->
        <text x="350" y="212" text-anchor="middle"
          font-family="'Bebas Neue',sans-serif" font-size="172" letter-spacing="0"
          fill="url(#edge-hi)" transform="skewX(-6)">BIGCAT</text>
      </svg>
    </div>
  </div>

  <div class="logo-subtext">enter name...</div>



  <!-- COUNTDOWN -->
  <div class="hero-countdown" style="padding:24px 0 8px;">
    <div class="hero-countdown-label" style="white-space:nowrap;">BIGCAT ワンマンライブ 「MIDNIGHT DANCE AGAIN」まで</div>
    <div class="hero-countdown-display">
      <div class="hcd-unit"><div class="hcd-num" id="cd-d">000</div><div class="hcd-label">DAYS</div></div>
      <div class="hcd-sep">:</div>
      <div class="hcd-unit"><div class="hcd-num" id="cd-h">00</div><div class="hcd-label">HRS</div></div>
      <div class="hcd-sep">:</div>
      <div class="hcd-unit"><div class="hcd-num" id="cd-m">00</div><div class="hcd-label">MIN</div></div>
      <div class="hcd-sep">:</div>
      <div class="hcd-unit"><div class="hcd-num" id="cd-s">00</div><div class="hcd-label">SEC</div></div>
    </div>
    <a class="ticket-btn" href="#" onclick="return false;">TICKET</a>
  </div>
</div>

<!-- INTRO -->
<div class="intro">
  <p class="intro-body">
    誰かの通った道をただ進むのではなく、<br>
    そり立つ壁を乗り越えて<span class="intro-em">這い上がっていく。</span><br><br>
    RISE TO BIGCATは<br>
    私たちの覚悟を証明する<span class="intro-em">誓いの言葉</span>です。
  </p>
</div>

<!-- MISSION LOG -->
<div class="mission-log-header">
  <span class="mission-log-title">MISSION LOG</span>
  <span class="mission-log-hint">— TAP FOR DETAILS —</span>
</div>

<div class="codes">
  <div class="code-card" onclick="openModal('000')">
    <div class="code-num-block"><span class="code-num">CODE</span><span class="code-num-id">000</span></div>
    <div class="code-body"><div class="code-label">変身</div><div class="code-kanji">TRANSFORMATION</div><div class="code-desc">セカンド衣装導入 — 新たな姿が、加わる。</div></div>
  </div>
  <div class="code-card" onclick="openModal('001')">
    <div class="code-num-block"><span class="code-num">CODE</span><span class="code-num-id">001</span></div>
    <div class="code-body"><div class="code-label">拡張</div><div class="code-kanji">EXPANSION</div><div class="code-desc">新グッズ発売 — 群のシンボルを纏え。</div></div>
  </div>
  <div class="code-card" onclick="openModal('002')">
    <div class="code-num-block"><span class="code-num">CODE</span><span class="code-num-id">002</span></div>
    <div class="code-body"><div class="code-label">遭遇</div><div class="code-kanji">ENCOUNTER</div><div class="code-desc">CITYROCK 開催 — 街に熱が解き放たれる。</div></div>
  </div>
  <div class="code-card" onclick="openModal('003')">
    <div class="code-num-block"><span class="code-num">CODE</span><span class="code-num-id">003</span></div>
    <div class="code-body"><div class="code-label">衝突</div><div class="code-kanji">COLLISION</div><div class="code-desc">3DAYS ツーマン企画 『RUN IT』</div></div>
  </div>
  <div class="code-card" onclick="openModal('004')">
    <div class="code-num-block"><span class="code-num">CODE</span><span class="code-num-id">004</span></div>
    <div class="code-body"><div class="code-label">集結</div><div class="code-kanji">CONVERGENCE</div><div class="code-desc">3DAYS ワンマン企画 『SYNC』</div></div>
  </div>
  <div class="code-card" onclick="openModal('005')">
    <div class="code-num-block"><span class="code-num">CODE</span><span class="code-num-id">005</span></div>
    <div class="code-body"><div class="code-label">加速</div><div class="code-kanji">ACCELERATION</div><div class="code-desc">6月5週連続シングルリリース — 五連撃。</div></div>
  </div>
  <div class="code-card omega" onclick="openModal('omega')">
    <div class="code-num-block"><span class="code-num">CODE</span><span class="code-num-id"><span class="omega-char">Ω</span></span></div>
    <div class="code-body"><div class="code-label">突破</div><div class="code-kanji">BREAKTHROUGH — 2周年記念ワンマンライブ in BIGCAT</div><div class="code-desc">誓いの場所へ、遂に辿り着く日。壁の向こうで待っているのは、BIGCATのステージだ。</div></div>
  </div>
</div>

<!-- SECRET FILES -->
<div class="secret-section">
  <div class="secret-header">
    <span class="secret-header-title">SECRET FILES</span>
    <span class="secret-header-sub">MORE FILES INCOMING_</span>
  </div>
  <div class="secret-file-list">
    <div class="secret-file"><div class="secret-lock">⊘</div><div class="secret-fname">????????????.wav</div><div class="secret-tag">LOCKED</div></div>
    <div class="secret-file"><div class="secret-lock">⊘</div><div class="secret-fname">????????????.jpg</div><div class="secret-tag">LOCKED</div></div>
    <div class="secret-file"><div class="secret-lock">⊘</div><div class="secret-fname">????????????.jpg</div><div class="secret-tag">LOCKED</div></div>
  </div>
  <div class="secret-statusbar"><span>3 items — ACCESS DENIED</span><span class="secret-blink">_</span></div>
</div>

<!-- MODAL -->
<div class="modal-overlay" id="modal-overlay" onclick="closeModal()">
  <div class="modal-box" onclick="event.stopPropagation()">
    <button class="modal-close" onclick="closeModal()">✕</button>
    <div class="modal-code-num" id="modal-code-num"></div>
    <div class="modal-title" id="modal-title"></div>
    <div class="modal-sub" id="modal-sub"></div>
    <div class="modal-divider"></div>
    <div class="modal-body" id="modal-body"></div>
  </div>
</div>

<!-- FOOTER -->
<div class="footer">
  <div class="footer-logo">L<span class="omega-char">Ω</span>PARA</div>
  <div class="footer-sub">
    CITY ROCK IDOL<br>
    since 2024.10.12<br>
    合同会社ミモロワークス
  </div>
</div>

<script>
const TARGET=new Date('2026-10-13T19:00:00+09:00');
function pad(n,l){return String(n).padStart(l,'0');}
function tick(){
  const d=TARGET-new Date(); if(d<=0)return;
  document.getElementById('cd-d').textContent=pad(Math.floor(d/86400000),3);
  document.getElementById('cd-h').textContent=pad(Math.floor((d%86400000)/3600000),2);
  document.getElementById('cd-m').textContent=pad(Math.floor((d%3600000)/60000),2);
  document.getElementById('cd-s').textContent=pad(Math.floor((d%60000)/1000),2);
}
setInterval(tick,1000);tick();

const CODES={
  '000':{
    num:'CODE 000',title:'変身',sub:'TRANSFORMATION — セカンド衣装導入',
    body:`<div class="mi-event-title">第二の刃、第二の装い。<br>L<span class="omega-char">Ω</span>PARAのもう一つの顔が日の目を浴びる。</div>
<p style="line-height:1.9;">現在のライブ衣装に加え、<strong>新たにセカンド衣装を導入!!!</strong><br><br>
セカンド衣装での不定期ライブ参戦や限定グッズ等を販売予定!!!</p>`
  },
  '001':{
    num:'CODE 001',title:'拡張',sub:'EXPANSION — 新グッズ発売',
    body:`<div class="mi-event-title">広がる仲間の印。群のシンボルを纏い、L<span class="omega-char">Ω</span>PARAを紡げ。</div>
<p style="line-height:1.9;"><strong>全4種類からなる新デザインTシャツの発売決定!!!</strong><br><br>
さらに他にも新グッズが続々登場予定!!!!</p>`
  },
  '002':{
    num:'CODE 002',title:'遭遇',sub:'ENCOUNTER — CITYROCK開催',
    body:`<div class="mi-event-title">L<span class="omega-char">Ω</span>PARAの熱が街に溢れ出す。新しい出会いの日。</div>
<p style="line-height:1.9;"><strong>L<span class="omega-char">Ω</span>PARA × ESAKA MUSE共催イベント『CITY ROCK』開催決定!!!</strong><br><br>
過去ソールドアウトも記録したL<span class="omega-char">Ω</span>PARAの代名詞のイベントが満を持して復活!!!</p>`
  },
  '003':{
    num:'CODE 003',title:'衝突',sub:'COLLISION — 3DAYS ツーマン企画『RUN IT』',
    body:`<div class="mi-event-title">Σ'sよ、立ち上がるのだ。雌雄を結するその日に、君の力を貸してくれ。</div>
<p style="margin-bottom:14px;line-height:1.9;"><strong>L<span class="omega-char">Ω</span>PARA主催3DAYツーマン企画『RUN IT』開催決定!!!</strong></p>
<div class="mi-row"><span class="mi-label">会場</span><span class="mi-val">BEYOND<br><span class="mi-note">〒542-0086 大阪府大阪市中央区西心斎橋2-18-9 リアライズ西心斎橋B2F</span></span></div>
<div class="mi-row"><span class="mi-label">時間</span><span class="mi-val">OPEN 19:00 / START 19:30</span></div>
<div class="mi-row"><span class="mi-label">料金</span><span class="mi-val">Adv ¥2,000 / Door ¥2,500</span></div>
<div class="mi-section-title">SCHEDULE</div>
<div class="mi-ticket omega-t"><div class="mi-ticket-name">- RAID 01 - <span style="font-size:11px;opacity:0.5;">2026年6月10日（月）</span></div><div class="mi-ticket-desc">L<span class="omega-char">Ω</span>PARA × ENVY PARANOID<br><span class="mi-note">『戦友』</span></div></div>
<div class="mi-ticket beta-t"><div class="mi-ticket-name">- RAID 02 - <span style="font-size:11px;opacity:0.5;">2026年7月27日（月）</span></div><div class="mi-ticket-desc">L<span class="omega-char">Ω</span>PARA × LØISLOID<br><span class="mi-note">『師兄』</span></div></div>
<div class="mi-ticket beta-t"><div class="mi-ticket-name">- RAID 03 - <span style="font-size:11px;opacity:0.5;">2026年8月18日（月）</span></div><div class="mi-ticket-desc">L<span class="omega-char">Ω</span>PARA × AZ-ON<br><span class="mi-note">『巨壁』</span></div></div>`
  },
  '004':{
    num:'CODE 004',title:'集結',sub:'CONVERGENCE — 3DAYS ワンマン企画『SYNC』',
    body:`<div class="mi-event-title">混同する波長が交わる日。君はもうL<span class="omega-char">Ω</span>PARAから抜け出せない。</div>
<p style="line-height:1.9;"><strong>3DAYSワンマン企画『SYNC』開催決定!!!</strong><br><br>
出会い、共に戦った者同士で熱を高め合う革命前哨戦。</p>`
  },
  '005':{
    num:'CODE 005',title:'加速',sub:'ACCELERATION — 6月5週シングル連続リリース',
    body:`<div class="mi-event-title">駆け抜ける良音の閃光。君はついて来れるのか？</div>
<p style="line-height:1.9;"><strong>5週連続シングルリリース決定!!!!</strong><br><br>
一切の手抜きなし!!!L<span class="omega-char">Ω</span>PARA渾身の五連撃。</p>`
  },
  'omega':{
    num:'CODE Ω — FINAL MISSION',title:'突破',sub:'L<span class="omega-char">Ω</span>PARA 2nd Anniversary One-Man Live',
    body:`<div class="mi-event-title">約束の場所で全てが覆る。衝撃に備えよ。</div>
<p style="margin-bottom:16px;line-height:1.9;">L<span class="omega-char">Ω</span>PARAデビュー2周年記念ワンマンライブ<br>
すべてはこの日のため。君との約束を果たすため。<br>
<strong>必ずBIGCATで会いましょう。</strong></p>
<div class="mi-event-title" style="font-size:17px;margin-bottom:16px;">『MIDNIGHT DANCE AGAIN』</div>
<div class="mi-row"><span class="mi-label">日程</span><span class="mi-val">2026年10月13日（火）</span></div>
<div class="mi-row"><span class="mi-label">場所</span><span class="mi-val">心斎橋 BIGCAT</span></div>
<div class="mi-row"><span class="mi-label">時間</span><span class="mi-val">OPEN 18:30 / START 19:00<br><span class="mi-note">終演 20:45〜21:00 予定 / 終演後物販 21:30〜24:00 @CIRCUS OSAKA（1D不要）</span></span></div>
<div class="mi-section-title">PRICE</div>
<div class="mi-row"><span class="mi-label" style="width:80px;"><span class="omega-char">Ω</span>-ticket</span><span class="mi-val">¥15,000</span></div>
<div class="mi-row"><span class="mi-label" style="width:80px;">β-ticket</span><span class="mi-val">¥6,000</span></div>
<div class="mi-row"><span class="mi-label" style="width:80px;">α-ticket <span class="mi-tag">電子</span></span><span class="mi-val">¥1,000</span></div>
<div class="mi-row"><span class="mi-label" style="width:80px;">α+-ticket <span class="mi-tag">手売</span></span><span class="mi-val">¥1,500</span></div>
<div class="mi-footnote">※ 全券種、入場時別途1ドリンク代必須</div>
<div class="mi-section-title">TICKET DETAILS</div>
<div class="mi-ticket omega-t"><div class="mi-ticket-name"><span class="omega-char">Ω</span>-ticket</div><div class="mi-ticket-desc">最優先入場・限定スウェット・アフターパーティー参加権・限定アクリルバングル・サイン入りフォトポスター（メンバー選択可能）</div></div>
<div class="mi-ticket beta-t"><div class="mi-ticket-name">β-ticket</div><div class="mi-ticket-desc">優先入場・アフターパーティー参加権・限定アクリルバングル</div></div>
<div class="mi-ticket alpha-t"><div class="mi-ticket-name">α-ticket <span class="mi-tag">電子</span></div><div class="mi-ticket-desc">一般入場のみ</div></div>
<div class="mi-ticket alpha-t"><div class="mi-ticket-name">α+-ticket <span class="mi-tag">手売</span></div><div class="mi-ticket-desc">一般入場のみ / 整理番号付与なし / アクキー型チケット<br><span class="mi-note">入場時にアクキーを提示すれば入場可能</span></div></div>`
  }
};

function openModal(code){
  const d=CODES[code];if(!d)return;
  document.getElementById('modal-code-num').innerHTML=d.num;
  document.getElementById('modal-title').innerHTML=d.title;
  document.getElementById('modal-sub').innerHTML=d.sub;
  document.getElementById('modal-body').innerHTML=d.body;
  document.getElementById('modal-overlay').classList.add('open');
  document.body.style.overflow='hidden';
}
function closeModal(){
  document.getElementById('modal-overlay').classList.remove('open');
  document.body.style.overflow='';
}
document.addEventListener('keydown',e=>{if(e.key==='Escape')closeModal();});
</script>
</body>
</html>
