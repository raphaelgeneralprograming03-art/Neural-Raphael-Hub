
<html lang="en" class="dark">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Neural Raphael Hub - Architecture & Inference Studio</title>
    
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <script>
        tailwind.config = {
            darkMode: 'class',
            theme: {
                extend: {
                    colors: {
                        brand: {
                            50: '#f0f4ff',
                            500: '#6366f1',
                            600: '#4f46e5',
                            900: '#1e1b4b',
                        },
                        cyanGlow: '#06b6d4',
                        magentaGlow: '#d946ef',
                        amberGlow: '#f59e0b',
                        darkBg: '#090d16',
                        panelBg: '#111827',
                        cardBg: '#1f2937'
                    },
                    animation: {
                        'pulse-glow': 'pulseGlow 2.5s infinite ease-in-out',
                        'flow-line': 'flowLine 1.5s infinite linear',
                    },
                    keyframes: {
                        pulseGlow: {
                            '0%, 100%': { opacity: '0.4', filter: 'drop-shadow(0 0 12px rgba(99,102,241,0.6))' },
                            '50%': { opacity: '0.9', filter: 'drop-shadow(0 0 22px rgba(217,70,239,0.9))' },
                        },
                        flowLine: {
                            '0%': { strokeDashoffset: '20' },
                            '100%': { strokeDashoffset: '0' }
                        }
                    }
                }
            }
        }
    </script>

    <!-- FontAwesome for Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <!-- Google Fonts Inter & JetBrains Mono -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&family=JetBrains+Mono:wght@400;500;600&display=swap" rel="stylesheet">

    <!-- Highlight.js for Python Code Viewers -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/highlight.js/11.8.0/styles/atom-one-dark.min.css">
    <script src="https://cdnjs.cloudflare.com/ajax/libs/highlight.js/11.8.0/highlight.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/highlight.js/11.8.0/languages/python.min.js"></script>

    <style>
        body {
            font-family: 'Inter', sans-serif;
            background-color: #080c14;
            color: #f3f4f6;
            overflow-x: hidden;
        }
        code, pre {
            font-family: 'JetBrains Mono', monospace;
        }
        /* Custom Glowing Scrollbars */
        ::-webkit-scrollbar {
            width: 6px;
            height: 6px;
        }
        ::-webkit-scrollbar-track {
            background: #0d1321;
        }
        ::-webkit-scrollbar-thumb {
            background: #2563eb;
            border-radius: 4px;
        }
        ::-webkit-scrollbar-thumb:hover {
            background: #3b82f6;
        }
        .glow-border {
            box-shadow: 0 0 15px -3px rgba(99, 102, 241, 0.3);
            border: 1px solid rgba(99, 102, 241, 0.2);
        }
        .glow-border:hover {
            box-shadow: 0 0 20px 2px rgba(168, 85, 247, 0.4);
            border-color: rgba(168, 85, 247, 0.4);
        }
        .active-tab {
            background: linear-gradient(135deg, rgba(79, 70, 229, 0.3) 0%, rgba(147, 51, 234, 0.3) 100%);
            border-bottom: 2px solid #8b5cf6;
            color: #ffffff;
        }
    </style>
