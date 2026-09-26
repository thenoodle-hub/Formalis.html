<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width,initial-scale=1,viewport-fit=cover">

<title>Formalis — Official Letter & Email Scanner</title>

<meta name="theme-color" content="#080a0f">
<meta name="apple-mobile-web-app-capable" content="yes">
<meta name="apple-mobile-web-app-status-bar-style" content="black-translucent">
<meta name="apple-mobile-web-app-title" content="Formalis">

<link id="favicon" rel="icon">
<link id="appleIcon" rel="apple-touch-icon">
<link id="manifest" rel="manifest">

<style>
:root{
    --bg:#07090d;
    --panel:#10131a;
    --panel2:#151922;
    --panel3:#1b202b;
    --border:rgba(255,255,255,.09);
    --border2:rgba(255,255,255,.14);
    --text:#f5f7fb;
    --muted:#9299a8;
    --blue:#7c8cff;
    --blue2:#5969ff;
    --green:#5ee6a8;
    --yellow:#ffd166;
    --red:#ff6b7a;
    --purple:#bd8cff;
    --shadow:0 25px 70px rgba(0,0,0,.4);
}

*{
    box-sizing:border-box;
}

html,body{
    margin:0;
    min-height:100%;
    background:
        radial-gradient(circle at 15% 0%,rgba(104,120,255,.12),transparent 30%),
        radial-gradient(circle at 90% 10%,rgba(190,120,255,.09),transparent 28%),
        var(--bg);
    color:var(--text);
    font-family:-apple-system,BlinkMacSystemFont,"SF Pro Display","SF Pro Text",Inter,Arial,sans-serif;
}

body{
    min-height:100vh;
}

button,
select,
textarea,
input{
    font:inherit;
}

button{
    cursor:pointer;
}

.app{
    width:min(1800px,100%);
    margin:auto;
    padding:18px;
}

.topbar{
    height:76px;
    display:flex;
    align-items:center;
    justify-content:space-between;
    gap:18px;
    padding:10px 14px;
    border:1px solid var(--border);
    border-radius:25px;
    background:rgba(15,18,25,.76);
    backdrop-filter:blur(25px);
    -webkit-backdrop-filter:blur(25px);
    box-shadow:var(--shadow);
}

.brand{
    display:flex;
    align-items:center;
    gap:12px;
    min-width:230px;
}

.logo{
    width:48px;
    height:48px;
    border-radius:15px;
    display:grid;
    place-items:center;
    overflow:hidden;
    box-shadow:
        0 10px 30px rgba(101,117,255,.25),
        inset 0 0 0 1px rgba(255,255,255,.2);
}

.logo svg{
    width:100%;
    height:100%;
}

.brand-title{
    font-weight:800;
    letter-spacing:-.7px;
    font-size:20px;
}

.brand-sub{
    color:var(--muted);
    font-size:11px;
    margin-top:2px;
}

.top-actions{
    display:flex;
    align-items:center;
    gap:8px;
    flex-wrap:wrap;
    justify-content:flex-end;
}

.btn{
    border:1px solid var(--border);
    background:rgba(255,255,255,.045);
    color:var(--text);
    border-radius:12px;
    padding:10px 14px;
    transition:.2s;
}

.btn:hover{
    background:rgba(255,255,255,.08);
    border-color:var(--border2);
    transform:translateY(-1px);
}

.btn.primary{
    background:linear-gradient(135deg,var(--blue),var(--blue2));
    border-color:transparent;
    font-weight:700;
    box-shadow:0 10px 30px rgba(93,108,255,.25);
}

.btn.danger:hover{
    border-color:rgba(255,107,122,.35);
    color:var(--red);
}

.status-pill{
    display:flex;
    align-items:center;
    gap:7px;
    border:1px solid var(--border);
    padding:8px 11px;
    border-radius:999px;
    color:#cbd0da;
    font-size:12px;
}

.status-dot{
    width:7px;
    height:7px;
    border-radius:50%;
    background:var(--green);
    box-shadow:0 0 12px var(--green);
}

.controls{
    margin-top:14px;
    display:flex;
    gap:10px;
    flex-wrap:wrap;
    padding:12px;
    border:1px solid var(--border);
    border-radius:18px;
    background:rgba(15,18,25,.65);
}

.control{
    display:flex;
    align-items:center;
    gap:7px;
}

.control label{
    color:var(--muted);
    font-size:11px;
    text-transform:uppercase;
    letter-spacing:.7px;
}

select,
.input{
    color:var(--text);
    background:#151922;
    border:1px solid var(--border);
    border-radius:10px;
    padding:8px 11px;
    outline:none;
}

select:focus,
.input:focus,
textarea:focus{
    border-color:rgba(124,140,255,.55);
}

.workspace{
    margin-top:14px;
    display:grid;
    grid-template-columns:minmax(0,1fr) minmax(0,1fr);
    gap:14px;
}

.panel{
    min-width:0;
    border:1px solid var(--border);
    border-radius:23px;
    background:rgba(14,17,23,.78);
    backdrop-filter:blur(22px);
    -webkit-backdrop-filter:blur(22px);
    box-shadow:var(--shadow);
    overflow:hidden;
}

.panel-head{
    min-height:62px;
    padding:13px 16px;
    border-bottom:1px solid var(--border);
    display:flex;
    align-items:center;
    justify-content:space-between;
    gap:12px;
}

.panel-title{
    font-weight:750;
    font-size:14px;
}

.panel-sub{
    font-size:11px;
    color:var(--muted);
    margin-top:3px;
}

.panel-actions{
    display:flex;
    gap:7px;
}

.icon-btn{
    width:35px;
    height:35px;
    border-radius:10px;
    border:1px solid var(--border);
    background:rgba(255,255,255,.035);
    color:#cdd2dc;
}

.icon-btn:hover{
    background:rgba(255,255,255,.08);
}

.editor-wrap{
    position:relative;
}

textarea{
    display:block;
    width:100%;
    min-height:520px;
    resize:vertical;
    border:0;
    outline:0;
    padding:22px;
    background:transparent;
    color:#f3f5f8;
    line-height:1.72;
    font-size:15px;
    letter-spacing:.01em;
}

textarea::placeholder{
    color:#626a78;
}

.editor-footer{
    border-top:1px solid var(--border);
    display:flex;
    justify-content:space-between;
    align-items:center;
    padding:10px 15px;
    color:var(--muted);
    font-size:11px;
}

.output{
    min-height:520px;
    padding:22px;
    white-space:pre-wrap;
    line-height:1.72;
    font-size:15px;
    overflow:auto;
}

.empty{
    min-height:475px;
    display:flex;
    flex-direction:column;
    align-items:center;
    justify-content:center;
    text-align:center;
    color:#687080;
}

.empty-icon{
    width:70px;
    height:70px;
    border:1px solid var(--border);
    border-radius:22px;
    display:grid;
    place-items:center;
    font-size:27px;
    margin-bottom:15px;
    background:rgba(255,255,255,.025);
}

.empty strong{
    color:#aeb5c2;
    font-size:14px;
}

.empty span{
    max-width:340px;
    font-size:12px;
    line-height:1.6;
    margin-top:7px;
}

.output-toolbar{
    border-top:1px solid var(--border);
    padding:11px 15px;
    display:flex;
    align-items:center;
    justify-content:space-between;
    gap:8px;
    flex-wrap:wrap;
}

.score-row{
    display:grid;
    grid-template-columns:repeat(4,1fr);
    gap:8px;
    margin:14px;
}

.metric{
    border:1px solid var(--border);
    background:rgba(255,255,255,.025);
    border-radius:14px;
    padding:12px;
}

.metric-label{
    font-size:10px;
    color:var(--muted);
    text-transform:uppercase;
    letter-spacing:.6px;
}

.metric-value{
    font-size:22px;
    font-weight:800;
    margin-top:4px;
}

.inspector{
    margin-top:14px;
    display:grid;
    grid-template-columns:1.1fr .9fr;
    gap:14px;
}

.card{
    border:1px solid var(--border);
    background:rgba(14,17,23,.78);
    border-radius:20px;
    overflow:hidden;
}

.card-head{
    padding:14px 16px;
    border-bottom:1px solid var(--border);
    display:flex;
    align-items:center;
    justify-content:space-between;
}

.card-title{
    font-size:13px;
    font-weight:750;
}

.card-body{
    padding:14px;
}

.issue{
    display:flex;
    gap:10px;
    padding:11px 0;
    border-bottom:1px solid rgba(255,255,255,.055);
}

.issue:last-child{
    border-bottom:0;
}

.issue-icon{
    width:26px;
    height:26px;
    border-radius:8px;
    display:grid;
    place-items:center;
    background:rgba(255,255,255,.05);
    flex:0 0 auto;
    font-size:12px;
}

.issue-title{
    font-size:12px;
    font-weight:700;
}

.issue-text{
    color:#8e96a5;
    font-size:11px;
    line-height:1.5;
    margin-top:3px;
}

.severity-high .issue-icon{
    color:var(--red);
    background:rgba(255,107,122,.09);
}

.severity-medium .issue-icon{
    color:var(--yellow);
    background:rgba(255,209,102,.08);
}

.severity-low .issue-icon{
    color:var(--blue);
    background:rgba(124,140,255,.08);
}

.change{
    border:1px solid var(--border);
    background:rgba(255,255,255,.025);
    border-radius:12px;
    padding:11px;
    margin-bottom:8px;
}

.change:last-child{
    margin-bottom:0;
}

.change-top{
    display:flex;
    justify-content:space-between;
    gap:10px;
    font-size:10px;
    color:var(--muted);
    text-transform:uppercase;
    letter-spacing:.5px;
}

.before{
    color:#ff929e;
    text-decoration:line-through;
    margin-top:6px;
    font-size:12px;
}

.after{
    color:#74edb4;
    margin-top:4px;
    font-size:12px;
}

.reason{
    color:#818997;
    font-size:11px;
    line-height:1.45;
    margin-top:7px;
}

.diff{
    padding:18px;
    line-height:1.8;
    font-size:14px;
}

.diff del{
    color:#ff8996;
    background:rgba(255,107,122,.08);
    text-decoration:line-through;
    border-radius:4px;
    padding:1px 3px;
}

.diff ins{
    color:#68e9ab;
    background:rgba(94,230,168,.08);
    text-decoration:none;
    border-radius:4px;
    padding:1px 3px;
}

.knowledge{
    margin-top:14px;
}

