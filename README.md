<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>中秋/国庆travel plan</title>
    <style>
        /* 基础重置与手机端适配 */
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }
        body {
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
            background-color: #f4f6f9;
            color: #333;
            line-height: 1.6;
            max-width: 600px;
            margin: 0 auto;
            padding-bottom: 30px;
        }

        /* 主题色 Pantone 16-4526 TCX (#00B1D2) */
        :root {
            --theme-color: #00B1D2;
        }

        /* 顶部封面 */
        .header {
            background-color: var(--theme-color);
            color: white;
            padding: 40px 20px;
            text-align: center;
            border-bottom-left-radius: 20px;
            border-bottom-right-radius: 20px;
            box-shadow: 0 4px 12px rgba(0, 177, 210, 0.2);
        }
        .header h1 {
            font-size: 22px;
            margin-bottom: 8px;
            letter-spacing: 1px;
        }
        .header p {
            font-size: 14px;
            opacity: 0.9;
        }

        .container {
            padding: 20px;
        }

        /* 阶段标题 */
        .phase-title {
            font-size: 18px;
            font-weight: bold;
            color: #2c3e50;
            margin: 20px 0 12px 0;
            display: flex;
            align-items: center;
        }
        .phase-title::before {
            content: "";
            display: inline-block;
            width: 4px;
            height: 18px;
            background-color: var(--theme-color);
            margin-right: 8px;
            border-radius: 2px;
        }

        /* 通用卡片样式 */
        .card {
            background: #ffffff;
            border-radius: 12px;
            padding: 16px;
            margin-bottom: 16px;
            box-shadow: 0 2px 8px rgba(0,0,0,0.04);
        }
        .card-header {
            font-size: 15px;
            font-weight: bold;
            color: var(--theme-color);
            margin-bottom: 12px;
            border-bottom: 1px solid #f0f0f0;
            padding-bottom: 8px;
        }

        /* 航班双列卡片布局 */
        .flight-grid {
            display: flex;
            gap: 12px;
            margin-bottom: 16px;
        }
        .flight-card {
            flex: 1;
            background: #ffffff;
            border-radius: 12px;
            padding: 14px 12px;
            box-shadow: 0 2px 8px rgba(0,0,0,0.04);
            border-top: 3px solid var(--theme-color);
        }
        .flight-tag {
            font-size: 12px;
            background-color: rgba(0, 177, 210, 0.1);
            color: var(--theme-color);
            padding: 2px 6px;
            border-radius: 4px;
            display: inline-block;
            margin-bottom: 8px;
            font-weight: bold;
        }
        .flight-route {
            font-size: 14px;
            font-weight: bold;
            margin-bottom: 4px;
            color: #2c3e50;
        }
        .flight-no {
            font-size: 13px;
            color: #888;
            margin-bottom: 10px;
        }
        .flight-detail {
            font-size: 12px;
            color: #555;
            line-height: 1.5;
        }
        .flight-time-main {
            font-size: 16px;
            font-weight: bold;
            color: #333;
            margin: 6px 0;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        .flight-time-main span {
            color: #999;
            font-size: 12px;
            font-weight: normal;
        }

        /* --- 新增：酒店排版样式 --- */
        .hotel-image {
            width: 100%;
            height: 180px;
            object-fit: cover;
            border-radius: 8px;
            margin-bottom: 12px;
        }
        .hotel-name {
            font-size: 16px;
            font-weight: bold;
            color: #2c3e50;
            margin-bottom: 10px;
        }
        .hotel-info-item {
            font-size: 13px;
            color: #555;
            margin-bottom: 8px;
            display: flex;
            align-items: flex-start;
            line-height: 1.5;
        }
        .hotel-info-item span {
            color: var(--theme-color);
            margin-right: 6px;
            font-weight: bold;
            white-space: nowrap;
        }

        /* 时间轴样式 */
        .timeline {
            margin-top: 10px;
            padding-left: 10px;
        }
        .timeline-item {
            position: relative;
            padding-left: 20px;
            padding-bottom: 20px;
            border-left: 2px solid #e0e6ed;
        }
        .timeline-item:last-child {
            border-left-color: transparent;
            padding-bottom: 0;
        }
        .timeline-item::before {
            content: "";
            position: absolute;
            left: -6px;
            top: 2px;
            width: 10px;
            height: 10px;
            border-radius: 50%;
            background-color: var(--theme-color);
            border: 2px solid #fff;
            box-shadow: 0 0 0 1px var(--theme-color);
        }
        .time-date {
            font-weight: bold;
            font-size: 15px;
            color: #2c3e50;
            margin-bottom: 4px;
        }
        .time-content {
            font-size: 14px;
            color: #666;
            background: #f8f9fa;
            padding: 10px;
            border-radius: 8px;
            margin-top: 6px;
        }
        .time-content p {
            margin-bottom: 4px;
        }
        .time-content p:last-child {
            margin-bottom: 0;
        }
    </style>
</head>
<body>

    <!-- 顶部封面 -->
    <div class="header">
        <h1>中秋/国庆travel plan</h1>
        <p>2026.09.26 - 2026.10.07</p>
    </div>

    <div class="container">
        <!-- 阶段一：十堰 -->
        <div class="phase-title">行程一：十堰 & 武当山 (9/26-10/3)</div>
        
        <!-- 航班信息 -->
        <div class="flight-grid">
            <div class="flight-card">
                <div class="flight-tag">去程</div>
                <div class="flight-route">广州 ✈️ 十堰</div>
                <div class="flight-no">CZ 3335</div>
                <div class="flight-detail">
                    <div>9/26</div>
                    <div>广州白云T2 - 十堰武当山</div>
                </div>
                <div class="flight-time-main">
                    07:35 <span>起飞</span>
                </div>
                <div class="flight-time-main">
                    09:50 <span>落地</span>
                </div>
                <div class="flight-detail" style="margin-top: 8px; text-align: center; color: var(--theme-color); font-weight: bold; background: #f0fbff; border-radius: 4px; padding: 2px;">
                    用时：2h15
                </div>
            </div>

            <div class="flight-card">
                <div class="flight-tag">返程</div>
                <div class="flight-route">十堰 ✈️ 广州</div>
                <div class="flight-no">CZ 3336</div>
                <div class="flight-detail">
                    <div>10/03</div>
                    <div>十堰武当山 - 广州白云T2</div>
                </div>
                <div class="flight-time-main">
                    10:40 <span>起飞</span>
                </div>
                <div class="flight-time-main">
                    12:55 <span>落地</span>
                </div>
                <div class="flight-detail" style="margin-top: 8px; text-align: center; color: var(--theme-color); font-weight: bold; background: #f0fbff; border-radius: 4px; padding: 2px;">
                    用时：2h15
                </div>
            </div>
        </div>

        <!-- 住宿卡片（全新设计） -->
        <div class="card">
            <div class="card-header">🏨 住宿安排</div>
            <!-- 高清无版权占位图：简约、原木、明亮落地窗风格 -->
            <img src="https://images.unsplash.com/photo-1631049307264-da0ec9d70304?auto=format&fit=crop&w=800&q=80" alt="酒店房间" class="hotel-image">
            <div class="hotel-name">品山筱院 (南岩景区店)</div>
            <div class="hotel-info-item">
                <span>📍 地址：</span>
                <div>丹江口市南岩风景区武当路道一堂东30米</div>
            </div>
            <div class="hotel-info-item">
                <span>🛏️ 房型：</span>
                <div>品山双床房</div>
            </div>
            <div class="hotel-info-item">
                <span>🕒 入住：</span>
                <div>9.27（14:00后） — 9.28（12:00前）</div>
            </div>
        </div>

        <!-- 行程时间轴 -->
        <div class="card">
            <div class="card-header">📅 每日日程</div>
            <div class="timeline">
                <div class="timeline-item">
                    <div class="time-date">9月26日 (落地 & 归家)</div>
                    <div class="time-content">
                        <p><strong>09:50</strong> 落地回家，等待吃午饭、休息。</p>
                        <p><strong>下午</strong> 去好邻居超市买菜。</p>
                        <p><strong>晚上</strong> 做饭。主打菜单：五指毛桃猪骨汤、土豆炖牛肉、凉拌生菜。</p>
                    </div>
                </div>
                <div class="timeline-item">
                    <div class="time-date">9月27日 (武当仙山)</div>
                    <div class="time-content">
                        <p><strong>上午</strong> 出发前往武当山。</p>
                        <p><strong>中午</strong> 入住南岩「品山筱院」。</p>
                        <p><strong>下午</strong> 进山游玩。</p>
                    </div>
                </div>
                <div class="timeline-item">
                    <div class="time-date">9月28日 (返程撸串)</div>
                    <div class="time-content">
                        <p><strong>中午</strong> 酒店退房。</p>
                        <p><strong>下午</strong> 返回十堰家中。</p>
                        <p><strong>晚上</strong> 吃烧烤。</p>
                    </div>
                </div>
                <div class="timeline-item">
                    <div class="time-date">9月29日 - 10月2日</div>
                    <div class="time-content">
                        <p>行程待定，机动安排。</p>
                    </div>
                </div>
            </div>
        </div>

        <!-- 阶段二：惠州 -->
        <div class="phase-title">行程二：惠州 (10/4-10/7)</div>
        
        <div class="card">
            <div class="card-header">🏄‍♂️ 冲浪训练营</div>
            <div class="timeline">
                <div class="timeline-item">
                    <div class="time-date">10月4日 - 10月7日</div>
                    <div class="time-content">
                        <p><strong>全天：</strong> 广州前往惠州，参加冲浪训练营，海浪与沙滩的特训！</p>
                    </div>
                </div>
            </div>
        </div>

    </div>

</body>
</html>
