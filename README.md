# Nour SFAR · 3D Portfolio

An interactive 3D portfolio where my education, career and certifications are told as **one AI system that grows with each role** — from the academic foundations underground to a production stack on Microsoft Azure.

**Live:** https://YOUR-APP-NAME.azurestaticapps.net  <!-- replace after the first deployment -->

![Intro view](docs/preview-intro.png)

## The tour

| Chapter | What you see |
|---|---|
| Education | ESSAI and IPEIT as rock layers under the platform, with projects and certificates as crystals |
| GOMYCODE | A live workshop stage — teaching and pitching AI |
| HARINGTON | A RAG library feeding two healthcare AI assistants (nearcare) |
| Freelance | A multi-agent orchestrator behind a secure API gateway |
| ADACTIM · WEVIOO | The enterprise layer: Azure AI Foundry, ITIL, automation |
| Azure | The whole stack lifts into the cloud, with AZ-104, AI-103, AB-100 and GH-300 |
| Beyond the job | Security rings and my LinkedIn series on AI engineering |

![Azure chapter](docs/preview-azure.png)

**Controls:** ← → or Space to move · **T** guided tour · **V** 2D mode · **F** full screen · drag to look around · click labels for details.

## Tech

- **Three.js** — scene, procedural textures, CSS2D labels
- **GSAP** — camera flights and scene animations
- **Vite** + `vite-plugin-singlefile` — builds to one self-contained `index.html` (no external requests)
- **Azure Static Web Apps** (Free plan) — hosting, HTTPS and security headers (`staticwebapp.config.json`)
- Accessible fallback: 2D mode, auto-enabled when WebGL is unavailable

## Run locally

```bash
npm install
npm run dev      # http://localhost:5173
npm run build    # outputs dist/index.html
```

## Deploy

Pushed to `main` → GitHub Actions → Azure Static Web Apps.
Build settings: app location `/`, output location `dist`, no API.

## Structure

```
src/
  main.js        renderer, camera, navigation, panel, tour, 2D mode
  world.js       the 3D world: platform, strata, career layers, Azure cloud
  slides.js      chapter content
  style.css      UI
  logos/ badges/ brand assets (see note below)
staticwebapp.config.json   Azure headers & routing
```

## Notes

Content is based on my public LinkedIn profile. Company logos, school logos and certification badges belong to their respective owners and are used only to identify my education, employers and earned certifications. Code is MIT-licensed.

Contact: [LinkedIn](https://www.linkedin.com/in/nour-sfar)
