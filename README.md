
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Aastha Traders — Premium Spice Exporters</title>
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,300;0,400;0,500;0,600;1,300;1,400&family=Montserrat:wght@300;400;500;600&display=swap" rel="stylesheet">
<style>
  *, *::before, *::after { margin: 0; padding: 0; box-sizing: border-box; }
  :root {
    --gold: #C9A84C;
    --gold-light: #E8D08A;
    --gold-dark: #8B6914;
    --cream: #FAF6EE;
    --dark: #1A1208;
    --dark2: #2E1F0A;
    --text: #3D2B0F;
    --muted: #7A6040;
    --border: rgba(201,168,76,0.25);
    --spice: #B85C1A;
  }
  html { scroll-behavior: smooth; }
  body { font-family: 'Montserrat', sans-serif; background: var(--cream); color: var(--text); overflow-x: hidden; }

  nav {
    position: fixed; top: 0; width: 100%; z-index: 100;
    background: rgba(26,18,8,0.96); backdrop-filter: blur(12px);
    border-bottom: 1px solid var(--border);
    padding: 0 5%;
    display: flex; align-items: center; justify-content: space-between; height: 70px;
  }
  .nav-logo { font-family: 'Cormorant Garamond', serif; font-size: 22px; font-weight: 600; color: var(--gold); letter-spacing: 2px; }
  .nav-logo span { color: #fff; font-weight: 300; }
  .nav-links { display: flex; gap: 36px; list-style: none; }
  .nav-links a { color: #ccc; font-size: 11px; letter-spacing: 2px; text-transform: uppercase; text-decoration: none; transition: color 0.3s; }
  .nav-links a:hover { color: var(--gold); }
  .nav-cta { background: var(--gold); color: var(--dark); font-size: 11px; letter-spacing: 2px; text-transform: uppercase; font-weight: 600; padding: 10px 22px; border: none; cursor: pointer; font-family: 'Montserrat', sans-serif; transition: background 0.3s; text-decoration: none; }
  .nav-cta:hover { background: var(--gold-light); }

  #home {
    min-height: 100vh; background: var(--dark);
    display: flex; align-items: center;
    position: relative; overflow: hidden; padding: 70px 5% 0;
  }
  .hero-bg {
    position: absolute; inset: 0; opacity: 0.08;
    background-image: repeating-linear-gradient(45deg, var(--gold) 0, var(--gold) 1px, transparent 0, transparent 50%);
    background-size: 30px 30px;
  }
  .hero-accent { position: absolute; right: 0; top: 0; bottom: 0; width: 42%; background: linear-gradient(135deg, #2E1F0A 0%, #1A1208 100%); border-left: 1px solid var(--border); }
  .hero-spice-circle {
    position: absolute; right: 5%; top: 50%; transform: translateY(-50%);
    width: 380px; height: 380px; border-radius: 50%;
    background: radial-gradient(circle at 40% 40%, #C9561A, #8B3A10, #3D1A05);
    display: flex; align-items: center; justify-content: center;
    box-shadow: 0 0 80px rgba(201,86,26,0.3), inset 0 0 60px rgba(0,0,0,0.4);
    font-size: 120px; text-align: center;
  }
  .hero-content { position: relative; z-index: 2; max-width: 560px; }
  .hero-tag { font-size: 10px; letter-spacing: 4px; text-transform: uppercase; color: var(--gold); margin-bottom: 20px; display: flex; align-items: center; gap: 12px; }
  .hero-tag::before { content: ''; display: block; width: 40px; height: 1px; background: var(--gold); }
  .hero-title { font-family: 'Cormorant Garamond', serif; font-size: clamp(48px, 6vw, 80px); font-weight: 300; color: #fff; line-height: 1.1; margin-bottom: 24px; }
  .hero-title em { color: var(--gold); font-style: italic; }
  .hero-sub { font-size: 13px; color: #aaa; line-height: 1.9; letter-spacing: 0.5px; margin-bottom: 40px; max-width: 440px; }
  .hero-btns { display: flex; gap: 16px; flex-wrap: wrap; }
  .btn-primary { background: var(--gold); color: var(--dark); font-size: 11px; letter-spacing: 2px; text-transform: uppercase; font-weight: 600; padding: 15px 36px; border: none; cursor: pointer; font-family: 'Montserrat', sans-serif; transition: all 0.3s; text-decoration: none; display: inline-block; }
  .btn-primary:hover { background: var(--gold-light); }
  .btn-outline { border: 1px solid var(--gold); color: var(--gold); font-size: 11px; letter-spacing: 2px; text-transform: uppercase; padding: 15px 36px; cursor: pointer; font-family: 'Montserrat', sans-serif; transition: all 0.3s; text-decoration: none; display: inline-block; background: transparent; }
  .btn-outline:hover { background: rgba(201,168,76,0.1); }
  .hero-stats { display: flex; gap: 48px; margin-top: 56px; padding-top: 40px; border-top: 1px solid rgba(201,168,76,0.2); }
  .stat-num { font-family: 'Cormorant Garamond', serif; font-size: 36px; font-weight: 600; color: var(--gold); }
  .stat-label { font-size: 10px; letter-spacing: 2px; text-transform: uppercase; color: #888; margin-top: 4px; }

  section { padding: 100px 5%; }
  .section-tag { font-size: 10px; letter-spacing: 4px; text-transform: uppercase; color: var(--gold); margin-bottom: 16px; display: flex; align-items: center; gap: 12px; }
  .section-tag::before { content: ''; display: block; width: 40px; height: 1px; background: var(--gold); }
  .section-title { font-family: 'Cormorant Garamond', serif; font-size: clamp(34px, 4vw, 52px); font-weight: 300; color: var(--dark); line-height: 1.2; margin-bottom: 20px; }
  .section-title em { color: var(--gold-dark); font-style: italic; }
  .divider { width: 60px; height: 1px; background: var(--gold); margin: 20px 0 40px; }

  #about { background: var(--cream); }
  .about-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 80px; align-items: center; }
  .about-text p { font-size: 14px; color: var(--muted); line-height: 2; margin-bottom: 16px; }
  .about-visual { background: var(--dark2); padding: 48px; position: relative; border: 1px solid var(--border); }
  .about-visual::before { content: ''; position: absolute; top: -1px; left: 40px; right: 40px; height: 3px; background: var(--gold); }
  .about-features { display: grid; grid-template-columns: 1fr 1fr; gap: 24px; }
  .feature-item { padding: 24px; border: 1px solid var(--border); }
  .feature-icon { font-size: 28px; margin-bottom: 12px; }
  .feature-title { font-size: 13px; font-weight: 600; color: var(--gold); letter-spacing: 1px; margin-bottom: 6px; }
  .feature-desc { font-size: 11px; color: #888; line-height: 1.7; }

  #products { background: var(--dark); }
  #products .section-title { color: #fff; }
  #products .section-tag { color: var(--gold-light); }
  #products .section-tag::before { background: var(--gold-light); }
  #products p.lead { color: #aaa; font-size: 14px; line-height: 2; max-width: 600px; margin-bottom: 60px; }
  .products-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 2px; }
  .product-card { background: var(--dark2); padding: 40px 32px; border: 1px solid var(--border); transition: all 0.3s; cursor: default; position: relative; overflow: hidden; }
  .product-card::after { content: ''; position: absolute; bottom: 0; left: 0; right: 0; height: 3px; background: var(--gold); transform: scaleX(0); transition: transform 0.3s; }
  .product-card:hover { border-color: var(--gold); }
  .product-card:hover::after { transform: scaleX(1); }
  .product-img-wrap { margin: -40px -32px 24px -32px; overflow: hidden; height: 180px; border-bottom: 2px solid var(--gold); }
  .product-img { width: 100%; height: 180px; object-fit: cover; display: block; filter: saturate(1.1) contrast(1.05); transition: transform 0.5s; }
  .product-card:hover .product-img { transform: scale(1.05); }
  .product-name { font-family: 'Cormorant Garamond', serif; font-size: 22px; font-weight: 500; color: #fff; margin-bottom: 8px; }
  .product-origin { font-size: 10px; letter-spacing: 2px; text-transform: uppercase; color: var(--gold); margin-bottom: 14px; }
  .product-desc { font-size: 12px; color: #888; line-height: 1.8; }
  .product-tags { display: flex; gap: 8px; margin-top: 20px; flex-wrap: wrap; }
  .tag { font-size: 9px; letter-spacing: 1.5px; text-transform: uppercase; border: 1px solid var(--border); color: #aaa; padding: 4px 10px; }

  #certificates { background: var(--cream); }
  .cert-intro { font-size: 14px; color: var(--muted); line-height: 2; max-width: 600px; margin-bottom: 60px; }
  .cert-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(220px, 1fr)); gap: 24px; }
  .cert-card { background: #fff; border: 1px solid var(--border); padding: 36px 28px; text-align: center; transition: border-color 0.3s; }
  .cert-card:hover { border-color: var(--gold); }
  .cert-badge { width: 70px; height: 70px; background: var(--dark); border-radius: 50%; display: flex; align-items: center; justify-content: center; margin: 0 auto 20px; font-size: 30px; border: 2px solid var(--gold); }
  .cert-name { font-family: 'Cormorant Garamond', serif; font-size: 18px; font-weight: 500; color: var(--dark); margin-bottom: 8px; }
  .cert-body { font-size: 10px; letter-spacing: 2px; text-transform: uppercase; color: var(--gold-dark); margin-bottom: 12px; }
  .cert-desc { font-size: 11px; color: var(--muted); line-height: 1.7; }

  #contact { background: var(--dark2); }
  #contact .section-title { color: #fff; }
  #contact .section-tag { color: var(--gold-light); }
  #contact .section-tag::before { background: var(--gold-light); }
  .contact-grid { display: grid; grid-template-columns: 1fr 1.4fr; gap: 80px; align-items: start; }
  .contact-info p { font-size: 13px; color: #aaa; line-height: 2; margin-bottom: 36px; }
  .contact-details { display: flex; flex-direction: column; gap: 20px; }
  .contact-item { display: flex; align-items: flex-start; gap: 16px; }
  .contact-icon { width: 40px; height: 40px; min-width: 40px; border: 1px solid var(--border); display: flex; align-items: center; justify-content: center; font-size: 16px; }
  .contact-label { font-size: 10px; letter-spacing: 2px; text-transform: uppercase; color: var(--gold); margin-bottom: 4px; }
  .contact-value { font-size: 13px; color: #ccc; }
  .whatsapp-btn { display: flex; align-items: center; gap: 10px; background: #25D366; color: #fff; padding: 14px 28px; font-size: 12px; letter-spacing: 1.5px; text-transform: uppercase; font-weight: 600; font-family: 'Montserrat', sans-serif; cursor: pointer; border: none; margin-top: 32px; transition: background 0.3s; width: fit-content; text-decoration: none; }
  .whatsapp-btn:hover { background: #1ebe5a; }
  .form-wrap { background: rgba(255,255,255,0.04); border: 1px solid var(--border); padding: 40px; }
  .form-row { display: grid; grid-template-columns: 1fr 1fr; gap: 16px; margin-bottom: 16px; }
  .form-group { margin-bottom: 16px; }
  .form-group label { display: block; font-size: 10px; letter-spacing: 2px; text-transform: uppercase; color: var(--gold); margin-bottom: 8px; }
  .form-group input, .form-group select, .form-group textarea {
    width: 100%; background: rgba(255,255,255,0.05); border: 1px solid var(--border);
    color: #fff; font-family: 'Montserrat', sans-serif; font-size: 13px;
    padding: 12px 16px; outline: none; transition: border-color 0.3s;
  }
  .form-group input:focus, .form-group select:focus, .form-group textarea:focus { border-color: var(--gold); }
  .form-group select option { background: var(--dark2); }
  .form-group textarea { resize: vertical; min-height: 110px; }
  .form-submit { background: var(--gold); color: var(--dark); font-size: 11px; letter-spacing: 2px; text-transform: uppercase; font-weight: 600; padding: 15px 40px; border: none; cursor: pointer; font-family: 'Montserrat', sans-serif; transition: background 0.3s; width: 100%; margin-top: 8px; }
  .form-submit:hover { background: var(--gold-light); }

  .map-section { background: var(--dark); padding: 0 5% 80px; }
  .map-label { font-size: 10px; letter-spacing: 3px; text-transform: uppercase; color: var(--gold); margin-bottom: 20px; display: flex; align-items: center; gap: 12px; }
  .map-label::before { content: ''; display: block; width: 40px; height: 1px; background: var(--gold); }
  .map-frame { border: 1px solid var(--border); overflow: hidden; height: 340px; }
  .map-frame iframe { width: 100%; height: 100%; border: none; filter: grayscale(0.3) contrast(1.1); }

  footer { background: var(--dark); border-top: 1px solid var(--border); padding: 40px 5%; }
  .footer-inner { display: flex; justify-content: space-between; align-items: center; flex-wrap: wrap; gap: 20px; }
  .footer-logo { font-family: 'Cormorant Garamond', serif; font-size: 20px; color: var(--gold); letter-spacing: 2px; }
  .footer-logo span { color: #666; font-weight: 300; }
  .footer-text { font-size: 11px; color: #555; }
  .footer-links { display: flex; gap: 24px; }
  .footer-links a { font-size: 10px; letter-spacing: 2px; text-transform: uppercase; color: #666; text-decoration: none; transition: color 0.3s; }
  .footer-links a:hover { color: var(--gold); }

  @media (max-width: 900px) {
    .about-grid, .contact-grid { grid-template-columns: 1fr; gap: 40px; }
    .products-grid { grid-template-columns: 1fr 1fr; }
    .hero-accent, .hero-spice-circle { display: none; }
    .form-row { grid-template-columns: 1fr; }
    .nav-links { display: none; }
  }
  @media (max-width: 600px) {
    .products-grid { grid-template-columns: 1fr; }
    .cert-grid { grid-template-columns: 1fr 1fr; }
  }
</style>
</head>
<body>

<nav>
  <div class="nav-logo">Aastha <span>Traders</span></div>
  <ul class="nav-links">
    <li><a href="#home">Home</a></li>
    <li><a href="#about">About</a></li>
    <li><a href="#products">Products</a></li>
    <li><a href="#certificates">Certificates</a></li>
    <li><a href="#contact">Contact</a></li>
  </ul>
  <a href="#contact" class="nav-cta">Get a Quote</a>
</nav>

<section id="home">
  <div class="hero-bg"></div>
  <div class="hero-accent"></div>
  <div class="hero-content">
    <div class="hero-tag">Premium Spice Exporters · Est. India</div>
    <h1 class="hero-title">The World's Finest<br><em>Indian Spices</em><br>at Your Door</h1>
    <p class="hero-sub">Aastha Traders is a trusted import-export house specialising in premium Indian spices. From the golden fields of turmeric to aromatic blends, we connect global markets with the finest produce.</p>
    <div class="hero-btns">
      <a href="#products" class="btn-primary">Explore Products</a>
      <a href="#contact" class="btn-outline">Request a Quote</a>
    </div>
    <div class="hero-stats">
      <div><div class="stat-num">15+</div><div class="stat-label">Countries Served</div></div>
      <div><div class="stat-num">50+</div><div class="stat-label">Spice Varieties</div></div>
      <div><div class="stat-num">100%</div><div class="stat-label">Quality Certified</div></div>
    </div>
  </div>
  <div class="hero-spice-circle">🌿</div>
</section>

<section id="about">
  <div class="about-grid">
    <div class="about-text">
      <div class="section-tag">Our Story</div>
      <h2 class="section-title">Rooted in Tradition,<br><em>Driven by Quality</em></h2>
      <div class="divider"></div>
      <p>Aastha Traders is a premier Indian import-export enterprise with deep roots in the rich spice-growing heartlands of India. Our name — Aastha, meaning faith — reflects our unwavering commitment to integrity, quality, and trust.</p>
      <p>We source directly from certified farmers and cooperatives, ensuring that every batch of spice we export carries the authentic aroma, colour, and potency that India is renowned for globally.</p>
      <p>Whether you are a food manufacturer, retail brand, or wholesaler, we offer seamless end-to-end export solutions with full regulatory compliance and documentation support.</p>
    </div>
    <div class="about-visual">
      <div class="about-features">
        <div class="feature-item">
          <div class="feature-icon">🌾</div>
          <div class="feature-title">Farm-Direct Sourcing</div>
          <div class="feature-desc">Traceable supply chain direct from certified farms across India</div>
        </div>
        <div class="feature-item">
          <div class="feature-icon">🔬</div>
          <div class="feature-title">Lab Tested</div>
          <div class="feature-desc">Every lot tested for purity, moisture, and contamination</div>
        </div>
        <div class="feature-item">
          <div class="feature-icon">📦</div>
          <div class="feature-title">Custom Packaging</div>
          <div class="feature-desc">Flexible packaging solutions — bulk or retail-ready formats</div>
        </div>
        <div class="feature-item">
          <div class="feature-icon">🚢</div>
          <div class="feature-title">Global Logistics</div>
          <div class="feature-desc">Reliable sea and air freight to 15+ countries worldwide</div>
        </div>
      </div>
    </div>
  </div>
</section>

<section id="products">
  <div class="section-tag">Our Range</div>
  <h2 class="section-title">Premium <em>Export Spices</em></h2>
  <div class="divider" style="background:var(--gold-light);"></div>
  <p class="lead">We specialise in sourcing, processing, and exporting the finest Indian spices, tailored to international food safety and quality standards.</p>
  <div class="products-grid">
    <div class="product-card">
      <div class="product-img-wrap"><img class="product-img" src="https://upload.wikimedia.org/wikipedia/commons/thumb/6/6c/Turmeric-Powder-and-Roots.jpg/1280px-Turmeric-Powder-and-Roots.jpg" alt="Turmeric" onerror="this.parentElement.style.background='#3D1A05';this.style.display='none'"></div>
      <div class="product-name">Turmeric</div>
      <div class="product-origin">Erode · Salem · Nizamabad</div>
      <div class="product-desc">High curcumin content (3–5%). Available in finger, bulb, and powder forms. APEDA certified, preferred by food and pharma industries globally.</div>
      <div class="product-tags"><span class="tag">Curcumin 3–5%</span><span class="tag">Organic Available</span><span class="tag">Bulk & Retail</span></div>
    </div>
    <div class="product-card">
      <div class="product-img-wrap"><img class="product-img" src="https://upload.wikimedia.org/wikipedia/commons/thumb/5/59/Chilli_variety.jpg/1280px-Chilli_variety.jpg" alt="Red Chilli" onerror="this.parentElement.style.background='#3D1A05';this.style.display='none'"></div>
      <div class="product-name">Red Chilli</div>
      <div class="product-origin">Guntur · Byadgi · Warangal</div>
      <div class="product-desc">Variety-specific export — Guntur Sannam, Byadgi, Teja. Available whole, crushed, or powdered with customisable heat levels (SHU).</div>
      <div class="product-tags"><span class="tag">Variety-Specific</span><span class="tag">High Colour</span><span class="tag">Steam Sterilised</span></div>
    </div>
    <div class="product-card">
      <div class="product-img-wrap"><img class="product-img" src="https://upload.wikimedia.org/wikipedia/commons/thumb/f/fd/Coriander_seeds.jpg/1280px-Coriander_seeds.jpg" alt="Coriander" onerror="this.parentElement.style.background='#3D1A05';this.style.display='none'"></div>
      <div class="product-name">Coriander</div>
      <div class="product-origin">Rajasthan · Madhya Pradesh</div>
      <div class="product-desc">Eagle and Scooter varieties. Rich in essential oils, strong aroma. Supplied as seeds, split, or powder — machine-cleaned and sortex processed.</div>
      <div class="product-tags"><span class="tag">Eagle & Scooter</span><span class="tag">Sortex Clean</span><span class="tag">High Oil</span></div>
    </div>
    <div class="product-card">
      <div class="product-img-wrap"><img class="product-img" src="https://upload.wikimedia.org/wikipedia/commons/thumb/1/11/Cumin_seeds.jpg/1280px-Cumin_seeds.jpg" alt="Cumin" onerror="this.parentElement.style.background='#3D1A05';this.style.display='none'"></div>
      <div class="product-name">Cumin (Jeera)</div>
      <div class="product-origin">Gujarat · Rajasthan</div>
      <div class="product-desc">Premium Unjha and Singapore cumin with rich volatile oils. EU-grade microbiological standards. Available machine-clean or double-sortex.</div>
      <div class="product-tags"><span class="tag">EU-Grade</span><span class="tag">Double Sortex</span><span class="tag">Low Moisture</span></div>
    </div>
    <div class="product-card">
      <div class="product-img-wrap"><img class="product-img" src="https://upload.wikimedia.org/wikipedia/commons/thumb/3/3c/Black_peppercorns.jpg/1280px-Black_peppercorns.jpg" alt="Black Pepper" onerror="this.parentElement.style.background='#3D1A05';this.style.display='none'"></div>
      <div class="product-name">Black Pepper</div>
      <div class="product-origin">Kerala · Karnataka</div>
      <div class="product-desc">Bold 500/550 g/l density, high piperine content. Available as whole, cracked, and ground. Meets FDA, FSSAI, and EU pesticide residue norms.</div>
      <div class="product-tags"><span class="tag">550 G/L Bold</span><span class="tag">High Piperine</span><span class="tag">FDA Compliant</span></div>
    </div>
    <div class="product-card">
      <div class="product-img-wrap"><img class="product-img" src="https://upload.wikimedia.org/wikipedia/commons/thumb/f/f8/Fenugreek_seeds.jpg/1280px-Fenugreek_seeds.jpg" alt="Fenugreek" onerror="this.parentElement.style.background='#3D1A05';this.style.display='none'"></div>
      <div class="product-name">Fenugreek</div>
      <div class="product-origin">Rajasthan · Gujarat</div>
      <div class="product-desc">Premium fenugreek seeds and powder rich in saponins and fibre. Widely exported for food, nutraceutical, and cosmetic applications.</div>
      <div class="product-tags"><span class="tag">Nutraceutical Grade</span><span class="tag">Powder & Seeds</span><span class="tag">Rich in Saponins</span></div>
    </div>
  </div>
</section>

<section id="certificates">
  <div class="section-tag">Compliance & Trust</div>
  <h2 class="section-title">Our <em>Certifications</em></h2>
  <div class="divider"></div>
  <p class="cert-intro">Aastha Traders operates with full regulatory compliance and internationally recognised certifications, giving our partners complete confidence in every consignment.</p>
  <div class="cert-grid">
    <div class="cert-card">
      <div class="cert-badge">🏛️</div>
      <div class="cert-name">APEDA Registration</div>
      <div class="cert-body">Agricultural & Processed Food Products</div>
      <div class="cert-desc">Registered with the Agricultural and Processed Food Products Export Development Authority, Government of India.</div>
    </div>
    <div class="cert-card">
      <div class="cert-badge">🌿</div>
      <div class="cert-name">FSSAI Licence</div>
      <div class="cert-body">Food Safety & Standards</div>
      <div class="cert-desc">Fully licensed under the Food Safety and Standards Authority of India for food processing and export operations.</div>
    </div>
    <div class="cert-card">
      <div class="cert-badge">✅</div>
      <div class="cert-name">ISO 22000</div>
      <div class="cert-body">Food Safety Management</div>
      <div class="cert-desc">Certified food safety management system ensuring end-to-end traceability and hazard control across the supply chain.</div>
    </div>
    <div class="cert-card">
      <div class="cert-badge">🌱</div>
      <div class="cert-name">Organic Certificate</div>
      <div class="cert-body">NPOP / NOP Certified</div>
      <div class="cert-desc">Certified organic produce available under National Programme for Organic Production (India) and USDA NOP standards.</div>
    </div>
    <div class="cert-card">
      <div class="cert-badge">🔬</div>
      <div class="cert-name">Phytosanitary Cert.</div>
      <div class="cert-body">Plant Quarantine Authority</div>
      <div class="cert-desc">Every shipment is accompanied by a phytosanitary certificate issued by the Plant Quarantine Authority of India.</div>
    </div>
    <div class="cert-card">
      <div class="cert-badge">🚢</div>
      <div class="cert-name">IEC Code</div>
      <div class="cert-body">Import Export Code · DGFT</div>
      <div class="cert-desc">Import Export Code issued by DGFT, Ministry of Commerce, Government of India — a mandatory credential for all exporters.</div>
    </div>
  </div>
</section>

<section id="contact">
  <div class="contact-grid">
    <div class="contact-info">
      <div class="section-tag">Get In Touch</div>
      <h2 class="section-title">Request a <em>Quote</em></h2>
      <div class="divider" style="background:var(--gold-light);"></div>
      <p>Reach out to us for pricing, product specifications, samples, or any trade enquiry. Our team typically responds within 24 hours.</p>
      <div class="contact-details">
        <div class="contact-item">
          <div class="contact-icon">📍</div>
          <div>
            <div class="contact-label">Address</div>
            <div class="contact-value">Aastha Traders, Pune, Maharashtra, India</div>
          </div>
        </div>
        <div class="contact-item">
          <div class="contact-icon">📞</div>
          <div>
            <div class="contact-label">Phone</div>
            <div class="contact-value">+91 90219 48353</div>
          </div>
        </div>
        <div class="contact-item">
          <div class="contact-icon">✉️</div>
          <div>
            <div class="contact-label">Email</div>
            <div class="contact-value">alexpillai24@aasthatraders.in</div>
          </div>
        </div>
      </div>
      <a href="https://wa.me/919021948353" class="whatsapp-btn" target="_blank">
        <svg width="18" height="18" viewBox="0 0 24 24" fill="currentColor"><path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347m-5.421 7.403h-.004a9.87 9.87 0 01-5.031-1.378l-.361-.214-3.741.982.998-3.648-.235-.374a9.86 9.86 0 01-1.51-5.26c.001-5.45 4.436-9.884 9.888-9.884 2.64 0 5.122 1.03 6.988 2.898a9.825 9.825 0 012.893 6.994c-.003 5.45-4.437 9.884-9.885 9.884m8.413-18.297A11.815 11.815 0 0012.05 0C5.495 0 .16 5.335.157 11.892c0 2.096.547 4.142 1.588 5.945L.057 24l6.305-1.654a11.882 11.882 0 005.683 1.448h.005c6.554 0 11.89-5.335 11.893-11.893a11.821 11.821 0 00-3.48-8.413z"/></svg>
        Chat on WhatsApp
      </a>
    </div>
    <div class="form-wrap">
      <div class="form-row">
        <div class="form-group">
          <label>Your Name</label>
          <input type="text" placeholder="Full name">
        </div>
        <div class="form-group">
          <label>Company</label>
          <input type="text" placeholder="Company name">
        </div>
      </div>
      <div class="form-row">
        <div class="form-group">
          <label>Email Address</label>
          <input type="email" placeholder="email@company.com">
        </div>
        <div class="form-group">
          <label>Country</label>
          <input type="text" placeholder="Destination country">
        </div>
      </div>
      <div class="form-group">
        <label>Product of Interest</label>
        <select>
          <option value="">Select a product</option>
          <option>Turmeric (Finger / Powder)</option>
          <option>Red Chilli (Guntur / Byadgi)</option>
          <option>Coriander Seeds / Powder</option>
          <option>Cumin (Jeera)</option>
          <option>Black Pepper</option>
          <option>Fenugreek</option>
          <option>Mixed / Multiple Products</option>
        </select>
      </div>
      <div class="form-group">
        <label>Approximate Quantity (MT/Month)</label>
        <input type="text" placeholder="e.g. 5 MT / month">
      </div>
      <div class="form-group">
        <label>Message / Specifications</label>
        <textarea placeholder="Tell us about your requirements — grade, packaging, certifications needed, delivery terms, etc."></textarea>
      </div>
      <button class="form-submit">Send Enquiry →</button>
    </div>
  </div>
</section>

<div class="map-section">
  <div class="map-label">Our Location — Pune, Maharashtra</div>
  <div class="map-frame">
    <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d242120.11365594485!2d73.72468!3d18.5204303!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x3bc2bf2e67461101%3A0x828d43bf9d9ee343!2sPune%2C%20Maharashtra!5e0!3m2!1sen!2sin!4v1711000000000!5m2!1sen!2sin" allowfullscreen loading="lazy"></iframe>
  </div>
</div>

<footer>
  <div class="footer-inner">
    <div class="footer-logo">Aastha <span>Traders</span></div>
    <div class="footer-text">© 2025 Aastha Traders. Premium Spice Exporters, Pune, India. | aasthatraders.in</div>
    <div class="footer-links">
      <a href="#home">Home</a>
      <a href="#products">Products</a>
    
