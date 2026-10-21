# -125
<!DOCTYPE html>
<html lang="zh-CN" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <!-- 微信端视口优化：禁止双指缩放、适配刘海屏与底部安全区 -->
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no, viewport-fit=cover">
    <meta name="format-detection" content="telephone=no">
    <!-- 微信分享卡片 OpenGraph 元信息 -->
    <meta property="og:title" content="🐓恋爱中的战斗鸡 | 甜辣暴击·热血限定汉堡">
    <meta property="og:description" content="本想一拳打爆地球，却不小心对你酥脆心动！点击测试你的专属甜辣战力，抢第二件半价神券！">
    <meta property="og:type" content="website">
    <title>恋爱中的战斗鸡 | 甜辣暴击·微信限定H5</title>
    <!-- 引入 Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>

    <script>
        tailwind.config = {
            theme: {
                extend: {
                    fontFamily: {
                        // 采用微信端 iOS 与 Android 原生高表现力中文字体栈，彻底告别境外字体卡顿
                        display: ['"PingFang SC"', '"Hiragino Sans GB"', '"Microsoft YaHei"', 'system-ui', 'sans-serif'],
                        sans: ['-apple-system', 'BlinkMacSystemFont', '"PingFang SC"', '"Helvetica Neue"', '"Microsoft YaHei"', 'sans-serif'],
                    },
                    colors: {
                        combat: {
                            red: '#FF2A4B',
                            orange: '#FF7A00',
                            yellow: '#FFD600',
                            dark: '#140B1C',
                        },
                        love: {
                            pink: '#FF5E9E',
                            light: '#FFE5F1',
                            purple: '#9D4EDD',
                        },
                        wechat: {
                            green: '#07C160',
                            dark: '#191919'
                        }
                    },
                    boxShadow: {
                        'manga': '6px 6px 0px #140B1C',
                        'manga-sm': '4px 4px 0px #140B1C',
                        'manga-lg': '10px 10px 0px #140B1C',
                        'manga-pink': '6px 6px 0px #FF2A4B',
                        'neon': '0 0 20px rgba(255, 94, 158, 0.7), 0 0 40px rgba(255, 42, 75, 0.4)',
                    }
                }
            }
        }
    </script>

    <style>
        /* 微信浏览器防下拉露底与点击高亮消除 */
        body {
            background-color: #140B1C;
            color: #FFFFFF;
            overflow-x: hidden;
            -webkit-tap-highlight-color: transparent;
            -webkit-touch-callout: none;
            padding-bottom: calc(84px + env(safe-area-inset-bottom));
        }
        .font-display {
            font-weight: 900;
            letter-spacing: 0.02em;
        }
                    },
                    boxShadow: {
                        'manga': '6px 6px 0px #140B1C',
                        'manga-sm': '4px 4px 0px #140B1C',
                        'manga-lg': '10px 10px 0px #140B1C',
                        'manga-pink': '6px 6px 0px #FF2A4B',
                        'neon': '0 0 20px rgba(255, 94, 158, 0.7), 0 0 40px rgba(255, 42, 75, 0.4)',
                    }
                }
            }
        }
    </script>

    <style>
        /* 自定义漫画网点与速度线背景 */
        body {
            background-color: #140B1C;
            color: #FFFFFF;
            overflow-x: hidden;
        }

        .halftone-bg {
            background-image: radial-gradient(rgba(255, 94, 158, 0.16) 2px, transparent 2px),
                              radial-gradient(rgba(255, 122, 0, 0.1) 2px, #140B1C 2px);
            background-size: 24px 24px;
            background-position: 0 0, 12px 12px;
        }

        .manga-speedlines {
            background: repeating-conic-gradient(
                from 0deg,
                rgba(255, 255, 255, 0.03) 0deg 4deg,
                transparent 4deg 12deg
            );
        }

        /* 悬浮动画与心跳动画 */
        @keyframes floatSlow {
            0%, 100% { transform: translateY(0px) rotate(0deg); }
            50% { transform: translateY(-12px) rotate(1.5deg); }
        }
        @keyframes heartBeat {
            0%, 100% { transform: scale(1); }
            15% { transform: scale(1.18); }
            30% { transform: scale(0.95); }
            45% { transform: scale(1.12); }
        }
        @keyframes flameFlicker {
            0%, 100% { transform: scaleY(1) translateY(0); opacity: 0.95; }
            50% { transform: scaleY(1.08) translateY(-4px); opacity: 1; }
        }
        @keyframes marquee {
            0% { transform: translateX(0%); }
            100% { transform: translateX(-50%); }
        }

        .animate-float {
            animation: floatSlow 3.6s ease-in-out infinite;
        }
        .animate-heartbeat {
            animation: heartBeat 1.6s infinite;
        }
        .animate-flame {
            animation: flameFlicker 1.2s ease-in-out infinite;
        }
        .animate-marquee {
            display: flex;
            width: 200%;
            animation: marquee 18s linear infinite;
        }

        /* 汉堡爆炸拆解视图过渡 */
        .burger-layer {
            transition: all 0.55s cubic-bezier(0.34, 1.56, 0.64, 1);
        }
        .exploded .layer-top-bun { transform: translateY(-95px) scale(1.03); }
        .exploded .layer-sauce-pink { transform: translateY(-62px) scale(1.05); }
        .exploded .layer-veggie { transform: translateY(-30px) scale(1.02); }
        .exploded .layer-chicken { transform: translateY(8px) scale(1.08); }
        .exploded .layer-cheese { transform: translateY(48px) scale(1.02); }
        .exploded .layer-bottom-bun { transform: translateY(85px) scale(1.02); }

        .layer-label {
            opacity: 0;
            transform: translateX(-15px);
            transition: all 0.4s ease;
            pointer-events: none;
        }
        .exploded .layer-label {
            opacity: 1;
            transform: translateX(0);
            pointer-events: auto;
        }

        /* 漫画文字描边 */
        .text-stroke-dark {
            -webkit-text-stroke: 2px #140B1C;
            paint-order: stroke fill;
        }
        .text-stroke-thick {
            -webkit-text-stroke: 5px #140B1C;
            paint-order: stroke fill;
        }

        /* 自定义滑块样式 */
        input[type=range] {
            -webkit-appearance: none;
            background: transparent;
        }
        input[type=range]::-webkit-slider-thumb {
            -webkit-appearance: none;
            height: 28px;
            width: 28px;
            border-radius: 50%;
            background: #FFD600;
            border: 3px solid #140B1C;
            box-shadow: 2px 2px 0px #140B1C;
            cursor: pointer;
            margin-top: -10px;
            transition: transform 0.15s ease;
        }
        input[type=range]::-webkit-slider-thumb:hover {
            transform: scale(1.15);
        }
        input[type=range]::-webkit-slider-runnable-track {
            width: 100%;
            height: 10px;
            cursor: pointer;
            border-radius: 999px;
            border: 2px solid #140B1C;
        }

        /* 音乐唱片旋转动画 */
        @keyframes spinSlow {
            from { transform: rotate(0deg); }
            to { transform: rotate(360deg); }
        }
        .animate-spin-music {
            animation: spinSlow 4s linear infinite;
        }
        /* 微信右上角分享手指引导浮动 */
        @keyframes pointUpRight {
            0%, 100% { transform: translate(0, 0); }
            50% { transform: translate(8px, -8px); }
        }
        .animate-share-arrow {
            animation: pointUpRight 1s ease-in-out infinite;
        }
    </style>
</head>
<body class="halftone-bg font-sans selection:bg-love-pink selection:text-white">

    <!-- 微信沉浸式顶部朋友圈热搜通告栏 -->
    <div class="bg-gradient-to-r from-wechat-green/20 via-love-pink/25 to-combat-red/20 border-b border-white/15 px-3 py-1.5 text-[11px] sm:text-xs flex items-center justify-between">
        <div class="flex items-center gap-1.5 truncate">
            <span class="px-1.5 py-0.5 rounded bg-wechat-green text-white font-black text-[10px]">微信专享</span>
            <span class="text-love-light truncate">已有 <strong class="text-combat-yellow">52,890</strong> 对情侣在微信共同拆解这颗汉堡</span>
        </div>
        <button onclick="openWeChatShareGuide()" class="text-combat-yellow font-black shrink-0 flex items-center gap-1 ml-2">
            <span>转发领券</span>
            <span>↗</span>
        </button>
    </div>

    <!-- 顶部街机状态导航栏（含仿微信小程序胶囊按钮） -->
    <header class="sticky top-0 z-40 bg-combat-dark/95 backdrop-blur-md border-b-4 border-love-pink">
        <div class="max-w-7xl mx-auto px-3 sm:px-6 lg:px-8 h-16 sm:h-20 flex items-center justify-between">
            <!-- 品牌 Logo -->
            <a href="#hero" class="flex items-center gap-2.5 group">
                <div class="w-10 h-10 sm:w-12 sm:h-12 rounded-2xl bg-gradient-to-br from-combat-red via-combat-orange to-love-pink border-2 border-white flex items-center justify-center shadow-manga-sm group-hover:rotate-6 transition-transform">
                    <span class="text-xl sm:text-2xl">🐓</span>
                </div>
                <div>
                    <div class="flex items-center gap-1.5">
                        <span class="font-display text-lg sm:text-2xl tracking-wider text-combat-yellow">恋爱中的战斗鸡</span>
                        <span class="bg-love-pink text-white text-[10px] sm:text-xs font-black px-1.5 py-0.5 rounded-full border border-combat-dark animate-pulse">KO!</span>
                    </div>
                    <p class="text-[10px] text-love-light/80">微信限定互动特辑 · 甜辣暴击</p>
                </div>
            </a>

            <!-- 导航链接（桌面端显示） -->
            <nav class="hidden md:flex items-center gap-6 font-bold text-sm">
                <a href="#story" class="hover:text-love-pink transition-colors">📖 恋爱四格</a>
                <a href="#anatomy" class="hover:text-love-pink transition-colors">🍔 6层拆解</a>
                <a href="#customizer" class="hover:text-love-pink transition-colors">🌶️ 甜辣调配</a>
                <a href="#minigame" class="hover:text-love-pink transition-colors">🕹️ 投喂赢券</a>
            </nav>

            <!-- 右侧：H5悬浮音乐按钮 + 仿微信胶囊菜单 -->
            <div class="flex items-center gap-2">
                <!-- 音效唱片开关 -->
                <button id="soundToggleBtn" onclick="toggleAudio()" class="w-9 h-9 rounded-full bg-love-pink/20 border-2 border-love-pink flex items-center justify-center shadow-sm" title="开启/关闭街机合成音效">
                    <span id="soundIcon" class="text-base animate-spin-music">🎵</span>
                </button>

                <!-- 仿微信小程序右上角胶囊 -->
                <div class="flex items-center bg-black/50 border border-white/30 rounded-full px-2.5 py-1 gap-2.5 text-white">
                    <button onclick="openWeChatShareGuide()" class="text-xs font-black hover:text-combat-yellow flex items-center gap-1" title="分享给微信好友">
                        <span>•••</span>
                    </button>
                    <span class="w-[1px] h-3.5 bg-white/30"></span>
                    <button onclick="openPosterModal()" class="text-xs font-black text-combat-yellow flex items-center gap-1" title="生成恋爱战力海报">
                        <span>◎</span>
                    </button>
                </div>
            </div>
        </div>
    </header>

    <!-- 第一屏：热血X恋爱 视觉主广告区 -->
    <section id="hero" class="relative overflow-hidden manga-speedlines pt-6 pb-16 lg:py-20 border-b-4 border-combat-dark">
        <!-- 顶部街机对战血条 HUD -->
        <div class="max-w-6xl mx-auto px-4 mb-8">
            <div class="bg-combat-dark/90 border-4 border-white rounded-2xl p-3 sm:p-4 shadow-manga">
                <div class="grid grid-cols-11 items-center gap-2 sm:gap-4">
                    <!-- 左侧：暴躁战斗力 -->
                    <div class="col-span-5">
                        <div class="flex justify-between items-center text-xs sm:text-sm font-black mb-1">
                            <span class="text-combat-yellow flex items-center gap-1">
                                <i class="fa-solid fa-fire text-combat-red"></i> 铁拳赤焰辣度
                            </span>
                            <span class="text-combat-red">MAX 9999</span>
                        </div>
                        <div class="w-full h-4 sm:h-5 bg-gray-800 rounded-lg p-0.5 border-2 border-white overflow-hidden">
                            <div class="h-full bg-gradient-to-r from-combat-yellow via-combat-orange to-combat-red rounded-sm w-[94%] animate-pulse"></div>
                        </div>
                    </div>

                    <!-- 中间：KO 爱心标志 -->
                    <div class="col-span-1 flex flex-col items-center justify-center">
                        <div class="w-10 h-10 sm:w-12 sm:h-12 rounded-full bg-combat-yellow border-3 border-combat-dark flex items-center justify-center shadow-manga-sm animate-heartbeat">
                            <span class="font-display text-combat-dark font-black text-sm sm:text-lg">VS</span>
                        </div>
                    </div>

                    <!-- 右侧：粉色恋爱值 -->
                    <div class="col-span-5">
                        <div class="flex justify-between items-center text-xs sm:text-sm font-black mb-1">
                            <span class="text-love-pink">OVERFLOW 520%</span>
                            <span class="text-love-light flex items-center gap-1">
                                初恋白桃芝士 <i class="fa-solid fa-heart text-love-pink"></i>
                            </span>
                        </div>
                        <div class="w-full h-4 sm:h-5 bg-gray-800 rounded-lg p-0.5 border-2 border-white overflow-hidden flex justify-end">
                            <div class="h-full bg-gradient-to-l from-love-light via-love-pink to-love-purple rounded-sm w-[98%] animate-pulse"></div>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <!-- 主体内容网格 -->
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 grid grid-cols-1 lg:grid-cols-12 gap-10 items-center">
            <!-- 左侧广告文案与口号 -->
            <div class="lg:col-span-6 space-y-6 text-center lg:text-left z-10">
                <div class="inline-flex items-center gap-2 px-4 py-1.5 rounded-full bg-love-light text-combat-dark font-black text-xs sm:text-sm border-3 border-combat-dark shadow-manga-sm">
                    <span class="px-2 py-0.5 bg-combat-red text-white rounded-full text-xs">2026春季限定</span>
                    <span>全城热恋 · 甜辣双修大作</span>
                </div>

                <h1 class="font-display text-4xl sm:text-6xl lg:text-7xl leading-tight tracking-tight">
                    <span class="block text-combat-yellow text-stroke-dark drop-shadow-[4px_4px_0px_#FF2A4B]">本想一拳打爆地球</span>
                    <span class="block text-white mt-2">却不小心对你</span>
                    <span class="inline-block bg-gradient-to-r from-love-pink via-combat-red to-combat-orange text-white px-4 py-1 rounded-2xl border-4 border-white shadow-manga mt-2 transform -rotate-2">
                        酥脆心动！💘
                    </span>
                </h1>

                <p class="text-base sm:text-lg text-love-light/90 max-w-xl mx-auto lg:mx-0 font-medium leading-relaxed">
                    当<strong class="text-combat-yellow font-black">180°C地狱魔鬼椒脆皮大鸡排</strong>，撞上<strong class="text-love-pink font-black">粉红玫瑰蜜桃瀑布流心芝士</strong>！每一口都是钢铁直男硬汉的铁汉柔情，外层咔滋爆裂，内里温柔拉丝！
                </p>

                <!-- 核心卖点勋章 -->
                <div class="grid grid-cols-3 gap-3 max-w-lg mx-auto lg:mx-0">
                    <div class="bg-white/10 backdrop-blur-sm border-2 border-love-pink/60 rounded-2xl p-3 text-center">
                        <div class="text-2xl font-black text-combat-yellow font-display">195g</div>
                        <div class="text-xs text-love-light mt-0.5">巨无霸整块鸡腿排</div>
                    </div>
                    <div class="bg-white/10 backdrop-blur-sm border-2 border-combat-orange/60 rounded-2xl p-3 text-center">
                        <div class="text-2xl font-black text-love-pink font-display">3重奏</div>
                        <div class="text-xs text-love-light mt-0.5">魔鬼辣×蜜桃甜×芝士香</div>
                    </div>
                    <div class="bg-white/10 backdrop-blur-sm border-2 border-combat-yellow/60 rounded-2xl p-3 text-center">
                        <div class="text-2xl font-black text-green-400 font-display">100%</div>
                        <div class="text-xs text-love-light mt-0.5">现点现炸多汁锁鲜</div>
                    </div>
                </div>

                <!-- 互动行动按钮组 -->
                <div class="flex flex-wrap items-center justify-center lg:justify-start gap-3 sm:gap-4 pt-2">
                    <button onclick="triggerLovePunch()" class="px-6 py-3.5 rounded-2xl bg-combat-yellow hover:bg-yellow-300 text-combat-dark font-black text-base sm:text-lg border-4 border-combat-dark shadow-manga active:translate-y-[1px] transition flex items-center gap-2 group">
                        <span class="text-2xl group-hover:scale-125 transition-transform">🥊</span>
                        <span>释放“恋爱暴击拳”</span>
                    </button>

                    <button onclick="openPosterModal()" class="px-5 py-3.5 rounded-2xl bg-love-pink hover:bg-pink-500 text-white font-black text-base sm:text-lg border-4 border-combat-dark shadow-manga transition flex items-center gap-2">
                        <span>📸</span>
                        <span>生成我的恋爱战力海报</span>
                    </button>
                </div>
            </div>
        </div>
    </section>

    <!-- 第五屏：街机互动小游戏《接住她的心！战斗鸡投喂大作战》 -->
    <section id="minigame" class="py-16 sm:py-20 bg-combat-dark border-t-4 border-white/20">
        <div class="max-w-5xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-8">
                <span class="px-4 py-1 rounded-full bg-green-400 text-combat-dark font-black text-xs border-2 border-combat-dark">
                    ARCADE MINI-GAME · 赢取满减神券
                </span>
                <h2 class="font-display text-3xl sm:text-5xl text-white mt-3">
                    🕹️ 战斗鸡的<span class="text-combat-yellow">恋爱投喂大作战</span>
                </h2>
                <p class="text-love-light/80 text-sm mt-2">
                    左右移动战斗鸡接住掉落的 <strong class="text-love-pink">💘粉红爱心、🍑蜜桃芝士、🍗脆皮鸡排</strong>，避开 <strong class="text-blue-300">🧊冷暴力冰块</strong>！满 100 分即可解锁【立减10元热恋神券】！
                </p>
            </div>

            <!-- 游戏机街机框体 -->
            <div class="bg-gradient-to-b from-love-pink via-combat-red to-combat-orange p-3 sm:p-5 rounded-3xl border-4 border-white shadow-manga-lg">
                <!-- 游戏顶部计分板 -->
                <div class="bg-combat-dark rounded-t-2xl px-4 py-3 flex flex-wrap items-center justify-between gap-2 border-b-2 border-white/20">
                    <div class="flex items-center gap-4">
                        <div class="text-xs sm:text-sm font-black">
                            <span class="text-love-light">心动得分:</span>
                            <span id="gameScore" class="font-display text-2xl text-combat-yellow ml-1">0</span>
                            <span class="text-xs text-white/60">/ 100</span>
                        </div>
                        <div class="text-xs sm:text-sm font-black">
                            <span class="text-love-light">剩余时间:</span>
                            <span id="gameTimer" class="font-display text-2xl text-love-pink ml-1">25</span>s
                        </div>
                    </div>

                    <div class="flex items-center gap-2">
                        <span id="couponStatusBadge" class="px-3 py-1 rounded-full bg-white/10 text-xs font-bold text-love-light">
                            🎁 满100分解锁隐藏优惠码
                        </span>
                        <button id="startGameBtn" onclick="startMiniGame()" class="px-4 py-1.5 rounded-xl bg-combat-yellow text-combat-dark font-black text-xs sm:text-sm border-2 border-white hover:bg-yellow-300 transition">
                            开始挑战 ▶
                        </button>
                    </div>
                </div>

                <!-- 游戏画布容器 -->
                <div id="gameCanvasWrapper" class="relative w-full h-80 sm:h-96 bg-[#1A0E26] rounded-b-2xl overflow-hidden select-none">
                    <canvas id="arcadeCanvas" class="w-full h-full block cursor-ew-resize"></canvas>

                    <!-- 游戏覆盖层（未开始或结束时显示） -->
                    <div id="gameOverlay" class="absolute inset-0 bg-combat-dark/85 backdrop-blur-sm flex flex-col items-center justify-center p-6 text-center z-20">
                        <div class="text-6xl mb-3 animate-bounce">🐓🍔💘</div>
                        <h3 id="overlayTitle" class="font-display text-2xl sm:text-3xl text-combat-yellow mb-2">
                            准备好帮战斗鸡收集恋爱食材了吗？
                        </h3>
                        <p id="overlaySub" class="text-xs sm:text-sm text-love-light/90 max-w-md mb-6">
                            支持鼠标滑动、手指触屏拖动或键盘 ⬅️ ➡️ 方向键操控。25秒内达到100分即刻掉落【¥10元热恋霸王券】！
                        </p>
                        <button onclick="startMiniGame()" class="px-8 py-3.5 rounded-2xl bg-gradient-to-r from-love-pink to-combat-red text-white font-black text-lg border-3 border-white shadow-manga hover:scale-105 transition">
                            立即投币开局 (FREE)
                        </button>
                    </div>
                </div>

                <!-- 移动端虚拟方向键辅助条 -->
                <div class="mt-3 flex sm:hidden items-center justify-between gap-4">
                    <button onmousedown="movePlayerStep(-45)" ontouchstart="movePlayerStep(-45)" class="flex-1 py-3 rounded-xl bg-combat-dark text-white font-black border-2 border-white active:bg-love-pink">
                        ⬅️ 左移闪避
                    </button>
                    <button onmousedown="movePlayerStep(45)" ontouchstart="movePlayerStep(45)" class="flex-1 py-3 rounded-xl bg-combat-dark text-white font-black border-2 border-white active:bg-love-pink">
                        右移接取 ➡️
                    </button>
                </div>
            </div>
        </div>
    </section>

    <!-- 第六屏：限定套餐抢购区 -->
    <section id="combos" class="py-16 sm:py-24 max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="text-center max-w-3xl mx-auto mb-12">
            <span class="px-4 py-1 rounded-full bg-combat-red text-white font-black text-xs border-2 border-white">
                LIMITED TIME COMBOS · 限时暴击套餐
            </span>
            <h2 class="font-display text-3xl sm:text-5xl text-white mt-3">
                一人独享很爽 · <span class="text-love-pink">两人同吃更甜</span>
            </h2>
        </div>

        <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
            <!-- 套餐 1：单人傲娇版 -->
            <div class="bg-white text-combat-dark rounded-3xl border-4 border-combat-dark shadow-manga p-6 flex flex-col justify-between hover:-translate-y-2 transition">
                <div>
                    <div class="flex justify-between items-center mb-4">
                        <span class="px-3 py-1 rounded-full bg-combat-orange/20 text-combat-orange font-black text-xs border border-combat-orange">
                            单人燃魂餐
                        </span>
                        <span class="text-2xl">🥊🍔🍟</span>
                    </div>
                    <h3 class="font-display text-2xl sm:text-3xl text-combat-dark">独狼恋爱暴击单人餐</h3>
                    <p class="text-xs text-gray-600 mt-1">哪怕一个人吃，也要体会谈恋爱般的微甜爆汁！</p>
                    <ul class="mt-4 space-y-2 text-sm font-bold text-gray-800 border-t-2 border-dashed border-gray-200 pt-4">
                        <li class="flex items-center gap-2"><i class="fa-solid fa-check text-combat-red"></i> 恋爱中的战斗鸡汉堡 × 1</li>
                        <li class="flex items-center gap-2"><i class="fa-solid fa-check text-combat-red"></i> 摇摇梅子脆薯条(中) × 1</li>
                        <li class="flex items-center gap-2"><i class="fa-solid fa-check text-combat-red"></i> 冰镇白桃乌龙气泡饮 × 1</li>
                    </ul>
                </div>

                <div class="mt-6 pt-4 border-t-2 border-gray-200 flex items-center justify-between">
                    <div>
                        <span class="text-xs text-gray-400 line-through font-bold">原价 ¥46.0</span>
                        <div class="font-display text-3xl text-combat-red">¥29.9</div>
                    </div>
                    <button onclick="openOrderModal('独狼恋爱暴击单人餐', 29.9)" class="px-5 py-3 rounded-xl bg-combat-dark text-combat-yellow font-black text-sm hover:bg-love-pink hover:text-white transition border-2 border-combat-dark">
                        立即抢购
                    </button>
                </div>
            </div>

            <!-- 套餐 2：双人热恋C位主推 -->
            <div class="bg-gradient-to-b from-love-light to-white text-combat-dark rounded-3xl border-4 border-combat-dark shadow-manga-pink p-6 flex flex-col justify-between transform md:-translate-y-4 relative">
                <div class="absolute -top-4 right-6 bg-combat-red text-white font-black text-xs px-4 py-1.5 rounded-full border-2 border-combat-dark shadow-manga-sm animate-bounce">
                    🔥 销量冠军 · 情侣必点
                </div>
                <div>
                    <div class="flex justify-between items-center mb-4">
                        <span class="px-3 py-1 rounded-full bg-love-pink text-white font-black text-xs">
                            双人CP限定桶
                        </span>
                        <span class="text-2xl">🐓💘🐓</span>
                    </div>
                    <h3 class="font-display text-2xl sm:text-3xl text-combat-red">全能王牌·双人热恋暴击桶</h3>
                    <p class="text-xs text-gray-700 mt-1">随餐附赠限定版【战斗鸡情侣拳击钥匙扣】一对！</p>
                    <ul class="mt-4 space-y-2 text-sm font-bold text-gray-800 border-t-2 border-dashed border-love-pink/40 pt-4">
                        <li class="flex items-center gap-2"><i class="fa-solid fa-heart text-love-pink"></i> 恋爱中的战斗鸡汉堡 × 2</li>
                        <li class="flex items-center gap-2"><i class="fa-solid fa-heart text-love-pink"></i> 爆汁赤焰脆皮琵琶腿 × 2</li>
                        <li class="flex items-center gap-2"><i class="fa-solid fa-heart text-love-pink"></i> 粉红草莓跳跳糖圣代 × 2</li>
                        <li class="flex items-center gap-2"><i class="fa-solid fa-heart text-love-pink"></i> 白桃乌龙气泡饮 × 2 + 周边礼</li>
                    </ul>
                </div>

                <div class="mt-6 pt-4 border-t-2 border-love-pink/40 flex items-center justify-between">
                    <div>
                        <span class="text-xs text-gray-500 line-through font-bold">原价 ¥98.0</span>
                        <div class="font-display text-3xl text-combat-red">¥59.9</div>
                    </div>
                    <button onclick="openOrderModal('全能王牌·双人热恋暴击桶', 59.9)" class="px-6 py-3 rounded-xl bg-gradient-to-r from-combat-red to-love-pink text-white font-black text-sm border-2 border-combat-dark shadow-manga-sm hover:scale-105 transition">
                        热恋秒杀 💘
                    </button>
                </div>
            </div>

            <!-- 套餐 3：宿舍开黑派对桶 -->
            <div class="bg-white text-combat-dark rounded-3xl border-4 border-combat-dark shadow-manga p-6 flex flex-col justify-between hover:-translate-y-2 transition">
                <div>
                    <div class="flex justify-between items-center mb-4">
                        <span class="px-3 py-1 rounded-full bg-purple-100 text-love-purple font-black text-xs border border-love-purple">
                            欢聚派对桶
                        </span>
                        <span class="text-2xl">🎉🍔🍗</span>
                    </div>
                    <h3 class="font-display text-2xl sm:text-3xl text-combat-dark">甜辣全开·四排狂欢全家桶</h3>
                    <p class="text-xs text-gray-600 mt-1">聚会开黑能量站，甜党辣党一桶全部满足！</p>
                    <ul class="mt-4 space-y-2 text-sm font-bold text-gray-800 border-t-2 border-dashed border-gray-200 pt-4">
                        <li class="flex items-center gap-2"><i class="fa-solid fa-star text-combat-yellow"></i> 恋爱中的战斗鸡汉堡 × 4</li>
                        <li class="flex items-center gap-2"><i class="fa-solid fa-star text-combat-yellow"></i> 赤焰鸡翅一对 + 黄金鸡块10块</li>
                        <li class="flex items-center gap-2"><i class="fa-solid fa-star text-combat-yellow"></i> 芝士瀑布大薯条 × 2 + 饮品 × 4</li>
                    </ul>
                </div>

                <div class="mt-6 pt-4 border-t-2 border-gray-200 flex items-center justify-between">
                    <div>
                        <span class="text-xs text-gray-400 line-through font-bold">原价 ¥176.0</span>
                        <div class="font-display text-3xl text-combat-red">¥109.0</div>
                    </div>
                    <button onclick="openOrderModal('甜辣全开·四排狂欢全家桶', 109.0)" class="px-5 py-3 rounded-xl bg-combat-dark text-combat-yellow font-black text-sm hover:bg-love-pink hover:text-white transition border-2 border-combat-dark">
                        立即抢购
                    </button>
                </div>
            </div>
        </div>
    </section>

    <!-- 页脚广告声明 -->
    <footer class="bg-black border-t-4 border-love-pink py-10 text-center text-xs text-white/60">
        <div class="max-w-5xl mx-auto px-4 space-y-3">
            <div class="font-display text-xl text-combat-yellow">🐓 恋爱中的战斗鸡 · FIGHTING ROOSTER IN LOVE</div>
            <p>本创意互动广告页面由 HTML5 + Tailwind CSS + SVG + Tone.js 强力驱动 · 粉色面包胚采用天然红甜菜汁调色，请放心大口热恋！</p>
            <p class="text-white/40">© 2026 恋爱中的战斗鸡创意餐饮实验室 · 祝天下有情人终成吃货眷属</p>
        </div>
    </footer>

    <!-- 下单与优惠券核销弹窗 (替代原生 alert) -->
    <div id="orderModal" class="fixed inset-0 bg-black/80 backdrop-blur-sm z-50 hidden items-center justify-center p-4">
        <div class="bg-white text-combat-dark rounded-3xl border-4 border-combat-dark shadow-manga-pink max-w-md w-full p-6 sm:p-8 relative animate-float" style="animation-duration: 5s;">
            <button onclick="closeOrderModal()" class="absolute top-4 right-4 w-9 h-9 rounded-full bg-gray-100 hover:bg-combat-red hover:text-white font-black border-2 border-combat-dark flex items-center justify-center transition">
                ✕
            </button>

            <div class="flex items-center gap-3 mb-4">
                <span class="text-4xl">🍔💘</span>
                <div>
                    <span class="text-xs font-black text-love-pink uppercase">INSTANT ORDER · 极速出餐</span>
                    <h3 class="font-display text-2xl text-combat-dark">确认你的热恋订单</h3>
                </div>
            </div>

            <div class="bg-love-light/50 rounded-2xl p-4 border-2 border-combat-dark mb-4">
                <div id="modalItemName" class="font-black text-base text-combat-dark">全能王牌·双人热恋暴击桶</div>
                <div class="flex justify-between items-center mt-2">
                    <span class="text-xs text-gray-600 font-bold">套餐金额：</span>
                    <span class="font-display text-2xl text-combat-red">¥<span id="modalItemPrice">59.9</span></span>
                </div>
            <!-- 导航与拆解开关按钮 -->
            <div class="flex flex-col md:flex-row items-center justify-between mb-12 gap-6">
                <div>
                    <span class="inline-block px-4 py-1 rounded-full bg-love-pink text-white font-black text-xs uppercase border-2 border-white mb-2">
                        BURGER ANATOMY SYSTEM
                    </span>
                    <h2 class="font-display text-3xl sm:text-5xl text-white">
                        6层硬核用料 · <span class="text-combat-yellow">全息战力拆解</span>
                    </h2>
                </div>
                <!-- 拆解开关按钮 -->
                <button id="explodeToggleBtn" onclick="toggleBurgerExplode()" class="px-6 py-3.5 rounded-2xl bg-combat-yellow text-combat-dark font-black text-base border-4 border-combat-dark shadow-manga hover:scale-105 transition flex items-center gap-2.5">
                    <span>🔍</span>
                    <span id="explodeBtnText">点击合体【还原完整汉堡】</span>
                </button>
            </div>
                    <h3 class="font-display text-2xl sm:text-3xl text-combat-dark">独狼恋爱暴击单人餐</h3>
                    <p class="text-xs text-gray-600 mt-1">哪怕一个人吃，也要体会谈恋爱般的微甜爆汁！</p>
                    <ul class="mt-4 space-y-2 text-sm font-bold text-gray-800 border-t-2 border-dashed border-gray-200 pt-4">
                        <li class="flex items-center gap-2"><span class="text-combat-red">✔</span> 恋爱中的战斗鸡汉堡 × 1</li>
                        <li class="flex items-center gap-2"><span class="text-combat-red">✔</span> 摇摇梅子脆薯条(中) × 1</li>
                        <li class="flex items-center gap-2"><span class="text-combat-red">✔</span> 冰镇白桃乌龙气泡饮 × 1</li>
                    </ul>
                </div>

                <div class="mt-6 pt-4 border-t-2 border-gray-200 flex items-center justify-between">
                    <div>
                        <span class="text-xs text-gray-400 line-through font-bold">原价 ¥46.0</span>
                        <div class="font-display text-3xl text-combat-red">¥29.9</div>
                    </div>
                    <button onclick="openOrderModal('独狼恋爱暴击单人餐', 29.9)" class="px-5 py-3 rounded-xl bg-combat-dark text-combat-yellow font-black text-sm hover:bg-love-pink hover:text-white transition border-2 border-combat-dark">
                        立即抢购
                    </button>
                </div>
            </div>

            <!-- 套餐 2：双人热恋C位主推 -->
            <div class="bg-gradient-to-b from-love-light to-white text-combat-dark rounded-3xl border-4 border-combat-dark shadow-manga-pink p-6 flex flex-col justify-between transform md:-translate-y-4 relative">
                <div class="absolute -top-4 right-6 bg-combat-red text-white font-black text-xs px-4 py-1.5 rounded-full border-2 border-combat-dark shadow-manga-sm animate-bounce">
                    🔥 销量冠军 · 情侣必点
                </div>
                <div>
                    <div class="flex justify-between items-center mb-4">
                        <span class="px-3 py-1 rounded-full bg-love-pink text-white font-black text-xs">
                            双人CP限定桶
                        </span>
                        <span class="text-2xl">🐓💘🐓</span>
                    </div>
                    <h3 class="font-display text-2xl sm:text-3xl text-combat-red">全能王牌·双人热恋暴击桶</h3>
                    <p class="text-xs text-gray-700 mt-1">随餐附赠限定版【战斗鸡情侣拳击钥匙扣】一对！</p>
                    <ul class="mt-4 space-y-2 text-sm font-bold text-gray-800 border-t-2 border-dashed border-love-pink/40 pt-4">
                        <li class="flex items-center gap-2"><span class="text-love-pink">❤</span> 恋爱中的战斗鸡汉堡 × 2</li>
                        <li class="flex items-center gap-2"><span class="text-love-pink">❤</span> 爆汁赤焰脆皮琵琶腿 × 2</li>
                        <li class="flex items-center gap-2"><span class="text-love-pink">❤</span> 粉红草莓跳跳糖圣代 × 2</li>
                        <li class="flex items-center gap-2"><span class="text-love-pink">❤</span> 白桃乌龙气泡饮 × 2 + 周边礼</li>
                    </ul>
                </div>

                <div class="mt-6 pt-4 border-t-2 border-love-pink/40 flex items-center justify-between">
                    <div>
                        <span class="text-xs text-gray-500 line-through font-bold">原价 ¥98.0</span>
                        <div class="font-display text-3xl text-combat-red">¥59.9</div>
                    </div>
                    <button onclick="openOrderModal('全能王牌·双人热恋暴击桶', 59.9)" class="px-6 py-3 rounded-xl bg-gradient-to-r from-combat-red to-love-pink text-white font-black text-sm border-2 border-combat-dark shadow-manga-sm hover:scale-105 transition">
                        热恋秒杀 💘
                    </button>
                </div>
            </div>

            <!-- 套餐 3：宿舍开黑派对桶 -->
            <div class="bg-white text-combat-dark rounded-3xl border-4 border-combat-dark shadow-manga p-6 flex flex-col justify-between hover:-translate-y-2 transition">
                <div>
                    <div class="flex justify-between items-center mb-4">
                        <span class="px-3 py-1 rounded-full bg-purple-100 text-love-purple font-black text-xs border border-love-purple">
                            欢聚派对桶
                        </span>
                        <span class="text-2xl">🎉🍔🍗</span>
                    </div>
                    <h3 class="font-display text-2xl sm:text-3xl text-combat-dark">甜辣全开·四排狂欢全家桶</h3>
                    <p class="text-xs text-gray-600 mt-1">聚会开黑能量站，甜党辣党一桶全部满足！</p>
                    <ul class="mt-4 space-y-2 text-sm font-bold text-gray-800 border-t-2 border-dashed border-gray-200 pt-4">
                        <li class="flex items-center gap-2"><span class="text-combat-orange">★</span> 恋爱中的战斗鸡汉堡 × 4</li>
                        <li class="flex items-center gap-2"><span class="text-combat-orange">★</span> 赤焰鸡翅一对 + 黄金鸡块10块</li>
                        <li class="flex items-center gap-2"><span class="text-combat-orange">★</span> 芝士瀑布大薯条 × 2 + 饮品 × 4</li>
                    </ul>
                </div>

                <div class="mt-6 pt-4 border-t-2 border-gray-200 flex items-center justify-between">
                    <div>
                        <span class="text-xs text-gray-400 line-through font-bold">原价 ¥176.0</span>
                        <div class="font-display text-3xl text-combat-red">¥109.0</div>
                    </div>
                    <button onclick="openOrderModal('甜辣全开·四排狂欢全家桶', 109.0)" class="px-5 py-3 rounded-xl bg-combat-dark text-combat-yellow font-black text-sm hover:bg-love-pink hover:text-white transition border-2 border-combat-dark">
                        立即抢购
                    </button>
                </div>
            </div>
        </div>
    </section>

    <!-- 页脚广告声明 -->
    <footer class="bg-black border-t-4 border-love-pink py-10 text-center text-xs text-white/60">
        <div class="max-w-5xl mx-auto px-4 space-y-2">
            <div class="font-display text-xl text-combat-yellow">🐓 恋爱中的战斗鸡 · 微信互动H5专享版</div>
            <p>粉色面包胚采用天然红甜菜汁调色，请放心大口热恋！</p>
            <p class="text-white/40">© 2026 恋爱中的战斗鸡创意餐饮实验室 · 支持微信内一键转发分享</p>
        </div>
    </footer>

    <!-- 微信端底部固定悬浮快捷栏 -->
    <div class="fixed bottom-0 left-0 right-0 z-40 bg-combat-dark/95 backdrop-blur-md border-t-3 border-love-pink px-3 py-2.5 shadow-[0_-8px_25px_rgba(0,0,0,0.6)]" style="padding-bottom: calc(10px + env(safe-area-inset-bottom));">
        <div class="max-w-3xl mx-auto flex items-center justify-between gap-2.5">
            <!-- 生成战力海报按钮 -->
            <button onclick="openPosterModal()" class="px-3 py-2.5 rounded-2xl bg-white/10 text-white font-black text-xs border-2 border-white/25 flex items-center gap-1.5 shrink-0 active:scale-95 transition">
                <span class="text-base">📸</span>
                <span>晒战力海报</span>
            </button>

            <!-- 微信召唤好友/对象请客 -->
            <button onclick="openWeChatShareGuide()" class="flex-1 py-2.5 px-3 rounded-2xl bg-wechat-green text-white font-black text-xs sm:text-sm border-2 border-white shadow-manga-sm flex items-center justify-center gap-1.5 active:scale-95 transition">
                <span class="text-base">💬</span>
                <span>召唤TA请我吃 (半价)</span>
            </button>

            <!-- 立即热恋下单 -->
            <button onclick="openOrderModal('全能王牌·双人热恋暴击桶', 59.9)" class="flex-1 py-2.5 px-3 rounded-2xl bg-gradient-to-r from-combat-red to-love-pink text-white font-black text-xs sm:text-sm border-2 border-white shadow-manga-sm flex items-center justify-center gap-1.5 active:scale-95 transition">
                <span class="text-base">🍔</span>
                <span>立即点餐 ¥29.9起</span>
            </button>
        </div>
    </div>

    <!-- 微信右上角转发分享引导蒙层 -->
    <div id="wechatShareOverlay" onclick="closeWeChatShareGuide()" class="fixed inset-0 bg-black/85 backdrop-blur-sm z-50 hidden flex-col items-end p-6 cursor-pointer select-none">
        <!-- 右上角指向箭头 -->
        <div class="mr-3 mt-1 text-right animate-share-arrow">
            <div class="text-5xl">↗️</div>
        </div>
        <div class="mt-4 mr-2 max-w-xs bg-white text-combat-dark rounded-3xl border-4 border-love-pink p-5 shadow-neon text-left">
            <div class="flex items-center gap-2 mb-2">
                <span class="px-2 py-0.5 rounded bg-wechat-green text-white text-xs font-black">微信福利</span>
                <span class="font-display text-lg text-combat-red">邀请TA一起吃甜辣暴击！</span>
            </div>
            <p class="text-xs text-gray-700 leading-relaxed font-bold">
                1. 点击微信右上角 <strong class="bg-gray-200 px-1.5 py-0.5 rounded">•••</strong> 按钮<br>
                2. 选择 <strong class="text-wechat-green">【发送给朋友】</strong> 或 <strong class="text-love-pink">【分享到朋友圈】</strong><br>
                3. 即可与好友共同解锁【双人桶立减¥10特权】！
            </p>
            <div class="mt-3 pt-3 border-t border-dashed border-gray-300 flex items-center justify-between">
                <span class="text-[11px] text-gray-500">或者直接复制暗示文案发给TA：</span>
                <button onclick="event.stopPropagation(); copyWeChatInviteText();" class="px-3 py-1 rounded-lg bg-combat-yellow text-combat-dark font-black text-xs border border-combat-dark">
                    复制投喂暗示
                </button>
            </div>
        </div>
        <p class="w-full text-center text-xs text-white/50 mt-10">（点击任意空白处关闭引导）</p>
    </div>

    <!-- 专属“恋爱战力海报”打卡弹窗 -->
    <div id="posterModal" class="fixed inset-0 bg-black/85 backdrop-blur-sm z-50 hidden items-center justify-center p-4">
        <div class="bg-gradient-to-b from-[#2B103C] to-combat-dark rounded-3xl border-4 border-combat-yellow max-w-sm w-full p-5 relative text-white shadow-neon">
            <button onclick="closePosterModal()" class="absolute top-3 right-3 w-8 h-8 rounded-full bg-white/15 text-white font-black flex items-center justify-center">
                ✕
            </button>

            <div class="text-center">
                <span class="px-2.5 py-0.5 rounded-full bg-love-pink text-white text-[10px] font-black">WECHAT EXCLUSIVE POSTER</span>
                <h3 class="font-display text-2xl text-combat-yellow mt-1">我的甜辣热恋战力卡</h3>
            </div>

            <!-- 海报主体卡片 -->
            <div class="my-4 bg-white text-combat-dark rounded-2xl border-3 border-combat-dark p-4 text-center relative overflow-hidden">
                <div class="text-5xl my-2" id="posterEmoji">🐓💘🔥</div>
                <div class="font-display text-xl text-combat-red" id="posterTitle">【铁汉柔情·甜辣双修宗师】</div>
                <p class="text-xs text-gray-600 mt-1" id="posterDesc">75%赤焰魔鬼辣 × 80%初恋白桃芝士</p>

                <div class="mt-3 pt-3 border-t-2 border-dashed border-gray-200 flex items-center justify-between text-left">
                    <div>
                        <div class="text-[11px] font-black text-combat-dark">恋爱中的战斗鸡 · 2026限定</div>
                        <div class="text-[10px] text-gray-500">截屏保存发给那个想一起吃汉堡的人</div>
                    </div>
                    <!-- 装饰性矢量二维码图案 -->
                    <div class="w-12 h-12 bg-combat-dark text-white rounded-lg p-1 flex flex-col items-center justify-center text-[9px] font-black leading-tight text-center shrink-0">
                        <span>微信</span>
                        <span class="text-combat-yellow">扫码吃</span>
                    </div>
                </div>
            </div>

            <div class="flex gap-2">
                <button onclick="copyWeChatInviteText()" class="flex-1 py-2.5 rounded-xl bg-wechat-green text-white font-black text-xs border-2 border-white">
                    📋 复制秀恩爱文案
                </button>
                <button onclick="closePosterModal(); openWeChatShareGuide();" class="flex-1 py-2.5 rounded-xl bg-love-pink text-white font-black text-xs border-2 border-white">
                    ↗ 转发给微信好友
                </button>
            </div>
        </div>
    </div>

    <!-- 下单与优惠券核销弹窗 -->
    <div id="orderModal" class="fixed inset-0 bg-black/80 backdrop-blur-sm z-50 hidden items-center justify-center p-4">
        <div class="bg-white text-combat-dark rounded-3xl border-4 border-combat-dark shadow-manga-pink max-w-md w-full p-6 sm:p-8 relative">
            <button onclick="closeOrderModal()" class="absolute top-4 right-4 w-9 h-9 rounded-full bg-gray-100 hover:bg-combat-red hover:text-white font-black border-2 border-combat-dark flex items-center justify-center transition">
                ✕
            </button>

            <div class="flex items-center gap-3 mb-4">
                <span class="text-4xl">🍔💘</span>
                <div>
                    <span class="text-xs font-black text-wechat-green uppercase">WECHAT PAY · 微信极速点单</span>
                    <h3 class="font-display text-2xl text-combat-dark">确认你的热恋订单</h3>
                </div>
            </div>

            <div class="bg-love-light/50 rounded-2xl p-4 border-2 border-combat-dark mb-4">
                <div id="modalItemName" class="font-black text-base text-combat-dark">全能王牌·双人热恋暴击桶</div>
                <div class="flex justify-between items-center mt-2">
                    <span class="text-xs text-gray-600 font-bold">微信专享价：</span>
                    <span class="font-display text-2xl text-combat-red">¥<span id="modalItemPrice">59.9</span></span>
                </div>
                <div id="modalDiscountRow" class="hidden justify-between items-center mt-1 text-xs font-black text-green-700">
                    <span>🎁 投喂小游戏通关神券：</span>
                    <span>-¥10.0</span>
                </div>
            </div>

            <!-- 优惠码复制区 -->
            <div class="bg-combat-dark text-white rounded-2xl p-3.5 mb-5 flex items-center justify-between">
                <div>
                    <div class="text-[11px] text-love-light">专属热恋口令码（门店/小程序可用）</div>
                    <div id="promoCodeText" class="font-display text-lg text-combat-yellow tracking-wider">LOVE-KO-520</div>
                </div>
                <button onclick="copyPromoCode()" class="px-3 py-1.5 rounded-xl bg-love-pink hover:bg-pink-500 text-white font-black text-xs border border-white transition">
                    复制口令
                </button>
            </div>

            <button onclick="confirmOrderSubmit()" class="w-full py-3.5 rounded-2xl bg-wechat-green hover:brightness-105 text-white font-black text-base border-3 border-combat-dark shadow-manga-sm transition flex items-center justify-center gap-2">
                <span>⚡</span>
                <span>微信一键下单 · 现炸出餐</span>
            </button>
        </div>
    </div>

    <!-- 全局轻提示消息盒子 -->
    <div id="toastMessage" class="fixed bottom-24 right-4 left-4 sm:left-auto sm:right-6 z-50 transform translate-y-24 opacity-0 transition-all duration-300 pointer-events-none flex justify-center sm:block">
        <div class="bg-combat-dark text-white border-3 border-combat-yellow rounded-2xl px-5 py-3 shadow-manga flex items-center gap-3">
            <span id="toastEmoji" class="text-2xl">💘</span>
            <span id="toastText" class="text-xs sm:text-sm font-bold">提示信息</span>
        </div>
    </div>

    <script>
        /* ==========================================
         * 1. 原生零依赖 Web Audio API 街机合成器（适配微信 WeixinJSBridge）
         * ========================================== */
        let soundEnabled = true;
        let audioCtx = null;

        function getAudioContext() {
            if (!audioCtx) {
                const AudioContextClass = window.AudioContext || window.webkitAudioContext;
                if (AudioContextClass) {
                    audioCtx = new AudioContextClass();
                }
            }
            if (audioCtx && audioCtx.state === 'suspended') {
                audioCtx.resume();
            }
            return audioCtx;
        }

        // 监听微信内置浏览器 WeixinJSBridgeReady 自动解锁音频上下文
        document.addEventListener('WeixinJSBridgeReady', function () {
            getAudioContext();
        }, false);

        // 播放单音辅助函数
        function playToneNote(freq, startTime, duration, type = 'triangle', gainVal = 0.12) {
            const ctx = getAudioContext();
            if (!ctx) return;
            const osc = ctx.createOscillator();
            const gain = ctx.createGain();
            osc.type = type;
            osc.frequency.setValueAtTime(freq, startTime);

            gain.gain.setValueAtTime(gainVal, startTime);
            gain.gain.exponentialRampToValueAtTime(0.001, startTime + duration);

            osc.connect(gain);
            gain.connect(ctx.destination);
            osc.start(startTime);
            osc.stop(startTime + duration);
        }

        function playSoundEffect(type) {
            if (!soundEnabled) return;
            try {
                const ctx = getAudioContext();
                if (!ctx) return;
                const now = ctx.currentTime;

                if (type === 'punch') {
                    // 热血连击+心动上扬琶音
                    playToneNote(261.6, now, 0.09, 'triangle', 0.15);
                    playToneNote(329.6, now + 0.06, 0.09, 'triangle', 0.15);
                    playToneNote(392.0, now + 0.12, 0.12, 'triangle', 0.15);
                    playToneNote(523.2, now + 0.18, 0.22, 'sine', 0.18);
                } else if (type === 'layer') {
                    playToneNote(440.0, now, 0.08, 'sine', 0.12);
                    playToneNote(554.3, now + 0.05, 0.12, 'sine', 0.12);
                } else if (type === 'catchGood') {
                    playToneNote(659.2, now, 0.08, 'triangle', 0.14);
                    playToneNote(880.0, now + 0.06, 0.14, 'triangle', 0.14);
                } else if (type === 'catchBad') {
                    playToneNote(174.6, now, 0.15, 'sawtooth', 0.12);
                    playToneNote(130.8, now + 0.08, 0.2, 'sawtooth', 0.12);
                } else if (type === 'win') {
                    playToneNote(523.2, now, 0.12, 'triangle', 0.16);
                    playToneNote(659.2, now + 0.1, 0.12, 'triangle', 0.16);
                    playToneNote(783.9, now + 0.2, 0.15, 'triangle', 0.16);
                    playToneNote(1046.5, now + 0.3, 0.35, 'triangle', 0.2);
                }
            } catch (err) {
                // 忽略部分静音环境限制
            }
        }

        function toggleAudio() {
            soundEnabled = !soundEnabled;
            const icon = document.getElementById('soundIcon');
            if (soundEnabled) {
                icon.textContent = '🎵';
                icon.classList.add('animate-spin-music');
                playSoundEffect('layer');
                showToast('🎵 微信街机音效已开启！', '🔊');
            } else {
                icon.textContent = '🔇';
                icon.classList.remove('animate-spin-music');
                showToast('已切换为静音浏览模式', '🔇');
            }
        }

        function playSoundEffect(type) {
            if (!soundEnabled || typeof Tone === 'undefined') return;
            try {
                if (Tone.context.state !== 'running') {
                    Tone.start();
                }
                initAudioIfNeeded();
                if (!synth) return;

                const now = Tone.now();
                if (type === 'punch') {
                    // 热血连击+心动上扬琶音
                    synth.triggerAttackRelease(['C4', 'E4'], '16n', now);
                    synth.triggerAttackRelease(['G4', 'B4'], '16n', now + 0.07);
                    synth.triggerAttackRelease(['C5', 'E5', 'G5'], '8n', now + 0.14);
                } else if (type === 'layer') {
                    synth.triggerAttackRelease(['A4', 'C#5'], '16n', now);
                } else if (type === 'catchGood') {
                    synth.triggerAttackRelease(['E5', 'A5'], '16n', now);
                } else if (type === 'catchBad') {
                    synth.triggerAttackRelease(['F3', 'B2'], '8n', now);
                } else if (type === 'win') {
                    synth.triggerAttackRelease(['C5', 'E5', 'G5'], '16n', now);
                    synth.triggerAttackRelease(['D5', 'F#5', 'A5'], '16n', now + 0.12);
                    synth.triggerAttackRelease(['E5', 'G#5', 'B5'], '4n', now + 0.24);
                }
            } catch (err) {
                // 忽略浏览器自动播放限制异常
            }
        }

        function toggleAudio() {
            soundEnabled = !soundEnabled;
            const icon = document.getElementById('soundIcon');
            const text = document.getElementById('soundText');
            if (soundEnabled) {
                icon.className = 'fa-solid fa-volume-high text-combat-yellow';
                text.textContent = '音效: 开启';
                playSoundEffect('layer');
                showToast('🎵 街机甜辣合成音效已开启！', '🔊');
            } else {
                icon.className = 'fa-solid fa-volume-xmark text-gray-400';
                text.textContent = '音效: 静音';
                showToast('已切换为静音模式', '🔇');
            }
        }

        /* ==========================================
         * 2. 主视觉“恋爱暴击拳”粒子与动效
         * ========================================== */
        const sfxLeftList = ['咔滋！CRUNCH! 🔥', '180°C 爆汁警告！⚡', '铁拳烈焰！🥊', '辣得过瘾！🌶️'];
        const sfxRightList = ['噗通~ DOKI! 💓', '白桃芝士暴击！🍑', '甜度超标 520%！💘', '铁汉柔情~ ✨'];
        let punchCounter = 0;

        function triggerLovePunch() {
            playSoundEffect('punch');
            punchCounter++;

            // 拳套出拳缩放动画
            const leftGlove = document.getElementById('leftGlove');
            const rightGlove = document.getElementById('rightGlove');
            leftGlove.style.transform = 'translate(-15px, -10px) scale(1.12)';
            rightGlove.style.transform = 'translate(15px, -10px) scale(1.12)';
            setTimeout(() => {
                leftGlove.style.transform = '';
                rightGlove.style.transform = '';
            }, 260);

            // 切换漫画拟声词
            document.getElementById('sfxBubbleLeft').textContent = sfxLeftList[punchCounter % sfxLeftList.length];
            document.getElementById('sfxBubbleRight').textContent = sfxRightList[punchCounter % sfxRightList.length];

            // 生成爱心与火焰飞溅粒子
            const container = document.getElementById('heroParticleContainer');
            const emojis = ['💘', '🔥', '🍑', '🥊', '✨', '🍗', '💖'];
            for (let i = 0; i < 10; i++) {
                const span = document.createElement('span');
                span.textContent = emojis[Math.floor(Math.random() * emojis.length)];
                span.className = 'absolute text-2xl sm:text-3xl select-none transition-all duration-700 ease-out';
                span.style.left = '50%';
                span.style.top = '50%';
                container.appendChild(span);

                const angle = (Math.PI * 2 * i) / 10 + (Math.random() * 0.5);
                const distance = 110 + Math.random() * 110;
                const tx = Math.cos(angle) * distance;
                const ty = Math.sin(angle) * distance;

                requestAnimationFrame(() => {
                    span.style.transform = `translate(${tx}px, ${ty}px) scale(1.3) rotate(${Math.random() * 90 - 45}deg)`;
                    span.style.opacity = '0';
                });

                setTimeout(() => span.remove(), 750);
            }
        }

        /* ==========================================
         * 3. 四格漫画分镜点击互动
         * ========================================== */
        const mangaDialogues = {
            1: '🔥【第一幕·孤傲拳王】战斗鸡阿烈：“我浑身裹满喀什魔鬼椒，整个快餐界没人能接住我一记脆皮勾拳！”',
            2: '🍑【第二幕·宿命邂逅】初恋白桃芝士酱：“阿烈先生，你的脆皮虽然滚烫，但闻起来好香呀~”',
            3: '💓【第三幕·化学反应】阿烈满脸通红：“什…什么？！我的魔鬼辣遇到她的蜜桃奶香，竟然变成了神仙甜辣味？！”',
            4: '🍔【第四幕·合体出道】合体宣言：“恋爱中的战斗鸡汉堡正式登场！外酥里嫩，又甜又辣，快来咬一口！”'
        };

        function playMangaPanel(index) {
            playSoundEffect('punch');
            const dialogueEl = document.getElementById('mangaDialogueText');
            dialogueEl.textContent = mangaDialogues[index];
            showToast(`已触发第 0${index} 幕剧场台词！`, '🎬');
        }

        /* ==========================================
         * 4. 汉堡 6 层战力拆解检视器
         * ========================================== */
        const burgerLayersData = [
            {
                badge: '第 01 层 · 颜值担当',
                stats: '松软度 999 · 少女心 100%',
                title: '粉红恋爱云朵甜菜面包胚',
                desc: '绝不使用人工色素！采用天然红甜菜根汁与新西兰黄油低温慢发酵，呈现出令人一见钟情的浪漫粉红色。烘烤后外皮微脆，内里像云朵般松软回弹。',
                spice: 15,
                sweet: 95
            },
            {
                badge: '第 02 层 · 灵魂伴侣',
                stats: '果香度 980 · 治愈力 MAX',
                title: '初恋白桃玫瑰流心芝士酱',
                desc: '真实水蜜桃果肉丁融合重瓣红玫瑰露与浓郁奶油芝士。清甜果香巧妙中和油炸感，每一口都能咬到水润蜜桃颗粒，宛如初恋般悸动！',
                spice: 10,
                sweet: 100
            },
            {
                badge: '第 03 层 · 爽脆节拍',
                stats: '清爽度 950 · 脆感加倍',
                title: '冷链冰山生菜 + 墨西哥辣椒圈',
                desc: '每日清晨冷链直达的鲜脆冰山生菜，搭配酸辣开胃的腌制墨西哥Jalapeño辣椒圈，在温柔与狂野之间架起爽脆桥梁。',
                spice: 70,
                sweet: 40
            },
            {
                badge: '第 04 层 · 绝对主角',
                stats: '酥脆度 999 · 多汁度 999',
                title: '195g 赤焰魔鬼脆皮大鸡腿排',
                desc: '甄选整块散养走地鸡大鸡腿肉，经过12小时喀什魔鬼辣椒与甜椒粉真空按摩入味。裹上独创“黄金龙鳞脆浆”，在180°C高温下精准锁住丰盈肉汁！',
                spice: 98,
                sweet: 65
            },
            {
                badge: '第 05 层 · 浓郁暴击',
                stats: '奶香度 960 · 拉丝感 MAX',
                title: '双倍熟成黄金车达芝士片',
                desc: '趁着大鸡排刚出油锅的滚烫余温，铺上加厚熟成黄金车达芝士片，瞬间半融化包裹住酥脆鳞片，咸香浓郁直击灵魂。',
                spice: 20,
                sweet: 88
            },
            {
                badge: '第 06 层 · 稳固基石',
                stats: '焦香度 920 · 承托力 MAX',
                title: '铁板炙烤蒜香黄油粉红底托',
                desc: '底层面包胚涂抹少许蒜香黄油，在铁板上炙烤出金黄焦香脆底，牢牢锁住上方倾泻而下的肉汁与蜜桃芝士酱，吃到最后一口也不塌陷！',
                spice: 25,
                sweet: 80
            }
        ];

        function toggleBurgerExplode() {
            playSoundEffect('layer');
            const stack = document.getElementById('burgerStackContainer');
            const btnText = document.getElementById('explodeBtnText');
            stack.classList.toggle('exploded');
            if (stack.classList.contains('exploded')) {
                btnText.textContent = '点击合体【还原完整汉堡】';
            } else {
                btnText.textContent = '点击开启【悬浮拆解模式】';
            }
        }

        function selectBurgerLayer(index) {
            playSoundEffect('layer');
            const data = burgerLayersData[index];
            document.getElementById('layerBadge').textContent = data.badge;
            document.getElementById('layerStats').textContent = data.stats;
            document.getElementById('layerTitle').textContent = data.title;
            document.getElementById('layerDesc').textContent = data.desc;
            document.getElementById('layerSpiceVal').textContent = data.spice + '%';
            document.getElementById('layerSpiceBar').style.width = data.spice + '%';
            document.getElementById('layerSweetVal').textContent = data.sweet + '%';
            document.getElementById('layerSweetBar').style.width = data.sweet + '%';
        }

        /* ==========================================
         * 5. 甜辣战力调配实验室逻辑
         * ========================================== */
        function updateFlavorLab() {
            const spice = parseInt(document.getElementById('spiceRange').value, 10);
            const sweet = parseInt(document.getElementById('sweetRange').value, 10);
            const hasEgg = document.getElementById('buffEgg').checked;
            const hasBacon = document.getElementById('buffBacon').checked;
            const hasPop = document.getElementById('buffPop').checked;

            // 更新标签文字
            let spiceDesc = '傲娇微辣';
            if (spice > 80) spiceDesc = '喷火魔鬼辣';
            else if (spice > 50) spiceDesc = '热血沸腾辣';
            document.getElementById('spiceValueLabel').textContent = `${spice}% · ${spiceDesc}`;

            let sweetDesc = '暗恋微甜';
            if (sweet > 80) sweetDesc = '满溢蜜桃芝士';
            else if (sweet > 50) sweetDesc = '热恋半糖芝士';
            document.getElementById('sweetValueLabel').textContent = `${sweet}% · ${sweetDesc}`;

            // 计算专属人格称号
            const titleEl = document.getElementById('customPersonaTitle');
            const descEl = document.getElementById('customPersonaDesc');
            const emojiEl = document.getElementById('customEmojiAvatar');

            if (spice >= 70 && sweet >= 70) {
                titleEl.textContent = '【铁汉柔情·甜辣双修宗师堡】';
                descEl.textContent = `${spice}%赤焰香辣配${sweet}%白桃流心芝士，既有硬核酥脆的过瘾痛快，又有包裹舌尖的粉红温柔！`;
                emojiEl.textContent = '🐓💘🔥';
            } else if (spice >= 70 && sweet < 70) {
                titleEl.textContent = '【钢铁直男·烈焰狂暴格斗堡】';
                descEl.textContent = `${spice}%极致魔鬼椒火力全开，只留${sweet}%清爽桃香点缀，适合追求纯粹痛快感的热血食客！`;
                emojiEl.textContent = '🥊🐓🌶️';
            } else if (spice < 70 && sweet >= 70) {
                titleEl.textContent = '【恋爱脑全开·蜜桃芝士瀑布堡】';
                descEl.textContent = `高达${sweet}%的双倍白桃车达芝士倾泻而下，温柔包裹${spice}%微辣脆皮鸡排，一口甜到心坎里！`;
                emojiEl.textContent = '🍑🧀💖';
            } else {
                titleEl.textContent = '【青涩初恋·黄金平衡轻享堡】';
                descEl.textContent = `${spice}%温和香辣与${sweet}%清新白桃酱刚刚好，像极了第一次牵手时恰到好处的心跳频率。`;
                emojiEl.textContent = '🌸🍔✨';
            }

            // 计算价格与卡路里
            let price = 29.9;
            let kcal = 560 + Math.round((spice + sweet) * 0.5);
            if (hasEgg) { price += 4; kcal += 75; }
            if (hasBacon) { price += 6; kcal += 95; }
            if (hasPop) { price += 2; kcal += 25; }

            document.getElementById('customPrice').textContent = price.toFixed(1);
            document.getElementById('customKcal').textContent = `${kcal} KCAL`;

            // 同步更新微信分享海报数据
            const posterEmoji = document.getElementById('posterEmoji');
            const posterTitle = document.getElementById('posterTitle');
            const posterDesc = document.getElementById('posterDesc');
            if (posterEmoji && posterTitle && posterDesc) {
                posterEmoji.textContent = emojiEl.textContent;
                posterTitle.textContent = titleEl.textContent;
                posterDesc.textContent = `${spice}%赤焰魔鬼辣 × ${sweet}%初恋白桃芝士`;
            }
        }

        function orderCustomBurger() {
            const title = document.getElementById('customPersonaTitle').textContent;
            const price = parseFloat(document.getElementById('customPrice').textContent);
            openOrderModal(`定制配方 ${title}`, price);
        }

        /* ==========================================
         * 6. 街机互动小游戏《战斗鸡投喂大作战》
         * ========================================== */
        const canvas = document.getElementById('arcadeCanvas');
        const ctx = canvas.getContext('2d');
        let gameActive = false;
        let score = 0;
        let timeLeft = 25;
        let gameTimerInterval = null;
        let animationFrameId = null;
        let unlockedCoupon = false;

        const player = {
            x: 200,
            width: 84,
            height: 55
        };
        let fallingItems = [];

        function resizeGameCanvas() {
            const wrapper = document.getElementById('gameCanvasWrapper');
            if (!wrapper) return;
            canvas.width = wrapper.clientWidth;
            canvas.height = wrapper.clientHeight;
            player.x = Math.min(Math.max(player.x, player.width / 2), canvas.width - player.width / 2);
            if (!gameActive) {
                drawIdleScene();
            }
        }

        function drawIdleScene() {
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            ctx.fillStyle = '#1A0E26';
            ctx.fillRect(0, 0, canvas.width, canvas.height);
        }

        function spawnFallingItem() {
            const goodPool = [
                { emoji: '🍗', pts: 15, good: true },
                { emoji: '💘', pts: 20, good: true },
                { emoji: '🍑', pts: 15, good: true },
                { emoji: '🧀', pts: 10, good: true },
                { emoji: '🌶️', pts: 15, good: true }
            ];
            const badPool = [
                { emoji: '🧊', pts: -15, good: false },
                { emoji: '🍋', pts: -10, good: false }
            ];

            const isGood = Math.random() > 0.24;
            const template = isGood
                ? goodPool[Math.floor(Math.random() * goodPool.length)]
                : badPool[Math.floor(Math.random() * badPool.length)];

            fallingItems.push({
                x: 30 + Math.random() * (canvas.width - 60),
                y: -25,
                speed: 2.8 + Math.random() * 2.6,
                emoji: template.emoji,
                pts: template.pts,
                good: template.good
            });
        }

        function startMiniGame() {
            resizeGameCanvas();
            playSoundEffect('punch');
            score = 0;
            timeLeft = 25;
            fallingItems = [];
            gameActive = true;
            player.x = canvas.width / 2;

            document.getElementById('gameScore').textContent = score;
            document.getElementById('gameTimer').textContent = timeLeft;
            document.getElementById('gameOverlay').classList.add('hidden');

            if (gameTimerInterval) clearInterval(gameTimerInterval);
            gameTimerInterval = setInterval(() => {
                timeLeft--;
                document.getElementById('gameTimer').textContent = timeLeft;
                if (timeLeft <= 0) {
                    endMiniGame();
                }
            }, 1000);

            if (animationFrameId) cancelAnimationFrame(animationFrameId);
            gameLoop();
        }

        function endMiniGame() {
            gameActive = false;
            clearInterval(gameTimerInterval);
            cancelAnimationFrame(animationFrameId);

            const overlay = document.getElementById('gameOverlay');
            const title = document.getElementById('overlayTitle');
            const sub = document.getElementById('overlaySub');
            overlay.classList.remove('hidden');

            if (score >= 100) {
                unlockedCoupon = true;
                playSoundEffect('win');
                title.textContent = `🎉 恭喜通关！心动得分 ${score} 分！`;
                sub.textContent = '你已成功解锁【立减 ¥10 元热恋霸王券】（优惠码：ROOSTER-LOVE-10），现在下单自动抵扣！';
                document.getElementById('couponStatusBadge').textContent = '✅ 已解锁 ¥10 元立减神券';
                document.getElementById('couponStatusBadge').className = 'px-3 py-1 rounded-full bg-green-400 text-combat-dark text-xs font-black';
                document.getElementById('promoCodeText').textContent = 'ROOSTER-LOVE-10';
                showToast('🎁 恭喜获得 ¥10 元热恋神券，下单自动减免！', '🏆');
            } else {
                title.textContent = `本局得分 ${score} 分，差一点就满100分啦！`;
                sub.textContent = '多接住 💘粉红爱心(+20分) 与 🍗脆皮鸡排(+15分)，再来一局解锁10元神券吧！';
            }
        }

        function gameLoop() {
            if (!gameActive) return;

            ctx.clearRect(0, 0, canvas.width, canvas.height);

            // 绘制背景网格装饰
            ctx.strokeStyle = 'rgba(255, 94, 158, 0.08)';
            ctx.lineWidth = 1;
            for (let x = 0; x < canvas.width; x += 40) {
                ctx.beginPath();
                ctx.moveTo(x, 0);
                ctx.lineTo(x, canvas.height);
                ctx.stroke();
            }

            // 随机生成掉落食材
            if (Math.random() < 0.065) {
                spawnFallingItem();
            }

            // 绘制玩家操控的“恋爱战斗鸡汉堡底托”
            const py = canvas.height - 55;
            ctx.save();
            ctx.fillStyle = '#FF5E9E';
            ctx.strokeStyle = '#FFFFFF';
            ctx.lineWidth = 3;
            ctx.beginPath();
            ctx.roundRect(player.x - player.width / 2, py, player.width, 36, 16);
            ctx.fill();
            ctx.stroke();

            ctx.font = '28px sans-serif';
            ctx.textAlign = 'center';
            ctx.fillText('🐓🍔', player.x, py + 27);
            ctx.restore();

            // 更新并绘制掉落物
            for (let i = fallingItems.length - 1; i >= 0; i--) {
                const item = fallingItems[i];
                item.y += item.speed;

                ctx.font = '28px sans-serif';
                ctx.textAlign = 'center';
                ctx.fillText(item.emoji, item.x, item.y);

                // 碰撞检测
                if (
                    item.y >= py - 5 &&
                    item.y <= py + 38 &&
                    Math.abs(item.x - player.x) < player.width / 2 + 18
                ) {
                    score = Math.max(0, score + item.pts);
                    document.getElementById('gameScore').textContent = score;
                    playSoundEffect(item.good ? 'catchGood' : 'catchBad');

                    if (score >= 100 && !unlockedCoupon) {
                        unlockedCoupon = true;
                        document.getElementById('couponStatusBadge').textContent = '✅ 已达成 100 分神券目标！';
                        document.getElementById('couponStatusBadge').className = 'px-3 py-1 rounded-full bg-green-400 text-combat-dark text-xs font-black';
                    }
                    fallingItems.splice(i, 1);
                    continue;
                }

                // 超出底部移除
                if (item.y > canvas.height + 30) {
                    fallingItems.splice(i, 1);
                }
            }

            animationFrameId = requestAnimationFrame(gameLoop);
        }

        // 鼠标与触屏操控战斗鸡移动
        canvas.addEventListener('mousemove', (e) => {
            const rect = canvas.getBoundingClientRect();
            player.x = e.clientX - rect.left;
        });

        canvas.addEventListener('touchmove', (e) => {
            if (!gameActive) return;
            e.preventDefault();
            const rect = canvas.getBoundingClientRect();
            player.x = e.touches[0].clientX - rect.left;
        }, { passive: false });

        window.addEventListener('keydown', (e) => {
            if (!gameActive) return;
            if (e.key === 'ArrowLeft') movePlayerStep(-35);
            if (e.key === 'ArrowRight') movePlayerStep(35);
        });

        function movePlayerStep(delta) {
            player.x = Math.min(Math.max(player.x + delta, player.width / 2), canvas.width - player.width / 2);
        }

        /* ==========================================
         * 7. 模态框下单与剪贴板功能
         * ========================================== */
        function openOrderModal(itemName, price) {
            playSoundEffect('punch');
            const modal = document.getElementById('orderModal');
            document.getElementById('modalItemName').textContent = itemName;

            const discountRow = document.getElementById('modalDiscountRow');
            let finalPrice = price;
            if (unlockedCoupon) {
                discountRow.classList.remove('hidden');
                discountRow.classList.add('flex');
                finalPrice = Math.max(9.9, price - 10);
            } else {
                discountRow.classList.add('hidden');
                discountRow.classList.remove('flex');
            }

            document.getElementById('modalItemPrice').textContent = finalPrice.toFixed(1);
            modal.classList.remove('hidden');
            modal.classList.add('flex');
        }

        function closeOrderModal() {
            const modal = document.getElementById('orderModal');
            modal.classList.add('hidden');
            modal.classList.remove('flex');
        }

        function copyPromoCode() {
            const code = document.getElementById('promoCodeText').textContent;
            const tempInput = document.createElement('textarea');
            tempInput.value = code;
            document.body.appendChild(tempInput);
            tempInput.select();
            document.execCommand('copy');
            document.body.removeChild(tempInput);
            playSoundEffect('catchGood');
            showToast(`口令码 ${code} 已复制到剪贴板！`, '📋');
        }

        function confirmOrderSubmit() {
            playSoundEffect('win');
            const itemName = document.getElementById('modalItemName').textContent;
            closeOrderModal();
            showToast(`🎉 微信点单成功！【${itemName}】正在180°C现炸！`, '🐓');
        }

        /* ==========================================
         * 8. 微信专属分享引导与战力海报交互
         * ========================================== */
        function openWeChatShareGuide() {
            playSoundEffect('layer');
            const overlay = document.getElementById('wechatShareOverlay');
            overlay.classList.remove('hidden');
            overlay.classList.add('flex');
        }

        function closeWeChatShareGuide() {
            const overlay = document.getElementById('wechatShareOverlay');
            overlay.classList.add('hidden');
            overlay.classList.remove('flex');
        }

        function openPosterModal() {
            playSoundEffect('punch');
            updateFlavorLab();
            const modal = document.getElementById('posterModal');
            modal.classList.remove('hidden');
            modal.classList.add('flex');
        }

        function closePosterModal() {
            const modal = document.getElementById('posterModal');
            modal.classList.add('hidden');
            modal.classList.remove('flex');
        }

        function copyWeChatInviteText() {
            const persona = document.getElementById('customPersonaTitle').textContent;
            const inviteStr = `🐓💘 我刚在《恋爱中的战斗鸡》测出了专属汉堡人格：${persona}！195g魔鬼脆皮大鸡排撞上初恋白桃流心芝士，快请我吃双人热恋暴击桶（口令码：LOVE-KO-520）！`;
            const tempInput = document.createElement('textarea');
            tempInput.value = inviteStr;
            document.body.appendChild(tempInput);
            tempInput.select();
            document.execCommand('copy');
            document.body.removeChild(tempInput);
            playSoundEffect('win');
            showToast('已复制微信投喂暗示文案，快去粘贴发给TA吧！', '💬');
        }

        function showToast(message, emoji = '💘') {
            const toast = document.getElementById('toastMessage');
            document.getElementById('toastText').textContent = message;
            document.getElementById('toastEmoji').textContent = emoji;
            toast.classList.remove('translate-y-24', 'opacity-0');
            setTimeout(() => {
                toast.classList.add('translate-y-24', 'opacity-0');
            }, 3200);
        }

        // 页面加载完成后初始化
        window.onload = function () {
            resizeGameCanvas();
            window.addEventListener('resize', resizeGameCanvas);
            updateFlavorLab();
        };
    </script>
</body>
</html>