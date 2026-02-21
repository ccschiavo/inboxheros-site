<!doctype html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Visea — AI-Powered Executive Assistance</title>
  <meta name="description" content="AI-powered, human-led executive assistance for founders and executives. Inbox, calendar, follow-through, travel, and ops—without hand-holding." />

  <style>
    :root{
      --bg:#0b0f19;
      --panel:#10182a;
      --panel2:#0e1627;
      --text:#e9eefc;
      --muted:#b6c2e2;
      --muted2:#93a4cc;
      --brand:#6ea8ff;
      --brand2:#8d7bff;
      --ok:#40d39c;
      --border:rgba(255,255,255,.10);
      --shadow: 0 18px 60px rgba(0,0,0,.35);
      --radius: 18px;
      --max: 1120px;
    }
    *{box-sizing:border-box}
    html,body{height:100%}
    body{
      margin:0;
      font-family: ui-sans-serif, system-ui, -apple-system, Segoe UI, Roboto, Helvetica, Arial, "Apple Color Emoji","Segoe UI Emoji";
      background: radial-gradient(1200px 600px at 20% -10%, rgba(110,168,255,.35), transparent 60%),
                  radial-gradient(900px 500px at 90% 10%, rgba(141,123,255,.25), transparent 60%),
                  var(--bg);
      color: var(--text);
      line-height: 1.45;
    }
    a{color:inherit}
    .wrap{max-width:var(--max); margin:0 auto; padding: 24px;}
    .topbar{
      position: sticky;
      top: 0;
      z-index: 10;
      background: rgba(11,15,25,.7);
      backdrop-filter: blur(10px);
      border-bottom: 1px solid var(--border);
    }
    .topbar .wrap{
      display:flex; align-items:center; justify-content:space-between; gap:16px;
      padding-top:14px; padding-bottom:14px;
    }
    .brand{
      display:flex; align-items:center; gap:10px; text-decoration:none;
      font-weight:700; letter-spacing:.2px;
    }
    .logo{
      width:34px; height:34px; border-radius:12px;
      background: linear-gradient(135deg, var(--brand), var(--brand2));
      box-shadow: 0 12px 30px rgba(110,168,255,.25);
    }
    nav{display:flex; gap:14px; flex-wrap:wrap; align-items:center}
    nav a{
      text-decoration:none;
      color: var(--muted);
      font-weight:600;
      font-size: 14px;
      padding:8px 10px;
      border-radius: 12px;
    }
    nav a:hover{background: rgba(255,255,255,.05); color: var(--text);}
    .btn{
      display:inline-flex; align-items:center; justify-content:center;
      gap:10px;
      padding: 12px 16px;
      border-radius: 14px;
      border: 1px solid var(--border);
      text-decoration:none;
      font-weight: 700;
      font-size: 14px;
      cursor:pointer;
      transition: transform .05s ease, background .2s ease;
      user-select:none;
    }
    .btn:active{transform: translateY(1px);}
    .btn.primary{
      background: linear-gradient(135deg, rgba(110,168,255,.95), rgba(141,123,255,.95));
      border-color: transparent;
      color: #061022;
    }
    .btn.ghost{
      background: rgba(255,255,255,.04);
      color: var(--text);
    }
    .btn.small{padding:10px 12px; border-radius: 12px;}
    .hero{
      padding: 54px 0 24px;
    }
    .grid{
      display:grid;
      grid-template-columns: 1.15fr .85fr;
      gap: 28px;
      align-items: start;
    }
    @media (max-width: 920px){
      .grid{grid-template-columns:1fr;}
      nav{display:none}
    }
    .h-eyebrow{
      display:inline-flex; gap:10px; align-items:center;
      padding: 8px 12px;
      border: 1px solid var(--border);
      border-radius: 999px;
      background: rgba(255,255,255,.03);
      color: var(--muted);
      font-weight: 700;
      font-size: 13px;
    }
    .dot{width:8px;height:8px;border-radius:50%; background: var(--ok); box-shadow: 0 0 0 6px rgba(64,211,156,.12);}
    h1{
      margin: 14px 0 10px;
      font-size: 44px;
      line-height: 1.05;
      letter-spacing: -1px;
    }
    @media (max-width: 520px){
      h1{font-size: 36px;}
    }
    .lead{
      color: var(--muted);
      font-size: 18px;
      max-width: 62ch;
      margin: 12px 0 18px;
    }
    .cta-row{display:flex; gap:12px; flex-wrap:wrap; margin-top: 10px;}
    .card{
      background: linear-gradient(180deg, rgba(255,255,255,.05), rgba(255,255,255,.02));
      border: 1px solid var(--border);
      border-radius: var(--radius);
      box-shadow: var(--shadow);
    }
    .card.pad{padding: 18px;}
    .mini{
      display:grid; gap:10px;
    }
    .mini .row{
      display:flex; gap:10px; align-items:flex-start;
      padding: 12px;
      border-radius: 14px;
      background: rgba(255,255,255,.03);
      border: 1px solid rgba(255,255,255,.06);
    }
    .check{
      width: 18px; height: 18px; border-radius: 6px;
      background: rgba(64,211,156,.18);
      border: 1px solid rgba(64,211,156,.28);
      display:flex; align-items:center; justify-content:center;
      flex: 0 0 auto;
      margin-top: 2px;
    }
    .check svg{width:14px;height:14px; fill: var(--ok);}
    .row strong{display:block; font-size: 14px;}
    .row span{display:block; color: var(--muted2); font-size: 13px; margin-top: 2px;}
    section{padding: 26px 0;}
    .section-title{
      font-size: 26px;
      letter-spacing: -.4px;
      margin: 0 0 10px;
    }
    .section-sub{
      color: var(--muted);
      margin: 0 0 16px;
      max-width: 80ch;
    }
    .cols-2{
      display:grid; grid-template-columns: 1fr 1fr; gap: 18px;
    }
    @media(max-width: 900px){ .cols-2{grid-template-columns: 1fr;} }
    .pill{
      display:inline-flex; align-items:center; gap:8px;
      padding: 8px 10px;
      border-radius: 999px;
      border: 1px solid rgba(255,255,255,.08);
      background: rgba(255,255,255,.03);
      color: var(--muted);
      font-weight:700;
      font-size: 13px;
    }
    .list{
      margin: 12px 0 0; padding: 0; list-style:none;
      display:grid; gap:10px;
    }
    .list li{
      padding: 12px;
      border-radius: 14px;
      border: 1px solid rgba(255,255,255,.07);
      background: rgba(255,255,255,.03);
      color: var(--muted);
    }
    .list li b{color: var(--text);}
    .pricing{
      display:grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 16px;
    }
    @media(max-width: 980px){ .pricing{grid-template-columns:1fr;} }
    .price-card{padding: 18px;}
    .price-top{display:flex; align-items:flex-start; justify-content:space-between; gap: 12px;}
    .price-name{font-weight: 800; font-size: 18px; letter-spacing:-.2px;}
    .price-tag{
      font-weight: 900;
      font-size: 14px;
      color: #061022;
      background: linear-gradient(135deg, rgba(110,168,255,.95), rgba(141,123,255,.95));
      border-radius: 999px;
      padding: 8px 10px;
      white-space: nowrap;
    }
    .price-desc{color: var(--muted); margin: 10px 0 12px;}
    .divider{height:1px; background: rgba(255,255,255,.08); margin: 14px 0;}
    .muted-note{color: var(--muted2); font-size: 13px;}
    .how{
      display:grid; grid-template-columns: 1fr 1fr 1fr; gap: 14px;
    }
    @media(max-width: 980px){ .how{grid-template-columns:1fr;} }
    .step{padding: 16px;}
    .step .n{
      display:inline-flex; width: 30px; height: 30px; border-radius: 12px;
      align-items:center; justify-content:center;
      background: rgba(110,168,255,.14);
      border: 1px solid rgba(110,168,255,.22);
      font-weight: 900;
      color: var(--brand);
    }
    .step h3{margin: 10px 0 6px; font-size: 16px;}
    .step p{margin:0; color: var(--muted); font-size: 14px;}
    .rules{margin-top: 14px;}
    .rules .list li{color: var(--muted2);}
    .proof{
      display:grid; grid-template-columns: 1.1fr .9fr; gap: 16px;
      align-items:start;
    }
    @media(max-width: 980px){ .proof{grid-template-columns:1fr;} }
    blockquote{
      margin: 0;
      padding: 16px;
      border-radius: 16px;
      border: 1px solid rgba(255,255,255,.08);
      background: rgba(255,255,255,.03);
      color: var(--muted);
    }
    blockquote b{color: var(--text);}
    .case{
      padding: 16px;
      border-radius: 16px;
      border: 1px solid rgba(255,255,255,.08);
      background: rgba(255,255,255,.03);
      color: var(--muted);
    }
    .case .row2{display:grid; gap:10px; margin-top: 10px;}
    .case .tag{font-weight:900; color: var(--text);}
    .form{
      display:grid; grid-template-columns: 1fr 1fr; gap: 12px;
    }
    @media(max-width: 720px){ .form{grid-template-columns:1fr;} }
    label{display:grid; gap:6px; color: var(--muted2); font-size: 13px; font-weight:700;}
    input, select, textarea{
      background: rgba(255,255,255,.04);
      border: 1px solid rgba(255,255,255,.10);
      border-radius: 14px;
      padding: 12px 12px;
      color: var(--text);
      font-size: 14px;
      outline:none;
    }
    textarea{min-height: 110px; resize: vertical;}
    input:focus, select:focus, textarea:focus{
      border-color: rgba(110,168,255,.45);
      box-shadow: 0 0 0 4px rgba(110,168,255,.12);
    }
    .form-actions{display:flex; gap:12px; flex-wrap:wrap; margin-top: 12px;}
    footer{
      padding: 30px 0 40px;
      color: var(--muted2);
      border-top: 1px solid rgba(255,255,255,.08);
      margin-top: 20px;
    }
    .tiny{font-size: 12px; color: var(--muted2);}
    .badge-row{display:flex; gap:10px; flex-wrap:wrap; margin-top: 10px;}
  </style>
