# FitQuest ⚡

A simple, mobile-first fitness habit tracker. No build step, no dependencies, no accounts. Your data stays in your own browser (`localStorage`).

## Features
- **Progress summary on top:** day streak, weekly completion %, active days this month, total goals smashed, a 7-day bar chart and a 4-week heatmap.
- **Daily log:** per-exercise counters with goal progress bars, plus water, sleep, weight, energy and a short note.
- **Fully editable exercises:** rename, change goal, unit and step size, add or remove anytime. Past logs are preserved.
- **Back-date:** tap any bar or heatmap square (or use the date arrows) to log another day.
- **Backup / Restore:** export your data to JSON and import it on another device.
- **Daily wisdom:** a rotating principle from training traditions worldwide.
- **Installable and offline:** works as a home-screen app once opened online.

## Repo contents
| File | Purpose |
|---|---|
| `index.html` | The whole app (HTML, CSS, JS) |
| `manifest.webmanifest`, `icon.svg` | Home-screen install support |
| `sw.js` | Offline cache |
| `.github/workflows/pages.yml` | Auto-deploys to GitHub Pages on every push to `main` |
| `.nojekyll` | Tells Pages to serve files as-is |
| `LICENSE`, `.gitignore` | MIT license and housekeeping |

## Run locally
Open `index.html` in a browser. (Install and offline features need the hosted `https` version.)

## Deploy on GitHub Pages
1. Create a new repository (e.g. `fitquest`) and upload **all** files, including the `.github` folder. Dragging the unzipped folder contents into GitHub's "Upload files" page works, or use git:
   ```bash
   git init && git add . && git commit -m "FitQuest"
   git branch -M main
   git remote add origin https://github.com/<you>/fitquest.git
   git push -u origin main
   ```
2. In the repo go to **Settings → Pages**, and under **Source** choose **GitHub Actions**.
3. The workflow runs on the next push (or open the **Actions** tab and run "Deploy to GitHub Pages" manually). Your tracker goes live at `https://<you>.github.io/fitquest/`.
4. On your phone, open the link and choose **Add to Home Screen**.

*No Actions? Alternative:* skip the workflow, set Pages source to **Deploy from a branch** → `main` / root.

## Your data
Stored per browser and per device. Use **Backup** regularly and **Restore** to move between devices. Clearing site data erases your logs.

## Customize
Default exercises live in the `DEFAULT` object near the top of the script in `index.html`; the daily wisdom list is `WISDOM`. Colors are CSS variables under `:root`.

## License
MIT
