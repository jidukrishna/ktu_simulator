# Contributing to KTU Open Simulations

Anyone can contribute a simulation. You don't need to be a great programmer — if you've built something that helps visualize a concept, it belongs here.

---

## Two ways to contribute

### Option A — GitHub Pull Request *(preferred)*

Full control, instant credit on the site. Follow the step-by-step guide below.

### Option B — Google Form *(if you don't know GitHub)*

Just fill out the form and attach your `.html` file — we'll add it to the repo for you.  
**[→ Submit via Google Form](https://docs.google.com/forms/d/e/1FAIpQLSfjeQurmGfM2b1tTWiUerO8hFphvBtzSWCPCmU2-r54lnVuAg/viewform?usp=header)**

---

## What counts as a simulation?

Anything interactive that helps understand a topic:
- A visual algorithm step-through
- A physics concept with sliders
- A data structure visualizer
- A formula explorer with live inputs

If it runs in a browser and teaches something, submit it.

---

## Requirements

- **Single HTML file** — all CSS and JS must be inline. No external dependencies except public CDNs (e.g. cdnjs.cloudflare.com).
- **Must work offline** — if it needs a server to run, it won't work on GitHub Pages.
- **Mobile-friendly preferred** — not required, but appreciated.
- **Validate with test cases** — make sure simulations work for all test cases.

---

## Step-by-step submission (GitHub)

### 1. Fork the repo

Click **Fork** on the top right of this repo page. This creates your own copy.

### 2. Clone your fork

```bash
git clone https://github.com/jidukrishna/ktu_simulator.git
cd ktu_simulator
```

### 3. Add your HTML file

Put your file in the correct branch/subject folder:

```
simulations/
├── cse/
│   ├── toc/          ← Theory of Computation
│   ├── os/           ← Operating Systems
│   ├── cn/           ← Computer Networks
│   └── dsa/          ← Data Structures & Algorithms
├── ece/
│   ├── signals/
│   └── circuits/
├── eee/
├── mech/
├── civil/
└── applied_electronics/
```

Name your file clearly, all lowercase, no spaces:

```
✅ nfa_to_dfa.html
✅ fourier_visualizer.html
❌ My Simulation (1).html
❌ untitled.html
```

**If your subject folder doesn't exist yet, create it.**

### 4. Add your entry to `data/simulations.json`

Open `data/simulations.json` and add your entry under the correct branch and subject.

```json
{
  "CSE": {
    "Theory of Computation": [
      {
        "title": "NFA to DFA Converter",
        "description": "Step-by-step conversion of NFA to equivalent DFA with state table.",
        "file": "simulations/cse/toc/nfa_to_dfa.html",
        "author": "Your Name",
        "author_link": "https://github.com/yourusername",
        "date": "2026-05-01"
      }
    ]
  }
}
```

**Rules:**
- `title` — short and clear, max ~40 chars
- `description` — one sentence explaining what it does, max ~100 chars
- `file` — path relative to the repo root
- `author_link` — optional, can be GitHub, LinkedIn, or personal site
- `date` — the date you're submitting (YYYY-MM-DD)

**If your subject doesn't exist yet in the JSON**, add it as a new key:

```json
"Computer Networks": [
  { ...your entry... }
]
```

### 5. Test it locally

```bash
python -m http.server
```

Open `http://localhost:8000` in your browser. Check:
- Your simulation appears in the right branch and subject
- The `launch` button opens your file correctly
- Your simulation actually works

### 6. Commit and push

```bash
git add .
git commit -m "add: NFA to DFA converter (CSE / TOC)"
git push origin main
```

Use this commit message format:
```
add: <simulation name> (<branch> / <subject>)
```

### 7. Open a Pull Request

Go to your fork on GitHub and click **"Compare & pull request"**.

In the PR description, briefly mention:
- What the simulation does
- Which subject/module it's for
- How to use it (if not obvious)

---

## PR will be rejected if

- The file doesn't run on GitHub Pages
- External dependencies are missing or broken
- The JSON entry has wrong file path
- If the simulation fails test cases

---

## Questions?

Open an issue or reach out at [jidu.dev](https://jidu.dev).
