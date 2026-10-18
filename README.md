# MMAgrid

Komplett webbplats i en enda fil: `index.html`. Ingen server, databas eller installation behövs.

## Öppna lokalt
Dubbelklicka på `index.html`.

## Lägg upp gratis med egen webbadress
- **Netlify:** gå till app.netlify.com/drop och dra in den här mappen. Du får en länk som `något.netlify.app`.
- **Cloudflare Pages:** "Direct upload" ger en länk som `något.pages.dev`.
- **GitHub Pages:** lägg `index.html` i ett repo och slå på Pages.
- **Egen domän:** köp en hos en registrar (t.ex. Loopia eller Namecheap), lägg till den under
  "Custom domain" i tjänsten och sätt in de DNS-poster tjänsten visar. HTTPS ordnas automatiskt.

## Uppdatera innehållet
Mappen `source/` innehåller allt som behövs för att bygga om sidan:
- `data.json` – ranking, rekord och kommande matcher för alla viktklasser
- `template.html` – sidans kod, inklusive statistik (`STATS`) och highlights (`HIGHLIGHTS`)
- `hero.jpg` – startbilden
- `build.py` – kör `python3 build.py` för att skapa en ny `index.html`

## Bra att veta
- Sidorna nås via hash-adresser (`/#/ranking`), så inga serverinställningar krävs.
- Forumfliken fungerar bara när sidan öppnas via claude.ai. På andra adresser visas ett meddelande
  om det (en länk till t.ex. Discord kan läggas in via `COMMUNITY_URL` i `template.html`).
- Statistiken kommer från UFC.com/UFCStats via Kaggle-databasen "UFC Fighters Database 2026" (juni 2026).
