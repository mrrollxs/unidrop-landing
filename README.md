# UniDrop landing page

Struttura pronta per GitHub Pages: `index.html` + `style.css` (home), più `download/index.html` (pagina di download, raggiungibile come `getunidrop.app/download/`).

## Immagini da aggiungere in `images/`

Il codice referenzia questi file — mettili nella cartella `images/` con questi nomi esatti (o modifica i `src` in `index.html` se preferisci nomi diversi):

| File | Dove appare |
|---|---|
| `hero-icon.png` | Icona grande nel riquadro della Hero |
| `icon-link.png` | Card "Share Anywhere, with a Link." |
| `icon-nearby.png` | Card "Effortless Nearby Sharing." |
| `icon-clipboard.png` | Card "Your Clipboard, On Command." |
| `icon-apple.svg` | Cerchio Apple (sezione Download) |
| `icon-android.svg` | Cerchio Android (sezione Download) |
| `icon-windows.png` | Cerchio Windows (sezione Download) |
| `icon-download.svg` | Freccina nel pulsante Download |
| `icon-mail.svg` | Icona email (footer) |
| `favicon.png` | Icona nella tab del browser (opzionale) |

## Link da sostituire

In `index.html`, cerca i commenti `<!-- SOSTITUISCI ... -->`:
- pulsante Download → già impostato su `download/` (la pagina interna, non serve modificarlo)

## Da completare in `download/index.html`

Questa pagina ha ancora dei placeholder da riempire prima del deploy:
- `[INSERISCI QUI IL TUO LINK APP STORE PER iOS]` → link reale App Store
- `[INSERISCI QUI IL TUO LINK APP STORE PER macOS]` → link reale Mac App Store
- I link Windows (Microsoft Store) e Android (beta Google Play + Google Group) sono già inseriti
- indirizzo email footer → già impostato su `unidrop.app@gmail.com`
- Privacy Policy / Terms & Conditions → già impostati sui tuoi link Gist

## Deploy su GitHub Pages con dominio custom

1. Crea un repository pubblico su GitHub (es. `unidrop-landing`)
2. Carica dentro `index.html`, `style.css` e la cartella `images/`
3. Aggiungi un file chiamato `CNAME` (senza estensione) nella root del repo, contenente solo:
   ```
   getunidrop.app
   ```
4. Vai su **Settings → Pages** del repo → Source: `main` branch, cartella `/ (root)`
5. Sul pannello DNS del tuo dominio (dove lo hai registrato), imposta:
   - Record **A** su `@` verso: `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - (opzionale) record **CNAME** su `www` verso `tuo-username.github.io`
6. Nelle impostazioni Pages di GitHub, spunta "Enforce HTTPS" una volta che il DNS si è propagato (può richiedere qualche ora)
