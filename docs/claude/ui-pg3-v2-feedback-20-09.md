# UI · PG3 Preparazione alla firma v2, dopo il feedback del 20/09

Versione 1.6 · 25/09/2026 · file **Cleclà | UI** (`0k5JkkrVwDydzvUoRHv8ye`), pagina `🚧 UI Layouts – WIP`. Due sezioni: `PG3 · Preparazione alla firma v2 · feedback 20/09 🚧` (`4435:172035`, desktop 1440) e `PG3 · Preparazione alla firma v2 · mobile 440 🚧` (`4456:181570`), più la sezione di archivio `PG3 v2 · Fuori perimetro dopo le risposte di sviluppo 25/09 🗄` (`4501:189579`). La PG3 precedente resta in pagina finché la v2 non è approvata.

## Revisione del 25/09 — risposte dello sviluppo su firma e verifica

Le risposte del team di sviluppo sul processo di firma hanno cambiato tre cose. Il confronto completo sta in `claude/coerenza-firma-verifica-25-09.md`; qui il risultato sulle tavole.

**Youtrust al posto di Yousign.** È il nuovo nome commerciale dello stesso servizio. Quindici testi di interfaccia aggiornati, desktop e mobile.

**Stato «Firma in corso».** Lo sviluppo chiede uno stato che si sblocca solo dopo la validazione su Youtrust. Badge `Brand white` con `Type = With loader`, la grammatica già decisa il 24/09 per «qualcuno sta lavorando». Applicato alla riga di Elena in F3, e in una tavola nuova:

| Tavola nuova | Node desktop | Node mobile |
|---|---|---|
| F2d · Firma avviata, in attesa di validazione (Venditore) | `4501:189056` | `4501:189370` |

F2d è F2c dopo il clic su «Firma»: la sezione Firma perde lo stroke, il testo dice che la pagina si può chiudere e che la validazione non è immediata, una riga porta nome, ora di avvio e badge, la CTA piena diventa «Riapri la firma su Youtrust» in Outline. Passo successivo «In attesa dell'esito della firma», avanzamento «Firme: 0 su 4». Su mobile la CTA sta nella barra sticky, in Outline.

Nella riga di Elena in F3 il promemoria sparisce: con la firma già aperta non ha senso sollecitare.

**La raccolta dati per il notaio esce dalla piattaforma.** Per le persone non registrate lo sviluppo non avvia nessuna verifica: identità e dati si raccolgono dentro il processo di firma. I tre pannelli desktop e i tre fogli mobile di caricamento ed estrazione sono usciti dal perimetro, insieme alle copie delle F1 precedenti, nella sezione di archivio. Il foglio «Richiedi una modifica al contratto» resta in perimetro.

**I tempi di verifica sono riconciliati.** Nessuna procedura Youtrust è immediata, quindi cade l'assunto della verifica in tempo reale per chi è già registrato: F1a mostra Giulia in «Verifica in corso». Vanno corretti anche `claude/ui-pg3-preparazione-firma.md` e `revisione-wireframe-sprint2.md`, che dichiarano ancora il controllo in tempo reale.

## Decisioni prese con Giovane il 24/09

- Prima il desktop, poi il mobile.
- F4 diventa tre stati più una modale: contratto da aprire, contratto aperto con modifiche e benestare, firma aperta.
- Sollecito in F5: ognuno sollecita solo le persone della propria parte. Il blocco del footer sul pagamento resta solo nella vista Acquirente.
- **Badge neutri con icona di stato**, applicati a PG3 v2 e alle righe di PG2 v2 che non hanno già un'icona di stato.
- Le tavole di confronto sui badge sono state eliminate: nella sezione restano solo le schermate approvate.
- **Barra di percorso mobile su `bg-white`**, come lo stepper in spalla su desktop. Provata su PG4 v2 e poi estesa a PG2 v2 e PG3 v2 mobile.

## La tappa passa da cinque momenti a tre

Stepper di spalla a tre passi: **Persone e documenti** (`icon/badge`) · **Contratto preliminare** (`icon/fact_check`) · **Firme** (`icon/draw`). Consensi è uscita.

