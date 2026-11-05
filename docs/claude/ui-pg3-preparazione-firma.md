# UI — PG3 Preparazione alla firma (Sprint 4)

File Figma: **Cleclà | UI** → pagina `🫟 UI Layouts – WIP`, sezione `PG3 · Preparazione alla firma ✅`.
Diciotto frame, nove desktop 1440 e nove mobile 440, generati dai wireframe della sezione `PG3 · Preparazione alla firma — Desktop 1440` con i componenti della libreria **Cleclà | Design System (Flowbite)**.

**Pagine di fase — desktop 1440 e mobile 440**

| Stato | Desktop | Mobile |
|---|---|---|
| F1 · Parti da completare (Venditore) | 1440 × 1358 | 440 × 2127 |
| F1 · Parti da completare (Acquirente) | 1440 × 1358 | 440 × 2087 |
| F2 · Documenti da caricare e verificare | 1440 × 1222 | 440 × 1736 |
| F3 · Consensi da dare | 1440 × 1415 | 440 × 2147 |
| F4 · Contratto pronto da firmare | 1440 × 2452 | 440 × 3000 |
| F5 · In attesa delle altre firme | 1440 × 1313 | 440 × 1795 |

**Pannelli Yousign — desktop 1440 e foglio mobile 440**

| Frame | Desktop | Mobile |
|---|---|---|
| Carica il documento (passaggio 1 di 3) | 1440 × 900 | 440 × 956 |
| Controlla i dati letti (passaggio 2 di 3) | 1440 × 1219 | 440 × 956 |
| Esito negativo (stato alternativo, passaggio 3 di 3) | 1440 × 900 | 440 × 956 |

Stato: **epica PG3 riaperta il 17/09** sul modello di chi carica i documenti e sugli stati della verifica. Gate di libreria superato su tutti i frame: da 3 a 40 istanze per frame, tutte da libreria, nessun fill o stroke fuori dalle variabili, nessun testo senza stile. Unica eccezione `System Bar`, componente locale già usato da PG1 e PG2 mobile.

## Revisione del 17/09 — chi carica i documenti, e quanti stati servono

### La catena a cinque passaggi è caduta

F1 raccontava per ogni persona una sequenza di cinque passaggi: Invitato → Registrato → Dati inseriti → Documento verificato → Consensi dati. Mescolava tre cose diverse — l'accesso alla piattaforma, l'anagrafica e i consensi — e sopra tutte poggiava su un presupposto che il cliente ha smentito: che ogni cointestatario si registrasse per conto proprio.

**Chi è entrato per primo nella trattativa carica i documenti degli altri.** Il primo Venditore carica il documento delle persone che aggiunge dalla propria parte, il primo Acquirente fa lo stesso dalla sua. Alla persona aggiunta arriva solo l'email di Yousign per la verifica d'identità, che nessuno può fare al posto suo: niente account, niente anagrafica da compilare, niente catena.

Al suo posto, **una riga, un badge**.

### Cinque stati, e due percorsi diversi

| Stato | Badge | Quando |
|---|---|---|
| Da caricare | Brand white | il documento non c'è ancora |
| Email inviata | Warning | il documento è caricato, Yousign ha scritto alla persona |
| Verifica in corso | Brand blue | la persona ha aperto la verifica, Yousign sta controllando |
| Verifica superata | Success | fatta |
| Esito negativo | Danger | con il motivo in chiaro e due uscite |

**Chi era già registrato non passa da «Email inviata» né da «Verifica in corso».** Il primo Venditore e il primo Acquirente sono già in piattaforma: caricano il proprio documento e la verifica è in tempo reale, esattamente come deciso in Sprint 2. Per loro la scala è quella approvata a tre stati: Da caricare → Verifica superata / Esito negativo.

I due stati in più esistono solo per le persone aggiunte, dove un'attesa c'è davvero: fra il caricamento del documento e la verifica passa il tempo che quella persona impiega ad aprire l'email e a farsi riconoscere.

**L'esito negativo porta due uscite**: «Riprova la verifica» e «Invia di nuovo l'email». Sono le due cose che può fare chi ha caricato il documento — ricaricarlo o rimandare la richiesta — e restano affiancate a sinistra, con «Rimuovi» spinto all'estremo destro della riga perché non si legga come un terzo tentativo.

### Si agisce solo sulla propria parte

