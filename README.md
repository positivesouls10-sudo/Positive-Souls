# Positive-Souls[positive-souls.html](https://github.com/user-attachments/files/25837110/index.html)<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Positive Souls — Self Discipline Mastery</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,300;0,400;0,600;0,700;1,300;1,400&family=DM+Sans:wght@300;400;500;600&display=swap" rel="stylesheet">
<style>
  :root {
    --green-deep:   #0d2b1e;
    --green-dark:   #14402d;
    --green-mid:    #1e6645;
    --green-accent: #2d9b63;
    --green-light:  #4cc88a;
    --gold:         #c9a84c;
    --gold-light:   #e8c97a;
    --white:        #f7f5f0;
    --white-pure:   #ffffff;
    --gray-soft:    #e8e4dc;
    --gray-mid:     #9e9b94;
    --text-dark:    #0d1a12;
    --font-display: 'Cormorant Garamond', serif;
    --font-body:    'DM Sans', sans-serif;
  }

  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  html { scroll-behavior: smooth; }

  body {
    font-family: var(--font-body);
    background: var(--white);
    color: var(--text-dark);
    overflow-x: hidden;
  }

  /* ─── NAV ─── */
  nav {
    position: fixed; top: 0; width: 100%; z-index: 100;
    display: flex; align-items: center; justify-content: space-between;
    padding: 1.2rem 5%;
    background: rgba(13,27,20,0.92);
    backdrop-filter: blur(12px);
    border-bottom: 1px solid rgba(77,200,138,0.12);
    transition: background 0.3s;
  }
  .nav-logo {
    font-family: var(--font-display);
    font-size: 1.6rem; font-weight: 700;
    color: var(--white);
    letter-spacing: 0.02em;
  }
  .nav-logo span { color: var(--green-light); }
  .nav-links { display: flex; gap: 2.2rem; list-style: none; }
  .nav-links a {
    color: rgba(247,245,240,0.75);
    text-decoration: none; font-size: 0.85rem;
    letter-spacing: 0.08em; text-transform: uppercase;
    font-weight: 500; transition: color 0.2s;
  }
  .nav-links a:hover { color: var(--green-light); }
  .nav-cta {
    background: var(--green-accent);
    color: var(--white-pure) !important;
    padding: 0.55rem 1.4rem;
    border-radius: 100px;
    font-weight: 600 !important;
    transition: background 0.2s, transform 0.2s !important;
  }
  .nav-cta:hover { background: var(--green-light) !important; transform: translateY(-1px); }
  .hamburger { display: none; flex-direction: column; gap: 5px; cursor: pointer; }
  .hamburger span { width: 24px; height: 2px; background: var(--white); display: block; transition: 0.3s; }

  /* ─── HERO ─── */
  #hero {
    min-height: 100vh;
    background: var(--green-deep);
    display: grid; place-items: center;
    position: relative; overflow: hidden;
    padding: 6rem 5% 4rem;
  }
  .hero-bg-orb {
    position: absolute; border-radius: 50%; filter: blur(90px); opacity: 0.25; pointer-events: none;
  }
  .orb1 { width: 600px; height: 600px; background: var(--green-mid); top: -150px; right: -100px; }
  .orb2 { width: 400px; height: 400px; background: var(--green-accent); bottom: -100px; left: -80px; }
  .orb3 { width: 200px; height: 200px; background: var(--gold); top: 40%; left: 30%; opacity: 0.12; }

  .hero-grid {
    display: grid; grid-template-columns: 1fr 1fr;
    gap: 4rem; align-items: center;
    max-width: 1200px; width: 100%; position: relative; z-index: 1;
  }
  .hero-eyebrow {
    display: inline-flex; align-items: center; gap: 0.6rem;
    font-size: 0.78rem; letter-spacing: 0.18em; text-transform: uppercase;
    color: var(--green-light); font-weight: 600; margin-bottom: 1.4rem;
  }
  .hero-eyebrow::before {
    content: ''; width: 28px; height: 1px; background: var(--green-light);
  }
  .hero-title {
    font-family: var(--font-display);
    font-size: clamp(2.8rem, 5vw, 4.8rem);
    font-weight: 700; line-height: 1.08;
    color: var(--white);
    margin-bottom: 1.5rem;
  }
  .hero-title em { color: var(--green-light); font-style: italic; }
  .hero-sub {
    font-size: 1.1rem; line-height: 1.7;
    color: rgba(247,245,240,0.7);
    max-width: 480px; margin-bottom: 2.5rem;
  }
  .btn-primary {
    display: inline-block;
    background: var(--green-accent);
    color: var(--white-pure);
    padding: 1rem 2.4rem;
    border-radius: 100px;
    font-size: 0.95rem; font-weight: 600;
    letter-spacing: 0.04em;
    text-decoration: none;
    transition: background 0.25s, transform 0.25s, box-shadow 0.25s;
    box-shadow: 0 8px 32px rgba(45,155,99,0.4);
    border: none; cursor: pointer;
  }
  .btn-primary:hover {
    background: var(--green-light);
    transform: translateY(-3px);
    box-shadow: 0 14px 40px rgba(76,200,138,0.45);
  }
  .btn-secondary {
    display: inline-block;
    background: transparent;
    color: var(--white);
    padding: 1rem 2.4rem;
    border-radius: 100px;
    font-size: 0.95rem; font-weight: 500;
    letter-spacing: 0.04em;
    text-decoration: none;
    border: 1.5px solid rgba(247,245,240,0.3);
    transition: border-color 0.25s, color 0.25s;
    margin-left: 1rem;
    cursor: pointer;
  }
  .btn-secondary:hover { border-color: var(--green-light); color: var(--green-light); }

  .hero-stats {
    display: flex; gap: 2rem; margin-top: 3rem;
    padding-top: 2rem;
    border-top: 1px solid rgba(247,245,240,0.1);
  }
  .stat-item {}
  .stat-num {
    font-family: var(--font-display);
    font-size: 2rem; font-weight: 700;
    color: var(--green-light); line-height: 1;
  }
  .stat-label { font-size: 0.78rem; color: rgba(247,245,240,0.55); margin-top: 0.3rem; letter-spacing: 0.05em; }

  .hero-visual {
    position: relative;
  }
  .hero-image-wrap {
    border-radius: 24px; overflow: hidden;
    position: relative;
    aspect-ratio: 4/5;
    box-shadow: 0 40px 100px rgba(0,0,0,0.5);
  }
  .hero-image-wrap img {
    width: 100%; height: 100%; object-fit: cover;
  }
  .hero-badge {
    position: absolute; bottom: -20px; left: -20px;
    background: var(--green-dark);
    border: 1px solid var(--green-accent);
    border-radius: 16px; padding: 1.2rem 1.5rem;
    box-shadow: 0 20px 60px rgba(0,0,0,0.4);
  }
  .hero-badge-title { font-size: 0.7rem; letter-spacing: 0.1em; text-transform: uppercase; color: var(--green-light); margin-bottom: 0.3rem; }
  .hero-badge-text { font-family: var(--font-display); font-size: 1.15rem; color: var(--white); font-weight: 600; }
  .hero-badge-sub { font-size: 0.75rem; color: rgba(247,245,240,0.5); margin-top: 0.2rem; }

  /* ─── SECTION DEFAULTS ─── */
  section { padding: 6rem 5%; }
  .section-label {
    display: inline-flex; align-items: center; gap: 0.6rem;
    font-size: 0.75rem; letter-spacing: 0.2em; text-transform: uppercase;
    color: var(--green-accent); font-weight: 600; margin-bottom: 1rem;
  }
  .section-label::before { content: ''; width: 24px; height: 1px; background: var(--green-accent); }
  .section-title {
    font-family: var(--font-display);
    font-size: clamp(2rem, 3.5vw, 3.2rem);
    font-weight: 700; line-height: 1.15;
    margin-bottom: 1.2rem;
  }
  .section-body { font-size: 1.05rem; line-height: 1.75; color: #4a5550; max-width: 620px; }
  .container { max-width: 1200px; margin: 0 auto; }

  /* ─── ABOUT ─── */
  #about { background: var(--white-pure); }
  .about-grid {
    display: grid; grid-template-columns: 1fr 1fr;
    gap: 5rem; align-items: center;
    max-width: 1200px; margin: 0 auto;
  }
  .about-image {
    position: relative; border-radius: 20px; overflow: hidden;
    aspect-ratio: 1;
    box-shadow: 0 30px 80px rgba(13,43,30,0.15);
  }
  .about-image img { width: 100%; height: 100%; object-fit: cover; }
  .about-image::after {
    content: ''; position: absolute; inset: 0;
    background: linear-gradient(135deg, rgba(30,102,69,0.3) 0%, transparent 60%);
  }
  .about-decoration {
    position: absolute; top: -15px; right: -15px;
    width: 100px; height: 100px; border-radius: 50%;
    background: var(--green-accent); opacity: 0.15; z-index: -1;
  }
  .mission-pillars { display: flex; flex-direction: column; gap: 1.2rem; margin-top: 2rem; }
  .pillar {
    display: flex; gap: 1rem; align-items: flex-start;
    padding: 1.2rem; border-radius: 12px;
    border: 1px solid var(--gray-soft);
    transition: border-color 0.2s, box-shadow 0.2s;
  }
  .pillar:hover { border-color: var(--green-accent); box-shadow: 0 4px 20px rgba(45,155,99,0.1); }
  .pillar-icon {
    width: 40px; height: 40px; border-radius: 10px;
    background: var(--green-deep); color: var(--green-light);
    display: grid; place-items: center; font-size: 1.1rem; flex-shrink: 0;
  }
  .pillar-text h4 { font-size: 0.95rem; font-weight: 600; margin-bottom: 0.2rem; }
  .pillar-text p { font-size: 0.85rem; color: var(--gray-mid); line-height: 1.5; }

  /* ─── PROBLEMS ─── */
  #problems {
    background: var(--green-deep);
    position: relative; overflow: hidden;
  }
  #problems .section-label { color: var(--gold-light); }
  #problems .section-label::before { background: var(--gold-light); }
  #problems .section-title { color: var(--white); }
  #problems .section-body { color: rgba(247,245,240,0.65); }
  .problems-grid {
    display: grid; grid-template-columns: repeat(2, 1fr);
    gap: 1.5rem; margin-top: 3rem;
    max-width: 1200px; margin-left: auto; margin-right: auto;
  }
  .problem-card {
    background: rgba(255,255,255,0.04);
    border: 1px solid rgba(255,255,255,0.08);
    border-radius: 16px; padding: 2rem;
    position: relative; overflow: hidden;
    transition: background 0.3s, border-color 0.3s, transform 0.3s;
  }
  .problem-card:hover {
    background: rgba(255,255,255,0.07);
    border-color: rgba(76,200,138,0.3);
    transform: translateY(-4px);
  }
  .problem-card::before {
    content: ''; position: absolute; top: 0; left: 0;
    width: 3px; height: 100%;
    background: linear-gradient(to bottom, var(--gold), transparent);
  }
  .problem-number {
    font-family: var(--font-display); font-size: 4rem; font-weight: 700;
    color: rgba(201,168,76,0.12); line-height: 1;
    position: absolute; top: 0.5rem; right: 1.5rem;
  }
  .problem-icon { font-size: 1.8rem; margin-bottom: 1rem; }
  .problem-card h3 {
    font-size: 1.25rem; font-weight: 600; color: var(--white);
    margin-bottom: 0.7rem;
  }
  .problem-card p { font-size: 0.9rem; color: rgba(247,245,240,0.6); line-height: 1.65; }

  /* ─── COURSE ─── */
  #course { background: #f4f7f5; }
  .course-wrapper {
    display: grid; grid-template-columns: 1fr 1.1fr;
    gap: 5rem; align-items: center;
    max-width: 1200px; margin: 0 auto;
  }
  .course-modules { margin-top: 2rem; display: flex; flex-direction: column; gap: 1rem; }
  .module {
    display: flex; gap: 1.2rem; align-items: flex-start;
    padding: 1.4rem; border-radius: 14px;
    background: var(--white-pure);
    box-shadow: 0 2px 12px rgba(13,43,30,0.06);
    transition: box-shadow 0.2s, transform 0.2s;
  }
  .module:hover { box-shadow: 0 8px 30px rgba(13,43,30,0.12); transform: translateY(-2px); }
  .module-num {
    width: 36px; height: 36px; border-radius: 50%;
    background: var(--green-deep); color: var(--green-light);
    font-size: 0.8rem; font-weight: 700;
    display: grid; place-items: center; flex-shrink: 0;
  }
  .module-text h4 { font-size: 0.95rem; font-weight: 600; margin-bottom: 0.25rem; }
  .module-text p { font-size: 0.83rem; color: var(--gray-mid); line-height: 1.5; }
  .course-visual {
    position: relative;
  }
  .course-mockup {
    border-radius: 20px; overflow: hidden;
    aspect-ratio: 3/4;
    box-shadow: 0 40px 100px rgba(13,43,30,0.2);
    position: relative;
  }
  .course-mockup img { width: 100%; height: 100%; object-fit: cover; }
  .course-tag {
    position: absolute; top: 1.5rem; left: 1.5rem;
    background: var(--green-deep); color: var(--green-light);
    font-size: 0.75rem; font-weight: 600; letter-spacing: 0.08em;
    text-transform: uppercase; padding: 0.5rem 1rem; border-radius: 100px;
  }
  .course-ribbon {
    position: absolute; bottom: 1.5rem; left: 1.5rem; right: 1.5rem;
    background: rgba(13,27,20,0.9); backdrop-filter: blur(12px);
    border-radius: 12px; padding: 1.2rem;
    border: 1px solid rgba(76,200,138,0.2);
  }
  .ribbon-title { font-size: 0.8rem; color: var(--green-light); margin-bottom: 0.4rem; font-weight: 600; }
  .ribbon-name { font-family: var(--font-display); font-size: 1.2rem; color: var(--white); font-weight: 700; }
  .ribbon-meta { font-size: 0.75rem; color: rgba(247,245,240,0.5); margin-top: 0.3rem; }

  /* ─── BENEFITS ─── */
  #benefits { background: var(--white-pure); }
  .benefits-header { text-align: center; max-width: 650px; margin: 0 auto 3.5rem; }
  .benefits-header .section-label { justify-content: center; }
  .benefits-header .section-label::before { display: none; }
  .benefits-grid {
    display: grid; grid-template-columns: repeat(3, 1fr);
    gap: 1.5rem; max-width: 1200px; margin: 0 auto;
  }
  .benefit-card {
    padding: 2.5rem 2rem;
    border-radius: 20px;
    background: #f4f7f5;
    border: 1px solid transparent;
    transition: border-color 0.3s, box-shadow 0.3s, background 0.3s;
    text-align: center;
  }
  .benefit-card:hover {
    background: var(--white-pure);
    border-color: var(--green-accent);
    box-shadow: 0 12px 40px rgba(45,155,99,0.12);
  }
  .benefit-icon {
    width: 64px; height: 64px; border-radius: 18px;
    background: var(--green-deep);
    margin: 0 auto 1.4rem;
    display: grid; place-items: center;
    font-size: 1.6rem;
  }
  .benefit-card h3 { font-size: 1.1rem; font-weight: 600; margin-bottom: 0.7rem; }
  .benefit-card p { font-size: 0.88rem; color: #6a7a72; line-height: 1.65; }

  /* ─── TESTIMONIALS ─── */
  #testimonials {
    background: var(--green-dark);
    position: relative; overflow: hidden;
  }
  #testimonials .section-title { color: var(--white); }
  .testi-header { text-align: center; max-width: 600px; margin: 0 auto 3.5rem; }
  .testi-header .section-label { justify-content: center; color: var(--gold-light); }
  .testi-header .section-label::before { display: none; }
  .testi-grid {
    display: grid; grid-template-columns: repeat(3, 1fr);
    gap: 1.5rem; max-width: 1200px; margin: 0 auto;
  }
  .testi-card {
    background: rgba(255,255,255,0.05);
    border: 1px solid rgba(255,255,255,0.1);
    border-radius: 20px; padding: 2.2rem;
    transition: transform 0.3s, border-color 0.3s;
    position: relative;
  }
  .testi-card:hover { transform: translateY(-6px); border-color: rgba(76,200,138,0.3); }
  .testi-quote { font-size: 3rem; color: var(--green-accent); opacity: 0.6; line-height: 1; margin-bottom: 1rem; font-family: Georgia, serif; }
  .testi-text {
    font-family: var(--font-display); font-size: 1.1rem; font-style: italic;
    line-height: 1.65; color: rgba(247,245,240,0.9); margin-bottom: 1.8rem;
  }
  .testi-stars { color: var(--gold); letter-spacing: 3px; margin-bottom: 1.2rem; font-size: 0.85rem; }
  .testi-author { display: flex; gap: 1rem; align-items: center; }
  .testi-avatar {
    width: 46px; height: 46px; border-radius: 50%;
    background: var(--green-mid); overflow: hidden; flex-shrink: 0;
  }
  .testi-avatar img { width: 100%; height: 100%; object-fit: cover; }
  .testi-name { font-weight: 600; font-size: 0.9rem; color: var(--white); }
  .testi-role { font-size: 0.78rem; color: rgba(247,245,240,0.5); margin-top: 0.15rem; }

  /* ─── PRICING ─── */
  #pricing { background: #f4f7f5; text-align: center; }
  .pricing-header { max-width: 600px; margin: 0 auto 3.5rem; }
  .pricing-header .section-label { justify-content: center; }
  .pricing-header .section-label::before { display: none; }
  .pricing-card {
    max-width: 500px; margin: 0 auto;
    background: var(--green-deep);
    border-radius: 28px; padding: 3rem 2.5rem;
    position: relative; overflow: hidden;
    box-shadow: 0 40px 100px rgba(13,43,30,0.3);
  }
  .pricing-badge {
    position: absolute; top: 1.5rem; right: 1.5rem;
    background: var(--gold); color: var(--text-dark);
    font-size: 0.72rem; font-weight: 700; letter-spacing: 0.08em;
    text-transform: uppercase; padding: 0.4rem 0.9rem; border-radius: 100px;
  }
  .pricing-card-label { font-size: 0.75rem; letter-spacing: 0.2em; text-transform: uppercase; color: var(--green-light); margin-bottom: 0.6rem; }
  .pricing-card-name {
    font-family: var(--font-display); font-size: 2rem; font-weight: 700;
    color: var(--white); margin-bottom: 2rem;
  }
  .pricing-divider { height: 1px; background: rgba(255,255,255,0.1); margin-bottom: 2rem; }
  .price-amount {
    font-family: var(--font-display); font-size: 4.5rem; font-weight: 700;
    color: var(--white); line-height: 1;
    margin-bottom: 0.5rem;
  }
  .price-amount sup { font-size: 2rem; vertical-align: top; margin-top: 0.8rem; display: inline-block; }
  .price-note { font-size: 0.85rem; color: rgba(247,245,240,0.5); margin-bottom: 2.5rem; }
  .pricing-features { list-style: none; text-align: left; margin-bottom: 2.5rem; display: flex; flex-direction: column; gap: 0.85rem; }
  .pricing-features li { display: flex; gap: 0.8rem; align-items: center; font-size: 0.9rem; color: rgba(247,245,240,0.85); }
  .pricing-features li::before { content: '✓'; color: var(--green-light); font-weight: 700; flex-shrink: 0; }
  .pricing-card .btn-primary { width: 100%; text-align: center; font-size: 1rem; padding: 1.1rem; }
  .guarantee { margin-top: 1.2rem; font-size: 0.8rem; color: rgba(247,245,240,0.45); }

  /* ─── CONTACT ─── */
  #contact { background: var(--white-pure); }
  .contact-grid {
    display: grid; grid-template-columns: 1fr 1fr;
    gap: 5rem; align-items: start;
    max-width: 1200px; margin: 0 auto;
  }
  .contact-info { padding-top: 1rem; }
  .contact-info .section-body { margin-bottom: 2.5rem; }
  .contact-detail { display: flex; gap: 1rem; align-items: center; margin-bottom: 1.2rem; }
  .contact-icon {
    width: 42px; height: 42px; border-radius: 10px;
    background: var(--green-deep); color: var(--green-light);
    display: grid; place-items: center; font-size: 1rem; flex-shrink: 0;
  }
  .contact-detail-text p { font-size: 0.8rem; color: var(--gray-mid); }
  .contact-detail-text strong { font-size: 0.92rem; color: var(--text-dark); }
  .contact-form { display: flex; flex-direction: column; gap: 1.2rem; }
  .form-group { display: flex; flex-direction: column; gap: 0.45rem; }
  .form-group label { font-size: 0.82rem; font-weight: 600; color: var(--text-dark); letter-spacing: 0.04em; }
  .form-group input,
  .form-group textarea {
    padding: 0.9rem 1.2rem;
    border: 1.5px solid var(--gray-soft);
    border-radius: 10px;
    font-family: var(--font-body); font-size: 0.9rem;
    background: #f8faf9;
    transition: border-color 0.2s, box-shadow 0.2s;
    outline: none; resize: vertical;
  }
  .form-group input:focus,
  .form-group textarea:focus {
    border-color: var(--green-accent);
    box-shadow: 0 0 0 4px rgba(45,155,99,0.1);
    background: var(--white-pure);
  }
  .form-group textarea { min-height: 130px; }
  .contact-form .btn-primary { align-self: flex-start; margin-top: 0.5rem; }

  /* ─── FOOTER ─── */
  footer {
    background: var(--green-deep);
    padding: 3.5rem 5% 2rem;
    text-align: center;
  }
  .footer-logo {
    font-family: var(--font-display); font-size: 1.8rem; font-weight: 700;
    color: var(--white); margin-bottom: 0.6rem; display: block;
  }
  .footer-logo span { color: var(--green-light); }
  .footer-tagline { font-size: 0.85rem; color: rgba(247,245,240,0.45); margin-bottom: 2rem; }
  .footer-social { display: flex; justify-content: center; gap: 1rem; margin-bottom: 2rem; }
  .social-link {
    width: 40px; height: 40px; border-radius: 10px;
    background: rgba(255,255,255,0.06);
    border: 1px solid rgba(255,255,255,0.1);
    display: grid; place-items: center;
    text-decoration: none; color: rgba(247,245,240,0.7);
    font-size: 1rem; transition: background 0.2s, color 0.2s, border-color 0.2s;
  }
  .social-link:hover { background: var(--green-accent); color: var(--white); border-color: var(--green-accent); }
  .footer-divider { height: 1px; background: rgba(255,255,255,0.08); margin-bottom: 1.5rem; }
  .footer-copy { font-size: 0.8rem; color: rgba(247,245,240,0.35); }

  /* ─── SCROLL ANIMATIONS ─── */
  .reveal { opacity: 0; transform: translateY(30px); transition: opacity 0.7s, transform 0.7s; }
  .reveal.visible { opacity: 1; transform: none; }
  .reveal-delay-1 { transition-delay: 0.1s; }
  .reveal-delay-2 { transition-delay: 0.2s; }
  .reveal-delay-3 { transition-delay: 0.3s; }
  .reveal-delay-4 { transition-delay: 0.4s; }

  /* ─── SCROLL TO TOP ─── */
  #scrollTop {
    position: fixed; bottom: 2rem; right: 2rem;
    width: 44px; height: 44px; border-radius: 50%;
    background: var(--green-accent); color: var(--white);
    border: none; cursor: pointer; font-size: 1.2rem;
    display: grid; place-items: center;
    box-shadow: 0 8px 24px rgba(45,155,99,0.4);
    opacity: 0; pointer-events: none;
    transition: opacity 0.3s, transform 0.3s;
    z-index: 99;
  }
  #scrollTop.show { opacity: 1; pointer-events: all; }
  #scrollTop:hover { transform: translateY(-3px); }

  /* ─── RESPONSIVE ─── */
  @media (max-width: 900px) {
    .hero-grid { grid-template-columns: 1fr; gap: 2.5rem; text-align: center; }
    .hero-sub { margin: 0 auto 2.5rem; }
    .hero-visual { order: -1; max-width: 400px; margin: 0 auto; }
    .hero-stats { justify-content: center; }
    .about-grid, .course-wrapper, .contact-grid { grid-template-columns: 1fr; gap: 3rem; }
    .about-image { max-width: 400px; }
    .problems-grid { grid-template-columns: 1fr; }
    .benefits-grid { grid-template-columns: 1fr 1fr; }
    .testi-grid { grid-template-columns: 1fr; max-width: 500px; margin: 0 auto; }
    nav { padding: 1rem 5%; }
    .nav-links { display: none; }
    .nav-links.open {
      display: flex; flex-direction: column;
      position: fixed; top: 60px; left: 0; right: 0;
      background: rgba(13,27,20,0.98); padding: 2rem;
      gap: 1.5rem; z-index: 99;
    }
    .hamburger { display: flex; }
  }
  @media (max-width: 600px) {
    .benefits-grid { grid-template-columns: 1fr; }
    .hero-stats { flex-wrap: wrap; gap: 1.5rem; }
    section { padding: 4rem 5%; }
  }