| Tavola | Node | Stato |
|---|---|---|
| F1a · In attesa del documento dell'altra parte (Venditore) | `4435:173358` | Giulia in verifica, «Vai al contratto» disabilitata |
| F1 · Persone e documenti (Venditore) | `4435:172036` | Elenco completo, «Vai al contratto» attiva |
| F1 · Persone e documenti (Acquirente) | `4435:172893` | Elenco completo, «Vai al contratto» attiva |
| F2a · Contratto da aprire (Venditore) | `4435:173704` | Dichiarazione da accettare prima di aprire il contratto |
| F2b · Contratto aperto, modifiche e benestare (Venditore) | `4435:174085` | Giulia ha dato il benestare, tocca a Marco |
| F2c · Firma aperta (Venditore) | `4435:174419` | Benestare di entrambi, modifiche chiuse, firma attiva |
| F2d · Firma avviata, in attesa di validazione (Venditore) | `4501:189056` | Firma aperta su Youtrust, esito da attendere |
| Modale · Richiedi una modifica (fondo F2b) | `4435:174735` | |
| F3 · Firme (Venditore) | `4435:174803` | 2 firme su 4, Elena in firma, promemoria solo a Sara |
| F3 · Firme (Acquirente) | `4435:175156` | Promemoria solo a Sara, CTA pagamento disabilitata |
| PG3 v2 · Contenuti dei bottoni info | tavola a parte | Comunione legale, Identificazione della clientela |

F1b è stata rimappata su F1a: con la raccolta dati fuori dalla piattaforma lo stato «documenti completi» coincideva con F1, e l'unico stato bloccante rimasto è l'attesa del documento dell'altra parte. L'ordine di lettura in sezione è F1a, F1 Venditore, F1 Acquirente.

## Regole applicate su tutte le tavole

- **«PASSO SUCCESSIVO» al posto di «RESPONSABILITÀ»**, come già deciso il 15/09 per la trattativa. Il valore dice chi deve fare cosa: «Tocca a te: vai al contratto», «In attesa di Giulia Rossi».
- **Niente badge di fase accanto al titolo**: lo stato lo dice lo stepper, come in PG2 v2.
- **Stroke di stato a sinistra solo sul blocco dove tocca a te**, 4 px `text-fg-warning`, lo stesso di PG2 v2.
- **Un solo bottone pieno per pagina.** Le CTA dentro le righe sono Outline o link.
- **Meno avvisi.** Resta solo l'Alert sulla scadenza del documento di Marco, che è un rischio reale. Escono il feedback di corrispondenza, il callout sull'annuncio sospeso (diventa una riga sotto la CTA di firma), la nota Info e l'avviso giallo di F5.
- **Badge neutri con icona di stato**, vedi la sezione dedicata.
- **Spalla come PG2 v2**: collegamenti «Guida al contratto preliminare» e «Riepilogo degli accordi» sotto lo stepper, card «Hai dubbi?» con «Apri la chat».

## F1 · Persone e documenti

Le vecchie F1 e F2 sono una schermata sola. Sopra le box un titolo di sezione, «Chi firma e i documenti d'identità», con il bottone info sull'identificazione della clientela ai fini dell'antiriciclaggio. Poi due box: **la tua parte** in cima, con lo stroke e in fondo il blocco «Aggiungi una persona dalla tua parte», e **l'altra parte** sotto, in sola lettura. L'ordine si ribalta nella vista Acquirente.

Dal 25/09 la schermata distingue due categorie di persone.

**Chi ha un account Cleclà** — il primo Venditore e il primo Acquirente — tiene il documento d'identità in piattaforma, con i suoi stati: Da caricare, Verifica in corso, Verificato, Esito negativo.

**Le persone aggiunte** non hanno niente da caricare qui. La riga porta un badge `In attesa` in sola lettura e la nota «L'identità di X si verifica dentro la firma, su Youtrust. Da qui non c'è niente da caricare». Sono sparite la CTA di caricamento, «Riprova la verifica» e «Invia di nuovo l'email»; resta «Rimuovi», che riguarda la persona e non il documento.

Il conteggio di parte dice «2 firmatari» invece di contare documenti, e l'avanzamento in testata dice «Elenco di chi firma: completo». Il blocco di aggiunta chiede nome, cognome ed email, che sono i tre campi che lo sviluppo dichiara necessari per avviare la procedura di firma.

