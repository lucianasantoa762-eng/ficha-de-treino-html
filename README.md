# ficha-de-treino-html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<title>Ficha de treino</title>
<style>
:root{--bg:#f4f4f1;--card:#fff;--tx:#191918;--tx2:#6f6f69;--bd:#e6e6e0;--chip:#efefea;box-sizing:border-box;padding-top:env(safe-area-inset-top,0px);padding-bottom:env(safe-area-inset-bottom,0px)}
@media (prefers-color-scheme:dark){:root:not([data-theme="light"]){--bg:#121211;--card:#1d1d1b;--tx:#f3f2ec;--tx2:#a5a49b;--bd:#2f2f2c;--chip:#2a2a27}}
:root[data-theme="dark"]{--bg:#121211;--card:#1d1d1b;--tx:#f3f2ec;--tx2:#a5a49b;--bd:#2f2f2c;--chip:#2a2a27}
html{scroll-padding-top:env(safe-area-inset-top,0px)}
*{box-sizing:border-box;-webkit-tap-highlight-color:transparent}
body{margin:0;background:var(--bg);color:var(--tx);font-family:system-ui,-apple-system,"Segoe UI",Roboto,sans-serif;line-height:1.45}
main{max-width:520px;margin:0 auto;padding:16px 16px 40px}
.hero{border-radius:24px;padding:22px;color:#fff;background:linear-gradient(135deg,#0F6E56 0%,#534AB7 100%);display:flex;align-items:center;gap:18px;margin-bottom:16px}
.hero h1{font-size:24px;font-weight:600;margin:0 0 2px;letter-spacing:-.02em}
.hero p{margin:0;font-size:13px;opacity:.8}
.hero .st{display:flex;gap:16px;margin-top:12px;font-size:12px;opacity:.9}
.hero .st b{display:block;font-size:20px;font-weight:600;opacity:1}
.ring{position:relative;width:88px;height:88px;flex:none}
.ring svg{transform:rotate(-90deg)}
.ring span{position:absolute;inset:0;display:flex;align-items:center;justify-content:center;font-size:20px;font-weight:600}
#tabs{display:grid;grid-template-columns:repeat(4,minmax(0,1fr));gap:8px;margin-bottom:16px}
.tab{border:0;background:var(--card);color:var(--tx);border-radius:16px;padding:12px 4px;font:inherit;cursor:pointer;text-align:center;border:1.5px solid transparent;transition:transform .15s}
.tab:active{transform:scale(.96)}
.tab b{display:block;font-size:14px;font-weight:600}
.tab small{font-size:11px;color:var(--tx2)}
.tab.on{border-color:var(--c);background:color-mix(in srgb,var(--c) 12%,var(--card))}
.tab.on b{color:var(--c)}
.card{background:var(--card);border-radius:24px;padding:20px;margin-bottom:16px}
.card h2{font-size:20px;font-weight:600;margin:0;letter-spacing:-.01em}
.tag{display:inline-block;font-size:12px;padding:3px 10px;border-radius:99px;background:color-mix(in srgb,var(--c) 15%,transparent);color:var(--c);font-weight:500;margin:6px 0 12px}
.bar{height:6px;background:var(--chip);border-radius:99px;overflow:hidden;margin-bottom:8px}
.bar div{height:100%;width:0;background:var(--c);border-radius:99px;transition:width .35s}
.ex{display:flex;align-items:center;gap:12px;padding:13px 14px;margin-top:8px;background:var(--chip);border-radius:14px;cursor:pointer;font-size:15px;transition:transform .15s,opacity .2s}
.ex:active{transform:scale(.98)}
.ck{width:24px;height:24px;border-radius:50%;border:2px solid var(--tx2);flex:none;display:flex;align-items:center;justify-content:center;color:#fff;font-size:13px;transition:all .2s}
.ex.d{opacity:.6}
.ex.d .ck{background:var(--c);border-color:var(--c)}
.ex.d .nm{text-decoration:line-through}
.sec{font-size:13px;font-weight:600;color:var(--tx2);text-transform:uppercase;letter-spacing:.06em;margin:24px 4px 10px}
.fr{display:grid;grid-template-columns:repeat(2,minmax(0,1fr));gap:8px}
.fc{background:var(--card);border-radius:14px;padding:12px 14px;display:flex;justify-content:space-between;align-items:center;font-size:14px}
.dots{display:flex;gap:4px}.dots i{width:10px;height:10px;border-radius:50%;background:var(--chip)}.dots i.a{background:#7F77DD}
.foot{display:flex;justify-content:space-between;align-items:center;margin-top:20px;font-size:12px;color:var(--tx2)}
button.rs{font:inherit;font-size:13px;color:var(--tx);background:var(--card);border:0;border-radius:99px;padding:9px 16px;cursor:pointer}
</style>
</head>
<body>
<main>
<div class="hero">
<div class="ring"><svg width="88" height="88" viewBox="0 0 88 88"><circle cx="44" cy="44" r="36" fill="none" stroke="rgba(255,255,255,.25)" stroke-width="9"/><circle id="rg" cx="44" cy="44" r="36" fill="none" stroke="#fff" stroke-width="9" stroke-linecap="round" stroke-dasharray="226.2" stroke-dashoffset="226.2" style="transition:stroke-dashoffset .4s"/></svg><span id="pct">0%</span></div>
<div><h1>Ficha de treino</h1><p>Sexta a domingo: descanso</p>
<div class="st"><div><b id="tot">0</b>feitos</div><div><b id="rem">31</b>restantes</div></div></div>
</div>
<div id="tabs"></div>
<div class="card" id="card">
<div style="display:flex;justify-content:space-between;align-items:baseline"><h2 id="dt"></h2><span id="dc" style="font-size:13px;color:var(--tx2)"></span></div>
<span class="tag" id="ds"></span>
<div class="bar"><div id="db"></div></div>
<div id="list"></div>
</div>
<div class="sec">Frequência semanal</div>
<div class="fr" id="freq"></div>
<div class="foot"><span>Zera sozinho toda segunda.</span><button class="rs" id="reset">Zerar semana</button></div>
</main>
<script>
var dias=[
{n:"Seg",d:"Segunda",c:"#7F77DD",t:"Peito, bíceps e ombro",ex:["Crucifixo na máquina","Supino inclinado","Supino reto","Crossover polia alta","Rosca Scott máquina","Rosca bayesiana","Rosca martelo polia com corda","Elevação lateral"]},
{n:"Ter",d:"Terça",c:"#378ADD",t:"Costas, tríceps e abdômen",ex:["Puxada alta","Remada baixa máquina","Pull around máquina","Tríceps polia alta","Tríceps francês","Tríceps máquina","Abdômen máquina","Abdominal com peso"]},
{n:"Qua",d:"Quarta",c:"#1D9E75",t:"Pernas e abdômen",ex:["Cadeira extensora","Cadeira flexora","Leg press 45","Panturrilha em pé máquina","Agachamento hack","Abdominal com 20 kg"]},
{n:"Qui",d:"Quinta",c:"#D85A30",t:"Braço completo",ex:["Rosca martelo polia","Rosca bayesiana","Rosca Scott","Tríceps corda","Tríceps francês","Elevação lateral","Desenvolvimento máquina","Supino reto máquina","Puxada alta máquina"]}
];
var freq=[["Bíceps",2],["Tríceps",2],["Ombro",2],["Abdômen",2],["Peito",2],["Costas",2],["Pernas",1]];
var TOTAL=0;dias.forEach(function(x){TOTAL+=x.ex.length;});
var KEY="ficha-treino-v1";
function weekId(){var d=new Date();var w=(d.getDay()+6)%7;d.setDate(d.getDate()-w);return d.getFullYear()+"-"+(d.getMonth()+1)+"-"+d.getDate();}
function blank(){return {week:weekId(),done:[{},{},{},{}]};}
var st=blank();
try{var raw=localStorage.getItem(KEY);if(raw){var p=JSON.parse(raw);if(p&&p.week===weekId()&&p.done&&p.done.length===4){st=p;}}}catch(e){}
function save(){try{localStorage.setItem(KEY,JSON.stringify(st));}catch(e){}}
var g=new Date().getDay();var cur=(g>=1&&g<=4)?g-1:0;
function render(){
var tabs=document.getElementById('tabs');tabs.innerHTML='';
dias.forEach(function(x,i){
var b=document.createElement('button');
b.className='tab'+(i===cur?' on':'');b.style.setProperty('--c',x.c);
b.innerHTML='<b>'+x.n+'</b><small>'+Object.keys(st.done[i]).length+'/'+x.ex.length+'</small>';
b.onclick=function(){cur=i;render();};
tabs.appendChild(b);
});
var x=dias[cur],c=Object.keys(st.done[cur]).length;
document.getElementById('card').style.setProperty('--c',x.c);
document.getElementById('dt').textContent=x.d;
document.getElementById('ds').textContent=x.t;
document.getElementById('dc').textContent=c+' de '+x.ex.length;
document.getElementById('db').style.width=Math.round(c/x.ex.length*100)+'%';
var l=document.getElementById('list');l.innerHTML='';
x.ex.forEach(function(e,j){
var r=document.createElement('div');
r.className='ex'+(st.done[cur][j]?' d':'');
r.innerHTML='<span class="ck">'+(st.done[cur][j]?'&#10003;':'')+'</span><span class="nm"></span>';
r.lastChild.textContent=e;
r.onclick=function(){if(st.done[cur][j]){delete st.done[cur][j];}else{st.done[cur][j]=1;}save();render();};
l.appendChild(r);
});
var t=0;st.done.forEach(function(d){t+=Object.keys(d).length;});
var pc=Math.round(t/TOTAL*100);
document.getElementById('tot').textContent=t;
document.getElementById('rem').textContent=TOTAL-t;
document.getElementById('pct').textContent=pc+'%';
document.getElementById('rg').style.strokeDashoffset=226.2*(1-t/TOTAL);
}
document.getElementById('freq').innerHTML=freq.map(function(f){
return '<div class="fc"><span>'+f[0]+'</span><span class="dots"><i class="a"></i><i class="'+(f[1]>1?'a':'')+'"></i></span></div>';
}).join('');
document.getElementById('reset').onclick=function(){st=blank();save();render();};
render();
</script>
</body>
</html>