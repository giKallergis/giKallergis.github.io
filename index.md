<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Georgios Kallergis | ML Researcher — Drug Discovery</title>
  <meta name="description" content="ML researcher building transformer language models for drug discovery. PhD from Helmholtz Centre for Infection Research.">
  <meta property="og:title" content="Georgios Kallergis">
  <meta property="og:description" content="ML researcher — transformer language models for drug discovery">
  <meta property="og:url" content="https://gikallergis.github.io/">
  <link rel="canonical" href="https://gikallergis.github.io/">
  <link href="https://fonts.googleapis.com/css2?family=Source+Serif+4:ital,wght@0,400;0,600;0,700;1,400&family=Inter:wght@400;500;600&family=JetBrains+Mono:wght@400;500&display=swap" rel="stylesheet">
  <style>
    :root {
      --ink: #1a1a2e;
      --body: #3d3d5c;
      --muted: #6b6b8a;
      --border: #d8d8e8;
      --surface: #f0eff5;
      --bg: #faf9fe;
      --accent: #4361ee;
      --accent-soft: #eef0fd;
      --highlight: #e8faf0;
      --highlight-text: #1b7a44;
    }

    * { margin: 0; padding: 0; box-sizing: border-box; }

    body {
      font-family: 'Inter', -apple-system, sans-serif;
      color: var(--body);
      background: var(--bg);
      line-height: 1.65;
      -webkit-font-smoothing: antialiased;
    }

    .container {
      max-width: 740px;
      margin: 0 auto;
      padding: 0 24px;
    }

    /* ── Header ── */
    header { padding: 56px 0 0; }

    .header-row {
      display: flex;
      align-items: center;
      gap: 24px;
      margin-bottom: 20px;
    }

    .avatar {
      width: 88px;
      height: 88px;
      border-radius: 50%;
      background: linear-gradient(135deg, var(--accent), #7c3aed);
      display: flex;
      align-items: center;
      justify-content: center;
      font-family: 'Source Serif 4', serif;
      font-size: 34px;
      font-weight: 700;
      color: white;
      flex-shrink: 0;
      letter-spacing: -1px;
    }

    h1 {
      font-family: 'Source Serif 4', serif;
      font-size: 30px;
      font-weight: 700;
      color: var(--ink);
      line-height: 1.2;
      letter-spacing: -0.5px;
    }

    .tagline { font-size: 14px; color: var(--muted); margin-top: 3px; }

    .intro {
      font-size: 15.5px;
      color: var(--body);
      line-height: 1.7;
      margin-bottom: 12px;
    }
    .intro a {
      color: var(--accent);
      text-decoration: none;
      border-bottom: 1px solid transparent;
      transition: border-color 0.15s;
    }
    .intro a:hover { border-bottom-color: var(--accent); }

    .status {
      display: inline-block;
      background: var(--highlight);
      color: var(--highlight-text);
      font-size: 13px;
      font-weight: 500;
      padding: 5px 14px;
      border-radius: 20px;
      margin-bottom: 28px;
    }

    .quick-links {
      display: flex;
      gap: 10px;
      flex-wrap: wrap;
      margin-bottom: 32px;
    }
    .quick-links a {
      display: inline-flex;
      align-items: center;
      gap: 6px;
      font-size: 13px;
      font-weight: 500;
      color: var(--body);
      text-decoration: none;
      padding: 7px 14px;
      border: 1px solid var(--border);
      border-radius: 8px;
      transition: all 0.15s;
    }
    .quick-links a:hover {
      border-color: var(--accent);
      color: var(--accent);
      background: var(--accent-soft);
    }

    /* ── Tabs ── */
    .tab-bar {
      display: flex;
      gap: 0;
      border-bottom: 2px solid var(--border);
      margin-bottom: 32px;
      overflow-x: auto;
      -webkit-overflow-scrolling: touch;
    }

    .tab-btn {
      font-family: 'Inter', sans-serif;
      font-size: 14px;
      font-weight: 500;
      color: var(--muted);
      background: none;
      border: none;
      padding: 12px 20px;
      cursor: pointer;
      position: relative;
      white-space: nowrap;
      transition: color 0.15s;
    }
    .tab-btn:hover { color: var(--ink); }
    .tab-btn.active { color: var(--accent); }
    .tab-btn.active::after {
      content: '';
      position: absolute;
      bottom: -2px;
      left: 0;
      right: 0;
      height: 2px;
      background: var(--accent);
      border-radius: 1px 1px 0 0;
    }

    /* ── Panels ── */
    .tab-panel {
      display: none;
      animation: fadeIn 0.25s ease;
    }
    .tab-panel.active { display: block; }

    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(6px); }
      to   { opacity: 1; transform: translateY(0); }
    }

    h2 {
      font-family: 'Source Serif 4', serif;
      font-size: 21px;
      font-weight: 600;
      color: var(--ink);
      margin-bottom: 18px;
      letter-spacing: -0.3px;
    }

    h3 {
      font-family: 'Source Serif 4', serif;
      font-size: 17px;
      font-weight: 600;
      color: var(--ink);
      margin: 28px 0 12px;
    }

    p + p { margin-top: 12px; }

    /* ── Publication card ── */
    .pub-card {
      background: white;
      border: 1px solid var(--border);
      border-radius: 12px;
      padding: 22px;
      margin-bottom: 16px;
      transition: box-shadow 0.2s;
    }
    .pub-card:hover { box-shadow: 0 4px 20px rgba(67,97,238,0.07); }

    .pub-venue {
      font-size: 11px;
      font-weight: 600;
      text-transform: uppercase;
      letter-spacing: 0.8px;
      color: var(--accent);
      margin-bottom: 6px;
    }
    .pub-title {
      font-family: 'Source Serif 4', serif;
      font-size: 16px;
      font-weight: 600;
      color: var(--ink);
      line-height: 1.45;
      margin-bottom: 6px;
    }
    .pub-title a { color: inherit; text-decoration: none; border-bottom: 1px solid transparent; transition: border-color 0.15s; }
    .pub-title a:hover { border-bottom-color: var(--ink); }

    .pub-authors { font-size: 13.5px; color: var(--muted); margin-bottom: 10px; }
    .pub-authors strong { color: var(--ink); font-weight: 600; }

    .pub-summary {
      font-size: 13.5px;
      color: var(--body);
      line-height: 1.65;
      padding-top: 10px;
      border-top: 1px solid var(--border);
    }

    /* ── Repo grid ── */
    .repo-grid { display: grid; gap: 10px; }

    .repo-item {
      display: flex;
      align-items: flex-start;
      gap: 12px;
      padding: 14px 16px;
      background: white;
      border: 1px solid var(--border);
      border-radius: 10px;
      text-decoration: none;
      transition: all 0.15s;
    }
    .repo-item:hover { border-color: var(--accent); box-shadow: 0 2px 12px rgba(67,97,238,0.06); }

    .repo-icon {
      width: 34px;
      height: 34px;
      border-radius: 8px;
      background: var(--accent-soft);
      display: flex;
      align-items: center;
      justify-content: center;
      flex-shrink: 0;
      font-size: 15px;
    }
    .repo-name {
      font-family: 'JetBrains Mono', monospace;
      font-size: 13.5px;
      font-weight: 500;
      color: var(--ink);
    }
    .repo-desc { font-size: 13px; color: var(--muted); margin-top: 2px; line-height: 1.5; }

    /* ── Tags ── */
    .tag-row { display: flex; flex-wrap: wrap; gap: 8px; }

    .tag {
      font-family: 'JetBrains Mono', monospace;
      font-size: 12px;
      font-weight: 500;
      color: var(--body);
      padding: 5px 12px;
      background: var(--surface);
      border-radius: 6px;
    }

    .tag--muted {
      font-family: 'Inter', sans-serif;
      font-size: 13px;
      color: var(--muted);
      padding: 6px 14px;
      background: var(--surface);
      border-radius: 6px;
    }

    /* ── About ── */
    .about-block {
      font-size: 15px;
      line-height: 1.75;
      color: var(--body);
    }
    .about-block a { color: var(--accent); text-decoration: none; }
    .about-block a:hover { text-decoration: underline; }

    /* ── Contact ── */
    .contact-card {
      background: white;
      border: 1px solid var(--border);
      border-radius: 12px;
      padding: 24px;
    }
    .contact-row {
      display: flex;
      align-items: center;
      gap: 12px;
      padding: 10px 0;
    }
    .contact-row + .contact-row { border-top: 1px solid var(--border); }
    .contact-label { font-size: 13px; color: var(--muted); width: 70px; flex-shrink: 0; }
    .contact-value a { color: var(--accent); text-decoration: none; font-size: 14px; font-weight: 500; }
    .contact-value a:hover { text-decoration: underline; }

    /* ── Footer ── */
    footer {
      padding: 32px 0 48px;
      border-top: 1px solid var(--border);
      margin-top: 48px;
      text-align: center;
      font-size: 13px;
      color: var(--muted);
    }

    @media (max-width: 520px) {
      header { padding-top: 36px; }
      .header-row { gap: 16px; }
      .avatar { width: 64px; height: 64px; font-size: 26px; }
      h1 { font-size: 24px; }
      .tab-btn { padding: 10px 14px; font-size: 13px; }
      .quick-links a { font-size: 12px; padding: 6px 10px; }
    }
  </style>