</style>
</head>
<body>

<!-- NAV -->
<nav id="navbar">
  <div class="nav-logo">Positive<span>Souls</span></div>
  <ul class="nav-links" id="navLinks">
    <li><a href="#about">About</a></li>
    <li><a href="#course">Course</a></li>
    <li><a href="#benefits">Benefits</a></li>
    <li><a href="#testimonials">Stories</a></li>
    <li><a href="#pricing">Pricing</a></li>
    <li><a href="#contact" class="nav-cta">Enroll Now</a></li>
  </ul>
  <div class="hamburger" id="hamburger" onclick="toggleMenu()">
    <span></span><span></span><span></span>
  </div>
</nav>

<!-- HERO -->
<section id="hero">
  <div class="hero-bg-orb orb1"></div>
  <div class="hero-bg-orb orb2"></div>
  <div class="hero-bg-orb orb3"></div>
  <div class="hero-grid">
    <div class="hero-content">
      <div class="hero-eyebrow">Positive Souls</div>
      <h1 class="hero-title">
        Build Powerful<br>
        <em>Self Discipline</em><br>
        and Transform Your Life
      </h1>
      <p class="hero-sub">
        Learn daily habits, deep focus, and an unbreakable mindset that lead to lasting success — one intentional day at a time.
      </p>
      <div>
        <a href="#pricing" class="btn-primary">Start Your Transformation</a>
        <a href="#course" class="btn-secondary">Learn More</a>
      </div>
      <div class="hero-stats">
        <div class="stat-item">
          <div class="stat-num">2,400+</div>
          <div class="stat-label">Students Enrolled</div>
        </div>
        <div class="stat-item">
          <div class="stat-num">94%</div>
          <div class="stat-label">Success Rate</div>
        </div>
        <div class="stat-item">
          <div class="stat-num">30-Day</div>
          <div class="stat-label">Guarantee</div>
        </div>
      </div>
    </div>
    <div class="hero-visual">
      <div class="hero-image-wrap">
        <img src="https://images.unsplash.com/photo-1506905925346-21bda4d32df4?w=800&q=80" alt="Mountain peak - symbol of discipline and achievement">
      </div>
      <div class="hero-badge">
        <div class="hero-badge-title">Featured Program</div>
        <div class="hero-badge-text">Self Discipline Mastery</div>
        <div class="hero-badge-sub">6 Modules · 40+ Lessons</div>
      </div>
    </div>
  </div>
