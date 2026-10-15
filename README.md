<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<title>Présence – Politiques Commerciales Internationales (Pr. Raouf Radouane)</title>
<script src="https://cdnjs.cloudflare.com/ajax/libs/qrcodejs/1.0.0/qrcode.min.js"></script>
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
<style>
:root {
  --bg: #f8fafc;
  --card: #ffffff;
  --ink: #0f172a;
  --mut: #64748b;
  --line: #e2e8f0;
  --nav: #0b192c;
  --btn: #2563eb;
  --btn-hover: #1d4ed8;
  --btnink: #ffffff;
  --ok: #10b981;
  --bad: #ef4444;
  --warn: #f59e0b;
  --bar: #3b82f6;
  --radius: 10px;
  --shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.05), 0 2px 4px -1px rgba(0, 0, 0, 0.03);
}

@media (prefers-color-scheme: dark) {
  :root:not([data-theme="light"]) {
    --bg: #0f172a;
    --card: #1e293b;
    --ink: #f8fafc;
    --mut: #94a3b8;
    --line: #334155;
    --nav: #020617;
    --ok: #34d399;
    --bad: #f87171;
    --warn: #fbbf24;
    --bar: #60a5fa;
  }
}

* { box-sizing: border-box; }
body {
  margin: 0;
  background: var(--bg);
  color: var(--ink);
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
  line-height: 1.5;
  padding-bottom: 40px;
}

header {
  background: var(--nav);
  color: #fff;
  padding: 16px 24px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 12px;
  flex-wrap: wrap;
  box-shadow: var(--shadow);
  border-bottom: 1px solid #1e3a8a;
}
header b { font-size: 1.1rem; letter-spacing: -0.01em; }
header small { display: block; opacity: 0.85; font-size: 0.82rem; margin-top: 2px; color: #93c5fd; }

main { max-width: 1000px; margin: 0 auto; padding: 24px 16px; }

h1 { font-size: 1.5rem; margin: 0 0 4px; font-weight: 700; letter-spacing: -0.02em; }
h2 { font-size: 1.15rem; margin: 0 0 12px; font-weight: 600; }
p.sub { color: var(--mut); margin: 0 0 20px; font-size: 0.95rem; }

.bar {
  display: flex;
  gap: 12px;
  flex-wrap: wrap;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 20px;
}

button, .btn {
  font: inherit;
  cursor: pointer;
  border: 0;
  border-radius: 8px;
  padding: 9px 16px;
  background: var(--btn);
  color: var(--btnink);
  font-weight: 600;
  font-size: 0.9rem;
  transition: all 0.15s ease;
  display: inline-flex;
  align-items: center;
  justify-content: center;
  gap: 6px;
}
button:hover { background: var(--btn-hover); }
button.ghost { background: transparent; color: var(--ink); border: 1px solid var(--line); }
button.ghost:hover { background: var(--line); }
button.danger { background: transparent; color: var(--bad); padding: 4px 8px; font-weight: 500; }
button.danger:hover { background: rgba(239, 68, 68, 0.1); }
button.sm { padding: 5px 10px; font-size: 0.82rem; }

button:focus-visible, input:focus-visible, textarea:focus-visible {
  outline: 2px solid var(--btn);
  outline-offset: 2px;
}

.card {
  background: var(--card);
  border: 1px solid var(--line);
  border-radius: var(--radius);
  padding: 20px;
  margin-bottom: 20px;
  box-shadow: var(--shadow);
}

.live {
  display: grid;
  grid-template-columns: auto 1fr;
  gap: 24px;
  align-items: center;
}
@media(max-width: 600px) { .live { grid-template-columns: 1fr; justify-items: center; text-align: center; } }

#qr {
  background: #fff;
  padding: 16px;
  border-radius: var(--radius);
  border: 1px solid var(--line);
  display: flex;
  justify-content: center;
  align-items: center;
  min-width: 212px;
  min-height: 212px;
}

.big { font-size: 2.2rem; font-weight: 800; line-height: 1; }
.link { font-size: 0.85rem; color: var(--mut); margin: 10px 0; }
.scroll { overflow-x: auto; margin-top: 10px; }

table { width: 100%; border-collapse: collapse; min-width: 580px; font-size: 0.92rem; }
th, td { text-align: left; padding: 10px 12px; border-bottom: 1px solid var(--line); }
th { color: var(--mut); font-weight: 600; font-size: 0.82rem; text-transform: uppercase; letter-spacing: 0.05em; }
tr:last-child td { border-bottom: none; }

.rate-container { display: flex; align-items: center; gap: 8px; }
.rate-bg { background: var(--line); width: 80px; height: 7px; border-radius: 4px; overflow: hidden; }
.rate-fill { height: 100%; background: var(--bar); border-radius: 4px; }
.low { color: var(--bad); font-weight: 600; }