## F2 · Contratto preliminare

Ordine delle sezioni, uguale nei quattro stati: contratto, sintesi, richieste di modifica, benestare, firma.

- **Dichiarazione obbligatoria** con casella: «Riconosco che l'accordo con Giulia Rossi è stato raggiunto con l'intervento mediatorio di Cleclà», con link al testo completo. Finché non è spuntata l'anteprima dice che il contratto si apre dopo e «Apri il contratto» è disabilitata.
- **Sintesi ridotta** a prezzo, data del rogito, data di consegna delle chiavi e le due condizioni sospensive attive, con i valori di T4 in PG2 v2. «Le parti coinvolte» è uscita.
- **Richieste di modifica**: gestite dal team legale, storico visibile a entrambi con richiesta, autore, data e risposta, bottone «Richiedi una modifica». In F2c e F2d il bottone sparisce e una riga dice che le modifiche sono chiuse.
- **Benestare al contratto**: una riga per parte con badge «Da dare» o «Dato il …», CTA «Dai il benestare». Solo Marco e Giulia, non le persone aggiunte.
- **Firma**: disabilitata in F2a e F2b, con la riga che spiega quando si apre. In F2c la CTA è «Firma contratto, privacy e antiriciclaggio» e il testo nomina le tre cose che si firmano insieme. In F2d la firma è già partita e la CTA diventa «Riapri la firma su Youtrust». Sotto, la nota FEQ/FEA e la riga sull'annuncio che esce dai risultati.

La modale «Richiedi una modifica» ha due campi: punto del contratto (facoltativo) e cosa vuoi modificare e perché.

## F3 · Firme

Ex F5. Stessa lista «Chi ha firmato e chi manca». Tre stati per riga: Firmato, Firma in corso, In attesa. Il promemoria compare solo su chi hai aggiunto tu e solo se non ha ancora aperto la firma; sull'altra riga una nota dice chi lo manda. Le due alert sono sostituite da una card neutra «Dopo le firme», con un testo diverso per ruolo. La CTA «Vai al pagamento registrazione» esiste solo nella vista Acquirente, disabilitata con la nota «Si attiva quando ricevi la fattura della registrazione». Date delle firme al 25/09/2026, dopo il benestare.

## Mobile 440

Sezione `4456:181570`. Una tavola per ogni pagina desktop, più il foglio delle modifiche.

| Tavola | Node | Barra sticky |
|---|---|---|
| M-1 / F1a In attesa dell'altra parte | `4456:182258` | «Vai al contratto», disabilitata |
| M-1 / F1 Venditore | `4456:181571` | «Vai al contratto» |
| M-1 / F1 Acquirente | `4456:181901` | «Vai al contratto» |
| M-2 / F2a Contratto da aprire | `4456:182578` | «Apri il contratto», disabilitata |
| M-2 / F2b Modifiche e benestare | `4456:182820` | «Dai il benestare» |
| M-2 / F2c Firma aperta | `4456:183125` | «Firma contratto, privacy e antiriciclaggio» |
| M-2 / F2d Firma avviata | `4501:189370` | «Riapri la firma su Youtrust», Outline |
| M-3 / F3 Venditore | `4456:183420` | nessuna |
| M-3 / F3 Acquirente | `4456:183681` | «Vai al pagamento registrazione», disabilitata |
| Foglio · Richiedi una modifica | `4456:184197` | fondo M-2 F2b |

Regole, prese dalla shell mobile di PG3 e da PG2 v2:

- **Barra di percorso a tre segmenti**: occhiello con la tappa, «Sei qui: …» e «passo n di 3», segmenti pieni fino al passo corrente. Sfondo `bg-white` dal 24/09, come lo stepper in spalla su desktop, per distinguerla dalle card in `bg-surface-subtle`.
- **Un solo bottone pieno, nella barra sticky.** La CTA principale sale nella barra e sparisce dalla card. In F2a e F2b il bottone di firma disabilitato è tolto dalla card, perché il testo dice già quando si apre. F3 Venditore non ha barra, come il desktop non ha footer.
- **Righe impilate**: identità, badge sotto il nome, eventuale motivo, azioni una sotto l'altra. Stesso trattamento per le righe della sintesi, per lo storico delle modifiche, per la card del passo successivo e per i campi di «Aggiungi una persona», a piena larghezza.
- **Box e sezioni** con padding 16, titolo di sezione a 22.

