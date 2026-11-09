# mtravascio.github.io

Sito personale, pubblicato da GitHub Pages all'indirizzo **https://mtravascio.github.io/**.
Una pagina sola, scritta a mano in HTML e CSS, senza framework, senza JavaScript,
senza cookie né font di terze parti oltre a Google Fonts.

## Com'è fatto

```
index.html              tutta la pagina
assets/css/style.css    un solo foglio di stile
assets/img/libri/       le copertine dei 18 libri (440 px di larghezza)
assets/img/ebook/       sei copertine dei manuali tradotti (300 px)
.nojekyll               dice a GitHub di servire i file così come sono, senza Jekyll
```

Le sezioni di `index.html` sono commentate (`<!-- ============ APP ============ -->`):
si trova la parte da cambiare cercando il titolo della sezione.

## Modificare

1. Apri `index.html` e cambia il testo, oppure aggiungi un blocco copiando uno di
   quelli vicini.
2. Per una copertina nuova: metti il JPG in `assets/img/libri/`, largo **440 px**,
   e aggiungi un `<a class="book">…</a>` nella griglia giusta.
3. Anteprima locale:

   ```bash
   python3 -m http.server 8000    # poi http://localhost:8000
   ```

4. Pubblica:

   ```bash
   git add -A && git commit -m "Aggiornato il sito" && git push
   ```

   GitHub Pages impiega 20–40 secondi.

## Dove sono i contenuti

| Cosa | Dove |
|---|---|
| App (3) | sezione `01 · App` — link a Google Play e App Store |
| Libri (18) | sezione `02 · Libri`, tre gruppi: *Salva la tua anima*, *Equilibrio e Spirito*, *Open Edition* |
| Manuali tradotti (139) | sezione `03 · Traduzioni` |
| Siti (6) | sezione `04 · Siti` |
| Progetti open source | sezione `05 · Codice` |
| Contatti | sezione `06 · Contatti` |

I link ai libri sono le schede Kindle su Amazon (`amazon.it/dp/ASIN`); la pagina
autore è `amazon.it/Massimo-Travascio/e/B0GCXYGBWJ`.

## Numeri da tenere aggiornati

Nella copertina ci sono quattro numeri: **18** libri, **3** app, **139** manuali,
**5** siti. Quando cambiano vanno corretti a mano in `index.html` (cerca `class="fact"`).

## Note

- Il sito è volutamente **senza JavaScript**: non c'è niente da tracciare.
- I font arrivano da Google Fonts; se si vuole togliere anche quella dipendenza
  basta scaricare i tre caratteri in `assets/fonts/` e cambiare `@font-face`.
- Non c'è un `CNAME`: il sito vive sul dominio `mtravascio.github.io`. Il dominio
  `iveatorino.it` è un altro repository (`mtravascio/iveatorino`).