</section>

<!-- ABOUT -->
<section id="about">
  <div class="about-grid">
    <div class="about-image reveal">
      <div class="about-decoration"></div>
      <img src="https://images.unsplash.com/photo-1522202176988-66273c2fd55f?w=800&q=80" alt="Focused individual working with discipline">
    </div>
    <div class="about-text reveal reveal-delay-1">
      <div class="section-label">Our Mission</div>
      <h2 class="section-title">We Help People Become the Best Version of Themselves</h2>
      <p class="section-body">
        At Positive Souls, we believe that every person carries the potential for extraordinary discipline and growth. Our mission is to give you the tools, systems, and mindset shifts to unlock that potential — so you can build the life you've always envisioned.
      </p>
      <div class="mission-pillars">
        <div class="pillar">
          <div class="pillar-icon">🧠</div>
          <div class="pillar-text">
            <h4>Rewire Your Mindset</h4>
            <p>Transform how you think about challenges, habits, and daily effort.</p>
          </div>
        </div>
        <div class="pillar">
          <div class="pillar-icon">🔄</div>
          <div class="pillar-text">
            <h4>Build Lasting Habits</h4>
            <p>Science-backed habit systems that stick and compound over time.</p>
          </div>
        </div>
        <div class="pillar">
          <div class="pillar-icon">🎯</div>
          <div class="pillar-text">
            <h4>Master Self-Discipline</h4>
            <p>Develop the focus and consistency to achieve any goal you set.</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- PROBLEMS -->
