# EduPath — Your Personalized Academic & Career Roadmap

A responsive, single-file-origin HTML/CSS/JavaScript academic and career roadmap demo, now organized into separate files for easier explanation and maintenance.

## Project structure

```text
EduPath/
├── index.html
├── css/
│   └── style.css
├── js/
│   ├── data.js
│   └── app.js
└── README.md
```

## Run in VS Code

1. Extract the `EduPath` folder.
2. Open the folder in VS Code.
3. Install the **Live Server** extension (or open `index.html` directly in a browser).
4. Right-click `index.html` → **Open with Live Server**.
5. Register a demo account using a name, email, and password of at least 6 characters. Do not use a real or reused password.
6. Complete the profile, generate a roadmap, mark steps complete, and open Resources.

## What each file does

- **index.html** — page structure, main app containers, and links to the CSS and JavaScript files.
- **css/style.css** — all visual styling, layout, colors, and responsive mobile/tablet rules.
- **js/data.js** — career pathway data: descriptions, skills, roadmap steps, and resource links.
- **js/app.js** — application logic: registration/login demo, profile handling, career matching, roadmap generation, progress tracking, resource checks, navigation, and rendering.

The two JavaScript files are loaded in this order: `data.js` first, then `app.js`. Keep that order because `app.js` uses the career data declared in `data.js`.

## Important demo limitations

- **Demo authentication only:** passwords are stored in browser `localStorage` and are not hashed. Use only throwaway demo credentials. This is not production-safe authentication.
- Data remains in the same browser profile on the same device and can be cleared by clearing site data. There is no multi-device sync or server database.
- Recommendations are deterministic rules, not a live AI model. Resource set is curated/static, not live search.
- URL checks are basic heuristics. HTTPS/domain matching does not establish trust, verify page content, or check malware reputation. Price labels are not live-verified.
- No real job feed or mentor matching is implemented.

## 90-minute demo schedule

- 0–10 min: extract, open, and run the project.
- 10–20 min: test registration/login and local persistence.
- 20–35 min: complete a profile and demonstrate career matching.
- 35–50 min: show roadmap sequencing and completion tracking.
- 50–60 min: show resource source labels and trust limitations.
- 60–75 min: test mobile width, empty profile, and logout/login.
- 75–90 min: rehearse the demo and prepare report/poster explanation.

## Production upgrade path

1. Replace localStorage authentication with Supabase Auth; never store plaintext passwords.
2. Add database tables and row-level security for profiles, roadmap steps, and progress.
3. Move link/reputation checks to a server-side endpoint and use a reputable security API only after reviewing terms, quotas, and privacy.
4. Add live job/course search from documented official APIs; do not describe static sample data as live.
5. Add an LLM server-side only as an optional explanation layer, grounded in approved resource records. Never trust an AI-generated URL without separate validation.

## Deployment note

This is a static website and can be published using GitHub Pages, Netlify, or another static hosting service. Upload the complete folder structure—not just `index.html`—so the CSS and JavaScript files load correctly. After deployment, test registration, profile saving, roadmap generation, and resource links on the published URL.

**Note:** The original demo behavior and visual design have been kept; the code has only been separated into files.
