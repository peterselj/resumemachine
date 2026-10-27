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