<section id="problems">
  <div class="container">
    <div class="section-label reveal">Do You Recognize Yourself?</div>
    <h2 class="section-title reveal reveal-delay-1" style="color:var(--white)">Common Struggles That Hold People Back</h2>
    <p class="section-body reveal reveal-delay-2">You're not lazy. You're not broken. These patterns are simply habits that haven't been reprogrammed — yet.</p>
    <div class="problems-grid">
      <div class="problem-card reveal reveal-delay-1">
        <div class="problem-number">01</div>
        <div class="problem-icon">😔</div>
        <h3>Procrastination</h3>
        <p>You know what needs to be done, but you keep putting it off. Days turn into weeks and the goals stay out of reach.</p>
      </div>
      <div class="problem-card reveal reveal-delay-2">
        <div class="problem-number">02</div>
        <div class="problem-icon">🌀</div>
        <h3>Lack of Focus</h3>
        <p>Distracted by phones, noise, and endless to-do lists — your energy is scattered and your deep work suffers.</p>
      </div>
      <div class="problem-card reveal reveal-delay-3">
        <div class="problem-number">03</div>
        <div class="problem-icon">⛓️</div>
        <h3>Bad Habits</h3>
        <p>Patterns that drain your energy, time, and confidence. You know you should change them — but they always pull you back.</p>
      </div>
      <div class="problem-card reveal reveal-delay-4">
        <div class="problem-number">04</div>
        <div class="problem-icon">📉</div>
        <h3>No Consistency</h3>
        <p>You start strong but fade quickly. The motivation wave crashes and you're back at square one — feeling stuck and defeated.</p>
      </div>
    </div>
  </div>