Le righe della controparte sono in sola lettura, esito negativo compreso. Nella vista Venditore la riga di Sara Motta dice «Motivo: documento scaduto · se ne occupa Giulia Rossi» e non offre nessun bottone: un errore che Marco non può risolvere, mostrato con una CTA, sarebbe un vicolo cieco.

È anche la risposta al punto aperto sul promemoria, che era rimasto: il sollecito lo manda chi ha aggiunto la persona, non chiunque veda la pagina.

### Aggiungere e togliere

La sezione in fondo alla card si chiama ora **«Aggiungi una persona dalla tua parte»** e il bottone dice «Aggiungi», non «Invita»: non si invita nessuno a registrarsi. I tre campi restano nome, cognome ed email, e una riga sotto il titolo dice dove finisce il resto — «Il documento d'identità lo carichi tu, dalla schermata dei documenti. Alla persona arriva solo l'email di Yousign per la verifica».

**«Rimuovi» compare solo sulle persone che hai aggiunto tu**, come link scuro senza freccia, in fondo alla riga. Mai sul primo Venditore o sul primo Acquirente, che sono le parti della trattativa, e mai sulle righe dell'altra parte.

### Cosa cambia in F2

F2 è la schermata dove il caricamento avviene davvero, quindi è lì che la nuova responsabilità si vede: la riga di Elena porta la CTA **«Carica il documento di Elena»** e la nota che lo carica Marco. La responsabilità in testa alla pagina passa da «In attesa di Elena e Sara» a **«Tocca a entrambi»**, perché il documento di Elena è lavoro di Marco e quello di Sara è lavoro di Giulia.

Allineati anche i conteggi, che prima dicevano 1 e 2 sulla stessa schermata: ora sono due su quattro verificati in testata, nella card e nel piede.

### Distribuzione degli stati fra i frame

I cinque stati non stanno in quattro righe: sono distribuiti fra la vista Venditore e quella Acquirente, così che la coppia li mostri tutti.

| | F1 Venditore | F1 Acquirente | F2 Venditore |
|---|---|---|---|
| Marco Ferrero · Venditore | Da caricare | Verifica superata | Verifica superata |
| Elena Ferrero · Venditore | Esito negativo | Verifica in corso | Da caricare |
| Giulia Rossi · Acquirente | Verifica superata | Verifica superata | Verifica superata |
| Sara Motta · Acquirente | Verifica in corso | Email inviata | Esito negativo |

## Seconda passata del 17/09

### I pannelli Yousign contano tre passi, non cinque

Il «passaggio 2 di 5» contava la catena dell'invito, che non esiste più. Ora il contatore conta quello che i pannelli fanno davvero: **1 carica il documento · 2 controlla i dati letti · 3 esito**. L'esito negativo è la variante negativa del passo 3, non un quarto passo. Se in implementazione i tre dovessero collassare in uno solo, il contatore si toglie del tutto invece di restare a un passo su uno.

### Gli Alert esplicativi diventano bottoni info

Stessa regola di PG1 e PG2: **l'Alert resta in pagina solo per ciò che constata un fatto di questa pratica, il resto va nel popover del punto interrogativo accanto al titolo a cui si riferisce.**

- «Perché li chiediamo e chi li vede» → `?` accanto a «Documenti d'identità», in F2.
- «Comunione legale dei beni» → `?` accanto a «Chi firmerà», in F1 Venditore. Nella variante Acquirente non c'è, perché è un fatto del venditore.
- L'avviso sulla scadenza del documento di Marco resta un Alert in riga: constata una data di questa pratica, non spiega una regola.
- **L'antiriciclaggio in F3 resta com'è**, per scelta: dove vada è una domanda aperta.

I due testi stanno nella tavola `PG3 · Contenuti dei bottoni info`, accanto alla sezione, con l'intestazione del `Popover` attiva perché la tavola serve a leggerli. In pagina il popover resta senza intestazione, com'è in PG1.

### La zona di caricamento dice cosa accetta e come

Le due zone del pannello «Carica il documento» erano un segno `+` e una parola, Fronte o Retro: non dicevano né che file accettano né come si aggiunge. Ora ogni zona porta `icon/upload_file`, il nome della faccia, la riga su come aggiungere il file e il formato.

