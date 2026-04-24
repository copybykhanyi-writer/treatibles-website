<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Treatibles — Harmony for the Whole Family</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,700;1,400&family=DM+Sans:wght@300;400;500&display=swap" rel="stylesheet">
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  :root {
    --cream: #FAF6EF;
    --warm-white: #FFFDF8;
    --forest: #2D4A2F;
    --forest-light: #3D6340;
    --sage: #7A9E7E;
    --sage-light: #B5CEB8;
    --amber: #D4813A;
    --amber-light: #E9A96A;
    --charcoal: #2C2C2A;
    --muted: #6B6B68;
    --border: rgba(45,74,47,0.12);
    --font-display: 'Playfair Display', Georgia, serif;
    --font-body: 'DM Sans', sans-serif;
  }

  html { scroll-behavior: smooth; }

  body {
    font-family: var(--font-body);
    background: var(--cream);
    color: var(--charcoal);
    font-size: 16px;
    line-height: 1.6;
    overflow-x: hidden;
  }

  /* NAV */
  nav {
    background: var(--warm-white);
    border-bottom: 1px solid var(--border);
    padding: 0 2rem;
    height: 64px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    position: sticky;
    top: 0;
    z-index: 100;
  }

  .nav-logo {
    font-family: var(--font-display);
    font-size: 22px;
    font-weight: 700;
    color: var(--forest);
    letter-spacing: -0.5px;
  }

  .nav-logo span {
    color: var(--amber);
  }

  .nav-links {
    display: flex;
    gap: 2rem;
    list-style: none;
  }

  .nav-links a {
    text-decoration: none;
    color: var(--muted);
    font-size: 14px;
    font-weight: 400;
    letter-spacing: 0.02em;
    transition: color 0.2s;
  }

  .nav-links a:hover { color: var(--forest); }

  .nav-actions {
    display: flex;
    gap: 1rem;
    align-items: center;
  }

  .btn-primary {
    background: var(--forest);
    color: var(--cream);
    border: none;
    padding: 10px 20px;
    border-radius: 100px;
    font-family: var(--font-body);
    font-size: 14px;
    font-weight: 500;
    cursor: pointer;
    transition: background 0.2s;
    text-decoration: none;
    display: inline-block;
  }

  .btn-primary:hover { background: var(--forest-light); }

  .btn-outline {
    background: transparent;
    color: var(--forest);
    border: 1.5px solid var(--forest);
    padding: 9px 20px;
    border-radius: 100px;
    font-family: var(--font-body);
    font-size: 14px;
    font-weight: 500;
    cursor: pointer;
    transition: all 0.2s;
    text-decoration: none;
    display: inline-block;
  }

  .btn-outline:hover {
    background: var(--forest);
    color: var(--cream);
  }

  /* BANNER */
  .announcement {
    background: var(--forest);
    color: var(--sage-light);
    text-align: center;
    font-size: 12px;
    letter-spacing: 0.08em;
    padding: 8px;
    font-weight: 400;
  }

  /* HERO */
  .hero {
    display: grid;
    grid-template-columns: 1fr 1fr;
    min-height: calc(100vh - 64px);
    max-height: 800px;
  }

  .hero-left {
    background: var(--warm-white);
    padding: 6rem 4rem 4rem 5rem;
    display: flex;
    flex-direction: column;
    justify-content: center;
    border-right: 1px solid var(--border);
  }

  .hero-eyebrow {
    font-size: 11px;
    letter-spacing: 0.2em;
    text-transform: uppercase;
    color: var(--amber);
    font-weight: 500;
    margin-bottom: 1.5rem;
  }

  .hero-headline {
    font-family: var(--font-display);
    font-size: clamp(38px, 4vw, 56px);
    line-height: 1.12;
    color: var(--forest);
    margin-bottom: 1.5rem;
    letter-spacing: -1px;
  }

  .hero-headline em {
    font-style: italic;
    color: var(--amber);
  }

  .hero-sub {
    font-size: 17px;
    color: var(--muted);
    line-height: 1.7;
    max-width: 440px;
    margin-bottom: 2.5rem;
    font-weight: 300;
  }

  .hero-cta-group {
    display: flex;
    gap: 1rem;
    align-items: center;
    flex-wrap: wrap;
  }

  .hero-trust {
    margin-top: 3rem;
    display: flex;
    align-items: center;
    gap: 1rem;
  }

  .stars {
    display: flex;
    gap: 2px;
  }

  .star {
    width: 14px;
    height: 14px;
    background: var(--amber);
    clip-path: polygon(50% 0%,61% 35%,98% 35%,68% 57%,79% 91%,50% 70%,21% 91%,32% 57%,2% 35%,39% 35%);
  }

  .trust-text {
    font-size: 13px;
    color: var(--muted);
  }

  .trust-text strong {
    color: var(--charcoal);
    font-weight: 500;
  }

  .hero-right {
    background: var(--forest);
    position: relative;
    overflow: hidden;
    display: flex;
    align-items: center;
    justify-content: center;
  }

  .hero-visual {
    width: 100%;
    height: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
    gap: 2rem;
    padding: 3rem;
  }

  .hero-pet-selector {
    text-align: center;
  }

  .pet-question {
    font-family: var(--font-display);
    font-size: 28px;
    color: var(--cream);
    margin-bottom: 0.5rem;
    font-style: italic;
  }

  .pet-sub {
    font-size: 13px;
    color: var(--sage-light);
    letter-spacing: 0.05em;
    margin-bottom: 2rem;
  }

  .pet-cards {
    display: flex;
    gap: 1rem;
    justify-content: center;
  }

  .pet-card {
    background: rgba(255,255,255,0.08);
    border: 1.5px solid rgba(255,255,255,0.15);
    border-radius: 16px;
    padding: 1.5rem 1.25rem;
    text-align: center;
    cursor: pointer;
    transition: all 0.25s;
    min-width: 110px;
  }

  .pet-card:hover {
    background: rgba(255,255,255,0.15);
    border-color: var(--amber-light);
    transform: translateY(-3px);
  }

  .pet-icon {
    font-size: 32px;
    display: block;
    margin-bottom: 0.5rem;
  }

  .pet-label {
    font-size: 13px;
    color: var(--sage-light);
    font-weight: 500;
    letter-spacing: 0.05em;
    text-transform: uppercase;
  }

  .hero-badge {
    background: rgba(212,129,58,0.2);
    border: 1px solid var(--amber-light);
    border-radius: 100px;
    padding: 6px 16px;
    display: inline-flex;
    align-items: center;
    gap: 8px;
    font-size: 12px;
    color: var(--amber-light);
    letter-spacing: 0.05em;
  }

  .badge-dot {
    width: 6px;
    height: 6px;
    background: var(--amber-light);
    border-radius: 50%;
    animation: pulse 2s infinite;
  }

  @keyframes pulse {
    0%, 100% { opacity: 1; }
    50% { opacity: 0.4; }
  }

  /* NEEDS SECTION */
  .needs {
    background: var(--warm-white);
    padding: 5rem 5rem;
    border-bottom: 1px solid var(--border);
  }

  .section-label {
    font-size: 11px;
    letter-spacing: 0.2em;
    text-transform: uppercase;
    color: var(--amber);
    font-weight: 500;
    margin-bottom: 0.75rem;
  }

  .section-headline {
    font-family: var(--font-display);
    font-size: clamp(28px, 3vw, 40px);
    color: var(--forest);
    line-height: 1.2;
    letter-spacing: -0.5px;
    margin-bottom: 3rem;
    max-width: 540px;
  }

  .needs-grid {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 1px;
    background: var(--border);
    border: 1px solid var(--border);
    border-radius: 16px;
    overflow: hidden;
  }

  .need-card {
    background: var(--warm-white);
    padding: 2rem 1.5rem;
    transition: background 0.2s;
    cursor: pointer;
  }

  .need-card:hover { background: var(--cream); }

  .need-icon {
    width: 44px;
    height: 44px;
    background: var(--sage-light);
    border-radius: 12px;
    display: flex;
    align-items: center;
    justify-content: center;
    margin-bottom: 1rem;
    font-size: 20px;
  }

  .need-title {
    font-family: var(--font-display);
    font-size: 18px;
    color: var(--forest);
    margin-bottom: 0.5rem;
    font-weight: 700;
  }

  .need-desc {
    font-size: 13px;
    color: var(--muted);
    line-height: 1.6;
  }

  /* PRODUCTS */
  .products {
    padding: 5rem;
    background: var(--cream);
  }

  .products-header {
    display: flex;
    justify-content: space-between;
    align-items: flex-end;
    margin-bottom: 2.5rem;
  }

  .product-tabs {
    display: flex;
    gap: 0.5rem;
  }

  .tab {
    padding: 7px 16px;
    border-radius: 100px;
    font-size: 13px;
    font-weight: 500;
    cursor: pointer;
    border: 1.5px solid var(--border);
    background: transparent;
    color: var(--muted);
    transition: all 0.2s;
    font-family: var(--font-body);
  }

  .tab.active, .tab:hover {
    background: var(--forest);
    color: var(--cream);
    border-color: var(--forest);
  }

  .products-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 1.5rem;
  }

  .product-card {
    background: var(--warm-white);
    border: 1px solid var(--border);
    border-radius: 20px;
    overflow: hidden;
    transition: transform 0.25s, box-shadow 0.25s;
    cursor: pointer;
  }

  .product-card:hover {
    transform: translateY(-4px);
    box-shadow: 0 12px 40px rgba(45,74,47,0.12);
  }

  .product-img {
    aspect-ratio: 4/3;
    background: var(--sage-light);
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 56px;
    position: relative;
    overflow: hidden;
  }

  .product-badge {
    position: absolute;
    top: 12px;
    left: 12px;
    background: var(--forest);
    color: var(--cream);
    font-size: 11px;
    font-weight: 500;
    padding: 4px 10px;
    border-radius: 100px;
    letter-spacing: 0.04em;
  }

  .product-info {
    padding: 1.25rem 1.5rem 1.5rem;
  }

  .product-name {
    font-family: var(--font-display);
    font-size: 17px;
    color: var(--forest);
    margin-bottom: 0.25rem;
    font-weight: 700;
  }

  .product-desc {
    font-size: 13px;
    color: var(--muted);
    margin-bottom: 1rem;
    line-height: 1.5;
  }

  .product-footer {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  .product-price {
    font-size: 20px;
    font-weight: 500;
    color: var(--charcoal);
  }

  .product-price span {
    font-size: 13px;
    color: var(--muted);
    font-weight: 300;
  }

  .btn-add {
    background: var(--amber);
    color: white;
    border: none;
    padding: 8px 18px;
    border-radius: 100px;
    font-size: 13px;
    font-weight: 500;
    cursor: pointer;
    transition: background 0.2s;
    font-family: var(--font-body);
  }

  .btn-add:hover { background: var(--amber-light); }

  /* SOCIAL PROOF */
  .proof {
    background: var(--forest);
    padding: 5rem;
    color: var(--cream);
  }

  .proof-header {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 4rem;
    margin-bottom: 3rem;
    align-items: center;
  }

  .proof-stat-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 1px;
    background: rgba(255,255,255,0.1);
    border: 1px solid rgba(255,255,255,0.1);
    border-radius: 16px;
    overflow: hidden;
  }

  .proof-stat {
    padding: 1.5rem;
    background: var(--forest);
  }

  .stat-num {
    font-family: var(--font-display);
    font-size: 40px;
    color: var(--amber-light);
    line-height: 1;
    margin-bottom: 0.25rem;
  }

  .stat-label {
    font-size: 13px;
    color: var(--sage-light);
    font-weight: 300;
  }

  .proof-tagline {
    font-family: var(--font-display);
    font-size: clamp(26px, 2.5vw, 36px);
    line-height: 1.25;
    letter-spacing: -0.5px;
  }

  .proof-tagline em {
    font-style: italic;
    color: var(--amber-light);
  }

  .reviews-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 1.5rem;
  }

  .review-card {
    background: rgba(255,255,255,0.06);
    border: 1px solid rgba(255,255,255,0.1);
    border-radius: 16px;
    padding: 1.75rem;
  }

  .review-stars {
    display: flex;
    gap: 3px;
    margin-bottom: 1rem;
  }

  .review-star {
    width: 12px;
    height: 12px;
    background: var(--amber-light);
    clip-path: polygon(50% 0%,61% 35%,98% 35%,68% 57%,79% 91%,50% 70%,21% 91%,32% 57%,2% 35%,39% 35%);
  }

  .review-text {
    font-size: 14px;
    color: var(--sage-light);
    line-height: 1.7;
    font-style: italic;
    margin-bottom: 1.25rem;
    font-family: var(--font-display);
    font-weight: 400;
  }

  .reviewer {
    display: flex;
    align-items: center;
    gap: 10px;
  }

  .reviewer-avatar {
    width: 36px;
    height: 36px;
    border-radius: 50%;
    background: var(--sage);
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 14px;
    font-weight: 500;
    color: var(--forest);
  }

  .reviewer-name {
    font-size: 13px;
    font-weight: 500;
    color: var(--cream);
  }

  .reviewer-date {
    font-size: 12px;
    color: rgba(255,255,255,0.35);
  }

  /* MISSION */
  .mission {
    padding: 6rem 5rem;
    background: var(--warm-white);
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 6rem;
    align-items: center;
  }

  .mission-visual {
    background: var(--cream);
    border-radius: 24px;
    padding: 3rem;
    border: 1px solid var(--border);
    text-align: center;
  }

  .mission-icon-row {
    display: flex;
    justify-content: center;
    gap: 1rem;
    margin-bottom: 2rem;
    font-size: 48px;
  }

  .mission-values {
    display: flex;
    flex-direction: column;
    gap: 0;
  }

  .value-row {
    display: flex;
    align-items: center;
    gap: 1rem;
    padding: 1rem 0;
    border-bottom: 1px solid var(--border);
  }

  .value-row:last-child { border-bottom: none; }

  .value-dot {
    width: 8px;
    height: 8px;
    background: var(--amber);
    border-radius: 50%;
    flex-shrink: 0;
  }

  .value-name {
    font-size: 14px;
    font-weight: 500;
    color: var(--forest);
    min-width: 160px;
  }

  .value-desc {
    font-size: 13px;
    color: var(--muted);
  }

  .seal-badge {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    background: var(--sage-light);
    color: var(--forest);
    padding: 8px 16px;
    border-radius: 100px;
    font-size: 12px;
    font-weight: 500;
    letter-spacing: 0.05em;
    margin-top: 1.5rem;
  }

  /* GUARANTEE */
  .guarantee {
    background: var(--amber);
    padding: 4rem 5rem;
    display: grid;
    grid-template-columns: 1fr auto;
    align-items: center;
    gap: 3rem;
  }

  .guarantee-text h2 {
    font-family: var(--font-display);
    font-size: clamp(24px, 2.5vw, 36px);
    color: white;
    margin-bottom: 0.75rem;
    letter-spacing: -0.5px;
  }

  .guarantee-text p {
    font-size: 16px;
    color: rgba(255,255,255,0.85);
    font-weight: 300;
    max-width: 560px;
  }

  .guarantee-pills {
    display: flex;
    flex-direction: column;
    gap: 0.75rem;
  }

  .guarantee-pill {
    background: rgba(255,255,255,0.2);
    border: 1px solid rgba(255,255,255,0.3);
    padding: 10px 20px;
    border-radius: 100px;
    font-size: 13px;
    color: white;
    font-weight: 500;
    white-space: nowrap;
    display: flex;
    align-items: center;
    gap: 8px;
  }

  .pill-check {
    width: 16px;
    height: 16px;
    background: white;
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    flex-shrink: 0;
  }

  .pill-check::after {
    content: '';
    width: 8px;
    height: 4px;
    border-left: 2px solid var(--amber);
    border-bottom: 2px solid var(--amber);
    transform: rotate(-45deg) translateY(-1px);
    display: block;
  }

  /* FOOTER */
  footer {
    background: var(--charcoal);
    color: rgba(255,255,255,0.5);
    padding: 4rem 5rem 2rem;
  }

  .footer-grid {
    display: grid;
    grid-template-columns: 2fr 1fr 1fr 1fr;
    gap: 3rem;
    margin-bottom: 3rem;
    padding-bottom: 3rem;
    border-bottom: 1px solid rgba(255,255,255,0.08);
  }

  .footer-brand h3 {
    font-family: var(--font-display);
    font-size: 22px;
    color: white;
    margin-bottom: 0.75rem;
  }

  .footer-brand h3 span { color: var(--amber-light); }

  .footer-brand p {
    font-size: 13px;
    line-height: 1.7;
    max-width: 260px;
    margin-bottom: 1.5rem;
  }

  .footer-contact {
    font-size: 13px;
    line-height: 2;
  }

  .footer-col h4 {
    font-size: 11px;
    letter-spacing: 0.15em;
    text-transform: uppercase;
    color: rgba(255,255,255,0.3);
    margin-bottom: 1rem;
    font-weight: 500;
  }

  .footer-col ul {
    list-style: none;
    display: flex;
    flex-direction: column;
    gap: 0.6rem;
  }

  .footer-col a {
    color: rgba(255,255,255,0.5);
    text-decoration: none;
    font-size: 13px;
    transition: color 0.2s;
  }

  .footer-col a:hover { color: white; }

  .footer-bottom {
    display: flex;
    justify-content: space-between;
    align-items: center;
    font-size: 12px;
  }

  .footer-disclaimer {
    font-size: 11px;
    line-height: 1.6;
    max-width: 600px;
    margin-top: 1.5rem;
    padding-top: 1.5rem;
    border-top: 1px solid rgba(255,255,255,0.06);
    opacity: 0.5;
  }

  /* ANIMATIONS */
  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(24px); }
    to { opacity: 1; transform: translateY(0); }
  }

  .hero-left > * {
    animation: fadeUp 0.7s ease both;
  }

  .hero-eyebrow { animation-delay: 0.1s; }
  .hero-headline { animation-delay: 0.2s; }
  .hero-sub { animation-delay: 0.3s; }
  .hero-cta-group { animation-delay: 0.4s; }
  .hero-trust { animation-delay: 0.5s; }

  /* RESPONSIVE */
  @media (max-width: 900px) {
    .hero { grid-template-columns: 1fr; max-height: none; }
    .hero-left { padding: 3rem 2rem; }
    .hero-right { min-height: 360px; }
    .needs { padding: 3rem 2rem; }
    .needs-grid { grid-template-columns: 1fr 1fr; }
    .products { padding: 3rem 2rem; }
    .products-grid { grid-template-columns: 1fr 1fr; }
    .proof { padding: 3rem 2rem; }
    .proof-header { grid-template-columns: 1fr; gap: 2rem; }
    .reviews-grid { grid-template-columns: 1fr; }
    .mission { grid-template-columns: 1fr; padding: 3rem 2rem; gap: 2rem; }
    .guarantee { grid-template-columns: 1fr; padding: 3rem 2rem; }
    footer { padding: 3rem 2rem 2rem; }
    .footer-grid { grid-template-columns: 1fr 1fr; }
    nav { padding: 0 1.5rem; }
    .nav-links { display: none; }
  }
