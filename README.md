[index.html.html](https://github.com/user-attachments/files/25578918/index.html.html)
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>PsychoWrite Pro — AI Content Engine</title>
<link href="https://fonts.googleapis.com/css2?family=Syne:wght@400;600;700;800&family=DM+Sans:ital,opsz,wght@0,9..40,300;0,9..40,400;0,9..40,500;1,9..40,300&display=swap" rel="stylesheet">
<style>
:root{--bg:#080810;--surface:#11111c;--surface2:#191926;--surface3:#22223a;--border:#252538;--border2:#32324f;--accent:#7c5cfc;--accent2:#fc5c9c;--accent3:#5cfcb8;--accent4:#fcb85c;--text:#e4e4f0;--muted:#5a5a7a;--muted2:#8888aa;--glow:rgba(124,92,252,0.18)}
*{box-sizing:border-box;margin:0;padding:0}html{scroll-behavior:smooth}
body{background:var(--bg);color:var(--text);font-family:'DM Sans',sans-serif;min-height:100vh;overflow-x:hidden}
body::before{content:'';position:fixed;inset:0;background:radial-gradient(ellipse 70% 50% at 15% 10%,rgba(124,92,252,0.07) 0%,transparent 60%),radial-gradient(ellipse 60% 50% at 85% 90%,rgba(252,92,156,0.05) 0%,transparent 60%);pointer-events:none;z-index:0}
.wrap{max-width:960px;margin:0 auto;padding:0 24px;position:relative;z-index:1}
header{padding:36px 0 28px;border-bottom:1px solid var(--border);margin-bottom:36px;display:flex;align-items:flex-end;justify-content:space-between}
.logo{font-family:'Syne',sans-serif;font-size:26px;font-weight:800;letter-spacing:-0.5px}
.logo .p1{color:var(--accent)}.logo .p2{color:var(--accent2)}.logo .p3{color:var(--accent3)}
.tagline{font-size:11px;color:var(--muted);margin-top:3px;letter-spacing:1.5px;text-transform:uppercase}
.vbadge{padding:4px 12px;background:rgba(124,92,252,0.12);border:1px solid rgba(124,92,252,0.3);border-radius:100px;font-size:11px;color:var(--accent);font-weight:600}
.step-header{display:flex;align-items:center;gap:10px;margin-bottom:14px}
.step-num{width:24px;height:24px;border-radius:50%;background:linear-gradient(135deg,var(--accent),var(--accent2));display:flex;align-items:center;justify-content:center;font-family:'Syne',sans-serif;font-size:11px;font-weight:800;color:white;flex-shrink:0}
.step-title{font-family:'Syne',sans-serif;font-size:12px;font-weight:700;letter-spacing:1.5px;text-transform:uppercase;color:var(--accent)}
.step-sub{font-size:11px;color:var(--muted);margin-left:auto;font-style:italic}
.form-block{margin-bottom:30px}
.cat-tabs{display:flex;gap:6px;flex-wrap:wrap;margin-bottom:14px}
.cat-tab{padding:6px 14px;border-radius:8px;border:1px solid var(--border);background:var(--surface);color:var(--muted2);font-size:12px;font-weight:600;cursor:pointer;transition:all .15s;font-family:'Syne',sans-serif}
.cat-tab:hover{border-color:var(--border2);color:var(--text)}
.cat-tab.active{background:var(--surface3);border-color:var(--accent);color:var(--accent)}
.ct-grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(148px,1fr));gap:8px}
.ct-card{background:var(--surface);border:1px solid var(--border);border-radius:10px;padding:11px 14px;cursor:pointer;transition:all .15s;user-select:none}
.ct-card:hover{border-color:var(--border2);background:var(--surface2)}
.ct-card.active{border-color:var(--accent);background:rgba(124,92,252,0.1)}
.ct-icon{font-size:16px;margin-bottom:4px}.ct-name{font-size:12px;font-weight:600;color:var(--text)}.ct-hint{font-size:10px;color:var(--muted);margin-top:2px}
.smart-box{background:linear-gradient(135deg,rgba(124,92,252,0.08),rgba(252,92,156,0.05));border:1px solid rgba(124,92,252,0.25);border-radius:12px;padding:16px 20px;margin-bottom:24px;display:none}
.smart-box.show{display:block}
.smart-box-title{font-family:'Syne',sans-serif;font-size:11px;font-weight:700;letter-spacing:1.5px;text-transform:uppercase;color:var(--accent);margin-bottom:10px}
.smart-rec{display:flex;flex-wrap:wrap;gap:8px;align-items:center}
.smart-tag{padding:5px 12px;border-radius:100px;font-size:12px;cursor:pointer;transition:all .15s;border:1px solid;font-weight:500}
.smart-tag.fw{background:rgba(252,92,156,0.1);border-color:rgba(252,92,156,0.3);color:var(--accent2)}
.smart-tag.fw:hover,.smart-tag.fw.picked{background:var(--accent2);border-color:var(--accent2);color:#fff}
.smart-tag.tr{background:rgba(92,252,184,0.1);border-color:rgba(92,252,184,0.3);color:var(--accent3)}
.smart-tag.tr:hover,.smart-tag.tr.picked{background:var(--accent3);border-color:var(--accent3);color:#080810}
.smart-lbl{font-size:11px;color:var(--muted);font-weight:600}
select,input,textarea{width:100%;background:var(--surface);border:1px solid var(--border);border-radius:10px;color:var(--text);font-family:'DM Sans',sans-serif;font-size:14px;padding:12px 16px;outline:none;transition:border-color .2s,box-shadow .2s;appearance:none;-webkit-appearance:none}
select:focus,input:focus,textarea:focus{border-color:var(--accent);box-shadow:0 0 0 3px var(--glow)}
textarea{resize:vertical;min-height:80px;line-height:1.6}
.input-row{display:grid;grid-template-columns:1fr 1fr;gap:14px;margin-bottom:24px}
.kw-suggestions{display:flex;flex-wrap:wrap;gap:6px;margin-top:8px;min-height:28px}
.kw-tag{padding:4px 12px;background:rgba(252,184,92,0.1);border:1px solid rgba(252,184,92,0.25);border-radius:100px;font-size:12px;color:var(--accent4);cursor:pointer;transition:all .15s}
.kw-tag:hover,.kw-tag.used{background:var(--accent4);border-color:var(--accent4);color:#080810;font-weight:600}
.kw-loading{font-size:11px;color:var(--muted);font-style:italic}
.chips{display:flex;flex-wrap:wrap;gap:7px}
.chip{padding:7px 15px;border-radius:100px;border:1px solid var(--border);background:var(--surface);color:var(--muted2);font-size:13px;cursor:pointer;transition:all .15s;user-select:none;font-family:'DM Sans',sans-serif}
.chip:hover{border-color:var(--border2);color:var(--text)}
.chip.active{background:var(--accent);border-color:var(--accent);color:#fff;font-weight:500}
.chip.green.active{background:var(--accent3);border-color:var(--accent3);color:#080810}
.fw-grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(168px,1fr));gap:8px}
.fw-card{background:var(--surface);border:1px solid var(--border);border-radius:10px;padding:12px 14px;cursor:pointer;transition:all .15s;user-select:none;position:relative}
.fw-card:hover{border-color:var(--border2);background:var(--surface2)}
.fw-card.active{border-color:var(--accent2);background:rgba(252,92,156,0.08)}
.fw-card.ai-rec::after{content:'✦ Best Pick';position:absolute;top:8px;right:8px;font-size:9px;font-weight:700;color:var(--accent3);letter-spacing:.5px}
.fw-name{font-family:'Syne',sans-serif;font-size:13px;font-weight:700;color:var(--text);margin-bottom:3px}
.fw-full{font-size:10px;color:var(--accent2);font-weight:600;margin-bottom:4px}
.fw-desc{font-size:11px;color:var(--muted);line-height:1.4}
.trig-cat-lbl{font-size:11px;font-weight:700;letter-spacing:1px;text-transform:uppercase;color:var(--muted2);margin-bottom:8px;padding-left:2px;display:flex;align-items:center;gap:6px}
.trig-cat-lbl::after{content:'';flex:1;height:1px;background:var(--border)}
.trig-grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(158px,1fr));gap:8px;margin-bottom:20px}
.trig-card{background:var(--surface);border:1px solid var(--border);border-radius:10px;padding:11px 14px;cursor:pointer;transition:all .15s;user-select:none;position:relative}
.trig-card:hover{border-color:var(--border2)}
.trig-card.active{border-color:var(--accent);background:rgba(124,92,252,0.1)}
.trig-icon{font-size:16px;margin-bottom:4px}.trig-name{font-size:12px;font-weight:600;color:var(--text)}.trig-desc{font-size:10px;color:var(--muted);margin-top:2px;line-height:1.3}
.trig-badge{position:absolute;top:7px;right:7px;font-size:9px;font-weight:700;padding:2px 6px;border-radius:100px}
.bs{background:rgba(252,92,156,0.2);color:var(--accent2)}.bt{background:rgba(92,252,184,0.2);color:var(--accent3)}.be{background:rgba(124,92,252,0.2);color:var(--accent)}.bu{background:rgba(252,184,92,0.2);color:var(--accent4)}
.auto-btn{padding:8px 16px;background:rgba(124,92,252,0.1);border:1px dashed rgba(124,92,252,0.4);border-radius:8px;color:var(--accent);font-size:12px;cursor:pointer;transition:all .15s;font-family:'DM Sans',sans-serif;font-weight:500}
.auto-btn:hover{background:rgba(124,92,252,0.2)}
.wc-section{background:var(--surface);border:1px solid var(--border);border-radius:12px;padding:18px 20px;margin-bottom:24px}
.wc-row{display:flex;align-items:center;gap:10px;flex-wrap:wrap;margin-top:10px}
.wc-lbl{font-size:13px;color:var(--muted2);white-space:nowrap}
.wc-presets{display:flex;gap:6px;flex-wrap:wrap}
.wc-btn{padding:6px 12px;border-radius:8px;border:1px solid var(--border);background:var(--surface2);color:var(--muted2);font-size:12px;cursor:pointer;transition:all .15s;font-weight:500}
.wc-btn:hover{border-color:var(--accent4);color:var(--accent4)}
.wc-btn.active{background:rgba(252,184,92,0.12);border-color:var(--accent4);color:var(--accent4)}
.wc-custom{width:90px!important;padding:6px 10px!important;font-size:13px;text-align:center}
.wc-unit{font-size:12px;color:var(--muted)}
.outline-row{display:flex;align-items:center;gap:10px;margin-bottom:12px}
.toggle-sw{position:relative;width:40px;height:22px;cursor:pointer;flex-shrink:0}
.toggle-sw input{opacity:0;width:0;height:0;position:absolute}
.toggle-track{position:absolute;inset:0;background:var(--surface3);border-radius:100px;border:1px solid var(--border2);transition:.2s}
.toggle-sw input:checked+.toggle-track{background:var(--accent);border-color:var(--accent)}
.toggle-thumb{position:absolute;top:3px;left:3px;width:14px;height:14px;border-radius:50%;background:white;transition:.2s;pointer-events:none}
.toggle-sw input:checked~.toggle-thumb{transform:translateX(18px)}
.toggle-lbl{font-size:13px;color:var(--text)}
.outline-opts{display:none;background:var(--surface);border:1px solid var(--border);border-radius:10px;padding:16px;margin-top:10px}
.outline-opts.show{display:block}
.outline-grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(130px,1fr));gap:8px;margin-top:10px}
.o-chip{padding:7px 12px;border-radius:8px;border:1px solid var(--border);background:var(--surface2);color:var(--muted2);font-size:12px;cursor:pointer;transition:all .15s;text-align:center}
.o-chip:hover{border-color:var(--accent);color:var(--text)}
.o-chip.active{background:rgba(124,92,252,0.12);border-color:var(--accent);color:var(--accent);font-weight:600}
.divider{border:none;border-top:1px solid var(--border);margin:28px 0}
.btn-gen{width:100%;padding:18px;background:linear-gradient(135deg,var(--accent) 0%,#9c5cfc 50%,var(--accent2) 100%);border:none;border-radius:12px;color:white;font-family:'Syne',sans-serif;font-size:15px;font-weight:700;letter-spacing:.8px;cursor:pointer;transition:all .2s;position:relative;overflow:hidden}
.btn-gen:hover{transform:translateY(-2px);box-shadow:0 10px 40px rgba(124,92,252,.35)}
.btn-gen:active{transform:translateY(0)}
.btn-gen:disabled{opacity:.55;cursor:not-allowed;transform:none;box-shadow:none}
.btn-inner{position:relative;z-index:1;display:flex;align-items:center;justify-content:center;gap:8px}
.shimmer{position:absolute;inset:0;background:linear-gradient(90deg,transparent 0%,rgba(255,255,255,.12) 50%,transparent 100%);transform:translateX(-100%)}
.btn-gen:hover .shimmer{animation:shimmer .7s ease}
@keyframes shimmer{to{transform:translateX(100%)}}
.out-section{margin-top:36px;display:none}
.out-section.visible{display:block}
.out-header{display:flex;justify-content:space-between;align-items:center;margin-bottom:14px}
.out-title{font-family:'Syne',sans-serif;font-size:20px;font-weight:800}
.out-actions{display:flex;gap:8px}
.btn-act{padding:8px 16px;background:var(--surface2);border:1px solid var(--border);border-radius:8px;color:var(--muted2);font-size:12px;cursor:pointer;transition:all .15s;font-family:'DM Sans',sans-serif;font-weight:500}
.btn-act:hover{border-color:var(--accent3);color:var(--accent3)}
.meta-tags{display:flex;gap:6px;flex-wrap:wrap;margin-bottom:14px}
.mt{padding:4px 11px;border-radius:100px;font-size:10px;font-weight:700;letter-spacing:.8px;text-transform:uppercase}
.mt-p{background:rgba(124,92,252,.12);color:var(--accent);border:1px solid rgba(124,92,252,.25)}
.mt-k{background:rgba(252,92,156,.12);color:var(--accent2);border:1px solid rgba(252,92,156,.25)}
.mt-g{background:rgba(92,252,184,.12);color:var(--accent3);border:1px solid rgba(92,252,184,.25)}
.mt-y{background:rgba(252,184,92,.12);color:var(--accent4);border:1px solid rgba(252,184,92,.25)}
.out-box{background:var(--surface);border:1px solid var(--border);border-radius:14px;padding:28px;font-size:14.5px;line-height:1.85;white-space:pre-wrap;min-height:200px}
.out-box.loading{display:flex;align-items:center;justify-content:center;min-height:160px;color:var(--muted)}
.dots span{display:inline-block;width:8px;height:8px;border-radius:50%;background:var(--accent);margin:0 3px;animation:bounce 1.2s infinite}
.dots span:nth-child(2){animation-delay:.2s;background:var(--accent2)}
.dots span:nth-child(3){animation-delay:.4s;background:var(--accent3)}
@keyframes bounce{0%,60%,100%{transform:translateY(0)}30%{transform:translateY(-10px)}}
.char-info{font-size:11px;color:var(--muted);margin-top:8px;text-align:right}
.regen-row{display:flex;gap:8px;margin-top:12px;flex-wrap:wrap}
.btn-regen{flex:1;min-width:130px;padding:11px 12px;background:var(--surface);border:1px solid var(--border);border-radius:9px;color:var(--muted2);font-size:12px;cursor:pointer;transition:all .15s;font-family:'DM Sans',sans-serif}
.btn-regen:hover{border-color:var(--accent);color:var(--text)}
.hint{font-size:11px;color:var(--muted);margin-top:5px;font-style:italic;line-height:1.4}
@media(max-width:620px){.input-row{grid-template-columns:1fr}.fw-grid,.ct-grid{grid-template-columns:repeat(2,1fr)}header{flex-direction:column;align-items:flex-start;gap:10px}}
</style>
</head>
<body>
<div class="wrap">
<header>
  <div>
    <div class="logo"><span class="p1">Psycho</span><span class="p2">Write</span> <span class="p3">Pro</span></div>
    <div class="tagline">Psychology-Powered Content Engine · Any Niche · Any Format</div>
  </div>
  <div class="vbadge">v2.0</div>
</header>

<!-- 1. CONTENT TYPE -->
<div class="form-block">
  <div class="step-header"><div class="step-num">1</div><div class="step-title">Content Type</div><div class="step-sub">Choose your platform & format</div></div>
  <div class="cat-tabs" id="catTabs">
    <div class="cat-tab active" data-cat="social">📱 Social Media</div>
    <div class="cat-tab" data-cat="website">🌐 Website</div>
    <div class="cat-tab" data-cat="email">📧 Email</div>
    <div class="cat-tab" data-cat="blog">📝 Blog & Articles</div>
    <div class="cat-tab" data-cat="ads">💰 Ads & Sales</div>
    <div class="cat-tab" data-cat="video">🎬 Video & Scripts</div>
  </div>
  <div id="ctGrid" class="ct-grid"></div>
</div>

<!-- SMART AI RECOMMENDATIONS -->
<div class="smart-box" id="smartBox">
  <div class="smart-box-title">✦ AI Recommendations for <span id="smartType">this type</span></div>
  <div class="smart-rec" id="smartRec"></div>
</div>

<!-- 2–4. NICHE, TOPIC, AUDIENCE -->
<div class="input-row">
  <div>
    <div class="step-header"><div class="step-num">2</div><div class="step-title">Niche / Industry</div></div>
    <input type="text" id="nicheInput" placeholder="e.g. Skincare, SaaS, Real Estate, Fitness…" oninput="debounceKw()" />
  </div>
  <div>
    <div class="step-header"><div class="step-num">3</div><div class="step-title">Product / Service / Topic</div></div>
    <input type="text" id="topicInput" placeholder="e.g. Anti-aging serum, coaching, online course…" oninput="debounceKw()" />
  </div>
</div>
<div class="form-block" style="margin-top:-10px">
  <div class="step-header"><div class="step-num">4</div><div class="step-title">Target Audience</div></div>
  <input type="text" id="audienceInput" placeholder="e.g. Women 25–40 with acne, first-time entrepreneurs, Gen Z gamers…" />
  <p class="hint">Be specific — the sharper the audience, the more powerful the psychology.</p>
</div>

<!-- 5. KEYWORD SUGGESTIONS -->
<div class="form-block">
  <div class="step-header"><div class="step-num">5</div><div class="step-title">Keyword Suggestions</div><div class="step-sub">Click to add to your content</div></div>
  <div class="kw-suggestions" id="kwSugg"><span class="kw-loading">Enter niche & topic above to get keyword ideas…</span></div>
</div>

<!-- 6. TONE -->
<div class="form-block">
  <div class="step-header"><div class="step-num">6</div><div class="step-title">Tone of Voice</div></div>
  <div class="chips" id="toneChips">
    <div class="chip green active" data-val="Conversational & Friendly">Conversational</div>
    <div class="chip green" data-val="Professional & Authoritative">Professional</div>
    <div class="chip green" data-val="Bold & Provocative">Bold</div>
    <div class="chip green" data-val="Empathetic & Warm">Empathetic</div>
    <div class="chip green" data-val="Humorous & Witty">Humorous</div>
    <div class="chip green" data-val="Urgent & Persuasive">Urgent</div>
    <div class="chip green" data-val="Inspirational & Motivational">Inspirational</div>
    <div class="chip green" data-val="Educational & Informative">Educational</div>
    <div class="chip green" data-val="Luxury & Refined">Luxury</div>
    <div class="chip green" data-val="Raw & Authentic">Raw / Real</div>
    <div class="chip green" data-val="Playful & Fun">Playful</div>
    <div class="chip green" data-val="Minimalist & Direct">Direct</div>
  </div>
</div>

<!-- 7. FRAMEWORK -->
<div class="form-block">
  <div class="step-header"><div class="step-num">7</div><div class="step-title">Copywriting Framework</div><div class="step-sub">✦ Best Picks are highlighted for your content type</div></div>
  <div class="fw-grid" id="fwGrid"></div>
</div>

<!-- 8. WORD COUNT -->
<div class="wc-section">
  <div class="step-header"><div class="step-num">8</div><div class="step-title">Word Count / Length</div></div>
  <div class="wc-row">
    <span class="wc-lbl">Target length:</span>
    <div class="wc-presets">
      <div class="wc-btn active" data-val="Short (under 300 words)">Short &lt;300</div>
      <div class="wc-btn" data-val="Medium (300–600 words)">Medium 300–600</div>
      <div class="wc-btn" data-val="Long (600–1000 words)">Long 600–1k</div>
      <div class="wc-btn" data-val="In-depth (1000–1500 words)">1k–1.5k</div>
      <div class="wc-btn" data-val="Comprehensive (1500–2500 words)">1.5k–2.5k</div>
    </div>
    <span class="wc-unit">or</span>
    <input class="wc-custom" type="number" id="wcCustom" placeholder="custom" min="50" max="5000" />
    <span class="wc-unit">words</span>
  </div>
</div>

<!-- 9. BLOG OUTLINE (shown for blog types) -->
<div class="form-block" id="blogSection" style="display:none">
  <div class="step-header"><div class="step-num">9</div><div class="step-title">Blog Outline</div><div class="step-sub">Generate structure before writing</div></div>
  <div class="outline-row">
    <label class="toggle-sw">
      <input type="checkbox" id="outlineToggle" onchange="document.getElementById('outlineOpts').classList.toggle('show',this.checked)" />
      <div class="toggle-track"></div>
      <div class="toggle-thumb"></div>
    </label>
    <span class="toggle-lbl">Generate Blog Outline First</span>
  </div>
  <div class="outline-opts" id="outlineOpts">
    <p class="hint">Choose outline structure:</p>
    <div class="outline-grid" id="outlineGrid">
      <div class="o-chip active" data-val="How-to guide with numbered steps">How-To Guide</div>
      <div class="o-chip" data-val="Listicle with numbered tips">Listicle</div>
      <div class="o-chip" data-val="Problem-solution structure">Problem/Solution</div>
      <div class="o-chip" data-val="Comparison / vs article">Comparison</div>
      <div class="o-chip" data-val="Beginner's ultimate guide with all sections">Ultimate Guide</div>
      <div class="o-chip" data-val="Opinion / thought leadership piece">Opinion Piece</div>
      <div class="o-chip" data-val="Case study with results and data">Case Study</div>
      <div class="o-chip" data-val="FAQ format with detailed answers">FAQ Format</div>
      <div class="o-chip" data-val="Storytelling / narrative arc">Story-Driven</div>
      <div class="o-chip" data-val="Pillar page with subtopic sections">Pillar Page</div>
    </div>
  </div>
</div>

<!-- 10. PSYCHOLOGY TRIGGERS -->
<div class="form-block">
  <div class="step-header">
    <div class="step-num" id="trigStepNum">10</div>
    <div class="step-title">Psychology Triggers</div>
    <div class="step-sub">Multi-select · auto-matched to your content type</div>
  </div>
  <div style="display:flex;gap:8px;margin-bottom:16px;flex-wrap:wrap">
    <button class="auto-btn" onclick="autoTriggers()">✦ Auto-Select Best for My Content Type</button>
    <button class="auto-btn" style="border-color:rgba(252,92,156,0.4);color:var(--accent2)" onclick="clearTriggers()">✕ Clear All</button>
  </div>

  <div class="trig-cat-lbl">🔥 Conversion & Sales</div>
  <div class="trig-grid" id="tcSales">
    <div class="trig-card" data-val="Loss Aversion"><span class="trig-badge bs">SALES</span><div class="trig-icon">😰</div><div class="trig-name">Loss Aversion</div><div class="trig-desc">Fear of losing &gt; desire to gain</div></div>
    <div class="trig-card" data-val="Scarcity Effect"><span class="trig-badge bu">URGENCY</span><div class="trig-icon">⏳</div><div class="trig-name">Scarcity</div><div class="trig-desc">Limited = more desirable</div></div>
    <div class="trig-card" data-val="Anchoring Effect"><span class="trig-badge bs">SALES</span><div class="trig-icon">⚓</div><div class="trig-name">Anchoring</div><div class="trig-desc">First price sets value perception</div></div>
    <div class="trig-card" data-val="Decoy Effect"><span class="trig-badge bs">SALES</span><div class="trig-icon">🎭</div><div class="trig-name">Decoy Effect</div><div class="trig-desc">3rd option makes choice obvious</div></div>
    <div class="trig-card" data-val="Reciprocity"><span class="trig-badge bs">SALES</span><div class="trig-icon">🤝</div><div class="trig-name">Reciprocity</div><div class="trig-desc">Give value first, get loyalty back</div></div>
    <div class="trig-card" data-val="Urgency"><span class="trig-badge bu">URGENCY</span><div class="trig-icon">⚡</div><div class="trig-name">Urgency</div><div class="trig-desc">Time-limited pressure to act now</div></div>
  </div>

  <div class="trig-cat-lbl">🛡️ Trust & Credibility</div>
  <div class="trig-grid" id="tcTrust">
    <div class="trig-card" data-val="Social Proof"><span class="trig-badge bt">TRUST</span><div class="trig-icon">👥</div><div class="trig-name">Social Proof</div><div class="trig-desc">Others use & love it</div></div>
    <div class="trig-card" data-val="Authority Bias"><span class="trig-badge bt">TRUST</span><div class="trig-icon">🏆</div><div class="trig-name">Authority</div><div class="trig-desc">Experts & credentials = trust</div></div>
    <div class="trig-card" data-val="Halo Effect"><span class="trig-badge bt">TRUST</span><div class="trig-icon">✨</div><div class="trig-name">Halo Effect</div><div class="trig-desc">One great trait elevates all</div></div>
    <div class="trig-card" data-val="Commitment & Consistency"><span class="trig-badge bt">TRUST</span><div class="trig-icon">🔒</div><div class="trig-name">Consistency</div><div class="trig-desc">Small yes leads to bigger yes</div></div>
    <div class="trig-card" data-val="Transparency & Honesty"><span class="trig-badge bt">TRUST</span><div class="trig-icon">🪟</div><div class="trig-name">Transparency</div><div class="trig-desc">Honesty builds deeper trust</div></div>
  </div>

  <div class="trig-cat-lbl">🧠 Engagement & Retention</div>
  <div class="trig-grid" id="tcEngage">
    <div class="trig-card" data-val="Curiosity Gap"><span class="trig-badge be">ENGAGE</span><div class="trig-icon">🔍</div><div class="trig-name">Curiosity Gap</div><div class="trig-desc">Tease the answer, hook them in</div></div>
    <div class="trig-card" data-val="Storytelling"><span class="trig-badge be">ENGAGE</span><div class="trig-icon">📖</div><div class="trig-name">Storytelling</div><div class="trig-desc">Narrative creates emotional bond</div></div>
    <div class="trig-card" data-val="Confirmation Bias"><span class="trig-badge be">ENGAGE</span><div class="trig-icon">💡</div><div class="trig-name">Confirmation</div><div class="trig-desc">Validate what they already believe</div></div>
    <div class="trig-card" data-val="Mere-Exposure Effect"><span class="trig-badge be">ENGAGE</span><div class="trig-icon">🔁</div><div class="trig-name">Familiarity</div><div class="trig-desc">Repetition creates preference</div></div>
    <div class="trig-card" data-val="Goal Gradient Effect"><span class="trig-badge be">ENGAGE</span><div class="trig-icon">🎯</div><div class="trig-name">Goal Gradient</div><div class="trig-desc">Progress motivates completion</div></div>
    <div class="trig-card" data-val="Pattern Interrupt"><span class="trig-badge be">ENGAGE</span><div class="trig-icon">💥</div><div class="trig-name">Pattern Interrupt</div><div class="trig-desc">Surprise stops the scroll</div></div>
  </div>

  <div class="trig-cat-lbl">💬 Emotional & Identity</div>
  <div class="trig-grid" id="tcEmotion">
    <div class="trig-card" data-val="Identity & Belonging"><span class="trig-badge be">IDENTITY</span><div class="trig-icon">🪞</div><div class="trig-name">Identity</div><div class="trig-desc">"This is who I am" connection</div></div>
    <div class="trig-card" data-val="Pain Amplification"><span class="trig-badge bs">EMOTION</span><div class="trig-icon">😤</div><div class="trig-name">Pain Amp.</div><div class="trig-desc">Make the problem feel real & urgent</div></div>
    <div class="trig-card" data-val="Aspiration & Dream Outcome"><span class="trig-badge be">EMOTION</span><div class="trig-icon">🌟</div><div class="trig-name">Aspiration</div><div class="trig-desc">Paint the dream they want</div></div>
    <div class="trig-card" data-val="Fear & Safety"><span class="trig-badge bu">EMOTION</span><div class="trig-icon">🛡️</div><div class="trig-name">Fear & Safety</div><div class="trig-desc">Protect from bad outcomes</div></div>
    <div class="trig-card" data-val="Exclusivity & VIP Status"><span class="trig-badge bs">EMOTION</span><div class="trig-icon">💎</div><div class="trig-name">Exclusivity</div><div class="trig-desc">Not everyone gets access</div></div>
  </div>
</div>

<!-- 11. EXTRA CONTEXT -->
<div class="form-block">
  <div class="step-header"><div class="step-num" id="ctxStepNum">11</div><div class="step-title">Key Message & Extra Details</div></div>
  <textarea id="contextInput" placeholder="Add USPs, offers, pricing, specific CTAs, brand voice, keywords to include, or anything else the AI should know…"></textarea>
  <div id="usedKwsDiv" style="display:flex;flex-wrap:wrap;gap:6px;margin-top:8px"></div>
</div>

<hr class="divider">

<button class="btn-gen" id="genBtn" onclick="generate()">
  <div class="btn-inner"><span>⚡</span><span>Generate Psychology-Driven Content</span></div>
  <div class="shimmer"></div>
</button>

<!-- OUTPUT -->
<div class="out-section" id="outSection">
  <hr class="divider">
  <div class="out-header">
    <div class="out-title">✦ Your Content</div>
    <div class="out-actions">
      <button class="btn-act" onclick="copyOut()">📋 Copy</button>
      <button class="btn-act" onclick="downloadOut()">⬇ Download</button>
    </div>
  </div>
  <div id="metaTags" class="meta-tags"></div>
  <div class="out-box" id="outBox"></div>
  <div class="char-info" id="charInfo"></div>
  <div class="regen-row">
    <button class="btn-regen" onclick="generate()">🔄 Regenerate</button>
    <button class="btn-regen" onclick="gen('make it significantly shorter and punchier')">✂️ Shorter</button>
    <button class="btn-regen" onclick="gen('write a stronger, more urgent and creative CTA')">🔥 Stronger CTA</button>
    <button class="btn-regen" onclick="gen('rewrite with deeper storytelling and emotional resonance')">💭 More Emotional</button>
    <button class="btn-regen" onclick="gen('optimize for SEO with natural keyword integration and proper heading structure')">🔍 SEO Boost</button>
    <button class="btn-regen" onclick="gen('completely different angle, hook, and structure')">🎲 New Angle</button>
  </div>
</div>
<div style="height:80px"></div>
</div>

<script>
const CT = {
  social:[
    {icon:'📸',name:'Instagram Caption',hint:'Feed post copy'},
    {icon:'🎠',name:'Instagram Carousel',hint:'Slide-by-slide copy'},
    {icon:'💬',name:'Instagram Story',hint:'Poll / swipe-up CTA'},
    {icon:'🎵',name:'TikTok Caption',hint:'Short + hooky'},
    {icon:'🐦',name:'Twitter/X Post',hint:'280 chars max'},
    {icon:'🧵',name:'Twitter/X Thread',hint:'Multi-tweet story'},
    {icon:'💼',name:'LinkedIn Post',hint:'Professional value post'},
    {icon:'👥',name:'Facebook Post',hint:'Community / share bait'},
    {icon:'📌',name:'Pinterest Description',hint:'SEO + visual hook'},
  ],
  website:[
    {icon:'🏠',name:'Homepage Hero',hint:'Above-the-fold copy'},
    {icon:'📜',name:'About Page',hint:'Brand story + trust'},
    {icon:'🛍️',name:'Services Page',hint:'Offer + benefits'},
    {icon:'💰',name:'Pricing Page',hint:'Value + CTA'},
    {icon:'📞',name:'Contact Page',hint:'CTA + reassurance'},
    {icon:'❓',name:'FAQ Page',hint:'Objection handling'},
    {icon:'🌟',name:'Testimonials Page',hint:'Social proof copy'},
    {icon:'🚀',name:'Landing Page',hint:'Full conversion page'},
    {icon:'🎁',name:'Thank You Page',hint:'Post-conversion delight'},
    {icon:'📋',name:'Case Study',hint:'Story + results'},
    {icon:'🏷️',name:'Product Page',hint:'Ecommerce detail copy'},
    {icon:'⚖️',name:'Comparison Page',hint:'Us vs them breakdown'},
    {icon:'🍪',name:'404 / Error Page',hint:'Keep them engaged'},
    {icon:'🗺️',name:'Microcopy / UI Text',hint:'Buttons, labels, hints'},
  ],
  email:[
    {icon:'📧',name:'Email Subject Line',hint:'Open rate booster'},
    {icon:'👋',name:'Welcome Email',hint:'First impression'},
    {icon:'📣',name:'Promotional Email',hint:'Sales / offer'},
    {icon:'🔁',name:'Re-engagement Email',hint:'Win back subscribers'},
    {icon:'🛒',name:'Cart Abandonment',hint:'Recover lost sales'},
    {icon:'📰',name:'Newsletter',hint:'Value + stories + CTA'},
    {icon:'💌',name:'Nurture Sequence',hint:'Multi-email flow'},
    {icon:'🎉',name:'Launch Announcement',hint:'Hype + urgency'},
    {icon:'🙏',name:'Thank You Email',hint:'Post-purchase warmth'},
    {icon:'⭐',name:'Review Request Email',hint:'Social proof ask'},
    {icon:'🔔',name:'Onboarding Email',hint:'New user activation'},
  ],
  blog:[
    {icon:'📝',name:'Blog Post',hint:'Full article'},
    {icon:'📋',name:'Blog Outline',hint:'Structure before writing'},
    {icon:'🔢',name:'Listicle',hint:'Top X of Y format'},
    {icon:'❓',name:'How-To Article',hint:'Step-by-step guide'},
    {icon:'⚖️',name:'Comparison Article',hint:'A vs B breakdown'},
    {icon:'💡',name:'Opinion / Thought Leadership',hint:'Your POV piece'},
    {icon:'📖',name:'Ultimate Guide',hint:'Definitive resource'},
    {icon:'📊',name:'Data-Driven Report',hint:'Stats + insights'},
    {icon:'🎙️',name:'Interview Article',hint:'Q&A format'},
    {icon:'🔖',name:'Content Roundup',hint:'Curated best-of'},
    {icon:'🧩',name:'Pillar Page',hint:'SEO hub content'},
    {icon:'📰',name:'Press Release',hint:'Newsworthy announcement'},
  ],
  ads:[
    {icon:'💰',name:'Facebook/IG Ad',hint:'Paid social copy'},
    {icon:'🔍',name:'Google Search Ad',hint:'Headlines + descriptions'},
    {icon:'📺',name:'YouTube Ad Script',hint:'Pre-roll hook copy'},
    {icon:'🛍️',name:'Product Description',hint:'Ecommerce persuasion'},
    {icon:'🎯',name:'Retargeting Ad',hint:'Warm audience nudge'},
    {icon:'📱',name:'App Store Description',hint:'Download CTA copy'},
    {icon:'💸',name:'Sales Page',hint:'Long-form persuasion'},
    {icon:'🎪',name:'Advertorial',hint:'Native ad article'},
    {icon:'📦',name:'Packaging Copy',hint:'Product labels + inserts'},
    {icon:'🏷️',name:'Tagline / Slogan',hint:'Brand one-liner'},
    {icon:'🤝',name:'Affiliate Copy',hint:'Partner promotion'},
  ],
  video:[
    {icon:'🎬',name:'YouTube Script',hint:'Full video script'},
    {icon:'📣',name:'YouTube Hook / Intro',hint:'First 30 seconds'},
    {icon:'🎵',name:'Reel / TikTok Script',hint:'15–60 second video'},
    {icon:'🎙️',name:'Podcast Intro / Outro',hint:'Show open & close'},
    {icon:'📺',name:'Explainer Video Script',hint:'Product walkthrough'},
    {icon:'🎤',name:'Webinar Script',hint:'Presentation flow'},
    {icon:'💼',name:'Video Sales Letter',hint:'VSL persuasion copy'},
    {icon:'⚡',name:'Video Ad Script',hint:'Paid video copy'},
    {icon:'🔴',name:'Live Stream Outline',hint:'Going live structure'},
  ]
};

const FW = [
  {name:'AIDA',full:'Attention, Interest, Desire, Action',desc:'Classic 4-step flow. Works on any platform.',best:['Instagram Caption','Facebook/IG Ad','Email Subject Line','Landing Page','Homepage Hero','Promotional Email']},
  {name:'PAS',full:'Problem, Agitate, Solution',desc:'Pain → twist knife → relief. Powerful for problem-aware audiences.',best:['Blog Post','Facebook/IG Ad','Sales Page','Newsletter','Product Page','Cart Abandonment']},
  {name:'PASO',full:'Problem, Agitate, Solution, Outcome',desc:'PAS + the transformation they\'ll achieve.',best:['Landing Page','Sales Page','YouTube Script','Webinar Script','Case Study','Video Sales Letter']},
  {name:'HERO',full:'Hook, Engage, Reveal, Offer',desc:'Story-driven. Great for video and long-form.',best:['YouTube Script','Reel / TikTok Script','Instagram Carousel','Blog Post','Video Sales Letter','Webinar Script']},
  {name:'SLAP',full:'Stop, Look, Act, Purchase',desc:'Pattern interrupt for fast-scroll content.',best:['Instagram Caption','TikTok Caption','Twitter/X Post','Facebook/IG Ad','Retargeting Ad','Instagram Story']},
  {name:'PAPA',full:'Problem, Advantages, Proof, Action',desc:'Lead with advantages + credibility.',best:['Services Page','Product Page','Testimonials Page','Cart Abandonment','Promotional Email','Re-engagement Email']},
  {name:'4Cs',full:'Clear, Concise, Compelling, Credible',desc:'Quality filter — every word earns its place.',best:['Homepage Hero','About Page','Pricing Page','Google Search Ad','Tagline / Slogan','Microcopy / UI Text']},
  {name:'FAB',full:'Features, Advantages, Benefits',desc:'Transform specs into emotional outcomes.',best:['Product Description','Product Page','Services Page','App Store Description','Packaging Copy','Comparison Page']},
  {name:'QUEST',full:'Qualify, Understand, Educate, Stimulate, Transition',desc:'Guides skeptics to believers.',best:['Blog Post','Ultimate Guide','Webinar Script','Pillar Page','How-To Article','Onboarding Email']},
  {name:'ACE',full:'Attention, Content, Engage',desc:'Value-first. Builds trust before asking.',best:['LinkedIn Post','Newsletter','Blog Outline','Listicle','Content Roundup','Twitter/X Thread']},
  {name:'ACC',full:'Awareness, Comprehension, Conversion',desc:'Cold to buying in 3 stages.',best:['YouTube Ad Script','Explainer Video Script','Comparison Article','Pillar Page','Advertorial','Google Search Ad']},
  {name:'BAB',full:'Before, After, Bridge',desc:'Show transformation — pain, dream, path.',best:['Testimonials Page','Welcome Email','Instagram Carousel','Re-engagement Email','Opinion / Thought Leadership','Case Study']},
];

const TM = {
  'Instagram Caption':['Loss Aversion','Scarcity Effect','Curiosity Gap','Pattern Interrupt','Storytelling'],
  'Instagram Carousel':['Curiosity Gap','Goal Gradient Effect','Storytelling','Confirmation Bias','Authority Bias'],
  'Instagram Story':['Scarcity Effect','Urgency','Social Proof','Loss Aversion'],
  'TikTok Caption':['Pattern Interrupt','Curiosity Gap','Storytelling','Identity & Belonging'],
  'Twitter/X Post':['Pattern Interrupt','Curiosity Gap','Confirmation Bias'],
  'Twitter/X Thread':['Curiosity Gap','Storytelling','Goal Gradient Effect','Authority Bias'],
  'LinkedIn Post':['Authority Bias','Social Proof','Storytelling','Aspiration & Dream Outcome'],
  'Facebook Post':['Social Proof','Storytelling','Confirmation Bias','Identity & Belonging'],
  'Homepage Hero':['Anchoring Effect','Social Proof','Aspiration & Dream Outcome','Halo Effect','Loss Aversion'],
  'About Page':['Storytelling','Transparency & Honesty','Identity & Belonging','Halo Effect'],
  'Services Page':['Social Proof','Authority Bias','Loss Aversion','Anchoring Effect','Pain Amplification'],
  'Pricing Page':['Anchoring Effect','Decoy Effect','Scarcity Effect','Social Proof','Loss Aversion'],
  'Landing Page':['Loss Aversion','Social Proof','Scarcity Effect','Pain Amplification','Aspiration & Dream Outcome','Urgency'],
  'FAQ Page':['Transparency & Honesty','Social Proof','Commitment & Consistency','Authority Bias'],
  'Product Page':['Social Proof','Scarcity Effect','Anchoring Effect','Aspiration & Dream Outcome','Loss Aversion'],
  'Sales Page':['Pain Amplification','Loss Aversion','Social Proof','Scarcity Effect','Anchoring Effect','Aspiration & Dream Outcome','Urgency'],
  'Comparison Page':['Authority Bias','Transparency & Honesty','Anchoring Effect','Social Proof'],
  'Thank You Page':['Reciprocity','Commitment & Consistency','Social Proof'],
  'Case Study':['Social Proof','Authority Bias','Storytelling','Aspiration & Dream Outcome'],
  'Testimonials Page':['Social Proof','Halo Effect','Authority Bias','Aspiration & Dream Outcome'],
  'Contact Page':['Transparency & Honesty','Social Proof','Commitment & Consistency'],
  'Email Subject Line':['Curiosity Gap','Scarcity Effect','Loss Aversion','Pattern Interrupt'],
  'Welcome Email':['Reciprocity','Commitment & Consistency','Storytelling','Aspiration & Dream Outcome'],
  'Promotional Email':['Scarcity Effect','Urgency','Loss Aversion','Social Proof'],
  'Cart Abandonment':['Loss Aversion','Scarcity Effect','Social Proof','Urgency'],
  'Newsletter':['Storytelling','Reciprocity','Mere-Exposure Effect','Curiosity Gap'],
  'Re-engagement Email':['Loss Aversion','Curiosity Gap','Reciprocity','Aspiration & Dream Outcome'],
  'Launch Announcement':['Scarcity Effect','Urgency','Social Proof','Aspiration & Dream Outcome'],
  'Blog Post':['Curiosity Gap','Storytelling','Authority Bias','Goal Gradient Effect','Confirmation Bias'],
  'Blog Outline':['Curiosity Gap','Goal Gradient Effect','Authority Bias'],
  'Listicle':['Curiosity Gap','Goal Gradient Effect','Authority Bias','Social Proof'],
  'How-To Article':['Authority Bias','Goal Gradient Effect','Aspiration & Dream Outcome','Commitment & Consistency'],
  'Ultimate Guide':['Authority Bias','Curiosity Gap','Goal Gradient Effect','Social Proof'],
  'Opinion / Thought Leadership':['Confirmation Bias','Storytelling','Authority Bias','Identity & Belonging'],
  'Comparison Article':['Authority Bias','Transparency & Honesty','Confirmation Bias','Social Proof'],
  'YouTube Script':['Storytelling','Curiosity Gap','Pattern Interrupt','Aspiration & Dream Outcome','Loss Aversion'],
  'Reel / TikTok Script':['Pattern Interrupt','Curiosity Gap','Storytelling','Identity & Belonging'],
  'Facebook/IG Ad':['Loss Aversion','Social Proof','Pain Amplification','Scarcity Effect','Pattern Interrupt'],
  'Product Description':['Aspiration & Dream Outcome','Anchoring Effect','Social Proof','Exclusivity & VIP Status'],
  'Video Sales Letter':['Pain Amplification','Loss Aversion','Social Proof','Scarcity Effect','Storytelling','Urgency'],
  'Google Search Ad':['Curiosity Gap','Loss Aversion','Social Proof','Urgency'],
  'Tagline / Slogan':['Identity & Belonging','Aspiration & Dream Outcome','Halo Effect'],
  'Webinar Script':['Curiosity Gap','Social Proof','Aspiration & Dream Outcome','Scarcity Effect','Goal Gradient Effect'],
};

const BLOG_TYPES = ['Blog Post','Blog Outline','Listicle','How-To Article','Comparison Article','Ultimate Guide','Opinion / Thought Leadership','Data-Driven Report','Case Study','Pillar Page','Press Release'];

let selCT = 'Instagram Caption';
let selFW = 'AIDA';
let kwTimer = null;
let usedKws = [];

function init(){
  renderCT('social');
  renderFW('Instagram Caption');
  setupTone();
  setupWC();
  setupOutlineChips();
  setupTriggers();
}

function renderCT(cat){
  const g = document.getElementById('ctGrid');
  g.innerHTML = (CT[cat]||[]).map(t=>`<div class="ct-card ${selCT===t.name?'active':''}" data-val="${t.name}" onclick="pickCT('${t.name}')"><div class="ct-icon">${t.icon}</div><div class="ct-name">${t.name}</div><div class="ct-hint">${t.hint}</div></div>`).join('');
}

function pickCT(n){
  selCT=n;
  document.querySelectorAll('.ct-card').forEach(c=>c.classList.toggle('active',c.dataset.val===n));
  renderFW(n);
  showSmart(n);
  autoTriggers(n);
  document.getElementById('blogSection').style.display = BLOG_TYPES.includes(n)?'block':'none';
}

document.getElementById('catTabs').addEventListener('click',e=>{
  const t=e.target.closest('.cat-tab'); if(!t)return;
  document.querySelectorAll('.cat-tab').forEach(x=>x.classList.remove('active'));
  t.classList.add('active');
  renderCT(t.dataset.cat);
});

function showSmart(ct){
  const box=document.getElementById('smartBox');
  document.getElementById('smartType').textContent=ct;
  const bfw=FW.filter(f=>f.best.includes(ct)).slice(0,3);
  const btr=(TM[ct]||[]).slice(0,4);
  let h=`<span class="smart-lbl">Frameworks:</span>`;
  h+=bfw.map(f=>`<span class="smart-tag fw" onclick="pickSmFW('${f.name}')">${f.name} — ${f.full}</span>`).join('');
  h+=`<span class="smart-lbl" style="margin-left:8px">Triggers:</span>`;
  h+=btr.map(t=>`<span class="smart-tag tr" onclick="pickSmTR('${t}')">${t}</span>`).join('');
  document.getElementById('smartRec').innerHTML=h;
  box.classList.add('show');
}

function pickSmFW(n){selFW=n;renderFW(selCT);document.querySelectorAll('.smart-tag.fw').forEach(t=>t.classList.toggle('picked',t.textContent.startsWith(n)))}
function pickSmTR(n){document.querySelectorAll('.trig-card').forEach(c=>{if(c.dataset.val===n)c.classList.add('active')});document.querySelectorAll('.smart-tag.tr').forEach(t=>{if(t.textContent===n)t.classList.add('picked')})}

function renderFW(ct){
  const best=FW.filter(f=>f.best.includes(ct)).map(f=>f.name);
  if(!selFW||!FW.find(f=>f.name===selFW))selFW=best[0]||'AIDA';
  document.getElementById('fwGrid').innerHTML=FW.map(f=>`<div class="fw-card ${selFW===f.name?'active':''} ${best.includes(f.name)?'ai-rec':''}" onclick="pickFW('${f.name}')"><div class="fw-name">${f.name}</div><div class="fw-full">${f.full}</div><div class="fw-desc">${f.desc}</div></div>`).join('');
}

function pickFW(n){selFW=n;document.querySelectorAll('.fw-card').forEach(c=>c.classList.toggle('active',c.querySelector('.fw-name').textContent===n))}

function setupTone(){
  document.getElementById('toneChips').addEventListener('click',e=>{
    const c=e.target.closest('.chip');if(!c)return;
    document.querySelectorAll('#toneChips .chip').forEach(x=>x.classList.remove('active'));
    c.classList.add('active');
  });
}

function setupWC(){
  document.querySelectorAll('.wc-btn').forEach(b=>b.addEventListener('click',()=>{
    document.querySelectorAll('.wc-btn').forEach(x=>x.classList.remove('active'));
    b.classList.add('active');
    document.getElementById('wcCustom').value='';
  }));
}

function setupOutlineChips(){
  document.getElementById('outlineGrid').addEventListener('click',e=>{
    const c=e.target.closest('.o-chip');if(!c)return;
    document.querySelectorAll('.o-chip').forEach(x=>x.classList.remove('active'));
    c.classList.add('active');
  });
}

function setupTriggers(){
  document.querySelectorAll('.trig-card').forEach(c=>c.addEventListener('click',()=>c.classList.toggle('active')));
}

function autoTriggers(ct){
  const n=ct||selCT;
  const rec=TM[n]||[];
  document.querySelectorAll('.trig-card').forEach(c=>c.classList.toggle('active',rec.includes(c.dataset.val)));
}

function clearTriggers(){document.querySelectorAll('.trig-card').forEach(c=>c.classList.remove('active'))}

function debounceKw(){
  clearTimeout(kwTimer);
  kwTimer=setTimeout(fetchKw,900);
}

async function fetchKw(){
  const niche=document.getElementById('nicheInput').value.trim();
  const topic=document.getElementById('topicInput').value.trim();
  if(!niche&&!topic)return;
  const c=document.getElementById('kwSugg');
  c.innerHTML='<span class="kw-loading">Generating keyword ideas…</span>';
  try{
    const r=await fetch('https://api.anthropic.com/v1/messages',{method:'POST',headers:{'Content-Type':'application/json'},body:JSON.stringify({model:'claude-sonnet-4-20250514',max_tokens:250,messages:[{role:'user',content:`Generate 12 short, high-impact SEO and content keywords for: niche="${niche}", topic="${topic}". Return ONLY a valid JSON array of strings, nothing else. No markdown, no explanation.`}]})});
    const d=await r.json();
    const raw=d.content.map(i=>i.text||'').join('').replace(/```json|```/g,'').trim();
    const kws=JSON.parse(raw);
    c.innerHTML=kws.map(k=>`<span class="kw-tag ${usedKws.includes(k)?'used':''}" onclick="useKw('${k.replace(/'/g,"&#39;")}')">${k}</span>`).join('');
  }catch(e){c.innerHTML='<span class="kw-loading">Could not load suggestions. Try again.</span>'}
}

function useKw(kw){
  if(usedKws.includes(kw))return;
  usedKws.push(kw);
  const ctx=document.getElementById('contextInput');
  ctx.value=ctx.value?(ctx.value+', '+kw):kw;
  document.querySelectorAll('.kw-tag').forEach(t=>{if(t.textContent===kw)t.classList.add('used')});
  renderUsedKws();
}

function renderUsedKws(){
  document.getElementById('usedKwsDiv').innerHTML=usedKws.map(k=>`<span class="kw-tag used" style="font-size:11px">${k} <span onclick="rmKw('${k.replace(/'/g,"&#39;")}')" style="cursor:pointer;opacity:.6;margin-left:2px">✕</span></span>`).join('');
}

function rmKw(kw){
  usedKws=usedKws.filter(k=>k!==kw);
  const ctx=document.getElementById('contextInput');
  ctx.value=ctx.value.split(', ').filter(k=>k!==kw).join(', ');
  document.querySelectorAll('.kw-tag').forEach(t=>{if(t.textContent.startsWith(kw))t.classList.remove('used')});
  renderUsedKws();
}

async function generate(mod=''){
  const tone=document.querySelector('#toneChips .chip.active')?.dataset.val||'Conversational';
  const audience=document.getElementById('audienceInput').value||'general audience';
  const niche=document.getElementById('nicheInput').value||'general';
  const topic=document.getElementById('topicInput').value||'product or service';
  const context=document.getElementById('contextInput').value;
  const triggers=Array.from(document.querySelectorAll('.trig-card.active')).map(c=>c.dataset.val);
  const wcCustom=document.getElementById('wcCustom').value;
  const wcPreset=document.querySelector('.wc-btn.active')?.dataset.val||'';
  const wc=wcCustom?`${wcCustom} words`:wcPreset;
  const isOutline=document.getElementById('outlineToggle')?.checked;
  const outStyle=document.querySelector('.o-chip.active')?.dataset.val||'';
  const fwObj=FW.find(f=>f.name===selFW);

  const btn=document.getElementById('genBtn');
  btn.disabled=true;

  const outSec=document.getElementById('outSection');
  const outBox=document.getElementById('outBox');
  outSec.classList.add('visible');
  outBox.className='out-box loading';
  outBox.innerHTML='<div class="dots"><span></span><span></span><span></span></div>';
  document.getElementById('charInfo').textContent='';
  document.getElementById('metaTags').innerHTML='';
  outSec.scrollIntoView({behavior:'smooth',block:'start'});

  const outlineInstr=isOutline?`\n\nIMPORTANT: First generate a detailed blog outline using "${outStyle}" structure with H2/H3 sections, then write the full content following that outline exactly.`:'';

  const prompt=`You are PsychoWrite Pro — a world-class psychology-driven content writer and neuromarketing expert. You master every copywriting framework and every platform's nuances.

ASSIGNMENT: Write a "${selCT}"

NICHE: ${niche}
PRODUCT/SERVICE/TOPIC: ${topic}
TARGET AUDIENCE: ${audience}
COPYWRITING FRAMEWORK: ${selFW} (${fwObj?.full||''}) — follow this structure exactly
TONE OF VOICE: ${tone}
TARGET LENGTH: ${wc}
PSYCHOLOGY TRIGGERS (embed naturally, never explicitly): ${triggers.length>0?triggers.join(', '):'Social Proof, Loss Aversion'}
EXTRA CONTEXT / KEY MESSAGE: ${context||'Make it compelling and conversion-focused'}
${mod?`SPECIAL INSTRUCTION: ${mod}`:''}
${outlineInstr}

STRICT RULES:
1. Structure content using ${selFW} framework — each stage must be clear in the flow
2. Embed psychology triggers subtly — they should feel natural, never salesy or obvious
3. Always use "you/your" language, never "we/our" unless it's brand-specific
4. Use strong verbs: smash, uncover, eliminate, discover, transform, ignite, unlock
5. NEVER open with: "Are you looking for...", "In today's world...", "Have you ever wondered..."
6. Lead with your STRONGEST hook — most powerful line goes first
7. Cut every filler word — every sentence must earn its place
8. End with a creative, specific CTA that matches the platform (not generic "Buy Now")
9. Format correctly for ${selCT}: use line breaks for social, headers for long-form, emojis if social
10. Write ONLY the content — no intro sentences like "Here is your...", no labels, no meta-commentary

Write it now:`;

  try{
    const r=await fetch('https://api.anthropic.com/v1/messages',{method:'POST',headers:{'Content-Type':'application/json'},body:JSON.stringify({model:'claude-sonnet-4-20250514',max_tokens:1800,messages:[{role:'user',content:prompt}]})});
    const d=await r.json();
    const txt=d.content.map(i=>i.text||'').join('\n').trim();
    outBox.className='out-box';
    outBox.textContent=txt;
    const wds=txt.split(/\s+/).filter(Boolean).length;
    document.getElementById('charInfo').textContent=`${txt.length} characters · ${wds} words · ${selCT}`;
    document.getElementById('metaTags').innerHTML=`<span class="mt mt-p">${selCT}</span><span class="mt mt-k">${selFW} — ${fwObj?.full||''}</span><span class="mt mt-g">${tone.split(' ')[0]}</span>${triggers.slice(0,3).map(t=>`<span class="mt mt-y">${t}</span>`).join('')}`;
  }catch(e){
    outBox.className='out-box';
    outBox.textContent='Something went wrong. Please try again.';
  }
  btn.disabled=false;
}

function gen(mod){generate(mod)}

function copyOut(){
  const txt=document.getElementById('outBox').textContent;
  navigator.clipboard.writeText(txt).then(()=>{
    const b=document.querySelector('.btn-act');
    b.textContent='✓ Copied!';
    setTimeout(()=>b.textContent='📋 Copy',2000);
  });
}

function downloadOut(){
  const txt=document.getElementById('outBox').textContent;
  const a=document.createElement('a');
  a.href=URL.createObjectURL(new Blob([txt],{type:'text/plain'}));
  a.download=`psychowrite-${selCT.toLowerCase().replace(/[\s/]+/g,'-')}.txt`;
  a.click();
}

init();
showSmart('Instagram Caption');
autoTriggers('Instagram Caption');
</script>
</body>
</html>
