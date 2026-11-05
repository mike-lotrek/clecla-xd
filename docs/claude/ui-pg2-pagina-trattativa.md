# UI — PG2 Pagina trattativa (Sprint 4)

File Figma: **Cleclà | UI** → pagina `🫟 UI Layouts – WIP`, sezione `PG2 · Pagina trattativa`.
Trentaquattro frame, generati dai wireframe della sezione `PG2 · Pagina trattativa — Desktop 1440` con i componenti della libreria **Cleclà | Design System (Flowbite)**.

**Pagine di stato — desktop 1440 e mobile 440**

| Stato | Desktop | Mobile |
|---|---|---|
| T2 · Venditore | 1440 × 2062 | 440 × 2757 |
| T2b · Stallo · Cleclà suggerisce la media (Venditore) | 1440 × 2205 | 440 × 2958 |
| T2c · Stallo · la media è sul tavolo (Venditore) | 1440 × 2205 | 440 × 2958 |
| T3 · In attesa (Acquirente) | 1440 × 2034 | 440 × 2586 |
| T4 · Riepilogo e conferma | 1440 × 2075 | 440 × 2874 |
| T5 · Chiusura, in attesa del preliminare | 1440 × 1122 | 440 × 1607 |

**Overlay e modali — desktop 1440 e mobile 440**

| Frame | Desktop | Mobile |
|---|---|---|
| Onboarding di fase 1, 2, 3 di 3 (T1) | 1440 × 900 | 440 × 956 |
| Proponi una condizione — 1, 2, 3 di 3 | 1440 × 900 | 440 × 956 |
| Rispondi — Data del rogito | 1440 × 900 | 440 × 956 |
| Rispondi — Data del rogito · «Accetta» | 1440 × 900 | 440 × 956 |
| Rispondi — Data del rogito · «Fai una controproposta» | 1440 × 900 | 440 × 956 |
| Rispondi — Prezzo (con Rifiuta) | 1440 × 900 | 440 × 956 |
| Rispondi — Prezzo · «Rifiuta» | 1440 × 900 | 440 × 956 |

Restano fuori solo gli stub T0 e T6, confine dichiarato dal wireframe.

Accanto alla fila delle pagine di stato ci sono due tavole di riferimento, non navigabili: il documento di puntuazione con tutti i blocchi aperti, nella versione Venditore (898 × 1903) e in quella Acquirente (898 × 1907).

Stato: **epica PG2 riaperta e richiusa il 16/09** dopo le guide del cliente del 14/09.

## Revisione del 16/09

### Il documento di puntuazione è diviso in blocchi per gruppo

Era una card unica con quattro occhielli e dieci righe separate da divider: si leggeva come un elenco lungo, e per arrivare alla condizione su cui agire si scorreva tutto. Ora sopra restano titolo, paragrafo e il link «Scarica il documento (PDF)», e sotto c'è **un blocco bianco per gruppo**, apribile e chiudibile con il segno +/− già usato in PG1 e, prima ancora, nel «Vedi dettaglio» del calcolatore budget (frame `Calcolatore-Budget/Risultato` e `Calcolatore-Budget/3`).

La testata di ogni blocco porta il nome del gruppo in Heading 4/Medium e, sotto, un conteggio che dice quante condizioni contiene e in che stato sono: «3 condizioni · 1 in attesa di risposta», «4 condizioni · 1 accettata, 1 rifiutata». Serve a tenere informativo il blocco chiuso, altrimenti chiudere sarebbe solo nascondere.

**Default: aperto il gruppo su cui tocca agire, chiusi gli altri.** In T2 e T3 è «Tempistiche e disponibilità», che porta la data del rogito in attesa di risposta; in T2b è «Prezzo e pagamento».

Il blocco è un frame bianco (`input/bg-default`) con raggio 12 e padding 20/24 su desktop, 16 su mobile, dentro la card crema della sezione: lo stesso rapporto fondo-card di PG1. La riga di condizione non cambia.

**L'ordine dei blocchi segue le fasi**: prezzo, condizioni sospensive, dichiarazioni, tempistiche. «Tempistiche e disponibilità» chiude la lista perché la data del rogito si concorda per ultima, in Fase 3, quando prezzo e condizioni sono noti; finché il prezzo non è concordato la riga porta lo stato «Si concorda dopo il prezzo», come si vede in T2b. Consegna del possesso e indennità restano dichiarabili dal Venditore già in Fase 2, quindi il blocco non è bloccato per intero: lo è la singola condizione.

