<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width,initial-scale=1,viewport-fit=cover,user-scalable=no">
<meta name="apple-mobile-web-app-capable" content="yes">
<meta name="apple-mobile-web-app-status-bar-style" content="default">
<meta name="apple-mobile-web-app-title" content="Échecs Paris">
<meta name="theme-color" content="#ffffff">
<meta name="description" content="Calendrier des tournois d'échecs à Paris 2026 — homologués FFE">
<title>Tournois Échecs · Paris 2026</title>

<!-- Apple touch icon (chess king SVG inline) -->
<link rel="apple-touch-icon" href="data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAxMjAgMTIwIj4KICA8IS0tIEZvbmQgdmVydCBmb25jw6kgc3R5bGUgw6ljaGlxdWllciAtLT4KICA8cmVjdCB3aWR0aD0iMTIwIiBoZWlnaHQ9IjEyMCIgcng9IjI0IiBmaWxsPSIjMWE2YjJlIi8+CiAgPCEtLSBDYXNlcyBkZSBsJ8OpY2hpcXVpZXIgLS0+CiAgPHJlY3QgeD0iMTAiIHk9IjEwIiB3aWR0aD0iMTgiIGhlaWdodD0iMTgiIGZpbGw9IiNmNWRlYjMiIHJ4PSIyIi8+CiAgPHJlY3QgeD0iNDYiIHk9IjEwIiB3aWR0aD0iMTgiIGhlaWdodD0iMTgiIGZpbGw9IiNmNWRlYjMiIHJ4PSIyIi8+CiAgPHJlY3QgeD0iODIiIHk9IjEwIiB3aWR0aD0iMTgiIGhlaWdodD0iMTgiIGZpbGw9IiNmNWRlYjMiIHJ4PSIyIi8+CiAgPHJlY3QgeD0iMjgiIHk9IjI4IiB3aWR0aD0iMTgiIGhlaWdodD0iMTgiIGZpbGw9IiNmNWRlYjMiIHJ4PSIyIi8+CiAgPHJlY3QgeD0iNjQiIHk9IjI4IiB3aWR0aD0iMTgiIGhlaWdodD0iMTgiIGZpbGw9IiNmNWRlYjMiIHJ4PSIyIi8+CiAgPCEtLSBQacOoY2Ugcm9pIGJsYW5jaGUgY2VudHJhbGUgLS0+CiAgPHRleHQgeD0iNjAiIHk9Ijg0IiBmb250LXNpemU9IjYyIiB0ZXh0LWFuY2hvcj0ibWlkZGxlIiBmaWxsPSJ3aGl0ZSIgZm9udC1mYW1pbHk9InNlcmlmIj7imZQ8L3RleHQ+CiAgPCEtLSBUZXh0ZSDDiVAgZW4gYmFzIC0tPgogIDx0ZXh0IHg9IjYwIiB5PSIxMTIiIGZvbnQtc2l6ZT0iMTMiIHRleHQtYW5jaG9yPSJtaWRkbGUiIGZpbGw9IiNmNWRlYjMiIGZvbnQtZmFtaWx5PSJzYW5zLXNlcmlmIiBmb250LXdlaWdodD0iYm9sZCIgbGV0dGVyLXNwYWNpbmc9IjIiPsOJQ0hFQ1M8L3RleHQ+Cjwvc3ZnPgo=">

