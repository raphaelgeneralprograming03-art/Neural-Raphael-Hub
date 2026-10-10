/**
 * Project: Neural Raphael Hub
 * Description: GitHub Clone Clone with custom dark red & bright green neon theme.
 * File: server.js (Core Backend, SQLite Database & Frontend Dashboard)
 * Target: ~500 lines of robust, modular code.
 */

const express = require('express');
const sqlite3 = require('sqlite3').verbose();
const bodyParser = require('body-parser');
const path = require('path');
const crypto = require('crypto');

const app = express();
const PORT = process.env.PORT || 3000;

// Middleware configuration
app.use(bodyParser.urlencoded({ extended: true }));
app.use(bodyParser.json());
app.use(express.static(path.join(__dirname, 'public')));

// Database Initialization (SQLite)
const dbFile = path.join(__dirname, 'neural_raphael_hub.db');
const db = new sqlite3.Database(dbFile, (err) => {
    if (err) {
        console.error('Error opening database 500 error:', err.message);
    } else {
        console.log('Connected to the Neural Raphael Hub SQLite database.');
        initializeDatabase();
    }
});

// Database Schema Creation
function initializeDatabase() {
    db.serialize(() => {
        // Users Table
        db.run(`CREATE TABLE IF NOT EXISTS users (
            id INTEGER PRIMARY KEY AUTOINCREMENT,
            username TEXT UNIQUE NOT NULL,
            email TEXT UNIQUE NOT NULL,
            created_at DATETIME DEFAULT CURRENT_TIMESTAMP
        )`);

        // Repositories Table
        db.run(`CREATE TABLE IF NOT EXISTS repositories (
            id INTEGER PRIMARY KEY AUTOINCREMENT,
            name TEXT NOT NULL,
            description TEXT,
            owner_id INTEGER,
            is_private BOOLEAN DEFAULT 0,
            stars INTEGER DEFAULT 0,
            forks INTEGER DEFAULT 0,
            created_at DATETIME DEFAULT CURRENT_TIMESTAMP,
            FOREIGN KEY(owner_id) REFERENCES users(id)
        )`);

        // Commits Table
        db.run(`CREATE TABLE IF NOT EXISTS commits (
            id INTEGER PRIMARY KEY AUTOINCREMENT,
            repo_id INTEGER,
            message TEXT NOT NULL,
            hash TEXT NOT NULL,
            author TEXT,
            created_at DATETIME DEFAULT CURRENT_TIMESTAMP,
            FOREIGN KEY(repo_id) REFERENCES repositories(id)
        )`);

        // Issues Table
        db.run(`CREATE TABLE IF NOT EXISTS issues (
            id INTEGER PRIMARY KEY AUTOINCREMENT,
            repo_id INTEGER,
            title TEXT NOT NULL,
            body TEXT,
            status TEXT DEFAULT 'open',
            created_at DATETIME DEFAULT CURRENT_TIMESTAMP,
            FOREIGN KEY(repo_id) REFERENCES repositories(id)
        )`);

        // Seed initial data if empty
        db.get(`SELECT COUNT(*) as count FROM users`, (err, row) => {
            if (row && row.count === 0) {
                seedInitialData();
            }
        });
    });
}

function seedInitialData() {
    db.run(`INSERT INTO users (username, email) VALUES ('raphael_neural', 'raphael@neuralhub.com')`, function(err) {
        if (!err) {
            const userId = this.lastID;
            db.run(`INSERT INTO repositories (name, description, owner_id, is_private, stars, forks) VALUES 
                ('neural-core', 'Core intelligence engine for Neural Raphael Hub', ?, 0, 142, 38),
                ('quantum-net', 'Distributed decentralized network nodes', ?, 0, 89, 12)`, 
                [userId, userId]);
        }
    });
}

// ==========================================
// API REST ENDPOINTS
// ==========================================

// Get all repositories and overview stats
app.apiRouter = express.Router();

app.get('/api/repos', (req, res) => {
    const query = `
        SELECT r.*, u.username as owner_name 
        FROM repositories r 
        JOIN users u ON r.owner_id = u.id
        ORDER BY r.created_at DESC
    `;
    db.all(query, [], (err, rows) => {
        if (err) {
            res.status(500).json({ error: err.message });
            return;
        }
        res.json({ repositories: rows });
    });
});