</head>
<body>

<div class="container">

  <header>
    <div class="header-row">
      <div class="avatar">GK</div>
      <div>
        <h1>Georgios Kallergis</h1>
        <p class="tagline">ML Researcher · Drug Discovery</p>
      </div>
    </div>
    <p class="intro">
      I recently completed my PhD at the
      <a href="https://www.helmholtz-hzi.de/">Helmholtz Centre for Infection Research</a>,
      where I developed <strong>ChemLM</strong> — a transformer-based chemical language model
      that outperformed state-of-the-art models at identifying drug candidates against
      <em>Pseudomonas aeruginosa</em>, a WHO-priority multidrug-resistant pathogen.
    </p>
    <span class="status">🔬 Open to ML / AI Scientist roles in pharma, biotech &amp; drug discovery</span>
    <div class="quick-links">
      <a href="https://www.nature.com/articles/s42004-025-01484-4">📄 Paper</a>
      <a href="https://github.com/hzi-bifo/ChemLM">💻 ChemLM</a>
      <a href="https://linkedin.com/in/georgios-kallergis">👤 LinkedIn</a>
      <a href="https://github.com/giKallergis">🐙 GitHub</a>
      <a href="mailto:gkallergis7@gmail.com">✉️ Email</a>
    </div>
  </header>

  <!-- Tab bar -->
  <nav class="tab-bar" role="tablist">
    <button class="tab-btn active" role="tab" data-tab="publications">Publications</button>
    <button class="tab-btn" role="tab" data-tab="projects">Projects</button>
    <button class="tab-btn" role="tab" data-tab="about">About</button>
    <button class="tab-btn" role="tab" data-tab="contact">Contact</button>
  </nav>

  <!-- PUBLICATIONS -->
  <div class="tab-panel active" id="publications" role="tabpanel">
    <h2>Selected Publication</h2>
    <div class="pub-card">
      <p class="pub-venue">Communications Chemistry · Nature · 2025</p>
      <p class="pub-title">
        <a href="https://www.nature.com/articles/s42004-025-01484-4">
          Domain adaptable language modeling of chemical compounds identifies potent pathoblockers for <em>Pseudomonas aeruginosa</em>
        </a>
      </p>
      <p class="pub-authors">
        <strong>Kallergis, G.</strong>, Asgari, E., Empting, M., Hirsch, A.K.H., Klawonn, F., &amp; McHardy, A.C.
      </p>
      <p class="pub-summary">
        ChemLM uses domain-adaptive pretraining on chemical SMILES strings to generate and rank novel compounds.
        Applied to anti-virulence drug discovery, it identified potent pathoblockers validated in vitro —
        outperforming existing generative chemistry models on this task.
      </p>
    </div>
    <p style="font-size:14px; color:var(--muted); margin-top:16px;">
      More publications to be added as ongoing work is published.
    </p>
  </div>

  <!-- PROJECTS -->
  <div class="tab-panel" id="projects" role="tabpanel">
    <h2>Repositories</h2>
    <div class="repo-grid">
      <a class="repo-item" href="https://github.com/hzi-bifo/ChemLM">
        <div class="repo-icon">🧬</div>
        <div>
          <div class="repo-name">ChemLM</div>
          <div class="repo-desc">Transformer chemical language model for drug candidate generation</div>
        </div>
      </a>
      <a class="repo-item" href="https://github.com/giKallergis/esm2-embedding-service">
        <div class="repo-icon">🔗</div>
        <div>
          <div class="repo-name">esm2-embedding-service</div>
          <div class="repo-desc">FastAPI service for protein embeddings from ESM-2</div>
        </div>
      </a>
      <a class="repo-item" href="https://github.com/giKallergis/medmnist-vit-benchmark">
        <div class="repo-icon">🩺</div>
        <div>
          <div class="repo-name">medmnist-vit-benchmark</div>
          <div class="repo-desc">Vision Transformer benchmark on BloodMNIST dataset</div>
        </div>
      </a>
      <a class="repo-item" href="https://github.com/hzi-bifo/seminar-plotting">
        <div class="repo-icon">📊</div>
        <div>
          <div class="repo-name">seminar-plotting</div>
          <div class="repo-desc">Data visualization course materials</div>
        </div>
      </a>
      <a class="repo-item" href="https://github.com/hzi-bifo/seminar-dlmb-2026-summer-public">
        <div class="repo-icon">🧠</div>
        <div>
          <div class="repo-name">seminar-dlmb</div>
          <div class="repo-desc">Deep Learning for Molecular Biology seminar</div>
        </div>
      </a>
    </div>

    <h3>Coming Soon</h3>
    <div class="tag-row">
      <span class="tag--muted">LoRA task adaptation</span>
      <span class="tag--muted">Contrastive learning</span>
      <span class="tag--muted">Drug–target interaction</span>
      <span class="tag--muted">Chemical space evaluation</span>
      <span class="tag--muted">Curriculum learning</span>
    </div>
  </div>

  <!-- ABOUT -->
  <div class="tab-panel" id="about" role="tabpanel">
    <h2>About</h2>
    <div class="about-block">
      <p>
        I'm a machine learning researcher focused on applying transformer architectures
        to molecular and biological data. My PhD work at the
        <a href="https://www.helmholtz-hzi.de/">Helmholtz Centre for Infection Research</a>
        (Braunschweig, Germany) centered on building generative language models over chemical
        SMILES representations to accelerate early-stage drug discovery against antimicrobial-resistant pathogens.
      </p>
      <p>
        Beyond ChemLM, I've worked on protein language models (ESM-2 embeddings),
        vision transformers for medical imaging, and deep learning curriculum development
        for graduate students in molecular biology.
      </p>
    </div>

    <h3>Technical Stack</h3>
    <div class="tag-row">
      <span class="tag">Python</span>
      <span class="tag">PyTorch</span>
      <span class="tag">HuggingFace</span>
      <span class="tag">Transformers</span>
      <span class="tag">scikit-learn</span>
      <span class="tag">RDKit</span>
      <span class="tag">FastAPI</span>
      <span class="tag">Docker</span>
      <span class="tag">Git</span>
      <span class="tag">Linux</span>
      <span class="tag">SLURM</span>
    </div>

    <h3>Education</h3>
    <div class="about-block">
      <p>
        <strong>PhD, Computational Biology / ML</strong><br>
        Helmholtz Centre for Infection Research, Braunschweig, Germany
      </p>
    </div>
  </div>

  <!-- CONTACT -->
  <div class="tab-panel" id="contact" role="tabpanel">
    <h2>Get in Touch</h2>
    <div class="contact-card">
      <div class="contact-row">
        <span class="contact-label">Email</span>
        <span class="contact-value"><a href="mailto:gkallergis7@gmail.com">gkallergis7@gmail.com</a></span>
      </div>
      <div class="contact-row">
        <span class="contact-label">LinkedIn</span>
        <span class="contact-value"><a href="https://linkedin.com/in/georgios-kallergis">georgios-kallergis</a></span>
      </div>
      <div class="contact-row">
        <span class="contact-label">GitHub</span>
        <span class="contact-value"><a href="https://github.com/giKallergis">giKallergis</a></span>
      </div>
    </div>
  </div>

  <footer>Built with GitHub Pages</footer>

</div>

<script>
  const tabs = document.querySelectorAll('.tab-btn');
  const panels = document.querySelectorAll('.tab-panel');

  tabs.forEach(btn => {
    btn.addEventListener('click', () => {
      const target = btn.dataset.tab;
      tabs.forEach(t => t.classList.remove('active'));
      panels.forEach(p => p.classList.remove('active'));
      btn.classList.add('active');
      document.getElementById(target).classList.add('active');
      history.replaceState(null, '', '#' + target);
    });
  });

  // Restore tab from URL hash
  window.addEventListener('DOMContentLoaded', () => {
    const hash = location.hash.replace('#', '');
    if (hash) {
      const btn = document.querySelector('[data-tab="' + hash + '"]');
      if (btn) btn.click();
    }
  });
</script>

</body>
</html>