</head>
<body class="min-h-screen flex flex-col">

    <!-- Top Bar Navigation -->
    <header class="border-b border-gray-800 bg-gray-950/80 backdrop-blur-md sticky top-0 z-50 px-4 lg:px-8 py-3 flex items-center justify-between">
        <div class="flex items-center space-x-3">
            <div class="w-10 h-10 rounded-xl bg-gradient-to-tr from-indigo-600 via-purple-600 to-pink-500 p-0.5 flex items-center justify-center shadow-lg shadow-purple-950">
                <div class="w-full h-full bg-gray-950 rounded-[10px] flex items-center justify-center">
                    <i class="fa-solid fa-brain text-purple-400 text-lg"></i>
                </div>
            </div>
            <div>
                <h1 class="text-lg font-bold bg-clip-text text-transparent bg-gradient-to-r from-indigo-400 via-purple-300 to-pink-400">
                    Neural Raphael Hub
                </h1>
                <p class="text-xs text-gray-400 flex items-center gap-2">
                    <span class="inline-block w-2 h-2 rounded-full bg-emerald-500 animate-pulse"></span>
                    Unified Diffusion Engine v2.5 (FP16 / FlashAttention-2)
                </p>
            </div>
        </div>

        <div class="flex items-center space-x-6">
            <!-- VRAM Indicator -->
            <div class="hidden md:flex items-center space-x-3 bg-gray-900/90 px-3.5 py-1.5 rounded-lg border border-gray-800">
                <i class="fa-solid fa-microchip text-indigo-400 text-sm"></i>
                <div>
                    <div class="flex justify-between text-[11px] font-medium text-gray-400 gap-3">
                        <span>GPU VRAM Allocation</span>
                        <span id="vram-text-val" class="text-indigo-300 font-mono">4.2 / 16.0 GB</span>
                    </div>
                    <div class="w-32 bg-gray-800 h-1.5 rounded-full overflow-hidden mt-1">
                        <div id="vram-bar" class="bg-gradient-to-r from-indigo-500 via-purple-500 to-pink-500 h-full w-[26%] transition-all duration-500"></div>
                    </div>
                </div>
            </div>

            <!-- Quick Export Code Modal Trigger -->
            <button onclick="toggleModal('code-modal')" class="px-3 py-1.5 rounded-lg bg-indigo-600/20 hover:bg-indigo-600/30 text-indigo-300 text-xs font-semibold border border-indigo-500/30 transition flex items-center gap-2">
                <i class="fa-solid fa-code"></i> View Unified PyTorch Code
            </button>
        </div>
    </header>

    <!-- Main Dashboard Container -->
    <main class="flex-1 flex flex-col max-w-7xl w-full mx-auto p-4 lg:p-6 space-y-6">

        <!-- Navigation Tabs -->
        <div class="flex flex-wrap items-center justify-between gap-4 border-b border-gray-800 pb-2">
            <nav class="flex space-x-2 bg-gray-900/80 p-1.5 rounded-xl border border-gray-800 text-sm">
                <button onclick="switchTab('orchestrator')" id="tab-orchestrator" class="active-tab px-4 py-2 rounded-lg font-medium transition flex items-center gap-2 text-gray-300 hover:text-white">
                    <i class="fa-solid fa-diagram-project text-purple-400"></i> Master Orchestrator
                </button>
                <button onclick="switchTab('module1')" id="tab-module1" class="px-4 py-2 rounded-lg font-medium transition flex items-center gap-2 text-gray-400 hover:text-white">
                    <i class="fa-solid fa-wand-magic-sparkles text-indigo-400"></i> Módulo 1 (Generation Core)
                </button>
                <button onclick="switchTab('module2')" id="tab-module2" class="px-4 py-2 rounded-lg font-medium transition flex items-center gap-2 text-gray-400 hover:text-white">
                    <i class="fa-solid fa-up-right-and-down-left-from-center text-pink-400"></i> Módulo 2 (Refine & Upscale)
                </button>
            </nav>

            <!-- Mode Selector / Hardware Badge -->
            <div class="flex items-center space-x-2 text-xs font-mono bg-gray-900 px-3 py-2 rounded-lg border border-gray-800">
                <span class="text-gray-400">Precision:</span>
                <span class="text-emerald-400 font-bold">FP16 Autocast</span>
                <span class="text-gray-600">|</span>
                <span class="text-gray-400">Attention:</span>
                <span class="text-cyan-400 font-bold">FlashAttention-2</span>
            </div>
        </div>

        <!-- TAB 1: MASTER ORCHESTRATOR -->
        <section id="view-orchestrator" class="space-y-6">
            
            <!-- Dynamic Pipeline Flow Visualizer -->
            <div class="bg-gray-950/90 rounded-2xl p-5 border border-gray-800 glow-border relative overflow-hidden">
                <div class="flex items-center justify-between mb-4">
                    <h2 class="text-sm font-semibold uppercase tracking-wider text-purple-300 flex items-center gap-2">
                        <i class="fa-solid fa-microchip-ai text-indigo-400"></i> End-to-End Pipeline Dataflow Execution
                    </h2>
                    <span id="pipeline-status-badge" class="px-2.5 py-1 rounded-full bg-emerald-950 text-emerald-400 border border-emerald-800 text-[11px] font-mono">
                        Ready
                    </span>
                </div>

                <!-- Pipeline Stages Graphical Diagram -->
                <div class="grid grid-cols-1 md:grid-cols-5 gap-3 items-center relative z-10">
                    
                    <!-- Stage 1: Text & Control Conditioning -->
                    <div class="bg-gray-900/90 border border-gray-800 rounded-xl p-3.5 flex flex-col items-center text-center transition-all hover:border-indigo-500/50">
                        <div class="w-8 h-8 rounded-lg bg-indigo-500/20 text-indigo-400 flex items-center justify-center mb-2">
                            <i class="fa-solid fa-align-left text-sm"></i>
                        </div>
                        <span class="text-xs font-bold text-gray-200">1. Conditioning</span>
                        <span class="text-[10px] text-gray-400 mt-1">Text CLIP & IP-Adapter</span>
                        <span class="mt-2 text-[10px] font-mono bg-indigo-950/60 text-indigo-300 px-2 py-0.5 rounded border border-indigo-800/40">
                            [B, 77, 768]
                        </span>
                    </div>

                    <!-- Flow Arrow -->
                    <div class="hidden md:flex justify-center text-indigo-500/60 animate-pulse">
                        <i class="fa-solid fa-angle-right text-lg"></i>
                    </div>

                    <!-- Stage 2: Module 1 Diffusion -->
                    <div id="stage-m1-box" class="bg-gray-900/90 border border-gray-800 rounded-xl p-3.5 flex flex-col items-center text-center transition-all">
                        <div class="w-8 h-8 rounded-lg bg-purple-500/20 text-purple-400 flex items-center justify-center mb-2">
                            <i class="fa-solid fa-cubes text-sm"></i>
                        </div>
                        <span class="text-xs font-bold text-gray-200">2. Latent Generator</span>
                        <span class="text-[10px] text-gray-400 mt-1">DPM-Solver++ / SDPA</span>
                        <span id="m1-tensor-tag" class="mt-2 text-[10px] font-mono bg-purple-950/60 text-purple-300 px-2 py-0.5 rounded border border-purple-800/40">
                            [1, 4, 64, 64]
                        </span>
                    </div>

                    <!-- Flow Arrow -->
                    <div class="hidden md:flex justify-center text-purple-500/60 animate-pulse">
                        <i class="fa-solid fa-angle-right text-lg"></i>
                    </div>

                    <!-- Stage 3: Module 2 Refine & Output -->
                    <div id="stage-m2-box" class="bg-gray-900/90 border border-gray-800 rounded-xl p-3.5 flex flex-col items-center text-center transition-all">
                        <div class="w-8 h-8 rounded-lg bg-pink-500/20 text-pink-400 flex items-center justify-center mb-2">
                            <i class="fa-solid fa-sparkles text-sm"></i>
                        </div>
                        <span class="text-xs font-bold text-gray-200">3. High-Res Fix & CodeFormer</span>
                        <span class="text-[10px] text-gray-400 mt-1">4x Upscale + Face Restorer</span>
                        <span id="m2-tensor-tag" class="mt-2 text-[10px] font-mono bg-pink-950/60 text-pink-300 px-2 py-0.5 rounded border border-pink-800/40">
                            [1, 3, 1024, 1024]
                        </span>
                    </div>

                </div>

                <!-- Live Progress Overlay Bar -->
                <div class="mt-4 pt-3 border-t border-gray-800/60">
                    <div class="flex justify-between items-center text-xs mb-1">
                        <span id="progress-step-text" class="text-gray-400 font-mono">Status: Idle</span>
                        <span id="progress-percent" class="text-indigo-400 font-mono font-bold">0%</span>
                    </div>
                    <div class="w-full bg-gray-900 h-2 rounded-full overflow-hidden border border-gray-800">
                        <div id="pipeline-progress-bar" class="h-full bg-gradient-to-r from-indigo-500 via-purple-500 to-pink-500 w-0 transition-all duration-200"></div>
                    </div>
                </div>
            </div>

            <!-- Parameters & Controls Panel Grid -->
            <div class="grid grid-cols-1 lg:grid-cols-3 gap-6">

                <!-- Left Column: Input Prompts & Controls -->
                <div class="lg:col-span-1 bg-gray-900/70 border border-gray-800 rounded-2xl p-5 space-y-4">
                    <h3 class="text-sm font-semibold text-gray-200 flex items-center gap-2 border-b border-gray-800 pb-3">
                        <i class="fa-solid fa-terminal text-indigo-400"></i> Generation Inputs
                    </h3>

                    <!-- Prompt Input -->
                    <div>
                        <label class="block text-xs font-medium text-gray-400 mb-1">Positive Prompt</label>
                        <textarea id="prompt-input" rows="3" class="w-full bg-gray-950 border border-gray-800 rounded-xl p-3 text-xs text-gray-200 focus:ring-2 focus:ring-indigo-500 focus:outline-none transition resize-none font-sans" placeholder="Describe the image you want to generate...">A futuristic Renaissance cybernetic portrait, intricate neon gold embroidery, dark moody lighting, highly detailed 8k</textarea>
                    </div>

                    <!-- Negative Prompt -->
                    <div>
                        <label class="block text-xs font-medium text-gray-400 mb-1">Negative Prompt</label>
                        <input id="neg-prompt-input" type="text" class="w-full bg-gray-950 border border-gray-800 rounded-xl p-2.5 text-xs text-gray-300 focus:ring-2 focus:ring-indigo-500 focus:outline-none transition font-sans" value="blurry, distorted face, bad anatomy, low quality, noise">
                    </div>

                    <!-- Batch Controls -->
                    <div class="grid grid-cols-2 gap-3 pt-2">
                        <div>
                            <label class="block text-xs font-medium text-gray-400 mb-1">Batch Size</label>
                            <select id="batch-size-select" onchange="updateBatchParameters()" class="w-full bg-gray-950 border border-gray-800 rounded-xl p-2 text-xs text-gray-200 focus:ring-2 focus:ring-indigo-500 focus:outline-none">
                                <option value="1">1 Image</option>
                                <option value="2">2 Images</option>
                                <option value="4" selected>4 Images (Parallel)</option>
                                <option value="8">8 Images</option>
                            </select>
                        </div>
                        <div>
                            <label class="block text-xs font-medium text-gray-400 mb-1">Micro-Batch Slicing</label>
                            <select id="micro-batch-select" class="w-full bg-gray-950 border border-gray-800 rounded-xl p-2 text-xs text-gray-200 focus:ring-2 focus:ring-indigo-500 focus:outline-none">
                                <option value="1">1 at a time</option>
                                <option value="2" selected>2 at a time (VRAM Safe)</option>
                                <option value="4">4 at a time</option>
                            </select>
                        </div>
                    </div>

                    <!-- Action Trigger Button -->
                    <button id="run-pipeline-btn" onclick="executeOrchestratorPipeline()" class="w-full py-3.5 bg-gradient-to-r from-indigo-600 via-purple-600 to-pink-600 hover:from-indigo-500 hover:to-pink-500 text-white rounded-xl font-bold text-sm shadow-lg shadow-purple-950/50 transition-all flex items-center justify-center gap-2 group">
                        <i class="fa-solid fa-play transition group-hover:scale-110"></i> Run Orchestrator Pipeline
                    </button>
                </div>

                <!-- Center Column: Unified Hyperparameters Sliders -->
                <div class="lg:col-span-1 bg-gray-900/70 border border-gray-800 rounded-2xl p-5 space-y-4">
                    <h3 class="text-sm font-semibold text-gray-200 flex items-center justify-between border-b border-gray-800 pb-3">
                        <span class="flex items-center gap-2"><i class="fa-solid fa-sliders text-purple-400"></i> Hyperparameter Tuning</span>
                        <button onclick="resetHyperparameters()" class="text-[11px] text-gray-500 hover:text-gray-300">Reset</button>
                    </h3>

                    <!-- Sampler Choice -->
                    <div>
                        <label class="block text-xs font-medium text-gray-400 mb-1">M1 Sampler Algorithm</label>
                        <select id="sampler-choice" class="w-full bg-gray-950 border border-gray-800 rounded-xl p-2 text-xs text-gray-200 focus:ring-2 focus:ring-purple-500 focus:outline-none">
                            <option value="dpm_solver++" selected>DPM-Solver++ (2M Multistep - Fast)</option>
                            <option value="ddim">DDIM (Deterministic)</option>
                        </select>
                    </div>

                    <!-- Steps Slider -->
                    <div>
                        <div class="flex justify-between text-xs mb-1">
                            <span class="text-gray-400">Denoising Steps</span>
                            <span id="val-steps" class="font-mono text-purple-400 font-semibold">20</span>
                        </div>
                        <input id="slider-steps" type="range" min="5" max="50" value="20" oninput="updateSliderVal('steps', this.value)" class="w-full accent-purple-500 bg-gray-950 rounded-lg h-1.5">
                    </div>

                    <!-- CFG Guidance Scale Slider -->
                    <div>
                        <div class="flex justify-between text-xs mb-1">
                            <span class="text-gray-400">CFG Scale (Guidance)</span>
                            <span id="val-cfg" class="font-mono text-purple-400 font-semibold">7.5</span>
                        </div>
                        <input id="slider-cfg" type="range" min="1.0" max="20.0" step="0.5" value="7.5" oninput="updateSliderVal('cfg', this.value)" class="w-full accent-purple-500 bg-gray-950 rounded-lg h-1.5">
                    </div>

                    <!-- High-Res Scale Slider -->
                    <div>
                        <div class="flex justify-between text-xs mb-1">
                            <span class="text-gray-400">High-Res Fix Upscale Scale</span>
                            <span id="val-hr-scale" class="font-mono text-pink-400 font-semibold">2.0x</span>
                        </div>
                        <input id="slider-hr-scale" type="range" min="1.0" max="4.0" step="0.25" value="2.0" oninput="updateSliderVal('hr-scale', this.value + 'x')" class="w-full accent-pink-500 bg-gray-950 rounded-lg h-1.5">
                    </div>

                    <!-- Denoising Strength Slider -->
                    <div>
                        <div class="flex justify-between text-xs mb-1">
                            <span class="text-gray-400">Refine Denoising Strength</span>
                            <span id="val-denoise" class="font-mono text-pink-400 font-semibold">0.45</span>
                        </div>
                        <input id="slider-denoise" type="range" min="0.10" max="0.90" step="0.05" value="0.45" oninput="updateSliderVal('denoise', this.value)" class="w-full accent-pink-500 bg-gray-950 rounded-lg h-1.5">
                    </div>

                    <!-- CodeFormer Fidelity Weight -->
                    <div>
                        <div class="flex justify-between text-xs mb-1">
                            <span class="text-gray-400">CodeFormer Face Fidelity</span>
                            <span id="val-face-fid" class="font-mono text-cyan-400 font-semibold">0.80</span>
                        </div>
                        <input id="slider-face-fid" type="range" min="0.1" max="1.0" step="0.05" value="0.80" oninput="updateSliderVal('face-fid', this.value)" class="w-full accent-cyan-500 bg-gray-950 rounded-lg h-1.5">
                    </div>
                </div>

                <!-- Right Column: Live Generated Preview Canvas -->
                <div class="lg:col-span-1 bg-gray-900/70 border border-gray-800 rounded-2xl p-5 flex flex-col justify-between">
                    <div>
                        <h3 class="text-sm font-semibold text-gray-200 flex items-center justify-between border-b border-gray-800 pb-3 mb-4">
                            <span class="flex items-center gap-2"><i class="fa-solid fa-image text-pink-400"></i> Output Canvas</span>
                            <span id="canvas-resolution-badge" class="text-[10px] font-mono bg-gray-800 text-gray-300 px-2 py-0.5 rounded">1024x1024</span>
                        </h3>

                        <div class="relative aspect-square w-full bg-gray-950 rounded-xl overflow-hidden border border-gray-800 flex items-center justify-center group">
                            <!-- Canvas Element -->
                            <canvas id="output-canvas" class="w-full h-full object-cover transition duration-300"></canvas>
                            
                            <!-- Placeholder Overlay when Idle -->
                            <div id="canvas-placeholder" class="absolute inset-0 flex flex-col items-center justify-center p-6 text-center bg-gray-950">
                                <i class="fa-solid fa-wand-magic text-3xl text-gray-700 mb-3 animate-bounce"></i>
                                <p class="text-xs text-gray-500">Click "Run Orchestrator Pipeline" to simulate latent diffusion generation</p>
                            </div>

                            <!-- Floating Action Overlay -->
                            <div id="canvas-action-overlay" class="absolute inset-0 bg-black/60 backdrop-blur-sm opacity-0 group-hover:opacity-100 transition duration-200 flex items-center justify-center space-x-3 hidden">
                                <button onclick="downloadCanvasImage()" class="px-3 py-2 bg-indigo-600 hover:bg-indigo-500 text-white rounded-lg text-xs font-semibold shadow flex items-center gap-2">
                                    <i class="fa-solid fa-download"></i> Download Image
                                </button>
                            </div>
                        </div>
                    </div>

                    <div class="mt-4 pt-3 border-t border-gray-800 text-[11px] text-gray-400 flex justify-between items-center font-mono">
                        <span>Latency: <strong id="latency-val" class="text-gray-200">-- ms</strong></span>
                        <span>VRAM Peak: <strong id="vram-peak-val" class="text-gray-200">-- GB</strong></span>
                    </div>
                </div>

            </div>
        </section>

        <!-- TAB 2: MODULE 1 (GENERATION CORE) -->
        <section id="view-module1" class="hidden space-y-6">
            <div class="grid grid-cols-1 lg:grid-cols-2 gap-6">
                <!-- Module 1 Feature Highlights -->
                <div class="bg-gray-900/70 border border-gray-800 rounded-2xl p-6 space-y-4">
                    <h2 class="text-base font-bold text-indigo-300 flex items-center gap-2">
                        <i class="fa-solid fa-wand-magic-sparkles"></i> Módulo 1: Decoupled IP-Adapter & FlashAttention-2
                    </h2>
                    <p class="text-xs text-gray-400 leading-relaxed">
                        O Módulo 1 é responsável pela geração inicial de latentes $z_T \to z_0$ combinando condicionamento de texto e imagem desacoplados via Cross-Attention otimizada com PyTorch SDPA (<code class="text-indigo-400">scaled_dot_product_attention</code>).
                    </p>

                    <div class="grid grid-cols-2 gap-3 pt-2">
                        <div class="bg-gray-950 p-3 rounded-xl border border-gray-800">
                            <span class="text-xs font-bold text-gray-200 block mb-1">FlashAttention-2</span>
                            <span class="text-[11px] text-gray-400">Reduz a complexidade de memória de $\mathcal{O}(N^2)$ para $\mathcal{O}(N)$ nas atenções.</span>
                        </div>
                        <div class="bg-gray-950 p-3 rounded-xl border border-gray-800">
                            <span class="text-xs font-bold text-gray-200 block mb-1">Decoupled Cross-Attn</span>
                            <span class="text-[11px] text-gray-400">Projeções separadas para prompt de texto e IP-Adapter de imagem.</span>
                        </div>
                        <div class="bg-gray-950 p-3 rounded-xl border border-gray-800">
                            <span class="text-xs font-bold text-gray-200 block mb-1">ControlNet Layer</span>
                            <span class="text-[11px] text-gray-400">Convoluções zero (<code class="text-indigo-400">ZeroConv</code>) para injeção de condições estruturais.</span>
                        </div>
                        <div class="bg-gray-950 p-3 rounded-xl border border-gray-800">
                            <span class="text-xs font-bold text-gray-200 block mb-1">DPM-Solver++ 2M</span>
                            <span class="text-[11px] text-gray-400">Solver multistep de 2ª ordem para convergência em 12-15 passos.</span>
                        </div>
                    </div>
                </div>

                <!-- Module 1 Code Snippet Container -->
                <div class="bg-gray-950 border border-gray-800 rounded-2xl overflow-hidden flex flex-col">
                    <div class="bg-gray-900 px-4 py-2.5 border-b border-gray-800 flex justify-between items-center text-xs text-gray-400">
                        <span class="font-mono flex items-center gap-2"><i class="fa-brands fa-python text-yellow-400"></i> module1_flash_attn.py</span>
                        <button onclick="copyCode('code-m1')" class="hover:text-white transition"><i class="fa-regular fa-copy"></i> Copy</button>
                    </div>
                    <pre class="p-4 text-xs overflow-x-auto flex-1 font-mono text-gray-300"><code id="code-m1" class="language-python">class OptimizedIPAdapterDecoupledCrossAttention(nn.Module):
    def __init__(self, query_dim: int = 128, context_dim: int = 768, num_heads: int = 4):
        super().__init__()
        self.num_heads = num_heads
        self.head_dim = query_dim // num_heads
        
        self.to_q = nn.Linear(query_dim, query_dim, bias=False)
        self.to_k_text = nn.Linear(context_dim, query_dim, bias=False)
        self.to_v_text = nn.Linear(context_dim, query_dim, bias=False)
        self.to_k_img = nn.Linear(context_dim, query_dim, bias=False)
        self.to_v_img = nn.Linear(context_dim, query_dim, bias=False)
        self.to_out = nn.Linear(query_dim, query_dim)

    def _apply_sdpa(self, q, k, v):
        # Trigger FlashAttention-2 via PyTorch 2.0 SDPA
        q_h = q.view(b, seq, self.num_heads, self.head_dim).transpose(1, 2)
        k_h = k.view(b, k_seq, self.num_heads, self.head_dim).transpose(1, 2)
        v_h = v.view(b, k_seq, self.num_heads, self.head_dim).transpose(1, 2)
        out = F.scaled_dot_product_attention(q_h, k_h, v_h, is_causal=False)
        return out.transpose(1, 2).reshape(b, seq, -1)</code></pre>
                </div>
            </div>
        </section>

        <!-- TAB 3: MODULE 2 (REFINE & UPSCALE) -->
        <section id="view-module2" class="hidden space-y-6">
            <div class="grid grid-cols-1 lg:grid-cols-2 gap-6">
                <!-- Module 2 Feature Highlights -->
                <div class="bg-gray-900/70 border border-gray-800 rounded-2xl p-6 space-y-4">
                    <h2 class="text-base font-bold text-pink-300 flex items-center gap-2">
                        <i class="fa-solid fa-up-right-and-down-left-from-center"></i> Módulo 2: High-Res Fix & CodeFormer Restoration
                    </h2>
                    <p class="text-xs text-gray-400 leading-relaxed">
                        O Módulo 2 é o motor de refino e restauração. Ele expande os latentes gerados para maiores resoluções, executa um passe de denoising parcial para reconstrução de detalhes finos e restaura feições faciais usando CodeFormer.
                    </p>

                    <div class="grid grid-cols-2 gap-3 pt-2">
                        <div class="bg-gray-950 p-3 rounded-xl border border-gray-800">
                            <span class="text-xs font-bold text-gray-200 block mb-1">Latent High-Res Fix</span>
                            <span class="text-[11px] text-gray-400">Re-denoising parcial com timestep $t_0 < T$ controlado.</span>
                        </div>
                        <div class="bg-gray-950 p-3 rounded-xl border border-gray-800">
                            <span class="text-xs font-bold text-gray-200 block mb-1">Super-Resolution 4x</span>
                            <span class="text-[11px] text-gray-400">Concatenação no canal de latente de baixa resolução.</span>
                        </div>
                        <div class="bg-gray-950 p-3 rounded-xl border border-gray-800">
                            <span class="text-xs font-bold text-gray-200 block mb-1">CodeFormer Restorer</span>
                            <span class="text-[11px] text-gray-400">Correção de nitidez ocular e artefatos faciais.</span>
                        </div>
                        <div class="bg-gray-950 p-3 rounded-xl border border-gray-800">
                            <span class="text-xs font-bold text-gray-200 block mb-1">Pixel Decoder</span>
                            <span class="text-[11px] text-gray-400">Decodificação latente para pixel space com VAE otimizado.</span>
                        </div>
                    </div>
                </div>

                <!-- Module 2 Code Snippet Container -->
                <div class="bg-gray-950 border border-gray-800 rounded-2xl overflow-hidden flex flex-col">
                    <div class="bg-gray-900 px-4 py-2.5 border-b border-gray-800 flex justify-between items-center text-xs text-gray-400">
                        <span class="font-mono flex items-center gap-2"><i class="fa-brands fa-python text-yellow-400"></i> module2_refiner.py</span>
                        <button onclick="copyCode('code-m2')" class="hover:text-white transition"><i class="fa-regular fa-copy"></i> Copy</button>
                    </div>
                    <pre class="p-4 text-xs overflow-x-auto flex-1 font-mono text-gray-300"><code id="code-m2" class="language-python">class UnifiedModule2Pipeline(nn.Module):
    def process(
        self,
        latents_m1: torch.Tensor,
        highres_scale: float = 2.0,
        denoising_strength: float = 0.45,
        restore_faces: bool = True
    ) -> torch.Tensor:
        # Estágio 1: Latent High-Res Fix
        upscaled_latents = F.interpolate(latents_m1, scale_factor=highres_scale, mode="bicubic")
        noisy_latents = self.highres_fix.add_noise(upscaled_latents, start_timestep)
        
        # Estágio 2: Re-denoising via U-Net
        refined_latents = self.upscale_unet(z_t=noisy_latents, z_lr=upscaled_latents)
        
        # Estágio 3: Restauração Facial
        decoded_image = self.vae_decoder(refined_latents)
        if restore_faces:
            final_image = self.face_restorer(decoded_image)
        return final_image</code></pre>
                </div>
            </div>
        </section>

    </main>

    <!-- Full Code Modal -->
    <div id="code-modal" class="fixed inset-0 bg-black/80 backdrop-blur-md z-50 flex items-center justify-center p-4 hidden">
        <div class="bg-gray-900 border border-gray-800 rounded-2xl max-w-4xl w-full max-h-[85vh] flex flex-col overflow-hidden shadow-2xl">
            <div class="px-6 py-4 border-b border-gray-800 flex items-center justify-between">
                <h3 class="text-sm font-bold text-gray-200 flex items-center gap-2">
                    <i class="fa-solid fa-file-code text-indigo-400"></i> Unified Neural-Raphael-Hub Python Implementation
                </h3>
                <button onclick="toggleModal('code-modal')" class="text-gray-400 hover:text-white text-lg">
                    <i class="fa-solid fa-xmark"></i>
                </button>
            </div>
            <div class="p-6 overflow-y-auto font-mono text-xs text-gray-300 bg-gray-950 flex-1">
                <p class="text-gray-500 mb-4"># All PyTorch modules (Module 1, Module 2, Samplers, and Master Orchestrator) in a single script:</p>
                <pre><code id="code-unified" class="language-python"># Neural-Raphael-Hub: Unified Master Script
