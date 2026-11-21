# Next-Token Lab

Ten pages: `index.html` (start page, the machine and the notebook), one page per module from `m1-access.html` to `m8-backend.html`, and the attention deep dive, `m2b-attention.html`. Each file is self-contained: no outside scripts, fonts or trackers, and no network calls except Module 8's backend, which sends only when a student presses its button.

## Put it online with GitHub Pages
1. Sign in at github.com and create a new public repository, for example `next-token-lab`.
2. On the repository page, choose "uploading an existing file", drag in all ten `.html` files, and commit.
3. Open Settings, then Pages. Under "Build and deployment", choose "Deploy from a branch", pick the `main` branch and the `/ (root)` folder, and save.
4. After a minute or two the site is live at `https://YOUR-USERNAME.github.io/next-token-lab/`. Share that address.

Keep all the pages in the same folder of the same site: that is what lets them share one notebook.

## Settings
Each page's script begins with the same settings block (search for `instructorEmail`). If you change a setting, change it in all ten files (a find-and-replace across the folder does it).
- `instructorEmail`: where "Send progress" addresses reports. Currently aes95@pitt.edu.
- `teachback`: where teach-back prompts go. Currently ChatGPT. UPMC devices redirect ChatGPT to Copilot; switch both the name and the address if your students work there.
- `mailLimit`: how long the emailed summary can be.

## What gets saved
Everything a student does is kept in their notebook: notes, checklists, every teach-back draft and attempt, the exact prompt the lab built, the raw reply they pasted (including replies the lab couldn't read), their disagreements, notes on their model, and a capture log of every paste. "Download my lab state" (Start page, notes drawer, send dialog, and the model) saves all of it as one JSON file, which also restores the notebook later.

## The machine
A runnable, zoomable model of a language model, opened from "The machine" on every page and shown inline on the Start page: a context line of tokens, an embedding cube per token, residual lanes, four drawn layers of attention heads and neurons (standing in for 32), unembedding, softmax and the pick, which loops back into the context. Every part opens to an explanation, clickable math with live worked examples, and a notes box. Status lights show mastery from the teach-backs, and "Light by mastery" dims what isn't mastered yet.

## How saving works
Each student's notebook lives in their own browser, for this site only. Clearing browser data, switching devices, or using a private window loses it, unless the student downloads a backup from the Start page and restores it later. Nothing is sent anywhere until the student chooses a send option, and then it opens as a draft email they can read first.

When you preview a page inside Claude, it saves to Claude's preview storage instead, and the links between pages won't work until the pages are hosted together.