</section>

<!-- COURSE -->
<section id="course">
  <div class="course-wrapper">
    <div class="course-info">
      <div class="section-label reveal">The Program</div>
      <h2 class="section-title reveal reveal-delay-1">Self Discipline Mastery</h2>
      <p class="section-body reveal reveal-delay-2">A comprehensive, step-by-step system designed to rebuild you from the inside out — with proven frameworks used by the world's highest performers.</p>
      <div class="course-modules reveal reveal-delay-3">
        <div class="module">
          <div class="module-num">01</div>
          <div class="module-text">
            <h4>Habit Building System</h4>
            <p>Design your personal habit stack using behavioural science and daily rituals that create momentum.</p>
          </div>
        </div>
        <div class="module">
          <div class="module-num">02</div>
          <div class="module-text">
            <h4>Daily Discipline Routines</h4>
            <p>A morning-to-night framework that builds structure, reduces decision fatigue, and sustains your energy.</p>
          </div>
        </div>
        <div class="module">
          <div class="module-num">03</div>
          <div class="module-text">
            <h4>Productivity Techniques</h4>
            <p>Deep work strategies, time-blocking, and focus tools to multiply your output without burning out.</p>
          </div>
        </div>
        <div class="module">
          <div class="module-num">04</div>
          <div class="module-text">
            <h4>Mental Strength Training</h4>
            <p>Resilience practices, journaling systems, and mindset reframes to keep you going when it gets hard.</p>
          </div>
        </div>
      </div>
    </div>
    <div class="course-visual reveal reveal-delay-2">
      <div class="course-mockup">
        <img src="https://images.unsplash.com/photo-1517486808906-6ca8b3f04846?w=700&q=80" alt="Students learning and growing together">
        <div class="course-tag">Bestseller 🏆</div>
        <div class="course-ribbon">
          <div class="ribbon-title">Enrolled Course</div>
          <div class="ribbon-name">Self Discipline Mastery</div>
          <div class="ribbon-meta">6 Modules · 40+ Video Lessons · Lifetime Access</div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- BENEFITS -->
