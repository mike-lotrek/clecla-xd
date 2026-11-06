# Verifica · archivio documenti per i contratti (Finalizzazione)

05/11/2026. Verifica di sola lettura: nessuna modifica a Figma, a FigJam o ai fogli.

## Esito

Nessuna fonte prevede una pagina o un archivio dedicato ai contratti. I requisiti chiedono però di archiviare i documenti del contratto, e le fonti successive li collocano nell'Archivio documentazione immobile, cartella 8 «Contratto e pagamenti».

## Requisiti: «MVP Functional Requirements Definition» (versione del 16/10/2026)

- Riga 12, Caricamento documentazione tecnica: «Creazione di uno spazio di archivio documentazione relativa all'immobile e all'interazione specifica venditore-acquirente».
- Riga 33, Accettazione finale e firma digitale: «salvataggio nello spazio di archiviazione» e «Archiviazione sicura in formato PDF con marca temporale».
- Riga 37, Annullamento contratto preliminare, output: «Archivio storico e download documentazione».

## User flow: board «[EXT] Cleclà | User Flows» (`DXvZbuexjok4HOsLSuLiEK`)

Tavola REVIEW 16/03, `388:2166`. I nodi sono database, nessuna schermata:

- `388:2207` Salvataggio contratto negli archivi
- `388:2208`, `388:2209` Archiviazione contratto annullato
- `388:2211` Archiviazione contratto «inefficace»
- `388:2212` Archiviazione profilo immobile come «venduto»
- `394:2787` Archiviazione documento di sentenza o accordo avvocato
- `394:2540` Salvataggio accordo

Architettura, `333:348`: gli archivi sono due, `333:58` personali e `333:61` immobile. `333:61` è collegato solo al Profilo immobile del venditore (`333:41`, connettore `333:72`).

## Altri documenti su Drive

- User Stories, foglio «Finalizzazione - REVIEW 16/03»: E5 e E7 (archiviazione con marca temporale, sbloccata dal pagamento della registrazione), E10 («Archiviazione contratto» dopo il recesso).
- Contenuti, foglio Pagine, riga 42: «l'archiviazione del documento all'interno dell'apposito archivio».
- Contenuti, foglio Struttura backoffice, righe 49, 50 e 52: ricevute di registrazione e accordo con «salvataggio nell'archivio immobile».
- Contenuti, foglio Priority guides, riga 1377: i documenti «finiscono nella cartella «8. Contratto e pagamenti» dell'archivio dell'immobile».
- «Checklist documenti per archivio», foglio «Contratto e Pagamenti»: otto voci, tra cui contratto preliminare, ricevuta di registrazione e ricevuta delle imposte.

## Documenti nel repo

- `clecla_pg_finalizzazione_v2.md:394-396`: blocco «I documenti di questo contratto» con rimando all'Archivio dell'immobile.
- `clecla_pg_finalizzazione_v2.md:421`: in Gestione contratti, i contratti chiusi e annullati hanno i documenti scaricabili.
- `clecla_pg_finalizzazione_v2.md:779`: per i documenti del rogito, nessuna superficie di caricamento nuova.
- `archivio-documentazione-decisioni.md:46`: cartella 8 «Contratto e pagamenti».

## Punti da decidere col cliente

1. Dove trova i documenti l'acquirente: la board Architettura collega l'Archivio immobile solo al venditore, mentre la PG (`clecla_pg_finalizzazione_v2.md:395`) dà a entrambi il link «Vedi la documentazione dell'immobile». L'unico archivio raggiungibile dall'acquirente è «Archivio documentazione (personali)» (`333:58`). Vedi la sezione sotto.
2. Accesso all'archivio dopo l'annullamento: ancora aperto (`claude/ui-finalizzazione-pg1.md:97`). I requisiti chiedono archivio storico e download.
3. Cartella «Notaio»: oggi assente nell'Archivio (`claude/modifiche-risposte-cliente-07-10.md:32`).
4. Colonne «Cartella aggiuntiva» della Checklist (Contratto preliminare, Mutuo, Rogito): da chiarire se indicano cartelle in più o solo il processo a cui serve il documento. Se sono cartelle, contraddicono `archivio-documentazione-decisioni.md:31`, per cui l'archivio non tiene mutuo e rogito.

## Archivio personale dell'acquirente (aggiunta del 05/11)

Ipotesi del team: i documenti dell'acquirente stanno in «Archivio documentazione (personali)». Lo stesso acquirente può avere trattative e contratti su immobili diversi, quindi la pagina deve avere più cartelle di archivio.