**Ogni blocco porta un marcatore di stato**, uno solo, quello che chiede azione: spunta verde se tutte le condizioni applicabili sono concordate, orologio warning se ce n'è una in attesa di risposta, cerchio neutro se restano cose da affrontare. Il dettaglio lo dà il conteggio in testata («4 condizioni · 1 accettata, 1 rifiutata»). Mostrare un segno per condizione trasformerebbe la testata in una seconda barra di progresso, contro la regola delle forme fissata in PG3.

Il callout «I mobili si trattano fuori da qui» è sceso dentro il blocco «Prezzo e pagamento»: parla di cosa entra nel prezzo, e in fondo alla pagina era staccato dal suo oggetto.

Accanto alla prima pagina stanno due **tavole di riferimento** — `Riferimento · Documento di puntuazione, tutto aperto`, una per ruolo — con i quattro blocchi aperti insieme. Non sono schermate: servono a leggere il contenuto per intero senza aprire un blocco alla volta, e lo dichiarano nell'etichetta sopra la tavola.

### Le condizioni sospensive scendono a quattro

«Acquisto o soluzione abitativa del venditore» non compare fra le condizioni delle guide del 14/09 ed è uscita dal gruppo, dal documento di puntuazione e dalla lista della modale. Restano mutuo, vendita di un immobile dell'acquirente, prelazione agraria, regolarità edilizia e conformità catastale.

La barra dell'accordo resta a **otto segmenti**: conta le condizioni applicabili, e quella uscita era «non applicabile».

### La modale «Proponi una condizione» non ripropone le concordate

Una condizione su cui c'è già un accordo non si ridiscute, quindi non compare più fra le opzioni: sono uscite le tre righe che portavano il badge «Già concordata» — prezzo, mutuo, sanatoria — e con esse i due gruppi rimasti senza opzioni. Restano sei opzioni in due gruppi. Il gruppo si chiama ora **«Condizioni sospensive»**, come in pagina e nei frame approvati (I43): «Clausole sospensive» era l'unica occorrenza fuori riga.

Effetto collaterale: il foglio mobile non ha più bisogno del corpo scorrevole, e la modale desktop torna in un frame da 900.

### Lo stallo sul prezzo è uno stato, T2b

Il documento del cliente dà la regola — dopo due proposte rifiutate senza accordo, Cleclà suggerisce la media fra l'ultima proposta e l'ultima controproposta — ma nella UI non esisteva nulla. Ora c'è uno stato dedicato, desktop e mobile:

- la condizione Prezzo prende il badge **«In stallo»** (Warning) e mostra l'ultima proposta con la controproposta a fianco;
- il blocco «Prezzo e pagamento» si apre da solo, gli altri restano chiusi;
- sotto la riga, un `Alert` Complex/Info porta il prezzo suggerito e il calcolo da cui esce, con due uscite;
- la responsabilità passa a «Tocca a entrambi» e l'avanzamento scende a 2 condizioni su 8.

Il prezzo suggerito resta una proposta, non un prezzo imposto: è la formula del documento e regge il principio «le decisioni finali sono sempre le tue».

### Lo stallo è in due tempi (18/09)

La schermata dello stallo faceva due cose insieme: annunciava il blocco e offriva già «Accetta € 290.000», come se la media fosse una proposta che Cleclà mette sul tavolo. Ora sono due stati.

**T2b — Cleclà suggerisce la media.** L'`Alert` dice «Vi siete fermati sul prezzo: ti suggeriamo la media» e porta il numero con il calcolo da cui esce. La CTA è **«Proponi € 290.000»**, la seconda uscita resta «Continua a trattare», la condizione Prezzo porta il badge **«In stallo»** e la responsabilità resta **«Tocca a entrambi»**: il suggerimento arriva a tutti e due e si muove chi vuole per primo.

**T2c — la media è sul tavolo.** Una delle due parti ha proposto. La riga di prezzo dice «Proposta: € 290.000 · da Giulia Rossi, oggi · su suggerimento di Cleclà», il badge torna **«In attesa di risposta»**, il contatore delle proposte passa a tre, la CTA è **«Accetta € 290.000»** e la responsabilità diventa **«Tocca a te»**.

I due frame sono in fila, desktop e mobile, con l'etichetta sopra.

