# KTU Open Simulations

A community-built gallery of interactive simulations for KTU students.  
Built by students, for students — open source, no logins, no nonsense.  
Students can use ai to create simulations, verify test cases and submit.

**[→ Open the site](https://ktu.jidu.dev)**

---

## What's in here

Interactive browser simulations organized by branch and subject:

| Branch | Subjects |
|--------|----------|
| CSE | Theory of Computation, Operating Systems, ... |
| ECE | Signals & Systems, ... |
| EEE | *(open for contributions)* |
| MECH | *(open for contributions)* |
| CIVIL | *(open for contributions)* |
| APPLIED ELECTRONICS | *(open for contributions)* |

Each simulation is a single self-contained HTML file — no installs, no accounts, just open and use.

---

## How to contribute

Got a simulation? Submit it.  
Read the full guide → **[CONTRIBUTING.md](./CONTRIBUTING.md)**

**Know GitHub?**

Short version:
1. Fork the repo
2. Add your `.html` file under `simulations/branch/subject/`
3. Add one entry to `data/simulations.json`
4. Open a PR

**Don't know GitHub?**  
Use the [Google Form](https://docs.google.com/forms/d/e/1FAIpQLSfjeQurmGfM2b1tTWiUerO8hFphvBtzSWCPCmU2-r54lnVuAg/viewform?usp=header) — we'll handle the rest.

---

## Run locally

```bash
git clone https://github.com/jidukrishna/ktu_simulator.git
cd ktu_simulator
python -m http.server
```

Open `http://localhost:8000`

> Direct file open (`file://`) won't work — the page fetches `data/simulations.json` which needs a server.

---

## Stack

Vanilla HTML, CSS, JS. No frameworks, no build step, no dependencies.  
Hosted on GitHub Pages.

---

Built by [jidu.dev](https://jidu.dev) · KTU RSET
