# Resume site

A single-page, responsive resume/portfolio site. No build step, no dependencies, no tracking.

## Files

| File | What it does |
| --- | --- |
| `index.html` | All your content (text, links, sections) |
| `styles.css` | Colors, spacing, layout, dark mode, print styles |
| `resume.pdf` | Optional: drop your PDF here so "Download résumé" works |

## How to edit

1. Open `index.html` in Notepad, VS Code, or any editor.
2. Replace the placeholder text: `Your Name`, `you@example.com`, `+1 (000) 000-0000`,
   `City, Country`, and the LinkedIn/GitHub/Website URLs.
3. Duplicate an `<li class="timeline-item">` block to add a job.
   Duplicate an `<article class="card">` block to add a project.
4. Save and refresh the browser.

To change the accent color, edit `--accent` in the `:root` block at the top of
`styles.css`. Dark mode colors are in the `[data-theme="dark"]` block right below it.

## Preview it

Double-click `index.html`. That's it.

To preview over a local server (closer to production):

```powershell
cd "$env:USERPROFILE\Desktop\resume-site"
python -m http.server 8000
# then open http://localhost:8000
```

## Features

- Fully responsive (desktop, tablet, phone) with a proper mobile menu
- Light / dark theme toggle, remembered across visits, respects OS preference
- Sticky header with scroll-spy navigation
- Subtle scroll animations, disabled automatically for reduced-motion users
- Accessible: skip link, semantic landmarks, visible focus states, ARIA labels
- "Save PDF" button with a dedicated print stylesheet (clean, ATS-friendly output)
- Copy-email button
- Zero external requests — fonts are the system UI font, so it loads instantly

## Deploy it free

**GitHub Pages**
1. Create a repo, upload `index.html` + `styles.css` (and `resume.pdf`).
2. Settings → Pages → Source: `main` branch, `/` root.
3. Your site is live at `https://<username>.github.io/<repo>/`.

**Netlify / Vercel**
Drag the `resume-site` folder onto the Netlify dashboard, or run `vercel` in the folder.

**Custom domain:** add a `CNAME` file containing your domain, then point a CNAME DNS record to your host.

## Generate your PDF résumé

Click **Save PDF** in the header → in the print dialog choose *Save as PDF* →
enable *Background graphics* for the best result. Margins are already handled.
