<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Jatin Chauhan – Applied AI Engineer</title>
<link href="https://fonts.googleapis.com/css2?family=DM+Mono:ital,wght@0,300;0,400;0,500;1,400&family=Fraunces:ital,opsz,wght@0,9..144,300;0,9..144,600;0,9..144,700;1,9..144,300&display=swap" rel="stylesheet">
<style>
  :root {
    --bg: #0d0f14;
    --surface: #13161d;
    --border: #1e232e;
    --accent: #5bffb5;
    --accent2: #4fa8ff;
    --text: #d6dce8;
    --muted: #6b7589;
    --heading: #ffffff;
    --tag-bg: #1a2030;
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }

  body {
    background: var(--bg);
    color: var(--text);
    font-family: 'DM Mono', monospace;
    font-size: 13px;
    line-height: 1.6;
    min-height: 100vh;
    padding: 40px 24px;
  }

  .page {
    max-width: 880px;
    margin: 0 auto;
    animation: fadeUp 0.6s ease both;
  }

  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(20px); }
    to   { opacity: 1; transform: translateY(0); }
  }

  /* ── HEADER ── */
  .header {
    display: grid;
    grid-template-columns: 1fr auto;
    align-items: start;
    gap: 24px;
    padding-bottom: 28px;
    border-bottom: 1px solid var(--border);
    margin-bottom: 28px;
  }

  .name {
    font-family: 'Fraunces', serif;
    font-size: 52px;
    font-weight: 700;
    color: var(--heading);
    line-height: 1;
    letter-spacing: -1px;
  }

  .name span { color: var(--accent); }

  .title-line {
    margin-top: 10px;
    font-size: 10.5px;
    letter-spacing: 3px;
    text-transform: uppercase;
    color: var(--muted);
  }

  .contact-block {
    text-align: right;
    font-size: 11.5px;
    color: var(--muted);
    line-height: 2.1;
  }

  .contact-block a { color: var(--accent2); text-decoration: none; }
  .contact-block a:hover { text-decoration: underline; }

  /* ── SUMMARY ── */
  .summary {
    background: var(--surface);
    border: 1px solid var(--border);
    border-left: 3px solid var(--accent);
    padding: 16px 20px;
    margin-bottom: 28px;
    font-family: 'Fraunces', serif;
    font-style: italic;
    font-size: 14.5px;
    color: #b0bdd4;
    line-height: 1.75;
    font-weight: 300;
  }

  /* ── BODY GRID ── */
  .body-grid {
    display: grid;
    grid-template-columns: 2fr 1fr;
    gap: 32px;
  }

  /* ── SECTION ── */
  .section { margin-bottom: 28px; }

  .section-label {
    font-size: 9.5px;
    letter-spacing: 4px;
    text-transform: uppercase;
    color: var(--accent);
    margin-bottom: 14px;
    display: flex;
    align-items: center;
    gap: 10px;
  }

  .section-label::after {
    content: '';
    flex: 1;
    height: 1px;
    background: var(--border);
  }

  /* ── JOB ── */
  .job { margin-bottom: 22px; }

  .job-header {
    display: flex;
    justify-content: space-between;
    align-items: baseline;
    margin-bottom: 2px;
  }

  .company {
    font-family: 'Fraunces', serif;
    font-size: 16px;
    font-weight: 600;
    color: var(--heading);
  }

  .date { font-size: 11px; color: var(--muted); }

  .role { color: var(--accent2); font-size: 11.5px; margin-bottom: 10px; }

  .sub-role {
    font-size: 11px;
    color: var(--accent);
    letter-spacing: 1.5px;
    text-transform: uppercase;
    margin: 10px 0 6px;
    opacity: 0.8;
  }

  .bullets { padding-left: 0; list-style: none; }

  .bullets li {
    position: relative;
    padding-left: 16px;
    margin-bottom: 5px;
    color: #99a8be;
    font-size: 12.5px;
    line-height: 1.55;
  }

  .bullets li::before {
    content: '›';
    position: absolute;
    left: 0;
    color: var(--accent);
    font-size: 14px;
  }

  .hl  { color: var(--accent);  font-weight: 500; }
  .hl2 { color: var(--accent2); }

  /* ── PROJECT ── */
  .project {
    background: var(--surface);
    border: 1px solid var(--border);
    padding: 13px 16px;
    margin-bottom: 10px;
    transition: border-color 0.2s;
  }

  .project:hover { border-color: var(--accent); }

  .project-name {
    font-family: 'Fraunces', serif;
    font-weight: 600;
    color: var(--heading);
    font-size: 14px;
    margin-bottom: 6px;
  }

  .project-bullets { padding-left: 0; list-style: none; }

  .project-bullets li {
    position: relative;
    padding-left: 14px;
    margin-bottom: 4px;
    color: #8896ae;
    font-size: 12px;
    line-height: 1.5;
  }

  .project-bullets li::before {
    content: '·';
    position: absolute;
    left: 0;
    color: var(--accent2);
  }

  /* ── SIDEBAR ── */
  .skills-group { margin-bottom: 16px; }

  .skills-group-name {
    font-size: 10px;
    color: var(--muted);
    letter-spacing: 2px;
    text-transform: uppercase;
    margin-bottom: 8px;
  }

  .tags { display: flex; flex-wrap: wrap; gap: 6px; }

  .tag {
    background: var(--tag-bg);
    border: 1px solid var(--border);
    color: #9caabb;
    font-size: 11px;
    padding: 3px 9px;
    border-radius: 2px;
    transition: border-color 0.15s, color 0.15s;
  }

  .tag:hover { border-color: var(--accent); color: var(--accent); cursor: default; }
  .tag.hot { border-color: #2a3a2e; background: #0e1f16; color: var(--accent); }

  /* ── METRIC BARS ── */
  .metric-row {
    display: flex;
    align-items: center;
    gap: 10px;
    margin-bottom: 8px;
  }

  .metric-label { font-size: 11px; color: var(--muted); width: 90px; flex-shrink: 0; }

  .bar-track {
    flex: 1;
    height: 4px;
    background: var(--border);
    border-radius: 2px;
    overflow: hidden;
  }

  .bar-fill {
    height: 100%;
    border-radius: 2px;
    background: var(--accent);
    animation: fillBar 1s ease both;
  }

  @keyframes fillBar { from { width: 0 !important; } }

  .metric-pct { font-size: 11px; color: var(--accent); width: 32px; text-align: right; }

  /* ── EDUCATION ── */
  .edu-item { margin-bottom: 14px; }

  .edu-school {
    font-family: 'Fraunces', serif;
    font-size: 14px;
    font-weight: 600;
    color: var(--heading);
  }

  .edu-detail { font-size: 11.5px; color: var(--muted); line-height: 1.8; }

  /* ── CERT / ACHIEVE ── */
  .cert-item {
    display: flex;
    gap: 8px;
    margin-bottom: 8px;
    font-size: 11.5px;
    color: #8896ae;
    align-items: flex-start;
  }

  .cert-dot {
    width: 6px; height: 6px;
    border-radius: 50%;
    background: var(--accent2);
    margin-top: 5px;
    flex-shrink: 0;
  }

  .cert-dot.green { background: var(--accent); }
</style>
</head>
<body>
<div class="page">

  <!-- HEADER -->
  <header class="header">
    <div>
      <div class="name">Jatin<span>.</span><br>Chauhan</div>
      <div class="title-line">Applied AI Engineer &nbsp;·&nbsp; Generative AI &amp; ML Systems &nbsp;·&nbsp; 2+ Years at Samsung</div>
    </div>
    <div class="contact-block">
      <div><a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="244e471d1d1514171317141c1c644349454d480a474b49">[email&#160;protected]</a></div>
      <div>+91 9911189974</div>
      <div>Dwarka Sector-8, New Delhi – 110077</div>
      <div><a href="https://www.linkedin.com/in/jatin-chauhan-a07153171/">linkedin.com/in/jatin-chauhan</a></div>
      <div><a href="https://github.com/chauhan-03">github.com/chauhan-03</a></div>
    </div>
  </header>

  <!-- SUMMARY -->
  <div class="summary">
    AI Engineer with 2+ years building production-grade ML &amp; GenAI systems for Samsung's large-scale consumer platforms.
    Experienced across the full stack — real-time inference, cloud-native pipelines, LLM-based automation, and
    embedded AI — serving millions of global devices.
  </div>

  <!-- BODY -->
  <div class="body-grid">
    <div>

      <!-- EXPERIENCE -->
      <div class="section">
        <div class="section-label">Experience</div>

        <!-- Samsung FTE -->
        <div class="job">
          <div class="job-header">
            <div class="company">Samsung Electronics</div>
            <div class="date">Jan 2024 – Present</div>
          </div>
          <div class="role">Software Engineer &nbsp;·&nbsp; New Delhi, India</div>

          <div class="sub-role">MS Copilot — Voice &amp; Audio Intelligence</div>
          <ul class="bullets">
            <li>Designed and optimised microservices for voice/audio intelligence in MS Copilot on Samsung TVs; delivered <span class="hl">10–15 production features</span> improving latency, throughput, and reliability at scale.</li>
            <li>Built event-driven REST APIs for real-time speech processing; reduced false-positive triggers by <span class="hl">93.3%</span> via statistical validation and log-based rule refinement.</li>
            <li>Enhanced backend observability with structured logging, profiling, and API-level analytics dashboards for anomaly tracking.</li>
          </ul>

          <div class="sub-role">AI Interpreter — Live Translate (ASR → NMT → TTS)</div>
          <ul class="bullets">
            <li>Integrated and benchmarked full multilingual translation pipeline using <span class="hl2">WER, CER, BLEU</span>; improved translation consistency by <span class="hl">20%</span> through bottleneck analysis and defect clustering.</li>
            <li>Applied quantization-aware optimisations to reduce inference latency across 5+ language pairs.</li>
            <li>Automated dataset generation including timestamp alignment, transcript validation, and multilingual speech profiling.</li>
          </ul>

          <div class="sub-role">Vision AI Automation Suite</div>
          <ul class="bullets">
            <li>Deployed ML-based anomaly detection (Python, scikit-learn, TensorFlow) for Samsung's internal VAC AI chatbot; improved detection quality by <span class="hl">20%</span>.</li>
            <li>Built AWS ingestion pipelines (SQS, S3, Lambda) processing <span class="hl2">~2TB multimedia data/day</span>; automated ETL, labelling, and model evaluation workflows — cutting manual effort by <span class="hl">50%</span>.</li>
            <li>Improved model accuracy from <span class="hl">85% → 92%</span> via advanced feature extraction and data-centric iteration; reduced false-positive alerts by <span class="hl">30%+</span>, saving 20+ engineering hours/month.</li>
          </ul>

          <div class="sub-role">Quick Share Integration</div>
          <ul class="bullets">
            <li>Optimised Wi-Fi Direct &amp; BLE handshake procedures, reducing pairing latency by <span class="hl">18%</span>.</li>
            <li>Created Python/PyTest automation for regression, stress, and connectivity scenarios.</li>
          </ul>
        </div>

        <!-- Samsung Intern -->
        <div class="job">
          <div class="job-header">
            <div class="company">Samsung Electronics</div>
            <div class="date">Jul 2023 – Dec 2023</div>
          </div>
          <div class="role">Automation Engineer Intern &nbsp;·&nbsp; New Delhi, India</div>
          <ul class="bullets">
            <li>Engineered Python + Robot Framework automation libraries for the VD framework; improved defect detection efficiency by <span class="hl">10%</span>.</li>
            <li>Automated <span class="hl">70%</span> of regression workflows using parallel execution, saving <span class="hl">30+ hours</span> per release cycle.</li>
          </ul>
        </div>
      </div>

      <!-- PROJECTS -->
      <div class="section">
        <div class="section-label">Generative AI Projects</div>

        <div class="project">
          <div class="project-name">Audio Intelligence Agent</div>
          <ul class="project-bullets">
            <li>Built an AI agent that converts long-form audio to structured summaries and action insights using ASR + LLMs.</li>
            <li>Designed prompt workflows for summarisation and action extraction; integrated pipeline for real-world audio analytics.</li>
            <li>Stack: <span class="hl2">Whisper ASR · LangChain · OpenAI · FAISS</span></li>
          </ul>
        </div>
      </div>

    </div><!-- /main -->

    <div>

      <!-- PROFICIENCY -->
      <div class="section">
        <div class="section-label">Proficiency</div>
        <div class="metric-row">
          <div class="metric-label">ML Systems</div>
          <div class="bar-track"><div class="bar-fill" style="width:88%"></div></div>
          <div class="metric-pct">88%</div>
        </div>
        <div class="metric-row">
          <div class="metric-label">GenAI / LLMs</div>
          <div class="bar-track"><div class="bar-fill" style="width:82%"></div></div>
          <div class="metric-pct">82%</div>
        </div>
        <div class="metric-row">
          <div class="metric-label">Cloud / AWS</div>
          <div class="bar-track"><div class="bar-fill" style="width:80%"></div></div>
          <div class="metric-pct">80%</div>
        </div>
        <div class="metric-row">
          <div class="metric-label">Deep Learning</div>
          <div class="bar-track"><div class="bar-fill" style="width:78%"></div></div>
          <div class="metric-pct">78%</div>
        </div>
        <div class="metric-row">
          <div class="metric-label">Data / ETL</div>
          <div class="bar-track"><div class="bar-fill" style="width:76%"></div></div>
          <div class="metric-pct">76%</div>
        </div>
      </div>

      <!-- SKILLS -->
      <div class="section">
        <div class="section-label">Tech Stack</div>

        <div class="skills-group">
          <div class="skills-group-name">Generative AI &amp; LLMs</div>
          <div class="tags">
            <span class="tag hot">LLMs</span>
            <span class="tag hot">RAG</span>
            <span class="tag">LangChain</span>
            <span class="tag">Prompt Eng.</span>
            <span class="tag">FAISS</span>
            <span class="tag">Vector Search</span>
          </div>
        </div>

        <div class="skills-group">
          <div class="skills-group-name">Machine Learning</div>
          <div class="tags">
            <span class="tag hot">Python</span>
            <span class="tag">scikit-learn</span>
            <span class="tag">TensorFlow</span>
            <span class="tag">Classification</span>
            <span class="tag">Anomaly Det.</span>
          </div>
        </div>

        <div class="skills-group">
          <div class="skills-group-name">Deep Learning &amp; Speech</div>
          <div class="tags">
            <span class="tag">CRNN</span>
            <span class="tag">PANNs</span>
            <span class="tag">ASR Pipelines</span>
            <span class="tag">NMT / TTS</span>
          </div>
        </div>

        <div class="skills-group">
          <div class="skills-group-name">Cloud &amp; MLOps</div>
          <div class="tags">
            <span class="tag hot">AWS</span>
            <span class="tag">S3</span>
            <span class="tag">SQS</span>
            <span class="tag">Lambda</span>
            <span class="tag">EC2</span>
            <span class="tag">Athena</span>
            <span class="tag">REST APIs</span>
          </div>
        </div>

        <div class="skills-group">
          <div class="skills-group-name">Data &amp; Testing</div>
          <div class="tags">
            <span class="tag">SQL / MySQL</span>
            <span class="tag">ETL</span>
            <span class="tag">Robot Framework</span>
            <span class="tag">PyTest</span>
            <span class="tag">Selenium</span>
            <span class="tag">Git</span>
          </div>
        </div>
      </div>

      <!-- EDUCATION -->
      <div class="section">
        <div class="section-label">Education</div>
        <div class="edu-item">
          <div class="edu-school">Maharaja Surajmal<br>Institute of Technology</div>
          <div class="edu-detail">
            B.Tech – Electronics &amp; Comm. Eng.<br>
            Aug 2019 – May 2023<br>
            <span style="color:var(--accent)">CGPA 9.1 / 10 &nbsp;·&nbsp; Top 1%</span><br>
            Applied Mathematics: 90%
          </div>
        </div>
      </div>

      <!-- ACHIEVEMENTS -->
      <div class="section">
        <div class="section-label">Achievements</div>
        <div class="cert-item">
          <div class="cert-dot green"></div>
          <div>Spot Award Winner — Vision AI Companion Suite</div>
        </div>
        <div class="cert-item">
          <div class="cert-dot green"></div>
          <div>Samsung Internal ML Certification — Top Tier</div>
        </div>
        <div class="cert-item">
          <div class="cert-dot green"></div>
          <div>Level-3 Certified: Gen-AI Tool Development at Samsung</div>
        </div>
        <div class="cert-item">
          <div class="cert-dot green"></div>
          <div>Consecutive 2-year "Exceeds Most" annual rating</div>
        </div>
      </div>

      <!-- CERTIFICATIONS -->
      <div class="section">
        <div class="section-label">Certifications</div>
        <div class="cert-item">
          <div class="cert-dot"></div>
          <div>Python DSA — Udemy (2025)</div>
        </div>
        <div class="cert-item">
          <div class="cert-dot"></div>
          <div>Prompt Engineering Bootcamp — Udemy (2025)</div>
        </div>
        <div class="cert-item">
          <div class="cert-dot"></div>
          <div>Statistics for Data Science — Ude
