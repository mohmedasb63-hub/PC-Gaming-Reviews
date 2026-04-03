[index (2).html](https://github.com/user-attachments/files/26471964/index.2.html)
<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>PC GAMING REVIEWS - الموسوعة الشاملة</title>
    <style>
        :root {
            --bg-color: #050505;
            --surface-color: rgba(31, 40, 51, 0.8);
            --primary-neon: #ff0055;
            --secondary-neon: #00f3ff;
            --text-main: #e0e0e0;
            --text-light: #ffffff;
            --price-color: #00ff88;
            --glass-border: rgba(255, 255, 255, 0.1);
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            transition: all 0.3s ease;
        }

        body {
            background-color: var(--bg-color);
            background-image: radial-gradient(circle at 50% 0%, #1a001a 0%, #050505 70%);
            color: var(--text-main);
            line-height: 1.6;
            min-height: 100vh;
            display: flex;
            flex-direction: column;
        }

        header {
            text-align: center;
            padding: 50px 20px;
            background: rgba(0, 0, 0, 0.6);
            backdrop-filter: blur(10px);
            border-bottom: 2px solid var(--primary-neon);
            box-shadow: 0 0 30px rgba(255, 0, 85, 0.3);
        }

        header h1 {
            color: var(--text-light);
            font-size: 3.5em;
            letter-spacing: 4px;
            text-shadow: 0 0 15px var(--primary-neon), 0 0 30px var(--secondary-neon);
            font-weight: 900;
        }

        .container {
            max-width: 1300px;
            margin: 40px auto;
            padding: 0 20px;
            flex: 1;
        }

        .grid-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 25px;
        }

        .card {
            background: var(--surface-color);
            backdrop-filter: blur(10px);
            border-radius: 20px;
            overflow: hidden;
            border: 1px solid var(--glass-border);
            cursor: pointer;
            position: relative;
        }

        .card:hover {
            transform: translateY(-10px) scale(1.02);
            box-shadow: 0 15px 40px rgba(0, 243, 255, 0.3);
            border-color: var(--secondary-neon);
        }

        .card img {
            width: 100%;
            height: 200px;
            object-fit: cover;
            border-bottom: 2px solid var(--glass-border);
        }

        .card-content { padding: 20px; text-align: center; }
        .card h2 { color: var(--text-light); font-size: 1.4em; }

        #details-page { display: none; animation: fadeIn 0.5s ease; }
        @keyframes fadeIn { from { opacity: 0; } to { opacity: 1; } }

        .back-btn {
            background: linear-gradient(45deg, var(--primary-neon), #990033);
            color: white; border: none; padding: 12px 25px;
            border-radius: 8px; cursor: pointer; margin-bottom: 30px;
            font-weight: bold; box-shadow: 0 0 15px rgba(255, 0, 85, 0.4);
        }

        .details-header {
            font-size: 2.2em; color: var(--text-light);
            margin-bottom: 20px; border-bottom: 2px solid var(--secondary-neon);
            padding-bottom: 10px; display: block;
        }

        .item-list {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 20px;
        }

        .item-card {
            background: rgba(255, 255, 255, 0.05);
            border: 1px solid #333; border-radius: 12px;
            padding: 20px; cursor: pointer;
        }

        .item-card:hover { border-color: var(--primary-neon); background: rgba(255, 255, 255, 0.1); }

        .comparison-section { margin-top: 50px; overflow-x: auto; }
        table {
            width: 100%; border-collapse: collapse; background: rgba(0,0,0,0.4);
            border-radius: 10px; overflow: hidden; margin-top: 20px;
        }
        th, td { padding: 15px; text-align: center; border: 1px solid #333; }
        th { background: var(--primary-neon); color: white; }

        .modal {
            display: none; position: fixed; z-index: 1000; left: 0; top: 0;
            width: 100%; height: 100%; background: rgba(0,0,0,0.9);
            backdrop-filter: blur(8px);
        }
        .modal-content {
            background: var(--surface-color); margin: 5% auto; padding: 30px;
            border: 2px solid var(--secondary-neon); width: 80%; max-width: 700px;
            border-radius: 20px; color: white; position: relative;
        }
        .close {
            position: absolute; left: 20px; top: 10px; color: var(--primary-neon);
            font-size: 35px; font-weight: bold; cursor: pointer;
        }

        footer {
            text-align: center; padding: 25px; background: #020202;
            color: var(--secondary-neon); border-top: 1px solid var(--primary-neon);
            margin-top: auto; font-weight: bold; letter-spacing: 1.5px;
        }
    </style>
</head>
<body>

    <header>
        <h1>PC GAMING REVIEWS</h1>
        <p>الموسوعة الكاملة لمقارنة قطع الهاردوير لجميع الأجيال (2026)</p>
    </header>

    <div class="container">
        <div id="main-page" class="grid-container">
            <div class="card" onclick="openDetails('gpu')">
                <img src="https://images.unsplash.com/photo-1591488320449-011701bb6704?auto=format&fit=crop&w=500" alt="GPU">
                <div class="card-content"><h2>كروت الشاشة</h2><span class="eng-title">GPUs</span></div>
            </div>
            <div class="card" onclick="openDetails('cpu')">
                <img src="https://images.unsplash.com/photo-1591799264318-7e6ef8ddb7ea?auto=format&fit=crop&w=500" alt="CPU">
                <div class="card-content"><h2>المعالجات</h2><span class="eng-title">CPUs</span></div>
            </div>
            <div class="card" onclick="openDetails('ram')">
                <img src="https://images.unsplash.com/photo-1562976540-1502c2145186?auto=format&fit=crop&w=500" alt="RAM">
                <div class="card-content"><h2>الرامات</h2><span class="eng-title">RAM</span></div>
            </div>
            <div class="card" onclick="openDetails('storage')">
                <img src="https://images.unsplash.com/photo-1531492746076-161ca9bcad58?auto=format&fit=crop&w=500" alt="Storage">
                <div class="card-content"><h2>التخزين</h2><span class="eng-title">Storage NVMe</span></div>
            </div>
            <div class="card" onclick="openDetails('case')">
                <img src="https://images.unsplash.com/photo-1547082299-de196ea013d6?auto=format&fit=crop&w=500" alt="Case">
                <div class="card-content"><h2>صناديق الحاسوب</h2><span class="eng-title">PC Cases</span></div>
            </div>
            <div class="card" onclick="openDetails('monitor')">
                <img src="https://images.unsplash.com/photo-1527443224154-c4a3942d3acf?auto=format&fit=crop&w=500" alt="Monitor">
                <div class="card-content"><h2>الشاشات</h2><span class="eng-title">Monitors</span></div>
            </div>
            <div class="card" onclick="openDetails('cooling')">
                <img src="https://images.unsplash.com/photo-1587202372634-32705e3bf49c?auto=format&fit=crop&w=500" alt="Cooling">
                <div class="card-content"><h2>أنظمة التبريد</h2><span class="eng-title">Cooling Systems</span></div>
            </div>
            <div class="card" onclick="openDetails('motherboard')">
                <img src="https://images.unsplash.com/photo-1518770660439-4636190af475?auto=format&fit=crop&w=500" alt="Motherboard">
                <div class="card-content"><h2>اللوحات الأم</h2><span class="eng-title">Motherboards</span></div>
            </div>
        </div>

        <div id="details-page">
            <button class="back-btn" onclick="goBack()">⟵ العودة للأقسام</button>
            <h2 id="category-title" class="details-header">العنوان</h2>
            <div id="items-container" class="item-list"></div>
            <div class="comparison-section">
                <h3 style="color: var(--primary-neon);">جدول المقارنة الفنية (الأجيال):</h3>
                <div id="comparison-table-container"></div>
            </div>
        </div>
    </div>

    <div id="infoModal" class="modal">
        <div class="modal-content">
            <span class="close" onclick="closeModal()">&times;</span>
            <h2 id="modal-title" style="color: var(--secondary-neon);"></h2>
            <hr style="border: 1px solid #333; margin: 15px 0;">
            <p id="modal-desc" style="font-size: 1.1em; line-height: 1.8;"></p>
            <div id="modal-specs" style="margin-top: 20px; color: var(--price-color); font-weight: bold;"></div>
        </div>
    </div>

    <footer>
        &copy; 2026 جميع الحقوق محفوظة لـ محمد احمد خالد MOHAMED KILLUA99
    </footer>

    <script>
        const partsData = {
            gpu: {
                title: "كروت الشاشة (جيل 5000 و 4000 و AMD)",
                items: [
                    { name: "NVIDIA RTX 5090", desc: "أقوى كرت في العالم بمعمارية Blackwell.", price: "$1,999", full: "يعتبر القمة المطلقة للأداء بمعمارية Blackwell الجديدة، يدعم ذاكرة GDDR7 فائقة السرعة وتقنيات DLSS 4. مصمم للمحترفين واللاعبين على دقة 8K." },
                    { name: "NVIDIA RTX 4090", desc: "ملك الجيل السابق الذي لا يزال قوياً جداً.", price: "$1,599", full: "بمعمارية Ada Lovelace، يقدم أداءً لا يضاهى في الرندرة وتتبع الأشعة، مع ذاكرة ضخمة تبلغ 24 جيجابايت." },
                    { name: "AMD Radeon RX 9900 XTX", desc: "وحش AMD الجديد بمعمارية RDNA 4.", price: "$1,099", full: "يقدم قيمة مقابل سعر ممتازة، مع تحسن هائل في تقنيات تتبع الأشعة وذاكرة وصول عشوائي للفيديو سريعة جداً." }
                ],
                compare: `<table><tr><th>الكرت</th><th>المعمارية</th><th>الذاكرة</th></tr><tr><td>RTX 5090</td><td>Blackwell</td><td>32GB GDDR7</td></tr><tr><td>RTX 4090</td><td>Lovelace</td><td>24GB GDDR6X</td></tr></table>`
            },
            cpu: {
                title: "المعالجات (AMD 9000 & Intel Ultra)",
                items: [
                    { name: "AMD Ryzen 9 9950X", desc: "معالج الجيل الجديد بـ 16 نواة.", price: "$699", full: "بمعمارية Zen 5، يقدم أداء إنتاجياً مذهلاً وكفاءة طاقة أفضل بمرتين من الجيل السابق، مثالي لعمليات الرندرة الثقيلة." },
                    { name: "Intel Core Ultra 9 285K", desc: "ثورة إنتل الجديدة لتقليل الحرارة.", price: "$599", full: "يمثل تغييراً جذرياً في فلسفة إنتل، حيث يركز على الأداء لكل واط وتوفير الطاقة مع الحفاظ على سرعات تردد عالية جداً." }
                ],
                compare: `<table><tr><th>المعالج</th><th>الأنوية</th><th>السرعة</th></tr><tr><td>Ryzen 9950X</td><td>16</td><td>5.7GHz</td></tr><tr><td>Ultra 285K</td><td>24</td><td>5.5GHz</td></tr></table>`
            },
            ram: {
                title: "الرامات (DDR5 & DDR4)",
                items: [
                    { name: "Corsair Dominator Titanium 64GB", desc: "أحدث رامات DDR5 بسرعة 8000MHz.", price: "$320", full: "تقدم سرعات خرافية لنقل البيانات، مثالية لفك الضغط والرندرة وتطبيقات الذكاء الاصطناعي التي تتطلب سرعة ذاكرة عالية." },
                    { name: "G.Skill Trident Z5 32GB", desc: "الأكثر شعبية للاعبين بسرعة 7200MHz.", price: "$160", full: "توازن ممتاز بين السعر والأداء، مع توقيتات منخفضة تضمن استقرار الفريمات في الألعاب الثقيلة." }
                ],
                compare: `<table><tr><th>النوع</th><th>السرعة</th><th>الاستخدام</th></tr><tr><td>DDR5</td><td>8000MHz</td><td>الأجيال الحديثة</td></tr><tr><td>DDR4</td><td>3600MHz</td><td>تجميعات اقتصادية</td></tr></table>`
            },
            storage: {
                title: "وحدات التخزين NVMe",
                items: [
                    { name: "Crucial T705 2TB Gen5", desc: "أسرع SSD في العالم حالياً.", price: "$290", full: "بسرعة قراءة تصل إلى 14,500 ميجابايت في الثانية، ينهي تماماً فترات التحميل في الألعاب والبرامج." },
                    { name: "Samsung 990 PRO 2TB", desc: "ملك الاستقرار والأداء من سامسونج.", price: "$170", full: "يعتبر الخيار الأكثر موثوقية للاعبين والمصنعين، مع تبريد ذاتي ممتاز وعمر افتراضي طويل جداً." }
                ],
                compare: `<table><tr><th>النوع</th><th>سرعة القراءة</th><th>الواجهة</th></tr><tr><td>Gen 5 NVMe</td><td>14.5 GB/s</td><td>PCIe 5.0</td></tr><tr><td>Gen 4 NVMe</td><td>7.4 GB/s</td><td>PCIe 4.0</td></tr></table>`
            },
            case: {
                title: "صناديق الحاسوب (PC Cases)",
                items: [
                    { name: "Lian Li O11 Vision", desc: "تصميم زجاجي بانورامي بدون أعمدة.", price: "$150", full: "يوفر رؤية كاملة لقطع الحاسوب من 3 جهات، مع دعم واسع للمبردات المائية وتصميم الغرفة المزدوجة." },
                    { name: "Hyte Y70 Touch", desc: "كيس مزود بشاشة لمس مدمجة.", price: "$360", full: "يحتوي على شاشة 4K عمودية مدمجة لعرض إحصائيات الجهاز أو الصور، ويعطي طابعاً مستقبلياً للتجميعة." }
                ],
                compare: `<table><tr><th>الكيس</th><th>الميزة</th><th>الحجم</th></tr><tr><td>Lian Li O11</td><td>رؤية 3D</td><td>Mid-Tower</td></tr><tr><td>Hyte Y70</td><td>شاشة لمس</td><td>Large Mid</td></tr></table>`
            },
            monitor: {
                title: "الشاشات (Monitors)",
                items: [
                    { name: "Samsung Odyssey OLED G9", desc: "شاشة فائقة العرض 49 بوصة OLED.", price: "$1,799", full: "بتردد 240Hz واستجابة 0.03ms، تقدم أعمق درجات اللون الأسود وأفضل تجربة غمر بصري." },
                    { name: "ASUS ROG Swift 360Hz", desc: "شاشة 2K مخصصة للمحترفين.", price: "$699", full: "أسرع شاشة في فئة الـ 1440p، مصممة خصيصاً لألعاب المنافسات مثل Valorant و Counter-Strike." }
                ],
                compare: `<table><tr><th>الشاشة</th><th>التردد</th><th>النوع</th></tr><tr><td>Odyssey OLED</td><td>240Hz</td><td>OLED</td></tr><tr><td>ROG Swift</td><td>360Hz</td><td>IPS</td></tr></table>`
            },
            cooling: {
                title: "أنظمة التبريد (Cooling Systems)",
                items: [
                    { name: "NZXT Kraken Elite 360", desc: "تبريد مائي بشاشة LCD عالية الدقة.", price: "$280", full: "يسمح لك بعرض صور متحركة GIF أو إحصائيات الجهاز بشكل حي، مع مضخة قوية جداً من أحدث الأجيال." },
                    { name: "Noctua NH-D15 G2", desc: "الجيل الثاني من أسطورة التبريد الهوائي.", price: "$150", full: "يتفوق على معظم المبردات المائية في الهدوء والعمر الافتراضي، مع مروحة معاد تصميمها بالكامل لأفضل ضغط هواء." }
                ],
                compare: `<table><tr><th>المبرد</th><th>النوع</th><th>الضوضاء</th></tr><tr><td>Kraken Elite</td><td>مائي 360</td><td>منخفضة</td></tr><tr><td>Noctua G2</td><td>هوائي مزدوج</td><td>شبه منعدمة</td></tr></table>`
            },
            motherboard: {
                title: "اللوحات الأم (Motherboards)",
                items: [
                    { name: "ASUS ROG Crosshair X870E", desc: "أفضل لوحة لمعالجات AMD الجيل الجديد.", price: "$750", full: "دعم كامل لـ PCIe 5.0، تقنية Wi-Fi 7، ونظام طاقة (VRM) جبار لضمان أقصى كسر سرعة مستقر." },
                    { name: "MSI Z890 GODLIKE", desc: "اللوحة الأسطورية لمعالجات إنتل ألترا.", price: "$1,200", full: "تأتي مع شاشة لمس مدمجة وميزات احترافية لتتبع الأخطاء، وهي مصممة لتحطيم الأرقام القياسية في الأداء." }
                ],
                compare: `<table><tr><th>اللوحة</th><th>الشريحة</th><th>المقبس</th></tr><tr><td>ROG X870E</td><td>X870E</td><td>AM5</td></tr><tr><td>MSI Z890</td><td>Z890</td><td>LGA 1851</td></tr></table>`
            }
        };

        function openDetails(key) {
            const data = partsData[key];
            if(!data) return;
            document.getElementById('main-page').style.display = 'none';
            document.getElementById('details-page').style.display = 'block';
            document.getElementById('category-title').innerText = data.title;
            const container = document.getElementById('items-container');
            container.innerHTML = data.items.map(item => `
                <div class="item-card" onclick="showFullInfo('${item.name}', '${item.full}', '${item.price}')">
                    <h3 style="color:var(--secondary-neon)">${item.name}</h3>
                    <p>${item.desc}</p>
                    <div style="color:var(--price-color); margin-top:10px;">${item.price}</div>
                </div>
            `).join('');
            document.getElementById('comparison-table-container').innerHTML = data.compare || "لا يوجد جدول مقارنة متاح حالياً";
            window.scrollTo(0,0);
        }

        function showFullInfo(name, full, price) {
            document.getElementById('modal-title').innerText = name;
            document.getElementById('modal-desc').innerText = full;
            document.getElementById('modal-specs').innerText = "السعر الحالي: " + price;
            document.getElementById('infoModal').style.display = "block";
        }

        function closeModal() { document.getElementById('infoModal').style.display = "none"; }
        function goBack() { document.getElementById('details-page').style.display = 'none'; document.getElementById('main-page').style.display = 'grid'; }
        window.onclick = function(e) { if (e.target == document.getElementById('infoModal')) closeModal(); }
    </script>
</body>
</html>