</style>
</head>
<body>

<div class="announcement">
  Free shipping on all orders over $75 &nbsp;·&nbsp; Shipping to all 50 states &nbsp;·&nbsp; Lab tested &amp; certified
</div>

<nav>
  <div class="nav-logo">Treat<span>ibles</span></div>
  <ul class="nav-links">
    <li><a href="#">For Dogs</a></li>
    <li><a href="#">For Cats</a></li>
    <li><a href="#">For Horses</a></li>
    <li><a href="#">Learn</a></li>
    <li><a href="#">For Vets</a></li>
  </ul>
  <div class="nav-actions">
    <a href="#" class="btn-outline">Sign In</a>
    <a href="#" class="btn-primary">Shop Now</a>
  </div>
</nav>

<!-- HERO -->
<section class="hero">
  <div class="hero-left">
    <div class="hero-eyebrow">Organic · Hemp-Derived · Vet-Friendly</div>
    <h1 class="hero-headline">
      Your pet<br>deserves to <em>feel</em><br>like family.
    </h1>
    <p class="hero-sub">
      Natural hemp-derived wellness products that help dogs, cats, and horses with anxiety, pain, and aging — made with organic ingredients you can actually pronounce.
    </p>
    <div class="hero-cta-group">
      <a href="#" class="btn-primary">Find the Right Product</a>
      <a href="#" class="btn-outline">How It Works</a>
    </div>
    <div class="hero-trust">
      <div class="stars">
        <div class="star"></div>
        <div class="star"></div>
        <div class="star"></div>
        <div class="star"></div>
        <div class="star"></div>
      </div>
      <div class="trust-text">
        Trusted by <strong>100,000+ pet families</strong> across the US
      </div>
    </div>
  </div>
  <div class="hero-right">
    <div class="hero-visual">
      <div class="hero-badge">
        <div class="badge-dot"></div>
        Compassion Certified
      </div>
      <div class="hero-pet-selector">
        <div class="pet-question">Who are we helping today?</div>
        <div class="pet-sub">Select your pet to see the right products</div>
        <div class="pet-cards">
          <div class="pet-card">
            <span class="pet-icon">🐕</span>
            <div class="pet-label">Dogs</div>
          </div>
          <div class="pet-card">
            <span class="pet-icon">🐈</span>
            <div class="pet-label">Cats</div>
          </div>
          <div class="pet-card">
            <span class="pet-icon">🐎</span>
            <div class="pet-label">Horses</div>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- NEEDS -->