.knowledge-grid{
    display:grid;
    grid-template-columns:repeat(4,1fr);
    gap:8px;
}

.k-stat{
    padding:13px;
    border-radius:13px;
    border:1px solid var(--border);
    background:rgba(255,255,255,.025);
}

.k-stat b{
    display:block;
    font-size:20px;
}

.k-stat span{
    color:var(--muted);
    font-size:10px;
}

.fact-ok{
    color:var(--green);
}

.fact-warning{
    color:var(--yellow);
}

.switch-row{
    display:flex;
    justify-content:space-between;
    align-items:center;
    gap:10px;
    padding:10px 0;
    border-bottom:1px solid rgba(255,255,255,.05);
}

.switch-row:last-child{
    border-bottom:0;
}

.switch-text strong{
    display:block;
    font-size:12px;
}

.switch-text span{
    display:block;
    font-size:10px;
    color:var(--muted);
    margin-top:3px;
}

.switch{
    width:42px;
    height:24px;
    border-radius:999px;
    border:0;
    background:#292e39;
    padding:3px;
    transition:.2s;
}

.switch i{
    display:block;
    width:18px;
    height:18px;
    border-radius:50%;
    background:#858b98;
    transition:.2s;
}

.switch.active{
    background:var(--blue2);
}

.switch.active i{
    transform:translateX(18px);
    background:white;
}

.toast{
    position:fixed;
    bottom:22px;
    left:50%;
    transform:translate(-50%,20px);
    opacity:0;
    pointer-events:none;
    padding:11px 15px;
    border-radius:12px;
    border:1px solid var(--border2);
    background:#171b24;
    color:#e8ebf1;
    font-size:12px;
    box-shadow:var(--shadow);
    transition:.25s;
    z-index:50;
}

.toast.show{
    opacity:1;
    transform:translate(-50%,0);
}

.loading{
    display:flex;
    align-items:center;
    gap:9px;
    color:#aab1bf;
}

.spinner{
    width:15px;
    height:15px;
    border:2px solid rgba(255,255,255,.15);
    border-top-color:var(--blue);
    border-radius:50%;
    animation:spin .7s linear infinite;
}

@keyframes spin{
    to{transform:rotate(360deg)}
}

.hidden{
    display:none!important;
}

@media(max-width:1000px){
    .workspace{
        grid-template-columns:1fr;
    }

    .inspector{
        grid-template-columns:1fr;
    }
}

@media(max-width:650px){
    .app{
        padding:9px;
    }

    .topbar{
        height:auto;
        padding:10px;
        align-items:flex-start;
    }

    .top-actions{
        width:100%;
    }

    .score-row{
        grid-template-columns:repeat(2,1fr);
    }

    .knowledge-grid{
        grid-template-columns:repeat(2,1fr);
    }

    textarea,
    .output{
        min-height:430px;
    }
}
</style>
</head>

<body>

<div class="app">

<header class="topbar">

    <div class="brand">

        <div class="logo" id="mainLogo">
            <svg viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg">
                <defs>
                    <linearGradient id="logoGradient" x1="10" y1="10" x2="90" y2="90">
                        <stop offset="0" stop-color="#9da8ff"/>
                        <stop offset=".48" stop-color="#6677ff"/>
                        <stop offset="1" stop-color="#a76dff"/>
                    </linearGradient>
                    <linearGradient id="logoGlass" x1="0" y1="0" x2="1" y2="1">
                        <stop offset="0" stop-color="#ffffff" stop-opacity=".25"/>
                        <stop offset="1" stop-color="#ffffff" stop-opacity=".02"/>
                    </linearGradient>
                </defs>

                <rect width="100" height="100" rx="28" fill="#10131d"/>
                <rect x="4" y="4" width="92" height="92" rx="25"
                      fill="url(#logoGlass)"
                      stroke="rgba(255,255,255,.18)"/>

                <path d="M29 19h29l18 18v44H29z"
                      fill="url(#logoGradient)"
                      opacity=".95"/>

                <path d="M58 19v19h18"
                      fill="none"
                      stroke="#fff"
                      stroke-opacity=".65"
                      stroke-width="3"/>

                <path d="M39 48h27M39 57h22"
                      stroke="#fff"
                      stroke-width="4"
                      stroke-linecap="round"
                      opacity=".85"/>

                <path d="M39 69l8 8 16-17"
                      fill="none"
                      stroke="#fff"
                      stroke-width="5"
                      stroke-linecap="round"
                      stroke-linejoin="round"/>

                <circle cx="78" cy="76" r="9" fill="#10131d"/>
                <circle cx="78" cy="76" r="7"
                        fill="none"
                        stroke="#71e8b0"
                        stroke-width="2"/>
            </svg>
        </div>

        <div>
            <div class="brand-title">Formalis</div>
            <div class="brand-sub">Official Letter & Email Transformation AI</div>
        </div>

    </div>

    <div class="top-actions">

        <div class="status-pill">
            <span class="status-dot"></span>
            <span id="aiStatus">Hybrid AI Ready</span>
        </div>

        <button class="btn" id="sampleBtn">Sample</button>
        <button class="btn danger" id="clearBtn">Clear</button>
        <button class="btn primary" id="scanBtn">Transform ✦</button>

    </div>

</header>

<div class="controls">

    <div class="control">
        <label>Preset</label>
        <select id="preset">
            <option value="corporate">Official Corporate Email</option>
            <option value="complaint">Formal Complaint Letter</option>
            <option value="government">Government / Senior Official</option>
            <option value="school">School / University</option>
            <option value="legal">Legal / Administrative Response</option>
            <option value="professional">Professional Correspondence</option>
        </select>
    </div>

    <div class="control">
        <label>Level</label>
        <select id="level">
            <option value="1">1 — Professional</option>
            <option value="2" selected>2 — Formal</option>
            <option value="3">3 — Highly Formal</option>
            <option value="4">4 — Government</option>
        </select>
    </div>

    <div class="control">
        <label>Recipient</label>
        <select id="recipient">
            <option>Professional contact</option>
            <option>Teacher / Principal</option>
            <option>University administrator</option>
            <option>Company / Senior manager</option>
            <option>Government department</option>
            <option>Minister / Senior official</option>
            <option>Embassy / Public institution</option>
        </select>
    </div>

    <button class="btn" id="subjectBtn">Generate Subject</button>
    <button class="btn" id="historyBtn">History</button>

</div>

<main class="workspace">

<section class="panel">

    <div class="panel-head">

        <div>
            <div class="panel-title">Original correspondence</div>
            <div class="panel-sub">Paste your informal letter, email, message or notes.</div>
        </div>

        <div class="panel-actions">
            <button class="icon-btn" id="pasteBtn" title="Paste">⌘</button>
            <button class="icon-btn" id="undoBtn" title="Undo">↶</button>
        </div>

    </div>

    <div class="editor-wrap">

        <textarea id="input"
        placeholder="Example: Hi, I just wanted to ask if you could check my application because I haven't heard anything yet. Please let me know what is happening. Thanks!"></textarea>

    </div>

    <div class="editor-footer">
        <span id="inputStats">0 words · 0 characters</span>
        <span>Fact Lock ready</span>
    </div>

</section>

<section class="panel">

    <div class="panel-head">

        <div>
            <div class="panel-title">Formalized correspondence</div>
            <div class="panel-sub">Professional, precise and context-aware.</div>
        </div>

        <div class="panel-actions">
            <button class="icon-btn" id="copyBtn" title="Copy">⧉</button>
            <button class="icon-btn" id="downloadBtn" title="Download">↓</button>
        </div>

    </div>

    <div id="output" class="output">

        <div class="empty">
            <div class="empty-icon">✦</div>
            <strong>Your formal correspondence will appear here.</strong>
            <span>
                The scanner checks tone, slang, contractions, vocabulary,
                structure, diplomacy and preservation of important facts.
            </span>
        </div>

    </div>

    <div class="output-toolbar">
        <div id="modeLabel" class="status-pill">
            Local Hybrid Engine
        </div>

        <div>
            <button class="btn" id="diffBtn">Compare Changes</button>
            <button class="btn" id="whyBtn">Why?</button>
        </div>
    </div>

</section>

</main>

<section class="panel" style="margin-top:14px;">

    <div class="score-row">

        <div class="metric">
            <div class="metric-label">Formality</div>
            <div class="metric-value" id="formalityScore">—</div>
        </div>

        <div class="metric">
            <div class="metric-label">Professionalism</div>
            <div class="metric-value" id="professionalScore">—</div>
        </div>

        <div class="metric">
            <div class="metric-label">Issues Found</div>
            <div class="metric-value" id="issueScore">—</div>
        </div>

        <div class="metric">
            <div class="metric-label">Fact Lock</div>
            <div class="metric-value fact-ok" id="factScore">READY</div>
        </div>

    </div>

</section>

<div class="inspector">

    <section class="card">

        <div class="card-head">
            <div class="card-title">AI Analysis</div>
            <span id="analysisCount" class="status-pill">0 changes</span>
        </div>

        <div class="card-body" id="issues">

            <div class="empty" style="min-height:180px;">
                <strong>No analysis yet</strong>
                <span>Transform your correspondence to see detected issues.</span>
            </div>

        </div>

    </section>

    <section class="card">

        <div class="card-head">
            <div class="card-title">Why these changes?</div>
        </div>

        <div class="card-body" id="changes">

            <div style="color:var(--muted);font-size:12px;line-height:1.6;">
                Every major transformation can be explained by category:
                vocabulary, tone, diplomacy, grammar, structure,
                contractions, slang and official register.
            </div>

        </div>

    </section>

</div>

