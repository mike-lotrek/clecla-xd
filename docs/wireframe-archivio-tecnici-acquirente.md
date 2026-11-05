# Wireframe — Archivio, tecnici e percorso acquirente

File Figma: **Cleclà | UI** → pagina `📏 Wireframe` sotto **🚧 Sprint 2**, contenitore *Archivio, tecnici e percorso acquirente*.
Generati il 07/08/2026 dalle priority guide del file `20260127_Cleclà_Contenuti 2.xlsx` (righe 750-970) e dai flussi `Ricerca immobile` e `Definizione calendario appuntamenti`.

Sidebar e navigazione sono lasciate come ingombri tratteggiati: struttura e comportamento sono già definiti altrove.

## Cosa c'è nella pagina — 22 frame in 5 sezioni

**5 · Archivio documentazione immobile (Desktop 1440)** — 5 frame
A1 predisposto e vuoto · A2 checklist generata · A3 completo per la pubblicazione · A4 completo per il preliminare · A5 completo per il rogito.

**6 · Trova tecnico e Listing tecnici (Desktop 1440)** — 4 frame
Trova tecnico con contesto e senza contesto · Listing con mappa primaria e card · i quattro stati vuoti.

**7 · Listing immobili e Annuncio immobile (Desktop 1440)** — 4 frame
Listing con filtri, split lista/mappa e ricerca salvata · stati vuoti · annuncio pubblico per utente non loggato · annuncio con prenotazione per utente verificato.

**8 · Mobile 375** — 4 frame
Archivio con traguardi in bottom bar · listing tecnici con mappa a un terzo di schermo · listing immobili con toggle lista/mappa · annuncio con CTA visita sticky.

**9 · Modali** — 5 frame
Caricamento documento · eliminazione · chi può vedere questo documento · dettaglio tecnico · conferma della richiesta di visita.

## Decisioni di struttura

- **Tre traguardi impilati, non un contatore su 32 documenti.** Per pubblicare (6) → per il preliminare (7) → per il rogito (19). Un unico contatore sarebbe scoraggiante e falso, perché molti documenti servono solo mesi dopo. Si apre solo il traguardo corrente.
- **Le 8 cartelle non sono modificabili dall'utente.** Il vincolo è dichiarato con il motivo: così tecnici, notaio e banca trovano tutto dove se lo aspettano. Questa scelta supera la riga del foglio *Pagine* che descrive le cartelle come determinate dall'utente.
- **La visibilità è informazione di primo livello.** Ogni riga documento porta il proprio livello (solo tu e Cleclà / anche l'acquirente in trattativa / pubblico nell'annuncio). La planimetria è il caso critico: viene pubblicata nell'annuncio e va detto prima.
- **La mappa è elemento primario, non accessorio.** Vale sia per i tecnici sia per gli immobili: in una provincia con valli alpine la distanza in linea d'aria non dice nulla sul tempo di percorrenza. Proposte le isocrone al posto del raggio.
- **Vedere è libero, agire richiede un account.** Gli annunci e i dettagli restano pubblici e indicizzabili; servono un account solo salvare una ricerca, salvare un annuncio e richiedere una visita.
- **Il calendario del venditore è visibile senza account.** Permette di capire se esistono orari compatibili prima di investire in registrazione e verifica identità.
- **Il costo complessivo per l'acquirente sta sopra la piega.** Provvigione, imposta di registro e spese notarili con un totale indicativo, prima della visita e non in trattativa.

## Punti aperti che si aggiungono ai precedenti

| Tema | Cosa va deciso |
|---|---|
| Le 8 cartelle dell'archivio | Struttura da validare con il team e con un notaio |
| Accesso dei tecnici | È previsto in evoluzione un accesso diretto alla piattaforma, o il caricamento resta sempre a carico dell'utente? |
| Regola di ingresso nell'elenco tecnici | Serve la regola reale: è ciò che rende l'elenco credibile invece che una pagina gialla |
| Recensioni dei tecnici | Chi può recensire e come si modera |
| Listini dei tecnici | Se dichiarano prezzi, vanno marcati come indicativi e non vincolanti per Cleclà |
| «L'ho contattato» | Proposta: senza, chi torna dopo tre giorni non ricorda a chi ha già scritto |
| Isocrone | Fattibilità e costo con il team tech |
| Listing limitato per non registrati | Interpretato come vincolo di ingresso, non come contenuto nascosto: da validare |
| Filtro «solo documentazione verificata» | Da attivare quando la quota di annunci validati non svuota i risultati |
| Stato «in trattativa» sull'annuncio | Da validare se mostrarlo pubblicamente |
| Sezione in evidenza | I due criteri proposti sono oggettivi e non sponsorizzati: da confermare |
| 48 e 24 ore | I tempi di risposta e di annullamento della visita vanno confermati |
| Costo complessivo per l'acquirente | Da validare se esporlo nell'annuncio, con l'elenco esatto dei servizi inclusi |
| Campi di contesto pubblicabili | Quali dati sulla zona raccolti per il perito possono comparire nell'annuncio |

## Stato complessivo della pagina

54 frame in 10 sezioni, sotto due contenitori: *Profilo immobile* (32 frame) e *Archivio, tecnici e percorso acquirente* (22 frame).