**Da segnalare al cliente**: il documento di piattaforma dice che «Cleclà propone la media», cioè che è Cleclà a mettere la cifra sul tavolo. Qui Cleclà suggerisce e la proposta la fa una delle due parti. È una differenza di responsabilità, non di parole, e regge meglio il principio «le decisioni finali sono sempre le tue»: va confermata.

### Le parti, le trattative in parallelo, la CTA di riga

**Le due parti sono due card indipendenti affiancate.** L'avatar è allineato in alto al nome e l'identità verificata scende da badge a riga minima — pallino verde da 8 px e testo a 12 in `text-fg-success-strong`: era il segno più forte della testata per un'informazione su cui non si agisce.

**Le trattative in parallelo diventano righe cliccabili**: fondo bianco, bordo, stato a destra e freccia; la riga corrente resta senza fondo e senza freccia, così si distingue da sola. Su mobile l'accesso rapido è il chip «Trattativa 1 di 3» in testata di pagina. Un box flottante in basso è stato scartato: competerebbe con la barra sticky della CTA e coprirebbe contenuto.

**La CTA di riga è un link, non un bottone.** «Rispondi →» usa `Button` Link-orange Size=Small, l'unica taglia piccola che il DS espone davvero: il bottone pieno pesava più della condizione a cui si riferisce.

### Seconda passata del 16/09

**I blocchi prendono il crema, il contenitore sparisce.** Prova chiesta in revisione: la sezione «Documento di puntuazione» non è più una card: titolo, paragrafo e link al PDF stanno sul fondo nudo della pagina, allineati alla colonna di contenuto, e i quattro blocchi in accordion sono in `bg-surface-subtle`. Il rapporto si inverte rispetto a prima, quando i blocchi erano bianchi dentro una card crema. Da verificare il badge `Brand white` su questo fondo: è il limite C7, e su crema la pillola perde il contorno.

**Fuori i badge che non dicono lo stato di una condizione.** «Prezzo verificato — Studio di vendibilità disponibile», «Prezzo verificato — coerente con i valori di mercato della zona» e «Inserita dal sistema» sono usciti da pagine e tavole, dodici occorrenze: mettevano sulla stessa riga due informazioni di natura diversa e rendevano più lenta la scansione degli esiti. Nella colonna dello stato resta solo l'esito della condizione.

**La sidebar non è più alta quanto la pagina.** Segue il pattern del componente `Sidebar - Chiusa`: pannello da 900 px dentro un contenitore da 948, e il bottone di apertura da 32 px sotto, centrato sul pannello. Applicato ai cinque frame desktop di PG2; le altre PG usano ancora la sidebar stirata.

**Le due card delle parti sono su tutte le pagine**, T4 e T5 comprese.

**Su mobile le righe dello switch tornano orizzontali**: i due testi in una colonna a sinistra, la freccia a destra. Il layout verticale ereditato dalla riga di condizione mandava la freccia sotto il testo.

**Lo stepper in spalla è allineato a PG1: si vede solo la tappa Trattativa.** La spalla mostrava tutte e cinque le tappe del percorso venditore — Profilo immobile, Pubblicazione, Visite, Trattativa, Contratto — con i separatori verticali e i quattro sotto-passi dentro la tappa corrente. Ora restano il titolo «Trattativa» e i suoi quattro sotto-passi, ciascuno con l'icona del passo come in PG1: `icon/description` per «Guida alla trattativa», `icon/edit` per «Proposta delle condizioni», `icon/compare_arrows` per «Risposte e controproposte», `icon/handshake` per «Accordo raggiunto». `Trust inner` scende da 637 a 357 px e la spalla da 905 a 604-625. Gli stati Completed / Active / Initial dei sotto-passi restano quelli di ciascuno stato di pagina.

Rifatti i fondi PNG dei undici overlay desktop, che sono un'esportazione di T2 e non si aggiornano da soli. I fogli mobile non sono toccati: la barra di percorso mobile non è cambiata.

### La reciprocità è dichiarata a entrambi

Il venditore leggeva quante trattative ha aperte, l'acquirente che «il proprietario può trattare anche con altri». Nessuno dei due leggeva che vale anche al contrario. Ora la riga dice, da una parte, «Anche Giulia Rossi può trattare su altri immobili: finché non firmate il preliminare non siete vincolati, né tu né lei», e dall'altra la stessa cosa ribaltata.

### Il punto interrogativo è sempre il bottone indaco

