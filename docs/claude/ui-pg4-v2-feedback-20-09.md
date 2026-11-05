# UI · PG4 Pagamento registrazione v2, dopo il feedback del 20/09

Versione 1.2 · 24/09/2026 · file **Cleclà | UI** (`0k5JkkrVwDydzvUoRHv8ye`), pagina `🚧 UI Layouts – WIP`. Due sezioni: `PG4 · Pagamento registrazione v2 · feedback 20/09 🚧` (`4456:179479`, desktop 1440) e `PG4 · Pagamento registrazione v2 · mobile 440 🚧` (`4456:184264`), entrambe sotto PG3 v2. La PG4 precedente resta in pagina finché la v2 non è approvata.

Perimetro: pagine di stato, desktop e mobile. PG4 completa.

## Decisioni prese con Giovane il 24/09

- **Nuovo stato R0, fattura in arrivo.** R1 parte dalla fattura ricevuta, con i 5 giorni per pagare.
- **Spalla: tappa Registrazione a tre passi.** Pagamento della registrazione · Deposito all'Agenzia delle Entrate · Registrato. La firma è chiusa in PG3 v2 e non si ripete.
- **CTA di R3: «Carica i documenti per il rogito»**, unico Primary, apre la cartella dell'immobile.
- Prima il desktop, poi il mobile (fatto lo stesso giorno).
- **Barra di percorso mobile su `bg-white`**, come lo stepper in spalla su desktop. Provata qui e poi estesa a PG2 v2 e PG3 v2 mobile.

## Le tavole desktop

| Tavola | Node | Stato |
|---|---|---|
| R0 · Fattura in arrivo (Acquirente) | `4456:181272` | Tutti hanno firmato, Cleclà prepara la fattura, CTA disabilitata |
| R1 · Fattura ricevuta, da pagare (Acquirente) | `4456:179599` | Tocca a Giulia, 216,00 € entro il 03/10/2026 |
| R2 · Pagata, registrazione in corso (Acquirente) | `4456:179718` | Ci pensiamo noi, fino a 30 giorni di calendario |
| R3 · Registrato (Acquirente) | `4456:179821` | Registrato il 20/10/2026, si preparano i documenti per il rogito |
| R4 · Pagamento in corso (Venditore) | `4456:179940` | In attesa di Giulia, nessun avviso |
| PG4 v2 · Contenuti dei bottoni info | `4456:181558` | Perché si paga la registrazione |

## Le tavole mobile 440

| Tavola | Node |
|---|---|
| M-0 / R0 · Fattura in arrivo | `4456:184265` |
| M-1 / R1 · Fattura ricevuta, da pagare | `4456:184428` |
| M-2 / R2 · Pagata, registrazione in corso | `4456:184591` |
| M-3 / R3 · Registrato | `4456:184741` |
| M-4 / R4 · Pagamento in corso (Venditore) | `4456:184917` |

Date allineate a PG3 v2: ultima firma 26/09/2026, fattura 28/09, pagamento entro il 03/10, pagata il 30/09, deposito dal 01/10, registrazione entro il 26/10, registrata il 20/10. Sospensive di R3 con i valori di T4 in PG2 v2.

## Regole applicate

Le stesse di PG3 v2: «PASSO SUCCESSIVO» al posto di «RESPONSABILITÀ», niente badge di fase accanto al titolo, stroke di 4 px `text-fg-warning` solo sul blocco dove tocca a te (la card «Cosa paghi» di R1), un solo bottone pieno per pagina, badge Brand white con icona di stato, spalla con «Guida al contratto preliminare», «Riepilogo degli accordi» e card «Hai dubbi?» con «Apri la chat».

**Zero Alert in tutta la PG4 v2.** Uscite l'avviso sull'annullamento a 30 giorni (R1, R4), l'avviso sull'archiviazione (R2, R4) e il traguardo Success di R3, che diventa il titolo della prima card, «Il contratto è registrato».

**Due scadenze nella riga dei fatti.** «PAGAMENTO ENTRO» (5 giorni dalla fattura, tocca all'acquirente) e «REGISTRAZIONE ENTRO» (30 giorni dall'ultima firma, ci pensa Cleclà). In R2 resta solo la seconda, in R3 diventa «REGISTRATO IL».

## Regole mobile

Shell della PG4 mobile precedente: `System Bar`, `Navbar` mobile, colonna da 408 con padding 16, back link al posto del breadcrumb. Il contenuto è clonato dalle tavole desktop v2, con padding delle card a 16.

- **Barra di percorso al posto dello stepper.** «REGISTRAZIONE DEL CONTRATTO», «Sei qui: …» e «passo n di 3», tre segmenti arancio fino al passo in corso compreso. Sparisce il conteggio «TAPPA n DI n» della versione precedente, che era un punto aperto. **Sfondo `bg-white`**, la stessa variabile del blocco stepper in spalla su desktop: la distingue dalle card in `bg-surface-subtle` e la fa leggere come orientamento. Raggio a 8 come le card mobile. Funziona finché nessun'altra card mobile è bianca.
- **Fatti impilati**: passo successivo, poi le scadenze.
- **Righe etichetta-valore impilate** (avanzamento di R2, sospensive di R3): tappa sopra, data o stato sotto.
- **Badge sotto il titolo o la riga** («Pagata il …» in R2, «0 di 19 caricati» in R3, «In attesa» in R4), come nei riquadri di PG2 v2 mobile.
- **Download di R3** in Outline a tutta larghezza, uno sotto l'altro. La riga della fattura in R1 va a capo.
- **Collegamenti della spalla** sopra la card «Hai dubbi?».
- **Barra sticky** con la CTA della pagina e, sotto, la sua nota. Padding inferiore della colonna a 128, perché la barra con la nota è più alta.

