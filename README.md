
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Neural Raphael Hub- Dashboard</title>
    <style>
        /* CSS3 - Estilização Estilo GitHub Dark */
        :root {
            --color-canvas-default: #0d1117;
            --color-canvas-overlay: #161b22;
            --color-border-default: #30363d;
            --color-text-primary: #c9d1d9;
            --color-accent: #58a6ff;
            --color-success: #238636;
        }

        body {
            background-color: var(--color-canvas-default);
            color: var(--color-text-primary);
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, Arial, sans-serif;
            margin: 0;
            overflow-x: hidden;
        }

        #neural-canvas {
            position: fixed;
            top: 0;
            left: 0;
            z-index: -1;
            opacity: 0.4;
        }

        header {
            background-color: var(--color-canvas-overlay);
            padding: 16px 32px;
            border-bottom: 1px solid var(--color-border-default);
            display: flex;
            align-items: center;
            justify-content: space-between;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }

        .card {
            background: var(--color-canvas-overlay);
            border: 1px solid var(--color-border-default);
            border-radius: 6px;
            padding: 24px;
            margin-bottom: 20px;
        }

        .status-badge {
            display: inline-block;
            padding: 2px 10px;
            border-radius: 12px;
            background: var(--color-success);
            font-size: 12px;
            color: white;
        }

        .db-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 20px;
        }

        code {
            background: #000;
            padding: 10px;
            display: block;
            border-radius: 4px;
            color: #7ee787;
            font-family: 'Courier New', Courier, monospace;
            margin-top: 10px;
            white-space: pre-wrap;
        }

        input, button {
            background: #21262d;
            border: 1px solid var(--color-border-default);
            color: white;
            padding: 8px 12px;
            border-radius: 6px;
            margin-top: 10px;
        }

        button {
            background: var(--color-success);
            cursor: pointer;
        }
    </style>
</head>
<body>

    <canvas id="neural-canvas"></canvas>

    <header>
        <div style="font-weight: 600; font-size: 18px;">
            Neural Raphael Hub / <span style="font-weight: 400;">Overview</span>
        </div>
        <div class="status-badge">System Online</div>
    </header>

    <div class="container">
        <!-- Visão Geral -->
        <section class="card">
            <h2>Visão Geral do Aplicativo</h2>
            <p>O <strong>Neural Raphael D.B</strong> é um motor de base de dados híbrido que combina processamento neural com estruturas relacionais de alta performance. Configuração espelhada nos padrões de infraestrutura da GitHub.</p>
            <div class="db-grid">
                <div>
                    <strong>Latência:</strong> 0.02ms <br>
                    <strong>Engine:</strong> C++ Core v2.4 <br>
                    <strong>Scripting:</strong> Python 3.10 Bridge
                </div>
                <div>
                    <strong>Status:</strong> Synced with Repository <br>
                    <strong>ID:</strong> NRDB-9921-X
                </div>
            </div>
        </section>

        <!-- Banco de Dados Interativo (JS) -->
        <section class="card">
            <h3>Gerenciador de Dados (LocalStorage DB)</h3>
            <input type="text" id="dbInput" placeholder="Inserir nova chave de dado...">
            <button onclick="saveData()">Armazenar no DB</button>
            <div id="dbOutput"></div>
        </section>

        <!-- Seção de Código Embutido -->
        <section class="card">
            <h3>Core Logic (C++ & Python Integration)</h3>
            <p>Os blocos abaixo representam o backend contido neste arquivo:</p>
            
            <h4>Python Engine Module:</h4>
            <code id="python-code">
# Python Script para Processamento Neural
def process_neural_data(data):
    print(f"Neural Raphael Hub analisando: {data}")
    return True

if __name__ == "__main__":
    process_neural_data("Handshake")
            </code>

            <h4>C++ Data Layer:</h4>
            <code id="cpp-code">
#include &lt;iostream&gt;
using namespace std;

int main() {
    cout << "Neural Raphael Hub Engine Iniciada" << endl;
    return 0;
}
            </code>
        </section>
    </div>

    <!-- JavaScript - Lógica de Animação Canvas e DB -->
    <script>
        // 1. Canvas 2D - Animação de Rede Neural
        const canvas = document.getElementById('neural-canvas');
        const ctx = canvas.getContext('2d');
        let dots = [];

        function resize() {
            canvas.width = window.innerWidth;
            canvas.height = window.innerHeight;
        }

        window.addEventListener('resize', resize);
        resize();

        for(let i=0; i<80; i++) {
            dots.push({
                x: Math.random() * canvas.width,
                y: Math.random() * canvas.height,
                vx: (Math.random() - 0.5) * 0.5,
                vy: (Math.random() - 0.5) * 0.5
            });
        }

        function draw() {
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            ctx.fillStyle = '#58a6ff';
            ctx.strokeStyle = '#58a6ff';

            dots.forEach(d => {
                d.x += d.vx;
                d.y += d.vy;
                if(d.x < 0 || d.x > canvas.width) d.vx *= -1;
                if(d.y < 0 || d.y > canvas.height) d.vy *= -1;

                ctx.beginPath();
                ctx.arc(d.x, d.y, 2, 0, Math.PI*2);
                ctx.fill();

                dots.forEach(d2 => {
                    let dist = Math.hypot(d.x - d2.x, d.y - d2.y);
                    if(dist < 100) {
                        ctx.globalAlpha = 1 - (dist/100);
                        ctx.beginPath();
                        ctx.moveTo(d.x, d.y);
                        ctx.lineTo(d2.x, d2.y);
                        ctx.stroke();
                        ctx.globalAlpha = 1;
                    }
                });
            });
            requestAnimationFrame(draw);
        }
        draw();

        // 2. Lógica de "Banco de Dados" (JS)
        function saveData() {
            const val = document.getElementById('dbInput').value;
            if(val) {
                localStorage.setItem('NRH_' + Date.now(), val);
                updateDisplay();
                alert('Dado armazenado na Neural Raphael Hub!');
            }
        }

        function updateDisplay() {
            let html = "<ul>";
            for(let i=0; i<localStorage.length; i++){
                let key = localStorage.key(i);
                if(key.startsWith('NRH_')) {
                    html += `<li>${localStorage.getItem(key)}</li>`;
                }
            }
            html += "</ul>";
            document.getElementById('dbOutput').innerHTML = html;
        }
        updateDisplay();
    </script>

    <!-- Metadados de Compilação (Ocultos para o navegador, legíveis por interpretadores) -->
    <!-- 
    PYTHON_START
    import sys
    # Este bloco pode ser lido por um script de extração python
    def core():
        print("Neural Raphael Hub Online")
    PYTHON_END

    CPP_START
    // Este bloco pode ser compilado via g++ se extraído
    #include <vector>
    int main() { return 0; }
    CPP_END
    -->
</body>
</html>
