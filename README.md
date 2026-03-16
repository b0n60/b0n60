
<style>
@import url('https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@300;400;700&family=Bebas+Neue&family=DM+Sans:wght@300;400;600&display=swap');
*{box-sizing:border-box;margin:0;padding:0}
:root{
  --bg:#07080d;--bg2:#0d0e16;--bg3:#12131d;--bg4:#1a1b28;
  --g:#39ff14;--c:#00e5ff;--r:#ff2d55;--a:#ffcc00;--p:#bf5fff;--o:#ff6b35;
  --dim:rgba(255,255,255,.08);--dim2:rgba(255,255,255,.04);
  --muted:rgba(255,255,255,.3);--soft:rgba(255,255,255,.55);--w:#f0f0f0;
  --mono:'JetBrains Mono',monospace;--head:'Bebas Neue',sans-serif;--body:'DM Sans',sans-serif;
  --gb:rgba(255,255,255,.04);--gbh:rgba(255,255,255,.07);--gbr:rgba(255,255,255,.1);
}
html,body{background:var(--bg);color:var(--w);font-family:var(--body);overflow-x:hidden}
body::after{content:'';position:fixed;inset:0;background:repeating-linear-gradient(0deg,transparent,transparent 3px,rgba(0,0,0,.05) 3px,rgba(0,0,0,.05) 4px);pointer-events:none;z-index:9998}
.orb{position:fixed;border-radius:50%;pointer-events:none;z-index:0}
.orb1{width:500px;height:500px;background:radial-gradient(circle,rgba(57,255,20,.07) 0%,transparent 70%);top:-150px;left:-150px}
.orb2{width:400px;height:400px;background:radial-gradient(circle,rgba(0,229,255,.05) 0%,transparent 70%);top:40%;right:-100px}
.orb3{width:350px;height:350px;background:radial-gradient(circle,rgba(191,95,255,.04) 0%,transparent 70%);bottom:5%;left:10%}

/* GLASS */
.glass{background:var(--gb);border:1px solid var(--gbr);backdrop-filter:blur(14px);-webkit-backdrop-filter:blur(14px)}

/* HERO */
.hero{position:relative;z-index:2;padding:2.2rem 2rem 1.8rem;border-bottom:1px solid var(--dim)}
.hero-bg{position:absolute;inset:0;background-image:linear-gradient(rgba(57,255,20,.03) 1px,transparent 1px),linear-gradient(90deg,rgba(57,255,20,.03) 1px,transparent 1px);background-size:40px 40px;pointer-events:none}
.hero-scan{position:absolute;left:0;right:0;height:1px;background:rgba(57,255,20,.2);animation:scan 7s linear infinite;pointer-events:none}
@keyframes scan{0%{top:0;opacity:0}5%{opacity:1}95%{opacity:1}100%{top:100%;opacity:0}}
.hero-inner{position:relative;z-index:2;max-width:900px;margin:0 auto;display:grid;grid-template-columns:auto 1fr;gap:2rem;align-items:center}
@media(max-width:580px){.hero-inner{grid-template-columns:1fr}}

/* AVATAR */
.av{width:90px;height:90px;border:1px solid rgba(57,255,20,.45);border-radius:6px;background:rgba(57,255,20,.05);display:flex;align-items:center;justify-content:center;flex-shrink:0;position:relative;overflow:hidden;cursor:pointer;transition:all .3s}
.av:hover{border-color:var(--g);background:rgba(57,255,20,.1);transform:scale(1.03)}
.av-inner{position:relative;z-index:1;display:flex;flex-direction:column;align-items:center;gap:2px}
.av-penguin{font-size:32px;line-height:1;filter:drop-shadow(0 0 6px rgba(57,255,20,.5))}
.av-handle{font-family:var(--mono);font-size:8px;color:var(--g);letter-spacing:.1em}
.av-cursor{position:absolute;bottom:4px;right:6px;width:5px;height:10px;background:var(--g);animation:blink .7s step-end infinite}
@keyframes blink{50%{opacity:0}}
.av-tag{position:absolute;top:-7px;right:-7px;background:var(--r);color:#fff;font-size:6px;padding:2px 5px;border-radius:2px;font-family:var(--mono);letter-spacing:.08em;font-weight:700;z-index:3}

/* HANDLE */
.handle{font-family:var(--head);font-size:clamp(2.8rem,7vw,4.4rem);color:var(--g);line-height:.95;letter-spacing:.06em;text-shadow:0 0 40px rgba(57,255,20,.25)}
.handle-sub{font-family:var(--mono);font-size:10px;color:var(--muted);text-transform:uppercase;letter-spacing:.13em;margin:.3rem 0 .85rem;line-height:1.65}
.badges{display:flex;flex-wrap:wrap;gap:.3rem}
.badge{font-family:var(--mono);font-size:8px;padding:3px 8px;border-radius:2px;text-transform:uppercase;letter-spacing:.07em;border:1px solid;transition:all .2s;cursor:default;display:inline-flex;align-items:center;gap:4px}
.badge:hover{filter:brightness(1.3);transform:translateY(-1px)}
.b-g{color:var(--g);border-color:rgba(57,255,20,.3);background:rgba(57,255,20,.06)}
.b-c{color:var(--c);border-color:rgba(0,229,255,.28);background:rgba(0,229,255,.05)}
.b-r{color:var(--r);border-color:rgba(255,45,85,.28);background:rgba(255,45,85,.05)}
.b-a{color:var(--a);border-color:rgba(255,204,0,.28);background:rgba(255,204,0,.05)}
.b-p{color:var(--p);border-color:rgba(191,95,255,.28);background:rgba(191,95,255,.05)}
.hero-stats{display:flex;gap:1.8rem;margin-top:1.1rem;flex-wrap:wrap}
.hs{cursor:default}
.hs-n{font-family:var(--head);font-size:1.9rem;color:var(--g);line-height:1;transition:color .2s}
.hs:hover .hs-n{color:var(--c)}
.hs-l{font-family:var(--mono);font-size:7px;color:var(--muted);text-transform:uppercase;letter-spacing:.12em}

/* DROPDOWN NAV */
.nav-wrap{position:relative;z-index:100;background:rgba(7,8,13,.92);border-bottom:1px solid var(--dim);backdrop-filter:blur(16px);padding:.6rem 1.5rem}
.nav-label{font-family:var(--mono);font-size:9px;color:var(--muted);text-transform:uppercase;letter-spacing:.1em;margin-bottom:.4rem;display:flex;align-items:center;gap:.4rem}
.dropdown{position:relative;display:inline-block;width:100%}
.dd-btn{width:100%;background:var(--gb);border:1px solid var(--gbr);border-radius:4px;padding:.6rem 1rem;font-family:var(--mono);font-size:11px;color:var(--w);cursor:pointer;display:flex;align-items:center;justify-content:space-between;gap:.5rem;transition:all .2s;text-align:left}
.dd-btn:hover{background:var(--gbh);border-color:rgba(57,255,20,.3)}
.dd-btn.open{border-color:var(--g);background:var(--gbh)}
.dd-btn-left{display:flex;align-items:center;gap:.6rem}
.dd-chevron{font-size:10px;color:var(--muted);transition:transform .25s}
.dd-chevron.open{transform:rotate(180deg)}
.dd-menu{position:absolute;top:calc(100% + 4px);left:0;right:0;background:rgba(13,14,22,.97);border:1px solid var(--gbr);border-radius:4px;overflow:hidden;z-index:200;max-height:0;opacity:0;transition:max-height .3s cubic-bezier(.16,1,.3,1),opacity .2s}
.dd-menu.open{max-height:500px;opacity:1;border-color:rgba(57,255,20,.2)}
.dd-item{font-family:var(--mono);font-size:11px;padding:.6rem 1rem;cursor:pointer;display:flex;align-items:center;gap:.7rem;transition:background .15s,color .15s;color:var(--muted);border-bottom:1px solid var(--dim)}
.dd-item:last-child{border-bottom:none}
.dd-item:hover{background:rgba(57,255,20,.06);color:var(--w)}
.dd-item.active{color:var(--g);background:rgba(57,255,20,.05)}
.dd-item-icon{width:16px;height:16px;display:flex;align-items:center;justify-content:center;flex-shrink:0;font-size:13px}
.dd-item-label{flex:1}
.dd-item-tag{font-size:7px;color:var(--r);border:1px solid rgba(255,45,85,.25);padding:1px 5px;border-radius:2px;text-transform:uppercase;letter-spacing:.08em}
.dd-item-tag.live{color:var(--g);border-color:rgba(57,255,20,.25)}

/* PANELS */
.pnl{display:none;position:relative;z-index:2;max-width:900px;margin:0 auto;padding:1.8rem 1.5rem 3rem;animation:pfade .3s ease}
@keyframes pfade{from{opacity:0;transform:translateY(5px)}to{opacity:1;transform:none}}
.pnl.on{display:block}

/* SECTION LABEL */
.sl{font-family:var(--mono);font-size:8px;color:var(--g);text-transform:uppercase;letter-spacing:.18em;margin-bottom:.9rem;display:flex;align-items:center;gap:.7rem}
.sl::after{content:'';flex:1;height:1px;background:var(--dim)}
.sl-icon{font-size:12px}

/* TERMINAL */
.term{background:rgba(8,9,16,.95);border:1px solid rgba(57,255,20,.15);border-radius:6px;overflow:hidden;backdrop-filter:blur(8px)}
.tbar{background:rgba(255,255,255,.04);padding:.5rem 1rem;display:flex;align-items:center;gap:.45rem;border-bottom:1px solid var(--dim)}
.tdot{width:11px;height:11px;border-radius:50%;transition:filter .2s;cursor:pointer}
.tdot:hover{filter:brightness(1.4) saturate(1.3)}
.tbar-title{font-family:var(--mono);font-size:9px;color:var(--muted);margin-left:.4rem;flex:1}
.tbar-os{font-family:var(--mono);font-size:8px;color:var(--muted);display:flex;align-items:center;gap:.3rem}
.tbody{padding:.85rem 1rem;font-family:var(--mono);font-size:11.5px;line-height:1.9;height:360px;overflow-y:auto}
.tbody::-webkit-scrollbar{width:3px}.tbody::-webkit-scrollbar-thumb{background:rgba(57,255,20,.25)}
.tline{display:block;animation:tlfade .12s ease}
@keyframes tlfade{from{opacity:0}to{opacity:1}}
.tc{color:var(--g)}.ti{color:var(--c)}.tp{color:var(--r)}.tg{color:var(--a)}.tv{color:var(--p)}.tw{color:var(--w)}.td{color:var(--muted)}
.cursor{display:inline-block;width:6px;height:12px;background:var(--g);animation:blink .7s step-end infinite;vertical-align:middle}

/* CMD BUTTONS */
.cmd-btns{display:flex;gap:.45rem;flex-wrap:wrap;margin-top:.9rem}
.cb{font-family:var(--mono);font-size:8px;padding:5px 11px;border-radius:3px;cursor:pointer;text-transform:uppercase;letter-spacing:.08em;border:1px solid;transition:all .2s;background:none;display:inline-flex;align-items:center;gap:4px}
.cb:hover{filter:brightness(1.25);transform:translateY(-1px)}
.cb:active{transform:scale(.96)}
.cb-g{color:var(--g);border-color:rgba(57,255,20,.38)}
.cb-c{color:var(--c);border-color:rgba(0,229,255,.38)}
.cb-a{color:var(--a);border-color:rgba(255,204,0,.38)}
.cb-p{color:var(--p);border-color:rgba(191,95,255,.38)}
.cb-r{color:var(--r);border-color:rgba(255,45,85,.38)}

/* VITALS GRID */
.vitals-grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(145px,1fr));gap:.55rem;margin-top:.8rem}
.vcard{background:var(--gb);border:1px solid var(--gbr);border-radius:4px;padding:.75rem;transition:all .25s;cursor:default}
.vcard:hover{background:var(--gbh);border-color:rgba(0,229,255,.2);transform:translateY(-2px)}
.vcard-l{font-family:var(--mono);font-size:7px;color:var(--muted);text-transform:uppercase;letter-spacing:.1em;margin-bottom:4px;display:flex;align-items:center;gap:4px}
.vcard-v{font-family:var(--mono);font-size:10px;color:var(--c)}