## Per tavola

- **R0.** «Importo in preparazione» al posto della cifra. Card «Quando paghi»: fattura via email e in pagina, 5 giorni per pagarla, poi fino a 30 giorni di calendario per registrare. «Paga la registrazione» disabilitata, «Si attiva quando ricevi la fattura della registrazione».
- **R1.** Importo senza IVA con la ragione (imposta, non servizio), riga della fattura con «Scarica la fattura». Scomposizione ridotta a imposta di registro e marche da bollo, senza importo per riga. «Perché si paga» riscritto su data certa, prova dell'accordo, adempimento fiscale, tutela in caso di controversia; il testo lungo va nel popover. Via «Perché tocca a te»: la riga «la registrazione è a carico dell'acquirente» sta nella nota dell'importo. Card neutra «Dopo il pagamento» con primo giorno lavorativo, 30 giorni di calendario e registrazione in ufficio a circa 15 giorni. Il blocco duplicato eliminato è il link «Come funziona la registrazione» del footer, che ripeteva la FAQ. CTA «Paga 216,00 €».
- **R2.** Stessa precisazione sui 30 giorni, nel testo e nella riga «Registrazione all'Agenzia delle Entrate». Righe: pagamento ricevuto, deposito avviato, registrazione in corso, ricevuta e contratto registrato. Badge «Pagata il 30/09/2026» Brand white con spunta.
- **R3.** Opponibile ai terzi è la data di registrazione: «Da questa data il contratto ha una data certa, che vale anche verso chi non l'ha firmato». Download in Outline. Sospensive: solo quelle generate dalle dichiarazioni della pratica (mutuo, regolarità urbanistica e conformità catastale), con scadenza e chi comunica. Notaio con città, senza provincia di Cuneo. Documenti per il rogito come rimando alla cartella. «La tua provvigione»: solo quella dell'acquirente.
- **R4.** Card «La registrazione del contratto»: la paga l'acquirente, al venditore non è richiesto nulla. Riga di Giulia con fattura e scadenza, badge «In attesa» con puntino. Via il promemoria del venditore e il suo contatore a 48 ore.

## Discrepanze da segnalare

- **I due termini non si sommano.** 5 giorni per pagare più fino a 30 giorni di calendario per registrare possono superare i 30 giorni dall'ultima firma. Con le date in pagina: deposito dal 01/10, 30 giorni portano al 31/10, oltre il termine del 26/10. Va chiarito quale termine vale e cosa si dice all'utente.
- **«Fattura» per un'imposta.** Il cliente dice fattura; l'importo è un'imposta dell'Agenzia delle Entrate, non un servizio. In pagina resta «fattura», come in PG3 v2.
- **Nome della tappa.** «Registrazione» in spalla è una tappa nuova: i percorsi approvati non la hanno (I10, I12).
- **«Trova un notaio»** resta fuori dal glossario (I26).
- **«Provvigione»** contro «fee» e «costi di mediazione» altrove (I05), e la formula su quando è dovuta (I06).
- **Registrazione tardiva.** Il cliente dice che il contratto non si annulla e c'è una piccola penale; la project knowledge diceva il contrario. In pagina non c'è più nessuna delle due cose.

## Punti aperti

- Come il sistema sa che la fattura è stata emessa (partono i 5 giorni, si attiva la CTA).
- Entro quanto arriva la fattura dopo l'ultima firma: nessuno SLA in pagina.
- Date di R2 automatiche o inserite da Cleclà: ipotesi annotata sulla card.
- Importo di esempio (216,00 €) e protocollo di esempio (2026/CN/0004821): formato e provenienza da confermare.
- Punto aperto 20 sulla registrazione tardiva: resta il posto dove si chiude. R5 non è disegnata.
- Stato alternativo bonifico in R2 e stati successivi della riga in R4: annotati, non disegnati.
- Mobile: segmenti arancio fino al passo in corso, diversi dalla barra dei punti di PG2 v2 (verde, warning, grigio). Da uniformare se il cliente lo chiede.

## Nota operativa

Tavole desktop clonate dalla PG4 precedente; spalla sostituita con quella di PG3 v2 F3 Acquirente, stepper ricostruito con i nav link della PG4 precedente (icone payments, account_balance, verified già a posto, scala indigo). Annotazioni della PG4 precedente rimosse e riscritte. Gate di libreria superato: da 62 a 69 istanze per tavola desktop, da 23 a 30 per tavola mobile, nessun fill o stroke senza variabile. Senza stile restano solo il titolo mobile a 28 e l'etichetta della barra a 14, limite già registrato in PG3.

Le tavole mobile sono copie: se una desktop cambia, va rigenerata anche la mobile, con la barra di percorso su `bg-white`. Trappola nuova: una riga orizzontale che diventa verticale si porta dietro `primaryAxisAlignItems = SPACE_BETWEEN`, che annulla l'`itemSpacing`. Va rimesso a `MIN`. Lo stesso vale per il fix del link «Scarica la fattura»: il testo clonato era in `FILL` verticale, allineato in alto, e va centrato.
