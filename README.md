<!DOCTYPE html><html lang="pt-BR"><head><meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<title>Neural Raphael Hub · GitHub Edition</title><link rel=preconnect href="https://fonts.googleapis.com"><link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700&family=JetBrains+Mono:wght@400;500&display=swap" rel=stylesheet>
<style>
:root{--bg:#080c14;--b2:#111827;--bd:#1f2937;--fg:#f3f4f6;--mu:#9ca3af;--ac:#818cf8;--gr:#34d399;--rd:#f87171;--pu:#c084fc;--ad:#0f2a24;--dd:#2d1517;--gd:linear-gradient(90deg,#6366f1,#a855f7,#ec4899);box-sizing:border-box;padding-top:env(safe-area-inset-top,0px);padding-bottom:env(safe-area-inset-bottom,0px)}
@media(prefers-color-scheme:light){:root:not([data-theme=dark]){--bg:#f8fafc;--b2:#fff;--bd:#d9dee8;--fg:#111827;--mu:#4b5563;--ac:#4f46e5;--gr:#059669;--rd:#dc2626;--pu:#9333ea;--ad:#d1fae5;--dd:#fee2e2}}
:root[data-theme=light]{--bg:#f8fafc;--b2:#fff;--bd:#d9dee8;--fg:#111827;--mu:#4b5563;--ac:#4f46e5;--gr:#059669;--rd:#dc2626;--pu:#9333ea;--ad:#d1fae5;--dd:#fee2e2}
html{scroll-padding-top:env(safe-area-inset-top,0px)}
body{margin:0;background:var(--bg);color:var(--fg);font:14px/1.5 Inter,-apple-system,"Segoe UI",sans-serif}
a{color:var(--ac);cursor:pointer;text-decoration:none}a:hover{text-decoration:underline}
.hd{background:color-mix(in srgb,var(--b2) 85%,transparent);backdrop-filter:blur(8px);border-bottom:1px solid var(--bd);padding:10px 14px;display:flex;gap:10px;align-items:center;position:sticky;top:env(safe-area-inset-top,0px);z-index:9}
input,textarea,select{background:var(--bg);color:var(--fg);border:1px solid var(--bd);border-radius:6px;padding:6px 10px;font:inherit;max-width:100%;box-sizing:border-box}
textarea{width:100%;min-height:260px;font:12px 'JetBrains Mono',ui-monospace,Menlo,Consolas,monospace}
.btn{background:var(--b2);color:var(--fg);border:1px solid var(--bd);border-radius:6px;padding:4px 12px;cursor:pointer;font:inherit;font-size:13px}
.btn.g{background:linear-gradient(90deg,#6366f1,#a855f7);color:#fff;border-color:transparent}.btn.on{color:var(--pu)}
#sw{position:relative;flex:1}#sr{position:absolute;top:36px;left:0;right:0;background:var(--bg);border:1px solid var(--bd);border-radius:6px;display:none;max-height:300px;overflow:auto}
#sr div{padding:6px 10px;cursor:pointer}#sr div:hover{background:var(--b2)}
.w{max-width:1000px;margin:0 auto;padding:14px}
.rt{font-size:20px;margin:6px 0}.mu{color:var(--mu)}.pill{border:1px solid var(--bd);border-radius:20px;font-size:12px;padding:0 8px;color:var(--mu)}
.tabs{display:flex;gap:4px;border-bottom:1px solid var(--bd);overflow-x:auto;margin:10px 0 14px}
.tabs a{color:var(--fg);padding:8px 12px;white-space:nowrap;border-bottom:2px solid transparent}.tabs a.on{border-color:#a855f7;font-weight:600}
.ct{background:var(--bd);border-radius:20px;padding:0 6px;font-size:12px;margin-left:4px}
.box{border:1px solid var(--bd);border-radius:6px;margin:10px 0;overflow:hidden}
.bh{background:var(--b2);padding:8px 12px;border-bottom:1px solid var(--bd);display:flex;gap:8px;align-items:center;flex-wrap:wrap}.r{margin-left:auto}
.row{display:flex;gap:10px;padding:8px 12px;border-top:1px solid var(--bd);align-items:center}.row:first-child{border:0}.row .t{flex:1;min-width:0}
.sc{overflow-x:auto}table{border-collapse:collapse;font:12px/20px 'JetBrains Mono',ui-monospace,Menlo,Consolas,monospace;width:100%}
td.ln{color:var(--mu);text-align:right;padding:0 10px;user-select:none;width:1%;white-space:nowrap}td{white-space:pre;padding:0 8px}
.pr{padding:12px;white-space:pre-wrap;font:12px 'JetBrains Mono',ui-monospace,Menlo,Consolas,monospace;margin:0;overflow-x:auto}
.md{padding:4px 16px 12px}.md code{background:var(--b2);padding:1px 5px;border-radius:5px}.md pre{background:var(--b2);padding:10px;border-radius:6px;overflow-x:auto}
.md h1,.md h2{border-bottom:1px solid var(--bd);padding-bottom:4px}
i{font-style:normal}i.c{color:var(--mu)}i.s{color:var(--ac)}i.k{color:var(--rd)}i.n{color:var(--pu)}
tr.a{background:var(--ad)}tr.d{background:var(--dd)}
.lb{border-radius:20px;padding:0 8px;font-size:12px;color:#fff}
.log{background:#05070d;color:#e6edf3;padding:10px;font:12px/1.5 'JetBrains Mono',ui-monospace,Menlo,Consolas,monospace;white-space:pre-wrap;max-height:300px;overflow:auto;margin:0}
.hm{display:grid;grid-template-rows:repeat(7,11px);grid-auto-flow:column;gap:3px}.hm b{width:11px;height:11px;border-radius:2px;background:var(--b2);border:1px solid var(--bd)}
.bar{display:flex;height:8px;border-radius:4px;overflow:hidden;margin:8px 0}
.st{font-size:12px;border-radius:20px;padding:0 8px}.ok{color:var(--gr)}.er{color:var(--rd)}
.lg{width:32px;height:32px;border-radius:10px;background:linear-gradient(135deg,#4f46e5,#9333ea,#ec4899);display:flex;align-items:center;justify-content:center}.gt{background:var(--gd);-webkit-background-clip:text;background-clip:text;color:transparent}.box,.btn{transition:.2s}.box:hover{box-shadow:0 0 18px -4px rgba(168,85,247,.35)}.card{padding:14px;cursor:pointer}</style></head><body>
<div class="hd"><a onclick="go({home:1})" style="display:flex;gap:8px;align-items:center;color:inherit"><span class=lg>🧠</span><b class=gt>Neural Raphael Hub</b></a>
<div id="sw"><input id="sq" style="width:100%" placeholder="Buscar arquivos e issues ( / )" oninput="search(this.value)"><div id="sr"></div></div>
<span id=me class=pill></span><button class="btn" onclick="theme()">◐</button></div>
<div class="w" id="app"></div>
<script>
const $=s=>document.querySelector(s),K='nrh-gh-3',D=864e5;
const esc=s=>String(s).replace(/[&<>]/g,c=>({'&':'&amp;','<':'&lt;','>':'&gt;'}[c]));
// hash (cyrb53) para SHAs de commit
function h53(s){let a=0xdeadbeef,b=0x41c6ce57;for(let i=0;i<s.length;i++){const c=s.charCodeAt(i);a=Math.imul(a^c,2654435761);b=Math.imul(b^c,1597334677)}a=Math.imul(a^a>>>16,2246822507)^Math.imul(b^b>>>13,3266489909);b=Math.imul(b^b>>>16,2246822507)^Math.imul(a^a>>>13,3266489909);return(b>>>0).toString(16).padStart(8,'0')+(a>>>0).toString(16).padStart(8,'0')}
function ago(t){const s=(Date.now()-t)/1e3;return s<60?'agora':s<3600?Math.floor(s/60)+' min atrás':s<864e2?Math.floor(s/3600)+' h atrás':Math.floor(s/864e2)+' dias atrás'}
// fuzzy match (subsequência com bônus de consecutivos)
function fz(q,s){q=q.toLowerCase();s=s.toLowerCase();let i=0,sc=0,l=-2;for(let j=0;j<s.length&&i<q.length;j++)if(s[j]==q[i]){sc+=j==l+1?3:1;l=j;i++}return i==q.length?sc-s.length/50:-1}
// diff por LCS (programação dinâmica)
function diff(a,b){const A=a?a.split('\n'):[],B=b?b.split('\n'):[],n=A.length,m=B.length,T=Array.from({length:n+1},()=>new Uint16Array(m+1));
for(let i=n-1;i>=0;i--)for(let j=m-1;j>=0;j--)T[i][j]=A[i]===B[j]?T[i+1][j+1]+1:Math.max(T[i+1][j],T[i][j+1]);
let i=0,j=0,r=[];while(i<n&&j<m){if(A[i]===B[j]){r.push([' ',A[i]]);i++;j++}else if(T[i+1][j]>=T[i][j+1])r.push(['-',A[i++]]);else r.push(['+',B[j++]])}
while(i<n)r.push(['-',A[i++]]);while(j<m)r.push(['+',B[j++]]);return r}
function diffH(ch){return ch.map(c=>{const d=diff(c.a,c.b),ad=d.filter(x=>x[0]=='+').length,rm=d.filter(x=>x[0]=='-').length;
return`<div class=box><div class=bh><b>${esc(c.p)}</b><span class=r><span class=ok>+${ad}</span> <span class=er>−${rm}</span></span></div><div class=sc><table>${d.map(x=>`<tr class="${x[0]=='+'?'a':x[0]=='-'?'d':''}"><td class=ln>${x[0]}</td><td>${esc(x[1])}</td></tr>`).join('')}</table></div></div>`}).join('')}
// realce de sintaxe
function hl(src,p){if(/\.md$/.test(p))return esc(src);const re=/(#.*|\/\/.*|\/\*.*?\*\/)|("(?:\\.|[^"\\\n])*"|'(?:\\.|[^'\\\n])*')|\b(class|def|return|import|from|self|if|else|elif|for|in|not|None|True|False|const|let|function|with|as|while|lambda|raise|try|except|super|run|name|on|steps|uses|var|new|this|static|public|private|void|int|float|double|char|struct|enum|interface|extends|switch|case|break|continue|do|typeof|export|default|catch|finally|throw|null|true|false|undefined|and|or|pass|is|fn|func|impl|mut|use|pub|match|type|package|using|select|where|SELECT|FROM|WHERE)\b|\b(\d+\.?\d*)\b/g;let o='',l=0,m;
while(m=re.exec(src)){o+=esc(src.slice(l,m.index));o+=`<i class=${m[1]?'c':m[2]?'s':m[3]?'k':'n'}>${esc(m[0])}</i>`;l=re.lastIndex}return o+esc(src.slice(l))}
// markdown mínimo
function md(t){let c=0,o='';for(const L of t.split('\n')){if(L.startsWith('```')){o+=c?'</pre>':'<pre>';c=!c;continue}if(c){o+=esc(L)+'\n';continue}
const x=esc(L).replace(/`([^`]+)`/g,'<code>$1</code>').replace(/\*\*([^*]+)\*\*/g,'<b>$1</b>'),n=L.indexOf(' ');
o+=/^#{1,3} /.test(L)?`<h${n}>${x.slice(n+1)}</h${n}>`:/^- /.test(L)?`<li>${x.slice(2)}</li>`:x?`<p>${x}</p>`:''}return o}
// lint: balanceamento de colchetes em .py
function lint(s){const st=[],pr={')':'(',']':'[','}':'{'};let ln=1;for(const ch of s.replace(/#.*/g,'')){if(ch=='\n')ln++;if('([{'.includes(ch))st.push(ch);else if(pr[ch]&&st.pop()!==pr[ch])return'linha '+ln}return st.length?'delimitador não fechado':''}
function rng(a){return()=>{a|=0;a=a+0x6D2B79F5|0;let t=Math.imul(a^a>>>15,1|a);t=t+Math.imul(t^t>>>7,61|t)^t;return((t^t>>>14)>>>0)/4294967296}}
function seed(name,owner){const n=Date.now(),F={
'README.md':'# Neural Raphael Hub\n\nEstúdio de inferência: **geração latente** + **refino e upscale**.\n\n- Módulo 1: IP-Adapter desacoplado com FlashAttention-2\n- Módulo 2: High-Res Fix e CodeFormer\n- Samplers: DDIM e DPM-Solver++\n\nUso: execute o workflow em Actions.',
'module1_flash_attn.py':'class OptimizedIPAdapterDecoupledCrossAttention(nn.Module):\n    def __init__(self, query_dim: int = 128, context_dim: int = 768, num_heads: int = 4):\n        super().__init__()\n        self.num_heads = num_heads\n        self.head_dim = query_dim // num_heads\n        self.to_q = nn.Linear(query_dim, query_dim, bias=False)\n        self.to_k_text = nn.Linear(context_dim, query_dim, bias=False)\n        self.to_v_text = nn.Linear(context_dim, query_dim, bias=False)\n\n    def _apply_sdpa(self, q, k, v):\n        # FlashAttention-2 via PyTorch SDPA\n        out = F.scaled_dot_product_attention(q, k, v, is_causal=False)\n        return out.transpose(1, 2)',
'module2_refiner.py':'class UnifiedModule2Pipeline(nn.Module):\n    def process(self, latents_m1, highres_scale: float = 2.0, denoising_strength: float = 0.45, restore_faces: bool = True):\n        up = F.interpolate(latents_m1, scale_factor=highres_scale, mode="bicubic")\n        refined = self.upscale_unet(z_t=up, z_lr=up)\n        img = self.vae_decoder(refined)\n        if restore_faces:\n            img = self.face_restorer(img)\n        return img',
'orchestrator.py':'import torch\n\ndef run(prompt, steps=20, cfg=7.5, hr_scale=2.0):\n    latents = module1(prompt, steps=steps, cfg=cfg)\n    return module2(latents, highres_scale=hr_scale)',
'samplers/ddim.py':'def ddim_step(x, eps, a_t, a_prev):\n    x0 = (x - (1 - a_t) ** 0.5 * eps) / a_t ** 0.5\n    return a_prev ** 0.5 * x0 + (1 - a_prev) ** 0.5 * eps',
'samplers/dpm_solver.py':'def dpm_solver_2m(x, eps, eps_prev, h, h_prev):\n    r = h_prev / h\n    d = (1 + 1 / (2 * r)) * eps - (1 / (2 * r)) * eps_prev\n    return x - h * d',
'.github/workflows/pipeline.yml':'name: pipeline\non: push\nsteps:\n  - uses: checkout\n  - run: lint\n  - run: pipeline'};
const r1='# Neural Raphael Hub\n\nEstúdio de inferência.',ch=(p,a,b)=>({p,a,b});
const C=[{m:'docs: expand README',t:n-D,ch:[ch('README.md',r1,F['README.md'])]},
{m:'feat: add DDIM and DPM-Solver++ samplers',t:n-5*D,ch:['orchestrator.py','samplers/ddim.py','samplers/dpm_solver.py','.github/workflows/pipeline.yml'].map(p=>ch(p,'',F[p]))},
{m:'Initial commit',t:n-9*D,ch:[ch('README.md','',r1),ch('module1_flash_attn.py','',F['module1_flash_attn.py']),ch('module2_refiner.py','',F['module2_refiner.py'])]}].map(c=>({...c,a:'raphael',sha:h53(c.m+c.t)}));
const X={id:slug(name)+'-'+Math.random().toString(36).slice(2,6),name,owner,desc:'',files:F,commits:C,star:[],watch:[],fork:0,
issues:[{t:'Suporte a ControlNet no Módulo 1',b:'Adicionar ZeroConv para condições estruturais.',l:'enhancement',o:1,d:n-2*D},{t:'VRAM estoura com batch 8',b:'Reproduz em GPU de 16 GB.',l:'bug',o:1,d:n-3*D},{t:'Documentar fidelidade do CodeFormer',b:'',l:'docs',o:0,d:n-6*D}],
prs:[{t:'feat: add Euler ancestral sampler',br:'feat/euler',s:'open',d:n-D/2,ch:[ch('samplers/euler.py','','def euler_a_step(x, eps, sigma, sigma_next):\n    return x + (sigma_next - sigma) * eps')]},
{t:'tune: lower default CFG to 7.0',br:'tune/cfg',s:'open',d:n-D/3,ch:[ch('orchestrator.py',F['orchestrator.py'],F['orchestrator.py'].replace('cfg=7.5','cfg=7.0'))]}],runs:[]};return X}
let S,R={},db,UID='local',V={home:1,tab:'code',p:'',f:1,raw:0,sh:0};const UN={},W=()=>S.owner==UID||UID=='local',slug=s=>s.toLowerCase().replace(/[^\w-]+/g,'-').replace(/^-+|-+$/g,'');
try{R=JSON.parse(localStorage.getItem(K))||{}}catch(e){}
function save(){R[S.id]=S;try{localStorage.setItem(K,JSON.stringify(R))}catch(e){}if(db)db.collection('repos').doc(S.id).set({owner:S.owner,name:S.name,data:JSON.stringify(S)}).catch(()=>{})}
async function names(){try{const u=await claude.use('user'),ids=[...new Set(Object.values(R).map(r=>r.owner))].filter(x=>x!='local'),P=await u.profiles(ids);ids.forEach(i=>UN[i]=P[i].name||'usuário');if(!V.edit)render()}catch(e){}}
(async()=>{try{const u=await claude.use('user');if(u){const m=await u.me();UID=m.id||'local';UN[UID]=m.name||'você';$('#me').textContent=UN[UID]}db=await claude.use('db');
if(db)db.collection('repos').onSnapshot(q=>{const n={};q.docs.forEach(d=>{try{n[d.id]=JSON.parse(d.data().data)}catch(e){}});R=n;if(S)S=R[S.id]||null;if(!S)V.home=1;names();if(!V.edit)render()},()=>{})}catch(e){}render()})();
function newRepo(name,tpl){name=slug(name||'');if(!name)return;const r=seed(name,UID),n=Date.now();if(!tpl){r.files={'README.md':'# '+name+'\n\nNovo repositório.'};r.commits=[{m:'Initial commit',t:n,a:UN[UID]||'você',sha:h53(name+n),ch:[{p:'README.md',a:'',b:r.files['README.md']}]}];r.issues=[];r.prs=[]}
S=r;save();V={tab:'code',p:'',f:1,raw:0,sh:0};render()}
function openRepo(id){S=R[id];V={tab:'code',p:'',f:1,raw:0,sh:0};render()}
function tg(k){const a=S[k],i=a.indexOf(UID);i<0?a.push(UID):a.splice(i,1);save();render()}
function forkRepo(){const c=JSON.parse(JSON.stringify(S));S.fork++;save();c.id=slug(S.name)+'-'+Math.random().toString(36).slice(2,6);Object.assign(c,{owner:UID,forkOf:S.id,star:[],watch:[],fork:0});S=c;save();V={tab:'code',p:'',f:1,raw:0,sh:0};render()}
function openPR(){const o=R[S.forkOf];if(!o)return;const ch=[...new Set([...Object.keys(S.files),...Object.keys(o.files)])].filter(p=>S.files[p]!==o.files[p]).map(p=>({p,a:o.files[p]||'',b:S.files[p]||''}));if(!ch.length)return;o.prs.unshift({t:'Mudanças de '+(UN[UID]||'fork'),br:(UN[UID]||'fork')+':main',s:'open',d:Date.now(),ch});const c=S;S=o;save();S=c;render()}
function delRepo(){delete R[S.id];try{localStorage.setItem(K,JSON.stringify(R))}catch(e){}if(db)db.collection('repos').doc(S.id).delete().catch(()=>{});S=null;V.home=1;render()}
function blame(p){let L=[];for(const c of[...S.commits].reverse()){const x=c.ch.find(k=>k.p==p);if(!x)continue;const n=[];let i=0;for(const[t]of diff(x.a,x.b)){if(t==' ')n.push(L[i++]);else if(t=='-')i++;else n.push(c.sha.slice(0,7)+' '+c.a)}L=n}return L}
function homeView(){const L=Object.values(R).sort((a,b)=>b.commits[0].t-a.commits[0].t),q=V.hq||'';
$('#app').innerHTML=`<div class=box style="padding:16px;background:linear-gradient(135deg,rgba(99,102,241,.18),rgba(236,72,153,.12))"><h2 style="margin:0" class=gt>Seus algoritmos e softwares, arquivados.</h2><p class=mu>Crie repositórios, versione código, abra issues e pull requests, faça forks. Compartilhado com quem usa esta página.</p><input id=rn placeholder="nome-do-repositorio"> <button class="btn g" onclick="newRepo($('#rn').value,0)">+ Novo repositório</button> <button class=btn onclick="newRepo($('#rn').value||'neural-raphael-hub',1)">Modelo Neural Raphael</button></div>
<input style="width:100%" placeholder="Buscar repositórios e código…" value="${esc(q)}" onchange="V.hq=this.value;render()">${L.filter(r=>!q||fz(q,r.name)>=0||Object.values(r.files).some(c=>c.includes(q))).map(r=>`<div class="box card" onclick="openRepo('${r.id}')"><b class=gt>${esc(UN[r.owner]||'usuário')} / ${esc(r.name)}</b> <span class=pill>Public</span>${r.forkOf?' <span class=mu>fork</span>':''}<br><span class=mu>${esc(r.desc||'')} ★ ${r.star.length} · ⑂ ${r.fork} · ${r.commits.length} commits · ${ago(r.commits[0].t)}</span></div>`).join('')||'<p class=mu>Nenhum repositório ainda. Crie o primeiro acima.</p>'}`}
function go(o){Object.assign(V,o);render();scrollTo(0,0)}
function theme(){const r=document.documentElement;r.dataset.theme=(r.dataset.theme||(matchMedia('(prefers-color-scheme:light)').matches?'light':'dark'))=='dark'?'light':'dark'}
function search(q){const r=$('#sr');if(!q||!S){r.style.display='none';return}
const f=Object.keys(S.files).map(p=>[fz(q,p),'📄 '+p,`go({tab:'code',p:'${p}',edit:0,cm:0});$('#sr').style.display='none'`]),
i=S.issues.map((x,k)=>[fz(q,x.t),'⊙ '+x.t,`go({tab:'issues',f:${x.o?1:0}});$('#sr').style.display='none'`]);
const g=Object.entries(S.files).flatMap(([p,c])=>c.split('\n').map((l,n)=>l.toLowerCase().includes(q.toLowerCase())?[.5,'🔎 '+p+':'+(n+1)+' '+l.trim().slice(0,40),`go({tab:'code',p:'${p}',edit:0,cm:0});$('#sr').style.display='none'`]:null).filter(Boolean)).slice(0,4);const L=[...f,...i,...g].filter(x=>x[0]>=0).sort((a,b)=>b[0]-a[0]).slice(0,8);
r.style.display='block';r.innerHTML=L.length?L.map(x=>`<div onclick="${x[2]}">${esc(x[1])}</div>`).join(''):'<div class=mu>Nada encontrado</div>'}
addEventListener('keydown',e=>{if(e.key=='/'&&!/INPUT|TEXTAREA/.test(document.activeElement.tagName)){e.preventDefault();$('#sq').focus()}});
const touch=p=>S.commits.find(c=>c.ch.some(x=>x.p==p||x.p.startsWith(p+'/')));
function mkCommit(m,ch){S.commits.unshift({m,t:Date.now(),a:UN[UID]||'você',sha:h53(m+Date.now()+Math.random()),ch});save()}
function codeView(){if(V.edit)return editor();if(V.cm)return commitsView();const p=V.p,f=S.files[p],lc=S.commits[0];
const cr=`<a onclick="go({p:''})">${S.name}</a>`+p.split('/').filter(Boolean).map((s,i,a)=>` / <a onclick="go({p:'${a.slice(0,i+1).join('/')}'})">${esc(s)}</a>`).join('');
const bar=`<div class=bh><b>${lc.a}</b> <span>${esc(lc.m)}</span><span class=mu>${lc.sha.slice(0,7)} · ${ago(lc.t)}</span><a class=r onclick="go({cm:1,fh:0})">⏱ ${S.commits.length} commits</a></div>`;
if(f!==undefined){const L=hl(f,p).split('\n'),BL=V.bl?blame(p):[],isMd=/\.md$/.test(p)&&!V.raw;
return`<p>${cr}</p><div class=box>${bar}<div class=bh><span class=mu>${f.split('\n').length} linhas · ${f.length} bytes</span><span class=r><button class=btn onclick="go({cm:1,fh:'${p}'})">Histórico</button> <button class=btn onclick="go({bl:${V.bl?0:1}})">Blame</button> <button class=btn onclick="go({raw:${V.raw?0:1}})">${V.raw?'Preview':'Raw'}</button> <button class=btn onclick="try{navigator.clipboard.writeText(S.files['${p}'])}catch(e){}">Copiar</button> <button class=btn onclick="go({edit:1,np:0})">Editar</button> <button class=btn onclick="delF('${p}')">Excluir</button></span></div>
${isMd?`<div class=md>${md(f)}</div>`:V.raw?`<pre class=pr>${esc(f)}</pre>`:`<div class=sc><table>${L.map((x,i)=>`<tr class="${V.hlL==i+1?'a':''}"><td class=ln style="cursor:pointer" onclick="V.hlL=${i+1};render()">${i+1}</td>${V.bl?`<td class=mu>${BL[i]||''}</td>`:''}<td>${x}</td></tr>`).join('')}</table></div>`}</div>`}
const pre=p?p+'/':'',E=new Map();for(const k in S.files)if(k.startsWith(pre)){const r=k.slice(pre.length);E.set(r.split('/')[0],r.includes('/'))}
const rows=[...E].sort((a,b)=>(b[1]-a[1])||(a[0]<b[0]?-1:1)).map(([n,d])=>{const q=pre+n,c=touch(q);return`<div class=row><span>${d?'📁':'📄'}</span><a class=t onclick="go({p:'${q}'})">${esc(n)}</a><span class="mu t" style="flex:2;overflow:hidden;white-space:nowrap;text-overflow:ellipsis">${esc(c.m)}</span><span class=mu>${ago(c.t)}</span></div>`}).join('');
const rd=S.files[pre+'README.md'];
return`<p>${cr}</p><div class=box>${bar}${rows}</div><button class="btn g" onclick="go({edit:1,np:1})">+ Novo arquivo</button>${rd?`<div class=box><div class=bh>📖 README.md</div><div class=md>${md(rd)}</div></div>`:''}`}
function editor(){const p=V.np?'':V.p,v=S.files[p]||'';return`<div class=box><div class=bh>${V.np?'Novo arquivo: <input id=ep placeholder="pasta/arquivo.py">':'Editando <input id=ep value="'+esc(p)+'">'}</div><div style="padding:10px"><textarea id=ev>${esc(v)}</textarea><p><input id=em style="width:100%" placeholder="Mensagem do commit"></p><span id=ee class=er></span><p><button class="btn g" onclick="commit()">Commit changes</button> <button class=btn onclick="go({edit:0})">Cancelar</button></p></div></div>`}
function commit(){if(!W())return;const p=V.np?$('#ep').value.trim():V.p;if(!/^[\w.\/-]+$/.test(p)){$('#ee').textContent='Caminho inválido';return}
const a=S.files[p]||'',b=$('#ev').value;if(a===b){$('#ee').textContent='Sem alterações';return}S.files[p]=b;mkCommit($('#em').value||(a?'Update ':'Create ')+p,[{p,a,b}]);V.edit=0;V.p=p;render()}
function delF(p){if(!W()||!(p in S.files))return;const a=S.files[p];delete S.files[p];mkCommit('Delete '+p,[{p,a,b:''}]);V.p=p.split('/').slice(0,-1).join('/');render()}
function commitsView(){return`<p><a onclick="go({cm:0})">← Code</a>${V.fh?'<span class=mu> Histórico de '+esc(V.fh)+'</span>':''}</p>`+S.commits.filter(c=>!V.fh||c.ch.some(x=>x.p==V.fh)).map((c,i)=>`<div class=box><div class=row><div class=t><b>${esc(c.m)}</b><br><span class=mu>${c.a} · ${ago(c.t)}</span></div><code>${c.sha.slice(0,7)}</code><button class=btn onclick="go({sh:V.sh==='${c.sha}'?0:'${c.sha}'})">diff</button><button class=btn onclick="revert('${c.sha}')">Revert</button></div>${V.sh==c.sha?diffH(c.ch):''}</div>`).join('')}
function issuesView(){const q=V.iq||'',o=S.issues.filter(i=>i.o).length,cl=S.issues.length-o,col={bug:'#d1242f',enhancement:'#1f883d',docs:'#0969da'};
const L=S.issues.map((x,i)=>[x,i]).filter(([x])=>!!x.o==!!V.f&&(!q||fz(q,x.t)>=0));
return`<div style="display:flex;gap:8px;flex-wrap:wrap"><input style="flex:1" placeholder="Filtrar issues" value="${esc(q)}" onchange="go({iq:this.value})"><button class="btn g" onclick="go({ni:1})">New issue</button></div>
${V.ni?`<div class=box style="padding:10px"><input id=nt style="width:100%" placeholder="Título"><p><textarea id=nb style="min-height:80px" placeholder="Descrição"></textarea></p><select id=nl><option>bug<option>enhancement<option>docs</select> <button class="btn g" onclick="addIssue()">Criar</button></div>`:''}
<div class=box><div class=bh><a onclick="go({f:1})" style="${V.f?'font-weight:700':''}">${o} Open</a><a onclick="go({f:0})" style="${V.f?'':'font-weight:700'}">${cl} Closed</a></div>
${L.map(([x,i])=>`<div class=row><span class="${x.o?'ok':'mu'}">${x.o?'⊙':'✔'}</span><div class=t><b>${esc(x.t)}</b> <span class=lb style="background:${col[x.l]}">${x.l}</span><br><span class=mu>#${i+1} · ${ago(x.d)}</span>${x.b?`<br>${esc(x.b)}`:''}${(x.cm||[]).map(c=>`<br><span class=mu>💬 ${esc(c)}</span>`).join('')}<br><input placeholder="Comentar…" onchange="(S.issues[${i}].cm=S.issues[${i}].cm||[]).push((UN[UID]||'você')+': '+this.value);save();render()"></div><button class=btn onclick="S.issues[${i}].o=${x.o?0:1};save();render()">${x.o?'Fechar':'Reabrir'}</button></div>`).join('')||'<div class="row mu">Nenhuma issue.</div>'}</div>`}
function addIssue(){const t=$('#nt').value.trim();if(!t)return;S.issues.unshift({t,b:$('#nb').value,l:$('#nl').value,o:1,d:Date.now()});V.ni=0;V.f=1;save();render()}
function prsView(){return S.prs.map((p,i)=>`<div class=box><div class=row><span class="${p.s=='open'?'ok':'mu'}">⑂</span><div class=t><b>${esc(p.t)}</b><br><span class=mu>${p.br} → main · ${ago(p.d)}</span></div><span class="st ${p.s=='open'?'ok':'mu'}">${p.s}</span>${p.conf?'<span class=er>conflito</span>':''}${p.s=='open'?`<button class="btn g" onclick="merge(${i})">Merge</button>`:''}<button class=btn onclick="go({pr:V.pr===${i}?-1:${i}})">files</button></div>${V.pr===i?diffH(p.ch):''}</div>`).join('')}
function merge(i){if(!W())return;const p=S.prs[i];if(p.ch.some(c=>{const u=S.files[c.p]||'';return u!==c.a&&u!==c.b})){p.conf=1;save();render();return}p.ch.forEach(c=>{c.b?S.files[c.p]=c.b:delete S.files[c.p]});mkCommit('Merge pull request: '+p.t,p.ch);p.s='merged';save();render()}
const sl=ms=>new Promise(r=>setTimeout(r,ms));
async function runWf(){const r={id:S.runs.length+1,t:Date.now(),st:'running',log:[]};S.runs.unshift(r);const L=x=>{r.log.push(x);if(V.tab=='actions')render()};
L('▶ Checkout');await sl(300);const bad=[];for(const p in S.files)if(p.endsWith('.py')){const e=lint(S.files[p]);L((e?'✖ ':'✔ ')+'lint '+p+(e?' ('+e+')':''));if(e)bad.push(p);await sl(200)}
if(bad.length){r.st='failure';L('Falhou: '+bad.length+' arquivo(s)');save();render();return}
const T=20,ab=t=>Math.pow(Math.cos((t/T+.008)/1.008*Math.PI/2),2);L('▶ Módulo 1: cronograma cosseno, '+T+' passos');
for(let t=T;t>=0;t-=5){L('  passo '+(T-t)+'/'+T+'  ᾱ='+ab(t).toFixed(4)+'  σ='+Math.sqrt((1-ab(t))/ab(t)).toFixed(3));await sl(250)}
L('▶ Módulo 2: High-Res Fix 2.0x → [1, 3, 1024, 1024]');await sl(400);L('✔ CodeFormer fidelity 0.80');r.st='success';save();render()}
function actionsView(){return`<button class="btn g" onclick="runWf()">▶ Run workflow</button>`+S.runs.map(r=>`<div class=box><div class=bh><span class="${r.st=='success'?'ok':r.st=='failure'?'er':'mu'}">${r.st=='success'?'✔':r.st=='failure'?'✖':'●'}</span><b>pipeline #${r.id}</b><span class=mu>${ago(r.t)} · ${r.st}</span></div><pre class=log>${esc(r.log.join('\n'))}</pre></div>`).join('')||'<p class=mu>Nenhuma execução ainda. O lint valida delimitadores dos .py.</p>'}
function insView(){const R=rng(7),cell=[],day=Math.floor(Date.now()/D),cm={};S.commits.forEach(c=>{const k=Math.floor(c.t/D);cm[k]=(cm[k]||0)+3});
for(let i=370;i>=0;i--){const v=(R()>.6?Math.ceil(R()*3):0)+(cm[day-i]||0),l=Math.min(4,v);cell.push(`<b style="${l?`background:var(--gr);opacity:${.25+l*.19}`:''}"></b>`)}
const ex={},tot={};let all=0;for(const p in S.files){const e=(p.match(/\.(\w+)$/)||[,'other'])[1],n=S.files[p].length;ex[e]=(ex[e]||0)+n;all+=n}
const nm={py:'Python',md:'Markdown',yml:'YAML'},cl={py:'#3572A5',md:'#083fa1',yml:'#cb171e'};
const lg=Object.entries(ex).sort((a,b)=>b[1]-a[1]),lines=Object.values(S.files).reduce((a,s)=>a+s.split('\n').length,0);
return`<div class=box><div class=bh>Atividade de commits</div><div class=sc style="padding:12px"><div class=hm>${cell.join('')}</div></div></div>
<div class=box style="padding:12px"><b>Linguagens</b><div class=bar>${lg.map(([e,n])=>`<span style="width:${n/all*100}%;background:${cl[e]||'#888'}"></span>`).join('')}</div>${lg.map(([e,n])=>`<span style="margin-right:12px">● ${nm[e]||e} <span class=mu>${(n/all*100).toFixed(1)}%</span></span>`).join('')}</div>
<div class=box style="padding:12px"><b>Resumo</b><br>${S.commits.length} commits · ${Object.keys(S.files).length} arquivos · ${lines} linhas · ${S.issues.filter(i=>i.o).length} issues abertas · ${S.prs.filter(p=>p.s=='merged').length} PRs mescladas</div>`}
function render(){if(V.home||!S)return homeView();const own=S.owner==UID,o=S.issues.filter(i=>i.o).length,po=S.prs.filter(p=>p.s=='open').length,T=[['code','Code'],['issues','Issues',o],['prs','Pull requests',po],['actions','Actions'],['projects','Projects'],['releases','Releases'],['insights','Insights']];
const b={code:codeView,issues:issuesView,prs:prsView,actions:actionsView,insights:insView,releases:relView,projects:projView}[V.tab]();
$('#app').innerHTML=`<div class=rt><a onclick="go({home:1})">${esc(UN[S.owner]||'usuário')}</a> / <b class=gt>${esc(S.name)}</b> <span class=pill>Public</span>${S.forkOf?' <span class=mu>fork</span>':''}</div><input style="width:100%" placeholder="Descrição" value="${esc(S.desc||'')}" ${own?'':'disabled'} onchange="S.desc=this.value;save()"><div style="display:flex;gap:6px;flex-wrap:wrap;margin:6px 0"><button class="btn ${S.watch.includes(UID)?'on':''}" onclick="tg('watch')">👁 Watch ${S.watch.length}</button><button class=btn onclick="forkRepo()">⑂ Fork ${S.fork}</button><button class="btn ${S.star.includes(UID)?'on':''}" onclick="tg('star')">★ Star ${S.star.length}</button>${own&&S.forkOf&&R[S.forkOf]?'<button class="btn g" onclick="openPR()">Abrir PR</button>':''}${own?'<button class=btn onclick="delRepo()">🗑</button>':''}</div>${own?'':'<p class=mu>🔒 Somente leitura: faça um fork para editar.</p>'}
<div class=tabs>${T.map(t=>`<a class="${V.tab==t[0]?'on':''}" onclick="go({tab:'${t[0]}',edit:0,cm:0})">${t[1]}${t[2]?`<span class=ct>${t[2]}</span>`:''}</a>`).join('')}</div>${tools()}${b}`}

// ===== Módulo avançado: branches, ZIP/CRC32, releases, projetos, revert, markdown+, insights =====
function md(t){let c=0,o='';const T=[],il=x=>esc(x).replace(/`([^`]+)`/g,'<code>$1</code>').replace(/\*\*([^*]+)\*\*/g,'<b>$1</b>').replace(/\*([^*]+)\*/g,'<em>$1</em>').replace(/\[([^\]]+)\]\((https?:[^)\s]+)\)/g,'<a href="$2" target=_blank rel=noopener>$1</a>');
const fl=()=>{if(!T.length)return;const r=T.map(l=>l.split('|').slice(1,-1).map(x=>x.trim()));o+='<table style="font:inherit"><tr>'+r[0].map(x=>`<th>${il(x)}</th>`).join('')+'</tr>'+r.slice(2).map(a=>'<tr>'+a.map(x=>`<td style="white-space:normal">${il(x)}</td>`).join('')+'</tr>').join('')+'</table>';T.length=0};
for(const L of t.split('\n')){if(L.startsWith('```')){fl();o+=c?'</pre>':'<pre>';c=!c;continue}if(c){o+=esc(L)+'\n';continue}if(/^\|.*\|$/.test(L)){T.push(L);continue}fl();let m;
o+=(m=L.match(/^(#{1,4}) (.*)/))?`<h${m[1].length}>${il(m[2])}</h${m[1].length}>`:/^(-{3,}|\*{3,})$/.test(L)?'<hr>':(m=L.match(/^> (.*)/))?`<blockquote style="border-left:3px solid var(--bd);margin:0;padding-left:10px;color:var(--mu)">${il(m[1])}</blockquote>`:(m=L.match(/^[-*] \[( |x)\] (.*)/))?`<div>${m[1]=='x'?'☑':'☐'} ${il(m[2])}</div>`:(m=L.match(/^(?:[-*]|\d+\.) (.*)/))?`<li>${il(m[1])}</li>`:L.trim()?`<p>${il(L)}</p>`:''}fl();return o}
function commit(){if(!W())return;const p=$('#ep').value.trim(),old=V.np?'':V.p;if(!/^[\w.\/-]+$/.test(p)){$('#ee').textContent='Caminho inválido';return}
const a=old?S.files[old]:S.files[p]||'',b=$('#ev').value,mv=old&&old!=p;if(a===b&&!mv){$('#ee').textContent='Sem alterações';return}
const ch=[];if(mv){ch.push({p:old,a,b:''});delete S.files[old]}S.files[p]=b;ch.push({p,a:mv?'':a,b});mkCommit($('#em').value||(mv?'Rename '+old+' → '+p:a?'Update '+p:'Create '+p),ch);V.edit=0;V.p=p;render()}
function revert(sha){if(!W())return;const c=S.commits.find(x=>x.sha==sha);if(!c)return;const ch=c.ch.map(x=>({p:x.p,a:x.b,b:x.a}));ch.forEach(x=>x.b?S.files[x.p]=x.b:delete S.files[x.p]);mkCommit('Revert "'+c.m+'"',ch);render()}
// branches
function brSave(){S.br=S.br||{};S.br[S.cur||'main']={files:S.files,commits:S.commits}}
function brSwitch(n){brSave();const b=S.br[n];if(!b)return;S.files=b.files;S.commits=b.commits;S.cur=n;V.p='';save();render()}
function brNew(){const n=slug($('#bn').value);if(!n||!W())return;brSave();if(S.br[n])return;S.br[n]=JSON.parse(JSON.stringify(S.br[S.cur||'main']));brSwitch(n)}
function brMerge(){const c=S.cur||'main';if(c=='main'||!W())return;brSave();const m=S.br.main,x=S.br[c],ch=[];
for(const p of new Set([...Object.keys(m.files),...Object.keys(x.files)]))if(m.files[p]!==x.files[p])ch.push({p,a:m.files[p]||'',b:x.files[p]||''});
if(ch.length){ch.forEach(k=>k.b?m.files[k.p]=k.b:delete m.files[k.p]);m.commits.unshift({m:'Merge branch '+c,t:Date.now(),a:UN[UID]||'você',sha:h53(c+Date.now()),ch})}
delete S.br[c];S.files=m.files;S.commits=m.commits;S.cur='main';V.p='';save();render()}
// ZIP (método "store") com CRC32
const CT=(()=>{const t=[];for(let n=0;n<256;n++){let c=n;for(let k=0;k<8;k++)c=c&1?0xEDB88320^(c>>>1):c>>>1;t[n]=c>>>0}return t})();
const crc=u=>{let c=-1;for(const b of u)c=CT[(c^b)&255]^(c>>>8);return(c^-1)>>>0};
function zip(files){const E=new TextEncoder(),P=[],CD=[];let off=0,cs=0;const ks=Object.keys(files);
for(const p of ks){const n=E.encode(p),d=E.encode(files[p]),cr=crc(d),h=new DataView(new ArrayBuffer(30)),g=new DataView(new ArrayBuffer(46));
h.setUint32(0,0x04034b50,true);h.setUint16(4,20,true);h.setUint16(6,0x800,true);h.setUint32(14,cr,true);h.setUint32(18,d.length,true);h.setUint32(22,d.length,true);h.setUint16(26,n.length,true);P.push(h.buffer,n,d);
g.setUint32(0,0x02014b50,true);g.setUint16(4,20,true);g.setUint16(6,20,true);g.setUint16(8,0x800,true);g.setUint32(16,cr,true);g.setUint32(20,d.length,true);g.setUint32(24,d.length,true);g.setUint16(28,n.length,true);g.setUint32(42,off,true);CD.push(g.buffer,n);
off+=30+n.length+d.length;cs+=46+n.length}
const e=new DataView(new ArrayBuffer(22));e.setUint32(0,0x06054b50,true);e.setUint16(8,ks.length,true);e.setUint16(10,ks.length,true);e.setUint32(12,cs,true);e.setUint32(16,off,true);
return new Blob([...P,...CD,e.buffer],{type:'application/zip'})}
async function dl(name,data){try{const d=await claude.use('downloads');if(d){await d.save({filename:name,data});return}}catch(e){}const a=document.createElement('a');a.href=URL.createObjectURL(data instanceof Blob?data:new Blob([data]));a.download=name;a.click()}
function imp(fl){if(!fl)return;const r=new FileReader();r.onload=()=>{try{const x=JSON.parse(r.result);if(!x.files||!x.commits)return;Object.assign(x,{id:slug(x.name||'import')+'-'+Math.random().toString(36).slice(2,6),owner:UID,star:[],watch:[]});S=x;save();V={tab:'code',p:'',f:1,raw:0,sh:0};render()}catch(e){}};r.readAsText(fl[0]||fl)}
async function upl(fs){if(!W())return;const d=S.files[V.p]!==undefined?V.p.split('/').slice(0,-1).join('/'):V.p,ch=[];for(const f of fs){const p=(d?d+'/':'')+f.name.replace(/[^\w.\/-]/g,'_'),b=await f.text(),a=S.files[p]||'';if(a!==b){S.files[p]=b;ch.push({p,a,b})}}if(ch.length)mkCommit('Upload '+ch.length+' file(s)',ch);render()}
function tools(){if(V.tab!='code'||V.cm||V.edit)return'';const br=['main',...Object.keys(S.br||{}).filter(x=>x!='main')],c=S.cur||'main';
return`<div style="display:flex;gap:6px;flex-wrap:wrap;align-items:center;margin-bottom:8px"><select onchange="brSwitch(this.value)">${br.map(b=>`<option ${b==c?'selected':''}>${esc(b)}</option>`).join('')}</select>${W()?`<input id=bn placeholder="nova-branch" style="width:110px"><button class=btn onclick="brNew()">+ Branch</button>${c!='main'?'<button class="btn g" onclick="brMerge()">Merge → main</button>':''}<label class=btn>⬆ Arquivos<input type=file multiple hidden onchange="upl(this.files)"></label>`:''}<button class=btn onclick="dl(S.name+'.zip',zip(S.files))">⬇ ZIP</button><button class=btn onclick="dl(S.name+'.json',JSON.stringify(S))">⬇ JSON</button><label class=btn>⬆ Importar JSON<input type=file accept=".json" hidden onchange="imp(this.files)"></label></div>`}
// releases (notas automáticas a partir dos commits)
function relView(){const L=S.rel||[];return(W()?`<div class=box style="padding:10px"><input id=rt placeholder="v1.0.0"> <input id=rn2 placeholder="Título"><p><textarea id=rb style="min-height:70px" placeholder="Notas (vazio = gerar dos commits)"></textarea></p><button class="btn g" onclick="addRel()">Publicar release</button></div>`:'')+L.map((r,i)=>`<div class=box><div class=bh><b class=gt>${esc(r.tag)}</b> ${esc(r.title)}<span class="mu r">${r.sha.slice(0,7)} · ${ago(r.t)}</span></div><div class=md>${md(r.notes)}</div><div class=row><button class=btn onclick="dl(S.name+'-'+S.rel[${i}].tag+'.zip',zip(S.rel[${i}].files))">⬇ Source (zip)</button></div></div>`).join('')||'<p class=mu>Sem releases.</p>'}
function addRel(){const tag=$('#rt').value.trim();if(!tag)return;let n=$('#rb').value;if(!n){const pv=(S.rel||[])[0],k=pv?S.commits.findIndex(c=>c.sha==pv.sha):-1;n='## Mudanças\n'+S.commits.slice(0,k<0?S.commits.length:k).map(c=>'- '+c.m).join('\n')}
(S.rel=S.rel||[]).unshift({tag,title:$('#rn2').value,notes:n,sha:S.commits[0].sha,t:Date.now(),files:{...S.files}});save();render()}
// projetos (kanban)
function projView(){const P=S.pj=S.pj||{cols:['A fazer','Em andamento','Feito'],cards:[]};
return`<div style="display:flex;gap:10px;overflow-x:auto">${P.cols.map((c,ci)=>`<div class=box style="min-width:230px;flex:1"><div class=bh><b>${esc(c)}</b><span class=ct>${P.cards.filter(k=>k.c==ci).length}</span></div>${P.cards.map((k,ki)=>k.c==ci?`<div class=row style="flex-wrap:wrap"><span class=t>${esc(k.t)}</span>${ci>0?`<button class=btn onclick="mvc(${ki},-1)">◀</button>`:''}${ci<2?`<button class=btn onclick="mvc(${ki},1)">▶</button>`:''}<button class=btn onclick="S.pj.cards.splice(${ki},1);save();render()">✕</button></div>`:'').join('')}<div class=row><input style="width:100%" placeholder="+ Cartão" onchange="addCard(${ci},this.value)"></div></div>`).join('')}</div>`}
const mvc=(i,d)=>{S.pj.cards[i].c+=d;save();render()},addCard=(c,t)=>{if(!t.trim())return;S.pj.cards.push({c,t});save();render()};
// insights: frequência de código (diff) e contribuidores
const _iv=insView;insView=function(){const Q={},A={};S.commits.forEach(c=>{const k=new Date(c.t).toISOString().slice(5,10);c.ch.forEach(x=>{const d=diff(x.a,x.b);Q[k]=Q[k]||[0,0];Q[k][0]+=d.filter(y=>y[0]=='+').length;Q[k][1]+=d.filter(y=>y[0]=='-').length});A[c.a]=(A[c.a]||0)+1});
const ks=Object.keys(Q).sort(),mx=Math.max(1,...ks.map(k=>Math.max(...Q[k]))),w=40,W2=Math.max(ks.length*w,200);
return _iv()+`<div class=box style="padding:12px"><b>Frequência de código</b><div class=sc><svg viewBox="0 0 ${W2} 112" style="width:${W2}px">${ks.map((k,i)=>`<rect x="${i*w+4}" y="${55-Q[k][0]/mx*50}" width="14" height="${Q[k][0]/mx*50}" fill="#34d399"/><rect x="${i*w+20}" y="55" width="14" height="${Q[k][1]/mx*50}" fill="#f87171"/><text x="${i*w+4}" y="108" font-size="9" fill="#9ca3af">${k}</text>`).join('')}</svg></div></div><div class=box style="padding:12px"><b>Contribuidores</b>${Object.entries(A).sort((a,b)=>b[1]-a[1]).map(([n,c])=>`<div>${esc(n)} <span class=mu>${c} commits</span></div>`).join('')}</div>`};
// feed de atividade na home
const _hv=homeView;homeView=function(){_hv();const A=Object.values(R).flatMap(r=>r.commits.slice(0,5).map(c=>({r,c}))).sort((a,b)=>b.c.t-a.c.t).slice(0,8);$('#app').insertAdjacentHTML('beforeend',`<div class=box><div class=bh><b>Atividade recente</b></div>${A.map(({r,c})=>`<div class=row><span class=t><b>${esc(c.a)}</b> em ${esc(r.name)}: ${esc(c.m)}</span><span class=mu>${ago(c.t)}</span></div>`).join('')||'<div class="row mu">Sem atividade.</div>'}</div>`)};
// atalhos estilo GitHub: g c / g i / g p / g a / g r / g b e "t"
let gk=0;addEventListener('keydown',e=>{if(/INPUT|TEXTAREA|SELECT/.test(document.activeElement.tagName)||!S||V.home)return;if(gk){gk=0;const m={c:'code',i:'issues',p:'prs',a:'actions',r:'releases',b:'projects'}[e.key];if(m)go({tab:m,edit:0,cm:0});return}if(e.key=='g')gk=1;if(e.key=='t'){e.preventDefault();$('#sq').focus()}});

render();
/* ============================================================
   NEURAL RAPHAEL HUB
   BLOCO 2 — CORE ENGINE
   ============================================================
   Objetivos:
   - barramento de eventos
   - estado global
   - roteador
   - permissões
   - notificações
   - command palette
   - cache
   - IDs
   - validação
   - telemetria local
   - extensões para os próximos blocos
   ============================================================ */

const NRH2 = (() => {

    const VERSION = "2.0.0";
    const PREFIX = "nrh-core";

    /* ---------------------------------------------------------
       UTILIDADES
       --------------------------------------------------------- */

    const now = () => Date.now();

    const uid = (prefix = "id") =>
        prefix + "_" +
        Date.now().toString(36) + "_" +
        Math.random().toString(36).slice(2, 10);

    const clone = value => {
        if (value === undefined) return undefined;
        return JSON.parse(JSON.stringify(value));
    };

    const isObject = value =>
        value !== null &&
        typeof value === "object" &&
        !Array.isArray(value);

    const isString = value =>
        typeof value === "string";

    const isFunction = value =>
        typeof value === "function";

    const clamp = (value, min, max) =>
        Math.max(min, Math.min(max, value));

    const sleep = ms =>
        new Promise(resolve => setTimeout(resolve, ms));

    const normalize = value =>
        String(value ?? "")
            .normalize("NFD")
            .replace(/[\u0300-\u036f]/g, "")
            .toLowerCase()
            .trim();

    const slugify = value =>
        normalize(value)
            .replace(/[^a-z0-9]+/g, "-")
            .replace(/^-+|-+$/g, "")
            .slice(0, 100);

    const timestamp = () =>
        new Date().toISOString();

    const safeJSON = value => {
        try {
            return JSON.stringify(value);
        } catch {
            return null;
        }
    };

    /* ---------------------------------------------------------
       EVENT BUS
       --------------------------------------------------------- */

    const events = new Map();

    function on(event, handler) {

        if (!events.has(event)) {
            events.set(event, new Set());
        }

        events.get(event).add(handler);

        return () => off(event, handler);
    }

    function once(event, handler) {

        const unsubscribe = on(event, (...args) => {
            unsubscribe();
            handler(...args);
        });

        return unsubscribe;
    }

    function off(event, handler) {

        const set = events.get(event);

        if (!set) {
            return false;
        }

        set.delete(handler);

        if (!set.size) {
            events.delete(event);
        }

        return true;
    }

    function emit(event, payload) {

        const listeners = events.get(event);

        if (!listeners) {
            return;
        }

        for (const listener of [...listeners]) {

            try {
                listener(payload);
            } catch (error) {

                console.error(
                    "[NRH EVENT ERROR]",
                    event,
                    error
                );
            }
        }
    }

    /* ---------------------------------------------------------
       STORE
       --------------------------------------------------------- */

    const store = {

        state: {
            version: VERSION,
            initialized: false,

            user: null,

            route: {
                page: "home",
                params: {}
            },

            ui: {
                sidebar: true,
                commandPalette: false,
                notifications: false,
                modal: null,
                loading: false
            },

            preferences: {
                theme: "auto",
                density: "comfortable",
                animations: true
            },

            repositories: {},

            notifications: [],

            sessions: [],

            activity: [],

            extensions: {}
        },

        subscribers: new Set(),

        get(path) {

            if (!path) {
                return this.state;
            }

            return path
                .split(".")
                .reduce(
                    (obj, key) =>
                        obj == null ? undefined : obj[key],
                    this.state
                );
        },

        set(path, value) {

            const parts = path.split(".");
            let target = this.state;

            for (let i = 0; i < parts.length - 1; i++) {

                const key = parts[i];

                if (!isObject(target[key])) {
                    target[key] = {};
                }

                target = target[key];
            }

            target[parts.at(-1)] = value;

            this.notify(path, value);

            return value;
        },

        update(path, updater) {

            const current = this.get(path);

            const next =
                isFunction(updater)
                    ? updater(current)
                    : updater;

            return this.set(path, next);
        },

        subscribe(handler) {

            this.subscribers.add(handler);

            return () => {
                this.subscribers.delete(handler);
            };
        },

        notify(path, value) {

            for (const subscriber of [
                ...this.subscribers
            ]) {

                try {
                    subscriber({
                        path,
                        value,
                        state: this.state
                    });
                } catch (error) {
                    console.error(
                        "[NRH STORE]",
                        error
                    );
                }
            }

            emit("store:update", {
                path,
                value
            });
        }
    };

    /* ---------------------------------------------------------
       STORAGE
       --------------------------------------------------------- */

    const storage = {

        memory: new Map(),

        key(key) {
            return `${PREFIX}:${key}`;
        },

        get(key, fallback = null) {

            const storageKey = this.key(key);

            try {

                const raw =
                    localStorage.getItem(storageKey);

                if (raw !== null) {
                    return JSON.parse(raw);
                }

            } catch (error) {

                console.warn(
                    "[NRH STORAGE GET]",
                    error
                );
            }

            if (this.memory.has(storageKey)) {
                return clone(
                    this.memory.get(storageKey)
                );
            }

            return fallback;
        },

        set(key, value) {

            const storageKey = this.key(key);

            this.memory.set(
                storageKey,
                clone(value)
            );

            try {

                localStorage.setItem(
                    storageKey,
                    JSON.stringify(value)
                );

            } catch (error) {

                console.warn(
                    "[NRH STORAGE SET]",
                    error
                );
            }

            emit("storage:set", {
                key,
                value
            });

            return value;
        },

        remove(key) {

            const storageKey = this.key(key);

            this.memory.delete(storageKey);

            try {
                localStorage.removeItem(storageKey);
            } catch {}

            emit("storage:remove", {
                key
            });
        },

        clear() {

            try {

                Object.keys(localStorage)
                    .filter(key =>
                        key.startsWith(PREFIX + ":")
                    )
                    .forEach(key =>
                        localStorage.removeItem(key)
                    );

            } catch {}

            this.memory.clear();

            emit("storage:clear");
        }
    };

    /* ---------------------------------------------------------
       ROUTER
       --------------------------------------------------------- */

    const router = {

        routes: new Map(),

        register(name, handler) {

            if (!isFunction(handler)) {
                throw new TypeError(
                    "Route handler precisa ser uma função."
                );
            }

            this.routes.set(name, handler);

            return this;
        },

        exists(name) {
            return this.routes.has(name);
        },

        navigate(name, params = {}) {

            const handler = this.routes.get(name);

            store.set(
                "route",
                {
                    page: name,
                    params
                }
            );

            emit("route:change", {
                name,
                params
            });

            if (handler) {

                try {
                    return handler(params);
                } catch (error) {

                    console.error(
                        "[NRH ROUTER]",
                        error
                    );

                    emit("route:error", {
                        name,
                        params,
                        error
                    });
                }
            }
        },

        current() {
            return clone(
                store.get("route")
            );
        }
    };

    /* ---------------------------------------------------------
       PERMISSÕES
       --------------------------------------------------------- */

    const permissions = {

        levels: {
            none: 0,
            read: 10,
            triage: 20,
            write: 30,
            maintain: 40,
            admin: 50,
            owner: 60
        },

        compare(a, b) {

            const A =
                this.levels[a] ??
                this.levels.none;

            const B =
                this.levels[b] ??
                this.levels.none;

            return A - B;
        },

        allows(current, required) {

            return this.compare(
                current,
                required
            ) >= 0;
        },

        repositoryRole(repository, userId) {

            if (!repository || !userId) {
                return "none";
            }

            if (
                repository.owner === userId
            ) {
                return "owner";
            }

            const collaborators =
                repository.collaborators || {};

            return collaborators[userId] ||
                "none";
        },

        can(repository, userId, required) {

            const role =
                this.repositoryRole(
                    repository,
                    userId
                );

            return this.allows(
                role,
                required
            );
        }
    };

    /* ---------------------------------------------------------
       NOTIFICAÇÕES
       --------------------------------------------------------- */

    const notifications = {

        push({
            title,
            message = "",
            type = "info",
            link = null,
            persistent = false
        }) {

            const item = {
                id: uid("notification"),
                title,
                message,
                type,
                link,
                persistent,
                read: false,
                createdAt: now()
            };

            store.update(
                "notifications",
                list => [
                    item,
                    ...(list || [])
                ].slice(0, 200)
            );

            emit(
                "notification:new",
                item
            );

            return item;
        },

        markRead(id) {

            store.update(
                "notifications",
                list =>
                    (list || []).map(item =>
                        item.id === id
                            ? {
                                ...item,
                                read: true
                            }
                            : item
                    )
            );
        },

        markAllRead() {

            store.update(
                "notifications",
                list =>
                    (list || []).map(item => ({
                        ...item,
                        read: true
                    }))
            );
        },

        unread() {

            return (
                store.get("notifications") || []
            ).filter(item => !item.read);
        },

        remove(id) {

            store.update(
                "notifications",
                list =>
                    (list || []).filter(
                        item =>
                            item.id !== id
                    )
            );
        },

        clear() {

            store.set(
                "notifications",
                []
            );
        }
    };

    /* ---------------------------------------------------------
       ACTIVITY LOG
       --------------------------------------------------------- */

    const activity = {

        add(type, payload = {}) {

            const item = {
                id: uid("activity"),
                type,
                payload: clone(payload),
                user:
                    store.get("user")?.id ||
                    "anonymous",
                createdAt: now()
            };

            store.update(
                "activity",
                list =>
                    [
                        item,
                        ...(list || [])
                    ].slice(0, 1000)
            );

            emit(
                "activity:new",
                item
            );

            return item;
        },

        list(limit = 50) {

            return (
                store.get("activity") || []
            ).slice(0, limit);
        }
    };

    /* ---------------------------------------------------------
       REPOSITORY SERVICE
       --------------------------------------------------------- */

    const repositories = {

        create({
            owner,
            name,
            description = "",
            visibility = "public"
        }) {

            if (!owner) {
                throw new Error(
                    "Owner obrigatório."
                );
            }

            const cleanName =
                slugify(name);

            if (!cleanName) {
                throw new Error(
                    "Nome de repositório inválido."
                );
            }

            const id =
                `${owner}/${cleanName}`;

            if (
                store.get(
                    `repositories.${id}`
                )
            ) {
                throw new Error(
                    "Repositório já existe."
                );
            }

            const repository = {

                id,

                owner,

                name: cleanName,

                fullName:
                    `${owner}/${cleanName}`,

                description,

                visibility,

                defaultBranch: "main",

                branches: {
                    main: {
                        name: "main",
                        protected: false,
                        head: null
                    }
                },

                files: {},

                commits: [],

                issues: [],

                pullRequests: [],

                releases: [],

                projects: [],

                collaborators: {},

                stars: [],

                watchers: [],

                forks: [],

                createdAt: now(),

                updatedAt: now()
            };

            store.set(
                `repositories.${id}`,
                repository
            );

            activity.add(
                "repository.created",
                {
                    repository: id
                }
            );

            emit(
                "repository:create",
                repository
            );

            return repository;
        },

        get(id) {
            return store.get(
                `repositories.${id}`
            );
        },

        update(id, updater) {

            const repository =
                this.get(id);

            if (!repository) {
                throw new Error(
                    "Repositório não encontrado."
                );
            }

            const updated =
                isFunction(updater)
                    ? updater(clone(repository))
                    : {
                        ...repository,
                        ...updater
                    };

            updated.updatedAt = now();

            store.set(
                `repositories.${id}`,
                updated
            );

            emit(
                "repository:update",
                updated
            );

            return updated;
        },

        remove(id) {

            const repository =
                this.get(id);

            if (!repository) {
                return false;
            }

            store.update(
                "repositories",
                all => {

                    const next = {
                        ...(all || {})
                    };

                    delete next[id];

                    return next;
                }
            );

            activity.add(
                "repository.deleted",
                {
                    repository: id
                }
            );

            emit(
                "repository:delete",
                repository
            );

            return true;
        },

        list(owner = null) {

            const all =
                Object.values(
                    store.get(
                        "repositories"
                    ) || {}
                );

            if (!owner) {
                return all;
            }

            return all.filter(
                repository =>
                    repository.owner === owner
            );
        }
    };

    /* ---------------------------------------------------------
       FILE SERVICE
       --------------------------------------------------------- */

    const files = {

        normalizePath(path) {

            return String(path || "")
                .replaceAll("\\", "/")
                .replace(/^\/+/, "")
                .replace(/\/+/g, "/")
                .split("/")
                .filter(Boolean)
                .join("/");
        },

        exists(repository, path) {

            const p =
                this.normalizePath(path);

            return Object.prototype
                .hasOwnProperty.call(
                    repository.files || {},
                    p
                );
        },

        read(repository, path) {

            const p =
                this.normalizePath(path);

            if (!this.exists(repository, p)) {
                return null;
            }

            return repository.files[p];
        },

        write(
            repository,
            path,
            content
        ) {

            const p =
                this.normalizePath(path);

            if (!p) {
                throw new Error(
                    "Caminho inválido."
                );
            }

            if (
                !isString(content)
            ) {
                throw new TypeError(
                    "Conteúdo precisa ser texto."
                );
            }

            repository.files[p] =
                content;

            repository.updatedAt =
                now();

            return repository;
        },

        remove(repository, path) {

            const p =
                this.normalizePath(path);

            if (
                !this.exists(
                    repository,
                    p
                )
            ) {
                return false;
            }

            delete repository.files[p];

            repository.updatedAt =
                now();

            return true;
        },

        list(repository, directory = "") {

            const prefix =
                this.normalizePath(
                    directory
                );

            const base =
                prefix
                    ? prefix + "/"
                    : "";

            const result =
                new Map();

            for (
                const path of Object.keys(
                    repository.files || {}
                )
            ) {

                if (
                    !path.startsWith(base)
                ) {
                    continue;
                }

                const rest =
                    path.slice(
                        base.length
                    );

                if (!rest) {
                    continue;
                }

                const slash =
                    rest.indexOf("/");

                const name =
                    slash === -1
                        ? rest
                        : rest.slice(
                            0,
                            slash
                        );

                result.set(
                    name,
                    slash !== -1
                );
            }

            return [...result]
                .map(([name, directory]) => ({
                    name,
                    directory
                }))
                .sort((a, b) =>
                    Number(b.directory) -
                    Number(a.directory) ||
                    a.name.localeCompare(
                        b.name
                    )
                );
        }
    };

    /* ---------------------------------------------------------
       COMMAND REGISTRY
       --------------------------------------------------------- */

    const commands = new Map();

    function registerCommand(
        id,
        {
            title,
            description = "",
            shortcut = "",
            handler,
            keywords = []
        }
    ) {

        if (!id) {
            throw new Error(
                "Command ID obrigatório."
            );
        }

        if (!isFunction(handler)) {
            throw new TypeError(
                "Command handler inválido."
            );
        }

        commands.set(id, {
            id,
            title,
            description,
            shortcut,
            handler,
            keywords
        });

        return commands.get(id);
    }

    function executeCommand(
        id,
        ...args
    ) {

        const command =
            commands.get(id);

        if (!command) {
            return false;
        }

        try {

            return command.handler(
                ...args
            );

        } catch (error) {

            notifications.push({
                title:
                    "Erro ao executar comando",
                message:
                    error.message,
                type: "error"
            });

            console.error(
                "[NRH COMMAND]",
                error
            );

            return false;
        }
    }

    function searchCommands(query) {

        const q =
            normalize(query);

        if (!q) {
            return [...commands.values()];
        }

        return [...commands.values()]
            .map(command => {

                const haystack =
                    normalize([
                        command.title,
                        command.description,
                        ...command.keywords
                    ].join(" "));

                let score = 0;

                if (
                    haystack.includes(q)
                ) {
                    score += 100;
                }

                if (
                    normalize(
                        command.title
                    ).startsWith(q)
                ) {
                    score += 50;
                }

                if (
                    normalize(
                        command.title
                    ).includes(q)
                ) {
                    score += 25;
                }

                return {
                    command,
                    score
                };
            })
            .filter(item =>
                item.score > 0
            )
            .sort(
                (a, b) =>
                    b.score - a.score
            )
            .map(item =>
                item.command
            );
    }

    /* ---------------------------------------------------------
       COMMANDS PADRÃO
       --------------------------------------------------------- */

    registerCommand(
        "home",
        {
            title: "Ir para início",
            description:
                "Abrir página principal",
            shortcut: "G H",
            keywords: [
                "home",
                "inicio",
                "dashboard"
            ],
            handler() {

                if (
                    typeof go ===
                    "function"
                ) {
                    go({
                        home: 1
                    });
                } else {
                    router.navigate(
                        "home"
                    );
                }
            }
        }
    );

    registerCommand(
        "theme",
        {
            title:
                "Alternar tema",
            description:
                "Alternar entre tema claro e escuro",
            shortcut:
                "Ctrl+Shift+L",
            keywords: [
                "tema",
                "dark",
                "light"
            ],
            handler() {

                if (
                    typeof theme ===
                    "function"
                ) {
                    theme();
                }
            }
        }
    );

    registerCommand(
        "repository:refresh",
        {
            title:
                "Atualizar repositório",
            description:
                "Renderizar novamente a página atual",
            keywords: [
                "refresh",
                "reload",
                "atualizar"
            ],
            handler() {

                if (
                    typeof render ===
                    "function"
                ) {
                    render();
                }

                emit(
                    "repository:refresh"
                );
            }
        }
    );

    registerCommand(
        "notification:read-all",
        {
            title:
                "Marcar notificações como lidas",
            description:
                "Limpar contador de notificações não lidas",
            keywords: [
                "notifications",
                "read",
                "lidas"
            ],
            handler() {

                notifications
                    .markAllRead();
            }
        }
    );

    /* ---------------------------------------------------------
       KEYBOARD ENGINE
       --------------------------------------------------------- */

    const keyboard = {

        bindings: new Map(),

        bind(key, handler, options = {}) {

            const id =
                uid("key");

            this.bindings.set(
                id,
                {
                    key,
                    handler,
                    ctrl: !!options.ctrl,
                    shift: !!options.shift,
                    alt: !!options.alt,
                    meta: !!options.meta
                }
            );

            return () =>
                this.bindings.delete(id);
        },

        match(binding, event) {

            return (
                event.key.toLowerCase() ===
                binding.key.toLowerCase() &&

                !!event.ctrlKey ===
                binding.ctrl &&

                !!event.shiftKey ===
                binding.shift &&

                !!event.altKey ===
                binding.alt &&

                !!event.metaKey ===
                binding.meta
            );
        },

        init() {

            window.addEventListener(
                "keydown",
                event => {

                    const tag =
                        document
                            .activeElement
                            ?.tagName;

                    const editing =
                        tag === "INPUT" ||
                        tag === "TEXTAREA" ||
                        tag === "SELECT" ||
                        document
                            .activeElement
                            ?.isContentEditable;

                    for (
                        const binding of
                        this.bindings.values()
                    ) {

                        if (
                            editing &&
                            !binding.allowEditing
                        ) {
                            continue;
                        }

                        if (
                            this.match(
                                binding,
                                event
                            )
                        ) {

                            event.preventDefault();

                            try {
                                binding.handler(
                                    event
                                );
                            } catch (
                                error
                            ) {
                                console.error(
                                    error
                                );
                            }

                            return;
                        }
                    }
                }
            );
        }
    };

    keyboard.init();

    /* ---------------------------------------------------------
       COMMAND PALETTE
       --------------------------------------------------------- */

    const palette = {

        open() {

            store.set(
                "ui.commandPalette",
                true
            );

            emit(
                "palette:open"
            );
        },

        close() {

            store.set(
                "ui.commandPalette",
                false
            );

            emit(
                "palette:close"
            );
        },

        toggle() {

            store.update(
                "ui.commandPalette",
                value => !value
            );

            emit(
                store.get(
                    "ui.commandPalette"
                )
                    ? "palette:open"
                    : "palette:close"
            );
        },

        search(query) {
            return searchCommands(
                query
            );
        },

        execute(id) {

            this.close();

            return executeCommand(
                id
            );
        }
    };

    keyboard.bind(
        "k",
        () => palette.toggle(),
        {
            ctrl: true
        }
    );

    /* ---------------------------------------------------------
       MODAL ENGINE
       --------------------------------------------------------- */

    const modal = {

        open(config = {}) {

            const data = {
                id: uid("modal"),
                title:
                    config.title ||
                    "Neural Raphael Hub",
                content:
                    config.content || "",
                actions:
                    config.actions || [],
                closeable:
                    config.closeable !== false
            };

            store.set(
                "ui.modal",
                data
            );

            emit(
                "modal:open",
                data
            );

            return data.id;
        },

        close() {

            const current =
                store.get("ui.modal");

            store.set(
                "ui.modal",
                null
            );

            emit(
                "modal:close",
                current
            );
        }
    };

    /* ---------------------------------------------------------
       USER SESSION
       --------------------------------------------------------- */

    const auth = {

        login(user) {

            if (!user) {
                throw new Error(
                    "Usuário inválido."
                );
            }

            const normalized = {
                id:
                    user.id ||
                    uid("user"),
                name:
                    user.name ||
                    "Usuário",
                username:
                    user.username ||
                    slugify(
                        user.name ||
                        "usuario"
                    ),
                avatar:
                    user.avatar ||
                    "",
                createdAt:
                    user.createdAt ||
                    now()
            };

            store.set(
                "user",
                normalized
            );

            storage.set(
                "session",
                normalized
            );

            activity.add(
                "auth.login"
            );

            emit(
                "auth:login",
                normalized
            );

            return normalized;
        },

        logout() {

            const current =
                store.get("user");

            store.set(
                "user",
                null
            );

            storage.remove(
                "session"
            );

            activity.add(
                "auth.logout"
            );

            emit(
                "auth:logout",
                current
            );
        },

        restore() {

            const session =
                storage.get(
                    "session"
                );

            if (session) {
                store.set(
                    "user",
                    session
                );
            }

            return session;
        },

        current() {
            return store.get(
                "user"
            );
        },

        isAuthenticated() {
            return !!this.current();
        }
    };

    /* ---------------------------------------------------------
       REPOSITORY GUARDS
       --------------------------------------------------------- */

    const guard = {

        authenticated() {

            if (
                !auth.isAuthenticated()
            ) {

                notifications.push({
                    title:
                        "Autenticação necessária",
                    message:
                        "Entre na sua conta para continuar.",
                    type: "warning"
                });

                return false;
            }

            return true;
        },

        repository(
            repository,
            level = "read"
        ) {

            if (!repository) {
                return false;
            }

            const user =
                auth.current();

            if (!user) {
                return level === "read" &&
                    repository.visibility ===
                        "public";
            }

            return permissions.can(
                repository,
                user.id,
                level
            ) ||
                (
                    level === "read" &&
                    repository.visibility ===
                        "public"
                );
        }
    };

    /* ---------------------------------------------------------
       PERSISTÊNCIA DO CORE
       --------------------------------------------------------- */

    function persist() {

        storage.set(
            "core-state",
            {
                preferences:
                    store.get(
                        "preferences"
                    ),

                activity:
                    store.get(
                        "activity"
                    ),

                notifications:
                    store.get(
                        "notifications"
                    )
            }
        );
    }

    function restore() {

        const saved =
            storage.get(
                "core-state"
            );

        if (!saved) {
            return;
        }

        if (
            saved.preferences
        ) {
            store.set(
                "preferences",
                {
                    ...store.get(
                        "preferences"
                    ),
                    ...saved.preferences
                }
            );
        }

        if (
            Array.isArray(
                saved.activity
            )
        ) {
            store.set(
                "activity",
                saved.activity
            );
        }

        if (
            Array.isArray(
                saved.notifications
            )
        ) {
            store.set(
                "notifications",
                saved.notifications
            );
        }
    }

    /* ---------------------------------------------------------
       EXTENSIONS
       --------------------------------------------------------- */

    const extensions = {

        register(
            name,
            extension
        ) {

            if (!name) {
                throw new Error(
                    "Nome da extensão obrigatório."
                );
            }

            store.set(
                `extensions.${name}`,
                {
                    ...extension,
                    registeredAt:
                        now()
                }
            );

            emit(
                "extension:register",
                {
                    name,
                    extension
                }
            );
        },

        get(name) {

            return store.get(
                `extensions.${name}`
            );
        },

        list() {

            return Object.keys(
                store.get(
                    "extensions"
                ) || {}
            );
        }
    };

    /* ---------------------------------------------------------
       INITIALIZAÇÃO
       --------------------------------------------------------- */

    function init() {

        if (
            store.get(
                "initialized"
            )
        ) {
            return;
        }

        restore();

        auth.restore();

        store.set(
            "initialized",
            true
        );

        activity.add(
            "core.initialized",
            {
                version: VERSION
            }
        );

        persist();

        emit(
            "core:ready",
            {
                version: VERSION
            }
        );
    }

    /* ---------------------------------------------------------
       AUTOSAVE
       --------------------------------------------------------- */

    let autosaveTimer = null;

    function autosave() {

        clearTimeout(
            autosaveTimer
        );

        autosaveTimer =
            setTimeout(
                persist,
                500
            );
    }

    on(
        "store:update",
        autosave
    );

    /* ---------------------------------------------------------
       API PÚBLICA
       --------------------------------------------------------- */

    return {

        VERSION,

        util: {
            now,
            uid,
            clone,
            isObject,
            isString,
            clamp,
            sleep,
            normalize,
            slugify,
            timestamp,
            safeJSON
        },

        events: {
            on,
            once,
            off,
            emit
        },

        store,

        storage,

        router,

        permissions,

        notifications,

        activity,

        repositories,

        files,

        commands: {
            register:
                registerCommand,
            execute:
                executeCommand,
            search:
                searchCommands
        },

        keyboard,

        palette,

        modal,

        auth,

        guard,

        extensions,

        init,

        persist,

        restore
    };

})();


/* ============================================================
   INTEGRAÇÃO COM O NÚCLEO ORIGINAL
   ============================================================ */

NRH2.events.on(
    "repository:create",
    repository => {

        console.log(
            "[Neural Raphael Hub] Repositório criado:",
            repository.fullName
        );
    }
);

NRH2.events.on(
    "repository:update",
    repository => {

        console.log(
            "[Neural Raphael Hub] Repositório atualizado:",
            repository.fullName
        );
    }
);

NRH2.events.on(
    "notification:new",
    notification => {

        console.log(
            "[NRH Notification]",
            notification.title
        );
    }
);


/* ============================================================
   COMANDOS EXTRAS
   ============================================================ */

NRH2.commands.register(
    "repository:create",
    {
        title:
            "Criar novo repositório",
        description:
            "Cria um novo projeto no Neural Raphael Hub",
        keywords: [
            "repo",
            "repository",
            "novo",
            "criar"
        ],

        handler() {

            const name =
                prompt(
                    "Nome do repositório:"
                );

            if (!name) {
                return;
            }

            const user =
                NRH2.auth.current();

            const owner =
                user?.username ||
                UID ||
                "local";

            try {

                const repository =
                    NRH2.repositories.create({
                        owner,
                        name,
                        description:
                            "Novo projeto Neural Raphael Hub"
                    });

                NRH2.notifications.push({
                    title:
                        "Repositório criado",
                    message:
                        repository.fullName,
                    type:
                        "success"
                });

            } catch (error) {

                NRH2.notifications.push({
                    title:
                        "Não foi possível criar",
                    message:
                        error.message,
                    type:
                        "error"
                });
            }
        }
    }
);


NRH2.commands.register(
    "notifications",
    {
        title:
            "Abrir notificações",
        description:
            "Visualizar atividade e notificações",
        keywords: [
            "alertas",
            "atividade",
            "notifications"
        ],

        handler() {

            NRH2.palette.close();

            NRH2.store.set(
                "ui.notifications",
                true
            );

            NRH2.events.emit(
                "notifications:open"
            );
        }
    }
);


/* ============================================================
   ATALHO GLOBAL DA PALETA
   ============================================================ */

NRH2.keyboard.bind(
    "p",
    () => {

        if (
            NRH2.store.get(
                "ui.commandPalette"
            )
        ) {
            return;
        }

        NRH2.palette.open();

    },
    {
        ctrl: true,
        shift: true
    }
);


/* ============================================================
   START
   ============================================================ */

NRH2.init();

console.log(
    `%cNeural Raphael Hub Core ${NRH2.VERSION}`,
    "font-weight:bold"
);

console.log(
    "Core Engine carregado."
);
<script>
/* ============================================================
   NEURAL RAPHAEL HUB
   BLOCO 3 — USERS / PROFILES / ORGANIZATIONS / COLLABORATORS
   ------------------------------------------------------------
   Este módulo depende do NRH2 criado no BLOCO 2.
   Não substitui o BLOCO 1.
   Não altera o designer original.
   Namespace principal: NRH3
   ============================================================ */

(function (global) {
    "use strict";

    if (!global.NRH2) {
        console.error(
            "[NRH3] NRH2 não encontrado. " +
            "Carregue o BLOCO 2 antes do BLOCO 3."
        );
        return;
    }

    const NRH2 = global.NRH2;

    const VERSION = "3.0.0";

    /* =========================================================
       3.1 — UTILIDADES
       ========================================================= */

    function clone(value) {
        if (typeof NRH2.clone === "function") {
            return NRH2.clone(value);
        }

        try {
            return JSON.parse(JSON.stringify(value));
        } catch (err) {
            return value;
        }
    }

    function now() {
        return new Date().toISOString();
    }

    function uid(prefix) {
        prefix = prefix || "id";

        return prefix +
            "_" +
            Date.now().toString(36) +
            "_" +
            Math.random().toString(36).slice(2, 10);
    }

    function normalize(value) {
        return String(value || "")
            .trim()
            .toLowerCase();
    }

    function slugify(value) {
        return normalize(value)
            .normalize("NFD")
            .replace(/[\u0300-\u036f]/g, "")
            .replace(/[^a-z0-9]+/g, "-")
            .replace(/^-+|-+$/g, "")
            .slice(0, 80);
    }

    function validLogin(login) {
        return /^[a-zA-Z0-9][a-zA-Z0-9-_]{0,38}$/.test(
            String(login || "")
        );
    }

    function validEmail(email) {
        return /^[^\s@]+@[^\s@]+\.[^\s@]+$/.test(
            String(email || "")
        );
    }

    function emit(event, payload) {
        if (typeof NRH2.emit === "function") {
            NRH2.emit(event, payload);
        }
    }

    function save() {
        if (
            NRH2.persistence &&
            typeof NRH2.persistence.save === "function"
        ) {
            NRH2.persistence.save();
        }
    }

    function escapeHTML(value) {
        return String(value == null ? "" : value)
            .replace(/&/g, "&amp;")
            .replace(/</g, "&lt;")
            .replace(/>/g, "&gt;")
            .replace(/"/g, "&quot;")
            .replace(/'/g, "&#039;");
    }

    /* =========================================================
       3.2 — CONSTANTES DE PERMISSÃO
       ========================================================= */

    const ROLES = {
        NONE: "none",
        READ: "read",
        TRIAGE: "triage",
        WRITE: "write",
        MAINTAIN: "maintain",
        ADMIN: "admin",
        OWNER: "owner"
    };

    const ROLE_WEIGHT = {
        none: 0,
        read: 1,
        triage: 2,
        write: 3,
        maintain: 4,
        admin: 5,
        owner: 6
    };

    const ROLE_PERMISSIONS = {
        none: [],

        read: [
            "repo.read",
            "issues.read",
            "pulls.read",
            "releases.read",
            "projects.read"
        ],

        triage: [
            "repo.read",
            "issues.read",
            "issues.manage",
            "pulls.read",
            "pulls.triage",
            "releases.read",
            "projects.read"
        ],

        write: [
            "repo.read",
            "repo.write",
            "issues.read",
            "issues.manage",
            "pulls.read",
            "pulls.write",
            "releases.read",
            "releases.write",
            "projects.read",
            "projects.write"
        ],

        maintain: [
            "repo.read",
            "repo.write",
            "repo.maintain",
            "issues.read",
            "issues.manage",
            "pulls.read",
            "pulls.write",
            "pulls.merge",
            "releases.read",
            "releases.write",
            "projects.read",
            "projects.write",
            "settings.read"
        ],

        admin: [
            "repo.read",
            "repo.write",
            "repo.maintain",
            "repo.admin",
            "issues.read",
            "issues.manage",
            "pulls.read",
            "pulls.write",
            "pulls.merge",
            "releases.read",
            "releases.write",
            "projects.read",
            "projects.write",
            "settings.read",
            "settings.write",
            "members.read",
            "members.write"
        ],

        owner: [
            "*"
        ]
    };

    /* =========================================================
       3.3 — EXTENSÃO DO ESTADO DO NRH2
       ========================================================= */

    const state = NRH2.store && NRH2.store.state
        ? NRH2.store.state
        : null;

    if (!state) {
        console.error("[NRH3] Estado global do NRH2 não disponível.");
        return;
    }

    state.users = state.users || {};
    state.organizations = state.organizations || {};
    state.teams = state.teams || {};
    state.invitations = state.invitations || {};
    state.collaborators = state.collaborators || {};
    state.followers = state.followers || {};
    state.sessions = state.sessions || {};

    /* =========================================================
       3.4 — USERS SERVICE
       ========================================================= */

    const users = {

        create(data) {
            data = data || {};

            const login = String(data.login || "").trim();

            if (!validLogin(login)) {
                throw new Error(
                    "Login inválido. Use letras, números, '-' ou '_'."
                );
            }

            const key = normalize(login);

            if (this.get(login)) {
                throw new Error("Este login já está em uso.");
            }

            if (data.email && !validEmail(data.email)) {
                throw new Error("E-mail inválido.");
            }

            const id = uid("usr");

            const user = {
                id,
                login,
                username: login,

                name: data.name || login,

                email: data.email || "",

                bio: data.bio || "",

                company: data.company || "",

                location: data.location || "",

                website: data.website || "",

                avatar: data.avatar || "",

                avatar_url: data.avatar_url || "",

                status: data.status || "active",

                type: data.type || "User",

                hireable:
                    data.hireable === true,

                public: data.public !== false,

                verified:
                    data.verified === true,

                createdAt: now(),
                updatedAt: now(),

                followers: [],
                following: [],

                organizations: [],

                repositories: [],

                starred: [],

                preferences: {
                    theme: "system",
                    language: "pt-BR",
                    emailNotifications: true,
                    webNotifications: true
                },

                security: {
                    twoFactorEnabled: false,
                    sessions: []
                },

                stats: {
                    repositories: 0,
                    contributions: 0,
                    followers: 0,
                    following: 0
                }
            };

            state.users[key] = user;

            emit("user:created", {
                user: clone(user)
            });

            save();

            return clone(user);
        },

        get(loginOrId) {
            if (!loginOrId) {
                return null;
            }

            const value = String(loginOrId);

            if (state.users[value]) {
                return clone(state.users[value]);
            }

            const key = normalize(value);

            if (state.users[key]) {
                return clone(state.users[key]);
            }

            const found = Object.values(state.users)
                .find(user =>
                    user.id === value ||
                    normalize(user.login) === key
                );

            return found ? clone(found) : null;
        },

        getRaw(loginOrId) {
            if (!loginOrId) {
                return null;
            }

            const value = String(loginOrId);
            const key = normalize(value);

            if (state.users[key]) {
                return state.users[key];
            }

            return Object.values(state.users)
                .find(user =>
                    user.id === value ||
                    normalize(user.login) === key
                ) || null;
        },

        list(options) {
            options = options || {};

            let result = Object.values(state.users);

            if (options.status) {
                result = result.filter(
                    user => user.status === options.status
                );
            }

            if (options.search) {
                const query = normalize(options.search);

                result = result.filter(user =>
                    normalize(user.login).includes(query) ||
                    normalize(user.name).includes(query) ||
                    normalize(user.bio).includes(query)
                );
            }

            result.sort((a, b) =>
                normalize(a.login).localeCompare(
                    normalize(b.login)
                )
            );

            if (options.limit) {
                result = result.slice(0, options.limit);
            }

            return clone(result);
        },

        update(loginOrId, patch) {
            const user = this.getRaw(loginOrId);

            if (!user) {
                throw new Error("Usuário não encontrado.");
            }

            patch = patch || {};

            const allowed = [
                "name",
                "bio",
                "company",
                "location",
                "website",
                "avatar",
                "avatar_url",
                "hireable",
                "public"
            ];

            allowed.forEach(key => {
                if (Object.prototype.hasOwnProperty.call(patch, key)) {
                    user[key] = patch[key];
                }
            });

            user.updatedAt = now();

            emit("user:updated", {
                user: clone(user)
            });

            save();

            return clone(user);
        },

        delete(loginOrId) {
            const user = this.getRaw(loginOrId);

            if (!user) {
                return false;
            }

            const key = normalize(user.login);

            delete state.users[key];

            Object.values(state.organizations)
                .forEach(org => {
                    org.members =
                        (org.members || [])
                        .filter(id => id !== user.id);
                });

            emit("user:deleted", {
                userId: user.id,
                login: user.login
            });

            save();

            return true;
        }
    };

    /* =========================================================
       3.5 — PERFIL
       ========================================================= */

    const profiles = {

        get(loginOrId) {
            const user = users.get(loginOrId);

            if (!user) {
                return null;
            }

            return {
                id: user.id,
                login: user.login,
                name: user.name,
                bio: user.bio,
                company: user.company,
                location: user.location,
                website: user.website,
                avatar: user.avatar,
                avatar_url: user.avatar_url,
                type: user.type,
                createdAt: user.createdAt,
                repositories: user.repositories || [],
                organizations: user.organizations || [],
                stats: clone(user.stats || {}),
                followers: (user.followers || []).length,
                following: (user.following || []).length
            };
        },

        update(loginOrId, patch) {
            return users.update(loginOrId, patch);
        }
    };

    /* =========================================================
       3.6 — FOLLOW / SOCIAL GRAPH
       ========================================================= */

    const social = {

        follow(followerLogin, targetLogin) {
            const follower = users.getRaw(followerLogin);
            const target = users.getRaw(targetLogin);

            if (!follower || !target) {
                throw new Error("Usuário não encontrado.");
            }

            if (follower.id === target.id) {
                throw new Error(
                    "Um usuário não pode seguir a si próprio."
                );
            }

            follower.following =
                follower.following || [];

            target.followers =
                target.followers || [];

            if (!follower.following.includes(target.id)) {
                follower.following.push(target.id);
            }

            if (!target.followers.includes(follower.id)) {
                target.followers.push(follower.id);
            }

            follower.stats.following =
                follower.following.length;

            target.stats.followers =
                target.followers.length;

            emit("social:follow", {
                follower: follower.login,
                target: target.login
            });

            save();

            return true;
        },

        unfollow(followerLogin, targetLogin) {
            const follower = users.getRaw(followerLogin);
            const target = users.getRaw(targetLogin);

            if (!follower || !target) {
                return false;
            }

            follower.following =
                (follower.following || [])
                .filter(id => id !== target.id);

            target.followers =
                (target.followers || [])
                .filter(id => id !== follower.id);

            follower.stats.following =
                follower.following.length;

            target.stats.followers =
                target.followers.length;

            emit("social:unfollow", {
                follower: follower.login,
                target: target.login
            });

            save();

            return true;
        },

        followers(loginOrId) {
            const user = users.getRaw(loginOrId);

            if (!user) {
                return [];
            }

            return (user.followers || [])
                .map(id => users.get(id))
                .filter(Boolean);
        },

        following(loginOrId) {
            const user = users.getRaw(loginOrId);

            if (!user) {
                return [];
            }

            return (user.following || [])
                .map(id => users.get(id))
                .filter(Boolean);
        }
    };

    /* =========================================================
       3.7 — ORGANIZATIONS
       ========================================================= */

    const organizations = {

        create(data) {
            data = data || {};

            const login =
                String(
                    data.login ||
                    data.name ||
                    ""
                ).trim();

            if (!validLogin(login)) {
                throw new Error(
                    "Identificador da organização inválido."
                );
            }

            const key = normalize(login);

            if (state.organizations[key]) {
                throw new Error(
                    "Esta organização já existe."
                );
            }

            const owner = users.getRaw(
                data.owner ||
                (NRH2.auth &&
                    NRH2.auth.current
                    ? NRH2.auth.current()
                    : null)
            );

            if (!owner) {
                throw new Error(
                    "É necessário um proprietário válido."
                );
            }

            const org = {
                id: uid("org"),

                login,

                name:
                    data.name ||
                    login,

                description:
                    data.description ||
                    "",

                avatar:
                    data.avatar ||
                    "",

                website:
                    data.website ||
                    "",

                email:
                    data.email ||
                    "",

                location:
                    data.location ||
                    "",

                public:
                    data.public !== false,

                createdAt: now(),
                updatedAt: now(),

                owners: [owner.id],

                members: [owner.id],

                teams: [],

                repositories: [],

                invitations: [],

                settings: {
                    defaultRepositoryRole:
                        ROLES.READ,

                    memberVisibility:
                        "public",

                    allowInvitations:
                        true
                },

                stats: {
                    members: 1,
                    repositories: 0,
                    teams: 0
                }
            };

            state.organizations[key] = org;

            owner.organizations =
                owner.organizations || [];

            if (!owner.organizations.includes(org.id)) {
                owner.organizations.push(org.id);
            }

            emit("organization:created", {
                organization: clone(org),
                owner: owner.login
            });

            save();

            return clone(org);
        },

        get(loginOrId) {
            if (!loginOrId) {
                return null;
            }

            const value = String(loginOrId);
            const key = normalize(value);

            if (state.organizations[key]) {
                return clone(state.organizations[key]);
            }

            const found =
                Object.values(state.organizations)
                    .find(org =>
                        org.id === value ||
                        normalize(org.login) === key
                    );

            return found ? clone(found) : null;
        },

        getRaw(loginOrId) {
            if (!loginOrId) {
                return null;
            }

            const value = String(loginOrId);
            const key = normalize(value);

            if (state.organizations[key]) {
                return state.organizations[key];
            }

            return Object.values(state.organizations)
                .find(org =>
                    org.id === value ||
                    normalize(org.login) === key
                ) || null;
        },

        list() {
            return clone(
                Object.values(state.organizations)
                    .sort((a, b) =>
                        normalize(a.login)
                            .localeCompare(
                                normalize(b.login)
                            )
                    )
            );
        },

        update(loginOrId, patch) {
            const org = this.getRaw(loginOrId);

            if (!org) {
                throw new Error(
                    "Organização não encontrada."
                );
            }

            patch = patch || {};

            [
                "name",
                "description",
                "avatar",
                "website",
                "email",
                "location",
                "public"
            ].forEach(key => {
                if (
                    Object.prototype.hasOwnProperty
                        .call(patch, key)
                ) {
                    org[key] = patch[key];
                }
            });

            org.updatedAt = now();

            emit("organization:updated", {
                organization: clone(org)
            });

            save();

            return clone(org);
        },

        addMember(loginOrId, userLogin, role) {
            const org = this.getRaw(loginOrId);
            const user = users.getRaw(userLogin);

            if (!org || !user) {
                throw new Error(
                    "Organização ou usuário não encontrado."
                );
            }

            role = role || ROLES.READ;

            if (!ROLE_WEIGHT.hasOwnProperty(role)) {
                throw new Error(
                    "Papel de organização inválido."
                );
            }

            if (!org.members.includes(user.id)) {
                org.members.push(user.id);
            }

            if (!user.organizations.includes(org.id)) {
                user.organizations.push(org.id);
            }

            org.memberRoles =
                org.memberRoles || {};

            org.memberRoles[user.id] = role;

            org.stats.members =
                org.members.length;

            emit("organization:member_added", {
                organization: org.login,
                user: user.login,
                role
            });

            save();

            return clone(org);
        },

        removeMember(loginOrId, userLogin) {
            const org = this.getRaw(loginOrId);
            const user = users.getRaw(userLogin);

            if (!org || !user) {
                return false;
            }

            if (org.owners.includes(user.id)) {
                throw new Error(
                    "O proprietário não pode ser removido diretamente."
                );
            }

            org.members =
                org.members
                    .filter(id => id !== user.id);

            user.organizations =
                (user.organizations || [])
                    .filter(id => id !== org.id);

            if (org.memberRoles) {
                delete org.memberRoles[user.id];
            }

            org.stats.members =
                org.members.length;

            emit("organization:member_removed", {
                organization: org.login,
                user: user.login
            });

            save();

            return true;
        },

        members(loginOrId) {
            const org = this.getRaw(loginOrId);

            if (!org) {
                return [];
            }

            return org.members
                .map(id => users.get(id))
                .filter(Boolean);
        }
    };

    /* =========================================================
       3.8 — TEAMS
       ========================================================= */

    const teams = {

        create(orgLogin, data) {
            const org = organizations.getRaw(orgLogin);

            if (!org) {
                throw new Error(
                    "Organização não encontrada."
                );
            }

            data = data || {};

            const name =
                String(data.name || "").trim();

            if (!name) {
                throw new Error(
                    "Nome da equipe é obrigatório."
                );
            }

            const slug = slugify(name);

            const existing =
                Object.values(state.teams)
                    .find(team =>
                        team.organizationId === org.id &&
                        team.slug === slug
                    );

            if (existing) {
                throw new Error(
                    "Esta equipe já existe."
                );
            }

            const team = {
                id: uid("team"),

                organizationId:
                    org.id,

                name,

                slug,

                description:
                    data.description || "",

                privacy:
                    data.privacy || "closed",

                members: [],

                maintainers: [],

                repositories: [],

                createdAt: now(),
                updatedAt: now()
            };

            state.teams[team.id] = team;

            if (!org.teams.includes(team.id)) {
                org.teams.push(team.id);
            }

            org.stats.teams =
                org.teams.length;

            emit("team:created", {
                team: clone(team)
            });

            save();

            return clone(team);
        },

        get(id) {
            return state.teams[id]
                ? clone(state.teams[id])
                : null;
        },

        getRaw(id) {
            return state.teams[id] || null;
        },

        list(orgLogin) {
            const org = organizations.getRaw(orgLogin);

            if (!org) {
                return [];
            }

            return org.teams
                .map(id => this.get(id))
                .filter(Boolean);
        },

        addMember(teamId, userLogin) {
            const team = this.getRaw(teamId);
            const user = users.getRaw(userLogin);

            if (!team || !user) {
                throw new Error(
                    "Equipe ou usuário não encontrado."
                );
            }

            const org =
                organizations.getRaw(
                    team.organizationId
                );

            if (!org || !org.members.includes(user.id)) {
                throw new Error(
                    "O usuário precisa pertencer à organização."
                );
            }

            if (!team.members.includes(user.id)) {
                team.members.push(user.id);
            }

            team.updatedAt = now();

            emit("team:member_added", {
                team: team.slug,
                user: user.login
            });

            save();

            return clone(team);
        },

        removeMember(teamId, userLogin) {
            const team = this.getRaw(teamId);
            const user = users.getRaw(userLogin);

            if (!team || !user) {
                return false;
            }

            team.members =
                team.members
                    .filter(id => id !== user.id);

            team.maintainers =
                team.maintainers
                    .filter(id => id !== user.id);

            team.updatedAt = now();

            emit("team:member_removed", {
                team: team.slug,
                user: user.login
            });

            save();

            return true;
        },

        members(teamId) {
            const team = this.getRaw(teamId);

            if (!team) {
                return [];
            }

            return team.members
                .map(id => users.get(id))
                .filter(Boolean);
        }
    };

    /* =========================================================
       3.9 — COLABORADORES DE REPOSITÓRIO
       ========================================================= */

    const collaborators = {

        key(repoId, userId) {
            return String(repoId) +
                "::" +
                String(userId);
        },

        grant(repoId, userLogin, role, actorLogin) {
            const user = users.getRaw(userLogin);

            if (!user) {
                throw new Error(
                    "Usuário não encontrado."
                );
            }

            role = role || ROLES.WRITE;

            if (!ROLE_WEIGHT.hasOwnProperty(role)) {
                throw new Error(
                    "Papel de colaborador inválido."
                );
            }

            const key =
                this.key(repoId, user.id);

            const record = {
                id: key,

                repositoryId:
                    repoId,

                userId:
                    user.id,

                role,

                grantedBy:
                    actorLogin || null,

                createdAt:
                    now(),

                updatedAt:
                    now()
            };

            state.collaborators[key] = record;

            emit("repository:collaborator_granted", {
                repositoryId: repoId,
                user: user.login,
                role,
                grantedBy: actorLogin || null
            });

            save();

            return clone(record);
        },

        revoke(repoId, userLogin) {
            const user = users.getRaw(userLogin);

            if (!user) {
                return false;
            }

            const key =
                this.key(repoId, user.id);

            if (!state.collaborators[key]) {
                return false;
            }

            delete state.collaborators[key];

            emit("repository:collaborator_revoked", {
                repositoryId: repoId,
                user: user.login
            });

            save();

            return true;
        },

        get(repoId, userLogin) {
            const user = users.getRaw(userLogin);

            if (!user) {
                return null;
            }

            const record =
                state.collaborators[
                    this.key(repoId, user.id)
                ];

            return record
                ? clone(record)
                : null;
        },

        list(repoId) {
            return Object.values(
                state.collaborators
            )
                .filter(record =>
                    record.repositoryId === repoId
                )
                .map(record => ({
                    ...clone(record),
                    user:
                        users.get(record.userId)
                }));
        }
    };

    /* =========================================================
       3.10 — RESOLUÇÃO DE PERMISSÕES
       ========================================================= */

    const access = {

        weight(role) {
            return ROLE_WEIGHT[role] || 0;
        },

        permissions(role) {
            return clone(
                ROLE_PERMISSIONS[role] ||
                ROLE_PERMISSIONS.none
            );
        },

        hasRole(currentRole, requiredRole) {
            return this.weight(currentRole) >=
                this.weight(requiredRole);
        },

        canRole(role, permission) {
            const list =
                ROLE_PERMISSIONS[role] ||
                [];

            return list.includes("*") ||
                list.includes(permission);
        },

        repositoryRole(repoId, userLogin) {
            const user =
                users.getRaw(userLogin);

            if (!user) {
                return ROLES.NONE;
            }

            /*
             * Proprietário global do usuário.
             */
            const current =
                NRH2.auth &&
                typeof NRH2.auth.current === "function"
                    ? NRH2.auth.current()
                    : null;

            /*
             * Colaborador explícito.
             */
            const collaborator =
                collaborators.get(
                    repoId,
                    user.login
                );

            let best =
                collaborator
                    ? collaborator.role
                    : ROLES.NONE;

            /*
             * Integração opcional com o sistema
             * de repositories do NRH2.
             */
            let repo = null;

            if (
                NRH2.repositories &&
                typeof NRH2.repositories.get ===
                    "function"
            ) {
                try {
                    repo =
                        NRH2.repositories.get(repoId);
                } catch (err) {
                    repo = null;
                }
            }

            if (repo) {

                const owner =
                    repo.owner ||
                    repo.ownerLogin ||
                    repo.owner_id;

                if (
                    owner &&
                    normalize(owner) ===
                        normalize(user.login)
                ) {
                    best = ROLES.OWNER;
                }

                if (
                    repo.permissions &&
                    repo.permissions[user.id]
                ) {
                    const repoRole =
                        repo.permissions[user.id];

                    if (
                        this.weight(repoRole) >
                        this.weight(best)
                    ) {
                        best = repoRole;
                    }
                }

                if (
                    repo.collaborators &&
                    repo.collaborators[user.login]
                ) {
                    const repoRole =
                        repo.collaborators[user.login];

                    if (
                        this.weight(repoRole) >
                        this.weight(best)
                    ) {
                        best = repoRole;
                    }
                }
            }

            /*
             * Usuário autenticado como proprietário
             * do próprio recurso, quando aplicável.
             */
            if (
                current &&
                typeof current === "object" &&
                current.login &&
                normalize(current.login) ===
                    normalize(user.login)
            ) {
                /*
                 * Não elevamos automaticamente para owner
                 * do repositório. A propriedade precisa
                 * estar associada ao repositório.
                 */
            }

            return best;
        },

        canRepository(
            repoId,
            userLogin,
            permission
        ) {
            const role =
                this.repositoryRole(
                    repoId,
                    userLogin
                );

            return this.canRole(
                role,
                permission
            );
        }
    };

    /* =========================================================
       3.11 — CONVITES
       ========================================================= */

    const invitations = {

        create(data) {
            data = data || {};

            const target =
                users.getRaw(
                    data.user ||
                    data.username
                );

            if (!target) {
                throw new Error(
                    "Usuário convidado não encontrado."
                );
            }

            const invitation = {
                id: uid("inv"),

                type:
                    data.type ||
                    "repository",

                targetId:
                    data.repositoryId ||
                    data.organizationId ||
                    data.teamId ||
                    null,

                userId:
                    target.id,

                inviterId:
                    data.inviterId ||
                    null,

                role:
                    data.role ||
                    ROLES.READ,

                state:
                    "pending",

                message:
                    data.message ||
                    "",

                createdAt:
                    now(),

                respondedAt:
                    null
            };

            state.invitations[
                invitation.id
            ] = invitation;

            emit("invitation:created", {
                invitation:
                    clone(invitation)
            });

            save();

            return clone(invitation);
        },

        get(id) {
            return state.invitations[id]
                ? clone(state.invitations[id])
                : null;
        },

        listForUser(userLogin) {
            const user =
                users.getRaw(userLogin);

            if (!user) {
                return [];
            }

            return Object.values(
                state.invitations
            )
                .filter(inv =>
                    inv.userId === user.id
                )
                .map(clone);
        },

        accept(id) {
            const invitation =
                state.invitations[id];

            if (!invitation) {
                throw new Error(
                    "Convite não encontrado."
                );
            }

            if (invitation.state !== "pending") {
                throw new Error(
                    "Este convite não está pendente."
                );
            }

            invitation.state =
                "accepted";

            invitation.respondedAt =
                now();

            if (
                invitation.type ===
                "organization"
            ) {
                organizations.addMember(
                    invitation.targetId,
                    invitation.userId,
                    invitation.role
                );
            }

            if (
                invitation.type ===
                "team"
            ) {
                teams.addMember(
                    invitation.targetId,
                    invitation.userId
                );
            }

            emit("invitation:accepted", {
                invitation:
                    clone(invitation)
            });

            save();

            return clone(invitation);
        },

        decline(id) {
            const invitation =
                state.invitations[id];

            if (!invitation) {
                throw new Error(
                    "Convite não encontrado."
                );
            }

            invitation.state =
                "declined";

            invitation.respondedAt =
                now();

            emit("invitation:declined", {
                invitation:
                    clone(invitation)
            });

            save();

            return clone(invitation);
        }
    };

    /* =========================================================
       3.12 — AUTENTICAÇÃO DE USUÁRIO
       ========================================================= */

    const identity = {

        register(data) {
            const user =
                users.create(data);

            /*
             * Criamos uma sessão local simples.
             * Em uma versão com backend, isso será
             * substituído por sessão segura no servidor.
             */
            const session = {
                id: uid("ses"),
                userId: user.id,
                login: user.login,
                createdAt: now(),
                lastSeenAt: now(),
                type: "local"
            };

            state.sessions[
                session.id
            ] = session;

            if (
                NRH2.auth &&
                typeof NRH2.auth.login ===
                    "function"
            ) {
                try {
                    NRH2.auth.login(
                        user.login
                    );
                } catch (err) {
                    console.warn(
                        "[NRH3] Login NRH2 não aplicado:",
                        err
                    );
                }
            }

            emit("identity:registered", {
                user: clone(user),
                session: clone(session)
            });

            save();

            return {
                user,
                session
            };
        },

        login(loginOrId) {
            const user =
                users.get(loginOrId);

            if (!user) {
                throw new Error(
                    "Usuário não encontrado."
                );
            }

            const session = {
                id: uid("ses"),
                userId: user.id,
                login: user.login,
                createdAt: now(),
                lastSeenAt: now(),
                type: "local"
            };

            state.sessions[
                session.id
            ] = session;

            if (
                NRH2.auth &&
                typeof NRH2.auth.login ===
                    "function"
            ) {
                try {
                    NRH2.auth.login(
                        user.login
                    );
                } catch (err) {
                    console.warn(
                        "[NRH3] Falha ao sincronizar login.",
                        err
                    );
                }
            }

            emit("identity:login", {
                user: clone(user),
                session: clone(session)
            });

            save();

            return clone(session);
        },

        logout(sessionId) {
            if (
                !state.sessions[sessionId]
            ) {
                return false;
            }

            const session =
                state.sessions[sessionId];

            delete state.sessions[sessionId];

            if (
                NRH2.auth &&
                typeof NRH2.auth.logout ===
                    "function"
            ) {
                try {
                    NRH2.auth.logout();
                } catch (err) {
                    console.warn(
                        "[NRH3] Logout NRH2 falhou.",
                        err
                    );
                }
            }

            emit("identity:logout", {
                session: clone(session)
            });

            save();

            return true;
        },

        session(sessionId) {
            return state.sessions[
                sessionId
            ]
                ? clone(
                    state.sessions[sessionId]
                )
                : null;
        }
    };

    /* =========================================================
       3.13 — AUDITORIA
       ========================================================= */

    const audit = {

        log(action, data) {
            const entry = {
                id: uid("audit"),

                action,

                timestamp:
                    now(),

                actor:
                    data &&
                    data.actor
                        ? data.actor
                        : null,

                resource:
                    data &&
                    data.resource
                        ? data.resource
                        : null,

                metadata:
                    data &&
                    data.metadata
                        ? clone(data.metadata)
                        : {}
            };

            if (
                NRH2.activity &&
                typeof NRH2.activity.add ===
                    "function"
            ) {
                try {
                    NRH2.activity.add(
                        action,
                        entry
                    );
                } catch (err) {
                    console.warn(
                        "[NRH3] Não foi possível registrar atividade.",
                        err
                    );
                }
            }

            emit("audit:event", entry);

            return entry;
        }
    };

    /* =========================================================
       3.14 — EVENTOS AUTOMÁTICOS
       ========================================================= */

    if (typeof NRH2.on === "function") {

        NRH2.on(
            "user:created",
            payload => {
                audit.log(
                    "user.created",
                    {
                        actor:
                            payload.user.login,

                        resource:
                            payload.user.id,

                        metadata: {
                            login:
                                payload.user.login
                        }
                    }
                );
            }
        );

        NRH2.on(
            "organization:created",
            payload => {
                audit.log(
                    "organization.created",
                    {
                        actor:
                            payload.owner,

                        resource:
                            payload.organization.id,

                        metadata: {
                            login:
                                payload.organization.login
                        }
                    }
                );
            }
        );

        NRH2.on(
            "organization:member_added",
            payload => {
                audit.log(
                    "organization.member_added",
                    {
                        actor: null,

                        resource:
                            payload.organization,

                        metadata: {
                            user:
                                payload.user,

                            role:
                                payload.role
                        }
                    }
                );
            }
        );

        NRH2.on(
            "repository:collaborator_granted",
            payload => {
                audit.log(
                    "repository.collaborator_granted",
                    {
                        actor:
                            payload.grantedBy,

                        resource:
                            payload.repositoryId,

                        metadata: {
                            user:
                                payload.user,

                            role:
                                payload.role
                        }
                    }
                );
            }
        );
    }

    /* =========================================================
       3.15 — SEED DE DESENVOLVIMENTO
       ========================================================= */

    function seedDevelopmentUsers() {

        /*
         * Só cria usuários se o banco local estiver vazio.
         * Isso não substitui dados existentes.
         */

        if (Object.keys(state.users).length > 0) {
            return;
        }

        let owner;

        try {
            owner = users.create({
                login: "raphael",
                name: "Raphael",
                bio: "Criador do Neural Raphael Hub",
                company: "Neural Raphael Hub",
                location: "Brasil",
                website: "",
                public: true
            });
        } catch (err) {
            console.warn(
                "[NRH3] Seed do usuário principal:",
                err
            );
            return;
        }

        try {
            users.create({
                login: "developer",
                name: "Developer",
                bio: "Conta de desenvolvimento",
                public: true
            });

            users.create({
                login: "reviewer",
                name: "Code Reviewer",
                bio: "Revisão e qualidade de código",
                public: true
            });

            users.create({
                login: "designer",
                name: "Interface Designer",
                bio: "Design e experiência",
                public: true
            });
        } catch (err) {
            console.warn(
                "[NRH3] Seed de usuários secundários:",
                err
            );
        }

        try {
            organizations.create({
                login: "neural-raphael",
                name: "Neural Raphael",
                description:
                    "Organização principal do Neural Raphael Hub.",
                owner: owner.login,
                public: true
            });
        } catch (err) {
            console.warn(
                "[NRH3] Seed da organização:",
                err
            );
        }
    }

    /* =========================================================
       3.16 — COMPONENTES DE INTERFACE
       ========================================================= */

    const ui = {

        avatar(user, size) {
            user = user || {};

            size =
                Number(size) ||
                40;

            const source =
                user.avatar_url ||
                user.avatar ||
                "";

            if (source) {
                return `
                    <img
                        src="${escapeHTML(source)}"
                        alt="${escapeHTML(user.login || "")}"
                        width="${size}"
                        height="${size}"
                        style="
                            width:${size}px;
                            height:${size}px;
                            border-radius:50%;
                            object-fit:cover;
                        "
                    >
                `;
            }

            const letter =
                escapeHTML(
                    (
                        user.name ||
                        user.login ||
                        "?"
                    )
                    .charAt(0)
                    .toUpperCase()
                );

            return `
                <div
                    aria-label="${escapeHTML(
                        user.login || ""
                    )}"
                    style="
                        width:${size}px;
                        height:${size}px;
                        border-radius:50%;
                        display:flex;
                        align-items:center;
                        justify-content:center;
                        font-weight:700;
                        background:
                            linear-gradient(
                                135deg,
                                #6e40c9,
                                #2f81f7
                            );
                        color:#fff;
                    "
                >
                    ${letter}
                </div>
            `;
        },

        profileCard(loginOrId) {
            const user =
                users.get(loginOrId);

            if (!user) {
                return `
                    <div class="nrh3-empty">
                        Usuário não encontrado.
                    </div>
                `;
            }

            return `
                <article
                    class="nrh3-profile-card"
                    data-user="${escapeHTML(
                        user.login
                    )}"
                >

                    <div
                        class="nrh3-profile-avatar"
                    >
                        ${this.avatar(user, 72)}
                    </div>

                    <div
                        class="nrh3-profile-body"
                    >

                        <h3>
                            ${escapeHTML(
                                user.name
                            )}
                        </h3>

                        <div
                            class="nrh3-profile-login"
                        >
                            @${escapeHTML(
                                user.login
                            )}
                        </div>

                        ${
                            user.bio
                                ? `
                                    <p>
                                        ${escapeHTML(
                                            user.bio
                                        )}
                                    </p>
                                `
                                : ""
                        }

                        <div
                            class="nrh3-profile-meta"
                        >
                            ${
                                user.location
                                    ? `
                                        <span>
                                            📍
                                            ${escapeHTML(
                                                user.location
                                            )}
                                        </span>
                                    `
                                    : ""
                            }

                            ${
                                user.company
                                    ? `
                                        <span>
                                            🏢
                                            ${escapeHTML(
                                                user.company
                                            )}
                                        </span>
                                    `
                                    : ""
                            }
                        </div>

                        <div
                            class="nrh3-profile-stats"
                        >
                            <span>
                                <strong>
                                    ${
                                        user.stats
                                            .repositories || 0
                                    }
                                </strong>
                                repositórios
                            </span>

                            <span>
                                <strong>
                                    ${
                                        user.stats
                                            .followers || 0
                                    }
                                </strong>
                                seguidores
                            </span>

                            <span>
                                <strong>
                                    ${
                                        user.stats
                                            .following || 0
                                    }
                                </strong>
                                seguindo
                            </span>
                        </div>

                    </div>
                </article>
            `;
        },

        organizationCard(loginOrId) {
            const org =
                organizations.get(loginOrId);

            if (!org) {
                return `
                    <div>
                        Organização não encontrada.
                    </div>
                `;
            }

            return `
                <article
                    class="nrh3-organization-card"
                >

                    <div
                        class="nrh3-org-avatar"
                    >
                        ${
                            org.avatar
                                ? `
                                    <img
                                        src="${escapeHTML(
                                            org.avatar
                                        )}"
                                        alt=""
                                    >
                                `
                                : `
                                    <div>
                                        ${escapeHTML(
                                            org.name
                                                .charAt(0)
                                                .toUpperCase()
                                        )}
                                    </div>
                                `
                        }
                    </div>

                    <div>

                        <h3>
                            ${escapeHTML(
                                org.name
                            )}
                        </h3>

                        <div>
                            @${escapeHTML(
                                org.login
                            )}
                        </div>

                        <p>
                            ${escapeHTML(
                                org.description ||
                                ""
                            )}
                        </p>

                        <small>
                            ${
                                org.stats.members
                            }
                            membros ·
                            ${
                                org.stats.repositories
                            }
                            repositórios
                        </small>

                    </div>

                </article>
            `;
        }
    };

    /* =========================================================
       3.17 — COMANDOS DO SISTEMA
       ========================================================= */

    if (
        NRH2.commands &&
        typeof NRH2.commands.register ===
            "function"
    ) {

        NRH2.commands.register({
            id: "user:profile",
            label: "Abrir perfil do usuário",
            description:
                "Localiza e abre o perfil de um usuário.",
            keywords: [
                "user",
                "usuario",
                "perfil",
                "profile"
            ],

            run(args) {
                const login =
                    args &&
                    args[0]
                        ? args[0]
                        : null;

                const user =
                    users.get(login);

                if (!user) {
                    throw new Error(
                        "Usuário não encontrado."
                    );
                }

                emit(
                    "navigation:user",
                    {
                        login:
                            user.login
                    }
                );

                return user;
            }
        });

        NRH2.commands.register({
            id: "organization:list",
            label: "Listar organizações",
            description:
                "Lista as organizações disponíveis.",
            keywords: [
                "organization",
                "organizacao",
                "org"
            ],

            run() {
                return organizations.list();
            }
        });

        NRH2.commands.register({
            id: "organization:create",
            label: "Criar organização",
            description:
                "Cria uma nova organização.",
            keywords: [
                "organization",
                "create",
                "org"
            ],

            run(args) {

                const login =
                    args &&
                    args[0]
                        ? args[0]
                        : "nova-organizacao";

                return organizations.create({
                    login,
                    name: login,
                    owner:
                        NRH2.auth &&
                        typeof NRH2.auth.current ===
                            "function"
                            ? NRH2.auth.current()
                            : "raphael"
                });
            }
        });
    }

    /* =========================================================
       3.18 — API PÚBLICA
       ========================================================= */

    const NRH3 = {

        VERSION,

        ROLES,

        ROLE_WEIGHT,

        ROLE_PERMISSIONS,

        state,

        users,

        profiles,

        social,

        organizations,

        teams,

        collaborators,

        access,

        invitations,

        identity,

        audit,

        ui,

        escapeHTML,

        init() {
            seedDevelopmentUsers();

            emit("nrh3:ready", {
                version: VERSION
            });

            console.log(
                "%c[NRH3] Users & Collaboration Engine " +
                VERSION +
                " carregado.",
                "color:#58a6ff;font-weight:bold"
            );

            return this;
        }
    };

    /* =========================================================
       3.19 — EXPOSIÇÃO GLOBAL
       ========================================================= */

    global.NRH3 = NRH3;

    /* =========================================================
       3.20 — INICIALIZAÇÃO
       ========================================================= */

    NRH3.init();

})(window);


/* ============================================================
   FIM DO BLOCO 3
   ============================================================ */
</script>
<script>
/* ============================================================
   NEURAL RAPHAEL HUB
   BLOCO 4 — ADVANCED REPOSITORIES
   ------------------------------------------------------------
   Depende:
     BLOCO 1 — Núcleo original
     BLOCO 2 — NRH2 Core
     BLOCO 3 — NRH3 Users / Organizations
   Namespace: NRH4
   ============================================================ */

(function (global) {
    "use strict";

    if (!global.NRH2) {
        console.error("[NRH4] NRH2 não encontrado.");
        return;
    }

    if (!global.NRH3) {
        console.error("[NRH4] NRH3 não encontrado.");
        return;
    }

    const NRH2 = global.NRH2;
    const NRH3 = global.NRH3;

    const VERSION = "4.0.0";

    const state =
        NRH2.store &&
        NRH2.store.state
            ? NRH2.store.state
            : null;

    if (!state) {
        console.error(
            "[NRH4] Estado global não disponível."
        );
        return;
    }

    /* =========================================================
       4.1 — UTILIDADES
       ========================================================= */

    function now() {
        return new Date().toISOString();
    }

    function uid(prefix) {
        return (
            String(prefix || "id") +
            "_" +
            Date.now().toString(36) +
            "_" +
            Math.random()
                .toString(36)
                .slice(2, 10)
        );
    }

    function clone(value) {
        try {
            return JSON.parse(
                JSON.stringify(value)
            );
        } catch (error) {
            return value;
        }
    }

    function normalize(value) {
        return String(value || "")
            .trim()
            .toLowerCase();
    }

    function slugify(value) {
        return normalize(value)
            .normalize("NFD")
            .replace(/[\u0300-\u036f]/g, "")
            .replace(/[^a-z0-9]+/g, "-")
            .replace(/^-+|-+$/g, "")
            .slice(0, 100);
    }

    function escapeHTML(value) {
        return String(
            value == null ? "" : value
        )
            .replace(/&/g, "&amp;")
            .replace(/</g, "&lt;")
            .replace(/>/g, "&gt;")
            .replace(/"/g, "&quot;")
            .replace(/'/g, "&#039;");
    }

    function emit(event, payload) {
        if (
            typeof NRH2.emit ===
            "function"
        ) {
            NRH2.emit(
                event,
                payload
            );
        }
    }

    function save() {
        if (
            NRH2.persistence &&
            typeof NRH2.persistence.save ===
                "function"
        ) {
            NRH2.persistence.save();
        }
    }

    /* =========================================================
       4.2 — ESTADO
       ========================================================= */

    state.repositories =
        state.repositories || {};

    state.repositoryStars =
        state.repositoryStars || {};

    state.repositoryWatchers =
        state.repositoryWatchers || {};

    state.repositoryForks =
        state.repositoryForks || {};

    state.repositoryTopics =
        state.repositoryTopics || {};

    state.repositoryTemplates =
        state.repositoryTemplates || {};

    /* =========================================================
       4.3 — REPOSITORY SERVICE
       ========================================================= */

    const repositories = {

        create(data) {
            data = data || {};

            const name =
                String(data.name || "")
                    .trim();

            if (!name) {
                throw new Error(
                    "Nome do repositório é obrigatório."
                );
            }

            if (
                !/^[a-zA-Z0-9._-]+$/.test(name)
            ) {
                throw new Error(
                    "Nome do repositório contém caracteres inválidos."
                );
            }

            const ownerLogin =
                data.owner ||
                data.ownerLogin ||
                (
                    NRH2.auth &&
                    typeof NRH2.auth.current ===
                        "function"
                        ? NRH2.auth.current()
                        : null
                ) ||
                "raphael";

            const owner =
                NRH3.users.getRaw(
                    ownerLogin
                );

            const organization =
                data.organization
                    ? NRH3.organizations
                        .getRaw(
                            data.organization
                        )
                    : null;

            if (
                !owner &&
                !organization
            ) {
                throw new Error(
                    "Proprietário do repositório não encontrado."
                );
            }

            const ownerKey =
                organization
                    ? organization.login
                    : owner.login;

            const fullName =
                ownerKey +
                "/" +
                name;

            const duplicate =
                this.find(fullName);

            if (duplicate) {
                throw new Error(
                    "O repositório já existe."
                );
            }

            const id =
                uid("repo");

            const visibility =
                data.visibility === "private"
                    ? "private"
                    : "public";

            const repo = {

                id,

                name,

                full_name:
                    fullName,

                slug:
                    slugify(fullName),

                owner:
                    owner
                        ? owner.login
                        : organization.login,

                ownerId:
                    owner
                        ? owner.id
                        : organization.id,

                ownerType:
                    organization
                        ? "Organization"
                        : "User",

                organizationId:
                    organization
                        ? organization.id
                        : null,

                description:
                    data.description || "",

                homepage:
                    data.homepage || "",

                visibility,

                private:
                    visibility === "private",

                fork:
                    data.fork === true,

                archived:
                    data.archived === true,

                disabled:
                    false,

                template:
                    data.template === true,

                default_branch:
                    data.default_branch ||
                    "main",

                language:
                    data.language ||
                    null,

                license:
                    data.license ||
                    null,

                topics:
                    Array.isArray(data.topics)
                        ? [
                            ...new Set(
                                data.topics
                                    .map(
                                        normalize
                                    )
                                    .filter(Boolean)
                            )
                        ]
                        : [],

                files:
                    data.files
                        ? clone(data.files)
                        : {
                            "README.md":
                                "# " +
                                name +
                                "\n"
                        },

                branches:
                    data.branches
                        ? clone(data.branches)
                        : {
                            main: {
                                name: "main",
                                protected: false,
                                sha: null
                            }
                        },

                tags:
                    data.tags
                        ? clone(data.tags)
                        : [],

                stars: [],

                watchers: [],

                subscribers: [],

                collaborators: {},

                forks: [],

                parent:
                    data.parent ||
                    null,

                source:
                    data.source ||
                    null,

                createdAt: now(),

                updatedAt: now(),

                pushedAt:
                    now(),

                stats: {

                    stars: 0,

                    watchers: 0,

                    forks: 0,

                    issues: 0,

                    pullRequests: 0,

                    commits: 0,

                    contributors: 0,

                    size: 0
                },

                features: {

                    issues:
                        data.has_issues !== false,

                    projects:
                        data.has_projects !== false,

                    wiki:
                        data.has_wiki !== false,

                    discussions:
                        data.has_discussions !== false,

                    actions:
                        data.has_actions !== false,

                    pages:
                        data.has_pages !== false
                },

                merge: {

                    allowMergeCommit:
                        data.allow_merge_commit !== false,

                    allowSquash:
                        data.allow_squash !== false,

                    allowRebase:
                        data.allow_rebase !== false,

                    allowAutoMerge:
                        data.allow_auto_merge === true,

                    deleteBranchOnMerge:
                        data.delete_branch_on_merge !== false
                },

                security: {

                    secretScanning:
                        false,

                    dependabot:
                        false,

                    vulnerabilityAlerts:
                        false
                }
            };

            state.repositories[id] =
                repo;

            /*
             * Compatibilidade com estruturas que
             * utilizem o login como chave.
             */
            state.repositories[
                repo.slug
            ] = repo;

            if (owner) {

                owner.repositories =
                    owner.repositories || [];

                if (
                    !owner.repositories
                        .includes(id)
                ) {
                    owner.repositories.push(id);
                }

                owner.stats =
                    owner.stats || {};

                owner.stats.repositories =
                    owner.repositories.length;
            }

            if (organization) {

                organization.repositories =
                    organization.repositories || [];

                if (
                    !organization.repositories
                        .includes(id)
                ) {
                    organization.repositories
                        .push(id);
                }

                organization.stats =
                    organization.stats || {};

                organization.stats.repositories =
                    organization.repositories
                        .length;
            }

            emit(
                "repository:created",
                {
                    repository:
                        clone(repo)
                }
            );

            save();

            return clone(repo);
        },

        get(idOrName) {

            if (!idOrName) {
                return null;
            }

            const value =
                String(idOrName);

            if (
                state.repositories[value]
            ) {
                return clone(
                    state.repositories[value]
                );
            }

            const key =
                slugify(value);

            if (
                state.repositories[key]
            ) {
                return clone(
                    state.repositories[key]
                );
            }

            const found =
                Object.values(
                    state.repositories
                )
                .find(repo =>
                    repo &&
                    (
                        repo.id === value ||
                        normalize(
                            repo.full_name
                        ) === normalize(value) ||
                        normalize(
                            repo.name
                        ) === normalize(value)
                    )
                );

            return found
                ? clone(found)
                : null;
        },

        getRaw(idOrName) {

            if (!idOrName) {
                return null;
            }

            const value =
                String(idOrName);

            if (
                state.repositories[value]
            ) {
                return state.repositories[value];
            }

            const key =
                slugify(value);

            if (
                state.repositories[key]
            ) {
                return state.repositories[key];
            }

            return Object.values(
                state.repositories
            )
            .find(repo =>
                repo &&
                (
                    repo.id === value ||
                    normalize(
                        repo.full_name
                    ) === normalize(value) ||
                    normalize(
                        repo.name
                    ) === normalize(value)
                )
            ) || null;
        },

        find(fullName) {

            const wanted =
                normalize(fullName);

            return Object.values(
                state.repositories
            )
            .find(repo =>
                repo &&
                normalize(
                    repo.full_name
                ) === wanted
            )
            || null;
        },

        list(options) {

            options =
                options || {};

            let result =
                Object.values(
                    state.repositories
                )
                .filter(repo =>
                    repo &&
                    repo.id
                );

            /*
             * Remove possíveis duplicações
             * provocadas pela chave id + slug.
             */
            const seen =
                new Set();

            result =
                result.filter(repo => {

                    if (
                        seen.has(repo.id)
                    ) {
                        return false;
                    }

                    seen.add(repo.id);

                    return true;
                });

            if (
                options.owner
            ) {

                const owner =
                    normalize(
                        options.owner
                    );

                result =
                    result.filter(repo =>
                        normalize(
                            repo.owner
                        ) === owner
                    );
            }

            if (
                options.visibility
            ) {

                result =
                    result.filter(repo =>
                        repo.visibility ===
                            options.visibility
                    );
            }

            if (
                options.language
            ) {

                result =
                    result.filter(repo =>
                        normalize(
                            repo.language
                        ) ===
                        normalize(
                            options.language
                        )
                    );
            }

            if (
                options.topic
            ) {

                const topic =
                    normalize(
                        options.topic
                    );

                result =
                    result.filter(repo =>
                        (
                            repo.topics || []
                        )
                        .map(normalize)
                        .includes(topic)
                    );
            }

            if (
                options.search
            ) {

                const query =
                    normalize(
                        options.search
                    );

                result =
                    result.filter(repo =>
                        normalize(
                            repo.name
                        ).includes(query) ||
                        normalize(
                            repo.full_name
                        ).includes(query) ||
                        normalize(
                            repo.description
                        ).includes(query) ||
                        (
                            repo.topics || []
                        )
                        .some(topic =>
                            normalize(topic)
                                .includes(query)
                        )
                    );
            }

            if (
                options.archived !==
                undefined
            ) {

                result =
                    result.filter(repo =>
                        repo.archived ===
                        options.archived
                    );
            }

            switch (
                options.sort
            ) {

                case "stars":

                    result.sort(
                        (a, b) =>
                            b.stats.stars -
                            a.stats.stars
                    );

                    break;

                case "forks":

                    result.sort(
                        (a, b) =>
                            b.stats.forks -
                            a.stats.forks
                    );

                    break;

                case "updated":

                    result.sort(
                        (a, b) =>
                            String(
                                b.updatedAt
                            )
                            .localeCompare(
                                String(
                                    a.updatedAt
                                )
                            )
                    );

                    break;

                default:

                    result.sort(
                        (a, b) =>
                            normalize(
                                a.full_name
                            )
                            .localeCompare(
                                normalize(
                                    b.full_name
                                )
                            )
                    );
            }

            if (
                options.limit
            ) {
                result =
                    result.slice(
                        0,
                        Number(
                            options.limit
                        )
                    );
            }

            return clone(result);
        },

        update(
            idOrName,
            patch
        ) {

            const repo =
                this.getRaw(
                    idOrName
                );

            if (!repo) {
                throw new Error(
                    "Repositório não encontrado."
                );
            }

            patch =
                patch || {};

            const allowed = [
                "description",
                "homepage",
                "visibility",
                "private",
                "language",
                "license",
                "default_branch",
                "archived",
                "has_issues",
                "has_projects",
                "has_wiki",
                "has_discussions",
                "has_actions",
                "has_pages",
                "allow_merge_commit",
                "allow_squash",
                "allow_rebase",
                "allow_auto_merge"
            ];

            allowed.forEach(key => {

                if (
                    Object.prototype
                        .hasOwnProperty
                        .call(
                            patch,
                            key
                        )
                ) {

                    if (
                        key ===
                        "has_issues"
                    ) {
                        repo.features.issues =
                            Boolean(
                                patch[key]
                            );

                        return;
                    }

                    if (
                        key ===
                        "has_projects"
                    ) {
                        repo.features.projects =
                            Boolean(
                                patch[key]
                            );

                        return;
                    }

                    if (
                        key ===
                        "has_wiki"
                    ) {
                        repo.features.wiki =
                            Boolean(
                                patch[key]
                            );

                        return;
                    }

                    if (
                        key ===
                        "has_discussions"
                    ) {
                        repo.features.discussions =
                            Boolean(
                                patch[key]
                            );

                        return;
                    }

                    if (
                        key ===
                        "has_actions"
                    ) {
                        repo.features.actions =
                            Boolean(
                                patch[key]
                            );

                        return;
                    }

                    if (
                        key ===
                        "has_pages"
                    ) {
                        repo.features.pages =
                            Boolean(
                                patch[key]
                            );

                        return;
                    }

                    if (
                        key ===
                        "allow_merge_commit"
                    ) {
                        repo.merge
                            .allowMergeCommit =
                            Boolean(
                                patch[key]
                            );

                        return;
                    }

                    if (
                        key ===
                        "allow_squash"
                    ) {
                        repo.merge
                            .allowSquash =
                            Boolean(
                                patch[key]
                            );

                        return;
                    }

                    if (
                        key ===
                        "allow_rebase"
                    ) {
                        repo.merge
                            .allowRebase =
                            Boolean(
                                patch[key]
                            );

                        return;
                    }

                    if (
                        key ===
                        "allow_auto_merge"
                    ) {
                        repo.merge
                            .allowAutoMerge =
                            Boolean(
                                patch[key]
                            );

                        return;
                    }

                    repo[key] =
                        patch[key];
                }
            });

            if (
                patch.visibility
            ) {

                repo.visibility =
                    patch.visibility;

                repo.private =
                    patch.visibility ===
                    "private";
            }

            repo.updatedAt =
                now();

            emit(
                "repository:updated",
                {
                    repository:
                        clone(repo)
                }
            );

            save();

            return clone(repo);
        },

        remove(idOrName) {

            const repo =
                this.getRaw(
                    idOrName
                );

            if (!repo) {
                return false;
            }

            delete state.repositories[
                repo.id
            ];

            delete state.repositories[
                repo.slug
            ];

            const owner =
                NRH3.users.getRaw(
                    repo.owner
                );

            if (owner) {

                owner.repositories =
                    (
                        owner.repositories ||
                        []
                    )
                    .filter(
                        id =>
                            id !== repo.id
                    );

                owner.stats =
                    owner.stats || {};

                owner.stats.repositories =
                    owner.repositories.length;
            }

            emit(
                "repository:deleted",
                {
                    repositoryId:
                        repo.id,

                    fullName:
                        repo.full_name
                }
            );

            save();

            return true;
        }
    };

    /* =========================================================
       4.4 — STARS
       ========================================================= */

    const stars = {

        has(repoId, userLogin) {

            const user =
                NRH3.users.getRaw(
                    userLogin
                );

            const repo =
                repositories.getRaw(
                    repoId
                );

            if (!user || !repo) {
                return false;
            }

            return (
                repo.stars || []
            )
            .includes(
                user.id
            );
        },

        add(repoId, userLogin) {

            const repo =
                repositories.getRaw(
                    repoId
                );

            const user =
                NRH3.users.getRaw(
                    userLogin
                );

            if (!repo || !user) {
                throw new Error(
                    "Usuário ou repositório não encontrado."
                );
            }

            repo.stars =
                repo.stars || [];

            if (
                !repo.stars
                    .includes(user.id)
            ) {

                repo.stars.push(
                    user.id
                );
            }

            repo.stats.stars =
                repo.stars.length;

            user.starred =
                user.starred || [];

            if (
                !user.starred
                    .includes(repo.id)
            ) {

                user.starred.push(
                    repo.id
                );
            }

            repo.updatedAt =
                now();

            emit(
                "repository:starred",
                {
                    repositoryId:
                        repo.id,

                    user:
                        user.login
                }
            );

            save();

            return true;
        },

        remove(repoId, userLogin) {

            const repo =
                repositories.getRaw(
                    repoId
                );

            const user =
                NRH3.users.getRaw(
                    userLogin
                );

            if (!repo || !user) {
                return false;
            }

            repo.stars =
                (
                    repo.stars ||
                    []
                )
                .filter(
                    id =>
                        id !== user.id
                );

            repo.stats.stars =
                repo.stars.length;

            user.starred =
                (
                    user.starred ||
                    []
                )
                .filter(
                    id =>
                        id !== repo.id
                );

            emit(
                "repository:unstarred",
                {
                    repositoryId:
                        repo.id,

                    user:
                        user.login
                }
            );

            save();

            return true;
        },

        list(repoId) {

            const repo =
                repositories.getRaw(
                    repoId
                );

            if (!repo) {
                return [];
            }

            return (
                repo.stars || []
            )
            .map(
                id =>
                    NRH3.users.get(id)
            )
            .filter(Boolean);
        }
    };

    /* =========================================================
       4.5 — WATCHERS / SUBSCRIBERS
       ========================================================= */

    const watchers = {

        watching(repoId, userLogin) {

            const repo =
                repositories.getRaw(
                    repoId
                );

            const user =
                NRH3.users.getRaw(
                    userLogin
                );

            if (!repo || !user) {
                return false;
            }

            return (
                repo.watchers || []
            )
            .includes(
                user.id
            );
        },

        add(repoId, userLogin) {

            const repo =
                repositories.getRaw(
                    repoId
                );

            const user =
                NRH3.users.getRaw(
                    userLogin
                );

            if (!repo || !user) {
                throw new Error(
                    "Usuário ou repositório não encontrado."
                );
            }

            repo.watchers =
                repo.watchers || [];

            if (
                !repo.watchers
                    .includes(user.id)
            ) {

                repo.watchers.push(
                    user.id
                );
            }

            repo.subscribers =
                repo.subscribers || [];

            if (
                !repo.subscribers
                    .includes(user.id)
            ) {

                repo.subscribers.push(
                    user.id
                );
            }

            repo.stats.watchers =
                repo.watchers.length;

            emit(
                "repository:watched",
                {
                    repositoryId:
                        repo.id,

                    user:
                        user.login
                }
            );

            save();

            return true;
        },

        remove(repoId, userLogin) {

            const repo =
                repositories.getRaw(
                    repoId
                );

            const user =
                NRH3.users.getRaw(
                    userLogin
                );

            if (!repo || !user) {
                return false;
            }

            repo.watchers =
                (
                    repo.watchers ||
                    []
                )
                .filter(
                    id =>
                        id !== user.id
                );

            repo.subscribers =
                (
                    repo.subscribers ||
                    []
                )
                .filter(
                    id =>
                        id !== user.id
                );

            repo.stats.watchers =
                repo.watchers.length;

            emit(
                "repository:unwatched",
                {
                    repositoryId:
                        repo.id,

                    user:
                        user.login
                }
            );

            save();

            return true;
        }
    };

    /* =========================================================
       4.6 — TOPICS
       ========================================================= */

    const topics = {

        list(repoId) {

            const repo =
                repositories.getRaw(
                    repoId
                );

            return repo
                ? clone(
                    repo.topics || []
                )
                : [];
        },

        add(repoId, topic) {

            const repo =
                repositories.getRaw(
                    repoId
                );

            if (!repo) {
                throw new Error(
                    "Repositório não encontrado."
                );
            }

            topic =
                normalize(topic);

            if (!topic) {
                return false;
            }

            repo.topics =
                repo.topics || [];

            if (
                !repo.topics.includes(topic)
            ) {

                repo.topics.push(
                    topic
                );
            }

            repo.updatedAt =
                now();

            emit(
                "repository:topic_added",
                {
                    repositoryId:
                        repo.id,

                    topic
                }
            );

            save();

            return true;
        },

        remove(repoId, topic) {

            const repo =
                repositories.getRaw(
                    repoId
                );

            if (!repo) {
                return false;
            }

            topic =
                normalize(topic);

            repo.topics =
                (
                    repo.topics ||
                    []
                )
                .filter(
                    value =>
                        normalize(value) !==
                        topic
                );

            repo.updatedAt =
                now();

            emit(
                "repository:topic_removed",
                {
                    repositoryId:
                        repo.id,

                    topic
                }
            );

            save();

            return true;
        },

        set(repoId, list) {

            const repo =
                repositories.getRaw(
                    repoId
                );

            if (!repo) {
                throw new Error(
                    "Repositório não encontrado."
                );
            }

            repo.topics =
                [
                    ...new Set(
                        (
                            Array.isArray(list)
                                ? list
                                : []
                        )
                        .map(normalize)
                        .filter(Boolean)
                    )
                ];

            repo.updatedAt =
                now();

            save();

            return clone(
                repo.topics
            );
        }
    };

    /* =========================================================
       4.7 — FORKS
       ========================================================= */

    const forks = {

        list(repoId) {

            const repo =
                repositories.getRaw(
                    repoId
                );

            if (!repo) {
                return [];
            }

            return (
                repo.forks || []
            )
            .map(
                id =>
                    repositories.get(id)
            )
            .filter(Boolean);
        },

        create(repoId, ownerLogin) {

            const parent =
                repositories.getRaw(
                    repoId
                );

            const owner =
                NRH3.users.getRaw(
                    ownerLogin
                );

            if (!parent) {
                throw new Error(
                    "Repositório original não encontrado."
                );
            }

            if (!owner) {
                throw new Error(
                    "Usuário não encontrado."
                );
            }

            if (
                parent.private &&
                !NRH3.access.canRepository(
                    parent.id,
                    owner.login,
                    "repo.read"
                )
            ) {
                throw new Error(
                    "Você não tem acesso a este repositório privado."
                );
            }

            const forkName =
                parent.name;

            let finalName =
                forkName;

            let counter = 1;

            while (
                repositories.find(
                    owner.login +
                    "/" +
                    finalName
                )
            ) {

                finalName =
                    forkName +
                    "-" +
                    counter;

                counter++;
            }

            const fork =
                repositories.create({

                    name:
                        finalName,

                    owner:
                        owner.login,

                    description:
                        parent.description,

                    visibility:
                        parent.visibility,

                    fork:
                        true,

                    parent:
                        parent.id,

                    source:
                        parent.source ||
                        parent.id,

                    default_branch:
                        parent.default_branch,

                    language:
                        parent.language,

                    license:
                        parent.license,

                    topics:
                        parent.topics,

                    files:
                        parent.files,

                    branches:
                        parent.branches,

                    features: clone(
                        parent.features
                    )
                });

            parent.forks =
                parent.forks || [];

            parent.forks.push(
                fork.id
            );

            parent.stats.forks =
                parent.forks.length;

            state.repositoryForks[
                fork.id
            ] = parent.id;

            emit(
                "repository:forked",
                {
                    source:
                        parent.id,

                    fork:
                        fork.id,

                    owner:
                        owner.login
                }
            );

            save();

            return fork;
        }
    };

    /* =========================================================
       4.8 — COLABORADORES
       ========================================================= */

    const repositoryCollaborators = {

        add(
            repoId,
            userLogin,
            role,
            actorLogin
        ) {

            const repo =
                repositories.getRaw(
                    repoId
                );

            if (!repo) {
                throw new Error(
                    "Repositório não encontrado."
                );
            }

            const result =
                NRH3.collaborators.grant(
                    repo.id,
                    userLogin,
                    role ||
                        NRH3.ROLES.WRITE,
                    actorLogin
                );

            repo.collaborators =
                repo.collaborators || {};

            const user =
                NRH3.users.getRaw(
                    userLogin
                );

            repo.collaborators[
                user.id
            ] = {
                role:
                    result.role,

                login:
                    user.login,

                grantedAt:
                    now()
            };

            repo.updatedAt =
                now();

            save();

            return result;
        },

        remove(
            repoId,
            userLogin
        ) {

            const repo =
                repositories.getRaw(
                    repoId
                );

            if (!repo) {
                return false;
            }

            const user =
                NRH3.users.getRaw(
                    userLogin
                );

            if (!user) {
                return false;
            }

            const removed =
                NRH3.collaborators.revoke(
                    repo.id,
                    user.login
                );

            if (
                repo.collaborators
            ) {
                delete repo.collaborators[
                    user.id
                ];
            }

            save();

            return removed;
        },

        list(repoId) {

            const repo =
                repositories.getRaw(
                    repoId
                );

            if (!repo) {
                return [];
            }

            return NRH3.collaborators
                .list(repo.id);
        }
    };

    /* =========================================================
       4.9 — TEMPLATES
       ========================================================= */

    const templates = {

        enable(repoId) {

            const repo =
                repositories.getRaw(
                    repoId
                );

            if (!repo) {
                throw new Error(
                    "Repositório não encontrado."
                );
            }

            repo.template =
                true;

            state.repositoryTemplates[
                repo.id
            ] = true;

            repo.updatedAt =
                now();

            emit(
                "repository:template_enabled",
                {
                    repositoryId:
                        repo.id
                }
            );

            save();

            return clone(repo);
        },

        disable(repoId) {

            const repo =
                repositories.getRaw(
                    repoId
                );

            if (!repo) {
                return false;
            }

            repo.template =
                false;

            delete state.repositoryTemplates[
                repo.id
            ];

            repo.updatedAt =
                now();

            save();

            return true;
        },

        use(
            repoId,
            ownerLogin,
            newName
        ) {

            const source =
                repositories.getRaw(
                    repoId
                );

            if (!source) {
                throw new Error(
                    "Template não encontrado."
                );
            }

            if (!source.template) {
                throw new Error(
                    "Este repositório não é um template."
                );
            }

            return repositories.create({

                name:
                    newName ||
                    source.name +
                    "-copy",

                owner:
                    ownerLogin,

                description:
                    source.description,

                visibility:
                    "public",

                language:
                    source.language,

                license:
                    source.license,

                topics:
                    source.topics,

                files:
                    source.files,

                branches:
                    source.branches
            });
        }
    };

    /* =========================================================
       4.10 — ARQUIVAMENTO
       ========================================================= */

    const archive = {

        archive(repoId) {

            const repo =
                repositories.getRaw(
                    repoId
                );

            if (!repo) {
                throw new Error(
                    "Repositório não encontrado."
                );
            }

            repo.archived =
                true;

            repo.updatedAt =
                now();

            emit(
                "repository:archived",
                {
                    repositoryId:
                        repo.id
                }
            );

            save();

            return clone(repo);
        },

        restore(repoId) {

            const repo =
                repositories.getRaw(
                    repoId
                );

            if (!repo) {
                return false;
            }

            repo.archived =
                false;

            repo.updatedAt =
                now();

            emit(
                "repository:unarchived",
                {
                    repositoryId:
                        repo.id
                }
            );

            save();

            return true;
        }
    };

    /* =========================================================
       4.11 — VISIBILIDADE
       ========================================================= */

    const visibility = {

        set(
            repoId,
            value
        ) {

            value =
                normalize(value);

            if (
                value !== "public" &&
                value !== "private"
            ) {
                throw new Error(
                    "Visibilidade deve ser public ou private."
                );
            }

            const repo =
                repositories.getRaw(
                    repoId
                );

            if (!repo) {
                throw new Error(
                    "Repositório não encontrado."
                );
            }

            repo.visibility =
                value;

            repo.private =
                value === "private";

            repo.updatedAt =
                now();

            emit(
                "repository:visibility_changed",
                {
                    repositoryId:
                        repo.id,

                    visibility:
                        value
                }
            );

            save();

            return clone(repo);
        }
    };

    /* =========================================================
       4.12 — ACCESS CONTROL
       ========================================================= */

    const access = {

        canRead(
            repoId,
            userLogin
        ) {

            const repo =
                repositories.getRaw(
                    repoId
                );

            if (!repo) {
                return false;
            }

            if (
                repo.visibility ===
                "public"
            ) {
                return true;
            }

            return NRH3.access
                .canRepository(
                    repo.id,
                    userLogin,
                    "repo.read"
                );
        },

        canWrite(
            repoId,
            userLogin
        ) {

            return NRH3.access
                .canRepository(
                    repoId,
                    userLogin,
                    "repo.write"
                );
        },

        canAdmin(
            repoId,
            userLogin
        ) {

            return NRH3.access
                .canRepository(
                    repoId,
                    userLogin,
                    "repo.admin"
                );
        }
    };

    /* =========================================================
       4.13 — ESTATÍSTICAS
       ========================================================= */

    const statistics = {

        calculate(repoId) {

            const repo =
                repositories.getRaw(
                    repoId
                );

            if (!repo) {
                return null;
            }

            let fileCount = 0;

            let totalBytes = 0;

            Object.values(
                repo.files || {}
            )
            .forEach(content => {

                fileCount++;

                totalBytes +=
                    String(
                        content == null
                            ? ""
                            : content
                    ).length;
            });

            repo.stats.size =
                totalBytes;

            repo.stats.files =
                fileCount;

            repo.stats.stars =
                (
                    repo.stars || []
                ).length;

            repo.stats.watchers =
                (
                    repo.watchers || []
                ).length;

            repo.stats.forks =
                (
                    repo.forks || []
                ).length;

            return clone(
                repo.stats
            );
        }
    };

    /* =========================================================
       4.14 — PESQUISA GLOBAL
       ========================================================= */

    const search = {

        repositories(query, options) {

            options =
                options || {};

            const results =
                repositories.list({
                    ...options,
                    search:
                        query
                });

            return results.map(
                repo => ({
                    type:
                        "repository",

                    id:
                        repo.id,

                    name:
                        repo.name,

                    full_name:
                        repo.full_name,

                    description:
                        repo.description,

                    owner:
                        repo.owner,

                    visibility:
                        repo.visibility,

                    language:
                        repo.language,

                    topics:
                        repo.topics,

                    stars:
                        repo.stats.stars,

                    forks:
                        repo.stats.forks,

                    watchers:
                        repo.stats.watchers
                })
            );
        }
    };

    /* =========================================================
       4.15 — CARD VISUAL
       ========================================================= */

    const ui = {

        card(repoId) {

            const repo =
                repositories.get(
                    repoId
                );

            if (!repo) {

                return `
                    <div
                        class="nrh4-empty"
                    >
                        Repositório não encontrado.
                    </div>
                `;
            }

            const visibilityIcon =
                repo.visibility ===
                "private"
                    ? "🔒"
                    : "🌐";

            const topics =
                (
                    repo.topics || []
                )
                .slice(0, 6)
                .map(
                    topic =>
                        `
                        <span
                            class="nrh4-topic"
                        >
                            ${escapeHTML(
                                topic
                            )}
                        </span>
                        `
                )
                .join("");

            return `
                <article
                    class="nrh4-repository-card"
                    data-repository-id="${escapeHTML(
                        repo.id
                    )}"
                >

                    <header>

                        <div>

                            <div
                                class="nrh4-repo-name"
                            >
                                ${escapeHTML(
                                    repo.full_name
                                )}
                            </div>

                            <div
                                class="nrh4-repo-visibility"
                            >
                                ${visibilityIcon}
                                ${escapeHTML(
                                    repo.visibility
                                )}
                            </div>

                        </div>

                        ${
                            repo.archived
                                ? `
                                    <span>
                                        ARCHIVED
                                    </span>
                                `
                                : ""
                        }

                    </header>

                    <p>
                        ${escapeHTML(
                            repo.description ||
                            "Sem descrição."
                        )}
                    </p>

                    <div
                        class="nrh4-topics"
                    >
                        ${topics}
                    </div>

                    <footer>

                        <span>
                            ★
                            ${repo.stats.stars}
                        </span>

                        <span>
                            ◉
                            ${repo.stats.watchers}
                        </span>

                        <span>
                            ⑂
                            ${repo.stats.forks}
                        </span>

                        ${
                            repo.language
                                ? `
                                    <span>
                                        ●
                                        ${escapeHTML(
                                            repo.language
                                        )}
                                    </span>
                                `
                                : ""
                        }

                    </footer>

                </article>
            `;
        },

        list(list) {

            return (
                Array.isArray(list)
                    ? list
                    : []
            )
            .map(
                repo =>
                    this.card(
                        repo.id
                    )
            )
            .join("");
        }
    };

    /* =========================================================
       4.16 — COMPATIBILIDADE COM NRH2
       ========================================================= */

    /*
     * Não substituímos NRH2.repositories.
     *
     * Em vez disso, adicionamos métodos que permitem
     * que módulos futuros descubram a implementação
     * avançada do NRH4.
     */

    if (
        NRH2.repositories
    ) {

        NRH2.repositories.advanced =
            repositories;

        NRH2.repositories.stars =
            stars;

        NRH2.repositories.watchers =
            watchers;

        NRH2.repositories.forks =
            forks;

        NRH2.repositories.topics =
            topics;

        NRH2.repositories.templates =
            templates;

        NRH2.repositories.archive =
            archive;

        NRH2.repositories.visibility =
            visibility;
    }

    /* =========================================================
       4.17 — COMANDOS
       ========================================================= */

    if (
        NRH2.commands &&
        typeof NRH2.commands.register ===
            "function"
    ) {

        NRH2.commands.register({

            id:
                "repository:search",

            label:
                "Pesquisar repositórios",

            description:
                "Pesquisa repositórios pelo nome, descrição ou tópico.",

            keywords: [
                "repo",
                "repository",
                "repositório",
                "search",
                "pesquisa"
            ],

            run(args) {

                const query =
                    args &&
                    args.length
                        ? args.join(" ")
                        : "";

                return search
                    .repositories(
                        query
                    );
            }
        });

        NRH2.commands.register({

            id:
                "repository:star",

            label:
                "Favoritar repositório",

            description:
                "Adiciona uma estrela ao repositório.",

            keywords: [
                "star",
                "estrela",
                "favorite"
            ],

            run(args) {

                if (
                    !args ||
                    !args[0]
                ) {
                    throw new Error(
                        "Informe o repositório."
                    );
                }

                const login =
                    NRH2.auth &&
                    typeof NRH2.auth.current ===
                        "function"
                        ? NRH2.auth.current()
                        : "raphael";

                return stars.add(
                    args[0],
                    login
                );
            }
        });

        NRH2.commands.register({

            id:
                "repository:fork",

            label:
                "Criar fork",

            description:
                "Cria uma cópia derivada do repositório.",

            keywords: [
                "fork",
                "clone",
                "copy"
            ],

            run(args) {

                const login =
                    NRH2.auth &&
                    typeof NRH2.auth.current ===
                        "function"
                        ? NRH2.auth.current()
                        : "raphael";

                return forks.create(
                    args[0],
                    login
                );
            }
        });
    }

    /* =========================================================
       4.18 — EVENTOS
       ========================================================= */

    if (
        typeof NRH2.on ===
        "function"
    ) {

        NRH2.on(
            "repository:created",
            payload => {

                if (
                    payload &&
                    payload.repository
                ) {

                    statistics.calculate(
                        payload.repository.id
                    );
                }
            }
        );

        NRH2.on(
            "repository:forked",
            payload => {

                emit(
                    "activity:repository_fork",
                    payload
                );
            }
        );

        NRH2.on(
            "repository:starred",
            payload => {

                emit(
                    "activity:repository_star",
                    payload
                );
            }
        );
    }

    /* =========================================================
       4.19 — SEED DE REPOSITÓRIO
       ========================================================= */

    function seedRepository() {

        const existing =
            repositories.find(
                "raphael/neural-raphael-hub"
            );

        if (existing) {
            return existing;
        }

        try {

            return repositories.create({

                name:
                    "neural-raphael-hub",

                owner:
                    "raphael",

                description:
                    "Plataforma modular de desenvolvimento colaborativo Neural Raphael Hub.",

                visibility:
                    "public",

                language:
                    "JavaScript",

                topics: [
                    "javascript",
                    "html",
                    "css",
                    "ai",
                    "github",
                    "collaboration",
                    "neural-raphael"
                ],

                files: {

                    "README.md":
                        "# Neural Raphael Hub\n\n" +
                        "Plataforma modular de desenvolvimento.\n",

                    "index.html":
                        "<!DOCTYPE html>\n" +
                        "<html lang=\"pt-BR\">\n" +
                        "<head>\n" +
                        "  <meta charset=\"UTF-8\">\n" +
                        "  <title>Neural Raphael Hub</title>\n" +
                        "</head>\n" +
                        "<body>\n" +
                        "  <h1>Neural Raphael Hub</h1>\n" +
                        "</body>\n" +
                        "</html>\n"
                }
            });

        } catch (error) {

            console.warn(
                "[NRH4] Seed não criado:",
                error
            );

            return null;
        }
    }

    /* =========================================================
       4.20 — API PÚBLICA
       ========================================================= */

    const NRH4 = {

        VERSION,

        state,

        repositories,

        stars,

        watchers,

        forks,

        topics,

        collaborators:
            repositoryCollaborators,

        templates,

        archive,

        visibility,

        access,

        statistics,

        search,

        ui,

        seed:
            seedRepository,

        init() {

            const repo =
                seedRepository();

            emit(
                "nrh4:ready",
                {
                    version:
                        VERSION,

                    repository:
                        repo
                            ? repo.id
                            : null
                }
            );

            console.log(
                "%c[NRH4] Advanced Repository Engine " +
                VERSION +
                " carregado.",
                "color:#3fb950;font-weight:bold"
            );

            return this;
        }
    };

    /* =========================================================
       4.21 — EXPORTAÇÃO GLOBAL
       ========================================================= */

    global.NRH4 =
        NRH4;

    /*
     * Inicialização.
     */

    NRH4.init();

})(window);

/* ============================================================
   FIM DO BLOCO 4
   ============================================================ */
</script>
<script>
/* ============================================================
   NEURAL RAPHAEL HUB
   BLOCO 5 — GIT ENGINE
   ------------------------------------------------------------
   Dependências:
     BLOCO 1 — Núcleo original
     BLOCO 2 — NRH2
     BLOCO 3 — NRH3
     BLOCO 4 — NRH4

   Objetivo:
     - objetos Git
     - blobs
     - trees
     - commits
     - branches
     - tags
     - refs
     - histórico
     - diff
     - comparação
     - merge
     - blame
     - checkout interno

   Namespace:
     NRH5
   ============================================================ */

(function (global) {
    "use strict";

    if (!global.NRH2) {
        console.error("[NRH5] NRH2 não encontrado.");
        return;
    }

    if (!global.NRH3) {
        console.error("[NRH5] NRH3 não encontrado.");
        return;
    }

    if (!global.NRH4) {
        console.error("[NRH5] NRH4 não encontrado.");
        return;
    }

    const NRH2 = global.NRH2;
    const NRH3 = global.NRH3;
    const NRH4 = global.NRH4;

    const VERSION = "5.0.0";

    const state =
        NRH2.store &&
        NRH2.store.state
            ? NRH2.store.state
            : null;

    if (!state) {
        console.error(
            "[NRH5] Estado global não encontrado."
        );
        return;
    }

    /* =========================================================
       5.1 — ESTADO GIT
       ========================================================= */

    state.gitObjects =
        state.gitObjects || {};

    state.gitRefs =
        state.gitRefs || {};

    state.gitCommits =
        state.gitCommits || {};

    state.gitTrees =
        state.gitTrees || {};

    state.gitBlobs =
        state.gitBlobs || {};

    state.gitTags =
        state.gitTags || {};

    state.gitReflogs =
        state.gitReflogs || {};

    state.gitIndexes =
        state.gitIndexes || {};

    state.gitRemotes =
        state.gitRemotes || {};

    /* =========================================================
       5.2 — UTILIDADES
       ========================================================= */

    function now() {
        return new Date().toISOString();
    }

    function uid(prefix) {
        return (
            String(prefix || "id") +
            "_" +
            Date.now().toString(36) +
            "_" +
            Math.random()
                .toString(36)
                .slice(2, 12)
        );
    }

    function clone(value) {
        try {
            return JSON.parse(
                JSON.stringify(value)
            );
        } catch (error) {
            return value;
        }
    }

    function normalize(value) {
        return String(value || "")
            .trim()
            .toLowerCase();
    }

    function emit(event, payload) {
        if (
            typeof NRH2.emit ===
            "function"
        ) {
            NRH2.emit(
                event,
                payload
            );
        }
    }

    function save() {
        if (
            NRH2.persistence &&
            typeof NRH2.persistence.save ===
                "function"
        ) {
            NRH2.persistence.save();
        }
    }

    function escapeHTML(value) {
        return String(
            value == null ? "" : value
        )
        .replace(/&/g, "&amp;")
        .replace(/</g, "&lt;")
        .replace(/>/g, "&gt;")
        .replace(/"/g, "&quot;")
        .replace(/'/g, "&#039;");
    }

    /*
     * SHA-1 assíncrono via Web Crypto.
     *
     * Existe também o fallback determinístico abaixo,
     * pois o sistema pode estar sendo executado em ambiente
     * local onde crypto.subtle não esteja disponível.
     */

    async function sha1(text) {

        const input =
            String(text);

        if (
            global.crypto &&
            global.crypto.subtle &&
            typeof global.crypto.subtle.digest ===
                "function"
        ) {

            const data =
                new TextEncoder()
                    .encode(input);

            const hash =
                await global.crypto.subtle
                    .digest(
                        "SHA-1",
                        data
                    );

            return Array
                .from(
                    new Uint8Array(hash)
                )
                .map(
                    byte =>
                        byte
                            .toString(16)
                            .padStart(
                                2,
                                "0"
                            )
                )
                .join("");
        }

        return fallbackHash(input);
    }

    /*
     * Fallback não criptográfico.
     * Serve somente para manter o motor funcional.
     */
    function fallbackHash(text) {

        let h1 =
            0x811c9dc5;

        let h2 =
            0x01000193;

        for (
            let i = 0;
            i < text.length;
            i++
        ) {

            const code =
                text.charCodeAt(i);

            h1 ^=
                code;

            h1 =
                Math.imul(
                    h1,
                    16777619
                );

            h2 ^=
                code + i;

            h2 =
                Math.imul(
                    h2,
                    2246822519
                );
        }

        let result =
            (
                h1 >>> 0
            )
            .toString(16)
            .padStart(
                8,
                "0"
            );

        result +=
            (
                h2 >>> 0
            )
            .toString(16)
            .padStart(
                8,
                "0"
            );

        while (
            result.length < 40
        ) {
            result +=
                result;
        }

        return result.slice(
            0,
            40
        );
    }

    async function gitHash(
        type,
        content
    ) {

        const body =
            typeof content ===
                "string"
                ? content
                : JSON.stringify(
                    content
                );

        const header =
            type +
            " " +
            body.length +
            "\0";

        return sha1(
            header +
            body
        );
    }

    /* =========================================================
       5.3 — OBJETOS GIT
       ========================================================= */

    const objects = {

        async write(
            type,
            content,
            metadata
        ) {

            const body =
                typeof content ===
                    "string"
                    ? content
                    : JSON.stringify(
                        content
                    );

            const sha =
                await gitHash(
                    type,
                    body
                );

            const object = {

                sha,

                type,

                size:
                    body.length,

                content:
                    body,

                metadata:
                    clone(
                        metadata || {}
                    ),

                createdAt:
                    now()
            };

            /*
             * Objetos Git são tratados como
             * imutáveis depois de criados.
             */

            if (
                !state.gitObjects[sha]
            ) {

                state.gitObjects[
                    sha
                ] = object;
            }

            if (
                type === "blob"
            ) {

                state.gitBlobs[
                    sha
                ] = object;
            }

            if (
                type === "tree"
            ) {

                state.gitTrees[
                    sha
                ] = object;
            }

            if (
                type === "commit"
            ) {

                state.gitCommits[
                    sha
                ] = object;
            }

            emit(
                "git:object_created",
                {
                    sha,
                    type
                }
            );

            save();

            return sha;
        },

        get(sha) {

            return state.gitObjects[
                sha
            ]
                ? clone(
                    state.gitObjects[
                        sha
                    ]
                )
                : null;
        },

        exists(sha) {

            return Boolean(
                state.gitObjects[
                    sha
                ]
            );
        },

        remove(sha) {

            /*
             * Objetos não devem ser removidos
             * normalmente. Esta função existe apenas
             * para manutenção de banco local.
             */

            if (
                !state.gitObjects[
                    sha
                ]
            ) {
                return false;
            }

            delete state.gitObjects[
                sha
            ];

            delete state.gitBlobs[
                sha
            ];

            delete state.gitTrees[
                sha
            ];

            delete state.gitCommits[
                sha
            ];

            save();

            return true;
        }
    };

    /* =========================================================
       5.4 — BLOBS
       ========================================================= */

    const blobs = {

        async create(
            content,
            metadata
        ) {

            return objects.write(
                "blob",
                String(
                    content == null
                        ? ""
                        : content
                ),
                metadata
            );
        },

        read(sha) {

            const object =
                objects.get(
                    sha
                );

            if (
                !object ||
                object.type !==
                    "blob"
            ) {
                return null;
            }

            return object.content;
        },

        exists(sha) {

            const object =
                objects.get(
                    sha
                );

            return Boolean(
                object &&
                object.type ===
                    "blob"
            );
        }
    };

    /* =========================================================
       5.5 — TREES
       ========================================================= */

    const trees = {

        async create(
            entries
        ) {

            entries =
                Array.isArray(entries)
                    ? entries
                    : [];

            const normalized =
                entries
                    .map(entry => ({

                        mode:
                            entry.mode ||
                            "100644",

                        type:
                            entry.type ||
                            "blob",

                        name:
                            entry.name,

                        path:
                            entry.path ||
                            entry.name,

                        sha:
                            entry.sha,

                        size:
                            Number(
                                entry.size ||
                                0
                            )
                    }))
                    .sort(
                        (a, b) =>
                            a.path.localeCompare(
                                b.path
                            )
                    );

            const sha =
                await objects.write(
                    "tree",
                    normalized
                );

            return sha;
        },

        get(sha) {

            const object =
                objects.get(
                    sha
                );

            if (
                !object ||
                object.type !==
                    "tree"
            ) {
                return null;
            }

            try {

                return JSON.parse(
                    object.content
                );

            } catch (error) {

                return [];
            }
        },

        async fromFiles(
            files
        ) {

            files =
                files || {};

            const entries = [];

            for (
                const path of
                Object.keys(files)
            ) {

                const content =
                    files[path];

                const blobSha =
                    await blobs.create(
                        content,
                        {
                            path
                        }
                    );

                entries.push({

                    mode:
                        "100644",

                    type:
                        "blob",

                    name:
                        path
                            .split("/")
                            .pop(),

                    path,

                    sha:
                        blobSha,

                    size:
                        String(
                            content == null
                                ? ""
                                : content
                        ).length
                });
            }

            return this.create(
                entries
            );
        },

        files(sha) {

            const tree =
                this.get(
                    sha
                );

            if (!tree) {
                return {};
            }

            const result = {};

            tree.forEach(
                entry => {

                    if (
                        entry.type ===
                        "blob"
                    ) {

                        const content =
                            blobs.read(
                                entry.sha
                            );

                        result[
                            entry.path
                        ] =
                            content == null
                                ? ""
                                : content;
                    }
                }
            );

            return result;
        }
    };

    /* =========================================================
       5.6 — COMMITS
       ========================================================= */

    const commits = {

        async create(data) {

            data =
                data || {};

            const message =
                String(
                    data.message ||
                    ""
                ).trim();

            if (!message) {
                throw new Error(
                    "Mensagem do commit é obrigatória."
                );
            }

            let treeSha =
                data.tree;

            if (
                !treeSha &&
                data.files
            ) {

                treeSha =
                    await trees.fromFiles(
                        data.files
                    );
            }

            if (!treeSha) {
                throw new Error(
                    "Tree do commit não encontrada."
                );
            }

            const parents =
                Array.isArray(
                    data.parents
                )
                    ? [
                        ...data.parents
                    ]
                    : data.parent
                        ? [
                            data.parent
                        ]
                        : [];

            const author =
                data.author ||
                "raphael";

            const committer =
                data.committer ||
                author;

            const authorUser =
                NRH3.users.get(
                    author
                );

            const commitData = {

                tree:
                    treeSha,

                parents,

                message,

                author: {

                    name:
                        authorUser
                            ? authorUser.name
                            : author,

                    login:
                        authorUser
                            ? authorUser.login
                            : author,

                    email:
                        authorUser
                            ? authorUser.email
                            : "",

                    date:
                        data.authorDate ||
                        now()
                },

                committer: {

                    name:
                        authorUser
                            ? authorUser.name
                            : committer,

                    login:
                        authorUser
                            ? authorUser.login
                            : committer,

                    email:
                        authorUser
                            ? authorUser.email
                            : "",

                    date:
                        data.committerDate ||
                        now()
                },

                signature:
                    data.signature ||
                    null,

                verification: {

                    verified:
                        Boolean(
                            data.verified
                        ),

                    reason:
                        data.verified
                            ? "valid"
                            : "unsigned"
                }
            };

            const sha =
                await objects.write(
                    "commit",
                    commitData
                );

            state.gitCommits[
                sha
            ] = {

                sha,

                ...commitData,

                createdAt:
                    now()
            };

            emit(
                "git:commit_created",
                {
                    sha,
                    commit:
                        clone(
                            state.gitCommits[
                                sha
                            ]
                        )
                }
            );

            save();

            return sha;
        },

        get(sha) {

            return state.gitCommits[
                sha
            ]
                ? clone(
                    state.gitCommits[
                        sha
                    ]
                )
                : null;
        },

        shortSha(sha) {

            return String(
                sha || ""
            )
            .slice(
                0,
                7
            );
        },

        message(sha) {

            const commit =
                this.get(
                    sha
                );

            return commit
                ? commit.message
                : "";
        },

        parents(sha) {

            const commit =
                this.get(
                    sha
                );

            return commit
                ? clone(
                    commit.parents ||
                    []
                )
                : [];
        }
    };

    /* =========================================================
       5.7 — REPOSITORY GIT STATE
       ========================================================= */

    function repoKey(repo) {

        return (
            repo.id ||
            repo.full_name ||
            repo.slug
        );
    }

    function ensureGitState(
        repo
    ) {

        if (!repo) {
            throw new Error(
                "Repositório inválido."
            );
        }

        const key =
            repoKey(repo);

        repo.git =
            repo.git || {};

        repo.git.refs =
            repo.git.refs || {};

        repo.git.branches =
            repo.git.branches || {};

        repo.git.tags =
            repo.git.tags || {};

        repo.git.head =
            repo.git.head ||
            "refs/heads/" +
            (
                repo.default_branch ||
                "main"
            );

        repo.git.initialized =
            Boolean(
                repo.git.initialized
            );

        if (
            !repo.git.initialized
        ) {

            const branch =
                repo.default_branch ||
                "main";

            repo.git.branches[
                branch
            ] = {

                name:
                    branch,

                protected:
                    false,

                upstream:
                    null,

                head:
                    null,

                createdAt:
                    now()
            };

            repo.git.refs[
                "refs/heads/" +
                branch
            ] = null;

            repo.git.initialized =
                true;
        }

        state.gitRefs[
            key
        ] =
            repo.git.refs;

        return repo;
    }

    /* =========================================================
       5.8 — INIT REPOSITORY
       ========================================================= */

    const git = {

        async init(repoId) {

            const repo =
                NRH4.repositories
                    .getRaw(
                        repoId
                    );

            if (!repo) {
                throw new Error(
                    "Repositório não encontrado."
                );
            }

            ensureGitState(
                repo
            );

            /*
             * Se o repositório já possuir arquivos,
             * criamos o primeiro tree/commit.
             */

            const branch =
                repo.default_branch ||
                "main";

            if (
                !repo.git.branches[
                    branch
                ].head
            ) {

                const treeSha =
                    await trees.fromFiles(
                        repo.files || {}
                    );

                const initialSha =
                    await commits.create({

                        message:
                            "Initial commit",

                        tree:
                            treeSha,

                        parents: [],

                        author:
                            repo.owner
                    });

                repo.git.branches[
                    branch
                ].head =
                    initialSha;

                repo.git.refs[
                    "refs/heads/" +
                    branch
                ] =
                    initialSha;

                repo.git.initialCommit =
                    initialSha;

                repo.git.head =
                    "refs/heads/" +
                    branch;

                repo.git.history =
                    [
                        initialSha
                    ];

                repo.stats.commits =
                    1;
            }

            repo.updatedAt =
                now();

            save();

            emit(
                "git:repository_initialized",
                {
                    repositoryId:
                        repo.id,

                    head:
                        repo.git.branches[
                            branch
                        ].head
                }
            );

            return clone(
                repo.git
            );
        },

        getHead(
            repoId,
            branch
        ) {

            const repo =
                NRH4.repositories
                    .getRaw(
                        repoId
                    );

            if (!repo) {
                return null;
            }

            ensureGitState(
                repo
            );

            branch =
                branch ||
                repo.default_branch ||
                "main";

            return (
                repo.git.branches[
                    branch
                ]
                    ? repo.git.branches[
                        branch
                    ].head
                    : null
            );
        },

        getFiles(
            repoId,
            branch
        ) {

            const head =
                this.getHead(
                    repoId,
                    branch
                );

            if (!head) {
                return {};
            }

            const commit =
                commits.get(
                    head
                );

            if (!commit) {
                return {};
            }

            return trees.files(
                commit.tree
            );
        }
    };

    /* =========================================================
       5.9 — BRANCHES
       ========================================================= */

    const branches = {

        list(repoId) {

            const repo =
                NRH4.repositories
                    .getRaw(
                        repoId
                    );

            if (!repo) {
                return [];
            }

            ensureGitState(
                repo
            );

            return Object.values(
                repo.git.branches
            )
            .map(
                branch =>
                    clone(branch)
            );
        },

        get(
            repoId,
            name
        ) {

            const repo =
                NRH4.repositories
                    .getRaw(
                        repoId
                    );

            if (!repo) {
                return null;
            }

            ensureGitState(
                repo
            );

            return repo.git.branches[
                name
            ]
                ? clone(
                    repo.git.branches[
                        name
                    ]
                )
                : null;
        },

        async create(
            repoId,
            name,
            from
        ) {

            const repo =
                NRH4.repositories
                    .getRaw(
                        repoId
                    );

            if (!repo) {
                throw new Error(
                    "Repositório não encontrado."
                );
            }

            ensureGitState(
                repo
            );

            name =
                String(name || "")
                    .trim();

            if (
                !/^[A-Za-z0-9._/-]+$/.test(
                    name
                )
            ) {
                throw new Error(
                    "Nome de branch inválido."
                );
            }

            if (
                repo.git.branches[
                    name
                ]
            ) {
                throw new Error(
                    "Branch já existe."
                );
            }

            const sourceBranch =
                from ||
                repo.default_branch ||
                "main";

            const sourceHead =
                repo.git.branches[
                    sourceBranch
                ]
                    ? repo.git.branches[
                        sourceBranch
                    ].head
                    : null;

            repo.git.branches[
                name
            ] = {

                name,

                protected:
                    false,

                upstream:
                    null,

                head:
                    sourceHead,

                createdAt:
                    now()
            };

            repo.git.refs[
                "refs/heads/" +
                name
            ] =
                sourceHead;

            emit(
                "git:branch_created",
                {
                    repositoryId:
                        repo.id,

                    branch:
                        name,

                    from:
                        sourceBranch,

                    head:
                        sourceHead
                }
            );

            save();

            return clone(
                repo.git.branches[
                    name
                ]
            );
        },

        delete(
            repoId,
            name
        ) {

            const repo =
                NRH4.repositories
                    .getRaw(
                        repoId
                    );

            if (!repo) {
                return false;
            }

            ensureGitState(
                repo
            );

            if (
                name ===
                repo.default_branch
            ) {
                throw new Error(
                    "A branch padrão não pode ser removida."
                );
            }

            if (
                !repo.git.branches[
                    name
                ]
            ) {
                return false;
            }

            delete repo.git.branches[
                name
            ];

            delete repo.git.refs[
                "refs/heads/" +
                name
            ];

            emit(
                "git:branch_deleted",
                {
                    repositoryId:
                        repo.id,

                    branch:
                        name
                }
            );

            save();

            return true;
        },

        protect(
            repoId,
            name,
            options
        ) {

            const repo =
                NRH4.repositories
                    .getRaw(
                        repoId
                    );

            if (!repo) {
                throw new Error(
                    "Repositório não encontrado."
                );
            }

            ensureGitState(
                repo
            );

            const branch =
                repo.git.branches[
                    name
                ];

            if (!branch) {
                throw new Error(
                    "Branch não encontrada."
                );
            }

            branch.protected =
                true;

            branch.protection =
                {
                    requirePullRequest:
                        true,

                    requiredApprovals:
                        Number(
                            options &&
                            options.requiredApprovals ||
                            1
                        ),

                    requireStatusChecks:
                        Boolean(
                            options &&
                            options.requireStatusChecks
                        ),

                    allowForcePush:
                        false
                };

            save();

            return clone(
                branch
            );
        }
    };

    /* =========================================================
       5.10 — COMMIT EM BRANCH
       ========================================================= */

    const history = {

        async commit(
            repoId,
            branch,
            data
        ) {

            const repo =
                NRH4.repositories
                    .getRaw(
                        repoId
                    );

            if (!repo) {
                throw new Error(
                    "Repositório não encontrado."
                );
            }

            ensureGitState(
                repo
            );

            branch =
                branch ||
                repo.default_branch ||
                "main";

            if (
                !repo.git.branches[
                    branch
                ]
            ) {
                await branches.create(
                    repo.id,
                    branch
                );
            }

            const branchData =
                repo.git.branches[
                    branch
                ];

            if (
                branchData.protected &&
                data &&
                data.force
            ) {
                throw new Error(
                    "Não é permitido force update em branch protegida."
                );
            }

            const previous =
                branchData.head;

            let files;

            if (
                data &&
                data.files
            ) {

                files =
                    clone(
                        data.files
                    );

            } else {

                files =
                    git.getFiles(
                        repo.id,
                        branch
                    );
            }

            if (
                data &&
                data.changes
            ) {

                Object.keys(
                    data.changes
                )
                .forEach(path => {

                    const change =
                        data.changes[
                            path
                        ];

                    if (
                        change ===
                        null
                    ) {

                        delete files[
                            path
                        ];

                    } else {

                        files[
                            path
                        ] =
                            String(
                                change
                            );
                    }
                });
            }

            const treeSha =
                await trees.fromFiles(
                    files
                );

            const author =
                data &&
                data.author
                    ? data.author
                    : repo.owner;

            const message =
                data &&
                data.message
                    ? data.message
                    : "Update " +
                      branch;

            const sha =
                await commits.create({

                    message,

                    tree:
                        treeSha,

                    parent:
                        previous,

                    author
                });

            branchData.head =
                sha;

            repo.git.refs[
                "refs/heads/" +
                branch
            ] =
                sha;

            repo.git.head =
                "refs/heads/" +
                branch;

            repo.git.history =
                repo.git.history ||
                [];

            repo.git.history.unshift(
                sha
            );

            /*
             * Mantém também o snapshot atual
             * compatível com o Bloco 1/4.
             */

            repo.files =
                files;

            repo.updatedAt =
                now();

            repo.pushedAt =
                now();

            repo.stats =
                repo.stats || {};

            repo.stats.commits =
                (
                    repo.stats.commits ||
                    0
                ) + 1;

            emit(
                "git:branch_updated",
                {
                    repositoryId:
                        repo.id,

                    branch,

                    sha,

                    parent:
                        previous,

                    message
                }
            );

            emit(
                "repository:commit",
                {
                    repository:
                        clone(repo),

                    sha,

                    branch,

                    message
                }
            );

            save();

            return clone(
                commits.get(
                    sha
                )
            );
        },

        list(
            repoId,
            branch,
            limit
        ) {

            const repo =
                NRH4.repositories
                    .getRaw(
                        repoId
                    );

            if (!repo) {
                return [];
            }

            ensureGitState(
                repo
            );

            branch =
                branch ||
                repo.default_branch ||
                "main";

            let sha =
                thisHead(
                    repo,
                    branch
                );

            const result = [];

            const max =
                Number(
                    limit ||
                    100
                );

            const visited =
                new Set();

            while (
                sha &&
                result.length < max &&
                !visited.has(sha)
            ) {

                visited.add(
                    sha
                );

                const commit =
                    commits.get(
                        sha
                    );

                if (!commit) {
                    break;
                }

                result.push(
                    commit
                );

                sha =
                    (
                        commit.parents ||
                        []
                    )[0] ||
                    null;
            }

            return result;
        }
    };

    function thisHead(
        repo,
        branch
    ) {

        return repo.git &&
            repo.git.branches &&
            repo.git.branches[
                branch
            ]
                ? repo.git.branches[
                    branch
                ].head
                : null;
    }

    /* =========================================================
       5.11 — TAGS
       ========================================================= */

    const tags = {

        async create(
            repoId,
            name,
            target,
            message,
            author
        ) {

            const repo =
                NRH4.repositories
                    .getRaw(
                        repoId
                    );

            if (!repo) {
                throw new Error(
                    "Repositório não encontrado."
                );
            }

            ensureGitState(
                repo
            );

            if (
                repo.git.tags[
                    name
                ]
            ) {
                throw new Error(
                    "Tag já existe."
                );
            }

            const commitSha =
                target ||
                git.getHead(
                    repo.id,
                    repo.default_branch
                );

            if (!commitSha) {
                throw new Error(
                    "Commit alvo não encontrado."
                );
            }

            const tagObject = {

                name,

                target:
                    commitSha,

                type:
                    "commit",

                message:
                    message ||
                    name,

                tagger:
                    author ||
                    repo.owner,

                date:
                    now()
            };

            const sha =
                await objects.write(
                    "tag",
                    tagObject
                );

            state.gitTags[
                sha
            ] =
                {
                    sha,
                    ...tagObject
                };

            repo.git.tags[
                name
            ] =
                {
                    name,
                    sha,
                    target:
                        commitSha,
                    createdAt:
                        now()
                };

            repo.git.refs[
                "refs/tags/" +
                name
            ] =
                commitSha;

            emit(
                "git:tag_created",
                {
                    repositoryId:
                        repo.id,

                    name,

                    sha,

                    target:
                        commitSha
                }
            );

            save();

            return clone(
                repo.git.tags[
                    name
                ]
            );
        },

        list(repoId) {

            const repo =
                NRH4.repositories
                    .getRaw(
                        repoId
                    );

            if (!repo) {
                return [];
            }

            ensureGitState(
                repo
            );

            return Object.values(
                repo.git.tags
            )
            .map(
                clone
            );
        },

        get(
            repoId,
            name
        ) {

            const repo =
                NRH4.repositories
                    .getRaw(
                        repoId
                    );

            if (!repo) {
                return null;
            }

            ensureGitState(
                repo
            );

            return repo.git.tags[
                name
            ]
                ? clone(
                    repo.git.tags[
                        name
                    ]
                )
                : null;
        }
    };

    /* =========================================================
       5.12 — REF MANAGEMENT
       ========================================================= */

    const refs = {

        get(
            repoId,
            ref
        ) {

            const repo =
                NRH4.repositories
                    .getRaw(
                        repoId
                    );

            if (!repo) {
                return null;
            }

            ensureGitState(
                repo
            );

            return (
                repo.git.refs[
                    ref
                ] ||
                null
            );
        },

        list(
            repoId
        ) {

            const repo =
                NRH4.repositories
                    .getRaw(
                        repoId
                    );

            if (!repo) {
                return {};
            }

            ensureGitState(
                repo
            );

            return clone(
                repo.git.refs
            );
        },

        update(
            repoId,
            ref,
            sha
        ) {

            const repo =
                NRH4.repositories
                    .getRaw(
                        repoId
                    );

            if (!repo) {
                throw new Error(
                    "Repositório não encontrado."
                );
            }

            ensureGitState(
                repo
            );

            const old =
                repo.git.refs[
                    ref
                ] || null;

            repo.git.refs[
                ref
            ] =
                sha;

            state.gitReflogs[
                repo.id
            ] =
                state.gitReflogs[
                    repo.id
                ] || [];

            state.gitReflogs[
                repo.id
            ].push({

                ref,

                old,

                new:
                    sha,

                timestamp:
                    now()
            });

            emit(
                "git:ref_updated",
                {
                    repositoryId:
                        repo.id,

                    ref,

                    old,

                    new:
                        sha
                }
            );

            save();

            return sha;
        }
    };

    /* =========================================================
       5.13 — DIFF
       ========================================================= */

    function diffLines(
        oldText,
        newText
    ) {

        const oldLines =
            String(
                oldText || ""
            ).split("\n");

        const newLines =
            String(
                newText || ""
            ).split("\n");

        const n =
            oldLines.length;

        const m =
            newLines.length;

        /*
         * LCS.
         */

        const matrix =
            Array.from(
                {
                    length:
                        n + 1
                },
                () =>
                    Array(
                        m + 1
                    ).fill(0)
            );

        for (
            let i = n - 1;
            i >= 0;
            i--
        ) {

            for (
                let j = m - 1;
                j >= 0;
                j--
            ) {

                matrix[i][j] =
                    oldLines[i] ===
                    newLines[j]
                        ? matrix[i + 1][j + 1] + 1
                        : Math.max(
                            matrix[i + 1][j],
                            matrix[i][j + 1]
                        );
            }
        }

        const result = [];

        let i = 0;
        let j = 0;

        while (
            i < n &&
            j < m
        ) {

            if (
                oldLines[i] ===
                newLines[j]
            ) {

                result.push({
                    type:
                        "context",

                    line:
                        oldLines[i],

                    oldLine:
                        i + 1,

                    newLine:
                        j + 1
                });

                i++;
                j++;

            } else if (
                matrix[i + 1][j] >=
                matrix[i][j + 1]
            ) {

                result.push({
                    type:
                        "remove",

                    line:
                        oldLines[i],

                    oldLine:
                        i + 1,

                    newLine:
                        null
                });

                i++;

            } else {

                result.push({
                    type:
                        "add",

                    line:
                        newLines[j],

                    oldLine:
                        null,

                    newLine:
                        j + 1
                });

                j++;
            }
        }

        while (
            i < n
        ) {

            result.push({
                type:
                    "remove",

                line:
                    oldLines[i],

                oldLine:
                    i + 1,

                newLine:
                    null
            });

            i++;
        }

        while (
            j < m
        ) {

            result.push({
                type:
                    "add",

                line:
                    newLines[j],

                oldLine:
                    null,

                newLine:
                    j + 1
            });

            j++;
        }

        return result;
    }

    const diff = {

        file(
            oldText,
            newText
        ) {

            return diffLines(
                oldText,
                newText
            );
        },

        files(
            oldFiles,
            newFiles
        ) {

            oldFiles =
                oldFiles || {};

            newFiles =
                newFiles || {};

            const paths =
                [
                    ...new Set([
                        ...Object.keys(
                            oldFiles
                        ),
                        ...Object.keys(
                            newFiles
                        )
                    ])
                ]
                .sort();

            const result = [];

            paths.forEach(
                path => {

                    const existsOld =
                        Object.prototype
                            .hasOwnProperty
                            .call(
                                oldFiles,
                                path
                            );

                    const existsNew =
                        Object.prototype
                            .hasOwnProperty
                            .call(
                                newFiles,
                                path
                            );

                    if (
                        !existsOld
                    ) {

                        result.push({
                            path,

                            status:
                                "added",

                            additions:
                                String(
                                    newFiles[
                                        path
                                    ] || ""
                                )
                                .split("\n")
                                .length,

                            deletions:
                                0,

                            patch:
                                diffLines(
                                    "",
                                    newFiles[
                                        path
                                    ]
                                )
                        });

                        return;
                    }

                    if (
                        !existsNew
                    ) {

                        result.push({
                            path,

                            status:
                                "removed",

                            additions:
                                0,

                            deletions:
                                String(
                                    oldFiles[
                                        path
                                    ] || ""
                                )
                                .split("\n")
                                .length,

                            patch:
                                diffLines(
                                    oldFiles[
                                        path
                                    ],
                                    ""
                                )
                        });

                        return;
                    }

                    if (
                        String(
                            oldFiles[path]
                        ) ===
                        String(
                            newFiles[path]
                        )
                    ) {
                        return;
                    }

                    const patch =
                        diffLines(
                            oldFiles[path],
                            newFiles[path]
                        );

                    const additions =
                        patch.filter(
                            x =>
                                x.type ===
                                "add"
                        ).length;

                    const deletions =
                        patch.filter(
                            x =>
                                x.type ===
                                "remove"
                        ).length;

                    result.push({

                        path,

                        status:
                            "modified",

                        additions,

                        deletions,

                        changes:
                            additions +
                            deletions,

                        patch
                    });
                }
            );

            return result;
        }
    };

    /* =========================================================
       5.14 — COMPARE COMMITS / BRANCHES
       ========================================================= */

    const compare = {

        files(
            repoId,
            base,
            head
        ) {

            const baseCommit =
                resolveRef(
                    repoId,
                    base
                );

            const headCommit =
                resolveRef(
                    repoId,
                    head
                );

            if (
                !baseCommit ||
                !headCommit
            ) {

                throw new Error(
                    "Base ou head não encontrado."
                );
            }

            const baseData =
                commits.get(
                    baseCommit
                );

            const headData =
                commits.get(
                    headCommit
                );

            if (
                !baseData ||
                !headData
            ) {

                throw new Error(
                    "Commit de comparação não encontrado."
                );
            }

            const baseFiles =
                trees.files(
                    baseData.tree
                );

            const headFiles =
                trees.files(
                    headData.tree
                );

            const changed =
                diff.files(
                    baseFiles,
                    headFiles
                );

            return {

                base:
                    baseCommit,

                head:
                    headCommit,

                files:
                    changed,

                additions:
                    changed.reduce(
                        (
                            total,
                            file
                        ) =>
                            total +
                            (
                                file.additions ||
                                0
                            ),
                        0
                    ),

                deletions:
                    changed.reduce(
                        (
                            total,
                            file
                        ) =>
                            total +
                            (
                                file.deletions ||
                                0
                            ),
                        0
                    ),

                total:
                    changed.length
            };
        },

        commits(
            repoId,
            base,
            head
        ) {

            const baseSha =
                resolveRef(
                    repoId,
                    base
                );

            const headSha =
                resolveRef(
                    repoId,
                    head
                );

            if (
                !baseSha ||
                !headSha
            ) {
                return [];
            }

            const baseSet =
                collectAncestors(
                    baseSha
                );

            const result = [];

            let current =
                headSha;

            const visited =
                new Set();

            while (
                current &&
                !visited.has(
                    current
                )
            ) {

                visited.add(
                    current
                );

                if (
                    current ===
                    baseSha
                ) {
                    break;
                }

                if (
                    !baseSet.has(
                        current
                    )
                ) {

                    const commit =
                        commits.get(
                            current
                        );

                    if (commit) {
                        result.push(
                            commit
                        );
                    }
                }

                const commit =
                    commits.get(
                        current
                    );

                current =
                    commit &&
                    commit.parents &&
                    commit.parents[0]
                        ? commit.parents[0]
                        : null;
            }

            return result;
        }
    };

    function resolveRef(
        repoId,
        ref
    ) {

        const repo =
            NRH4.repositories
                .getRaw(
                    repoId
                );

        if (!repo) {
            return null;
        }

        ensureGitState(
            repo
        );

        if (
            state.gitCommits[
                ref
            ]
        ) {
            return ref;
        }

        if (
            repo.git.refs[
                ref
            ]
        ) {
            return repo.git.refs[
                ref
            ];
        }

        if (
            ref.startsWith(
                "refs/"
            )
        ) {
            return (
                repo.git.refs[
                    ref
                ] ||
                null
            );
        }

        if (
            repo.git.branches[
                ref
            ]
        ) {
            return repo.git.branches[
                ref
            ].head;
        }

        if (
            repo.git.tags[
                ref
            ]
        ) {
            return repo.git.tags[
                ref
            ].target;
        }

        const found =
            Object.keys(
                state.gitCommits
            )
            .find(
                sha =>
                    sha.startsWith(
                        ref
                    )
            );

        return found ||
            null;
    }

    function collectAncestors(
        sha
    ) {

        const set =
            new Set();

        const queue =
            [sha];

        while (
            queue.length
        ) {

            const current =
                queue.shift();

            if (
                !current ||
                set.has(current)
            ) {
                continue;
            }

            set.add(
                current
            );

            const commit =
                commits.get(
                    current
                );

            if (
                commit &&
                Array.isArray(
                    commit.parents
                )
            ) {

                commit.parents
                    .forEach(
                        parent =>
                            queue.push(
                                parent
                            )
                    );
            }
        }

        return set;
    }

    /* =========================================================
       5.15 — MERGE BASE
       ========================================================= */

    const mergeBase = {

        find(
            repoId,
            left,
            right
        ) {

            const leftSha =
                resolveRef(
                    repoId,
                    left
                );

            const rightSha =
                resolveRef(
                    repoId,
                    right
                );

            if (
                !leftSha ||
                !rightSha
            ) {
                return null;
            }

            const leftAncestors =
                collectAncestors(
                    leftSha
                );

            const queue =
                [rightSha];

            const visited =
                new Set();

            while (
                queue.length
            ) {

                const current =
                    queue.shift();

                if (
                    !current ||
                    visited.has(
                        current
                    )
                ) {
                    continue;
                }

                visited.add(
                    current
                );

                if (
                    leftAncestors.has(
                        current
                    )
                ) {
                    return current;
                }

                const commit =
                    commits.get(
                        current
                    );

                if (
                    commit &&
                    commit.parents
                ) {

                    commit.parents
                        .forEach(
                            parent =>
                                queue.push(
                                    parent
                                )
                        );
                }
            }

            return null;
        }
    };

    /* =========================================================
       5.16 — MERGE
       ========================================================= */

    const merge = {

        async branches(
            repoId,
            baseBranch,
            headBranch,
            options
        ) {

            options =
                options || {};

            const repo =
                NRH4.repositories
                    .getRaw(
                        repoId
                    );

            if (!repo) {
                throw new Error(
                    "Repositório não encontrado."
                );
            }

            ensureGitState(
                repo
            );

            const base =
                branches.get(
                    repo.id,
                    baseBranch
                );

            const head =
                branches.get(
                    repo.id,
                    headBranch
                );

            if (
                !base ||
                !head
            ) {
                throw new Error(
                    "Branch não encontrada."
                );
            }

            if (
                base.protected &&
                options.allowProtected !== true
            ) {

                /*
                 * Proteção pode ser usada futuramente
                 * pelo sistema de Pull Requests.
                 */

                if (
                    options.pullRequest !== true
                ) {
                    throw new Error(
                        "Branch protegida requer fluxo de Pull Request."
                    );
                }
            }

            const baseSha =
                base.head;

            const headSha =
                head.head;

            if (
                baseSha ===
                headSha
            ) {

                return {
                    status:
                        "up_to_date",

                    sha:
                        baseSha,

                    conflicts:
                        []
                };
            }

            const baseCommit =
                commits.get(
                    baseSha
                );

            const headCommit =
                commits.get(
                    headSha
                );

            const baseFiles =
                baseCommit
                    ? trees.files(
                        baseCommit.tree
                    )
                    : {};

            const headFiles =
                headCommit
                    ? trees.files(
                        headCommit.tree
                    )
                    : {};

            const mergeResult =
                threeWayMerge(
                    baseFiles,
                    baseFiles,
                    headFiles
                );

            if (
                mergeResult.conflicts.length
            ) {

                return {

                    status:
                        "conflict",

                    base:
                        baseSha,

                    head:
                        headSha,

                    conflicts:
                        mergeResult.conflicts,

                    files:
                        mergeResult.files
                };
            }

            const treeSha =
                await trees.fromFiles(
                    mergeResult.files
                );

            const message =
                options.message ||
                "Merge " +
                headBranch +
                " into " +
                baseBranch;

            const sha =
                await commits.create({

                    message,

                    tree:
                        treeSha,

                    parents:
                        [
                            baseSha,
                            headSha
                        ],

                    author:
                        options.author ||
                        repo.owner
                });

            base.head =
                sha;

            repo.git.refs[
                "refs/heads/" +
                baseBranch
            ] =
                sha;

            repo.files =
                mergeResult.files;

            repo.stats =
                repo.stats || {};

            repo.stats.commits =
                (
                    repo.stats.commits ||
                    0
                ) + 1;

            repo.updatedAt =
                now();

            emit(
                "git:merged",
                {

                    repositoryId:
                        repo.id,

                    base:
                        baseBranch,

                    head:
                        headBranch,

                    sha
                }
            );

            save();

            return {

                status:
                    "merged",

                sha,

                base:
                    baseBranch,

                head:
                    headBranch,

                conflicts:
                    []
            };
        }
    };

    function threeWayMerge(
        base,
        ours,
        theirs
    ) {

        base =
            base || {};

        ours =
            ours || {};

        theirs =
            theirs || {};

        const paths =
            [
                ...new Set([
                    ...Object.keys(base),
                    ...Object.keys(ours),
                    ...Object.keys(theirs)
                ])
            ]
            .sort();

        const result = {};

        const conflicts = [];

        paths.forEach(
            path => {

                const baseValue =
                    base[path];

                const oursValue =
                    ours[path];

                const theirsValue =
                    theirs[path];

                const oursChanged =
                    String(
                        oursValue
                    ) !==
                    String(
                        baseValue
                    );

                const theirsChanged =
                    String(
                        theirsValue
                    ) !==
                    String(
                        baseValue
                    );

                if (
                    !oursChanged &&
                    !theirsChanged
                ) {

                    if (
                        oursValue !==
                        undefined
                    ) {
                        result[path] =
                            oursValue;
                    }

                    return;
                }

                if (
                    oursChanged &&
                    !theirsChanged
                ) {

                    if (
                        oursValue !==
                        undefined
                    ) {
                        result[path] =
                            oursValue;
                    }

                    return;
                }

                if (
                    !oursChanged &&
                    theirsChanged
                ) {

                    if (
                        theirsValue !==
                        undefined
                    ) {
                        result[path] =
                            theirsValue;
                    }

                    return;
                }

                if (
                    String(
                        oursValue
                    ) ===
                    String(
                        theirsValue
                    )
                ) {

                    if (
                        oursValue !==
                        undefined
                    ) {
                        result[path] =
                            oursValue;
                    }

                    return;
                }

                conflicts.push({

                    path,

                    base:
                        baseValue,

                    ours:
                        oursValue,

                    theirs:
                        theirsValue
                });
            }
        );

        return {
            files:
                result,

            conflicts
        };
    }

    /* =========================================================
       5.17 — BLAME
       ========================================================= */

    const blame = {

        file(
            repoId,
            branch,
            path
        ) {

            const repo =
                NRH4.repositories
                    .getRaw(
                        repoId
                    );

            if (!repo) {
                return [];
            }

            const log =
                history.list(
                    repo.id,
                    branch,
                    500
                );

            const lines = {};

            let currentContent =
                git.getFiles(
                    repo.id,
                    branch
                )[path];

            if (
                currentContent ==
                null
            ) {
                return [];
            }

            const currentLines =
                String(
                    currentContent
                ).split(
                    "\n"
                );

            currentLines.forEach(
                (
                    line,
                    index
                ) => {

                    lines[index] = {

                        line,

                        lineNumber:
                            index + 1,

                        commit:
                            log[0]
                                ? log[0].sha
                                : null,

                        author:
                            log[0] &&
                            log[0].author
                                ? log[0]
                                    .author
                                    .login
                                : repo.owner
                    };
                }
            );

            /*
             * Refinamento simples:
             * procura commits anteriores que alteraram
             * o arquivo.
             */

            for (
                let i = 1;
                i < log.length;
                i++
            ) {

                const commit =
                    log[i];

                const parentSha =
                    (
                        commit.parents ||
                        []
                    )[0];

                if (!parentSha) {
                    continue;
                }

                const parent =
                    commits.get(
                        parentSha
                    );

                if (!parent) {
                    continue;
                }

                const parentFiles =
                    trees.files(
                        parent.tree
                    );

                const oldContent =
                    parentFiles[
                        path
                    ];

                const oldLines =
                    String(
                        oldContent == null
                            ? ""
                            : oldContent
                    )
                    .split(
                        "\n"
                    );

                const newContent =
                    trees.files(
                        commit.tree
                    )[path];

                const newLines =
                    String(
                        newContent == null
                            ? ""
                            : newContent
                    )
                    .split(
                        "\n"
                    );

                const changes =
                    diffLines(
                        oldLines.join(
                            "\n"
                        ),
                        newLines.join(
                            "\n"
                        )
                    );

                /*
                 * Atribuição aproximada por posição.
                 */

                const changedLines =
                    changes.filter(
                        item =>
                            item.type ===
                            "add"
                    );

                changedLines.forEach(
                    item => {

                        const index =
                            (
                                item.newLine ||
                                1
                            ) - 1;

                        if (
                            lines[index]
                        ) {

                            lines[index] = {

                                ...lines[index],

                                commit:
                                    commit.sha,

                                author:
                                    commit.author
                                        ? commit.author
                                            .login
                                        : repo.owner
                            };
                        }
                    }
                );
            }

            return Object.values(
                lines
            );
        }
    };

    /* =========================================================
       5.18 — CHECKOUT
       ========================================================= */

    const checkout = {

        run(
            repoId,
            branch
        ) {

            const repo =
                NRH4.repositories
                    .getRaw(
                        repoId
                    );

            if (!repo) {
                throw new Error(
                    "Repositório não encontrado."
                );
            }

            ensureGitState(
                repo
            );

            if (
                !repo.git.branches[
                    branch
                ]
            ) {
                throw new Error(
                    "Branch não encontrada."
                );
            }

            repo.git.head =
                "refs/heads/" +
                branch;

            const files =
                git.getFiles(
                    repo.id,
                    branch
                );

            repo.files =
                clone(files);

            repo.updatedAt =
                now();

            emit(
                "git:checkout",
                {

                    repositoryId:
                        repo.id,

                    branch,

                    files:
                        clone(files)
                }
            );

            save();

            return {
                branch,

                files
            };
        }
    };

    /* =========================================================
       5.19 — REMOTES
       ========================================================= */

    const remotes = {

        add(
            repoId,
            name,
            url
        ) {

            const repo =
                NRH4.repositories
                    .getRaw(
                        repoId
                    );

            if (!repo) {
                throw new Error(
                    "Repositório não encontrado."
                );
            }

            state.gitRemotes[
                repo.id
            ] =
                state.gitRemotes[
                    repo.id
                ] || {};

            state.gitRemotes[
                repo.id
            ][name] = {

                name,

                url,

                createdAt:
                    now()
            };

            save();

            return clone(
                state.gitRemotes[
                    repo.id
                ][name]
            );
        },

        list(repoId) {

            return clone(
                state.gitRemotes[
                    repoId
                ] || {}
            );
        },

        remove(
            repoId,
            name
        ) {

            if (
                !state.gitRemotes[
                    repoId
                ]
            ) {
                return false;
            }

            if (
                !state.gitRemotes[
                    repoId
                ][name]
            ) {
                return false;
            }

            delete state.gitRemotes[
                repoId
            ][name];

            save();

            return true;
        }
    };

    /* =========================================================
       5.20 — REFLLOG
       ========================================================= */

    const reflog = {

        list(repoId) {

            return clone(
                state.gitReflogs[
                    repoId
                ] || []
            );
        },

        clear(repoId) {

            delete state.gitReflogs[
                repoId
            ];

            save();

            return true;
        }
    };

    /* =========================================================
       5.21 — RESET
       ========================================================= */

    const reset = {

        hard(
            repoId,
            branch,
            target
        ) {

            const repo =
                NRH4.repositories
                    .getRaw(
                        repoId
                    );

            if (!repo) {
                throw new Error(
                    "Repositório não encontrado."
                );
            }

            ensureGitState(
                repo
            );

            const sha =
                resolveRef(
                    repo.id,
                    target
                );

            if (!sha) {
                throw new Error(
                    "Commit alvo não encontrado."
                );
            }

            const branchData =
                repo.git.branches[
                    branch
                ];

            if (!branchData) {
                throw new Error(
                    "Branch não encontrada."
                );
            }

            const old =
                branchData.head;

            branchData.head =
                sha;

            repo.git.refs[
                "refs/heads/" +
                branch
            ] =
                sha;

            state.gitReflogs[
                repo.id
            ] =
                state.gitReflogs[
                    repo.id
                ] || [];

            state.gitReflogs[
                repo.id
            ].push({

                ref:
                    "refs/heads/" +
                    branch,

                old,

                new:
                    sha,

                timestamp:
                    now(),

                action:
                    "reset --hard"
            });

            repo.files =
                git.getFiles(
                    repo.id,
                    branch
                );

            emit(
                "git:reset",
                {

                    repositoryId:
                        repo.id,

                    branch,

                    old,

                    new:
                        sha
                }
            );

            save();

            return clone(
                branchData
            );
        }
    };

    /* =========================================================
       5.22 — SERIALIZAÇÃO
       ========================================================= */

    const serialization = {

        exportRepository(
            repoId
        ) {

            const repo =
                NRH4.repositories
                    .getRaw(
                        repoId
                    );

            if (!repo) {
                throw new Error(
                    "Repositório não encontrado."
                );
            }

            ensureGitState(
                repo
            );

            return {

                version:
                    VERSION,

                repository:
                    clone(repo),

                objects:
                    clone(
                        state.gitObjects
                    ),

                commits:
                    clone(
                        state.gitCommits
                    ),

                trees:
                    clone(
                        state.gitTrees
                    ),

                blobs:
                    clone(
                        state.gitBlobs
                    ),

                tags:
                    clone(
                        state.gitTags
                    ),

                reflog:
                    clone(
                        state.gitReflogs[
                            repo.id
                        ] || []
                    )
            };
        }
    };

    /* =========================================================
       5.23 — UI DE HISTÓRICO
       ========================================================= */

    const ui = {

        commitRow(
            commit
        ) {

            if (!commit) {
                return "";
            }

            const short =
                commits.shortSha(
                    commit.sha
                );

            const author =
                commit.author &&
                commit.author.login
                    ? commit.author.login
                    : "unknown";

            return `
                <div
                    class="nrh5-commit-row"
                    data-sha="${escapeHTML(
                        commit.sha
                    )}"
                >

                    <div
                        class="nrh5-commit-sha"
                    >
                        ${escapeHTML(
                            short
                        )}
                    </div>

                    <div
                        class="nrh5-commit-message"
                    >
                        ${escapeHTML(
                            commit.message
                        )}
                    </div>

                    <div
                        class="nrh5-commit-author"
                    >
                        ${escapeHTML(
                            author
                        )}
                    </div>

                    <div
                        class="nrh5-commit-date"
                    >
                        ${escapeHTML(
                            commit.author &&
                            commit.author.date
                                ? commit.author.date
                                : ""
                        )}
                    </div>

                </div>
            `;
        },

        history(
            repoId,
            branch,
            limit
        ) {

            const list =
                history.list(
                    repoId,
                    branch,
                    limit ||
                    50
                );

            return `
                <section
                    class="nrh5-history"
                >

                    <header>
                        <strong>
                            Histórico
                        </strong>

                        <span>
                            ${
                                list.length
                            }
                            commits
                        </span>
                    </header>

                    <div>
                        ${
                            list
                                .map(
                                    commit =>
                                        this.commitRow(
                                            commit
                                        )
                                )
                                .join("")
                        }
                    </div>

                </section>
            `;
        },

        diff(
            comparison
        ) {

            if (!comparison) {
                return "";
            }

            return `
                <section
                    class="nrh5-diff"
                >

                    <header>

                        <strong>
                            Comparação
                        </strong>

                        <span>
                            +
                            ${comparison.additions}
                            /
                            -
                            ${comparison.deletions}
                        </span>

                    </header>

                    ${
                        (
                            comparison.files ||
                            []
                        )
                        .map(
                            file =>
                                `
                                <article
                                    class="nrh5-diff-file"
                                >

                                    <h4>
                                        ${escapeHTML(
                                            file.path
                                        )}
                                    </h4>

                                    <pre>${escapeHTML(
                                        (
                                            file.patch ||
                                            []
                                        )
                                        .map(
                                            line => {

                                                const prefix =
                                                    line.type ===
                                                    "add"
                                                        ? "+"
                                                        : line.type ===
                                                          "remove"
                                                            ? "-"
                                                            : " ";

                                                return (
                                                    prefix +
                                                    line.line
                                                );
                                            }
                                        )
                                        .join(
                                            "\n"
                                        )
                                    )}</pre>

                                </article>
                                `
                        )
                        .join("")
                    }

                </section>
            `;
        }
    };

    /* =========================================================
       5.24 — COMANDOS DO NRH2
       ========================================================= */

    if (
        NRH2.commands &&
        typeof NRH2.commands.register ===
            "function"
    ) {

        NRH2.commands.register({

            id:
                "git:branches",

            label:
                "Listar branches",

            description:
                "Lista branches do repositório atual.",

            keywords: [
                "git",
                "branch",
                "branches"
            ],

            run(args) {

                return branches.list(
                    args &&
                    args[0]
                );
            }
        });

        NRH2.commands.register({

            id:
                "git:history",

            label:
                "Ver histórico Git",

            description:
                "Mostra os commits de uma branch.",

            keywords: [
                "git",
                "history",
                "commits",
                "log"
            ],

            run(args) {

                const repo =
                    args &&
                    args[0];

                const branch =
                    args &&
                    args[1];

                return history.list(
                    repo,
                    branch
                );
            }
        });

        NRH2.commands.register({

            id:
                "git:compare",

            label:
                "Comparar branches",

            description:
                "Compara duas referências Git.",

            keywords: [
                "git",
                "compare",
                "diff"
            ],

            run(args) {

                if (
                    !args ||
                    args.length < 3
                ) {

                    throw new Error(
                        "Uso: git:compare repo base head"
                    );
                }

                return compare.files(
                    args[0],
                    args[1],
                    args[2]
                );
            }
        });

        NRH2.commands.register({

            id:
                "git:checkout",

            label:
                "Trocar branch",

            description:
                "Faz checkout lógico de uma branch.",

            keywords: [
                "git",
                "checkout",
                "branch"
            ],

            run(args) {

                if (
                    !args ||
                    args.length < 2
                ) {

                    throw new Error(
                        "Uso: git:checkout repo branch"
                    );
                }

                return checkout.run(
                    args[0],
                    args[1]
                );
            }
        });
    }

    /* =========================================================
       5.25 — COMPATIBILIDADE COM NRH4
       ========================================================= */

    if (
        NRH4.repositories
    ) {

        NRH4.repositories.git =
            git;

        NRH4.repositories.branches =
            branches;

        NRH4.repositories.commits =
            commits;

        NRH4.repositories.tags =
            tags;

        NRH4.repositories.refs =
            refs;

        NRH4.repositories.history =
            history;

        NRH4.repositories.compare =
            compare;

        NRH4.repositories.merge =
            merge;

        NRH4.repositories.blame =
            blame;
    }

    /* =========================================================
       5.26 — API PÚBLICA
       ========================================================= */

    const NRH5 = {

        VERSION,

        state,

        objects,

        blobs,

        trees,

        commits,

        git,

        branches,

        history,

        tags,

        refs,

        diff,

        compare,

        mergeBase,

        merge,

        blame,

        checkout,

        remotes,

        reflog,

        reset,

        serialization,

        ui,

        init() {

            emit(
                "nrh5:ready",
                {
                    version:
                        VERSION
                }
            );

            console.log(
                "%c[NRH5] Git Engine " +
                VERSION +
                " carregado.",
                "color:#f0883e;font-weight:bold"
            );

            return this;
        }
    };

    /* =========================================================
       5.27 — EXPORTAÇÃO
       ========================================================= */

    global.NRH5 =
        NRH5;

    /* =========================================================
       5.28 — INICIALIZAÇÃO
       ========================================================= */

    NRH5.init();

})(window);

/* ============================================================
   FIM DO BLOCO 5
   ============================================================ */
</script>
<script>
/* ============================================================
   NEURAL RAPHAEL HUB
   BLOCK 6 — ISSUES ENGINE
   Version: 6.0.0
   Dependencies:
     NRH2 — Core Engine
     NRH3 — Users/Auth
     NRH4 — Repository Engine
     NRH5 — Git Engine
   ============================================================ */

const NRH6 = (() => {
  "use strict";

  const VERSION = "6.0.0";

  /* ------------------------------------------------------------
     INTERNAL STATE
     ------------------------------------------------------------ */

  const state = {
    issues: {},
    issueCounters: {},
    comments: {},
    labels: {},
    milestones: {},
    events: {},
    reactions: {},
    dependencies: {},
    watchers: {},
    locks: {},
    subscriptions: {},
    issueLinks: {}
  };

  /* ------------------------------------------------------------
     UTILITIES
     ------------------------------------------------------------ */

  function now() {
    return new Date().toISOString();
  }

  function uid(prefix = "id") {
    return (
      prefix +
      "_" +
      Math.random().toString(36).slice(2, 10) +
      "_" +
      Date.now().toString(36)
    );
  }

  function clone(value) {
    if (value === undefined) return undefined;

    try {
      return JSON.parse(JSON.stringify(value));
    } catch {
      return value;
    }
  }

  function normalize(value) {
    return String(value ?? "")
      .trim()
      .toLowerCase();
  }

  function safeString(value, fallback = "") {
    if (value === undefined || value === null) return fallback;
    return String(value);
  }

  function currentUser() {
    try {
      if (window.NRH3?.auth?.current) {
        return NRH3.auth.current();
      }

      if (window.NRH2?.auth?.current) {
        return NRH2.auth.current();
      }

      return NRH2?.store?.user || null;
    } catch {
      return null;
    }
  }

  function username() {
    const user = currentUser();

    return (
      user?.login ||
      user?.username ||
      user?.name ||
      user?.email ||
      "anonymous"
    );
  }

  function ensureArray(value) {
    return Array.isArray(value) ? value : [];
  }

  function ensureObject(value) {
    return value && typeof value === "object" ? value : {};
  }

  function emit(event, payload) {
    try {
      if (window.NRH2?.events?.emit) {
        NRH2.events.emit(event, payload);
      }
    } catch {
      /* optional integration */
    }

    try {
      window.dispatchEvent(
        new CustomEvent("nrh6:" + event, {
          detail: clone(payload)
        })
      );
    } catch {
      /* browser compatibility */
    }
  }

  function requireRepository(repoId) {
    const repo =
      window.NRH4?.repositories?.get?.(repoId) ||
      window.NRH2?.repositories?.get?.(repoId);

    if (!repo) {
      throw new Error("Repository not found: " + repoId);
    }

    return repo;
  }

  function ensureRepositoryState(repoId) {
    if (!state.issueCounters[repoId]) {
      state.issueCounters[repoId] = 0;
    }

    if (!state.labels[repoId]) {
      state.labels[repoId] = {};
    }

    if (!state.milestones[repoId]) {
      state.milestones[repoId] = {};
    }

    if (!state.events[repoId]) {
      state.events[repoId] = [];
    }

    if (!state.issueLinks[repoId]) {
      state.issueLinks[repoId] = {};
    }
  }

  function ensureIssueCollection(repoId) {
    if (!state.issues[repoId]) {
      state.issues[repoId] = {};
    }

    ensureRepositoryState(repoId);

    return state.issues[repoId];
  }

  function issueKey(repoId, number) {
    return repoId + "#" + number;
  }

  function getIssue(repoId, number) {
    const collection = ensureIssueCollection(repoId);
    return collection[String(number)] || null;
  }

  function assertIssue(repoId, number) {
    const issue = getIssue(repoId, number);

    if (!issue) {
      throw new Error(
        `Issue #${number} not found in repository ${repoId}`
      );
    }

    return issue;
  }

  function updateIssueTimestamp(issue) {
    issue.updatedAt = now();
  }

  function createEvent(repoId, number, type, payload = {}) {
    ensureRepositoryState(repoId);

    const event = {
      id: uid("event"),
      repositoryId: repoId,
      issueNumber: Number(number),
      type,
      actor: username(),
      payload: clone(payload),
      createdAt: now()
    };

    state.events[repoId].push(event);

    emit("issue:event", event);

    return event;
  }

  function notifyUsers(repoId, issue, eventType, payload = {}) {
    const users = new Set();

    if (issue.author) {
      users.add(issue.author);
    }

    ensureArray(issue.assignees).forEach(user => {
      users.add(
        typeof user === "string"
          ? user
          : user?.login || user?.username
      );
    });

    ensureArray(issue.watchers).forEach(user => {
      users.add(
        typeof user === "string"
          ? user
          : user?.login || user?.username
      );
    });

    users.delete(username());

    users.forEach(target => {
      if (!target) return;

      try {
        if (window.NRH2?.notifications?.push) {
          NRH2.notifications.push({
            user: target,
            type: "issue",
            title: `Issue #${issue.number}`,
            message: eventType,
            repositoryId: repoId,
            issueNumber: issue.number,
            payload
          });
        }
      } catch {
        /* notification service optional */
      }
    });
  }

  /* ------------------------------------------------------------
     ISSUES
     ------------------------------------------------------------ */

  const issues = {

    create(repoId, input = {}) {
      requireRepository(repoId);

      const collection = ensureIssueCollection(repoId);

      state.issueCounters[repoId] += 1;

      const number = state.issueCounters[repoId];

      const title = safeString(input.title).trim();

      if (!title) {
        throw new Error("Issue title is required.");
      }

      const issue = {
        id: uid("issue"),
        nodeId: uid("node"),
        repositoryId: repoId,
        number,

        title,
        body: safeString(input.body),

        state: input.state === "closed"
          ? "closed"
          : "open",

        stateReason:
          input.stateReason ||
          (input.state === "closed" ? "completed" : null),

        author:
          input.author ||
          username(),

        assignees: ensureArray(input.assignees)
          .map(value =>
            typeof value === "string"
              ? value
              : value?.login || value?.username
          )
          .filter(Boolean),

        labels: ensureArray(input.labels)
          .map(value =>
            typeof value === "string"
              ? value
              : value?.name
          )
          .filter(Boolean),

        milestone:
          input.milestone || null,

        locked: false,

        comments: [],

        reactions: {},

        watchers: [],

        linkedPullRequests: [],

        linkedCommits: [],

        parentIssue: null,

        subIssues: [],

        dependencies: {
          blockedBy: [],
          blocking: []
        },

        createdAt: now(),
        updatedAt: now(),
        closedAt:
          input.state === "closed"
            ? now()
            : null
      };

      collection[number] = issue;

      createEvent(
        repoId,
        number,
        "opened",
        {
          title: issue.title
        }
      );

      emit("issue:created", clone(issue));

      return clone(issue);
    },

    get(repoId, number) {
      const issue = getIssue(repoId, number);

      return issue ? clone(issue) : null;
    },

    list(repoId, options = {}) {
      const collection = ensureIssueCollection(repoId);

      let result = Object.values(collection);

      const stateFilter =
        options.state ||
        "open";

      if (stateFilter !== "all") {
        result = result.filter(
          issue => issue.state === stateFilter
        );
      }

      if (options.author) {
        const author = normalize(options.author);

        result = result.filter(
          issue =>
            normalize(issue.author) === author
        );
      }

      if (options.assignee) {
        const assignee = normalize(options.assignee);

        result = result.filter(
          issue =>
            issue.assignees.some(
              user =>
                normalize(user) === assignee
            )
        );
      }

      if (options.label) {
        const label = normalize(options.label);

        result = result.filter(
          issue =>
            issue.labels.some(
              value =>
                normalize(value) === label
            )
        );
      }

      if (options.milestone) {
        result = result.filter(
          issue =>
            String(issue.milestone) ===
            String(options.milestone)
        );
      }

      if (options.search) {
        const query = normalize(options.search);

        result = result.filter(issue => {
          const text =
            `${issue.title} ${issue.body}`.toLowerCase();

          return text.includes(query);
        });
      }

      const sort =
        options.sort ||
        "created";

      result.sort((a, b) => {
        if (sort === "updated") {
          return (
            new Date(b.updatedAt) -
            new Date(a.updatedAt)
          );
        }

        if (sort === "comments") {
          return (
            b.comments.length -
            a.comments.length
          );
        }

        if (sort === "number") {
          return b.number - a.number;
        }

        return (
          new Date(b.createdAt) -
          new Date(a.createdAt)
        );
      });

      if (options.direction === "asc") {
        result.reverse();
      }

      const page =
        Math.max(1, Number(options.page || 1));

      const perPage =
        Math.max(
          1,
          Math.min(
            100,
            Number(options.perPage || 30)
          )
        );

      const start =
        (page - 1) * perPage;

      return {
        items: clone(
          result.slice(
            start,
            start + perPage
          )
        ),

        total: result.length,

        page,

        perPage,

        hasNextPage:
          start + perPage < result.length
      };
    },

    update(repoId, number, patch = {}) {
      const issue =
        assertIssue(repoId, number);

      if (
        patch.title !== undefined
      ) {
        const title =
          safeString(patch.title).trim();

        if (!title) {
          throw new Error(
            "Issue title cannot be empty."
          );
        }

        issue.title = title;
      }

      if (
        patch.body !== undefined
      ) {
        issue.body =
          safeString(patch.body);
      }

      if (
        patch.milestone !== undefined
      ) {
        issue.milestone =
          patch.milestone || null;
      }

      if (
        patch.stateReason !== undefined
      ) {
        issue.stateReason =
          patch.stateReason;
      }

      if (
        patch.assignees !== undefined
      ) {
        issue.assignees =
          ensureArray(
            patch.assignees
          );
      }

      updateIssueTimestamp(issue);

      createEvent(
        repoId,
        number,
        "edited",
        {
          fields:
            Object.keys(patch)
        }
      );

      emit("issue:updated", clone(issue));

      return clone(issue);
    },

    close(repoId, number, reason = "completed") {
      const issue =
        assertIssue(repoId, number);

      if (issue.state === "closed") {
        return clone(issue);
      }

      issue.state = "closed";

      issue.stateReason =
        reason;

      issue.closedAt =
        now();

      updateIssueTimestamp(issue);

      createEvent(
        repoId,
        number,
        "closed",
        {
          reason
        }
      );

      notifyUsers(
        repoId,
        issue,
        "Issue closed."
      );

      emit(
        "issue:closed",
        clone(issue)
      );

      return clone(issue);
    },

    reopen(repoId, number) {
      const issue =
        assertIssue(repoId, number);

      issue.state = "open";

      issue.stateReason =
        null;

      issue.closedAt =
        null;

      updateIssueTimestamp(issue);

      createEvent(
        repoId,
        number,
        "reopened"
      );

      notifyUsers(
        repoId,
        issue,
        "Issue reopened."
      );

      emit(
        "issue:reopened",
        clone(issue)
      );

      return clone(issue);
    },

    lock(repoId, number, reason = "resolved") {
      const issue =
        assertIssue(repoId, number);

      issue.locked = true;

      issue.lockReason =
        reason;

      updateIssueTimestamp(issue);

      createEvent(
        repoId,
        number,
        "locked",
        {
          reason
        }
      );

      return clone(issue);
    },

    unlock(repoId, number) {
      const issue =
        assertIssue(repoId, number);

      issue.locked = false;

      issue.lockReason =
        null;

      updateIssueTimestamp(issue);

      createEvent(
        repoId,
        number,
        "unlocked"
      );

      return clone(issue);
    },

    delete(repoId, number) {
      const collection =
        ensureIssueCollection(repoId);

      const issue =
        assertIssue(repoId, number);

      delete collection[number];

      delete state.comments[
        issue.id
      ];

      createEvent(
        repoId,
        number,
        "deleted"
      );

      emit(
        "issue:deleted",
        {
          repositoryId: repoId,
          number
        }
      );

      return true;
    }
  };

  /* ------------------------------------------------------------
     COMMENTS
     ------------------------------------------------------------ */

  const comments = {

    create(repoId, number, body) {
      const issue =
        assertIssue(repoId, number);

      if (issue.locked) {
        throw new Error(
          "Issue is locked."
        );
      }

      body =
        safeString(body).trim();

      if (!body) {
        throw new Error(
          "Comment body is required."
        );
      }

      const comment = {
        id: uid("comment"),
        nodeId: uid("node"),
        repositoryId: repoId,
        issueNumber: Number(number),
        author: username(),
        body,
        createdAt: now(),
        updatedAt: now(),
        reactions: {}
      };

      if (!state.comments[issue.id]) {
        state.comments[issue.id] = {};
      }

      state.comments[
        issue.id
      ][comment.id] = comment;

      issue.comments.push(
        comment.id
      );

      updateIssueTimestamp(issue);

      createEvent(
        repoId,
        number,
        "commented",
        {
          commentId:
            comment.id
        }
      );

      notifyUsers(
        repoId,
        issue,
        "New issue comment.",
        {
          commentId:
            comment.id
        }
      );

      emit(
        "issue:comment",
        clone(comment)
      );

      return clone(comment);
    },

    list(repoId, number) {
      const issue =
        assertIssue(repoId, number);

      const bucket =
        state.comments[issue.id] ||
        {};

      return clone(
        Object.values(bucket)
          .sort(
            (a, b) =>
              new Date(a.createdAt) -
              new Date(b.createdAt)
          )
      );
    },

    get(repoId, number, commentId) {
      const issue =
        assertIssue(repoId, number);

      return clone(
        state.comments[
          issue.id
        ]?.[commentId] ||
        null
      );
    },

    update(
      repoId,
      number,
      commentId,
      body
    ) {
      const comment =
        comments.get(
          repoId,
          number,
          commentId
        );

      if (!comment) {
        throw new Error(
          "Comment not found."
        );
      }

      const issue =
        assertIssue(repoId, number);

      const stored =
        state.comments[
          issue.id
        ][commentId];

      if (
        stored.author !==
        username()
      ) {
        throw new Error(
          "Only the comment author can edit it."
        );
      }

      stored.body =
        safeString(body).trim();

      stored.updatedAt =
        now();

      updateIssueTimestamp(issue);

      createEvent(
        repoId,
        number,
        "comment_edited",
        {
          commentId
        }
      );

      emit(
        "issue:comment_updated",
        clone(stored)
      );

      return clone(stored);
    },

    delete(repoId, number, commentId) {
      const issue =
        assertIssue(repoId, number);

      const bucket =
        state.comments[
          issue.id
        ];

      const comment =
        bucket?.[commentId];

      if (!comment) {
        throw new Error(
          "Comment not found."
        );
      }

      if (
        comment.author !==
        username()
      ) {
        throw new Error(
          "Only the comment author can delete it."
        );
      }

      delete bucket[commentId];

      issue.comments =
        issue.comments.filter(
          id => id !== commentId
        );

      updateIssueTimestamp(issue);

      createEvent(
        repoId,
        number,
        "comment_deleted",
        {
          commentId
        }
      );

      emit(
        "issue:comment_deleted",
        {
          repositoryId: repoId,
          issueNumber: number,
          commentId
        }
      );

      return true;
    }
  };

  /* ------------------------------------------------------------
     LABELS
     ------------------------------------------------------------ */

  const labels = {

    create(repoId, input = {}) {
      requireRepository(repoId);

      ensureRepositoryState(repoId);

      const name =
        safeString(input.name).trim();

      if (!name) {
        throw new Error(
          "Label name is required."
        );
      }

      const key =
        normalize(name);

      if (
        state.labels[repoId][key]
      ) {
        throw new Error(
          "Label already exists."
        );
      }

      const label = {
        id: uid("label"),
        repositoryId: repoId,
        name,
        description:
          safeString(
            input.description
          ),
        color:
          safeString(
            input.color,
            "6e7781"
          ).replace("#", ""),
        default:
          Boolean(input.default),
        createdAt: now(),
        updatedAt: now()
      };

      state.labels[
        repoId
      ][key] = label;

      emit(
        "label:created",
        clone(label)
      );

      return clone(label);
    },

    get(repoId, name) {
      ensureRepositoryState(repoId);

      return clone(
        state.labels[
          repoId
        ][normalize(name)] ||
        null
      );
    },

    list(repoId) {
      ensureRepositoryState(repoId);

      return clone(
        Object.values(
          state.labels[repoId]
        )
      );
    },

    update(repoId, name, patch = {}) {
      const key =
        normalize(name);

      const label =
        state.labels[
          repoId
        ]?.[key];

      if (!label) {
        throw new Error(
          "Label not found."
        );
      }

      if (
        patch.name !== undefined &&
        normalize(patch.name) !== key
      ) {
        const newKey =
          normalize(patch.name);

        if (
          state.labels[
            repoId
          ][newKey]
        ) {
          throw new Error(
            "A label with this name already exists."
          );
        }

        delete state.labels[
          repoId
        ][key];

        label.name =
          safeString(
            patch.name
          ).trim();

        state.labels[
          repoId
        ][newKey] = label;
      }

      if (
        patch.description !== undefined
      ) {
        label.description =
          safeString(
            patch.description
          );
      }

      if (
        patch.color !== undefined
      ) {
        label.color =
          safeString(
            patch.color
          ).replace("#", "");
      }

      label.updatedAt =
        now();

      emit(
        "label:updated",
        clone(label)
      );

      return clone(label);
    },

    remove(repoId, name) {
      const key =
        normalize(name);

      if (
        !state.labels[
          repoId
        ]?.[key]
      ) {
        return false;
      }

      delete state.labels[
        repoId
      ][key];

      Object.values(
        state.issues[
          repoId
        ] || {}
      ).forEach(issue => {
        issue.labels =
          issue.labels.filter(
            label =>
              normalize(label) !==
              key
          );
      });

      emit(
        "label:deleted",
        {
          repositoryId: repoId,
          name
        }
      );

      return true;
    },

    addToIssue(
      repoId,
      number,
      name
    ) {
      const issue =
        assertIssue(repoId, number);

      const label =
        labels.get(repoId, name);

      if (!label) {
        throw new Error(
          "Label not found."
        );
      }

      const exists =
        issue.labels.some(
          value =>
            normalize(value) ===
            normalize(label.name)
        );

      if (!exists) {
        issue.labels.push(
          label.name
        );

        updateIssueTimestamp(issue);

        createEvent(
          repoId,
          number,
          "labeled",
          {
            label:
              label.name
          }
        );

        emit(
          "issue:labeled",
          {
            issue:
              clone(issue),
            label:
              clone(label)
          }
        );
      }

      return clone(issue);
    },

    removeFromIssue(
      repoId,
      number,
      name
    ) {
      const issue =
        assertIssue(repoId, number);

      issue.labels =
        issue.labels.filter(
          value =>
            normalize(value) !==
            normalize(name)
        );

      updateIssueTimestamp(issue);

      createEvent(
        repoId,
        number,
        "unlabeled",
        {
          label: name
        }
      );

      emit(
        "issue:unlabeled",
        {
          repositoryId: repoId,
          issueNumber: number,
          label: name
        }
      );

      return clone(issue);
    },

    set(repoId, number, names) {
      const issue =
        assertIssue(repoId, number);

      issue.labels =
        ensureArray(names)
          .map(
            value =>
              typeof value === "string"
                ? value
                : value?.name
          )
          .filter(Boolean);

      updateIssueTimestamp(issue);

      createEvent(
        repoId,
        number,
        "labels_updated",
        {
          labels:
            clone(issue.labels)
        }
      );

      return clone(issue);
    }
  };

  /* ------------------------------------------------------------
     ASSIGNEES
     ------------------------------------------------------------ */

  const assignees = {

    list(repoId) {
      const result = new Set();

      Object.values(
        state.issues[
          repoId
        ] || {}
      ).forEach(issue => {
        ensureArray(
          issue.assignees
        ).forEach(user =>
          result.add(user)
        );
      });

      return [
        ...result
      ];
    },

    add(repoId, number, users) {
      const issue =
        assertIssue(repoId, number);

      const incoming =
        ensureArray(users);

      incoming.forEach(user => {
        const login =
          typeof user === "string"
            ? user
            : user?.login ||
              user?.username;

        if (
          login &&
          !issue.assignees.includes(login)
        ) {
          issue.assignees.push(
            login
          );

          createEvent(
            repoId,
            number,
            "assigned",
            {
              assignee:
                login
            }
          );
        }
      });

      updateIssueTimestamp(issue);

      emit(
        "issue:assigned",
        clone(issue)
      );

      return clone(issue);
    },

    remove(repoId, number, users) {
      const issue =
        assertIssue(repoId, number);

      const removeSet =
        new Set(
          ensureArray(users)
            .map(user =>
              typeof user === "string"
                ? user
                : user?.login ||
                  user?.username
            )
            .filter(Boolean)
        );

      issue.assignees =
        issue.assignees.filter(
          user => {
            const removed =
              removeSet.has(user);

            if (removed) {
              createEvent(
                repoId,
                number,
                "unassigned",
                {
                  assignee: user
                }
              );
            }

            return !removed;
          }
        );

      updateIssueTimestamp(issue);

      emit(
        "issue:unassigned",
        clone(issue)
      );

      return clone(issue);
    },

    set(repoId, number, users) {
      const issue =
        assertIssue(repoId, number);

      issue.assignees =
        ensureArray(users)
          .map(user =>
            typeof user === "string"
              ? user
              : user?.login ||
                user?.username
          )
          .filter(Boolean);

      updateIssueTimestamp(issue);

      createEvent(
        repoId,
        number,
        "assignees_updated",
        {
          assignees:
            clone(issue.assignees)
        }
      );

      return clone(issue);
    }
  };

  /* ------------------------------------------------------------
     MILESTONES
     ------------------------------------------------------------ */

  const milestones = {

    create(repoId, input = {}) {
      requireRepository(repoId);

      ensureRepositoryState(repoId);

      const title =
        safeString(
          input.title
        ).trim();

      if (!title) {
        throw new Error(
          "Milestone title is required."
        );
      }

      const existing =
        Object.values(
          state.milestones[
            repoId
          ]
        ).some(
          milestone =>
            normalize(
              milestone.title
            ) === normalize(title)
        );

      if (existing) {
        throw new Error(
          "Milestone already exists."
        );
      }

      const number =
        Object.keys(
          state.milestones[
            repoId
          ]
        ).length + 1;

      const milestone = {
        id: uid("milestone"),
        number,
        repositoryId: repoId,

        title,

        description:
          safeString(
            input.description
          ),

        state:
          input.state === "closed"
            ? "closed"
            : "open",

        dueOn:
          input.dueOn ||
          null,

        creator:
          username(),

        createdAt: now(),
        updatedAt: now(),

        closedAt:
          input.state === "closed"
            ? now()
            : null
      };

      state.milestones[
        repoId
      ][milestone.id] =
        milestone;

      emit(
        "milestone:created",
        clone(milestone)
      );

      return clone(milestone);
    },

    get(repoId, number) {
      return clone(
        Object.values(
          state.milestones[
            repoId
          ] || {}
        ).find(
          milestone =>
            Number(
              milestone.number
            ) === Number(number)
        ) || null
      );
    },

    list(repoId, options = {}) {
      ensureRepositoryState(repoId);

      let result =
        Object.values(
          state.milestones[
            repoId
          ]
        );

      if (
        options.state &&
        options.state !== "all"
      ) {
        result =
          result.filter(
            milestone =>
              milestone.state ===
              options.state
          );
      }

      result.sort(
        (a, b) =>
          new Date(a.createdAt) -
          new Date(b.createdAt)
      );

      return clone(result);
    },

    update(repoId, number, patch = {}) {
      const milestone =
        milestones.get(
          repoId,
          number
        );

      if (!milestone) {
        throw new Error(
          "Milestone not found."
        );
      }

      if (
        patch.title !== undefined
      ) {
        milestone.title =
          safeString(
            patch.title
          ).trim();
      }

      if (
        patch.description !== undefined
      ) {
        milestone.description =
          safeString(
            patch.description
          );
      }

      if (
        patch.dueOn !== undefined
      ) {
        milestone.dueOn =
          patch.dueOn ||
          null;
      }

      if (
        patch.state !== undefined
      ) {
        milestone.state =
          patch.state === "closed"
            ? "closed"
            : "open";

        milestone.closedAt =
          milestone.state === "closed"
            ? now()
            : null;
      }

      milestone.updatedAt =
        now();

      const stored =
        state.milestones[
          repoId
        ][milestone.id];

      Object.assign(
        stored,
        milestone
      );

      emit(
        "milestone:updated",
        clone(stored)
      );

      return clone(stored);
    },

    close(repoId, number) {
      return milestones.update(
        repoId,
        number,
        {
          state: "closed"
        }
      );
    },

    reopen(repoId, number) {
      return milestones.update(
        repoId,
        number,
        {
          state: "open"
        }
      );
    },

    delete(repoId, number) {
      const milestone =
        milestones.get(
          repoId,
          number
        );

      if (!milestone) {
        return false;
      }

      delete state.milestones[
        repoId
      ][milestone.id];

      Object.values(
        state.issues[
          repoId
        ] || {}
      ).forEach(issue => {
        if (
          Number(issue.milestone) ===
          Number(number)
        ) {
          issue.milestone =
            null;
        }
      });

      emit(
        "milestone:deleted",
        {
          repositoryId: repoId,
          number
        }
      );

      return true;
    },

    progress(repoId, number) {
      const milestone =
        milestones.get(
          repoId,
          number
        );

      if (!milestone) {
        throw new Error(
          "Milestone not found."
        );
      }

      const issuesResult =
        issues.list(
          repoId,
          {
            state: "all",
            perPage: 100
          }
        );

      const related =
        issuesResult.items.filter(
          issue =>
            Number(
              issue.milestone
            ) === Number(number)
        );

      const open =
        related.filter(
          issue =>
            issue.state === "open"
        ).length;

      const closed =
        related.filter(
          issue =>
            issue.state === "closed"
        ).length;

      const total =
        related.length;

      return {
        milestone:
          clone(milestone),

        total,

        open,

        closed,

        percent:
          total === 0
            ? 0
            : Math.round(
                (closed / total) *
                100
              )
      };
    }
  };

  /* ------------------------------------------------------------
     REACTIONS
     ------------------------------------------------------------ */

  const reactions = {

    allowed: [
      "+1",
      "-1",
      "laugh",
      "hooray",
      "confused",
      "heart",
      "rocket",
      "eyes"
    ],

    toggle(
      repoId,
      number,
      targetType,
      targetId,
      content
    ) {
      const issue =
        assertIssue(repoId, number);

      if (
        !this.allowed.includes(
          content
        )
      ) {
        throw new Error(
          "Unsupported reaction."
        );
      }

      const key =
        [
          repoId,
          number,
          targetType,
          targetId
        ].join(":");

      if (!state.reactions[key]) {
        state.reactions[key] = {};
      }

      if (
        !state.reactions[key][content]
      ) {
        state.reactions[key][content] =
          new Set();
      }

      const users =
        state.reactions[key][content];

      const user =
        username();

      let active = false;

      if (users.has(user)) {
        users.delete(user);
      } else {
        users.add(user);
        active = true;
      }

      if (
        !issue.reactions[targetId]
      ) {
        issue.reactions[targetId] =
          {};
      }

      issue.reactions[targetId][content] =
        users.size;

      updateIssueTimestamp(issue);

      createEvent(
        repoId,
        number,
        active
          ? "reaction_added"
          : "reaction_removed",
        {
          targetType,
          targetId,
          content
        }
      );

      emit(
        "issue:reaction",
        {
          repositoryId: repoId,
          issueNumber: number,
          targetType,
          targetId,
          content,
          active,
          count: users.size
        }
      );

      return {
        content,
        active,
        count: users.size
      };
    },

    list(
      repoId,
      number,
      targetType,
      targetId
    ) {
      assertIssue(repoId, number);

      const key =
        [
          repoId,
          number,
          targetType,
          targetId
        ].join(":");

      const source =
        state.reactions[key] ||
        {};

      const result = {};

      Object.keys(source)
        .forEach(reaction => {
          result[reaction] =
            source[reaction].size;
        });

      return result;
    }
  };

  /* ------------------------------------------------------------
     WATCHERS / SUBSCRIPTIONS
     ------------------------------------------------------------ */

  const watchers = {

    subscribe(repoId, number, user) {
      const issue =
        assertIssue(repoId, number);

      const login =
        user ||
        username();

      if (!issue.watchers.includes(login)) {
        issue.watchers.push(login);
      }

      if (!state.watchers[repoId]) {
        state.watchers[repoId] = {};
      }

      if (!state.watchers[repoId][number]) {
        state.watchers[repoId][number] =
          new Set();
      }

      state.watchers[
        repoId
      ][number].add(login);

      createEvent(
        repoId,
        number,
        "subscribed",
        {
          user: login
        }
      );

      return clone(issue.watchers);
    },

    unsubscribe(repoId, number, user) {
      const issue =
        assertIssue(repoId, number);

      const login =
        user ||
        username();

      issue.watchers =
        issue.watchers.filter(
          value =>
            value !== login
        );

      state.watchers[
        repoId
      ]?.[number]?.delete(login);

      createEvent(
        repoId,
        number,
        "unsubscribed",
        {
          user: login
        }
      );

      return clone(issue.watchers);
    },

    list(repoId, number) {
      const issue =
        assertIssue(repoId, number);

      return clone(
        issue.watchers
      );
    }
  };

  /* ------------------------------------------------------------
     ISSUE DEPENDENCIES
     ------------------------------------------------------------ */

  const dependencies = {

    block(repoId, blockerNumber, blockedNumber) {
      const blocker =
        assertIssue(
          repoId,
          blockerNumber
        );

      const blocked =
        assertIssue(
          repoId,
          blockedNumber
        );

      if (
        blockerNumber ===
        blockedNumber
      ) {
        throw new Error(
          "An issue cannot block itself."
        );
      }

      if (
        blocked.dependencies.blockedBy
          .includes(blockerNumber)
      ) {
        return clone(blocked);
      }

      blocked.dependencies.blockedBy
        .push(blockerNumber);

      blocker.dependencies.blocking
        .push(blockedNumber);

      updateIssueTimestamp(
        blocker
      );

      updateIssueTimestamp(
        blocked
      );

      createEvent(
        repoId,
        blockedNumber,
        "blocked",
        {
          by: blockerNumber
        }
      );

      emit(
        "issue:dependency",
        {
          repositoryId: repoId,
          blocker:
            blockerNumber,
          blocked:
            blockedNumber
        }
      );

      return clone(blocked);
    },

    unblock(repoId, blockerNumber, blockedNumber) {
      const blocker =
        assertIssue(
          repoId,
          blockerNumber
        );

      const blocked =
        assertIssue(
          repoId,
          blockedNumber
        );

      blocked.dependencies.blockedBy =
        blocked.dependencies.blockedBy
          .filter(
            value =>
              Number(value) !==
              Number(blockerNumber)
          );

      blocker.dependencies.blocking =
        blocker.dependencies.blocking
          .filter(
            value =>
              Number(value) !==
              Number(blockedNumber)
          );

      updateIssueTimestamp(
        blocker
      );

      updateIssueTimestamp(
        blocked
      );

      createEvent(
        repoId,
        blockedNumber,
        "unblocked",
        {
          by: blockerNumber
        }
      );

      return clone(blocked);
    },

    blockedBy(repoId, number) {
      const issue =
        assertIssue(
          repoId,
          number
        );

      return clone(
        issue.dependencies
          .blockedBy
          .map(
            dependencyNumber =>
              getIssue(
                repoId,
                dependencyNumber
              )
          )
          .filter(Boolean)
      );
    },

    blocking(repoId, number) {
      const issue =
        assertIssue(
          repoId,
          number
        );

      return clone(
        issue.dependencies
          .blocking
          .map(
            dependencyNumber =>
              getIssue(
                repoId,
                dependencyNumber
              )
          )
          .filter(Boolean)
      );
    }
  };

  /* ------------------------------------------------------------
     SUB-ISSUES
     ------------------------------------------------------------ */

  const subIssues = {

    add(repoId, parentNumber, childNumber) {
      const parent =
        assertIssue(
          repoId,
          parentNumber
        );

      const child =
        assertIssue(
          repoId,
          childNumber
        );

      if (
        parentNumber ===
        childNumber
      ) {
        throw new Error(
          "An issue cannot be its own sub-issue."
        );
      }

      if (
        parent.subIssues.includes(
          childNumber
        )
      ) {
        return clone(parent);
      }

      parent.subIssues.push(
        childNumber
      );

      child.parentIssue =
        parentNumber;

      updateIssueTimestamp(
        parent
      );

      updateIssueTimestamp(
        child
      );

      createEvent(
        repoId,
        parentNumber,
        "sub_issue_added",
        {
          child:
            childNumber
        }
      );

      return clone(parent);
    },

    remove(repoId, parentNumber, childNumber) {
      const parent =
        assertIssue(
          repoId,
          parentNumber
        );

      const child =
        assertIssue(
          repoId,
          childNumber
        );

      parent.subIssues =
        parent.subIssues.filter(
          value =>
            Number(value) !==
            Number(childNumber)
        );

      if (
        Number(child.parentIssue) ===
        Number(parentNumber)
      ) {
        child.parentIssue =
          null;
      }

      updateIssueTimestamp(
        parent
      );

      updateIssueTimestamp(
        child
      );

      createEvent(
        repoId,
        parentNumber,
        "sub_issue_removed",
        {
          child:
            childNumber
        }
      );

      return clone(parent);
    },

    list(repoId, parentNumber) {
      const parent =
        assertIssue(
          repoId,
          parentNumber
        );

      return clone(
        parent.subIssues
          .map(number =>
            getIssue(
              repoId,
              number
            )
          )
          .filter(Boolean)
      );
    },

    parent(repoId, childNumber) {
      const child =
        assertIssue(
          repoId,
          childNumber
        );

      if (
        child.parentIssue === null
      ) {
        return null;
      }

      return clone(
        getIssue(
          repoId,
          child.parentIssue
        )
      );
    }
  };

  /* ------------------------------------------------------------
     LINKS TO COMMITS / PULL REQUESTS
     ------------------------------------------------------------ */

  const links = {

    commit(repoId, number, sha) {
      const issue =
        assertIssue(repoId, number);

      if (
        !issue.linkedCommits.includes(
          sha
        )
      ) {
        issue.linkedCommits.push(
          sha
        );
      }

      updateIssueTimestamp(issue);

      createEvent(
        repoId,
        number,
        "commit_linked",
        {
          sha
        }
      );

      return clone(issue);
    },

    pullRequest(repoId, number, prNumber) {
      const issue =
        assertIssue(repoId, number);

      if (
        !issue.linkedPullRequests.includes(
          prNumber
        )
      ) {
        issue.linkedPullRequests.push(
          prNumber
        );
      }

      updateIssueTimestamp(issue);

      createEvent(
        repoId,
        number,
        "pull_request_linked",
        {
          pullRequest:
            prNumber
        }
      );

      return clone(issue);
    },

    commits(repoId, number) {
      return clone(
        assertIssue(
          repoId,
          number
        ).linkedCommits
      );
    },

    pullRequests(repoId, number) {
      return clone(
        assertIssue(
          repoId,
          number
        ).linkedPullRequests
      );
    }
  };

  /* ------------------------------------------------------------
     EVENTS / TIMELINE
     ------------------------------------------------------------ */

  const timeline = {

    list(repoId, number, options = {}) {
      assertIssue(repoId, number);

      let result =
        ensureArray(
          state.events[
            repoId
          ]
        ).filter(
          event =>
            Number(event.issueNumber) ===
            Number(number)
        );

      if (options.type) {
        result =
          result.filter(
            event =>
              event.type ===
              options.type
          );
      }

      if (options.actor) {
        result =
          result.filter(
            event =>
              normalize(event.actor) ===
              normalize(options.actor)
          );
      }

      result.sort(
        (a, b) =>
          new Date(a.createdAt) -
          new Date(b.createdAt)
      );

      return clone(result);
    }
  };

  /* ------------------------------------------------------------
     MENTIONS
     ------------------------------------------------------------ */

  const mentions = {

    extract(text) {
      const value =
        safeString(text);

      const found =
        value.match(
          /(^|\s)@([a-zA-Z0-9][a-zA-Z0-9._-]*)/g
        ) || [];

      return [
        ...new Set(
          found.map(
            token =>
              token
                .trim()
                .slice(1)
          )
        )
      ];
    },

    notify(repoId, issue, text) {
      const users =
        this.extract(text);

      users.forEach(user => {
        try {
          if (
            window.NRH2
              ?.notifications
              ?.push
          ) {
            NRH2.notifications.push({
              user,
              type: "mention",
              title:
                `Mention in #${issue.number}`,
              message:
                `${username()} mentioned you.`,
              repositoryId:
                repoId,
              issueNumber:
                issue.number
            });
          }
        } catch {
          /* optional */
        }
      });

      return users;
    }
  };

  /* ------------------------------------------------------------
     SEARCH
     ------------------------------------------------------------ */

  const search = {

    issues(repoId, query, options = {}) {
      return issues.list(
        repoId,
        {
          ...options,
          state:
            options.state ||
            "all",
          search:
            query
        }
      );
    },

    advanced(repoId, filters = {}) {
      let result =
        issues.list(
          repoId,
          {
            state:
              filters.state ||
              "all",
            perPage: 100
          }
        ).items;

      if (filters.label) {
        const label =
          normalize(
            filters.label
          );

        result =
          result.filter(
            issue =>
              issue.labels.some(
                value =>
                  normalize(value) ===
                  label
              )
          );
      }

      if (filters.assignee) {
        const user =
          normalize(
            filters.assignee
          );

        result =
          result.filter(
            issue =>
              issue.assignees.some(
                value =>
                  normalize(value) ===
                  user
              )
          );
      }

      if (filters.author) {
        const user =
          normalize(
            filters.author
          );

        result =
          result.filter(
            issue =>
              normalize(
                issue.author
              ) === user
          );
      }

      if (
        filters.milestone !==
        undefined
      ) {
        result =
          result.filter(
            issue =>
              Number(
                issue.milestone
              ) ===
              Number(
                filters.milestone
              )
          );
      }

      if (filters.mentioned) {
        const user =
          normalize(
            filters.mentioned
          );

        result =
          result.filter(
            issue =>
              mentions
                .extract(
                  issue.body
                )
                .some(
                  mention =>
                    normalize(
                      mention
                    ) === user
                )
          );
      }

      return clone(result);
    }
  };

  /* ------------------------------------------------------------
     STATISTICS
     ------------------------------------------------------------ */

  const statistics = {

    repository(repoId) {
      const result =
        issues.list(
          repoId,
          {
            state: "all",
            perPage: 100
          }
        ).items;

      const open =
        result.filter(
          issue =>
            issue.state === "open"
        ).length;

      const closed =
        result.filter(
          issue =>
            issue.state === "closed"
        ).length;

      const comments =
        result.reduce(
          (total, issue) =>
            total +
            issue.comments.length,
          0
        );

      const labelsCount = {};

      result.forEach(issue => {
        issue.labels.forEach(label => {
          labelsCount[label] =
            (labelsCount[label] || 0) +
            1;
        });
      });

      return {
        total:
          result.length,

        open,

        closed,

        comments,

        completion:
          result.length === 0
            ? 0
            : Math.round(
                (closed /
                  result.length) *
                100
              ),

        labels:
          labelsCount
      };
    }
  };

  /* ------------------------------------------------------------
     SERIALIZATION
     ------------------------------------------------------------ */

  const serialization = {

    exportRepository(repoId) {
      requireRepository(repoId);

      return {
        version: VERSION,
        repositoryId: repoId,
        exportedAt: now(),

        issues:
          clone(
            state.issues[
              repoId
            ] || {}
          ),

        labels:
          clone(
            state.labels[
              repoId
            ] || {}
          ),

        milestones:
          clone(
            state.milestones[
              repoId
            ] || {}
          ),

        events:
          clone(
            state.events[
              repoId
            ] || []
          ),

        comments:
          Object.fromEntries(
            Object.entries(
              state.comments
            )
          )
      };
    },

    importRepository(repoId, data) {
      requireRepository(repoId);

      if (
        !data ||
        typeof data !== "object"
      ) {
        throw new Error(
          "Invalid Issues export."
        );
      }

      ensureRepositoryState(repoId);

      if (data.issues) {
        state.issues[repoId] =
          clone(data.issues);
      }

      if (data.labels) {
        state.labels[repoId] =
          clone(data.labels);
      }

      if (data.milestones) {
        state.milestones[repoId] =
          clone(data.milestones);
      }

      if (data.events) {
        state.events[repoId] =
          clone(data.events);
      }

      if (data.comments) {
        Object.assign(
          state.comments,
          clone(data.comments)
        );
      }

      const numbers =
        Object.keys(
          state.issues[repoId]
        ).map(Number);

      state.issueCounters[repoId] =
        numbers.length
          ? Math.max(...numbers)
          : 0;

      emit(
        "issues:imported",
        {
          repositoryId: repoId
        }
      );

      return true;
    }
  };

  /* ------------------------------------------------------------
     UI HELPERS
     ------------------------------------------------------------ */

  const ui = {

    badge(issue) {
      const stateClass =
        issue.state === "open"
          ? "open"
          : "closed";

      return `
        <span
          class="nrh-issue-badge ${stateClass}"
          data-issue="${issue.number}"
        >
          ${issue.state === "open"
            ? "●"
            : "✓"}
          #${issue.number}
        </span>
      `;
    },

    row(issue) {
      const labels =
        issue.labels
          .map(
            label => `
              <span class="nrh-issue-label">
                ${label}
              </span>
            `
          )
          .join("");

      const assignees =
        issue.assignees
          .map(
            user => `
              <span
                class="nrh-issue-assignee"
              >
                @${user}
              </span>
            `
          )
          .join("");

      return `
        <article
          class="nrh-issue-row"
          data-repository="${issue.repositoryId}"
          data-issue="${issue.number}"
        >
          <div class="nrh-issue-main">

            <div class="nrh-issue-title">
              ${issue.state === "open"
                ? "●"
                : "✓"}

              <strong>
                #${issue.number}
                ${issue.title}
              </strong>
            </div>

            <div class="nrh-issue-meta">
              ${issue.author}
              ·
              ${issue.comments.length}
              comments
              ·
              ${new Date(
                issue.updatedAt
              ).toLocaleString()}
            </div>

            <div class="nrh-issue-labels">
              ${labels}
              ${assignees}
            </div>

          </div>
        </article>
      `;
    },

    list(repoId, options = {}) {
      const result =
        issues.list(
          repoId,
          options
        );

      return `
        <section
          class="nrh-issues"
          data-repository="${repoId}"
        >

          <header
            class="nrh-issues-header"
          >
            <strong>
              Issues
            </strong>

            <span>
              ${result.total}
            </span>
          </header>

          <div
            class="nrh-issues-list"
          >
            ${
              result.items.length
                ? result.items
                    .map(
                      issue =>
                        ui.row(issue)
                    )
                    .join("")
                : `
                  <div
                    class="nrh-empty"
                  >
                    No issues found.
                  </div>
                `
            }
          </div>

        </section>
      `;
    },

    detail(repoId, number) {
      const issue =
        issues.get(
          repoId,
          number
        );

      if (!issue) {
        return `
          <div class="nrh-error">
            Issue not found.
          </div>
        `;
      }

      const issueComments =
        comments.list(
          repoId,
          number
        );

      const eventList =
        timeline.list(
          repoId,
          number
        );

      return `
        <article
          class="nrh-issue-detail"
          data-repository="${repoId}"
          data-issue="${number}"
        >

          <header>

            <div>
              <h1>
                ${issue.title}
              </h1>

              <div>
                ${ui.badge(issue)}
                opened by
                <strong>
                  @${issue.author}
                </strong>
              </div>
            </div>

            <div>
              ${
                issue.state === "open"
                  ? `
                    <button
                      data-action="close-issue"
                      data-issue="${number}"
                    >
                      Close issue
                    </button>
                  `
                  : `
                    <button
                      data-action="reopen-issue"
                      data-issue="${number}"
                    >
                      Reopen issue
                    </button>
                  `
              }
            </div>

          </header>

          <section
            class="nrh-issue-body"
          >
            ${issue.body}
          </section>

          <section
            class="nrh-issue-sidebar"
          >

            <div>
              <strong>
                Assignees
              </strong>

              ${
                issue.assignees
                  .map(
                    user =>
                      `<div>@${user}</div>`
                  )
                  .join("")
              }
            </div>

            <div>
              <strong>
                Labels
              </strong>

              ${
                issue.labels
                  .map(
                    label =>
                      `<div>${label}</div>`
                  )
                  .join("")
              }
            </div>

            <div>
              <strong>
                Milestone
              </strong>

              ${
                issue.milestone ||
                "None"
              }
            </div>

          </section>

          <section
            class="nrh-issue-comments"
          >

            <h2>
              Comments
            </h2>

            ${
              issueComments
                .map(
                  comment => `
                    <article
                      class="nrh-comment"
                      data-comment="${comment.id}"
                    >

                      <header>
                        <strong>
                          @${comment.author}
                        </strong>

                        <time>
                          ${new Date(
                            comment.createdAt
                          ).toLocaleString()}
                        </time>
                      </header>

                      <div>
                        ${comment.body}
                      </div>

                    </article>
                  `
                )
                .join("")
            }

          </section>

          <section
            class="nrh-issue-timeline"
          >

            <h2>
              Timeline
            </h2>

            ${
              eventList
                .map(
                  event => `
                    <div
                      class="nrh-timeline-event"
                    >
                      <strong>
                        ${event.type}
                      </strong>

                      <span>
                        @${event.actor}
                      </span>

                      <time>
                        ${new Date(
                          event.createdAt
                        ).toLocaleString()}
                      </time>
                    </div>
                  `
                )
                .join("")
            }

          </section>

        </article>
      `;
    }
  };

  /* ------------------------------------------------------------
     PERSISTENCE
     ------------------------------------------------------------ */

  const persistence = {

    key:
      "neural_raphael_hub_issues_v6",

    save() {
      try {
        const payload = {
          version: VERSION,
          state
        };

        localStorage.setItem(
          this.key,
          JSON.stringify(payload)
        );

        return true;
      } catch {
        return false;
      }
    },

    restore() {
      try {
        const raw =
          localStorage.getItem(
            this.key
          );

        if (!raw) {
          return false;
        }

        const payload =
          JSON.parse(raw);

        if (
          !payload ||
          !payload.state
        ) {
          return false;
        }

        Object.assign(
          state,
          payload.state
        );

        return true;
      } catch {
        return false;
      }
    },

    clear() {
      try {
        localStorage.removeItem(
          this.key
        );

        return true;
      } catch {
        return false;
      }
    }
  };

  /* ------------------------------------------------------------
     COMMANDS
     ------------------------------------------------------------ */

  function registerCommands() {
    if (
      !window.NRH2?.commands?.register
    ) {
      return;
    }

    NRH2.commands.register(
      "issues:list",
      ({ repositoryId } = {}) => {
        if (!repositoryId) {
          throw new Error(
            "repositoryId is required."
          );
        }

        return issues.list(
          repositoryId,
          {
            state: "all",
            perPage: 100
          }
        );
      }
    );

    NRH2.commands.register(
      "issue:create",
      ({
        repositoryId,
        title,
        body
      } = {}) => {
        return issues.create(
          repositoryId,
          {
            title,
            body
          }
        );
      }
    );

    NRH2.commands.register(
      "issue:close",
      ({
        repositoryId,
        number
      } = {}) => {
        return issues.close(
          repositoryId,
          number
        );
      }
    );

    NRH2.commands.register(
      "issue:reopen",
      ({
        repositoryId,
        number
      } = {}) => {
        return issues.reopen(
          repositoryId,
          number
        );
      }
    );

    NRH2.commands.register(
      "issue:search",
      ({
        repositoryId,
        query
      } = {}) => {
        return search.issues(
          repositoryId,
          query,
          {
            state: "all",
            perPage: 100
          }
        );
      }
    );
  }

  /* ------------------------------------------------------------
     EVENT WIRING
     ------------------------------------------------------------ */

  function wireEvents() {

    window.addEventListener(
      "beforeunload",
      () => {
        persistence.save();
      }
    );

    if (
      window.NRH2?.events?.on
    ) {

      NRH2.events.on(
        "repository:created",
        payload => {
          if (
            payload?.id ||
            payload?.repositoryId
          ) {
            ensureRepositoryState(
              payload.id ||
              payload.repositoryId
            );
          }
        }
      );

      NRH2.events.on(
        "repository:deleted",
        payload => {
          const repoId =
            payload?.id ||
            payload?.repositoryId;

          if (!repoId) return;

          delete state.issues[
            repoId
          ];

          delete state.labels[
            repoId
          ];

          delete state.milestones[
            repoId
          ];

          delete state.events[
            repoId
          ];

          delete state.issueCounters[
            repoId
          ];
        }
      );
    }
  }

  /* ------------------------------------------------------------
     INIT
     ------------------------------------------------------------ */

  function init() {
    persistence.restore();

    registerCommands();

    wireEvents();

    emit(
      "initialized",
      {
        version: VERSION
      }
    );

    console.log(
      `%cNRH6 Issues Engine ${VERSION}`,
      "color:#58a6ff;font-weight:bold"
    );

    return api;
  }

  /* ------------------------------------------------------------
     PUBLIC API
     ------------------------------------------------------------ */

  const api = {
    VERSION,

    state,

    init,

    issues,

    comments,

    labels,

    assignees,

    milestones,

    reactions,

    watchers,

    dependencies,

    subIssues,

    links,

    timeline,

    mentions,

    search,

    statistics,

    serialization,

    persistence,

    ui
  };

  return api;
})();

window.NRH6 = NRH6;

NRH6.init();

/* ============================================================
   END BLOCK 6
   ============================================================ */
</script>
<script>
/* ============================================================
   NEURAL RAPHAEL HUB
   BLOCK 7 — PULL REQUEST ENGINE
   Version: 7.0.0

   Dependencies:
     NRH2 — Core Engine
     NRH3 — Users/Auth
     NRH4 — Repository Engine
     NRH5 — Git Engine
     NRH6 — Issues Engine
   ============================================================ */

const NRH7 = (() => {
  "use strict";

  const VERSION = "7.0.0";

  /* ==========================================================
     STATE
     ========================================================== */

  const state = {
    pullRequests: {},
    counters: {},
    reviews: {},
    reviewComments: {},
    reviewers: {},
    events: {},
    checks: {},
    mergeRecords: {}
  };

  /* ==========================================================
     UTILITIES
     ========================================================== */

  function now() {
    return new Date().toISOString();
  }

  function uid(prefix = "id") {
    return (
      prefix +
      "_" +
      Math.random().toString(36).slice(2, 10) +
      "_" +
      Date.now().toString(36)
    );
  }

  function clone(value) {
    if (value === undefined) return undefined;

    try {
      return JSON.parse(JSON.stringify(value));
    } catch {
      return value;
    }
  }

  function str(value, fallback = "") {
    if (value === undefined || value === null) {
      return fallback;
    }

    return String(value);
  }

  function normalize(value) {
    return str(value).trim().toLowerCase();
  }

  function array(value) {
    return Array.isArray(value) ? value : [];
  }

  function currentUser() {
    try {
      if (window.NRH3?.auth?.current) {
        return NRH3.auth.current();
      }

      if (window.NRH2?.auth?.current) {
        return NRH2.auth.current();
      }

      return NRH2?.store?.user || null;
    } catch {
      return null;
    }
  }

  function username() {
    const user = currentUser();

    return (
      user?.login ||
      user?.username ||
      user?.name ||
      user?.email ||
      "anonymous"
    );
  }

  function emit(event, payload) {
    try {
      if (window.NRH2?.events?.emit) {
        NRH2.events.emit(event, payload);
      }
    } catch {
      /* optional */
    }

    try {
      window.dispatchEvent(
        new CustomEvent(
          "nrh7:" + event,
          {
            detail: clone(payload)
          }
        )
      );
    } catch {
      /* optional */
    }
  }

  function repository(repoId) {
    const repo =
      window.NRH4?.repositories?.get?.(repoId) ||
      window.NRH2?.repositories?.get?.(repoId);

    if (!repo) {
      throw new Error(
        "Repository not found: " + repoId
      );
    }

    return repo;
  }

  function ensureRepository(repoId) {
    repository(repoId);

    if (!state.pullRequests[repoId]) {
      state.pullRequests[repoId] = {};
    }

    if (!state.counters[repoId]) {
      state.counters[repoId] = 0;
    }

    if (!state.reviews[repoId]) {
      state.reviews[repoId] = {};
    }

    if (!state.reviewComments[repoId]) {
      state.reviewComments[repoId] = {};
    }

    if (!state.reviewers[repoId]) {
      state.reviewers[repoId] = {};
    }

    if (!state.events[repoId]) {
      state.events[repoId] = [];
    }

    if (!state.checks[repoId]) {
      state.checks[repoId] = {};
    }

    if (!state.mergeRecords[repoId]) {
      state.mergeRecords[repoId] = {};
    }
  }

  function getStored(repoId, number) {
    ensureRepository(repoId);

    return (
      state.pullRequests[repoId][
        String(number)
      ] || null
    );
  }

  function requirePR(repoId, number) {
    const pr =
      getStored(repoId, number);

    if (!pr) {
      throw new Error(
        `Pull request #${number} not found.`
      );
    }

    return pr;
  }

  function createEvent(
    repoId,
    number,
    type,
    payload = {}
  ) {
    ensureRepository(repoId);

    const event = {
      id: uid("prevent"),
      repositoryId: repoId,
      pullRequestNumber:
        Number(number),
      type,
      actor: username(),
      payload: clone(payload),
      createdAt: now()
    };

    state.events[repoId].push(
      event
    );

    emit(
      "pull_request:event",
      event
    );

    return event;
  }

  function update(pr) {
    pr.updatedAt = now();
  }

  function branchExists(repoId, branch) {
    try {
      if (
        window.NRH5?.branches?.get
      ) {
        return Boolean(
          NRH5.branches.get(
            repoId,
            branch
          )
        );
      }
    } catch {
      /* continue */
    }

    try {
      const repo =
        repository(repoId);

      return Boolean(
        repo.branches?.[branch]
      );
    } catch {
      return false;
    }
  }

  function resolveRef(repoId, ref) {
    if (
      window.NRH5?.resolveRef
    ) {
      return NRH5.resolveRef(
        repoId,
        ref
      );
    }

    if (
      window.NRH5?.git?.getHead
    ) {
      try {
        return NRH5.git.getHead(
          repoId,
          ref
        );
      } catch {
        return null;
      }
    }

    return null;
  }

  function compare(
    repoId,
    base,
    head
  ) {
    try {
      if (
        window.NRH5?.compare?.files
      ) {
        return NRH5.compare.files(
          repoId,
          base,
          head
        );
      }
    } catch {
      /* fallback */
    }

    return [];
  }

  function compareCommits(
    repoId,
    base,
    head
  ) {
    try {
      if (
        window.NRH5?.compare?.commits
      ) {
        return NRH5.compare.commits(
          repoId,
          base,
          head
        );
      }
    } catch {
      /* fallback */
    }

    return [];
  }

  function changedFiles(
    repoId,
    base,
    head
  ) {
    const result =
      compare(
        repoId,
        base,
        head
      );

    if (
      Array.isArray(result)
    ) {
      return result;
    }

    return result?.files || [];
  }

  function getFiles(repoId, ref) {
    try {
      if (
        window.NRH5?.git?.getFiles
      ) {
        return clone(
          NRH5.git.getFiles(
            repoId,
            ref
          )
        );
      }
    } catch {
      /* fallback */
    }

    try {
      const repo =
        repository(repoId);

      return clone(
        repo.files || {}
      );
    } catch {
      return {};
    }
  }

  function branchHead(
    repoId,
    branch
  ) {
    try {
      if (
        window.NRH5?.branches?.get
      ) {
        const result =
          NRH5.branches.get(
            repoId,
            branch
          );

        if (
          typeof result === "string"
        ) {
          return result;
        }

        return (
          result?.sha ||
          result?.commit ||
          result?.head ||
          null
        );
      }
    } catch {
      /* continue */
    }

    try {
      return resolveRef(
        repoId,
        branch
      );
    } catch {
      return null;
    }
  }

  /* ==========================================================
     PULL REQUEST CORE
     ========================================================== */

  const pullRequests = {

    create(repoId, input = {}) {
      ensureRepository(repoId);

      const title =
        str(input.title).trim();

      if (!title) {
        throw new Error(
          "Pull request title is required."
        );
      }

      const base =
        str(
          input.base ||
          input.baseBranch ||
          "main"
        ).trim();

      const head =
        str(
          input.head ||
          input.headBranch
        ).trim();

      if (!head) {
        throw new Error(
          "Head branch is required."
        );
      }

      if (
        base === head
      ) {
        throw new Error(
          "Base and head branches must be different."
        );
      }

      if (
        !branchExists(
          repoId,
          base
        )
      ) {
        throw new Error(
          `Base branch '${base}' does not exist.`
        );
      }

      if (
        !branchExists(
          repoId,
          head
        )
      ) {
        throw new Error(
          `Head branch '${head}' does not exist.`
        );
      }

      const existing =
        Object.values(
          state.pullRequests[
            repoId
          ]
        ).find(pr =>
          pr.state === "open" &&
          pr.base.ref === base &&
          pr.head.ref === head
        );

      if (existing) {
        throw new Error(
          "An open pull request already exists for these branches."
        );
      }

      state.counters[
        repoId
      ] += 1;

      const number =
        state.counters[
          repoId
        ];

      const headSha =
        branchHead(
          repoId,
          head
        );

      const baseSha =
        branchHead(
          repoId,
          base
        );

      const pr = {
        id: uid("pr"),

        nodeId: uid("node"),

        repositoryId: repoId,

        number,

        title,

        body:
          str(input.body),

        state:
          "open",

        draft:
          Boolean(input.draft),

        locked: false,

        author:
          input.author ||
          username(),

        base: {
          ref: base,
          sha: baseSha,
          repositoryId: repoId
        },

        head: {
          ref: head,
          sha: headSha,
          repositoryId: repoId
        },

        maintainerCanModify:
          input.maintainerCanModify !== false,

        mergeable: null,

        mergeableState:
          "unknown",

        rebaseable: null,

        commits: [],

        changedFiles: [],

        additions: 0,

        deletions: 0,

        reviewers: [],

        requestedReviewers: [],

        reviews: [],

        reviewComments: [],

        comments: [],

        labels: [],

        assignees: [],

        milestone:
          input.milestone ||
          null,

        linkedIssues: [],

        linkedCommits: [],

        checks: [],

        merge: null,

        createdAt: now(),

        updatedAt: now(),

        closedAt: null,

        mergedAt: null
      };

      state.pullRequests[
        repoId
      ][number] = pr;

      refresh(
        repoId,
        number
      );

      createEvent(
        repoId,
        number,
        "opened",
        {
          base,
          head
        }
      );

      if (
        input.issueNumber &&
        window.NRH6?.links?.pullRequest
      ) {
        try {
          NRH6.links.pullRequest(
            repoId,
            input.issueNumber,
            number
          );

          pr.linkedIssues.push(
            Number(
              input.issueNumber
            )
          );
        } catch {
          /* optional */
        }
      }

      emit(
        "pull_request:created",
        clone(pr)
      );

      return clone(pr);
    },

    get(repoId, number) {
      return clone(
        getStored(
          repoId,
          number
        )
      );
    },

    list(repoId, options = {}) {
      ensureRepository(repoId);

      let result =
        Object.values(
          state.pullRequests[
            repoId
          ]
        );

      const filterState =
        options.state ||
        "open";

      if (
        filterState !== "all"
      ) {
        result =
          result.filter(
            pr =>
              pr.state ===
              filterState
          );
      }

      if (
        options.base
      ) {
        result =
          result.filter(
            pr =>
              pr.base.ref ===
              options.base
          );
      }

      if (
        options.head
      ) {
        result =
          result.filter(
            pr =>
              pr.head.ref ===
              options.head
          );
      }

      if (
        options.author
      ) {
        result =
          result.filter(
            pr =>
              normalize(
                pr.author
              ) ===
              normalize(
                options.author
              )
          );
      }

      if (
        options.draft !==
        undefined
      ) {
        result =
          result.filter(
            pr =>
              pr.draft ===
              Boolean(
                options.draft
              )
          );
      }

      if (
        options.search
      ) {
        const query =
          normalize(
            options.search
          );

        result =
          result.filter(pr => {
            const text =
              `${pr.title} ${pr.body}`
                .toLowerCase();

            return text.includes(
              query
            );
          });
      }

      const sort =
        options.sort ||
        "created";

      result.sort(
        (a, b) => {
          if (
            sort === "updated"
          ) {
            return (
              new Date(
                b.updatedAt
              ) -
              new Date(
                a.updatedAt
              )
            );
          }

          if (
            sort === "number"
          ) {
            return (
              b.number -
              a.number
            );
          }

          return (
            new Date(
              b.createdAt
            ) -
            new Date(
              a.createdAt
            )
          );
        }
      );

      if (
        options.direction ===
        "asc"
      ) {
        result.reverse();
      }

      const page =
        Math.max(
          1,
          Number(
            options.page || 1
          )
        );

      const perPage =
        Math.max(
          1,
          Math.min(
            100,
            Number(
              options.perPage ||
              30
            )
          )
        );

      const start =
        (page - 1) *
        perPage;

      return {
        items: clone(
          result.slice(
            start,
            start + perPage
          )
        ),

        total:
          result.length,

        page,

        perPage,

        hasNextPage:
          start + perPage <
          result.length
      };
    },

    update(
      repoId,
      number,
      patch = {}
    ) {
      const pr =
        requirePR(
          repoId,
          number
        );

      if (
        patch.title !==
        undefined
      ) {
        const title =
          str(
            patch.title
          ).trim();

        if (!title) {
          throw new Error(
            "Pull request title cannot be empty."
          );
        }

        pr.title = title;
      }

      if (
        patch.body !==
        undefined
      ) {
        pr.body =
          str(
            patch.body
          );
      }

      if (
        patch.draft !==
        undefined
      ) {
        pr.draft =
          Boolean(
            patch.draft
          );
      }

      if (
        patch.maintainerCanModify !==
        undefined
      ) {
        pr.maintainerCanModify =
          Boolean(
            patch.maintainerCanModify
          );
      }

      if (
        patch.milestone !==
        undefined
      ) {
        pr.milestone =
          patch.milestone ||
          null;
      }

      if (
        patch.state ===
        "closed"
      ) {
        pr.state =
          "closed";

        pr.closedAt =
          now();
      }

      if (
        patch.state ===
        "open"
      ) {
        pr.state =
          "open";

        pr.closedAt =
          null;
      }

      update(pr);

      createEvent(
        repoId,
        number,
        "edited",
        {
          fields:
            Object.keys(
              patch
            )
        }
      );

      emit(
        "pull_request:updated",
        clone(pr)
      );

      return clone(pr);
    },

    close(repoId, number) {
      const pr =
        requirePR(
          repoId,
          number
        );

      if (
        pr.mergedAt
      ) {
        throw new Error(
          "Merged pull requests cannot be reopened or closed as ordinary PRs."
        );
      }

      pr.state =
        "closed";

      pr.closedAt =
        now();

      update(pr);

      createEvent(
        repoId,
        number,
        "closed"
      );

      emit(
        "pull_request:closed",
        clone(pr)
      );

      return clone(pr);
    },

    reopen(repoId, number) {
      const pr =
        requirePR(
          repoId,
          number
        );

      if (
        pr.mergedAt
      ) {
        throw new Error(
          "Merged pull requests cannot be reopened."
        );
      }

      pr.state =
        "open";

      pr.closedAt =
        null;

      update(pr);

      createEvent(
        repoId,
        number,
        "reopened"
      );

      emit(
        "pull_request:reopened",
        clone(pr)
      );

      return clone(pr);
    },

    readyForReview(
      repoId,
      number
    ) {
      const pr =
        requirePR(
          repoId,
          number
        );

      pr.draft =
        false;

      update(pr);

      createEvent(
        repoId,
        number,
        "ready_for_review"
      );

      emit(
        "pull_request:ready",
        clone(pr)
      );

      return clone(pr);
    }
  };

  /* ==========================================================
     REFRESH / DIFF / COMMITS
     ========================================================== */

  function refresh(
    repoId,
    number
  ) {
    const pr =
      requirePR(
        repoId,
        number
      );

    const headSha =
      branchHead(
        repoId,
        pr.head.ref
      );

    const baseSha =
      branchHead(
        repoId,
        pr.base.ref
      );

    pr.head.sha =
      headSha;

    pr.base.sha =
      baseSha;

    let files = [];

    try {
      files =
        changedFiles(
          repoId,
          pr.base.ref,
          pr.head.ref
        );
    } catch {
      files = [];
    }

    pr.changedFiles =
      clone(files);

    pr.additions =
      files.reduce(
        (total, file) =>
          total +
          Number(
            file.additions ||
            file.added ||
            0
          ),
        0
      );

    pr.deletions =
      files.reduce(
        (total, file) =>
          total +
          Number(
            file.deletions ||
            file.deleted ||
            0
          ),
        0
      );

    try {
      const commits =
        compareCommits(
          repoId,
          pr.base.ref,
          pr.head.ref
        );

      pr.commits =
        Array.isArray(
          commits
        )
          ? clone(commits)
          : clone(
              commits?.commits ||
              []
            );
    } catch {
      pr.commits = [];
    }

    try {
      const mergeBase =
        NRH5?.mergeBase?.find?.(
          repoId,
          pr.base.ref,
          pr.head.ref
        );

      pr.mergeBase =
        mergeBase ||
        null;
    } catch {
      pr.mergeBase =
        null;
    }

    evaluateMergeability(
      repoId,
      number
    );

    update(pr);

    return clone(pr);
  }

  function evaluateMergeability(
    repoId,
    number
  ) {
    const pr =
      requirePR(
        repoId,
        number
      );

    if (
      pr.state !== "open"
    ) {
      pr.mergeable =
        false;

      pr.mergeableState =
        "closed";

      return false;
    }

    try {
      const baseFiles =
        getFiles(
          repoId,
          pr.base.ref
        );

      const headFiles =
        getFiles(
          repoId,
          pr.head.ref
        );

      const baseKeys =
        new Set(
          Object.keys(
            baseFiles || {}
          )
        );

      const headKeys =
        new Set(
          Object.keys(
            headFiles || {}
          )
        );

      let additions = 0;
      let deletions = 0;

      for (
        const key of headKeys
      ) {
        if (
          !baseKeys.has(key)
        ) {
          additions++;
        }
      }

      for (
        const key of baseKeys
      ) {
        if (
          !headKeys.has(key)
        ) {
          deletions++;
        }
      }

      const sameTree =
        additions === 0 &&
        deletions === 0 &&
        JSON.stringify(
          baseFiles
        ) ===
        JSON.stringify(
          headFiles
        );

      if (
        sameTree
      ) {
        pr.mergeable =
          false;

        pr.mergeableState =
          "empty";

        return false;
      }

      /*
       * If the Git Engine exposes a merge
       * simulation, use it to detect conflicts.
       */

      if (
        window.NRH5?.merge?.branches
      ) {
        try {
          const simulated =
            NRH5.merge.branches(
              repoId,
              pr.base.ref,
              pr.head.ref,
              {
                dryRun: true
              }
            );

          if (
            simulated?.conflicts?.length
          ) {
            pr.mergeable =
              false;

            pr.mergeableState =
              "conflicts";

            return false;
          }
        } catch {
          /*
           * Some NRH5 versions perform
           * the actual merge in this method.
           * Do not execute destructive merge
           * logic during refresh.
           */
        }
      }

      pr.mergeable =
        true;

      pr.mergeableState =
        "clean";

      return true;

    } catch {
      pr.mergeable =
        null;

      pr.mergeableState =
        "unknown";

      return null;
    }
  }

  const changes = {

    refresh(repoId, number) {
      return refresh(
        repoId,
        number
      );
    },

    files(repoId, number) {
      const pr =
        requirePR(
          repoId,
          number
        );

      refresh(
        repoId,
        number
      );

      return clone(
        pr.changedFiles
      );
    },

    commits(repoId, number) {
      const pr =
        requirePR(
          repoId,
          number
        );

      refresh(
        repoId,
        number
      );

      return clone(
        pr.commits
      );
    },

    stats(repoId, number) {
      const pr =
        requirePR(
          repoId,
          number
        );

      refresh(
        repoId,
        number
      );

      return {
        files:
          pr.changedFiles.length,

        commits:
          pr.commits.length,

        additions:
          pr.additions,

        deletions:
          pr.deletions
      };
    }
  };

  /* ==========================================================
     REVIEWERS
     ========================================================== */

  const reviewers = {

    request(
      repoId,
      number,
      users = []
    ) {
      const pr =
        requirePR(
          repoId,
          number
        );

      const list =
        array(users)
          .map(
            user =>
              typeof user === "string"
                ? user
                : user?.login ||
                  user?.username
          )
          .filter(Boolean);

      list.forEach(user => {
        if (
          !pr.requestedReviewers
            .includes(user)
        ) {
          pr.requestedReviewers
            .push(user);
        }
      });

      update(pr);

      createEvent(
        repoId,
        number,
        "review_requested",
        {
          reviewers:
            clone(list)
        }
      );

      emit(
        "pull_request:review_requested",
        {
          pullRequest:
            clone(pr),
          reviewers:
            clone(list)
        }
      );

      return clone(
        pr.requestedReviewers
      );
    },

    remove(
      repoId,
      number,
      users = []
    ) {
      const pr =
        requirePR(
          repoId,
          number
        );

      const remove =
        new Set(
          array(users)
            .map(
              user =>
                typeof user === "string"
                  ? user
                  : user?.login ||
                    user?.username
            )
            .filter(Boolean)
        );

      pr.requestedReviewers =
        pr.requestedReviewers
          .filter(
            user =>
              !remove.has(user)
          );

      update(pr);

      createEvent(
        repoId,
        number,
        "review_request_removed",
        {
          reviewers:
            [...remove]
        }
      );

      return clone(
        pr.requestedReviewers
      );
    },

    list(repoId, number) {
      return clone(
        requirePR(
          repoId,
          number
        ).requestedReviewers
      );
    }
  };

  /* ==========================================================
     REVIEWS
     ========================================================== */

  const reviews = {

    create(
      repoId,
      number,
      input = {}
    ) {
      const pr =
        requirePR(
          repoId,
          number
        );

      const event =
        str(
          input.event
        ).toUpperCase();

      const allowed = [
        "",
        "PENDING",
        "COMMENT",
        "APPROVE",
        "REQUEST_CHANGES"
      ];

      if (
        !allowed.includes(event)
      ) {
        throw new Error(
          "Invalid review event."
        );
      }

      const commitId =
        input.commitId ||
        pr.head.sha ||
        null;

      const review = {
        id: uid("review"),

        nodeId: uid("node"),

        repositoryId: repoId,

        pullRequestNumber:
          Number(number),

        user:
          username(),

        body:
          str(input.body),

        event:
          event || "PENDING",

        state:
          event || "PENDING",

        commitId,

        comments: [],

        submittedAt:
          event &&
          event !== "PENDING"
            ? now()
            : null,

        createdAt: now(),

        updatedAt: now()
      };

      if (
        state.reviews[
          repoId
        ][number] === undefined
      ) {
        state.reviews[
          repoId
        ][number] = {};
      }

      state.reviews[
        repoId
      ][number][review.id] =
        review;

      pr.reviews.push(
        review.id
      );

      if (
        event ===
        "APPROVE"
      ) {
        pr.mergeableState =
          pr.mergeableState ===
          "clean"
            ? "clean"
            : pr.mergeableState;
      }

      update(pr);

      createEvent(
        repoId,
        number,
        "review_submitted",
        {
          reviewId:
            review.id,
          event:
            review.event
        }
      );

      emit(
        "pull_request:review",
        clone(review)
      );

      return clone(review);
    },

    list(repoId, number) {
      requirePR(
        repoId,
        number
      );

      return clone(
        Object.values(
          state.reviews[
            repoId
          ]?.[number] ||
          {}
        ).sort(
          (a, b) =>
            new Date(
              a.createdAt
            ) -
            new Date(
              b.createdAt
            )
        )
      );
    },

    get(
      repoId,
      number,
      reviewId
    ) {
      requirePR(
        repoId,
        number
      );

      return clone(
        state.reviews[
          repoId
        ]?.[number]?.[
          reviewId
        ] || null
      );
    },

    submit(
      repoId,
      number,
      reviewId,
      event,
      body
    ) {
      const review =
        this.get(
          repoId,
          number,
          reviewId
        );

      if (!review) {
        throw new Error(
          "Review not found."
        );
      }

      if (
        review.user !==
        username()
      ) {
        throw new Error(
          "Only the review author can submit this review."
        );
      }

      const normalized =
        str(event)
          .toUpperCase();

      if (
        ![
          "COMMENT",
          "APPROVE",
          "REQUEST_CHANGES"
        ].includes(
          normalized
        )
      ) {
        throw new Error(
          "Invalid review submission."
        );
      }

      const stored =
        state.reviews[
          repoId
        ][number][reviewId];

      stored.event =
        normalized;

      stored.state =
        normalized;

      if (
        body !== undefined
      ) {
        stored.body =
          str(body);
      }

      stored.submittedAt =
        now();

      stored.updatedAt =
        now();

      createEvent(
        repoId,
        number,
        "review_submitted",
        {
          reviewId,
          event:
            normalized
        }
      );

      emit(
        "pull_request:review_submitted",
        clone(stored)
      );

      return clone(stored);
    },

    dismiss(
      repoId,
      number,
      reviewId,
      message = ""
    ) {
      const review =
        this.get(
          repoId,
          number,
          reviewId
        );

      if (!review) {
        throw new Error(
          "Review not found."
        );
      }

      const stored =
        state.reviews[
          repoId
        ][number][reviewId];

      stored.state =
        "DISMISSED";

      stored.dismissed =
        true;

      stored.dismissalMessage =
        str(message);

      stored.updatedAt =
        now();

      createEvent(
        repoId,
        number,
        "review_dismissed",
        {
          reviewId,
          message
        }
      );

      return clone(stored);
    },

    summary(repoId, number) {
      const list =
        this.list(
          repoId,
          number
        );

      return {
        total:
          list.length,

        pending:
          list.filter(
            review =>
              review.state ===
              "PENDING"
          ).length,

        approved:
          list.filter(
            review =>
              review.state ===
              "APPROVE"
          ).length,

        changesRequested:
          list.filter(
            review =>
              review.state ===
              "REQUEST_CHANGES"
          ).length,

        comments:
          list.filter(
            review =>
              review.state ===
              "COMMENT"
          ).length,

        dismissed:
          list.filter(
            review =>
              review.state ===
              "DISMISSED"
          ).length
      };
    }
  };

  /* ==========================================================
     REVIEW COMMENTS
     ========================================================== */

  const reviewComments = {

    create(
      repoId,
      number,
      input = {}
    ) {
      const pr =
        requirePR(
          repoId,
          number
        );

      const body =
        str(
          input.body
        ).trim();

      if (!body) {
        throw new Error(
          "Review comment body is required."
        );
      }

      const path =
        str(
          input.path
        ).trim();

      if (!path) {
        throw new Error(
          "Review comment path is required."
        );
      }

      const side =
        str(
          input.side ||
          "RIGHT"
        ).toUpperCase();

      if (
        ![
          "LEFT",
          "RIGHT"
        ].includes(side)
      ) {
        throw new Error(
          "Invalid review comment side."
        );
      }

      const comment = {
        id: uid("reviewcomment"),

        nodeId: uid("node"),

        repositoryId: repoId,

        pullRequestNumber:
          Number(number),

        reviewId:
          input.reviewId ||
          null,

        user:
          username(),

        body,

        path,

        line:
          input.line !== undefined
            ? Number(
                input.line
              )
            : null,

        startLine:
          input.startLine !==
          undefined
            ? Number(
                input.startLine
              )
            : null,

        side,

        startSide:
          str(
            input.startSide ||
            side
          ).toUpperCase(),

        commitId:
          input.commitId ||
          pr.head.sha ||
          null,

        inReplyTo:
          input.inReplyTo ||
          null,

        subjectType:
          input.subjectType ||
          "line",

        createdAt: now(),

        updatedAt: now(),

        resolved: false
      };

      if (
        !state.reviewComments[
          repoId
        ][number]
      ) {
        state.reviewComments[
          repoId
        ][number] = {};
      }

      state.reviewComments[
        repoId
      ][number][comment.id] =
        comment;

      pr.reviewComments.push(
        comment.id
      );

      if (
        comment.reviewId
      ) {
        const review =
          state.reviews[
            repoId
          ][number]?.[
            comment.reviewId
          ];

        if (review) {
          review.comments.push(
            comment.id
          );
        }
      }

      update(pr);

      createEvent(
        repoId,
        number,
        "review_comment_created",
        {
          commentId:
            comment.id,
          path,
          line:
            comment.line
        }
      );

      emit(
        "pull_request:review_comment",
        clone(comment)
      );

      return clone(comment);
    },

    list(repoId, number) {
      requirePR(
        repoId,
        number
      );

      return clone(
        Object.values(
          state.reviewComments[
            repoId
          ]?.[number] ||
          {}
        ).sort(
          (a, b) =>
            new Date(
              a.createdAt
            ) -
            new Date(
              b.createdAt
            )
        )
      );
    },

    get(
      repoId,
      number,
      commentId
    ) {
      requirePR(
        repoId,
        number
      );

      return clone(
        state.reviewComments[
          repoId
        ]?.[number]?.[
          commentId
        ] || null
      );
    },

    reply(
      repoId,
      number,
      commentId,
      body
    ) {
      const parent =
        this.get(
          repoId,
          number,
          commentId
        );

      if (!parent) {
        throw new Error(
          "Parent review comment not found."
        );
      }

      return this.create(
        repoId,
        number,
        {
          body,
          path:
            parent.path,
          line:
            parent.line,
          side:
            parent.side,
          startLine:
            parent.startLine,
          startSide:
            parent.startSide,
          commitId:
            parent.commitId,
          inReplyTo:
            parent.id,
          subjectType:
            parent.subjectType
        }
      );
    },

    resolve(
      repoId,
      number,
      commentId
    ) {
      const comment =
        this.get(
          repoId,
          number,
          commentId
        );

      if (!comment) {
        throw new Error(
          "Review comment not found."
        );
      }

      const stored =
        state.reviewComments[
          repoId
        ][number][commentId];

      stored.resolved =
        true;

      stored.resolvedBy =
        username();

      stored.resolvedAt =
        now();

      stored.updatedAt =
        now();

      createEvent(
        repoId,
        number,
        "review_comment_resolved",
        {
          commentId
        }
      );

      return clone(stored);
    },

    unresolve(
      repoId,
      number,
      commentId
    ) {
      const comment =
        this.get(
          repoId,
          number,
          commentId
        );

      if (!comment) {
        throw new Error(
          "Review comment not found."
        );
      }

      const stored =
        state.reviewComments[
          repoId
        ][number][commentId];

      stored.resolved =
        false;

      stored.resolvedBy =
        null;

      stored.resolvedAt =
        null;

      stored.updatedAt =
        now();

      return clone(stored);
    }
  };

  /* ==========================================================
     ISSUE INTEGRATION
     ========================================================== */

  const issues = {

    link(
      repoId,
      prNumber,
      issueNumber
    ) {
      const pr =
        requirePR(
          repoId,
          prNumber
        );

      if (
        !window.NRH6?.issues?.get
      ) {
        throw new Error(
          "NRH6 Issues Engine is unavailable."
        );
      }

      const issue =
        NRH6.issues.get(
          repoId,
          issueNumber
        );

      if (!issue) {
        throw new Error(
          "Issue not found."
        );
      }

      if (
        !pr.linkedIssues.includes(
          Number(issueNumber)
        )
      ) {
        pr.linkedIssues.push(
          Number(issueNumber)
        );
      }

      try {
        NRH6.links.pullRequest(
          repoId,
          issueNumber,
          prNumber
        );
      } catch {
        /* optional */
      }

      update(pr);

      createEvent(
        repoId,
        prNumber,
        "issue_linked",
        {
          issueNumber
        }
      );

      return clone(pr);
    },

    list(
      repoId,
      prNumber
    ) {
      const pr =
        requirePR(
          repoId,
          prNumber
        );

      if (
        !window.NRH6?.issues?.get
      ) {
        return [];
      }

      return clone(
        pr.linkedIssues
          .map(
            number =>
              NRH6.issues.get(
                repoId,
                number
              )
          )
          .filter(Boolean)
      );
    },

    closeLinked(
      repoId,
      prNumber
    ) {
      const pr =
        requirePR(
          repoId,
          prNumber
        );

      if (
        !window.NRH6?.issues?.close
      ) {
        return [];
      }

      const closed = [];

      pr.linkedIssues.forEach(
        number => {
          try {
            const result =
              NRH6.issues.close(
                repoId,
                number,
                "completed"
              );

            closed.push(
              result
            );
          } catch {
            /* continue */
          }
        }
      );

      return clone(closed);
    }
  };

  /* ==========================================================
     LABELS / ASSIGNEES / MILESTONES
     ========================================================== */

  const metadata = {

    labels: {
      set(repoId, number, labels) {
        const pr =
          requirePR(
            repoId,
            number
          );

        pr.labels =
          array(labels)
            .map(
              label =>
                typeof label ===
                "string"
                  ? label
                  : label?.name
            )
            .filter(Boolean);

        update(pr);

        createEvent(
          repoId,
          number,
          "labels_updated",
          {
            labels:
              clone(
                pr.labels
              )
          }
        );

        return clone(
          pr.labels
        );
      }
    },

    assignees: {
      set(
        repoId,
        number,
        users
      ) {
        const pr =
          requirePR(
            repoId,
            number
          );

        pr.assignees =
          array(users)
            .map(
              user =>
                typeof user ===
                "string"
                  ? user
                  : user?.login ||
                    user?.username
            )
            .filter(Boolean);

        update(pr);

        createEvent(
          repoId,
          number,
          "assignees_updated",
          {
            assignees:
              clone(
                pr.assignees
              )
          }
        );

        return clone(
          pr.assignees
        );
      }
    },

    milestone: {
      set(
        repoId,
        number,
        milestone
      ) {
        const pr =
          requirePR(
            repoId,
            number
          );

        pr.milestone =
          milestone ||
          null;

        update(pr);

        createEvent(
          repoId,
          number,
          "milestone_updated",
          {
            milestone:
              pr.milestone
          }
        );

        return clone(pr);
      }
    }
  };

  /* ==========================================================
     GENERAL PR COMMENTS
     ========================================================== */

  const comments = {

    create(
      repoId,
      number,
      body
    ) {
      const pr =
        requirePR(
          repoId,
          number
        );

      if (
        pr.locked
      ) {
        throw new Error(
          "Pull request is locked."
        );
      }

      const value =
        str(body).trim();

      if (!value) {
        throw new Error(
          "Comment body is required."
        );
      }

      const comment = {
        id: uid("prcomment"),

        nodeId: uid("node"),

        repositoryId: repoId,

        pullRequestNumber:
          Number(number),

        user:
          username(),

        body: value,

        createdAt: now(),

        updatedAt: now()
      };

      pr.comments.push(
        comment
      );

      update(pr);

      createEvent(
        repoId,
        number,
        "commented",
        {
          commentId:
            comment.id
        }
      );

      emit(
        "pull_request:comment",
        clone(comment)
      );

      return clone(comment);
    },

    list(repoId, number) {
      return clone(
        requirePR(
          repoId,
          number
        ).comments
      );
    }
  };

  /* ==========================================================
     CHECKS
     ========================================================== */

  const checks = {

    set(
      repoId,
      number,
      input = {}
    ) {
      const pr =
        requirePR(
          repoId,
          number
        );

      const check = {
        id: uid("check"),

        name:
          str(
            input.name ||
            "CI"
          ),

        status:
          input.status ||
          "queued",

        conclusion:
          input.conclusion ||
          null,

        sha:
          input.sha ||
          pr.head.sha ||
          null,

        url:
          input.url ||
          null,

        startedAt:
          input.startedAt ||
          now(),

        completedAt:
          input.completedAt ||
          null,

        output:
          input.output ||
          ""
      };

      if (
        !state.checks[
          repoId
        ][number]
      ) {
        state.checks[
          repoId
        ][number] = {};
      }

      state.checks[
        repoId
      ][number][
        check.id
      ] = check;

      pr.checks.push(
        check.id
      );

      update(pr);

      emit(
        "pull_request:check",
        clone(check)
      );

      return clone(check);
    },

    complete(
      repoId,
      number,
      checkId,
      conclusion,
      output = ""
    ) {
      const pr =
        requirePR(
          repoId,
          number
        );

      const check =
        state.checks[
          repoId
        ]?.[number]?.[
          checkId
        ];

      if (!check) {
        throw new Error(
          "Check not found."
        );
      }

      check.status =
        "completed";

      check.conclusion =
        conclusion;

      check.output =
        output;

      check.completedAt =
        now();

      update(pr);

      return clone(check);
    },

    list(repoId, number) {
      requirePR(
        repoId,
        number
      );

      return clone(
        Object.values(
          state.checks[
            repoId
          ]?.[number] ||
          {}
        )
      );
    },

    summary(repoId, number) {
      const list =
        this.list(
          repoId,
          number
        );

      return {
        total:
          list.length,

        queued:
          list.filter(
            check =>
              check.status ===
              "queued"
          ).length,

        running:
          list.filter(
            check =>
              check.status ===
              "in_progress"
          ).length,

        passed:
          list.filter(
            check =>
              check.conclusion ===
              "success"
          ).length,

        failed:
          list.filter(
            check =>
              [
                "failure",
                "cancelled",
                "timed_out"
              ].includes(
                check.conclusion
              )
          ).length
      };
    },

    canMerge(
      repoId,
      number
    ) {
      const summary =
        this.summary(
          repoId,
          number
        );

      return (
        summary.failed === 0 &&
        summary.running === 0 &&
        summary.queued === 0
      );
    }
  };

  /* ==========================================================
     MERGE
     ========================================================== */

  const merge = {

    canMerge(
      repoId,
      number
    ) {
      const pr =
        requirePR(
          repoId,
          number
        );

      refresh(
        repoId,
        number
      );

      if (
        pr.state !== "open"
      ) {
        return {
          allowed: false,
          reason:
            "Pull request is not open."
        };
      }

      if (
        pr.draft
      ) {
        return {
          allowed: false,
          reason:
            "Draft pull request cannot be merged."
        };
      }

      if (
        pr.mergeable === false
      ) {
        return {
          allowed: false,
          reason:
            pr.mergeableState
        };
      }

      const reviewSummary =
        reviews.summary(
          repoId,
          number
        );

      if (
        reviewSummary.changesRequested >
        0
      ) {
        return {
          allowed: false,
          reason:
            "Changes have been requested."
        };
      }

      return {
        allowed: true,
        reason: "clean"
      };
    },

    execute(
      repoId,
      number,
      options = {}
    ) {
      const pr =
        requirePR(
          repoId,
          number
        );

      const check =
        this.canMerge(
          repoId,
          number
        );

      if (
        !check.allowed
      ) {
        throw new Error(
          `Pull request cannot be merged: ${check.reason}`
        );
      }

      const method =
        options.method ||
        "merge";

      const allowedMethods = [
        "merge",
        "squash",
        "rebase"
      ];

      if (
        !allowedMethods.includes(
          method
        )
      ) {
        throw new Error(
          "Unsupported merge method."
        );
      }

      const message =
        options.message ||
        `${pr.title} (#${pr.number})`;

      let result = null;

      /*
       * Prefer the Git Engine's branch merge.
       * If the current NRH5 implementation
       * exposes a different signature, this
       * block remains isolated for later
       * adapter work.
       */

      if (
        window.NRH5?.merge?.branches
      ) {
        try {
          result =
            NRH5.merge.branches(
              repoId,
              pr.base.ref,
              pr.head.ref,
              {
                message,
                method,
                pullRequest:
                  pr.number
              }
            );
        } catch (error) {
          /*
           * The PR remains open when the
           * underlying Git merge fails.
           */
          throw error;
        }
      } else {
        throw new Error(
          "Git Engine merge service is unavailable."
        );
      }

      const mergeSha =
        result?.sha ||
        result?.commit ||
        result?.id ||
        null;

      pr.merge = {
        sha:
          mergeSha,

        method,

        message,

        mergedBy:
          username(),

        result:
          clone(result),

        createdAt:
          now()
      };

      pr.mergedAt =
        now();

      pr.closedAt =
        now();

      pr.state =
        "closed";

      pr.mergeable =
        false;

      pr.mergeableState =
        "merged";

      update(pr);

      state.mergeRecords[
        repoId
      ][number] =
        clone(pr.merge);

      createEvent(
        repoId,
        number,
        "merged",
        {
          sha:
            mergeSha,
          method
        }
      );

      /*
       * If this PR is associated with
       * Issues, close them after a
       * successful merge.
       */

      if (
        options.closeLinkedIssues !==
        false
      ) {
        try {
          issues.closeLinked(
            repoId,
            number
          );
        } catch {
          /* optional */
        }
      }

      emit(
        "pull_request:merged",
        clone(pr)
      );

      return clone(pr);
    },

    abort(
      repoId,
      number
    ) {
      const pr =
        requirePR(
          repoId,
          number
        );

      if (
        pr.state !== "open"
      ) {
        throw new Error(
          "Only open pull requests can be aborted."
        );
      }

      createEvent(
        repoId,
        number,
        "merge_aborted"
      );

      return clone(pr);
    }
  };

  /* ==========================================================
     DIFF
     ========================================================== */

  const diff = {

    files(
      repoId,
      number
    ) {
      const pr =
        requirePR(
          repoId,
          number
        );

      refresh(
        repoId,
        number
      );

      return clone(
        pr.changedFiles
      );
    },

    file(
      repoId,
      number,
      path
    ) {
      const pr =
        requirePR(
          repoId,
          number
        );

      try {
        if (
          window.NRH5?.diff?.file
        ) {
          return clone(
            NRH5.diff.file(
              repoId,
              pr.base.ref,
              pr.head.ref,
              path
            )
          );
        }
      } catch {
        /* fallback */
      }

      const file =
        pr.changedFiles.find(
          item =>
            item.path ===
            path
        );

      return clone(
        file || null
      );
    }
  };

  /* ==========================================================
     TIMELINE
     ========================================================== */

  const timeline = {

    list(repoId, number) {
      requirePR(
        repoId,
        number
      );

      return clone(
        state.events[
          repoId
        ].filter(
          event =>
            Number(
              event.pullRequestNumber
            ) ===
            Number(number)
        ).sort(
          (a, b) =>
            new Date(
              a.createdAt
            ) -
            new Date(
              b.createdAt
            )
        )
      );
    }
  };

  /* ==========================================================
     STATISTICS
     ========================================================== */

  const statistics = {

    repository(repoId) {
      const result =
        pullRequests.list(
          repoId,
          {
            state: "all",
            perPage: 100
          }
        ).items;

      const open =
        result.filter(
          pr =>
            pr.state === "open"
        ).length;

      const closed =
        result.filter(
          pr =>
            pr.state === "closed" &&
            !pr.mergedAt
        ).length;

      const merged =
        result.filter(
          pr =>
            Boolean(
              pr.mergedAt
            )
        ).length;

      const drafts =
        result.filter(
          pr =>
            pr.draft
        ).length;

      const totalComments =
        result.reduce(
          (sum, pr) =>
            sum +
            pr.comments.length +
            pr.reviewComments.length,
          0
        );

      return {
        total:
          result.length,

        open,

        closed,

        merged,

        drafts,

        comments:
          totalComments,

        mergeRate:
          result.length
            ? Math.round(
                (merged /
                  result.length) *
                100
              )
            : 0
      };
    }
  };

  /* ==========================================================
     SERIALIZATION
     ========================================================== */

  const serialization = {

    exportRepository(repoId) {
      ensureRepository(repoId);

      return {
        version:
          VERSION,

        repositoryId:
          repoId,

        exportedAt:
          now(),

        pullRequests:
          clone(
            state.pullRequests[
              repoId
            ]
          ),

        reviews:
          clone(
            state.reviews[
              repoId
            ]
          ),

        reviewComments:
          clone(
            state.reviewComments[
              repoId
            ]
          ),

        reviewers:
          clone(
            state.reviewers[
              repoId
            ]
          ),

        events:
          clone(
            state.events[
              repoId
            ]
          ),

        checks:
          clone(
            state.checks[
              repoId
            ]
          ),

        mergeRecords:
          clone(
            state.mergeRecords[
              repoId
            ]
          )
      };
    },

    importRepository(
      repoId,
      data
    ) {
      repository(repoId);

      if (
        !data ||
        typeof data !==
        "object"
      ) {
        throw new Error(
          "Invalid Pull Request export."
        );
      }

      ensureRepository(repoId);

      if (
        data.pullRequests
      ) {
        state.pullRequests[
          repoId
        ] =
          clone(
            data.pullRequests
          );
      }

      if (
        data.reviews
      ) {
        state.reviews[
          repoId
        ] =
          clone(
            data.reviews
          );
      }

      if (
        data.reviewComments
      ) {
        state.reviewComments[
          repoId
        ] =
          clone(
            data.reviewComments
          );
      }

      if (
        data.reviewers
      ) {
        state.reviewers[
          repoId
        ] =
          clone(
            data.reviewers
          );
      }

      if (
        data.events
      ) {
        state.events[
          repoId
        ] =
          clone(
            data.events
          );
      }

      if (
        data.checks
      ) {
        state.checks[
          repoId
        ] =
          clone(
            data.checks
          );
      }

      if (
        data.mergeRecords
      ) {
        state.mergeRecords[
          repoId
        ] =
          clone(
            data.mergeRecords
          );
      }

      const numbers =
        Object.keys(
          state.pullRequests[
            repoId
          ]
        ).map(Number);

      state.counters[
        repoId
      ] =
        numbers.length
          ? Math.max(...numbers)
          : 0;

      emit(
        "pull_requests:imported",
        {
          repositoryId:
            repoId
        }
      );

      return true;
    }
  };

  /* ==========================================================
     UI
     ========================================================== */

  const ui = {

    stateBadge(pr) {
      if (
        pr.mergedAt
      ) {
        return `
          <span
            class="nrh-pr-badge merged"
          >
            ✓ Merged
          </span>
        `;
      }

      if (
        pr.state ===
        "closed"
      ) {
        return `
          <span
            class="nrh-pr-badge closed"
          >
            Closed
          </span>
        `;
      }

      if (
        pr.draft
      ) {
        return `
          <span
            class="nrh-pr-badge draft"
          >
            Draft
          </span>
        `;
      }

      return `
        <span
          class="nrh-pr-badge open"
        >
          Open
        </span>
      `;
    },

    row(pr) {
      const review =
        reviews.summary(
          pr.repositoryId,
          pr.number
        );

      return `
        <article
          class="nrh-pr-row"
          data-repository="${pr.repositoryId}"
          data-pr="${pr.number}"
        >

          <div
            class="nrh-pr-icon"
          >
            ${pr.mergedAt
              ? "✓"
              : pr.state === "open"
                ? "↗"
                : "×"}
          </div>

          <div
            class="nrh-pr-main"
          >

            <div
              class="nrh-pr-title"
            >
              <strong>
                #${pr.number}
                ${pr.title}
              </strong>

              ${ui.stateBadge(pr)}
            </div>

            <div
              class="nrh-pr-meta"
            >
              ${pr.author}
              wants to merge

              <strong>
                ${pr.head.ref}
              </strong>

              into

              <strong>
                ${pr.base.ref}
              </strong>
            </div>

            <div
              class="nrh-pr-stats"
            >
              ${pr.commits.length}
              commits ·

              ${pr.changedFiles.length}
              files ·

              +${pr.additions}
              / -${pr.deletions}

              ·

              ${review.approved}
              approvals
            </div>

          </div>

        </article>
      `;
    },

    list(
      repoId,
      options = {}
    ) {
      const result =
        pullRequests.list(
          repoId,
          options
        );

      return `
        <section
          class="nrh-pr-list"
          data-repository="${repoId}"
        >

          <header
            class="nrh-pr-list-header"
          >
            <strong>
              Pull Requests
            </strong>

            <span>
              ${result.total}
            </span>
          </header>

          <div>
            ${
              result.items.length
                ? result.items
                    .map(
                      pr =>
                        ui.row(pr)
                    )
                    .join("")
                : `
                    <div
                      class="nrh-empty"
                    >
                      No pull requests found.
                    </div>
                  `
            }
          </div>

        </section>
      `;
    },

    detail(
      repoId,
      number
    ) {
      const pr =
        pullRequests.get(
          repoId,
          number
        );

      if (!pr) {
        return `
          <div
            class="nrh-error"
          >
            Pull request not found.
          </div>
        `;
      }

      refresh(
        repoId,
        number
      );

      const reviewSummary =
        reviews.summary(
          repoId,
          number
        );

      const checkSummary =
        checks.summary(
          repoId,
          number
        );

      const reviewList =
        reviews.list(
          repoId,
          number
        );

      const commentsList =
        reviewComments.list(
          repoId,
          number
        );

      return `
        <article
          class="nrh-pr-detail"
          data-repository="${repoId}"
          data-pr="${number}"
        >

          <header
            class="nrh-pr-detail-header"
          >

            <div>

              <h1>
                ${pr.title}
              </h1>

              <div
                class="nrh-pr-subtitle"
              >
                ${ui.stateBadge(pr)}

                <strong>
                  #${pr.number}
                </strong>

                opened by

                <strong>
                  @${pr.author}
                </strong>
              </div>

            </div>

            <div>

              ${
                pr.state === "open"
                  ? `
                    <button
                      data-action="close-pr"
                      data-pr="${number}"
                    >
                      Close
                    </button>
                  `
                  : !pr.mergedAt
                    ? `
                      <button
                        data-action="reopen-pr"
                        data-pr="${number}"
                      >
                        Reopen
                      </button>
                    `
                    : ""
              }

            </div>

          </header>

          <section
            class="nrh-pr-description"
          >
            ${pr.body}
          </section>

          <section
            class="nrh-pr-branches"
          >

            <div>
              <strong>
                ${pr.head.ref}
              </strong>

              <small>
                ${pr.head.sha || "unknown"}
              </small>
            </div>

            <div>
              →
            </div>

            <div>
              <strong>
                ${pr.base.ref}
              </strong>

              <small>
                ${pr.base.sha || "unknown"}
              </small>
            </div>

          </section>

          <section
            class="nrh-pr-stats"
          >

            <div>
              <strong>
                ${pr.commits.length}
              </strong>
              commits
            </div>

            <div>
              <strong>
                ${pr.changedFiles.length}
              </strong>
              files
            </div>

            <div>
              <strong>
                +${pr.additions}
              </strong>
              additions
            </div>

            <div>
              <strong>
                -${pr.deletions}
              </strong>
              deletions
            </div>

          </section>

          <section
            class="nrh-pr-reviews"
          >

            <h2>
              Reviews
            </h2>

            <div>
              Approved:
              ${reviewSummary.approved}
            </div>

            <div>
              Changes requested:
              ${reviewSummary.changesRequested}
            </div>

            <div>
              Comments:
              ${reviewSummary.comments}
            </div>

            ${
              reviewList
                .map(
                  review => `
                    <article
                      class="nrh-review"
                    >

                      <strong>
                        @${review.user}
                      </strong>

                      <span>
                        ${review.state}
                      </span>

                      <p>
                        ${review.body}
                      </p>

                    </article>
                  `
                )
                .join("")
            }

          </section>

          <section
            class="nrh-pr-checks"
          >

            <h2>
              Checks
            </h2>

            <div>
              Passed:
              ${checkSummary.passed}
            </div>

            <div>
              Failed:
              ${checkSummary.failed}
            </div>

            <div>
              Running:
              ${checkSummary.running}
            </div>

          </section>

          <section
            class="nrh-pr-review-comments"
          >

            <h2>
              Review comments
            </h2>

            ${
              commentsList
                .map(
                  comment => `
                    <article
                      class="nrh-review-comment"
                    >

                      <header>
                        <strong>
                          @${comment.user}
                        </strong>

                        <code>
                          ${comment.path}
                        </code>

                        ${
                          comment.line
                            ? `:${comment.line}`
                            : ""
                        }
                      </header>

                      <div>
                        ${comment.body}
                      </div>

                      <footer>
                        ${
                          comment.resolved
                            ? "Resolved"
                            : "Unresolved"
                        }
                      </footer>

                    </article>
                  `
                )
                .join("")
            }

          </section>

          <section
            class="nrh-pr-diff"
          >

            <h2>
              Changed files
            </h2>

            ${
              pr.changedFiles
                .map(
                  file => `
                    <div
                      class="nrh-diff-file"
                    >

                      <strong>
                        ${file.path || file.filename || ""}
                      </strong>

                      <span>
                        +${file.additions || 0}
                        -
                        ${file.deletions || 0}
                      </span>

                    </div>
                  `
                )
                .join("")
            }

          </section>

          ${
            pr.state === "open" &&
            !pr.draft
              ? `
                <section
                  class="nrh-pr-merge-box"
                >

                  <strong>
                    ${
                      pr.mergeableState ===
                      "clean"
                        ? "Ready to merge"
                        : pr.mergeableState
                    }
                  </strong>

                  <button
                    data-action="merge-pr"
                    data-pr="${number}"
                  >
                    Merge Pull Request
                  </button>

                </section>
              `
              : ""
          }

        </article>
      `;
    }
  };

  /* ==========================================================
     PERSISTENCE
     ========================================================== */

  const persistence = {

    key:
      "neural_raphael_hub_pr_v7",

    save() {
      try {
        localStorage.setItem(
          this.key,
          JSON.stringify({
            version:
              VERSION,
            state
          })
        );

        return true;
      } catch {
        return false;
      }
    },

    restore() {
      try {
        const raw =
          localStorage.getItem(
            this.key
          );

        if (!raw) {
          return false;
        }

        const payload =
          JSON.parse(raw);

        if (
          !payload?.state
        ) {
          return false;
        }

        Object.assign(
          state,
          payload.state
        );

        return true;
      } catch {
        return false;
      }
    },

    clear() {
      try {
        localStorage.removeItem(
          this.key
        );

        return true;
      } catch {
        return false;
      }
    }
  };

  /* ==========================================================
     COMMAND REGISTRATION
     ========================================================== */

  function registerCommands() {
    if (
      !window.NRH2?.commands?.register
    ) {
      return;
    }

    NRH2.commands.register(
      "pr:list",
      ({
        repositoryId,
        state:
          filterState
      } = {}) => {
        return pullRequests.list(
          repositoryId,
          {
            state:
              filterState ||
              "open",
            perPage: 100
          }
        );
      }
    );

    NRH2.commands.register(
      "pr:create",
      ({
        repositoryId,
        title,
        body,
        base,
        head,
        draft
      } = {}) => {
        return pullRequests.create(
          repositoryId,
          {
            title,
            body,
            base,
            head,
            draft
          }
        );
      }
    );

    NRH2.commands.register(
      "pr:merge",
      ({
        repositoryId,
        number,
        method
      } = {}) => {
        return merge.execute(
          repositoryId,
          number,
          {
            method
          }
        );
      }
    );

    NRH2.commands.register(
      "pr:review",
      ({
        repositoryId,
        number,
        event,
        body
      } = {}) => {
        return reviews.create(
          repositoryId,
          number,
          {
            event,
            body
          }
        );
      }
    );

    NRH2.commands.register(
      "pr:refresh",
      ({
        repositoryId,
        number
      } = {}) => {
        return changes.refresh(
          repositoryId,
          number
        );
      }
    );
  }

  /* ==========================================================
     EVENT WIRING
     ========================================================== */

  function wireEvents() {

    window.addEventListener(
      "beforeunload",
      () => {
        persistence.save();
      }
    );

    if (
      window.NRH2?.events?.on
    ) {

      NRH2.events.on(
        "repository:deleted",
        payload => {
          const repoId =
            payload?.id ||
            payload?.repositoryId;

          if (!repoId) {
            return;
          }

          delete state.pullRequests[
            repoId
          ];

          delete state.counters[
            repoId
          ];

          delete state.reviews[
            repoId
          ];

          delete state.reviewComments[
            repoId
          ];

          delete state.reviewers[
            repoId
          ];

          delete state.events[
            repoId
          ];

          delete state.checks[
            repoId
          ];

          delete state.mergeRecords[
            repoId
          ];
        }
      );

      NRH2.events.on(
        "git:commit",
        payload => {
          const repoId =
            payload?.repositoryId ||
            payload?.repoId;

          if (!repoId) {
            return;
          }

          Object.values(
            state.pullRequests[
              repoId
            ] || {}
          )
          .filter(
            pr =>
              pr.state === "open"
          )
          .forEach(
            pr => {
              try {
                refresh(
                  repoId,
                  pr.number
                );
              } catch {
                /* continue */
              }
            }
          );
        }
      );
    }
  }

  /* ==========================================================
     INIT
     ========================================================== */

  function init() {
    persistence.restore();

    registerCommands();

    wireEvents();

    emit(
      "initialized",
      {
        version:
          VERSION
      }
    );

    console.log(
      `%cNRH7 Pull Request Engine ${VERSION}`,
      "color:#a371f7;font-weight:bold"
    );

    return api;
  }

  /* ==========================================================
     PUBLIC API
     ========================================================== */

  const api = {
    VERSION,

    state,

    init,

    pullRequests,

    changes,

    reviewers,

    reviews,

    reviewComments,

    issues,

    metadata,

    comments,

    checks,

    merge,

    diff,

    timeline,

    statistics,

    serialization,

    persistence,

    ui
  };

  return api;
})();

window.NRH7 = NRH7;

NRH7.init();

/* ============================================================
   END BLOCK 7
   ============================================================ */
</script>

</script></body></html>
