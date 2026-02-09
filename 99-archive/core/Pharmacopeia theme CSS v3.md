/* ═══════════════════════════════════════════════════════════════════════════
   PHARMACOPEIA.INFO — CYBER-APOTHECARY AESTHETIC v3.0

   Design Philosophy: Minimalismo + Identidade Botânica
   ═══════════════════════════════════════════════════════════════════════════ */

:root {
    /* Layout */
    --width: 650px;

    /* Typography */
    --font-main: "Georgia", "Garamond", serif;
    --font-mono: "Courier New", monospace;
    --font-scale: 1em;

    /* Colors — Light Mode */
    --background-color: #fffff8;
    --heading-color: #111;
    --text-color: #444;
    --link-color: #2e5d4b;
    --visited-color: #234a3b;
    --code-background-color: #e8f2ed;
    --code-color: #2e5d4b;
    --blockquote-color: #555;

    /* Accent Colors */
    --accent: #2e5d4b;
    --accent-light: #4a8c6f;
    --amber: #b8860b;
    --gray: #707070;
    --gray-light: #d0d0d0;

    /* Semantic Colors */
    --success: #2e7d32;
    --warning: #f57c00;
    --error: #c62828;
    --info: #1565c0;

    /* Badges */
    --badge-lurker: #9e9e9e;
    --badge-operative: #43a047;
    --badge-debugger: #fb8c00;
    --badge-architect: #5c6bc0;
    --badge-elder: #ffd700;
}

@media (prefers-color-scheme: dark) {
    :root {
        --background-color: #0a0a08;
        --heading-color: #f5f5ed;
        --text-color: #ddd;
        --link-color: #5ba882;
        --visited-color: #3d7a5f;
        --code-background-color: #151512;
        --code-color: #5ba882;
        --blockquote-color: #b8b8a8;
        --gray-light: #404040;
    }
}

/* ═══════════════════════════════════════════════════════════════════════════
   BASE STYLES
   ═══════════════════════════════════════════════════════════════════════════ */

* {
    box-sizing: border-box;
}

body {
    font-family: var(--font-main);
    font-size: var(--font-scale);
    margin: auto;
    padding: 20px;
    max-width: var(--width);
    text-align: left;
    background-color: var(--background-color);
    word-wrap: break-word;
    overflow-wrap: break-word;
    line-height: 1.6;
    color: var(--text-color);
}

/* ═══════════════════════════════════════════════════════════════════════════
   TYPOGRAPHY
   ═══════════════════════════════════════════════════════════════════════════ */

h1, h2, h3, h4, h5, h6 {
    font-family: var(--font-mono);
    color: var(--heading-color);
    line-height: 1.3;
    margin-top: 2em;
    margin-bottom: 0.5em;
}

h1 {
    font-size: 2.5em;
    border-bottom: 2px solid var(--heading-color);
    padding-bottom: 0.3em;
    margin-top: 0;
}

h2 {
    font-size: 1.5em;
    border-left: 4px solid var(--accent);
    padding-left: 12px;
}

h3 {
    font-size: 1.25em;
    color: var(--accent);
}

p {
    margin-bottom: 1em;
}

strong, b {
    color: var(--heading-color);
    font-weight: 700;
}

/* ═══════════════════════════════════════════════════════════════════════════
   LINKS
   ═══════════════════════════════════════════════════════════════════════════ */

a {
    color: var(--link-color);
    cursor: pointer;
    text-decoration: none;
    border-bottom: 1px dotted var(--link-color);
}

a:hover {
    border-bottom-style: solid;
}

a:visited {
    color: var(--visited-color);
}

/* Título do site - sem efeitos */
h1 a,
.title a {
    border-bottom: none;
    color: inherit;
}

h1 a:hover,
.title a:hover {
    border-bottom: none;
    text-decoration: none;
}

/* External links */
a[href^="http"]:not([href*="pharmacopeia"])::after {
    content: " ↗";
    font-size: 0.8em;
}