Dove un «?» apre un popover, è il `Help icon (?)` — cerchio indaco da 18 — e non l'icona nuda: nelle due modali e nei due fogli «Proponi una condizione» il punto interrogativo accanto ai titoli di gruppo è ora quel bottone. Per riusarlo ovunque è diventato un componente locale, nella sezione `DS · Candidati dalla Trattativa 🧩`.

**Il bottone indaco fa solo quello.** Negli `Alert` il `Right icon style` è la ✕ di chiusura del DS: lì l'icona a destra chiude l'avviso, non apre un aiuto.

### Cosa resta fuori

Il passo 5 delle guide — i dati di chi firma insieme a te — resta in PG3, come deciso: la trattativa si chiude sull'accordo, la raccolta delle persone appartiene alla preparazione della firma.

## Revisione del 17/09 — le cifre nelle modali

### La cifra in discussione diventa la cosa più grande della modale

Nelle modali «Rispondi alla condizione» il valore su cui si decide stava a 20 px, la stessa misura di un titolo di blocco: si leggeva come una riga fra le altre. Ora è a **48/Light**, la misura scelta in revisione: 60 px, come il risultato del calcolatore budget, prendeva troppo spazio verticale dentro una modale che ha già tre bottoni in fondo. Nessuna linea di separazione sotto la cifra. Stessa misura su desktop e su mobile.

Vale per «€ 270.000» nelle due modali sul prezzo e per «15/03/2027» nelle tre sulla data del rogito, dove il dato protagonista è la data.

Restano a misura di testo le cifre che non sono protagoniste: il campo «Detrazione dal prezzo» del passaggio 2 di «Proponi una condizione», che è un input, e il «€ 5.000» dentro la frase di anteprima del passaggio 3.

### Il riferimento di mercato diventa un confronto fra tre cifre

La barra a quattro fasce è durata una revisione. Nelle modali sul prezzo il blocco «Riferimento di mercato» è uscito e al suo posto c'è **«Confronto prezzi»**, l'opzione A scelta e disegnata in revisione su `3858:100090`: un asse lineare e sotto una tabella di tre righe.

L'asse è una traccia grigia larga quanto il blocco, con il dominio da 260 a 295 mila euro, e tre punti: la proposta in discussione è un cerchio pieno indaco da 16 px con bordo bianco, lo studio di vendibilità un pallino indigo/500 da 12, il prezzo dell'annuncio un cerchio vuoto bordato indaco da 12. Chi guarda vede prima dove cade la proposta rispetto alle altre due, poi legge i numeri sotto.

La tabella ripete i tre marcatori come simbolo a inizio riga e porta etichetta, cifra e differenza rispetto alla proposta: «€ 8.000 in meno (−2,9%)» per lo studio, «€ 15.000 in meno (−5,3%)» per l'annuncio. La riga della proposta non ha differenza, perché è il termine di paragone. L'intestazione del blocco è su due colonne: il titolo a sinistra, «Differenza della proposta» sopra l'ultima colonna.

**Le fasce escono dalle modali di risposta.** Consigliato, Poco consigliato e le altre dicono se conviene pubblicare a quel prezzo; qui la domanda è di quanto la proposta si scosta da due cifre note, e la risposta è un numero. La scala delle fasce resta dov'è nata, nella Pubblicazione.

Su mobile la traccia si ricostruisce a 352 px e i punti si ricalcolano sullo stesso dominio: 92,6 per la proposta, 175,0 per lo studio, 245,4 per l'annuncio. Le tre colonne della tabella a 352 px non ci stanno, quindi **la differenza scende sotto l'etichetta** a 12 px e il prezzo resta a destra; l'intestazione perde la colonna «Differenza della proposta», che non ha più una colonna da intestare.

**Nello stato «hai premuto Rifiuta» il confronto non c'è**, né su desktop né su mobile: restano la cifra proposta, il campo della motivazione e la CTA. Chi ha già deciso di rifiutare non ha più bisogno del paragone, e il foglio mobile scende da 740 a 590 px.

### Riaprire una condizione ha finalmente un punto di ingresso

La modale di accettazione lo prometteva già — «Accettando, questa condizione si chiude: Potrai riaprirla, ma dovrai ridiscuterla con Giulia Rossi» — ma in pagina non c'era nessun modo di farlo. Ora **in fondo al blocco di gruppo, sotto un divider, c'è un link secondario «Riapri una condizione concordata»**, `Button` Link-dark Size=Small, lo stesso peso di «Annulla la trattativa» e di «Modifica una condizione» in T4.

