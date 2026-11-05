# Coerenza PG1–PG4 con le risposte tecniche su firma e verifica (25/09)

Confronto fra le risposte dello sviluppo sul processo di firma digitale e sulla verifica di documenti/identità e le tavole v2, file **Cleclà | UI** (`0k5JkkrVwDydzvUoRHv8ye`), pagina `🚧 UI Layouts – WIP`. Le decisioni prese con Giovane il 25/09 sono state applicate alle tavole: questo documento tiene il confronto e il registro di cosa è cambiato.

PG1 e PG2 non contengono schermate operative di firma o verifica: PG1 la cita solo nella guida statica, PG2 si ferma al benestare. PG4 tratta il pagamento della registrazione all'Agenzia delle Entrate, che le risposte non toccano. Il lavoro è tutto su PG3.

## Decisioni del 25/09

- **Youtrust è il nuovo nome commerciale di Yousign.** Un solo fornitore, non due.
- **Lo stato «in corso» della firma va aggiunto**, come chiede lo sviluppo.
- **I tempi di verifica vanno riconciliati**: nessuna procedura Youtrust è immediata, quindi cade l'assunto della verifica in tempo reale per chi è già registrato.
- **La raccolta dati per il notaio esce dalla piattaforma.** I pannelli di caricamento ed estrazione dati non sono più un passaggio Cleclà.
- Per le persone aggiunte resta in F1 un badge di stato in sola lettura, senza azioni.
- La F1 precedente va conservata come versione vecchia, non eliminata.

## Cosa è cambiato nelle tavole

**Rinomina.** Quindici testi di interfaccia passano da Yousign a Youtrust, desktop e mobile. Restano com'erano i testi nella sezione `_DELETE`.

**Stato «Firma in corso».** Badge `Brand white` con `Type = With loader`, la stessa grammatica dei badge decisa il 24/09 per «qualcuno sta lavorando». Applicato in due punti:

- F3 Firme, riga di Elena, desktop e mobile, viste Venditore e Acquirente: sottotitolo «Firma aperta il 25/09/2026 · 16:05» e nota «Elena ha aperto la firma su Youtrust: l'esito arriva quando la validazione è completa». Il promemoria sparisce da quella riga: con la firma già aperta non ha senso sollecitare.
- **Tavola nuova F2d · Firma avviata, in attesa di validazione** (desktop `4501:189056`, mobile `4501:189370`), clonata da F2c. È la schermata che vede chi ha appena premuto «Firma»: la sezione Firma perde lo stroke arancione, il testo dice che la pagina si può chiudere, una riga porta nome, ora di avvio e badge, e la CTA piena diventa «Riapri la firma su Youtrust» in Outline. Passo successivo «In attesa dell'esito della firma», avanzamento «Firme: 0 su 4».

**Raccolta dati fuori piattaforma.** I tre pannelli desktop e i tre fogli mobile di caricamento ed estrazione sono stati spostati nella sezione `PG3 v2 · Fuori perimetro dopo le risposte di sviluppo 25/09 🗄` (`4501:189579`), insieme alle copie delle F1 precedenti. Il foglio «Richiedi una modifica al contratto» resta in perimetro: non c'entra con Youtrust.

**F1 rifatta.** Le righe delle persone aggiunte perdono ogni azione sul documento e portano un badge `In attesa` in sola lettura, con la nota «L'identità di X si verifica dentro la firma, su Youtrust. Da qui non c'è niente da caricare». Sparisce la CTA di caricamento, spariscono «Riprova la verifica» e «Invia di nuovo l'email»; resta «Rimuovi», che riguarda la persona, non il documento. Il conteggio di parte passa da «1 di 2 verificati» a «2 firmatari», e l'avanzamento in testata da «2 documenti su 4 verificati» a «Elenco di chi firma: completo».

Il sottotitolo di sezione e l'helper del blocco di aggiunta sono riscritti sul nuovo modello: il documento serve solo a chi ha un account Cleclà, per gli altri bastano nome, cognome ed email, che sono i campi che lo sviluppo dichiara necessari per avviare la procedura.

**F1b diventa F1a.** Con la raccolta dati fuori, lo stato «documenti completi» coincideva con F1, quindi la tavola è stata rimappata sull'unico stato bloccante rimasto: **F1a · In attesa del documento dell'altra parte**, con Giulia in «Verifica in corso» e «Vai al contratto» disabilitata. È anche la riconciliazione sui tempi: un utente registrato passa da uno stato di attesa, non più da una verifica istantanea. L'ordine di lettura in sezione è ora F1a, F1 Venditore, F1 Acquirente.

**Popover.** «Identificazione della clientela ai fini dell'antiriciclaggio» e «Comunione legale dei beni» sono riscritti: dicono dove finisce il documento e chi lo vede nel nuovo modello.

## Punti che restano aperti

- **Come fa il sistema a sapere che l'elenco di chi firma è completo.** Oggi «Vai al contratto» si sblocca sui documenti dei registrati, ma nessuna schermata dichiara chi chiude l'elenco né quando. Serve una risposta prima di disegnare altro.
- **Dove carica il documento l'acquirente registrato.** Per il venditore il caricamento sta nel profilo immobile; per l'acquirente non è disegnato da nessuna parte. Era un buco già prima, adesso si vede di più perché è rimasto l'unico documento in piattaforma.
- **Che cosa Youtrust restituisce durante la firma per le persone aggiunte.** Il badge in sola lettura presuppone che arrivi almeno un «in attesa / verificata»: se non arriva niente fino alla firma, quel badge va tolto e la riga resta senza stato.
- **La pagina di rientro dopo la firma.** Lo sviluppo non sa se Youtrust farà un redirect; F2d è la schermata che regge il rientro, ma non è dichiarata come destinazione.
- **Glossario.** «Youtrust» sostituisce «Yousign» al §I16 e ovunque compaia. «Firma in corso» è una voce nuova. Restano aperte le voci già segnalate per PG3 v2: «Verificato» contro «Verifica superata» (§I19), «benestare», «intervento mediatorio».

## Documenti di progetto da correggere

`claude/ui-pg3-preparazione-firma.md` e `revisione-wireframe-sprint2.md` dichiarano che il controllo Yousign è in tempo reale per chi è già registrato. Non è più vero: vanno corretti insieme al glossario.
