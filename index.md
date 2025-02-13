<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>友嘉科技服务中心</title>
    <link href="https://unpkg.com/ionicons@5.5.2/dist/css/ionicons.min.css" rel="stylesheet">
    <style>
        :root {
            --primary-color: #00f7ff;
            --secondary-color: #6c5ce7;
            --bg-gradient: linear-gradient(135deg, #1a1a2e 0%, #16213e 100%);
            --neon-shadow: 0 0 15px rgba(0, 247, 255, 0.5);
            --section-spacing: 120px;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Microsoft YaHei', 'Helvetica Neue', sans-serif;
        }

        body {
            background: var(--bg-gradient);
            color: #ffffff;
            line-height: 1.8;
            overflow-x: hidden;
        }

        /* 语言切换 */
        .lang-switcher {
            position: fixed;
            top: 30px;
            right: 50px;
            z-index: 1000;
            display: flex;
            gap: 12px;
        }

        .lang-btn {
            background: rgba(255,255,255,0.1);
            border: 1px solid var(--primary-color);
            color: var(--primary-color);
            padding: 10px 25px;
            border-radius: 30px;
            cursor: pointer;
            transition: all 0.3s;
            backdrop-filter: blur(5px);
        }

        .lang-btn.active {
            background: var(--primary-color);
            color: #000;
        }

        /* 粒子背景 */
        #particles-js {
            position: fixed;
            width: 100%;
            height: 100%;
            z-index: -1;
        }

        /* 主标题区 */
        .hero {
            text-align: center;
            padding: 180px 20px 150px;
            position: relative;
        }

        .hero::before {
            content: '';
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            width: 300px;
            height: 300px;
            background: radial-gradient(circle, rgba(0,247,255,0.2) 0%, transparent 70%);
        }

        .hero h1 {
            font-size: 4.5em;
            background: linear-gradient(45deg, #00f7ff, #6c5ce7);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            margin-bottom: 30px;
            animation: glow 2s ease-in-out infinite alternate;
        }

        /* 内容区块 */
        .section {
            padding: var(--section-spacing) 20px;
            max-width: 1400px;
            margin: 0 auto;
        }

        .section-title {
            font-size: 2.8em;
            text-align: center;
            margin-bottom: 80px;
            position: relative;
        }

        .section-title::after {
            content: '';
            display: block;
            width: 80px;
            height: 3px;
            background: var(--primary-color);
            margin: 20px auto;
            box-shadow: var(--neon-shadow);
        }

        /* 卡片布局 */
        .card-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 40px;
            padding: 20px;
        }

        .card {
            background: rgba(255,255,255,0.05);
            border: 1px solid rgba(0, 247, 255, 0.3);
            border-radius: 20px;
            padding: 40px;
            transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
            position: relative;
            overflow: hidden;
        }

        .card::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: linear-gradient(45deg, transparent, rgba(0,247,255,0.1), transparent);
            transform: rotate(45deg);
        }

        .card:hover {
            transform: translateY(-15px) rotateX(10deg);
            box-shadow: 0 25px 40px rgba(0,0,0,0.3),
                        var(--neon-shadow);
        }

        /* 硬件配置表 */
        .spec-table {
            background: rgba(0,0,0,0.3);
            border-radius: 15px;
            padding: 30px;
            margin: 40px 0;
            border: 1px solid rgba(0,247,255,0.2);
        }

        table {
            width: 100%;
            border-collapse: collapse;
            background: rgba(255,255,255,0.03);
            backdrop-filter: blur(5px);
        }

        th, td {
            padding: 18px;
            border-bottom: 1px solid rgba(0,247,255,0.1);
            text-align: left;
        }

        th {
            background: linear-gradient(45deg, rgba(0,247,255,0.2), rgba(108,92,231,0.2));
            font-weight: 600;
            color: var(--primary-color);
        }

        tr:hover {
            background: rgba(0,247,255,0.03);
        }

        /* 页脚备案 */
        footer {
            text-align: center;
            padding: 60px 20px;
            border-top: 1px solid rgba(0,247,255,0.2);
            margin-top: 100px;
        }

        .copyright {
            font-size: 0.9em;
            opacity: 0.8;
            line-height: 1.6;
        }

        /* 响应式设计 */
        @media (max-width: 768px) {
            .hero h1 { font-size: 2.8em; }
            .section-title { font-size: 2em; }
            .card-grid { grid-template-columns: 1fr; }
            .lang-switcher { top: 20px; right: 20px; }
            table { display: block; overflow-x: auto; }
        }

        @keyframes glow {
            from { text-shadow: 0 0 10px rgba(0,247,255,0.3); }
            to { text-shadow: 0 0 30px rgba(0,247,255,0.6); }
        }
    </style>
