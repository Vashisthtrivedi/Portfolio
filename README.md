
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>VT | Transformation Media</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@300;500;700&family=JetBrains+Mono:wght@400;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --accent: #8b5cf6;
            --bg: #020617;
        }

        body {
            background-color: var(--bg);
            color: #f8fafc;
            font-family: 'Space Grotesk', sans-serif;
            overflow-x: hidden;
        }

        /* Futuristic Animated Background */
        .mesh-bg {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: -1;
            background: 
                radial-gradient(at 0% 0%, rgba(139, 92, 246, 0.15) 0px, transparent 50%),
                radial-gradient(at 100% 100%, rgba(30, 58, 138, 0.2) 0px, transparent 50%);
            animation: meshMove 20s ease-in-out infinite alternate;
        }

        @keyframes meshMove {
            0% { transform: scale(1); }
            100% { transform: scale(1.1); }
        }

        /* Scanline Effect */
        body::after {
            content: " ";
            display: block;
            position: fixed;
            top: 0;
            left: 0;
            bottom: 0;
            right: 0;
            background: linear-gradient(rgba(18, 16, 16, 0) 50%, rgba(0, 0, 0, 0.1) 50%), 
                        linear-gradient(90deg, rgba(255, 0, 0, 0.02), rgba(0, 255, 0, 0.01), rgba(0, 0, 255, 0.02));
            z-index: 100;
            background-size: 100% 4px, 3px 100%;
            pointer-events: none;
        }

        .cyber-card {
            background: rgba(15, 23, 42, 0.6);
            backdrop-filter: blur(20px);
            border: 1px solid rgba(255, 255, 255, 0.05);
            position: relative;
            transition: all 0.4s cubic-bezier(0.23, 1, 0.32, 1);
        }

        .cyber-card:hover {
            border-color: var(--accent);
            background: rgba(139, 92, 246, 0.1);
            transform: translateX(8px);
            box-shadow: -5px 0 20px rgba(139, 92, 246, 0.2);
        }

        .cyber-card::before {
            content: '';
            position: absolute;
            left: 0;
            top: 0;
            height: 100%;
            width: 2px;
            background: var(--accent);
            transform: scaleY(0);
            transition: transform 0.3s ease;
        }

        .cyber-card:hover::before {
            transform: scaleY(1);
        }

        .mono {
            font-family: 'JetBrains Mono', monospace;
        }

        .glitch-text {
            text-shadow: 0.05em 0 0 rgba(255, 0, 80, 0.75),
                        -0.025em -0.05em 0 rgba(0, 255, 200, 0.75);
            animation: glitch 2s infinite;
        }

        @keyframes glitch {
            0% { text-shadow: 1px 0 0 #ff0050, -1px 0 0 #00ffc8; }
            2% { text-shadow: 3px 0 0 #ff0050, -3px 0 0 #00ffc8; }
            4% { text-shadow: 1px 0 0 #ff0050, -1px 0 0 #00ffc8; }
            100% { text-shadow: 1px 0 0 #ff0050, -1px 0 0 #00ffc8; }
        }

        .category-header {
            border-left: 2px solid var(--accent);
            padding-left: 1rem;
            margin: 3rem 0 1rem 0;
        }

        .status-dot {
            width: 6px;
            height: 6px;
            background: #22c55e;
            border-radius: 50%;
            display: inline-block;
            box-shadow: 0 0 10px #22c55e;
            margin-right: 8px;
        }
    </style>
</head>
<body class="flex flex-col items-center py-16 px-6">
    <div class="mesh-bg"></div>

    <!-- Header Section -->
    <header class="flex flex-col items-center mb-16 text-center">
        <div class="relative mb-6">
            <div class="absolute -inset-1 bg-gradient-to-r from-purple-600 to-blue-600 rounded-full blur opacity-75 animate-pulse"></div>
            <img src="https://ui-avatars.com/api/?name=Vashisth+Trivedi&background=020617&color=8b5cf6&size=128" 
                 class="relative w-28 h-28 rounded-full border-2 border-white/10 grayscale hover:grayscale-0 transition-all duration-500">
        </div>
        
        <h1 class="text-4xl font-bold tracking-tighter mb-2 glitch-text">VASHISTH TRIVEDI</h1>
        <div class="mono text-[10px] text-purple-400 tracking-[0.4em] uppercase font-bold mb-4">
            System.Status: <span class="text-emerald-400">Online</span> // ID: VT-2026
        </div>
        <p class="text-slate-500 text-sm max-w-xs font-light">Transformation through advanced digital media & visual storytelling.</p>
    </header>

    <main class="w-full max-w-md space-y-4">
        
        <!-- CBC Section -->
        <div class="category-header">
            <h2 class="mono text-[11px] font-bold text-slate-400 tracking-widest uppercase">/CBC Highlights Project</h2>
        </div>
        
        <a href="https://www.youtube.com/watch?v=h1bbwAwPPFI" target="_blank" class="cyber-card flex items-center p-4 rounded-lg group">
            <div class="flex-grow">
                <div class="flex items-center text-[10px] text-purple-500 mono mb-1">
                    <span class="status-dot"></span> CBC.NEWS_PROD
                </div>
                <p class="font-bold text-slate-200 group-hover:text-white">Iqaluit Girls Hockey</p>
            </div>
            <span class="mono text-[10px] text-slate-600">01</span>
        </a>

        <a href="https://www.youtube.com/watch?v=y7lXbQFy-3w" target="_blank" class="cyber-card flex items-center p-4 rounded-lg group">
            <div class="flex-grow">
                <div class="flex items-center text-[10px] text-purple-500 mono mb-1">
                    <span class="status-dot"></span> CBC.COMMUNITY
                </div>
                <p class="font-bold text-slate-200 group-hover:text-white">Saskatchewan Local Stories</p>
            </div>
            <span class="mono text-[10px] text-slate-600">02</span>
        </a>

        <a href="https://www.youtube.com/watch?v=2_8Cade2Yg8" target="_blank" class="cyber-card flex items-center p-4 rounded-lg group">
            <div class="flex-grow">
                <p class="font-bold text-slate-200 group-hover:text-white">Just Bins </p>
            </div>
            <span class="mono text-[10px] text-slate-600">03</span>
        </a>

        <a href="https://www.youtube.com/watch?v=IxD6LyKJKSw" target="_blank" class="cyber-card flex items-center p-4 rounded-lg group">
            <div class="flex-grow">
                <p class="font-bold text-slate-200 group-hover:text-white">Big River News</p>
            </div>
            <span class="mono text-[10px] text-slate-600">04</span>
        </a>

        <a href="https://youtu.be/388BuSc71wI" target="_blank" class="cyber-card flex items-center p-4 rounded-lg group">
            <div class="flex-grow">
                <p class="font-bold text-slate-200 group-hover:text-white">History of Northern Sask</p>
            </div>
            <span class="mono text-[10px] text-slate-600">05</span>
        </a>

        <a href="https://www.youtube.com/watch?v=tvd6_KyhwEE" target="_blank" class="cyber-card flex items-center p-4 rounded-lg group">
            <div class="flex-grow">
                <p class="font-bold text-slate-200 group-hover:text-white text-red-400">Immigration Scam Investigation</p>
            </div>
            <span class="mono text-[10px] text-slate-600">06</span>
        </a>

        <a href="https://www.youtube.com/watch?v=iPJMa83qPfQ" target="_blank" class="cyber-card flex items-center p-4 rounded-lg group">
            <div class="flex-grow">
                <p class="font-bold text-slate-200 group-hover:text-white">Regina City Mayor Coverage</p>
            </div>
            <span class="mono text-[10px] text-slate-600">07</span>
        </a>

        <!-- SGI Section -->
        <div class="category-header">
            <h2 class="mono text-[11px] font-bold text-slate-400 tracking-widest uppercase">/SGI- Digital Media Manager</h2>
        </div>

        <a href="https://vimeo.com/790500275" target="_blank" class="cyber-card flex items-center p-4 rounded-lg group">
            <div class="flex-grow">
                <div class="flex items-center text-[10px] text-blue-500 mono mb-1">
                    TRANSFORM_MODULE.V1
                </div>
                <p class="font-bold text-slate-200 group-hover:text-white">Digital Transformation</p>
            </div>
            <span class="mono text-[10px] text-slate-600">VIMEO</span>
        </a>

        <a href="https://vimeo.com/790508023" target="_blank" class="cyber-card flex items-center p-4 rounded-lg group">
            <div class="flex-grow">
                <p class="font-bold text-slate-200 group-hover:text-white">Butler Buyers Insurance</p>
            </div>
            <span class="mono text-[10px] text-slate-600">VIMEO</span>
        </a>

        <a href="https://vimeo.com/791283811" target="_blank" class="cyber-card flex items-center p-4 rounded-lg group">
            <div class="flex-grow">
                <p class="font-bold text-slate-200 group-hover:text-white">E-Inspection Showcase</p>
            </div>
            <span class="mono text-[10px] text-slate-600">VIMEO</span>
        </a>

        <a href="https://vimeo.com/437240696" target="_blank" class="cyber-card flex items-center p-4 rounded-lg group">
            <div class="flex-grow">
                <p class="font-bold text-slate-200 group-hover:text-white">Marketing Creative</p>
            </div>
            <span class="mono text-[10px] text-slate-600">VIMEO</span>
        </a>

        <a href="https://vimeo.com/499659867" target="_blank" class="cyber-card flex items-center p-4 rounded-lg group">
            <div class="flex-grow">
                <p class="font-bold text-slate-200 group-hover:text-white">Community Impact Project</p>
            </div>
            <span class="mono text-[10px] text-slate-600">VIMEO</span>
        </a>

        <a href="https://www.youtube.com/watch?v=cWKeXFl74f0" target="_blank" class="cyber-card flex items-center p-4 rounded-lg group">
            <div class="flex-grow">
                <p class="font-bold text-slate-200 group-hover:text-white">Rural Road Safety (STARS)</p>
            </div>
            <span class="mono text-[10px] text-slate-600">YT</span>
        </a>

        <a href="https://www.youtube.com/watch?v=STkA4IFzbOc" target="_blank" class="cyber-card flex items-center p-4 rounded-lg group">
            <div class="flex-grow">
                <p class="font-bold text-slate-200 group-hover:text-white">SGI FYI Motorcycle</p>
            </div>
            <span class="mono text-[10px] text-slate-600">YT</span>
        </a>

        <!-- Cinema Section -->
        <div class="category-header">
            <h2 class="mono text-[11px] font-bold text-slate-400 tracking-widest uppercase">/India Projects/h2>
        </div>

        <a href="https://www.youtube.com/watch?v=7bOpbHsEeEA" target="_blank" class="cyber-card flex items-center p-4 rounded-lg group">
            <div class="flex-grow">
                <p class="font-bold text-slate-200 group-hover:text-white">Music Video Portfolio</p>
            </div>
            <span class="mono text-[10px] text-emerald-500">IND</span>
        </a>

        <a href="https://www.youtube.com/watch?v=comot2PoYQY" target="_blank" class="cyber-card flex items-center p-4 rounded-lg group">
            <div class="flex-grow">
                <p class="font-bold text-slate-200 group-hover:text-white">Commercial Reels</p>
            </div>
            <span class="mono text-[10px] text-emerald-500">IND</span>
        </a>

        <a href="https://www.youtube.com/watch?v=ey7XGdPC2nw" target="_blank" class="cyber-card flex items-center p-4 rounded-lg group">
            <div class="flex-grow">
                <p class="font-bold text-slate-200 group-hover:text-white">Documentary Work</p>
            </div>
            <span class="mono text-[10px] text-emerald-500">IND</span>
        </a>

        <a href="https://www.youtube.com/watch?v=wuHSD8YVw1A" target="_blank" class="cyber-card flex items-center p-4 rounded-lg group">
            <div class="flex-grow">
                <p class="font-bold text-slate-200 group-hover:text-white italic">Assistant Director Work</p>
            </div>
            <span class="mono text-[10px] text-emerald-500">IND</span>
        </a>

        <!-- NPO Section -->
        <div class="category-header">
            <h2 class="mono text-[11px] font-bold text-slate-400 tracking-widest uppercase">/Non_Profit_Protocol</h2>
        </div>

        <a href="https://www.youtube.com/watch?v=eZqw9Os2FE4" target="_blank" class="cyber-card flex items-center p-4 rounded-lg group">
            <div class="flex-grow">
                <p class="font-bold text-slate-200 group-hover:text-white">Regina Museum Series</p>
            </div>
            <span class="mono text-[10px] text-amber-500">DIR</span>
        </a>

        <a href="https://www.youtube.com/@thecaringplacetcp5890" target="_blank" class="cyber-card flex items-center p-4 rounded-lg group">
            <div class="flex-grow">
                <p class="font-bold text-slate-200 group-hover:text-white">The Caring Place Archive</p>
            </div>
            <span class="mono text-[10px] text-amber-500">ARCH</span>
        </a>

        <!-- Contact Area -->
        <div class="pt-10 flex flex-col items-center">
            <a href="mailto:3vedivashisth@gmail.com" class="w-full bg-white text-black font-black py-4 px-8 rounded-sm hover:bg-purple-500 hover:text-white transition-all duration-300 flex justify-between items-center group">
                <span class="mono text-xs uppercase tracking-widest">Hire Me</span>
                <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 group-hover:translate-x-1 transition-transform" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="3" d="M14 5l7 7m0 0l-7 7m7-7H3"/></svg>
            </a>
        </div>
    </main>

    <footer class="mt-24 pb-12 flex flex-col items-center opacity-40 hover:opacity-100 transition-opacity">
        <div class="flex space-x-8 mb-8">
            <a href="https://www.instagram.com/storywithcamera/" target="_blank" class="mono text-[10px] tracking-widest uppercase hover:text-purple-400 transition-colors">INSTAGRAM</a>
            <a href="https://www.linkedin.com/in/vashisth-trivedi-61369a69/" target="_blank" class="mono text-[10px] tracking-widest uppercase hover:text-purple-400 transition-colors">LINKEDIN</a>
        </div>
        <div class="mono text-[8px] tracking-[0.6em] font-bold">VASHISTH TRIVEDI // END_OF_LINE</div>
    </footer>
</body>
</html>