.row { display: grid; grid-template-columns: 160px 1fr 60px; gap: 12px; align-items: center; margin: 6px 0; font-size: 0.9rem; }
.track { background: var(--line); border-radius: 4px; height: 10px; overflow: hidden; }
.track i { display: block; height: 100%; border-radius: 4px; background: var(--bar); }

input, textarea {
  font: inherit;
  width: 100%;
  padding: 10px 12px;
  border: 1px solid var(--line);
  border-radius: 8px;
  background: var(--bg);
  color: var(--ink);
  transition: border-color 0.15s;
}

dialog {
  border: 1px solid var(--line);
  border-radius: var(--radius);
  background: var(--card);
  color: var(--ink);
  width: min(500px, 92vw);
  padding: 24px;
  box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.2);
}
dialog::backdrop { background: rgba(0, 0, 0, 0.5); backdrop-filter: blur(2px); }

.msg { margin-top: 14px; padding: 12px 16px; border-radius: 8px; font-weight: 500; font-size: 0.9rem; }
.msg.ok { background: rgba(16, 185, 129, 0.15); color: var(--ok); border: 1px solid rgba(16, 185, 129, 0.3); }
.msg.err { background: rgba(239, 68, 68, 0.15); color: var(--bad); border: 1px solid rgba(239, 68, 68, 0.3); }

.empty { color: var(--mut); padding: 16px 0; text-align: center; font-size: 0.9rem; }
.note { font-size: 0.85rem; color: var(--mut); margin-top: 8px; }
.narrow { max-width: 440px; margin: 40px auto; }

#toast {
  position: fixed;
  left: 50%;
  bottom: 24px;
  transform: translateX(-50%);
  background: var(--nav);
  color: #fff;
  padding: 10px 20px;
  border-radius: 30px;
  font-size: 0.88rem;
  box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.3);
  display: none;
  z-index: 99;
}

.stats { display: grid; grid-template-columns: repeat(auto-fit, minmax(130px, 1fr)); gap: 12px; margin-bottom: 20px; }
.stat { background: var(--card); border: 1px solid var(--line); border-radius: var(--radius); padding: 16px; box-shadow: var(--shadow); }
.stat b { display: block; font-size: 1.8rem; line-height: 1.1; font-weight: 700; }
.stat span { color: var(--mut); font-size: 0.82rem; font-weight: 500; }

details { border-bottom: 1px solid var(--line); padding: 8px 0; }
summary { cursor: pointer; list-style: none; font-weight: 500; }
summary::-webkit-details-marker { display: none; }
.abs { color: var(--mut); font-size: 0.88rem; padding: 10px 0 6px; line-height: 1.6; }

.links-box {
  background: #f1f5f9;
  border: 1px solid var(--line);
  border-radius: var(--radius);
  padding: 16px;
  margin-bottom: 20px;
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 16px;
}
@media(max-width: 768px) { .links-box { grid-template-columns: 1fr; } }
</style>
</head>
<body>
<header>
  <div>
    <b>UM5 Souissi · Master CI : Politiques Commerciales Internationales</b>
    <small>Pr. Raouf Radouane · Suivi de présence sécurisé (Version Finale)</small>
  </div>
  <span id="mode" class="note" style="color:#fff;opacity:.8;margin:0"></span>
</header>
<main id="app"></main>

<dialog id="dlg">
  <h2>Ajouter des étudiants</h2>
  <p class="note" style="margin:0 0 12px">Format : <b>Nom Prénom; Code Apogée</b> (une ligne par étudiant).</p>
  <textarea id="bulk" rows="6" placeholder="Abdelkarim Oubbahma; 25024052&#10;Imane Bouihi; 25023986"></textarea>
  <div style="display:flex;gap:10px;justify-content:flex-end;margin-top:16px">
    <button class="ghost" id="cancel">Annuler</button>
    <button id="saveStu">Ajouter</button>
  </div>
</dialog>

<dialog id="cfmDlg">
  <p id="cfmTxt" style="margin:0 0 18px;font-size:1rem;"></p>
  <div style="display:flex;gap:10px;justify-content:flex-end">
    <button class="ghost" id="cfmNo">Annuler</button>
    <button id="cfmYes">Confirmer</button>
  </div>
</dialog>

<dialog id="edDlg">
  <h2>Modifier l'étudiant</h2>
  <label for="edNom" style="font-size:.85rem;font-weight:600">Nom et prénom</label>
  <input id="edNom" style="margin:6px 0 12px">
  <label for="edNum" style="font-size:.85rem;font-weight:600">Code Apogée</label>
  <input id="edNum" style="margin:6px 0 16px">
  <div style="display:flex;gap:10px;justify-content:flex-end">
    <button class="ghost" id="edNo">Annuler</button>
    <button id="edYes">Enregistrer</button>
  </div>