/* PALETTE */
.palette{display:flex;gap:5px;flex-wrap:wrap;margin-top:.5rem}
.pc{width:20px;height:20px;border-radius:2px;cursor:default;transition:transform .2s;border:1px solid rgba(255,255,255,.08)}
.pc:hover{transform:scale(1.4)}

/* SKILLS */
.skill-row{display:grid;grid-template-columns:160px 1fr 34px;align-items:center;gap:.75rem;margin-bottom:.6rem}
@media(max-width:500px){.skill-row{grid-template-columns:110px 1fr 28px}}
.sname{font-family:var(--mono);font-size:8px;color:var(--soft);text-transform:uppercase;letter-spacing:.06em;display:flex;align-items:center;gap:5px}
.track{height:4px;background:var(--dim);border-radius:2px;overflow:hidden}
.fill{height:100%;border-radius:2px;width:0;transition:width 1.5s cubic-bezier(.16,1,.3,1)}
.fg{background:var(--g)}.fc{background:var(--c)}.fp{background:var(--p)}.fa{background:var(--a)}
.spct{font-family:var(--mono);font-size:8px;color:var(--muted);text-align:right}

/* TOOL CARDS */
.tool-grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(200px,1fr));gap:.7rem;margin-top:.8rem}
.tc-card{background:var(--gb);border:1px solid var(--gbr);border-radius:5px;padding:1.1rem;transition:all .25s;position:relative;overflow:hidden;cursor:default}
.tc-card::before{content:'';position:absolute;top:0;left:0;right:0;height:2px;background:var(--c);transform:scaleX(0);transform-origin:left;transition:transform .35s}
.tc-card:hover{background:var(--gbh);border-color:rgba(0,229,255,.22);transform:translateY(-3px)}
.tc-card:hover::before{transform:scaleX(1)}
.tc-head{display:flex;align-items:center;gap:.5rem;margin-bottom:.3rem}
.tc-icon{font-size:16px}
.tc-name{font-family:var(--head);font-size:1.1rem;color:var(--c);letter-spacing:.05em}
.tc-rep{font-family:var(--mono);font-size:7px;color:var(--muted);text-transform:uppercase;letter-spacing:.08em;margin-bottom:.5rem}
.tc-desc{font-size:11px;color:rgba(255,255,255,.5);line-height:1.7}
.tc-stack{display:flex;gap:.3rem;flex-wrap:wrap;margin-top:.65rem}
.tsp{font-family:var(--mono);font-size:7px;background:rgba(255,255,255,.05);color:var(--soft);padding:2px 6px;border-radius:2px;text-transform:uppercase;letter-spacing:.05em}

/* MITRE */
.mitre-grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(108px,1fr));gap:.45rem;margin-top:.8rem}
.mc{background:var(--gb);border:1px solid var(--gbr);border-radius:3px;padding:.55rem .65rem;border-left:2px solid transparent;transition:all .2s;cursor:default}
.mc:hover{background:var(--gbh);border-left-color:var(--g);transform:translateY(-1px)}
.mc-ph{font-family:var(--mono);font-size:7px;color:var(--r);text-transform:uppercase;letter-spacing:.05em}
.mc-name{font-family:var(--mono);font-size:9px;color:var(--w);margin-top:2px;font-weight:700}
.mc-pct{font-family:var(--mono);font-size:8px;margin-top:3px}
.chart-box{background:var(--gb);border:1px solid var(--gbr);border-radius:5px;padding:1rem;margin-top:.9rem}

