
<html lang="pt-BR">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Neural Raphael Hub</title>
  <!-- Ícones Font Awesome -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css" />
  <style>
    :root {
      --bg-color: #0b0d17;
      --card-bg: #111425;
      --border-color: #1f243d;
      --text-main: #ffffff;
      --text-muted: #8c94a8;
      --accent-purple: #8b5cf6;
      --accent-purple-hover: #7c3aed;
      --pink-gradient: linear-gradient(135deg, #a855f7, #ec4899);
      --banner-bg: linear-gradient(135deg, rgba(30, 20, 60, 0.8), rgba(15, 10, 35, 0.9));
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
      font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen, Ubuntu, Cantarell, sans-serif;
    }

    body {
      background-color: var(--bg-color);
      color: var(--text-main);
      padding: 16px;
      max-width: 600px;
      margin: 0 auto;
    }

    /* Top Bar Header */
    header {
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 12px;
      margin-bottom: 20px;
    }

    .brand {
      display: flex;
      align-items: center;
      gap: 10px;
      font-weight: bold;
      font-size: 1.1rem;
      color: #c084fc;
    }

    .brand-icon {
      background: var(--pink-gradient);
      width: 36px;
      height: 36px;
      border-radius: 8px;
      display: flex;
      align-items: center;
      justify-content: center;
      color: white;
      font-size: 1.1rem;
    }

    .header-inputs {
      display: flex;
      align-items: center;
      gap: 8px;
      flex: 1;
      justify-content: flex-end;
    }

    .search-files {
      background-color: var(--card-bg);
      border: 1px solid var(--border-color);
      color: var(--text-muted);
      padding: 8px 12px;
      border-radius: 6px;
      font-size: 0.9rem;
      width: 100%;
      max-width: 160px;
    }

    .icon-btn {
      background-color: var(--card-bg);
      border: 1px solid var(--border-color);
      color: var(--text-main);
      padding: 8px;
      border-radius: 6px;
      cursor: pointer;
      display: flex;
      align-items: center;
      justify-content: center;
    }

    /* Hero Banner */
    .hero-card {
      background: var(--banner-bg);
      border: 1px solid var(--border-color);
      border-radius: 12px;
      padding: 24px 20px;
      margin-bottom: 20px;
      box-shadow: 0 4px 20px rgba(0, 0, 0, 0.4);
    }

    .hero-title {
      font-size: 1.4rem;
      font-weight: 700;
      color: #c084fc;
      line-height: 1.3;
      margin-bottom: 16px;
    }

    .hero-description {
      color: var(--text-muted);
      font-size: 0.95rem;
      line-height: 1.5;
      margin-bottom: 20px;
    }

    .repo-input-group {
      display: flex;
      flex-direction: column;
      gap: 12px;
    }

    .repo-name-input {
      background-color: #0d0f1d;
      border: 1px solid var(--border-color);
      color: var(--text-main);
      padding: 10px 14px;
      border-radius: 6px;
      font-size: 0.95rem;
      outline: none;
    }

    .repo-name-input:focus {
      border-color: var(--accent-purple);
    }

    .action-buttons {
      display: flex;
      gap: 10px;
      flex-wrap: wrap;
    }

    .btn-primary {
      background-color: var(--accent-purple);
      color: white;
      border: none;
      padding: 10px 16px;
      border-radius: 6px;
      font-weight: 600;
      font-size: 0.9rem;
      cursor: pointer;
      display: flex;
      align-items: center;
      gap: 6px;
      transition: background-color 0.2s;
    }

    .btn-primary:hover {
      background-color: var(--accent-purple-hover);
    }

    .btn-secondary {
      background-color: #1a1d36;
      color: var(--text-main);
      border: 1px solid var(--border-color);
      padding: 10px 16px;
      border-radius: 6px;
      font-size: 0.9rem;
      cursor: pointer;
    }

    /* Main Repo Search */
    .main-search-input {
      width: 100%;
      background-color: var(--card-bg);
      border: 1px solid var(--border-color);
      color: var(--text-main);
      padding: 12px 16px;
      border-radius: 8px;
      font-size: 0.95rem;
      margin-bottom: 16px;
      outline: none;
    }

    .main-search-input:focus {
      border-color: var(--accent-purple);
    }

    /* Repositories List */
    .repo-list {
      display: flex;
      flex-direction: column;
      gap: 12px;
    }

    .repo-card {
      background-color: var(--card-bg);
      border: 1px solid var(--border-color);
      border-radius: 8px;
      padding: 16px;
    }

    .repo-header {
      display: flex;
      align-items: center;
      gap: 8px;
      margin-bottom: 10px;
    }

    .repo-user {
      color: #8b5cf6;
      font-weight: 600;
      font-size: 1rem;
    }

    .repo-slash {
      color: var(--text-muted);
    }

    .repo-title {
      color: #ec4899;
      font-weight: 700;
      font-size: 1rem;
    }

    .badge-public {
      background-color: rgba(255, 255, 255, 0.05);
      border: 1px solid var(--border-color);
      color: var(--text-muted);
      font-size: 0.75rem;
      padding: 2px 8px;
      border-radius: 12px;
      margin-left: auto;
    }

    .repo-stats {
      display: flex;
      align-items: center;
      gap: 12px;
      color: var(--text-muted);
      font-size: 0.85rem;
    }

    .repo-stats span {
      display: flex;
      align-items: center;
      gap: 4px;
    }
  </style>
</head>
<body>

  <!-- Top Bar -->
  <header>
    <div class="brand">
      <div class="brand-icon"><i class="fa-solid fa-brain"></i></div>
      <span>Neural Raphael Hub</span>
    </div>
    <div class="header-inputs">
      <input type="text" class="search-files" placeholder="Buscar arquivos" />
      <button class="icon-btn"><i class="fa-regular fa-moon"></i></button>
    </div>
  </header>

  <!-- Hero Banner -->
  <section class="hero-card">
    <h1 class="hero-title">Seus algoritmos e softwares, arquivados.</h1>
    <p class="hero-description">
      Crie repositórios, versione código, abra issues e pull requests, faça forks. Compartilhado com quem usa esta página.
    </p>
    <div class="repo-input-group">
      <input type="text" id="newRepoInput" class="repo-name-input" placeholder="nome-do-repositorio" />
      <div class="action-buttons">
        <button class="btn-primary" onclick="createRepository()">
          + Novo repositório
        </button>
        <button class="btn-secondary">Modelo Neural Raphael</button>
      </div>
    </div>
  </section>

  <!-- Search Repositories -->
  <input 
    type="text" 
    id="filterInput" 
    class="main-search-input" 
    placeholder="Buscar repositórios e código..." 
    oninput="filterRepositories()" 
  />

  <!-- Repository List -->
  <div class="repo-list" id="repoList">
    <!-- Card Inicial 1 -->
    <div class="repo-card">
      <div class="repo-header">
        <span class="repo-user">usuário</span>
        <span class="repo-slash">/</span>
        <span class="repo-title">neural-raphael-hub</span>
        <span class="badge-public">Public</span>
      </div>
      <div class="repo-stats">
        <span><i class="fa-regular fa-star"></i> 0</span>
        <span><i class="fa-solid fa-code-fork"></i> 0</span>
        <span>• 3 commits</span>
        <span>• 2 dias atrás</span>
      </div>
    </div>

    <!-- Card Inicial 2 -->
    <div class="repo-card">
      <div class="repo-header">
        <span class="repo-user">usuário</span>
        <span class="repo-slash">/</span>
        <span class="repo-title">neural-raphael-hub</span>
        <span class="badge-public">Public</span>
      </div>
      <div class="repo-stats">
        <span><i class="fa-regular fa-star"></i> 0</span>
        <span><i class="fa-solid fa-code-fork"></i> 0</span>
        <span>• 3 commits</span>
        <span>• 2 dias atrás</span>
      </div>
    </div>
  </div>

  <script>
    // Função para criar novos repositórios dinamicamente
    function createRepository() {
      const input = document.getElementById('newRepoInput');
      const repoName = input.value.trim();

      if (!repoName) {
        alert('Por favor, digite o nome do repositório!');
        return;
      }

      const repoList = document.getElementById('repoList');
      const newCard = document.createElement('div');
      newCard.className = 'repo-card';
      
      newCard.innerHTML = `
        <div class="repo-header">
          <span class="repo-user">usuário</span>
          <span class="repo-slash">/</span>
          <span class="repo-title">${repoName}</span>
          <span class="badge-public">Public</span>
        </div>
        <div class="repo-stats">
          <span><i class="fa-regular fa-star"></i> 0</span>
          <span><i class="fa-solid fa-code-fork"></i> 0</span>
          <span>• 1 commit</span>
          <span>• Agora mesmo</span>
        </div>
      `;

      // Adiciona o novo repositório no topo da lista
      repoList.prepend(newCard);
      input.value = '';
    }

    // Função para filtrar repositórios da lista
    function filterRepositories() {
      const filterText = document.getElementById('filterInput').value.toLowerCase();
      const cards = document.querySelectorAll('.repo-card');

      cards.forEach(card => {
        const title = card.querySelector('.repo-title').textContent.toLowerCase();
        if (title.includes(filterText)) {
          card.style.display = 'block';
        } else {
          card.style.display = 'none';
        }
      });
    }
  </script>
</body>
</html>
