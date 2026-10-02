
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Neural-Raphael-Hub | Cloud Git, Containers & Web Hosting</title>
    <style>
        :root {
            --bg-dark: #0d1117;
            --card-bg: #161b22;
            --border-color: #30363d;
            --accent-red: #ff2a2a;
            --text-main: #c9d1d9;
            --text-white: #f0f6fc;
            --green-btn: #238636;
            --blue-link: #58a6ff;
        }

        * { box-sizing: border-box; margin: 0; padding: 0; font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif; }

        body { background: var(--bg-dark); color: var(--text-main); height: 100vh; display: flex; flex-direction: column; overflow: hidden; }

        /* HEADER */
        header {
            background: #161b22; padding: 12px 24px;
            display: flex; align-items: center; justify-content: space-between;
            border-bottom: 1px solid var(--border-color);
        }

        .brand { font-weight: bold; color: var(--text-white); font-size: 16px; display: flex; align-items: center; gap: 10px; }
        .brand span { color: var(--accent-red); }

        .btn {
            background: var(--card-bg); border: 1px solid var(--border-color);
            color: var(--text-white); padding: 6px 12px; border-radius: 6px;
            cursor: pointer; font-size: 12px; font-weight: 500;
        }

        .btn-green { background: var(--green-btn); border-color: rgba(240,246,252,0.1); }
        .btn-green:hover { background: #2ea043; }

        /* LAYOUT */
        #hub-layout { display: flex; flex-grow: 1; height: calc(100vh - 55px); }

        /* SIDEBAR */
        #sidebar {
            width: 280px; background: #0d1117; border-right: 1px solid var(--border-color);
            padding: 15px; display: flex; flex-direction: column; gap: 20px;
        }

        .menu-section-title { font-size: 11px; font-weight: 600; color: #8b949e; text-transform: uppercase; margin-bottom: 8px; }

        .item-link {
            padding: 6px 10px; font-size: 13px; border-radius: 6px;
            cursor: pointer; display: flex; align-items: center; justify-content: space-between;
            color: var(--text-main); margin-bottom: 2px;
        }
        .item-link:hover { background: #21262d; }
        .item-link.active { background: #1f6feb22; color: var(--blue-link); font-weight: 600; }

        /* MAIN CONTENT WORKSPACE */
        #main-content { flex-grow: 1; display: flex; flex-direction: column; background: var(--bg-dark); }

        .repo-header {
            padding: 16px 24px; border-bottom: 1px solid var(--border-color);
            display: flex; justify-content: space-between; align-items: center;
        }

        .repo-title { font-size: 18px; color: var(--blue-link); font-weight: 600; }

        /* WORKSPACE TABS */
        .repo-tabs { display: flex; gap: 15px; padding: 0 24px; border-bottom: 1px solid var(--border-color); background: #161b22; }
        .tab-btn { padding: 10px 0; font-size: 13px; color: #8b949e; cursor: pointer; border-bottom: 2px solid transparent; }
        .tab-btn.active { color: var(--text-white); border-bottom-color: var(--accent-red); font-weight: 600; }

        .workspace-panel { flex-grow: 1; padding: 20px; display: none; overflow-y: auto; }
        .workspace-panel.active { display: block; }

        /* CODE EDITOR & DEPLOYER */
        #code-editor {
            width: 100%; height: 250px; background: #0d1117;
            border: 1px solid var(--border-color); color: #79c0ff;
            padding: 12px; font-family: monospace; font-size: 13px;
            border-radius: 6px; outline: none; margin-bottom: 15px;
        }

        .web-preview-box {
            width: 100%; height: 250px; background: #fff;
            border: 1px solid var(--border-color); border-radius: 6px;
        }

        .active-url-badge {
            background: rgba(0, 230, 118, 0.15); border: 1px solid #00e676;
            color: #00e676; padding: 8px 12px; border-radius: 6px;
            font-size: 12px; display: inline-flex; align-items: center; gap: 8px; margin-bottom: 15px;
        }
    </style>
</head>
<body>

    <header>
        <div class="brand">
            <div style="width:12px; height:12px; background:var(--accent-red); border-radius:50%;"></div>
            Neural-Raphael-Hub <span>Platform</span>
        </div>
        <div>
            <button class="btn btn-green" onclick="hub.openRepoModal()">+ Novo Repositório</button>
        </div>
    </header>

    <div id="hub-layout">
        <!-- SIDEBAR REPOS & CONTAINERS -->
        <div id="sidebar">
            <div>
                <div class="menu-section-title">Seus Repositórios</div>
                <div id="repo-list"></div>
            </div>

            <div>
                <div class="menu-section-title">Containers & Docker</div>
                <div id="container-list"></div>
            </div>

            <div>
                <div class="menu-section-title">Tags & Releases</div>
                <div id="tag-list"></div>
            </div>
        </div>

        <!-- WORKSPACE PRINCIPAL -->
        <div id="main-content">
            <div class="repo-header">
                <div>
                    <span class="repo-title" id="current-repo-name">neural-raphael-core</span>
                    <span style="font-size:12px; color:#8b949e; margin-left:10px;">Public</span>
                </div>
                <button class="btn btn-green" onclick="hub.deployWebSite()">🚀 Activar / Connect Site Link</button>
            </div>

            <div class="repo-tabs">
                <div class="tab-btn active" onclick="hub.switchTab('code')">Code & Editor</div>
                <div class="tab-btn" onclick="hub.switchTab('hosting')">Web Hosting & Active Links</div>
                <div class="tab-btn" onclick="hub.switchTab('branches')">Branches</div>
            </div>

            <!-- TAB CODE -->
            <div class="workspace-panel active" id="tab-code">
                <div style="margin-bottom:10px; display:flex; justify-content:space-between; align-items:center;">
                    <span style="font-size:12px; color:#8b949e;">Arquivo: index.html</span>
                    <button class="btn" onclick="hub.saveCode()">Salvar Alterações</button>
                </div>
                <textarea id="code-editor" spellcheck="false"></textarea>
                <div style="font-size:12px; color:#8b949e; margin-bottom:8px;">Live Web Engine Preview:</div>
                <iframe class="web-preview-box" id="web-preview"></iframe>
            </div>

            <!-- TAB HOSTING -->
            <div class="workspace-panel" id="tab-hosting">
                <h3>Gerenciador de Links e Tag Sites</h3>
                <p style="font-size:12px; color:#8b949e; margin-top:5px; margin-bottom:20px;">
                    O Neural-Raphael-Hub permite publicar seu repositório na Web diretamente com ativação de domínio e tags.
                </p>

                <div id="hosting-status-container">
                    <div class="active-url-badge" id="active-url-box">
                        ⚡ Site Ativo e Conectado à Web: <a href="#" id="active-web-link" target="_blank" style="color:#00e676; font-weight:bold;">https://neural-raphael-core.hub.net</a>
                    </div>
                </div>
            </div>

            <!-- TAB BRANCHES -->
            <div class="workspace-panel" id="tab-branches">
                <h3>Branches do Git</h3>
                <div id="branches-container" style="margin-top:15px;"></div>
            </div>
        </div>
    </div>

    <script>
        /**
         * NEURAL-RAPHAEL-HUB ENGINE
         * Gerenciador de Plataforma estilo GitHub com Conexão/Ativação de Links Web
         */
        class NeuralRaphaelHub {
            constructor() {
                this.repositories = [
                    {
                        id: 'repo-1',
                        name: 'neural-raphael-core',
                        activeLink: 'https://neural-raphael-core.hub.net',
                        code: '<!DOCTYPE html>\n<html>\n<head>\n  <style>body{background:#0d1117; color:#00e676; font-family:sans-serif; text-align:center; padding-top:40px;}</style>\n</head>\n<body>\n  <h1>Neural-Raphael-Hub Engine</h1>\n  <p>Site hospedado e ativo na Web com conexão direta!</p>\n</body>\n</html>',
                        branches: ['main', 'dev'],
                        tags: ['v1.0.0']
                    }
                ];

                this.containers = [
                    { name: 'web-nginx-container', status: 'Running' }
                ];

                this.activeRepoId = 'repo-1';
                this.init();
            }

            init() {
                this.renderSidebar();
                this.loadActiveRepo();
            }

            renderSidebar() {
                // Render Repos
                const repoList = document.getElementById('repo-list');
                repoList.innerHTML = '';
                this.repositories.forEach(repo => {
                    const item = document.createElement('div');
                    item.className = `item-link ${repo.id === this.activeRepoId ? 'active' : ''}`;
                    item.innerHTML = `📁 ${repo.name}`;
                    item.onclick = () => this.selectRepo(repo.id);
                    repoList.appendChild(item);
                });

                // Render Containers
                const cntList = document.getElementById('container-list');
                cntList.innerHTML = '';
                this.containers.forEach(cnt => {
                    const item = document.createElement('div');
                    item.className = 'item-link';
                    item.innerHTML = `📦 ${cnt.name}`;
                    cntList.appendChild(item);
                });

                // Render Tags
                const tagList = document.getElementById('tag-list');
                tagList.innerHTML = '';
                const activeRepo = this.getActiveRepo();
                activeRepo.tags.forEach(tag => {
                    const item = document.createElement('div');
                    item.className = 'item-link';
                    item.innerHTML = `🏷️ ${tag}`;
                    tagList.appendChild(item);
                });
            }

            getActiveRepo() {
                return this.repositories.find(r => r.id === this.activeRepoId);
            }

            selectRepo(id) {
                this.activeRepoId = id;
                this.renderSidebar();
                this.loadActiveRepo();
            }

            loadActiveRepo() {
                const repo = this.getActiveRepo();
                document.getElementById('current-repo-name').textContent = repo.name;
                document.getElementById('code-editor').value = repo.code;
                document.getElementById('web-preview').srcdoc = repo.code;
                document.getElementById('active-web-link').textContent = repo.activeLink;
                document.getElementById('active-web-link').href = repo.activeLink;

                // Render Branches
                const branchBox = document.getElementById('branches-container');
                branchBox.innerHTML = '';
                repo.branches.forEach(b => {
                    const div = document.createElement('div');
                    div.style.cssText = "padding:10px; background:#161b22; margin-bottom:5px; border-radius:6px;";
                    div.textContent = `🌿 Branch: ${b}`;
                    branchBox.appendChild(div);
                });
            }

            saveCode() {
                const repo = this.getActiveRepo();
                repo.code = document.getElementById('code-editor').value;
                document.getElementById('web-preview').srcdoc = repo.code;
                alert('Código salvo e atualizado com sucesso!');
            }

            deployWebSite() {
                const repo = this.getActiveRepo();
                alert(`Conexão ativada! O repositório [${repo.name}] foi implantado com sucesso no link:\n${repo.activeLink}`);
            }

            switchTab(tabName) {
                document.querySelectorAll('.tab-btn').forEach(b => b.classList.remove('active'));
                document.querySelectorAll('.workspace-panel').forEach(p => p.classList.remove('active'));

                event.target.classList.add('active');
                document.getElementById(`tab-${tabName}`).classList.add('active');
            }

            openRepoModal() {
                const name = prompt('Nome do Novo Repositório:');
                if (name) {
                    const newRepo = {
                        id: `repo-${Date.now()}`,
                        name: name,
                        activeLink: `https://${name}.hub.net`,
                        code: `<h1>${name} está no ar!</h1>`,
                        branches: ['main'],
                        tags: ['v0.0.1']
                    };
                    this.repositories.push(newRepo);
                    this.selectRepo(newRepo.id);
                }
            }
        }

        const hub = new NeuralRaphaelHub();
    </script>
</body>
</html>
