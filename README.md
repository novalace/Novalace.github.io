# Novalace.github.io
Website
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>NovaLace — Fairy-tale finds for modern castles</title>
  <link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,400;0,600;1,400&family=Great+Vibes&display=swap" rel="stylesheet">
  <style>
    :root {
      --lavender: #c9b1ff;
      --blush: #f8c4d8;
      --gold: #f0d9a8;
      --deep: #2a1b3d;
      --soft-purple: #e8deff;
      --glow: 0 0 20px rgba(201, 177, 255, 0.4);
    }

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: 'Cormorant Garamond', serif;
      background: linear-gradient(135deg, #1a1025 0%, #2a1b3d 40%, #3d2a5a 100%);
      color: #f8f0ff;
      line-height: 1.6;
      overflow-x: hidden;
    }

    /* Glitter background effect */
    body::before {
      content: "";
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background-image: 
        radial-gradient(1.5px 1.5px at 20px 30px, #fff, transparent),
        radial-gradient(1.5px 1.5px at 40px 70px, rgba(240, 217, 168, 0.8), transparent),
        radial-gradient(1.5px 1.5px at 90px 40px, rgba(201, 177, 255, 0.7), transparent),
        radial-gradient(1.5px 1.5px at 130px 80px, #fff, transparent),
        radial-gradient(1.5px 1.5px at 160px 120px, rgba(248, 196, 216, 0.6), transparent);
      background-size: 200px 200px;
      animation: glitter 8s linear infinite;
      pointer-events: none;
      z-index: 0;
      opacity: 0.6;
    }

    @keyframes glitter {
      from { transform: translateY(0); }
      to { transform: translateY(-200px); }
    }

    .container {
      max-width: 1100px;
      margin: 0 auto;
      padding: 0 24px;
      position: relative;
      z-index: 1;
    }

    /* Header */
    header {
      padding: 30px 0;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }

    .logo {
      font-family: 'Great Vibes', cursive;
      font-size: 2.8rem;
      background: linear-gradient(90deg, #f0d9a8, #c9b1ff, #f8c4d8);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      text-shadow: var(--glow);
      letter-spacing: 1px;
    }

    nav a {
      color: #f0d9a8;
      text-decoration: none;
      margin-left: 32px;
      font-size: 1.15rem;
      letter-spacing: 1px;
      transition: all 0.3s ease;
      position: relative;
    }

    nav a::after {
      content: "";
      position: absolute;
      bottom: -4px;
      left: 0;
      width: 0;
      height: 1px;
      background: var(--lavender);
      transition: width 0.3s ease;
    }

    nav a:hover::after {
      width: 100%;
    }

    /* Hero */
    .hero {
      text-align: center;
      padding: 100px 0 120px;
    }

    .hero h1 {
      font-family: 'Great Vibes', cursive;
      font-size: 5.5rem;
      background: linear-gradient(90deg, #f0d9a8, #e8deff, #f8c4d8, #c9b1ff);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      margin-bottom: 16px;
      text-shadow: 0 0 40px rgba(201, 177, 255, 0.5);
      animation: glowPulse 4s ease-in-out infinite alternate;
    }

    @keyframes glowPulse {
      from { filter: brightness(1); }
      to { filter: brightness(1.15); }
    }

    .tagline {
      font-size: 1.6rem;
      color: var(--gold);
      letter-spacing: 3px;
      margin-bottom: 40px;
      font-style: italic;
    }

    .hero p {
      max-width: 600px;
      margin: 0 auto 50px;
      font-size: 1.25rem;
      color: #e0d0ff;
    }

    .btn {
      display: inline-block;
      padding: 16px 42px;
      background: linear-gradient(135deg, #c9b1ff, #f8c4d8);
      color: #2a1b3d;
      text-decoration: none;
      border-radius: 50px;
      font-size: 1.15rem;
      font-weight: 600;
      letter-spacing: 1px;
      box-shadow: 0 0 30px rgba(201, 177, 255, 0.5);
      transition: all 0.3s ease;
    }

    .btn:hover {
      transform: translateY(-3px);
      box-shadow: 0 0 40px rgba(248, 196, 216, 0.7);
    }

    /* Sections */
    section {
      padding: 90px 0;
    }

    .section-title {
      text-align: center;
      font-family: 'Great Vibes', cursive;
      font-size: 3.2rem;
      margin-bottom: 16px;
      background: linear-gradient(90deg, #f0d9a8, #c9b1ff);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
    }

    .section-subtitle {
      text-align: center;
      color: var(--gold);
      font-size: 1.2rem;
      margin-bottom: 60px;
      letter-spacing: 2px;
    }

    /* Product Grid */
    .products {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
      gap: 40px;
    }

    .product-card {
      background: rgba(255, 255, 255, 0.05);
      border: 1px solid rgba(201, 177, 255, 0.2);
      border-radius: 20px;
      padding: 30px;
      text-align: center;
      backdrop-filter: blur(10px);
      transition: all 0.4s ease;
      position: relative;
      overflow: hidden;
    }

    .product-card::before {
      content: "";
      position: absolute;
      top: -50%;
      left: -50%;
      width: 200%;
      height: 200%;
      background: radial-gradient(circle, rgba(201, 177, 255, 0.1) 0%, transparent 70%);
      opacity: 0;
      transition: opacity 0.4s ease;
    }

    .product-card:hover {
      transform: translateY(-10px);
      border-color: var(--lavender);
      box-shadow: 0 15px 40px rgba(201, 177, 255, 0.2);
    }

    .product-card:hover::before {
      opacity: 1;
    }

    .product-card h3 {
      font-size: 1.6rem;
      margin: 20px 0 10px;
      color: var(--gold);
    }

    .product-card p {
      color: #d0c0f0;
      font-size: 1.1rem;
    }

    .price {
      display: block;
      margin-top: 18px;
      font-size: 1.3rem;
      color: var(--blush);
    }

    /* About */
    .about-content {
      max-width: 700px;
      margin: 0 auto;
      text-align: center;
      font-size: 1.3rem;
      color: #e8deff;
    }

    /* Footer */
    footer {
      text-align: center;
      padding: 60px 0 40px;
      border-top: 1px solid rgba(201, 177, 255, 0.15);
      margin-top: 40px;
    }

    footer .logo {
      font-size: 2.2rem;
      margin-bottom: 12px;
    }

    footer p {
      color: #b0a0d0;
      font-size: 1rem;
    }

    /* Responsive */
    @media (max-width: 768px) {
      .hero h1 {
        font-size: 3.5rem;
      }
      nav {
        display: none;
      }
      .logo {
        font-size: 2.2rem;
      }
    }
  </style>
</head>
<body>
  <div class="container">
    <!-- Header -->
    <header>
      <div class="logo">NovaLace</div>
      <nav>
        <a href="#home">Home</a>
        <a href="#collection">Collection</a>
        <a href="#about">Our Story</a>
        <a href="#contact">Contact</a>
      </nav>
    </header>

    <!-- Hero -->
    <section class="hero" id="home">
      <h1>NovaLace</h1>
      <p class="tagline">Fairy-tale finds for modern castles</p>
      <p>Soft, personalized pieces that feel like they wandered out of a storybook. Wall hangings, mirrors, quiet objects, and little enchantments made to live with you.</p>
      <a href="#collection" class="btn">Explore the Collection</a>
    </section>

    <!-- Collection -->
    <section id="collection">
      <h2 class="section-title">The Collection</h2>
      <p class="section-subtitle">Quiet magic for every corner</p>
      
      <div class="products">
        <div class="product-card">
          <div style="font-size: 3rem;">🪞</div>
          <h3>Dream Mirrors</h3>
          <p>Personalized wall mirrors that catch moonlight and secrets.</p>
          <span class="price">From $68</span>
        </div>
        
        <div class="product-card">
          <div style="font-size: 3rem;">✨</div>
          <h3>Lace Wall Hangings</h3>
          <p>Delicate tapestries woven with names, dates, and quiet wishes.</p>
          <span class="price">From $54</span>
        </div>
        
        <div class="product-card">
          <div style="font-size: 3rem;">🌙</div>
          <h3>Moonlit Objects</h3>
          <p>Small enchanted pieces for shelves, nightstands, and windowsills.</p>
          <span class="price">From $32</span>
        </div>
      </div>
    </section>

    <!-- About -->
    <section id="about">
      <h2 class="section-title">Our Story</h2>
      <p class="section-subtitle">Once upon a modern home</p>
      <div class="about-content">
        <p>NovaLace was born from the belief that every home deserves a little quiet magic. We create soft, personalized pieces — the kind that feel like they belong in a storybook but live beautifully in real rooms.</p>
        <br>
        <p>Every item is designed to feel personal, delicate, and just a little enchanted.</p>
      </div>
    </section>

    <!-- Footer -->
    <footer id="contact">
      <div class="logo">NovaLace</div>
      <p>Fairy-tale finds for modern castles</p>
      <p style="margin-top: 20px; font-size: 0.95rem;">© 2026 NovaLace · Made with quiet magic</p>
    </footer>
  </div>
</body>
</html>
