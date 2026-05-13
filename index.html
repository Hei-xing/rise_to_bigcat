<!DOCTYPE html>
<html lang="ja">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>RISE TO BIGCAT — LΩPARA</title>
<link href="https://fonts.googleapis.com/css2?family=Nanum+Brush+Script&family=Bebas+Neue&family=Orbitron:wght@700;900&family=Rajdhani:wght@400;600;700&family=Share+Tech+Mono&display=swap" rel="stylesheet">
<style>
*{margin:0;padding:0;box-sizing:border-box;}

:root{
  --bg1:   #2a4aaa;
  --bg2:   #4a7acc;
  --bg3:   #5a9aaa;
  --bg4:   #7a6acc;
  --bg5:   #9a5aaa;
  --pink:  #ff44aa;
  --pink2: #ff88cc;
  --cyan:  #44ddff;
  --white: #ffffff;
  --ink:   #0a0820;
  --dim:   rgba(255,255,255,0.45);
  --panel: rgba(10,8,32,0.55);
  --border:rgba(255,255,255,0.15);
}

html{scroll-behavior:smooth;}

body{
  background: linear-gradient(160deg, #1a2a88 0%, #3a6aaa 25%, #4a8aaa 45%, #6a5aaa 70%, #8844aa 100%);
  background-attachment: fixed;
  color: var(--white);
  font-family: 'Rajdhani', sans-serif;
  font-weight: 600;
  min-height: 100vh;
  overflow-x: hidden;
}

/* ── グレイン ── */
body::before{
  content:'';
  position:fixed;inset:0;
  background-image:url("data:image/svg+xml,%3Csvg viewBox='0 0 200 200' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.9' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)'/%3E%3C/svg%3E");
  background-size:160px;opacity:0.04;pointer-events:none;z-index:0;mix-blend-mode:overlay;
}

/* ── ポスターフレーム ── */
.poster-frame{ display:none; }

/* ── ハザードマーク ── */
.hazard{ display:none; }
.hazard-lb{bottom:20px;left:20px;width:100px;height:60px;}
.hazard-rt{top:60px;right:20px;width:70px;height:42px;opacity:0.6;}
.hazard svg{width:100%;height:100%;}

/* ── STATUS BAR ── */
.status-bar{
  position:relative;z-index:10;
  display:flex;align-items:center;justify-content:space-between;
  padding:10px 24px;
  background:rgba(0,0,0,0.35);
  border-bottom:1px solid var(--border);
  backdrop-filter:blur(8px);
  font-size:11px;letter-spacing:3px;color:var(--dim);
}
.status-center{display:flex;align-items:center;gap:6px;}
.status-dot{width:5px;height:5px;border-radius:50%;background:var(--pink);animation:pulse 2s infinite;}
@keyframes pulse{0%,100%{opacity:1;}50%{opacity:0.2;}}
.status-dot:nth-child(2){animation-delay:.3s;}
.status-dot:nth-child(3){animation-delay:.6s;}

/* ── HERO ── */
.hero{
  position:relative;z-index:1;
  text-align:center;
  padding:36px 20px 28px;
}

.hero-topbar{
  display:flex;justify-content:space-between;align-items:flex-start;
  padding:0 4px;margin-bottom:20px;
  font-size:10px;letter-spacing:3px;color:var(--dim);line-height:1.8;
}
.hero-topbar-right{text-align:right;}

/* ── SVG LOGO ── */
.logo-wrap{width:100%;max-width:720px;margin:0 auto 8px;position:relative;}
.logo-svg{width:100%;height:auto;overflow:visible;}

/* ── COUNTDOWN ── */
.hero-countdown{
  display:flex;flex-direction:column;align-items:center;
  margin-top:20px;
}
.hero-countdown-label{
  font-size:10px;letter-spacing:2px;
  color:var(--dim);margin-bottom:12px;white-space:nowrap;
}
.hero-countdown-display{display:inline-flex;align-items:flex-start;}
.hcd-unit{display:flex;flex-direction:column;align-items:center;padding:0 10px;}
.hcd-num{
  font-family:'Orbitron',monospace;
  font-size:clamp(30px,7vw,56px);font-weight:900;
  color:var(--white);line-height:1;
  text-shadow: 0 2px 0 rgba(0,0,0,0.4), 0 0 8px rgba(255,68,170,0.3);
  -webkit-font-smoothing: antialiased;
  letter-spacing: 2px;
}
.hcd-label{font-size:9px;letter-spacing:2px;color:var(--dim);margin-top:4px;}
.hcd-sep{
  font-family:'Orbitron',monospace;
  font-size:clamp(20px,4vw,36px);font-weight:900;
  color:var(--pink);opacity:.5;padding-top:4px;line-height:1;
}

/* TICKET */
.share-btn{
  display:inline-flex;align-items:center;justify-content:center;gap:6px;
  padding:9px 8px;
  font-family:'Bebas Neue',sans-serif;
  font-size:18px;letter-spacing:4px;
  color:var(--white);
  background:rgba(10,30,120,0.55);
  border:1px solid rgba(100,150,255,0.4);
  text-decoration:none;
  white-space:nowrap;
  backdrop-filter:blur(8px);
  box-shadow:0 0 16px rgba(50,100,255,0.25);
  transition:transform .15s,box-shadow .2s;
}
.ticket-btn{
  display:inline-flex;align-items:center;justify-content:center;
  padding:9px 8px;
  font-family:'Bebas Neue',sans-serif;
  font-size:18px;letter-spacing:4px;
  color:var(--white);
  background:rgba(10,30,120,0.55);
  text-decoration:none;
  border:1px solid rgba(100,150,255,0.4);
  white-space:nowrap;
  text-align:center;
  backdrop-filter:blur(8px);
  box-shadow:0 0 16px rgba(50,100,255,0.25);
  transition:transform .15s,box-shadow .2s;
}

/* ── PANEL (共通UI枠) ── */
.panel{
  background:var(--panel);
  border:1px solid var(--border);
  backdrop-filter:blur(10px);
}
.panel-header{
  display:flex;align-items:center;justify-content:space-between;
  padding:10px 16px;
  border-bottom:1px solid var(--border);
  background:rgba(0,0,0,0.2);
}
.panel-title{
  font-family:'Bebas Neue',sans-serif;
  font-size:18px;letter-spacing:6px;color:var(--white);
}
.panel-hint{font-size:10px;letter-spacing:2px;color:var(--dim);}

/* ── DIVIDER ── */
.divider{
  position:relative;z-index:1;
  display:flex;align-items:center;gap:12px;
  padding:0 20px;margin:8px 0 0;
}
.divider::before,.divider::after{content:'';flex:1;height:1px;background:linear-gradient(90deg,transparent,rgba(255,255,255,0.2),transparent);}
.divider-text{font-size:9px;letter-spacing:5px;color:var(--dim);}

/* ── INTRO ── */
.intro{
  position:relative;z-index:1;
  max-width:640px;margin:24px auto 32px;
  padding:0 28px;text-align:center;
}
.intro-body{font-size:16px;line-height:2.1;color:rgba(255,255,255,0.7);font-weight:600;}
.intro-em{color:var(--pink);font-weight:700;}

/* ── CODES GRID ── */
.codes{
  position:relative;z-index:1;
  display:grid;grid-template-columns:repeat(2,1fr);
  gap:1px;
  background:rgba(255,255,255,0.06);
  border-top:1px solid var(--border);
  border-bottom:1px solid var(--border);
}
.code-card{
  background:var(--panel);
  backdrop-filter:blur(10px);
  padding:14px 16px;
  display:flex;align-items:center;gap:12px;
  cursor:default;position:relative;overflow:hidden;
  transition:background .2s;
}
.code-card::before{
  content:'';position:absolute;top:0;left:0;
  width:0;height:2px;background:var(--pink);
  transition:width .25s;
}
.code-card:hover{background:rgba(255,68,170,0.1);}
.code-card:hover::before{width:100%;}

.code-card.omega{
  grid-column:1/-1;
  background:rgba(255,68,170,0.12);
  border-top:2px solid var(--pink);
  padding:20px 24px;
}
.code-card.omega::before{background:var(--white);width:100%;}
.code-card.omega:hover{background:rgba(255,68,170,0.2);}

.code-num-block{
  flex-shrink:0;text-align:center;width:50px;
  border-right:1px solid rgba(255,255,255,0.1);
  margin-right:4px;padding-right:8px;
}
.code-num{font-size:9px;font-weight:700;color:var(--pink2);letter-spacing:2px;display:block;line-height:1.3;}
.code-num-id{font-family:'Bebas Neue',sans-serif;font-size:28px;color:rgba(255,255,255,0.9);display:block;line-height:1;}
.code-card.omega .code-num{color:var(--pink);}
.code-card.omega .code-num-id{font-size:44px;color:var(--pink);text-shadow:0 0 20px rgba(255,68,170,0.6);}
.code-body{flex:1;min-width:0;}
.code-label{font-family:'Bebas Neue',sans-serif;font-size:20px;color:var(--white);letter-spacing:2px;margin-bottom:1px;}
.code-card.omega .code-label{font-size:28px;color:var(--white);}
.code-kanji{font-size:10px;color:var(--dim);letter-spacing:2px;margin-bottom:3px;text-transform:uppercase;}
.code-card.omega .code-kanji{color:rgba(255,255,255,0.35);}
.code-desc{font-size:12px;color:rgba(255,255,255,0.5);line-height:1.5;font-weight:600;}
.code-card.omega .code-desc{font-size:13px;color:rgba(255,255,255,0.6);}

/* ── SECRET FILES ── */
.secret-section{position:relative;z-index:1;padding:0;}
.secret-file-list{padding:0;}
.secret-file{
  display:flex;align-items:center;gap:16px;
  padding:12px 20px;
  border-bottom:1px solid rgba(255,255,255,0.05);
  transition:background .2s;cursor:default;
}
.secret-file:hover{background:rgba(255,255,255,0.03);}
.secret-lock{font-size:13px;color:rgba(255,255,255,0.2);flex-shrink:0;width:16px;text-align:center;}
.secret-fname{font-size:13px;color:rgba(255,255,255,0.25);letter-spacing:2px;flex:1;font-weight:600;}
.secret-tag{
  font-size:9px;letter-spacing:2px;
  color:var(--pink2);border:1px solid rgba(255,136,204,0.3);
  padding:2px 8px;flex-shrink:0;font-weight:700;
}
.secret-statusbar{
  display:flex;justify-content:space-between;
  padding:8px 20px;
  background:rgba(0,0,0,0.2);
  border-top:1px solid rgba(255,255,255,0.05);
  font-size:9px;letter-spacing:2px;color:var(--dim);
}
.secret-blink{animation:blink 1.2s step-end infinite;}
@keyframes blink{0%,100%{opacity:1;}50%{opacity:0;}}

/* ── MODAL ── */
.modal-overlay{
  position:fixed;inset:0;
  background:rgba(5,0,20,0.88);
  z-index:10000;
  display:flex;align-items:center;justify-content:center;
  padding:24px;
  opacity:0;pointer-events:none;
  transition:opacity .25s;
  backdrop-filter:blur(8px);
}
.modal-overlay.open{opacity:1;pointer-events:all;}
.modal-box{
  background:linear-gradient(160deg,rgba(20,10,60,0.97),rgba(30,15,80,0.97));
  border:1px solid rgba(255,68,170,0.3);
  border-top:2px solid var(--pink);
  max-width:480px;width:100%;max-height:88vh;overflow-y:auto;
  padding:36px 32px 32px;
  position:relative;
  transform:translateY(12px);transition:transform .25s;
}
.modal-overlay.open .modal-box{transform:translateY(0);}
.modal-close{
  position:absolute;top:16px;right:16px;
  background:none;border:1px solid rgba(255,68,170,0.3);
  color:var(--dim);font-size:13px;
  width:30px;height:30px;cursor:default;
  display:flex;align-items:center;justify-content:center;
  font-family:'Share Tech Mono',monospace;
  transition:border-color .2s,color .2s;
}
.modal-close:hover{border-color:var(--pink);color:var(--pink);}
.modal-code-num{font-family:'Orbitron',monospace;font-size:10px;font-weight:700;letter-spacing:4px;color:var(--pink2);opacity:.7;margin-bottom:8px;}
.modal-title{font-family:'Bebas Neue',sans-serif;font-size:36px;color:var(--white);letter-spacing:3px;margin-bottom:4px;}
.modal-sub{font-size:11px;letter-spacing:2px;color:var(--dim);text-transform:uppercase;font-weight:600;}
.modal-divider{height:1px;background:rgba(255,68,170,0.25);margin:16px 0;}
.modal-body{font-size:15px;color:rgba(255,255,255,0.7);line-height:1.9;font-weight:600;}
.modal-body strong{color:var(--pink2);font-weight:700;}
.mi-event-title{font-family:'Bebas Neue',sans-serif;font-size:18px;color:var(--pink2);letter-spacing:2px;margin-bottom:14px;line-height:1.4;}
.mi-row{display:flex;gap:12px;margin-bottom:10px;font-size:14px;line-height:1.7;}
.mi-label{font-size:10px;letter-spacing:2px;color:var(--dim);flex-shrink:0;padding-top:2px;width:36px;font-weight:600;}
.mi-label-wide{width:120px;}
.mi-val{color:rgba(255,255,255,0.75);}
.mi-note{font-size:11px;color:rgba(255,255,255,0.35);display:block;margin-top:2px;font-weight:600;}
.mi-section-title{font-family:'Orbitron',monospace;font-size:9px;letter-spacing:4px;color:var(--pink2);opacity:.6;margin:16px 0 10px;padding-bottom:6px;border-bottom:1px solid rgba(255,68,170,0.15);}
.mi-ticket{border-left:2px solid rgba(255,255,255,0.1);padding:6px 0 6px 12px;margin-bottom:8px;}
.mi-ticket.omega-t{border-left-color:var(--pink);}
.mi-ticket.beta-t{border-left-color:rgba(255,136,204,0.5);}
.mi-ticket.alpha-t{border-left-color:rgba(255,255,255,0.15);}
.mi-ticket-name{font-family:'Bebas Neue',sans-serif;font-size:16px;color:var(--white);letter-spacing:1px;margin-bottom:2px;}
.mi-ticket-desc{font-size:12px;color:rgba(255,255,255,0.45);line-height:1.6;font-weight:600;}
.mi-tag{font-size:8px;background:rgba(255,68,170,0.15);color:var(--pink2);padding:1px 5px;border:1px solid rgba(255,68,170,0.3);font-weight:700;vertical-align:middle;letter-spacing:1px;}
.mi-footnote{font-size:10px;color:var(--dim);margin-top:12px;padding-top:8px;border-top:1px solid rgba(255,255,255,0.08);font-weight:600;}

/* ── FOOTER ── */
.footer{
  position:relative;z-index:1;
  display:flex;align-items:center;justify-content:space-between;
  padding:20px 24px 32px;
  border-top:1px solid var(--border);
  background:rgba(0,0,0,0.25);
}
.footer-logo{
  font-family:'Bebas Neue',sans-serif;
  font-size:24px;letter-spacing:6px;
  color:var(--white);opacity:.6;
}
.footer-sub{font-size:10px;letter-spacing:2px;color:var(--dim);text-align:right;line-height:1.9;}

/* responsive */
@media(max-width:600px){
  .codes{grid-template-columns:1fr;}
  .hcd-unit{padding:0 8px;}
  .poster-frame{inset:6px;}
}
.omega-char{font-family:'Orbitron',monospace!important;font-style:normal;}
</style>
</head>
<body>

<!-- ポスターフレーム -->
<div class="poster-frame"></div>

<!-- ハザードマーク 左下 -->
<div class="hazard hazard-lb">
  <svg viewBox="0 0 120 72" xmlns="http://www.w3.org/2000/svg">
    <defs>
      <pattern id="haz" x="0" y="0" width="24" height="24" patternUnits="userSpaceOnUse" patternTransform="rotate(-45)">
        <rect width="12" height="24" fill="rgba(0,0,0,0.7)"/>
        <rect x="12" width="12" height="24" fill="rgba(255,255,255,0.12)"/>
      </pattern>
    </defs>
    <rect width="120" height="72" fill="url(#haz)"/>
    <rect width="120" height="72" fill="none" stroke="rgba(255,255,255,0.2)" stroke-width="1.5"/>
  </svg>
</div>

<!-- ハザードマーク 右上 -->
<div class="hazard hazard-rt">
  <svg viewBox="0 0 120 72" xmlns="http://www.w3.org/2000/svg">
    <defs>
      <pattern id="haz2" x="0" y="0" width="20" height="20" patternUnits="userSpaceOnUse" patternTransform="rotate(-45)">
        <rect width="10" height="20" fill="rgba(0,0,0,0.6)"/>
        <rect x="10" width="10" height="20" fill="rgba(255,68,170,0.18)"/>
      </pattern>
    </defs>
    <rect width="120" height="72" fill="url(#haz2)"/>
    <rect width="120" height="72" fill="none" stroke="rgba(255,68,170,0.3)" stroke-width="1"/>
  </svg>
</div>

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
    <div>CITY ROCK IDOL<br>L<span class="omega-char">Ω</span>PARA</div>
    <div style="font-size:18px;opacity:.15;">⊕</div>
    <div class="hero-topbar-right">心斎橋 BIGCAT<br>2026.10.13 TUE</div>
  </div>

  <!-- SVGロゴ + 縦書きカタカナ -->
  <div class="logo-wrap">
    <svg class="logo-svg" viewBox="0 0 700 320" xmlns="http://www.w3.org/2000/svg">
      <defs>
        <!-- RISE TO: 白〜シアン -->
        <linearGradient id="g-rt" x1="0" y1="0" x2="0" y2="1">
          <stop offset="0%"  stop-color="#ffffff"/>
          <stop offset="40%" stop-color="#aaddff"/>
          <stop offset="100%" stop-color="#4488cc"/>
        </linearGradient>
        <!-- BIGCAT: 白〜ピンク〜パープル -->
        <linearGradient id="g-bc" x1="0" y1="0" x2="0" y2="1">
          <stop offset="0%"   stop-color="#ffffff"/>
          <stop offset="20%"  stop-color="#ffccee"/>
          <stop offset="50%"  stop-color="#ff44aa"/>
          <stop offset="80%"  stop-color="#aa22cc"/>
          <stop offset="100%" stop-color="#440088"/>
        </linearGradient>
        <!-- ハイライト -->
        <linearGradient id="g-hi" x1="0" y1="0" x2="0" y2="1">
          <stop offset="0%"  stop-color="white" stop-opacity="0.55"/>
          <stop offset="30%" stop-color="white" stop-opacity="0"/>
        </linearGradient>
        <!-- アウトライン -->
        <linearGradient id="g-out" x1="0" y1="0" x2="0" y2="1">
          <stop offset="0%"  stop-color="rgba(255,255,255,0.6)"/>
          <stop offset="100%" stop-color="rgba(180,100,255,0.4)"/>
        </linearGradient>
      </defs>

      <!-- RISE TO 手書き -->
      <text x="350" y="152" text-anchor="middle"
        font-family="'Nanum Brush Script',cursive"
        font-size="160" letter-spacing="2"
        fill="rgba(0,0,0,0.12)"
        transform="translate(3,4)">RISE TO</text>
      <text x="350" y="152" text-anchor="middle"
        font-family="'Nanum Brush Script',cursive"
        font-size="160" letter-spacing="2"
        fill="#0a0820">RISE TO</text>

      <!-- BIGCAT 本体（黒） -->
      <text x="350" y="310" text-anchor="middle"
        font-family="'Nanum Brush Script',cursive"
        font-size="250" letter-spacing="0"
        fill="rgba(0,0,0,0.1)"
        transform="translate(5,5)">BIGCAT</text>
      <text x="350" y="310" text-anchor="middle"
        font-family="'Nanum Brush Script',cursive"
        font-size="250" letter-spacing="0"
        fill="#0a0820">BIGCAT</text>
    </svg>
  </div>

    </div>
  </div>
  </div>

  <!-- COUNTDOWN -->
  <div class="hero-countdown">
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
    <div style="display:flex;align-items:stretch;justify-content:center;gap:12px;width:100%;max-width:280px;margin:16px auto 0;">
    <a class="ticket-btn" href="#" onclick="return false;" style="flex:1;text-align:center;">TICKET</a>
    <a class="share-btn" href="#" onclick="shareToX();return false;" style="flex:1;text-align:center;">
      <svg width="14" height="14" viewBox="0 0 24 24" fill="currentColor"><path d="M18.244 2.25h3.308l-7.227 8.26 8.502 11.24H16.17l-4.714-6.231-5.401 6.231H2.744l7.73-8.835L1.254 2.25H8.08l4.253 5.622zm-1.161 17.52h1.833L7.084 4.126H5.117z"/></svg>
      <span style="font-size:14px;letter-spacing:2px;">でシェア</span>
    </a>
    </div>
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
<div class="panel" style="margin:0 0 1px;">
  <div class="panel-header">
    <span class="panel-title">MISSION LOG</span>
    <span class="panel-hint">— TAP FOR DETAILS —</span>
  </div>
</div>

<div class="codes">
  <div class="code-card">
    <div class="code-num-block"><span class="code-num">CODE</span><span class="code-num-id">000</span></div>
    <div class="code-body"><div class="code-label">変身</div><div class="code-kanji">TRANSFORMATION</div><div class="code-desc">セカンド衣装導入 — 新たな姿が、加わる。</div></div>
  </div>
  <div class="code-card">
    <div class="code-num-block"><span class="code-num">CODE</span><span class="code-num-id">001</span></div>
    <div class="code-body"><div class="code-label">拡張</div><div class="code-kanji">EXPANSION</div><div class="code-desc">新グッズ発売 — 群のシンボルを纏え。</div></div>
  </div>
  <div class="code-card">
    <div class="code-num-block"><span class="code-num">CODE</span><span class="code-num-id">002</span></div>
    <div class="code-body"><div class="code-label">遭遇</div><div class="code-kanji">ENCOUNTER</div><div class="code-desc">CITYROCK 開催 — 街に熱が解き放たれる。</div></div>
  </div>
  <div class="code-card">
    <div class="code-num-block"><span class="code-num">CODE</span><span class="code-num-id">003</span></div>
    <div class="code-body"><div class="code-label">衝突</div><div class="code-kanji">COLLISION</div><div class="code-desc">3DAYS ツーマン企画 『RUN IT』</div></div>
  </div>
  <div class="code-card">
    <div class="code-num-block"><span class="code-num">CODE</span><span class="code-num-id">004</span></div>
    <div class="code-body"><div class="code-label">集結</div><div class="code-kanji">CONVERGENCE</div><div class="code-desc">3DAYS ワンマン企画 『SYNC』</div></div>
  </div>
  <div class="code-card">
    <div class="code-num-block"><span class="code-num">CODE</span><span class="code-num-id">005</span></div>
    <div class="code-body"><div class="code-label">加速</div><div class="code-kanji">ACCELERATION</div><div class="code-desc">6月5週連続シングルリリース — L<span class="omega-char">Ω</span>PARA渾身の五連撃。</div></div>
  </div>
  <div class="code-card omega">
    <div class="code-num-block"><span class="code-num">CODE</span><span class="code-num-id"><span class="omega-char">Ω</span></span></div>
    <div class="code-body"><div class="code-label">突破</div><div class="code-kanji">BREAKTHROUGH — 2周年記念ワンマンライブ in BIGCAT</div><div class="code-desc">誓いの場所へ、遂に辿り着く日。壁の向こうで待っているのは、BIGCATのステージだ。</div></div>
  </div>
</div>

<!-- SECRET FILES -->
<div class="secret-section" style="margin-top:1px;">
  <div class="panel">
    <div class="panel-header">
      <span class="panel-title">SECRET FILES</span>
      <span class="panel-hint">MORE FILES INCOMING_</span>
    </div>
    <div class="secret-file-list">
      <div class="secret-file"><div class="secret-lock">⊘</div><div class="secret-fname">????????????.wav</div><div class="secret-tag">LOCKED</div></div>
      <div class="secret-file"><div class="secret-lock">⊘</div><div class="secret-fname">????????????.jpg</div><div class="secret-tag">LOCKED</div></div>
      <div class="secret-file"><div class="secret-lock">⊘</div><div class="secret-fname">????????????.jpg</div><div class="secret-tag">LOCKED</div></div>
    </div>
    <div class="secret-statusbar"><span>3 items — ACCESS DENIED</span><span class="secret-blink">_</span></div>
  </div>
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
  <div class="footer-sub">CITY ROCK IDOL<br>since 2024.10.12<br>合同会社ミモロワークス</div>
</div>

<script>
const TARGET=new Date('2026-10-13T19:00:00+09:00');
function pad(n,l){return String(n).padStart(l,'0');}
function tick(){
  const d=TARGET-new Date();if(d<=0)return;
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
<div class="mi-row"><span class="mi-label mi-label-wide"><span class="omega-char">Ω</span>-ticket <span class="mi-tag">電子</span></span><span class="mi-val">¥15,000</span></div>
<div class="mi-row"><span class="mi-label mi-label-wide">β-ticket <span class="mi-tag">電子</span></span><span class="mi-val">¥6,000</span></div>
<div class="mi-row"><span class="mi-label mi-label-wide">α-ticket <span class="mi-tag">電子</span></span><span class="mi-val">¥1,000</span></div>
<div class="mi-row"><span class="mi-label mi-label-wide">α+-ticket <span class="mi-tag">手売</span></span><span class="mi-val">¥1,500</span></div>
<div class="mi-footnote">※ 全券種、入場時別途1ドリンク代必須</div>
<div class="mi-section-title">TICKET DETAILS</div>
<div class="mi-ticket omega-t"><div class="mi-ticket-name"><span class="omega-char">Ω</span>-ticket</div><div class="mi-ticket-desc">最優先入場・限定スウェット・アフターパーティー参加権・限定アクリルバングル・サイン入りフォトポスター（メンバー選択可能）</div></div>
<div class="mi-ticket beta-t"><div class="mi-ticket-name">β-ticket</div><div class="mi-ticket-desc">優先入場・アフターパーティー参加権・限定アクリルバングル</div></div>
<div class="mi-ticket alpha-t"><div class="mi-ticket-name">α-ticket <span class="mi-tag">電子</span></div><div class="mi-ticket-desc">一般入場のみ</div></div>
<div class="mi-ticket alpha-t"><div class="mi-ticket-name">α+-ticket <span class="mi-tag">手売</span></div><div class="mi-ticket-desc">一般入場のみ / 整理番号付与なし / アクキー型チケット<br><span class="mi-note">入場時にアクキーを提示すれば入場可能</span></div></div>`
  }
};

function shareToX(){
  const d = TARGET - new Date();
  const days  = Math.floor(d / 86400000);
  const hours = Math.floor((d % 86400000) / 3600000);
  const mins  = Math.floor((d % 3600000) / 60000);
  const secs  = Math.floor((d % 60000) / 1000);
  const text = `LΩPARAが魅せる、BIGCATへの軌跡\n「RISE TO BIGCAT」詳細情報はこちら▼\n\nLΩPARA 2周年記念ワンマンライブ 『MIDNIGHT DANCE AGAIN』まで...\n${days}日/${hours}時間/${mins}分/${secs}秒\n\n#RISETOBIGCAT #LΩPARABIGCATワンマンライブ2026 #ろーぱら`;
  const url = 'https://hei-xing.github.io/rise_to_bigcat/';
  window.open('https://twitter.com/intent/tweet?text=' + encodeURIComponent(text) + '&url=' + encodeURIComponent(url), '_blank');
}

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
