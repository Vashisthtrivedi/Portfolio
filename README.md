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