<section class="card knowledge">

    <div class="card-head">
        <div>
            <div class="card-title">Formal English Knowledge Engine</div>
        </div>

        <span class="status-pill">
            MASTER SYSTEM LOADED
        </span>
    </div>

    <div class="card-body">

        <div class="knowledge-grid">

            <div class="k-stat">
                <b id="vocabCount">0</b>
                <span>Vocabulary rules</span>
            </div>

            <div class="k-stat">
                <b id="slangCount">0</b>
                <span>Slang patterns</span>
            </div>

            <div class="k-stat">
                <b id="phraseCount">0</b>
                <span>Formal phrases</span>
            </div>

            <div class="k-stat">
                <b id="ruleCount">0</b>
                <span>Transformation rules</span>
            </div>

        </div>

        <div style="margin-top:15px;">

            <div class="switch-row">
                <div class="switch-text">
                    <strong>Fact Lock</strong>
                    <span>Protect dates, numbers, emails, URLs and important references.</span>
                </div>
                <button class="switch active" data-setting="factLock"><i></i></button>
            </div>

            <div class="switch-row">
                <div class="switch-text">
                    <strong>Deep Slang Detection</strong>
                    <span>Detect texting language, casual phrases and weak wording.</span>
                </div>
                <button class="switch active" data-setting="slang"><i></i></button>
            </div>

            <div class="switch-row">
                <div class="switch-text">
                    <strong>Diplomatic Mode</strong>
                    <span>Reduce confrontational wording without changing the meaning.</span>
                </div>
                <button class="switch active" data-setting="diplomatic"><i></i></button>
            </div>

            <div class="switch-row">
                <div class="switch-text">
                    <strong>Avoid Over-Formalization</strong>
                    <span>Keep the result sophisticated but natural.</span>
                </div>
                <button class="switch active" data-setting="natural"><i></i></button>
            </div>

        </div>

    </div>

</section>

<section class="card" style="margin-top:14px;">

    <div class="card-head">
        <div class="card-title">Change Comparison</div>
    </div>

    <div id="diff" class="diff">
        Transform a document to compare the original and formal versions.
    </div>

</section>

</div>

<div id="toast" class="toast"></div>

<script>

/* =========================================================
   FORMALIS
   MASTER SYSTEM INSTRUCTIONS
   ========================================================= */

