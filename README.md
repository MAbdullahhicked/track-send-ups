# Track Send-Up

A single-page study tracker for the Class X (SSC) send-up scope, session 2026–27.

The whole app lives in `index.html` — no dependencies, no build step, no backend. Open the
file in a browser or serve it as a static site and it works.

## What it covers

| Paper | Scope |
| --- | --- |
| Mathematics | Chapters with their textbook exercises |
| English | Chapters and texts |
| Pakistan Studies | Book I and Book II |
| Chemistry | Theory plus the nine PBA practicals |
| Computer Science | Theory plus the Computer PBA topics |
| Urdu | Prose, poems, ghazals, plus creative-writing notes |
| Tarjuma Tul Quran | Surahs and concepts |
| Physics | Chapters and practicals |

Every entry is a checkbox. The header totals everything ticked, each tab shows its own
progress, the study log in the footer compares all papers, and a countdown runs to the next
paper on the date sheet.

## Features

- Tick tracking for every chapter, text, surah and practical
- Exercise-level tracking for Mathematics, with chapter ticks synced to their exercises
- Per-paper progress bars and an overall total in the study log
- Next-paper card with a live countdown and the full date sheet
- Tab that reopens on the page you were last using
- State saved in `localStorage`, so it survives a reload in the same browser
- Responsive layout with light print styling

## Running locally

Open `index.html` directly, or serve the folder:

```sh
python -m http.server 8000
```

Then visit <http://localhost:8000>.

## Deploying

Static hosting is enough — no configuration required.

On Vercel: import this repository, choose **Other** as the framework preset, leave the build
command and output directory empty, and deploy. `index.html` is served at the root.

## Notes

Progress is stored per browser in `localStorage`; it is not synced between devices or
cleared by clearing site data. Exam dates follow the school's date sheet.