<section id="benefits">
  <div class="benefits-header reveal">
    <div class="section-label">What You Gain</div>
    <h2 class="section-title">The Life That Awaits on the Other Side</h2>
  </div>
  <div class="benefits-grid">
    <div class="benefit-card reveal reveal-delay-1">
      <div class="benefit-icon">🎯</div>
      <h3>Laser-Sharp Focus</h3>
      <p>Train your attention like a muscle. Eliminate distractions and do your most important work with clarity and calm.</p>
    </div>
    <div class="benefit-card reveal reveal-delay-2">
      <div class="benefit-icon">💪</div>
      <h3>Iron Self-Control</h3>
      <p>Resist impulses, say no to what doesn't serve you, and act from your values rather than your emotions.</p>
    </div>
    <div class="benefit-card reveal reveal-delay-3">
      <div class="benefit-icon">🌱</div>
      <h3>Better Daily Habits</h3>
      <p>Replace destructive patterns with empowering routines that run automatically — so growth becomes effortless.</p>
    </div>
    <div class="benefit-card reveal reveal-delay-1">
      <div class="benefit-icon">🚀</div>
      <h3>Achieve Goals Faster</h3>
      <p>With systems in place, your goals stop feeling impossible. Watch consistent action compound into extraordinary results.</p>
    </div>
    <div class="benefit-card reveal reveal-delay-2">
      <div class="benefit-icon">🧘</div>
      <h3>Inner Peace & Clarity</h3>
      <p>A disciplined mind is a calm mind. Reduce anxiety and overwhelm by taking control of your time and energy.</p>
    </div>
    <div class="benefit-card reveal reveal-delay-3">
      <div class="benefit-icon">🏆</div>
      <h3>Unshakeable Confidence</h3>
      <p>Every promise you keep to yourself builds self-trust. Show up as the person you know you're capable of being.</p>
    </div>
  </div>
