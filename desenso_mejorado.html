<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Dungeon Descent</title>
<link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@400;700;900&family=Crimson+Text:ital,wght@0,400;0,600;1,400&display=swap" rel="stylesheet">
<style>
:root{--bg:#0a0608;--stone:#1a1418;--stone2:#241c20;--gold:#c9922a;--gold2:#f0bc5a;--blood2:#c0392b;--text:#e8d5b7;--text2:#a89070;--border:#3d2f1e;}
*{margin:0;padding:0;box-sizing:border-box;}
body{background:var(--bg);color:var(--text);font-family:'Crimson Text',serif;overflow:hidden;height:100vh;user-select:none;}
canvas{display:block;}
.screen{position:fixed;inset:0;display:flex;align-items:center;justify-content:center;}
.screen.hidden{display:none;}

#menuScreen{background:radial-gradient(ellipse at 50% 30%,#1a0e0a 0%,#080507 70%);flex-direction:column;z-index:50;}
.torches{position:absolute;inset:0;pointer-events:none;}
.torch{position:absolute;width:8px;height:30px;background:linear-gradient(to top,#8b4513,#c9922a);border-radius:2px;}
.torch::after{content:'';position:absolute;top:-16px;left:-6px;width:20px;height:22px;background:radial-gradient(ellipse,#f0bc5a 0%,#e85d04 40%,transparent 70%);border-radius:50%;animation:flicker 1.2s ease-in-out infinite alternate;}
.torch.t1{top:10%;left:7%;}.torch.t2{top:10%;right:7%;}.torch.t3{bottom:15%;left:4%;}.torch.t4{bottom:15%;right:4%;}
@keyframes flicker{from{opacity:.7;transform:scaleX(.8);}to{opacity:1;transform:scaleX(1.1);}}

.menu-content{position:relative;z-index:2;width:100%;display:flex;flex-direction:column;align-items:center;}
.game-title{font-family:'Cinzel',serif;font-size:clamp(2rem,5vw,4rem);font-weight:900;color:var(--gold2);letter-spacing:.12em;text-align:center;text-shadow:0 0 30px rgba(201,146,42,.7),0 4px 8px #000;animation:tp 3s ease-in-out infinite;}
@keyframes tp{0%,100%{text-shadow:0 0 30px rgba(201,146,42,.6),0 4px 8px #000;}50%{text-shadow:0 0 55px rgba(240,188,90,.95),0 4px 8px #000;}}
.game-subtitle{font-family:'Cinzel',serif;font-size:clamp(.65rem,1.2vw,.9rem);color:var(--text2);letter-spacing:.4em;margin-top:.3rem;text-align:center;}
.sep{width:280px;height:2px;margin:.8rem auto;background:linear-gradient(to right,transparent,var(--gold),var(--gold2),var(--gold),transparent);}

/* CLASS CARDS */
.class-section{width:100%;max-width:1000px;padding:0 1rem;}
.section-label{font-family:'Cinzel',serif;font-size:.75rem;letter-spacing:.3em;color:var(--text2);text-align:center;margin-bottom:.6rem;}
.class-grid{display:grid;grid-template-columns:repeat(4,1fr);gap:.7rem;}
.class-card{background:var(--stone);border:2px solid var(--border);border-radius:6px;padding:.85rem .7rem;cursor:pointer;transition:all .25s;display:flex;flex-direction:column;align-items:center;gap:.3rem;position:relative;overflow:hidden;}
.class-card:hover{transform:translateY(-4px);box-shadow:0 8px 25px rgba(0,0,0,.5);}
.class-card.selected{box-shadow:0 0 20px rgba(201,146,42,.25);}
.class-card.selected::after{content:'✦ ELEGIDO ✦';position:absolute;bottom:0;left:0;right:0;font-family:'Cinzel',serif;font-size:.48rem;letter-spacing:.15em;background:var(--cc,var(--gold));color:#000;padding:.22rem;text-align:center;font-weight:700;}
.warrior-card{--cc:#c9922a;}.warrior-card:hover,.warrior-card.selected{border-color:#c9922a;}
.summoner-card{--cc:#9333ea;}.summoner-card:hover,.summoner-card.selected{border-color:#9333ea;}
.mage-card{--cc:#4cc9f0;}.mage-card:hover,.mage-card.selected{border-color:#4cc9f0;}
.assassin-card{--cc:#4a9e3f;}.assassin-card:hover,.assassin-card.selected{border-color:#4a9e3f;}
.ci{width:40px;height:40px;border-radius:50%;display:flex;align-items:center;justify-content:center;font-size:1.2rem;font-weight:900;}
.warrior-card .ci{background:rgba(201,146,42,.18);color:#c9922a;}
.summoner-card .ci{background:rgba(147,51,234,.18);color:#9333ea;}
.mage-card .ci{background:rgba(76,201,240,.18);color:#4cc9f0;}
.assassin-card .ci{background:rgba(74,158,63,.18);color:#4a9e3f;}
.cn{font-family:'Cinzel',serif;font-size:.78rem;font-weight:700;letter-spacing:.08em;color:var(--cc,var(--gold));}
.cs{font-size:.7rem;color:var(--text2);text-align:center;line-height:1.5;}

/* ABILITY PREVIEW in menu */
.ab-preview{width:100%;margin-top:.3rem;border-top:1px solid rgba(255,255,255,.07);padding-top:.3rem;display:flex;flex-direction:column;gap:.2rem;}
.ab-row{display:flex;align-items:center;gap:.3rem;}
.ab-key{font-family:'Cinzel',serif;font-size:.5rem;background:rgba(0,0,0,.4);border:1px solid rgba(255,255,255,.15);border-radius:2px;padding:.1rem .25rem;color:var(--text2);min-width:14px;text-align:center;}
.ab-name{font-size:.58rem;color:var(--text);flex:1;}
.ab-lv{font-size:.5rem;color:var(--text2);}

.start-btn{margin-top:.9rem;padding:.72rem 2.6rem;font-family:'Cinzel',serif;font-size:.92rem;font-weight:700;letter-spacing:.2em;background:linear-gradient(135deg,#7a5a10,var(--gold),#7a5a10);color:#0a0608;border:none;cursor:pointer;border-radius:2px;transition:all .2s;text-transform:uppercase;box-shadow:0 0 20px rgba(201,146,42,.35);}
.start-btn:hover{transform:translateY(-2px);box-shadow:0 0 40px rgba(240,188,90,.55);}
.continue-btn{padding:.52rem 2rem;font-family:'Cinzel',serif;font-size:.78rem;font-weight:700;letter-spacing:.18em;background:rgba(10,6,8,.85);color:var(--gold2);border:1px solid rgba(201,146,42,.5);cursor:pointer;border-radius:2px;transition:all .2s;text-transform:uppercase;}
.continue-btn:hover{background:rgba(201,146,42,.15);border-color:var(--gold2);transform:translateY(-2px);}
.continue-btn:disabled{opacity:.3;cursor:not-allowed;transform:none;}

/* HUD */
#hud{position:fixed;inset:0;pointer-events:none;z-index:10;padding:.75rem;}
#hud.hidden{display:none;}
.hud-top{display:flex;justify-content:space-between;align-items:flex-start;}
.hud-panel{background:rgba(10,6,8,.88);border:1px solid rgba(201,146,42,.28);border-radius:3px;padding:.42rem .65rem;backdrop-filter:blur(2px);}
.stat-row{display:flex;align-items:center;gap:.42rem;font-size:.77rem;}
.bar-wrap{width:125px;height:7px;background:#1a0e0f;border-radius:2px;overflow:hidden;}
.bar-fill{height:100%;border-radius:2px;transition:width .22s;}
.hp-bar{background:linear-gradient(90deg,#8b1a1a,#e74c3c);}
.exp-bar{background:linear-gradient(90deg,#1a5276,#4cc9f0);}
.hl{font-family:'Cinzel',serif;font-size:.58rem;letter-spacing:.1em;color:var(--text2);}
.hv{font-size:.77rem;color:var(--gold2);font-weight:600;min-width:1.8rem;}
.floor-badge{font-family:'Cinzel',serif;font-size:1.15rem;font-weight:900;color:var(--gold2);text-align:center;text-shadow:0 0 18px rgba(201,146,42,.8);}
.floor-lbl{font-size:.52rem;letter-spacing:.28em;color:var(--text2);text-align:center;}
.hud-bottom{position:absolute;bottom:.75rem;left:50%;transform:translateX(-50%);}
.ab-bar{display:flex;gap:.4rem;align-items:flex-end;}
.ab-slot{width:52px;height:52px;background:var(--stone);border:1px solid var(--border);border-radius:4px;display:flex;flex-direction:column;align-items:center;justify-content:center;position:relative;transition:border-color .2s,opacity .2s;overflow:hidden;}
.ab-slot.unlocked{border-color:var(--gold);}
.ab-slot.locked{opacity:.22;filter:grayscale(1);}
.ab-slot .sk{position:absolute;top:2px;right:3px;font-family:'Cinzel',serif;font-size:.44rem;color:var(--text2);}
.ab-slot .si{font-size:1.25rem;line-height:1;}
.ab-slot .sn{font-size:.37rem;color:var(--text2);text-align:center;line-height:1.1;position:absolute;bottom:2px;left:0;right:0;white-space:pre-line;padding:0 1px;}
.ab-slot .cd-ov{position:absolute;inset:0;border-radius:4px;background:rgba(0,0,0,.72);display:flex;align-items:center;justify-content:center;font-family:'Cinzel',serif;font-size:.68rem;color:#fff;font-weight:700;}

/* NOTIF */
#notif{position:fixed;top:18%;left:50%;transform:translate(-50%,-50%);z-index:100;pointer-events:none;text-align:center;}
.nb{font-family:'Cinzel',serif;padding:.8rem 1.7rem;background:rgba(8,4,6,.96);border:2px solid var(--gold);border-radius:4px;animation:na .3s ease;box-shadow:0 0 35px rgba(201,146,42,.35);}
.nb.hidden{display:none;}
@keyframes na{from{opacity:0;transform:scale(.83);}to{opacity:1;transform:scale(1);}}
.nt{font-size:1.05rem;color:var(--gold2);letter-spacing:.16em;}
.ns{font-size:.8rem;color:var(--text);margin-top:.22rem;}

/* GAME CONTROL BUTTONS */
#gameControls{position:fixed;top:.75rem;right:.75rem;display:flex;gap:.4rem;z-index:20;pointer-events:all;}
#gameControls.hidden{display:none;}
.ctrl-btn{width:42px;height:42px;border:1px solid rgba(201,146,42,.45);border-radius:4px;background:rgba(10,6,8,.88);color:var(--gold2);font-size:1rem;cursor:pointer;display:flex;align-items:center;justify-content:center;backdrop-filter:blur(2px);transition:all .18s;position:relative;}
.ctrl-btn:hover{background:rgba(201,146,42,.22);border-color:var(--gold2);transform:translateY(-1px);}
.ctrl-btn:active{transform:translateY(0);}
.ctrl-btn .ctt{position:absolute;bottom:-22px;left:50%;transform:translateX(-50%);font-family:'Cinzel',serif;font-size:.42rem;color:var(--text2);white-space:nowrap;pointer-events:none;opacity:0;transition:opacity .15s;}
.ctrl-btn:hover .ctt{opacity:1;}
@keyframes saveFlash{0%{border-color:var(--gold2);box-shadow:0 0 14px rgba(240,188,90,.8);}100%{border-color:rgba(201,146,42,.45);box-shadow:none;}}
.ctrl-btn.saved{animation:saveFlash .7s ease;}

/* PAUSE SCREEN */
#pauseScreen{background:rgba(0,0,0,.82);flex-direction:column;gap:1.2rem;z-index:150;backdrop-filter:blur(4px);}
#pauseScreen.hidden{display:none;}
.pause-title{font-family:'Cinzel',serif;font-size:2.2rem;font-weight:900;color:var(--gold2);letter-spacing:.2em;text-shadow:0 0 28px rgba(240,188,90,.6);}
.pause-sep{width:220px;height:1px;background:linear-gradient(to right,transparent,var(--gold),transparent);}
.pause-btn{padding:.58rem 1.8rem;font-family:'Cinzel',serif;font-size:.82rem;font-weight:700;letter-spacing:.18em;cursor:pointer;border-radius:2px;background:var(--stone2);color:var(--gold2);border:1px solid rgba(201,146,42,.4);transition:all .2s;min-width:180px;text-align:center;}
.pause-btn:hover{background:rgba(201,146,42,.18);border-color:var(--gold2);}
.pause-info{font-size:.72rem;color:var(--text2);text-align:center;line-height:1.9;}

/* END */
#endScreen{background:rgba(0,0,0,.93);flex-direction:column;gap:1.3rem;z-index:200;}
.end-title{font-family:'Cinzel',serif;font-size:2.7rem;font-weight:900;}
.end-title.death{color:var(--blood2);text-shadow:0 0 35px rgba(192,57,43,.7);}
.end-title.win{color:var(--gold2);text-shadow:0 0 35px rgba(240,188,90,.7);}
.end-stats{font-size:1rem;color:var(--text2);text-align:center;line-height:2.1;}
.end-btn{padding:.62rem 2rem;font-family:'Cinzel',serif;font-size:.86rem;font-weight:700;letter-spacing:.16em;cursor:pointer;border-radius:2px;background:var(--stone2);color:var(--gold2);border:1px solid var(--gold);transition:all .2s;}
.end-btn:hover{background:var(--gold);color:#000;}
</style>
</head>
<body>

<!-- MENU -->
<div id="menuScreen" class="screen">
  <div class="torches">
    <div class="torch t1"></div><div class="torch t2"></div>
    <div class="torch t3"></div><div class="torch t4"></div>
  </div>
  <div class="menu-content">
    <div class="game-title">DUNGEON DESCENT</div>
    <div class="game-subtitle">▲ BAJA A LAS PROFUNDIDADES ▲</div>
    <div class="sep"></div>
    <div class="class-section">
      <div class="section-label">— ELIGE TU CLASE —</div>
      <div class="class-grid">

        <div class="class-card warrior-card selected" id="card-warrior" onclick="selectClass('warrior',this)">
          <div class="ci">⚔</div>
          <div class="cn">GUERRERO</div>
          <div class="cs">❤ 150 &nbsp;🛡 15 &nbsp;⚔ 25</div>
          <div class="ab-preview">
            <div class="ab-row"><span class="ab-key">Q</span><span class="ab-name">Golpe Giratorio</span><span class="ab-lv">Nv1</span></div>
            <div class="ab-row"><span class="ab-key">E</span><span class="ab-name">Furia Berserk</span><span class="ab-lv">Nv5</span></div>
            <div class="ab-row"><span class="ab-key">R</span><span class="ab-name">Postura Escudo</span><span class="ab-lv">Nv10</span></div>
            <div class="ab-row"><span class="ab-key">F</span><span class="ab-name">Torbellino</span><span class="ab-lv">Nv15</span></div>
          </div>
        </div>

        <div class="class-card summoner-card" id="card-summoner" onclick="selectClass('summoner',this)">
          <div class="ci">☠</div>
          <div class="cn">INVOCADOR</div>
          <div class="cs">❤ 100 &nbsp;🛡 8 &nbsp;⚔ 18</div>
          <div class="ab-preview">
            <div class="ab-row"><span class="ab-key">Q</span><span class="ab-name">Invocar Minion</span><span class="ab-lv">Nv1</span></div>
            <div class="ab-row"><span class="ab-key">E</span><span class="ab-name">Espectro Furia</span><span class="ab-lv">Nv5</span></div>
            <div class="ab-row"><span class="ab-key">R</span><span class="ab-name">Ejercito Muerto</span><span class="ab-lv">Nv10</span></div>
            <div class="ab-row"><span class="ab-key">F</span><span class="ab-name">Dragon Espectral</span><span class="ab-lv">Nv15</span></div>
          </div>
        </div>

        <div class="class-card mage-card" id="card-mage" onclick="selectClass('mage',this)">
          <div class="ci">✦</div>
          <div class="cn">MAGO</div>
          <div class="cs">❤ 80 &nbsp;🛡 5 &nbsp;⚔ 40</div>
          <div class="ab-preview">
            <div class="ab-row"><span class="ab-key">Q</span><span class="ab-name">Bola de Fuego</span><span class="ab-lv">Nv1</span></div>
            <div class="ab-row"><span class="ab-key">E</span><span class="ab-name">Rayo de Hielo</span><span class="ab-lv">Nv5</span></div>
            <div class="ab-row"><span class="ab-key">R</span><span class="ab-name">Tormenta Eléct.</span><span class="ab-lv">Nv10</span></div>
            <div class="ab-row"><span class="ab-key">F</span><span class="ab-name">Meteorito</span><span class="ab-lv">Nv15</span></div>
          </div>
        </div>

        <div class="class-card assassin-card" id="card-assassin" onclick="selectClass('assassin',this)">
          <div class="ci">◆</div>
          <div class="cn">ASESINO</div>
          <div class="cs">❤ 110 &nbsp;🛡 7 &nbsp;⚔ 35</div>
          <div class="ab-preview">
            <div class="ab-row"><span class="ab-key">Q</span><span class="ab-name">Veneno</span><span class="ab-lv">Nv1</span></div>
            <div class="ab-row"><span class="ab-key">E</span><span class="ab-name">Teletransporte</span><span class="ab-lv">Nv5</span></div>
            <div class="ab-row"><span class="ab-key">R</span><span class="ab-name">Lluvia de Dagas</span><span class="ab-lv">Nv10</span></div>
            <div class="ab-row"><span class="ab-key">F</span><span class="ab-name">Sombra Mortal</span><span class="ab-lv">Nv15</span></div>
          </div>
        </div>

      </div>
    </div>
    <button class="start-btn" onclick="startGame()">⚔ COMENZAR AVENTURA ⚔</button>
    <div id="continueWrap" style="margin-top:.5rem;display:flex;flex-direction:column;align-items:center;gap:.3rem;">
      <button class="continue-btn" id="continueBtn" onclick="continueGame()">▶ CONTINUAR PARTIDA</button>
      <div id="saveInfo" style="font-family:'Cinzel',serif;font-size:.55rem;color:var(--text2);letter-spacing:.08em;text-align:center;"></div>
    </div>
  </div>
</div>

<!-- GAME -->
<div id="gameScreen" class="screen hidden"><canvas id="gameCanvas"></canvas></div>

<!-- HUD -->
<div id="hud" class="hidden">
  <div class="hud-top">
    <div style="display:flex;flex-direction:column;gap:.3rem;">
      <div class="hud-panel">
        <div class="stat-row"><span class="hl">HP</span><div class="bar-wrap"><div class="bar-fill hp-bar" id="hpBar" style="width:100%"></div></div><span class="hv" id="hpVal">150</span></div>
        <div class="stat-row" style="margin-top:.28rem"><span class="hl">EXP</span><div class="bar-wrap"><div class="bar-fill exp-bar" id="expBar" style="width:0%"></div></div><span class="hv" id="expVal">0</span></div>
      </div>
      <div class="hud-panel"><div class="stat-row" style="gap:.65rem"><span>⚔ <span id="atkVal">25</span></span><span>🛡 <span id="defVal">15</span></span><span>🪙 <span id="goldVal">0</span></span></div></div>
    </div>
    <div><div class="hud-panel" style="text-align:center;min-width:80px"><div class="floor-lbl">PISO</div><div class="floor-badge" id="floorBadge">1</div><div class="hl" id="className" style="text-align:center">GUERRERO</div><div class="hl" style="text-align:center">Nv <span id="levelVal">1</span></div></div></div>
    <div style="display:flex;flex-direction:column;gap:.3rem;">
      <div class="hud-panel"><div class="stat-row"><span class="hl">Enemigos:</span><span id="enemyCount" class="hv">0</span></div><div class="stat-row"><span class="hl">Kills:</span><span id="killCount" class="hv">0</span></div></div>
    </div>
  </div>
  <div class="hud-bottom"><div class="ab-bar" id="abBar"></div></div>
</div>

<!-- GAME CONTROL BUTTONS -->
<div id="gameControls" class="hidden">
  <button class="ctrl-btn" onclick="togglePause()" id="pauseBtn" title="Pausar (P)">⏸<span class="ctt">PAUSAR</span></button>
  <button class="ctrl-btn" onclick="saveGame()" id="saveBtn" title="Guardar progreso">💾<span class="ctt">GUARDAR</span></button>
  <button class="ctrl-btn" onclick="pauseGoMenu()" title="Volver al menú">🏠<span class="ctt">MENÚ</span></button>
</div>

<!-- PAUSE SCREEN -->
<div id="pauseScreen" class="screen hidden">
  <div class="pause-title">⏸ PAUSA</div>
  <div class="pause-sep"></div>
  <div class="pause-info" id="pauseInfo"></div>
  <div class="pause-sep"></div>
  <div style="display:flex;flex-direction:column;gap:.6rem;align-items:center">
    <button class="pause-btn" onclick="togglePause()">▶ CONTINUAR</button>
    <button class="pause-btn" onclick="saveGame()">💾 GUARDAR PROGRESO</button>
    <button class="pause-btn" onclick="confirmRestart()">🔄 REINICIAR PARTIDA</button>
    <button class="pause-btn" onclick="pauseGoMenu()">🏠 VOLVER AL MENÚ</button>
  </div>
</div>

<!-- NOTIF -->
<div id="notif"><div class="nb hidden" id="nb"><div class="nt" id="nt"></div><div class="ns" id="ns"></div></div></div>

<!-- END -->
<div id="endScreen" class="screen hidden">
  <div class="end-title" id="endTitle">GAME OVER</div>
  <div class="end-stats" id="endStats"></div>
  <div style="display:flex;gap:1rem">
    <button class="end-btn" onclick="goMenu()">🏠 Menú</button>
    <button class="end-btn" onclick="restartGame()">⚔ Reintentar</button>
  </div>
</div>

<script>
// ═══════════════════════════════════════════
//  CONSTANTS
// ═══════════════════════════════════════════
const TILE=48,COLS=25,ROWS=18,W=COLS*TILE,H=ROWS*TILE;
const MAX_PART=90,MAX_DMG=30;

// ─── CLASS DEFINITIONS ───────────────────
const CLASSES={
  warrior:{
    name:'GUERRERO',hp:150,atk:25,def:15,spd:3,color:'#c9922a',
    ab:[
      {k:'Q',n:'Golpe\nGiratorio', i:'◎',lv:1, cd:4,  desc:'Daño en área cercana'},
      {k:'E',n:'Furia\nBerserk',   i:'▲',lv:5, cd:8,  desc:'ATQ x2 por 5s'},
      {k:'R',n:'Postura\nEscudo',  i:'◈',lv:10,cd:12, desc:'Bloquea 3 golpes'},
      {k:'F',n:'Torbellino',       i:'✦',lv:15,cd:20, desc:'Daño masivo de área'},
    ]
  },
  summoner:{
    name:'INVOCADOR',hp:100,atk:18,def:8,spd:3,color:'#9333ea',
    ab:[
      {k:'Q',n:'Invocar\nMinion',  i:'◉',lv:1, cd:6,  desc:'Invoca un aliado'},
      {k:'E',n:'Espectro\nFuria',  i:'◈',lv:5, cd:10, desc:'Minion explosivo'},
      {k:'R',n:'Ejercito\nMuerto', i:'☆',lv:10,cd:15, desc:'3 minions a la vez'},
      {k:'F',n:'Dragon\nEspectral',i:'★',lv:15,cd:25, desc:'Dragon aliado poderoso'},
    ]
  },
  mage:{
    name:'MAGO',hp:80,atk:40,def:5,spd:3,color:'#4cc9f0',
    ab:[
      {k:'Q',n:'Bola de\nFuego',   i:'●',lv:1, cd:3,  desc:'Proyectil de fuego'},
      {k:'E',n:'Rayo de\nHielo',   i:'◆',lv:5, cd:6,  desc:'Congela enemigos cercanos'},
      {k:'R',n:'Tormenta\nEléct.', i:'✦',lv:10,cd:12, desc:'Rayos en área'},
      {k:'F',n:'Meteorito',        i:'★',lv:15,cd:20, desc:'Impacto devastador'},
    ]
  },
  assassin:{
    name:'ASESINO',hp:110,atk:35,def:7,spd:5,color:'#4a9e3f',
    ab:[
      {k:'Q',n:'Veneno',           i:'◇',lv:1, cd:4,  desc:'Envenena área cercana'},
      {k:'E',n:'Teletransp.',      i:'◈',lv:5, cd:5,  desc:'Dash al cursor'},
      {k:'R',n:'Lluvia\nDagas',    i:'◆',lv:10,cd:10, desc:'Dagas en todas dir.'},
      {k:'F',n:'Sombra\nMortal',   i:'★',lv:15,cd:18, desc:'Crítico x5 al más cercano'},
    ]
  },
};

// ─── ENEMY DEFINITIONS ───────────────────
const ENEMY_DEFS=[
  {id:'zombie',   name:'Zombie',      hp:80, atk:12,def:2, spd:1.2,exp:25,gold:3, mf:1 },
  {id:'slime',    name:'Slime',       hp:50, atk:8, def:1, spd:1.5,exp:20,gold:2, mf:1 },
  {id:'skeleton', name:'Esqueleto',   hp:50, atk:18,def:3, spd:2.5,exp:30,gold:7, mf:3 },
  {id:'vampire',  name:'Vampiro',     hp:90, atk:22,def:5, spd:2.8,exp:45,gold:12,mf:5 },
  {id:'witch',    name:'Bruja',       hp:55, atk:25,def:3, spd:2.0,exp:40,gold:10,mf:7 },
  {id:'golem',    name:'Golem',       hp:250,atk:30,def:20,spd:0.8,exp:80,gold:20,mf:10},
  {id:'darkknight',name:'Cab.Oscuro', hp:500,atk:40,def:25,spd:2.0,exp:200,gold:50,mf:1,isBoss:true},
];

// ─── DETAILED ENEMY SHAPES ───────────────
const SHAPES={
  warrior:(ctx,x,y,r,col)=>{
    ctx.fillStyle=col;
    ctx.fillRect(x-r*.65,y-r*.9,r*1.3,r*1.8);
    ctx.fillStyle='#8a6010';
    ctx.fillRect(x-r,y-r*.85,r*.4,r*.5);
    ctx.fillRect(x+r*.6,y-r*.85,r*.4,r*.5);
    ctx.fillStyle=col;
    ctx.fillRect(x-r*.5,y-r*1.5,r,r*.7);
    ctx.fillStyle='rgba(0,0,0,.4)';
    ctx.fillRect(x-r*.35,y-r*1.3,r*.7,r*.25);
    ctx.fillStyle='#ccc';
    ctx.fillRect(x+r*.7,y-r*1.2,r*.2,r*1.6);
    ctx.fillStyle='#8a6010';
    ctx.fillRect(x+r*.55,y-r*.3,r*.5,r*.15);
    ctx.fillStyle='#8a6010';
    ctx.beginPath();ctx.ellipse(x-r*.9,y+r*.1,r*.3,r*.45,0,0,6.28);ctx.fill();
    ctx.fillStyle=col;
    ctx.beginPath();ctx.ellipse(x-r*.9,y+r*.1,r*.18,r*.3,0,0,6.28);ctx.fill();
  },
  summoner:(ctx,x,y,r,col)=>{
    ctx.fillStyle='#1a0a2a';
    ctx.beginPath();ctx.moveTo(x-r*.8,y+r);ctx.lineTo(x+r*.8,y+r);ctx.lineTo(x+r*.5,y-r*.5);ctx.lineTo(x-r*.5,y-r*.5);ctx.closePath();ctx.fill();
    ctx.strokeStyle=col;ctx.lineWidth=1.5;
    ctx.beginPath();ctx.moveTo(x,y-r*.4);ctx.lineTo(x,y+r*.8);ctx.stroke();
    ctx.fillStyle='#1a0a2a';
    ctx.beginPath();ctx.arc(x,y-r*.9,r*.55,0,6.28);ctx.fill();
    ctx.fillStyle=col;
    ctx.beginPath();ctx.arc(x-r*.2,y-r*.95,r*.12,0,6.28);ctx.fill();
    ctx.beginPath();ctx.arc(x+r*.2,y-r*.95,r*.12,0,6.28);ctx.fill();
    ctx.strokeStyle='#6a3aaa';ctx.lineWidth=2.5;
    ctx.beginPath();ctx.moveTo(x+r*.7,y+r);ctx.lineTo(x+r*.7,y-r*1.4);ctx.stroke();
    ctx.fillStyle=col;
    ctx.beginPath();ctx.arc(x+r*.7,y-r*1.5,r*.2,0,6.28);ctx.fill();
    ctx.strokeStyle=col;ctx.lineWidth=1;
    ctx.beginPath();ctx.arc(x+r*.7,y-r*1.5,r*.32,0,6.28);ctx.stroke();
  },
  mage:(ctx,x,y,r,col)=>{
    ctx.fillStyle='#0a1a2a';
    ctx.beginPath();ctx.moveTo(x-r*.7,y+r);ctx.lineTo(x+r*.7,y+r);ctx.lineTo(x+r*.4,y-r*.4);ctx.lineTo(x-r*.4,y-r*.4);ctx.closePath();ctx.fill();
    ctx.strokeStyle=col;ctx.lineWidth=1.5;
    ctx.beginPath();ctx.moveTo(x-r*.3,y);ctx.lineTo(x+r*.3,y);ctx.stroke();
    ctx.beginPath();ctx.moveTo(x-r*.2,y+r*.35);ctx.lineTo(x+r*.2,y+r*.35);ctx.stroke();
    ctx.fillStyle='#0a1a2a';
    ctx.beginPath();ctx.moveTo(x-r*.6,y-r*.4);ctx.lineTo(x+r*.6,y-r*.4);ctx.lineTo(x,y-r*1.8);ctx.closePath();ctx.fill();
    ctx.fillStyle=col;ctx.fillRect(x-r*.6,y-r*.55,r*1.2,r*.2);
    ctx.fillStyle='#c8a87a';
    ctx.beginPath();ctx.ellipse(x,y-r*.7,r*.35,r*.3,0,0,6.28);ctx.fill();
    ctx.fillStyle=col;
    ctx.beginPath();ctx.arc(x-r*.12,y-r*.72,r*.07,0,6.28);ctx.fill();
    ctx.beginPath();ctx.arc(x+r*.12,y-r*.72,r*.07,0,6.28);ctx.fill();
    ctx.strokeStyle='#8aaabb';ctx.lineWidth=2;
    ctx.beginPath();ctx.moveTo(x+r*.6,y+r*.6);ctx.lineTo(x+r,y-r*.2);ctx.stroke();
    ctx.fillStyle=col;ctx.beginPath();ctx.arc(x+r,y-r*.2,r*.14,0,6.28);ctx.fill();
  },
  assassin:(ctx,x,y,r,col)=>{
    ctx.fillStyle='#0a140a';
    ctx.fillRect(x-r*.6,y-r*.8,r*1.2,r*1.7);
    ctx.fillStyle='#121c12';
    ctx.beginPath();ctx.arc(x,y-r*.9,r*.5,0,6.28);ctx.fill();
    ctx.beginPath();ctx.moveTo(x-r*.8,y-r*.4);ctx.lineTo(x+r*.8,y-r*.4);ctx.lineTo(x+r,y+r);ctx.lineTo(x-r,y+r);ctx.closePath();ctx.fill();
    ctx.fillStyle=col;
    ctx.beginPath();ctx.arc(x-r*.18,y-r*.95,r*.1,0,6.28);ctx.fill();
    ctx.beginPath();ctx.arc(x+r*.18,y-r*.95,r*.1,0,6.28);ctx.fill();
    ctx.strokeStyle=col;ctx.lineWidth=2;
    ctx.beginPath();ctx.moveTo(x-r*.7,y-.2*r);ctx.lineTo(x-r*.7,y-r*1.2);ctx.stroke();
    ctx.beginPath();ctx.moveTo(x+r*.7,y-.2*r);ctx.lineTo(x+r*.7,y-r*1.2);ctx.stroke();
    ctx.fillStyle=col;ctx.fillRect(x-r*.6,y+r*.15,r*1.2,r*.12);
  },
  zombie:(ctx,x,y,r,col)=>{
    ctx.fillStyle='#3a5a28';
    ctx.fillRect(x-r*.65,y-r*.7,r*1.3,r*1.6);
    ctx.fillStyle='#2a3a18';
    ctx.fillRect(x-r*.55,y,r*1.1,r*.5);
    ctx.fillRect(x-r*.4,y-r*.65,r*.25,r*.35);
    ctx.fillStyle='#4a6a30';
    ctx.beginPath();ctx.ellipse(x+r*.08,y-r*1.05,r*.52,r*.48,0.2,0,6.28);ctx.fill();
    ctx.strokeStyle='#ff4444';ctx.lineWidth=1.5;
    for(const ex of[x-r*.18,x+r*.22]){
      ctx.beginPath();ctx.moveTo(ex-r*.1,y-r*1.12);ctx.lineTo(ex+r*.1,y-r*.92);ctx.stroke();
      ctx.beginPath();ctx.moveTo(ex+r*.1,y-r*1.12);ctx.lineTo(ex-r*.1,y-r*.92);ctx.stroke();
    }
    ctx.strokeStyle='#880000';ctx.lineWidth=1.5;
    ctx.beginPath();ctx.moveTo(x-r*.22,y-r*.82);ctx.lineTo(x-r*.08,y-r*.74);ctx.lineTo(x+r*.05,y-r*.82);ctx.lineTo(x+r*.2,y-r*.74);ctx.stroke();
    ctx.fillStyle='#3a5a28';
    ctx.fillRect(x-r*1.2,y-r*.5,r*.6,r*.25);
    ctx.fillRect(x+r*.6,y-r*.5,r*.6,r*.25);
    ctx.strokeStyle='#880000';ctx.lineWidth=1.5;
    for(let i=0;i<3;i++){ctx.beginPath();ctx.moveTo(x-r*1.2+i*r*.15,y-r*.5);ctx.lineTo(x-r*1.25+i*r*.15,y-r*.7);ctx.stroke();}
    for(let i=0;i<3;i++){ctx.beginPath();ctx.moveTo(x+r*1.1+i*r*.1,y-r*.5);ctx.lineTo(x+r*1.05+i*r*.1,y-r*.7);ctx.stroke();}
  },
  slime:(ctx,x,y,r,col)=>{
    ctx.fillStyle=col;
    ctx.beginPath();ctx.ellipse(x,y+r*.15,r,r*.72,0,0,6.28);ctx.fill();
    ctx.beginPath();ctx.ellipse(x-r*.3,y+r*.78,r*.18,r*.28,-.3,0,6.28);ctx.fill();
    ctx.beginPath();ctx.ellipse(x+r*.2,y+r*.8,r*.14,r*.22,.2,0,6.28);ctx.fill();
    ctx.fillStyle='rgba(255,255,255,.35)';
    ctx.beginPath();ctx.ellipse(x-r*.28,y-r*.2,r*.28,r*.2,-.4,0,6.28);ctx.fill();
    ctx.fillStyle='#fff';
    ctx.beginPath();ctx.ellipse(x-r*.25,y,r*.2,r*.24,0,0,6.28);ctx.fill();
    ctx.beginPath();ctx.ellipse(x+r*.25,y,r*.2,r*.24,0,0,6.28);ctx.fill();
    ctx.fillStyle='#111';
    ctx.beginPath();ctx.arc(x-r*.22,y+r*.04,r*.12,0,6.28);ctx.fill();
    ctx.beginPath();ctx.arc(x+r*.28,y+r*.04,r*.12,0,6.28);ctx.fill();
    ctx.fillStyle='#fff';
    ctx.beginPath();ctx.arc(x-r*.18,y,r*.04,0,6.28);ctx.fill();
    ctx.beginPath();ctx.arc(x+r*.32,y,r*.04,0,6.28);ctx.fill();
    ctx.strokeStyle='rgba(0,0,0,.5)';ctx.lineWidth=1.5;
    ctx.beginPath();ctx.arc(x,y+r*.18,r*.18,0.2,Math.PI-.2);ctx.stroke();
  },
  skeleton:(ctx,x,y,r,col)=>{
    ctx.strokeStyle=col;ctx.lineWidth=2;
    ctx.beginPath();ctx.rect(x-r*.45,y-r*.6,r*.9,r*1.0);ctx.stroke();
    for(let i=0;i<3;i++){
      ctx.beginPath();ctx.moveTo(x-r*.45,y-r*.4+i*r*.3);ctx.lineTo(x+r*.45,y-r*.4+i*r*.3);ctx.stroke();
    }
    ctx.beginPath();ctx.ellipse(x,y+r*.5,r*.4,r*.2,0,0,6.28);ctx.stroke();
    ctx.beginPath();ctx.moveTo(x-r*.25,y+r*.65);ctx.lineTo(x-r*.3,y+r*1.5);ctx.stroke();
    ctx.beginPath();ctx.moveTo(x+r*.25,y+r*.65);ctx.lineTo(x+r*.3,y+r*1.5);ctx.stroke();
    ctx.beginPath();ctx.moveTo(x-r*.45,y-r*.5);ctx.lineTo(x-r*1.0,y+r*.1);ctx.stroke();
    ctx.beginPath();ctx.moveTo(x+r*.45,y-r*.5);ctx.lineTo(x+r*1.0,y+r*.1);ctx.stroke();
    ctx.fillStyle=col;
    ctx.beginPath();ctx.ellipse(x,y-r*1.05,r*.42,r*.45,0,0,6.28);ctx.fill();
    ctx.fillStyle='#000';
    ctx.beginPath();ctx.ellipse(x-r*.16,y-r*1.08,r*.13,r*.15,0,0,6.28);ctx.fill();
    ctx.beginPath();ctx.ellipse(x+r*.16,y-r*1.08,r*.13,r*.15,0,0,6.28);ctx.fill();
    ctx.fillStyle='#88aaff';
    ctx.beginPath();ctx.arc(x-r*.16,y-r*1.08,r*.07,0,6.28);ctx.fill();
    ctx.beginPath();ctx.arc(x+r*.16,y-r*1.08,r*.07,0,6.28);ctx.fill();
    ctx.fillStyle=col;
    ctx.beginPath();ctx.rect(x-r*.3,y-r*.7,r*.6,r*.18);ctx.fill();
    ctx.fillStyle='#000';
    for(let i=0;i<4;i++)ctx.fillRect(x-r*.26+i*r*.15,y-r*.7,r*.08,r*.12);
  },
  vampire:(ctx,x,y,r,col)=>{
    ctx.fillStyle='#1a0010';
    ctx.beginPath();ctx.moveTo(x,y-r*.3);ctx.lineTo(x-r*1.4,y+r*.8);ctx.lineTo(x-r*.5,y+r*.2);ctx.lineTo(x,y+r);ctx.lineTo(x+r*.5,y+r*.2);ctx.lineTo(x+r*1.4,y+r*.8);ctx.closePath();ctx.fill();
    ctx.fillStyle='#2a0020';
    ctx.beginPath();ctx.moveTo(x,y-r*.1);ctx.lineTo(x-r*.8,y+r*.7);ctx.lineTo(x-r*.3,y+r*.2);ctx.lineTo(x,y+r*.6);ctx.lineTo(x+r*.3,y+r*.2);ctx.lineTo(x+r*.8,y+r*.7);ctx.closePath();ctx.fill();
    ctx.fillStyle='#0a0010';
    ctx.fillRect(x-r*.42,y-r*.7,r*.84,r*1.5);
    ctx.fillStyle='#d4c0c8';
    ctx.beginPath();ctx.ellipse(x,y-r*1.0,r*.42,r*.48,0,0,6.28);ctx.fill();
    ctx.fillStyle='#0a0010';
    ctx.beginPath();ctx.ellipse(x,y-r*1.38,r*.42,r*.22,0,0,6.28);ctx.fill();
    ctx.beginPath();ctx.moveTo(x-r*.42,y-r*1.2);ctx.lineTo(x-r*.3,y-r*.6);ctx.lineTo(x,y-r*.55);ctx.closePath();ctx.fill();
    ctx.fillStyle='#ff0022';
    ctx.beginPath();ctx.arc(x-r*.16,y-r*1.02,r*.1,0,6.28);ctx.fill();
    ctx.beginPath();ctx.arc(x+r*.16,y-r*1.02,r*.1,0,6.28);ctx.fill();
    ctx.fillStyle='rgba(255,0,34,.2)';
    ctx.beginPath();ctx.arc(x-r*.16,y-r*1.02,r*.2,0,6.28);ctx.fill();
    ctx.beginPath();ctx.arc(x+r*.16,y-r*1.02,r*.2,0,6.28);ctx.fill();
    ctx.fillStyle='#fff';
    ctx.beginPath();ctx.moveTo(x-r*.12,y-r*.76);ctx.lineTo(x-r*.08,y-r*.6);ctx.lineTo(x-r*.04,y-r*.76);ctx.closePath();ctx.fill();
    ctx.beginPath();ctx.moveTo(x+r*.04,y-r*.76);ctx.lineTo(x+r*.08,y-r*.6);ctx.lineTo(x+r*.12,y-r*.76);ctx.closePath();ctx.fill();
  },
  witch:(ctx,x,y,r,col)=>{
    ctx.fillStyle='#1a0a1a';
    ctx.beginPath();ctx.moveTo(x-r*.5,y-r*.3);ctx.lineTo(x-r*.85,y+r*1.2);ctx.lineTo(x+r*.85,y+r*1.2);ctx.lineTo(x+r*.5,y-r*.3);ctx.closePath();ctx.fill();
    ctx.strokeStyle=col;ctx.lineWidth=1;
    ctx.beginPath();ctx.moveTo(x-r*.3,y+r*.4);ctx.lineTo(x+r*.3,y+r*.4);ctx.stroke();
    ctx.beginPath();ctx.moveTo(x-r*.5,y+r*.8);ctx.lineTo(x+r*.5,y+r*.8);ctx.stroke();
    ctx.fillStyle='#2a1a2a';
    ctx.fillRect(x-r*.4,y-r*.9,r*.8,r*.65);
    ctx.fillStyle='#c8a87a';
    ctx.beginPath();ctx.ellipse(x,y-r*1.1,r*.38,r*.42,0,0,6.28);ctx.fill();
    ctx.fillStyle='#1a0a1a';
    ctx.beginPath();ctx.moveTo(x-r*.55,y-r*.72);ctx.lineTo(x+r*.55,y-r*.72);ctx.lineTo(x,y-r*2.0);ctx.closePath();ctx.fill();
    ctx.beginPath();ctx.ellipse(x,y-r*.72,r*.65,r*.18,0,0,6.28);ctx.fill();
    ctx.fillStyle=col;
    ctx.beginPath();ctx.ellipse(x,y-r*.88,r*.52,r*.13,0,0,6.28);ctx.fill();
    ctx.fillStyle=col;
    ctx.beginPath();ctx.ellipse(x-r*.17,y-r*1.14,r*.12,r*.08,0,0,6.28);ctx.fill();
    ctx.beginPath();ctx.ellipse(x+r*.17,y-r*1.14,r*.12,r*.08,0,0,6.28);ctx.fill();
    ctx.fillStyle='#9a7850';
    ctx.beginPath();ctx.arc(x,y-r*.98,r*.07,0,6.28);ctx.fill();
    ctx.strokeStyle='#5a3a8a';ctx.lineWidth=3;
    ctx.beginPath();ctx.moveTo(x+r*.5,y+r*1.1);ctx.lineTo(x+r*.85,y-r*.8);ctx.stroke();
    ctx.fillStyle=col;
    ctx.beginPath();ctx.arc(x+r*.85,y-r*.85,r*.22,0,6.28);ctx.fill();
    ctx.fillStyle='rgba(255,255,255,.3)';
    ctx.beginPath();ctx.arc(x+r*.78,y-r*.92,r*.08,0,6.28);ctx.fill();
  },
  golem:(ctx,x,y,r,col)=>{
    ctx.fillStyle=col;
    ctx.fillRect(x-r*.85,y+r*.2,r*.7,r*.9);
    ctx.fillRect(x+r*.15,y+r*.2,r*.7,r*.9);
    ctx.strokeStyle='#555';ctx.lineWidth=1.5;
    ctx.beginPath();ctx.moveTo(x-r*.6,y+r*.4);ctx.lineTo(x-r*.4,y+r*.65);ctx.lineTo(x-r*.55,y+r*.9);ctx.stroke();
    ctx.beginPath();ctx.moveTo(x+r*.35,y+r*.5);ctx.lineTo(x+r*.55,y+r*.7);ctx.stroke();
    ctx.fillStyle=col;
    ctx.fillRect(x-r*.95,y-r*.9,r*1.9,r*1.2);
    ctx.strokeStyle='#aaa';ctx.lineWidth=1.5;
    ctx.beginPath();ctx.arc(x,y-r*.25,r*.4,0,6.28);ctx.stroke();
    ctx.beginPath();ctx.moveTo(x,y-r*.65);ctx.lineTo(x,y+r*.15);ctx.moveTo(x-r*.4,y-r*.25);ctx.lineTo(x+r*.4,y-r*.25);ctx.stroke();
    ctx.strokeStyle='#555';
    ctx.beginPath();ctx.moveTo(x-r*.7,y-r*.7);ctx.lineTo(x-r*.4,y-r*.4);ctx.lineTo(x-r*.6,y-.1*r);ctx.stroke();
    ctx.fillStyle=col;
    ctx.fillRect(x-r*1.6,y-r*.85,r*.68,r*1.1);
    ctx.fillRect(x+r*.92,y-r*.85,r*.68,r*1.1);
    ctx.beginPath();ctx.arc(x-r*1.28,y+r*.35,r*.4,0,6.28);ctx.fill();
    ctx.beginPath();ctx.arc(x+r*1.28,y+r*.35,r*.4,0,6.28);ctx.fill();
    ctx.fillStyle=col;
    ctx.fillRect(x-r*.65,y-r*1.75,r*1.3,r*.9);
    ctx.fillStyle='#ff6600';
    ctx.fillRect(x-r*.45,y-r*1.55,r*.35,r*.25);
    ctx.fillRect(x+r*.1,y-r*1.55,r*.35,r*.25);
    ctx.fillStyle='rgba(255,100,0,.35)';
    ctx.fillRect(x-r*.55,y-r*1.62,r*.55,r*.38);
    ctx.fillRect(x+r*.0,y-r*1.62,r*.55,r*.38);
    ctx.fillStyle='#555';
    for(let i=0;i<4;i++)ctx.fillRect(x-r*.42+i*r*.25,y-r*.95,r*.18,r*.22);
  },
  darkknight:(ctx,x,y,r,col)=>{
    ctx.fillStyle='rgba(100,0,200,.12)';
    ctx.beginPath();ctx.arc(x,y,r*1.6,0,6.28);ctx.fill();
    ctx.fillStyle='#1a0030';
    ctx.fillRect(x-r*.7,y+r*.3,r*.55,r*.8);
    ctx.fillRect(x+r*.15,y+r*.3,r*.55,r*.8);
    ctx.fillStyle=col;
    ctx.beginPath();ctx.moveTo(x-r*.5,y+r*.35);ctx.lineTo(x-r*.6,y+r*.15);ctx.lineTo(x-r*.4,y+r*.35);ctx.closePath();ctx.fill();
    ctx.beginPath();ctx.moveTo(x+r*.5,y+r*.35);ctx.lineTo(x+r*.6,y+r*.15);ctx.lineTo(x+r*.4,y+r*.35);ctx.closePath();ctx.fill();
    ctx.fillStyle='#0a0020';
    ctx.fillRect(x-r*.85,y-r*.85,r*1.7,r*1.2);
    ctx.strokeStyle=col;ctx.lineWidth=1.5;
    ctx.beginPath();ctx.moveTo(x-r*.5,y-r*.6);ctx.lineTo(x,y-r*.1);ctx.lineTo(x+r*.5,y-r*.6);ctx.stroke();
    ctx.beginPath();ctx.moveTo(x-r*.55,y-r*.1);ctx.lineTo(x+r*.55,y-r*.1);ctx.stroke();
    ctx.fillStyle=col;
    for(let s=-1;s<=1;s+=2){
      const sx=x+s*r*.82;
      ctx.fillRect(sx-r*.22,y-r*.85,r*.44,r*.35);
      ctx.beginPath();ctx.moveTo(sx-r*.18,y-r*.85);ctx.lineTo(sx,y-r*1.15);ctx.lineTo(sx+r*.18,y-r*.85);ctx.closePath();ctx.fill();
    }
    ctx.fillStyle='#0a0020';
    ctx.fillRect(x-r*1.4,y-r*.75,r*.58,r*.9);
    ctx.fillRect(x+r*.82,y-r*.75,r*.58,r*.9);
    ctx.fillStyle=col;
    ctx.fillRect(x-r*1.3,y+r*.18,r*.38,r*.35);
    ctx.fillRect(x+r*.9,y+r*.18,r*.38,r*.35);
    ctx.fillStyle='#0a0020';
    ctx.fillRect(x-r*.68,y-r*1.75,r*1.36,r*.95);
    ctx.fillStyle=col;
    ctx.fillRect(x-r*.5,y-r*1.42,r*1.0,r*.16);
    ctx.fillStyle=col;
    ctx.beginPath();ctx.moveTo(x-r*.55,y-r*1.75);ctx.lineTo(x-r*.45,y-r*2.05);ctx.lineTo(x-r*.35,y-r*1.75);ctx.closePath();ctx.fill();
    ctx.beginPath();ctx.moveTo(x-r*.15,y-r*1.75);ctx.lineTo(x,y-r*2.2);ctx.lineTo(x+r*.15,y-r*1.75);ctx.closePath();ctx.fill();
    ctx.beginPath();ctx.moveTo(x+r*.35,y-r*1.75);ctx.lineTo(x+r*.45,y-r*2.05);ctx.lineTo(x+r*.55,y-r*1.75);ctx.closePath();ctx.fill();
    ctx.fillStyle='#1a0030';
    ctx.fillRect(x+r*.88,y-r*1.5,r*.3,r*2.4);
    ctx.fillStyle=col;
    ctx.fillRect(x+r*.93,y-r*1.5,r*.2,r*2.4);
    ctx.strokeStyle=col;ctx.lineWidth=.5;
    ctx.strokeRect(x+r*.88,y-r*1.5,r*.3,r*2.4);
    ctx.fillStyle=col;
    ctx.fillRect(x+r*.72,y-.6*r,r*.62,r*.2);
  },
  // Q — Minion básico: esqueleto pequeño con ojos morados
  minion:(ctx,x,y,r,col)=>{
    // Huesos del cuerpo
    ctx.strokeStyle='#c8b8e8';ctx.lineWidth=2;
    ctx.beginPath();ctx.rect(x-r*.35,y-r*.5,r*.7,r*.9);ctx.stroke();
    ctx.beginPath();ctx.moveTo(x-r*.35,y-r*.3);ctx.lineTo(x+r*.35,y-r*.3);ctx.stroke();
    ctx.beginPath();ctx.moveTo(x-r*.35,y+r*.1);ctx.lineTo(x+r*.35,y+r*.1);ctx.stroke();
    // Piernas
    ctx.beginPath();ctx.moveTo(x-r*.2,y+r*.4);ctx.lineTo(x-r*.25,y+r);ctx.stroke();
    ctx.beginPath();ctx.moveTo(x+r*.2,y+r*.4);ctx.lineTo(x+r*.25,y+r);ctx.stroke();
    // Brazos
    ctx.beginPath();ctx.moveTo(x-r*.35,y-r*.4);ctx.lineTo(x-r*.8,y+r*.1);ctx.stroke();
    ctx.beginPath();ctx.moveTo(x+r*.35,y-r*.4);ctx.lineTo(x+r*.8,y+r*.1);ctx.stroke();
    // Cráneo
    ctx.fillStyle='#c8b8e8';
    ctx.beginPath();ctx.ellipse(x,y-r*.85,r*.32,r*.35,0,0,6.28);ctx.fill();
    // Mandíbula
    ctx.fillRect(x-r*.22,y-r*.58,r*.44,r*.14);
    // Dientes
    ctx.fillStyle='#1a0a2a';
    for(let i=0;i<3;i++)ctx.fillRect(x-r*.18+i*r*.14,y-r*.58,r*.08,r*.1);
    // Ojos morados brillantes
    ctx.fillStyle='#9333ea';
    ctx.beginPath();ctx.arc(x-r*.12,y-r*.92,r*.08,0,6.28);ctx.fill();
    ctx.beginPath();ctx.arc(x+r*.12,y-r*.92,r*.08,0,6.28);ctx.fill();
    // Aura morada
    ctx.fillStyle='rgba(147,51,234,.15)';
    ctx.beginPath();ctx.arc(x,y,r*1.1,0,6.28);ctx.fill();
  },

  // E — Espectro de Furia: fantasma llameante rojo-naranja
  specter:(ctx,x,y,r,col)=>{
    const t=performance.now()*.002;
    // Cola fantasmal ondulante
    ctx.fillStyle='rgba(220,60,20,.55)';
    ctx.beginPath();
    ctx.moveTo(x-r*.6,y+r*.2);
    ctx.quadraticCurveTo(x-r*.4,y+r*.8+Math.sin(t)*r*.2,x,y+r*1.1);
    ctx.quadraticCurveTo(x+r*.4,y+r*.8+Math.sin(t+1)*r*.2,x+r*.6,y+r*.2);
    ctx.closePath();ctx.fill();
    // Cuerpo
    ctx.fillStyle='#e84020';
    ctx.beginPath();ctx.ellipse(x,y-r*.1,r*.65,r*.75,0,0,6.28);ctx.fill();
    // Llamas internas
    ctx.fillStyle='#ff8844';
    ctx.beginPath();ctx.ellipse(x,y-r*.2,r*.42,r*.5,0,0,6.28);ctx.fill();
    ctx.fillStyle='#ffcc44';
    ctx.beginPath();ctx.ellipse(x,y-r*.3,r*.2,r*.28,0,0,6.28);ctx.fill();
    // Ojos vacíos negros
    ctx.fillStyle='#110000';
    ctx.beginPath();ctx.ellipse(x-r*.22,y-r*.2,r*.18,r*.22,-.2,0,6.28);ctx.fill();
    ctx.beginPath();ctx.ellipse(x+r*.22,y-r*.2,r*.18,r*.22,.2,0,6.28);ctx.fill();
    // Brillo rojo en ojos
    ctx.fillStyle='#ff2200';
    ctx.beginPath();ctx.arc(x-r*.22,y-r*.22,r*.08,0,6.28);ctx.fill();
    ctx.beginPath();ctx.arc(x+r*.22,y-r*.22,r*.08,0,6.28);ctx.fill();
    // Llamas en la cabeza
    ctx.fillStyle='rgba(255,100,0,.7)';
    for(let f=0;f<3;f++){
      const fx=x+(-1+f)*r*.3,fy=y-r*.7;
      ctx.beginPath();ctx.moveTo(fx-r*.1,fy);ctx.lineTo(fx,fy-r*(.4+Math.sin(t+f)*.15));ctx.lineTo(fx+r*.1,fy);ctx.closePath();ctx.fill();
    }
    // Aura roja
    ctx.fillStyle='rgba(232,64,32,.12)';
    ctx.beginPath();ctx.arc(x,y,r*1.25,0,6.28);ctx.fill();
  },

  // R — Ejército Muerto: guerrero zombie armado
  army:(ctx,x,y,r,col)=>{
    // Armadura oxidada
    ctx.fillStyle='#3a2a18';
    ctx.fillRect(x-r*.6,y-r*.75,r*1.2,r*1.55);
    // Placa pechera
    ctx.fillStyle='#2a1a0a';
    ctx.fillRect(x-r*.48,y-r*.65,r*.96,r*.9);
    // Grietas en armadura
    ctx.strokeStyle='#5a3a18';ctx.lineWidth=1.5;
    ctx.beginPath();ctx.moveTo(x-r*.2,y-r*.55);ctx.lineTo(x,y-r*.25);ctx.lineTo(x-.1*r,y+r*.1);ctx.stroke();
    // Cabeza putrefacta
    ctx.fillStyle='#304a20';
    ctx.beginPath();ctx.ellipse(x,y-r*1.05,r*.42,r*.45,0,0,6.28);ctx.fill();
    // Yelmo roto
    ctx.fillStyle='#2a1a0a';
    ctx.fillRect(x-r*.42,y-r*1.45,r*.84,r*.48);
    ctx.fillStyle='#3a2a18';
    ctx.fillRect(x-r*.38,y-r*1.5,r*.76,r*.18);
    // Ranura de visera con brillo
    ctx.fillStyle='#88cc44';
    ctx.fillRect(x-r*.32,y-r*1.22,r*.64,r*.14);
    // Ojos brillantes verdes
    ctx.fillStyle='#44ff22';
    ctx.beginPath();ctx.arc(x-r*.16,y-r*1.18,r*.07,0,6.28);ctx.fill();
    ctx.beginPath();ctx.arc(x+r*.16,y-r*1.18,r*.07,0,6.28);ctx.fill();
    // Espada oxidada
    ctx.fillStyle='#4a3a28';
    ctx.fillRect(x+r*.65,y-r*1.3,r*.22,r*1.9);
    ctx.fillStyle='#6a5a38';
    ctx.fillRect(x+r*.68,y-r*1.3,r*.16,r*1.9);
    // Guarda de espada
    ctx.fillStyle='#4a3a28';
    ctx.fillRect(x+r*.5,y-r*.35,r*.52,r*.18);
    // Escudo deteriorado
    ctx.fillStyle='#2a1a0a';
    ctx.beginPath();ctx.ellipse(x-r*.85,y,r*.32,r*.42,0,0,6.28);ctx.fill();
    ctx.strokeStyle='#5a3a18';ctx.lineWidth=1.5;
    ctx.beginPath();ctx.ellipse(x-r*.85,y,r*.32,r*.42,0,0,6.28);ctx.stroke();
    ctx.fillStyle='#44ff22';
    ctx.beginPath();ctx.arc(x-r*.85,y,r*.1,0,6.28);ctx.fill();
    // Aura verde necromántica
    ctx.fillStyle='rgba(68,255,34,.08)';
    ctx.beginPath();ctx.arc(x,y,r*1.2,0,6.28);ctx.fill();
  },

  // F — Dragón Espectral: dragón grande morado etéreo
  dragon:(ctx,x,y,r,col)=>{
    const t=performance.now()*.0018;
    // Aura grande
    ctx.fillStyle='rgba(147,51,234,.1)';
    ctx.beginPath();ctx.arc(x,y,r*1.8,0,6.28);ctx.fill();
    // Cola ondulante
    ctx.strokeStyle='#6a1aaa';ctx.lineWidth=r*.35;ctx.lineCap='round';
    ctx.beginPath();
    ctx.moveTo(x-r*.4,y+r*.3);
    ctx.quadraticCurveTo(x-r*1.2,y+r*.8+Math.sin(t)*r*.3,x-r*1.8,y+r*.3+Math.sin(t+1)*r*.25);
    ctx.stroke();
    ctx.strokeStyle='#9333ea';ctx.lineWidth=r*.15;
    ctx.beginPath();
    ctx.moveTo(x-r*.4,y+r*.3);
    ctx.quadraticCurveTo(x-r*1.2,y+r*.8+Math.sin(t)*r*.3,x-r*1.8,y+r*.3+Math.sin(t+1)*r*.25);
    ctx.stroke();
    // Cuerpo principal
    ctx.fillStyle='#4a0a8a';
    ctx.beginPath();ctx.ellipse(x,y,r*.85,r*.65,0,0,6.28);ctx.fill();
    ctx.fillStyle='#6a2aaa';
    ctx.beginPath();ctx.ellipse(x,y,r*.6,r*.45,0,0,6.28);ctx.fill();
    // Escamas
    ctx.strokeStyle='#8840cc';ctx.lineWidth=1;
    for(let s=0;s<5;s++){
      const sx=x-r*.4+s*r*.2,sy=y-r*.1;
      ctx.beginPath();ctx.arc(sx,sy,r*.15,Math.PI,0);ctx.stroke();
    }
    // Alas
    for(const ws of[-1,1]){
      ctx.fillStyle='rgba(74,10,138,.75)';
      ctx.beginPath();
      ctx.moveTo(x+ws*r*.5,y-r*.2);
      ctx.lineTo(x+ws*r*1.7,y-r*1.1+Math.sin(t+ws)*r*.15);
      ctx.lineTo(x+ws*r*1.4,y+r*.3);
      ctx.lineTo(x+ws*r*.6,y+r*.1);
      ctx.closePath();ctx.fill();
      // Membrana alar interna
      ctx.fillStyle='rgba(147,51,234,.3)';
      ctx.beginPath();
      ctx.moveTo(x+ws*r*.55,y-r*.15);
      ctx.lineTo(x+ws*r*1.5,y-r*.9+Math.sin(t+ws)*r*.12);
      ctx.lineTo(x+ws*r*1.2,y+r*.2);
      ctx.closePath();ctx.fill();
    }
    // Cuello y cabeza
    ctx.fillStyle='#4a0a8a';
    ctx.beginPath();ctx.ellipse(x+r*.5,y-r*.6,r*.28,r*.45,.4,0,6.28);ctx.fill();
    // Cabeza
    ctx.fillStyle='#5a1a9a';
    ctx.beginPath();ctx.ellipse(x+r*.75,y-r*1.05,r*.42,r*.32,0.3,0,6.28);ctx.fill();
    // Cuernos
    ctx.fillStyle='#cc88ff';
    ctx.beginPath();ctx.moveTo(x+r*.62,y-r*1.25);ctx.lineTo(x+r*.5,y-r*1.65);ctx.lineTo(x+r*.72,y-r*1.28);ctx.closePath();ctx.fill();
    ctx.beginPath();ctx.moveTo(x+r*.88,y-r*1.28);ctx.lineTo(x+r*.95,y-r*1.62);ctx.lineTo(x+r*1.0,y-r*1.28);ctx.closePath();ctx.fill();
    // Ojos dragón
    ctx.fillStyle='#ffcc00';
    ctx.beginPath();ctx.ellipse(x+r*.68,y-r*1.05,r*.1,r*.08,0.3,0,6.28);ctx.fill();
    ctx.beginPath();ctx.ellipse(x+r*.9,y-r*1.02,r*.1,r*.08,0.3,0,6.28);ctx.fill();
    ctx.fillStyle='#220000';
    ctx.beginPath();ctx.ellipse(x+r*.68,y-r*1.05,r*.05,r*.07,0.3,0,6.28);ctx.fill();
    ctx.beginPath();ctx.ellipse(x+r*.9,y-r*1.02,r*.05,r*.07,0.3,0,6.28);ctx.fill();
    // Fuego de la boca
    ctx.fillStyle='rgba(200,100,255,.8)';
    ctx.beginPath();ctx.moveTo(x+r*1.1,y-r*.95);ctx.lineTo(x+r*1.6,y-r*.8+Math.sin(t*2)*r*.1);ctx.lineTo(x+r*1.1,y-r*.85);ctx.closePath();ctx.fill();
    ctx.fillStyle='rgba(255,200,255,.6)';
    ctx.beginPath();ctx.moveTo(x+r*1.12,y-r*.92);ctx.lineTo(x+r*1.45,y-r*.82+Math.sin(t*2)*r*.08);ctx.lineTo(x+r*1.12,y-r*.86);ctx.closePath();ctx.fill();
  },
};

// ═══════════════════════════════════════════
//  GAME STATE  — clase seleccionada se guarda FUERA de G
// ═══════════════════════════════════════════
let selectedClass = 'warrior';   // ← variable global independiente del estado de juego

let G={},canvas,ctx,tileCanvas,tileCtx;
let keys={},mouse={x:0,y:0,down:false,clicked:false};
let raf,lastTime=0,notifTO;

function mkState(){
  return{
    cls: selectedClass,   // ← siempre usa la clase actualmente seleccionada
    floor:1,kills:0,
    player:null,enemies:[],projectiles:[],particles:[],minions:[],pickups:[],dmgNums:[],
    tiles:[],stairs:null,cleared:false,abCDs:[0,0,0,0],
    berserkEnd:0,shieldHits:0,cam:{x:0,y:0}
  };
}

// ═══════════════════════════════════════════
//  MENU
// ═══════════════════════════════════════════
function selectClass(c, el){
  selectedClass = c;   // ← guarda en variable global
  document.querySelectorAll('.class-card').forEach(x=>x.classList.remove('selected'));
  el.classList.add('selected');
}

function startGame(){
  G = mkState();       // mkState() ya lee selectedClass correctamente
  initGame();
}

function goMenu(){
  cancelAnimationFrame(raf);
  show('menuScreen');hide('gameScreen');hide('hud');hide('endScreen');hide('gameControls');hide('pauseScreen');
  paused=false;
  document.querySelectorAll('.class-card').forEach(x=>x.classList.remove('selected'));
  const card = document.getElementById('card-'+selectedClass);
  if(card) card.classList.add('selected');
  refreshContinueBtn();
}

function restartGame(){hide('endScreen');startGame();}
function show(id){document.getElementById(id).classList.remove('hidden');}
function hide(id){document.getElementById(id).classList.add('hidden');}

// ═══════════════════════════════════════════
//  PAUSE
// ═══════════════════════════════════════════
let paused=false;
function togglePause(){
  paused=!paused;
  const btn=document.getElementById('pauseBtn');
  if(paused){
    cancelAnimationFrame(raf);
    btn.textContent='▶';btn.querySelector('.ctt').textContent='REANUDAR';
    // Update pause info panel
    const p=G.player;
    document.getElementById('pauseInfo').innerHTML=
      `Clase: ${CLASSES[G.cls].name} &nbsp;|&nbsp; Piso: ${G.floor} &nbsp;|&nbsp; Nivel: ${p.lv}<br>`+
      `HP: ${Math.round(p.hp)}/${Math.round(p.mhp)} &nbsp;|&nbsp; Oro: ${p.gold} &nbsp;|&nbsp; Kills: ${G.kills}`;
    show('pauseScreen');
  }else{
    btn.innerHTML='⏸<span class="ctt">PAUSAR</span>';
    hide('pauseScreen');
    lastTime=performance.now();
    loop(lastTime);
  }
}

// ═══════════════════════════════════════════
//  SAVE / LOAD
// ═══════════════════════════════════════════
function saveGame(){
  const p=G.player;if(!p)return;
  const save={
    cls:G.cls,floor:G.floor,kills:G.kills,
    player:{hp:p.hp,mhp:p.mhp,atk:p.atk,def:p.def,spd:p.spd,
            exp:p.exp,expN:p.expN,lv:p.lv,gold:p.gold,r:p.r,face:p.face,iframes:0},
    abCDs:[0,0,0,0],berserkEnd:0,shieldHits:0,
    savedAt:new Date().toLocaleString('es')
  };
  localStorage.setItem('dungeonSave',JSON.stringify(save));
  // Flash save button
  const btn=document.getElementById('saveBtn');
  btn.classList.add('saved');
  btn.textContent='✔';
  setTimeout(()=>{btn.classList.remove('saved');btn.textContent='💾';},1000);
  showNotif('💾 Progreso guardado',save.savedAt,'#4cc9f0');
}

function loadSave(){
  const raw=localStorage.getItem('dungeonSave');
  if(!raw)return null;
  try{return JSON.parse(raw);}catch(e){return null;}
}

function refreshContinueBtn(){
  const save=loadSave();
  const btn=document.getElementById('continueBtn');
  const info=document.getElementById('saveInfo');
  if(save){
    btn.disabled=false;
    const cls=CLASSES[save.cls]?CLASSES[save.cls].name:save.cls;
    info.textContent=`${cls}  •  Piso ${save.floor}  •  Nivel ${save.player.lv}  •  ${save.savedAt||''}`;
    info.style.color='var(--text2)';
  }else{
    btn.disabled=true;
    info.textContent='— Sin partida guardada —';
  }
}

function continueGame(){
  const save=loadSave();
  if(!save){showNotif('Sin guardado','No hay partida guardada','#e74c3c');return;}
  // Seleccionar la clase del guardado visualmente
  selectedClass=save.cls;
  document.querySelectorAll('.class-card').forEach(x=>x.classList.remove('selected'));
  const card=document.getElementById('card-'+save.cls);
  if(card)card.classList.add('selected');
  // Reconstruir estado desde el guardado
  G=mkState();
  G.floor=save.floor;
  G.kills=save.kills||0;
  G.player={...save.player, iframes:0, face:save.player.face||1};
  G.abCDs=[0,0,0,0];
  G.berserkEnd=0;
  G.shieldHits=0;
  initGame();
  showNotif('▶ Partida cargada',`Piso ${save.floor} — Nivel ${save.player.lv}`,CLASSES[save.cls].color);
}

function confirmRestart(){
  if(confirm('¿Reiniciar la partida? El progreso no guardado se perderá.')){
    if(paused){paused=false;hide('pauseScreen');}
    restartGame();
  }
}

function pauseGoMenu(){
  paused=false;hide('pauseScreen');
  goMenu();
}

// ═══════════════════════════════════════════
//  INIT
// ═══════════════════════════════════════════
function initGame(){
  hide('menuScreen');hide('endScreen');show('gameScreen');show('hud');show('gameControls');
  paused=false;
  canvas=document.getElementById('gameCanvas');
  canvas.width=window.innerWidth;canvas.height=window.innerHeight;
  ctx=canvas.getContext('2d');ctx.imageSmoothingEnabled=false;
  tileCanvas=document.createElement('canvas');
  tileCanvas.width=W;tileCanvas.height=H;
  tileCtx=tileCanvas.getContext('2d');
  setupInput();
  newFloor(true);
  buildAbBar();
  updateHUD();
  cancelAnimationFrame(raf);
  lastTime=performance.now();
  loop(lastTime);
}

function newFloor(fresh){
  const c=CLASSES[G.cls];
  if(fresh||!G.player){
    G.player={x:W/2,y:H/2,hp:c.hp,mhp:c.hp,atk:c.atk,def:c.def,spd:c.spd,
      exp:0,expN:100,lv:1,gold:0,r:16,face:1,iframes:0};
  }else{
    G.player.hp=Math.min(G.player.mhp,G.player.hp+G.player.mhp*.3);
  }
  G.enemies=[];G.projectiles=[];G.particles=[];G.minions=[];G.pickups=[];G.dmgNums=[];
  G.cleared=false;G.stairs=null;G.abCDs=G.abCDs||[0,0,0,0];
  genTiles();renderTileCache();spawnEnemies();updateHUD();
}

// ═══════════════════════════════════════════
//  TILES
// ═══════════════════════════════════════════
function genTiles(){
  G.tiles=[];
  for(let r=0;r<ROWS;r++){G.tiles[r]=[];for(let c=0;c<COLS;c++){G.tiles[r][c]=(r===0||r===ROWS-1||c===0||c===COLS-1||Math.random()<.055)?1:0;}}
  for(let r=6;r<12;r++)for(let c=10;c<15;c++)G.tiles[r][c]=0;
}
function isSolid(wx,wy){
  const c=wx/TILE|0,r=wy/TILE|0;
  if(r<0||r>=ROWS||c<0||c>=COLS)return true;
  return G.tiles[r][c]===1;
}
function renderTileCache(){
  tileCtx.fillStyle='#0d0910';tileCtx.fillRect(0,0,W,H);
  for(let r=0;r<ROWS;r++){
    for(let c=0;c<COLS;c++){
      const x=c*TILE,y=r*TILE;
      if(G.tiles[r][c]===1){
        // Base stone — much brighter than floor
        tileCtx.fillStyle='#3a2e40';tileCtx.fillRect(x,y,TILE,TILE);
        // Inner beveled face
        tileCtx.fillStyle='#2e2438';tileCtx.fillRect(x+4,y+4,TILE-8,TILE-8);
        // Top-left highlight
        tileCtx.fillStyle='#5a4a68';tileCtx.fillRect(x,y,TILE,3);
        tileCtx.fillStyle='#4a3a58';tileCtx.fillRect(x,y,3,TILE);
        // Bottom-right shadow
        tileCtx.fillStyle='#1a1020';tileCtx.fillRect(x,y+TILE-3,TILE,3);
        tileCtx.fillStyle='#1a1020';tileCtx.fillRect(x+TILE-3,y,3,TILE);
        // Corner rivets
        tileCtx.fillStyle='#7a6888';
        tileCtx.fillRect(x+1,y+1,5,5);tileCtx.fillRect(x+TILE-6,y+1,5,5);
        tileCtx.fillStyle='#1a1020';
        tileCtx.fillRect(x+1,y+TILE-6,5,5);tileCtx.fillRect(x+TILE-6,y+TILE-6,5,5);
        // Bright outer border — clearly separates wall from floor
        tileCtx.strokeStyle='#7050b0';tileCtx.lineWidth=1.5;
        tileCtx.strokeRect(x+.75,y+.75,TILE-1.5,TILE-1.5);
        // Crack detail on some tiles
        if((r*7+c*13)%5===0){
          tileCtx.strokeStyle='rgba(0,0,0,.55)';tileCtx.lineWidth=1;
          tileCtx.beginPath();
          tileCtx.moveTo(x+10,y+14);tileCtx.lineTo(x+18,y+22);tileCtx.lineTo(x+14,y+32);
          tileCtx.stroke();
        }
      }else{
        const shade=(r+c)%2===0?'#120e14':'#100c12';
        tileCtx.fillStyle=shade;tileCtx.fillRect(x,y,TILE,TILE);
        tileCtx.strokeStyle='#1a1520';tileCtx.lineWidth=.5;tileCtx.strokeRect(x,y,TILE,TILE);
      }
    }
  }
}

// ═══════════════════════════════════════════
//  ENEMY SPAWN
// ═══════════════════════════════════════════
function spawnEnemies(){
  const f=G.floor,mult=Math.pow(1.15,f-1);
  const pool=ENEMY_DEFS.filter(e=>!e.isBoss&&e.mf<=f);
  const count=4+f;
  for(let i=0;i<count;i++){
    const d=pool[Math.random()*pool.length|0];
    mkEnemy(d,mult);
  }
  if(f%5===0){mkEnemy(ENEMY_DEFS[6],mult*1.5);showNotif('⚠ JEFE ⚠','Caballero Oscuro ha aparecido!','#c0392b');}
}
function mkEnemy(d,mult){
  let x,y,t=0;
  do{x=TILE*2+Math.random()*(W-TILE*4);y=TILE*2+Math.random()*(H-TILE*4);t++;}
  while(dst(x,y,W/2,H/2)<160&&t<30);
  G.enemies.push({...d,x,y,
    hp:Math.round(d.hp*mult),mhp:Math.round(d.hp*mult),
    atk:Math.round(d.atk*mult),exp:Math.round(d.exp*mult),gold:Math.round(d.gold*mult),
    r:d.isBoss?30:20,acd:0,poison:0,frozen:0,uid:Math.random(),wb:Math.random()*6.28});
}

// ═══════════════════════════════════════════
//  INPUT
// ═══════════════════════════════════════════
function setupInput(){
  window.onkeydown=e=>{
    keys[e.key.toLowerCase()]=true;
    if(e.key.toLowerCase()==='p'||e.key==='Escape'){togglePause();return;}
    if(paused)return;
    if(e.key.toLowerCase()==='q')useAb(0);
    if(e.key.toLowerCase()==='e')useAb(1);
    if(e.key.toLowerCase()==='r')useAb(2);
    if(e.key.toLowerCase()==='f')useAb(3);
  };
  window.onkeyup=e=>{keys[e.key.toLowerCase()]=false;};
  canvas.onmousemove=e=>{const rc=canvas.getBoundingClientRect();mouse.x=e.clientX-rc.left;mouse.y=e.clientY-rc.top;};
  canvas.onmousedown=()=>{mouse.down=true;mouse.clicked=true;};
  canvas.onmouseup=()=>{mouse.down=false;};
  window.onresize=()=>{canvas.width=window.innerWidth;canvas.height=window.innerHeight;};
}

// ═══════════════════════════════════════════
//  ABILITIES BAR
// ═══════════════════════════════════════════
function buildAbBar(){
  const bar=document.getElementById('abBar');
  bar.innerHTML='';
  const col=CLASSES[G.cls].color;
  CLASSES[G.cls].ab.forEach((a,i)=>{
    const s=document.createElement('div');
    s.className='ab-slot locked';s.id='abs'+i;
    s.title=a.desc;
    s.innerHTML=`<span class="sk">${a.k}</span><span class="si" style="color:${col}">${a.i}</span><span class="sn">${a.n}</span>`;
    s.onclick=()=>useAb(i);
    bar.appendChild(s);
  });
  refreshAbBar();
}

function refreshAbBar(){
  const now=performance.now()/1000,p=G.player,ab=CLASSES[G.cls].ab;
  ab.forEach((a,i)=>{
    const el=document.getElementById('abs'+i);if(!el)return;
    const unlocked=p&&p.lv>=a.lv;
    el.className='ab-slot '+(unlocked?'unlocked':'locked');
    let ov=el.querySelector('.cd-ov');
    const cd=G.abCDs[i]-now;
    if(cd>0){
      if(!ov){ov=document.createElement('div');ov.className='cd-ov';el.appendChild(ov);}
      ov.textContent=cd.toFixed(1)+'s';
    }else if(ov)ov.remove();
  });
}

function useAb(i){
  const p=G.player,ab=CLASSES[G.cls].ab[i];
  if(!p||p.lv<ab.lv)return;
  const now=performance.now()/1000;
  if(G.abCDs[i]>now)return;
  G.abCDs[i]=now+ab.cd;
  const mx=mouse.x-canvas.width/2+G.cam.x;
  const my=mouse.y-canvas.height/2+G.cam.y;
  ({warrior:wAb,summoner:sAb,mage:mAb,assassin:aAb}[G.cls])(i,p,mx,my);
  refreshAbBar();
}

function wAb(i,p){
  const col=CLASSES[G.cls].color;
  if(i===0){aoe(p.x,p.y,120,p.atk*1.8,col);showNotif('Golpe Giratorio!','','',col);}
  else if(i===1){G.berserkEnd=performance.now()/1000+5;burst(p.x,p.y,12,'#ff4444');showNotif('Furia Berserk!','ATQ x2 por 5s',col);}
  else if(i===2){G.shieldHits=3;showNotif('Postura Escudo!','3 golpes bloqueados',col);}
  else{aoe(p.x,p.y,200,p.atk*4,col);burst(p.x,p.y,18,'#ffd700');showNotif('Torbellino!','',col);}
}
function sAb(i,p){
  const MAX_PER_TYPE=10;
  // Cada habilidad invoca un "tipo" distinto (0=minion,1=espectro,2=ejercito,3=dragon)
  const type=['minion','specter','army','dragon'][i];
  const n=i===2?3:1;
  // Contar cuántos súbditos de este tipo ya existen
  const existing=G.minions.filter(m=>m.type===type).length;
  const slots=Math.min(n, MAX_PER_TYPE-existing);
  if(slots<=0){
    showNotif('¡Límite alcanzado!','Ya tienes 10 '+type+'s',CLASSES[G.cls].color);
    return;
  }
  // Daño = triple del ATQ del invocador; dragón hace el doble de eso
  const baseDmg = p.atk * 3 * (i===3 ? 2 : 1);
  for(let j=0;j<slots;j++){
    const a=Math.random()*6.28;
    const typeRadii={minion:13,specter:15,army:16,dragon:26};
    G.minions.push({
      x:p.x+Math.cos(a)*40, y:p.y+Math.sin(a)*40,
      hp:60+p.lv*8, mhp:60+p.lv*8,
      atk:baseDmg,
      spd:type==='dragon'?4:type==='specter'?3.5:3,
      r:typeRadii[type],
      acd:0,
      type,
      uid:Math.random()
    });
  }
  const total=existing+slots;
  showNotif(
    type==='dragon'?'🐉 Dragón Espectral!':'☠ Minion invocado!',
    `${total}/${MAX_PER_TYPE} — ATQ: ${Math.round(baseDmg)}`,
    CLASSES[G.cls].color
  );
}
function mAb(i,p,mx,my){
  const col=CLASSES[G.cls].color;
  const dx=mx-p.x,dy=my-p.y,l=Math.hypot(dx,dy)||1;
  if(i===0){pushProj(p.x,p.y,dx/l*8,dy/l*8,p.atk*2.5,10,'#e85d04','player',false);}
  else if(i===1){G.enemies.forEach(e=>{if(dst(e.x,e.y,p.x,p.y)<200){e.frozen=3;addDmg(e.x,e.y,'FREEZE','#4cc9f0');}});showNotif('Rayo de Hielo!','',col);}
  else if(i===2){aoe(p.x,p.y,180,p.atk*2,col);burst(p.x,p.y,14,col);showNotif('Tormenta Eléct.!','',col);}
  else{for(let j=0;j<8;j++){const a=j/8*6.28;pushProj(p.x,p.y,Math.cos(a)*6,Math.sin(a)*6,p.atk*4,14,'#ff6600','player',true);}showNotif('Meteorito!','',col);}
}
function aAb(i,p,mx,my){
  const col=CLASSES[G.cls].color;
  if(i===0){aoe(p.x,p.y,100,p.atk*1.5,col);G.enemies.forEach(e=>{if(dst(e.x,e.y,p.x,p.y)<100)e.poison=6;});showNotif('Veneno!','',col);}
  else if(i===1){p.x=mx;p.y=my;burst(p.x,p.y,10,col);showNotif('Teletransporte!','',col);}
  else if(i===2){for(let j=0;j<12;j++){const a=j/12*6.28;pushProj(p.x,p.y,Math.cos(a)*5,Math.sin(a)*5,p.atk*1.8,6,col,'player',false);}showNotif('Lluvia de Dagas!','',col);}
  else{const e=nearest(p.x,p.y);if(e){hitEnemy(e,p.atk*5);burst(e.x,e.y,20,col);showNotif('Sombra Mortal!','Crítico x5!',col);}}
}

// ═══════════════════════════════════════════
//  COMBAT
// ═══════════════════════════════════════════
function melee(){
  const p=G.player;if(!p)return;
  G.enemies.forEach(e=>{
    if(dst(e.x,e.y,p.x,p.y)<85){
      let d=p.atk;
      if(G.berserkEnd>performance.now()/1000)d*=2;
      hitEnemy(e,d);
    }
  });
  burst(p.x+p.face*42,p.y,5,CLASSES[G.cls].color);
}
function aoe(x,y,r,dmg,col){
  G.enemies.forEach(e=>{if(dst(e.x,e.y,x,y)<r){hitEnemy(e,dmg);burst(e.x,e.y,5,col);}});
}
function hitEnemy(e,dmg){
  const d=Math.max(1,dmg-e.def);e.hp-=d;
  addDmg(e.x,e.y-e.r,Math.round(d),'#f0bc5a');burst(e.x,e.y,3,'#c0392b');
  if(e.hp<=0)killEnemy(e);
}
function killEnemy(e){
  const p=G.player;
  p.exp+=e.exp;p.gold+=e.gold;G.kills++;
  burst(e.x,e.y,10,'#ffd700');
  if((e.id==='slime')&&!e._mini){
    for(let i=0;i<2;i++){
      const s={...ENEMY_DEFS[1],_mini:true,x:e.x+(i?18:-18),y:e.y,
        hp:12,mhp:12,atk:4,def:0,spd:2,r:12,acd:0,poison:0,frozen:0,uid:Math.random(),wb:0};
      G.enemies.push(s);
    }
  }
  if(Math.random()<.38)G.pickups.push({x:e.x,y:e.y,t:'g',v:e.gold,r:10,life:8});
  if(Math.random()<.22)G.pickups.push({x:e.x,y:e.y+18,t:'h',v:Math.round(G.player.mhp*.15),r:10,life:8});
  G.enemies=G.enemies.filter(x=>x!==e);
  while(p.exp>=p.expN){
    p.exp-=p.expN;p.lv++;p.expN=Math.round(p.expN*1.3);
    p.mhp=Math.round(p.mhp*1.1);p.hp=p.mhp;
    p.atk=Math.round(p.atk*1.08);p.def=Math.round(p.def*1.06);
    const na=CLASSES[G.cls].ab.find(a=>a.lv===p.lv);
    showNotif('✦ Nivel '+p.lv+'!',na?na.n.replace('\n',' ')+' desbloqueada!':'Stats aumentados',CLASSES[G.cls].color);
    refreshAbBar();
  }
  if(G.enemies.length===0&&!G.cleared){
    G.cleared=true;G.stairs={x:W/2+80,y:H/2+40};
    showNotif('PISO LIMPIADO','Busca las escaleras','#c9922a');
  }
  updateHUD();
}
function nearest(x,y){let r=null,m=Infinity;G.enemies.forEach(e=>{const d=dst(e.x,e.y,x,y);if(d<m){m=d;r=e;}});return r;}
function pushProj(x,y,vx,vy,dmg,r,col,own,pierce){G.projectiles.push({x,y,vx,vy,dmg,r,col,own,pierce,life:3,dead:false});}

// ═══════════════════════════════════════════
//  UPDATE
// ═══════════════════════════════════════════
function update(dt){
  const p=G.player;if(!p)return;
  const now=performance.now()/1000;

  let vx=(keys['a']||keys['arrowleft']?-1:0)+(keys['d']||keys['arrowright']?1:0);
  let vy=(keys['w']||keys['arrowup']?-1:0)+(keys['s']||keys['arrowdown']?1:0);
  if(vx&&vy){vx*=.707;vy*=.707;}
  if(vx)p.face=vx>0?1:-1;
  const step=p.spd*60*dt;
  const nx=p.x+vx*step,ny=p.y+vy*step;
  if(!isSolid(nx,p.y))p.x=nx;
  if(!isSolid(p.x,ny))p.y=ny;
  p.x=Math.max(TILE,Math.min(W-TILE,p.x));
  p.y=Math.max(TILE,Math.min(H-TILE,p.y));
  if(p.iframes>0)p.iframes-=dt;
  G.cam.x=p.x;G.cam.y=p.y;

  if(mouse.clicked){mouse.clicked=false;melee();}

  for(let i=G.enemies.length-1;i>=0;i--){
    const e=G.enemies[i];
    if(e.frozen>0){e.frozen-=dt;continue;}
    if(e.poison>0){e.poison-=dt;if(Math.random()<dt*2){e.hp-=Math.round(e.atk*.25);if(e.hp<=0){killEnemy(e);continue;}}}
    e.wb+=dt*1.5;
    const dx=p.x-e.x,dy=p.y-e.y,d=Math.hypot(dx,dy)||1;
    if(e.id==='vampire'&&e.hp<e.mhp*.2&&d>120){e.x-=dx/d*e.spd*50*dt;e.y-=dy/d*e.spd*50*dt;}
    else if(d>e.r+p.r){e.x+=dx/d*e.spd*50*dt;e.y+=dy/d*e.spd*50*dt;}
    if(d<e.r+p.r+6&&now>e.acd){
      e.acd=now+(e.id==='golem'?2.2:1.1);
      if(p.iframes<=0){
        let dmg=Math.max(1,e.atk-p.def);
        if(G.shieldHits>0){G.shieldHits--;addDmg(p.x,p.y-30,'BLOCK','#c9922a');dmg=0;}
        if(e.id==='vampire'){e.hp=Math.min(e.mhp,e.hp+dmg*.4);}
        p.hp-=dmg;p.iframes=.45;
        addDmg(p.x,p.y-30,Math.round(dmg),'#e74c3c');
        if(p.hp<=0){endGame(false);return;}
        updateHUD();
      }
    }
    if(e.id==='witch'&&d<320&&now>e.acd-.3){
      pushProj(e.x,e.y,dx/d*5,dy/d*5,e.atk,7,'#9933cc','enemy',false);
      e.acd=now+2.2;
    }
  }

  for(let i=G.minions.length-1;i>=0;i--){
    const m=G.minions[i];
    if(m.hp<=0){G.minions.splice(i,1);continue;}
    const t=nearest(m.x,m.y);
    if(t){
      const dx=t.x-m.x,dy=t.y-m.y,d=Math.hypot(dx,dy)||1;
      if(d>m.r+t.r+4){m.x+=dx/d*m.spd*50*dt;m.y+=dy/d*m.spd*50*dt;}
      if(d<m.r+t.r+8&&now>m.acd){m.acd=now+1;hitEnemy(t,m.atk);}
    }
  }

  for(let i=G.projectiles.length-1;i>=0;i--){
    const pr=G.projectiles[i];
    pr.x+=pr.vx*50*dt;pr.y+=pr.vy*50*dt;pr.life-=dt;
    if(pr.life<=0||isSolid(pr.x,pr.y)){G.projectiles.splice(i,1);continue;}
    if(pr.own==='player'){
      for(let j=G.enemies.length-1;j>=0;j--){
        const e=G.enemies[j];
        if(dst(pr.x,pr.y,e.x,e.y)<pr.r+e.r){
          hitEnemy(e,pr.dmg);
          if(!pr.pierce){G.projectiles.splice(i,1);break;}
        }
      }
    }else{
      if(p.iframes<=0&&dst(pr.x,pr.y,p.x,p.y)<pr.r+p.r){
        let d=Math.max(1,pr.dmg-p.def);
        if(G.shieldHits>0){G.shieldHits--;d=0;}
        p.hp-=d;p.iframes=.3;
        if(p.hp<=0){endGame(false);return;}
        G.projectiles.splice(i,1);updateHUD();
      }
    }
  }

  for(let i=G.particles.length-1;i>=0;i--){
    const q=G.particles[i];
    q.x+=q.vx*50*dt;q.y+=q.vy*50*dt;q.vy+=1.5*dt*50;q.life-=dt;
    if(q.life<=0)G.particles.splice(i,1);
  }

  for(let i=G.dmgNums.length-1;i>=0;i--){
    const dn=G.dmgNums[i];dn.y-=24*dt;dn.life-=dt;
    if(dn.life<=0)G.dmgNums.splice(i,1);
  }

  for(let i=G.pickups.length-1;i>=0;i--){
    const pk=G.pickups[i];pk.life-=dt;
    if(pk.life<=0){G.pickups.splice(i,1);continue;}
    if(dst(pk.x,pk.y,p.x,p.y)<pk.r+p.r+6){
      if(pk.t==='g'){p.gold+=pk.v;addDmg(pk.x,pk.y,'+'+pk.v+'g','#ffd700');}
      else{p.hp=Math.min(p.mhp,p.hp+pk.v);addDmg(pk.x,pk.y,'+'+pk.v+'hp','#2ecc71');}
      G.pickups.splice(i,1);updateHUD();
    }
  }

  if(G.stairs&&dst(p.x,p.y,G.stairs.x,G.stairs.y)<40){
    G.floor++;
    showNotif('Piso '+G.floor,'Bajando a las profundidades...','#c9922a');
    newFloor(false);
    document.getElementById('floorBadge').textContent=G.floor;
  }

  refreshAbBar();
}

// ═══════════════════════════════════════════
//  DRAW
// ═══════════════════════════════════════════
function draw(){
  const cw=canvas.width,ch=canvas.height;
  ctx.clearRect(0,0,cw,ch);
  const ox=cw/2-G.cam.x,oy=ch/2-G.cam.y;
  const vx0=-ox,vy0=-oy,vx1=vx0+cw,vy1=vy0+ch;

  ctx.drawImage(tileCanvas,ox,oy);

  ctx.save();
  ctx.translate(ox,oy);

  if(G.stairs){
    const{x,y}=G.stairs,pulse=.8+Math.sin(performance.now()*.0025)*.2;
    ctx.globalAlpha=pulse;
    ctx.fillStyle='rgba(201,146,42,.25)';
    ctx.beginPath();ctx.arc(x,y,30,0,6.28);ctx.fill();
    ctx.globalAlpha=1;
    ctx.fillStyle=`rgba(201,146,42,${pulse})`;
    for(let s=0;s<4;s++)ctx.fillRect(x-18+s*5,y-10+s*7,34-s*8,6);
    ctx.fillStyle='#f0bc5a';ctx.font='bold .52rem Cinzel,serif';
    ctx.textAlign='center';ctx.fillText('BAJAR',x,y+38);
    ctx.globalAlpha=1;
  }

  for(const pk of G.pickups){
    ctx.globalAlpha=Math.min(1,pk.life);
    ctx.fillStyle=pk.t==='g'?'#ffd700':'#e74c3c';
    ctx.beginPath();ctx.arc(pk.x,pk.y,pk.r,0,6.28);ctx.fill();
    ctx.fillStyle='rgba(255,255,255,.4)';
    ctx.beginPath();ctx.arc(pk.x-pk.r*.3,pk.y-pk.r*.3,pk.r*.25,0,6.28);ctx.fill();
    ctx.globalAlpha=1;
  }

  for(const m of G.minions){
    if(m.x<vx0-55||m.x>vx1+55||m.y<vy0-55||m.y>vy1+55)continue;
    const shapeKey=m.type||'minion';
    const fn=SHAPES[shapeKey]||SHAPES.minion;
    fn(ctx,m.x,m.y,m.r,CLASSES[G.cls].color);
    drawHPbar(m.x,m.y,m.r,m.hp,m.mhp,'#9333ea');
    // Label del tipo encima
    ctx.fillStyle='rgba(147,51,234,.9)';ctx.font='bold .38rem Cinzel,serif';
    ctx.textAlign='center';
    const labels={minion:'MINION',specter:'ESPECTRO',army:'GUERRERO',dragon:'DRAGÓN'};
    ctx.fillText(labels[m.type]||'ALIADO',m.x,m.y-m.r-14);
  }

  for(const e of G.enemies){
    if(e.x<vx0-50||e.x>vx1+50||e.y<vy0-50||e.y>vy1+50)continue;
    const bob=Math.sin(e.wb)*2.2;
    ctx.save();
    if(e.frozen>0)ctx.filter='hue-rotate(155deg) brightness(1.7) saturate(2)';
    else if(e.poison>0)ctx.filter='hue-rotate(90deg) saturate(2.5)';
    const fn=SHAPES[e.id]||SHAPES.zombie;
    fn(ctx,e.x,e.y+bob,e.r,null);
    ctx.filter='none';
    ctx.restore();
    drawHPbar(e.x,e.y,e.r,e.hp,e.mhp,e.hp/e.mhp>.5?'#2ecc71':e.hp/e.mhp>.25?'#f39c12':'#e74c3c');
    if(e.isBoss){
      ctx.fillStyle='#e74c3c';ctx.font='bold .52rem Cinzel,serif';
      ctx.textAlign='center';ctx.fillText(e.name,e.x,e.y-e.r-16);
    }
  }

  for(const pr of G.projectiles){
    if(pr.x<vx0||pr.x>vx1||pr.y<vy0||pr.y>vy1)continue;
    ctx.fillStyle=pr.col;
    ctx.beginPath();ctx.arc(pr.x,pr.y,pr.r,0,6.28);ctx.fill();
    ctx.fillStyle='rgba(255,255,255,.3)';
    ctx.beginPath();ctx.arc(pr.x-pr.r*.3,pr.y-pr.r*.3,pr.r*.35,0,6.28);ctx.fill();
  }

  for(const q of G.particles){
    ctx.globalAlpha=Math.max(0,q.life/q.ml);
    ctx.fillStyle=q.col;
    ctx.fillRect(q.x-q.r,q.y-q.r,q.r*2,q.r*2);
  }
  ctx.globalAlpha=1;

  const p=G.player;
  if(p){
    const flash=p.iframes>0&&(performance.now()/80|0)%2;
    if(!flash){
      ctx.save();
      if(G.berserkEnd>performance.now()/1000){ctx.shadowBlur=20;ctx.shadowColor='#ff3300';}
      if(G.shieldHits>0){ctx.shadowBlur=16;ctx.shadowColor='#c9922a';}
      if(p.face<0){ctx.save();ctx.scale(-1,1);SHAPES[G.cls](ctx,-p.x,p.y,p.r,CLASSES[G.cls].color);ctx.restore();}
      else SHAPES[G.cls](ctx,p.x,p.y,p.r,CLASSES[G.cls].color);
      ctx.restore();
    }
    if(mouse.down){
      ctx.strokeStyle='rgba(255,255,255,.06)';ctx.lineWidth=1;
      ctx.beginPath();ctx.arc(p.x,p.y,85,0,6.28);ctx.stroke();
    }
  }

  ctx.textAlign='center';ctx.textBaseline='middle';
  for(const dn of G.dmgNums){
    ctx.globalAlpha=Math.max(0,dn.life/dn.ml);
    ctx.fillStyle=dn.col;
    ctx.font='bold .82rem Cinzel,serif';
    ctx.fillText(dn.txt,dn.x,dn.y);
  }
  ctx.globalAlpha=1;

  ctx.restore();
}

function drawHPbar(x,y,r,hp,mhp,col){
  const w=r*2.4,h=4,bx=x-w/2,by=y-r-10;
  ctx.fillStyle='rgba(0,0,0,.5)';ctx.fillRect(bx-1,by-1,w+2,h+2);
  ctx.fillStyle='#1a0e0f';ctx.fillRect(bx,by,w,h);
  ctx.fillStyle=col;ctx.fillRect(bx,by,w*Math.max(0,hp/mhp),h);
}

// ═══════════════════════════════════════════
//  HELPERS
// ═══════════════════════════════════════════
function burst(x,y,n,col){
  const free=MAX_PART-G.particles.length;
  const count=Math.min(n,free);
  for(let i=0;i<count;i++){
    const a=Math.random()*6.28,s=1+Math.random()*3;
    G.particles.push({x,y,vx:Math.cos(a)*s,vy:Math.sin(a)*s-1.5,r:1.5+Math.random()*2,col,life:.4+Math.random()*.3,ml:.7});
  }
}
function addDmg(x,y,txt,col){
  if(G.dmgNums.length>=MAX_DMG)G.dmgNums.shift();
  G.dmgNums.push({x,y,txt:String(txt),col,life:.85,ml:.85});
}
function showNotif(t,s,col='#c9922a'){
  const b=document.getElementById('nb');
  document.getElementById('nt').textContent=t;
  document.getElementById('nt').style.color=col;
  document.getElementById('ns').textContent=s;
  b.classList.remove('hidden');
  clearTimeout(notifTO);
  notifTO=setTimeout(()=>b.classList.add('hidden'),2400);
}
function updateHUD(){
  const p=G.player;if(!p)return;
  document.getElementById('hpBar').style.width=(p.hp/p.mhp*100)+'%';
  document.getElementById('hpVal').textContent=Math.round(p.hp)+'/'+Math.round(p.mhp);
  document.getElementById('expBar').style.width=(p.exp/p.expN*100)+'%';
  document.getElementById('expVal').textContent=p.exp+'/'+p.expN;
  document.getElementById('levelVal').textContent=p.lv;
  document.getElementById('atkVal').textContent=Math.round(p.atk);
  document.getElementById('defVal').textContent=Math.round(p.def);
  document.getElementById('goldVal').textContent=p.gold;
  document.getElementById('floorBadge').textContent=G.floor;
  document.getElementById('className').textContent=CLASSES[G.cls].name;
  document.getElementById('killCount').textContent=G.kills;
  document.getElementById('enemyCount').textContent=G.enemies.length+' vivos';
}
function endGame(won){
  cancelAnimationFrame(raf);hide('hud');hide('gameScreen');hide('gameControls');hide('pauseScreen');
  paused=false;
  const p=G.player;
  document.getElementById('endTitle').textContent=won?'¡VICTORIA!':'GAME OVER';
  document.getElementById('endTitle').className='end-title '+(won?'win':'death');
  document.getElementById('endStats').innerHTML=`Clase: ${CLASSES[G.cls].name}<br>Piso: ${G.floor}<br>Nivel: ${p.lv}<br>Kills: ${G.kills}<br>Oro: ${p.gold}`;
  show('endScreen');
}
function dst(ax,ay,bx,by){const dx=ax-bx,dy=ay-by;return Math.sqrt(dx*dx+dy*dy);}

// ═══════════════════════════════════════════
//  LOOP
// ═══════════════════════════════════════════
function loop(ts){
  if(paused)return;
  const dt=Math.min((ts-lastTime)/1000,.05);
  lastTime=ts;
  update(dt);draw();
  raf=requestAnimationFrame(loop);
}

// Inicializar botón continuar al cargar
refreshContinueBtn();
</script>
</body>
</html>
