# UI · PG2 Pagina trattativa v2, dopo il feedback del 20/09

Versione 2.3 · 28/09/2026 · file **Cleclà | UI** (`0k5JkkrVwDydzvUoRHv8ye`), pagina `🚧 UI Layouts – WIP`. Due sezioni: `PG2 · Pagina trattativa v2 · feedback 20/09 🚧` (`4371:29245`, desktop 1440) e `PG2 · Pagina trattativa v2 · mobile 440 🚧` (`4435:165755`). Le tavole della PG2 precedente sono state eliminate dalla pagina il 24/09 e restano solo nel backup (`💿 UI Layouts – Backup 22.09`, sezione `4300:30222`): questa è ora l'unica PG2.

Perimetro: pagine di stato e modali, desktop e mobile. PG2 completa.

## Decisioni del 28/09

- **Icona di stato in alto a destra, da sola, a 26 px**, alta quanto il badge (26) e allineata al suo bordo superiore. Su mobile, dove il badge scende sotto la provenienza, sta a destra del titolo, centrata sulla riga del titolo (28). Esce da sinistra, dove spostava il testo dei riquadri e delle card: ora titolo, storico, piede e dichiarazioni partono dallo stesso margine. È l'ultimo elemento della testata, dopo il badge. Scartata la variante con l'icona dentro il badge: lo slot del badge DS è a 12 px e nelle card delle dichiarazioni obbligava ad aggiungere un badge «Completate». Prove: `4615:38065` (scelta), `4615:37652` (scartata), `4603:37257` (28 px a sinistra).
- **Stroke verde sui riquadri completati.** 4 px a sinistra, `text-fg-success-strong`, su riquadri e card con la spunta. Resta lo stroke warning su «tocca a te»; nessuno stroke su «in attesa dell'altra parte». Eccezione: le parti «Pronta» della prima risposta (D-0c, M-0c) restano senza stroke, perché l'altra parte non le ha ancora ricevute.
- Applicato a tutte le pagine di stato con riquadri, desktop (T1, T1b, D-0a, D-0c, T2, T3, T3a, T2b, T2c, chiusura bloccata, D-4) e mobile (M-0, M-0a, M-0c, M-1 T2, M-1 T3, M-1a, M-2, M-3, M-5). Fondi PNG di modali e fogli riesportati da T1b, T2, T3 desktop e mobile; `pg2bg` aggiornato.

## Annulla la trattativa (28/09)

Il link «Annulla la trattativa» in fondo alla pagina ha ora l'icona `icon/delete_outline` a sinistra e resta Link-dark, per non competere con la CTA. Aggiornato su tutte le pagine desktop e mobile (27 istanze); fondi di modali e fogli riesportati.

Il link apre una conferma:

| Tavola | Node |
|---|---|
| X1 · Annulla la trattativa · conferma (Venditore), modale su T2 | `4639:163600` |
| X1 · Annulla la trattativa · conferma, foglio mobile su T2 mobile | `4639:163724` |