</section>

<!-- TESTIMONIALS -->
<section id="testimonials">
  <div class="testi-header reveal">
    <div class="section-label">Student Stories</div>
    <h2 class="section-title">Real Lives. Real Transformation.</h2>
  </div>
  <div class="testi-grid">
    <div class="testi-card reveal reveal-delay-1">
      <div class="testi-quote">"</div>
      <p class="testi-text">This course completely rewired how I start my day. Within three weeks I had built a morning routine I actually stick to — and my productivity doubled. I finally feel like I'm in control of my life.</p>
      <div class="testi-stars">★★★★★</div>
      <div class="testi-author">
        <div class="testi-avatar">
          <img src="https://images.unsplash.com/photo-1531123897727-8f129e1688ce?w=100&q=80" alt="Sarah M.">
        </div>
        <div>
          <div class="testi-name">Sarah M.</div>
          <div class="testi-role">Marketing Manager, New York</div>
        </div>
      </div>
    </div>
    <div class="testi-card reveal reveal-delay-2">
      <div class="testi-quote">"</div>
      <p class="testi-text">I've tried every productivity app and book out there. Nothing clicked until Positive Souls. The habit stacking module alone was worth 10x the price. I went from procrastinator to someone who ships every day.</p>
      <div class="testi-stars">★★★★★</div>
      <div class="testi-author">
        <div class="testi-avatar">
          <img src="https://images.unsplash.com/photo-1507003211169-0a1dd7228f2d?w=100&q=80" alt="James T.">
        </div>
        <div>
          <div class="testi-name">James T.</div>
          <div class="testi-role">Freelance Designer, London</div>
        </div>
      </div>
    </div>
    <div class="testi-card reveal reveal-delay-3">
      <div class="testi-quote">"</div>
      <p class="testi-text">The mental strength module hit me hard in the best way. I used to give up the moment things felt uncomfortable. Now I push through. I've lost 12kg, finished my degree, and finally started my business.</p>
      <div class="testi-stars">★★★★★</div>
      <div class="testi-author">
        <div class="testi-avatar">
          <img src="https://images.unsplash.com/photo-1534528741775-53994a69daeb?w=100&q=80" alt="Priya K.">
        </div>
        <div>
          <div class="testi-name">Priya K.</div>
          <div class="testi-role">Entrepreneur, Singapore</div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- PRICING -->
<section id="pricing">
  <div class="pricing-header reveal">
    <div class="section-label">Invest in Yourself</div>
    <h2 class="section-title">One Investment. A Lifetime of Discipline.</h2>
  </div>
  <div class="pricing-card reveal reveal-delay-1">
    <div class="pricing-badge">Most Popular</div>
    <div class="pricing-card-label">Complete Program</div>
    <div class="pricing-card-name">Self Discipline Mastery</div>
    <div class="pricing-divider"></div>
    <div class="price-amount"><sup>$</sup>197</div>
    <div class="price-note">One-time payment · Lifetime access</div>
    <ul class="pricing-features">
      <li>6 in-depth modules with 40+ video lessons</li>
      <li>Printable habit tracker & daily planner</li>
      <li>Mental strength audio meditations</li>
      <li>Private community access for accountability</li>
      <li>Lifetime updates — the course grows with you</li>
      <li>30-day money-back guarantee</li>
    </ul>
    <a href="#contact" class="btn-primary">Enroll Now — Start Today</a>
    <p class="guarantee">🔒 30-day money-back guarantee. No questions asked.</p>
  </div>
</section>

