# Farm Biosecurity Designer

Simulatore didattico 2D per costruire planimetrie di allevamenti e discutere la biosicurezza.

## Funzioni

- Edifici, stanze, corridoi, pavimentazioni, zone di lavaggio, filtri sanitari e quarantena.
- Griglia metrica (20 pixel = 1 metro); aggancio alla griglia e ai bordi degli elementi.
- Ridimensionamento tramite maniglia, trascinamento e rotazione di 90° (eccetto porte/segmenti).
- Pareti condivise: i muri dei locali adiacenti sono disegnati una sola volta.
- Porte ancorate alle pareti dei locali e aperture rappresentate lungo i muri (clic vicino al muro).
- Analisi dei collegamenti locali/ingressi tramite porte e verifiche orientative di biosicurezza.
- Download/caricamento dei progetti in JSON; stampa/esportazione PDF dal browser.
- Nessun account, backend, servizio esterno o libreria CDN.

## Uso locale

Aprire `index.html` con un browser moderno. I file `index.html` e `app.js` devono essere nella stessa cartella.

## Pubblicazione su GitHub Pages

1. Accedi a [GitHub](https://github.com) e crea un nuovo repository, ad esempio `farm-biosecurity-designer`, scegliendo visibilità **Public**.
2. Carica nella **radice** del repository i file `index.html`, `app.js`, `.nojekyll` e `README.md` (puoi usare **Add file → Upload files**).
3. Conferma con **Commit changes**.
4. Apri **Settings → Pages** e imposta **Build and deployment → Deploy from a branch**, poi **Branch: main** e cartella **/(root)**; fai clic su **Save**.
5. Dopo la pubblicazione, il simulatore sarà disponibile su `https://NOMEUTENTE.github.io/farm-biosecurity-designer/` sostituendo `NOMEUTENTE` con l'account GitHub.

Se scegli un repository con altro nome, anche la parte finale del link cambia. Su GitHub Pages pubblico il codice e le risorse del sito sono visibili a tutti.

## Utilizzo didattico

Ogni studente può disegnare un allevamento e scaricare il proprio progetto JSON, da poter riaprire e correggere. Può inoltre salvare la vista come PDF usando il pulsante **Stampa / salva PDF** e scegliendo **Salva come PDF** nel browser. Non avviene alcun caricamento dei progetti su un server.

**Limiti della valutazione:** l'algoritmo rileva porte collegate a muri e raggiungibilità geometrica dei locali, ma non rappresenta persone, animali, direzione dei flussi, ingressi controllati, requisiti specifici per specie, né conformità legale. Il controllo della presenza di un filtro sanitario non prova che ogni percorso lo attraversi: per questo la valutazione va usata come spunto di discussione e non come certificazione.

## Struttura

- `index.html`: interfaccia e stile, inclusa la vista di stampa.
- `app.js`: editor vettoriale SVG, connessioni, salvataggio JSON e verifiche didattiche.
- `.nojekyll`: disabilita l'elaborazione Jekyll in GitHub Pages.

## Licenza

Codice utilizzabile e modificabile per finalità didattiche; vedere `LICENSE`.