</dialog>

<div id="toast" role="status"></div>

<script>
const defaultStudents = [
  { id: "s1", name: "Abdelkarim Oubbahma", num: "25024052" },
  { id: "s2", name: "Imane Bouihi", num: "25023986" },
  { id: "s3", name: "Ghita Azmi", num: "25024043" },
  { id: "s4", name: "Fatima Ezahra El Kamel", num: "25024909" },
  { id: "s5", name: "Oumaima Bouaicha", num: "25023736" },
  { id: "s6", name: "Fatimaezzahra Laayati", num: "25023904" },
  { id: "s7", name: "Youssef Achari", num: "25023957" },
  { id: "s8", name: "Salma Mokhtari", num: "25023421" },
  { id: "s9", name: "Boutaina Elbakkar", num: "K131333491" },
  { id: "s10", name: "Othmane Elaouji", num: "25023962" },
  { id: "s11", name: "Douaa Doubir", num: "25023971" },
  { id: "s12", name: "Zineb El Idrissi", num: "22011649" },
  { id: "s13", name: "Wiam Labyed", num: "24022012" },
  { id: "s14", name: "Kaoutar El Idrissi", num: "22011651" },
  { id: "s15", name: "Khalil Tazi Hnyine", num: "25023954" },
  { id: "s16", name: "Hiba Ahejrir", num: "25023166" },
  { id: "s17", name: "Azize Ait Richat", num: "25024034" },
  { id: "s18", name: "Nouhaila Gounaine", num: "25024048" },
  { id: "s19", name: "Kanza Korchi", num: "25023426" },
  { id: "s20", name: "Rania Sedjari", num: "25023572" },
  { id: "s21", name: "Walid Er-Rahali", num: "25023917" },
  { id: "s22", name: "Karitia Fatima Ange Soro", num: "25023876" },
  { id: "s23", name: "Kaoutar Nachet", num: "25023981" },
  { id: "s24", name: "Nidal Rejim", num: "25023978" },
  { id: "s25", name: "Bassma Ben Daia", num: "25027593" },
  { id: "s26", name: "Aya Bkare", num: "25023743" },
  { id: "s27", name: "Ouissal El-ghazi", num: "23027875" },
  { id: "s28", name: "Hafsa El Ansari", num: "25023408" },
  { id: "s29", name: "Hanane Abouelmaali", num: "25027587" },
  { id: "s30", name: "Anass Aouraghe", num: "25024030" },
  { id: "s31", name: "Khadija El Hiti", num: "25029999" },
  { id: "s32", name: "Fadwa Tamzaiti", num: "25023982" },
  { id: "s33", name: "Khawla Zin El Alaoui", num: "25024035" },
  { id: "s34", name: "Salma Semlali", num: "25024001" },
  { id: "s35", name: "Hadil Lamghairbat", num: "22018588" },
  { id: "s36", name: "Yassine Addioual", num: "25024023" },
  { id: "s37", name: "Imane Kadda", num: "25023914" },
  { id: "s38", name: "Meryem Boubakari", num: "25023411" },
  { id: "s39", name: "Salma Bouasila", num: "25023958" },
  { id: "s40", name: "Firdaws Akhatas", num: "25023559" }
];

const defaultSessions = [
  { id: "x1", title: "Séance du 24/09/2026", ts: 1758672000000, open: false, tok: "t1" },
  { id: "x2", title: "Séance du 01/06/2026", ts: 1779840000000, open: false, tok: "t2" },
  { id: "x3", title: "Séance du 08/10/2026", ts: 1760035200000, open: false, tok: "t3" }
];

const defaultAtt = [
  ...["25024052", "25023986", "25024043", "25024001", "25023876", "25027593", "25029999", "25023736", "25023971", "25023421", "25023917", "25024023", "24022012", "K131333491", "25024030", "23027875", "25023743"].map(num => {
    const st = defaultStudents.find(s => s.num === num);
    return st ? { id: "x1_" + st.id, sid: "x1", stid: st.id, ts: 1758672000000 } : null;
  }).filter(Boolean),
  ...["25024052", "25023982", "25023411", "25023426", "25023743", "23027875", "22011649", "25023421", "25023978", "25023971", "22018588", "25023917", "25024023", "25023954", "25023957", "25023408", "25024909", "25023958", "25029999", "25023914", "25023981", "25023572", "24022012", "25023876", "K131333491", "25024035", "25023986", "25024043"].map(num => {
    const st = defaultStudents.find(s => s.num === num);
    return st ? { id: "x2_" + st.id, sid: "x2", stid: st.id, ts: 1779840000000 } : null;
  }).filter(Boolean),
  ...["25024052", "25029999", "25024030", "25023954", "25023978", "25023904", "25023957", "25024909", "25023971", "25023421", "25023917", "25024023", "25023914", "25023958", "25027593", "25027587", "22011649", "22011651", "25024048", "25023981", "25023572", "24022012", "25023876", "K131333491", "25023426", "25024035", "25023986", "25024043", "25024001"].map(num => {
    const st = defaultStudents.find(s => s.num === num);
    return st ? { id: "x3_" + st.id, sid: "x3", stid: st.id, ts: 1760035200000 } : null;
  }).filter(Boolean)
];

