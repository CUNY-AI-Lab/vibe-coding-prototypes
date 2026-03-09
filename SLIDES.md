# SLIDES.md — Vibe-Coding Prototypes

## CAIL Spotlight Workshop #2

Companion to `index.html`. Keep this file in sync whenever slide titles or text content change.

* * *

## Slide 1 — Title

**Label:** CAIL Spotlight Workshop #2
**Title:** Vibe-Coding Prototypes
**Date:** Tuesday, March 10, 4:00–5:30 pm
**Stage:** Chladni Figures artifact (`src/chladni.html`)

* * *

## Slide 2 — Agenda

**Label:** Workshop
**Title:** Agenda

**Stage (agenda table):**

Part 1 — Setup:
- Install Homebrew / Node.js
- Install and launch Gemini CLI

Part 2 — Agentic Workflows:
- Reorganize the folder with approval
- Establish an agent workflow
- Create `AGENTS.md`
- Verify the reorganized project

Part 3 — Prototype + Publish:
- Customize the focus timer
- Authenticate with GitHub CLI
- Create remote repository
- Push to GitHub
- Deploy to GitHub Pages

* * *

## Slide 3 — Section Break

**Tag:** Part 1
**Title:** Setup

* * *

## Slide 4 — Install Homebrew / Node.js

**Label:** Setup
**Title:** Install Homebrew / Node.js

**Stage (stageCompare):**

- **macOS — Terminal:**
  1. Install Homebrew from brew.sh
  2. Add Homebrew to PATH
  3. Confirm with `brew --version`

- **Windows — PowerShell:**
  1. Install Node.js LTS from nodejs.org
  2. Reopen PowerShell
  3. Confirm with `node --version`

* * *

## Slide 5 — Gemini CLI Setup

**Label:** Setup
**Title:** Install and Launch Gemini CLI

**Stage (step-grid, fragments):**
1. Install Gemini CLI
2. Run `gemini`
3. Complete login
4. Return to the terminal
5. Confirm Gemini is ready for prompts

* * *

## Slide 6 — Section Break

**Tag:** Part 2
**Title:** Agentic Workflows

* * *

## Slide 7 — Directory Reorganization Demo

**Label:** Demo
**Title:** Reorganize the Folder with Approval
**Download:** `src/project-prototype.zip` — functional but messy focus timer (11 files, flat)

**Stage (stageCenter, fragments):**
- **Big:** Unzip the starter folder — it's intentionally messy.
- Ask Gemini to inspect, propose a plan, and reorganize with approval:
  - `index.html`
  - `css/style.css`
  - `js/main.js`
  - `assets/icon.svg`
  - `assets/config.json`

* * *

## Slide 8 — Establish an Agent Workflow

**Label:** Demo
**Title:** Establish an Agent Workflow

**Stage (stageCenter):**
- **Big:** Before making changes, the agent must propose a plan and wait for approval.
- **Prompt:** "Inspect this folder. Propose a plan before changing anything."
- **Prompt:** "Do not create, move, or delete files until I approve the plan."

* * *

## Slide 9 — Agentic Documentation

**Label:** Tool
**Title:** Create `AGENTS.md`

**Stage (step-grid, fragments):**
1. State the project overview and purpose
2. Define file structure and code style conventions
3. Include build, test, and setup commands
4. Add anything you'd tell a new teammate

* * *

## Slide 10 — Verify the Reorganized Project

**Label:** Demo
**Title:** Verify the Reorganized Project

**Stage (step-grid, fragments):**
1. Open `index.html` in the browser
2. Confirm the focus timer still works
3. Check that styles, scripts, and assets load correctly
4. Review the clean file tree: `css/`, `js/`, `assets/`

* * *

## Slide 11 — Section Break

**Tag:** Part 3
**Title:** Prototype + Publish

* * *

## Slide 12 — Customize the Focus Timer

**Label:** Demo
**Title:** Customize the Focus Timer

**Stage (step-grid, fragments):**
1. Prompt Gemini to add a feature — e.g. session history, sound alerts, or custom intervals
2. Keep changes in the right files: CSS in `css/`, JS in `js/`
3. Test locally in the browser
4. Revise one change at a time
5. Keep the app simple enough to publish today

* * *

## Slide 13 — Authenticate with GitHub CLI

**Label:** Publish
**Title:** Authenticate with GitHub CLI

**Stage (step-grid, fragments):**
1. Install GitHub CLI (`brew install gh` on macOS, `npm install -g gh` on Windows)
2. Run `gh auth login`
3. Choose GitHub.com → HTTPS → Login with a web browser
4. Complete authentication in the browser
5. Confirm with `gh auth status`

* * *

## Slide 14 — Create Remote Repository

**Label:** Publish
**Title:** Create Remote Repository

**Stage (step-grid, fragments):**
1. Initialize git locally: `git init`
2. Create the repo on GitHub: `gh repo create REPO --public --source=.`
3. Confirm the remote is set: `git remote -v`

* * *

## Slide 15 — Push to GitHub

**Label:** Publish
**Title:** Push to GitHub

**Stage (step-grid, fragments):**
1. `git add .`
2. `git commit -m "first prototype"`
3. `git push`

* * *

## Slide 16 — Enable GitHub Pages

**Label:** Publish
**Title:** Enable GitHub Pages

**Stage (step-grid, fragments):**

1. Go to `github.com/USERNAME/REPO`
2. Click the **Settings** tab
3. Click **Pages** in the left sidebar
4. Under **Source**, select **Deploy from a branch**
5. Choose **main** → **/ (root)** and click **Save**
6. Visit `USERNAME.github.io/REPO`

* * *

## Slide 17 — Resources

**Label:** Resources
**Title:** Links & References

**Stage (link list):**
- [ailab.gc.cuny.edu](https://ailab.gc.cuny.edu) — CUNY AI Lab — home page, announcements, and model notes
- [ailab.gc.cuny.edu/resources](https://ailab.gc.cuny.edu/resources) — CAIL Resources — guides, readings, and workshop materials
- [chat.ailab.gc.cuny.edu](https://chat.ailab.gc.cuny.edu) — CAIL Sandbox (Open WebUI) — GLM 5, Kimi K2.5, and more
- [tools.ailab.gc.cuny.edu](https://tools.ailab.gc.cuny.edu) — CAIL Tools — additional lab utilities and experiments
- [newmedialab.cuny.edu](https://newmedialab.cuny.edu) — CUNY New Media Lab — workshop series host
- [aitoolkit.gc.commons.edu](https://aitoolkit.gc.commons.edu) — GC AI Toolkit — curated tools and resources for the Graduate Center community
- [github.com/cuny-ai-lab](https://github.com/cuny-ai-lab) — CUNY AI Lab on GitHub — open source repos, workshop decks, datasets
- [cuny-ai-lab.github.io/gen-dev-foundations](https://cuny-ai-lab.github.io/gen-dev-foundations/) — Foundations Workshop deck — companion CAIL workshop #1
- [code.visualstudio.com/docs](https://code.visualstudio.com/docs) — VS Code documentation — setup, extensions, integrated terminal
- [github.com/google-gemini/gemini-cli](https://github.com/google-gemini/gemini-cli) — Gemini CLI — open-source AI coding agent that runs in your terminal
- [docs.github.com](https://docs.github.com) — GitHub documentation — repos, Pages, pull requests, Actions

* * *

_Last synced: 2026-03-09. Deck has 17 slides. Update both this file and `index.html` together._