A favore:

- Contenuti, foglio Pagine, riga 33 (ramo acquirente): «Raccoglie e permette il caricamento di tutti i documenti richiesti per la compravendita dell'immobile». Sul ramo venditore (riga 23) la stessa pagina raccoglie solo i «documenti personali».
- Requisiti, riga 12: la CTA «Aggiungi/Carica documento» sta «nel profilo immobile (venditore) o al profilo utente (acquirente)».

Da risolvere:

- Contenuti, foglio Priority guides, righe 463-464: per l'acquirente la pagina ha solo «Sezione ID personale» e «Sezione Privacy». Sulla riga 463 c'è un commento del 27/02: «Come funziona per l'acquirente? Dove si archivia?».
- Nessuna fonte prevede un raggruppamento per immobile o per contratto. Pagine parla solo di cartelle scelte dall'utente tra le opzioni fornite al caricamento.
- Contenuti, foglio Label, riga 42: la voce è «Documenti personali», che non descriverebbe più il contenuto.
- Nell'Architettura `333:58` è figlio di Profilo utente (`333:25`), quindi è la stessa pagina per entrambi i ruoli.
- Visibilità per l'acquirente: Priority guides, riga 990, dice «a trattativa avviata»; `clecla_pg_finalizzazione_v2.md:395` dice «a contratto firmato».

Stato: si passa prima dal cliente (05/11). Nulla è disegnato finché non risponde.

Versione che proponiamo come migliore, da far scegliere al cliente: l'archivio dei documenti di compravendita sta dentro il Profilo immobile (n) dell'acquirente (`333:42`), che ha già come figli Trattative e Gestione contratti. L'archivio personale resta integro, con i soli documenti personali. Più immobili significano più profili, quindi non servono cartelle per immobile. I documenti condivisi restano uno solo, cioè quello della cartella 8 dell'immobile.

Conseguenze se il cliente la sceglie:

- Board Architettura: aggiungere il collegamento da `333:42` all'archivio dell'immobile.
- Contenuti, foglio Pagine, riga 33: da riallineare, perché assegna all'archivio personale dell'acquirente i documenti di compravendita.
- Requisiti, riga 12: la CTA di caricamento dell'acquirente sta «al profilo utente». Va chiarito cosa carica l'acquirente e da dove.
- Visibilità per cartella: l'archivio dell'immobile contiene anche documenti che l'acquirente non dovrebbe vedere per forza (per esempio «Identità e titolarità» e «Mandato e privacy»). Va definito quali cartelle vede.

Alternativa da mostrare al cliente: archivio personale su due livelli, con un'area per i documenti personali e una cartella per ogni immobile in acquisto. Richiede di rinominare la voce «Documenti personali».

## Commenti del cliente sui punti aperti (aggiunta del 05/11)

Board «[EXT] Cleclà | Feedback» (`1ZS96SiXSktrMXrvLrsPA0`), letti dopo la prima stesura. Riguardano i punti 2, 3 e 4 e il blocco documenti:

- 08/10, `3231:17827`, `1958621769`: la sezione documenti notaio si riduce a «un semplice rimando all'archivio dei documenti, cartella notaio».
- 12/10, `3206:16936`, `1962781096`: «non saranno presenti cartelle dedicate alla raccolta dei documenti necessari per il rogito, il mutuo e le altre pratiche». Chiede per l'acquirente un elenco anche per il mutuo e un pulsante «Scarica». Va in direzione opposta al commento del 08/10.
- 08/10, `3231:16126`, `1957985140`: «per legge abbiamo l'obbligo di mantenere per 10 anni la documentazione». Riguarda la conservazione, non dice se l'utente continua ad accedere.
- 10/10, `3231:16201`, `1961027019`: il blocco documenti in pagina contratto non serve, perché «ha già una sua sezione dove sono visibili tutti i documenti del contratto». Contraddice `clecla_pg_finalizzazione_v2.md:394`.

## Non verificato

Tavole del file Figma «Cleclà | UI». Sulla board Feedback, i thread precedenti al 01/10/2026. `20260924_Contratto preliminare v1.docx` e `20260311_Contratto preliminare v1.pdf`: compaiono nella ricerca su Drive per «archivio» e «contratto preliminare», ma non li ho aperti. La ricerca su Drive si è fermata alla prima pagina di risultati.

## Termini nuovi per il glossario

Nessuno.