## Badge neutri con icona di stato (scelta del 24/09, estesa il 25/09)

Tutti i badge di stato sono Brand white. Lo stato lo porta un segno dentro il badge, costruito con proprietà già presenti nel componente `Badge` (`Show left icon`, `Left icon`, `Type`):

| Stato | Esempi | Segno |
|---|---|---|
| Fatto | Verificato, Firmato, Dato il …, Documento caricato | icona `.check` |
| Tocca a te | Da caricare, Da dare, Da completare | icona `.clock` |
| In attesa di qualcuno | In attesa | `Type = With dot` |
| Qualcuno sta lavorando | Verifica in corso, **Firma in corso** | `Type = With loader` |
| Errore | Esito negativo | resta **Danger**, senza segno |

È la grammatica delle icone dei riquadri di PG2 v2: spunta per fatto, orologio per tocca a te, cerchio per in attesa. L'errore resta colorato perché chiede un'azione, cioè il caso in cui il cliente accetta il colore.

«Email inviata» è uscita dalla scala con la revisione del 25/09: non esiste più un'email di verifica che parta dalla piattaforma.

**Dove è applicata**

- PG3 v2, desktop e mobile: tutte le tavole.
- PG2 v2, desktop e mobile, solo dove la riga non ha già un'icona di stato: «Da completare» nella card «Le tue dichiarazioni» (T1, T1b, D-0c, chiusura bloccata e le mobile corrispondenti) con l'orologio. In T5, «In corso» sui documenti d'identità diventa orologio perché è lavoro vostro, «In attesa» sulla bozza del contratto diventa puntino. I badge nella colonna destra dei riquadri degli argomenti non cambiano: hanno già l'icona di stato a sinistra del titolo, e un secondo segno la ripeterebbe.
- Le tavole «Prova» di PG2 v2 restano com'erano, come documentazione.

## Discrepanze da segnalare

- **«Youtrust»** sostituisce «Yousign» in tutto il glossario, a partire dal §I16.
- **«Firma in corso»** è una voce nuova, senza corrispondenza nel glossario.
- **«Vai al contratto»** in pagina, il cliente scrive «Vai a contratto».
- **«Benestare»** è un termine del cliente, nuovo per il glossario, come «Dato» e «Da dare» sui badge.
- **Stati del documento**: nel file i badge dicono «Verificato», il glossario (§I19) «Verifica superata». Ho lasciato la forma del file. Restano in uso solo per chi ha un account.
- **«Intervento mediatorio»** contro il copy approvato «Non siamo il terzo attore della compravendita» (§15.7), già segnalato per PG2.
- **Nome della fase**: il titolo resta «Prepara la firma», il glossario dice «Preparazione alla firma» (I18).
- **«Identificazione della clientela ai fini dell'antiriciclaggio»** va aggiornata nel glossario.

## Punti aperti