**Compare solo nei gruppi che contengono almeno una condizione con badge «Accettata».** In T2 e T3 sono Prezzo e pagamento, Condizioni sospensive e Dichiarazioni; resta fuori Tempistiche e disponibilità, dove non c'è ancora niente di concordato, e in T2b resta fuori anche il Prezzo, che è in stallo. In tutto 25 occorrenze su nove frame, tavole di riferimento comprese.

Sta in fondo al gruppo e non su ogni riga chiusa: con quattro condizioni accettate dentro un gruppo, quattro link ripeterebbero la stessa azione proprio sulle righe che devono stare zitte. Una condizione rifiutata non passa da qui: si ripropone dalla modale «Proponi una condizione», che le rifiutate le tiene in lista e le concordate no.

Quello che il link apre non è ancora disegnato, ed è annotato come da definire: la simmetria vorrebbe una modale che elenca le sole condizioni concordate di quel gruppo, l'opposto esatto di «Proponi una condizione».

### Lo stepper della trattativa ha la sua icona

`icon/compare_arrows` ha sostituito il segnaposto `radio_button_unchecked` sul terzo sotto-passo, «Risposte e controproposte», in tutte e dieci le occorrenze dello stepper della trattativa: PG1, PG2 e le tavole di stato. L'icona esiste nella pagina Icons del design system (node `3195:21517`) e si istanzia dalla sua chiave di componente. Il limite registrato il 16/09 — «non importabile via MCP» — era sbagliato: non funzionava `importComponentByKeyAsync`, non l'icona.

Effetto sulle altezze: la modale sul prezzo passa da 745 a 757 px dentro un frame da 900, il foglio mobile da 794 a 757 dentro 956.

## Decisioni di layout — pagine di stato desktop

- **Stessa shell di PG1**: navbar, sidebar dell'area autenticata, colonna di contenuto da 850 (frame 898 con padding 24), spalla da 322. T2, T2b, T3, T4 e T5 sono la stessa pagina in cinque momenti.
- **Lo stepper orizzontale del wireframe diventa la spalla, e la spalla mostra solo la tappa Trattativa.** Come in PG1: titolo della tappa e i quattro sotto-passi con le icone. Il sotto-passo attivo cambia con lo stato: `Risposte e controproposte` in T2, T2b e T3, `Accordo raggiunto` in T4 e T5.
- **Il floating button «Serve aiuto?» sparisce**: il suo posto è la card «Hai dubbi?» in fondo alla spalla.
- **La spalla non porta l'indice**: il documento di puntuazione è già un indice di sé stesso, e dal 16/09 lo è anche a colpo d'occhio.
- **«Scarica il documento (PDF)» sta nella testata della sezione**, sopra i blocchi. Il PDF è quel documento. Stessa scelta in T4 con «Scarica il riepilogo (PDF)».
- **La riga di responsabilità è una card a sé**, con l'occhiello «PASSO SUCCESSIVO», l'etichetta a 20 px e, a destra, il contatore e la barra dell'accordo.
- **La riga di condizione è un blocco costruito a mano**, non un `List item`.
- **Il CTA «Rispondi» sta sotto il badge, nella colonna destra della riga.**
- **In T4 l'header resta quello di T2**, contro il wireframe che lo riduce a titolo e badge.
- **In T5 la barra delle condizioni cade**: il progresso che conta è quello dei documenti.

## Decisioni di layout — mobile 440

La shell è quella di PG1 mobile: `System Bar`, `Navbar` Device=Mobile, colonna da 408 (frame 440, padding 16, padding-bottom 96), barra sticky in fondo.

- **La spalla si scompone**: il percorso diventa una barra in cima con «Sei qui: Trattativa», il contatore di tappa e la barra segmentata; la card «Hai dubbi?» scende in fondo. Su T3 la barra ha quattro segmenti e dice «tappa 3 di 4».
- **Cadono i sotto-passi della trattativa**: su 440 sarebbero una seconda mappa sopra la prima.
- **Il breadcrumb diventa un back link singolo.**
- **La riga di condizione si impila**: nome, valore e provenienza, poi il badge di stato e l'eventuale azione.
- **La CTA principale passa nella barra sticky**; le azioni secondarie restano in fondo al contenuto come link.
- **Si impilano** anche le due parti, le trattative in parallelo, le condizioni concordate di T4, i passi di «Cosa succede dopo», i documenti di T5 e, in T2b, le due uscite della proposta di Cleclà.
- **«Prezzo verificato — Studio di vendibilità disponibile» non è più un badge ma una riga con icona**: il Badge non manda il testo a capo e a 376 px la pillola tagliava la seconda riga.
- **Titolo di pagina a 28, titoli di sezione a 22**, come in PG1 mobile; le sezioni passano da padding 24 a 16.