/* THREAT */
.threat-grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(200px,1fr));gap:.7rem;margin-top:.8rem}
.thcard{background:var(--gb);border:1px solid var(--gbr);border-radius:5px;padding:1rem;border-left:2px solid;transition:all .25s;cursor:default}
.thcard:hover{background:var(--gbh);transform:translateY(-2px)}
.thcard-head{display:flex;align-items:center;gap:.5rem;margin-bottom:.4rem}
.thcard-icon{font-size:16px}
.thcard-l{font-family:var(--mono);font-size:7px;text-transform:uppercase;letter-spacing:.1em}
.thcard-v{font-family:var(--head);font-size:1.2rem;letter-spacing:.04em}
.thcard-sub{font-size:10px;color:var(--muted);margin-top:.3rem;line-height:1.6}

/* KillChain */
.kc-step{display:flex;gap:.9rem;align-items:flex-start;margin-bottom:.65rem;opacity:0;transform:translateX(-8px);transition:all .4s}
.kc-step.vis{opacity:1;transform:none}
.kc-num{width:30px;height:30px;border:1px solid;border-radius:3px;display:flex;align-items:center;justify-content:center;font-family:var(--mono);font-size:11px;flex-shrink:0;font-weight:700}
.kc-title{font-family:var(--mono);font-size:10px;font-weight:700;margin-bottom:3px}
.kc-desc{font-size:10px;color:var(--muted);line-height:1.6}

/* PRESS */
.press-grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(260px,1fr));gap:.7rem;margin-top:.8rem}
.pcard{background:var(--gb);border:1px solid var(--gbr);border-radius:5px;padding:1.1rem;transition:all .25s;position:relative}
.pcard::after{content:'PRESS';position:absolute;top:.6rem;right:.7rem;font-family:var(--mono);font-size:6px;color:var(--a);border:1px solid rgba(255,204,0,.25);padding:1px 5px;border-radius:2px;letter-spacing:.1em}
.pcard:hover{background:var(--gbh);border-color:rgba(255,204,0,.2);transform:translateY(-2px)}
.pcard-pub{font-family:var(--mono);font-size:7px;color:var(--a);text-transform:uppercase;letter-spacing:.1em;margin-bottom:.35rem}
.pcard-q{font-size:11px;color:var(--soft);line-height:1.75;font-style:italic}
.pcard-date{font-family:var(--mono);font-size:7px;color:var(--muted);margin-top:.5rem}

/* CONNECT */
.conn-grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(200px,1fr));gap:.7rem;margin-top:.8rem}
.cc{display:flex;align-items:center;gap:.9rem;background:var(--gb);border:1px solid var(--gbr);border-radius:5px;padding:.8rem 1rem;text-decoration:none;color:var(--w);transition:all .25s}
.cc:hover{background:var(--gbh);border-color:rgba(57,255,20,.28);transform:translateY(-2px)}
.cc:active{transform:scale(.97)}
.cc-ico{width:36px;height:36px;border-radius:4px;display:flex;align-items:center;justify-content:center;flex-shrink:0;font-size:18px}
.cc-name{font-family:var(--mono);font-size:10px;font-weight:700;color:var(--w)}
.cc-sub{font-family:var(--mono);font-size:8px;color:var(--muted)}
.opencall{background:var(--gb);border:1px solid var(--gbr);border-left:2px solid var(--a);border-radius:5px;padding:1.1rem;margin-top:.9rem;transition:border-color .2s}
.opencall:hover{border-color:rgba(255,204,0,.35)}
.oc-l{font-family:var(--mono);font-size:7px;color:var(--a);text-transform:uppercase;letter-spacing:.12em;margin-bottom:.5rem;display:flex;align-items:center;gap:.4rem}
.oc-t{font-size:11px;color:var(--soft);line-height:1.85}
.callout{background:rgba(57,255,20,.04);border:1px solid rgba(57,255,20,.1);border-radius:4px;padding:.8rem 1rem;margin:1rem 0;font-size:11px;color:var(--soft);line-height:1.8}
.callout strong{color:var(--g)}

/* CHAR CARDS */
.char-grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(220px,1fr));gap:.7rem;margin-top:.8rem}
.char-card{background:var(--gb);border:1px solid var(--gbr);border-radius:5px;padding:1rem;transition:all .25s;cursor:default}
.char-card:hover{background:var(--gbh);transform:translateY(-2px)}
.char-head{display:flex;align-items:center;gap:.5rem;margin-bottom:.4rem}
.char-icon{font-size:18px}
.char-title{font-family:var(--mono);font-size:9px;color:var(--c);text-transform:uppercase;letter-spacing:.08em}
.char-text{font-size:11px;color:rgba(255,255,255,.5);line-height:1.7}

/* INCIDENT CARDS */
.inc-grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(220px,1fr));gap:.55rem;margin-top:.7rem}
.inc-card{background:var(--gb);border:1px solid var(--gbr);border-radius:4px;padding:.8rem;transition:all .22s;cursor:default;display:flex;align-items:flex-start;gap:.6rem}
.inc-card:hover{background:var(--gbh);transform:translateY(-1px)}
.inc-ico{font-size:16px;flex-shrink:0;margin-top:1px}
.inc-yr{font-family:var(--mono);font-size:7px;color:var(--r);text-transform:uppercase;letter-spacing:.08em}
.inc-title{font-family:var(--mono);font-size:9px;color:var(--w);font-weight:700;margin:.15rem 0}
.inc-desc{font-size:10px;color:var(--muted);line-height:1.55}

/* FOOTER */
.footer{position:relative;z-index:2;background:rgba(7,8,13,.95);border-top:1px solid var(--dim);padding:1.4rem 2rem;text-align:center;backdrop-filter:blur(8px)}
.footer-t{font-family:var(--mono);font-size:8px;color:var(--muted);letter-spacing:.1em;text-transform:uppercase;line-height:2.4}
</style>

<div class="orb orb1"></div>
<div class="orb orb2"></div>
<div class="orb orb3"></div>

<!-- ═══ HERO ═══════════════════════════════════════════════════════ -->
<div class="hero">
  <div class="hero-bg"></div>
  <div class="hero-scan"></div>
  <div class="hero-inner">
    <div class="av" title="b0n60">
      <div class="av-inner">
        <div class="av-penguin">🐧</div>
        <div class="av-handle">b0n60</div>
      </div>
      <div class="av-cursor"></div>
      <div class="av-tag">ZA</div>
    </div>
    <div>
      <div class="handle">b0n60</div>
      <div class="handle-sub">⚔️ SOC Analyst &nbsp;·&nbsp; 🌐 Full Stack Dev &nbsp;·&nbsp; 🏢 Jolinkomo Tech Solutions &nbsp;·&nbsp; 🇿🇦 Johannesburg, ZA</div>
      <div class="badges">
        <span class="badge b-g">🔐 Wazuh Certified</span>
        <span class="badge b-c">🛡️ Blue Team</span>
        <span class="badge b-r">🔴 ZA Threat Intel</span>
        <span class="badge b-a">📰 Media Cited</span>
        <span class="badge b-p">⚙️ Custom SIEM</span>
        <span class="badge b-g">🌐 Full Stack</span>
        <span class="badge b-c">🔍 Detection Eng</span>
      </div>
      <div class="hero-stats">
        <div class="hs"><div class="hs-n">5</div><div class="hs-l">⏱ Yrs Cyber</div></div>
        <div class="hs"><div class="hs-n">847</div><div class="hs-l">📋 Custom Rules</div></div>
        <div class="hs"><div class="hs-n">6</div><div class="hs-l">💻 Languages</div></div>
        <div class="hs"><div class="hs-n">R18B</div><div class="hs-l">🏛️ Gap Researched</div></div>
      </div>
    </div>
  </div>
</div>