Su desktop la riga dice «Trascina qui il file o cercalo sul dispositivo», su mobile «Scegli il file dal dispositivo», perché su 440 il trascinamento non esiste. Il formato resta **jpg e png**, come deciso in Sprint 2, e scende sulla singola zona: la riga sopra non lo ripete più e dice solo che servono il fronte e il retro dello stesso documento.

Le zone passano da 160 a 175 px su desktop e da 120 a 155 su mobile; il pannello desktop da 594 a 609, il foglio mobile da 719 a 768.

**Da avere dai dev**: il peso massimo del file, che oggi non è scritto da nessuna parte e andrebbe accanto a «JPG o PNG»; e se la fotocamera è un ingresso previsto su mobile, perché in quel caso la riga diventa «Scatta una foto o scegli dal dispositivo».

**Da sistemare**: il pannello ripete a piena riga il testo «Perché li chiediamo e chi li vede», che in F2 è diventato il popover del bottone info. O esce anche da qui, o anche qui sta dietro un bottone.

### F4 porta un riepilogo delle parti

Sopra «Le vostre condizioni, in sintesi» c'è ora **«Le parti coinvolte»**: tre righe nella stessa forma etichetta/valore della card sotto — Venditori, Acquirenti, Immobile. Prima con chi stai firmando, poi che cosa avete concordato.

Non duplica «Chi ha firmato e chi manca» dentro la sezione Firma: quello dice lo stato dell'atto persona per persona, questo dice chi sono le parti e da che lato stanno.

### Sidebar e stepper allineati alle altre PG

**La sidebar non è più alta quanto la pagina**: pannello da 900 px dentro un contenitore da 948, bottone di apertura da 32 sotto, centrato. È il pattern del componente `Sidebar - Chiusa` già applicato a PG2.

**La spalla mostra solo la tappa Contratto**, come PG1 e PG2 mostrano solo Trattativa: sono cadute Profilo immobile, Pubblicazione, Visite e Trattativa con i loro separatori, e `Trust inner` scende da 642 a 362 px. I quattro sotto-passi hanno le loro icone, prese dalla pagina Icons del design system: `icon/group` per Parti da completare, `icon/badge` per Documenti d'identità, `icon/fact_check` per Consensi, `icon/draw` per Firma del preliminare.

**I colori dello stepper passano alla scala indigo**, quella già codificata in PG2. Completed: cerchio `indigo/200`, icona `indigo/800`, testo `text-onlight-medium`. Active: cerchio `indigo/950`, icona `text-fg-ondark-strong`, testo `text-onlight-strong`, con il desc «Sei qui» in `text-onlight-soft`. Initial: cerchio `indigo/050`, icona `indigo/400`, testo `text-onlight-soft`.

Il peso del testo segue la stessa regola su tutto il file: **Medium per Completed e Active, Light per Initial**. Completed e Active si distinguono per colore, non per peso.

PG3 e PG4 usavano token di sfondo generici — `bg-target-softer`, `bg-neutral-tertiary`, `bg-surface-dark-transparent` — e i cerchi venivano grigi invece che indaco. Allineati nello stesso passaggio i quattro stepper di PG4 e la tavola di lavoro sciolta di PG1, che era rimasta indietro: ora tutti e quattordici gli stepper del file usano la stessa scala.

## Tre progressi, tre forme (revisione 10/09, aggiornata il 17/09)

La pagina raccontava tre avanzamenti diversi con lo stesso grafico, e su mobile non si capiva più quale barra parlasse di cosa. La regola, valida su 1440 e su 440:

- **Percorso → stepper.** I cerchi della spalla su desktop, la barra segmentata della barra di percorso su mobile. Su una pagina ce n'è uno solo, e nient'altro usa quella forma.
- **Responsabilità e avanzamento della fase → due fatti etichettati, senza grafico.** «RESPONSABILITÀ / Tocca a te» accanto a «AVANZAMENTO / 1 persona su 4 ha il documento verificato». Un conteggio su un insieme di persone non è una posizione in una sequenza: disegnarlo come barra lo faceva leggere come un secondo percorso.
- **La catena della singola persona non esiste più.** I pallini a tre stati sono caduti insieme ai cinque passaggi: con un badge solo per riga non c'è più una sequenza da disegnare. Resta valido il principio — una sequenza dentro una riga non è il percorso della pratica — se la forma dovesse tornare.

