<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="theme-color" content="#10150f">
  <meta name="description" content="Ammie Camp TV — music, entertainment, interviews, lifestyle and fresh talent.">
  <title>Ammie Camp TV | Discover Talent. Inspire Creativity.</title>
  <style>
    :root {
      --bg: #090b09;
      --panel: #121812;
      --panel-2: #192219;
      --green: #263d2b;
      --red: #e34b58;
      --cream: #f4f1e9;
      --muted: #b9c0b5;
      --line: rgba(255,255,255,.12);
      --max: 1160px;
    }
    * { box-sizing: border-box; }
    html { scroll-behavior: smooth; }
    body {
      margin: 0; background: var(--bg); color: var(--cream);
      font-family: Inter, ui-sans-serif, system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
      line-height: 1.6;
    }
    a { color: inherit; text-decoration: none; }
    img { display: block; max-width: 100%; }
    .wrap { width: min(var(--max), calc(100% - 40px)); margin-inline: auto; }
    .topbar {
      position: sticky; top: 0; z-index: 20; background: rgba(9,11,9,.92);
      backdrop-filter: blur(14px); border-bottom: 1px solid var(--line);
    }
    .nav { min-height: 74px; display: flex; align-items: center; justify-content: space-between; gap: 24px; }
    .brand { font-size: 1.12rem; font-weight: 900; letter-spacing: .09em; }
    .brand span { color: var(--red); }
    .navlinks { display: flex; align-items: center; gap: 28px; color: var(--muted); font-size: .93rem; }
    .navlinks a:hover { color: white; }
    .nav-cta, .btn {
      display: inline-flex; align-items: center; justify-content: center; gap: 9px;
      border-radius: 7px; padding: 11px 17px; font-weight: 750; font-size: .9rem;
      transition: transform .2s, background .2s;
    }
    .nav-cta, .btn-primary { background: var(--red); color: white; }
    .btn:hover, .nav-cta:hover { transform: translateY(-2px); }
    .menu-btn { display: none; border: 1px solid var(--line); background: var(--panel); color: white; border-radius: 7px; padding: 9px 12px; font-size: 1.2rem; }
    .hero {
      min-height: 590px; display: grid; align-items: center; position: relative; overflow: hidden;
      background:
        linear-gradient(90deg, rgba(7,10,7,.97) 0%, rgba(7,10,7,.86) 48%, rgba(7,10,7,.28) 100%),
        linear-gradient(0deg, rgba(7,10,7,.7), transparent 55%),
        url("ammie.jpg") center/cover no-repeat;
    }
    .hero-inner { padding-block: 90px; max-width: 720px; }
    .eyebrow { color: #f08a91; text-transform: uppercase; letter-spacing: .19em; font-weight: 800; font-size: .75rem; }
    h1 { font-size: clamp(2.65rem, 6vw, 5.2rem); line-height: 1.02; letter-spacing: -.045em; margin: 17px 0 20px; }
    h1 span { color: var(--red); }
    .hero p { color: #d2d6ce; font-size: clamp(1rem, 2vw, 1.2rem); max-width: 590px; margin: 0 0 28px; }
    .actions { display: flex; flex-wrap: wrap; gap: 12px; }
    .btn-outline { border: 1px solid rgba(255,255,255,.38); color: white; }
    .section { padding: 82px 0; }
    .section-head { display: flex; justify-content: space-between; align-items: end; gap: 20px; margin-bottom: 28px; }
    .kicker { color: var(--red); text-transform: uppercase; letter-spacing: .16em; font-weight: 800; font-size: .72rem; }
    h2 { font-size: clamp(1.8rem, 4vw, 2.8rem); line-height: 1.1; letter-spacing: -.03em; margin: 8px 0 0; }
    .section-intro { color: var(--muted); max-width: 600px; margin: 14px 0 0; }
    .about-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 42px; align-items: center; }
    .about-panel { background: linear-gradient(145deg, var(--panel-2), var(--panel)); border: 1px solid var(--line); border-radius: 16px; padding: 32px; }
    .about-panel p { color: var(--muted); margin-bottom: 0; }
    .stat-row { display: grid; grid-template-columns: repeat(3,1fr); gap: 12px; margin-top: 24px; }
    .stat { background: rgba(255,255,255,.04); border: 1px solid var(--line); padding: 15px; border-radius: 10px; }
    .stat strong { display: block; color: white; font-size: 1.15rem; }
    .stat small { color: var(--muted); }
    .feature-art {
      min-height: 330px; border-radius: 16px; border: 1px solid var(--line);
      background: radial-gradient(circle at 70% 25%, rgba(227,75,88,.42), transparent 28%),
                  linear-gradient(135deg, #263d2b, #10150f 65%);
      display: grid; place-items: center; text-align: center; padding: 30px;
    }
    .feature-art strong { font-size: clamp(2rem, 5vw, 3.6rem); line-height: 1.05; letter-spacing: -.05em; }
    .feature-art span { display: block; color: #f08a91; letter-spacing: .2em; font-size: .75rem; margin-top: 12px; font-weight: 800; }
    .cards { display: grid; grid-template-columns: repeat(3,1fr); gap: 18px; }
    .card { overflow: hidden; border: 1px solid var(--line); background: var(--panel); border-radius: 13px; }
    .card-visual { aspect-ratio: 16/10; display: grid; place-items: center; background: linear-gradient(135deg, #263d2b, #121812); color: #f08a91; font-size: 2.5rem; }
    .card-body { padding: 20px; }
    .card h3 { margin: 0 0 7px; font-size: 1.15rem; }
    .card p { color: var(--muted); font-size: .93rem; margin: 0 0 14px; }
    .text-link { color: #f08a91; font-weight: 750; font-size: .9rem; }
    .social { background: linear-gradient(135deg, #192719, #10150f); border-block: 1px solid var(--line); }
    .social-row { display: flex; flex-wrap: wrap; gap: 12px; margin-top: 25px; }
    .social-link { border: 1px solid var(--line); background: rgba(255,255,255,.05); border-radius: 8px; padding: 12px 17px; font-weight: 750; }
    .social-link:hover { border-color: var(--red); }
    .contact-box { background: var(--panel); border: 1px solid var(--line); border-radius: 15px; padding: 30px; display: flex; justify-content: space-between; align-items: center; gap: 25px; }
    .contact-box p { color: var(--muted); margin-bottom: 0; }
    footer { padding: 28px 0; color: var(--muted); border-top: 1px solid var(--line); font-size: .88rem; }
    .footer-row { display: flex; justify-content: space-between; gap: 18px; flex-wrap: wrap; }
    @media (max-width: 760px) {
      .wrap { width: min(100% - 32px, var(--max)); }
      .nav { min-height: 64px; }
      .menu-btn { display: inline-flex; }
      .nav-cta { display: none; }
      .navlinks {
        display: none; position: absolute; top: 64px; left: 0; right: 0; padding: 18px 22px 22px;
        background: #10150f; border-bottom: 1px solid var(--line); flex-direction: column; align-items: stretch; gap: 0;
      }
      .navlinks.open { display: flex; }
      .navlinks a { padding: 12px 4px; border-bottom: 1px solid var(--line); }
      .hero { min-height: 560px; background-position: 62% center; }
      .hero-inner { padding-block: 76px; }
      .hero p { max-width: 480px; }
      .section { padding: 62px 0; }
      .about-grid { grid-template-columns: 1fr; gap: 20px; }
      .feature-art { min-height: 240px; }
      .cards { grid-template-columns: 1fr; }
      .card-visual { aspect-ratio: 16/7; }
      .section-head { display: block; }
      .contact-box { display: block; }
      .contact-box .btn { margin-top: 20px; }
      .stat-row { gap: 8px; }
      .stat { padding: 12px 9px; }
    }
    @media (max-width: 380px) {
      .hero { min-height: 520px; }
      .actions .btn { width: 100%; }
      .about-panel { padding: 23px; }
    }
  </style>
</head>
<body>
  <div class="topbar">
    <div class="wrap nav">
      <a class="brand" href="#home"><span>AMMIE</span> CAMP TV</a>
      <button class="menu-btn" id="menuBtn" aria-label="Open navigation" aria-expanded="false">☰</button>
      <nav class="navlinks" id="navLinks" aria-label="Main navigation">
        <a href="#home">Home</a><a href="#about">About</a><a href="#shows">What We Do</a><a href="#social">Follow Us</a><a href="#contact">Contact</a>
      </nav>
      <a class="nav-cta" href="https://www.youtube.com/@AMMIECAMPTV" target="_blank" rel="noopener">Watch our channel ↗</a>
    </div>
  </div>

  <main>
    <section class="hero" id="home">
      <div class="wrap">
        <div class="hero-inner">
          <div class="eyebrow">Music · Entertainment · Lifestyle</div>
          <h1>Discover talent.<br><span>Inspire creativity.</span></h1>
          <p>A home for music, interviews, lifestyle, events and fresh talent. We give young creators a platform to shine and share their stories with the world.</p>
          <div class="actions">
            <a class="btn btn-primary" href="#shows">Explore Ammie Camp</a>
            <a class="btn btn-outline" href="#contact">Join our talent community</a>
          </div>
        </div>
      </div>
    </section>

    <section class="section" id="about">
      <div class="wrap about-grid">
        <div>
          <div class="kicker">Who we are</div>
          <h2>A platform for the next generation.</h2>
          <p class="section-intro">Ammie Wyz Camp is an entertainment and talent-development platform dedicated to discovering, supporting and promoting young talent.</p>
          <p class="section-intro">Through our media platforms, we showcase creativity, music, interviews, events and inspiring stories—giving young people an opportunity to share their gifts with the world.</p>
          <div class="stat-row">
            <div class="stat"><strong>Talent</strong><small>Discovery</small></div>
            <div class="stat"><strong>Stories</strong><small> & Culture</small></div>
            <div class="stat"><strong>Creativity</strong><small> & Growth</small></div>
          </div>
        </div>
        <div class="feature-art">
          <div><strong>AMMIE<br>CAMP TV</strong><span>YOUR VOICE. YOUR STAGE.</span></div>
        </div>
      </div>
    </section>

    <section class="section" id="shows">
      <div class="wrap">
        <div class="section-head">
          <div><div class="kicker">Explore our world</div><h2>What happens at Ammie Camp</h2></div>
          <p class="section-intro">Real people, fresh ideas and stories worth sharing.</p>
        </div>
        <div class="cards">
          <article class="card"><div class="card-visual">♫</div><div class="card-body"><h3>Music & Freestyles</h3><p>Discover upcoming artists, performances and new sounds.</p><a class="text-link" href="https://www.youtube.com/@AMMIECAMPTV" target="_blank" rel="noopener">Watch on YouTube ↗</a></div></article>
          <article class="card"><div class="card-visual">◉</div><div class="card-body"><h3>Interviews & Stories</h3><p>Meet creators and hear the stories behind their journeys.</p><a class="text-link" href="https://www.youtube.com/@AMMIECAMPTV" target="_blank" rel="noopener">Explore interviews ↗</a></div></article>
          <article class="card"><div class="card-visual">✦</div><div class="card-body"><h3>Lifestyle & Events</h3><p>Street culture, experiences, food, events and everyday life.</p><a class="text-link" href="https://www.tiktok.com/@ammiewyzcamptv" target="_blank" rel="noopener">See our videos ↗</a></div></article>
        </div>
      </div>
    </section>

    <section class="section social" id="social">
      <div class="wrap">
        <div class="kicker">Stay connected</div>
        <h2>Follow Ammie Camp TV</h2>
        <p class="section-intro">Follow our channels for music, interviews, events and the latest entertainment.</p>
        <div class="social-row">
          <a class="social-link" href="https://www.youtube.com/@AMMIECAMPTV" target="_blank" rel="noopener">▶ YouTube</a>
          <a class="social-link" href="https://www.tiktok.com/@ammiewyzcamptv" target="_blank" rel="noopener">♪ TikTok</a>
          <a class="social-link" href="https://www.facebook.com/share/1cT5cwFAQt/" target="_blank" rel="noopener">f Facebook</a>
        </div>
      </div>
    </section>

    <section class="section" id="contact">
      <div class="wrap">
        <div class="contact-box">
          <div><div class="kicker">Let's work together</div><h2>Have talent or a project?</h2><p>Artists, young creators and partners are welcome. Get in touch and let's create something meaningful.</p></div>
          <a class="btn btn-primary" href="mailto:ammiewyz@gmail.com">Contact Ammie Camp ↗</a>
        </div>
      </div>
    </section>
  </main>

  <footer>
    <div class="wrap footer-row"><span><strong>AMMIE CAMP TV</strong> · Discover Talent. Inspire Creativity.</span><span>© 2026 Ammie Camp. All rights reserved.</span></div>
  </footer>

  <script>
    const menuBtn = document.getElementById('menuBtn');
    const navLinks = document.getElementById('navLinks');
    menuBtn.addEventListener('click', () => {
      const open = navLinks.classList.toggle('open');
      menuBtn.setAttribute('aria-expanded', String(open));
      menuBtn.textContent = open ? '✕' : '☰';
    });
    navLinks.querySelectorAll('a').forEach(link => link.addEventListener('click', () => {
      navLinks.classList.remove('open');
      menuBtn.setAttribute('aria-expanded', 'false');
      menuBtn.textContent = '☰';
    }));
  </script>
</body>
</html>