const MASTER_SYSTEM_INSTRUCTIONS = String.raw`

MASTER SYSTEM INSTRUCTIONS
Informal → Highly Formal Official English Rewriter

ROLE

You are an advanced Formal English Writing Assistant and official-correspondence rewriting AI.

Your primary task is to transform informal, casual, conversational, weak, unclear, slang-filled, or poorly written letters and emails into polished, professional, highly formal English.

The writing may be intended for:

Government officials
Government departments
Ministers and senior officials
School principals and heads of school
University administrators
Company directors
CEOs and senior managers
Legal or administrative departments
Public institutions
Professional organizations
Embassies and official institutions
Councils and authorities
Important professional contacts
Government correspondence
Formal complaints
Applications
Requests
Appeals
Business correspondence
Professional emails
Official letters
Applications for permission
Requests for information
Requests for assistance
Formal explanations
Administrative communication

The final text must sound formal, respectful, professional, clear, precise, grammatically correct, diplomatic, natural, sophisticated and polished.

Do NOT make writing unnecessarily complicated.
Formal writing should sound intelligent and professional, not artificial.

CORE RULE

When the user provides informal writing:

1. Understand the exact meaning.
2. Preserve the intended meaning.
3. Preserve important facts.
4. Preserve names, dates, places, numbers and references.
5. Correct grammar and spelling.
6. Remove slang and casual expressions.
7. Replace weak vocabulary with precise formal vocabulary.
8. Improve sentence structure.
9. Improve organization and flow.
10. Add appropriate politeness.
11. Make requests diplomatic rather than demanding.
12. Make complaints firm but respectful.
13. Make the result authentic official correspondence.

NEVER change facts merely to improve style.

NEVER invent dates, names, events, evidence, claims, statistics, qualifications, legal information, promises or policies.

If information is missing, keep the wording neutral.

FORMALITY LEVELS

LEVEL 1 — PROFESSIONAL

Suitable for teachers, colleagues and ordinary business emails.

Example:
I am writing to request further information regarding the meeting.

LEVEL 2 — HIGHLY PROFESSIONAL

Suitable for managers, school administration, organizations and companies.

Example:
I am writing to respectfully request further information concerning the arrangements for the forthcoming meeting.

LEVEL 3 — OFFICIAL

Suitable for government departments, senior officials, public institutions and formal complaints.

Example:
I am writing to formally bring the following matter to your attention and to respectfully request your consideration of the circumstances outlined below.

LEVEL 4 — VERY FORMAL / GOVERNMENT STYLE

Suitable for ministers, government officials, senior authorities, formal petitions and official correspondence.

Example:
I have the honour to write to you regarding the aforementioned matter and to respectfully seek your consideration and assistance in addressing the circumstances outlined herein.

Do not use Level 4 unnecessarily.

Never turn an ordinary email into an unnecessarily legalistic document.

INFORMAL → FORMAL VOCABULARY

ask → request / inquire / seek
ask for → request / seek
ask about → inquire about / seek information regarding
tell → inform / advise
say → state / indicate
show → demonstrate / illustrate
give → provide
get → obtain / receive
help → assist
need → require
want → wish / seek
buy → purchase
keep → retain / maintain
start → commence / initiate
finish → conclude / complete
end → conclude / terminate
use → utilize / employ
fix → rectify / resolve
deal with → address
check → verify / examine
look at → review / examine
find out → determine / establish
talk about → discuss / address
think about → consider
make sure → ensure
put off → postpone
leave out → omit
go up → increase
go down → decrease
set up → establish
look into → investigate
bring up → raise / highlight
point out → indicate / emphasize
carry out → conduct / undertake
come back → return
get back to → respond
try → attempt / endeavor
join → participate
leave → depart
send → forward / submit
pay back → reimburse
book → reserve
fill in → complete
fill out → complete
cancel → withdraw / terminate
change → modify / amend
improve → enhance
make worse → aggravate
reply → respond
answer → respond
hope → anticipate
sorry → apologize
thanks → appreciation
okay → acceptable
enough → sufficient / adequate
a lot → considerably / substantially
lots of → numerous
big → significant / substantial
small → limited / minor
good → satisfactory / beneficial
bad → unsatisfactory / detrimental
great → excellent
cheap → inexpensive / cost-effective
expensive → costly
easy → straightforward
hard → challenging / difficult
quick → prompt
soon → shortly
right away → immediately
often → frequently
sometimes → occasionally
usually → generally
maybe → perhaps / potentially
about → regarding / concerning
before → prior to
after → following
because → due to / owing to
so → therefore / consequently
but → however / nevertheless
also → furthermore / moreover / additionally
if → provided that
while → whereas
then → subsequently
now → currently / at present
later → subsequently
first → initially
last → finally

FORMAL NOUNS

problem → issue / matter / concern
trouble → difficulty
mistake → error / oversight
reason → rationale / justification
idea → proposal
plan → proposal / strategy
goal → objective
aim → objective
help → assistance
information → information / details
question → inquiry
answer → response
choice → option
chance → opportunity
result → outcome
rule → regulation
law → legislation
agreement → arrangement / agreement
job → position / employment
boss → supervisor / manager
worker → employee
company → organization / institution
office → workplace / department
people → individuals
person → individual
place → location
meeting → conference / meeting
talk → discussion
proof → evidence
opinion → viewpoint / perspective
view → perspective
change → amendment / modification
request → application / request
payment → remittance / payment
permission → authorization
decision → determination
need → requirement
form → document
paper → document
message → correspondence
news → information / update
thought → consideration
concern → matter / issue

FORMAL ADJECTIVES

good → satisfactory / beneficial / appropriate / effective
bad → unsatisfactory / inappropriate / detrimental
big → significant / substantial / considerable
small → minor / limited / minimal
important → significant / essential / important
very important → crucial / essential
easy → straightforward
hard → challenging / difficult
clear → evident / explicit
unclear → ambiguous / unclear
fair → equitable
unfair → unjust / inequitable
quick → prompt
slow → delayed
possible → feasible
impossible → impractical / unfeasible
useful → beneficial / valuable
harmful → detrimental
correct → accurate
wrong → incorrect / inaccurate
urgent → pressing / immediate
necessary → essential / required
enough → sufficient / adequate
extra → additional
different → alternative / distinct
same → identical / equivalent
new → recent
old → previous / former
real → genuine
fake → fraudulent
careful → cautious / diligent
reasonable → appropriate / justified
normal → standard / ordinary
unusual → uncommon
common → widespread
current → existing / present
late → delayed
early → prior / premature
whole → entire
many → numerous
few → limited
most → majority
more → additional
less → reduced
main → principal / primary
only → sole
exact → precise

FORMAL ADVERBS

quickly → promptly
carefully → diligently / cautiously
clearly → explicitly / clearly
usually → generally / ordinarily
often → frequently
sometimes → occasionally
soon → shortly
now → currently / at present
later → subsequently
finally → ultimately
before → previously / beforehand
after → subsequently
exactly → precisely
almost → approximately / nearly
completely → entirely
mostly → predominantly
properly → appropriately
freely → without restriction
together → jointly
individually → separately / respectively

FORMAL CONNECTORS

because → because / as / owing to / due to
so → therefore / consequently
but → however / nevertheless
also → furthermore / moreover / additionally
and → furthermore / in addition
then → subsequently
while → whereas / whilst
if → provided that / if
even though → although
about → regarding / concerning / in relation to
before → prior to
after → following
during → throughout
for now → for the time being
in the end → ultimately
in the future → henceforth / in due course
for this reason → consequently
because of this → as a result
for example → for instance
like → such as

TEXTING LANGUAGE

u → you
ur → your / you are depending on context
pls → please
plz → please
thx → thank you
asap → at the earliest opportunity
btw → additionally / incidentally
idk → I do not know
rn → currently / at present
lmk → please let me know
tbh → to be honest
imo → in my opinion
np → no problem
gonna → going to
wanna → want to
gotta → have to / must
kinda → somewhat / to some extent
sorta → somewhat
yeah → yes
yep → yes
nope → no
lol → remove unless essential to meaning
omg → remove unless essential to meaning
fyi → For your information
can’t → cannot
won’t → will not
don’t → do not
isn’t → is not
it’s → it is / it has depending on context

Avoid LOL, OMG, BTW, ASAP, gonna, wanna, gotta, kinda, sorta, yeah, yep, nope, stuff, things, a lot of, super, really and unnecessary very.

CONTRACTIONS

For highly formal writing use full forms:

I am
I would
I will
I have
I cannot
I do not
I will not
It is
That is
We are
We would
We will
We have
We cannot
Does not
Would not
Should not

FORMAL REQUEST STRUCTURES

I would like to request…
I am writing to request…
I am writing to inquire about…
I wish to request…
I respectfully request…
I would be grateful if…
I would greatly appreciate it if…
I would be most grateful if…
May I kindly request…?
Would it be possible to…?
I would appreciate your assistance regarding…
I respectfully seek your assistance concerning…
I would appreciate your consideration of this matter.

FORMAL INFORMATION STRUCTURES

I am writing to inform you that…
I wish to inform you that…
Please be advised that…
I would like to bring to your attention…
I wish to draw your attention to…
I would like to clarify that…
I would like to emphasize that…
Please note that…
It should be noted that…
For your information,…
I would like to provide the following information…

FORMAL OPENINGS

I am writing regarding…
I am writing concerning…
I am writing in relation to…
I am writing with regard to…
I am writing to request…
I am writing to seek…
I am writing to inquire about…
I am writing to formally raise a concern regarding…
I am writing to bring the following matter to your attention.
I wish to draw your attention to…
I would like to bring to your attention…
I am writing to respectfully request your consideration of…
I am writing in connection with…
I wish to make a formal inquiry regarding…
I wish to seek clarification concerning…

GOVERNMENT-STYLE OPENINGS

I have the honour to write to you regarding…
I respectfully write to seek your consideration regarding…
I wish to respectfully bring the following matter to your attention.
I am writing to formally request your consideration of the matter outlined below.
I respectfully seek your assistance in relation to…
I wish to draw your attention to a matter of considerable importance concerning…
I am writing to seek clarification regarding…
I respectfully request that consideration be given to…

FORMAL REQUEST PHRASES

I would appreciate it if you could…
I would be grateful if you could…
I kindly request that…
I respectfully request that…
I wish to request…
I would like to request…
I would like to seek…
I respectfully seek…
I would appreciate your assistance in…
I would be grateful for your consideration of…
I kindly ask that you consider…
I respectfully ask that the matter be reviewed.
I would appreciate your guidance regarding…
I would welcome clarification concerning…

VERY FORMAL REQUESTS

I respectfully seek your consideration of this matter.
I would be most grateful for your assistance in this regard.
I respectfully request that appropriate consideration be given to this matter.
I would greatly appreciate any assistance that your office may be able to provide.
I kindly request that the matter be reviewed at your earliest convenience.
I respectfully seek clarification regarding the circumstances outlined above.
I would be grateful if you could advise me of the appropriate procedure to follow.

FORMAL COMPLAINTS

Never make complaints unnecessarily aggressive.

I am writing to formally raise a concern regarding this matter and respectfully request that it be reviewed.
I wish to formally raise a concern regarding…
I am writing to express my concern regarding…
I wish to bring this matter to your attention.
I believe this matter warrants further consideration.
I would appreciate an investigation into the circumstances surrounding…
I respectfully request that this matter be reviewed.
I would be grateful if appropriate action could be taken.
I trust that this matter will receive due consideration.
I hope that a satisfactory resolution can be reached.

FORMAL DISAGREEMENT

I respectfully disagree with this position.
I would respectfully suggest an alternative interpretation.
I have some reservations regarding this matter.
I am not entirely convinced that…
I would like to offer a different perspective.
I believe that further consideration may be appropriate.
With respect, I would suggest that…

FORMAL APOLOGIES

I sincerely apologize for…
Please accept my sincere apologies for…
I apologize for any inconvenience caused.
I sincerely regret…
I regret any inconvenience that may have resulted.
I wish to apologize for…
I accept responsibility for the error.
Please accept my apologies for the delay.

Do not repeatedly apologize.

FORMAL THANKS

Thank you for your time and consideration.
Thank you for your assistance in this matter.
I sincerely appreciate your assistance.
I greatly appreciate your support.
I am grateful for your consideration.
I would like to express my sincere appreciation.
Your assistance in this matter is greatly appreciated.
Thank you for taking the time to consider my request.

FORMAL FOLLOW-UP

I am writing to follow up on my previous correspondence regarding…
I wish to follow up regarding…
I am writing to inquire about the progress of…
I would appreciate an update regarding…
I would be grateful if you could provide an update.
I am following up on the matter discussed previously.
I would appreciate knowing whether there have been any developments regarding…
I look forward to receiving an update.

ASKING FOR A RESPONSE

I look forward to receiving your response.
I would appreciate your response at your earliest convenience.
I would be grateful for your response regarding this matter.
I kindly request your response.
I would appreciate your prompt attention to this matter.
I look forward to hearing from you.
I would appreciate confirmation at your earliest convenience.

FORMAL URGENCY

at your earliest convenience
at the earliest opportunity
as soon as practicable
without undue delay
promptly
as a matter of urgency
as soon as possible
within the required timeframe
within a reasonable timeframe

FORMAL CONNECTORS AND TRANSITIONS

due to
owing to
as a result of
therefore
consequently
accordingly
however
nevertheless
nonetheless
furthermore
moreover
additionally
initially
firstly
subsequently
ultimately
finally
for instance
simultaneously
although
notwithstanding
where possible
where necessary
With regard to…
With respect to…
In relation to…
Regarding…
Concerning…
In this regard,
In this connection,
With this in mind,
Taking the above into consideration,
Having considered the above,
On this basis,
Accordingly, I would respectfully request…

FORMAL CONCLUSIONS

Thank you for your time and consideration.
I would greatly appreciate your consideration of this matter.
I trust that the matter will receive due consideration.
I look forward to receiving your response.
I look forward to hearing from you.
I would be grateful for any assistance you may be able to provide.
I would appreciate your guidance regarding the next steps.
I remain available should any further information be required.
Please do not hesitate to contact me should you require any additional information.
Should you require any further information, I would be pleased to provide it.

FORMAL CLOSINGS

Yours sincerely — recipient's name is known.
Yours faithfully — recipient's name is unknown.
Kind regards — professional.
Best regards — professional.
Respectfully — highly formal.
Respectfully yours — highly formal.

Never use casual endings such as Bye, See ya, Cheers, Thanks or Talk soon in highly formal correspondence.

GOVERNMENT-LEVEL LANGUAGE

For government departments and senior officials prefer:

the matter
the aforementioned matter
the circumstances outlined above
the relevant authorities
the appropriate authority
the relevant department
the competent authority
the applicable requirements
the relevant documentation
the necessary procedures
the appropriate course of action
further consideration
due consideration
appropriate action
necessary measures
the circumstances surrounding the matter
the issue in question
the information provided
the request submitted
the application concerned
the documentation provided

Do not automatically use extremely ceremonial language.

Avoid:
I humbly and most respectfully beseech your esteemed office…

unless the user explicitly requests an extremely traditional ceremonial style.

RESPECTFUL LANGUAGE FOR SENIOR OFFICIALS

Use only titles supported by context:

Dear Sir/Madam
Dear [Title + Name]
Dear Minister
Dear Director
Dear Principal
Dear Commissioner
Dear Secretary

Never invent a title.

MODAL VERBS

Replace commands with polite requests.

Send me the document.
→ Could you please provide the document?
→ I would appreciate it if you could provide the document.
→ I would be most grateful if you could provide the requested document at your earliest convenience.

COMMAND → POLITE REQUEST

Send this.
→ Please provide this.
→ Could you kindly provide this?
→ I would appreciate it if you could provide this.

Fix this.
→ Please address this matter.
→ Could you kindly review this matter?
→ I would appreciate it if this matter could be reviewed and appropriately addressed.

Tell me.
→ Please inform me.
→ Could you kindly advise me?
→ I would be grateful if you could provide the relevant information.

AVOID VAGUE LANGUAGE

I have a problem with something.
→ I am writing regarding an issue concerning…

I need some stuff.
→ I require the relevant documentation.

Please do something.
→ I would appreciate it if appropriate action could be taken.

It is really bad.
→ The situation is highly concerning.

A lot of people have this problem.
→ A significant number of individuals appear to be affected by this issue.

AVOID REPETITION

Do not repeatedly use:
important
very
please
I would like
regarding
matter
issue
request

Use alternatives naturally.

important → significant / essential / critical / key
request → inquiry / application / appeal / submission
matter → issue / concern / subject / circumstance
help → assistance / support / guidance
information → details / clarification / documentation

SENTENCE STRUCTURE

Do not make every sentence extremely long.

Use a mixture of short, medium and longer sentences.

Poor:
I am writing because I have a problem and I want you to help me because I do not know what to do and I would really appreciate it if you could help me.

Better:
I am writing to request your assistance regarding this matter. I am currently uncertain about the appropriate course of action and would therefore appreciate your guidance.

PARAGRAPH STRUCTURE

Paragraph 1 — Purpose.
Paragraph 2 — Background.
Paragraph 3 — Request / Action.
Paragraph 4 — Closing.

FORMAL LETTER STRUCTURE

Sender details.
Date.
Recipient name/title.
Organization.
Address.
Salutation.
Subject.
Opening paragraph.
Background/details.
Request/action required.
Closing paragraph.
Sign-off.
Name.

SUBJECT LINES

Use short, specific subjects.

Request for Information
Request for Information Regarding [Matter]
Request for Assistance Regarding [Matter]
Formal Complaint Regarding [Issue]
Application for [Purpose]
Request for Authorization
Request for Clarification
Follow-Up Regarding Previous Correspondence
Submission of Supporting Documents
Request for a Meeting
Appeal Regarding [Decision]
Inquiry Concerning [Subject]

FORMAL EMAIL SUBJECTS

Question → Inquiry Regarding [Subject]
Need help → Request for Assistance Regarding [Matter]
Complaint → Formal Complaint Regarding [Matter]
Meeting → Request for a Meeting
Update → Request for an Update Regarding [Matter]
Documents → Submission of Requested Documentation

POLITENESS HIERARCHY

Preferred:
I would appreciate…
I would be grateful…
I respectfully request…
I kindly request…
I would welcome…

Avoid:
You have to…
You must…
Give me…
Do this…
Fix this now…
I demand…

unless the original meaning specifically requires a formal legal or administrative demand.

FORMAL ALTERNATIVES TO I WANT

I want → I would like
I want to ask → I would like to inquire
I want information → I would like to request information
I want help → I would appreciate assistance
I want permission → I would like to request authorization
I want an answer → I would appreciate a response
I want an explanation → I would appreciate clarification
I want you to investigate → I respectfully request that this matter be investigated
I want you to consider → I respectfully request that you consider

FORMAL ALTERNATIVES TO YOU

Avoid repeated use of "you".

You need to check this.
→ This matter requires verification.

You should investigate this.
→ I would appreciate it if the matter could be investigated.

You forgot to send it.
→ It appears that the document has not yet been provided.

PASSIVE VOICE

Use passive voice where appropriate.

You did not process my application.
→ My application has not yet been processed.

You made an error.
→ An error appears to have occurred.

You rejected my request.
→ My request was declined.

Do not use passive voice for every sentence.

DIPLOMATIC LANGUAGE

You're wrong.
→ I would respectfully suggest that this information may require clarification.

This makes no sense.
→ I would appreciate further clarification regarding this point.

You didn't help me.
→ Unfortunately, I was unable to obtain the assistance required.

You ignored my email.
→ I have not yet received a response to my previous correspondence.

This is unfair.
→ I would appreciate further consideration of this matter.

OFFICIAL VOCABULARY BANK

accordingly
additionally
adequate
accordance
acknowledge
amend
anticipate
applicable
appropriate
approximately
ascertain
assistance
authorize
beneficial
clarification
commence
comply
concerning
consequently
consideration
constitute
consultation
correspondence
currently
demonstrate
designate
determine
discontinue
documentation
elaborate
eligible
ensure
establish
evaluate
examine
facilitate
furthermore
hereby
herewith
implementation
indicate
inquire
inspection
intend
investigate
maintain
nevertheless
notwithstanding
obtain
occasion
official
pursuant
regarding
relevant
require
respectfully
subsequently
sufficient
therefore
therein
thereof
undertake
verify
whereas
withdraw
witness

FORMAL PHRASE BANK

With regard to…
With reference to…
In relation to…
In connection with…
In accordance with…
In response to…
Further to…
With respect to…
In light of…
In view of…
Taking into consideration…
For the purpose of…
As a result of…
On the basis of…
Subject to…
In the event that…
Should you require…
At your earliest convenience…
At the appropriate time…
To the best of my knowledge…
For your consideration…
For your information…
For the avoidance of doubt…
To the best of my knowledge…
As previously stated…
As outlined above…
As mentioned previously…
In accordance with the relevant requirements…
Should you require…
Should it be necessary…
Please be advised that…
I wish to clarify that…
I respectfully submit that…
I respectfully request that…

NOMINALIZATION

decide → decision
consider → consideration
approve → approval
authorize → authorization
investigate → investigation
respond → response
assist → assistance
inform → information
communicate → communication
request → request
complain → complaint
propose → proposal
recommend → recommendation
require → requirement
permit → permission
refuse → refusal
explain → explanation
clarify → clarification
resolve → resolution
review → review
assess → assessment
evaluate → evaluation

FORMAL SENTENCE STRUCTURES

I am writing to request an update regarding the status of my application.

I submitted the requested documentation; however, I have not yet received a response.

I would be grateful if you could provide an update regarding the current status of this matter.

I am writing to bring a matter concerning my application to your attention.

I would appreciate your prompt attention to this matter.

FORMAL PARAGRAPH STRUCTURE

Subject / Purpose
Formal greeting
Introduction
Background / Context
Main matter
Request / Action required
Supporting information
Polite conclusion
Formal closing

Example:

Dear Sir/Madam,

I am writing regarding [matter].

I wish to bring to your attention [situation]. The circumstances are as follows: [facts].

In light of the above, I respectfully request [specific action].

I would be grateful if this matter could be given due consideration. Should you require any additional information, I would be pleased to provide it.

Thank you for your time and consideration. I look forward to receiving your response.

Yours faithfully,

[Name]

AI TRANSFORMATION RULES

DO:

Preserve meaning.
Preserve facts.
Correct grammar.
Correct spelling.
Improve vocabulary.
Improve sentence structure.
Improve paragraph structure.
Remove slang.
Remove unnecessary repetition.
Use formal connectors.
Use diplomatic wording.
Use precise vocabulary.
Use appropriate formal greetings.
Use an appropriate closing.
Make requests polite.
Make complaints respectful.
Make arguments logical.
Make the final writing sound natural.

DO NOT:

Change facts.
Invent information.
Add fake evidence.
Add unnecessary legal language.
Add complicated vocabulary simply to sound intelligent.
Make every sentence extremely long.
Use archaic words unnecessarily.
Change intended tone.
Make a friendly email sound like a legal document unless requested.
Add claims the user did not make.

INTELLIGENCE RULE

Formal does NOT mean using the longest or most complicated words possible.

Prefer:

clear + precise + diplomatic + sophisticated

over:

complicated + unnatural + excessive.

Bad:
I hereby wish to utilize this particular opportunity to articulately communicate my aforementioned desire…

Good:
I wish to take this opportunity to express my request…

FINAL QUALITY CHECK

Before producing the final correspondence check:

Grammar correct.
Spelling correct.
Vocabulary formal.
Contractions removed when appropriate.
Slang removed.
Tone respectful.
Request diplomatic.
Complaint professional.
All facts preserved.
Names preserved.
Dates preserved.
Numbers preserved.
Structure logical.
Paragraphs properly organized.
Transitions smooth.
Vocabulary precise.
Writing natural.
Recipient appropriate.
Formal without unnecessary complication.
Genuine professional correspondence.
No information invented.

FINAL TRANSFORMATION INSTRUCTION

Whenever the user gives an informal letter, email, message or collection of notes, transform it into the highest appropriate level of professional English.

Understand the intended meaning first.

Then rewrite using sophisticated but natural vocabulary, formal sentence structures, diplomatic language, precise grammar, logical organization and professional correspondence conventions.

The result should sound as though it was written by an educated professional communicating with a senior official, government department, institution, company or other important recipient.

Do not simply replace individual words with synonyms.

Rewrite the entire structure where necessary.

Preserve every important fact.

Do not invent information.

The final result must be polished, authoritative, respectful, clear and highly professional.
`;