app.post('/api/repos', (req, res) => {
    const { name, description, owner_id, is_private } = req.body;
    const query = `INSERT INTO repositories (name, description, owner_id, is_private) VALUES (?, ?, ?, ?)`;
    db.run(query, [name, description, owner_id || 1, is_private ? 1 : 0], function(err) {
        if (err) {
            res.status(500).json({ error: err.message });
            return;
        }
        res.json({ id: this.lastID, message: 'Repository created successfully.' });
    });
});

app.get('/api/stats', (req, res) => {
    db.get(`SELECT COUNT(*) as total_repos FROM repositories`, (err, repoRow) => {
        db.get(`SELECT COUNT(*) as total_users FROM users`, (err, userRow) => {
            db.get(`SELECT COUNT(*) as total_issues FROM issues`, (err, issueRow) => {
                res.json({
                    repositories: repoRow ? repoRow.total_repos : 0,
                    users: userRow ? userRow.total_users : 0,
                    issues: issueRow ? issueRow.total_issues : 0,
                    active_nodes: 99.9
                });
            });
        });
    });
});

// ==========================================
// FRONTEND INTERFACE ROUTE (Dashboard HTML)
// ==========================================

app.get('/', (req, res) => {
    res.send(`
        <!DOCTYPE html>
        <html lang="pt-BR">
        <head>
            <meta charset="UTF-8">
            <meta name="viewport" content="width=device-width, initial-scale=1.0">
            <title>Neural Raphael Hub - Visão Geral do Aplicativo</title>
            <style>
                :root {
                    --bg-dark-red: #1a0202;
                    --card-dark-red: #2b0505;
                    --border-red: #590d0d;
                    --accent-green: #00ff66;
                    --accent-green-dim: #00b347;
                    --text-main: #e6e6e6;
                    --black-detail: #000000;
                }

                * {
                    box-sizing: border-box;
                    margin: 0;
                    padding: 0;
                    font-family: 'Courier New', Courier, monospace;
                }

                body {
                    background-color: var(--bg-dark-red);
                    color: var(--text-main);
                    min-height: 100vh;
                    display: flex;
                    flex-direction: column;
                }

                header {
                    background-color: var(--black-detail);
                    border-bottom: 2px solid var(--accent-green);
                    padding: 15px 30px;
                    display: flex;
                    justify-content: space-between;
                    align-items: center;
                }

                header h1 {
                    color: var(--accent-green);
                    font-size: 1.5rem;
                    text-shadow: 0 0 10px rgba(0, 255, 102, 0.4);
                }

                nav a {
                    color: var(--text-main);
                    text-decoration: none;
                    margin-left: 20px;
                    font-weight: bold;
                    transition: color 0.3s;
                }

                nav a:hover {
                    color: var(--accent-green);
                }

                .container {
                    max-width: 1200px;
                    margin: 30px auto;
                    padding: 0 20px;
                    flex: 1;
                    width: 100%;
                }

                .dashboard-grid {
                    display: grid;
                    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
                    gap: 20px;
                    margin-bottom: 30px;
                }

                .card {
                    background-color: var(--card-dark-red);
                    border: 1px solid var(--border-red);
                    border-top: 3px solid var(--accent-green);
                    padding: 20px;
                    border-radius: 4px;
                    box-shadow: 0 4px 15px rgba(0, 0, 0, 0.8);
                }

                .card h3 {
                    color: var(--accent-green);
                    font-size: 0.9rem;
                    text-transform: uppercase;
                    margin-bottom: 10px;
                }

                .card .value {
                    font-size: 1.8rem;
                    font-weight: bold;
                    color: var(--text-main);
                }

                .section-title {
                    border-bottom: 1px solid var(--border-red);
                    padding-bottom: 10px;
                    margin-bottom: 20px;
                    color: var(--accent-green);
                    font-size: 1.2rem;
                }

                .repo-list {
                    list-style: none;
                }

                .repo-item {
                    background-color: var(--card-dark-red);
                    border: 1px solid var(--border-red);
                    padding: 15px;
                    margin-bottom: 15px;
                    border-radius: 4px;
                    display: flex;
                    justify-content: space-between;
                    align-items: center;
                }

                .repo-info h4 a {
                    color: var(--accent-green);
                    text-decoration: none;
                }

                .repo-info h4 a:hover {
                    text-decoration: underline;
                }

                .repo-info p {
                    font-size: 0.85rem;
                    color: #b3b3b3;
                    margin-top: 5px;
                }

                .repo-meta {
                    font-size: 0.8rem;
                    color: var(--accent-green-dim);
                }

                footer {
                    background-color: var(--black-detail);
                    border-top: 1px solid var(--border-red);
                    text-align: center;
                    padding: 15px;
                    font-size: 0.8rem;
                    color: var(--accent-green-dim);
                }

                .btn {
                    background-color: var(--black-detail);
                    color: var(--accent-green);
                    border: 1px solid var(--accent-green);
                    padding: 8px 15px;
                    cursor: pointer;
                    font-weight: bold;
                    transition: all 0.3s;
                }

                .btn:hover {
                    background-color: var(--accent-green);
                    color: var(--black-detail);
                }
            </style>
        </head>
        <body>
            <header>
                <h1>⚡ NEURAL RAPHAEL HUB</h1>
                <nav>
                    <a href="/">Visão Geral</a>
                    <a href="#repos">Repositórios</a>
                    <a href="#issues">Issues</a>
                    <a href="#settings">Configurações</a>
                </nav>
            </header>

            <div class="container">
                <div style="display: flex; justify-content: space-between; align-items: center; margin-bottom: 25px;">
                    <h2>Visão Geral do Aplicativo</h2>
                    <button class="btn" onclick="alert('Funcionalidade de criação rápida pronta para o próximo módulo!')">+ Novo Repositório</button>
                </div>

                <div class="dashboard-grid">
                    <div class="card">
                        <h3>Repositórios Totais</h3>
                        <div class="value" id="stat-repos">Carregando...</div>
                    </div>
                    <div class="card">
                        <h3>Desenvolvedores</h3>
                        <div class="value" id="stat-users">Carregando...</div>
                    </div>
                    <div class="card">
                        <h3>Issues Abertas</h3>
                        <div class="value" id="stat-issues">Carregando...</div>
                    </div>
                    <div class="card">
                        <h3>Status do Núcleo</h3>
                        <div class="value" id="stat-nodes" style="color: var(--accent-green);">100% OK</div>
                    </div>
                </div>

                <h3 class="section-title">Repositórios em Destaque</h3>
                <ul class="repo-list" id="repo-list-container">
                    <li class="repo-item">Carregando repositórios...</li>
                </ul>
            </div>

            <footer>
                Neural Raphael Hub &copy; 2026 - Todos os direitos reservados. Sistema Protegido por Criptografia Neural.
            </footer>

            <script>
                // Fetch stats and repositories dynamically
                async function loadDashboardData() {
                    try {
                        const statsRes = await fetch('/api/stats');
                        const stats = await statsRes.json();
                        document.getElementById('stat-repos').innerText = stats.repositories;
                        document.getElementById('stat-users').innerText = stats.users;
                        document.getElementById('stat-issues').innerText = stats.issues;

                        const reposRes = await fetch('/api/repos');
                        const reposData = await reposRes.json();
                        const container = document.getElementById('repo-list-container');
                        
                        if (reposData.repositories.length === 0) {
                            container.innerHTML = '<li class="repo-item">Nenhum repositório encontrado.</li>';
                            return;
                        }

                        container.innerHTML = reposData.repositories.map(repo => \`
                            <li class="repo-item">
                                <div class="repo-info">
                                    <h4><a href="#">\${repo.owner_name} / \${repo.name}</a></h4>
                                    <p>\${repo.description || 'Sem descrição cadastrada.'}</p>
                                </div>
                                <div class="repo-meta">
                                    ★ \${repo.stars} &nbsp;|&nbsp; ⑂ \${repo.forks}
                                </div>
                            </li>
                        \`).join('');
                    } catch (err) {
                        console.error('Erro ao carregar dados do painel:', err);
                    }
                }

                loadDashboardData();
            </script>
        </body>
        </html>
    `);
});

// Start Server
app.listen(PORT, () => {
    console.log(\`Neural Raphael Hub server running on port \${PORT}\`);
});