Sulla barra di percorso mobile la revisione è più profonda: prima aveva due righe con due contatori che si contendevano la stessa barra. Ora ha tre righe — occhiello con la tappa e la sua posizione nel percorso («CONTRATTO · TAPPA 5 DI 5»), riga con il passo corrente dentro la fase e il suo contatore («Sei qui: Parti da completare» · «passo 1 di 4»), barra a quattro segmenti che disegna quei quattro passi. Un solo contatore accanto alla barra, la tappa dichiarata a parole.

Effetto collaterale voluto: **su desktop non resta nessuna barra segmentata.** Il percorso lo dice la spalla, il resto sono numeri scritti.

## Gerarchia tipografica dentro le card (revisione 11/09)

In F4 il titolo del blocco «Chi ha firmato e chi manca» aveva lo stesso peso dei nomi dei firmatari: entrambi Paragraph/Medium, quindi la lista non aveva una testa e l'etichetta si confondeva con il primo nome. Tre livelli, dove servono tutti e tre:

1. **Titolo di card → Heading 3/Semibold** su desktop, 22 su mobile. «Chi firmerà», «Documenti d'identità», «Consensi», «Le vostre condizioni, in sintesi».
2. **Etichetta di blocco dentro la card → occhiello** (Paragraph mini/Medium, maiuscolo). «CHI HA FIRMATO E CHI MANCA», come RESPONSABILITÀ e AVANZAMENTO nella card in alto.
3. **Contenuto → Paragraph/Medium.** Nomi, valori, dati.

La regola non è «l'etichetta va sempre in occhiello», è **l'etichetta deve pesare diversamente da ciò che la segue**. Sopra una lista di nomi in Paragraph/Medium ci vuole l'occhiello; sopra una griglia di campi, che hanno già le loro etichette in mini, l'occhiello sparirebbe dentro il rumore e serve invece il Paragraph/Medium — è il caso di «Dati estratti dal documento» e «I due campi che il documento non contiene» nel pannello Yousign, che restano come sono.

Su mobile, nella stessa lista, il badge «Non ha ancora firmato» è sceso sotto il nome: affiancato lasciava 150 px a un'etichetta che ne chiede 226, ed è comunque la forma già usata in tutte le altre liste di persone su 440.

## Le due famiglie di Alert (revisione 11/09)

Il box di feedback «Il contratto riporta le 8 condizioni…» era un `Alert` Complex con il titolo nascosto, e si vedeva: restava un guscio pensato per due livelli di testo con un livello solo dentro. La divisione ora è netta.

- **Complex — titolo e corpo — per ciò che spiega.** Comunione legale dei beni, perché chiediamo i documenti e chi li vede, cos'è l'antiriciclaggio, il tuo annuncio si sospende, cosa succede quando avranno firmato tutti.
- **Default — una riga sola — per ciò che constata.** La corrispondenza con la trattativa, il documento in scadenza, il contratto non ancora archiviato, l'esito negativo del caricamento.

Il colore segue il fatto, non il tono della pagina: Success per una conferma, Warning per un avviso che chiede attenzione, Danger per un errore, Info per una spiegazione.

**Correzione a quanto scritto in precedenza:** il set `Alert` ha dodici varianti — Complex, Default e Small per Success, Danger, Warning e Info. Il Danger c'era, non l'avevo trovato perché nel file UI non era ancora istanziato da nessuna parte e la ricognizione dei componenti parte dalle istanze presenti. L'avviso di esito negativo del pannello Yousign è passato da Warning a Default/Danger. Nella riga di persona di F2, invece, l'errore resta affidato al badge Danger e al motivo in chiaro: dentro una riga un alert a bordo pieno peserebbe più della riga stessa.

## Decisioni di layout — pagine di fase desktop