<section class="needs">
  <div class="section-label">What we address</div>
  <h2 class="section-headline">The right support, for what your pet is going through</h2>
  <div class="needs-grid">
    <div class="need-card">
      <div class="need-icon">⚡</div>
      <div class="need-title">Anxiety &amp; Stress</div>
      <div class="need-desc">Thunderstorms, fireworks, travel, separation — calm support without sedation.</div>
    </div>
    <div class="need-card">
      <div class="need-icon">🦴</div>
      <div class="need-title">Joint &amp; Mobility</div>
      <div class="need-desc">Keep senior pets moving comfortably. Trusted by thousands with aging dogs.</div>
    </div>
    <div class="need-card">
      <div class="need-icon">🌙</div>
      <div class="need-title">Sleep &amp; Rest</div>
      <div class="need-desc">Restless nights and difficulty settling down — gentle, natural support.</div>
    </div>
    <div class="need-card">
      <div class="need-icon">💚</div>
      <div class="need-title">Daily Wellness</div>
      <div class="need-desc">Build a daily routine that keeps your pet thriving, inside and out.</div>
    </div>
  </div>
</section>

<!-- PRODUCTS -->
<section class="products">
  <div class="products-header">
    <div>
      <div class="section-label">Best sellers</div>
      <h2 class="section-headline" style="margin-bottom:0">Products that actually work</h2>
    </div>
    <div class="product-tabs">
      <button class="tab active">Dogs</button>
      <button class="tab">Cats</button>
      <button class="tab">Horses</button>
    </div>
  </div>
  <div class="products-grid">
    <div class="product-card">
      <div class="product-img" style="background: #C8DBC9;">
        <div class="product-badge">Extra Strength</div>
        🍠
      </div>
      <div class="product-info">
        <div class="product-name">Sweet Potato Hard Chews</div>
        <div class="product-desc">10 mg · Dogs who need stronger support for anxiety or chronic pain</div>
        <div class="product-footer">
          <div class="product-price"><span>From</span> $45</div>
          <button class="btn-add">Add to Cart</button>
        </div>
      </div>
    </div>
    <div class="product-card">
      <div class="product-img" style="background: #D4E8C2;">
        <div class="product-badge">Most Popular</div>
        🎃
      </div>
      <div class="product-info">
        <div class="product-name">Pumpkin Hard Chews</div>
        <div class="product-desc">1 mg &amp; 4 mg · Perfect for daily use and new-to-hemp pets</div>
        <div class="product-footer">
          <div class="product-price"><span>From</span> $38</div>
          <button class="btn-add">Add to Cart</button>
        </div>
      </div>
    </div>
    <div class="product-card">
      <div class="product-img" style="background: #DDD0C8;">
        <div class="product-badge">New</div>
        💊
      </div>
      <div class="product-info">
        <div class="product-name">Capsules 25 mg</div>
        <div class="product-desc">Easy dosing for dogs who are picky or need precise amounts</div>
        <div class="product-footer">
          <div class="product-price">$120</div>
          <button class="btn-add">Add to Cart</button>
        </div>
      </div>
    </div>
  </div>
  <div style="text-align: center; margin-top: 2.5rem;">
    <a href="#" class="btn-outline">View all products →</a>
  </div>