Contenuto: eyebrow «ANNULLA LA TRATTATIVA», titolo «Vuoi annullare la trattativa con Giulia Rossi?», box «Cosa succede se annulli» con tre conseguenze, campo facoltativo «Ti va di dirci perché?» (modello approvato dell'eliminazione del profilo, §12.4 del glossario), bottone Destructive-fill «Annulla la trattativa» e uscita «Continua la trattativa». L'uscita sicura non si chiama «Annulla», per non avere due «annulla» con significati opposti.

Le quattro conseguenze scritte sono ipotesi, non coperte da glossario né da documenti di flusso: avviso all'altra parte, proposte e dichiarazioni che decadono, altre trattative che continuano, motivo letto solo da Cleclà. Annotate sulle tavole.

## Decisioni del 24/09

- **Invio unico, solo per la prima risposta del venditore.** Prezzo, data del rogito, data di consegna e dichiarazioni del venditore partono insieme. Dai turni successivi ogni argomento si muove da solo, con invio diretto.
- **Colore dello stato: stroke a sinistra solo su «tocca a te».** Esteso il 28/09 ai completati, in verde.
- **La pagina della Bacheca acquirente resta all'epica Visita**; da qui parte solo la card dell'immobile visitato nei suoi tre stati.
- **Elenco trattative dal selettore ricreato dal backup**, adeguato alle regole v2.
- **Barra di percorso mobile su `bg-white`**, come lo stepper in spalla su desktop. Provata su PG4 v2 e poi estesa a PG2 v2 e PG3 v2 mobile.

## Le tavole desktop

Prima fila, pagine di stato:

| Tavola | Node | Stato |
|---|---|---|
| D-0 / T1 · invio singolo · **scartata** | `4390:159355` | Resta come documentazione del confronto |
| D-0b / T1 · Prima proposta ricevuta (invio unico) | `4413:160184` | L'acquirente ha proposto prezzo e data del rogito; il venditore prepara la prima risposta |
| D-1 / T2 · Venditore | `4371:29246` | Tocca al venditore sul prezzo, rogito concordato, consegna in attesa dell'acquirente |
| D-1 / T3 · Acquirente | `4371:29991` | Stesso momento visto da Giulia: tocca a lei sulla consegna |
| D-2 / T2b · Stallo, suggerimento | `4371:30734` | Cleclà suggerisce la media dentro il riquadro Prezzo |
| D-3 / T2c · Stallo, media proposta | `4371:31272` | La media è sul tavolo, tocca al venditore |
| D-5 / Chiusura bloccata | `4371:31792` | Tre argomenti concordati, manca una dichiarazione del venditore |
| D-6 / Riepilogo in corso | `4371:32333` | Riepilogo raggiungibile in ogni momento, si popola con gli accordi |
| D-7 / T4 · Riepilogo e conferma | `4371:32772` | Accordo raggiunto, stato iniziale del bottone di conferma |
| D-8 / T5 · Chiusura | `4371:33277` | Accordo confermato, si prepara il preliminare |
| D-4 / Elenco trattative (popover aperto) | `4435:171547` | T2 con il popover del selettore «1 di 3 su questo immobile» |

Seconda fila, prima risposta del venditore (invio unico), fondo T1b:

| Modale | Node |
|---|---|
| P1 · Rispondi — Prezzo | `4413:160608` |
| P2 · Rispondi — Prezzo · controproposta | `4413:160690` |
| P3 · Rispondi — Data del rogito · controproposta | `4413:160756` |
| P4 · Proponi — Data di consegna delle chiavi | `4413:160830` |
| P5 · Le tue dichiarazioni (Venditore) | `4413:160910` |

Terza fila, prima risposta in preparazione e invio, più le prove di colore:

| Tavola | Node |
|---|---|
| D-0c · Risposta in preparazione, 2 di 4 pronte | `4413:160993` |
| B2 · Rivedi e invia la prima risposta | `4413:161473` |
| Prova 1 · stroke per ogni stato | `4418:161596` |
| Prova 2 · sfondo tinto per ogni stato | `4418:161945` |
| Prova 3 · stroke solo su «tocca a te» · **scelta** | `4418:162428` |
| Prova 4 · sfondo tinto solo su «tocca a te» | `4418:162771` |

Quarta fila, turni successivi (invio diretto):

| Modale | Fondo | Node |
|---|---|---|
| R1 · Rispondi — Prezzo | T2 | `4418:164712` |
| R2 · Rispondi — Prezzo · hai premuto «Rifiuta» | T2 | `4418:164792` |
| R3 · Rispondi — Prezzo · hai premuto «Accetta» | T2 | `4418:164852` |
| R4 · Rispondi — Data di consegna delle chiavi (Acquirente) | T3 | `4418:164896` |

Quinta fila, il percorso dell'acquirente dalla proposta alla prima risposta, più l'onboarding del venditore:

| Tavola | Fondo | Node |
|---|---|---|
| A-P1 · Fai una proposta, 1 di 2 · Le tue dichiarazioni | Bacheca acquirente | `4418:164949` |
| A-P2 · Fai una proposta, 2 di 2 · Prezzo e data del rogito | Bacheca acquirente | `4418:165017` |
| Onboarding di fase (Venditore, una box) | T1b | `4418:165092` |
| D-1a / T3a · Prima risposta di Marco ricevuta (Acquirente) | — | `4418:165134` |
| Card · Immobile visitato in Bacheca acquirente, tre stati | — | `4418:165692` |

## Le tavole mobile 440

Prima fila, pagine di stato (una per ogni pagina desktop, esclusa la T1 scartata):

| Tavola | Node |
|---|---|
| M-0 / T1 · Prima proposta ricevuta (invio unico) | `4435:166235` |
| M-0c / Prima risposta in preparazione, 2 di 4 | `4435:166729` |
| M-1 / T2 · Venditore | `4435:165756` |
| M-1 / T3 · Acquirente | `4435:167223` |
| M-1a / T3a · Prima risposta di Marco ricevuta | `4435:167671` |
| M-2 / T2b · Stallo, suggerimento | `4435:168133` |
| M-3 / T2c · Stallo, media proposta | `4435:168609` |
| M-5 / Chiusura bloccata | `4435:169062` |
| M-6 / Riepilogo in corso | `4435:169514` |
| M-7 / T4 · Riepilogo e conferma | `4435:169841` |
| M-8 / T5 · Chiusura | `4435:170226` |

Seconda fila, fogli:

| Foglio | Fondo | Node |
|---|---|---|
| P1–P5 · prima risposta | T1b mobile | `4435:170615`, `4435:170689`, `4435:170754`, `4435:170823`, `4435:170902` |
| B2 · Rivedi e invia | T1b mobile | `4435:170979` |
| R1–R3 · prezzo, turni successivi | T2 mobile | `4435:171065`, `4435:171138`, `4435:171191` |
| R4 · data di consegna (Acquirente) | T3 mobile | `4435:171238` |
| A-P1, A-P2 · Fai una proposta | nessuno | `4435:171285`, `4435:171355` |
| Punti della trattativa (dalla barra) | T2 mobile | `4435:171465` |
| Onboarding di fase | T1b mobile | `4435:171428` |
| Le tue trattative su questo immobile (dal selettore) | T2 mobile | `4435:171951` |

## Elenco trattative dal selettore

Ricreato dal backup (`4300:33179` il popover, `4300:32909` il foglio) e portato sulla v2: il popover si apre sotto il chip «1 di 3 su questo immobile» di T2, il foglio mobile ha sotto la T2 mobile. Contenuti invariati rispetto al backup, compreso il link in fondo.

Applicata la regola dello stroke: le righe su cui tocca al venditore portano un marcatore da 4 px in `text-fg-warning` a sinistra. Qui sono la trattativa corrente con Giulia Rossi («Tocca a te») e quella con Chiara Vietti («Accordo da confermare»); la riga di Andrea Bianchi («In attesa di Andrea Bianchi») resta neutra. La stessa regola è stata estesa alle righe del blocco «Trattative in parallelo» di T1, T1b, D-0c, T2, T2b, T2c, chiusura bloccata, D-4 e delle pagine mobile corrispondenti. Tecnicamente è un rettangolo in posizione assoluta dentro la riga, con clip: le righe hanno già un bordo di 1 px su tutti i lati, e un nodo Figma non regge due colori di stroke.

## Regole mobile

Shell mobile: `System Bar`, `Navbar` Device=Mobile, colonna da 408 (padding 16, padding-bottom 96), barra sticky in fondo, back link al posto del breadcrumb, titoli di sezione a 22.

**Barra dei punti al posto dello stepper.** In cima, sotto titolo e selettore: «TRATTATIVA · MANCANO 2 PUNTI SU 5», una riga che dice su cosa tocca a te («Tocca a te: prezzo») e cinque segmenti nello stesso ordine della pagina. Verde (`text-fg-success-strong`) = concordato o completato, warning = tocca a te, grigio = in attesa dell'altra parte. «Vedi i punti ›» apre il foglio con la lista completa dello stepper e i collegamenti a guida e riepilogo.

**Sfondo della barra: `bg-white`** (dal 24/09), la stessa variabile del blocco stepper in spalla su desktop. Prima era `bg-surface-subtle`, come le card, e la barra si leggeva come la prima sezione della pagina. Il bianco funziona finché nessun'altra card mobile è bianca.

**Un solo bottone pieno per schermata, nella barra sticky.** La CTA principale della pagina sale nella barra. Nei riquadri la CTA diventa Outline; nella prima risposta il bottone del blocco «La tua prima risposta» sparisce, e il blocco resta come stato. Il riepilogo in corso non ha barra sticky.

**Riquadri.** Padding 16. Il badge scende sotto la provenienza. Il piede resta orizzontale, tranne nello stallo.

**Dichiarazioni.** Le due card si impilano.

**Fogli.** Ancorati in basso, angoli superiori a 16, chiusura in alto a destra. Il contenuto è quello della modale desktop a 392. Il confronto prezzi si ricostruisce a 352: i punti mantengono la posizione relativa sull'asse, la differenza scende sotto l'etichetta a 12 px. I fogli P1, P3 e P4 superano i 900 px di altezza: in sviluppo il corpo scorre dentro il foglio.

**Fondi.** I fogli della proposta dell'acquirente non hanno una pagina sotto: non esiste ancora una bacheca acquirente mobile. I fondi PNG di T1b, T2 e T3 mobile sono stati riesportati il 24/09 dopo il cambio di sfondo della barra, e `pg2bg` è aggiornato con i nuovi hash.

## Struttura della pagina

Restano breadcrumb, titolo, selettore e avviso. Poi due sezioni: «Argomenti da trattare» e «Dichiarazioni delle parti». In fondo il blocco «Trattative in parallelo» e «Annulla la trattativa». Rispetto alla PG2 precedente sono uscite le due card delle parti, la riga «Passo successivo» con la barra a otto segmenti e il link «Come funziona la trattativa».

**Argomenti prima delle dichiarazioni.** Dopo il primo scambio le dichiarazioni sono da leggere, gli argomenti cambiano ogni giorno.

**Proponi entra nei riquadri.** «Proponi» compare solo su un argomento che nessuno ha ancora proposto, in pratica la data di consegna nella prima risposta.

**Il riquadro.** In alto marcatore di stato, titolo, valore corrente, provenienza e badge. In basso un piede: a sinistra «Vedi le proposte (n)», a destra la CTA. Aperto di default il riquadro su cui tocca agire.

**Dichiarazioni** in due card affiancate, con domanda, risposta e, quando serve, la condizione sospensiva generata con la sua scadenza.

**Meno avvisi.** Info in T1, T2 e T3a, Warning solo in chiusura bloccata, nessun avviso nelle altre.

**Condizioni sospensive nel riepilogo.** 24 px fra le condizioni attive e la riga «Non si applicano».

## Gerarchia dei bottoni e colore

**Un solo Primary per pagina.** Nella prima risposta l'unico Primary è «Invia a Giulia Rossi», disabilitato finché le quattro parti non sono pronte; i bottoni dei riquadri sono Outline. Nei turni successivi, se tocca a te su più argomenti (T3a), il Primary va sul primo in ordine di pagina e gli altri sono Outline. Su mobile il Primary sta nella barra sticky.

**Badge neutri.** Tutti Brand white. Gray nel DS esiste solo come contatore numerico.

**Stroke di stato.** 4 px a sinistra, interno. `text-fg-warning` sui blocchi «tocca a te», `text-fg-success-strong` (dal 28/09) su riquadri e card completati o concordati. Il warning vale per: riquadri, card delle dichiarazioni, card in Bacheca, righe delle trattative in parallelo e dell'elenco dal selettore. Icone: orologio = tocca a te, cerchio = in attesa dell'altra parte, spunta = fatto o concordato.

**Trattative in parallelo.** Blocco in `bg-surface-subtle`, presente in T1, T2, T2b, T2c, chiusura bloccata, T3 e T3a.

## T3a · Giulia dopo la prima risposta di Marco

Marco ha mandato insieme controproposta sul prezzo (€ 275.000), controproposta sulla data del rogito (15/09/2027), proposta sulla data di consegna (15/10/2027) e le sue dichiarazioni. Per Giulia i tre argomenti sono tutti «tocca a te», con stroke; da qui ogni risposta parte subito.

Nel riquadro della data del rogito una riga di contesto spiega perché la data è slittata: «Marco Ferrero ha dichiarato che serve una sanatoria: con il mutuo, i tempi indicativi salgono a circa 9 mesi dalla firma.»

## Card in Bacheca acquirente

Istanze del componente `card` (type=acquirente) già usato nella bacheca di Sprint 2, con testi e bottoni sovrascritti, in tre stati: dopo la visita («Fai una proposta»), proposta inviata, tocca a te (con stroke). La pagina che le ospita resta all'epica Visita. Il component set `card` segnala errori nel file.

## Le modali

Card crema da 668, eyebrow monospaced, titolo Heading 2, azioni a tutta larghezza. Il fondo è la pagina da cui si apre, esportata in PNG.

**Comuni a tutte.** Nessun passo di scelta della condizione. Campo «Nota per … (facoltativa)» in ogni proposta e controproposta. Nessuna scadenza negli argomenti: la scadenza sta nelle dichiarazioni, e la indica chi dichiara (ipotesi). Sulle date nessun rifiuto secco.

**Prima risposta (P1–P5).** CTA «Aggiungi alla risposta» con una riga sotto: «Giulia Rossi la riceve quando invii la risposta completa». Il confronto prezzi usa il prezzo dell'annuncio. Si chiude con B2 «Rivedi e invia».

**Turni successivi (R1–R4).** Invio diretto. In R1 il confronto usa come riferimento l'ultima proposta del venditore. R2 rifiuto con motivazione facoltativa. R3 conferma prima di accettare. R4 lato acquirente sulla data di consegna.

**Prima proposta dell'acquirente (A-P1, A-P2).** Parte dalla card in Bacheca. Prima le dichiarazioni, poi prezzo, data del rogito e nota.

**Onboarding di fase.** Una box sola per il venditore, con «Inizia la trattativa» e «Leggi la guida alla trattativa».

## Scelte di contenuto

- Data di consegna: «Data di consegna delle chiavi» ovunque, come in PG1.
- Riepilogo e T4: tre argomenti, poi le condizioni sospensive, poi la riga con quelle che non si applicano.
- T4: «Modifica un argomento»; sotto la CTA «Confermando riconosci l'intervento mediatorio di Cleclà» con il (?).
- T5: via verifica catastale e riga di responsabilità; «Mancano 2 documenti» sotto i documenti d'identità; CTA «Indica chi firma con te».
- Modali: eyebrow «RISPONDI ALLA PROPOSTA», «FAI UNA PROPOSTA · PASSAGGIO n DI 2».
- Mobile: «Vedi i punti ›» per aprire la lista dei punti.

## Discrepanze da segnalare

- «Argomenti da trattare» e «Dichiarazioni delle parti» restano termini nuovi, fuori dal glossario.
- «Intervento mediatorio» contro il copy approvato «Non siamo il terzo attore della compravendita» (§15.7 del glossario).
- PG1 dice «Ogni sì genera la condizione corrispondente», ma per la regolarità è il no a generare la sanatoria.
- «Identificazione della clientela ai fini dell'antiriciclaggio» al posto di «dichiarazione antiriciclaggio»: il glossario va aggiornato.
- «Si scioglie» per il contratto quando la condizione non si avvera: forma presa dalle correzioni di PG1.
- Destinazione del link in fondo all'elenco trattative: nel backup è «Vai ai tuoi immobili», mentre la destinazione prevista è l'area Trattative della Bacheca. Il nome va scelto insieme alla pagina indice.

## Punti aperti

- Annullamento: se l'acquirente può riaprire con una nuova proposta sullo stesso immobile; cosa vede l'altra parte dopo l'annullamento (non disegnato); conferma delle quattro conseguenze.

- M-0c: nella barra dei punti i segmenti di prezzo e data del rogito sono verdi anche se le parti sono solo pronte. Non coerente con la regola dello stroke, da decidere.
- Le righe delle trattative in parallelo restano con il solo marcatore warning.

- Chi fissa la scadenza di una condizione sospensiva: nelle modali il dichiarante, da confermare.
- Se una dichiarazione si modifica dopo l'invio.
- Chiusura bloccata vista dall'altra parte: annotata, non disegnata.
- Pagina indice delle trattative e blocco Trattative della Bacheca non ancora disegnati.
- «Accordo da confermare» su un'altra trattativa: se tocca davvero al venditore dipende da chi dei due ha già confermato. Nell'elenco è trattato come «tocca a te».
- Badge neutro nel DS: serve una variante Gray con testo.
- Riquadro con stroke di stato: da promuovere a componente, con la proprietà «tocca a te» booleana; lo stesso per la riga di elenco con il marcatore.
- Regola degli estremi dell'asse del confronto prezzi.
- Component set `card` della bacheca con errori.
- Mobile: colore dei segmenti «fatti» della barra (verde) diverso dallo stepper desktop, dove i punti completati sono neutri, e dalle barre di PG3 e PG4 mobile (pieni fino al passo in corso). Da confermare.

## Nota operativa

Plugin data su `figma.root`: `pg2lib` (pagine desktop), `pg2modal` (modali), `pg2mob` (pagine mobile), `pg2sheet` (fogli), `pg2bg` (hash dei fondi). **Dopo l'eliminazione della PG2 precedente queste funzioni non girano più**: usavano come modelli da clonare nodi delle vecchie tavole. Le tavole v2 non ne dipendono: sono copie indipendenti. Per riusare le funzioni vanno ripuntate su nodi equivalenti delle tavole v2. Il componente `Help icon (?)` sta nella sezione `DS · Candidati dalla Trattativa 🧩` e non è toccato.

Regole da riapplicare se si ricostruisce un riquadro: badge Brand white, un solo Primary per pagina, link per «Modifica», stroke su «tocca a te», icone orologio/cerchio/spunta. Le pagine mobile sono copie: se una pagina desktop cambia, va rigenerata anche la mobile, e con lei i fondi dei fogli che la usano. Una mobile rigenerata deve avere la barra di percorso su `bg-white`.