- **Stessa shell di PG1 e PG2**: navbar, sidebar dell'area autenticata, colonna di contenuto da 850 (frame 898 con padding 24), spalla da 322. F1, F2, F3, F4 e F5 sono la stessa pagina in cinque momenti.
- **La barra a 4 blocchi del wireframe diventa la spalla.** Parti · documenti · consensi · firma sono i sotto-passi della tappa `Contratto`; la tappa `Trattativa` si chiude in una riga. Il sotto-passo attivo cambia con lo stato e porta «Sei qui», come in PG2.
- **Il FAB «Serve aiuto?» sparisce**: il suo posto è la card «Hai dubbi?» in fondo alla spalla, con il testo adattato dalla trattativa alla firma.
- **La card di responsabilità porta due fatti etichettati**: chi deve agire e a che punto è la fase, in parole. Niente barra, per la regola qui sopra.
- **Il badge di stato della fase sta accanto al titolo**, come nel wireframe, e cambia in tutti e cinque i momenti.
- **La riga di persona è un blocco costruito a mano**, con `Avatar` a iniziali, nome, ruolo e badge di stato: lo stesso impianto in F1, F2, F3 e F5. Dal 17/09 porta un badge solo, più un'eventuale riga di motivo e azioni.
- **«(tu)» invece del badge «Tu»** del wireframe: è la forma già usata in PG2.
- **Le note di servizio del wireframe non entrano in pagina.** «Yousign è un contenitore», «il controllo è in tempo reale», il marcatore «STATO ALTERNATIVO» e il riquadro «PUNTO APERTO 20» sono annotazioni native, non testo di interfaccia.

## Decisioni di layout — mobile 440

La shell è quella di PG1 e PG2 mobile: `System Bar`, `Navbar` Device=Mobile, colonna da 408 (frame 440, padding 16, padding-bottom 96), barra sticky in fondo, card «Hai dubbi?» in coda. Il breadcrumb diventa un back link singolo, il titolo di pagina sta a 28 e i titoli di sezione a 22.

- **La barra di percorso è a tre righe** — tappa in occhiello, passo corrente con contatore, barra a quattro segmenti. È l'unico elemento segmentato della pagina. Diverge dalla barra di PG1 e PG2 mobile, dove i segmenti contano le tappe: qui contano i passi della fase, che sono quelli su cui l'utente può agire, e la tappa resta detta a parole.
- **La riga di persona si impila**: identità, badge di stato, eventuale motivo, azioni una sotto l'altra. Vale anche per la lista dei firmatari di F4, dove il badge è lungo 226 px.
- **I due consensi si impilano** in F3: privacy sopra, dichiarazione antiriciclaggio sotto.
- **Le righe del riepilogo condizioni** di F4 passano da etichetta e valore affiancati a etichetta sopra e valore sotto.
- **La CTA di firma resta dentro la card**, a piena larghezza e con il testo che va a capo: nomina due documenti e non si può accorciare. Nella barra sticky va «Firma ora», come nel footer desktop.
- **Le due uscite prima della firma** diventano bottoni a piena larghezza impilati.
- **La CTA di avanzamento di ogni stato passa nella barra sticky**, disabilitata dove lo era nel footer desktop; il testo che la accompagna («In attesa di 2 persone su 4») resta in fondo al contenuto.

## Decisioni di layout — pannelli Yousign

Il guscio desktop è quello delle modali di PG2: card da 668, fondo crema, raggio 16, padding 24, chiusura in alto a destra con `Nav tabs` Primary-square, occhiello monospaced e titolo Heading 2 centrati, corpo allineato a sinistra. Sotto lo scrim c'è **F1 vera, esportata in PNG** — una per il desktop e una per il mobile: se F1 cambia vanno rigenerate, com'è successo il 10/09 e di nuovo il 17/09.

- **Il caricamento è un pannello, non una pagina**: chi lo compila resta dentro Preparazione alla firma.
- **Le due zone di caricamento sono costruite a mano**, con bordo tratteggiato: il DS non ha un componente di upload. Su mobile si impilano.
- **Il pannello dei dati letti supera i 900 px**: su desktop il frame è alto 1219, come le modali lunghe di PG2. La griglia del wireframe è a due colonne su 760, sul desktop sta su 668 con due colonne da 304 e su mobile diventa una colonna sola, dieci campi in fila.
- **Su mobile il pannello diventa un foglio ancorato in basso**, largo quanto lo schermo, angoli superiori a 16 e nessun angolo in fondo. Quando il contenuto supera l'altezza utile il foglio si ferma a 896 px e il corpo scorre, mentre intestazione e azioni restano fissi: succede al foglio dei dati letti, dove il corpo è alto 568.
- **Lo stato di esito negativo è un frame a sé**, come gli stati alternativi delle modali di PG2, e lo dice il nome del frame. L'errore è un `Alert` Default/Danger, l'unico contenuto del pannello.


## Delta della variante Acquirente (F1)