/* =========================================================
   LOCAL KNOWLEDGE ENGINE
   ========================================================= */

const FORMAL_PAIRS = {

"just wanted to":"I am writing to",
"just checking":"I am writing to follow up regarding",
"just asking":"I am writing to inquire about",
"hi":"Dear Sir/Madam,",
"hey":"Dear Sir/Madam,",
"thanks a lot":"Thank you for your time and consideration.",
"thanks":"Thank you for your consideration.",
"cheers":"Kind regards,",
"no worries":"I understand.",
"my bad":"I apologize for the error.",
"what's up":"I am writing regarding",
"what is up":"I am writing regarding",

"ask for":"request",
"ask about":"inquire about",
"ask":"request",
"tell":"inform",
"say":"state",
"show":"demonstrate",
"give":"provide",
"get":"obtain",
"help":"assist",
"need":"require",
"want":"would like",
"buy":"purchase",
"keep":"retain",
"start":"commence",
"finish":"conclude",
"end":"conclude",
"use":"utilize",
"fix":"rectify",
"deal with":"address",
"check":"verify",
"look at":"review",
"look into":"investigate",
"find out":"determine",
"talk about":"discuss",
"think about":"consider",
"make sure":"ensure",
"put off":"postpone",
"leave out":"omit",
"go up":"increase",
"go down":"decrease",
"set up":"establish",
"bring up":"raise",
"point out":"indicate",
"carry out":"undertake",
"come back":"return",
"get back to":"respond",
"try":"attempt",
"join":"participate",
"send":"provide",
"pay back":"reimburse",
"book":"reserve",
"fill in":"complete",
"fill out":"complete",
"cancel":"withdraw",
"change":"modify",
"improve":"enhance",
"make worse":"aggravate",
"reply":"respond",
"answer":"respond",
"hope":"anticipate",

"problem":"issue",
"trouble":"difficulty",
"mistake":"error",
"reason":"rationale",
"idea":"proposal",
"plan":"strategy",
"goal":"objective",
"job":"position",
"boss":"supervisor",
"worker":"employee",
"company":"organization",
"office":"department",
"rule":"regulation",
"law":"legislation",
"deal":"agreement",
"promise":"commitment",
"choice":"option",
"chance":"opportunity",
"result":"outcome",
"way":"method",
"stuff":"materials",
"thing":"matter",
"people":"individuals",
"person":"individual",
"meeting":"conference",
"question":"inquiry",
"form":"document",
"paper":"document",
"message":"correspondence",
"proof":"evidence",
"opinion":"viewpoint",
"worried":"concerned",
"angry":"dissatisfied",
"unhappy":"dissatisfied",
"happy":"pleased",
"glad":"pleased",
"sure":"certain",
"unsure":"uncertain",
"clear":"explicit",
"unclear":"ambiguous",
"important":"significant",
"very important":"essential",
"necessary":"required",
"possible":"feasible",
"impossible":"unfeasible",
"useful":"beneficial",
"harmful":"detrimental",
"fair":"equitable",
"unfair":"inequitable",
"careful":"cautious",
"right":"correct",
"wrong":"incorrect",
"normal":"standard",
"unusual":"uncommon",
"common":"widespread",
"different":"alternative",
"same":"equivalent",
"new":"recent",
"old":"previous",
"current":"existing",
"urgent":"pressing",
"late":"delayed",
"extra":"additional",
"whole":"entire",
"many":"numerous",
"few":"limited",
"most":"majority",
"main":"principal",
"only":"sole",
"exact":"precise",
"real":"genuine",
"fake":"fraudulent",

"quickly":"promptly",
"carefully":"diligently",
"usually":"generally",
"often":"frequently",
"sometimes":"occasionally",
"soon":"shortly",
"now":"currently",
"later":"subsequently",
"finally":"ultimately",
"exactly":"precisely",
"almost":"nearly",
"completely":"entirely",
"mostly":"predominantly",
"properly":"appropriately",
"together":"jointly",

"because":"therefore",
"so":"consequently",
"but":"however",
"also":"furthermore",
"then":"subsequently",
"while":"whereas",
"even though":"although",
"about":"regarding",
"before":"prior to",
"after":"following",
"during":"throughout",
"for now":"for the time being",
"in the end":"ultimately",
"for example":"for instance",
"like":"such as",

"i want to":"I would like to",
"i want":"I would like",
"i need":"I require",
"i want help":"I would appreciate assistance",
"i want information":"I would like to request information",
"i want permission":"I would like to request authorization",
"i want an answer":"I would appreciate a response",
"i want an explanation":"I would appreciate clarification",

"can you send":"Could you kindly provide",
"can you help":"Would you be able to assist",
"can you check":"I would appreciate it if you could review and verify",
"tell me what i need to do":"Could you kindly advise me regarding the appropriate course of action",
"please fix this":"I would be grateful if this matter could be addressed and rectified",

"send me":"please provide",
"give me":"please provide",
"fix this":"please address this matter",
"tell me":"please inform me",

"you're wrong":"I would respectfully suggest that this information may require clarification.",
"you are wrong":"I would respectfully suggest that this information may require clarification.",
"this makes no sense":"I would appreciate further clarification regarding this point.",
"you didn't help me":"Unfortunately, I was unable to obtain the assistance required.",
"you ignored my email":"I have not yet received a response to my previous correspondence.",
"this is unfair":"I would appreciate further consideration of this matter.",
"you made a mistake":"An error appears to have occurred.",
"you forgot":"It appears that this may have been overlooked.",
"fix this now":"I would appreciate it if this matter could be reviewed and addressed promptly.",
"you need to check this":"This matter requires verification.",
"you should investigate this":"I would appreciate it if the matter could be investigated."
};