<!-- ═══ DROPDOWN NAV ════════════════════════════════════════════════ -->
<div class="nav-wrap">
  <div class="nav-label">🗂️ Navigate Profile</div>
  <div class="dropdown" id="dd-wrap">
    <button class="dd-btn" id="dd-btn" onclick="toggleDD()">
      <span class="dd-btn-left">
        <span id="dd-current-icon">💻</span>
        <span id="dd-current-label">Terminal</span>
      </span>
      <span class="dd-chevron" id="dd-chev">▼</span>
    </button>
    <div class="dd-menu" id="dd-menu">
      <div class="dd-item active" data-tab="terminal" data-icon="💻" onclick="selectTab(this)"><span class="dd-item-icon">💻</span><span class="dd-item-label">Terminal</span><span class="dd-item-tag live">live</span></div>
      <div class="dd-item" data-tab="stack" data-icon="⚡" onclick="selectTab(this)"><span class="dd-item-icon">⚡</span><span class="dd-item-label">Tech Stack</span></div>
      <div class="dd-item" data-tab="tools" data-icon="🔧" onclick="selectTab(this)"><span class="dd-item-icon">🔧</span><span class="dd-item-label">Custom Tools</span><span class="dd-item-tag">open source</span></div>
      <div class="dd-item" data-tab="threat" data-icon="🌍" onclick="selectTab(this)"><span class="dd-item-icon">🌍</span><span class="dd-item-label">Threat Intel</span><span class="dd-item-tag" style="color:var(--r);border-color:rgba(255,45,85,.25)">active</span></div>
      <div class="dd-item" data-tab="mitre" data-icon="🎯" onclick="selectTab(this)"><span class="dd-item-icon">🎯</span><span class="dd-item-label">MITRE ATT&CK</span></div>
      <div class="dd-item" data-tab="press" data-icon="📰" onclick="selectTab(this)"><span class="dd-item-icon">📰</span><span class="dd-item-label">Press Citations</span></div>
      <div class="dd-item" data-tab="connect" data-icon="📡" onclick="selectTab(this)"><span class="dd-item-icon">📡</span><span class="dd-item-label">Connect</span></div>
    </div>
  </div>
</div>

<div style="position:relative;z-index:2;max-width:900px;margin:0 auto">

<!-- ═══ TERMINAL ════════════════════════════════════════════════════ -->
<div class="pnl on" id="pnl-terminal">
  <div class="sl"><span class="sl-icon">💻</span> Terminal <span style="font-size:8px;color:var(--r);border:1px solid rgba(255,45,85,.25);padding:1px 6px;border-radius:2px">live</span></div>
  <div class="term">
    <div class="tbar">
      <div class="tdot" style="background:#ff5f57" title="Close"></div>
      <div class="tdot" style="background:#febc2e" title="Minimise"></div>
      <div class="tdot" style="background:#28c840" title="Maximise"></div>
      <span class="tbar-title">🐧 b0n60@jolinkomo-soc:~</span>
      <span class="tbar-os">🐧 Ubuntu 25.04</span>
    </div>
    <div class="tbody" id="term-out"></div>
  </div>
  <div class="cmd-btns">
    <button class="cb cb-g" onclick="replayTerm()">🔄 Replay</button>
    <button class="cb cb-c" onclick="runCmd('whoami')">👤 whoami</button>
    <button class="cb cb-a" onclick="runCmd('cat mission.txt')">📜 mission.txt</button>
    <button class="cb cb-p" onclick="runCmd('cat certs.txt')">🏅 certs.txt</button>
    <button class="cb cb-r" onclick="runCmd('uname -a')">🖥️ uname -a</button>
    <button class="cb cb-g" onclick="runCmd('./coverage --mitre')">🎯 mitre coverage</button>
  </div>

  <div style="margin-top:1.5rem">
    <div class="sl"><span class="sl-icon">📊</span> System vitals</div>
    <div class="vitals-grid">
      <div class="vcard"><div class="vcard-l">🐧 OS</div><div class="vcard-v">Ubuntu 25.04 x86_64</div></div>
      <div class="vcard"><div class="vcard-l">🎨 Theme</div><div class="vcard-v">Juno-ocean-v40</div></div>
      <div class="vcard"><div class="vcard-l">🖼️ Icons</div><div class="vcard-v">Papirus-Dark</div></div>
      <div class="vcard"><div class="vcard-l">⌨️ Terminal</div><div class="vcard-v">gnome-terminal</div></div>
      <div class="vcard"><div class="vcard-l">⚙️ CPU Usage</div><div class="vcard-v" id="cpu-v" style="color:var(--a)">462%</div></div>
      <div class="vcard"><div class="vcard-l">💾 Disk (/)</div><div class="vcard-v" style="color:var(--a)">126G / 234G (57%)</div></div>
    </div>
    <div style="margin-top:.8rem">
      <div class="sl"><span class="sl-icon">🎨</span> Colour palette</div>
      <div class="palette">
        <div class="pc" style="background:#0c0d14" title="#0c0d14"></div>
        <div class="pc" style="background:#1a1b28" title="#1a1b28"></div>
        <div class="pc" style="background:#2a2b3d" title="#2a2b3d"></div>
        <div class="pc" style="background:#39ff14" title="Neon Green"></div>
        <div class="pc" style="background:#00e5ff" title="Cyber Cyan"></div>
        <div class="pc" style="background:#ff2d55" title="Alert Red"></div>
        <div class="pc" style="background:#ffcc00" title="Amber"></div>
        <div class="pc" style="background:#bf5fff" title="Purple"></div>
        <div class="pc" style="background:#ff6b35" title="Orange"></div>
        <div class="pc" style="background:#f0f0f0" title="White"></div>
        <div class="pc" style="background:#888" title="Muted"></div>
        <div class="pc" style="background:#333" title="Dark"></div>
      </div>
    </div>
  </div>
</div>

<!-- ═══ STACK ═══════════════════════════════════════════════════════ -->
<div class="pnl" id="pnl-stack">
  <div class="sl"><span class="sl-icon">🛡️</span> Blue Team + Detection</div>
  <div class="skill-row"><span class="sname">🔐 Wazuh XDR</span><div class="track"><div class="fill fg" data-w="95"></div></div><span class="spct">95</span></div>
  <div class="skill-row"><span class="sname">📋 Graylog</span><div class="track"><div class="fill fg" data-w="90"></div></div><span class="spct">90</span></div>
  <div class="skill-row"><span class="sname">📡 LibreNMS</span><div class="track"><div class="fill fg" data-w="88"></div></div><span class="spct">88</span></div>
  <div class="skill-row"><span class="sname">🔍 Threat Hunting</span><div class="track"><div class="fill fg" data-w="91"></div></div><span class="spct">91</span></div>
  <div class="skill-row"><span class="sname">🚨 Incident Response</span><div class="track"><div class="fill fg" data-w="88"></div></div><span class="spct">88</span></div>
  <div class="skill-row"><span class="sname">🎯 MITRE ATT&amp;CK</span><div class="track"><div class="fill fg" data-w="93"></div></div><span class="spct">93</span></div>
  <div class="sl" style="margin-top:1.4rem"><span class="sl-icon">💻</span> Programming</div>
  <div class="skill-row"><span class="sname">🐍 Python</span><div class="track"><div class="fill fc" data-w="93"></div></div><span class="spct">93</span></div>
  <div class="skill-row"><span class="sname">⚡ JavaScript</span><div class="track"><div class="fill fc" data-w="88"></div></div><span class="spct">88</span></div>
  <div class="skill-row"><span class="sname">🌐 HTML / CSS</span><div class="track"><div class="fill fc" data-w="95"></div></div><span class="spct">95</span></div>
  <div class="skill-row"><span class="sname">🦀 Rust</span><div class="track"><div class="fill fp" data-w="72"></div></div><span class="spct">72</span></div>
  <div class="skill-row"><span class="sname">⚙️ C</span><div class="track"><div class="fill fp" data-w="76"></div></div><span class="spct">76</span></div>
  <div class="sl" style="margin-top:1.4rem"><span class="sl-icon">🏗️</span> Infrastructure</div>
  <div class="skill-row"><span class="sname">🔒 Network Hardening</span><div class="track"><div class="fill fa" data-w="91"></div></div><span class="spct">91</span></div>
  <div class="skill-row"><span class="sname">🏛️ Zero Trust Arch</span><div class="track"><div class="fill fa" data-w="86"></div></div><span class="spct">86</span></div>
  <div class="skill-row"><span class="sname">🐳 Docker</span><div class="track"><div class="fill fa" data-w="83"></div></div><span class="spct">83</span></div>
  <div class="sl" style="margin-top:1.4rem"><span class="sl-icon">🧰</span> Tool palette</div>
  <div style="display:flex;flex-wrap:wrap;gap:.35rem;margin-top:.5rem">
    <span class="badge b-g">🔐 Wazuh</span><span class="badge b-g">📋 Graylog</span><span class="badge b-g">📡 LibreNMS</span><span class="badge b-g">🛡️ Suricata</span>
    <span class="badge b-c">🦓 Zeek</span><span class="badge b-c">🔭 Wireshark</span><span class="badge b-c">🗺️ Nmap</span><span class="badge b-c">🐳 Docker</span>
    <span class="badge b-r">💀 Metasploit</span><span class="badge b-r">🕷️ Burp Suite</span><span class="badge b-r">🧬 MISP</span>
    <span class="badge b-a">🌿 Nginx</span><span class="badge b-a">🐘 PostgreSQL</span><span class="badge b-a">🐙 Git</span>
    <span class="badge b-p">🤖 Ollama</span><span class="badge b-p">🧠 Claude Code</span><span class="badge b-p">🟢 Node.js</span>
  </div>