- percorso a quattro tappe (Ricerca · Visita · Trattativa · **Contratto**), avatar di ruolo «A» su desktop, «TAPPA 4 DI 4» su mobile
- utente in navbar «Giulia / GR», «(tu)» su Giulia Rossi
- breadcrumb e back link «Le mie trattative» — ipotesi, annotata, come in PG1 e PG2
- il ruolo di Elena Ferrero perde il suffisso «coniuge in comunione legale»
- il callout della comunione legale sparisce: è un fatto del venditore
- le azioni si spostano di parte: Marco può agire su Elena, Giulia su Sara

F2, F3, F4 e F5 esistono solo in variante Venditore, come i wireframe.

## Mappatura sui componenti della libreria

| Blocco | Componente |
|---|---|
| Navbar | `Navbar` Device=Desktop / Mobile, User=User |
| Sidebar e spalla | shell dell'area autenticata, clonata da PG2 |
| Shell mobile | `System Bar` (componente locale ereditato da PG1 mobile), barra di percorso e barra sticky di PG2 |
| Breadcrumb | `Breadcrumb` + `Breadcrumb item`, tre livelli, l'ultimo Active |
| Percorso in spalla | `Stepper nav link` Type=Icon shape & text, stati Active/Initial/Completed, una sola tappa visibile |
| Avatar delle parti | `Avatar` Type=Placeholder, Size=base, iniziali MF / EF / GR / SM |
| Stati di riga e di fase | `Badge` Type=Default, Size=sm, senza icone |
| Spiegazioni | `Alert` Complex — Info per le note, Warning per la sospensione dell'annuncio |
| Constatazioni | `Alert` Default — Success per la corrispondenza, Warning per scadenza e archiviazione, Danger per l'esito negativo |
| CTA e link | `Button` Primary / Primary Disabled / Outline-dark / Link-dark Size=Small |
| Campi | `Input field` State=Initial / Filled |
| Consensi | `Checkbox input` Type=Checkbox input, Checked True/False |
| Help contestuale P7 | `Help icon (?)`, componente locale nato in PG1: cerchio indaco da 18 |
| Anteprima del documento | `icon/description` dentro un riquadro tratteggiato |
| Chiusura e occhiello di pannelli e fogli | `Nav tabs` Primary-square, stile `Cleclà/Eyebrow - monospaced/Small` |

Mappatura dei badge dal 17/09: **Brand white = Da caricare · Warning = Email inviata, in attesa, dati inseriti · Brand blue = Verifica in corso, stato della fase · Success = Verifica superata, firmato, consensi dati · Danger = Esito negativo**. Restano fuori scala «Non ha ancora firmato» in F4, che è Brand white, e i badge di fase in testata.

## Caselle di scelta: bordo tagliato e allineamento (verifica 10/09)

`Checkbox input` e `Radio item` hanno il **bordo allineato all'esterno**: una casella dichiarata 16 × 16 ne occupa davvero 18 × 18, e ogni contenitore con Clip content attivo le taglia un pixel per lato. In F3 il taglio si vedeva su tutte e otto le caselle.

Il rimedio applicato, in tre mosse:

1. **I frame di puro layout non clippano.** Su tutti i frame senza riempimento della sezione PG3 è stato tolto Clip content: 288 frame. Sono contenitori di allineamento, non ritagli.
2. **La casella sta dentro un frame «Casella»** con padding superiore, che le dà anche l'aria che serve al bordo esterno.
3. **Il padding superiore allinea la casella alla prima riga di testo**, non al blocco: vale `(altezza riga − altezza casella) / 2`, cioè 2 px con riga da 20 e casella da 16. È la differenza che si vede quando il testo va su due righe, come nella riga dell'antiriciclaggio.

Stessa correzione applicata a PG2, dove il problema esisteva ed era rimasto: nel `Foglio · Proponi una condizione — 1 di 3 – M` il Body clippa davvero, perché il foglio scorre, quindi lì il padding è sul contenitore — Foglio da 24 a 22, Body a 2, header e azioni a +2 — e la colonna di contenuto resta a 392 px senza spostare niente. Le venti opzioni della modale desktop e del foglio mobile hanno ora il radio centrato sulla prima riga con offset 1,5.

Il taglio residuo che resta in fondo ai fogli mobile è voluto: è il contenuto che scorre oltre l'altezza utile.