</section>

<!-- SOCIAL PROOF -->
<section class="proof">
  <div class="proof-header">
    <div>
      <div class="proof-tagline">
        Real pets.<br><em>Real results.</em><br>Real families.
      </div>
    </div>
    <div class="proof-stat-grid">
      <div class="proof-stat">
        <div class="stat-num">100k+</div>
        <div class="stat-label">Happy customers</div>
      </div>
      <div class="proof-stat">
        <div class="stat-num">5★</div>
        <div class="stat-label">Average rating</div>
      </div>
      <div class="proof-stat">
        <div class="stat-num">A+</div>
        <div class="stat-label">BBB rated</div>
      </div>
      <div class="proof-stat">
        <div class="stat-num">100%</div>
        <div class="stat-label">Organic hemp</div>
      </div>
    </div>
  </div>
  <div class="reviews-grid">
    <div class="review-card">
      <div class="review-stars">
        <div class="review-star"></div><div class="review-star"></div><div class="review-star"></div><div class="review-star"></div><div class="review-star"></div>
      </div>
      <div class="review-text">"My package was lost but Jessica immediately had my order resent via UPS the next day. Truly one of the easiest and best customer service experiences I've ever had."</div>
      <div class="reviewer">
        <div class="reviewer-avatar">BH</div>
        <div>
          <div class="reviewer-name">Bethany Hall</div>
          <div class="reviewer-date">Verified buyer</div>
        </div>
      </div>
    </div>
    <div class="review-card">
      <div class="review-stars">
        <div class="review-star"></div><div class="review-star"></div><div class="review-star"></div><div class="review-star"></div><div class="review-star"></div>
      </div>
      <div class="review-text">"These CBD bones picked my dog up and carried him. He responded 99% better than anything we'd tried before — other products either locked him up or left him unable to move."</div>
      <div class="reviewer">
        <div class="reviewer-avatar">VM</div>
        <div>
          <div class="reviewer-name">Virginia MacMahon</div>
          <div class="reviewer-date">Verified buyer</div>
        </div>
      </div>
    </div>
    <div class="review-card">
      <div class="review-stars">
        <div class="review-star"></div><div class="review-star"></div><div class="review-star"></div><div class="review-star"></div><div class="review-star"></div>
      </div>
      <div class="review-text">"We use Treatibles for horses, goats, and dogs at our sanctuary. Our senior dog with anxiety and dementia has not had a seizure in over a year since starting the soft chews."</div>
      <div class="reviewer">
        <div class="reviewer-avatar">FS</div>
        <div>
          <div class="reviewer-name">Farmhouse Sanctuary</div>
          <div class="reviewer-date">Verified buyer</div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- MISSION -->