let db=null, user=null, S=[], X=[], A=[], unsub=[];
const LS='pci_presence_v6', $=s=>document.querySelector(s);
const esc=s=>String(s||'').replace(/[&<>"']/g,c=>({'&':'&amp;','<':'&lt;','>':'&gt;','"':'&quot;',"'":'&#39;'}[c]));
const uid=()=>Math.random().toString(36).slice(2,10);
const arr=c=>c==='students'?S:c==='sessions'?X:A;

function toast(t){
  const e=$('#toast'); e.textContent=t; e.style.display='block';
  clearTimeout(toast.t); toast.t=setTimeout(()=>e.style.display='none',3200);
}

function saveLocal(){ try{localStorage.setItem(LS,JSON.stringify({S,X,A}))}catch(e){} }
function loadLocal(){ 
  try{
    const d=JSON.parse(localStorage.getItem(LS));
    if(d&&d.S&&d.S.length){S=d.S||[];X=d.X||[];A=d.A||[]}
    else { S=defaultStudents; X=defaultSessions; A=defaultAtt; saveLocal(); }
  }catch(e){ S=defaultStudents; X=defaultSessions; A=defaultAtt; } 
}

async function put(c,id,data){
  if(db){
    try{ await db.collection(c).doc(id).set(data); }
    catch(e){ toast('Écriture refusée : '+(e.message||e.code)); throw e; }
  } else {
    const a=arr(c), i=a.findIndex(r=>r.id===id), r={id,...data};
    i<0?a.push(r):a[i]=r; saveLocal(); render();
  }
}

async function rm(c,id){
  if(db){
    try{ await db.collection(c).doc(id).delete(); }
    catch(e){ toast('Suppression refusée'); }
  } else {
    const a=arr(c), i=a.findIndex(r=>r.id===id);
    if(i>=0) a.splice(i,1); saveLocal(); render();
  }
}

function sub(c,set){ unsub.push(db.collection(c).onSnapshot(s=>{set(s.docs.map(d=>({id:d.id,...d.data()})));render()},()=>{})) }

async function init(){
  try{ if(window.claude){ user=await claude.use('user'); db=await claude.use('db'); } }catch(e){}
  if(db){ sub('students',v=>S=v); sub('sessions',v=>X=v); sub('att',v=>A=v); } else loadLocal();
  $('#mode').textContent=db?'Stockage Cloud':'Stockage Local sécurisé';
  render();
}

const isProf=()=>user?user.isOwner():true;

const getBaseUrl=() => {
  let b = window.location.origin + window.location.pathname;
  if(b.startsWith('http://')) b = b.replace('http://', 'https://');
  return b;
};

const sessLink=(id,t)=>getBaseUrl() + '#s=' + id + (t ? '&t=' + t : '');
const orgLink=()=>getBaseUrl() + '?role=teacher';
const stuLink=()=>getBaseUrl() + '?role=student';
const sorted=()=>[...X].sort((a,b)=>a.ts-b.ts);
const fmt=t=>new Date(t).toLocaleString('fr-FR',{weekday:'short',day:'2-digit',month:'short',hour:'2-digit',minute:'2-digit'});
const presentIn=sid=>A.filter(a=>a.sid===sid);

addEventListener('hashchange',render);

function render(){
  if(BIG){
    const o=X.find(x=>x.open);
    if(o){
      BIG.q.innerHTML='';
      try{ new QRCode(BIG.q,{text:sessLink(o.id,o.tok),width:BIG.sz,height:BIG.sz,colorDark:'#000',colorLight:'#fff',correctLevel:QRCode.CorrectLevel.L}); }catch(e){}
    } else { BIG.d.remove(); BIG=null; }
  }
  const h=location.hash.match(/^#s=(\w+)/);
  if(h) return renderCheckin(h[1]);
  const urlParams = new URLSearchParams(location.search);
  if(urlParams.get('role')==='student'||!isProf()){
    renderStudentPortal();
    return;
  }
  renderDash();
}

function renderStudentPortal(){
  const ss=sorted(), open=ss.find(x=>x.open);
  let body='';
  if(!open){
    body='<p class="msg err" style="text-align:center">Aucune séance active pour le moment. Attendez que l\'enseignant ouvre une session.</p>';
  } else {
    body=`
      <p class="sub" style="text-align:center">Séance : <b>${esc(open.title)}</b></p>
      <label for="nom" style="font-size:.85rem;font-weight:600">Nom et Prénom</label>
      <input id="nom" autocomplete="name" placeholder="Ex : Abdelkarim Oubbahma" style="margin:6px 0 14px">
      <label for="num" style="font-size:.85rem;font-weight:600">Code Apogée</label>
      <input id="num" data-sid="${esc(open.id)}" autocomplete="off" placeholder="Ex : 25024052" style="margin:6px 0 14px">
      <label for="scode" style="font-size:.85rem;font-weight:600">Code de séance (4 chiffres affiché au tableau)</label>
      <input id="scode" maxlength="4" autocomplete="off" placeholder="Ex : 4829" style="margin:6px 0 18px;text-align:center;font-weight:bold;letter-spacing:4px;font-family:monospace">
      <button id="go" style="width:100%">Signer ma présence</button>
      <div id="res" role="status"></div>`;
  }
  $('#app').innerHTML=`<div class="card narrow"><h1>Portail Étudiant · Émargement</h1><p class="sub" style="text-align:center">Master CI · Politiques Commerciales Internationales</p>${body}</div>`;
  const go=$('#go'); if(go) go.onclick=checkin;
}

let Q='';
const norm=s=>s.normalize('NFD').replace(/[\u0300-\u036f]/g,'').toLowerCase().replace(/[^a-z0-9 ]/g,' ').split(/\s+/).filter(Boolean);

async function checkin(){
  const numInput = $('#num');
  const nomInput = $('#nom');
  const scodeInput = $('#scode');
  if(!numInput || !nomInput || !scodeInput) return;

  const sid=numInput.dataset.sid, n=numInput.value.trim().toLowerCase(), codeInput=scodeInput.value.trim(), r=$('#res');
  const ss0=X.find(x=>x.id===sid), tk=(location.hash.match(/t=(\w+)/)||[])[1];
  
  if(!ss0||!ss0.open){ r.className='msg err'; r.textContent='Cette séance est clôturée.'; return; }
  if(codeInput!==ss0.code){ r.className='msg err'; r.textContent='Code de séance à 4 chiffres incorrect.'; return; }
  if(!tk||(tk!==ss0.tok&&tk!==ss0.prev)){ r.className='msg err'; r.textContent='QR Code expiré (Rotation 2 min). Veuillez scanner le QR Code actif affiché au tableau.'; return; }
  
  const st=S.find(x=>x.num.toLowerCase()===n);
  if(!st){ r.className='msg err'; r.textContent="Code Apogée inconnu dans la liste de la classe."; return; }
  const nt=norm(nomInput.value);
  if(nt.join('').length<3||!nt.every(t=>norm(st.name).join('').includes(t))){
    r.className='msg err'; r.textContent='Le nom ne correspond pas à ce code Apogée.'; return; }
  try {
    await put('att',sid+'_'+st.id,{sid,stid:st.id,ts:Date.now()});
    r.className='msg ok'; r.textContent='✔ Présence validée avec succès pour '+st.name+'.';
  } catch(e) {
    r.className='msg err'; r.textContent="Impossible d'enregistrer la présence.";
  }
}

function renderDash(){
  const ss=sorted(), open=ss.find(x=>x.open), N=ss.length;
  const cnt=id=>A.filter(a=>a.stid===id&&ss.some(x=>x.id===a.sid)).length;
  const rate=id=>N?Math.round(100*cnt(id)/N):0;
  const stu=[...S].sort((a,b)=>a.name.localeCompare(b.name,'fr'));
  
  let live='';
  if(open){
    const p=presentIn(open.id).length;
    live=`
    <div class="card" style="border: 2px solid var(--btn);">
      <h2>Séance en cours · ${esc(open.title)}</h2>
      <div class="live">
        <div id="qr"></div>
        <div>
          <div class="big">${p} <span style="font-size:1.1rem;font-weight:400;color:var(--mut)">/ ${S.length} présents</span></div>
          <div class="link">Code de sécurité à 4 chiffres : <b style="font-size:1.3rem;color:var(--btn);font-family:monospace">${esc(open.code)}</b></div>
          <div class="link" style="color:var(--warn);font-weight:600;"><i class="fa-solid fa-clock"></i> Prochain changement QR dans <b id="cd">120</b>s</div>
          <div style="display:flex;gap:8px;flex-wrap:wrap;margin-top:12px">
            <button id="full"><i class="fa-solid fa-expand"></i> Afficher QR Géant</button>
            <button class="ghost" id="rotNow"><i class="fa-solid fa-rotate"></i> Changer maintenant</button>
            <button class="ghost" id="copyStu"><i class="fa-solid fa-copy"></i> Copier Lien</button>
            <button id="close" style="background:var(--bad)">Clôturer la séance</button>
          </div>
        </div>
      </div>
    </div>`;
  }

  const rows=stu.filter(s=>!Q.trim()||(s.name+' '+s.num).toLowerCase().includes(Q.trim().toLowerCase())).map(s=>{
    const r=rate(s.id);
    return `<tr>
      <td><b>${esc(s.name)}</b></td>
      <td><code>${esc(s.num)}</code></td>
      <td>${cnt(s.id)} / ${N}</td>
      <td class="${r<50&&N?'low':''}">
        <div class="rate-container">
          <div class="rate-bg"><div class="rate-fill" style="width:${r}%"></div></div>
          <span>${r}%</span>
        </div>
      </td>
      <td style="text-align:right">
        <button class="ghost sm" data-toggle="${s.id}">+ Présent</button>
        <button class="ghost sm" data-edit="${s.id}">Éditer</button>
        <button class="danger" data-del="${s.id}">Retirer</button>
      </td>
    </tr>`;
  }).join('');

  const bars=[...ss].reverse().map(x=>{
    const pr=new Set(presentIn(x.id).map(a=>a.stid)), p=pr.size, r=S.length?Math.round(100*p/S.length):0, ab=stu.filter(s=>!pr.has(s.id));
    return `<details>
      <summary>
        <div class="row">
          <span>${esc(fmt(x.ts))}</span>
          <div class="track"><i style="width:${r}%"></i></div>
          <span><b>${p}</b> / ${S.length}</span>
        </div>
      </summary>
      <div class="abs">
        <b>Absents (${ab.length}) :</b> ${ab.length?ab.map(s=>esc(s.name)).join(', '):'Aucun (Classe complète)'}
        <div style="margin-top:10px">
          <button class="danger sm" data-delsess="${x.id}">Supprimer cette séance</button>
        </div>
      </div>
    </details>`;
  }).join('');

  const low=N?stu.filter(s=>rate(s.id)<50):[];
  const avg=N&&S.length?Math.round(100*A.filter(a=>ss.some(x=>x.id===a.sid)).length/(N*S.length)):0;

  const stats=`
  <div class="stats">
    <div class="stat"><b>${S.length}</b><span>Étudiants</span></div>
    <div class="stat"><b>${N}</b><span>Séances</span></div>
    <div class="stat"><b>${avg}%</b><span>Taux moyen</span></div>
    <div class="stat"><b style="${low.length?'color:var(--bad)':''}">${low.length}</b><span>Sous 50%</span></div>
  </div>`;

  const linksBox=`
  <div class="links-box">
    <div>
      <label style="font-size:0.75rem;font-weight:700;color:var(--mut);text-transform:uppercase">Lien Organisateur (Enseignant)</label>
      <div style="display:flex;gap:6px;margin-top:4px">
        <input type="text" readonly value="${esc(orgLink())}" style="font-size:0.8rem;background:#fff">
        <button class="ghost sm" onclick="navigator.clipboard.writeText('${esc(orgLink())}');toast('Lien organisateur copié !')"><i class="fa-solid fa-copy"></i></button>
        <button class="sm" style="background:#25d366" onclick="window.open('https://api.whatsapp.com/send?text=' + encodeURIComponent('Lien Organisateur PCI : ${esc(orgLink())}'))"><i class="fa-brands fa-whatsapp"></i></button>
      </div>
    </div>
    <div>
      <label style="font-size:0.75rem;font-weight:700;color:var(--mut);text-transform:uppercase">Lien Étudiants (Émargement)</label>
      <div style="display:flex;gap:6px;margin-top:4px">
        <input type="text" readonly value="${esc(stuLink())}" style="font-size:0.8rem;background:#fff">
        <button class="ghost sm" onclick="navigator.clipboard.writeText('${esc(stuLink())}');toast('Lien étudiants copié !')"><i class="fa-solid fa-copy"></i></button>
        <button class="sm" style="background:#25d366" onclick="window.open('https://api.whatsapp.com/send?text=' + encodeURIComponent('Veuillez signer votre présence au cours de PCI via ce lien sécurisé : ${esc(stuLink())}'))"><i class="fa-brands fa-whatsapp"></i></button>
      </div>
    </div>
  </div>`;

  $('#app').innerHTML=`
  <div class="bar">
    <div><h1>Tableau de bord</h1><p class="sub">Module : Politiques Commerciales Internationales · Pr. Raouf Radouane</p></div>
    <div style="display:flex;gap:8px;flex-wrap:wrap">
      <button class="ghost" id="delLastSes" style="border-color:var(--bad);color:var(--bad)"><i class="fa-solid fa-trash-can"></i> Supprimer dernière séance</button>
      <button id="open"><i class="fa-solid fa-circle-play"></i> Ouvrir une séance</button>
    </div>
  </div>
  ${linksBox}
  ${stats}
  ${live}
  <div class="card">
    <div class="bar" style="margin-bottom:12px">
      <h2>Liste des étudiants (${S.length})</h2>
      <div style="display:flex;gap:8px">
        <button class="ghost" id="csv">Exporter CSV</button>
        <button id="add">Ajouter des étudiants</button>
      </div>
    </div>
    <input id="q" type="search" placeholder="Rechercher par nom ou code Apogée..." value="${esc(Q)}" style="margin-bottom:12px">
    ${S.length?`<div class="scroll"><table><thead><tr><th>Nom</th><th>Apogée</th><th>Présences</th><th>Assiduité</th><th style="text-align:right">Actions</th></tr></thead><tbody>${rows}</tbody></table></div>`:'<p class="empty">Aucun étudiant enregistré.</p>'}
  </div>
  <div class="card">
    <h2>Historique des séances</h2>
    ${N?bars:'<p class="empty">Aucune séance dans l\'historique.</p>'}
  </div>`;

  const openBtn = $('#open'); if(openBtn) openBtn.onclick=async()=>{ if(open&&!(await cfm('Une séance est déjà en cours. Voulez-vous la clôturer et en ouvrir une nouvelle ?')))return; newSession(); };
  const delLastBtn = $('#delLastSes'); if(delLastBtn) delLastBtn.onclick=async()=>{
    if(!ss.length){ toast('Aucune séance à supprimer.'); return; }
    if(await cfm('Voulez-vous vraiment supprimer la dernière séance enregistrée ?')){
      const last=ss[ss.length-1];
      for(const a of A.filter(a=>a.sid===last.id)) await rm('att',a.id);
      await rm('sessions',last.id);
      toast('Dernière séance supprimée.');
    }
  };
  const addBtn = $('#add'); if(addBtn) addBtn.onclick=()=>{$('#bulk').value='';$('#dlg').showModal();};
  const csvBtn = $('#csv'); if(csvBtn) csvBtn.onclick=exportCsv;
  const qInput = $('#q'); if(qInput) qInput.oninput=e=>{ Q=e.target.value; render(); const i=$('#q'); i.focus(); i.setSelectionRange(i.value.length,i.value.length); };

  document.querySelectorAll('[data-del]').forEach(b=>b.onclick=async()=>{ if(await cfm('Retirer cet étudiant de la liste ?')) rm('students',b.dataset.del); });
  document.querySelectorAll('[data-delsess]').forEach(b=>b.onclick=async()=>{
    if(await cfm('Supprimer définitivement cette séance et son historique ?')){
      const id=b.dataset.delsess;
      for(const a of A.filter(a=>a.sid===id)) await rm('att',a.id);
      await rm('sessions',id);
    }
  });

  document.querySelectorAll('[data-toggle]').forEach(b=>b.onclick=async()=>{
    if(!open){ toast('Ouvrez une séance pour marquer une présence manuelle.'); return; }
    const stid=b.dataset.toggle;
    await put('att',open.id+'_'+stid,{sid:open.id,stid,ts:Date.now()});
    toast('Présence ajoutée manuellement');
  });

  document.querySelectorAll('[data-edit]').forEach(b=>b.onclick=()=>{
    const s=S.find(x=>x.id===b.dataset.edit);
    $('#edNom').value=s.name; $('#edNum').value=s.num;
    $('#edDlg').showModal();
    $('#edNo').onclick=()=>$('#edDlg').close();
    $('#edYes').onclick=async()=>{
      const nm=$('#edNom').value.trim(), nu=$('#edNum').value.trim();
      if(!nm||!nu){ toast('Remplissez les deux champs'); return; }
      await put('students',s.id,{name:nm,num:nu});
      $('#edDlg').close();
    };
  });

  if(open){
    try{ new QRCode($('#qr'),{text:sessLink(open.id,open.tok),width:180,height:180,colorDark:'#000',colorLight:'#fff',correctLevel:QRCode.CorrectLevel.L}); }catch(e){}
    const fullBtn = $('#full'); if(fullBtn) fullBtn.onclick=()=>bigQR(open);
    const rotBtn = $('#rotNow'); if(rotBtn) rotBtn.onclick=()=>rotate(open);
    const copyStuBtn = $('#copyStu'); if(copyStuBtn) copyStuBtn.onclick=()=>{
      navigator.clipboard.writeText(sessLink(open.id,open.tok)).then(()=>toast('Lien de présence copié')).catch(()=>toast('Erreur de copie'));
    };
    const closeBtn = $('#close'); if(closeBtn) closeBtn.onclick=()=>put('sessions',open.id,{title:open.title,ts:open.ts,code:open.code,open:false,tok:open.tok});
  }
}

function cfm(msg){
  return new Promise(res=>{
    $('#cfmTxt').textContent=msg;
    const d=$('#cfmDlg'); d.showModal();
    $('#cfmNo').onclick=()=>{d.close();res(false)};
    $('#cfmYes').onclick=()=>{d.close();res(true)};
  });
}

function bigQR(o){
  const d=document.createElement('div');
  d.style.cssText='position:fixed;inset:0;background:#fff;color:#000;z-index:999;display:flex;flex-direction:column;align-items:center;justify-content:center;gap:20px;padding:20px;text-align:center;cursor:pointer';
  const q=document.createElement('div'); d.appendChild(q);
  const sz=Math.floor(Math.min(innerWidth,innerHeight)*0.7);
  try{ new QRCode(q,{text:sessLink(o.id,o.tok),width:sz,height:sz,colorDark:'#000',colorLight:'#fff',correctLevel:QRCode.CorrectLevel.L}); }catch(e){}
  const t=document.createElement('div');
  t.innerHTML=`<b style="font-size:1.8rem;display:block;margin-bottom:8px">Code de séance : <span style="color:var(--btn);font-family:monospace">${esc(o.code)}</span></b><span style="font-size:1.1rem;color:#666">QR Code dynamique (Rotation 2 min) · Cliquez n'importe où pour fermer</span>`;
  d.appendChild(t);
  d.onclick=()=>{d.remove();BIG=null};
  document.body.appendChild(d);
  BIG={d,q,sz};
}

let BIG=null, NEXT=Date.now()+120000;
const rtok=()=>Math.random().toString(36).slice(2,8);

async function rotate(o){
  NEXT=Date.now()+120000;
  await put('sessions',o.id,{title:o.title,ts:o.ts,code:o.code,open:true,tok:rtok(),prev:o.tok||''});
}

function tick(){
  const o=X.find(x=>x.open); 
  if(!o||!isProf()||new URLSearchParams(location.search).get('role')==='student'||/^#s=/.test(location.hash)) return;
  const cd=$('#cd'); if(cd) cd.textContent=Math.max(0,Math.ceil((NEXT-Date.now())/1000));
  if(Date.now()>=NEXT){ rotate(o); }
}
setInterval(tick,1000);

async function newSession(){
  for(const x of X.filter(x=>x.open)) await put('sessions',x.id,{title:x.title,ts:x.ts,code:x.code,open:false,tok:x.tok});
  const ts=Date.now(); NEXT=Date.now()+120000;
  const randCode=Math.floor(1000 + Math.random() * 9000).toString();
  await put('sessions',uid(),{title:'Séance du '+fmt(ts),ts,code:randCode,open:true,tok:rtok(),prev:''});
}

const cancelBtn = $('#cancel'); if(cancelBtn) cancelBtn.onclick=()=>$('#dlg').close();
const saveStuBtn = $('#saveStu'); if(saveStuBtn) saveStuBtn.onclick=async()=>{
  const lines=$('#bulk').value.split('\n').map(l=>l.trim()).filter(Boolean);
  let n=0, bad=0;
  for(const l of lines){
    const p=l.split(/[;\t,]/).map(x=>x.trim());
    if(p.length<2||!p[0]||!p[1]||S.some(s=>s.num.toLowerCase()===p[1].toLowerCase())){ bad++; continue; }
    await put('students',uid(),{name:p[0],num:p[1]}); n++;
  }
  $('#dlg').close();
  toast(n+' étudiant(s) ajouté(s)'+(bad?' ('+bad+' ligne(s) ignorée(s))':''));
};

async function exportCsv(){
  const ss=sorted(), has=new Set(A.map(a=>a.sid+'_'+a.stid));
  const head=['Nom','Code Apogée',...ss.map(x=>fmt(x.ts))];
  const q=v=>'"'+String(v).replace(/"/g,'""')+'"';
  const lines=[head.map(q).join(';'),...S.map(s=>[s.name,s.num,...ss.map(x=>has.has(x.id+'_'+s.id)?'Présent':'Absent')].map(q).join(';'))];
  const csvContent='\ufeff'+lines.join('\n');

  try {
    const d=await claude.use('downloads');
    if(d) return await d.save({filename:'presence-pci-um5.csv',data:csvContent});
  } catch(e){}

  const blob=new Blob([csvContent],{type:'text/csv;charset=utf-8;'});
  const url=URL.createObjectURL(blob);
  const a=document.createElement('a');
  a.href=url; a.download='presence-pci-um5.csv';
  document.body.appendChild(a); a.click();
  document.body.removeChild(a);
}

init();
</script>
</body>
</html>