- **Come fa il sistema a sapere che l'elenco di chi firma è completo.** «Vai al contratto» si sblocca sui documenti di chi ha un account, ma nessuna schermata dichiara chi chiude l'elenco né quando.
- **Dove carica il documento l'acquirente registrato.** Per il venditore il caricamento sta nel profilo immobile; per l'acquirente non è disegnato da nessuna parte. Era un buco già prima, adesso si vede di più perché è rimasto l'unico documento in piattaforma.
- **Che cosa Youtrust restituisce durante la firma per le persone aggiunte.** Il badge in sola lettura presuppone che arrivi almeno un «in attesa / verificata»: se non arriva niente fino alla firma, quel badge va tolto.
- **La pagina di rientro dopo la firma.** Lo sviluppo non sa se Youtrust farà un redirect. F2d regge il rientro, ma non è dichiarata come destinazione.
- **Il benestare dopo una modifica.** Se una parte chiede una modifica dopo che l'altra ha dato il benestare, il benestare riparte sulla nuova versione? In pagina non è scritto.
- **Chi può chiedere una modifica e fino a quando**: oggi entrambi, fino al secondo benestare.
- **Il testo completo della dichiarazione** sull'intervento mediatorio: lo deve fornire il cliente.
- **Dove vive la guida contestuale al preliminare**: in spalla c'è il link, la destinazione non è disegnata. Su mobile il link non c'è, come non c'è la spalla.
- **La firma è in fondo a una pagina da 2284 px in F2c e F2d.** L'ordine resta uguale nei quattro stati per non spostare i blocchi. Su mobile il problema non c'è, perché la firma sta nella barra sticky.
- **Le persone aggiunte e la privacy**: ricevono l'informativa via email e firmano con il preliminare, dentro Youtrust e senza account. Lo sviluppo lo conferma per l'identità; resta da confermare per la firma.
- **Fondi PNG di PG2 v2**: le modali desktop che hanno sotto T1b, D-0c o T5 mostrano ancora i badge senza icona. Si rigenerano insieme alla prossima modifica di quelle pagine.
- Ereditati: punto aperto 20, regime patrimoniale, soglia del promemoria.

## Sezione di archivio

`PG3 v2 · Fuori perimetro dopo le risposte di sviluppo 25/09 🗄` (`4501:189579`) contiene, con le annotazioni che dicono perché:

- le copie delle tre F1 precedenti, desktop e mobile, nella versione con la raccolta dati in piattaforma;
- i tre pannelli desktop e i tre fogli mobile di caricamento ed estrazione dati, spostati e non duplicati.

Niente in questa sezione è approvato: è materiale da riprendere se il cliente rimette in discussione la scelta.

## Limiti del DS

- **Manca la scala tipografica mobile.** Titolo di pagina a 28, titoli di sezione a 22, barra di percorso e titoli dei fogli sono valori messi a mano, fuori dagli stili, come nella PG3 precedente e in PG2 v2. Da 1 a 3 testi per tavola mobile.

## Nota operativa

Tutte le tavole sono cloni delle tavole PG3 precedenti e di PG2 v2. Gate di libreria superato sul desktop: da 8 a 94 istanze per tavola, nessun fill o stroke senza variabile, nessun testo senza stile. Sul mobile vale lo stesso, con l'eccezione della scala tipografica qui sopra.

I fondi PNG dei pannelli e dei fogli spostati in archivio non sono stati rigenerati: mostrano la F1 com'era prima del 25/09. È voluto, sono materiale d'archivio.

Le tavole mobile nascono da una funzione salvata nel plugin data di `figma.root` (`pg3mobBuild`). Prende una tavola desktop e la shell mobile della PG3 precedente (`3895:41276` Venditore, `3895:41014` Acquirente), copia i blocchi del Main content e li adatta alla colonna da 408. Si richiama con `new AsyncFunction('figma','cfg', codice + 'return await build(cfg);')`. **Attenzione:** la shell di partenza ha la barra di percorso su `bg-surface-subtle`, quindi dopo ogni rigenerazione va rimesso `bg-white`.

Trappola nuova: in un clone, `findOne` per nome «Titolo» può restituire il frame che contiene il testo invece del testo. Filtrare anche per `type === 'TEXT'`.

Sul `Badge`: `Theme`, `Type`, testo e icona vanno impostati in chiamate separate, e il testo va riscritto dopo il cambio di `Type`. Cambiando uno stato che era Danger va rimesso anche `Theme = Brand white`, altrimenti il badge resta rosso. Gli id delle icone sono `.check` `484:64489` e `.clock` `484:64705`.

Scansionare le sezioni di PG2 con `findAll` e leggere `componentProperties` fa crashare la chiamata, perché il component set `card` della bacheca ha errori. Il callback deve filtrare per nome e leggere le proprietà dentro un `try`.

Passando un frame da orizzontale a verticale l'altezza resta fissa e il contenuto si sovrappone: va rimessa `HUG` su tutti i frame con figli, dal più interno verso l'esterno, e sulle istanze di `Alert`. La barra sticky è in posizione assoluta: dopo ogni cambio di altezza va riportata in fondo con `sticky.y = frame.height - sticky.height`.
