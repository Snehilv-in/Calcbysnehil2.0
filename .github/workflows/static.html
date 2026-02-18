<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Solid Blue Calculator</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --bg-dark: #000000;
            --primary-blue: #0055ff;
            --btn-dark-blue: #1a1c23;
            --btn-action-blue: #2d3345;
            --accent-blue: #007bff;
            --font-heavy: "Inter", "system-ui", "-apple-system", sans-serif;
        }

        /* Secondary Solid Theme (Deep Slate) */
        body.theme-alt {
            --primary-blue: #ff9f0a;
            --btn-dark-blue: #1c1c1e;
            --btn-action-blue: #3a3a3c;
            --accent-blue: #ff9f0a;
        }

        body {
            background-color: var(--bg-dark);
            color: white;
            font-family: var(--font-heavy);
            font-weight: 900;
            margin: 0;
            height: 100dvh;
            display: flex;
            flex-direction: column;
            overflow: hidden;
            touch-action: none;
        }

        /* Loading Screen */
        #loadingScreen {
            position: fixed;
            inset: 0;
            background: #000;
            z-index: 9999;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            transition: opacity 0.6s ease, visibility 0.6s;
        }

        .logo-container {
            margin-bottom: 30px; /* Moved further up */
            display: flex;
            justify-content: center;
            align-items: center;
            width: 100px;
            height: 100px;
        }

        .s-logo {
            width: 100%;
            height: 100%;
            fill: none;
            stroke: #ffffff;
            stroke-width: 10; /* Slightly thinner to prevent edge collision */
            stroke-linecap: round;
            stroke-linejoin: round;
            stroke-dasharray: 300;
            stroke-dashoffset: 300;
            /* Subtle controlled radiance */
            filter: drop-shadow(0 0 5px rgba(255, 255, 255, 0.4));
            animation: drawLogo 2s ease forwards, glowPulse 3s ease-in-out infinite alternate;
        }

        @keyframes drawLogo {
            to { stroke-dashoffset: 0; }
        }

        @keyframes glowPulse {
            from { filter: drop-shadow(0 0 3px rgba(255, 255, 255, 0.2)); }
            to { filter: drop-shadow(0 0 8px rgba(255, 255, 255, 0.5)); }
        }

        .loading-bar {
            width: 140px;
            height: 4px;
            background: rgba(255,255,255,0.1);
            border-radius: 10px;
            overflow: hidden;
        }

        .loading-fill {
            height: 100%;
            width: 0%;
            background: var(--primary-blue);
            transition: width 0.3s ease;
        }

        /* Navigation */
        .top-nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 15px 25px;
            height: 70px;
        }

        .nav-icon {
            width: 44px;
            height: 44px;
            background: var(--btn-action-blue);
            border-radius: 12px;
            display: flex;
            justify-content: center;
            align-items: center;
            cursor: pointer;
            transition: transform 0.1s, background 0.2s;
        }

        /* Display */
        .display-area {
            flex-grow: 1;
            display: flex;
            flex-direction: column;
            justify-content: flex-end;
            padding: 20px 30px;
        }

        .expression { 
            color: #555; 
            font-size: 1.4rem; 
            text-align: right; 
            font-weight: 700;
            margin-bottom: 5px;
        }
        
        .result-container {
            display: flex;
            justify-content: flex-end;
            align-items: center; 
            height: 7rem;
        }

        .result-content {
            font-weight: 900;
            white-space: pre;
            line-height: 1;
            letter-spacing: -0.03em;
        }

        .cursor {
            width: 6px;
            background-color: var(--primary-blue);
            margin: 0 2px;
            animation: blink 1s step-end infinite;
            border-radius: 10px;
        }

        @keyframes blink { 50% { opacity: 0; } }

        /* Solid Buttons */
        .controls-area {
            padding: 10px 20px 40px 20px;
            max-width: 450px;
            margin: 0 auto;
            width: 100%;
        }

        .calc-grid {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 14px;
        }

        .solid-btn {
            aspect-ratio: 1/1;
            border-radius: 22px;
            display: flex;
            justify-content: center;
            align-items: center;
            font-size: 1.8rem;
            font-weight: 900;
            cursor: pointer;
            transition: transform 0.1s, filter 0.2s;
            user-select: none;
        }

        .solid-btn:active {
            transform: scale(0.92);
            filter: brightness(1.3);
        }

        .btn-num { background-color: var(--btn-dark-blue); color: white; }
        .btn-action { background-color: var(--btn-action-blue); color: #fff; }
        .btn-primary { background-color: var(--primary-blue); color: white; }

        /* History */
        #historyPanel {
            position: fixed;
            top: 0; left: 0; width: 85%; max-width: 320px; height: 100%;
            background: #111;
            z-index: 110;
            transform: translateX(-101%);
            transition: transform 0.3s ease;
            padding: 80px 25px;
        }

        #historyPanel.open { transform: translateX(0); }

        .overlay {
            position: fixed; inset: 0; background: rgba(0,0,0,0.7); 
            display: none; z-index: 100;
        }
    </style>