**Regola per il seguito:** dove c'è una casella di scelta, il contenitore non clippa oppure ha almeno 2 px di padding; e la casella si allinea alla prima riga di testo, mai al blocco. La correzione vera sta nel DS: bordo interno invece che esterno, o un padding trasparente dentro il componente.

## Discrepanze da sciogliere

- **«Verifica in corso» era stata eliminata in Sprint 2.** La revisione del Profilo immobile dichiara che il controllo Yousign è in tempo reale e ha fatto cadere il tracker a tre passi e il badge «in corso · 2-3 giorni». Qui lo stato torna, ma solo per le persone aggiunte, dove l'attesa non è la verifica in sé: è il tempo che quella persona impiega ad aprire l'email. Va confermato che le due letture convivano, altrimenti due epiche dicono cose diverse sullo stesso controllo.
- **Il lessico degli stati diverge dalla proposta di revisione.** In revisione erano «Verifica fatta» ed «Errore nella verifica»; in pagina sono «Verifica superata» ed «Esito negativo», che sono le forme registrate al §I19 del glossario e già usate in Sprint 2. Se si preferiscono le prime, va aggiornato il glossario.
- **«Email inviata» è una voce nuova**, senza corrispondenza nel glossario.
- **I consensi delle persone aggiunte.** La catena vecchia si chiudeva con «Consensi dati» per ciascuno. Se Elena e Sara non hanno un account, privacy e dichiarazione antiriciclaggio o viaggiano dentro il flusso Yousign o restano senza un posto: F3 oggi copre solo chi è in piattaforma. È la domanda aperta più grossa della revisione.
- **Nome della fase.** L'header dice «Prepara la firma», il glossario e la PG la chiamano «Preparazione alla firma» (I18). Titolo verbatim dal wireframe, breadcrumb e spalla con il nome della fase.
- **Indirizzo dell'immobile.** «Trilocale in Via Roma 12, Cuneo» in PG3, «Trilocale in Via Roma, Cuneo» in PG1 e PG2.
- **Soglia del promemoria.** Quattro giorni nel wireframe di PG2, 48 ore in PG4, nessuna attesa dichiarata qui.

## Punti aperti ereditati

- **Punto aperto 20** (F5): il venditore dipende da un pagamento che non può fare lui. Resta aperto cosa succede al contratto già firmato se l'acquirente non paga.
- **Dove va l'avviso sull'antiriciclaggio** (F3): tenuto aperto in revisione. Se spiega una regola va nel popover come gli altri, se constata un obbligo di questa pratica resta un Alert.
- **Il ruolo di ciascuno nel riepilogo delle parti** (F4): se ogni nome deve portare il proprio ruolo o basta il suffisso di Elena.
- **Conferma prima di rimuovere** (F1): se togliere una persona chiede una conferma, e cosa succede se quella persona ha già firmato o ha già superato la verifica.
- **Regime patrimoniale** (F1): se la dichiarazione si chiede prima o qui. Se qui, la riga «Comunione legale dei beni» diventa un input e non un avviso.
- **Ingresso al secondo livello dell'assistenza** (F4): se la coda o l'orario esistono, «Fatti aiutare a leggerlo» deve dichiararli.
- **Il ruolo non cambia i colori.** La collezione `Alias` ha un solo modo.
- **Quattro o cinque tappe.** Cinque nel percorso venditore, quattro nell'acquirente, sei nello stepper di «Come funziona». Su mobile si vede di più, perché l'occhiello dichiara il totale.
- **Confronto automatico fra scadenza del documento e data del rogito** (F2): da valutare con i dev.

## Limiti del DS emersi in lavorazione