</head>

<body>
  <div class="topbar">
    <div class="wrap">
      <a class="brand" href="#top" aria-label="Visea Home">
        <div class="logo"></div>
        <div>Visea</div>
      </a>

      <nav aria-label="Primary navigation">
        <a href="#services">What we handle</a>
        <a href="#how">How it works</a>
        <a href="#pricing">Packages</a>
        <a href="#proof">Proof</a>
        <a href="#book">Book a call</a>
      </nav>

      <a class="btn primary small" href="#book">Book a 15-Min Fit Call</a>
    </div>
  </div>

  <main id="top" class="wrap">
    <!-- HERO -->
    <header class="hero">
      <div class="grid">
        <div>
          <div class="h-eyebrow"><span class="dot"></span> AI-powered • Human-led • Executive support</div>
          <h1>Get 10+ hours back every week — without dropping balls.</h1>
          <p class="lead">
            Visea runs your inbox, calendar, and follow-through with experienced U.S.-based assistants and smart automation
            so you can stay focused on strategy.
          </p>

          <div class="badge-row">
            <span class="pill">Remote-first</span>
            <span class="pill">Tech-enabled</span>
            <span class="pill">Proactive support</span>
            <span class="pill">48–72 hour setup</span>
          </div>

          <div class="cta-row">
            <a class="btn primary" href="#book">Book a 15-Min Fit Call</a>
            <a class="btn ghost" href="#pricing">See Packages</a>
          </div>

          <p class="tiny" style="margin-top:10px;">
            This isn’t about replacing people with AI. It’s about supercharging great people with AI.
          </p>
        </div>

        <aside class="card pad">
          <div class="mini" aria-label="Key outcomes">
            <div class="row">
              <div class="check" aria-hidden="true">
                <svg viewBox="0 0 24 24"><path d="M9.0 16.2 4.8 12l-1.4 1.4L9 19 21 7l-1.4-1.4z"/></svg>
              </div>
              <div>
                <strong>Inbox handled daily</strong>
                <span>Triage, drafts, follow-ups, escalation rules.</span>
              </div>
            </div>
            <div class="row">
              <div class="check" aria-hidden="true">
                <svg viewBox="0 0 24 24"><path d="M9.0 16.2 4.8 12l-1.4 1.4L9 19 21 7l-1.4-1.4z"/></svg>
              </div>
              <div>
                <strong>Calendar under control</strong>
                <span>Scheduling, buffers, confirmations, reschedules.</span>
              </div>
            </div>
            <div class="row">
              <div class="check" aria-hidden="true">
                <svg viewBox="0 0 24 24"><path d="M9.0 16.2 4.8 12l-1.4 1.4L9 19 21 7l-1.4-1.4z"/></svg>
              </div>
              <div>
                <strong>Nothing slips</strong>
                <span>Tasks tracked, owners assigned, follow-through enforced.</span>
              </div>
            </div>
            <div class="row">
              <div class="check" aria-hidden="true">
                <svg viewBox="0 0 24 24"><path d="M9.0 16.2 4.8 12l-1.4 1.4L9 19 21 7l-1.4-1.4z"/></svg>
              </div>
              <div>
                <strong>48–72 hour setup</strong>
                <span>Quick wins first. Deeper systems next.</span>
              </div>
            </div>
          </div>
        </aside>
      </div>
    </header>

    <!-- PROBLEM / SOLUTION -->
    <section id="about">
      <h2 class="section-title">Executives don’t need “more tools.” They need fewer fires.</h2>
      <p class="section-sub">
        The hidden tax of leadership isn’t lack of talent — it’s logistics: inbox triage, calendar chaos, follow-ups,
        vendor coordination, travel, and projects that stall because no one owns the details.
      </p>

      <div class="cols-2">
        <div class="card pad">
          <span class="pill">The problem</span>
          <ul class="list">
            <li><b>Inbox overload</b> → important requests get buried</li>
            <li><b>Calendar ping-pong</b> → reschedules and time leaks</li>
            <li><b>Follow-ups slip</b> → revenue and relationships quietly bleed</li>
            <li><b>Ops clutter</b> → tasks scattered across too many places</li>
          </ul>
        </div>

        <div class="card pad">
          <span class="pill">The Visea solution</span>
          <ul class="list">
            <li><b>Human-led support</b> from experienced U.S.-based assistants</li>
            <li><b>AI + automation</b> to speed execution and reduce errors</li>
            <li><b>Proactive follow-through</b> so nothing stalls or disappears</li>
            <li><b>Integrated workflows</b> inside your existing tools</li>
          </ul>
        </div>
      </div>
    </section>

    <!-- SERVICES -->
    <section id="services">
      <h2 class="section-title">What we handle</h2>
      <p class="section-sub">Organized by executive outcomes — not random task lists.</p>

      <div class="cols-2">
        <div class="card pad">
          <h3 style="margin:0 0 8px;">Inbox & Communication</h3>
          <ul class="list">
            <li>Inbox triage, drafting, escalation rules</li>
            <li>Follow-ups, reminders, “nothing falls through” tracking</li>
            <li>Client/vendor coordination support</li>
          </ul>
        </div>

        <div class="card pad">
          <h3 style="margin:0 0 8px;">Calendar & Meetings</h3>
          <ul class="list">
            <li>Scheduling, confirmations, reschedules</li>
            <li>Agenda prep, meeting notes → action items</li>
            <li>Calendar protection (buffers, focus blocks, travel time)</li>
          </ul>
        </div>

        <div class="card pad">
          <h3 style="margin:0 0 8px;">Operations & Coordination</h3>
          <ul class="list">
            <li>Vendor coordination + quotes + bookings</li>
            <li>Simple project tracking + weekly status updates</li>
            <li>SOPs for recurring workflows</li>
          </ul>
        </div>

        <div class="card pad">
          <h3 style="margin:0 0 8px;">Travel & Logistics</h3>
          <ul class="list">
            <li>Flights/hotels/itineraries</li>
            <li>Confirmations + calendar integration</li>
            <li>Receipts and travel docs organized</li>
          </ul>
          <p class="muted-note" style="margin-top:12px;">
            Personal admin is available as an option (only if you want it).
          </p>
        </div>
      </div>
    </section>

    <!-- HOW IT WORKS -->
    <section id="how">
      <h2 class="section-title">How it works</h2>
      <p class="section-sub">Simple rhythm. Clear ownership. No babysitting required.</p>

      <div class="how">
        <div class="card step">
          <div class="n">1</div>
          <h3>Fit Call (15 minutes)</h3>
          <p>We confirm priorities, tools, and success metrics. If we’re not a fit, we’ll tell you.</p>
        </div>

        <div class="card step">
          <div class="n">2</div>
          <h3>Setup (48–72 hours)</h3>
          <p>We integrate into your workflow, set communication rules, and implement quick wins fast.</p>
        </div>

        <div class="card step">
          <div class="n">3</div>
          <h3>Weekly rhythm</h3>
          <p>Proactive execution + follow-through. You get a weekly recap so you always know what’s handled.</p>
        </div>
      </div>

      <div class="rules card pad">
        <span class="pill">Rules of engagement</span>
        <ul class="list">
          <li>One primary communication channel (Slack or Email)</li>
          <li>Clear escalation rules for urgent items</li>
          <li>Weekly “top priorities” message from you (or your operator)</li>
        </ul>
      </div>
    </section>

    <!-- PRICING -->
    <section id="pricing">
      <h2 class="section-title">Packages</h2>
      <p class="section-sub">Clear tiers. “Starting at” pricing. Scope confirmed on the fit call.</p>

      <div class="pricing">
        <div class="card price-card">
          <div class="price-top">
            <div>
              <div class="price-name">Executive Lite</div>
              <div class="muted-note">Dependable daily support.</div>
            </div>
            <div class="price-tag">Starting at $1,500/mo</div>
          </div>
          <p class="price-desc">Best for leaders who need inbox, calendar, and follow-through handled consistently.</p>
          <div class="divider"></div>
          <ul class="list">
            <li>Inbox triage + draft replies</li>
            <li>Calendar scheduling + confirmations</li>
            <li>Follow-up tracking (nothing slips)</li>
            <li>Basic travel booking support</li>
            <li>Weekly priorities check-in</li>
          </ul>
          <div class="form-actions">
            <a class="btn primary" href="#book">Book a Fit Call</a>
          </div>
        </div>

        <div class="card price-card" style="border-color: rgba(110,168,255,.25);">
          <div class="price-top">
            <div>
              <div class="price-name">Executive Plus</div>
              <div class="muted-note">More moving parts. Faster response.</div>
            </div>
            <div class="price-tag">Starting at $3,000/mo</div>
          </div>
          <p class="price-desc">Best for executives who want stronger coordination and meeting support.</p>
          <div class="divider"></div>
          <ul class="list">
            <li>Everything in Lite</li>
            <li>Meeting prep + notes → action items</li>
            <li>Vendor/client coordination</li>
            <li>SOPs + workflow streamlining</li>
            <li><b>Response-time SLA:</b> under 2 business hours</li>
          </ul>
          <div class="form-actions">
            <a class="btn primary" href="#book">Book a Fit Call</a>
          </div>
        </div>

        <div class="card price-card">
          <div class="price-top">
            <div>
              <div class="price-name">Chief-of-Staff Assist</div>
              <div class="muted-note">Proactive operations support.</div>
            </div>
            <div class="price-tag">Starting at $6,000/mo</div>
          </div>
          <p class="price-desc">Best for leaders who want ownership, reporting, and cross-functional follow-through.</p>
          <div class="divider"></div>
          <ul class="list">
            <li>Everything in Plus</li>
            <li>Project coordination + weekly reporting</li>
            <li>Team coordination + accountability nudges</li>
            <li>Cross-functional follow-through</li>
            <li>Weekly executive brief (wins, risks, next actions)</li>
          </ul>
          <div class="form-actions">
            <a class="btn primary" href="#book">Book a Fit Call</a>
          </div>
        </div>
      </div>

      <div class="card pad" style="margin-top: 16px;">
        <div style="display:flex; gap:12px; flex-wrap:wrap; align-items:center; justify-content:space-between;">
          <div>
            <div class="price-name" style="font-size:16px;">Optional Add-on: AI Ops</div>
            <div class="muted-note">+ $300–$1,500/mo (based on automation depth)</div>
          </div>
          <a class="btn ghost" href="#book">Ask about AI Ops</a>
        </div>
        <ul class="list" style="margin-top:12px;">
          <li>Inbox drafting + smart triage rules</li>
          <li>Meeting summaries → tasks</li>
          <li>Follow-up nudges + reminders</li>
          <li>Weekly executive brief automation</li>
        </ul>
        <p class="muted-note" style="margin-top:12px;">
          Final pricing depends on volume, complexity, and your tool stack. We confirm scope on the fit call.
        </p>
      </div>
    </section>

    <!-- PROOF -->
    <section id="proof">
      <h2 class="section-title">Proof (add yours here)</h2>
      <p class="section-sub">Start with 2–3 short testimonials and one mini case study. Keep it punchy.</p>

      <div class="proof">
        <div class="card pad">
          <h3 style="margin:0 0 10px;">Testimonials</h3>

          <blockquote>
            “Before Visea, I was missing follow-ups and living in my inbox. Now my calendar runs smoothly and I finally feel on top of things.”
            <div style="margin-top:10px; color:var(--muted2); font-weight:700;">— Name, Role/Company</div>
          </blockquote>

          <div style="height:12px;"></div>

          <blockquote>
            “They’re proactive — things get handled before I even think about them.”
            <div style="margin-top:10px; color:var(--muted2); font-weight:700;">— Name, Role/Company</div>
          </blockquote>
        </div>

        <div class="card pad">
          <h3 style="margin:0 0 10px;">48-hour quick wins</h3>
          <ul class="list">
            <li>Inbox rules + VIP filters + reply templates</li>
            <li>Calendar cleanup + scheduling system + meeting buffers</li>
            <li>Follow-up tracker so nothing slips</li>
            <li>Meeting notes → action items → reminders</li>
          </ul>

          <div style="height:14px;"></div>

          <div class="case">
            <div class="tag">Before → After (template)</div>
            <div class="row2">
              <div><b>Before:</b> Inbox backlog, scheduling chaos, follow-ups slipping</div>
              <div><b>After (14 days):</b> Inbox handled daily, booking system installed, weekly priority recap</div>
              <div><b>Result:</b> X hours saved/week + fewer missed opportunities</div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- FOUNDER NOTE + QUALIFICATION -->
    <section id="fit">
      <div class="card pad">
        <h2 class="section-title" style="margin-bottom:6px;">Built for founders, executives, and operators who move fast.</h2>
        <p class="section-sub" style="margin-bottom:10px;">
          Visea exists because modern leaders deserve support that’s proactive, integrated, and built for today’s workflows.
          If you’re juggling too much, we’ll help you get your time back — quickly and cleanly.
        </p>
        <p class="muted-note">
          Not for: anyone looking for a low-cost task doer with no systems. (We’re calm, but we’re not cheap.)
        </p>
      </div>
    </section>

    <!-- BOOK / FORM -->
    <section id="book">
      <h2 class="section-title">Book a 15-minute fit call</h2>
      <p class="section-sub">Fast call. Clear next steps. If we’re not a fit, we’ll tell you quickly.</p>

      <div class="card pad">
        <!--
          ✅ OPTION A (recommended): Replace the form with your Calendly embed.
          ✅ OPTION B: Keep this form and connect it to Formspree / Basin / Web3Forms, etc.

          To use Formspree:
          1) Create a form endpoint and replace ACTION_URL below.
          2) Set method="POST".
        -->
        <form id="intakeForm" action="ACTION_URL" method="POST">
          <div class="form">
            <label>
              Name
              <input name="name" type="text" placeholder="Your name" required />
            </label>

            <label>
              Email
              <input name="email" type="email" placeholder="you@company.com" required />
            </label>

            <label>
              Role / Title
              <input name="role" type="text" placeholder="Founder, CEO, COO, Operator…" required />
            </label>

            <label>
              Company + website
              <input name="company" type="text" placeholder="Company name + URL" required />
            </label>

            <label>
              Biggest pain (pick one)
              <select name="pain_primary" required>
                <option value="" disabled selected>Select one</option>
                <option>Inbox</option>
                <option>Calendar</option>
                <option>Follow-ups</option>
                <option>Meeting support</option>
                <option>Ops coordination</option>
                <option>Travel</option>
              </select>
            </label>

            <label>
              Secondary pain (optional)
              <select name="pain_secondary">
                <option value="" selected>Optional</option>
                <option>Inbox</option>
                <option>Calendar</option>
                <option>Follow-ups</option>
                <option>Meeting support</option>
                <option>Ops coordination</option>
                <option>Travel</option>
              </select>
            </label>

            <label>
              Email volume/day
              <select name="email_volume" required>
                <option value="" disabled selected>Select one</option>
                <option>0–50</option>
                <option>50–150</option>
                <option>150+</option>
              </select>
            </label>

            <label>
              Meetings/week
              <select name="meetings_per_week" required>
                <option value="" disabled selected>Select one</option>
                <option>0–5</option>
                <option>6–15</option>
                <option>16+</option>
              </select>
            </label>

            <label>
              Tools you use (comma-separated)
              <input name="tools" type="text" placeholder="Google/Outlook, Slack/Teams, ClickUp/Asana/Notion…" />
            </label>

            <label>
              When do you want support to start?
              <select name="start_timing" required>
                <option value="" disabled selected>Select one</option>
                <option>ASAP</option>
                <option>Within 2 weeks</option>
                <option>This quarter</option>
              </select>
            </label>

            <label>
              Budget range
              <select name="budget_range" required>
                <option value="" disabled selected>Select one</option>
                <option>$1.5k–$3k</option>
                <option>$3k–$6k</option>
                <option>$6k+</option>
              </select>
            </label>

            <label>
              What would make this an immediate win in the first 7 days?
              <textarea name="win_7_days" placeholder="Example: ‘Inbox back to zero daily’ or ‘No more scheduling ping-pong.’"></textarea>
            </label>
          </div>

          <div class="form-actions">
            <button class="btn primary" type="submit">Submit & Request Call</button>
            <a class="btn ghost" href="#pricing">Review packages</a>
          </div>

          <p class="tiny" style="margin-top:10px;">
            Prefer to book directly? Add your Calendly link here: <b>Replace ACTION_URL</b> or embed Calendly below.
          </p>
        </form>

        <!-- Calendly embed placeholder (optional)
        <div style="margin-top:16px;">
          <div class="card pad" style="background: rgba(255,255,255,.02);">
            <p class="muted-note">Calendly embed goes here.</p>
          </div>
        </div>
        -->
      </div>
    </section>

    <footer>
      <div class="wrap" style="padding:0;">
        <div style="display:flex; gap:12px; flex-wrap:wrap; align-items:center; justify-content:space-between;">
          <div><b>Visea</b> — AI-powered, human-led executive assistance.</div>
          <div class="tiny">© <span id="year"></span> Visea. All rights reserved.</div>
        </div>
        <div class="tiny" style="margin-top:10px;">
          Remote-first • U.S.-based assistants • Built for modern leaders
        </div>
      </div>
    </footer>
  </main>

  <script>
    // Set year in footer
    document.getElementById("year").textContent = new Date().getFullYear();

    // Optional: if you don't have a form backend yet, prevent accidental "dead submit"
    const form = document.getElementById("intakeForm");
    form.addEventListener("submit", (e) => {
      const action = form.getAttribute("action") || "";
      if (action === "ACTION_URL") {
        e.preventDefault();
        alert("Quick fix needed: replace ACTION_URL with your form endpoint (Formspree/Basin/Web3Forms) or embed Calendly.");
      }
    });
  </script>
</body>
</html>