</head>
<body>
    <div id="particles-js"></div>
    
    <div class="lang-switcher">
        <button class="lang-btn active" onclick="changeLanguage('zh-CN')">简体</button>
        <button class="lang-btn" onclick="changeLanguage('en')">English</button>
        <button class="lang-btn" onclick="changeLanguage('zh-TW')">繁體</button>
    </div>

    <section class="hero">
        <h1 data-i18n="title">友嘉共享科技服务中心</h1>
        <p data-i18n="slogan">超高端卓越性能设备 · 24小时全年无休服务</p>
    </section>

    <!-- 核心服务区块 -->
    <section class="section">
        <h2 class="section-title" data-i18n="coreServices">核心服务优势</h2>
        <div class="card-grid">
            <!-- 原有服务卡片... -->
        </div>
    </section>

    <!-- 新增硬件配置 -->
    <section class="section">
        <h2 class="section-title" data-i18n="gamingPc">2025旗舰电竞主机</h2>
        <div class="spec-table">
            <table>
                <thead>
                    <tr>
                        <th data-i18n="component">组件</th>
                        <th data-i18n="model">型号规格</th>
                        <th data-i18n="parameters">技术参数</th>
                        <th data-i18n="performance">性能指标</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td>CPU</td>
                        <td>AMD Ryzen 9 10980X3D (2025)</td>
                        <td>24核/5.8GHz/280W/5nm工艺</td>
                        <td>鲁大师: 1,580,000</td>
                    </tr>
                    <tr>
                        <td>GPU</td>
                        <td>NVIDIA RTX 6090 Ti</td>
                        <td>48GB GDDR7/核心2685MHz/600W</td>
                        <td>3DMark: 42,850</td>
                    </tr>
                    <!-- 更多配置行... -->
                </tbody>
            </table>
        </div>
    </section>

    <section class="section">
        <h2 class="section-title" data-i18n="workstation">双路工作站</h2>
        <div class="spec-table">
            <table>
                <thead>
                    <tr>
                        <th data-i18n="component">组件</th>
                        <th data-i18n="model">型号规格</th>
                        <th data-i18n="parameters">技术参数</th>
                        <th data-i18n="certification">认证标准</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td>CPU</td>
                        <td>Intel Xeon Platinum 9595×2</td>
                        <td>128核/4.5GHz/350W/10nm</td>
                        <td>ISO-9001:2025</td>
                    </tr>
                    <tr>
                        <td>内存</td>
                        <td>美光DDR5-6400 2TB</td>
                        <td>八通道/CL36/ECC纠错</td>
                        <td>JEDEC标准</td>
                    </tr>
                    <!-- 更多配置行... -->
                </tbody>
            </table>
        </div>
    </section>

    <footer>
        <div class="copyright">
            <p>©2025 友嘉科技 豫ICP备20258888号-12</p>
            <p>豫公网安备 41010902002097号</p>
            <p data-i18n="compliance">符合GB/T 35273-2025信息安全规范</p>
        </div>
    </footer>

    <script src="https://cdn.jsdelivr.net/particles.js/2.0.0/particles.min.js"></script>
    <script>
        // 粒子动画
        particlesJS('particles-js', {
            particles: {
                number: { value: 80 },
                color: { value: '#00f7ff' },
                size: { value: 3 },
                move: { speed: 1.5 }
            },
            interactivity: {
                events: {
                    onhover: { enable: true, mode: 'repulse' }
                }
            }
        });

        // 多语言支持
        const translations = {
            'zh-CN': {
                // 原有翻译...
                gamingPc: '2025旗舰电竞主机',
                workstation: '双路服务器工作站',
                component: '组件',
                model: '型号规格',
                parameters: '技术参数',
                performance: '性能指标',
                certification: '认证标准',
                compliance: '符合GB/T 35273-2025信息安全规范'
            },
            'en': {
                // 原有翻译...
                gamingPc: '2025 Gaming PC',
                workstation: 'Dual Workstation',
                component: 'Component',
                model: 'Model',
                parameters: 'Specifications',
                performance: 'Performance',
                certification: 'Certification',
                compliance: 'Compliant with GB/T 35273-2025'
            },
            'zh-TW': {
                // 原有翻译...
                gamingPc: '2025旗艦電競主機',
                workstation: '雙路工作站',
                component: '組件',
                model: '型號規格',
                parameters: '技術參數',
                performance: '性能指標',
                certification: '認證標準',
                compliance: '符合GB/T 35273-2025信息安全規範'
            }
        };

        function changeLanguage(lang) {
            document.querySelectorAll('.lang-btn').forEach(btn => btn.classList.remove('active'));
            event.target.classList.add('active');
            document.querySelectorAll('[data-i18n]').forEach(el => {
                const key = el.getAttribute('data-i18n');
                el.innerHTML = translations[lang][key] || el.innerHTML;
            });
        }

        // 3D卡片交互
        document.querySelectorAll('.card').forEach(card => {
            card.addEventListener('mousemove', e => {
                const rect = card.getBoundingClientRect();
                card.style.transform = `
                    perspective(1000px)
                    rotateX(${(e.clientY - rect.top - rect.height/2)/20}deg)
                    rotateY(${-(e.clientX - rect.left - rect.width/2)/20}deg)
                `;
            });
            card.addEventListener('mouseleave', () => {
                card.style.transform = 'none';
            });
        });
    </script>
</body>
</html>
