# Tips for setting up a new project

## config
https://github.com/postmodernistx/configs

---

## Readme
##### Guide för att skapa readme:
https://readme.so/

##### Hur infoga bild i readme:n
https://stackoverflow.com/questions/14494747/how-to-add-images-to-readme-md-on-github

##### Github Docs - Basic writing and formatting syntax
https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax

##### emoji-cheat-sheet 
https://github.com/ikatyang/emoji-cheat-sheet/blob/master/README.md

##### Shields / badges 

---

## Git commits 

##### Conventional commits
https://www.conventionalcommits.org/en/v1.0.0/

##### Gitmojis
https://gitmoji.dev/

---

## SCSS
##### BEM
https://github.com/Carowa27/TS_Group-assignments_potion-shop/blob/main/src/scss/_landingpage.scss

---

## Accessibility
a11y:
https://www.a11yproject.com/checklist/

---

## GitHub Pages
*OBS! att repot måste vara publikt :)*

##### Börja med:
https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site

##### Konfig för vite + github pages:
https://vitejs.dev/guide/static-deploy.html#github-pages
*(välj roots?)*

- Basically: skapa en fil `vite.config.js`
- Klistra in:
```
import { defineConfig } from "vite";
export default defineConfig({ base: "/inlamningsuppgift-1-Ayngie/", build: { target: "esnext" } });

```
**OBS 1!** - *Glöm ej byta ut namnet på repot :)*

**OBS 2!** - *Kan behöva rensa cachen för att det ska funka om man öppnat upp githubpagessidan o den inte laddades helt*...
Gör det genom att:
- öppna upp sidan där den deployas
- öppna inspect
- välj fliken network
- klicka i disable cache och OBS! med denna iklickad - uppdatera sidan!
- Därefter kan vi klicka ur den o så ska det funka.

##### Länka in css/scss
Länka in CSS:en/Sass via main.ts istället, så får du garanterat en korrekt komprimering av koden vid publicering :)
I vite: i main.js: `import "../scss/index.scss";`

---

## INSPO
### Medieinstitutet repon
https://github.com/orgs/Medieinstitutet/repositories

## Tips för juniorer
https://github.com/postmodernistx/career-advice-for-juniors