</div>

<!-- ═══ CUSTOM TOOLS ════════════════════════════════════════════════ -->
<div class="pnl" id="pnl-tools">
  <div class="sl"><span class="sl-icon">🔧</span> Custom-Built Tooling <span style="font-size:7px;color:var(--g);border:1px solid rgba(57,255,20,.25);padding:1px 6px;border-radius:2px;margin-left:.3rem">open source</span></div>
  <div class="callout">🇿🇦 Built for environments where commercial platforms fail. South African infrastructure has unique constraints — load-shedding, bandwidth limits, legacy systems — that generic tooling consistently misses. <strong>Take, fork, extend.</strong></div>
  <div class="tool-grid">
    <div class="tc-card"><div class="tc-head"><span class="tc-icon">🛡️</span><span class="tc-name">SentinelCore</span></div><div class="tc-rep">Wazuh replacement</div><div class="tc-desc">Lightweight SIEM engine for low-resource ZA environments. Custom rule engine with local threat intel feeds calibrated to South African attack patterns and ISP infrastructure.</div><div class="tc-stack"><span class="tsp">🐍 Python</span><span class="tsp">🦀 Rust</span><span class="tsp">🗃️ SQLite</span></div></div>
    <div class="tc-card"><div class="tc-head"><span class="tc-icon">📋</span><span class="tc-name">LogHound</span></div><div class="tc-rep">Graylog replacement</div><div class="tc-desc">High-noise, low-bandwidth log aggregator with built-in parsers for South African ISP and portal log formats. Designed for constrained networks with poor connectivity.</div><div class="tc-stack"><span class="tsp">🐍 Python</span><span class="tsp">🔴 Redis</span><span class="tsp">⚡ FastAPI</span></div></div>
    <div class="tc-card"><div class="tc-head"><span class="tc-icon">📡</span><span class="tc-name">NetPulse</span></div><div class="tc-rep">LibreNMS replacement</div><div class="tc-desc">Modular NMS with non-standard topology support. WhatsApp and SMS alerting for teams without 24/7 NOC coverage — a real South African operational constraint.</div><div class="tc-stack"><span class="tsp">🐍 Python</span><span class="tsp">⚙️ C</span><span class="tsp">📶 SNMP</span></div></div>
    <div class="tc-card"><div class="tc-head"><span class="tc-icon">🗺️</span><span class="tc-name">ThreatMapper</span></div><div class="tc-rep">IOC aggregation engine</div><div class="tc-desc">Pulls from MISP, AlienVault OTX, and curated local feeds. Enriches Wazuh alerts with South Africa-specific IOC context and government infrastructure indicators.</div><div class="tc-stack"><span class="tsp">🐍 Python</span><span class="tsp">🧬 MISP</span><span class="tsp">🔭 OTX</span></div></div>
  </div>
</div>

<!-- ═══ THREAT INTEL ════════════════════════════════════════════════ -->
<div class="pnl" id="pnl-threat">
  <div class="sl"><span class="sl-icon">🌍</span> South African Threat Landscape</div>
  <div class="threat-grid">
    <div class="thcard" style="border-left-color:var(--r)"><div class="thcard-head"><span class="thcard-icon">🚨</span><div><div class="thcard-l" style="color:var(--r)">Active Breach</div><div class="thcard-v" style="color:var(--r)">Gauteng Gov</div></div></div><div class="thcard-sub">3.67M files · 3.8TB · $25,000 dark web listing — healthcare, education, housing data exposed</div></div>
    <div class="thcard" style="border-left-color:var(--a)"><div class="thcard-head"><span class="thcard-icon">💰</span><div><div class="thcard-l" style="color:var(--a)">Spending Gap</div><div class="thcard-v" style="color:var(--a)">R18 Billion</div></div></div><div class="thcard-sub">Researched and cited shortfall in government spending on securing national key points — Sunday Times, 2022</div></div>
    <div class="thcard" style="border-left-color:var(--c)"><div class="thcard-head"><span class="thcard-icon">🕳️</span><div><div class="thcard-l" style="color:var(--c)">Primary Vector</div><div class="thcard-v" style="color:var(--c)">Web Exploit</div></div></div><div class="thcard-sub">SQLi · Credential stuffing · Outdated tech stacks across government portals and state departments</div></div>
    <div class="thcard" style="border-left-color:var(--p)"><div class="thcard-head"><span class="thcard-icon">🗺️</span><div><div class="thcard-l" style="color:var(--p)">Exposure Surface</div><div class="thcard-v" style="color:var(--p)">National</div></div></div><div class="thcard-sub">Any unpatched province, metro, or municipality. SA infrastructure is mappable by anyone with intent.</div></div>
  </div>
  <div class="sl" style="margin-top:1.5rem"><span class="sl-icon">🔗</span> Breach Kill Chain — MITRE ATT&amp;CK</div>
  <div id="kc-container" style="margin-top:.7rem"></div>
  <div class="sl" style="margin-top:1.5rem"><span class="sl-icon">📌</span> Notable SA Incidents</div>
  <div class="inc-grid">
    <div class="inc-card"><span class="inc-ico">🚢</span><div><div class="inc-yr">Jul 2021</div><div class="inc-title">Transnet</div><div class="inc-desc">Ransomware took down port systems, causing major shipping delays at all national entry points.</div></div></div>
    <div class="inc-card"><span class="inc-ico">⚖️</span><div><div class="inc-yr">Sep 2021</div><div class="inc-title">Dept of Justice</div><div class="inc-desc">Ransomware locked all systems. Courts, prosecutors, and administration paralysed.</div></div></div>
    <div class="inc-card"><span class="inc-ico">👤</span><div><div class="inc-yr">2022</div><div class="inc-title">President Ramaphosa</div><div class="inc-desc">Personal data accessed via TransUnion chain breach. ID, address, and contact details exposed.</div></div></div>
    <div class="inc-card"><span class="inc-ico">🏛️</span><div><div class="inc-yr">2022</div><div class="inc-title">Defence / SSA</div><div class="inc-desc">SpiderLog$ accessed military and state security webmail interfaces — verified by Umboko Sec.</div></div></div>
    <div class="inc-card"><span class="inc-ico">🏢</span><div><div class="inc-yr">2024</div><div class="inc-title">CIPC</div><div class="inc-desc">Hackers had full DB access since 2021. Plain text passwords, credit cards, director manipulation possible.</div></div></div>
    <div class="inc-card"><span class="inc-ico">🏛️</span><div><div class="inc-yr">Mar 2025</div><div class="inc-title">SA Parliament</div><div class="inc-desc">Social media hijacked to push $Ramaphosa crypto token. Coordinated cross-platform breach.</div></div></div>
  </div>
</div>