/* ═══════════════════════════════════════════════════════════════════════════
   NAVIGATION
   ═══════════════════════════════════════════════════════════════════════════ */

nav {
    margin-bottom: 2em;
}

nav a {
    margin-right: 12px;
}

/* ═══════════════════════════════════════════════════════════════════════════
   CODE
   ═══════════════════════════════════════════════════════════════════════════ */

code {
    font-family: var(--font-mono);
    padding: 2px 6px;
    background-color: var(--code-background-color);
    color: var(--code-color);
    border-radius: 3px;
    font-size: 0.9em;
}

pre {
    background-color: var(--code-background-color);
    color: var(--code-color);
    padding: 15px;
    border-radius: 3px;
    border-left: 4px solid var(--amber);
    overflow-x: auto;
    line-height: 1.5;
}

pre code {
    background: none;
    padding: 0;
    border-radius: 0;
}

.highlight, .code {
    padding: 1px 15px;
    background-color: var(--code-background-color);
    color: var(--code-color);
    border-radius: 3px;
    margin-block-start: 1em;
    margin-block-end: 1em;
    overflow-x: auto;
}

/* ═══════════════════════════════════════════════════════════════════════════
   LISTS
   ═══════════════════════════════════════════════════════════════════════════ */

ul, ol {
    margin-bottom: 1em;
    padding-left: 2em;
}

li {
    margin-bottom: 0.5em;
}

ul li::marker {
    color: var(--accent);
}

ol li::marker {
    color: var(--accent);
}

/* ═══════════════════════════════════════════════════════════════════════════
   BLOCKQUOTE
   ═══════════════════════════════════════════════════════════════════════════ */

blockquote {
    border-left: 4px solid var(--amber);
    color: var(--blockquote-color);
    padding-left: 20px;
    margin: 1.5em 0;
    font-style: italic;
}

/* ═══════════════════════════════════════════════════════════════════════════
   TABLES
   ═══════════════════════════════════════════════════════════════════════════ */

table {
    width: 100%;
    border-collapse: collapse;
    margin: 1.5em 0;
}

th {
    background-color: var(--accent);
    color: var(--background-color);
    padding: 8px 12px;
    text-align: left;
}

td {
    padding: 8px 12px;
    border-bottom: 1px solid var(--gray-light);
}

tr:hover {
    background-color: var(--code-background-color);
}

/* ═══════════════════════════════════════════════════════════════════════════
   IMAGES & MEDIA
   ═══════════════════════════════════════════════════════════════════════════ */

img {
    max-width: 100%;
    border-radius: 3px;
}

hr {
    border: 0;
    border-top: 1px dashed var(--gray-light);
    margin: 2em 0;
}

/* ═══════════════════════════════════════════════════════════════════════════
   BADGES (Gamificação)
   ═══════════════════════════════════════════════════════════════════════════ */

.badge {
    display: inline-block;
    font-family: var(--font-mono);
    font-size: 0.75em;
    font-weight: 600;
    padding: 3px 8px;
    border-radius: 12px;
    text-transform: uppercase;
    letter-spacing: 0.5px;
    margin-right: 6px;
}

.badge-lurker {
    background-color: var(--badge-lurker);
    color: white;
}

.badge-lurker::before { content: "👁 "; }

.badge-operative {
    background-color: var(--badge-operative);
    color: white;
}

.badge-operative::before { content: "✓ "; }

.badge-debugger {
    background-color: var(--badge-debugger);
    color: white;
}

.badge-debugger::before { content: "🔧 "; }

.badge-architect {
    background-color: var(--badge-architect);
    color: white;
}

.badge-architect::before { content: "🏛️ "; }

