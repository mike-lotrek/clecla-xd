# Wireframe — Profilo immobile e pubblicazione

File Figma: **Cleclà | UI** → pagina `📏 Wireframe` sotto **🚧 Sprint 2** (node `71:2493`).
Generati il 07/08/2026 a partire dalla PG `20260807_Clecla_PG_Profiloimmobile_1.xlsx`, dallo user flow `EXT Cleclà · User Flows` (profilo immobile e pubblicazione) e `User Flows 2` (definizione calendario appuntamenti), applicando l'interaction model Cleclà.

## Cosa c'è nella pagina — 32 frame in 5 sezioni

**0 · Legenda e punti aperti** — fonti, segni convenzionali, i 9 stati con condizione di ingresso e uscita, i 10 punti ancora da decidere.

**1 · Stati del profilo immobile (Desktop 1440)** — 9 frame
S1 Bozza · anagrafica · S2 Scheda tecnica da compilare · S3 Documento d'identità · S4 Documenti da firmare · S5 Documentazione e lavorazioni in corso · S6 Studio di vendibilità da leggere · S7 In attesa di pubblicazione · S8 Annuncio online · S8b Sospeso/Ritirato.

**2 · Scheda tecnica, gli 8 step (Desktop 1440)** — 8 frame
Dati catastali · Situazione giuridica · Regolarità urbanistica · Prestazione energetica · Caratteristiche architettoniche (7 sotto-gruppi 5a-5g) · Utenze e servizi · Dati fiscali · Prezzo e valutazione.

**3 · Punti critici Mobile 375** — 6 frame
Barra requisiti sticky · bottom-sheet «Cosa manca per pubblicare» · documento d'identità con scatto da fotocamera · firma con contenitore del provider · studio e prezzo · annuncio online.

**4 · Modali e stati alternativi** — 8 frame
Conferma invio scheda · caricamento documento · contenitore verifica identità e firma · prezzo fuori fascia · conflitto disponibilità/visite confermate · richiesta di modifica · archiviazione (distruttiva) · anteprima annuncio.

## Decisioni di struttura

- **Una pagina sola, nove stati.** Il badge nell'header ne mostra sempre uno; ogni blocco dichiara in quali stati compare.
- **Pannello requisiti persistente.** Su desktop è la colonna destra sticky ed è l'unica sede del progress (nell'header non si duplica). Su mobile diventa una barra sticky che apre un bottom-sheet. In S8 non sparisce: si trasforma in riepilogo dell'annuncio.
- **Blocco «Prossima azione» in testa.** Dichiara sempre chi ha la palla — «Tocca a te» / «Ci pensiamo noi» — con una sola azione alla volta e il motivo per cui serve.
- **Lavorazioni Cleclà distribuite, non raggruppate.** Foto, planimetria, visura, titolo, descrizione e dati APE compaiono nel punto della scheda a cui appartengono, ciascuno con stato e hint su chi se ne occupa e quando.
- **Errori inline, modali a parte.** Gli stati di errore e i percorsi alternativi stanno dentro la schermata in blocchi tratteggiati «STATO ALTERNATIVO»; hanno un frame proprio solo le 8 modali.
- **Yousign come contenitore.** Progettiamo header, caricamento, errore, chiusura, ritorno e stati di esito. La sequenza interna del provider è riportata a titolo informativo.
- **Pubblicazione senza CTA del venditore.** Dallo user flow lo sblocco e la pubblicazione sono azioni del backoffice: S7 è uno stato di attesa dichiarato, con tempo stimato e canale di avviso, non un bottone.

## Punti aperti prima di passare alla UI

| Tema | Cosa va deciso |
|---|---|
| Provvigione | Tre numeri diversi nello stesso prodotto: scheda tecnica 1% venditore (min. 2.000 €) e 2% acquirente (min. 4.000 €), landing 1,5%, hub calcolatori «Fee 1%» |
| Dati catastali | Proposta: chiederne 5 e derivare gli altri dalla visura, invece dei 15 dichiarati dal venditore |
| Dati del profilo utente | La PG del Profilo utente li marca come necessari alla firma del contratto, ma l'incarico si firma molto prima |
| Sospendi e Ritira | Non compaiono nei requisiti MVP né nello user flow; da decidere anche cosa accade all'incarico firmato |
| Freno alla pubblicazione | Se la pubblicazione parte in automatico, serve un «non pubblicare ancora» al venditore |
| Delega della visita | Il venditore può farsi sostituire da una persona di fiducia? |
| Riscaldamento e allarme | Nella scheda tecnica compaiono due e tre volte con opzioni diverse: qui unificati |
| Spese condominiali | Importo annuo nel titolo e mensile nella nota: risolto con un selettore, da confermare |
| Video | Servono i parametri di dimensione, lunghezza e formato annunciati nello user flow |
| Altre informazioni facoltative | Lo user flow segna il gruppo con un punto interrogativo |

## Non coperto

Restano fuori da questi wireframe, perché appartengono ad altre pagine: l'Archivio documentazione immobile, il Calendario visite (qui si definiscono solo le regole di disponibilità), la pagina Trova tecnico e il backoffice Cleclà.