- **`Checkbox input` e `Radio item` hanno il bordo allineato all'esterno.** L'ingombro reale supera di 1 px per lato quello dichiarato, e qualsiasi contenitore che clippa le taglia. Va corretto nel componente.
- **Mancano i token di progresso.** Servono per la barra di percorso mobile e, prima ancora, per la barra requisiti del Profilo immobile. Con la catena caduta il DS deve esporre almeno lo stepper segmentato; la fila di pallini di stato non serve più a PG3, ma il caso resta aperto altrove.
- **Manca un componente di upload.** Le zone di caricamento sono costruite a mano: bordo tratteggiato, icona, titolo, riga di istruzione e formato. È un pattern che tornerà ovunque si carichi un documento, a partire dall'Archivio: va promosso.
- **Manca la scala tipografica mobile.** I 28, i 22 e i 14 della barra di percorso sono valori messi a mano, fuori dagli stili, come in PG2.
- **`Alert` Complex ha un bottone incorporato** non governato da una proprietà booleana: va nascosto a mano, tranne dove serve davvero (il link alla FAQ in F3).
- **Le due varianti di Alert vogliono proprietà di testo diverse**: Complex usa `Body text`, Default usa `Text`. Scrivere sulla proprietà sbagliata non dà errore, lascia il testo di default.
- **Il Badge non manda il testo a capo**, e non esiste la taglia Small per i bottoni pieni e outline.

## Nota operativa

Confermato quanto già scritto per PG2: `getMainComponentAsync()` seguito da `createInstance()` è il modo che funziona, e i main component della libreria si risolvono anche per id una volta che il file li ha già istanziati almeno una volta.

Trappole nuove di questa lavorazione:

- **Il `Badge` cambia colore con `setProperties({Theme: …})` e testo con la chiave `Badge text#12:165`**, e le due chiamate vanno separate: passate insieme, la seconda può arrivare su un'istanza che la prima ha appena ricostruito.
- **Il bridge può perdere un'operazione.** Due volte in questa lavorazione un blocco di modifiche già confermato dal plugin è sparito: la tavola dei popover appena creata e, più avanti, i quattro bottoni info con la rimozione dei due Alert. Conviene rileggere lo stato prima di dare per fatto un passaggio, e tenere ogni intervento in una sola chiamata invece di spezzarlo.
- **Non clonare da un nodo che stai per rimuovere.** Prendendo il testo di riferimento dentro il blocco «Esito negativo · motivo e ripresa» e rimuovendo il blocco subito dopo, il clone successivo fallisce con «the node does not exist». Le sorgenti di clone si leggono prima, o si prendono da un nodo che resta.
- **La ricognizione dei componenti per istanze presenti nel file non è l'inventario della libreria.** Scandendo la pagina UI si trova solo ciò che qualcuno ha già usato: così il colore Danger degli Alert è stato dato per mancante quando invece il set ne ha dodici varianti. Per sapere cosa c'è davvero, si legge il `COMPONENT_SET` da un'istanza qualsiasi e si elencano i suoi figli.
- **Le coordinate dei figli di un frame sono relative al frame.** Impostare `child.x = frame.x` sposta il figlio fuori dal frame: i primi tre pannelli sono usciti tutti vuoti per questo. Vale anche per i figli di una sezione, quando si ricalcolano i suoi ingombri.
- **`figma.createFrame()` nasce con Clip content attivo.** Su un frame di layout è quasi sempre sbagliato, e si vede solo dove un figlio sborda di poco: le caselle di scelta, appunto.
- **Le istanze create da zero prendono la taglia di default del componente**, non quella usata altrove nel file: `icon/question_mark` nasce a 24 e in PG2 sta a 16.
- **Sostituire un testo cercandolo per contenuto colpisce anche gli omonimi.** Le sostituzioni globali vanno circoscritte al nodo giusto.
- **Cambiare lo stile di un testo, o la variante di un'istanza fra tipi diversi, significa rifare il nodo.** Si clona il nodo che porta lo stile giusto — o si istanzia la variante giusta — lo si inserisce al posto del vecchio e si rimuove quello.
- **Clonare un frame porta con sé le annotazioni.** Vanno azzerate sul clone prima di scriverne di nuove, altrimenti F2 eredita quelle di F1.
- **Il desc del `Stepper nav link` arriva con `visible = false`.** Dopo aver scritto «Sei qui» va rimesso visibile.
- **Per spostare il passo attivo nello stepper conviene clonare le istanze** già presenti (una Active, una Initial) e sostituirle, invece di cambiare la variante `State`: la variante non porta con sé gli override di colore che tengono leggibile il testo su fondo chiaro.
- **Per il foglio mobile con corpo scorrevole** basta fissare l'altezza del Body e rimetterci Clip content: intestazione e azioni, che stanno fuori dal Body, restano al loro posto.
- **I fondi dei pannelli e dei fogli sono PNG di F1**: ogni volta che F1 cambia vanno riesportati, altrimenti sotto lo scrim resta una schermata vecchia.
