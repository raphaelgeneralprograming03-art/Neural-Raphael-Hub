
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Neural-Raphael-Cromium | Next-Gen Cloud Platform & IDE</title>
    <style>
        :root {
            --bg-dark: #07080a;
            --bg-card: #111318;
            --toolbar-bg: #161820;
            --sidebar-bg: #0d0e12;
            --accent-red: #ff2a2a;
            --accent-glow: rgba(255, 42, 42, 0.4);
            --dark-ring: #030304;
            --text-main: #f1f3f9;
            --text-muted: #838996;
            --border-color: #262933;
            --border-active: #ff2a2a;
            --success-color: #00e676;
            --warning-color: #ffb300;
            --blue-color: #29b6f6;
            --purple-color: #ab47bc;
        }

        * {
            box-sizing: border-box;
            user-select: none;
            margin: 0;
            padding: 0;
        }

        body, html {
            height: 100%;
            width: 100%;
            font-family: 'Segoe UI', system-ui, -apple-system, monospace;
            background: var(--bg-dark);
            color: var(--text-main);
            overflow: hidden;
        }

        /* --- CHROMIUM RED/BLACK LOGO --- */
        .chromium-logo {
            width: 30px;
            height: 30px;
            position: relative;
            border-radius: 50%;
            background: var(--dark-ring);
            display: inline-block;
            box-shadow: 0 0 12px var(--accent-glow);
            flex-shrink: 0;
            cursor: pointer;
            transition: transform 0.2s;
        }

        .chromium-logo:hover {
            transform: scale(1.05);
        }

        .chromium-logo .center-circle {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            width: 10px;
            height: 10px;
            background: #ff0000;
            border-radius: 50%;
            z-index: 4;
            box-shadow: 0 0 10px #ff0000;
        }

        .chromium-logo .segment {
            position: absolute;
            width: 100%;
            height: 100%;
            border-radius: 50%;
            clip-path: polygon(50% 50%, 0 0, 100% 0);
        }

        .chromium-logo .seg1 { background: #1f1f1f; transform: rotate(0deg); }
        .chromium-logo .seg2 { background: #121212; transform: rotate(120deg); }
        .chromium-logo .seg3 { background: #080808; transform: rotate(240deg); }

        .chromium-logo .outer-ring {
            position: absolute;
            inset: 0;
            border-radius: 50%;
            border: 2px solid #282828;
            z-index: 3;
        }

        /* --- APP LAYOUT ROOT --- */
        #app-root {
            display: flex;
            flex-direction: column;
            height: 100vh;
            width: 100vw;
        }

        /* HEADER & NAVBAR */
        header {
            background: var(--toolbar-bg);
            padding: 8px 14px;
            display: flex;
            align-items: center;
            gap: 12px;
            border-bottom: 1px solid var(--border-color);
            z-index: 20;
        }

        .app-title {
            font-weight: 700;
            font-size: 14px;
            letter-spacing: 0.5px;
            color: var(--text-main);
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .app-title span {
            color: var(--accent-red);
        }

        .nav-group {
            display: flex;
            gap: 4px;
            align-items: center;
        }

        .btn {
            background: #1e212b;
            border: 1px solid var(--border-color);
            color: var(--text-main);
            padding: 6px 12px;
            border-radius: 6px;
            cursor: pointer;
            font-size: 12px;
            display: flex;
            align-items: center;
            gap: 6px;
            transition: all 0.2s;
        }

        .btn:hover {
            background: var(--accent-red);
            border-color: var(--accent-red);
            box-shadow: 0 0 10px var(--accent-glow);
        }

        .btn-icon {
            width: 32px;
            height: 32px;
            padding: 0;
            justify-content: center;
        }

        #address-bar-wrap {
            flex-grow: 1;
            position: relative;
            display: flex;
            align-items: center;
        }

        #address-bar {
            width: 100%;
            background: #090a0d;
            border: 1px solid var(--border-color);
            padding: 7px 35px 7px 32px;
            border-radius: 20px;
            color: var(--text-main);
            font-size: 12px;
            outline: none;
            transition: all 0.2s;
        }

        #address-bar:focus {
            border-color: var(--accent-red);
            box-shadow: 0 0 12px var(--accent-glow);
        }

        .protocol-badge {
            position: absolute;
            left: 10px;
            font-size: 11px;
        }

        /* WORKSPACE PANELS */
        #workspace {
            display: flex;
            flex-grow: 1;
            height: calc(100vh - 50px);
            position: relative;
        }

        /* SIDEBAR / REPOSITORY TREE */
        #sidebar {
            width: 300px;
            background: var(--sidebar-bg);
            border-right: 1px solid var(--border-color);
            display: flex;
            flex-direction: column;
            flex-shrink: 0;
        }

        .sidebar-tabs {
            display: flex;
            border-bottom: 1px solid var(--border-color);
            background: #090a0d;
        }

        .sidebar-tab-btn {
            flex: 1;
            padding: 10px;
            text-align: center;
            font-size: 11px;
            font-weight: 600;
            color: var(--text-muted);
            cursor: pointer;
            border-bottom: 2px solid transparent;
        }

        .sidebar-tab-btn.active {
            color: var(--accent-red);
            border-bottom-color: var(--accent-red);
            background: var(--sidebar-bg);
        }

        .sidebar-panel {
            flex-grow: 1;
            overflow-y: auto;
            padding: 12px;
            display: none;
        }

        .sidebar-panel.active {
            display: block;
        }

        .section-header {
            font-size: 11px;
            text-transform: uppercase;
            letter-spacing: 1px;
            color: var(--text-muted);
            margin-bottom: 10px;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .tree-item {
            padding: 6px 8px;
            font-size: 12px;
            border-radius: 4px;
            cursor: pointer;
            display: flex;
            align-items: center;
            gap: 8px;
            color: var(--text-main);
            margin-bottom: 2px;
        }

        .tree-item:hover {
            background: #181b24;
        }

        .tree-item.active {
            background: #222633;
            color: var(--accent-red);
            font-weight: 600;
        }

        .tree-indent {
            margin-left: 14px;
        }

        /* MAIN CONTENT AREA */
        #main-editor-area {
            flex-grow: 1;
            display: flex;
            flex-direction: column;
            background: var(--bg-dark);
            position: relative;
        }

        /* TOP TAB BAR */
        #tabs-bar {
            display: flex;
            background: #0b0c0f;
            border-bottom: 1px solid var(--border-color);
            overflow-x: auto;
        }

        .tab {
            padding: 8px 16px;
            font-size: 12px;
            background: #12141a;
            color: var(--text-muted);
            border-right: 1px solid var(--border-color);
            cursor: pointer;
            display: flex;
            align-items: center;
            gap: 8px;
            min-width: 130px;
            max-width: 200px;
        }

        .tab.active {
            background: var(--bg-dark);
            color: var(--text-main);
            border-top: 2px solid var(--accent-red);
        }

        .tab .close-tab {
            margin-left: auto;
            border-radius: 50%;
            padding: 2px 4px;
            font-size: 10px;
        }

        .tab .close-tab:hover {
            background: rgba(255,255,255,0.2);
        }

        /* EDITOR / PREVIEW split */
        #code-workspace {
            display: flex;
            flex-grow: 1;
            height: calc(100% - 180px);
        }

        #code-editor {
            flex: 1;
            background: #090a0d;
            color: #a9b7c6;
            border: none;
            padding: 15px;
            font-family: 'Consolas', 'Fira Code', monospace;
            font-size: 13px;
            resize: none;
            outline: none;
            line-height: 1.5;
            border-right: 1px solid var(--border-color);
        }

        #live-preview {
            flex: 1;
            background: #fff;
            border: none;
        }

        /* TERMINAL / LOGS BOTTOM PANEL */
        #bottom-panel {
            height: 180px;
            background: #0a0b0e;
            border-top: 1px solid var(--border-color);
            display: flex;
            flex-direction: column;
        }

        .panel-header {
            background: #111318;
            padding: 6px 12px;
            font-size: 11px;
            display: flex;
            gap: 15px;
            border-bottom: 1px solid var(--border-color);
        }

        .panel-tab {
            cursor: pointer;
            color: var(--text-muted);
        }

        .panel-tab.active {
            color: var(--accent-red);
            font-weight: bold;
        }

        #terminal-output {
            flex-grow: 1;
            padding: 10px;
            font-family: monospace;
            font-size: 12px;
            color: #00e676;
            overflow-y: auto;
            white-space: pre-wrap;
        }

        /* --- CANVAS OVERLAY (OVERVIEW) --- */
        #overview-overlay {
            position: fixed;
            inset: 0;
            background: rgba(5, 5, 8, 0.94);
            z-index: 1000;
            display: none;
            flex-direction: column;
            backdrop-filter: blur(12px);
        }

        #overview-overlay.active {
            display: flex;
        }

        .overview-top {
            padding: 16px 24px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            border-bottom: 1px solid var(--border-color);
        }

        #overview-canvas {
            flex-grow: 1;
            width: 100%;
            height: 100%;
        }

        /* CARD MODALS */
        .modal {
            position: fixed;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            background: var(--bg-card);
            border: 1px solid var(--border-color);
            border-radius: 8px;
            padding: 20px;
            width: 450px;
            z-index: 2000;
            display: none;
            box-shadow: 0 10px 30px rgba(0,0,0,0.8);
        }

        .modal.active {
            display: block;
        }

        .modal-header {
            font-weight: bold;
            margin-bottom: 15px;
            display: flex;
            justify-content: space-between;
        }

        .form-group {
            margin-bottom: 12px;
        }

        .form-group label {
            display: block;
            font-size: 11px;
            color: var(--text-muted);
            margin-bottom: 4px;
        }

        .form-group input, .form-group select {
            width: 100%;
            padding: 8px;
            background: #08090b;
            border: 1px solid var(--border-color);
            color: #fff;
            border-radius: 4px;
            outline: none;
        }

        /* BADGES */
        .badge {
            padding: 2px 6px;
            border-radius: 4px;
            font-size: 10px;
            font-weight: bold;
        }

        .badge-red { background: rgba(255,42,42,0.2); color: var(--accent-red); }
        .badge-green { background: rgba(0,230,118,0.2); color: var(--success-color); }
        .badge-blue { background: rgba(41,182,246,0.2); color: var(--blue-color); }
        .badge-purple { background: rgba(171,71,188,0.2); color: var(--purple-color); }
    </style>
