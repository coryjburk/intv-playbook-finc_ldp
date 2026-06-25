<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>User Manual — Eccles MBA Finance Leadership Interview Playbook</title>
<style>
  :root {
    --red: #CC0000;
    --red-dim: #990000;
    --gold: #c9a84c;
    --gold-dim: #9e7d35;
    --bg: #0d0f12;
    --bg2: #131619;
    --bg3: #1a1e23;
    --bg4: #212630;
    --border: #2a2f38;
    --border2: #353d49;
    --text: #e8eaed;
    --text2: #9aa5b4;
    --text3: #6b7685;
    --green: #22c55e;
    --blue: #3b82f6;
    --orange: #f59e0b;
    --radius: 10px;
    --radius-lg: 16px;
  }
  * { box-sizing: border-box; margin: 0; padding: 0; }
  html { scroll-behavior: smooth; }
  body { background: var(--bg); color: var(--text); font-family: 'Segoe UI', system-ui, sans-serif; min-height: 100vh; line-height: 1.6; }

  /* HEADER */
  #header {
    position: sticky; top: 0; z-index: 100;
    background: rgba(13,15,18,0.96); backdrop-filter: blur(12px);
    border-bottom: 1px solid var(--border);
    padding: 0 24px; height: 58px;
    display: flex; align-items: center; justify-content: space-between;
  }
  .header-left { display: flex; align-items: center; gap: 14px; }
  .header-logo { font-size: 13px; font-weight: 700; color: var(--red); letter-spacing: 0.06em; text-transform: uppercase; }
  .header-divider { width: 1px; height: 20px; background: var(--border2); }
  .header-title { font-size: 13px; color: var(--text2); letter-spacing: 0.02em; }
  .track-pill {
    background: rgba(204,0,0,0.15); border: 1px solid rgba(204,0,0,0.4);
    color: var(--red); font-size: 11px; font-weight: 700;
    padding: 3px 10px; border-radius: 20px; letter-spacing: 0.08em; text-transform: uppercase;
  }

  /* HERO */
  #hero {
    padding: 56px 40px 44px;
    background: linear-gradient(135deg, var(--bg) 0%, var(--bg2) 50%, rgba(204,0,0,0.04) 100%);
    border-bottom: 1px solid var(--border);
    position: relative; overflow: hidden;
  }
  #hero::before {
    content: ''; position: absolute; top: -80px; right: -80px;
    width: 400px; height: 400px;
    background: radial-gradient(circle, rgba(204,0,0,0.07) 0%, transparent 70%);
    pointer-events: none;
  }
  .hero-eyebrow {
    font-size: 11px; font-weight: 700; letter-spacing: 0.12em;
    color: var(--gold); text-transform: uppercase; margin-bottom: 16px;
    display: flex; align-items: center; gap: 8px;
  }
  .hero-eyebrow::before { content: ''; display: block; width: 28px; height: 2px; background: var(--gold); }
  .hero-title { font-size: clamp(30px, 5vw, 46px); font-weight: 800; line-height: 1.1; margin-bottom: 16px; }
  .hero-title span { color: var(--red); }
  .hero-desc { font-size: 15px; color: var(--text2); max-width: 720px; line-height: 1.65; }

  /* LAYOUT */
  #app { display: flex; align-items: flex-start; }
  #toc {
    width: 248px; min-width: 248px;
    background: var(--bg2); border-right: 1px solid var(--border);
    padding: 24px 0; position: sticky; top: 58px;
    height: calc(100vh - 58px); overflow-y: auto;
  }
  .toc-label {
    font-size: 10px; font-weight: 700; letter-spacing: 0.1em;
    color: var(--text3); text-transform: uppercase; padding: 8px 22px 6px;
  }
  .toc-link {
    display: block; padding: 8px 22px; cursor: pointer;
    font-size: 13px; color: var(--text2); text-decoration: none;
    border-left: 2px solid transparent; transition: all 0.15s;
  }
  .toc-link:hover { background: var(--bg3); color: var(--text); }
  .toc-link.active { background: rgba(204,0,0,0.08); color: var(--red); border-left-color: var(--red); }
  #content { flex: 1; padding: 40px 48px 100px; max-width: 880px; }

  /* SECTIONS */
  .doc-section { margin-bottom: 52px; scroll-margin-top: 74px; }
  .doc-section h2 {
    font-size: 24px; font-weight: 800; margin-bottom: 8px;
    display: flex; align-items: center; gap: 12px;
  }
  .doc-section h2 .sec-icon { font-size: 22px; }
  .doc-section h2 .sec-num {
    font-size: 13px; font-weight: 700; color: var(--gold);
    background: rgba(201,168,76,0.1); border: 1px solid rgba(201,168,76,0.25);
    width: 30px; height: 30px; border-radius: 8px;
    display: inline-flex; align-items: center; justify-content: center;
  }
  .doc-section > .lead { font-size: 15px; color: var(--text2); margin: 4px 0 22px; line-height: 1.7; }
  .doc-section h3 {
    font-size: 16px; font-weight: 700; color: var(--text);
    margin: 26px 0 10px; padding-top: 4px;
  }
  .doc-section p { font-size: 14px; color: var(--text2); margin-bottom: 14px; }
  .doc-section strong { color: var(--text); font-weight: 600; }
  .doc-section em { color: var(--gold); font-style: normal; font-weight: 600; }
  .doc-section a { color: var(--red); text-decoration: none; }
  .doc-section a:hover { text-decoration: underline; }
  .doc-section ul, .doc-section ol { margin: 0 0 16px 0; padding-left: 0; list-style: none; }
  .doc-section li {
    font-size: 14px; color: var(--text2); line-height: 1.65;
    padding: 7px 0 7px 26px; position: relative;
  }
  .doc-section ul li::before {
    content: '▶'; position: absolute; left: 4px; top: 8px;
    color: var(--red); font-size: 9px;
  }
  .doc-section ol { counter-reset: step; }
  .doc-section ol li { counter-increment: step; padding-left: 38px; }
  .doc-section ol li::before {
    content: counter(step); position: absolute; left: 0; top: 6px;
    background: rgba(204,0,0,0.15); color: var(--red);
    width: 22px; height: 22px; border-radius: 50%;
    font-size: 11px; font-weight: 700;
    display: flex; align-items: center; justify-content: center;
  }

  .card {
    background: var(--bg2); border: 1px solid var(--border);
    border-radius: var(--radius-lg); padding: 22px 24px; margin-bottom: 18px;
  }
  .card h3 { margin-top: 0; }

  .callout {
    border-radius: var(--radius); padding: 16px 18px; margin: 18px 0;
    font-size: 13.5px; line-height: 1.65; color: var(--text2);
    display: flex; gap: 12px; align-items: flex-start;
  }
  .callout .ic { font-size: 18px; flex-shrink: 0; line-height: 1.4; }
  .callout-gold { background: rgba(201,168,76,0.06); border: 1px solid rgba(201,168,76,0.25); }
  .callout-gold strong { color: var(--gold); }
  .callout-red { background: rgba(204,0,0,0.06); border: 1px solid rgba(204,0,0,0.25); }
  .callout-red strong { color: #ff6b6b; }
  .callout-blue { background: rgba(59,130,246,0.06); border: 1px solid rgba(59,130,246,0.25); }
  .callout-blue strong { color: var(--blue); }

  .pill {
    display: inline-block; font-size: 11px; font-weight: 700;
    padding: 2px 9px; border-radius: 12px; letter-spacing: 0.03em;
    text-transform: uppercase; margin: 0 2px;
  }
  .pill-found { background: rgba(34,197,94,0.1); color: var(--green); border: 1px solid rgba(34,197,94,0.25); }
  .pill-core { background: rgba(59,130,246,0.1); color: var(--blue); border: 1px solid rgba(59,130,246,0.25); }
  .pill-adv { background: rgba(204,0,0,0.1); color: #ff6b6b; border: 1px solid rgba(204,0,0,0.3); }

  /* TIER TABLE */
  table.tier { width: 100%; border-collapse: collapse; margin: 16px 0 20px; }
  table.tier th, table.tier td {
    text-align: left; padding: 11px 14px; font-size: 13px;
    border-bottom: 1px solid var(--border);
  }
  table.tier th { color: var(--text3); text-transform: uppercase; font-size: 10.5px; letter-spacing: 0.06em; font-weight: 700; }
  table.tier td { color: var(--text2); }
  .tier-dot { display: inline-block; width: 10px; height: 10px; border-radius: 50%; margin-right: 8px; vertical-align: middle; }
  .tier-name { font-weight: 700; color: var(--text); }

  /* STEP FLOW */
  .flow { display: flex; flex-direction: column; gap: 0; margin: 18px 0; }
  .flow-step { display: flex; gap: 16px; padding: 14px 0; border-bottom: 1px solid var(--border); }
  .flow-step:last-child { border-bottom: none; }
  .flow-badge {
    flex-shrink: 0; width: 34px; height: 34px; border-radius: 9px;
    display: flex; align-items: center; justify-content: center; font-size: 16px;
    background: rgba(204,0,0,0.12); border: 1px solid rgba(204,0,0,0.3);
  }
  .flow-body h4 { font-size: 14px; color: var(--text); font-weight: 700; margin-bottom: 3px; }
  .flow-body p { font-size: 13px; color: var(--text2); margin: 0; }

  /* FAQ */
  .faq-item { border-bottom: 1px solid var(--border); padding: 16px 0; }
  .faq-item:last-child { border-bottom: none; }
  .faq-q { font-size: 14px; font-weight: 700; color: var(--text); margin-bottom: 6px; }
  .faq-a { font-size: 13.5px; color: var(--text2); line-height: 1.65; }

  .footer {
    border-top: 1px solid var(--border); margin-top: 40px; padding-top: 22px;
    font-size: 12px; color: var(--text3);
  }
  code {
    background: var(--bg3); border: 1px solid var(--border); border-radius: 5px;
    padding: 1px 6px; font-size: 12.5px; color: var(--gold); font-family: 'Consolas', monospace;
  }

  ::-webkit-scrollbar { width: 6px; }
  ::-webkit-scrollbar-track { background: var(--bg); }
  ::-webkit-scrollbar-thumb { background: var(--border2); border-radius: 3px; }

  @media (max-width: 820px) {
    #toc { display: none; }
    #content { padding: 28px 22px 80px; }
    #hero { padding: 36px 22px 28px; }
  }
</style>
</head>
<body>

<div id="header">
  <div class="header-left">
    <span class="header-logo">Eccles MBA</span>
    <div class="header-divider"></div>
    <span class="header-title">Finance Leadership Interview Playbook</span>
    <span class="track-pill">User Manual</span>
  </div>
</div>

<div id="hero">
  <div class="hero-eyebrow">Finance Leadership · LDP Interview Preparation</div>
  <div class="hero-title">Playbook <span>User Manual</span></div>
  <div class="hero-desc">Everything you need to get the most out of the Finance Leadership Interview Playbook — how the question bank, frameworks, battlecard, and red flags are organized, how to run a full practice rep with AI coaching, and how the Readiness dashboard tracks your progress by category over time.</div>
</div>

<div id="app">
  <nav id="toc">
    <div class="toc-label">Contents</div>
    <a class="toc-link active" href="#overview">1 · Getting Started</a>
    <a class="toc-link" href="#question-bank">2 · The Question Bank</a>
    <a class="toc-link" href="#frameworks">3 · Frameworks</a>
    <a class="toc-link" href="#battlecard">4 · Battlecard</a>
    <a class="toc-link" href="#redflags">5 · Red Flags</a>
    <a class="toc-link" href="#practice">6 · Practice Mode &amp; AI Coach</a>
    <a class="toc-link" href="#readiness">7 · Tracking Your Readiness</a>
    <a class="toc-link" href="#deploy">8 · Deploying &amp; Sharing</a>
    <a class="toc-link" href="#faq">9 · FAQ</a>
  </nav>

  <main id="content">

    <!-- 1 -->
    <section class="doc-section" id="overview">
      <h2><span class="sec-num">1</span> Getting Started</h2>
      <p class="lead">The Finance Leadership Interview Playbook is a self-contained preparation tool for MBA students recruiting into Finance Leadership Development Programs (LDPs) and rotational programs at companies like Amazon, GE, AT&amp;T, Boeing, Honeywell, and Johnson &amp; Johnson.</p>

      <p>Everything lives in a single file. There's nothing to install and no account to create — open the playbook in any modern browser (Chrome or Edge recommended for the voice features) and you're ready to study.</p>

      <h3>What's inside</h3>
      <ul>
        <li><strong>100 interview questions</strong> across 8 finance categories, each with a conversational model answer, a technical deep dive, a coaching note, and a recruiter red flag.</li>
        <li><strong>10 core frameworks</strong> — the structured analytical approaches every LDP candidate should know cold.</li>
        <li><strong>A battlecard</strong> — quick-reference concepts, power phrases, and metrics to review right before an interview.</li>
        <li><strong>A red-flags guide</strong> — the specific answers and behaviors that eliminate candidates.</li>
        <li><strong>Practice Mode</strong> — record or type an answer and get structured AI coaching feedback.</li>
        <li><strong>A Readiness dashboard</strong> — tracks your coaching scores by category so you can see where you're interview-ready and where you need more reps.</li>
      </ul>

      <h3>Finding your way around</h3>
      <p>Use the tabs in the top navigation bar — <strong>Question Bank</strong>, <strong>Frameworks</strong>, <strong>Battlecard</strong>, <strong>Red Flags</strong>, and <strong>Readiness</strong> — to move between the main areas. The left sidebar mirrors that navigation and adds quick jumps to each question category.</p>

      <div class="callout callout-gold">
        <span class="ic">💡</span>
        <div>Behavioral and introduction coaching is handled directly by your Eccles career coaches. This playbook deliberately goes deep on the <strong>technical</strong> side — modeling, valuation, capital allocation, treasury, and the like — where self-service practice adds the most value.</div>
      </div>
    </section>

    <!-- 2 -->
    <section class="doc-section" id="question-bank">
      <h2><span class="sec-num">2</span> The Question Bank</h2>
      <p class="lead">The heart of the playbook: 100 questions you can filter, expand, and practice. This is where you'll spend most of your time.</p>

      <h3>The eight categories</h3>
      <ul>
        <li><strong>Financial Modeling &amp; Valuation</strong> — DCF, three-statement linkages, LBO, comparables, accretion/dilution.</li>
        <li><strong>FP&amp;A &amp; Budgeting</strong> — annual planning, zero-based budgeting, rolling forecasts, variance analysis.</li>
        <li><strong>Capital Allocation</strong> — ROIC vs. WACC, EVA, M&amp;A vs. organic, dividends and buybacks.</li>
        <li><strong>Risk Management</strong> — FX and interest-rate hedging, VaR, internal controls, credit risk.</li>
        <li><strong>Treasury &amp; Cash Management</strong> — liquidity, revolvers, commercial paper, the 13-week cash forecast.</li>
        <li><strong>Accounting &amp; Reporting</strong> — ASC 606, leases, purchase accounting, pensions, earnings quality.</li>
        <li><strong>Strategic Finance</strong> — business partnering, market entry, divestitures, competitive moats.</li>
        <li><strong>Behavioral &amp; Career</strong> — LDP motivation, leadership without authority, "why Eccles."</li>
      </ul>

      <h3>Difficulty levels</h3>
      <p>Every question is tagged so you can calibrate your prep:</p>
      <p>
        <span class="pill pill-found">Foundational</span> core concepts you must have cold &nbsp;·&nbsp;
        <span class="pill pill-core">Core</span> the bread-and-butter of most interviews &nbsp;·&nbsp;
        <span class="pill pill-adv">Advanced</span> final-round and differentiator material
      </p>

      <h3>Filtering</h3>
      <p>Use the <strong>Category</strong> and <strong>Level</strong> filter rows at the top of the Question Bank to narrow the list. The two filters work together — for example, <em>Capital Allocation</em> + <em>Advanced</em> shows only the hardest capital-allocation questions. The count on the right tells you how many questions match. You can also jump straight to a category from the left sidebar.</p>

      <h3>The four answer layers</h3>
      <p>Click any question to expand it. Inside, four tabs give you progressively deeper material:</p>
      <div class="flow">
        <div class="flow-step"><div class="flow-badge">💬</div><div class="flow-body"><h4>Conversational</h4><p>What a strong candidate actually sounds like saying this out loud — your model for a clean, confident spoken answer.</p></div></div>
        <div class="flow-step"><div class="flow-badge">🔬</div><div class="flow-body"><h4>Deep Dive</h4><p>The technical depth behind the answer — formulas, business context, metrics, and the advanced nuances that separate top candidates.</p></div></div>
        <div class="flow-step"><div class="flow-badge">🎯</div><div class="flow-body"><h4>Coaching</h4><p>How to deliver it well — what to emphasize, what to practice, and the credibility signals interviewers look for.</p></div></div>
        <div class="flow-step"><div class="flow-badge">🚩</div><div class="flow-body"><h4>Red Flag</h4><p>The specific mistake on this question that would weaken or eliminate you — so you know exactly what to avoid.</p></div></div>
      </div>
    </section>

    <!-- 3 -->
    <section class="doc-section" id="frameworks">
      <h2><span class="sec-num">3</span> Frameworks</h2>
      <p class="lead">Ten structured analytical approaches — DCF, zero-based budgeting, scenario analysis, EVA, the capital allocation framework, OKRs for finance, working capital optimization, the risk assessment matrix, the finance business partner model, and rolling forecasts.</p>
      <p>Each framework card gives you a short description, a numbered step-by-step process, and a <em>"use when"</em> note telling you exactly which interview situations it applies to. Treat these as the scaffolding for your answers: when an interviewer asks an open-ended technical question, reaching for the right framework is what makes your response sound structured and senior rather than improvised.</p>
      <div class="callout callout-blue">
        <span class="ic">🧮</span>
        <div>A good habit: when you study a question in the bank, note which framework it draws on, then flip to the Frameworks tab to rehearse the full process. The two reinforce each other.</div>
      </div>
    </section>

    <!-- 4 -->
    <section class="doc-section" id="battlecard">
      <h2><span class="sec-num">4</span> Battlecard</h2>
      <p class="lead">Your pre-interview cheat sheet — eight quick-reference sections built for the final review the night before, or even in the parking lot.</p>
      <p>The battlecard covers must-know concepts, technical power phrases you can drop into answers, metrics to know cold, capital allocation principles, the most common LDP interview mistakes, strong-candidate signals, final-round differentiators, and a last-minute review block. It's intentionally dense and skimmable. Don't try to learn from it cold — use it to <strong>refresh</strong> material you've already practiced in the Question Bank.</p>
    </section>

    <!-- 5 -->
    <section class="doc-section" id="redflags">
      <h2><span class="sec-num">5</span> Red Flags</h2>
      <p class="lead">Ten categories of answers and behaviors that get candidates cut — from weak modeling intuition and metric confusion to shallow strategic thinking, risk blind spots, and an inability to translate finance for a non-finance audience.</p>
      <p>Read this section the way an interviewer thinks. Each card lists the specific tells that signal a candidate isn't ready. Knowing them does two things: it helps you avoid the traps yourself, and it sharpens your ear for what "good" actually sounds like. Many of these red flags map directly to the per-question Red Flag tab in the Question Bank.</p>
    </section>

    <!-- 6 -->
    <section class="doc-section" id="practice">
      <h2><span class="sec-num">6</span> Practice Mode &amp; the AI Coach</h2>
      <p class="lead">Reading model answers builds knowledge. Practicing out loud builds readiness. Practice Mode is where you turn one into the other.</p>

      <h3>Starting a rep</h3>
      <p>Open any question, stay on the <strong>Conversational</strong> tab, and click <strong>🎙️ Practice This Question</strong>. A focused practice window opens with the question front and center.</p>

      <h3>Recording or typing your answer</h3>
      <div class="flow">
        <div class="flow-step"><div class="flow-badge">🎤</div><div class="flow-body"><h4>Voice</h4><p>Click <strong>Start Recording</strong> and answer out loud. Your words are transcribed live, and the tool counts filler words ("um," "uh," "like," "basically," and so on) so you can hear your own verbal habits. Voice capture works best in Chrome or Edge.</p></div></div>
        <div class="flow-step"><div class="flow-badge">⌨️</div><div class="flow-body"><h4>Type</h4><p>Prefer to write? Type or paste your answer into the text box instead. Either input works for AI coaching.</p></div></div>
      </div>

      <h3>Getting AI coaching feedback</h3>
      <p>Click <strong>Get AI Coaching Feedback</strong>. The coach evaluates your answer against the model answer for that question and returns structured, specific feedback in this format:</p>
      <ul>
        <li><strong>Readiness</strong> — a one-line verdict (Not Yet · Approaching · Interview-Ready · Standout) with the single biggest reason why.</li>
        <li><strong>What Landed</strong> — the specific strengths in your answer.</li>
        <li><strong>Highest-Leverage Fixes</strong> — the two most important gaps, each with a phrase you could actually say.</li>
        <li><strong>Say It Like This</strong> — your weakest moment, rewritten into stronger, interview-ready phrasing you can rehearse.</li>
        <li><strong>Standout Move</strong> — one advanced insight that would lift you into the top tier.</li>
        <li><strong>Delivery Note</strong> — appears only when filler words were detected, with a tactic to tighten up.</li>
      </ul>
      <p>The coach adapts its lens to the question: <strong>technical</strong> questions are judged on accuracy, precision, depth, and business connection; <strong>behavioral</strong> questions on structure, specificity, quantified impact, and leadership signal. It also calibrates to the question's difficulty — more demanding on Advanced, rewarding fundamentals on Foundational.</p>

      <div class="callout callout-gold">
        <span class="ic">🔌</span>
        <div>Depending on where you're running the playbook, AI coaching arrives one of two ways. When a live connection is available, the feedback appears right in the window. On a static deployment (like GitHub Pages), the tool hands you a ready-to-paste prompt to drop into Claude instead. Both give you the same structured coaching — see the next section for how each one logs your score.</div>
      </div>
    </section>

    <!-- 7 -->
    <section class="doc-section" id="readiness">
      <h2><span class="sec-num">7</span> Tracking Your Readiness</h2>
      <p class="lead">The Readiness dashboard turns individual practice reps into a picture of where you stand. Every time you get coaching feedback, its readiness score is logged to that question's category — so over time you can see which finance areas are interview-ready and which still need work.</p>

      <h3>How scoring works</h3>
      <p>With every piece of coaching feedback, the AI coach assigns a <strong>0–100 readiness score</strong> that matches the readiness tier it gave you. That score is recorded against the <strong>category</strong> of the question you practiced. The dashboard then shows your running average per category, plus an overall readiness number.</p>

      <table class="tier">
        <thead><tr><th>Score</th><th>Tier</th><th>What it means</th></tr></thead>
        <tbody>
          <tr><td>85–100</td><td><span class="tier-dot" style="background:#22c55e"></span><span class="tier-name">Standout</span></td><td>Top-decile answer; ready to differentiate in final rounds.</td></tr>
          <tr><td>70–84</td><td><span class="tier-dot" style="background:#c9a84c"></span><span class="tier-name">Interview-Ready</span></td><td>Solid and reliable; you can hold your own on this material.</td></tr>
          <tr><td>50–69</td><td><span class="tier-dot" style="background:#f59e0b"></span><span class="tier-name">Approaching</span></td><td>The foundation is there; targeted reps will get you over the line.</td></tr>
          <tr><td>0–49</td><td><span class="tier-dot" style="background:#ff6b6b"></span><span class="tier-name">Not Yet</span></td><td>Needs focused study before this category is interview-safe.</td></tr>
        </tbody>
      </table>

      <h3>Two ways your scores get logged</h3>
      <p>The dashboard fills in through a <strong>hybrid</strong> approach, so it works the same whether or not you have a live AI connection:</p>
      <div class="flow">
        <div class="flow-step"><div class="flow-badge">⚡</div><div class="flow-body"><h4>Automatic (live coaching)</h4><p>When live AI coaching is available, your score logs itself the moment feedback appears. You'll see a green <strong>"✓ Logged NN/100 to [category]"</strong> confirmation under the feedback. Nothing else to do.</p></div></div>
        <div class="flow-step"><div class="flow-badge">📋</div><div class="flow-body"><h4>Paste-back (copy-the-prompt path)</h4><p>When you use the copy-the-prompt path, copy the coach's full reply from Claude, paste it into the <strong>Track your progress</strong> box in the practice window, and tap <strong>Log Score</strong>. The tool reads the score and records it to the category you just practiced.</p></div></div>
      </div>

      <h3>Reading the dashboard</h3>
      <p>Open the <strong>Readiness</strong> tab to see:</p>
      <ul>
        <li><strong>Overall Readiness</strong> — your average across every logged attempt, with its tier color.</li>
        <li><strong>Practice Attempts Logged</strong> — how many reps you've recorded.</li>
        <li><strong>Categories Practiced</strong> — how many of the eight categories you've touched (e.g., 3/8).</li>
        <li><strong>Readiness by Category</strong> — a bar for each category showing its average score, tier color, and rep count. Categories you haven't practiced yet read <em>"no reps yet"</em> so your coverage gaps are obvious at a glance.</li>
      </ul>

      <div class="callout callout-red">
        <span class="ic">⚠️</span>
        <div><strong>One thing to know about auto-logging:</strong> the score travels at the very end of the coach's reply. On rare occasions when a reply runs especially long, that final line can get cut off — in which case your feedback still displays normally, it just won't log automatically. If you ever notice the green confirmation didn't appear, simply copy the coach's reply into the <strong>paste-back box</strong> and tap <strong>Log Score</strong>. That always works.</div>
      </div>

      <h3>Persistence &amp; reset</h3>
      <p>Your progress is saved locally in your browser, so it's there when you come back. A few practical notes: it's tied to the specific browser and device you use, so switching machines or clearing your browser data starts you fresh, and private/incognito windows won't retain progress between sessions. When you want a clean slate, use <strong>↺ Reset all progress</strong> at the bottom of the dashboard.</p>

      <div class="callout callout-gold">
        <span class="ic">📈</span>
        <div>Aim for breadth before depth: get at least one rep in every category to light up all eight bars, then circle back to push your <em>Not Yet</em> and <em>Approaching</em> categories toward Interview-Ready. The dashboard makes that triage easy.</div>
      </div>
    </section>

    <!-- 8 -->
    <section class="doc-section" id="deploy">
      <h2><span class="sec-num">8</span> Deploying &amp; Sharing</h2>
      <p class="lead">The playbook is one self-contained HTML file, which makes it easy to share and host.</p>
      <h3>Ways to use it</h3>
      <ul>
        <li><strong>Open locally</strong> — double-click the file to open it in your browser. Great for personal practice.</li>
        <li><strong>GitHub Pages</strong> — the most reliable way to give students a permanent link. Host the file in a repo and share the published URL.</li>
        <li><strong>Share the file directly</strong> — email or post it; recipients just open it in a browser.</li>
      </ul>
      <h3>A note on AI coaching by environment</h3>
      <p>On a plain static host like GitHub Pages, the browser can't reach the AI directly, so the coach uses the <strong>copy-the-prompt</strong> path — students paste the prompt into Claude and then paste the reply back to log their score. If you'd like coaching to run automatically in the window on a hosted deployment, that requires a small serverless proxy to keep the API key off the page (the same approach used on the PM playbook). Either way, the playbook stays fully functional and the Readiness dashboard works through the paste-back path.</p>
    </section>

    <!-- 9 -->
    <section class="doc-section" id="faq">
      <h2><span class="sec-num">9</span> FAQ</h2>
      <div class="faq-item">
        <div class="faq-q">The voice recording isn't working — what do I do?</div>
        <div class="faq-a">Voice capture relies on your browser's speech recognition, which works most reliably in Chrome and Edge. If it's unavailable, you can always type your answer into the text box instead — AI coaching works the same way.</div>
      </div>
      <div class="faq-item">
        <div class="faq-q">My Readiness dashboard is empty even though I practiced.</div>
        <div class="faq-a">A score only logs once coaching feedback is recorded. On the live path, look for the green "✓ Logged" confirmation. On the copy-the-prompt path, make sure you pasted the coach's full reply into the paste-back box and tapped Log Score. If a long reply didn't auto-log, the paste-back box will capture it.</div>
      </div>
      <div class="faq-item">
        <div class="faq-q">Why did a score not log automatically that one time?</div>
        <div class="faq-a">The score sits on the last line of the coach's reply. Very long replies can occasionally get truncated before that line. Your feedback still shows; just paste the reply into the paste-back box to log it.</div>
      </div>
      <div class="faq-item">
        <div class="faq-q">Will my progress follow me to another computer?</div>
        <div class="faq-a">No — progress is stored in the browser you're using. Switching devices or browsers, or clearing browsing data, starts a fresh dashboard. Use the same browser to keep building your history.</div>
      </div>
      <div class="faq-item">
        <div class="faq-q">Can I reset my scores and start over?</div>
        <div class="faq-a">Yes. The ↺ Reset all progress button at the bottom of the Readiness tab clears every logged score. It can't be undone, so the tool asks you to confirm first.</div>
      </div>
      <div class="faq-item">
        <div class="faq-q">Should I use this for behavioral interview prep?</div>
        <div class="faq-a">There's a Behavioral &amp; Career category for completeness, and the coach can evaluate those answers. But your Eccles coaches lead behavioral and introduction prep directly — lean on them for that and use the playbook to go deep on the technical material.</div>
      </div>
      <div class="footer">
        Eccles MBA — Finance Leadership Interview Playbook · User Manual · University of Utah David Eccles School of Business
      </div>
    </section>

  </main>
</div>

<script>
// Lightweight scrollspy to highlight the active section in the contents list
(function () {
  const links = Array.from(document.querySelectorAll('.toc-link'));
  const sections = links
    .map(l => document.getElementById(l.getAttribute('href').slice(1)))
    .filter(Boolean);

  function onScroll() {
    const offset = 90;
    let current = sections[0];
    for (const sec of sections) {
      if (sec.getBoundingClientRect().top - offset <= 0) current = sec;
    }
    links.forEach(l => l.classList.toggle('active', l.getAttribute('href') === '#' + current.id));
  }
  window.addEventListener('scroll', onScroll, { passive: true });
  links.forEach(l => l.addEventListener('click', () => {
    links.forEach(x => x.classList.remove('active'));
    l.classList.add('active');
  }));
  onScroll();
})();
</script>
</body>
</html>
