# ResumeMachine

Tailor your resume to any job posting using the AI assistant you already have: Claude, ChatGPT, or Gemini.

**Live page:** https://peterselj.github.io/resumemachine/

There's no app or backend here. The site is a static page plus one instructions file:

| File | What it is |
|---|---|
| `index.html` | The human-facing page: one-line setup, manual setup per assistant, tips |
| `resumemachine.md` | The product. Part 1 is a setup walkthrough an AI follows; Part 2 is the working instructions users paste into their Project / GPT / Gem |
| `llms.txt` | Pointer for AI assistants that land on the site root |
| `.nojekyll` | Tells GitHub Pages to serve the `.md` file as raw text instead of converting it to HTML |

To change how ResumeMachine behaves, edit Part 2 of `resumemachine.md`. To change setup steps, edit Part 1 and the matching tab in `index.html`.

## Making changes

`main` is what's live, so changes go through a branch and a pull request:

1. Create a branch (in VS Code: click the branch name in the bottom-left corner, then "Create new branch").
2. Make changes and preview them locally: run `python3 -m http.server 8000` in this folder and open http://localhost:8000.
3. Commit, push the branch, and open a pull request on GitHub. The PR template has a short checklist.
4. The **Check site** workflow runs automatically on every PR and catches broken links to the instructions file and malformed HTML.
5. Merge when it looks good. The live site updates a minute or two later.

Working with Claude? `CLAUDE.md` tells it how this repo works, including "branch and PR, never push to main."