</head>
<body class="theme-solid">

    <div id="loadingScreen">
        <div class="logo-container">
            <!-- viewBox adjusted to 120 120 with path centered to prevent cropping -->
            <svg class="s-logo" viewBox="-10 -10 120 120">
                <path d="M75,25 C75,25 30,15 25,40 C20,65 80,65 75,85 C70,105 25,95 25,95" />
            </svg>
        </div>
        <div class="loading-bar"><div id="loadingFill" class="loading-fill"></div></div>
        <div class="mt-8 text-white/20 text-[10px] tracking-[0.4em] font-black uppercase">Gemini &bull; Snehil</div>
    </div>

    <div id="historyPanel">
        <div class="flex justify-between items-center mb-8">
            <h2 class="text-2xl font-black italic">HISTORY</h2>
            <button onclick="clearHistory()" class="text-blue-500 font-black">CLEAR</button>
        </div>
        <div id="historyList" class="space-y-4 overflow-y-auto max-h-[70vh]"></div>
    </div>
    
    <div id="overlay" class="overlay" onclick="toggleHistory()"></div>

    <nav class="top-nav">
        <div class="nav-icon" onclick="toggleHistory()"><i class="fas fa-history"></i></div>
        <div class="text-[12px] tracking-[0.4em] font-black opacity-30 uppercase">Calculator</div>
        <div class="nav-icon" id="themeResetBtn"><i class="fas fa-sync-alt"></i></div>
    </nav>

    <main class="display-area">
        <div id="expression" class="expression"></div>
        <div class="result-container" id="resultArea">
            <div id="displayPrefix" class="result-content"></div>
            <div class="cursor" id="cursor"></div>
            <div id="displaySuffix" class="result-content"></div>
        </div>
    </main>

    <footer class="controls-area">
        <div class="calc-grid" id="buttonGrid">
            <div class="solid-btn btn-action" data-action="clear">AC</div>
            <div class="solid-btn btn-action" data-action="delete"><i class="fas fa-backspace"></i></div>
            <div class="solid-btn btn-action" data-action="operator" data-val="%">%</div>
            <div class="solid-btn btn-primary" data-action="operator" data-val="÷">÷</div>

            <div class="solid-btn btn-num" data-action="num" data-val="7">7</div>
            <div class="solid-btn btn-num" data-action="num" data-val="8">8</div>
            <div class="solid-btn btn-num" data-action="num" data-val="9">9</div>
            <div class="solid-btn btn-primary" data-action="operator" data-val="×">×</div>

            <div class="solid-btn btn-num" data-action="num" data-val="4">4</div>
            <div class="solid-btn btn-num" data-action="num" data-val="5">5</div>
            <div class="solid-btn btn-num" data-action="num" data-val="6">6</div>
            <div class="solid-btn btn-primary" data-action="operator" data-val="-">−</div>

            <div class="solid-btn btn-num" data-action="num" data-val="1">1</div>
            <div class="solid-btn btn-num" data-action="num" data-val="2">2</div>
            <div class="solid-btn btn-num" data-action="num" data-val="3">3</div>
            <div class="solid-btn btn-primary" data-action="operator" data-val="+">+</div>

            <div class="solid-btn btn-num" data-action="toggleSign">±</div>
            <div class="solid-btn btn-num" data-action="num" data-val="0">0</div>
            <div class="solid-btn btn-num" data-action="num" data-val=".">.</div>
            <div class="solid-btn btn-primary" data-action="calculate">=</div>
        </div>
    </footer>

    <script>
        const state = { current: '0', cursorPos: 1, prev: '', op: null, reset: false, history: [] };
        const ui = {
            prefix: document.getElementById('displayPrefix'),
            suffix: document.getElementById('displaySuffix'),
            cursor: document.getElementById('cursor'),
            expr: document.getElementById('expression'),
            history: document.getElementById('historyList'),
            panel: document.getElementById('historyPanel'),
            overlay: document.getElementById('overlay'),
            loadingScreen: document.getElementById('loadingScreen'),
            loadingFill: document.getElementById('loadingFill'),
            themeBtn: document.getElementById('themeResetBtn')
        };

        // Theme & Hold Logic
        let holdTimer, startTime;
        const toggleTheme = () => document.body.classList.toggle('theme-alt');
        const startHold = () => { startTime = Date.now(); holdTimer = setTimeout(toggleTheme, 600); };
        const endHold = () => {
            clearTimeout(holdTimer);
            if (Date.now() - startTime < 600) actions.clear();
        };

        ui.themeBtn.onmousedown = startHold; 
        ui.themeBtn.onmouseup = endHold;
        ui.themeBtn.ontouchstart = (e) => { startHold(); e.preventDefault(); };
        ui.themeBtn.ontouchend = (e) => { endHold(); e.preventDefault(); };

        function render() {
            const raw = state.current;
            ui.prefix.textContent = raw.slice(0, state.cursorPos);
            ui.suffix.textContent = raw.slice(state.cursorPos);
            const size = raw.length > 10 ? 2 : raw.length > 7 ? 3 : 4.5;
            ui.prefix.style.fontSize = ui.suffix.style.fontSize = size + 'rem';
            ui.cursor.style.height = (size * 1.1) + 'rem';
        }

        const actions = {
            num(n) {
                if (state.reset) { state.current = n === '.' ? '0.' : n; state.reset = false; }
                else {
                    if (n === '.' && state.current.includes('.')) return;
                    if (state.current === '0' && n !== '.') state.current = n;
                    else if (state.current.length < 15) state.current += n;
                }
                state.cursorPos = state.current.length;
                render();
            },
            operator(op) {
                if (state.op && !state.reset) actions.calculate();
                state.prev = state.current; state.op = op;
                ui.expr.textContent = `${state.prev} ${op}`;
                state.current = '0'; state.reset = false; state.cursorPos = 1;
                render();
            },
            delete() {
                state.current = state.current.slice(0, -1) || '0';
                state.cursorPos = state.current.length;
                render();
            },
            clear() {
                state.current = '0'; state.cursorPos = 1; state.prev = ''; state.op = null;
                ui.expr.textContent = ''; render();
            },
            toggleSign() {
                state.current = state.current.startsWith('-') ? state.current.slice(1) : '-' + state.current;
                state.cursorPos = state.current.length; render();
            },
            calculate() {
                if (!state.op) return;
                const p = parseFloat(state.prev), c = parseFloat(state.current);
                let res = 0;
                if (state.op === '+') res = p + c;
                if (state.op === '-') res = p - c;
                if (state.op === '×') res = p * c;
                if (state.op === '÷') res = c === 0 ? 'Error' : p / c;
                if (state.op === '%') res = p % c;
                
                const final = res === 'Error' ? 'Error' : parseFloat(res.toPrecision(10)).toString();
                if (final !== 'Error') state.history.unshift({ e: `${state.prev} ${state.op} ${state.current}`, r: final });
                ui.expr.textContent = `${state.prev} ${state.op} ${state.current}`;
                state.current = final; state.op = null; state.reset = true;
                state.cursorPos = state.current.length;
                updateHistoryUI(); render();
            }
        };

        function toggleHistory() {
            const open = ui.panel.classList.toggle('open');
            ui.overlay.style.display = open ? 'block' : 'none';
        }

        function updateHistoryUI() {
            ui.history.innerHTML = state.history.map(h => `
                <div class="text-right border-b border-white/5 pb-3">
                    <div class="text-gray-500 text-xs font-bold">${h.e}</div>
                    <div class="text-blue-500 text-xl font-black italic">${h.r}</div>
                </div>
            `).join('') || '<p class="opacity-20 text-center py-10">NO ENTRIES</p>';
        }

        function clearHistory() {
            state.history = [];
            updateHistoryUI();
        }

        document.getElementById('buttonGrid').onclick = (e) => {
            const btn = e.target.closest('.solid-btn');
            if (btn) actions[btn.dataset.action]?.(btn.dataset.val);
        };

        window.onload = () => {
            let p = 0;
            const iv = setInterval(() => {
                p += 25; ui.loadingFill.style.width = p + '%';
                if (p >= 100) { 
                    clearInterval(iv); 
                    setTimeout(() => { 
                        ui.loadingScreen.style.opacity = 0; 
                        ui.loadingScreen.style.visibility = 'hidden'; 
                    }, 400);
                }
            }, 200);
            render();
            updateHistoryUI();
        };
    </script>
</body>
</html>
