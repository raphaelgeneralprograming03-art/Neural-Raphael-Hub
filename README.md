
<html lang="pt-BR">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
  <title>Neural Raphael Hub · GitHub Edition (Full Unified Suite)</title>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700&family=JetBrains+Mono:wght@400;500&display=swap" rel="stylesheet">
  <style>
    :root {
      --bg: #080c14; --b2: #111827; --bd: #1f2937; --fg: #f3f4f6; --mu: #9ca3af;
      --ac: #818cf8; --gr: #34d399; --rd: #f87171; --pu: #c084fc; --ad: #0f2a24;
      --dd: #2d1517; --gd: linear-gradient(90deg, #6366f1, #a855f7, #ec4899);
      box-sizing: border-box; padding-top: env(safe-area-inset-top, 0px); padding-bottom: env(safe-area-inset-bottom, 0px);
    }
    @media (prefers-color-scheme: light) {
      :root:not([data-theme=dark]) {
        --bg: #f8fafc; --b2: #fff; --bd: #d9dee8; --fg: #111827; --mu: #4b5563;
        --ac: #4f46e5; --gr: #059669; --rd: #dc2626; --pu: #9333ea; --ad: #d1fae5; --dd: #fee2e2;
      }
    }
    :root[data-theme=light] {
      --bg: #f8fafc; --b2: #fff; --bd: #d9dee8; --fg: #111827; --mu: #4b5563;
      --ac: #4f46e5; --gr: #059669; --rd: #dc2626; --pu: #9333ea; --ad: #d1fae5; --dd: #fee2e2;
    }
    html { scroll-padding-top: env(safe-area-inset-top, 0px); }
    body { margin: 0; background: var(--bg); color: var(--fg); font: 14px/1.5 Inter, -apple-system, "Segoe UI", sans-serif; }
    a { color: var(--ac); cursor: pointer; text-decoration: none; } a:hover { text-decoration: underline; }
    .hd { background: color-mix(in srgb, var(--b2) 85%, transparent); backdrop-filter: blur(8px); border-bottom: 1px solid var(--bd); padding: 10px 14px; display: flex; gap: 10px; align-items: center; position: sticky; top: env(safe-area-inset-top, 0px); z-index: 9; }
    input, textarea, select { background: var(--bg); color: var(--fg); border: 1px solid var(--bd); border-radius: 6px; padding: 6px 10px; font: inherit; max-width: 100%; box-sizing: border-box; }
    textarea { width: 100%; min-height: 280px; font: 12px 'JetBrains Mono', ui-monospace, Menlo, Consolas, monospace; }
    .btn { background: var(--b2); color: var(--fg); border: 1px solid var(--bd); border-radius: 6px; padding: 4px 12px; cursor: pointer; font: inherit; font-size: 13px; }
    .btn.g { background: linear-gradient(90deg, #6366f1, #a855f7); color: #fff; border-color: transparent; } .btn.on { color: var(--pu); }
    .btn.danger { background: var(--dd); color: var(--rd); border-color: var(--rd); }
    #sw { position: relative; flex: 1; }
    #sr { position: absolute; top: 36px; left: 0; right: 0; background: var(--bg); border: 1px solid var(--bd); border-radius: 6px; display: none; max-height: 300px; overflow: auto; z-index: 10; }
    #sr div { padding: 6px 10px; cursor: pointer; } #sr div:hover { background: var(--b2); }
    .w { max-width: 1000px; margin: 0 auto; padding: 14px; }
    .rt { font-size: 20px; margin: 6px 0; } .mu { color: var(--mu); } .pill { border: 1px solid var(--bd); border-radius: 20px; font-size: 12px; padding: 0 8px; color: var(--mu); }
    .tabs { display: flex; gap: 4px; border-bottom: 1px solid var(--bd); overflow-x: auto; margin: 10px 0 14px; }
    .tabs a { color: var(--fg); padding: 8px 12px; white-space: nowrap; border-bottom: 2px solid transparent; } .tabs a.on { border-color: #a855f7; font-weight: 600; }
    .ct { background: var(--bd); border-radius: 20px; padding: 0 6px; font-size: 12px; margin-left: 4px; }
    .box { border: 1px solid var(--bd); border-radius: 6px; margin: 10px 0; overflow: hidden; }
    .bh { background: var(--b2); padding: 8px 12px; border-bottom: 1px solid var(--bd); display: flex; gap: 8px; align-items: center; flex-wrap: wrap; } .r { margin-left: auto; }
    .row { display: flex; gap: 10px; padding: 8px 12px; border-top: 1px solid var(--bd); align-items: center; } .row:first-child { border: 0; } .row .t { flex: 1; min-width: 0; }
    .sc { overflow-x: auto; } table { border-collapse: collapse; font: 12px/20px 'JetBrains Mono', ui-monospace, Menlo, Consolas, monospace; width: 100%; }
    td.ln { color: var(--mu); text-align: right; padding: 0 10px; user-select: none; width: 1%; white-space: nowrap; } td { white-space: pre; padding: 0 8px; }
    .pr { padding: 12px; white-space: pre-wrap; font: 12px 'JetBrains Mono', ui-monospace, Menlo, Consolas, monospace; margin: 0; overflow-x: auto; }
    .md { padding: 4px 16px 12px; } .md code { background: var(--b2); padding: 1px 5px; border-radius: 5px; } .md pre { background: var(--b2); padding: 10px; border-radius: 6px; overflow-x: auto; }
    .md h1, .md h2 { border-bottom: 1px solid var(--bd); padding-bottom: 4px; }
    i { font-style: normal; } i.c { color: var(--mu); } i.s { color: var(--ac); } i.k { color: var(--rd); } i.n { color: var(--pu); }
    tr.a { background: var(--ad); } tr.d { background: var(--dd); }
    .lb { border-radius: 20px; padding: 0 8px; font-size: 12px; color: #fff; }
    .log { background: #05070d; color: #e6edf3; padding: 10px; font: 12px/1.5 'JetBrains Mono', ui-monospace, Menlo, Consolas, monospace; white-space: pre-wrap; max-height: 300px; overflow: auto; margin: 0; }
    .hm { display: grid; grid-template-rows: repeat(7, 11px); grid-auto-flow: column; gap: 3px; } .hm b { width: 11px; height: 11px; border-radius: 2px; background: var(--b2); border: 1px solid var(--bd); }
    .bar { display: flex; height: 8px; border-radius: 4px; overflow: hidden; margin: 8px 0; }
    .st { font-size: 12px; border-radius: 20px; padding: 0 8px; } .ok { color: var(--gr); } .er { color: var(--rd); }
    .lg { width: 32px; height: 32px; border-radius: 10px; background: linear-gradient(135deg, #4f46e5, #9333ea, #ec4899); display: flex; align-items: center; justify-content: center; }
    .gt { background: var(--gd); -webkit-background-clip: text; background-clip: text; color: transparent; }
    .box, .btn { transition: .2s; } .box:hover { box-shadow: 0 0 18px -4px rgba(168, 85, 247, .35); } .card { padding: 14px; cursor: pointer; }
    .fr-bar { background: var(--b2); padding: 6px 10px; border-bottom: 1px solid var(--bd); display: flex; gap: 6px; align-items: center; flex-wrap: wrap; }
  </style>
</head>
<body>
<div class="hd">
  <a onclick="go({home:1})" style="display:flex;gap:8px;align-items:center;color:inherit"><span class="lg">🧠</span><b class="gt">Neural Raphael Hub</b></a>
  <div id="sw"><input id="sq" style="width:100%" placeholder="Buscar arquivos, issues e releases ( / )" oninput="search(this.value)"><div id="sr"></div></div>
  <span id="me" class="pill"></span><button class="btn" onclick="theme()">◐</button>
</div>
<div class="w" id="app"></div>

<script>
const $ = s => document.querySelector(s), K = 'nrh-gh-unified-v3', D = 864e5;
const esc = s => String(s).replace(/[&<>]/g, c => ({'&':'&amp;','<':'&lt;','>':'&gt;'}[c]));

function h53(s) {
  let a = 0xdeadbeef, b = 0x41c6ce57;
  for (let i = 0; i < s.length; i++) {
    const c = s.charCodeAt(i);
    a = Math.imul(a ^ c, 2654435761);
    b = Math.imul(b ^ c, 1597334677);
  }
  a = Math.imul(a ^ a >>> 16, 2246822507) ^ Math.imul(b ^ b >>> 13, 3266489909);
  b = Math.imul(b ^ b >>> 16, 2246822507) ^ Math.imul(a ^ a >>> 13, 3266489909);
  return (b >>> 0).toString(16).padStart(8, '0') + (a >>> 0).toString(16).padStart(8, '0');
}

function ago(t) {
  const s = (Date.now() - t) / 1e3;
  return s < 60 ? 'agora' : s < 3600 ? Math.floor(s / 60) + ' min atrás' : s < 864e2 ? Math.floor(s / 3600) + ' h atrás' : Math.floor(s / 864e2) + ' dias atrás';
}

function fz(q, s) {
  q = q.toLowerCase(); s = s.toLowerCase();
  let i = 0, sc = 0, l = -2;
  for (let j = 0; j < s.length && i < q.length; j++) {
    if (s[j] == q[i]) { sc += j == l + 1 ? 3 : 1; l = j; i++; }
  }
  return i == q.length ? sc - s.length / 50 : -1;
}

function diff(a, b) {
  const A = a ? a.split('\n') : [], B = b ? b.split('\n') : [], n = A.length, m = B.length;
  const T = Array.from({length: n + 1}, () => new Uint16Array(m + 1));
  for (let i = n - 1; i >= 0; i--) for (let j = m - 1; j >= 0; j--) T[i][j] = A[i] === B[j] ? T[i+1][j+1] + 1 : Math.max(T[i+1][j], T[i][j+1]);
  let i = 0, j = 0, r = [];
  while (i < n && j < m) {
    if (A[i] === B[j]) { r.push([' ', A[i]]); i++; j++; }
    else if (T[i+1][j] >= T[i][j+1]) r.push(['-', A[i++]]);
    else r.push(['+', B[j++]]);
  }
  while (i < n) r.push(['-', A[i++]]);
  while (j < m) r.push(['+', B[j++]]);
  return r;
}

function diffH(ch) {
  return ch.map(c => {
    const d = diff(c.a, c.b), ad = d.filter(x => x[0] == '+').length, rm = d.filter(x => x[0] == '-').length;
    return `<div class=box><div class=bh><b>${esc(c.p)}</b><span class=r><span class=ok>+${ad}</span> <span class=er>−${rm}</span></span></div><div class=sc><table>${d.map(x => `<tr class="${x[0] == '+' ? 'a' : x[0] == '-' ? 'd' : ''}"><td class=ln>${x[0]}</td><td>${esc(x[1])}</td></tr>`).join('')}</table></div></div>`;
  }).join('');
}

function hl(src, p) {
  if (/\.md$/.test(p)) return esc(src);
  const re = /(#.*|\/\/.*)|("(?:\\.|[^"\\\n])*"|'(?:\\.|[^'\\\n])*')|\b(class|def|return|import|from|self|if|else|elif|for|in|not|None|True|False|const|let|function|with|as|while|lambda|raise|try|except|super|run|name|on|steps|uses)\b|\b(\d+\.?\d*)\b/g;
  let o = '', l = 0, m;
  while (m = re.exec(src)) {
    o += esc(src.slice(l, m.index));
    o += `<i class=${m[1] ? 'c' : m[2] ? 's' : m[3] ? 'k' : 'n'}>${esc(m[0])}</i>`;
    l = re.lastIndex;
  }
  return o + esc(src.slice(l));
}

function md(t) {
  let c = 0, o = '';
  for (const L of (t || '').split('\n')) {
    if (L.startsWith('```')) { o += c ? '</pre>' : '<pre>'; c = !c; continue; }
    if (c) { o += esc(L) + '\n'; continue; }
    const x = esc(L).replace(/`([^`]+)`/g, '<code>$1</code>').replace(/\*\*([^*]+)\*\*/g, '<b>$1</b>'), n = L.indexOf(' ');
    o += /^#{1,3} /.test(L) ? `<h${n}>${x.slice(n + 1)}</h${n}>` : /^- /.test(L) ? `<li>${x.slice(2)}</li>` : x ? `<p>${x}</p>` : '';
  }
  return o;
}

function lint(s) {
  const st = [], pr = {')': '(', ']': '[', '}': '{'};
  let ln = 1;
  for (const ch of s.replace(/#.*/g, '')) {
    if (ch == '\n') ln++;
    if ('([{'.includes(ch)) st.push(ch);
    else if (pr[ch] && st.pop() !== pr[ch]) return 'linha ' + ln;
  }
  return st.length ? 'delimitador não fechado' : '';
}

function rng(a) {
  return () => {
    a |= 0; a = a + 0x6D2B79F5 | 0;
    let t = Math.imul(a ^ a >>> 15, 1 | a);
    t = t + Math.imul(t ^ t >>> 7, 61 | t) ^ t;
    return ((t ^ t >>> 14) >>> 0) / 4294967296;
  };
}

function seed(name, owner) {
  const n = Date.now(), F = {
    'README.md': '# Neural Raphael Hub\n\nEstúdio de inferência completo: **geração latente** + **refino e upscale**.\n\n- Módulo 1: IP-Adapter desacoplado com FlashAttention-2\n- Módulo 2: High-Res Fix e CodeFormer\n- Samplers: DDIM, DPM-Solver++ e Euler Ancestral\n\nUso: execute o workflow em Actions.',
    'module1_flash_attn.py': 'class OptimizedIPAdapterDecoupledCrossAttention(nn.Module):\n    def __init__(self, query_dim: int = 128, context_dim: int = 768, num_heads: int = 4):\n        super().__init__()\n        self.num_heads = num_heads\n        self.head_dim = query_dim // num_heads\n        self.to_q = nn.Linear(query_dim, query_dim, bias=False)\n        self.to_k_text = nn.Linear(context_dim, query_dim, bias=False)\n        self.to_v_text = nn.Linear(context_dim, query_dim, bias=False)\n\n    def _apply_sdpa(self, q, k, v):\n        out = F.scaled_dot_product_attention(q, k, v, is_causal=False)\n        return out.transpose(1, 2)',
    'module2_refiner.py': 'class UnifiedModule2Pipeline(nn.Module):\n    def process(self, latents_m1, highres_scale: float = 2.0, denoising_strength: float = 0.45, restore_faces: bool = True):\n        up = F.interpolate(latents_m1, scale_factor=highres_scale, mode="bicubic")\n        refined = self.upscale_unet(z_t=up, z_lr=up)\n        img = self.vae_decoder(refined)\n        if restore_faces:\n            img = self.face_restorer(img)\n        return img',
    'orchestrator.py': 'import torch\n\ndef run(prompt, steps=20, cfg=7.5, hr_scale=2.0):\n    latents = module1(prompt, steps=steps, cfg=cfg)\n    return module2(latents, highres_scale=hr_scale)',
    'samplers/ddim.py': 'def ddim_step(x, eps, a_t, a_prev):\n    x0 = (x - (1 - a_t) ** 0.5 * eps) / a_t ** 0.5\n    return a_prev ** 0.5 * x0 + (1 - a_prev) ** 0.5 * eps',
    'samplers/dpm_solver.py': 'def dpm_solver_2m(x, eps, eps_prev, h, h_prev):\n    r = h_prev / h\n    d = (1 + 1 / (2 * r)) * eps - (1 / (2 * r)) * eps_prev\n    return x - h * d',
    '.github/workflows/pipeline.yml': 'name: pipeline\non: push\nsteps:\n  - uses: checkout\n  - run: lint\n  - run: pipeline'
  };
  const r1 = '# Neural Raphael Hub\n\nEstúdio de inferência.', ch = (p, a, b) => ({p, a, b});
  const C = [
    {m: 'docs: expand README', t: n - D, ch: [ch('README.md', r1, F['README.md'])]},
    {m: 'feat: add DDIM and DPM-Solver++ samplers', t: n - 5 * D, ch: ['orchestrator.py', 'samplers/ddim.py', 'samplers/dpm_solver.py', '.github/workflows/pipeline.yml'].map(p => ch(p, '', F[p]))},
    {m: 'Initial commit', t: n - 9 * D, ch: [ch('README.md', '', r1), ch('module1_flash_attn.py', '', F['module1_flash_attn.py']), ch('module2_refiner.py', '', F['module2_refiner.py'])]}
  ].map(c => ({...c, a: 'raphael', sha: h53(c.m + c.t)}));

  return {
    id: slug(name) + '-' + Math.random().toString(36).slice(2, 6),
    name, owner, desc: 'Repositório de algoritmos de aprendizado profundo e processamento gráfico.', files: F, commits: C, star: [], watch: [], fork: 0, defaultBranch: 'main',
    issues: [
      {t: 'Suporte a ControlNet no Módulo 1', b: 'Adicionar ZeroConv para condições estruturais.', l: 'enhancement', o: 1, d: n - 2 * D, cm: []},
      {t: 'VRAM estoura com batch 8', b: 'Reproduz em GPU de 16 GB.', l: 'bug', o: 1, d: n - 3 * D, cm: []}
    ],
    prs: [
      {t: 'feat: add Euler ancestral sampler', br: 'feat/euler', s: 'open', d: n - D / 2, ch: [ch('samplers/euler.py', '', 'def euler_a_step(x, eps, sigma, sigma_next):\n    return x + (sigma_next - sigma) * eps')]}
    ],
    releases: [
      {tag: 'v1.0.0', title: 'First Stable Release', body: 'Lançamento inicial com IP-Adapter e CodeFormer.', d: n - 4 * D, assets: ['neural-raphael-v1.tar.gz']}
    ],
    runs: []
  };
}

let S = null, R = {}, UID = 'local', V = {home: 1, tab: 'code', p: '', f: 1, raw: 0, sh: 0};
const UN = {}, W = () => !S || S.owner == UID || UID == 'local';
const slug = s => s.toLowerCase().replace(/[^\w-]+/g, '-').replace(/^-+|-+$/g, '');

try { R = JSON.parse(localStorage.getItem(K)) || {}; } catch(e) {}

function save() {
  if (S) R[S.id] = S;
  try { localStorage.setItem(K, JSON.stringify(R)); } catch(e) {}
}

if (Object.keys(R).length === 0) {
  const seedRepo = seed('neural-raphael-hub', 'local');
  R[seedRepo.id] = seedRepo;
  save();
}

function newRepo(name, tpl) {
  name = slug(name || 'novo-repositorio');
  const r = seed(name, UID), n = Date.now();
  if (!tpl) {
    r.files = {'README.md': '# ' + name + '\n\nNovo repositório.'};
    r.commits = [{m: 'Initial commit', t: n, a: UN[UID] || 'você', sha: h53(name + n), ch: [{p: 'README.md', a: '', b: r.files['README.md']}]}];
    r.issues = []; r.prs = []; r.releases = [];
  }
  S = r; save();
  V = {home: 0, tab: 'code', p: '', f: 1, raw: 0, sh: 0};
  render();
}

function openRepo(id) {
  S = R[id];
  V = {home: 0, tab: 'code', p: '', f: 1, raw: 0, sh: 0};
  render();
}

function tg(k) {
  const a = S[k], i = a.indexOf(UID);
  i < 0 ? a.push(UID) : a.splice(i, 1);
  save(); render();
}

function forkRepo() {
  const c = JSON.parse(JSON.stringify(S));
  S.fork++; save();
  c.id = slug(S.name) + '-' + Math.random().toString(36).slice(2, 6);
  Object.assign(c, {owner: UID, forkOf: S.id, star: [], watch: [], fork: 0});
  S = c; save();
  V = {home: 0, tab: 'code', p: '', f: 1, raw: 0, sh: 0};
  render();
}

function openPR() {
  const o = R[S.forkOf]; if (!o) return;
  const ch = [...new Set([...Object.keys(S.files), ...Object.keys(o.files)])]
    .filter(p => S.files[p] !== o.files[p])
    .map(p => ({p, a: o.files[p] || '', b: S.files[p] || ''}));
  if (!ch.length) { alert('Nenhuma modificação detectada para abrir Pull Request.'); return; }
  o.prs.unshift({t: 'Mudanças de ' + (UN[UID] || 'fork'), br: (UN[UID] || 'fork') + ':main', s: 'open', d: Date.now(), ch});
  save(); render();
  alert('Pull Request criado no repositório de origem!');
}

function delRepo() {
  delete R[S.id];
  try { localStorage.setItem(K, JSON.stringify(R)); } catch(e) {}
  S = null; V.home = 1; render();
}

function blame(p) {
  let L = [];
  for (const c of [...S.commits].reverse()) {
    const x = c.ch.find(k => k.p == p);
    if (!x) continue;
    const n = []; let i = 0;
    for (const [t] of diff(x.a, x.b)) {
      if (t == ' ') n.push(L[i++]);
      else if (t == '-') i++;
      else n.push(c.sha.slice(0, 7) + ' ' + c.a);
    }
    L = n;
  }
  return L;
}

function homeView() {
  const L = Object.values(R).sort((a, b) => b.commits[0].t - a.commits[0].t), q = V.hq || '';
  $('#app').innerHTML = `
    <div class="box" style="padding:16px;background:linear-gradient(135deg,rgba(99,102,241,.18),rgba(236,72,153,.12))">
      <h2 style="margin:0" class="gt">Seus algoritmos e softwares, arquivados.</h2>
      <p class="mu">Crie repositórios, versione código, abra issues e pull requests, faça forks.</p>
      <input id="rn" placeholder="nome-do-repositorio">
      <button class="btn g" onclick="newRepo($('#rn').value, 0)">+ Novo repositório</button>
      <button class="btn" onclick="newRepo($('#rn').value || 'neural-raphael-hub', 1)">Modelo Neural Raphael</button>
    </div>
    <input style="width:100%" placeholder="Buscar repositórios e código…" value="${esc(q)}" oninput="V.hq=this.value;render()">
    ${L.filter(r => !q || fz(q, r.name) >= 0 || Object.values(r.files).some(c => c.includes(q))).map(r => `
      <div class="box card" onclick="openRepo('${r.id}')">
        <b class="gt">${esc(UN[r.owner] \vert{}\vert{} 'usuário')} / ${esc(r.name)}</b> <span class="pill">Public</span>${r.forkOf ? ' <span class="mu">fork</span>' : ''}<br>
        <span class="mu">${esc(r.desc || '')} ★ ${r.star.length} · ⑂ ${r.fork} · ${r.commits.length} commits · ${ago(r.commits[0].t)}</span>
      </div>
    `).join('') || '<p class="mu">Nenum repositório ainda. Crie o primeiro acima.</p>'}
  `;
}

function go(o) { Object.assign(V, o); render(); scrollTo(0, 0); }
function theme() {
  const r = document.documentElement;
  r.dataset.theme = (r.dataset.theme || (matchMedia('(prefers-color-scheme:light)').matches ? 'light' : 'dark')) == 'dark' ? 'light' : 'dark';
}

function search(q) {
  const r = $('#sr'); if (!q || !S) { r.style.display = 'none'; return; }
  const f = Object.keys(S.files).map(p => [fz(q, p), '📄 ' + p, `go({home:0,tab:'code',p:'${p}',edit:0,cm:0});$('#sr').style.display='none'`]);
  const i = S.issues.map((x, k) => [fz(q, x.t), '⊙ ' + x.t, `go({home:0,tab:'issues',f:${x.o ? 1 : 0}});$('#sr').style.display='none'`]);
  const rel = (S.releases || []).map(x => [fz(q, x.tag), '🏷 ' + x.tag + ' - ' + x.title, `go({home:0,tab:'releases'});$('#sr').style.display='none'`]);
  const g = Object.entries(S.files).flatMap(([p, c]) => c.split('\n').map((l, n) => l.toLowerCase().includes(q.toLowerCase()) ? [.5, '🔎 ' + p + ':' + (n + 1) + ' ' + l.trim().slice(0, 40), `go({home:0,tab:'code',p:'${p}',edit:0,cm:0});$('#sr').style.display='none'`] : null).filter(Boolean)).slice(0, 4);
  const L = [...f, ...i, ...rel, ...g].filter(x => x[0] >= 0).sort((a, b) => b[0] - a[0]).slice(0, 8);
  r.style.display = 'block';
  r.innerHTML = L.length ? L.map(x => `<div onclick="${x[2]}">${esc(x[1])}</div>`).join('') : '<div class="mu">Nada encontrado</div>';
}

addEventListener('keydown', e => {
  if (e.key == '/' && !/INPUT|TEXTAREA/.test(document.activeElement.tagName)) {
    e.preventDefault(); $('#sq').focus();
  }
});

const touch = p => S.commits.find(c => c.ch.some(x => x.p == p || x.p.startsWith(p + '/')));
function mkCommit(m, ch) {
  S.commits.unshift({m, t: Date.now(), a: UN[UID] || 'você', sha: h53(m + Date.now() + Math.random()), ch});
  save();
}

// ==========================================
// MÓDULO: EDITOR DE CÓDIGO (FIND & REPLACE)
// ==========================================
function executeSearchNext() {
  const query = $('#ff').value, area = $('#ev'), status = $('#fr-status');
  if (!query) return;
  const text = area.value, startPos = area.selectionEnd || 0, index = text.toLowerCase().indexOf(query.toLowerCase(), startPos);
  if (index !== -1) {
    area.focus(); area.setSelectionRange(index, index + query.length);
    status.textContent = `Posição: ${index}`;
  } else {
    const retryIndex = text.toLowerCase().indexOf(query.toLowerCase(), 0);
    if (retryIndex !== -1) {
      area.focus(); area.setSelectionRange(retryIndex, retryIndex + query.length);
      status.textContent = `Loop do início (posição ${retryIndex})`;
    } else {
      status.textContent = 'Não encontrado';
    }
  }
}

function executeReplaceAll() {
  const findVal = $('#ff').value, replaceVal = $('#fr').value, area = $('#ev'), status = $('#fr-status');
  if (!findVal) return;
  const parts = area.value.split(findVal), count = parts.length - 1;
  if (count > 0) {
    area.value = parts.join(replaceVal);
    status.textContent = `${count} substituição(ões)!`;
  } else {
    status.textContent = 'Nada alterado';
  }
}

function codeView() {
  if (V.edit) return editor();
  if (V.cm) return commitsView();
  const p = V.p, f = S.files[p], lc = S.commits[0];
  const cr = `<a onclick="go({p:''})">${S.name}</a>` + p.split('/').filter(Boolean).map((s, i, a) => ` / <a onclick="go({p:'${a.slice(0, i + 1).join('/')}'})">${esc(s)}</a>`).join('');
  const bar = `<div class=bh><b>${lc.a}</b> <span>${esc(lc.m)}</span><span class=mu>${lc.sha.slice(0, 7)} · ${ago(lc.t)}</span><a class=r onclick="go({cm:1})">⏱ ${S.commits.length} commits</a></div>`;
  
  if (f !== undefined) {
    const L = hl(f, p).split('\n'), BL = V.bl ? blame(p) : [], isMd = /\.md$/.test(p) && !V.raw;
    return `
      <p>${cr}</p>
      <div class=box>${bar}
        <div class=bh>
          <span class=mu>${f.split('\n').length} linhas · ${f.length} bytes</span>
          <span class=r>
            <button class=btn onclick="go({bl:${V.bl ? 0 : 1}})">Blame</button>
            <button class=btn onclick="go({raw:${V.raw ? 0 : 1}})">${V.raw ? 'Preview' : 'Raw'}</button>
            <button class=btn onclick="try{navigator.clipboard.writeText(S.files['${p}'])}catch(e){}">Copiar</button>
            <button class=btn onclick="go({edit:1,np:0})">Editar</button>
            <button class=btn onclick="delF('${p}')">Excluir</button>
          </span>
        </div>
        ${isMd ? `<div class=md>${md(f)}</div>` : V.raw ? `<pre class=pr>${esc(f)}</pre>` : `<div class=sc><table>${L.map((x, i) => `<tr><td class=ln>${i + 1}</td>${V.bl ? `<td class=mu>${BL[i] || ''}</td>` : ''}<td>${x}</td></tr>`).join('')}</table></div>`}
      </div>
    `;
  }
  
  const pre = p ? p + '/' : '', E = new Map();
  for (const k in S.files) if (k.startsWith(pre)) {
    const r = k.slice(pre.length);
    E.set(r.split('/')[0], r.includes('/'));
  }
  const rows = [...E].sort((a, b) => (b[1] - a[1]) || (a[0] < b[0] ? -1 : 1)).map(([n, d]) => {
    const q = pre + n, c = touch(q);
    return `<div class=row><span>${d ? '📁' : '📄'}</span><a class=t onclick="go({p:'${q}'})">${esc(n)}</a><span class="mu t" style="flex:2;overflow:hidden;white-space:nowrap;text-overflow:ellipsis">${esc(c.m)}</span><span class=mu>${ago(c.t)}</span></div>`;
  }).join('');
  const rd = S.files[pre + 'README.md'];
  return `<p>${cr}</p><div class=box>${bar}${rows}</div><button class="btn g" onclick="go({edit:1,np:1})">+ Novo arquivo</button>${rd ? `<div class=box><div class=bh>📖 README.md</div><div class=md>${md(rd)}</div></div>` : ''}`;
}

function editor() {
  const p = V.np ? '' : V.p, v = S.files[p] || '';
  return `
    <div class=box>
      <div class=bh>${V.np ? 'Novo arquivo: <input id=ep placeholder="pasta/arquivo.py">' : 'Editando ' + esc(p)}</div>
      <div class=fr-bar>
        <input id=ff placeholder="Localizar…">
        <input id=fr placeholder="Substituir…">
        <button class=btn onclick="executeSearchNext()">Próximo</button>
        <button class=btn onclick="executeReplaceAll()">Substituir Tudo</button>
        <span id="fr-status" class="mu" style="font-size:12px"></span>
      </div>
      <div style="padding:10px">
        <textarea id=ev>${esc(v)}</textarea>
        <p><input id=em style="width:100%" placeholder="Mensagem do commit"></p>
        <span id=ee class=er></span>
        <p>
          <button class="btn g" onclick="commit()">Commit changes</button>
          <button class=btn onclick="go({edit:0})">Cancelar</button>
        </p>
      </div>
    </div>
  `;
}

function commit() {
  if (!W()) return;
  const p = V.np ? $('#ep').value.trim() : V.p;
  if (!/^[\w.\/-]+$/.test(p)) {$('#ee').textContent = 'Caminho inválido'; return; }
  const a = S.files[p] || '', b = $('#ev').value;
  if (a === b) { $('#ee').textContent = 'Sem alterações'; return; }
  S.files[p] = b;
  mkCommit($('#em').value || (a ? 'Update ' : 'Create ') + p, [{p, a, b}]);
  V.edit = 0; V.p = p; render();
}

function delF(p) {
  if (!W() || !(p in S.files)) return;
  const a = S.files[p];
  delete S.files[p];
  mkCommit('Delete ' + p, [{p, a, b: ''}]);
  V.p = p.split('/').slice(0, -1).join('/');
  render();
}

function commitsView() {
  return `<p><a onclick="go({cm:0})">← Voltar ao Código</a></p>` + S.commits.map((c) => `
    <div class=box>
      <div class=row>
        <div class=t><b>${esc(c.m)}</b><br><span class=mu>${c.a} · ${ago(c.t)}</span></div>
        <code>${c.sha.slice(0, 7)}</code>
        <button class=btn onclick="go({sh:V.sh === '${c.sha}' ? 0 : '${c.sha}'})">diff</button>
      </div>
      ${V.sh == c.sha ? diffH(c.ch) : ''}
    </div>
  `).join('');
}

// ==========================================
// MÓDULO: ISSUES & COMENTÁRIOS
// ==========================================
function issuesView() {
  const q = V.iq || '', o = S.issues.filter(i => i.o).length, cl = S.issues.length - o;
  const col = {bug: '#d1242f', enhancement: '#1f883d', docs: '#0969da'};
  const L = S.issues.map((x, i) => [x, i]).filter(([x]) => !!x.o == !!V.f && (!q || fz(q, x.t) >= 0));

  return `
    <div style="display:flex;gap:8px;flex-wrap:wrap;margin-bottom:12px">
      <input style="flex:1" placeholder="Filtrar por título..." value="${esc(q)}" oninput="V.iq=this.value;render()">
      <button class="btn g" onclick="go({ni:!V.ni})">+ Nova Issue</button>
    </div>

    ${V.ni ? `
      <div class="box" style="padding:14px;margin-bottom:12px">
        <h4 style="margin:0 0 8px">Criar Nova Issue</h4>
        <input id="nt" style="width:100%;margin-bottom:8px" placeholder="Título resumido">
        <textarea id="nb" style="min-height:80px;margin-bottom:8px" placeholder="Descrição detalhada..."></textarea>
        <div style="display:flex;gap:8px;align-items:center">
          <label class="mu">Tag:</label>
          <select id="nl"><option value="bug">bug</option><option value="enhancement">enhancement</option><option value="docs">docs</option></select>
          <button class="btn g" onclick="addIssue()">Criar Issue</button>
          <button class="btn" onclick="go({ni:0})">Cancelar</button>
        </div>
      </div>
    ` : ''}

    <div class="box">
      <div class="bh">
        <a onclick="go({f:1})" style="${V.f ? 'font-weight:700' : ''}">⊙ ${o} Abertas</a>
        <a onclick="go({f:0})" style="${V.f ? '' : 'font-weight:700'}">✔ ${cl} Fechadas</a>
      </div>

      ${L.map(([x, i]) => `
        <div class="row" style="align-items:flex-start">
          <span class="${x.o ? 'ok' : 'mu'}" style="margin-top:2px">${x.o ? '⊙' : '✔'}</span>
          <div class="t">
            ${V.editIssue === i ? `
              <input id="ei_t_${i}" value="${esc(x.t)}" style="width:100%;margin-bottom:4px">
              <textarea id="ei_b_${i}" style="min-height:60px;width:100%;margin-bottom:6px">${esc(x.b)}</textarea>
              <button class="btn g" onclick="saveIssueEdit(${i})">Salvar Alterações</button>
              <button class="btn" onclick="go({editIssue:-1})">Cancelar</button>
            ` : `
              <b>${esc(x.t)}</b> <span class="lb" style="background:${col[x.l]}">${x.l}</span><br>
              <span class="mu">#${i + 1} aberta ${ago(x.d)}</span>
              ${x.b ? `<div class="md" style="padding:6px 0">${md(x.b)}</div>` : ''}
            `}

            <div style="margin-top:8px;border-top:1px dashed var(--bd);padding-top:6px">
              ${(x.cm || []).map((c, ci) => `
                <div style="background:var(--b2);padding:6px 10px;border-radius:6px;margin-top:4px;display:flex;justify-content:space-between;align-items:center">
                  <span>💬 ${esc(c)}</span>
                  <a class="er" style="font-size:11px" onclick="delComment(${i}, ${ci})">[excluir]</a>
                </div>
              `).join('')}
              <input placeholder="Adicionar comentário..." style="width:100%;margin-top:6px" onchange="addComment(${i}, this.value);this.value=''">
            </div>
          </div>

          <div style="display:flex;gap:4px;flex-direction:column;align-items:flex-end">
            <button class="btn" onclick="S.issues[${i}].o=${x.o ? 0 : 1};save();render()">${x.o ? 'Fechar' : 'Reabrir'}</button>
            <button class="btn" onclick="go({editIssue:${i}})">Editar</button>
            <button class="btn danger" onclick="delIssue(${i})">Excluir</button>
          </div>
        </div>
      `).join('') || '<div class="row mu">Nenhuma issue encontrada neste estado.</div>'}
    </div>
  `;
}

function addIssue() {
  const t = $('#nt').value.trim(); if (!t) return;
  S.issues.unshift({t, b: $('#nb').value, l: $('#nl').value, o: 1, d: Date.now(), cm: []});
  V.ni = 0; V.f = 1; save(); render();
}

function saveIssueEdit(i) {
  S.issues[i].t = $('#ei_t_' + i).value.trim();
  S.issues[i].b = $('#ei_b_' + i).value;
  V.editIssue = -1;
  save(); render();
}

function delIssue(i) {
  if (confirm('Deseja realmente excluir esta issue?')) {
    S.issues.splice(i, 1);
    save(); render();
  }
}

function addComment(i, txt) {
  if (!txt.trim()) return;
  S.issues[i].cm = S.issues[i].cm || [];
  S.issues[i].cm.push((UN[UID] || 'você') + ': ' + txt.trim());
  save(); render();
}

function delComment(i, ci) {
  S.issues[i].cm.splice(ci, 1);
  save(); render();
}

// ==========================================
// MÓDULO: PULL REQUESTS & MERGE
// ==========================================
function prsView() {
  return (S.prs || []).map((p, i) => `
    <div class=box>
      <div class=row>
        <span class="${p.s == 'open' ? 'ok' : 'mu'}">⑂</span>
        <div class=t><b>${esc(p.t)}</b><br><span class=mu>${p.br} → main · ${ago(p.d)}</span></div>
        <span class="st ${p.s == 'open' ? 'ok' : 'mu'}">${p.s}</span>
        ${p.s == 'open' ? `<button class="btn g" onclick="merge(${i})">Mesclar (Merge)</button>` : ''}
        <button class=btn onclick="go({pr:V.pr === ${i} ? -1 : ${i}})">Ver Alterações</button>
      </div>
      ${V.pr === i ? diffH(p.ch) : ''}
    </div>
  `).join('') || '<p class="mu">Nenhum Pull Request aberto.</p>';
}

function merge(i) {
  if (!W()) return;
  const p = S.prs[i];
  p.ch.forEach(c => { c.b ? S.files[c.p] = c.b : delete S.files[c.p]; });
  mkCommit('Merge pull request: ' + p.t, p.ch);
  p.s = 'merged'; save(); render();
}

// ==========================================
// MÓDULO: RELEASES & TAGS
// ==========================================
function releasesView() {
  S.releases = S.releases || [];
  return `
    <div style="display:flex; justify-content:space-between; align-items:center; margin-bottom: 12px;">
      <h3>Releases & Tags Git</h3>
      <button class="btn g" onclick="go({nr:!V.nr})">+ Criar Nova Release</button>
    </div>
    
    ${V.nr ? `
      <div class="box" style="padding: 14px; margin-bottom: 16px;">
        <h4 style="margin-top:0">Nova Publicação de Release</h4>
        <div style="display:grid; grid-template-columns: 1fr 1fr; gap: 10px; margin-bottom: 10px;">
          <div>
            <label class="mu">Tag da Release:</label>
            <input id="rtg" placeholder="ex: v1.2.0" style="width:100%">
          </div>
          <div>
            <label class="mu">Título da Release:</label>
            <input id="rti" placeholder="ex: Major Refactor" style="width:100%">
          </div>
        </div>
        
        <label class="mu">Notas de Lançamento:</label>
        <textarea id="rbo" style="min-height: 100px; margin: 6px 0;" placeholder="Descreva as melhorias..."></textarea>
        
        <label class="mu">Assets Binários Compilados (separados por vírgula):</label>
        <input id="ras" placeholder="ex: build.tar.gz, binary-win64.exe" style="width:100%; margin-bottom: 12px;">
        
        <button class="btn g" onclick="addRelease()">Publicar Release</button>
        <button class="btn" onclick="go({nr:0})">Cancelar</button>
      </div>
    ` : ''}

    ${S.releases.length ? S.releases.map((r) => `
      <div class="box" style="padding: 16px; margin-bottom: 12px;">
        <div style="display:flex; align-items:center; gap: 10px; border-bottom: 1px solid var(--bd); padding-bottom: 8px;">
          <b class="gt" style="font-size: 16px;">${esc(r.title)}</b>
          <span class="pill" style="background: var(--b2); border-color: var(--pu); color: var(--pu);">${esc(r.tag)}</span>
          <span class="mu r">${ago(r.d)}</span>
        </div>
        <div class="md" style="padding: 10px 0;">${md(r.body)}</div>
        
        <div style="background: var(--b2); padding: 8px 12px; border-radius: 6px; border: 1px solid var(--bd);">
          <b style="font-size: 12px;" class="mu">Assets Anexados:</b>
          <ul style="margin: 6px 0 0 0; padding-left: 20px; font-family: 'JetBrains Mono', monospace; font-size: 12px;">
            ${(r.assets || [S.name + '-' + r.tag + '.zip']).map(a => `
              <li><a onclick="alert('Download simulado do arquivo: ${esc(a)}')">📦 ${esc(a)}</a></li>
            `).join('')}
          </ul>
        </div>
      </div>
    `).join('') : '<p class="mu">Nenhuma release publicada até o momento.</p>'}
  `;
}

function addRelease() {
  const tag = $('#rtg').value.trim(), title = $('#rti').value.trim(), body = $('#rbo').value, rawAssets = $('#ras').value;
  if (!tag || !title) { alert('A tag e o título são obrigatórios!'); return; }
  const assets = rawAssets ? rawAssets.split(',').map(x => x.trim()).filter(Boolean) : [`${S.name}-${tag}.zip`];
  S.releases.unshift({ tag, title, body, d: Date.now(), assets });
  V.nr = 0; save(); render();
}

// ==========================================
// MÓDULO: ACTIONS / CI PIPELINES
// ==========================================
function actionsView() {
  S.runs = S.runs || [];
  return `
    <div style="display:flex;justify-content:space-between;align-items:center;margin-bottom:12px">
      <h3>Workflows de Integração Contínua (CI/CD)</h3>
      <button class="btn g" onclick="runWf()">▶ Executar Pipeline Manual</button>
    </div>
    ${S.runs.map(r => `
      <div class="box" style="margin-bottom:10px">
        <div class="bh">
          <span class="${r.st == 'success' ? 'ok' : r.st == 'failure' ? 'er' : 'mu'}">${r.st == 'success' ? '✔' : r.st == 'failure' ? '✖' : '●'}</span>
          <b>Pipeline #${r.id}</b>
          <span class="mu">${ago(r.t)} · Status: <b>${r.st}</b></span>
        </div>
        <pre class="log">${esc(r.log.join('\n'))}</pre>
      </div>
    `).join('') || '<p class="mu">Nenhuma execução registrada. Clique no botão acima para rodar a checagem sintática e inferência.</p>'}
  `;
}

const sleep = ms => new Promise(r => setTimeout(r, ms));
async function runWf() {
  const r = {id: S.runs.length + 1, t: Date.now(), st: 'running', log: []};
  S.runs.unshift(r);
  
  const L = msg => { r.log.push(msg); if (V.tab == 'actions') render(); };
  L('▶ Iniciando ambiente de execução virtual...'); await sleep(250);
  L('▶ Baixando código-fonte (git checkout)...'); await sleep(200);

  const bad = [];
  for (const p in S.files) {
    if (p.endsWith('.py')) {
      const e = lint(S.files[p]);
      L((e ? '✖ ' : '✔ ') + 'Linter sintático em ' + p + (e ? ' -> Erro: ' + e : ''));
      if (e) bad.push(p);
      await sleep(150);
    }
  }

  if (bad.length) {
    r.st = 'failure';
    L('\n✖ Pipeline abortada! Falha em ' + bad.length + ' arquivo(s).');
    save(); render(); return;
  }

  L('\n▶ Executando testes unitários do Módulo 1 (FlashAttention-2)...'); await sleep(300);
  L('✔ Tensores alocados em VRAM com sucesso.');
  L('▶ Testando Módulo 2 (High-Res Fix & CodeFormer)...'); await sleep(300);
  L('✔ Invariância latente confirmada.');
  
  r.st = 'success';
  L('\n✔ Pipeline concluída com sucesso sem erros!');
  save(); render();
}

// ==========================================
// MÓDULO: INSIGHTS & GRÁFICOS DE MÉTRIBAS
// ==========================================
function insView() {
  const R_fn = rng(7), cell = [], day = Math.floor(Date.now() / D), cm = {};
  S.commits.forEach(c => { const k = Math.floor(c.t / D); cm[k] = (cm[k] || 0) + 3; });
  for (let i = 370; i >= 0; i--) {
    const v = (R_fn() > .6 ? Math.ceil(R_fn() * 3) : 0) + (cm[day - i] || 0), l = Math.min(4, v);
    cell.push(`<b style="${l ? `background:var(--gr);opacity:${.25 + l * .19}` : ''}"></b>`);
  }
  const ex = {}; let all = 0;
  for (const p in S.files) {
    const e = (p.match(/\.(\w+)$/) || [, 'outros'])[1], n = S.files[p].length;
    ex[e] = (ex[e] || 0) + n; all += n;
  }
  const nm = {py: 'Python', md: 'Markdown', yml: 'YAML'}, cl = {py: '#3572A5', md: '#083fa1', yml: '#cb171e'};
  const lg = Object.entries(ex).sort((a, b) => b[1] - a[1]), lines = Object.values(S.files).reduce((a, s) => a + s.split('\n').length, 0);
  return `
    <div class=box><div class=bh>Mapa de Contribuição do Projeto (Ano Recente)</div><div class=sc style="padding:12px"><div class=hm>${cell.join('')}</div></div></div>
    <div class=box style="padding:12px">
      <b>Linguagens Utilizadas</b>
      <div class=bar>${lg.map(([e, n]) => `<span style="width:${n / all * 100}\%;background:${cl[e] || '#888'}"></span>`).join('')}</div>
      ${lg.map(([e, n]) => `<span style="margin-right:12px">● ${nm[e] \vert{}\vert{} e} <span class=mu>${(n / all * 100).toFixed(1)}%</span></span>`).join('')}
    </div>
    <div class=box style="padding:12px">
      <b>Estatísticas Gerais</b><br>
      ${S.commits.length} commits · ${Object.keys(S.files).length} arquivos · ${lines} linhas de código · ${S.issues.filter(i => i.o).length} issues abertas · ${S.prs.filter(p => p.s == 'merged').length} PRs mescladas
    </div>
  `;
}

// ==========================================
// MÓDULO: SETTINGS DO REPOSITÓRIO
// ==========================================
function settingsView() {
  if (!W()) return '<p class="mu">Você não tem permissão para alterar este repositório.</p>';

  return `
    <div class="box" style="padding:16px;margin-bottom:16px">
      <h3 style="margin-top:0">Configurações Gerais</h3>
      
      <label class="mu">Nome do Repositório:</label><br>
      <input id="st_name" value="${esc(S.name)}" style="width:100%;margin:4px 0 12px"><br>

      <label class="mu">Descrição do Projeto:</label><br>
      <input id="st_desc" value="${esc(S.desc || '')}" style="width:100%;margin:4px 0 12px"><br>

      <label class="mu">Branch Padrão (Default Branch):</label><br>
      <input id="st_branch" value="${esc(S.defaultBranch || 'main')}" style="width:100%;margin:4px 0 16px"><br>

      <button class="btn g" onclick="saveSettings()">Salvar Alterações</button>
    </div>

    <div class="box" style="padding:16px;border:1px solid var(--rd);background:rgba(248,113,113,0.05)">
      <h3 class="er" style="margin-top:0">Zona de Perigo</h3>
      <p class="mu">A exclusão removerá permanentemente o histórico de commits, arquivos, issues e releases deste repositório.</p>
      <button class="btn danger" onclick="confirmDelRepo()">Excluir este repositório permanentemente</button>
    </div>
  `;
}

function saveSettings() {
  const newName = slug($('#st_name').value);
  if (!newName) { alert('O nome do repositório não pode ficar em branco.'); return; }
  S.name = newName; S.desc = $('#st_desc').value; S.defaultBranch = $('#st_branch').value || 'main';
  save(); render(); alert('Configurações salvas!');
}

function confirmDelRepo() {
  const confirmName = prompt(`Digite "${S.name}" para confirmar a exclusão:`);
  if (confirmName === S.name) { delRepo(); } else if (confirmName !== null) { alert('Nome incorreto. Ação cancelada.'); }
}

// ==========================================
// RENDERIZADOR PRINCIPAL UNIFICADO
// ==========================================
function render() {
  if (V.home || !S) return homeView();
  const own = W(), o = S.issues.filter(i => i.o).length, po = S.prs.filter(p => p.s == 'open').length, relc = (S.releases || []).length;
  const T = [['code', 'Code'], ['issues', 'Issues', o], ['prs', 'Pull requests', po], ['actions', 'Actions'], ['releases', 'Releases', relc], ['insights', 'Insights'], ['settings', 'Settings']];
  const b = {code: codeView, issues: issuesView, prs: prsView, actions: actionsView, releases: releasesView, insights: insView, settings: settingsView}[V.tab]();
  
  $('#app').innerHTML = `
    <div class=rt>
      <a onclick="go({home:1})">${esc(UN[S.owner] || 'usuário')}</a> / <b class=gt>${esc(S.name)}</b>
      <span class=pill>Public</span>${S.forkOf ? ' <span class=mu>fork</span>' : ''}
    </div>
    <input style="width:100%" placeholder="Descrição" value="${esc(S.desc || '')}" ${own ? '' : 'disabled'} onchange="S.desc=this.value;save()">
    <div style="display:flex;gap:6px;flex-wrap:wrap;margin:6px 0">
      <button class="btn ${S.watch.includes(UID) ? 'on' : ''}" onclick="tg('watch')">👁 Watch ${S.watch.length}</button>
      <button class=btn onclick="forkRepo()">⑂ Fork ${S.fork}</button>
      <button class="btn ${S.star.includes(UID) ? 'on' : ''}" onclick="tg('star')">★ Star ${S.star.length}</button>
      ${own && S.forkOf && R[S.forkOf] ? '<button class="btn g" onclick="openPR()">Abrir PR</button>' : ''}
    </div>
    ${own ? '' : '<p class=mu>🔒 Somente leitura: faça um fork para editar.</p>'}
    <div class=tabs>
      ${T.map(t => `<a class="${V.tab == t[0] ? 'on' : ''}" onclick="go({tab:'${t[0]}',edit:0,cm:0})">${t[1]}${t[2] ? `<span class=ct>${t[2]}</span>` : ''}</a>`).join('')}
    </div>
    ${b}
  `;
}

UN[UID] = 'Você';
$('#me').textContent = UN[UID];
if (!S && Object.keys(R).length > 0) {
  S = R[Object.keys(R)[0]];
}
render();
</script>
</body>
</html>