<!-- CONTACT -->
<section id="contact">
  <div class="contact-grid">
    <div class="contact-info reveal">
      <div class="section-label">Get in Touch</div>
      <h2 class="section-title">Have Questions? We'd Love to Hear From You</h2>
      <p class="section-body">Whether you want to know more about the course, need support, or just want to say hello — our team is here for you.</p>
      <div style="margin-top: 2rem;">
        <div class="contact-detail">
          <div class="contact-icon">📧</div>
          <div class="contact-detail-text">
            <p>Email</p>
            <strong>hello@positivesouls.com</strong>
          </div>
        </div>
        <div class="contact-detail">
          <div class="contact-icon">💬</div>
          <div class="contact-detail-text">
            <p>Response Time</p>
            <strong>Within 24 hours</strong>
          </div>
        </div>
        <div class="contact-detail">
          <div class="contact-icon">🌍</div>
          <div class="contact-detail-text">
            <p>Community</p>
            <strong>Global · Always Online</strong>
          </div>
        </div>
      </div>
    </div>
    <div class="reveal reveal-delay-2">
      <form class="contact-form" onsubmit="handleSubmit(event)">
        <div class="form-group">
          <label for="name">Your Name</label>
          <input type="text" id="name" placeholder="e.g. Alex Johnson" required>
        </div>
        <div class="form-group">
          <label for="email">Email Address</label>
          <input type="email" id="email" placeholder="you@example.com" required>
        </div>
        <div class="form-group">
          <label for="message">Your Message</label>
          <textarea id="message" placeholder="Tell us how we can help you..." required></textarea>
        </div>
        <button type="submit" class="btn-primary">Send Message ✉️</button>
        <div id="formSuccess" style="display:none; color: var(--green-accent); font-size: 0.9rem; margin-top: 0.5rem;">
          ✓ Message sent! We'll be in touch within 24 hours.
        </div>
      </form>
    </div>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <a href="#hero" class="footer-logo">Positive<span>Souls</span></a>
  <p class="footer-tagline">Build discipline. Build habits. Build your life.</p>
  <div class="footer-social">
    <a class="social-link" href="#" title="Instagram" aria-label="Instagram">
      <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><rect x="2" y="2" width="20" height="20" rx="5"/><circle cx="12" cy="12" r="4"/><circle cx="17.5" cy="6.5" r="1" fill="currentColor" stroke="none"/></svg>
    </a>
    <a class="social-link" href="#" title="YouTube" aria-label="YouTube">
      <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M22.54 6.42A2.78 2.78 0 0 0 20.6 4.46C18.88 4 12 4 12 4s-6.88 0-8.6.46A2.78 2.78 0 0 0 1.46 6.42 29 29 0 0 0 1 12a29 29 0 0 0 .46 5.58A2.78 2.78 0 0 0 3.4 19.54C5.12 20 12 20 12 20s6.88 0 8.6-.46a2.78 2.78 0 0 0 1.94-1.96A29 29 0 0 0 23 12a29 29 0 0 0-.46-5.58z"/><polygon points="9.75 15.02 15.5 12 9.75 8.98 9.75 15.02" fill="currentColor" stroke="none"/></svg>
    </a>
    <a class="social-link" href="#" title="Twitter / X" aria-label="Twitter">
      <svg width="18" height="18" viewBox="0 0 24 24" fill="currentColor"><path d="M18.244 2.25h3.308l-7.227 8.26 8.502 11.24H16.17l-5.214-6.817L4.99 21.75H1.68l7.73-8.835L1.254 2.25H8.08l4.713 6.231zm-1.161 17.52h1.833L7.084 4.126H5.117z"/></svg>
    </a>
    <a class="social-link" href="#" title="Facebook" aria-label="Facebook">
      <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M18 2h-3a5 5 0 0 0-5 5v3H7v4h3v8h4v-8h3l1-4h-4V7a1 1 0 0 1 1-1h3z"/></svg>
    </a>
    <a class="social-link" href="#" title="LinkedIn" aria-label="LinkedIn">
      <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M16 8a6 6 0 0 1 6 6v7h-4v-7a2 2 0 0 0-2-2 2 2 0 0 0-2 2v7h-4v-7a6 6 0 0 1 6-6z"/><rect x="2" y="9" width="4" height="12"/><circle cx="4" cy="4" r="2"/></svg>
    </a>
  </div>
  <div class="footer-divider"></div>
  <p class="footer-copy">© Positive Souls · All rights reserved · Built with purpose 🌿</p>
</footer>

<!-- SCROLL TOP BUTTON -->
<button id="scrollTop" onclick="window.scrollTo({top:0,behavior:'smooth'})" aria-label="Back to top">↑</button>

<script>
  // Hamburger menu
  function toggleMenu() {
    const links = document.getElementById('navLinks');
    links.classList.toggle('open');
  }

  // Close menu on link click
  document.querySelectorAll('.nav-links a').forEach(link => {
    link.addEventListener('click', () => {
      document.getElementById('navLinks').classList.remove('open');
    });
  });

  // Scroll reveal
  const observer = new IntersectionObserver((entries) => {
    entries.forEach(entry => {
      if (entry.isIntersecting) {
        entry.target.classList.add('visible');
      }
    });
  }, { threshold: 0.12 });

  document.querySelectorAll('.reveal').forEach(el => observer.observe(el));

  // Scroll-to-top button
  const scrollTopBtn = document.getElementById('scrollTop');
  window.addEventListener('scroll', () => {
    scrollTopBtn.classList.toggle('show', window.scrollY > 500);
  });

  // Contact form
  function handleSubmit(e) {
    e.preventDefault();
    const success = document.getElementById('formSuccess');
    success.style.display = 'block';
    e.target.reset();
    setTimeout(() => success.style.display = 'none', 5000);
  }

  // Navbar scroll effect
  window.addEventListener('scroll', () => {
    const nav = document.getElementById('navbar');
    if (window.scrollY > 80) {
      nav.style.background = 'rgba(13,27,20,0.98)';
    } else {
      nav.style.background = 'rgba(13,27,20,0.92)';
    }
  });

  // Animate hero on load
  window.addEventListener('DOMContentLoaded', () => {
    document.querySelectorAll('#hero .hero-content > *').forEach((el, i) => {
      el.style.opacity = '0';
      el.style.transform = 'translateY(20px)';
      el.style.transition = `opacity 0.7s ${i * 0.15}s, transform 0.7s ${i * 0.15}s`;
      setTimeout(() => {
        el.style.opacity = '1';
        el.style.transform = 'none';
      }, 100);
    });
    const heroVisual = document.querySelector('.hero-visual');
    if (heroVisual) {
      heroVisual.style.opacity = '0';
      heroVisual.style.transform = 'translateX(30px)';
      heroVisual.style.transition = 'opacity 1s 0.5s, transform 1s 0.5s';
      setTimeout(() => {
        heroVisual.style.opacity = '1';
        heroVisual.style.transform = 'none';
      }, 100);
    }
  });
</script>
</body>
</html>