<style>
  :root {
    --bg: #f2f2f7;
    --card: #ffffff;
    --border: #e5e5ea;
    --border2: #f2f2f7;
    --txt: #1c1c1e;
    --txt2: #3c3c43;
    --txt3: #8e8e93;
    --blue: #007aff;
    --red: #ff3b30;
    --green: #34c759;
    --gold: #ff9500;
    --safe-top: env(safe-area-inset-top, 0px);
    --safe-bot: env(safe-area-inset-bottom, 0px);
  }
  * { box-sizing: border-box; margin: 0; padding: 0; -webkit-tap-highlight-color: transparent; }
  html, body { height: 100%; background: var(--bg); overflow: hidden; }
  body { font-family: -apple-system, 'SF Pro Display', 'Helvetica Neue', Arial, sans-serif; color: var(--txt); }

  #root { display: flex; flex-direction: column; height: 100%; padding-top: var(--safe-top); padding-bottom: var(--safe-bot); }

  /* ── TOP BAR ── */
  #topbar { background: var(--card); border-bottom: 1px solid var(--border); flex-shrink: 0; z-index: 100; }

  /* ── SCROLLABLE BODY ── */
  #scroll { flex: 1; overflow-y: auto; -webkit-overflow-scrolling: touch; overscroll-behavior: contain; }

  /* ── BOTTOM TAB BAR ── */
  #tabbar {
    display: flex; background: rgba(255,255,255,.92);
    backdrop-filter: blur(20px); -webkit-backdrop-filter: blur(20px);
    border-top: 1px solid var(--border); flex-shrink: 0;
    padding: 6px 0 8px;
  }
  .tab-btn {
    flex: 1; border: none; background: none; cursor: pointer;
    display: flex; flex-direction: column; align-items: center; gap: 2px;
    font-family: inherit; padding: 2px 0;
  }
  .tab-icon { font-size: 22px; line-height: 1; display: block; }
  .tab-label { font-size: 10px; font-weight: 600; }

  /* ── MONTH NAV ── */
  #month-nav { display: flex; align-items: center; justify-content: space-between; padding: 10px 2px 4px; }
  .nav-arrow { background: none; border: none; color: var(--blue); font-size: 26px; padding: 0 12px; cursor: pointer; line-height: 1; }
  #month-title-btn { background: none; border: none; cursor: pointer; text-align: center; padding: 2px 8px; border-radius: 8px; }
  #month-title { font-size: 20px; font-weight: 700; color: var(--txt); display: flex; align-items: center; gap: 5px; }
  .chevron { color: var(--blue); font-size: 13px; }
  #month-sub { font-size: 12px; color: var(--txt3); margin-top: 1px; }

  /* ── DAY HEADERS ── */
  #day-headers { display: grid; grid-template-columns: repeat(7,minmax(0,1fr)); padding: 0 2px 4px; }
  .dh { text-align: center; font-size: 11px; font-weight: 600; color: var(--txt3); }

  /* ── CALENDAR GRID ── */
  #cal-grid { padding: 0 2px; background: var(--card); border-bottom: 1px solid var(--border); }
  .week-row { display: grid; grid-template-columns: repeat(7,minmax(0,1fr)); border-top: 1px solid var(--border2); }
  .day-cell { overflow: hidden; padding: 1px 1px 3px; min-height: 62px; }
  .day-num {
    font-size: 15px; width: 26px; height: 26px; border-radius: 50%;
    display: flex; align-items: center; justify-content: center;
    margin: 2px auto 2px; font-weight: 400;
  }
  .day-num.today { background: var(--red); color: #fff; font-weight: 700; }
  .day-num.weekend { color: var(--txt3); }
  .evt-pill {
    display: flex; align-items: center; gap: 2px; padding: 1px 3px;
    border-radius: 3px; margin-bottom: 1px; cursor: pointer;
    overflow: hidden; white-space: nowrap; width: 100%;
    font-size: 9px; line-height: 1.3; font-weight: 500;
  }
  .evt-dot { width: 5px; height: 5px; border-radius: 50%; flex-shrink: 0; }
  .evt-name { overflow: hidden; text-overflow: ellipsis; white-space: nowrap; flex: 1; min-width: 0; }
  .more-lbl { font-size: 8px; color: var(--txt3); text-align: center; cursor: pointer; }

  /* ── PICKER ── */
  #picker { background: var(--card); border-bottom: 1px solid var(--border); display: none; }
  #picker.open { display: block; }
  #yr-nav { display: flex; align-items: center; justify-content: space-between; padding: 12px 16px 8px; }
  .yr-btn { background: var(--bg); border: none; border-radius: 8px; width: 36px; height: 36px; cursor: pointer; font-size: 18px; display: flex; align-items: center; justify-content: center; }
  #yr-label { font-weight: 700; font-size: 18px; }
  #month-grid { display: grid; grid-template-columns: repeat(3,1fr); gap: 8px; padding: 0 16px 16px; }
  .mth-btn {
    padding: 12px 4px; border-radius: 10px; border: none; cursor: pointer;
    font-family: inherit; font-size: 14px; font-weight: 500;
    background: transparent; color: var(--txt); position: relative;
  }
  .mth-btn.selected { background: var(--blue); color: #fff; }
  .mth-btn.has-evt { font-weight: 700; color: var(--blue); }
  .mth-btn.selected.has-evt { color: #fff; }
  .mth-dot { position: absolute; bottom: 4px; left: 50%; transform: translateX(-50%); width: 5px; height: 5px; border-radius: 50%; background: var(--blue); }

  /* ── LEGEND ── */
  #legend { background: var(--card); border-bottom: 1px solid var(--border); padding: 8px 14px; display: flex; flex-wrap: wrap; gap: 5px 12px; }
  .leg-item { display: flex; align-items: center; gap: 4px; font-size: 10.5px; color: var(--txt2); }
  .leg-dot { width: 7px; height: 7px; border-radius: 50%; }

  /* ── EVENT LIST ── */
  .evt-row {
    display: flex; align-items: flex-start; gap: 10px; padding: 11px 14px;
    border-bottom: 1px solid var(--border); background: var(--card); cursor: pointer;
  }
  .evt-row:active { background: #f5f5f5; }
  .date-block { text-align: center; min-width: 38px; flex-shrink: 0; }
  .date-mon { font-size: 10px; color: var(--txt3); text-transform: uppercase; }
  .date-day { font-size: 24px; font-weight: 200; color: var(--txt); line-height: 1; }
  .date-end { font-size: 9px; color: #c7c7cc; }
  .evt-dot2 { width: 9px; height: 9px; border-radius: 50%; margin-top: 7px; flex-shrink: 0; }
  .evt-info { flex: 1; min-width: 0; }
  .evt-time-lbl { font-size: 12px; color: var(--red); font-weight: 600; margin-bottom: 2px; }
  .evt-title { font-size: 14px; font-weight: 600; color: var(--txt); line-height: 1.2; margin-bottom: 2px; }
  .evt-loc { font-size: 12px; color: var(--txt3); overflow: hidden; text-overflow: ellipsis; white-space: nowrap; margin-bottom: 4px; }
  .tags { display: flex; gap: 4px; flex-wrap: wrap; }
  .tag { font-size: 10px; padding: 1px 7px; border-radius: 99px; }
  .arr { color: #c7c7cc; font-size: 14px; margin-top: 6px; flex-shrink: 0; }

  /* ── SEARCH ── */
  #search-bar { display: none; padding: 10px 14px 8px; }
  #search-bar.open { display: block; }
  .search-wrap { position: relative; margin-bottom: 8px; }
  .search-ico { position: absolute; left: 10px; top: 50%; transform: translateY(-50%); color: var(--txt3); font-size: 15px; }
  #search-input {
    width: 100%; border: none; background: #e5e5ea; border-radius: 10px;
    padding: 8px 12px 8px 34px; font-size: 15px; font-family: inherit; outline: none;
  }
  .cancel-btn { background: none; border: none; color: var(--blue); font-size: 14px; cursor: pointer; font-family: inherit; float: right; margin-top: -32px; padding: 8px 0; }
  .cat-scroll { display: flex; gap: 6px; overflow-x: auto; padding-bottom: 2px; scrollbar-width: none; }
  .cat-scroll::-webkit-scrollbar { display: none; }
  .cat-btn { font-size: 10px; padding: 2px 10px; border-radius: 99px; cursor: pointer; border: 1px solid transparent; white-space: nowrap; font-family: inherit; }
  .no-result { text-align: center; padding: 40px 16px; color: var(--txt3); font-size: 14px; }

  /* ── MODAL ── */
  #modal-overlay {
    position: fixed; inset: 0; background: rgba(0,0,0,.4);
    z-index: 500; display: none; align-items: flex-end;
  }
  #modal-overlay.open { display: flex; }
  #modal-sheet {
    background: var(--card); border-radius: 16px 16px 0 0; width: 100%;
    max-height: 88vh; overflow-y: auto; -webkit-overflow-scrolling: touch;
    padding-bottom: calc(20px + var(--safe-bot));
  }
  .modal-handle { width: 36px; height: 4px; background: #c7c7cc; border-radius: 2px; margin: 10px auto 14px; }
  .modal-header { padding: 0 16px 14px; border-bottom: 1px solid var(--border2); }
  .modal-badges { display: flex; gap: 5px; margin-bottom: 7px; flex-wrap: wrap; }
  .modal-title { font-size: 18px; font-weight: 700; color: var(--txt); line-height: 1.25; }
  .close-btn {
    background: var(--bg); border: none; border-radius: 50%; width: 28px; height: 28px;
    cursor: pointer; font-size: 14px; color: #666; display: flex; align-items: center; justify-content: center;
  }
  .modal-body { padding: 14px 16px 0; }
  .highlight-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 10px; margin-bottom: 14px; }
  .highlight-box { padding: 10px 12px; border-radius: 10px; border: 1px solid; }
  .hl-label { font-size: 10px; color: var(--txt3); text-transform: uppercase; letter-spacing: .05em; margin-bottom: 3px; }
  .hl-val { font-size: 17px; font-weight: 700; }
  .detail-row { display: flex; gap: 10px; margin-bottom: 10px; font-size: 13px; }
  .detail-icon { font-size: 17px; flex-shrink: 0; margin-top: 1px; }
  .detail-label { font-size: 10px; color: var(--txt3); text-transform: uppercase; letter-spacing: .04em; margin-bottom: 1px; }
  .detail-val { color: var(--txt); line-height: 1.4; }
  .contact-box { background: #f9f9f9; border: 1px solid var(--border); border-radius: 12px; padding: 12px 14px; margin-top: 12px; }
  .contact-title { font-size: 11px; color: var(--txt3); text-transform: uppercase; letter-spacing: .06em; font-weight: 600; margin-bottom: 8px; }
  .contact-row { display: flex; align-items: center; gap: 8px; padding: 6px 0; border-bottom: 1px solid var(--border2); }
  .contact-row:last-child { border-bottom: none; }
  .contact-row-left { font-size: 14px; flex-shrink: 0; }
  .contact-label { font-size: 10px; color: var(--txt3); text-transform: uppercase; letter-spacing: .04em; margin-bottom: 1px; }
  .contact-val { font-size: 14px; color: var(--txt); }
  a.clink { color: var(--blue); text-decoration: none; font-size: 14px; }
  .warn-box { background: #fffbeb; border: 1px solid #fde68a; border-radius: 10px; padding: 10px 12px; margin-top: 10px; font-size: 12px; color: #92400e; line-height: 1.5; }
  .action-row { display: flex; gap: 8px; margin-top: 12px; }
  .action-btn { flex: 1; display: flex; align-items: center; justify-content: center; gap: 5px; padding: 12px; border-radius: 12px; font-size: 14px; font-weight: 600; text-decoration: none; border: none; cursor: pointer; font-family: inherit; }
  .site-btn { display: flex; align-items: center; justify-content: center; gap: 6px; margin: 8px 0 0; padding: 13px; border-radius: 12px; color: #fff; font-size: 15px; font-weight: 600; text-decoration: none; background: #1c1c1e; }

  /* ── INSTALL GUIDE ── */
  #install-modal { position: fixed; inset: 0; background: rgba(0,0,0,.5); z-index: 600; display: none; align-items: flex-end; }
  #install-modal.open { display: flex; }
  #install-sheet { background: var(--card); border-radius: 16px 16px 0 0; width: 100%; padding: 20px 20px calc(20px + var(--safe-bot)); }
  .install-step { display: flex; gap: 14px; align-items: flex-start; padding: 12px 0; border-bottom: 1px solid var(--border2); }
  .install-step:last-child { border-bottom: none; }
  .step-num { width: 30px; height: 30px; border-radius: 50%; background: var(--blue); color: #fff; font-weight: 700; font-size: 14px; display: flex; align-items: center; justify-content: center; flex-shrink: 0; }
  .step-text { font-size: 14px; color: var(--txt); line-height: 1.5; }
  .step-em { font-weight: 600; }
  .ios-share { font-size: 20px; }
</style>
</head>
<body>
<div id="root">

  <!-- TOP BAR -->
  <div id="topbar">
    <div id="month-nav" style="display:none">
      <button class="nav-arrow" id="btn-prev">‹</button>
      <button id="month-title-btn">
        <div id="month-title"><span id="mth-name"></span><span class="chevron">▾</span></div>
        <div id="month-sub"></div>
      </button>
      <button class="nav-arrow" id="btn-next">›</button>
    </div>
    <div id="day-headers" style="display:none">
      <div class="dh">L</div><div class="dh">M</div><div class="dh">M</div>
      <div class="dh">J</div><div class="dh">V</div><div class="dh">S</div><div class="dh">D</div>
    </div>
    <div id="search-bar">
      <div class="search-wrap">
        <span class="search-ico">🔍</span>
        <input id="search-input" type="search" placeholder="Lieu, prix, heure, arrdt, contact…">
      </div>
      <button class="cancel-btn" id="cancel-search">Annuler</button>
      <div class="cat-scroll" id="cat-filters"></div>
    </div>
  </div>

  <!-- PICKER -->
  <div id="picker">
    <div id="yr-nav">
      <button class="yr-btn" id="yr-prev">‹</button>
      <span id="yr-label"></span>
      <button class="yr-btn" id="yr-next">›</button>
    </div>
    <div id="month-grid"></div>
  </div>

  <!-- SCROLLABLE -->
  <div id="scroll">
    <div id="cal-grid"></div>
    <div id="legend"></div>
    <div id="evt-list"></div>
  </div>

  <!-- TAB BAR -->
  <div id="tabbar">
    <button class="tab-btn" id="tab-cal">
      <span class="tab-icon">📅</span>
      <span class="tab-label" style="color:var(--blue)">Calendrier</span>
    </button>
    <button class="tab-btn" id="tab-search">
      <span class="tab-icon">🔍</span>
      <span class="tab-label" style="color:var(--txt3)">Rechercher</span>
    </button>
    <button class="tab-btn" id="tab-today">
      <span class="tab-icon" id="today-badge" style="width:24px;height:24px;line-height:24px;text-align:center;background:var(--red);border-radius:6px;color:#fff;font-size:13px;font-weight:700;display:block"></span>
      <span class="tab-label" style="color:var(--txt3)">Aujourd'hui</span>
    </button>
    <button class="tab-btn" id="tab-install">
      <span class="tab-icon">📲</span>
      <span class="tab-label" style="color:var(--txt3)">Installer</span>
    </button>
  </div>
</div>

<!-- MODAL -->
<div id="modal-overlay">
  <div id="modal-sheet"></div>
</div>

<!-- INSTALL GUIDE -->
<div id="install-modal">
  <div id="install-sheet">
    <div style="font-size:20px;font-weight:700;margin-bottom:4px">📲 Installer l'application</div>
    <div style="font-size:13px;color:var(--txt3);margin-bottom:16px">Ajoutez ce calendrier sur votre écran d'accueil iPhone — aucun App Store requis.</div>
    <div class="install-step">
      <div class="step-num">1</div>
      <div class="step-text">Ouvrez cette page dans <span class="step-em">Safari</span> (pas Chrome ni Firefox)</div>
    </div>
    <div class="install-step">
      <div class="step-num">2</div>
      <div class="step-text">Appuyez sur l'icône <span class="step-em">Partager</span> <span class="ios-share">⬆️</span> en bas de Safari</div>
    </div>
    <div class="install-step">
      <div class="step-num">3</div>
      <div class="step-text">Faites défiler et choisissez <span class="step-em">« Sur l'écran d'accueil »</span></div>
    </div>
    <div class="install-step">
      <div class="step-num">4</div>
      <div class="step-text">Appuyez sur <span class="step-em">Ajouter</span> — l'appli apparaît sur votre écran d'accueil !</div>
    </div>
    <div style="background:#f0f9ff;border:1px solid #bae6fd;border-radius:10px;padding:10px 12px;margin:12px 0;font-size:12px;color:#0369a1;line-height:1.5">
      💡 <strong>URL de l'application :</strong><br>
      <span id="app-url" style="font-family:monospace;word-break:break-all"></span>
    </div>
    <button onclick="document.getElementById('install-modal').classList.remove('open')" style="width:100%;padding:14px;background:var(--blue);color:#fff;border:none;border-radius:12px;font-size:16px;font-weight:600;cursor:pointer;font-family:inherit">Compris !</button>
  </div>
</div>

<script>
// ─── DATA ────────────────────────────────────────────────────────────────────
const EVENTS = [
  {
    id:1, date:"2026-05-30", dateFin:null,
    heure:"13h00", fin:"18h30",
    nom:"Schlak · 95e Tournoi Rapide Jeunes",
    lieu:"12 rue Chaptal, Paris 9e (Pigalle)",
    arrdt:"Paris 9e", metro:"Pigalle (L2, L12)",
    tarif:"6 / 12 / 18 € selon QF · 24 € sur place", tarifNum:18,
    age:"5–15 ans + adultes",
    format:"Rapide · 6 rondes · 15 min KO ou 12 min+3s",
    horaires:"Samedi 13h00 – 18h30",
    homologation:"FFE & FIDE",
    inscription:"schlak.org",
    contact_nom:"Schlak", contact_email:"contact@schlak.org", contact_tel:"", contact_site:"schlak.org",
    lien:"http://schlak.org/", statut:"confirmé", color:"#3b82f6", cat:"Jeunes",
  },
  {
    id:2, date:"2026-06-04", dateFin:"2026-06-14",
    heure:"Voir calendrier FFE", fin:"—",
    nom:"Top 16 · Finale par équipes",
    lieu:"Paris / IDF (lieu à confirmer)", arrdt:"IDF", metro:"—",
    tarif:"Compétition officielle (via club)", tarifNum:0,
    age:"Adultes licenciés", format:"Classique · 11 rondes", horaires:"4–14 juin 2026",
    homologation:"FFE", inscription:"Via club affilié FFE",
    contact_nom:"FFE", contact_email:"contact@ffechecs.fr", contact_tel:"01 39 44 65 80", contact_site:"echecs.asso.fr",
    lien:"https://www.echecs.asso.fr/", statut:"confirmé", color:"#ef4444", cat:"National",
  },
  {
    id:3, date:"2026-06-13", dateFin:null,
    heure:"Voir calendrier FFE", fin:"—",
    nom:"Top 12 Féminin · Finale",
    lieu:"Paris (lieu à confirmer)", arrdt:"Paris", metro:"—",
    tarif:"Compétition officielle (via club)", tarifNum:0,
    age:"Femmes licenciées", format:"Par équipes", horaires:"Journée du 13 juin",
    homologation:"FFE", inscription:"Via club affilié FFE",
    contact_nom:"FFE", contact_email:"contact@ffechecs.fr", contact_tel:"01 39 44 65 80", contact_site:"echecs.asso.fr",
    lien:"https://www.echecs.asso.fr/", statut:"confirmé", color:"#ec4899", cat:"Féminin",
  },
  {
    id:4, date:"2026-07-11", dateFin:"2026-07-17",
    heure:"Voir idf-echecs.fr", fin:"—",
    nom:"99e Championnat de Paris IDF",
    lieu:"Paris (gymnase à confirmer)", arrdt:"Paris", metro:"Voir idf-echecs.fr",
    tarif:"Voir idf-echecs.fr", tarifNum:30,
    age:"Tous niveaux · Licenciés A", format:"Classique · 7–9 rondes", horaires:"11–17 juillet 2026",
    homologation:"FFE & FIDE", inscription:"idf-echecs.fr",
    contact_nom:"Ligue IDF des Échecs", contact_email:"contact@idf-echecs.fr", contact_tel:"", contact_site:"idf-echecs.fr",
    lien:"https://idf-echecs.fr/", statut:"confirmé", color:"#f59e0b", cat:"Championnat",
  },
  {
    id:5, date:"2026-08-07", dateFin:"2026-08-16",
    heure:"1re ronde Nationaux : 15h (7 août)", fin:"16 août",
    nom:"Championnat de France · Vichy",
    lieu:"Palais des Congrès, Vichy (03)", arrdt:"Vichy", metro:"TGV Paris → Vichy ~3h",
    tarif:"Tarif réduit avant le 30 juin", tarifNum:50,
    age:"Tous · U8 à Vétérans (10 catégories)", format:"Classique & Opens · 9–11 rondes", horaires:"Nationaux 7–16 août · Opens 8–16 août",
    homologation:"FFE & FIDE", inscription:"echecs.asso.fr (ouvert le 11 mai)",
    contact_nom:"FFE", contact_email:"contact@ffechecs.fr", contact_tel:"01 39 44 65 80", contact_site:"echecs.asso.fr",
    lien:"https://www.echecs.asso.fr/default.aspx?Cat=15", statut:"confirmé", color:"#ef4444", cat:"National",
  },
  {
    id:6, date:"2026-09-26", dateFin:null,
    heure:"13h00", fin:"18h30",
    nom:"Schlak · 96e Tournoi Rapide Jeunes ⚑",
    lieu:"Paris (lieu à confirmer en sept.)", arrdt:"Paris", metro:"Voir schlak.org",
    tarif:"6 / 12 / 18 € selon QF · 24 € sur place", tarifNum:18,
    age:"5–15 ans + adultes", format:"Rapide · 6 rondes", horaires:"Samedi 13h00 – 18h30",
    homologation:"FFE & FIDE", inscription:"schlak.org",
    contact_nom:"Schlak", contact_email:"contact@schlak.org", contact_tel:"", contact_site:"schlak.org",
    lien:"http://schlak.org/", statut:"estimé", color:"#3b82f6", cat:"Jeunes",
  },
  {
    id:7, date:"2026-10-03", dateFin:"2026-10-04",
    heure:"Pointage 9h · 1re ronde 10h", fin:"~19h",
    nom:"Festival Tour Blanche · Paris 20e ⚑",
    lieu:"Mairie du 20e, Paris 20e", arrdt:"Paris 20e", metro:"Gambetta (L3)",
    tarif:"~10 € jeunes · ~20 € adultes", tarifNum:20,
    age:"Tous niveaux", format:"Rapide · 9 rondes · 12 min+3s", horaires:"Sam. 10h–20h · Dim. 9h–18h",
    homologation:"FFE & FIDE", inscription:"tourblanche.asso.fr",
    contact_nom:"Tour Blanche Échecs", contact_email:"contact@tourblanche.asso.fr", contact_tel:"", contact_site:"tourblanche.asso.fr",
    lien:"https://www.tourblanche.asso.fr/", statut:"estimé", color:"#8b5cf6", cat:"Open",
  },
  {
    id:8, date:"2026-10-17", dateFin:null,
    heure:"Pointage 9h · 1re ronde 10h30", fin:"~18h",
    nom:"Club 608 · 18e Rapide · Paris 15e ⚑",
    lieu:"Mairie du 15e, 31 rue Péclet, Paris 15e", arrdt:"Paris 15e", metro:"Vaugirard (L12)",
    tarif:"~20 € jeunes · ~25 € adultes", tarifNum:20,
    age:"Tous · Licence B minimum (Elo < 2200)", format:"Rapide · 9 rondes · 12 min+3s", horaires:"Pointage 9h–10h15 · 1re ronde 10h30 · Remise ~18h",
    homologation:"FFE & FIDE", inscription:"club608dechecsdeparis.fr",
    contact_nom:"Club 608 d'Échecs de Paris", contact_email:"contact@club608dechecsdeparis.fr", contact_tel:"", contact_site:"club608dechecsdeparis.fr",
    lien:"https://www.club608dechecsdeparis.fr/", statut:"estimé", color:"#10b981", cat:"Open",
  },
  {
    id:9, date:"2026-10-24", dateFin:null,
    heure:"13h00", fin:"18h30",
    nom:"Schlak · 97e Tournoi Rapide Jeunes ⚑",
    lieu:"Paris (lieu à confirmer)", arrdt:"Paris", metro:"Voir schlak.org",
    tarif:"6 / 12 / 18 € selon QF · 24 € sur place", tarifNum:18,
    age:"5–15 ans + adultes", format:"Rapide · 6 rondes", horaires:"Samedi 13h00 – 18h30",
    homologation:"FFE & FIDE", inscription:"schlak.org",
    contact_nom:"Schlak", contact_email:"contact@schlak.org", contact_tel:"", contact_site:"schlak.org",
    lien:"http://schlak.org/", statut:"estimé", color:"#3b82f6", cat:"Jeunes",
  },
  {
    id:10, date:"2026-11-11", dateFin:null,
    heure:"9h00", fin:"~18h00",
    nom:"Qualifications Jeunes Paris · CDPE ⚑",
    lieu:"Paris (ex : Halle Carpentier, 13e)", arrdt:"Paris 13e", metro:"Porte d'Ivry (L7)",
    tarif:"Gratuit / très faible", tarifNum:0,
    age:"Jeunes licenciés FFE · toutes catégories", format:"Système suisse · plusieurs rondes", horaires:"9h00 – 18h00 (journée entière)",
    homologation:"FFE", inscription:"Via club affilié · cdpe75.fr",
    contact_nom:"Comité Dép. Parisien des Échecs", contact_email:"cdpe75@gmail.com", contact_tel:"", contact_site:"cdpe75.fr",
    lien:"https://www.cdpe75.fr/", statut:"estimé", color:"#f59e0b", cat:"Jeunes",
  },
  {
    id:11, date:"2026-11-21", dateFin:null,
    heure:"13h00", fin:"18h30",
    nom:"Schlak · 98e Tournoi Rapide Jeunes ⚑",
    lieu:"Paris (lieu à confirmer)", arrdt:"Paris", metro:"Voir schlak.org",
    tarif:"6 / 12 / 18 € selon QF · 24 € sur place", tarifNum:18,
    age:"5–15 ans + adultes", format:"Rapide · 6 rondes", horaires:"Samedi 13h00 – 18h30",
    homologation:"FFE & FIDE", inscription:"schlak.org",
    contact_nom:"Schlak", contact_email:"contact@schlak.org", contact_tel:"", contact_site:"schlak.org",
    lien:"http://schlak.org/", statut:"estimé", color:"#3b82f6", cat:"Jeunes",
  },
  {
    id:12, date:"2026-12-05", dateFin:null,
    heure:"Pointage 13h45 · 1re ronde 14h", fin:"~17h30",
    nom:"Paris Jeunes Echecs · Rapide Jeunes ⚑",
    lieu:"12 bis rue Saint-Jean, Paris 17e", arrdt:"Paris 17e", metro:"La Fourche (L13)",
    tarif:"~15 €", tarifNum:15,
    age:"5–16 ans (collèges & joueurs de club)", format:"Rapide · 7 rondes", horaires:"Pointage 13h45 · Début 14h · Fin ~17h30",
    homologation:"FFE", inscription:"parisjeunesechecs@gmail.com",
    contact_nom:"Paris Jeunes Echecs", contact_email:"parisjeunesechecs@gmail.com", contact_tel:"06 23 15 53 35", contact_site:"parisjeunesechecs.com",
    lien:"http://www.parisjeunesechecs.com/", statut:"estimé", color:"#3b82f6", cat:"Jeunes",
  },
  {
    id:13, date:"2026-12-19", dateFin:null,
    heure:"Pointage 9h · 1re ronde 10h30", fin:"~18h",
    nom:"Club 608 · Rapide fin d'année ⚑",
    lieu:"Mairie du 15e, 31 rue Péclet, Paris 15e", arrdt:"Paris 15e", metro:"Vaugirard (L12)",
    tarif:"~20 € jeunes · ~25 € adultes", tarifNum:20,
    age:"Tous · Licence B minimum", format:"Rapide · 9 rondes · 12 min+3s", horaires:"Pointage 9h–10h15 · 1re ronde 10h30 · Remise ~18h",
    homologation:"FFE & FIDE", inscription:"club608dechecsdeparis.fr",
    contact_nom:"Club 608 d'Échecs de Paris", contact_email:"contact@club608dechecsdeparis.fr", contact_tel:"", contact_site:"club608dechecsdeparis.fr",
    lien:"https://www.club608dechecsdeparis.fr/", statut:"estimé", color:"#10b981", cat:"Open",
  },
];

const CATS = { Jeunes:"#3b82f6", Open:"#10b981", Championnat:"#f59e0b", National:"#ef4444", Féminin:"#ec4899" };
const MOIS_L = ["Janvier","Février","Mars","Avril","Mai","Juin","Juillet","Août","Septembre","Octobre","Novembre","Décembre"];
const MOIS_C = ["Jan","Fév","Mar","Avr","Mai","Juin","Juil","Août","Sep","Oct","Nov","Déc"];
const MOIS_M = ["jan","fév","mar","avr","mai","juin","juil","août","sep","oct","nov","déc"];

// ─── STATE ───────────────────────────────────────────────────────────────────
const now = new Date();
let state = { month:4, year:2026, view:"cal", pickerOpen:false, query:"", cat:"Tous", sel:null };

function eventsForDay(y,m,d){
  const iso=`${y}-${String(m+1).padStart(2,"0")}-${String(d).padStart(2,"0")}`;
  return EVENTS.filter(e=>iso>=e.date&&iso<=(e.dateFin||e.date));
}
function eventsForMonth(y,m){
  const ms=`${y}-${String(m+1).padStart(2,"0")}`;
  return EVENTS.filter(e=>e.date.startsWith(ms)||(e.dateFin&&e.dateFin>=ms+"-01"&&e.date<=ms+"-31")).sort((a,b)=>a.date.localeCompare(b.date));
}
function daysInMonth(y,m){ return new Date(y,m+1,0).getDate(); }
function startDay(y,m){ const d=new Date(y,m,1).getDay(); return d===0?6:d-1; }
function fmtDate(iso){ const[y,m,d]=iso.split("-"); return `${d}/${m}/${y}`; }

// ─── RENDER ──────────────────────────────────────────────────────────────────
function render(){
  const {month:m,year:y,view,pickerOpen,query,cat,sel}=state;
  const isSearch=view==="search";

  // Top bar
  document.getElementById("month-nav").style.display = isSearch?"none":"flex";
  document.getElementById("day-headers").style.display = isSearch?"none":"grid";
  document.getElementById("search-bar").classList.toggle("open",isSearch);
  document.getElementById("mth-name").textContent = MOIS_L[m];
  const me=eventsForMonth(y,m);
  document.getElementById("month-sub").textContent = `${y} · ${me.length} tournoi${me.length!==1?"s":""}`;

  // Picker
  document.getElementById("picker").classList.toggle("open",pickerOpen&&!isSearch);
  if(pickerOpen){
    document.getElementById("yr-label").textContent=y;
    const mg=document.getElementById("month-grid");
    mg.innerHTML="";
    MOIS_C.forEach((mn,i)=>{
      const ms=`${y}-${String(i+1).padStart(2,"0")}`;
      const has=EVENTS.some(e=>e.date.startsWith(ms)||(e.dateFin&&e.dateFin>=ms+"-01"&&e.date<=ms+"-31"));
      const btn=document.createElement("button");
      btn.className="mth-btn"+(i===m?" selected":"")+(has&&i!==m?" has-evt":"");
      btn.textContent=mn;
      if(has&&i!==m){ const dot=document.createElement("span"); dot.className="mth-dot"; btn.appendChild(dot); }
      btn.onclick=()=>{ state.month=i; state.pickerOpen=false; render(); };
      mg.appendChild(btn);
    });
  }

  // Calendar grid
  const cg=document.getElementById("cal-grid");
  if(isSearch){ cg.innerHTML=""; }
  else{
    const total=daysInMonth(y,m), off=startDay(y,m), rows=Math.ceil((off+total)/7);
    let html="";
    for(let r=0;r<rows;r++){
      html+=`<div class="week-row">`;
      for(let c=0;c<7;c++){
        const idx=r*7+c, d=idx-off+1, ok=d>=1&&d<=total;
        const isToday=ok&&y===now.getFullYear()&&m===now.getMonth()&&d===now.getDate();
        const wknd=c>=5;
        html+=`<div class="day-cell">`;
        if(ok){
          html+=`<div class="day-num${isToday?" today":wknd?" weekend":""}">${d}</div>`;
          const de=eventsForDay(y,m,d);
          de.slice(0,2).forEach(e=>{
            const name=e.nom.split("·")[0].replace(" ⚑","").trim();
            html+=`<div class="evt-pill" style="background:${e.color}1a;color:${e.color};border:1px solid ${e.color}33" data-id="${e.id}">
              <div class="evt-dot" style="background:${e.color}"></div>
              <span class="evt-name">${name}</span>
            </div>`;
          });
          if(de.length>2) html+=`<div class="more-lbl" data-id="${de[2].id}">+${de.length-2}</div>`;
        }
        html+=`</div>`;
      }
      html+=`</div>`;
    }
    cg.innerHTML=html;
    cg.querySelectorAll("[data-id]").forEach(el=>{
      el.onclick=e=>{ e.stopPropagation(); openModal(parseInt(el.dataset.id)); };
    });
  }

  // Legend
  const leg=document.getElementById("legend");
  if(isSearch){ leg.innerHTML=""; }
  else{
    leg.innerHTML=Object.entries(CATS).map(([c,col])=>`<div class="leg-item"><div class="leg-dot" style="background:${col}"></div>${c}</div>`).join("")
      +`<span style="font-size:10.5px;color:var(--txt3)">⚑ = date estimée</span>`;
  }

  // Event list
  const list=document.getElementById("evt-list");
  const toShow = isSearch ? getSearchResults() : me;
  if(!isSearch&&toShow.length===0){ list.innerHTML=`<div class="no-result">Pas de tournoi ce mois-ci</div>`; }
  else if(isSearch&&toShow.length===0){ list.innerHTML=`<div class="no-result">Aucun résultat.<br><small>Essayez "jeunes", "gratuit", "17e", "10h"…</small></div>`; }
  else{
    list.innerHTML="";
    if(isSearch){
      const info=document.createElement("div");
      info.style.cssText="padding:8px 14px 4px;font-size:12px;color:var(--txt3)";
      info.textContent=`${toShow.length} résultat${toShow.length!==1?"s":""}${query?` pour "${query}"`:""} ${cat!=="Tous"?`· ${cat}`:""}`;
      list.appendChild(info);
    }
    toShow.forEach(e=>list.appendChild(makeRow(e)));
  }

  // Tab colors
  document.querySelector("#tab-cal .tab-label").style.color=(!isSearch)?"var(--blue)":"var(--txt3)";
  document.querySelector("#tab-search .tab-label").style.color=isSearch?"var(--blue)":"var(--txt3)";

  // Today badge
  document.getElementById("today-badge").textContent=now.getDate();

  // Scroll to top
  document.getElementById("scroll").scrollTop=0;
}

function getSearchResults(){
  const q=state.query.toLowerCase().trim();
  return EVENTS.filter(e=>{
    if(state.cat!=="Tous"&&e.cat!==state.cat) return false;
    if(!q) return true;
    return [e.nom,e.lieu,e.arrdt,e.cat,e.tarif,e.age,e.format,e.metro,
            e.homologation,e.statut,String(e.tarifNum),e.heure,
            e.contact_nom,e.contact_email,e.contact_tel].join(" ").toLowerCase().includes(q);
  }).sort((a,b)=>a.date.localeCompare(b.date));
}

function makeRow(e){
  const div=document.createElement("div");
  div.className="evt-row";
  const d=new Date(e.date+"T00:00:00");
  const dF=e.dateFin?new Date(e.dateFin+"T00:00:00"):null;
  div.innerHTML=`
    <div class="date-block">
      <div class="date-mon">${MOIS_M[d.getMonth()]}</div>
      <div class="date-day">${d.getDate()}</div>
      ${dF&&dF>d?`<div class="date-end">→${dF.getDate()}</div>`:""}
    </div>
    <div class="evt-dot2" style="background:${e.color}"></div>
    <div class="evt-info">
      <div class="evt-time-lbl">🕐 ${e.heure}</div>
      <div class="evt-title">${e.nom.replace(" ⚑","")}</div>
      <div class="evt-loc">📍 ${e.lieu}</div>
      <div class="tags">
        <span class="tag" style="background:${e.color}18;color:${e.color};border:1px solid ${e.color}30">${e.cat}</span>
        <span class="tag" style="background:${e.statut==="confirmé"?"#d1fae5":"#fef9c3"};color:${e.statut==="confirmé"?"#065f46":"#92400e"}">${e.statut==="confirmé"?"✓ Confirmé":"⚑ Estimé"}</span>
        <span class="tag" style="background:var(--bg);color:var(--txt2)">💶 ${e.tarif.split("·")[0].trim()}</span>
      </div>
    </div>
    <div class="arr">›</div>`;
  div.onclick=()=>openModal(e.id);
  return div;
}

function openModal(id){
  const e=EVENTS.find(x=>x.id===id);
  if(!e) return;
  const sheet=document.getElementById("modal-sheet");
  sheet.innerHTML=`
    <div class="modal-handle"></div>
    <div class="modal-header">
      <div style="display:flex;justify-content:space-between;align-items:flex-start;gap:10px">
        <div style="flex:1">
          <div class="modal-badges">
            <span class="tag" style="font-size:11px;padding:2px 9px;background:${e.color}18;color:${e.color};border:1px solid ${e.color}30;border-radius:99px">${e.cat}</span>
            <span class="tag" style="font-size:11px;padding:2px 9px;background:${e.statut==="confirmé"?"#d1fae5":"#fef9c3"};color:${e.statut==="confirmé"?"#065f46":"#92400e"};border-radius:99px">${e.statut==="confirmé"?"✓ Confirmé":"⚑ Date estimée"}</span>
          </div>
          <div class="modal-title">${e.nom.replace(" ⚑","")}</div>
        </div>
        <button class="close-btn" id="modal-close">✕</button>
      </div>
    </div>
    <div class="modal-body">
      <div class="highlight-grid">
        <div class="highlight-box" style="background:#fff5f5;border-color:#fecaca">
          <div class="hl-label">Heure de début</div>
          <div class="hl-val" style="color:var(--red);font-size:15px">🕐 ${e.heure}</div>
        </div>
        <div class="highlight-box" style="background:#f0fdf4;border-color:#bbf7d0">
          <div class="hl-label">Tarif</div>
          <div class="hl-val" style="color:${e.tarifNum===0?"#10b981":e.tarifNum<=18?"#3b82f6":"var(--txt)"};font-size:14px">${e.tarif.split("·")[0].trim()}</div>
        </div>
      </div>
      ${[
        ["📅","Date",e.dateFin&&e.dateFin!==e.date?`${fmtDate(e.date)} → ${fmtDate(e.dateFin)}`:fmtDate(e.date)],
        ["🕐","Horaires complets",e.horaires],
        ["📍","Lieu",e.lieu],
        ["🚇","Métro / Accès",e.metro],
        ["👤","Public",e.age],
        ["🏁","Format",e.format],
        ["✅","Homologation",e.homologation],
        ["✏️","Inscription",e.inscription],
      ].map(([ic,lb,vl])=>`
        <div class="detail-row">
          <span class="detail-icon">${ic}</span>
          <div><div class="detail-label">${lb}</div><div class="detail-val">${vl}</div></div>
        </div>`).join("")}
      <div class="contact-box">
        <div class="contact-title">📞 Contact direct</div>
        <div class="contact-row">
          <div class="contact-row-left">🏛</div>
          <div><div class="contact-label">Organisateur</div><div class="contact-val">${e.contact_nom}</div></div>
        </div>
        ${e.contact_tel?`
        <div class="contact-row">
          <div class="contact-row-left">📱</div>
          <div><div class="contact-label">Téléphone</div><a href="tel:${e.contact_tel.replace(/\s/g,"")}" class="clink">${e.contact_tel}</a></div>
        </div>`:""}
        <div class="contact-row">
          <div class="contact-row-left">✉️</div>
          <div><div class="contact-label">Email</div><a href="mailto:${e.contact_email}" class="clink">${e.contact_email}</a></div>
        </div>
        <div class="contact-row">
          <div class="contact-row-left">🌐</div>
          <div><div class="contact-label">Site</div><a href="${e.lien}" target="_blank" class="clink">${e.contact_site}</a></div>
        </div>
      </div>
      ${e.statut==="estimé"?`<div class="warn-box"><strong>⚑ Date estimée</strong> — Basée sur le calendrier habituel du club. Vérifiez par email avant inscription.</div>`:""}
      <div class="action-row">
        ${e.contact_tel?`<a href="tel:${e.contact_tel.replace(/\s/g,"")}" class="action-btn" style="background:#34c759;color:#fff">📱 Appeler</a>`:""}
        <a href="mailto:${e.contact_email}" class="action-btn" style="background:#007aff;color:#fff">✉️ Email</a>
      </div>
      <a href="${e.lien}" target="_blank" class="site-btn">Voir le site officiel →</a>
    </div>`;
  document.getElementById("modal-overlay").classList.add("open");
  document.getElementById("modal-close").onclick=closeModal;
}
function closeModal(){ document.getElementById("modal-overlay").classList.remove("open"); }

// ─── EVENTS ──────────────────────────────────────────────────────────────────
document.getElementById("btn-prev").onclick=()=>{
  if(state.month===0){state.month=11;state.year--;}else state.month--;
  render();
};
document.getElementById("btn-next").onclick=()=>{
  if(state.month===11){state.month=0;state.year++;}else state.month++;
  render();
};
document.getElementById("month-title-btn").onclick=()=>{ state.pickerOpen=!state.pickerOpen; render(); };
document.getElementById("yr-prev").onclick=()=>{ state.year--; render(); };
document.getElementById("yr-next").onclick=()=>{ state.year++; render(); };

document.getElementById("tab-cal").onclick=()=>{ state.view="cal"; state.query=""; state.cat="Tous"; state.pickerOpen=false; render(); };
document.getElementById("tab-search").onclick=()=>{ state.view="search"; state.pickerOpen=false; render(); setTimeout(()=>document.getElementById("search-input").focus(),100); };
document.getElementById("tab-today").onclick=()=>{ state.month=now.getMonth(); state.year=now.getFullYear(); state.view="cal"; state.pickerOpen=false; render(); };
document.getElementById("tab-install").onclick=()=>{ document.getElementById("app-url").textContent=location.href; document.getElementById("install-modal").classList.add("open"); };

document.getElementById("cancel-search").onclick=()=>{ state.view="cal"; state.query=""; state.cat="Tous"; render(); };
document.getElementById("search-input").oninput=e=>{ state.query=e.target.value; render(); };

document.getElementById("modal-overlay").onclick=e=>{ if(e.target===document.getElementById("modal-overlay")) closeModal(); };

// Cat filters
const catFilters=document.getElementById("cat-filters");
["Tous","Jeunes","Open","Championnat","National","Féminin"].forEach(c=>{
  const btn=document.createElement("button");
  btn.className="cat-btn"; btn.textContent=c;
  btn.onclick=()=>{ state.cat=c; renderCatFilters(); render(); };
  catFilters.appendChild(btn);
});
function renderCatFilters(){
  catFilters.querySelectorAll(".cat-btn").forEach((btn,i)=>{
    const c=btn.textContent, col=CATS[c]||"#1c1c1e";
    const sel=state.cat===c;
    btn.style.background=sel?col:"#e5e5ea";
    btn.style.color=sel?"#fff":"#3c3c43";
    btn.style.borderColor=sel?col:"transparent";
  });
}
renderCatFilters();

// ─── PWA SETUP ───────────────────────────────────────────────────────────────
try {
  const manifest = {
    name:"Tournois Échecs Paris 2026", short_name:"Échecs Paris",
    description:"Calendrier des tournois d'échecs à Paris 2026",
    start_url:"./", display:"standalone", orientation:"portrait",
    background_color:"#ffffff", theme_color:"#ffffff",
    icons:[{src:"data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAxMjAgMTIwIj4KICA8IS0tIEZvbmQgdmVydCBmb25jw6kgc3R5bGUgw6ljaGlxdWllciAtLT4KICA8cmVjdCB3aWR0aD0iMTIwIiBoZWlnaHQ9IjEyMCIgcng9IjI0IiBmaWxsPSIjMWE2YjJlIi8+CiAgPCEtLSBDYXNlcyBkZSBsJ8OpY2hpcXVpZXIgLS0+CiAgPHJlY3QgeD0iMTAiIHk9IjEwIiB3aWR0aD0iMTgiIGhlaWdodD0iMTgiIGZpbGw9IiNmNWRlYjMiIHJ4PSIyIi8+CiAgPHJlY3QgeD0iNDYiIHk9IjEwIiB3aWR0aD0iMTgiIGhlaWdodD0iMTgiIGZpbGw9IiNmNWRlYjMiIHJ4PSIyIi8+CiAgPHJlY3QgeD0iODIiIHk9IjEwIiB3aWR0aD0iMTgiIGhlaWdodD0iMTgiIGZpbGw9IiNmNWRlYjMiIHJ4PSIyIi8+CiAgPHJlY3QgeD0iMjgiIHk9IjI4IiB3aWR0aD0iMTgiIGhlaWdodD0iMTgiIGZpbGw9IiNmNWRlYjMiIHJ4PSIyIi8+CiAgPHJlY3QgeD0iNjQiIHk9IjI4IiB3aWR0aD0iMTgiIGhlaWdodD0iMTgiIGZpbGw9IiNmNWRlYjMiIHJ4PSIyIi8+CiAgPCEtLSBQacOoY2Ugcm9pIGJsYW5jaGUgY2VudHJhbGUgLS0+CiAgPHRleHQgeD0iNjAiIHk9Ijg0IiBmb250LXNpemU9IjYyIiB0ZXh0LWFuY2hvcj0ibWlkZGxlIiBmaWxsPSJ3aGl0ZSIgZm9udC1mYW1pbHk9InNlcmlmIj7imZQ8L3RleHQ+CiAgPCEtLSBUZXh0ZSDDiVAgZW4gYmFzIC0tPgogIDx0ZXh0IHg9IjYwIiB5PSIxMTIiIGZvbnQtc2l6ZT0iMTMiIHRleHQtYW5jaG9yPSJtaWRkbGUiIGZpbGw9IiNmNWRlYjMiIGZvbnQtZmFtaWx5PSJzYW5zLXNlcmlmIiBmb250LXdlaWdodD0iYm9sZCIgbGV0dGVyLXNwYWNpbmc9IjIiPsOJQ0hFQ1M8L3RleHQ+Cjwvc3ZnPgo=",sizes:"512x512",type:"image/svg+xml"}]
  };
  const blob=new Blob([JSON.stringify(manifest)],{type:"application/json"});
  const url=URL.createObjectURL(blob);
  const link=document.createElement("link"); link.rel="manifest"; link.href=url;
  document.head.appendChild(link);
} catch(err){}

// Service Worker
if('serviceWorker' in navigator && location.protocol==='https:'){
  const sw=`
    const V='echecs-paris-v1';
    self.addEventListener('install',e=>{ self.skipWaiting(); e.waitUntil(caches.open(V).then(c=>c.add('/'))); });
    self.addEventListener('activate',e=>e.waitUntil(clients.claim()));
    self.addEventListener('fetch',e=>e.respondWith(caches.match(e.request).then(r=>r||fetch(e.request).catch(()=>caches.match('/')))));
  `;
  try {
    const blob=new Blob([sw],{type:'application/javascript'});
    navigator.serviceWorker.register(URL.createObjectURL(blob));
  } catch(e){}
}

// ─── INIT ─────────────────────────────────────────────────────────────────────
render();
</script>
</body>
</html>
