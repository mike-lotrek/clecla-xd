# Listing immobili e Annuncio immobile — decisioni e stato

Aggiornato al 19/08/2026. Priority guides: **`20260819_Clecla_PG_ListingAnnuncio_3.xlsx`** — 51 righe su due pagine (Annunci/Listing immobili e Annuncio immobile) più il foglio «Modifiche v2 e v3». Sostituisce sia la v2 del 18/08 sia il file delta sullo stato di default, che non vanno più usati.

Frame in Figma, sezione `Listing immobili e Annuncio immobile`:

| Frame | |
|---|---|
| `ACQ / Desktop 1440 — Annunci · pagina pubblica` | default senza filtri + due stati alternativi |
| `ACQ / Desktop 1440 — Listing immobili · stati vuoti e ricerca salvata` | tre stati vuoti + modale di salvataggio |
| `ACQ / Desktop 1440 — Annuncio immobile · utente non loggato` | include «Gli altri stati dell'annuncio» |
| `ACQ / Mobile 375 — Listing immobili · toggle lista e mappa` | |
| `ACQ / Mobile 375 — Annuncio immobile · CTA visita sticky` | |

## «Annunci» non è una pagina nuova: è il default di quella dei risultati

Il frame partiva dallo stato **con i filtri applicati**, che si raggiunge solo dopo aver cercato — il caso minoritario. Dal menu «Annunci», da un link condiviso o da un motore di ricerca ci si arriva **senza aver cercato nulla**. Quindi si inverte: default senza filtri, stato alternativo con i filtri attivi. È la stessa correzione fatta su Trova tecnico il 18/08.

**Perché si mostra tutto invece di chiedere di cercare.** Con 23 immobili in tutta la provincia il catalogo si scorre. Una pagina di atterraggio che chiede di filtrare fa credere che il catalogo sia grande, poi produce due risultati e sembra vuota: è lo stesso meccanismo presidiato dai chip dei filtri.

Differenze rispetto allo stato filtrato — tre blocchi, non una pagina:

| | Default | Con filtri |
|---|---|---|
| H1 | «Case in vendita da privati in provincia di Cuneo» | si riscrive sui filtri |
| Sottotitolo | dimensione del catalogo | «18 case su 23 corrispondono ai tuoi criteri» |
| Filtri | nessun badge, nessun chip | «5 attivi» + chip + «Azzera» |
| Esplora per comune | **c'è** | sparisce |
| Salva questa ricerca | **in evidenza in coda** | resta, meno centrale |

## H1 e regola di composizione

**Default: «Case in vendita da privati in provincia di Cuneo».** Forma nominale come le query reali, «case in vendita» in apertura, luogo in chiusura, 47 caratteri. «Da privati» non è riempitivo: è il differenziale del prodotto ed è una parola che si cerca.

Regola: `[Tipologia] + in vendita + da privati + [Luogo]`. Oltre i ~65 caratteri **«da privati» cade per primo**.

⚠️ **Da decidere con chi segue la SEO**: quali di queste pagine si indicizzano. Tipologia × comune × prezzo genera centinaia di combinazioni che oggi restituiscono zero o due risultati — pagine sottili che si cannibalizzano. Partire dal default e dai comuni con stock sufficiente, il resto in noindex finché il catalogo non cresce. Serve anche una verifica dei volumi reali: la scelta fra «case» e «immobili» è ragionata sul pattern delle query, non su dati.

## I due blocchi che esistono solo senza filtri

**Esplora per comune** — chip con i conteggi: Cuneo 14 · Borgo San Dalmazzo 4 · Boves 3 · Demonte 2 · Caraglio 0. Con questi numeri il comune è l'unico taglio che produce insiemi utilizzabili: la tipologia da sola lascia insiemi da uno o due. I conteggi sono in chiaro **anche quando sono zero** — un comune vuoto detto prima è un vicolo cieco evitato, detto dopo è una delusione. Sparisce appena si applica un filtro.

**Salva questa ricerca** — in coda ai risultati, non in testa: prima si guarda, poi si lascia un criterio. È la vera conversione della pagina finché il catalogo è piccolo. Assorbe il vecchio banner «Siamo partiti da poco nel Cuneese», ora rimosso perché la stessa informazione sta nel sottotitolo.

Il **banner del budget calcolato** non esiste più nel frame: la riga corrispondente è uscita dalle priority guides.