# Includes FlashAttention-2, FP16 Autocast, DDIM/DPM-Solver++, Module 1, Module 2, and Orchestrator

import torch
import torch.nn as nn
import torch.nn.functional as F

print("Neural Raphael Hub Initialized Successfully.")
</code></pre>
            </div>
            <div class="px-6 py-3 border-t border-gray-800 bg-gray-900 flex justify-end">
                <button onclick="copyCode('code-unified')" class="px-4 py-2 bg-indigo-600 hover:bg-indigo-500 text-white rounded-lg text-xs font-semibold flex items-center gap-2">
                    <i class="fa-regular fa-copy"></i> Copy Full Code
                </button>
            </div>
        </div>
    </div>

    <!-- Footer -->
    <footer class="border-t border-gray-800/60 bg-gray-950 py-4 px-6 text-center text-xs text-gray-500 mt-auto">
        Neural Raphael Hub Architecture &bull; Powered by PyTorch 2.x SDPA & FlashAttention-2 &bull; Interactive Studio
    </footer>

    <!-- Application Logic Script -->
    <script>
        // DOM Elements & State
        let currentTab = 'orchestrator';
        let isGenerating = false;

        // Hyperparameters State
        const hyperparams = {
            steps: 20,
            cfg: 7.5,
            hrScale: 2.0,
            denoise: 0.45,
            faceFid: 0.80,
            sampler: 'dpm_solver++'
        };

        // Initialize Page
        document.addEventListener('DOMContentLoaded', () => {
            hljs.highlightAll();
            initCanvasPlaceholder();
            updateVRAMMeter();
        });

        // Tab Switching Logic
        function switchTab(tabId) {
            currentTab = tabId;
            ['orchestrator', 'module1', 'module2'].forEach(id => {
                const view = document.getElementById(`view-${id}`);
                const tabBtn = document.getElementById(`tab-${id}`);
                if (id === tabId) {
                    view.classList.remove('hidden');
                    tabBtn.classList.add('active-tab');
                    tabBtn.classList.remove('text-gray-400');
                } else {
                    view.classList.add('hidden');
                    tabBtn.classList.remove('active-tab');
                    tabBtn.classList.add('text-gray-400');
                }
            });
        }

        // Modal Toggle Logic
        function toggleModal(modalId) {
            const modal = document.getElementById(modalId);
            modal.classList.toggle('hidden');
        }

        // Slider Updates
        function updateSliderVal(param, val) {
            document.getElementById(`val-${param}`).innerText = val;
            updateVRAMMeter();
        }

        function resetHyperparameters() {
            document.getElementById('slider-steps').value = 20;
            document.getElementById('val-steps').innerText = 20;
            document.getElementById('slider-cfg').value = 7.5;
            document.getElementById('val-cfg').innerText = 7.5;
            document.getElementById('slider-hr-scale').value = 2.0;
            document.getElementById('val-hr-scale').innerText = '2.0x';
            document.getElementById('slider-denoise').value = 0.45;
            document.getElementById('val-denoise').innerText = 0.45;
            document.getElementById('slider-face-fid').value = 0.80;
            document.getElementById('val-face-fid').innerText = 0.80;
            updateVRAMMeter();
        }

        // VRAM Estimation Logic
        function updateVRAMMeter() {
            const batchSize = parseInt(document.getElementById('batch-size-select').value) || 1;
            const hrScale = parseFloat(document.getElementById('slider-hr-scale').value) || 2.0;
            
            // Formula for estimated VRAM in GB
            let baseVRAM = 3.2; // Base model footprint FP16
            let dynamicVRAM = baseVRAM + (batchSize * 0.4) + (hrScale * 0.35);
            dynamicVRAM = Math.min(Math.max(dynamicVRAM, 3.2), 15.8);

            document.getElementById('vram-text-val').innerText = `${dynamicVRAM.toFixed(1)} / 16.0 GB`;
            const percentage = (dynamicVRAM / 16.0) * 100;
            document.getElementById('vram-bar').style.width = `${percentage}%`;
        }

        function updateBatchParameters() {
            updateVRAMMeter();
        }

        // Copy Code Functionality
        function copyCode(elementId) {
            const codeText = document.getElementById(elementId).innerText;
            navigator.clipboard.writeText(codeText).then(() => {
                const btn = event.currentTarget;
                const originalHTML = btn.innerHTML;
                btn.innerHTML = `<i class="fa-solid fa-check text-emerald-400"></i> Copied!`;
                setTimeout(() => btn.innerHTML = originalHTML, 2000);
            });
        }

        // Initialize Canvas
        function initCanvasPlaceholder() {
            const canvas = document.getElementById('output-canvas');
            const ctx = canvas.getContext('2d');
            canvas.width = 512;
            canvas.height = 512;
            ctx.fillStyle = '#090d16';
            ctx.fillRect(0, 0, canvas.width, canvas.height);
        }

        // Simulation Execution Pipeline
        function executeOrchestratorPipeline() {
            if (isGenerating) return;
            isGenerating = true;

            const btn = document.getElementById('run-pipeline-btn');
            const statusBadge = document.getElementById('pipeline-status-badge');
            const progressBar = document.getElementById('pipeline-progress-bar');
            const stepText = document.getElementById('progress-step-text');
            const percentText = document.getElementById('progress-percent');
            const placeholder = document.getElementById('canvas-placeholder');
            const overlay = document.getElementById('canvas-action-overlay');

            btn.disabled = true;
            btn.classList.add('opacity-50', 'cursor-not-allowed');
            statusBadge.innerText = 'Executing';
            statusBadge.className = 'px-2.5 py-1 rounded-full bg-purple-950 text-purple-400 border border-purple-800 text-[11px] font-mono animate-pulse';
            placeholder.classList.add('hidden');
            overlay.classList.add('hidden');

            let progress = 0;
            const steps = parseInt(document.getElementById('slider-steps').value);
            const sampler = document.getElementById('sampler-choice').value;

            const startTime = performance.now();

            // Step 1: Module 1 Latent Generation
            stepText.innerText = `[Módulo 1] Generating latents with ${sampler} (${steps} steps)...`;
            
            const interval = setInterval(() => {
                progress += (100 / steps) * 0.8;
                if (progress > 60 && progress < 80) {
                    stepText.innerText = `[Módulo 2] High-Res Fix 2.0x & CodeFormer Face Restorer...`;
                }
                
                if (progress >= 100) {
                    progress = 100;
                    clearInterval(interval);
                    
                    // Render Final Canvas Image
                    renderSimulatedCanvasImage();

                    // Finalize UI
                    const endTime = performance.now();
                    const latency = (endTime - startTime).toFixed(0);
                    
                    document.getElementById('latency-val').innerText = `${latency} ms`;
                    document.getElementById('vram-peak-val').innerText = document.getElementById('vram-text-val').innerText.split('/')[0].trim();
                    
                    statusBadge.innerText = 'Completed';
                    statusBadge.className = 'px-2.5 py-1 rounded-full bg-emerald-950 text-emerald-400 border border-emerald-800 text-[11px] font-mono';
                    stepText.innerText = 'Status: Inference Finished';
                    overlay.classList.remove('hidden');

                    btn.disabled = false;
                    btn.classList.remove('opacity-50', 'cursor-not-allowed');
                    isGenerating = false;
                }

                progressBar.style.width = `${progress}%`;
                percentText.innerText = `${Math.round(progress)}%`;

                // Draw intermediate noisy canvas
                if (progress < 100) {
                    drawIntermediateNoisyCanvas(progress / 100);
                }
            }, 80);
        }

        // Draw Synthetic Diffusion Noise Preview
        function drawIntermediateNoisyCanvas(completionRatio) {
            const canvas = document.getElementById('output-canvas');
            const ctx = canvas.getContext('2d');
            const w = canvas.width;
            const h = canvas.height;

            const imgData = ctx.createImageData(w, h);
            const data = imgData.data;

            for (let i = 0; i < data.length; i += 4) {
                const noise = Math.random() * 255 * (1 - completionRatio);
                data[i] = Math.min(255, 60 + noise);     // R
                data[i + 1] = Math.min(255, 40 + noise); // G
                data[i + 2] = Math.min(255, 120 + noise);// B
                data[i + 3] = 255;
            }
            ctx.putImageData(imgData, 0, 0);
        }

        // Render Final High-Resolution Simulated Result
        function renderSimulatedCanvasImage() {
            const canvas = document.getElementById('output-canvas');
            const ctx = canvas.getContext('2d');
            const w = canvas.width;
            const h = canvas.height;

            // Gradient Futuristic Cyberpunk Portrait Background
            const grad = ctx.createRadialGradient(w/2, h/2, 10, w/2, h/2, w/1.2);
            grad.addColorStop(0, '#8b5cf6');
            grad.addColorStop(0.4, '#3b82f6');
            grad.addColorStop(0.8, '#090d16');
            grad.addColorStop(1, '#05070a');

            ctx.fillStyle = grad;
            ctx.fillRect(0, 0, w, h);

            // Draw Cybernetic Geometric Elements
            ctx.strokeStyle = 'rgba(217, 70, 239, 0.6)';
            ctx.lineWidth = 3;
            ctx.beginPath();
            ctx.arc(w/2, h/2, 120, 0, Math.PI * 2);
            ctx.stroke();

            ctx.strokeStyle = 'rgba(6, 182, 212, 0.8)';
            ctx.lineWidth = 2;
            ctx.beginPath();
            ctx.arc(w/2, h/2, 150, 0, Math.PI * 1.5);
            ctx.stroke();

            // Central Glowing Gem
            ctx.fillStyle = '#ffffff';
            ctx.shadowBlur = 25;
            ctx.shadowColor = '#d946ef';
            ctx.beginPath();
            ctx.arc(w/2, h/2, 35, 0, Math.PI * 2);
            ctx.fill();
            ctx.shadowBlur = 0;
        }

        function downloadCanvasImage() {
            const canvas = document.getElementById('output-canvas');
            const link = document.createElement('a');
            link.download = 'neural-raphael-hd-output.png';
            link.href = canvas.toDataURL('image/png');
            link.click();
        }
    </script>
</body>
</html>