</head>
<body>

    <div id="app-root">
        <!-- HEADER TOP BAR -->
        <header>
            <div class="chromium-logo" onclick="app.toggleOverview()" title="Visão Geral do Sistema (Overview Canvas)">
                <div class="outer-ring"></div>
                <div class="center-circle"></div>
                <div class="segment seg1"></div>
                <div class="segment seg2"></div>
                <div class="segment seg3"></div>
            </div>

            <div class="app-title">
                Neural-Raphael-Cromium <span>IDE Engine</span>
            </div>

            <div class="nav-group">
                <button class="btn btn-icon" onclick="app.toggleOverview()" title="Overview Canvas 2D">🔳</button>
                <button class="btn" onclick="app.openModal('repo-modal')">➕ Novo Repositório</button>
                <button class="btn" onclick="app.openModal('container-modal')">📦 Novo Contêiner</button>
            </div>

            <div id="address-bar-wrap">
                <span class="protocol-badge">⚡</span>
                <input type="text" id="address-bar" value="neural://repository/main-core" onkeydown="app.handleAddressKey(event)">
            </div>

            <div class="nav-group">
                <button class="btn" onclick="app.gitCommit()">💾 Commit</button>
                <button class="btn" onclick="app.gitPush()">🚀 Push</button>
            </div>
        </header>

        <!-- WORKSPACE CORE -->
        <div id="workspace">
            <!-- SIDEBAR: REPOS, BRANCHES, CONTAINERS & TAGS -->
            <div id="sidebar">
                <div class="sidebar-tabs">
                    <div class="sidebar-tab-btn active" onclick="app.switchSidebarTab('repos')">REPOS</div>
                    <div class="sidebar-tab-btn" onclick="app.switchSidebarTab('branches')">BRANCHES</div>
                    <div class="sidebar-tab-btn" onclick="app.switchSidebarTab('containers')">DOCKER</div>
                    <div class="sidebar-tab-btn" onclick="app.switchSidebarTab('tags')">TAGS</div>
                </div>

                <!-- PANEL REPOSITORIES -->
                <div class="sidebar-panel active" id="panel-repos">
                    <div class="section-header">
                        <span>Repositórios Ativos</span>
                        <span class="badge badge-red" id="repo-count">0</span>
                    </div>
                    <div id="repo-tree-list"></div>
                </div>

                <!-- PANEL BRANCHES -->
                <div class="sidebar-panel" id="panel-branches">
                    <div class="section-header">
                        <span>Branches Git</span>
                        <button class="btn btn-icon" style="height:20px; width:20px;" onclick="app.createBranch()">+</button>
                    </div>
                    <div id="branch-tree-list"></div>
                </div>

                <!-- PANEL CONTAINERS -->
                <div class="sidebar-panel" id="panel-containers">
                    <div class="section-header">
                        <span>Contêineres Ativos</span>
                        <span class="badge badge-blue" id="container-count">0</span>
                    </div>
                    <div id="container-tree-list"></div>
                </div>

                <!-- PANEL TAGS & RELEASES -->
                <div class="sidebar-panel" id="panel-tags">
                    <div class="section-header">
                        <span>Tags & Versions</span>
                        <button class="btn btn-icon" style="height:20px; width:20px;" onclick="app.createTag()">+</button>
                    </div>
                    <div id="tag-tree-list"></div>
                </div>
            </div>

            <!-- MAIN EDITOR & LIVE ENGINE -->
            <div id="main-editor-area">
                <div id="tabs-bar">
                    <!-- Abas injetadas dinamicamente -->
                </div>

                <div id="code-workspace">
                    <textarea id="code-editor" spellcheck="false" oninput="app.onCodeChange()"></textarea>
                    <iframe id="live-preview"></iframe>
                </div>

                <!-- BOTTOM TERMINAL LOGS -->
                <div id="bottom-panel">
                    <div class="panel-header">
                        <span class="panel-tab active" onclick="app.switchTerminalTab('console')">Console Executável</span>
                        <span class="panel-tab" onclick="app.switchTerminalTab('docker')">Logs do Docker Container</span>
                        <span class="panel-tab" onclick="app.switchTerminalTab('git')">Git CLI Log</span>
                    </div>
                    <div id="terminal-output">Neural-Raphael Engine inicializada com sucesso.