<!-- ═══ MITRE ════════════════════════════════════════════════════════ -->
<div class="pnl" id="pnl-mitre">
  <div class="sl"><span class="sl-icon">🎯</span> ATT&amp;CK Coverage Matrix</div>
  <div style="font-family:var(--mono);font-size:9px;color:var(--muted);margin-bottom:.8rem">847 custom Wazuh rules · 124 Graylog pipelines · 63 LibreNMS thresholds. Hover each cell.</div>
  <div class="mitre-grid" id="mitre-grid"></div>
  <div class="chart-box" style="margin-top:1rem">
    <div style="font-family:var(--mono);font-size:8px;color:var(--g);text-transform:uppercase;letter-spacing:.14em;margin-bottom:.7rem;display:flex;align-items:center;gap:.4rem">📊 Coverage distribution</div>
    <canvas id="mitre-chart" height="170"></canvas>
  </div>
</div>

<!-- ═══ PRESS ════════════════════════════════════════════════════════ -->
<div class="pnl" id="pnl-press">
  <div class="sl"><span class="sl-icon">📰</span> Media &amp; Press Citations</div>
  <div class="callout">
    📋 Research conducted under <strong>Umboko Sec</strong> was independently verified by national media and cited in two major investigative pieces covering South Africa's cybersecurity crisis. Findings exposed a structural underfunding gap of at least <strong>R18 billion</strong> in government cybersecurity spending.
  </div>
  <div class="press-grid">
    <div class="pcard"><div class="pcard-pub">📰 Sunday Times — May 2022</div><div class="pcard-q">"Umboko Sec director Bongo Sijora told Sunday Times their research showed a shortfall of at least R18 billion in government spending on securing national key points and departments from cyber threats."</div><div class="pcard-date">Lax Cybersecurity Leaves SA a Playground for Hackers · TimesLive</div></div>
    <div class="pcard"><div class="pcard-pub">💻 MyBroadband — May 2022</div><div class="pcard-q">"The paper verified the group's claims with cybersecurity firms WolfPack Information Risk and Umboko Sec." — Independent verification of SpiderLog$'s access to military and intelligence infrastructure.</div><div class="pcard-date">Cyril Ramaphosa's Private Data Hacked · MyBroadband</div></div>
    <div class="pcard"><div class="pcard-pub">🕸️ Context — SpiderLog$</div><div class="pcard-q">"South Africa is a playground for hackers because anyone is able to map your country's digital infrastructure." — Verified by Umboko Sec: DoD, SSA, and state security webmail interfaces accessed.</div><div class="pcard-date">Defence + State Security Exposure · 2022</div></div>
  </div>
  <div class="sl" style="margin-top:1.5rem"><span class="sl-icon">🧬</span> Character &amp; Ethos</div>
  <div class="char-grid">
    <div class="char-card"><div class="char-head"><span class="char-icon">🧠</span><span class="char-title">Intellectual Range</span></div><div class="char-text">Draws connections between cybersecurity, genetics, philosophy, and political systems. Security as a discipline with human, societal, and structural dimensions — not just a technical exercise.</div></div>
    <div class="char-card"><div class="char-head"><span class="char-icon">🔨</span><span class="char-title">Builder Mentality</span></div><div class="char-text">Most repositories are intentional open builds — prototypes left accessible for others to extend. Knowledge transfer matters more than attribution. If it solves your problem, take it.</div></div>
    <div class="char-card"><div class="char-head"><span class="char-icon">🎯</span><span class="char-title">Precise Under Pressure</span></div><div class="char-text">Cited by national media during a live government breach crisis. Delivers structured, evidence-based analysis in environments where others speculate. Calm is the strategy.</div></div>
    <div class="char-card"><div class="char-head"><span class="char-icon">🌍</span><span class="char-title">Mission-Driven</span></div><div class="char-text">Focused on making the digital infrastructure that ordinary South Africans depend on — healthcare portals, housing systems, government services — genuinely secure against real threats.</div></div>
  </div>
</div>

<!-- ═══ CONNECT ══════════════════════════════════════════════════════ -->
<div class="pnl" id="pnl-connect">
  <div class="sl"><span class="sl-icon">📡</span> Get in Touch</div>
  <div class="conn-grid">
    <a class="cc" href="https://www.linkedin.com/in/bongo-sijora/" target="_blank">
      <div class="cc-ico" style="background:rgba(10,102,194,.2)">💼</div>
      <div><div class="cc-name">LinkedIn</div><div class="cc-sub">bongo-sijora</div></div>
    </a>
    <a class="cc" href="https://github.com/b0n60" target="_blank">
      <div class="cc-ico" style="background:rgba(255,255,255,.07)">🐙</div>
      <div><div class="cc-name">GitHub</div><div class="cc-sub">b0n60</div></div>
    </a>
  </div>
  <div class="opencall">
    <div class="oc-l">🤝 Collaboration open for</div>
    <div class="oc-t">🛡️ Blue team tooling &nbsp;·&nbsp; 🔍 Detection engineering &nbsp;·&nbsp; 🇿🇦 SA threat intelligence &nbsp;·&nbsp; 🌐 Full-stack secure app development &nbsp;·&nbsp; 📰 Cybersecurity research and press engagement.</div>
  </div>
  <div style="margin-top:.9rem">
    <div class="sl"><span class="sl-icon">⚡</span> Philosophy</div>
    <div class="callout">Five years building defences for infrastructure that millions of South Africans depend on — healthcare portals, government services, financial systems. The work is precise because the consequences of imprecision are real. The code is open because the knowledge transfer matters more than the credit. <strong>The mission is clear because the threat is not theoretical.</strong></div>
  </div>
</div>

</div><!-- /content wrapper -->

<div class="footer">
  <div class="footer-t">
    <span style="color:var(--g)">// b0n60</span> &nbsp;·&nbsp; 🐧 SOC Analyst &nbsp;·&nbsp; 🌐 Full Stack Dev &nbsp;·&nbsp; 🏢 Jolinkomo Tech Solutions &nbsp;·&nbsp; 🇿🇦 Johannesburg, ZA<br>
    🔒 Securing the infrastructure that millions depend on<br>
    <span style="color:rgba(255,255,255,.15)">Built with precision. Hardened by experience. Open by principle.</span>
  </div>
</div>

<script src="https://cdn.jsdelivr.net/npm/chart.js@4.4.0/dist/chart.umd.min.js"></script>
<script>
var built={};

function toggleDD(){
  var m=document.getElementById('dd-menu');
  var b=document.getElementById('dd-btn');
  var c=document.getElementById('dd-chev');
  var open=m.classList.contains('open');
  m.classList.toggle('open',!open);
  b.classList.toggle('open',!open);
  c.classList.toggle('open',!open);
}

document.addEventListener('click',function(e){
  var wrap=document.getElementById('dd-wrap');
  if(!wrap.contains(e.target)){
    document.getElementById('dd-menu').classList.remove('open');
    document.getElementById('dd-btn').classList.remove('open');
    document.getElementById('dd-chev').classList.remove('open');
  }
});

function selectTab(item){
  var id=item.getAttribute('data-tab');
  var icon=item.getAttribute('data-icon');
  var label=item.querySelector('.dd-item-label').textContent;
  document.querySelectorAll('.dd-item').forEach(function(i){i.classList.remove('active')});
  item.classList.add('active');
  document.getElementById('dd-current-icon').textContent=icon;
  document.getElementById('dd-current-label').textContent=label;
  document.getElementById('dd-menu').classList.remove('open');
  document.getElementById('dd-btn').classList.remove('open');
  document.getElementById('dd-chev').classList.remove('open');
  document.querySelectorAll('.pnl').forEach(function(p){p.classList.remove('on')});
  document.getElementById('pnl-'+id).classList.add('on');
  if(id==='stack'&&!built.stack){built.stack=true;setTimeout(animateBars,100)}
  if(id==='mitre'&&!built.mitre){built.mitre=true;setTimeout(buildMitre,100)}
  if(id==='threat'&&!built.threat){built.threat=true;setTimeout(buildKC,100)}
}

function animateBars(){
  document.querySelectorAll('.fill').forEach(function(f){
    f.style.width=f.getAttribute('data-w')+'%';
  });
}