<section class="mission">
  <div>
    <div class="section-label">Our mission</div>
    <h2 class="section-headline">Compassionate care for furry families</h2>
    <p style="font-size:16px; color: var(--muted); line-height:1.8; margin-bottom:2rem; font-weight:300;">
      Treatibles was built on one belief: pets are family. Every product we make reflects our commitment to high-quality, organic, hemp-derived ingredients — and to the humans who love their animals unconditionally.
    </p>
    <div class="mission-values">
      <div class="value-row">
        <div class="value-dot"></div>
        <div class="value-name">Compassionate Care</div>
        <div class="value-desc">We treat every pet as if they were our own</div>
      </div>
      <div class="value-row">
        <div class="value-dot"></div>
        <div class="value-name">Quality Ingredients</div>
        <div class="value-desc">Organic, third-party tested, no fillers</div>
      </div>
      <div class="value-row">
        <div class="value-dot"></div>
        <div class="value-name">Reliable Information</div>
        <div class="value-desc">Backed by science, transparent about what we know</div>
      </div>
      <div class="value-row">
        <div class="value-dot"></div>
        <div class="value-name">Integrity</div>
        <div class="value-desc">We never oversell or mislead pet families</div>
      </div>
    </div>
    <div class="seal-badge">✓ Compassion Certified</div>
  </div>
  <div class="mission-visual">
    <div class="mission-icon-row">🐕 🐈 🐎</div>
    <p style="font-family: var(--font-display); font-size: 22px; color: var(--forest); font-style: italic; line-height:1.4; margin-bottom:1.5rem;">
      "Harmony for the whole family"
    </p>
    <p style="font-size: 13px; color: var(--muted); line-height:1.7;">
      Happy pets make happy humans. That's why we go above and beyond — from the ingredients we source to the customer care team that answers the phone.
    </p>
    <div style="margin-top:2rem; padding-top: 1.5rem; border-top: 1px solid var(--border); text-align: left;">
      <div style="font-size:12px; color:var(--muted); margin-bottom:0.5rem; letter-spacing:0.05em; text-transform:uppercase;">Certificate of Analysis</div>
      <div style="font-size:13px; color:var(--forest); font-weight:500;">Every batch is third-party lab tested →</div>
    </div>
  </div>