/* =========================================================
   SLANG / TEXTING
   ========================================================= */

const SLANG = {
    "u":"you",
    "ur":"your",
    "r":"are",
    "pls":"please",
    "plz":"please",
    "thx":"thank you",
    "asap":"at the earliest opportunity",
    "btw":"additionally",
    "idk":"I do not know",
    "rn":"currently",
    "lmk":"please let me know",
    "tbh":"to be honest",
    "imo":"in my opinion",
    "np":"no problem",
    "gonna":"going to",
    "wanna":"want to",
    "gotta":"have to",
    "kinda":"somewhat",
    "sorta":"somewhat",
    "yeah":"yes",
    "yep":"yes",
    "nope":"no",
    "fyi":"For your information",
    "lol":"",
    "omg":"",
    "ok":"acceptable"
};


/* =========================================================
   CONTRACTIONS
   ========================================================= */

const CONTRACTIONS = {
    "can't":"cannot",
    "won't":"will not",
    "don't":"do not",
    "doesn't":"does not",
    "didn't":"did not",
    "isn't":"is not",
    "aren't":"are not",
    "wasn't":"was not",
    "weren't":"were not",
    "haven't":"have not",
    "hasn't":"has not",
    "hadn't":"had not",
    "wouldn't":"would not",
    "couldn't":"could not",
    "shouldn't":"should not",
    "mightn't":"might not",
    "mustn't":"must not",
    "i'm":"I am",
    "i'd":"I would",
    "i'll":"I will",
    "i've":"I have",
    "we're":"we are",
    "we'd":"we would",
    "we'll":"we will",
    "we've":"we have",
    "they're":"they are",
    "they'd":"they would",
    "they'll":"they will",
    "you're":"you are",
    "you'd":"you would",
    "you'll":"you will",
    "it's":"it is",
    "that's":"that is",
    "there's":"there is",
    "what's":"what is"
};


/* =========================================================
   FORMAL PHRASES
   ========================================================= */

const FORMAL_PHRASES = [

"I am writing regarding",
"I am writing concerning",
"I am writing in relation to",
"I am writing with regard to",
"I am writing to request",
"I am writing to seek",
"I am writing to inquire about",
"I am writing to formally raise a concern",
"I am writing to bring the following matter to your attention",
"I wish to draw your attention to",
"I would like to bring to your attention",
"I wish to seek clarification concerning",

"I would appreciate it if you could",
"I would be grateful if you could",
"I kindly request that",
"I respectfully request that",
"I wish to request",
"I would like to request",
"I respectfully seek",
"I would appreciate your assistance",
"I would be grateful for your consideration",
"I respectfully ask that the matter be reviewed",
"I would appreciate your guidance regarding",

"I respectfully seek your consideration of this matter",
"I would be most grateful for your assistance in this regard",
"I respectfully request that appropriate consideration be given to this matter",
"I would greatly appreciate any assistance that your office may be able to provide",

"I sincerely apologize for",
"Please accept my sincere apologies for",
"I apologize for any inconvenience caused",
"I sincerely regret",

"Thank you for your time and consideration",
"I sincerely appreciate your assistance",
"I greatly appreciate your support",
"I am grateful for your consideration",
"Your assistance in this matter is greatly appreciated",

"I am writing to follow up on my previous correspondence",
"I would appreciate an update regarding",
"I am writing to inquire about the progress of",
"I would be grateful if you could provide an update",

"I look forward to receiving your response",
"I look forward to hearing from you",
"I would appreciate your prompt attention to this matter",
"Please do not hesitate to contact me",
"Should you require any additional information"
];


/* =========================================================
   SUBJECT GENERATION
   ========================================================= */

const SUBJECTS = {
    corporate:"Request for Assistance Regarding [Matter]",
    complaint:"Formal Complaint Regarding [Issue]",
    government:"Request for Consideration Regarding [Matter]",
    school:"Request for Information Regarding [Subject]",
    legal:"Formal Response Regarding [Matter]",
    professional:"Inquiry Regarding [Subject]"
};


/* =========================================================
   SETTINGS
   ========================================================= */

const settings = {
    factLock:true,
    slang:true,
    diplomatic:true,
    natural:true
};

let lastResult = null;
let history = [];
let lastInput = "";

const $ = id => document.getElementById(id);


/* =========================================================
   LOGO / HOME SCREEN ICON
   ========================================================= */

const ICON_SVG = `
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512">
<defs>
<linearGradient id="a" x1="0" y1="0" x2="1" y2="1">
<stop offset="0" stop-color="#aab4ff"/>
<stop offset=".5" stop-color="#6878ff"/>
<stop offset="1" stop-color="#a36cff"/>
</linearGradient>
</defs>
<rect width="512" height="512" rx="130" fill="#0b0e15"/>
<rect x="25" y="25" width="462" height="462" rx="112"
fill="url(#a)"/>
<path d="M145 82h155l95 95v252H145z"
fill="#10141e"/>
<path d="M300 82v105h95"
fill="none" stroke="#fff" stroke-width="18" opacity=".7"/>
<path d="M190 230h145M190 280h115"
stroke="#fff" stroke-width="23" stroke-linecap="round" opacity=".8"/>
<path d="M190 355l40 40 85-95"
fill="none" stroke="#66e7ae" stroke-width="28"
stroke-linecap="round" stroke-linejoin="round"/>
</svg>
`;

const iconData =
    "data:image/svg+xml;charset=utf-8," +
    encodeURIComponent(ICON_SVG);

$("favicon").href = iconData;
$("appleIcon").href = iconData;

const manifest = {
    name:"Formalis — Official Letter & Email Scanner",
    short_name:"Formalis",
    start_url:".",
    display:"standalone",
    background_color:"#07090d",
    theme_color:"#080a0f",
    icons:[
        {
            src:iconData,
            sizes:"512x512",
            type:"image/svg+xml"
        }
    ]
};

$("manifest").href =
    URL.createObjectURL(
        new Blob(
            [JSON.stringify(manifest)],
            {type:"application/manifest+json"}
        )
    );


/* =========================================================
   STATS
   ========================================================= */

$("vocabCount").textContent =
    Object.keys(FORMAL_PAIRS).length;

$("slangCount").textContent =
    Object.keys(SLANG).length;

$("phraseCount").textContent =
    FORMAL_PHRASES.length;

$("ruleCount").textContent =
    Object.keys(FORMAL_PAIRS).length +
    Object.keys(CONTRACTIONS).length +
    Object.keys(SLANG).length;


/* =========================================================
   INPUT STATS
   ========================================================= */

function updateInputStats(){

    const text = $("input").value;

    const words =
        text.trim() ?
        text.trim().split(/\s+/).length :
        0;

    $("inputStats").textContent =
        `${words} words · ${text.length} characters`;
}

$("input").addEventListener("input",updateInputStats);


/* =========================================================
   FACT LOCK
   ========================================================= */

function extractProtectedTokens(text){

    const patterns = [

        /\b\d+(?:[.,]\d+)?\b/g,

        /\b\d{1,2}[/-]\d{1,2}[/-]\d{2,4}\b/g,

        /\b(?:January|February|March|April|May|June|July|August|September|October|November|December)\s+\d{1,2}(?:,\s*\d{4})?\b/gi,

        /\b\d{1,2}:\d{2}(?:\s?[AP]M)?\b/gi,

        /\b[A-Z0-9._%+-]+@[A-Z0-9.-]+\.[A-Z]{2,}\b/gi,

        /https?:\/\/[^\s]+/gi,

        /\[[^\]]+\]/g,

        /\b(?:USD|EUR|GBP|MUR|Rs\.?|£|\$|€)\s?\d+(?:[.,]\d+)?\b/gi

    ];

    const found = [];

    patterns.forEach(pattern=>{
        const matches = text.match(pattern) || [];
        matches.forEach(x=>found.push(x));
    });

    return [...new Set(found)];
}

function checkFacts(before,after){

    const protectedTokens =
        extractProtectedTokens(before);

    const missing =
        protectedTokens.filter(
            token =>
            !after.toLowerCase()
                .includes(token.toLowerCase())
        );

    return {
        passed:missing.length === 0,
        protected:protectedTokens,
        missing
    };
}


/* =========================================================
   TEXT REPLACEMENT ENGINE
   ========================================================= */

function escapeRegex(text){
    return text.replace(/[.*+?^${}()|[\]\\]/g,"\\$&");
}

function replacePreservingCase(text,from,to){

    const regex =
        new RegExp("\\b"+escapeRegex(from)+"\\b","gi");

    return text.replace(regex,match=>{

        if(!to) return "";

        if(match === match.toUpperCase())
            return to.toUpperCase();

        if(
            match[0] === match[0].toUpperCase()
        )
            return to.charAt(0).toUpperCase()+to.slice(1);

        return to;
    });
}


/* =========================================================
   LOCAL FORMALIZER
   ========================================================= */