## Decisioni di layout — overlay e modali

Il guscio desktop segue gli esempi già presenti nel file, nella sezione `Esempi di modali`:

- **Card da 668, fondo crema `bg-surface-default`, raggio 16, padding 24, nessuna ombra.** Scrim `bg-modal-bg` con opacità di riempimento 80%.
- **Chiusura in alto a destra**, dentro la card, con `Nav tabs` Type=Primary-square.
- **Occhiello monospaced e titolo Heading 2, centrati**; corpo allineato a sinistra.
- **Azioni in fondo al corpo, centrate**, con la secondaria come `Link-dark` sotto la primaria.
- **La card di onboarding** segue la stessa lingua ma resta a 560: è una coach card a tre passaggi.
- **La pagina sotto è reale**: T2 esportato in PNG come fill di un rettangolo, coperto dallo scrim. Un'immagine per il desktop, una per il mobile. **Se T2 cambia vanno rigenerate**, ed è successo due volte il 16/09: si esporta T2 una volta, si crea l'immagine con `figma.createImage` e si riassegna il fill a tutti i rettangoli di fondo in un passaggio.
- **Gli stati alternativi delle modali «Rispondi» sono frame a sé.**
- **La modale sul prezzo arriva a 863 px in un frame da 900**: con la cifra a 48 e il confronto prezzi restano 19 px per lato. Il foglio mobile corrispondente sta a 907 su 956, ancorato in basso.
- **Sulle date niente rifiuto secco**; sul prezzo il rifiuto c'è, con motivazione facoltativa.

**Su mobile la modale diventa un foglio ancorato in basso**, largo quanto lo schermo, angoli superiori a 16 e nessun angolo in fondo. Dopo la revisione del 16/09 nessun foglio supera l'altezza utile, quindi il corpo scorrevole non serve più: il foglio torna a hug e si ancora al fondo.

## Delta della variante Acquirente (T3)

- percorso a quattro tappe (Ricerca · Visita · **Trattativa** · Contratto), avatar di ruolo «A», breadcrumb «Le mie trattative»
- «(tu)» passa da Marco a Giulia; utente in navbar «Giulia / GR»
- responsabilità: «In attesa di Marco Ferrero»
- avviso di silenzio prolungato con «Manda un promemoria»
- riga «Data del rogito» senza CTA: al suo posto «In attesa della risposta di Marco Ferrero»
- provenienze ribaltate: «da te, 4 giorni fa», «proposta da te», «tua motivazione»
- badge del prezzo: «coerente con i valori di mercato della zona»
- «Trattative in parallelo» dice la reciprocità in una riga, senza i nomi delle altre trattative
- link «Vedi i documenti dell'immobile», che il Venditore non ha

## Mappatura sui componenti della libreria

| Blocco | Componente |
|---|---|
| Navbar | `Navbar` Device=Desktop / Mobile, User=User |
| Sidebar e spalla | shell dell'area autenticata di Sprint 2, clonata da PG1 |
| Shell mobile | `System Bar` (componente locale ereditato da PG1 mobile), barra di percorso e barra sticky di PG1 |
| Breadcrumb | `Breadcrumb` + `Breadcrumb item`, tre livelli, l'ultimo Active |
| Percorso in spalla | `Stepper nav link` Type=Icon shape & text, stati Active/Initial/Completed, una sola tappa visibile |
| Avatar delle parti | `Avatar` Type=Placeholder, Size=base, iniziali MF / GR |
| Blocco di gruppo del documento | frame costruito a mano, testata con `icon/add` / `icon/remove` su `button/border-primary` |
| Stati delle condizioni | `Badge` Type=Default, Size=sm, senza icone |
| Avvisi | `Alert` Default/Warning, Complex/Info, Complex/Warning, Default/Info |
| CTA e link | `Button` Primary / Outline-dark / Destructive-outline / Destructive-fill / Link-dark |
| Chiusura di modale e foglio | `Nav tabs` Type=Primary-square |
| Occhiello di modale e foglio | stile testo `Cleclà/Eyebrow - monospaced/Small` |
| Scelta della condizione | `Checkbox input` Type=Radio input |
| Pillole SÌ / NO | `Radio item` Size=Boxed, Type=Radio button |
| Campi del form | `Input field` State=Filled / Initial |
| Help contestuale P7 | `Help icon (?)`, componente locale: cerchio indaco da 18 con il punto interrogativo |