</section>

<!-- GUARANTEE -->
<section class="guarantee">
  <div class="guarantee-text">
    <h2>Not sure it'll work? We take the risk.</h2>
    <p>We stand behind every product we sell. If your pet doesn't respond the way you hoped, we'll make it right. No complicated returns, no runaround — just honest support from people who care.</p>
    <div style="margin-top:2rem;">
      <a href="#" style="background:white; color:var(--amber); border:none; padding:12px 24px; border-radius:100px; font-size:14px; font-weight:500; cursor:pointer; text-decoration:none; display:inline-block; font-family:var(--font-body);">Shop with Confidence →</a>
    </div>
  </div>
  <div class="guarantee-pills">
    <div class="guarantee-pill"><div class="pill-check"></div> Free shipping over $75</div>
    <div class="guarantee-pill"><div class="pill-check"></div> Satisfaction guarantee</div>
    <div class="guarantee-pill"><div class="pill-check"></div> Third-party lab tested</div>
    <div class="guarantee-pill"><div class="pill-check"></div> Vet-friendly formula</div>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <div class="footer-grid">
    <div class="footer-brand">
      <h3>Treat<span>ibles</span></h3>
      <p>Organic hemp-derived wellness products for dogs, cats, and horses. Harmony for the whole family.</p>
      <div class="footer-contact">
        <div>(707) 992-0854</div>
        <div>Mon–Fri, 9am–5pm PT</div>
        <div>Nashville, TN</div>
      </div>
    </div>
    <div class="footer-col">
      <h4>Shop</h4>
      <ul>
        <li><a href="#">For Dogs</a></li>
        <li><a href="#">For Cats</a></li>
        <li><a href="#">For Horses</a></li>
        <li><a href="#">Bundles</a></li>
        <li><a href="#">Best Sellers</a></li>
      </ul>
    </div>
    <div class="footer-col">
      <h4>Learn</h4>
      <ul>
        <li><a href="#">How It Works</a></li>
        <li><a href="#">For Veterinarians</a></li>
        <li><a href="#">Lab Results</a></li>
        <li><a href="#">Blog</a></li>
        <li><a href="#">FAQs</a></li>
      </ul>
    </div>
    <div class="footer-col">
      <h4>Account</h4>
      <ul>
        <li><a href="#">My Account</a></li>
        <li><a href="#">Autoship</a></li>
        <li><a href="#">Refer a Friend</a></li>
        <li><a href="#">Wholesale</a></li>
        <li><a href="#">Affiliate Program</a></li>
      </ul>
    </div>
  </div>
  <div class="footer-bottom">
    <div>©2026 Treatibles / AD Remedies, Inc. All rights reserved.</div>
    <div style="display:flex; gap:1rem;">
      <a href="#" style="color:rgba(255,255,255,0.4); text-decoration:none; font-size:12px;">Privacy</a>
      <a href="#" style="color:rgba(255,255,255,0.4); text-decoration:none; font-size:12px;">Terms</a>
      <a href="#" style="color:rgba(255,255,255,0.4); text-decoration:none; font-size:12px;">Refund Policy</a>
    </div>
  </div>
  <div class="footer-disclaimer">
    The statements made regarding these products have not been evaluated by the Food and Drug Administration. These products are not intended to diagnose, treat, cure, or prevent any disease. Always seek the advice of a veterinarian with any questions about a medical condition.
  </div>
</footer>

<script>
  const tabs = document.querySelectorAll('.tab');
  tabs.forEach(tab => {
    tab.addEventListener('click', () => {
      tabs.forEach(t => t.classList.remove('active'));
      tab.classList.add('active');
    });
  });
</script>
</body>
</html>