Aguardando comandos da CLI...</div>
                </div>
            </div>
        </div>
    </div>

    <!-- OVERVIEW CANVAS OVERLAY -->
    <div id="overview-overlay">
        <div class="overview-top">
            <div class="app-title">
                <div class="chromium-logo" style="transform: scale(0.8)">
                    <div class="outer-ring"></div>
                    <div class="center-circle"></div>
                    <div class="segment seg1"></div>
                    <div class="segment seg2"></div>
                    <div class="segment seg3"></div>
                </div>
                Visão Geral da Arquitetura (Canvas 2D Overview System)
            </div>
            <button class="btn btn-icon" onclick="app.toggleOverview()">✕</button>
        </div>
        <canvas id="overview-canvas"></canvas>
    </div>

    <!-- MODAL NOVO REPOSITÓRIO -->
    <div class="modal" id="repo-modal">
        <div class="modal-header">
            <span>Criar Novo Repositório</span>
            <span style="cursor:pointer;" onclick="app.closeModal('repo-modal')">✕</span>
        </div>
        <div class="form-group">
            <label>Nome do Repositório</label>
            <input type="text" id="new-repo-name" placeholder="ex: neural-ai-core">
        </div>
        <div class="form-group">
            <label>Visibilidade</label>
            <select id="new-repo-vis">
                <option value="public">Público</option>
                <option value="private">Privado</option>
            </select>
        </div>
        <button class="btn" style="width:100%; justify-content:center;" onclick="app.confirmCreateRepo()">Criar Repositório</button>
    </div>

    <!-- MODAL NOVO CONTÊINER -->
    <div class="modal" id="container-modal">
        <div class="modal-header">
            <span>Subir Novo Contêiner Docker</span>
            <span style="cursor:pointer;" onclick="app.closeModal('container-modal')">✕</span>
        </div>
        <div class="form-group">
            <label>Nome do Contêiner</label>
            <input type="text" id="new-container-name" placeholder="ex: node-runner-v16">
        </div>
        <div class="form-group">
            <label>Imagem Base</label>
            <select id="new-container-img">
                <option value="node:18-alpine">node:18-alpine</option>
                <option value="python:3.10-slim">python:3.10-slim</option>
                <option value="nginx:latest">nginx:latest</option>
                <option value="ubuntu:22.04">ubuntu:22.04</option>
            </select>
        </div>
        <button class="btn" style="width:100%; justify-content:center;" onclick="app.confirmCreateContainer()">Iniciar Contêiner</button>
    </div>

    <script>
        /**
         * ENGINE EXECUTÁVEL COMPLETA - NEURAL-RAPHAEL-CROMIUM PLATFORM
         * Gerenciador de Repositórios, Arquivos, Containers, Branches e Canvas Overview
         */
        class NeuralPlatformEngine {
            constructor() {
                // Estrutura de Armazenamento de Dados Extensível
                this.repositories = [];
                this.containers = [];
                this.tags = [];
                this.activeRepoId = null;
                this.activeBranch = 'main';
                this.openTabs = [];
                this.activeTabFileId = null;
                
                this.canvas = document.getElementById('overview-canvas');
                this.ctx = this.canvas.getContext('2d');
                
                this.initApp();
            }

            initApp() {
                this.seedDefaultData();
                this.renderSidebarPanels();
                this.setupCanvasResize();
                this.startOverviewRenderLoop();
                this.logTerminal("System", "Plataforma Neural-Raphael inicializada. Pronta para processamento.");
            }

            seedDefaultData() {
                // Repositório Padrão Inicial
                const defaultRepo = {
                    id: 'repo-1',
                    name: 'neural-raphael-core',
                    visibility: 'public',
                    branches: ['main', 'dev-feature', 'bugfix-canvas'],
                    files: [
                        { id: 'file-1', name: 'index.html', content: '<!DOCTYPE html>\n<html>\n<head>\n  <style>body{background:#111; color:#00e676; font-family:sans-serif; text-align:center; padding-top:50px;}</style>\n</head>\n<body>\n  <h1>Neural-Raphael App Executing</h1>\n  <p>Ambiente de código renderizado em tempo real.</p>\n</body>\n</html>' },
                        { id: 'file-2', name: 'styles.css', content: '/* Estilos globais do repositório */\nbody { margin: 0; padding: 0; }' },
                        { id: 'file-3', name: 'main.js', content: '// Script Principal\nconsole.log("Neural Core Active");' }
                    ]
                };

                // Contêiner Padrão
                const defaultContainer = {
                    id: 'cnt-1',
                    name: 'neural-web-proxy',
                    image: 'node:18-alpine',
                    status: 'running',
                    port: '8080:80'
                };

                // Tags Padrão
                this.tags = [
                    { name: 'v1.0.0-alpha', hash: 'a1b2c3d', date: '2026-03-30' },
                    { name: 'v1.1.0-stable', hash: 'f9e8d7c', date: '2026-04-01' }
                ];

                this.repositories.push(defaultRepo);
                this.containers.push(defaultContainer);
                this.activeRepoId = defaultRepo.id;

                // Abrir primeiro arquivo no editor
                this.openFile(defaultRepo.files[0].id);
            }

            // --- NAVEGAÇÃO DE SIDEBAR ---
            switchSidebarTab(tabName) {
                document.querySelectorAll('.sidebar-tab-btn').forEach(btn => btn.classList.remove('active'));
                document.querySelectorAll('.sidebar-panel').forEach(panel => panel.classList.remove('active'));

                event.target.classList.add('active');
                document.getElementById(`panel-${tabName}`).classList.add('active');
            }

            renderSidebarPanels() {
                // Render Repositórios
                const repoList = document.getElementById('repo-tree-list');
                repoList.innerHTML = '';
                document.getElementById('repo-count').textContent = this.repositories.length;

                this.repositories.forEach(repo => {
                    const repoEl = document.createElement('div');
                    repoEl.className = `tree-item ${repo.id === this.activeRepoId ? 'active' : ''}`;
                    repoEl.innerHTML = `📁 <strong>${repo.name}</strong> <span class="badge badge-blue">${repo.visibility}</span>`;
                    repoEl.onclick = () => this.selectRepository(repo.id);
                    repoList.appendChild(repoEl);

                    // Arquivos do Repositório Se For Ativo
                    if (repo.id === this.activeRepoId) {
                        repo.files.forEach(file => {
                            const fileEl = document.createElement('div');
                            fileEl.className = `tree-item tree-indent ${file.id === this.activeTabFileId ? 'active' : ''}`;
                            fileEl.innerHTML = `📄 ${file.name}`;
                            fileEl.onclick = (e) => {
                                e.stopPropagation();
                                this.openFile(file.id);
                            };
                            repoList.appendChild(fileEl);
                        });
                    }
                });

                // Render Branches
                const branchList = document.getElementById('branch-tree-list');
                branchList.innerHTML = '';
                const activeRepo = this.getActiveRepo();
                if (activeRepo) {
                    activeRepo.branches.forEach(branch => {
                        const bEl = document.createElement('div');
                        bEl.className = `tree-item ${branch === this.activeBranch ? 'active' : ''}`;
                        bEl.innerHTML = `🌿 ${branch} ${branch === this.activeBranch ? '(Current)' : ''}`;
                        bEl.onclick = () => this.switchBranch(branch);
                        branchList.appendChild(bEl);
                    });
                }

                // Render Containers
                const cntList = document.getElementById('container-tree-list');
                cntList.innerHTML = '';
                document.getElementById('container-count').textContent = this.containers.length;
                this.containers.forEach(cnt => {
                    const cEl = document.createElement('div');
                    cEl.className = 'tree-item';
                    cEl.innerHTML = `📦 <strong>${cnt.name}</strong> <span class="badge badge-green">${cnt.status}</span>`;
                    cntList.appendChild(cEl);
                });

                // Render Tags
                const tagList = document.getElementById('tag-tree-list');
                tagList.innerHTML = '';
                this.tags.forEach(tag => {
                    const tEl = document.createElement('div');
                    tEl.className = 'tree-item';
                    tEl.innerHTML = `🏷️ <strong>${tag.name}</strong> <span style="font-size:10px; color:var(--text-muted);">${tag.hash}</span>`;
                    tagList.appendChild(tEl);
                });
            }

            // --- EDITOR & TABS SYSTEM ---
            openFile(fileId) {
                const repo = this.getActiveRepo();
                const file = repo.files.find(f => f.id === fileId);
                if (!file) return;

                if (!this.openTabs.includes(fileId)) {
                    this.openTabs.push(fileId);
                }

                this.activeTabFileId = fileId;
                this.renderTabsUI();

                const editor = document.getElementById('code-editor');
                editor.value = file.content;
                this.updateLivePreview(file.content);
                this.renderSidebarPanels();
            }

            closeTab(fileId, e) {
                if (e) e.stopPropagation();
                this.openTabs = this.openTabs.filter(id => id !== fileId);
                
                if (this.activeTabFileId === fileId) {
                    this.activeTabFileId = this.openTabs.length > 0 ? this.openTabs[this.openTabs.length - 1] : null;
                }

                if (this.activeTabFileId) {
                    this.openFile(this.activeTabFileId);
                } else {
                    document.getElementById('code-editor').value = '';
                    document.getElementById('live-preview').srcdoc = '';
                }

                this.renderTabsUI();
            }

            renderTabsUI() {
                const tabsBar = document.getElementById('tabs-bar');
                tabsBar.innerHTML = '';

                const repo = this.getActiveRepo();
                this.openTabs.forEach(fileId => {
                    const file = repo.files.find(f => f.id === fileId);
                    if (!file) return;

                    const tab = document.createElement('div');
                    tab.className = `tab ${file.id === this.activeTabFileId ? 'active' : ''}`;
                    tab.onclick = () => this.openFile(file.id);
                    tab.innerHTML = `
                        📄 ${file.name}
                        <span class="close-tab" onclick="app.closeTab('${file.id}', event)">✕</span>
                    `;
                    tabsBar.appendChild(tab);
                });
            }

            onCodeChange() {
                if (!this.activeTabFileId) return;
                const content = document.getElementById('code-editor').value;
                const repo = this.getActiveRepo();
                const file = repo.files.find(f => f.id === this.activeTabFileId);
                if (file) {
                    file.content = content;
                    this.updateLivePreview(content);
                }
            }

            updateLivePreview(code) {
                const preview = document.getElementById('live-preview');
                preview.srcdoc = code;
            }

            // --- GIT SIMULATION & MODALS ---
            getActiveRepo() {
                return this.repositories.find(r => r.id === this.activeRepoId);
            }

            selectRepository(repoId) {
                this.activeRepoId = repoId;
                this.renderSidebarPanels();
                this.logTerminal("Git", `Switched active repository to ID: ${repoId}`);
            }

            switchBranch(branchName) {
                this.activeBranch = branchName;
                this.renderSidebarPanels();
                this.logTerminal("Git", `Checkout to branch '${branchName}'`);
            }

            gitCommit() {
                this.logTerminal("Git", `[${this.activeBranch}] Commit executado. Alterações salvas no staging.`);
            }

            gitPush() {
                this.logTerminal("Git", `Push realizado com sucesso para origin/${this.activeBranch}.`);
            }

            openModal(modalId) {
                document.getElementById(modalId).classList.add('active');
            }

            closeModal(modalId) {
                document.getElementById(modalId).classList.remove('active');
            }

            confirmCreateRepo() {
                const name = document.getElementById('new-repo-name').value || 'new-repo';
                const vis = document.getElementById('new-repo-vis').value;

                const newRepo = {
                    id: `repo-${Date.now()}`,
                    name: name,
                    visibility: vis,
                    branches: ['main'],
                    files: [
                        { id: `file-${Date.now()}`, name: 'README.md', content: `# ${name}\nRepositório criado na Plataforma Neural.` }
                    ]
                };

                this.repositories.push(newRepo);
                this.closeModal('repo-modal');
                this.selectRepository(newRepo.id);
                this.logTerminal("System", `Novo repositório criado: ${name}`);
            }

            confirmCreateContainer() {
                const name = document.getElementById('new-container-name').value || 'container-runner';
                const img = document.getElementById('new-container-img').value;

                const newCnt = {
                    id: `cnt-${Date.now()}`,
                    name: name,
                    image: img,
                    status: 'running',
                    port: '3000:3000'
                };

                this.containers.push(newCnt);
                this.closeModal('container-modal');
                this.renderSidebarPanels();
                this.logTerminal("Docker", `Contêiner estanciado: ${name} (${img})`);
            }

            createBranch() {
                const bName = prompt("Nome da nova branch:");
                if (bName) {
                    const repo = this.getActiveRepo();
                    repo.branches.push(bName);
                    this.switchBranch(bName);
                }
            }

            createTag() {
                const tagName = prompt("Nome da Tag (ex: v1.2.0):");
                if (tagName) {
                    this.tags.push({ name: tagName, hash: Math.random().toString(16).substr(2, 7), date: '2026-10-02' });
                    this.renderSidebarPanels();
                    this.logTerminal("Git", `Nova Tag criada: ${tagName}`);
                }
            }

            // --- CANVAS OVERVIEW 2D SYSTEM ---
            toggleOverview() {
                const overlay = document.getElementById('overview-overlay');
                overlay.classList.toggle('active');
                if (overlay.classList.contains('active')) {
                    this.setupCanvasResize();
                    this.drawOverviewTopology();
                }
            }

            setupCanvasResize() {
                this.canvas.width = window.innerWidth;
                this.canvas.height = window.innerHeight - 70;
            }

            drawOverviewTopology() {
                this.ctx.clearRect(0, 0, this.canvas.width, this.canvas.height);

                // Desenhar nó do núcleo central (Core Engine)
                const centerX = this.canvas.width / 2;
                const centerY = 120;

                this.drawNode(centerX, centerY, "Neural Core Engine", "#ff2a2a", "CORE");

                // Renderizar Repositórios no Canvas
                let repoX = centerX - ((this.repositories.length - 1) * 180) / 2;
                let repoY = 280;

                this.repositories.forEach((repo, idx) => {
                    const currentX = repoX + (idx * 200);
                    this.drawConnector(centerX, centerY, currentX, repoY);
                    this.drawNode(currentX, repoY, repo.name, "#29b6f6", "REPO");

                    // Renderizar Branches
                    repo.branches.forEach((b, bIdx) => {
                        const branchY = repoY + 120 + (bIdx * 50);
                        this.drawConnector(currentX, repoY, currentX, branchY);
                        this.drawNode(currentX, branchY, `branch: ${b}`, "#ab47bc", "GIT");
                    });
                });

                // Renderizar Contêineres à direita
                let cntX = centerX + 350;
                let cntY = 280;
                this.containers.forEach((cnt, cIdx) => {
                    const yPos = cntY + (cIdx * 90);
                    this.drawConnector(centerX, centerY, cntX, yPos);
                    this.drawNode(cntX, yPos, cnt.name, "#00e676", "DOCKER");
                });
            }

            drawNode(x, y, label, color, type) {
                this.ctx.save();
                this.ctx.shadowBlur = 15;
                this.ctx.shadowColor = color;

                this.ctx.fillStyle = "#111318";
                this.ctx.strokeStyle = color;
                this.ctx.lineWidth = 2;

                this.ctx.beginPath();
                this.ctx.roundRect(x - 75, y - 25, 150, 50, 8);
                this.ctx.fill();
                this.ctx.stroke();

                this.ctx.shadowBlur = 0;
                this.ctx.fillStyle = "#ffffff";
                this.ctx.font = "bold 11px monospace";
                this.ctx.textAlign = "center";
                this.ctx.fillText(label, x, y - 2);

                this.ctx.fillStyle = color;
                this.ctx.font = "9px sans-serif";
                this.ctx.fillText(`[${type}]`, x, y + 14);

                this.ctx.restore();
            }

            drawConnector(x1, y1, x2, y2) {
                this.ctx.save();
                this.ctx.strokeStyle = "rgba(255, 255, 255, 0.15)";
                this.ctx.lineWidth = 2;
                this.ctx.beginPath();
                this.ctx.moveTo(x1, y1);
                this.ctx.lineTo(x2, y2);
                this.ctx.stroke();
                this.ctx.restore();
            }

            startOverviewRenderLoop() {
                const render = () => {
                    if (document.getElementById('overview-overlay').classList.contains('active')) {
                        this.drawOverviewTopology();
                    }
                    requestAnimationFrame(render);
                };
                render();
            }

            // --- TERMINAL LOGS ---
            logTerminal(channel, message) {
                const term = document.getElementById('terminal-output');
                const time = new Date().toLocaleTimeString();
                term.textContent += `\n[${time}] [${channel}] > ${message}`;
                term.scrollTop = term.scrollHeight;
            }

            switchTerminalTab(tab) {
                document.querySelectorAll('.panel-tab').forEach(t => t.classList.remove('active'));
                event.target.classList.add('active');
                this.logTerminal("CLI", `Exibindo canal: ${tab}`);
            }

            handleAddressKey(e) {
                if (e.key === 'Enter') {
                    this.logTerminal("Router", `Navegando para rota: ${e.target.value}`);
                }
            }
        }

        // Inicializar aplicação globalmente
        const app = new NeuralPlatformEngine();
    </script>
</body>
</html>