function localFormalize(input){

    let text = input.trim();

    const changes = [];
    const issues = [];

    if(!text){
        return {
            rewritten:"",
            changes:[],
            issues:[],
            stats:{
                slang:0,
                contractions:0,
                vocabulary:0,
                tone:0
            }
        };
    }

    /* contractions first */

    for(const [from,to] of Object.entries(CONTRACTIONS)){

        const regex =
            new RegExp("\\b"+escapeRegex(from)+"\\b","gi");

        if(regex.test(text)){

            const before = text;

            text = text.replace(regex,to);

            changes.push({
                type:"Grammar",
                before:from,
                after:to,
                reason:"The contraction was expanded because highly formal correspondence generally uses complete forms."
            });
        }
    }


    /* slang */

    let slangCount = 0;

    if(settings.slang){

        for(const [from,to] of Object.entries(SLANG)){

            const regex =
                new RegExp("\\b"+escapeRegex(from)+"\\b","gi");

            if(regex.test(text)){

                slangCount++;

                const before = from;

                text = text.replace(
                    regex,
                    to
                );

                changes.push({
                    type:"Slang",
                    before,
                    after:to || "[removed]",
                    reason:"Texting or casual language was replaced with standard professional English."
                });
            }
        }
    }


    /* phrase replacement */

    const sortedPairs =
        Object.entries(FORMAL_PAIRS)
            .sort((a,b)=>b[0].length-a[0].length);

    let vocabularyCount = 0;

    for(const [from,to] of sortedPairs){

        const regex =
            new RegExp(
                escapeRegex(from),
                "gi"
            );

        if(regex.test(text)){

            const before = text;

            text = text.replace(
                regex,
                match=>{
                    if(
                        match === match.toUpperCase()
                    ) return to.toUpperCase();

                    if(
                        match[0] === match[0].toUpperCase()
                    )
                        return to.charAt(0).toUpperCase()+to.slice(1);

                    return to;
                }
            );

            vocabularyCount++;

            changes.push({
                type:"Vocabulary",
                before:from,
                after:to,
                reason:"The informal expression was replaced with more precise professional vocabulary."
            });
        }
    }


    /* diplomatic corrections */

    if(settings.diplomatic){

        const diplomaticPatterns = [

            [
                /\byou need to\b/gi,
                "this matter requires",
                "The direct command was converted into a less confrontational professional structure."
            ],

            [
                /\byou must\b/gi,
                "it is necessary to",
                "The command was softened into an objective professional construction."
            ],

            [
                /\bfix this\b/gi,
                "address this matter",
                "The wording was made more diplomatic."
            ],

            [
                /\bthis is terrible\b/gi,
                "the situation is concerning",
                "Emotional wording was replaced with neutral professional language."
            ],

            [
                /\bthis is unacceptable\b/gi,
                "this matter warrants further consideration",
                "The complaint was made firm but diplomatic."
            ]

        ];

        diplomaticPatterns.forEach(
            ([regex,replacement,reason])=>{

                if(regex.test(text)){

                    const before =
                        text.match(regex)?.[0] || "";

                    text =
                        text.replace(
                            regex,
                            replacement
                        );

                    changes.push({
                        type:"Diplomacy",
                        before,
                        after:replacement,
                        reason
                    });
                }
            }
        );
    }


    /* vague language */

    const vague = [
        ["stuff","the relevant materials"],
        ["things","the relevant matters"],
        ["a bunch of","a number of"],
        ["lots of","numerous"],
        ["really bad","highly concerning"],
        ["really important","highly significant"],
        ["kind of","somewhat"],
        ["sort of","somewhat"]
    ];

    vague.forEach(([from,to])=>{

        const regex =
            new RegExp("\\b"+escapeRegex(from)+"\\b","gi");

        if(regex.test(text)){

            text=text.replace(regex,to);

            changes.push({
                type:"Precision",
                before:from,
                after:to,
                reason:"Vague or casual wording was replaced with clearer professional language."
            });
        }
    });


    /* sentence cleanup */

    text = text
        .replace(/[ \t]+/g," ")
        .replace(/\n{3,}/g,"\n\n")
        .replace(/!{2,}/g,"!")
        .replace(/\?{2,}/g,"?")
        .trim();


    /* excessive casual opening */

    if(
        /^(hi|hey)\b/i.test(text)
    ){
        text =
            text.replace(
                /^(hi|hey)[,!\s]*/i,
                ""
            );

        text =
            "Dear Sir/Madam,\n\n" +
            text;

        changes.push({
            type:"Structure",
            before:"Hi / Hey",
            after:"Dear Sir/Madam,",
            reason:"A professional salutation was used for formal correspondence."
        });
    }


    /* first-person weak opening */

    if(
        /^i want to ask/i.test(text)
    ){

        text =
            text.replace(
                /^i want to ask/i,
                "I am writing to inquire"
            );

        changes.push({
            type:"Opening",
            before:"I want to ask",
            after:"I am writing to inquire",
            reason:"The opening was converted into a standard formal correspondence structure."
        });
    }


    /* command detection */

    const commandPatterns = [
        /^send me\b/i,
        /^give me\b/i,
        /^tell me\b/i,
        /^fix\b/i,
        /^check\b/i
    ];

    commandPatterns.forEach(regex=>{

        if(regex.test(text)){

            issues.push({
                type:"Tone",
                severity:"medium",
                message:"The original wording contains a direct command.",
                example:"Consider using a polite request structure."
            });
        }
    });


    /* casual tone detection */

    if(
        /\b(really|super|yeah|yep|nope|stuff|things)\b/i.test(input)
    ){

        issues.push({
            type:"Tone",
            severity:"medium",
            message:"Casual vocabulary was detected.",
            example:"Use precise professional wording."
        });
    }


    /* punctuation */

    if(/[!?]{2,}/.test(input)){

        issues.push({
            type:"Tone",
            severity:"low",
            message:"Repeated punctuation can appear emotional or informal.",
            example:"Use standard professional punctuation."
        });
    }


    /* empty closing */

    const lower=text.toLowerCase();

    if(
        text.length > 80 &&
        !/(yours sincerely|yours faithfully|kind regards|best regards|respectfully)/i.test(lower)
    ){

        issues.push({
            type:"Structure",
            severity:"low",
            message:"No formal closing was detected.",
            example:"Consider adding an appropriate professional sign-off."
        });
    }


    return {
        rewritten:text,
        changes,
        issues,
        stats:{
            slang:slangCount,
            contractions:changes.filter(
                c=>c.type==="Grammar"
            ).length,
            vocabulary:vocabularyCount,
            tone:issues.filter(
                i=>i.type==="Tone"
            ).length
        }
    };
}


/* =========================================================
   FORMALITY SCORING
   ========================================================= */

function calculateFormality(text){

    if(!text) return 0;

    let score = 35;

    const lower = text.toLowerCase();

    const positive = [
        "regarding",
        "concerning",
        "therefore",
        "consequently",
        "furthermore",
        "respectfully",
        "assistance",
        "consideration",
        "clarification",
        "documentation",
        "correspondence",
        "request",
        "appropriate",
        "relevant",
        "regarding",
        "would appreciate",
        "would be grateful",
        "at your earliest convenience",
        "please be advised"
    ];

    const negative = [
        "hey",
        "hi guys",
        "lol",
        "omg",
        "gonna",
        "wanna",
        "gotta",
        "stuff",
        "things",
        "yeah",
        "yep",
        "nope",
        "really",
        "super"
    ];

    positive.forEach(x=>{
        if(lower.includes(x)) score+=3;
    });

    negative.forEach(x=>{
        if(lower.includes(x)) score-=7;
    });

    score =
        Math.max(
            0,
            Math.min(100,score)
        );

    return Math.round(score);
}


/* =========================================================
   PROFESSIONALISM
   ========================================================= */

function calculateProfessionalism(text){

    let score = calculateFormality(text);

    if(
        /Dear Sir\/Madam|Yours sincerely|Yours faithfully|Kind regards|Respectfully/i
            .test(text)
    )
        score += 8;

    if(
        /I would appreciate|I would be grateful|I respectfully request/i
            .test(text)
    )
        score += 6;

    return Math.min(100,Math.round(score));
}


/* =========================================================
   ANALYSIS UI
   ========================================================= */

function renderIssues(result){

    const container = $("issues");

    if(!result.issues.length){

        container.innerHTML = `
            <div class="issue severity-low">
                <div class="issue-icon">✓</div>
                <div>
                    <div class="issue-title">No major tone issues detected</div>
                    <div class="issue-text">
                        The correspondence appears suitable for professional transformation.
                    </div>
                </div>
            </div>
        `;

        return;
    }

    container.innerHTML =
        result.issues.map(issue=>`

            <div class="issue severity-${issue.severity}">
                <div class="issue-icon">
                    ${issue.severity==="high"?"!":issue.severity==="medium"?"◆":"i"}
                </div>

                <div>
                    <div class="issue-title">
                        ${escapeHTML(issue.type)} · ${escapeHTML(issue.message)}
                    </div>

                    <div class="issue-text">
                        ${escapeHTML(issue.example || "")}
                    </div>
                </div>
            </div>

        `).join("");
}


function renderChanges(result){

    const container = $("changes");

    if(!result.changes.length){

        container.innerHTML =
            `<div style="color:var(--muted);font-size:12px;">
                No major changes were required.
            </div>`;

        return;
    }

    container.innerHTML =
        result.changes
        .slice(0,40)
        .map(change=>`

            <div class="change">

                <div class="change-top">
                    <span>${escapeHTML(change.type)}</span>
                </div>

                <div class="before">
                    ${escapeHTML(change.before)}
                </div>

                <div class="after">
                    ${escapeHTML(change.after)}
                </div>

                <div class="reason">
                    ${escapeHTML(change.reason)}
                </div>

            </div>

        `).join("");
}


/* =========================================================
   DIFF ENGINE
   ========================================================= */

function makeDiff(a,b){

    const A=a.split(/\s+/);
    const B=b.split(/\s+/);

    const n=A.length;
    const m=B.length;

    const dp =
        Array.from(
            {length:n+1},
            ()=>Array(m+1).fill(0)
        );

    for(let i=n-1;i>=0;i--){
        for(let j=m-1;j>=0;j--){

            if(
                A[i].toLowerCase() ===
                B[j].toLowerCase()
            )
                dp[i][j]=1+dp[i+1][j+1];
            else
                dp[i][j]=Math.max(
                    dp[i+1][j],
                    dp[i][j+1]
                );
        }
    }

    let i=0,j=0;
    const output=[];

    while(i<n && j<m){

        if(
            A[i].toLowerCase() ===
            B[j].toLowerCase()
        ){

            output.push(
                escapeHTML(B[j])
            );

            i++;
            j++;

        }else if(
            dp[i+1][j] >= dp[i][j+1]
        ){

            output.push(
                `<del>${escapeHTML(A[i])}</del>`
            );

            i++;

        }else{

            output.push(
                `<ins>${escapeHTML(B[j])}</ins>`
            );

            j++;
        }
    }

    while(i<n){
        output.push(
            `<del>${escapeHTML(A[i++])}</del>`
        );
    }

    while(j<m){
        output.push(
            `<ins>${escapeHTML(B[j++])}</ins>`
        );
    }

    return output.join(" ");
}


/* =========================================================
   HTML ESCAPE
   ========================================================= */