.badge-elder {
    background: linear-gradient(135deg, var(--badge-elder), #ffec8b);
    color: #111;
}

.badge-elder::before { content: "👑 "; }

/* Status Badges */
.badge-stable {
    background-color: var(--success);
    color: white;
}

.badge-beta {
    background-color: var(--amber);
    color: white;
}

.badge-draft {
    background-color: var(--gray);
    color: white;
}

/* ═══════════════════════════════════════════════════════════════════════════
   CALLOUT BOXES
   ═══════════════════════════════════════════════════════════════════════════ */

.callout {
    padding: 15px;
    margin: 1.5em 0;
    border-radius: 3px;
    border-left: 4px solid;
}

.callout-info {
    background-color: #e3f2fd;
    border-left-color: var(--info);
}

.callout-success {
    background-color: #e8f5e9;
    border-left-color: var(--success);
}

.callout-warning {
    background-color: #fff3e0;
    border-left-color: var(--warning);
}

.callout-error {
    background-color: #ffebee;
    border-left-color: var(--error);
}

.callout-tip {
    background-color: var(--code-background-color);
    border-left-color: var(--accent);
}

@media (prefers-color-scheme: dark) {
    .callout-info { background-color: rgba(33, 150, 243, 0.15); }
    .callout-success { background-color: rgba(76, 175, 80, 0.15); }
    .callout-warning { background-color: rgba(255, 152, 0, 0.15); }
    .callout-error { background-color: rgba(244, 67, 54, 0.15); }
    .callout-tip { background-color: rgba(61, 122, 95, 0.15); }
}

/* ═══════════════════════════════════════════════════════════════════════════
   BUTTONS
   ═══════════════════════════════════════════════════════════════════════════ */

button, .btn {
    font-family: var(--font-mono);
    font-size: 0.9em;
    padding: 8px 16px;
    background-color: var(--accent);
    color: var(--background-color);
    border: none;
    border-radius: 3px;
    cursor: pointer;
    text-decoration: none;
    display: inline-block;
}

button:hover, .btn:hover {
    background-color: var(--accent-light);
    border-bottom: none;
}

.btn-secondary {
    background-color: transparent;
    color: var(--accent);
    border: 2px solid var(--accent);
}

.btn-secondary:hover {
    background-color: var(--accent);
    color: var(--background-color);
}

/* ═══════════════════════════════════════════════════════════════════════════
   CARDS
   ═══════════════════════════════════════════════════════════════════════════ */

.card {
    padding: 15px;
    margin: 1em 0;
    border: 1px solid var(--gray-light);
    border-radius: 3px;
}

.card:hover {
    border-color: var(--accent);
}

/* ═══════════════════════════════════════════════════════════════════════════
   FOOTER
   ═══════════════════════════════════════════════════════════════════════════ */

footer {
    padding: 25px 0;
    text-align: center;
    border-top: 1px dashed var(--gray-light);
    margin-top: 3em;
    font-size: 0.9em;
    color: var(--gray);
}

/* ═══════════════════════════════════════════════════════════════════════════
   UTILITIES
   ═══════════════════════════════════════════════════════════════════════════ */

.inline {
    width: auto !important;
}

.text-center {
    text-align: center;
}

.text-muted {
    color: var(--gray);
}

.mt-1 { margin-top: 1em; }
.mb-1 { margin-bottom: 1em; }
.mt-2 { margin-top: 2em; }
.mb-2 { margin-bottom: 2em; }

/* ═══════════════════════════════════════════════════════════════════════════
   RESPONSIVE
   ═══════════════════════════════════════════════════════════════════════════ */

@media (max-width: 768px) {
    body {
        padding: 15px;
    }

    h1 {
        font-size: 2em;
    }

    h2 {
        font-size: 1.35em;
    }

    pre {
        padding: 10px;
        font-size: 0.85em;
    }

    table {
        font-size: 0.9em;
    }
}

/* ═══════════════════════════════════════════════════════════════════════════
   FIM DO CSS — PHARMACOPEIA.INFO v3.0 (Minimalista)
   ═══════════════════════════════════════════════════════════════════════════ */