/* ── TERMINAL ─────────────────────────────────── */
/* Realistic Ubuntu Tux ASCII with colour blocks */
var tuxLines=[
  '         <span style="color:#000;background:#f8f8f2">&#x2588;</span><span style="color:#000;background:#f8f8f2">&#x2588;</span><span style="color:#000;background:#f8f8f2">&#x2588;</span><span style="color:#000;background:#f8f8f2">&#x2588;</span><span style="color:#000;background:#f8f8f2">&#x2588;</span>         <span class="ti">OS:</span> <span class="tw">Ubuntu 25.04 x86_64</span>',
  '       <span style="color:#000;background:#f8f8f2">&#x2588;&#x2588;</span><span style="background:#f8f8f2;color:#f8f8f2">&#x2588;</span><span style="color:#ff2d55;background:#ff2d55">&#x2588;</span><span style="background:#f8f8f2;color:#f8f8f2">&#x2588;</span><span style="color:#ff2d55;background:#ff2d55">&#x2588;</span><span style="background:#f8f8f2;color:#f8f8f2">&#x2588;</span><span style="color:#000;background:#f8f8f2">&#x2588;&#x2588;</span>       <span class="ti">Theme:</span> <span class="tw">Juno-ocean-v40 [GTK2/3]</span>',
  '      <span style="color:#000;background:#f8f8f2">&#x2588;&#x2588;&#x2588;</span><span style="color:#ffcc00;background:#ffcc00">&#x2588;&#x2588;&#x2588;</span><span style="color:#000;background:#f8f8f2">&#x2588;&#x2588;&#x2588;</span>      <span class="ti">Icons:</span> <span class="tw">Papirus-Dark [GTK2/3]</span>',
  '     <span style="color:#000;background:#f8f8f2">&#x2588;</span><span style="background:#f8f8f2;color:#f8f8f2">&#x2588;&#x2588;</span><span style="color:#ffcc00;background:#ffcc00">&#x2588;&#x2588;&#x2588;&#x2588;&#x2588;</span><span style="background:#f8f8f2;color:#f8f8f2">&#x2588;&#x2588;</span><span style="color:#000;background:#f8f8f2">&#x2588;</span>     <span class="ti">Terminal:</span> <span class="tw">gnome-terminal</span>',
  '    <span style="color:#000;background:#1a1b28">&#x2588;&#x2588;&#x2588;</span><span style="color:#ffcc00;background:#ffcc00">&#x2588;&#x2588;&#x2588;&#x2588;&#x2588;&#x2588;&#x2588;</span><span style="color:#000;background:#1a1b28">&#x2588;&#x2588;&#x2588;</span>    <span class="ti">CPU Usage:</span> <span class="tg">462%</span>',
  '   <span style="color:#000;background:#1a1b28">&#x2588;&#x2588;&#x2588;&#x2588;&#x2588;</span><span style="color:#fff;background:#1a1b28">&#x2588;</span><span style="color:#ffcc00;background:#ffcc00">&#x2588;&#x2588;&#x2588;&#x2588;&#x2588;</span><span style="color:#fff;background:#1a1b28">&#x2588;</span><span style="color:#000;background:#1a1b28">&#x2588;&#x2588;&#x2588;&#x2588;&#x2588;</span>   <span class="ti">Disk (/):</span> <span class="tw">126G / 234G (57%)</span>',
  '  <span style="color:#1a1b28;background:#1a1b28">&#x2588;&#x2588;&#x2588;&#x2588;&#x2588;&#x2588;&#x2588;&#x2588;&#x2588;&#x2588;&#x2588;&#x2588;&#x2588;&#x2588;&#x2588;</span>',
  ' <span style="color:#1a1b28;background:#1a1b28">&#x2588;&#x2588;&#x2588;&#x2588;&#x2588;&#x2588;&#x2588;&#x2588;&#x2588;&#x2588;&#x2588;&#x2588;&#x2588;&#x2588;&#x2588;&#x2588;&#x2588;</span>',
];

var termSeq=[
  {t:'p',cmd:'neofetch'},
  {t:'art'},
  {t:'p',cmd:'whoami --verbose'},
  {t:'o',c:'tg',v:'Name       \u2192 b0n60'},
  {t:'o',c:'tg',v:'Role       \u2192 SOC Analyst + Full Stack Dev'},
  {t:'o',c:'ti',v:'Company    \u2192 Jolinkomo Tech Solutions'},
  {t:'o',c:'ti',v:'Location   \u2192 Johannesburg, Gauteng, ZA'},
  {t:'o',c:'tc',v:'Cert       \u2192 Wazuh Certified Engineer [OFFICIAL]'},
  {t:'o',c:'tv',v:'Focus      \u2192 Blue Team \xb7 Detection Eng \xb7 Custom SIEM'},
  {t:'o',c:'tw',v:'Press      \u2192 Sunday Times \xb7 MyBroadband \xb7 2022'},
  {t:'p',cmd:'cat mission.txt'},
  {t:'o',c:'tw',v:'South Africa is not a peripheral target.'},
  {t:'o',c:'tw',v:'It is a primary one. 5 years. 847 rules. Still going.'},
  {t:'o',c:'td',v:'R18bn gap. Documented. Published. Verified.'},
  {t:'p',cmd:'cat certs.txt'},
  {t:'o',c:'tc',v:'[VERIFIED]  Wazuh Certified Engineer (Official)'},
  {t:'o',c:'tc',v:'[ACTIVE]    Blue Team Ops \xb7 5 Years Production'},
  {t:'o',c:'tv',v:'[CITED]     Sunday Times \xb7 MyBroadband \xb7 Umboko Sec'},
  {t:'p',cmd:'uname -a'},
  {t:'o',c:'ti',v:'Linux jolinkomo-soc 6.11.0-25-generic #25-Ubuntu SMP'},
  {t:'o',c:'ti',v:'x86_64 GNU/Linux'},
  {t:'p',cmd:'./coverage --mitre --env za-gov'},
  {t:'o',c:'tc',v:'[LOADED] wazuh-rules-za.xml     \u2192 847 rules'},
  {t:'o',c:'tc',v:'[LOADED] graylog-pipelines.json \u2192 124 pipelines'},
  {t:'o',c:'tc',v:'[LOADED] librenms-alerts.conf   \u2192 63 thresholds'},
  {t:'b',l:'Initial Access   ',p:94,c:'tc'},
  {t:'b',l:'Exfiltration     ',p:91,c:'tc'},
  {t:'b',l:'Persistence      ',p:88,c:'tg'},
  {t:'b',l:'Defence Evasion  ',p:79,c:'tp'},
  {t:'p',cmd:'_',cur:true}
];

var cmdMap={
  'whoami':[
    {c:'tg',v:'Name       \u2192 b0n60'},
    {c:'tg',v:'Role       \u2192 SOC Analyst + Full Stack Dev'},
    {c:'ti',v:'Company    \u2192 Jolinkomo Tech Solutions'},
    {c:'ti',v:'Location   \u2192 Johannesburg, Gauteng, ZA'},
    {c:'tc',v:'Cert       \u2192 Wazuh Certified Engineer [OFFICIAL]'},
    {c:'tv',v:'Press      \u2192 Sunday Times \xb7 MyBroadband \xb7 2022'},
  ],
  'cat mission.txt':[
    {c:'tw',v:'South Africa is not a peripheral target \u2014 it is a primary one.'},
    {c:'tw',v:'Five years of real incidents on real infrastructure.'},
    {c:'td',v:'847 rules. 124 pipelines. R18bn gap documented and verified.'},
  ],
  'cat certs.txt':[
    {c:'tc',v:'[VERIFIED]  Wazuh Certified Engineer (Official)'},
    {c:'tg',v:'[ACTIVE]    Blue Team Ops \xb7 5 Years Production'},
    {c:'tv',v:'[CITED]     Sunday Times \xb7 MyBroadband \xb7 Umboko Sec'},
  ],
  'uname -a':[
    {c:'ti',v:'Linux jolinkomo-soc 6.11.0-25-generic #25-Ubuntu SMP'},
    {c:'ti',v:'x86_64 GNU/Linux'},
  ],
  './coverage --mitre':[
    {c:'tc',v:'[LOADED] wazuh-rules-za.xml     \u2192 847 rules'},
    {c:'tc',v:'[LOADED] graylog-pipelines.json \u2192 124 pipelines'},
    {c:'tc',v:'[LOADED] librenms-alerts.conf   \u2192 63 thresholds'},
    {c:'tg',v:'Initial Access   \u2588\u2588\u2588\u2588\u2588\u2588\u2588\u2588\u2588\u2588\u2588\u2588 94%'},
    {c:'tg',v:'Exfiltration     \u2588\u2588\u2588\u2588\u2588\u2588\u2588\u2588\u2588\u2588\u2588\u2588 91%'},
    {c:'tg',v:'Persistence      \u2588\u2588\u2588\u2588\u2588\u2588\u2588\u2588\u2588\u2588\u2591\u2591 88%'},
    {c:'tp',v:'Defence Evasion  \u2588\u2588\u2588\u2588\u2588\u2588\u2588\u2588\u2588\u2591\u2591\u2591 79% \u2190 active dev'},
  ]
};