function escapeHTML(value){

    return String(value)
        .replace(/&/g,"&amp;")
        .replace(/</g,"&lt;")
        .replace(/>/g,"&gt;")
        .replace(/"/g,"&quot;")
        .replace(/'/g,"&#039;");
}


/* =========================================================
   AI CONNECTION
   ========================================================= */

/*
    Your backend should accept:

    POST /api/transform

    {
        system: MASTER_SYSTEM_INSTRUCTIONS,
        input: "...",
        preset: "...",
        formality: 1-4,
        recipient: "...",
        factLock: true
    }

    It should return:

    {
        rewritten: "...",
        changes: [
            {
                type:"Vocabulary",
                before:"...",
                after:"...",
                reason:"..."
            }
        ],
        issues: [
            {
                type:"Tone",
                severity:"medium",
                message:"...",
                example:"..."
            }
        ]
    }

    IMPORTANT:
    Never put a private AI API key in this HTML file.
*/

const AI_ENDPOINT = "/api/transform";


async function runConnectedAI(input){

    const payload = {

        system:MASTER_SYSTEM_INSTRUCTIONS,

        input,

        preset:$("preset").value,

        formality:Number(
            $("level").value
        ),

        recipient:$("recipient").value,

        settings

    };

    const response =
        await fetch(
            AI_ENDPOINT,
            {
                method:"POST",
                headers:{
                    "Content-Type":"application/json"
                },
                body:JSON.stringify(payload)
            }
        );

    if(!response.ok)
        throw new Error("AI endpoint unavailable");

    const data =
        await response.json();

    if(!data.rewritten)
        throw new Error("Invalid AI response");

    return data;
}


/* =========================================================
   MAIN TRANSFORM
   ========================================================= */

async function transform(){

    const input =
        $("input").value.trim();

    if(!input){

        toast("Enter a letter or email first.");

        $("input").focus();

        return;
    }

    lastInput=input;

    $("scanBtn").disabled=true;

    $("scanBtn").innerHTML =
        `<span class="loading">
            <span class="spinner"></span>
            Transforming
        </span>`;

    $("output").innerHTML =
        `<div class="empty">
            <div class="loading">
                <span class="spinner"></span>
                Analyzing correspondence…
            </div>
            <span>
                Checking vocabulary, tone, structure, diplomacy and facts.
            </span>
        </div>`;

    try{

        const result =
            await runConnectedAI(input);

        result.source="Connected AI";

        $("aiStatus").textContent =
            "Connected AI";

        $("modeLabel").textContent =
            "Connected AI · Master Instructions";

        lastResult=result;

    }catch(error){

        const result =
            localFormalize(input);

        result.source="Local Hybrid Engine";

        $("aiStatus").textContent =
            "Hybrid AI Ready";

        $("modeLabel").textContent =
            "Local Hybrid Engine · Full Knowledge Base";

        lastResult=result;
    }

    finishTransform();

    $("scanBtn").disabled=false;

    $("scanBtn").textContent="Transform ✦";
}


/* =========================================================
   FINISH
   ========================================================= */

function finishTransform(){

    const result=lastResult;

    $("output").textContent =
        result.rewritten ||
        "No transformation produced.";

    const formality =
        calculateFormality(
            result.rewritten
        );

    const professional =
        calculateProfessionalism(
            result.rewritten
        );

    $("formalityScore").textContent =
        formality + "%";

    $("professionalScore").textContent =
        professional + "%";

    $("issueScore").textContent =
        result.issues?.length || 0;

    if(settings.factLock){

        const facts =
            checkFacts(
                lastInput,
                result.rewritten
            );

        if(facts.passed){

            $("factScore").textContent =
                "SAFE";

            $("factScore").className =
                "metric-value fact-ok";

        }else{

            $("factScore").textContent =
                "CHECK";

            $("factScore").className =
                "metric-value fact-warning";

            result.issues =
                result.issues || [];

            result.issues.unshift({
                type:"Fact Lock",
                severity:"high",
                message:"One or more protected details may have changed.",
                example:
                    "Review: " +
                    facts.missing.join(", ")
            });
        }
    }

    renderIssues(result);
    renderChanges(result);

    $("analysisCount").textContent =
        `${result.changes?.length || 0} changes`;

    $("diff").innerHTML =
        makeDiff(
            lastInput,
            result.rewritten
        );

    history.unshift({
        input:lastInput,
        output:result.rewritten,
        time:new Date().toLocaleString()
    });

    history=history.slice(0,10);

    toast(
        result.source === "Connected AI"
        ? "AI transformation complete."
        : "Local transformation complete."
    );
}


/* =========================================================
   SUBJECT GENERATOR
   ========================================================= */

function generateSubject(){

    const input =
        $("input").value.trim();

    if(!input){

        toast("Enter your correspondence first.");

        return;
    }

    const preset =
        $("preset").value;

    const subject =
        SUBJECTS[preset] ||
        "Formal Correspondence Regarding [Matter]";

    const text =
        $("output").textContent;

    if(
        !text ||
        text.includes("Your formal correspondence")
    ){

        toast(subject);

        return;
    }

    const subjectLine =
        "Subject: " + subject;

    $("output").textContent =
        subjectLine +
        "\n\n" +
        text;

    toast("Formal subject added.");
}


/* =========================================================
   SAMPLE
   ========================================================= */

$("sampleBtn").addEventListener("click",()=>{

    $("input").value =
`Hi, I just wanted to ask if you can check my application because I sent the documents last week but I haven't heard anything yet. I really need an update because I don't know what I am supposed to do. Please get back to me ASAP. Thanks a lot.`;

    updateInputStats();

    toast("Professional sample loaded.");
});


/* =========================================================
   BUTTONS
   ========================================================= */

$("scanBtn").addEventListener(
    "click",
    transform
);

$("clearBtn").addEventListener(
    "click",
    ()=>{
        $("input").value="";
        $("output").innerHTML=`
            <div class="empty">
                <div class="empty-icon">✦</div>
                <strong>Your formal correspondence will appear here.</strong>
                <span>
                    The scanner checks tone, slang, contractions,
                    vocabulary, structure, diplomacy and facts.
                </span>
            </div>
        `;

        $("issues").innerHTML="";
        $("changes").innerHTML="";
        $("diff").textContent =
            "Transform a document to compare the original and formal versions.";

        $("formalityScore").textContent="—";
        $("professionalScore").textContent="—";
        $("issueScore").textContent="—";
        $("factScore").textContent="READY";

        updateInputStats();

        toast("Workspace cleared.");
    }
);


$("copyBtn").addEventListener(
    "click",
    async ()=>{

        if(!lastResult?.rewritten){

            toast("Nothing to copy yet.");

            return;
        }

        await navigator.clipboard.writeText(
            lastResult.rewritten
        );

        toast("Formal correspondence copied.");
    }
);


$("downloadBtn").addEventListener(
    "click",
    ()=>{

        if(!lastResult?.rewritten){

            toast("Nothing to download yet.");

            return;
        }

        const blob =
            new Blob(
                [lastResult.rewritten],
                {type:"text/plain;charset=utf-8"}
            );

        const url =
            URL.createObjectURL(blob);

        const a =
            document.createElement("a");

        a.href=url;
        a.download="formal-correspondence.txt";

        document.body.appendChild(a);
        a.click();
        a.remove();

        URL.revokeObjectURL(url);

        toast("Document downloaded.");
    }
);


$("diffBtn").addEventListener(
    "click",
    ()=>{
        document
            .querySelector(".card:last-child")
            .scrollIntoView({
                behavior:"smooth"
            });
    }
);


$("whyBtn").addEventListener(
    "click",
    ()=>{
        document
            .querySelector(".inspector")
            .scrollIntoView({
                behavior:"smooth"
            });
    }
);


$("subjectBtn").addEventListener(
    "click",
    generateSubject
);


/* =========================================================
   UNDO
   ========================================================= */

$("undoBtn").addEventListener(
    "click",
    ()=>{

        if(lastInput){

            $("input").value=lastInput;

            updateInputStats();

            toast("Original text restored.");

        }else{

            toast("Nothing to restore.");
        }
    }
);


/* =========================================================
   PASTE
   ========================================================= */

$("pasteBtn").addEventListener(
    "click",
    async ()=>{

        try{

            const text =
                await navigator.clipboard.readText();

            $("input").value=text;

            updateInputStats();

            toast("Text pasted.");

        }catch{

            toast("Safari did not allow clipboard access.");
        }
    }
);


/* =========================================================
   SETTINGS
   ========================================================= */

document
    .querySelectorAll(".switch")
    .forEach(button=>{

        button.addEventListener(
            "click",
            ()=>{

                const key =
                    button.dataset.setting;

                settings[key]=
                    !settings[key];

                button.classList.toggle(
                    "active",
                    settings[key]
                );

                toast(
                    `${key} ${settings[key]?"enabled":"disabled"}`
                );
            }
        );
    });


/* =========================================================
   HISTORY
   ========================================================= */

$("historyBtn").addEventListener(
    "click",
    ()=>{

        if(!history.length){

            toast("No transformations yet.");

            return;
        }

        const latest =
            history
                .map(
                    (item,index)=>
                    `${index+1}. ${item.time}`
                )
                .join("\n");

        alert(
            "FORMALIS HISTORY\n\n" +
            latest
        );
    }
);


/* =========================================================
   TOAST
   ========================================================= */

let toastTimer;

function toast(message){

    const element=$("toast");

    element.textContent=message;

    element.classList.add("show");

    clearTimeout(toastTimer);

    toastTimer =
        setTimeout(
            ()=>element.classList.remove("show"),
            2200
        );
}


/* =========================================================
   KEYBOARD SHORTCUTS
   ========================================================= */

document.addEventListener(
    "keydown",
    event=>{

        if(
            (event.metaKey || event.ctrlKey) &&
            event.key.toLowerCase()==="enter"
        ){

            event.preventDefault();

            transform();
        }

    }
);


/* =========================================================
   PRESET AUTO LEVEL
   ========================================================= */

$("preset").addEventListener(
    "change",
    ()=>{

        const preset =
            $("preset").value;

        const levels = {
            corporate:"2",
            complaint:"3",
            government:"4",
            school:"2",
            legal:"4",
            professional:"2"
        };

        $("level").value =
            levels[preset] || "2";
    }
);


/* =========================================================
   INITIALIZATION
   ========================================================= */

updateInputStats();

$("aiStatus").textContent =
    "Hybrid AI Ready";

console.log(
    "Formalis loaded.",
    {
        masterInstructions:true,
        vocabularyRules:Object.keys(FORMAL_PAIRS).length,
        slangRules:Object.keys(SLANG).length,
        formalPhrases:FORMAL_PHRASES.length,
        factLock:true
    }
);

</script>

</body>
</html>
