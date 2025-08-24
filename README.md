<!doctype html>
<html lang="vi">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Khám phá Việt Nam</title>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;800&display=swap" rel="stylesheet">
  <style>
    :root {
      --bg: #0b1220;
      --fg: #f1f5f9;
      --muted: #9aa4b2;
      --brand: #00b894;
      --brand-2: #00a8ff;
      --card: #0f172a;
      --card-2: #101826;
      --stroke: rgba(255,255,255,.08);
      --shadow: 0 10px 30px rgba(0,0,0,.35);
      --radius: 18px;
    }
    * { box-sizing: border-box; }
    html, body { height: 100%; }
    body { margin: 0; font-family: Inter, system-ui, -apple-system, Segoe UI, Roboto, Arial, sans-serif; background: radial-gradient(1200px 600px at 70% -10%, rgba(0,184,148,.25), transparent 70%), radial-gradient(800px 500px at 10% 10%, rgba(0,168,255,.18), transparent 60%), var(--bg); color: var(--fg); }
    a { color: inherit; text-decoration: none; }
    .container { width: min(1200px, 92vw); margin: 0 auto; }
    header { position: sticky; top: 0; z-index: 50; backdrop-filter: blur(10px); background: linear-gradient(to bottom, rgba(11,18,32,.8), rgba(11,18,32,.4)); border-bottom: 1px solid var(--stroke); }
    .nav { display: flex; align-items: center; justify-content: space-between; padding: 14px 0; }
    .brand { display: flex; align-items: center; gap: 10px; font-weight: 800; letter-spacing: .4px; }
    .brand-badge { width: 36px; height: 36px; border-radius: 50%; background: conic-gradient(from 140deg, var(--brand), var(--brand-2)); box-shadow: var(--shadow); display: grid; place-items: center; font-weight: 800; color: #001017; }
    .nav-links { display: flex; gap: 18px; align-items: center; }
    .nav-links a { padding: 8px 12px; border-radius: 10px; color: var(--muted); }
    .nav-links a:hover { background: rgba(255,255,255,.06); color: var(--fg); }
    .cta { display: inline-flex; align-items: center; gap: 10px; padding: 10px 16px; border-radius: 12px; background: linear-gradient(135deg, var(--brand), var(--brand-2)); color: #001017; font-weight: 700; box-shadow: var(--shadow); }
    .hero { padding: 64px 0 32px; position: relative; overflow: clip; }
    .hero-grid { display: grid; grid-template-columns: 1.1fr .9fr; gap: 28px; align-items: center; }
    .hero h1 { font-size: clamp(32px, 5.5vw, 56px); line-height: 1.05; margin: 0 0 14px; }
    .hero p { font-size: clamp(16px, 2.2vw, 18px); color: var(--muted); margin: 0 0 22px; }
    .chip { display: inline-flex; align-items: center; gap: 8px; padding: 8px 12px; border: 1px solid var(--stroke); border-radius: 999px; color: var(--muted); font-size: 14px; }
    .searchbar { display: grid; grid-template-columns: 1fr auto; gap: 10px; padding: 10px; background: rgba(255,255,255,.05); border: 1px solid var(--stroke); border-radius: 14px; }
    .searchbar input { background: transparent; border: none; outline: none; color: var(--fg); font-size: 16px; padding: 12px; }
    .searchbar button { padding: 12px 16px; border-radius: 12px; border: 1px solid var(--stroke); background: #111a2e; color: var(--fg); font-weight: 600; }
    .hero-card { position: relative; border-radius: var(--radius); overflow: hidden; background: linear-gradient(160deg, rgba(0,184,148,.35), rgba(0,168,255,.25)), radial-gradient(600px 280px at 80% 10%, rgba(255,255,255,.08), transparent), url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" width="1200" height="800"><defs><linearGradient id="g" x1="0" y1="0" x2="1" y2="1"><stop offset="0" stop-color="%2300b894"/><stop offset="1" stop-color="%2300a8ff"/></linearGradient></defs><rect width="1200" height="800" fill="%230b1220"/><circle cx="900" cy="200" r="220" fill="url(%23g)" fill-opacity="0.25"/><circle cx="200" cy="600" r="260" fill="url(%23g)" fill-opacity="0.2"/></svg>'); background-size: cover; aspect-ratio: 4/3; border: 1px solid var(--stroke); box-shadow: var(--shadow); }
    .hero-stats { position: absolute; left: 18px; bottom: 18px; display: flex; gap: 12px; }
    .pill { background: rgba(15,23,42,.8); border: 1px solid var(--stroke); padding: 10px 14px; border-radius: 12px; }
    section { padding: 48px 0; }
    .section-head { display: flex; align-items: end; justify-content: space-between; margin-bottom: 18px; }
    .section-head h2 { margin: 0; font-size: clamp(22px, 3.8vw, 32px); }
    .cards { display: grid; grid-template-columns: repeat(3, 1fr); gap: 18px; }
    .card { background: linear-gradient(180deg, rgba(255,255,255,.04), rgba(255,255,255,.02)); border: 1px solid var(--stroke); border-radius: var(--radius); overflow: hidden; box-shadow: var(--shadow); display: grid; grid-template-rows: 160px auto; }
    .thumb { background: radial-gradient(300px 140px at 70% 30%, rgba(0,184,148,.35), transparent), radial-gradient(240px 120px at 20% 80%, rgba(0,168,255,.28), transparent); border-bottom: 1px solid var(--stroke); }
    .card-body { padding: 16px; display: grid; gap: 8px; }
    .meta { color: var(--muted); font-size: 14px; }
    .chip-row { display: flex; flex-wrap: wrap; gap: 8px; }
    .chip-sm { font-size: 12px; padding: 6px 10px; border: 1px solid var(--stroke); border-radius: 999px; color: var(--muted); }
    .grid-2 { display: grid; grid-template-columns: repeat(2, 1fr); gap: 18px; }
    .panel { background: linear-gradient(180deg, rgba(255,255,255,.04), rgba(255,255,255,.02)); border: 1px solid var(--stroke); border-radius: var(--radius); padding: 18px; box-shadow: var(--shadow); }
    .panel h3 { margin: 0 0 6px; }
    .list { display: grid; gap: 10px; color: var(--muted); }
    .newsletter { display: grid; grid-template-columns: 1.4fr .6fr; gap: 18px; align-items: center; background: linear-gradient(120deg, rgba(0,184,148,.15), rgba(0,168,255,.15)); border: 1px solid var(--stroke); border-radius: var(--radius); padding: 18px; }
    footer { padding: 32px 0 48px; border-top: 1px solid var(--stroke); color: var(--muted); }
    .footer-grid { display: grid; grid-template-columns: 1.2fr repeat(3, 1fr); gap: 18px; }
    .fine { margin-top: 18px; font-size: 12px; opacity: .85; }
    @media (max-width: 980px) {
      .hero-grid { grid-template-columns: 1fr; }
      .cards { grid-template-columns: 1fr 1fr; }
      .newsletter { grid-template-columns: 1fr; }
      .footer-grid { grid-template-columns: 1fr 1fr; }
    }
    @media (max-width: 640px) {
      .nav-links { display: none; }
      .cards { grid-template-columns: 1fr; }
      .footer-grid { grid-template-columns: 1fr; }
    }
  </style>
</head>
<body>
  <header>
    <div class="container nav">
      <div class="brand">
        <div class="brand-badge">VN</div>
        <div>Vietnam Travel</div>
      </div>
      <nav class="nav-links">
        <a href="#destinations">Điểm đến</a>
        <a href="#experiences">Trải nghiệm</a>
        <a href="#planning">Lên kế hoạch</a>
        <a href="#tips">Mẹo hay</a>
        <a class="cta" href="#newsletter">Nhận gợi ý</a>
      </nav>
    </div>
  </header>

  <main>
    <section class="hero">
      <div class="container hero-grid">
        <div>
          <div class="chip">Khám phá thiên nhiên – ẩm thực – văn hoá</div>
          <h1>Khám phá Việt Nam: từ núi rừng Hà Giang đến biển xanh Phú Quốc</h1>
          <p>Tìm cảm hứng cho hành trình tiếp theo với các gợi ý điểm đến, lịch trình ngắn ngày, đặc sản địa phương và sự kiện theo mùa.</p>
          <form class="searchbar" onsubmit="event.preventDefault()">
            <input aria-label="Tìm kiếm" placeholder="Bạn muốn đi đâu? Ví dụ: Hội An, Sa Pa, Côn Đảo">
            <button type="submit">Tìm</button>
          </form>
        </div>
        <div class="hero-card">
          <div class="hero-stats">
            <div class="pill">+3.000 km bờ biển</div>
            <div class="pill">54 dân tộc</div>
            <div class="pill">4 mùa sự kiện</div>
          </div>
        </div>
      </div>
    </section>

    <section id="destinations">
      <div class="container">
        <div class="section-head">
          <h2>Điểm đến nổi bật</h2>
          <a class="chip" href="#">Xem tất cả</a>
        </div>
        <div class="cards">
          <article class="card">
            <div class="thumb"></div>
            <div class="card-body">
              <h3>Hà Nội</h3>
              <div class="meta">Phố cổ, ẩm thực đường phố, di sản</div>
              <div class="chip-row">
                <span class="chip-sm">Cà phê trứng</span>
                <span class="chip-sm">Hồ Gươm</span>
                <span class="chip-sm">Làng nghề</span>
              </div>
            </div>
          </article>
          <article class="card">
            <div class="thumb"></div>
            <div class="card-body">
              <h3>Đà Nẵng & Hội An</h3>
              <div class="meta">Bãi biển, phố cổ, ẩm thực miền Trung</div>
              <div class="chip-row">
                <span class="chip-sm">Sơn Trà</span>
                <span class="chip-sm">Ngũ Hành Sơn</span>
                <span class="chip-sm">Cao lầu</span>
              </div>
            </div>
          </article>
          <article class="card">
            <div class="thumb"></div>
            <div class="card-body">
              <h3>TP. Hồ Chí Minh</h3>
              <div class="meta">Năng động, nghệ thuật, đêm muộn</div>
              <div class="chip-row">
                <span class="chip-sm">Nhà hát</span>
                <span class="chip-sm">Chợ đêm</span>
                <span class="chip-sm">Bùi Viện</span>
              </div>
            </div>
          </article>
        </div>
      </div>
    </section>

    <section id="experiences">
      <div class="container">
        <div class="section-head">
          <h2>Trải nghiệm theo sở thích</h2>
        </div>
        <div class="grid-2">
          <div class="panel">
            <h3>Thiên nhiên & ngoài trời</h3>
            <div class="list">
              <div>Chinh phục Fansipan</div>
              <div>Đi thuyền Hạ Long</div>
              <div>Lặn ngắm san hô Phú Quốc</div>
            </div>
          </div>
          <div class="panel">
            <h3>Văn hoá & di sản</h3>
            <div class="list">
              <div>Hoàng thành Huế</div>
              <div>Không gian cồng chiêng</div>
              <div>Lễ hội Chùa Hương</div>
            </div>
          </div>
          <div class="panel">
            <h3>Ẩm thực địa phương</h3>
            <div class="list">
              <div>Bún chả Hà Nội</div>
              <div>Bánh mì Hội An</div>
              <div>Hủ tiếu Sài Gòn</div>
            </div>
          </div>
          <div class="panel">
            <h3>Nghỉ dưỡng & wellness</h3>
            <div class="list">
              <div>Suối khoáng nóng</div>
              <div>Resort ven biển</div>
              <div>Thiền và yoga</div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section id="planning">
      <div class="container">
        <div class="section-head">
          <h2>Lên kế hoạch</h2>
        </div>
        <div class="grid-2">
          <div class="panel">
            <h3>Thời điểm lý tưởng</h3>
            <p class="meta">Miền Bắc: thu mát, đông lạnh. Miền Trung: nắng ấm quanh năm, mưa bão theo mùa. Miền Nam: khô ráo tháng 12–4.</p>
          </div>
          <div class="panel">
            <h3>Di chuyển</h3>
            <p class="meta">Máy bay nội địa, tàu hoả Bắc–Nam, xe khách liên tỉnh, xe máy cho hành trình ngắn.</p>
          </div>
        </div>
      </div>
    </section>

    <section id="newsletter">
      <div class="container">
        <div class="newsletter">
          <div>
            <h2>Nhận bản tin gợi ý hành trình</h2>
            <p class="meta">Nhập email để nhận ý tưởng điểm đến và lịch trình cuối tuần.</p>
            <form class="searchbar" onsubmit="event.preventDefault()">
              <input type="email" required placeholder="Email của bạn">
              <button type="submit">Đăng ký</button>
            </form>
          </div>
          <div class="panel">
            <h3>Lợi ích</h3>
            <div class="list">
              <div>Lịch sự kiện theo mùa</div>
              <div>Gợi ý món ăn địa phương</div>
              <div>Ưu đãi phòng và vé</div>
            </div>
          </div>
        </div>
      </div>
    </section>
  </main>

  <footer>
    <div class="container footer-grid">
      <div>
        <div class="brand" style="margin-bottom:10px">
          <div class="brand-badge">VN</div>
          <div>Vietnam Travel</div>
        </div>
        <div class="meta">Nguồn cảm hứng và hướng dẫn du lịch Việt Nam.</div>
        <div class="fine">© 2025 Vietnam Travel Template. Không liên kết với vietnam.travel.</div>
      </div>
      <div>
        <h4>Khám phá</h4>
        <div class="list">
          <a href="#">Miền Bắc</a>
          <a href="#">Miền Trung</a>
          <a href="#">Miền Nam</a>
        </div>
      </div>
      <div>
        <h4>Lập kế hoạch</h4>
        <div class="list">
          <a href="#">Phương tiện</a>
          <a href="#">Lịch trình</a>
          <a href="#">Ngân sách</a>
        </div>
      </div>
      <div>
        <h4>Liên hệ</h4>
        <div class="list">
          <a href="#">Hỗ trợ</a>
          <a href="#">Hợp tác</a>
          <a href="#">Bản quyền</a>
        </div>
      </div>
    </div>
  </footer>
</body>
</html>
