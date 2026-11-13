<!doctype html><html><head><meta charset=utf8><meta name=viewport content="width=device-width,initial-scale=1,viewport-fit=cover"><style>:root{color-scheme:light;box-sizing:border-box;padding-top:env(safe-area-inset-top,0px);padding-bottom:env(safe-area-inset-bottom,0px)}html{scroll-padding-top:env(safe-area-inset-top,0px)}body{margin:0;padding:0;font:14px -apple-system,BlinkMacSystemFont,sans-serif;background:#fff;color:#000}img{max-width:100%}[hidden]:not([hidden=until-found i]){display:none!important}</style></head><body>
<title>Bureau Padelistes</title>
<meta name="claude:viewport-fit-sides" content="cover">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Anton&family=Montserrat:wght@500;600;700;800&family=JetBrains+Mono:wght@500&display=swap">
<script src="https://cdnjs.cloudflare.com/ajax/libs/qrcode-generator/1.4.4/qrcode.min.js"></script>
<script src="https://cdn.jsdelivr.net/npm/jsqr@1.4.0/dist/jsQR.min.js"></script>
<style>
/* Espace bureau : bandeau « filet », atelier (formulaire + carte qui se retourne), registre des membres */
:root{
  --navy:#0b1a4a; --court:#2f5bd3; --lime:#d9ec4f;
  --bg:#eef3fc; --surface:#ffffff; --fg:#12245e; --muted:#56668c; --border:#d3dcef; --field:#f5f8fe;
  --ok:#1f8a55; --warn:#a86a12; --bad:#c0392b;
  --display:"Anton",Impact,"Arial Narrow",sans-serif;
  --body:"Montserrat",system-ui,-apple-system,sans-serif;
  --mono:"JetBrains Mono",ui-monospace,Menlo,monospace;
}
@media (prefers-color-scheme:dark){:root:not([data-theme="light"]){
  --bg:#070f2b;--surface:#0f1b45;--fg:#e8eefc;--muted:#9fb0d8;--border:#22336b;--field:#0a1538;
  --ok:#5fd39a;--warn:#e8b55a;--bad:#ff8a7a;color-scheme:dark}}
:root[data-theme="dark"]{--bg:#070f2b;--surface:#0f1b45;--fg:#e8eefc;--muted:#9fb0d8;--border:#22336b;--field:#0a1538;
  --ok:#5fd39a;--warn:#e8b55a;--bad:#ff8a7a;color-scheme:dark}
*{box-sizing:border-box}
[hidden]{display:none!important}
body{background:var(--bg);color:var(--fg);font:15px/1.5 var(--body)}
body::before{content:"";position:fixed;inset:0 0 auto;height:env(safe-area-inset-top,0px);z-index:10;background:var(--navy)}
.wrap{max-width:1100px;margin:0 auto;padding-left:max(16px,env(safe-area-inset-left,0px));padding-right:max(16px,env(safe-area-inset-right,0px))}
button,input,select{font:inherit;color:inherit}
:focus-visible{outline:3px solid var(--lime);outline-offset:2px}
.top{background:var(--navy);color:#fff;
  background-image:linear-gradient(90deg,transparent calc(50% - 4px),#2b4a80 calc(50% - 4px),#2b4a80 calc(50% + 4px),transparent calc(50% + 4px))}
.top .wrap{display:flex;align-items:center;justify-content:space-between;gap:12px;flex-wrap:wrap;padding-block:16px}
.brand{display:flex;align-items:center;gap:12px;min-width:0}
.brand img{width:46px;height:46px;border-radius:50%;border:3px solid #fff;flex:none}
.brand small{display:block;font-weight:800;font-size:.66rem;letter-spacing:.24em;text-transform:uppercase;color:#a9badd}
.brand h1{margin:0;font-family:var(--display);font-weight:400;font-size:1.7rem;line-height:1.05;letter-spacing:.01em}
.chip{font-family:var(--mono);font-size:.72rem;padding:4px 10px;border-radius:999px;background:rgba(255,255,255,.12);color:#fff;white-space:nowrap}
main .wrap{display:grid;gap:22px;padding-block:22px 48px}
.grid{display:grid;grid-template-columns:minmax(0,.85fr) minmax(0,1.15fr);gap:22px;align-items:start}
@media (max-width:860px){.grid{grid-template-columns:minmax(0,1fr)}}
.panel{background:var(--surface);border:1px solid var(--border);border-radius:14px;padding:20px;display:grid;gap:14px;min-width:0}
.panel h2{margin:0;font-family:var(--display);font-weight:400;font-size:1.45rem;letter-spacing:.02em;text-transform:uppercase;line-height:1.1;text-wrap:balance}
.hint{color:var(--muted);font-size:.85rem;margin:0}
.fields{display:grid;grid-template-columns:repeat(2,minmax(0,1fr));gap:12px}
@media (max-width:460px){.fields{grid-template-columns:minmax(0,1fr)}}
.full{grid-column:1/-1}
label{display:grid;gap:4px;font-size:.68rem;font-weight:800;letter-spacing:.14em;text-transform:uppercase;color:var(--muted)}
input,select{width:100%;padding:10px 12px;border:1px solid var(--border);border-radius:8px;background:var(--field);font-size:1rem;font-weight:500;letter-spacing:0;text-transform:none}
.mono{font-family:var(--mono)}
.row{display:flex;gap:8px;flex-wrap:wrap;align-items:center}
.btn{border:0;border-radius:9px;padding:11px 16px;font-weight:700;cursor:pointer;background:var(--court);color:#fff;text-decoration:none;display:inline-flex;align-items:center;justify-content:center;gap:6px}
.btn:disabled{opacity:.55;cursor:progress}
.btn.secondary{background:transparent;color:var(--fg);border:1px solid var(--border)}
.btn.danger{background:transparent;color:var(--bad);border:1px solid currentColor}
.btn.small{padding:6px 10px;font-size:.82rem}
.msg{font-size:.88rem;margin:0;min-height:1.2em}
.msg.err{color:var(--bad)}.msg.ok{color:var(--ok)}
.preview{display:grid;gap:10px;justify-items:center}
.preview .pc{max-width:620px}
.toolbar{display:flex;gap:8px;flex-wrap:wrap;align-items:center;justify-content:space-between}
.toolbar input{max-width:260px}
.list{display:grid;gap:8px}
.member{display:grid;grid-template-columns:minmax(0,1fr) auto;gap:8px 12px;align-items:center;padding:12px;border:1px solid var(--border);border-radius:10px}
.member .name{font-weight:700}
.member .meta{color:var(--muted);font-size:.8rem;display:flex;gap:10px;flex-wrap:wrap;font-variant-numeric:tabular-nums}
.member .acts{display:flex;gap:6px;flex-wrap:wrap;justify-content:flex-end}
@media (max-width:560px){.member{grid-template-columns:minmax(0,1fr)}.member .acts{justify-content:flex-start}}
.pill{font-size:.66rem;font-weight:800;letter-spacing:.1em;text-transform:uppercase;padding:2px 8px;border-radius:999px;border:1.5px solid currentColor}
.pill.ok{color:var(--ok)}.pill.warn{color:var(--warn)}.pill.bad{color:var(--bad)}
.empty{color:var(--muted);text-align:center;padding:24px 8px;border:1px dashed var(--border);border-radius:10px}
.banner{padding:12px 14px;border-radius:10px;border:1px solid var(--bad);color:var(--bad);font-size:.9rem}
.modal{position:fixed;inset:0;background:rgba(4,10,35,.65);display:grid;place-items:center;z-index:20;
  padding:max(16px,env(safe-area-inset-top,0px)) max(16px,env(safe-area-inset-right,0px)) max(16px,env(safe-area-inset-bottom,0px)) max(16px,env(safe-area-inset-left,0px))}
.modal .box{background:var(--surface);border-radius:16px;padding:22px;max-width:390px;width:100%;display:grid;gap:12px;justify-items:center;text-align:center;max-height:92vh;overflow:auto}
/* Connexion */
.gate{position:fixed;inset:0;z-index:50;background:var(--navy);display:grid;place-items:center;padding:16px;overflow:auto}
.gate form{width:100%;max-width:360px}
.gate label{display:grid;gap:6px;font-size:.8rem;font-weight:700;color:var(--muted)}
.gate input{padding:11px 12px;border:1px solid var(--border);border-radius:9px;background:var(--field);font-size:16px}
/* Scanner */
.scanbar{display:flex;align-items:center;justify-content:space-between;gap:14px;flex-wrap:wrap;margin-bottom:22px}
.scanbar .btn{font-size:1.05rem;padding:14px 22px}
.scanbox{max-width:440px!important}
.cam{position:relative;width:100%;aspect-ratio:1;border-radius:14px;overflow:hidden;background:#000}
.cam video{width:100%;height:100%;object-fit:cover;display:block}
.cam .aim{position:absolute;inset:18%;border:3px solid var(--lime);border-radius:14px;box-shadow:0 0 0 999px rgba(4,10,35,.35)}
.cam .camMsg{position:absolute;inset:0;display:grid;place-items:center;padding:20px;color:#fff;font-size:.95rem;text-align:center}
.verdict{width:100%;border-radius:14px;padding:18px;display:grid;gap:4px;color:#fff;text-align:center}
.verdict.ok{background:#1f8a55}.verdict.warn{background:#a86a12}.verdict.bad{background:#c0392b}.verdict.none{background:#56668c}
.verdict b{font-family:var(--display);font-weight:400;font-size:2rem;letter-spacing:.02em;text-transform:uppercase;line-height:1.05}
.verdict .who{font-size:1.15rem;font-weight:700}
.verdict .det{font-size:.88rem;opacity:.92}
.manual{display:flex;gap:8px;width:100%}
.manual input{flex:1;min-width:0;padding:10px 12px;border:1px solid var(--border);border-radius:9px;background:var(--field);font-family:var(--mono)}
.modal h3{margin:0;font-family:var(--display);font-weight:400;font-size:1.7rem;line-height:1.1}
.qr{background:#fff;padding:10px;border-radius:10px}
.qr svg{width:210px;height:210px;display:block}
.link{font-family:var(--mono);font-size:.68rem;word-break:break-all;color:var(--muted);user-select:all;max-height:5.5em;overflow:auto;width:100%}
.sub{margin:6px 0 0;font-family:var(--display);font-weight:400;font-size:1.1rem;letter-spacing:.02em;text-transform:uppercase}
.strip{width:100%;max-width:620px;aspect-ratio:1125/432;border-radius:10px;background:var(--navy);display:block}
.locked{max-width:460px;margin:8vh auto;text-align:center}
@media (prefers-reduced-motion:no-preference){.btn{transition:filter .15s}.btn:hover{filter:brightness(1.08)}}
/* Carte membre « terrain » — recto bleu / verso clair, se retourne au toucher.
   Toutes les tailles sont en cqw : 1cqw = 1 % de la largeur de la carte. */
.pc{
  --navy:#0b1a4a; --frame:#2b4a80; --mesh:#1a2c66;
  --court:#2f5bd3; --paper:#eef3fc; --ink:#12245e; --ink-soft:#2b4a80; --rule:#a9badd;
  --lime:#d9ec4f; --white:#ffffff;
  container-type:inline-size;
  width:100%; aspect-ratio:85.6/54; perspective:1800px;
  cursor:pointer; -webkit-tap-highlight-color:transparent; user-select:none;
}
.pc *{box-sizing:border-box}
.pc-inner{position:relative;width:100%;height:100%;transform-style:preserve-3d;transition:transform .75s cubic-bezier(.3,.7,.2,1)}
.pc.is-flipped .pc-inner{transform:rotateY(180deg)}
@media (prefers-reduced-motion:reduce){.pc-inner{transition:none}}
.pc-face{position:absolute;inset:0;border-radius:4.4cqw;background:var(--navy);overflow:hidden;
  backface-visibility:hidden;-webkit-backface-visibility:hidden;box-shadow:0 2.5cqw 6cqw rgba(4,10,35,.45)}
.pc-back{transform:rotateY(180deg)}
/* Safari peut laisser voir une face à travers l'autre : on masque la face cachée à mi-rotation */
.pc-front{visibility:visible;transition:visibility 0s linear .36s}
.pc-back{visibility:hidden;transition:visibility 0s linear .36s}
.pc.is-flipped .pc-front{visibility:hidden}
.pc.is-flipped .pc-back{visibility:visible}
.pc-inner{-webkit-transform-style:preserve-3d}
.pc-face{-webkit-transform:translateZ(.1px)}
.pc-back{-webkit-transform:rotateY(180deg) translateZ(.1px);transform:rotateY(180deg) translateZ(.1px)}

/* Cadre et filets du terrain */
.pc-frame{position:absolute;left:2cqw;right:2cqw;top:3.1%;bottom:3.1%;border-radius:3.2cqw;background:var(--frame)}
.pc-mesh{position:absolute;left:31.3%;width:37.4%;height:3.7%;
  background:
    repeating-linear-gradient(45deg,var(--mesh) 0 .18cqw,transparent .18cqw .9cqw),
    repeating-linear-gradient(-45deg,var(--mesh) 0 .18cqw,transparent .18cqw .9cqw),
    #3a5c9c}
.pc-mesh.top{top:3.1%}.pc-mesh.bot{bottom:3.1%}
.pc-slash{position:absolute;width:3.2cqw;height:2.4%;
  background:linear-gradient(115deg,transparent 30%,rgba(255,255,255,.55) 30% 38%,transparent 38% 62%,rgba(255,255,255,.55) 62% 70%,transparent 70%)}
.pc-slash.tl{left:5.6cqw;top:3.4%}.pc-slash.br{right:8.5cqw;bottom:3.4%}
.pc-court{position:absolute;left:4.25cqw;right:4.2cqw;top:6.8%;bottom:6.7%;overflow:hidden}
.pc-front .pc-court{background:
  repeating-linear-gradient(135deg,rgba(255,255,255,.055) 0 .22cqw,transparent .22cqw 1.1cqw),var(--court)}
.pc-back .pc-court{background:
  repeating-linear-gradient(135deg,rgba(43,74,128,.06) 0 .22cqw,transparent .22cqw 1.1cqw),var(--paper)}
.pc-line{position:absolute;background:var(--white)}
.pc-back .pc-line{background:var(--ink)}
.pc-line.v{top:0;bottom:0;width:.42cqw;transform:translateX(-50%)}
.pc-line.h{top:50%;height:.42cqw;transform:translateY(-50%)}
.pc-net{position:absolute;left:50%;top:4.4%;bottom:4.4%;width:2.1cqw;transform:translateX(-50%);z-index:2;
  border-left:.3cqw solid var(--navy);border-right:.3cqw solid var(--navy);
  background:
    repeating-linear-gradient(0deg,rgba(255,255,255,.55) 0 .12cqw,transparent .12cqw .55cqw),
    repeating-linear-gradient(90deg,rgba(255,255,255,.55) 0 .12cqw,transparent .12cqw .55cqw),
    #1e3f9a}
.pc-back .pc-net{background:
    repeating-linear-gradient(0deg,var(--navy) 0 .12cqw,transparent .12cqw .55cqw),
    repeating-linear-gradient(90deg,var(--navy) 0 .12cqw,transparent .12cqw .55cqw),
    #e6edf9}
.pc-net::before,.pc-net::after{content:"";position:absolute;left:-.55cqw;right:-.55cqw;height:1.8cqw;background:var(--navy);border-radius:.5cqw}
.pc-net::before{top:-.4cqw}.pc-net::after{bottom:-.4cqw}

/* Typo */
.pc-label{font-family:"Montserrat",system-ui,sans-serif;font-weight:800;text-transform:uppercase;line-height:1.35}
.pc-word{display:block;overflow:visible;font-family:"Anton","Impact","Arial Narrow Bold",sans-serif;font-weight:400}

/* ---------- Recto ---------- */
.pc-colL{position:absolute;left:0;width:15.3%;top:0;bottom:0;display:grid;place-items:center;text-align:center}
.pc-front .pc-colL .pc-label{color:var(--white);font-size:1.62cqw;letter-spacing:.11em;padding:0 .6cqw}
.pc-logo{position:absolute;border-radius:50%;background:#fff;overflow:hidden}
.pc-logo img{display:block;width:100%;height:100%;object-fit:cover;border-radius:50%}
.pc-front .pc-logo{left:32.7%;top:50%;width:25.6cqw;aspect-ratio:1;transform:translate(-50%,-50%);
  padding:1.25cqw;box-shadow:0 1.2cqw 2.4cqw rgba(5,15,60,.45);z-index:1}
.pc-front .pc-logo img{box-shadow:0 0 0 .3cqw var(--navy)}
.pc-carte,.pc-membre{position:absolute;left:68.3%;transform:translateX(-50%);white-space:nowrap;z-index:3}
.pc-carte{top:30.9%;color:var(--white)}
.pc-membre{top:52.9%;color:var(--lime)}
.pc-asso{position:absolute;left:68.3%;top:73.5%;transform:translateX(-50%);white-space:nowrap;
  color:#e3eaff;font-size:1.55cqw;letter-spacing:.32em}
.pc-ball{position:absolute;width:3.9cqw;aspect-ratio:1}
.pc-front .pc-ball{left:75%;top:17.5%;transform:translate(-50%,-50%)}
.pc-front .pc-ball::after{content:"";position:absolute;left:30%;top:78%;width:85%;height:28%;border-radius:50%;background:rgba(10,25,90,.45);z-index:-1}
.pc-speed{position:absolute;left:69.3%;top:14%;width:2.4cqw;height:3.6%;
  background:linear-gradient(170deg,transparent 0 22%,rgba(220,232,255,.85) 22% 34%,transparent 34% 62%,rgba(220,232,255,.85) 62% 74%,transparent 74%)}
.pc-ball svg{width:100%;height:100%;display:block;overflow:visible}
.pc-colR{position:absolute;right:0;width:15.3%;top:0;bottom:0;display:flex;flex-direction:column;align-items:center;text-align:center}
.pc-front .pc-colR{padding-top:6.2%}
.pc-front .pc-colR .pc-saison{color:#e3eaff;font-size:1.45cqw;letter-spacing:.38em;margin-bottom:1.2cqw;padding-left:.38em}
.pc-front .pc-year{color:var(--lime)}
.pc-dash{width:3.4cqw;height:.45cqw;border-radius:.3cqw;margin:1cqw 0 1.2cqw}
.pc-front .pc-dash{background:var(--white)}

/* ---------- Verso ---------- */
.pc-back .pc-colL{display:block}
.pc-back .pc-logo{left:50%;top:14%;width:10.6cqw;aspect-ratio:1;transform:translate(-50%,-50%);border:.42cqw solid var(--ink)}
.pc-back .pc-colL .pc-note{position:absolute;left:0;right:0;top:62%;transform:translateY(-50%);
  color:var(--ink-soft);font-size:1.32cqw;letter-spacing:.07em;line-height:1.75;padding:0 .4cqw}
.pc-cell{position:absolute;height:50%;padding:0 3.4cqw}
.pc-cell .pc-label{position:absolute;left:3.4cqw;top:12%;color:var(--ink-soft);font-size:1.58cqw;letter-spacing:.3em;white-space:nowrap}
.pc-cell .pc-rule{position:absolute;left:3.4cqw;right:5cqw;bottom:14%;height:.28cqw;background:var(--rule);border-radius:.2cqw}
.pc-val{position:absolute;left:3.4cqw;right:5cqw;bottom:17.5%;color:var(--ink);
  font-family:"Montserrat",system-ui,sans-serif;font-weight:700;font-size:2.9cqw;line-height:1.15;
  overflow:hidden;text-overflow:ellipsis;white-space:nowrap}
.pc-val.mono{font-family:"JetBrains Mono",ui-monospace,Menlo,monospace;font-weight:500;font-size:2.4cqw;letter-spacing:.02em}
.pc-stamp{font-family:"Montserrat",system-ui,sans-serif;font-weight:800;text-transform:uppercase;position:absolute;left:3.4cqw;bottom:20%;transform:rotate(-6deg);transform-origin:left bottom;
  border:.35cqw solid var(--ink);border-radius:.8cqw;padding:.6cqw 1.3cqw;color:var(--ink);
  font-size:1.35cqw;letter-spacing:.16em;display:flex;align-items:center;gap:.9cqw;white-space:nowrap;background:rgba(217,236,79,.35)}
.pc-stamp svg{width:2.2cqw;height:2.2cqw}
.pc-stamp.expired{border-color:#c0392b;color:#c0392b;background:rgba(192,57,43,.08)}
.pc-back .pc-colR{justify-content:center;padding-bottom:4%}
.pc-back .pc-year{color:var(--ink)}
.pc-back .pc-dash{background:var(--ink)}
.pc-back .pc-valid{color:var(--ink-soft);font-size:1.32cqw;letter-spacing:.08em;line-height:1.75;margin-top:2.2cqw}
.pc-back .pc-ball{left:50%;top:92%;transform:translate(-50%,-50%);width:3.6cqw}

</style>

<div class="gate" id="gate">
  <form class="panel" id="gateForm" autocomplete="on">
    <h2>Bureau · connexion</h2>
    <p class="hint" style="margin:0">Les Padelistes de Luminy — accès réservé.</p>
    <label>Identifiant<input id="gUser" name="username" autocomplete="username" autocapitalize="none" autocorrect="off" spellcheck="false" required></label>
    <label>Mot de passe<input id="gPass" name="password" type="password" autocomplete="current-password" required></label>
    <button class="btn" type="submit">Se connecter</button>
    <p class="msg err" id="gMsg"></p>
  </form>
</div>

<header class="top">
  <div class="wrap">
    <div class="brand">
      <img id="brandLogo" alt="">
      <div><small>Les Padelistes de Luminy · Bureau</small><h1>Cartes membres</h1></div>
    </div>
    <span class="chip" id="usage">Wallet : connexion…</span>
  </div>
</header>

<main>
  <div class="wrap">
    <div class="banner" id="banner" hidden></div>
    <div class="locked panel" id="locked" hidden>
      <h2>Accès réservé au bureau</h2>
      <p class="hint">Seul le propriétaire de cette page peut créer ou gérer les cartes membres.</p>
    </div>

    <div id="app">
      <div class="scanbar">
        <p class="hint" style="margin:0">Contrôle à l'entrée : l'appareil photo s'ouvre, prends le QR de la carte Wallet en photo.</p>
        <div class="row">
          <button class="btn" type="button" id="scanBtn">Scanner une carte</button>
          <button class="btn secondary" type="button" id="manualBtn">Vérifier un n°</button>
        </div>
      </div>
      <div class="grid">
        <section class="panel">
          <h2 id="formTitle">Nouveau membre</h2>
          <form id="cardForm" class="fields" autocomplete="off">
            <label>Prénom<input id="first" required></label>
            <label>Nom<input id="last" required></label>
            <label>N° de membre<input id="memberId" class="mono" required></label>
            <label>Saison<select id="year"></select></label>
            <label class="full">Valable jusqu'au<input id="fin" type="date" required></label>
            <div class="row full">
              <button class="btn" type="submit" id="submitBtn">Créer la carte</button>
              <button class="btn secondary" type="button" id="cancelEdit" hidden>Annuler</button>
            </div>
            <p class="msg full" id="formMsg"></p>
          </form>
          <p class="hint">La carte Wallet reçoit ton logo, le bleu du club et le terrain en fond. Au dos, un lien ouvre la carte recto/verso.</p>
        </section>
        <section class="panel">
          <h2>Aperçu</h2>
          <div class="preview">
            <div id="preview"></div>
            <p class="hint">Touche la carte pour voir le verso.</p>
            <h3 class="sub">Dans le Wallet</h3>
            <img id="stripPreview" class="strip" alt="Bandeau de la carte Wallet">
            <p class="hint">Ce bandeau s'affiche sur la carte Wallet, avec le nom, le n° et la date en dessous.</p>
          </div>
        </section>
      </div>

      <section class="panel" style="margin-top:22px">
        <div class="toolbar">
          <h2>Membres <span id="count" class="hint" style="font-family:var(--body);font-size:.9rem;text-transform:none"></span></h2>
          <input id="search" type="search" placeholder="Rechercher un membre">
        </div>
        <div class="list" id="list"><div class="empty">Chargement des membres…</div></div>
        <div class="row">
          <button class="btn secondary small" type="button" id="bulkBtn">Appliquer le design à toutes les cartes</button>
          <span class="msg" id="bulkMsg"></span>
        </div>
      </section>
    </div>
  </div>
</main>

<div class="modal" id="modal" hidden>
  <div class="box" role="dialog" aria-modal="true" aria-labelledby="mTitle">
    <h3 id="mTitle">Carte prête</h3>
    <p class="hint">Envoie ce lien au membre ou fais-lui scanner le QR code. Il voit sa carte recto/verso et le bouton « Ajouter à mon Wallet ».</p>
    <div class="qr" id="mQr"></div>
    <div class="link" id="mLink"></div>
    <div class="row" style="justify-content:center">
      <button class="btn" type="button" id="mCopy">Copier le lien</button>
      <a class="btn secondary" id="mOpen" href="#" target="_blank" rel="noopener">Ouvrir</a>
    </div>
    <p class="hint">Lien Wallet direct : <span class="mono" id="mWallet"></span></p>
    <p class="msg ok" id="mMsg"></p>
    <button class="btn secondary" type="button" id="mClose">Fermer</button>
  </div>
</div>

<div class="modal" id="scanModal" hidden>
  <div class="box scanbox" role="dialog" aria-modal="true" aria-labelledby="sTitle">
    <h3 id="sTitle">Scanner une carte</h3>
    <div class="cam" id="cam">
      <video id="video" playsinline muted></video>
      <div class="aim" id="aim"></div>
      <div class="camMsg" id="camMsg">Ouverture de la caméra…</div>
    </div>
    <div class="verdict" id="verdict" hidden></div>
    <div class="row" style="justify-content:center">
      <button class="btn" type="button" id="scanAgain" hidden>Scanner la suivante</button>
      <label class="btn secondary small" id="photoBtn">Reprendre la photo<input id="photo" type="file" accept="image/*" capture="environment" hidden></label>
    </div>
    <form class="manual" id="manualForm" autocomplete="off">
      <input id="manualId" placeholder="ou tape le n° (PDL-2026-001)" aria-label="Numéro de membre">
      <button class="btn secondary" type="submit">Vérifier</button>
    </form>
    <button class="btn secondary" type="button" id="sClose">Fermer</button>
  </div>
</div>

<script>window.LOGO = "data:image/png;base64,[IMAGE 172 Ko RETIRÉE]";</script>
<script>
/* Rendu partagé de la carte membre (aperçu admin + page membre). */
(function(){
  "use strict";
  var MOIS = ["janvier","février","mars","avril","mai","juin","juillet","août","septembre","octobre","novembre","décembre"];

  function esc(s){
    return String(s == null ? "" : s).replace(/[&<>"']/g, function(c){
      return {"&":"&amp;","<":"&lt;",">":"&gt;","\"":"&quot;","'":"&#39;"}[c];
    });
  }
  function frLong(fin){
    if (!fin) return "—";
    var p = fin.split("-");
    return parseInt(p[2],10) + " " + MOIS[parseInt(p[1],10)-1] + " " + p[0];
  }
  function isExpired(fin){ return !!fin && new Date(fin + "T23:59:59") < new Date(); }

  // Données de carte <-> fragment d'URL (UTF-8 → base64url)
  function encode(d){
    var json = JSON.stringify(d), bytes = new TextEncoder().encode(json), bin = "";
    bytes.forEach(function(b){ bin += String.fromCharCode(b); });
    return btoa(bin).replace(/\+/g,"-").replace(/\//g,"_").replace(/=+$/,"");
  }
  function decode(s){
    s = s.replace(/-/g,"+").replace(/_/g,"/");
    while (s.length % 4) s += "=";
    var bin = atob(s), bytes = new Uint8Array(bin.length);
    for (var i = 0; i < bin.length; i++) bytes[i] = bin.charCodeAt(i);
    return JSON.parse(new TextDecoder().decode(bytes));
  }

  function ball(seam){
    return '<svg viewBox="0 0 40 40" aria-hidden="true">' +
      '<circle cx="20" cy="20" r="18" fill="#d9ec4f"' + (seam === "ink" ? ' stroke="#12245e" stroke-width="2.6"' : '') + '/>' +
      '<path d="M9 6.5c7.5 7 7.5 20 0 27" fill="none" stroke="' + (seam === "ink" ? "#12245e" : "#ffffff") + '" stroke-width="2.6" stroke-linecap="round"/></svg>';
  }
  // Mot en gros caractères dessiné en SVG : largeur et hauteur fixées, quelle que soit la police chargée.
  function word(text, w, h, cls){
    var W = Math.round(w * 10), H = Math.round(h * 10);
    return '<svg class="pc-word ' + cls + '" viewBox="0 0 ' + W + ' ' + H + '" style="width:' + w + 'cqw;height:' + h + 'cqw" aria-hidden="true">' +
      '<text x="0" y="' + H + '" textLength="' + W + '" lengthAdjust="spacingAndGlyphs" font-size="' + Math.round(H / 0.72) + '" fill="currentColor">' + text + '</text></svg>';
  }
  var CHECK = '<svg viewBox="0 0 24 24" aria-hidden="true"><path d="M4 12.5l5 5L20 6.5" fill="none" stroke="currentColor" stroke-width="3" stroke-linecap="round" stroke-linejoin="round"/></svg>';

  // d = { c: club, p: prénom, n: nom, i: n° membre, y: année de début, f: fin (AAAA-MM-JJ) }
  function html(d, logo){
    var y1 = parseInt(d.y,10) || new Date().getFullYear(), y2 = y1 + 1;
    var club = esc(d.c || "Les Padelistes de Luminy");
    var clubLines = esc(d.c || "Les Padelistes de Luminy").replace(/ de /i, "<br>de ").replace(/^(\S+) /, "$1<br>");
    var exp = isExpired(d.f);
    var common = '<div class="pc-frame"></div><div class="pc-mesh top"></div><div class="pc-mesh bot"></div>' +
                 '<div class="pc-slash tl"></div><div class="pc-slash br"></div>';
    var logoImg = '<img src="' + esc(logo || window.LOGO) + '" alt="">';
    return '' +
    '<div class="pc-inner">' +
      '<div class="pc-face pc-front" aria-label="Recto de la carte membre ' + club + '">' + common +
        '<div class="pc-court">' +
          '<div class="pc-line v" style="left:15.3%"></div><div class="pc-line v" style="left:84.7%"></div>' +
          '<div class="pc-line h" style="left:15.3%;right:15.3%"></div>' +
          '<div class="pc-colL"><div class="pc-label">' + clubLines + '</div></div>' +
          '<div class="pc-logo">' + logoImg + '</div>' +
          '<div class="pc-speed"></div><div class="pc-ball">' + ball("white") + '</div>' +
          word("CARTE", 23, 8.3, "pc-carte") +
          word("MEMBRE", 33.7, 8.7, "pc-membre") +
          '<div class="pc-label pc-asso">Association étudiante</div>' +
          '<div class="pc-colR"><div class="pc-label pc-saison">Saison</div>' +
            word(y1, 10.5, 4.9, "pc-year") + '<div class="pc-dash"></div>' + word(y2, 10.5, 4.9, "pc-year") + '</div>' +
        '</div>' +
        '<div class="pc-net"></div>' +
      '</div>' +
      '<div class="pc-face pc-back" aria-label="Verso de la carte membre">' + common +
        '<div class="pc-court">' +
          '<div class="pc-line v" style="left:15.2%"></div><div class="pc-line v" style="left:85.5%"></div>' +
          '<div class="pc-line h" style="left:15.2%;right:14.5%"></div>' +
          '<div class="pc-colL"><div class="pc-logo">' + logoImg + '</div>' +
            '<div class="pc-label pc-note">Carte<br>personnelle<br>à présenter<br>au club</div></div>' +
          '<div class="pc-cell" style="left:15.2%;right:50%;top:0"><div class="pc-label">Nom</div>' +
            '<div class="pc-val">' + esc((d.n || "").toUpperCase()) + '</div><div class="pc-rule"></div></div>' +
          '<div class="pc-cell" style="left:50%;right:14.5%;top:0"><div class="pc-label">N° de membre</div>' +
            '<div class="pc-val mono">' + esc(d.i) + '</div><div class="pc-rule"></div></div>' +
          '<div class="pc-cell" style="left:15.2%;right:50%;top:50%"><div class="pc-label">Prénom</div>' +
            '<div class="pc-val">' + esc(d.p) + '</div><div class="pc-rule"></div></div>' +
          '<div class="pc-cell" style="left:50%;right:14.5%;top:50%"><div class="pc-label">Signature du bureau</div>' +
            (exp
              ? '<div class="pc-stamp expired">Carte expirée</div>'
              : '<div class="pc-stamp">' + CHECK + 'Validée par le bureau</div>') +
            '<div class="pc-rule"></div></div>' +
          '<div class="pc-colR">' + word(y1, 8.2, 4, "pc-year") + '<div class="pc-dash"></div>' + word(y2, 8.2, 4, "pc-year") +
            '<div class="pc-label pc-valid">Valable<br>jusqu\'au<br>' + esc(frLong(d.f)) + '</div>' +
            '<div class="pc-ball">' + ball("ink") + '</div></div>' +
        '</div>' +
        '<div class="pc-net"></div>' +
      '</div>' +
    '</div>';
  }

  function render(el, d, logo){
    el.classList.add("pc");
    el.setAttribute("role","button");
    el.setAttribute("tabindex","0");
    el.setAttribute("aria-label","Carte membre, touche pour la retourner");
    var flipped = el.classList.contains("is-flipped");
    el.innerHTML = html(d, logo);
    if (flipped) el.classList.add("is-flipped");
    if (!el.dataset.bound) {
      el.dataset.bound = "1";
      var flip = function(){ el.classList.toggle("is-flipped"); };
      el.addEventListener("click", flip);
      el.addEventListener("keydown", function(e){ if (e.key === "Enter" || e.key === " ") { e.preventDefault(); flip(); } });
    }
  }

  window.PadelCard = { render: render, encode: encode, decode: decode, frLong: frLong, isExpired: isExpired, esc: esc };
})();

</script>
<script>
(function(){
  "use strict";
  var SERVER = "Wallet wallet dev";
  var CARD_BASE = "https://claude.ai/artifact/EGp3HswnqjWRmjTWAmmp8t";
  // Le QR de la carte Wallet ouvre cette page avec #v=<n°> : le scanner de l'iPhone affiche directement le verdict
  var SELF = "https://claude.ai/artifact/MnrJCrS8FxKdKTuTX23bZr";
  var loaded = false, signedOut = false;
  var CLUB = "Les Padelistes de Luminy", PREFIX = "PDL", COLOR = "#2f5bd3";
  var $ = function(id){ return document.getElementById(id); };
  var C = window.PadelCard;
  var mcp = null, db = null, members = [], editing = null, current = null, usePro = true;

  $("brandLogo").src = window.LOGO;

  // ---------- Utilitaires ----------
  function fullName(m){ return (m.first + " " + m.last).trim(); }
  function frShort(fin){ var p = fin.split("-"); return p[2] + "/" + p[1] + "/" + p[0]; }
  function expiry(fin){ return fin + "T23:59:00+02:00"; }
  function seasonStart(){ var d = new Date(); return d.getMonth() >= 7 ? d.getFullYear() : d.getFullYear() - 1; }
  // Lien court (Wallet limite le dos de carte à 256 caractères) : [prénom, nom, n°, année, fin, série]
  function cardLink(m, serial){
    return CARD_BASE + "#" + C.encode([m.first, m.last, m.id, +m.year, m.fin, String(serial).replace(/-/g, "")]);
  }
  function errText(e){
    var code = e && e.code;
    if (code === "server_not_connected") return "Le connecteur WalletWallet n'est pas ajouté à ton compte : ajoute-le dans claude.ai, Réglages, Connecteurs.";
    if (code === "needs_reauth") return "La connexion à WalletWallet a expiré : reconnecte-la dans claude.ai, Réglages, Connecteurs.";
    if (code === "not_in_manifest" || code === "approval_required") return "Cette page n'a pas encore l'autorisation d'utiliser WalletWallet. Réessaie et accepte la demande.";
    if (code === "server_unavailable") return "WalletWallet ne répond pas pour le moment. Vérifie la liste avant de réessayer : la carte a peut-être été créée.";
    if (code === "tool_error") return "WalletWallet a refusé : " + (e.message || "erreur inconnue");
    return (e && e.message) || "Erreur inattendue.";
  }

  // ---------- Visuels de la carte Wallet (dessinés sur cette page) ----------
  var fontsReady = (document.fonts && document.fonts.load)
    ? Promise.all([document.fonts.load('400 90px "Anton"'), document.fonts.load('800 20px "Montserrat"')]).catch(function(){})
    : Promise.resolve();
  var logoImgP = new Promise(function(res, rej){ var i = new Image(); i.onload = function(){ res(i); }; i.onerror = rej; i.src = window.LOGO; });
  var artCache = {};
  function smallLogo(img){
    var c = document.createElement("canvas"); c.width = c.height = 180;
    var x = c.getContext("2d");
    x.beginPath(); x.arc(90, 90, 90, 0, Math.PI * 2); x.clip();
    x.drawImage(img, 0, 0, 180, 180);
    return c.toDataURL("image/png");
  }
  function spaced(x, px){ try { x.letterSpacing = px + "px"; } catch (e) {} }
  // Bandeau 1125×432 : le recto de la carte, recadré pour Apple Wallet (et image principale sur Google Wallet)
  function drawStrip(img, y1){
    var W = 1125, H = 432, c = document.createElement("canvas"); c.width = W; c.height = H;
    var x = c.getContext("2d");
    function rr(X, Y, w, h, r, fill){ x.beginPath(); x.moveTo(X + r, Y); x.arcTo(X + w, Y, X + w, Y + h, r); x.arcTo(X + w, Y + h, X, Y + h, r); x.arcTo(X, Y + h, X, Y, r); x.arcTo(X, Y, X + w, Y, r); x.closePath(); x.fillStyle = fill; x.fill(); }
    function mesh(X, Y, w, h){
      x.save(); x.beginPath(); x.rect(X, Y, w, h); x.clip();
      x.fillStyle = "#3a5c9c"; x.fillRect(X, Y, w, h);
      x.strokeStyle = "#1a2c66"; x.lineWidth = 2;
      for (var d = -h; d < w + h; d += 9) { x.beginPath(); x.moveTo(X + d, Y); x.lineTo(X + d + h, Y + h); x.moveTo(X + d + h, Y); x.lineTo(X + d, Y + h); x.stroke(); }
      x.restore();
    }
    x.fillStyle = "#0b1a4a"; x.fillRect(0, 0, W, H);
    rr(10, 10, W - 20, H - 20, 24, "#2b4a80");
    mesh(W * 0.31, 10, W * 0.38, 18); mesh(W * 0.31, H - 28, W * 0.38, 18);
    var X0 = 30, Y0 = 28, CW = W - 60, CH = H - 56;
    x.fillStyle = "#2f5bd3"; x.fillRect(X0, Y0, CW, CH);
    x.save(); x.beginPath(); x.rect(X0, Y0, CW, CH); x.clip();
    x.strokeStyle = "rgba(255,255,255,.06)"; x.lineWidth = 4;
    for (var d = -CH; d < CW; d += 18) { x.beginPath(); x.moveTo(X0 + d, Y0 + CH); x.lineTo(X0 + d + CH, Y0); x.stroke(); }
    x.restore();
    var L = X0 + CW * 0.13, R = X0 + CW * 0.87, MY = Y0 + CH / 2;
    x.fillStyle = "#fff"; x.fillRect(L - 3, Y0, 6, CH); x.fillRect(R - 3, Y0, 6, CH); x.fillRect(L, MY - 3, R - L, 6);
    // Colonne gauche : nom du club
    x.textAlign = "center"; x.textBaseline = "alphabetic"; x.fillStyle = "#fff";
    x.font = '800 15px "Montserrat", system-ui, sans-serif'; spaced(x, 1.5);
    ["LES", "PADELISTES", "DE LUMINY"].forEach(function(t, i){ x.fillText(t, X0 + CW * 0.065, MY - 18 + i * 24); });
    // Logo
    var LX = X0 + CW * 0.315, LR = CH * 0.36;
    x.save(); x.shadowColor = "rgba(5,15,60,.45)"; x.shadowBlur = 24; x.shadowOffsetY = 10;
    x.beginPath(); x.arc(LX, MY, LR + 12, 0, Math.PI * 2); x.fillStyle = "#fff"; x.fill(); x.restore();
    x.save(); x.beginPath(); x.arc(LX, MY, LR, 0, Math.PI * 2); x.clip(); x.drawImage(img, LX - LR, Y0 + CH / 2 - LR, LR * 2, LR * 2); x.restore();
    x.beginPath(); x.arc(LX, MY, LR, 0, Math.PI * 2); x.strokeStyle = "#0b1a4a"; x.lineWidth = 3; x.stroke();
    // Filet
    var NX = W / 2;
    x.fillStyle = "#0b1a4a"; x.fillRect(NX - 13, 16, 26, H - 32);
    x.fillStyle = "#1e3f9a"; x.fillRect(NX - 9, 18, 18, H - 36);
    x.strokeStyle = "rgba(255,255,255,.55)"; x.lineWidth = 1.5;
    for (var ny = 18; ny < H - 18; ny += 6) { x.beginPath(); x.moveTo(NX - 9, ny); x.lineTo(NX + 9, ny); x.stroke(); }
    for (var nx = NX - 9; nx <= NX + 9; nx += 6) { x.beginPath(); x.moveTo(nx, 18); x.lineTo(nx, H - 18); x.stroke(); }
    rr(NX - 17, 8, 34, 22, 6, "#0b1a4a"); rr(NX - 17, H - 30, 34, 22, 6, "#0b1a4a");
    // CARTE / MEMBRE
    var TX = X0 + CW * 0.685;
    spaced(x, 0);
    x.font = '400 96px "Anton", Impact, sans-serif'; x.fillStyle = "#fff"; x.fillText("CARTE", TX, Y0 + CH * 0.47, 230);
    x.font = '400 104px "Anton", Impact, sans-serif'; x.fillStyle = "#d9ec4f"; x.fillText("MEMBRE", TX, Y0 + CH * 0.73, 330);
    x.font = '800 15px "Montserrat", system-ui, sans-serif'; x.fillStyle = "#e3eaff"; spaced(x, 4);
    x.fillText("ASSOCIATION ÉTUDIANTE", TX, Y0 + CH * 0.85, 340);
    // Balle
    var BX = X0 + CW * 0.775, BY = Y0 + CH * 0.17;
    x.fillStyle = "rgba(10,25,90,.45)"; x.beginPath(); x.ellipse(BX + 6, BY + 18, 20, 6, 0, 0, Math.PI * 2); x.fill();
    x.fillStyle = "#d9ec4f"; x.beginPath(); x.arc(BX, BY, 17, 0, Math.PI * 2); x.fill();
    x.strokeStyle = "#fff"; x.lineWidth = 3; x.lineCap = "round"; x.beginPath(); x.arc(BX - 22, BY, 17, -0.75, 0.75); x.stroke();
    x.strokeStyle = "rgba(225,235,255,.85)"; x.lineWidth = 4;
    x.beginPath(); x.moveTo(BX - 62, BY - 12); x.lineTo(BX - 32, BY - 8); x.moveTo(BX - 58, BY + 2); x.lineTo(BX - 34, BY + 4); x.stroke();
    // Colonne droite : saison
    var SX = X0 + CW * 0.935;
    x.font = '800 13px "Montserrat", system-ui, sans-serif'; x.fillStyle = "#e3eaff"; spaced(x, 4);
    x.fillText("SAISON", SX, Y0 + CH * 0.2);
    spaced(x, 0); x.font = '400 54px "Anton", Impact, sans-serif'; x.fillStyle = "#d9ec4f";
    x.fillText(String(y1), SX, Y0 + CH * 0.42, 108);
    x.fillStyle = "#fff"; x.fillRect(SX - 16, Y0 + CH * 0.475, 32, 5);
    x.fillStyle = "#d9ec4f"; x.fillText(String(+y1 + 1), SX, Y0 + CH * 0.67, 108);
    return c.toDataURL("image/png");
  }
  function artFor(year){
    if (!artCache[year]) {
      artCache[year] = Promise.all([fontsReady, logoImgP]).then(function(r){
        var img = r[1];
        return { logo: smallLogo(img), strip: drawStrip(img, year) };
      });
    }
    return artCache[year];
  }
  function stripPreview(){
    var y = $("year").value;
    artFor(y).then(function(a){ if ($("year").value === y) $("stripPreview").src = a.strip; }).catch(function(){});
  }

  // ---------- Contenu de la carte Wallet ----------
  function passBody(m, link, art){
    var back = [];
    if (link && link.length <= 256) back.push({ label: "Ma carte recto / verso", value: link });
    back.push({ label: "Saison", value: m.year + "-" + (+m.year + 1) });
    back.push({ label: "Nom", value: m.last.toUpperCase() });
    back.push({ label: "Prénom", value: m.first });
    back.push({ label: "N° de membre", value: m.id });
    back.push({ label: "Club", value: CLUB + " · association étudiante" });
    var b = {
      logoText: CLUB,
      organizationName: CLUB,
      description: "Carte membre " + CLUB,
      secondaryFields: [{ label: "Membre", value: fullName(m) }, { label: "N°", value: m.id }, { label: "Valable jusqu'au", value: frShort(m.fin) }],
      backFields: back,
      barcodeValue: SELF + "#v=" + m.id, barcodeFormat: "QR", barcodeAltText: m.id,
      colorPreset: "blue",
      expirationDate: expiry(m.fin),
      sharingProhibited: true,
      notification: " "
    };
    if (art) {
      b.color = COLOR;
      b.logoURL = art.logo;
      b.stripURL = art.strip;
    }
    return b;
  }
  function call(tool, input){
    return mcp.callTool(SERVER, tool, input).then(function(r){ return r.payload || {}; });
  }
  function bodyFor(m, link, pro){
    if (!pro) return Promise.resolve(passBody(m, link, null));
    return artFor(m.year).then(function(a){ return passBody(m, link, a); }, function(){ return passBody(m, link, null); });
  }
  // Crée la carte ; si l'offre Pro n'est plus active, recommence sans les images.
  function createPass(m){
    return bodyFor(m, "", usePro).then(function(b){ return call("create_pass", b); }).catch(function(e){
      if (usePro && e && e.code === "tool_error" && /pro/i.test(e.message || "")) {
        usePro = false;
        return call("create_pass", passBody(m, "", null));
      }
      throw e;
    });
  }
  function updatePass(rec, m, link, pro){
    return bodyFor(m, link, pro).then(function(b){ return call("update_pass", Object.assign({ serialNumber: rec.serial }, b)); });
  }

  // ---------- Formulaire ----------
  (function(){
    var y0 = seasonStart(), sel = $("year");
    for (var y = y0 - 1; y <= y0 + 1; y++) {
      var o = document.createElement("option"); o.value = y; o.textContent = y + "-" + (y + 1); sel.appendChild(o);
    }
  })();
  function nextId(){
    var y = new Date().getFullYear(), n = 0;
    members.forEach(function(m){ var mm = /^PDL-\d{4}-(\d+)$/.exec(m.id || ""); if (mm) n = Math.max(n, +mm[1]); });
    return PREFIX + "-" + y + "-" + String(n + 1).padStart(3, "0");
  }
  function readForm(){
    return { first: $("first").value.trim(), last: $("last").value.trim(), id: $("memberId").value.trim(), year: $("year").value, fin: $("fin").value };
  }
  function resetForm(){
    editing = null;
    $("cardForm").reset();
    $("year").value = seasonStart();
    $("fin").value = (seasonStart() + 1) + "-08-31";
    $("memberId").value = nextId(); $("memberId").readOnly = false;
    $("formTitle").textContent = "Nouveau membre";
    $("submitBtn").textContent = "Créer la carte";
    $("cancelEdit").hidden = true;
    preview();
  }
  var lastPreview = "";
  function preview(){
    var m = readForm();
    var d = { c: CLUB, p: m.first || "Prénom", n: m.last || "Nom", i: m.id, y: +m.year, f: m.fin };
    var key = JSON.stringify(d);
    if (key === lastPreview) return; // évite de redessiner (et de perdre le toucher) quand rien n'a changé
    lastPreview = key;
    C.render($("preview"), d, window.LOGO);
  }
  $("cardForm").addEventListener("input", preview);
  $("cardForm").addEventListener("change", function(e){
    if (e.target.id === "year") { if (!editing) $("fin").value = (+$("year").value + 1) + "-08-31"; stripPreview(); }
    preview();
  });
  $("cancelEdit").addEventListener("click", resetForm);

  $("cardForm").addEventListener("submit", function(e){
    e.preventDefault();
    var m = readForm(), msg = $("formMsg"), btn = $("submitBtn");
    function fail(t){ msg.className = "msg full err"; msg.textContent = t; }
    if (!mcp) return fail("WalletWallet n'est pas disponible sur cette page.");
    if (new Date(expiry(m.fin)) <= new Date()) return fail("La date de fin doit être dans le futur.");
    if (!editing && members.some(function(x){ return x.id === m.id && !x.revoked; })) return fail("Ce numéro de membre existe déjà.");
    btn.disabled = true; msg.className = "msg full"; msg.textContent = editing ? "Mise à jour de la carte…" : "Création de la carte Wallet…";

    var job;
    if (editing) {
      var rec = members.find(function(x){ return x.serial === editing; });
      var link = cardLink(m, rec.serial);
      job = updatePass(rec, m, link, usePro).then(function(){
        var upd = { first: m.first, last: m.last, year: m.year, fin: m.fin, cardUrl: link, pro: usePro, updated: Date.now() };
        return saveDoc(rec.serial, upd, true).then(function(){ return Object.assign({}, rec, upd); });
      });
    } else {
      job = createPass(m).then(function(r){
        if (!r.serialNumber) throw { message: "Réponse inattendue de WalletWallet." };
        var pro = usePro, link = cardLink(m, r.serialNumber);
        var rec = { first: m.first, last: m.last, id: m.id, year: m.year, fin: m.fin, serial: r.serialNumber,
                    shareUrl: r.shareUrl, cardUrl: link, pro: pro, revoked: false, created: Date.now() };
        msg.textContent = "Ajout du lien recto/verso au dos de la carte…";
        return saveDoc(rec.serial, rec, false).then(function(){
          return updatePass(rec, m, link, pro).catch(function(){});
        }).then(function(){ return rec; });
      });
    }
    var wasEdit = !!editing;
    job.then(function(rec){
      resetForm(); refreshUsage();
      msg.className = "msg full ok";
      msg.textContent = wasEdit ? "Carte mise à jour : elle se rafraîchit seule dans le Wallet du membre." : "Carte créée" + (usePro ? "." : " (sans images : l'offre Pro n'est plus active).");
      openResult(rec);
    }).catch(function(err){ fail(errText(err)); })
      .finally(function(){ btn.disabled = false; });
  });

  // ---------- Base des membres ----------
  function saveDoc(id, data, merge){
    if (!db) return Promise.resolve();
    var ref = db.collection("members").doc(id);
    return (merge ? ref.update(data) : ref.set(data)).catch(function(){
      $("formMsg").className = "msg full err";
      $("formMsg").textContent = "La carte existe dans WalletWallet mais n'a pas pu être enregistrée dans la liste.";
    });
  }
  function status(m){
    if (m.revoked) return ["Révoquée", "bad"];
    if (C.isExpired(m.fin)) return ["Expirée", "warn"];
    return ["Active", "ok"];
  }
  function el(tag, cls, text){ var n = document.createElement(tag); if (cls) n.className = cls; if (text != null) n.textContent = text; return n; }
  function renderList(){
    var q = $("search").value.trim().toLowerCase(), list = $("list");
    list.innerHTML = "";
    var items = members.filter(function(m){ return !q || (fullName(m) + " " + m.id).toLowerCase().indexOf(q) >= 0; });
    var active = members.filter(function(m){ return status(m)[1] === "ok"; }).length;
    $("count").textContent = members.length ? "· " + active + " active" + (active > 1 ? "s" : "") : "";
    if (!items.length) {
      list.appendChild(el("div", "empty", members.length ? "Aucun membre ne correspond." : "Aucune carte pour l'instant. Remplis le formulaire pour créer la première."));
      return;
    }
    items.forEach(function(m){
      var row = el("div", "member"), info = el("div"), top = el("div", "row");
      top.appendChild(el("span", "name", fullName(m)));
      var st = status(m); top.appendChild(el("span", "pill " + st[1], st[0]));
      info.appendChild(top);
      var meta = el("div", "meta");
      meta.appendChild(el("span", "mono", m.id));
      meta.appendChild(el("span", null, "saison " + m.year + "-" + (+m.year + 1)));
      meta.appendChild(el("span", null, "jusqu'au " + frShort(m.fin)));
      info.appendChild(meta);
      var acts = el("div", "acts");
      if (!m.revoked) {
        var b1 = el("button", "btn small", "QR / lien"); b1.type = "button"; b1.onclick = function(){ openResult(m); };
        var b2 = el("button", "btn secondary small", "Modifier"); b2.type = "button"; b2.onclick = function(){ startEdit(m); };
        var b3 = el("button", "btn danger small", "Révoquer"); b3.type = "button";
        b3.onclick = function(){
          if (b3.dataset.confirm !== "1") {
            b3.dataset.confirm = "1"; b3.textContent = "Confirmer ?";
            setTimeout(function(){ if (!b3.disabled) { b3.dataset.confirm = ""; b3.textContent = "Révoquer"; } }, 4000);
            return;
          }
          b3.disabled = true; b3.textContent = "…";
          call("revoke_pass", { serialNumber: m.serial }).then(function(){
            return saveDoc(m.serial, { revoked: true, updated: Date.now() }, true);
          }).catch(function(err){
            b3.disabled = false; b3.dataset.confirm = ""; b3.textContent = "Révoquer";
            $("formMsg").className = "msg full err"; $("formMsg").textContent = errText(err);
          });
        };
        acts.appendChild(b1); acts.appendChild(b2); acts.appendChild(b3);
      }
      row.appendChild(info); row.appendChild(acts);
      list.appendChild(row);
    });
  }
  function startEdit(m){
    editing = m.serial;
    $("first").value = m.first; $("last").value = m.last; $("memberId").value = m.id;
    $("year").value = m.year; $("fin").value = m.fin; $("memberId").readOnly = true;
    $("formTitle").textContent = "Modifier " + fullName(m);
    $("submitBtn").textContent = "Mettre à jour";
    $("cancelEdit").hidden = false; $("formMsg").textContent = "";
    preview(); $("cardForm").scrollIntoView({ behavior: "smooth", block: "start" });
  }
  $("search").addEventListener("input", renderList);

  // Met à jour toutes les cartes actives avec le design actuel (une à la fois)
  $("bulkBtn").addEventListener("click", function(){
    var btn = this, msg = $("bulkMsg");
    if (!mcp) { msg.className = "msg err"; msg.textContent = "WalletWallet n'est pas disponible sur cette page."; return; }
    var todo = members.filter(function(m){ return !m.revoked && !C.isExpired(m.fin); });
    if (!todo.length) { msg.className = "msg"; msg.textContent = "Aucune carte active."; return; }
    btn.disabled = true; var done = 0, failed = 0;
    msg.className = "msg"; msg.textContent = "0 / " + todo.length + "…";
    todo.reduce(function(p, m){
      return p.then(function(){
        var link = cardLink(m, m.serial);
        return updatePass(m, m, link, usePro).then(function(){
          done++; return saveDoc(m.serial, { pro: usePro, cardUrl: link, updated: Date.now() }, true);
        }, function(){ failed++; }).then(function(){ msg.textContent = (done + failed) + " / " + todo.length + "…"; });
      });
    }, Promise.resolve()).then(function(){
      btn.disabled = false; refreshUsage();
      msg.className = failed ? "msg err" : "msg ok";
      msg.textContent = done + " carte" + (done > 1 ? "s" : "") + " mise" + (done > 1 ? "s" : "") + " à jour" + (failed ? ", " + failed + " en échec" : "") + ". Elles se rafraîchissent seules dans les Wallet.";
    });
  });

  // ---------- Fenêtre « carte prête » ----------
  function qrSvg(text){
    if (typeof qrcode !== "function") return "";
    var q = qrcode(0, "L"); q.addData(text); q.make();
    return q.createSvgTag({ cellSize: 4, margin: 0, scalable: true });
  }
  function openResult(m){
    current = m;
    $("mTitle").textContent = fullName(m);
    $("mQr").innerHTML = qrSvg(m.cardUrl);
    $("mLink").textContent = m.cardUrl;
    $("mOpen").href = m.cardUrl;
    $("mWallet").textContent = m.shareUrl || "—";
    $("mMsg").textContent = "";
    $("modal").hidden = false;
  }
  $("mClose").onclick = function(){ $("modal").hidden = true; };
  $("modal").addEventListener("click", function(e){ if (e.target === this) this.hidden = true; });
  document.addEventListener("keydown", function(e){ if (e.key === "Escape") $("modal").hidden = true; });
  $("mCopy").onclick = function(){
    var t = current.cardUrl;
    try {
      navigator.clipboard.writeText(t).then(function(){ $("mMsg").textContent = "Lien copié."; }, selectLink);
    } catch (e) { selectLink(); }
  };
  function selectLink(){
    var r = document.createRange(); r.selectNodeContents($("mLink"));
    var s = getSelection(); s.removeAllRanges(); s.addRange(r);
    $("mMsg").textContent = "Lien sélectionné : copie-le.";
  }

  // ---------- Scanner de cartes ----------
  var stream = null, scanning = false, canvas = document.createElement("canvas"), ctx = canvas.getContext("2d", { willReadFrequently: true });
  function lookup(text){
    var t = String(text || "").trim(), id = t, serial = null;
    var h = t.indexOf("#"), vm = /[#?&]v=([A-Za-z0-9-]+)/.exec(t);
    if (vm) id = decodeURIComponent(vm[1]);
    else if (h >= 0) {
      try { var d = C.decode(t.slice(h + 1)); if (Array.isArray(d)) { id = d[2]; serial = d[5]; } else if (d && d.id) { id = d.id; } } catch (e) {}
    }
    id = String(id || "").toUpperCase();
    var hits = members.filter(function(m){
      return (m.id || "").toUpperCase() === id || (serial && (m.serial || "").replace(/-/g, "") === serial);
    });
    hits.sort(function(a, b){ return (a.revoked ? 1 : 0) - (b.revoked ? 1 : 0) || (b.created || 0) - (a.created || 0); });
    return { code: id || t, m: hits[0] || null };
  }
  function showVerdict(text){
    var r = lookup(text), v = $("verdict"), m = r.m, cls, title, det;
    if (!m) { cls = "none"; title = "Carte inconnue"; det = "Aucun membre avec le code " + r.code; }
    else {
      var st = status(m);
      cls = st[1];
      title = cls === "ok" ? "Membre valide" : cls === "warn" ? "Carte expirée" : "Carte révoquée";
      det = m.id + " · saison " + m.year + "-" + (+m.year + 1) + " · " + (cls === "warn" ? "expirée le " : "jusqu'au ") + frShort(m.fin);
    }
    v.className = "verdict " + cls; v.innerHTML = "";
    v.appendChild(el("b", null, title));
    if (m) v.appendChild(el("span", "who", fullName(m)));
    v.appendChild(el("span", "det", det));
    v.hidden = false;
    $("scanAgain").hidden = false;
    stopCam(true);
    try { navigator.vibrate && navigator.vibrate(cls === "ok" ? 80 : [60, 60, 60]); } catch (e) {}
  }
  function decodeImage(src, w, h){
    if (typeof jsQR !== "function") return null;
    var max = 900, s = Math.min(1, max / Math.max(w, h));
    canvas.width = Math.round(w * s); canvas.height = Math.round(h * s);
    ctx.drawImage(src, 0, 0, canvas.width, canvas.height);
    var img = ctx.getImageData(0, 0, canvas.width, canvas.height);
    var code = jsQR(img.data, img.width, img.height, { inversionAttempts: "attemptBoth" });
    return code && code.data ? code.data : null;
  }
  function tick(){
    if (!scanning) return;
    var vd = $("video");
    if (vd.readyState >= 2 && vd.videoWidth) {
      var found = decodeImage(vd, vd.videoWidth, vd.videoHeight);
      if (found) { showVerdict(found); return; }
    }
    requestAnimationFrame(tick);
  }
  function camFail(t){
    $("camMsg").textContent = t; $("camMsg").hidden = false; $("aim").hidden = true;
  }
  function startCam(){
    $("verdict").hidden = true; $("scanAgain").hidden = true;
    $("cam").hidden = false; $("aim").hidden = false;
    $("camMsg").textContent = "Ouverture de la caméra…"; $("camMsg").hidden = false;
    if (!navigator.mediaDevices || !navigator.mediaDevices.getUserMedia) { camFail("Caméra indisponible ici : utilise « Prendre une photo du QR »."); return; }
    navigator.mediaDevices.getUserMedia({ video: { facingMode: "environment" }, audio: false }).then(function(s){
      if ($("scanModal").hidden) { s.getTracks().forEach(function(t){ t.stop(); }); return; }
      stream = s; var vd = $("video"); vd.srcObject = s;
      vd.setAttribute("playsinline", ""); vd.play();
      $("camMsg").hidden = true; scanning = true; setCamMode("ok"); requestAnimationFrame(tick);
    }).catch(function(){
      setCamMode("no");
      camFail(NATIVE);
    });
  }
  function stopCam(keepBox){
    scanning = false;
    if (stream) { stream.getTracks().forEach(function(t){ t.stop(); }); stream = null; }
    $("video").srcObject = null;
    if (keepBox) $("cam").hidden = true;
  }
  // Si la caméra en direct est bloquée sur cette page, le bouton ouvre directement l'appareil photo
  function camMode(){
    try { if (document.featurePolicy && !document.featurePolicy.allowsFeature("camera")) return "no"; } catch (e) {}
    try { return localStorage.getItem("pdl-cam") || ""; } catch (e) { return ""; }
  }
  function setCamMode(v){ try { localStorage.setItem("pdl-cam", v); } catch (e) {} }
  var NATIVE = "Utilise le scanner de QR code de l'iPhone (Centre de contrôle → « Scanner de code », ou l'appareil photo) et vise la carte Wallet : le résultat s'ouvre directement ici.";
  function scanNow(){
    $("scanModal").hidden = false; $("manualId").value = "";
    if (camMode() === "no") {
      $("verdict").hidden = true; $("scanAgain").hidden = true; $("cam").hidden = false;
      camFail(NATIVE);
    } else startCam();
  }
  // Ouverture depuis le scanner de l'iPhone : #v=PDL-2026-001
  function checkHash(){
    var vm = /[#&]v=([A-Za-z0-9-]+)/.exec(location.hash || "");
    if (!vm || !unlocked) return;
    $("scanModal").hidden = false; $("manualId").value = "";
    if (signedOut) {
      stopCam(true); var v = $("verdict"); v.className = "verdict none"; v.innerHTML = "";
      v.appendChild(el("b", null, "Connexion requise"));
      v.appendChild(el("span", "det", "Connecte-toi à claude.ai dans ce navigateur pour vérifier la carte " + vm[1] + "."));
      v.hidden = false; return;
    }
    if (!loaded) return;
    showVerdict("#v=" + vm[1]);
    $("scanAgain").hidden = true;
  }
  window.addEventListener("hashchange", checkHash);
  function openScan(){
    $("scanModal").hidden = false; $("manualId").value = "";
    $("verdict").hidden = true; $("scanAgain").hidden = true; $("cam").hidden = true;
  }
  // Le bouton ouvre directement l'appareil photo de l'iPhone
  function scanPhoto(){ openScan(); $("photo").click(); }
  $("scanBtn").onclick = scanPhoto;
  $("scanAgain").onclick = scanPhoto;
  $("manualBtn").onclick = function(){ openScan(); $("manualId").focus(); };

  // ---------- Connexion ----------
  var AUTH = "cc5b0390da028616fa03cb2c32bd076c97abf67f87b543e7d4b0fe3a2af85715", unlocked = false;
  try { unlocked = sessionStorage.getItem("pdl-auth") === AUTH; } catch (e) {}
  if (unlocked) $("gate").hidden = true; else setTimeout(function(){ $("gUser").focus(); }, 50);
  function sha256(s){
    return crypto.subtle.digest("SHA-256", new TextEncoder().encode(s)).then(function(b){
      return Array.prototype.map.call(new Uint8Array(b), function(x){ return ("0" + x.toString(16)).slice(-2); }).join("");
    });
  }
  $("gateForm").addEventListener("submit", function(e){
    e.preventDefault();
    var u = $("gUser").value.trim(), p = $("gPass").value;
    sha256("pdl-bureau|" + u + "|" + p).then(function(h){
      if (h !== AUTH) { $("gMsg").textContent = "Identifiant ou mot de passe incorrect."; $("gPass").value = ""; return; }
      unlocked = true; $("gMsg").textContent = ""; $("gPass").value = "";
      try { sessionStorage.setItem("pdl-auth", AUTH); } catch (e) {}
      $("gate").hidden = true; checkHash();
    }, function(){ $("gMsg").textContent = "Connexion impossible sur ce navigateur."; });
  });
  $("sClose").onclick = function(){ stopCam(); $("scanModal").hidden = true; };
  $("scanModal").addEventListener("click", function(e){ if (e.target === this) { stopCam(); this.hidden = true; } });
  document.addEventListener("keydown", function(e){ if (e.key === "Escape" && !$("scanModal").hidden) { stopCam(); $("scanModal").hidden = true; } });
  $("photo").addEventListener("change", function(){
    var f = this.files && this.files[0]; this.value = "";
    if (!f) return;
    var img = new Image(), url = URL.createObjectURL(f);
    img.onload = function(){
      var found = decodeImage(img, img.naturalWidth, img.naturalHeight);
      URL.revokeObjectURL(url);
      if (found) showVerdict(found);
      else { stopCam(true); var v = $("verdict"); v.className = "verdict none"; v.innerHTML = ""; v.appendChild(el("b", null, "QR non lu")); v.appendChild(el("span", "det", "Reprends la photo plus près, bien à plat, sans reflet.")); v.hidden = false; $("scanAgain").hidden = false; }
    };
    img.onerror = function(){ URL.revokeObjectURL(url); };
    img.src = url;
  });
  $("manualForm").addEventListener("submit", function(e){
    e.preventDefault(); var t = $("manualId").value.trim(); if (t) showVerdict(t);
  });

  // ---------- Quota ----------
  function refreshUsage(){
    if (!mcp) return;
    call("get_usage", {}).then(function(u){
      var plan = u.plan === "trial" ? "essai Pro" : (u.plan || "");
      $("usage").textContent = (u.count != null ? u.count + " / " + u.limit + " ce mois" : "Wallet connecté") + (plan ? " · " + plan : "");
      if (u.plan === "free") usePro = false;
    }).catch(function(e){ $("usage").textContent = "Wallet : non connecté"; showBanner(errText(e)); });
  }
  function showBanner(t){ $("banner").textContent = t; $("banner").hidden = false; }

  // ---------- Démarrage ----------
  resetForm(); stripPreview();
  Promise.all([
    claude.use("user").catch(function(){ return null; }),
    claude.use("mcp").catch(function(){ return null; }),
    claude.use("db").catch(function(){ return null; })
  ]).then(function(r){
    var user = r[0]; mcp = r[1]; db = r[2];
    var owner = user ? user.isOwner() : false;
    if (user && !owner) { $("app").hidden = true; $("locked").hidden = false; $("usage").textContent = "accès réservé"; return; }
    if (!db) { signedOut = true; checkHash(); }
    if (!mcp) showBanner("Ouvre cette page dans claude.ai pour créer des cartes : le connecteur WalletWallet n'est pas joignable ici.");
    refreshUsage();
    if (!db) { $("list").innerHTML = '<div class="empty">La liste des membres n\'est pas disponible sur cette vue.</div>'; return; }
    db.collection("members").orderBy("created", "desc").onSnapshot(function(snap){
      members = snap.docs.map(function(d){ return d.data(); });
      renderList();
      if (!loaded) { loaded = true; checkHash(); }
      if (!editing && !$("first").value) { $("memberId").value = nextId(); preview(); }
    }, function(){
      $("list").innerHTML = '<div class="empty">Impossible de charger la liste des membres. Recharge la page.</div>';
    });
  });
})();
</script>

</body></html>
