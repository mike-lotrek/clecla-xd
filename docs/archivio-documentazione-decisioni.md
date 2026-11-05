# Archivio documentazione immobile — decisioni e stato

Aggiornato al 18/08/2026. Copre solo l'archivio: le decisioni sul profilo immobile stanno in `claude/revisione-wireframe-sprint2.md`.

**Da cinque frame a due**, più due modali di caricamento. Frame in Figma, pagina `Archivio immobile`:

| Frame | Cosa mostra |
|---|---|
| `ARC / Desktop 1440 — Archivio documentazione · stato di default` | otto cartelle chiuse, archivio vuoto |
| `ARC / Desktop 1440 — Archivio documentazione dell'immobile` | archivio in lavorazione, una cartella aperta |
| `ARC / Modale — Caricamento di un documento (select chiusa)` | + stato alternativo «caricamento contestuale» |
| `ARC / Modale — Caricamento di un documento (select aperta)` | il dropdown in overlay |
| `ARC / Mobile 375 — Archivio documentazione` | stesse otto cartelle |

## La regola che tiene insieme tutto

**La lista dei documenti è la stessa per ogni immobile e c'è da subito, anche vuota.** Non si genera dalle risposte della scheda tecnica: cambia solo quali righe diventano *non pertinenti*. Lo stato di default non è un archivio che non esiste ancora, è un archivio già strutturato e vuoto.

Ne segue che lo stato alternativo «la lista dei documenti si crea quando ci mandi la scheda tecnica» era **falso** ed è stato eliminato.

## Da dove vengono i documenti

Dalla checklist ufficiale `20260420_Checklist.pdf`, confermata dalla sua versione per processo `20260420_Checklist_Cp_Mutuo_Rogito.pdf`: **la seconda è la prima filtrata sulle sole righe con una X**, riorganizzata per processo. Nessuna contraddizione fra le due.

L'archivio tiene:

- i **20 documenti marcati CP** (contratto preliminare)
- i **documenti interni Cleclà** — quelli senza X in nessuna colonna: incarico, privacy, identificazione e adeguata verifica della clientela, delega FEA, scheda di valutazione del rischio, studio di vendibilità, materiale fotografico, fatture e quietanze
- i **documenti condominiali** — regolamento, preventivo, consuntivo, verbali: non sono in checklist CP, servono alla trasparenza verso l'acquirente

L'archivio **non** tiene mutuo e rogito: quei processi avvengono fuori da Cleclà. Il mutuo non compare affatto — riguarda l'acquirente. Il rogito compare come **elenco informativo di nove voci** con accanto chi le rilascia.

Due voci CP che mancavano sono state aggiunte: **norme tecniche di attuazione** (accorpata alla riga GISMaster, sono tre estrazioni dello stesso strumento) e **scheda tecnica** (cartella 7, non si carica: si compila).

## Le otto cartelle

| # | Cartella | Righe | Chi se ne occupa |
|---|---|---|---|
| 1 | Identità e titolarità | 7 | Tu |
| 2 | Mandato e privacy | 6 | Cleclà — si firma nel percorso, non si carica |
| 3 | Catasto e urbanistica | 8 | misto |
| 4 | Prestazione energetica | 1 | Tu (certificatore) |
| 5 | Condominio | 4 | Tu (amministratore) |
| 6 | Fisco e locazione | 1 | Tu, condizionale |
| 7 | Annuncio e valutazione | 3 | Cleclà |
| 8 | Contratto e pagamenti | 4 | Cleclà |

Contatori: **fatti = validati**, denominatore = **righe pertinenti**. Le righe «non pertinente» restano visibili — la struttura stabile è essa stessa un'informazione — ma escono dal conteggio. Totale **8 di 31**.

## Decisioni prese il 18/08

**Un documento caricato non si elimina, si sostituisce.** La versione precedente resta archiviata con la sua data. Conseguenze applicate: nessuna CTA «Elimina» in nessuna riga, **modale di conferma eliminazione eliminata**, stato «eliminazione bloccata» eliminato. La sostituzione riusa la modale di caricamento con la tipologia già impostata.

**I documenti degli altri intestatari e del coniuge si chiedono a trattativa chiusa**, prima della redazione del preliminare. Non sono un blocco all'inizio: riga «più avanti», non «manca». *Da validare*: se la dichiarazione del regime patrimoniale segue la stessa regola.

**I moduli che si generano su richiesta non compaiono in elenco** — recesso dal preliminare, comunicazione e riconoscimento di inadempimento. Non si caricano: si creano dentro al percorso quando l'evento si verifica. Elencarli in anticipo genera confusione.

**Un documento già caricato non compare nell'elenco della select.** Prevenire il duplicato togliendolo dalla lista è più semplice che avvisare dopo: lo stato alternativo «Hai già caricato un APE il 12/09» è stato eliminato.

**Il caricamento non è contestuale.** Pannello persistente in colonna destra; la tipologia si sceglie dentro al pop-up da una **select vera** — chiusa per default, che si apre in overlay sopra al contenuto, con le voci raggruppate per cartella. Quando si arriva da una riga dell'archivio la select è già compilata e non si apre da sola, ma resta modificabile.

**Eliminati**: la modale «Chi può vedere questo documento» — la regola vive sulla riga della planimetria — e lo stato «Documenti condivisi con l'acquirente». **Rimosso** anche il pannello dei traguardi «A che punto sei», e con lui la barra sticky su mobile.

## Cosa diventa pubblico

**La planimetria è l'unico documento dell'archivio che diventa pubblico nell'annuncio.** Tutti gli altri li vede l'acquirente solo a trattativa avviata. La regola è dichiarata sulla riga della planimetria e nella nota di sezione. *Da validare con il team.*

## Punti aperti

- **Alert di scadenza prima del rogito** — «la tua carta d'identità scade il 30/11, il rogito è il 15/12»: richiede di conoscere la data del rogito e le scadenze dei documenti. *Da valutare con i dev.* Se non è realizzabile, il blocco cade.
- **Dichiarazione del regime patrimoniale**: prima o dopo la chiusura della trattativa.
- **Lista definitiva dei campi pubblici** nell'annuncio: le due legende del foglio 2.0 non sono applicate a nessun campo.
- Il foglio «Pagine» del file Contenuti descrive l'archivio come **diviso in cartelle determinate dall'utente**: questa PG lo supera, la riga va aggiornata.

## Vincoli di lavorazione

Matteo lavora nel file in parallelo: **prima di modificare un nodo va riletto**, e non si cancellano mai figli in blocco. Le annotazioni native vanno scritte con la pagina in focus, una a una.

Priority guides: `20260818_Clecla_PG_Archivio_1.xlsx` — 91 righe più un foglio «Modifiche v1».