var tb=document.getElementById('term-out');

function addLine(html){
  var d=document.createElement('div');
  d.className='tline';
  d.innerHTML=html;
  tb.appendChild(d);
  tb.scrollTop=tb.scrollHeight;
}

function typeCmd(cmd,done){
  var row=document.createElement('div');
  row.className='tline';
  row.innerHTML='<span class="tc">b0n60@jolinkomo</span><span class="td">:</span><span class="ti">~</span><span class="td">$</span> <span id="tgt_'+Date.now()+'"></span><span class="cursor"></span>';
  tb.appendChild(row);tb.scrollTop=tb.scrollHeight;
  var spans=row.querySelectorAll('span');
  var tgt=spans[spans.length-2];
  var cur=spans[spans.length-1];
  var i=0;
  function tick(){
    if(i<cmd.length){tgt.textContent+=cmd[i++];tb.scrollTop=tb.scrollHeight;setTimeout(tick,36+Math.random()*22);}
    else{if(cur)cur.style.display='none';setTimeout(done,150);}
  }
  tick();
}

function playSeq(seq,i){
  if(i>=seq.length)return;
  var s=seq[i];
  if(s.t==='p'){
    if(s.cur){addLine('<span class="tc">b0n60@jolinkomo</span><span class="td">:</span><span class="ti">~</span><span class="td">$</span> <span class="cursor"></span>');}
    else{typeCmd(s.cmd,function(){playSeq(seq,i+1);});}
    return;
  }
  if(s.t==='art'){
    tuxLines.forEach(function(l){addLine('<span style="font-size:11px;line-height:1.7">'+l+'</span>');});
    setTimeout(function(){playSeq(seq,i+1);},80);return;
  }
  if(s.t==='o'){addLine('<span class="'+s.c+'">'+s.v+'</span>');setTimeout(function(){playSeq(seq,i+1);},46);return;}
  if(s.t==='b'){
    var f=Math.round(s.p/5),e=20-f;
    addLine('<span class="td">'+s.l+'</span><span class="'+s.c+'">'+'█'.repeat(f)+'</span><span class="td">'+'░'.repeat(e)+'</span><span class="tg"> '+s.p+'%</span>');
    setTimeout(function(){playSeq(seq,i+1);},62);return;
  }
}

function replayTerm(){tb.innerHTML='';playSeq(termSeq,0);}

function runCmd(cmd){
  var out=cmdMap[cmd];if(!out)return;
  typeCmd(cmd,function(){
    out.forEach(function(o,idx){
      setTimeout(function(){addLine('<span class="'+o.c+'">'+o.v+'</span>');},idx*52);
    });
    setTimeout(function(){
      addLine('<span class="tc">b0n60@jolinkomo</span><span class="td">:</span><span class="ti">~</span><span class="td">$</span> <span class="cursor"></span>');
    },out.length*52+90);
  });
}

setInterval(function(){
  var v=document.getElementById('cpu-v');
  if(v)v.textContent=Math.round(380+Math.random()*160)+'%';
},2000);

/* MITRE */
var mitreData=[
  {ph:'TA0043',n:'Reconnaissance',p:94},{ph:'TA0001',n:'Initial Access',p:94},
  {ph:'TA0002',n:'Execution',p:88},{ph:'TA0003',n:'Persistence',p:88},
  {ph:'TA0004',n:'Priv Escalation',p:82},{ph:'TA0005',n:'Def Evasion',p:79},
  {ph:'TA0006',n:'Cred Access',p:91},{ph:'TA0007',n:'Discovery',p:90},
  {ph:'TA0008',n:'Lateral Mov',p:83},{ph:'TA0009',n:'Collection',p:90},
  {ph:'TA0010',n:'Exfiltration',p:91},{ph:'TA0011',n:'C2',p:84},
  {ph:'TA0040',n:'Impact',p:92},{ph:'TA0042',n:'Resource Dev',p:87}
];

function buildMitre(){
  var g=document.getElementById('mitre-grid');
  mitreData.forEach(function(m){
    var col=m.p>=90?'var(--g)':m.p>=85?'var(--c)':m.p>=80?'var(--a)':'var(--r)';
    var d=document.createElement('div');d.className='mc';
    d.innerHTML='<div class="mc-ph">'+m.ph+'</div><div class="mc-name">'+m.n+'</div><div class="mc-pct" style="color:'+col+'">'+m.p+'%</div>';
    g.appendChild(d);
  });
  setTimeout(function(){
    var ctx=document.getElementById('mitre-chart').getContext('2d');
    new Chart(ctx,{
      type:'bar',
      data:{labels:mitreData.map(function(m){return m.n;}),datasets:[{data:mitreData.map(function(m){return m.p;}),backgroundColor:mitreData.map(function(m){return m.p>=90?'#39ff14':m.p>=85?'#00e5ff':m.p>=80?'#ffcc00':'#ff2d55';}),borderWidth:0,borderRadius:3}]},
      options:{responsive:true,maintainAspectRatio:false,plugins:{legend:{display:false},tooltip:{callbacks:{label:function(c){return c.raw+'% coverage';}}}},scales:{x:{ticks:{color:'rgba(255,255,255,.3)',font:{size:8,family:"'JetBrains Mono',monospace"}},grid:{color:'rgba(255,255,255,.04)'},border:{color:'transparent'}},y:{ticks:{color:'rgba(255,255,255,.3)',font:{size:8}},grid:{color:'rgba(255,255,255,.04)'},border:{color:'transparent'},min:0,max:100}},animation:{duration:1400,easing:'easeOutCubic'}}
    });
  },200);
}

var kcData=[
  {n:'Reconnaissance',d:'Mapped gauteng.gov.za — outdated software, exposed login pages, misconfigured servers. Passive recon runs for weeks undetected.',c:'var(--c)'},
  {n:'Initial Access',d:'Exploited web application vulnerability — SQLi or credential reuse from a prior breach. Standard ZA government portal attack surface.',c:'var(--a)'},
  {n:'Persistence',d:'Planted backdoors across interconnected government systems. Even if the entry is patched, they stay in.',c:'var(--p)'},
  {n:'Lateral Movement',d:'Moved from web portal to internal database servers. Escalated privileges across departments using harvested credentials.',c:'var(--r)'},
  {n:'Exfiltration',d:'Extracted 3.8TB in staged chunks over time — small enough data flows to avoid triggering volume-based alarms. Zero detection.',c:'var(--r)'}
];

function buildKC(){
  var c=document.getElementById('kc-container');
  kcData.forEach(function(k,i){
    var d=document.createElement('div');d.className='kc-step';
    d.innerHTML='<div class="kc-num" style="border-color:'+k.c+';color:'+k.c+'">'+(i+1)+'</div><div><div class="kc-title" style="color:'+k.c+'">'+k.n+'</div><div class="kc-desc">'+k.d+'</div></div>';
    c.appendChild(d);
    setTimeout(function(){d.classList.add('vis');},i*180+80);
  });
}

setTimeout(function(){playSeq(termSeq,0);},400);
</script>