Mappatura dei badge: Success = accettata, fatto, identità verificata, conclusa · Warning = in attesa di risposta, accordo da confermare, fascia di prezzo poco consigliata, **in stallo** · Danger = rifiutata · Brand blue = inserita dal sistema, prezzo verificato, in corso · Brand white = non ancora affrontata, non applicabile, in attesa.

Lo stato `Disabled` del radio non serve più: le condizioni già concordate non compaiono nella lista.

## Limiti del DS emersi in lavorazione

- **`Stepper nav link` è pensato per fondo scuro.** La variante Initial lega il testo a `text-ondark-medium`: su fondo chiaro il testo sparisce. Serve una variante on-light.
- **Non esiste la taglia Small per i bottoni pieni e outline**: `Size=Small` c'è solo per i tipi Link. È la ragione per cui la CTA di riga è diventata un link arancio: una taglia intermedia per i bottoni pieni servirebbe.
- **Manca un marcatore di stato piccolo.** La spunta, l'orologio e il cerchio vuoto nelle testate dei blocchi sono icone del DS ricolorate a mano: il DS dovrebbe esporre un `Status dot` con i suoi stati.
- **Manca un badge neutro secondario**, e Brand white coincide con uno dei due fondi di superficie.
- **Il Badge non manda il testo a capo.**
- **Manca la scala tipografica mobile.**
- **Modals è 🚧 e Progress Bars sta sotto «🚨 Not used».**
- **`Alert` Complex ha un bottone incorporato** non governato da una proprietà booleana.
- **Il campo data usa `Input field`**: in implementazione va sostituito con il `Datepicker`.
- **Il confronto prezzi non è un componente.** Traccia, punti e righe sono costruiti a mano a 580 px su desktop e a 352 su mobile, e le posizioni dei punti sono coordinate assolute ricalcolate a ogni cambio di larghezza. Un grafico a una dimensione con marcatori legati a un valore, e la sua versione mobile con la differenza sotto l'etichetta, è una cosa che il DS dovrebbe esporre.
- **I colori delle quattro fasce non sono token.** Né qui né nel `Vendibilità` della Pubblicazione: sono valori fissi. Se la scala resta, servono quattro variabili.
- **Manca un componente di blocco espandibile.** La testata +/− dei gruppi è costruita a mano qui come in PG1: va promossa insieme al `Passo di percorso` nato in PG1.

## Punti aperti

- **Il ruolo continua a non cambiare i colori.**
- **Quattro o cinque tappe.** Cinque nel percorso venditore, quattro nell'acquirente, sei nello stepper di «Come funziona». Con la spalla ridotta alla sola tappa Trattativa la domanda resta aperta solo per la barra di percorso mobile, che il conteggio lo dichiara.
- **La voce di breadcrumb dell'Acquirente** («Le mie trattative») resta un'ipotesi.
- **In T3 la condizione sulla sanatoria porta «Inserita dal sistema», in T2 «Accettata»**: sono la stessa trattativa vista dalle due parti e lo stato dovrebbe coincidere. Trovato il 16/09, non risolto.
- **Lo stallo**: se il conteggio delle due proposte rifiutate è visibile prima che lo stallo scatti, e se l'acquirente vede la stessa schermata del venditore. In più, dal 18/09: se il suggerimento arriva davvero a entrambi nello stesso momento o prima a chi deve rispondere.
- **T4 non elenca la Regolarità edilizia e conformità catastale** tra le condizioni concordate, mentre la porta tra le sospensive.
- **Soglia e frequenza del promemoria**: 4 giorni qui, 48 ore in PG4.
- **Abbinamento delle quattro domande di help P7 ai gruppi** della modale Proponi: ipotesi.
- **Il gruppo «Dichiarazioni che entrano nel preliminare»**: raggruppamento ipotizzato in PG1.
- **Il dominio dell'asse.** L'asse va da 260 a 295 mila euro, scelti perché contengono le tre cifre dell'esempio con un margine. Serve una regola: estremi fissi per tutte le trattative, oppure calcolati sul minimo e sul massimo delle cifre in gioco più un margine. Con estremi calcolati due modali diverse non sono confrontabili a occhio; con estremi fissi una proposta fuori scala va gestita.
- **Un prezzo o un intervallo.** La Pubblicazione dà la fascia consigliata come intervallo («235 – 255 mila €»), PG2 come cifra secca («€ 278.000»). Lo studio di vendibilità produce una sola delle due forme.
- **Il nome della scala.** «Fascia di vendibilità» nella Pubblicazione, «fascia» e basta in PG2, e nel glossario il servizio ha già tre nomi (I25).
- **Cosa comporta riaprire una condizione**: se serve il consenso della controparte o se è unilaterale, in che stato torna la condizione e cosa succede al contatore dell'accordo e alla barra a otto segmenti.
- **Due verbi per la stessa azione**: «Riapri una condizione concordata» nei gruppi, «Modifica una condizione» in T4. Ne serve uno solo.
- **La maniglia del foglio mobile**: la chiusura è la ✕; se il foglio si trascina anche verso il basso, va aggiunta.
- **Stati non disegnati**, dichiarati in annotazione: SLA superato (T5), verifica catastale non superata (T5), stato iniziale del bottone di conferma (T4).

