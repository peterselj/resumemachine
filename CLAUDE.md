# ResumeMachine

Static GitHub Pages site (no build step) that helps job seekers set up a resume-tailoring workspace in their own AI assistant. Live at https://peterselj.github.io/resumemachine/ and deployed automatically from `main`.

## Workflow

- Never commit directly to `main`. Work on a branch, open a pull request, and let the owner review and merge. Merging to `main` publishes to the live site within a couple of minutes.
- Keep each PR to one idea. Fill in the PR template.
- The `Check site` workflow runs on every PR; keep it green.
- The owner is a novice developer: explain changes in plain language in PR descriptions.

## Files

- `resumemachine.md` is the product. Part 1 is a setup walkthrough an AI assistant follows; Part 2 is the working instructions users paste into a Project / GPT / Gem.
  - Part 1 tells assistants to copy "from `# Part 2: Working instructions` to the end of the file". Don't rename that heading or add content after Part 2.
  - It must work for Claude, ChatGPT, Gemini, and others. Don't add features only one assistant supports without a fallback.
  - Versioning: when Part 2 changes, bump the version in both the "Current version" line under What's new and the version line at the top of Part 2, and add a one-line What's new entry written for users. Installed copies use this to detect updates; the `Check site` workflow fails if they disagree.
  - Nothing is hidden from humans. The file is written to be readable by both people and AIs.
- `index.html` is the human page: plain HTML/CSS/JS in one file, no frameworks. The setup tabs must stay in sync with Part 1.
- `llms.txt` points AI assistants to the instructions. `.nojekyll` keeps GitHub Pages from converting the `.md` to HTML; don't delete it.

## Style

Matches the JobBoard repo (peterselj/JobBoard): Hanken Grotesk + IBM Plex Mono, forest green (`#234c3a`) on warm paper (`#f3f3ee`), white cards with 12px radius, 6px-radius buttons. Colors are CSS variables at the top of `index.html`, with a dark-mode set; change both together. Check layout at 390px wide (phone) with no horizontal scroll.

## Preview locally

`python3 -m http.server 8000`, then open http://localhost:8000.