## I filtri: chiusi di default, aperti in un drawer

**Default chiuso.** In pagina restano il pulsante «⊞ Filtri», il contatore e — solo se ci sono filtri attivi — il badge di conteggio e i chip con «Azzera i filtri».

**Aperto in un pannello laterale, non in pagina.** Un blocco che si espande spinge lista e mappa sotto la piega proprio mentre l'utente vuole vedere cosa cambia. Il drawer risolve anche il problema che l'ha fatto nascere: **«Altri filtri» era un accordion dentro la sezione dei filtri**. Con la verticalità del pannello i filtri stanno tutti insieme. Footer sticky con «Azzera i filtri» e «Vedi i 18 immobili».

Su mobile è **lo stesso pannello**, a tutto schermo dal basso.

## Lista e mappa: nessun toggle su desktop

Su 1440 stanno affiancate e ci restano. Il toggle esiste **solo su mobile**.

## Niente documenti visibili al pubblico

**Esporre quali documenti ci sono e quali mancano è controproducente per il venditore.** Eliminata la sezione «Documenti verificati» dall'annuncio mobile. Non resta nessun elenco di documenti con stato, né sull'annuncio né sulle card.

Resta il solo badge **«Documentazione verificata»**, che dichiara il controllo senza esporne il contenuto.

⚠️ **Da decidere**: se la regola vale anche per la **planimetria in galleria**. Nell'archivio è dichiarata come l'unico documento che diventa pubblico; se cade, va tolta dall'annuncio e va corretta quella riga.

## La fee

**Venditore 1%** — confermato da Matteo il 18/08. Le occorrenze all'**1,5%** sulla pagina «Come funziona» (gruppo `📦 Step 1`, nodi `1678:54892 · 55192 · 55534 · 55834`) sono versioni vecchie da aggiornare.

**Acquirente 2%**, con minimo 4.000 € più IVA nei wireframe dell'annuncio — il minimo non compare nelle pagine pubbliche, da allineare.

⚠️ **Resta aperto il momento in cui si paga**: «Come funziona» dice *al preliminare*, la Landing Acquirente dice *al rogito*, la Homepage dice *al momento dell'acquisto*. Finché il team non decide: **«si paga solo se la compravendita si conclude»**.

## «Se è la prima volta» → «Comprare da un privato, senza sorprese»

Contenuto ripreso alla lettera dalla pagina **Come funziona**, che resta la fonte canonica. In fondo alla lista, non in testa: prima i risultati, poi il contesto.

## Fuori perimetro: il flusso di richiesta visita

Eliminati il 18/08 i frame `Annuncio immobile · utente verificato e prenotazione` e `Modale — Conferma della richiesta di visita`. Prima è stato **salvato** il blocco `Gli altri stati dell'annuncio` — *In trattativa* e *Immobile archiviato* — spostato nell'annuncio pubblico.

Resta la FAQ **«Devo pagare per visitare?»**, ora un «?» accanto a «Vieni a vederla» con la risposta in annotazione.

## Punti aperti

- Quali pagine filtrate si indicizzano, e con quale soglia di stock per comune.
- Verifica dei volumi di ricerca reali («case» vs «immobili»).
- La planimetria in galleria: documento pubblico o no.
- Il momento in cui si attiva la fee dell'acquirente, e il minimo di 4.000 € + IVA.
- Aggiornare a 1% le quattro occorrenze all'1,5% sulla pagina «Come funziona».
- Chi aveva un immobile nei preferiti quando viene archiviato: serve una notifica.
- Il filtro «solo annunci con documentazione validata».
- I due criteri di messa in evidenza (nuovi della settimana, documentazione verificata).

## Nota operativa

Dal 19/08 il Desktop Bridge non risponde più: si lavora sul file con il **Figma MCP ufficiale** (`use_figma`). Due differenze pratiche: `getPluginData` non è supportato, quindi le librerie di helper salvate in `figma.root` non sono raggiungibili e i componenti vanno costruiti con Plugin API in chiaro; la palette va campionata dai nodi esistenti (bg `#fafafa`, bianco, bordi `#e5e5e5` e `#d1d1d1`, testi `#111111` `#282828` `#434343` `#737373` `#a3a3a3`).

**Convenzione sulle priority guides**: un file per area, versionato, che sostituisce il precedente. Niente file delta separati — si integra sempre nel file completo.