## Annotazioni native

Su T2: **il link «Riapri una condizione concordata» e le sue condizioni di comparsa**; modale «Rispondi»; spalla sticky; barra di progresso e token mancanti; visibilità delle trattative in parallelo per ruolo; conferma prima di annullare; **il pattern dei blocchi di gruppo e i default aperto/chiuso**.
Su T2b: **la regola dello stallo e i due punti da sciogliere con i dev**.
Su T3: silenzio prolungato e soglia da definire; breadcrumb non definita; percorso a quattro tappe.
Su T4: doppia conferma asincrona; header completo; punto aperto sulla Regolarità edilizia.
Su T5: i due stati alternativi del blocco documenti; perché cade la barra di progresso.
Su T2 mobile: la barra di percorso come equivalente della spalla; la riga di condizione impilata e il badge del prezzo diventato riga con icona.
Su T4 mobile: la barra sticky e la collocazione delle azioni secondarie.
Sugli overlay: T1 come primo accesso e variante Acquirente; perché solo il passo 3 offre le due uscite.
Sulle modali «Rispondi»: **lo stile della cifra protagonista** e **il dominio dell'asse del confronto prezzi**.
Sulle modali desktop: guscio allineato agli esempi in file; **le condizioni già concordate fuori dalla lista**; ipotesi su help P7; Datepicker; niente rifiuto secco sulle date.
Sul foglio mobile: perché il foglio è ancorato in basso e la maniglia come punto aperto.

## Nota operativa

`importComponentByKeyAsync` non risponde entro il timeout del bridge. Il modo che funziona è `getMainComponentAsync()` seguito da `createInstance()`. Per le icone, `swapComponent()` con il main component preso da un'istanza già presente nel file.

Se l'icona nel file non c'è ancora: `figma_execute_across_files` sul file del design system per trovarla e leggerne la `key`, poi `figma_instantiate_component` con quella chiave. È così che `icon/compare_arrows` è entrato il 17/09, dopo essere stato dichiarato non importabile.

Trappole incontrate:

- **Prima di disegnare un pattern nuovo, cercare se esiste già nel file.** Vale anche per il +/− dei blocchi: era già in PG1 e nel calcolatore budget.
- **Cambiare `layoutMode` da HORIZONTAL a VERTICAL inverte il significato dei sizing.** Dopo ogni flip vanno rimessi `layoutSizingVertical = 'HUG'`, `layoutSizingHorizontal = 'FILL'` e `layoutGrow = 0` sui figli.
- **Un frame creato da zero nasce con altezza fissa**: dopo avergli dato dei figli va messo `layoutSizingVertical = 'HUG'`, altrimenti resta alto quanto era nato e il blocco chiuso prende aria che non ha.
- **Rimuovere nodi mentre si scorre una copia dell'array dei figli lascia riferimenti morti**: `n.parent` diventa null e la chiamata successiva fallisce. Conviene rileggere `parent.children` a ogni giro.
- **`setProperties` rifiuta una chiave che non esiste su quell'istanza**: le chiavi portano il suffisso `#id` e vanno lette da `componentProperties`, non indovinate.
- **I figli di un'istanza non si possono rimuovere**: vanno nascosti con `visible = false`.
- **Per il fondo di overlay e fogli, `exportAsync` + `figma.createImage`** costa una chiamata e un'immagine, contro migliaia di nodi.
