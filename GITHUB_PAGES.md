# GitHub Pages
*OBS! att repot måste vara publikt :)*

### Börja med:
https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site

Vill välja branchen gh-pages. 

Finns gh-pages inte? Testa konfigurera om lite på repots settings --> Actions --> General. Klicka i read and write under Workflow permissions, samt allow github actions to create and approve pull request.

### .github --> workflows --> deploy.yml
Behöver också ha en mapp i roten av projektet som heter `.github` --> med en mapp `workflows` --> med fil `deploy.yml`. För innehål i deploy.yml, kolla exempel i detta repo. OBS! Bredvid mappen workflows (dvs på samma nivå i mappen .github) har vi en fil .keep (tom på innehåll).

### Konfig för vite + github pages:
https://vitejs.dev/guide/static-deploy.html#github-pages

- Basically: skapa en fil `vite.config.js`
- Klistra in:
```
import { defineConfig } from "vite";
export default defineConfig({ base: "/inlamningsuppgift-1-Ayngie/", build: { target: "esnext" } });

```
*OBS! Glöm ej byta ut namnet på repot :)*

### No build?
1. Kan behöva cleara cachen på sidan: *Kan behöva rensa cachen för att det ska funka om man öppnat upp githubpagessidan o den inte laddades helt*...
Gör det genom att:
- öppna upp sidan där den deployas
- öppna inspect
- välj fliken network
- klicka i disable cache och OBS! med denna iklickad - uppdatera sidan!
- Därefter kan vi klicka ur den o så ska det funka.

2. Samt kan behöva köra om alla deploy workflows: på pages build and deployment --> re-run all jobs.

### Länka in css/scss
Länka in CSS:en/Sass via main.ts istället, så får du garanterat en korrekt komprimering av koden vid publicering :)
I vite: i main.js: `import "../scss/index.scss";`

---

