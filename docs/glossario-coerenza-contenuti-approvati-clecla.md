# Glossario e pattern di coerenza: contenuti approvati Cleclà

Versione 1.1 · 10/09/2026 · aggiunte le decisioni su fee e importi, corrette le voci che citavano layer nascosti. Il dettaglio frame per frame sta nel file «incongruenze-contenuti-approvati-clecla.xlsx».
File Figma: **Cleclà | UI** (`0k5JkkrVwDydzvUoRHv8ye`)

## Come si legge

Il documento raccoglie le formulazioni già usate nei contenuti approvati di Cleclà, organizzate per concetto. Serve a scrivere contenuti nuovi senza riformulare in modo diverso cose già dette.

Ogni formulazione porta una sigla di fonte:

| Sigla | Fonte | Peso |
|---|---|---|
| **[A]** | Frame approvati elencati al §1 | Copy approvato. Riportato alla lettera, refusi compresi (elencati al §17). |
| **[PK]** | Project knowledge: wireframe, UI e note di decisione di Sprint 2 e 3 | Formulazione di lavoro, non copy approvato. Vale come riferimento finché content design non la chiude. |
| **[B]** | Manuale d'identità Cleclà v1.0 (stessi contenuti della Brand Strategy «NIDO» del 26/08/2025) | Regola di brand. |

Regola d'uso. Se un concetto ha una sola forma [A], si usa quella. Se ne ha più d'una, la voce rimanda a un'incongruenza del §16 e non va scelta una versione finché non è risolta. Se esiste solo in [PK], si usa segnalandolo. Le sigle /D e /M indicano la versione desktop e mobile dello stesso frame.

Metodo. Testi estratti in sola lettura dal file Figma il 10/09/2026, 16 sezioni, 4.953 nodi di testo, deduplicati per sezione. Esclusi i frame «SEO», che contengono ancora il template con lorem ipsum. Le sezioni portano nel nome il marcatore «in lavorazione» mentre le pagine portano quello di approvazione: su indicazione ricevuta, il contenuto delle sezioni linkate è trattato come approvato.

---

## 1. Frame analizzati

| Sigla | Pagina · sezione | Nodo | Cosa contiene | Ruolo |
|---|---|---|---|---|
| NAV | Navigazione · Step 2 | 1716:1163 | Homepage venditore /D e /M con menu e footer. I testi divergono da HV5 (vedi I46) | Venditore, pubblico |
| BAC | Bacheca V+A · Step 2 | 2129:670 | Bacheca vuota venditore e acquirente, menu account, aggiunta ruolo | Entrambi, autenticato |
| HV5 | Homepage - Vendi casa · Step 5 | 2053:7059 | Homepage venditore, calcolatori budget, tempistiche e documentazione | Venditore, pubblico |
| HV6 | Homepage - Vendi casa · Step 6 | 2547:3262 | Varianti del risultato budget e dell'elenco documenti | Venditore, pubblico |
| CC4 | Compra casa · Step 4 | 2053:10560 | Homepage acquirente, calcolatori budget e tempistiche | Acquirente, pubblico |
| EMC | Email - calcolatori · Step 4 | 2325:2895 | Email con i risultati dei tre calcolatori, varianti V e A | Entrambi |
| CF5 | Come funziona · Step 5 (modifiche PDF cliente 25-8) | 3429:4573 | Come funziona venditore e acquirente, confronto con agenzia, «Perché Cleclà» | Entrambi, pubblico |
| CFP | Come funziona · Passaggi | 2255:3380 | Contenuto dei sei passi: «Cosa fai tu» e «Cosa fa Cleclà» | Entrambi, pubblico |
| REG | Registrazione · Step 4 | 2053:14963 | Form di registrazione, email già usata, conferma email, link scaduto | Entrambi |
| EMR | Email - conferma mail · Step 3 | 2053:15982 | Email di verifica dell'indirizzo | Entrambi |
| LOG | Login · Step 3 | 2053:16042 | Accesso, errore credenziali, recupero e reimpostazione password | Entrambi |
| EMP | Email - recupero password · Step 3 | 2053:17331 | Email di reimpostazione password | Entrambi |
| CHI | Chi siamo · Step 4 (modifiche PDF cliente 25-8) | 3442:4181 | Idea, mission, vision, team, valori, «Cosa non è Cleclà» | Entrambi, pubblico |
| CON | Contatti · Step 3 | 2190:10693 | Contatti e rimando alle FAQ | Entrambi, pubblico |
| PRO | Profilo · Step 3 | 2547:19885 | Il mio account, dati per la firma, eliminazione del profilo | Entrambi, autenticato |
| IMP | Impostazioni profilo · Step 1 | 2112:24863 | Preferenze di notifica web e mail | Entrambi, autenticato (voci orientate al venditore) |

---

## 2. Voce e tono applicati

### 2.1 Come ci si rivolge all'utente

Sempre del tu, verbi alla seconda persona singolare. Cleclà parla di sé quasi sempre alla prima plurale: «Pensiamo noi a pubblicare il tuo annuncio su Cleclà e sui principali portali immobiliari.» (HV5), «Verifichiamo l'identità delle persone interessate a vedere l'immobile prima di fissare gli appuntamenti.» (HV5), «Monitoriamo le scadenze delle condizioni sospensive e ti avvisiamo per tempo» (CFP). [A]

Passa alla terza persona («Cleclà») in tre casi: nei confronti con l'agenzia («Cleclà verifica l'identità di venditore e acquirente prima dell'incontro.», CF5/D), in alcune descrizioni di fase («Cleclà valida e pubblica l'annuncio online.», NAV/M; «Cleclà ti affianca durante tutta la trattativa», CC4) e in una parte della colonna «COSA FA Cleclà» di CFP. La convivenza delle due voci nella stessa colonna è l'incongruenza I28.

La controparte si nomina per ruolo: «l'acquirente», «il venditore», «il proprietario» («contatta direttamente il proprietario della casa che ti interessa», CC4). Nei passaggi sulle commissioni compare «chi vende / chi compra» («1% per chi vende, 2% per chi compra», CF5). La forma «parte venditrice» compare una sola volta, nel titolo «Documenti che dovrai fornire tu come parte venditrice» (HV6). [A]

Il genere di default è il maschile («Se non sei stato tu a fare questa richiesta», EMP). L'unica forma doppia è nelle opzioni di stato civile: «Celibe/Nubile», «Sposato/a» (HV5). [A]

### 2.2 Titoli

Tre famiglie, tutte in sentence case. [A]

La domanda che l'utente si farebbe apre le sezioni informative e i calcolatori: «In quanto tempo posso vendere casa?», «Quanto risparmio con Cleclà?», «Quali documenti servono per vendere casa?», «Quanto costa vendere casa con Cleclà?», «In quanto tempo posso acquistare casa?», «È arrivato il momento di vendere casa?», «Hai qualche dubbio o domanda?», «Stai cercando casa?», «Vuoi eliminare il tuo profilo?», «Ti va di dirci perché?».

L'affermazione breve chiusa dal punto regge hero e promesse: «Vendi casa, a modo tuo.», «Acquista casa da un privato, senza sorprese.», «Trova la casa giusta. Senza rischi, senza sorprese.», «Quando clic fa casa.», «Vendere casa è un passo importante. Noi lo rendiamo sicuro.», «Costi chiari. Paghi solo quando concludi.», «Digitale, ma mai da solo.».

L'imperativo o lo stato raggiunto serve account ed email: «Crea il tuo profilo», «Controlla la tua email», «Scegli una nuova password», «Password aggiornata», «Link non valido o scaduto», «Verifica la tua email», «Reimposta la tua password».

Unica eccezione al sentence case: «La nostra Mission», «La nostra Vision» (CHI).

### 2.3 Occhielli

Convivono due stili. Minuscolo discorsivo: «gestisci la tua vendita» (HV5), «cerchi casa?» (CC4), «il nostro approccio», «founder» (CHI). Maiuscolo: «INIZIAMO DA QUI?», «PERCHÉ CLECLÀ», «COSA FAI TU», «COSA FA Cleclà», «COSTI», «VALUTAZIONE», «LA TUA NUOVA CASA TI ASPETTA», «NESSUN ANNUNCIO PRESENTE». Se il maiuscolo è uno stile tipografico applicato, la differenza sparisce in sviluppo; se è digitato, va uniformato (I32). [A]

### 2.4 Formule ricorrenti di rassicurazione

Sono il lessico che tiene insieme autonomia e supporto. Vanno riusate così come sono. [A]

| Formula | Dove |
|---|---|
| «senza sorprese» | CC4 hero, HV5 blocco documenti, HV5 «Contratti chiari, senza sorprese», CF5/M acquirente |
| «Niente sorprese, niente clausole nascoste.» | CF5/M |
| «Nessuna sorpresa, nessuna clausola nascosta, nessun costo che compare all'improvviso.» | CHI, valore Trasparenza |
| «Le decisioni finali restano sempre le tue.» / «Le decisioni finali sono sempre le tue.» | HV5 hero / HV5 Budget-1, HV6, NAV (I30) |
| «Scegli tu se procedere in autonomia o chiedere aiuto.» | CF5/M |
| «Non siamo qui per decidere al posto tuo, ma per darti gli strumenti giusti per farlo con sicurezza.» | CHI, valore Autonomia |
| «Quando hai bisogno, ci siamo.» | CF5/M, CHI/M |
| «Ti bastano pochi minuti.» | HV5, CF5, NAV (CTA finale) |
| «Saprai sempre a che punto sei e qual è il passo successivo.» | CF5/M |
| «Sai sempre dove sei e cosa ti aspetta» | CF5/D |
| «Ti guidiamo nella raccolta di tutto quello che serve, passo dopo passo.» | HV5 |

«Senza sorprese» compare almeno cinque volte nelle pagine pubbliche. Nota di scrittura: aggiungerne altre occorrenze come riempitivo la consuma; va tenuta per i punti in cui c'è davvero un costo o un passaggio da anticipare.

### 2.5 CTA

Il pattern applicato è verbo più oggetto. [A]

| Contesto | Label approvate |
|---|---|
| Calcolatori | «Calcola risparmio», «Calcola tempistiche», «Calcola documentazione», «Calcola ora», «Calcola», «Avanti», «Indietro», «Vedi dettaglio», «Chiudi dettaglio», «Modifica», «Ricomincia», «Ricevi il dettaglio per email» |
| Ingresso | «Registrati gratis», «Registrati (gratuito)», «Registrati», «Accedi», «Inizia a creare l'annuncio», «Inizia la ricerca», «Cerca casa», «Vai agli annunci», «Voglio vendere», «Voglio comprare», «Scopri come funziona Cleclà» |
| Email | «Conferma il tuo indirizzo email», «Reimposta la password», «Inserisci il tuo immobile», «Cerca immobili in vendita» |
| Account | «Accedi con questo account», «Recupera password», «Usa un'email diversa», «Invia di nuovo», «Torna alla registrazione», «Invia link di reset», «Richiedi un nuovo link», «Torna al login», «Apri l'app email», «Prova con un altra email», «Aggiorna password», «Accedi ora», «Modifica password», «Elimina account», «Elimina profilo», «Conferma eliminazione», «Annulla», «Logout» |
| Supporto | «Contattaci», «Vai alle FAQ» |
| Bacheca | «Inserisci immobile», «Aggiungi ruolo acquirente», «Trova tecnici» |

Restano label generiche, che l'interaction model (P5) sconsiglia: «Comincia subito», «Inizia subito», «Inizia da qui», «Torna indietro». Le coppie equivalenti con label diverse sono in I31.

### 2.6 Email transazionali

Struttura applicata a EMR ed EMP, da replicare. [A]

1. Titolo imperativo: «Verifica la tua email», «Reimposta la tua password».
2. Saluto: «Ciao [Nome],».
3. Corpo breve che dice perché si riceve l'email e cosa fare: «Ci siamo quasi. Manca solo un passo per attivare il tuo account su Cleclà e iniziare a gestire la compravendita della tua casa. Clicca il pulsante qui sotto per confermare il tuo indirizzo email.»
4. CTA.
5. Link di riserva: «Se il pulsante non funziona, incolla questo link nel browser:».
6. Validità e uscita di sicurezza: «Questo link è valido per 24 ore. Se non hai creato un account su Cleclà, ignora questa email.» / «Questo link è valido per 24 ore. Se non sei stato tu a fare questa richiesta, ignora questa email. Il tuo account è al sicuro.»
7. Footer legale: «Questa comunicazione ha carattere esclusivamente informativo e riguarda il servizio richiesto. Non costituisce comunicazione commerciale o promozionale.»

Le email dei calcolatori (EMC) aprono con «Abbiamo elaborato il calcolo in base ai dati che hai inserito.» seguito da «Qui trovi il dettaglio completo delle spese stimate.» / «Qui trovi le tempistiche di vendita del tuo immobile.» / «Qui trovi le tempistiche di acquisto del tuo immobile.», e chiudono con «Crea il tuo profilo e fai il primo passo» (V) o «Pronto per iniziare?» (A).

### 2.7 Errori ed esiti negativi

Pattern applicato nei flussi account: il titolo dice cosa è successo, il corpo dice perché e qual è la regola, le CTA danno una o più uscite. Nessun tono di rimprovero. [A]

| Situazione | Testo | Uscite |
|---|---|---|
| Email già registrata (REG) | «Questo indirizzo è già associato a un account Cleclà.» | «Accedi con questo account» · «Recupera password» · «Usa un'email diversa» |
| Credenziali errate (LOG) | «Email o password non corrette. Riprova o reimposta la password.» | «Reimposta la password» |
| Email non trovata nel recupero (LOG) | «Nessun account associato a questo indirizzo email.» | |
| Link di reset scaduto (LOG) | «Link non valido o scaduto» · «Il link che hai usato non è più valido. I link di reset scadono dopo 24 ore o dopo il primo utilizzo.» · «Se hai già reimpostato la password con questo link, accedi normalmente.» | «Richiedi un nuovo link» · «Torna al login» |
| Link di conferma scaduto (REG) | «Il link è scaduto» | «Invia di nuovo» · «Torna alla registrazione» |
| Password non coincidenti (REG) | «Le password devono coincidere» | |
| Attesa prima di un nuovo invio (LOG) | «Puoi richiederne uno nuovo tra 58s» | |

Regola della password, forma breve: «Almeno 8 caratteri, una lettera maiuscola, un numero e un carattere speciale.» Forma estesa: «La password deve contenere: Almeno 8 caratteri · Almeno una lettera maiuscola (A–Z) · Almeno un numero (0–9) · Almeno un carattere speciale (!, @, #...)». Placeholder: «Minimo 8 caratteri». [A]

In [PK] lo stesso pattern è fissato per gli esiti negativi di verifica (Yousign): motivo specifico, azione «Ripeti il caricamento» o «Ripeti la verifica», e la dichiarazione che nessun dato è stato salvato. L'interaction model (E4) chiede che il messaggio sia «specifico, empatico e indichi come uscirne».

### 2.8 Conferme e stati vuoti

[A]

- Aggiunta ruolo: «Profilo acquirente aggiunto. Potrai passare da un ruolo all'altro dalla tua bacheca.»
- Profilo eliminato: «Grazie!» · «Da adesso il tuo profilo non è più attivo.» · «L'eliminazione sarà confermata nei prossimi 30 giorni. Potrai riaprire un profilo con la stessa email in qualsiasi momento.»
- Password: «Password aggiornata» · «La tua password è stata reimpostata con successo. Ora puoi accedere con le nuove credenziali.»
- Bacheca venditore vuota: «NESSUN ANNUNCIO PRESENTE» · «Non hai ancora inserito un immobile, comincia subito!» (/M) · «Non hai ancora inserito un immobile, inizia adesso!» (/D)
- Bacheca acquirente vuota: «NESSUN ANNUNCIO SALVATO» · «Dai un'occhiata agli ultimi immobili inseriti»
- Saluto di bacheca: «Ciao Mario, ecco dove eravamo rimasti»

### 2.9 Note, asterischi e disclaimer

Il pattern è l'asterisco sull'etichetta della voce e la spiegazione in coda al blocco. Doppio asterisco per la seconda nota. [A]

- «*Queste spese valgono sia nel caso in cui si utilizzi Cleclà, sia nel caso in cui ci si affidi a un'agenzia immobiliare tradizionale.» (HV6)
- «*Calcolato su una provvigione media del 3% + IVA per parte, prassi comune delle agenzie tradizionali. Il range di mercato è 3–6% + IVA.» (EMC)
- «**Stime indicative. I prezzi reali variano in base al professionista scelto.» (EMC V)
- «**Stime indicative. I costi variano in base alla tipologia di acquisto. Spese notarili escluse.» (EMC A)
- «*Stime indicative» (HV6)
- «*Nessun costo da sostenere in questa fase» (CF5)
- «*Se non hai già un tecnico di riferimento, potrai trovarlo tramite la funzione "Trova tecnico" direttamente dal tuo profilo.» (EMC)

Due disclaimer sono ancora segnaposto: «*XXX Disclaimer tempistiche indipendenti da CLeclà» (HV5) e «*Disclaimer relativo al fatto che queste cose le paghi indipendentemente da Cleclà, anche con agenzia tradizionale» (HV5).

### 2.10 Regole di brand da tenere a fianco

[B] Il tono ha cinque tratti, ciascuno con il suo limite: diretto ma mai invadente, empatico ma non ridondante, autorevole ma non supponente, positivo ma realistico, puntuale ma non pedante. Il manuale chiede di non mettere le persone «in condizioni di stress».

Le tre coppie di esempi del manuale sono il riferimento più concreto sul tono nei momenti delicati.

| Da fare | Da evitare |
|---|---|
| «Il primo passo è creare la scheda del tuo immobile. Ti chiederemo solo le informazioni essenziali per conoscere il tuo immobile e proporti i tecnici più adatti. Niente stress: ti guideremo passo, passo.» | «Crea il tuo profilo e inserisci tutti i dati richiesti. È fondamentale attivarsi subito per non perdere tempo e vendere rapidamente.» |
| «La Due Diligence serve a verificare che tutto sia in regola prima di iniziare a vendere. Ti aiuta a evitare imprevisti, tutelando te e chi acquista.» | «La Due Diligence è obbligatoria e deve essere completata prima della pubblicazione. Se non la fai, potresti incorrere in problemi legali o bloccare l'intera trattativa.» |
| «Quando ricevi una richiesta di visita, sarai sempre informato in anticipo. Potrai scegliere giorno e orario con facilità, in base alla tua disponibilità. Nessuna sorpresa, solo appuntamenti gestiti con serenità.» | «Una volta che l'acquirente mostra interesse, ti verranno proposti i giorni e gli orari delle visite. Cerca di essere disponibile, altrimenti potresti perdere l'opportunità.» |

La regola che se ne ricava: si spiega a cosa serve una cosa invece di dire che è obbligatoria, e non si minaccia una perdita per ottenere un'azione. [PK] L'interaction model aggiunge: niente «Devi…» e «Non puoi…», il copilota suggerisce.

Nota: «Due Diligence» compare solo nel manuale. Nei frame approvati il concetto è espresso come verifica della regolarità (§6.3).

---

## 3. Il percorso e i nomi delle fasi

Le fasi non hanno ancora un nome unico: la tabella riporta tutte le versioni in uso. Vedi I10.

| Dove | Fasi |
|---|---|
| HV5 /D, stepper venditore [A] | Profilo · Annuncio · Visite · Trattativa · Contratto · Rogito |
| BAC e CF5/M, stepper [A] | Profilo · Annuncio · Visita · Trattativa · Contratto · Verso il rogito |
| CFP, titoli dei passi venditore [A] | 01 Crea il profilo · 02 Crea il tuo annuncio · 03 Gestisci le visite · 04 Gestisci la trattativa · 05 Firma il contratto preliminare · 06 Verso il rogito |
| CF5/M, titolo del passo 1 [A] | «Crea il profilo e inizia la vendita» |
| NAV/M, stepper [A] | Crea il profilo · Pubblica l'annuncio · (visite, trattativa, contratto descritti senza titolo proprio) |
| CC4, stepper acquirente [A] | Ricerca · Visita · Trattativa · Contratto preliminare · Rogito |
| CF5/M acquirente [A] | «Inizia la ricerca e crea il profilo» · «Prenota una visita» · … · «Ci siamo quasi! Arriva al rogito con tutto quello che ti serve.» |
| Interaction model [PK] | Venditore: Creazione profilo immobile · Pubblicazione annuncio · Visita · Trattativa · Contratto. Acquirente: Ricerca · Visita · Trattativa · Contratto |
| Spalla UI trattativa [PK] | Sotto-passi di Trattativa: Guida alla trattativa · Proposta delle condizioni · Risposte e controproposte · Accordo raggiunto |

Descrizioni di fase approvate, venditore (HV5/D): [A]

- Profilo: «Registrati gratis. Se decidi di vendere, prenota il servizio fotografico. Nel frattempo, noi prepariamo una valutazione puntuale e tu decidi il prezzo.»
- Annuncio: «Pensiamo noi a pubblicare il tuo annuncio su Cleclà e sui principali portali immobiliari.»
- Visite: «Gestisci in autonomia le disponibilità e fissa le visite tramite il tuo calendario. Le persone sono sempre verificate da noi.»
- Trattativa: «Tratti direttamente con l'acquirente, ma puoi contare sul nostro supporto fino al raggiungimento di un accordo chiaro e tutelante.»
- Contratto: «Stipuliamo il contratto sulla base degli accordi presi. Firmi digitalmente, come l'acquirente, in modo semplice e sicuro.»
- Rogito: «Il notaio riceverà tutta la documentazione necessaria per predisporre l'atto e, se dovesse servire un'integrazione, saremo al tuo fianco fino al completamento della pratica.»

Descrizioni di fase approvate, acquirente (CC4/D): [A]

- Ricerca: «Sfoglia gli annunci e salva i tuoi immobili preferiti.»
- Visita: «Prenota la visita direttamente dalla scheda dell'immobile.»
- Trattativa: «Negozia con il venditore. Cleclà ti affianca durante tutta la trattativa, fino al raggiungimento di un accordo sicuro e tutelante.»
- Contratto preliminare: «Stipuliamo il compromesso sulla base degli accordi raggiunti. Tu e il venditore firmate digitalmente, comodamente da casa, in modo semplice e sicuro.»
- Rogito: stesso testo del venditore.

Sottotitolo del blocco percorso: «Ti accompagnamo in tutte le fasi» seguito da una delle varianti di I11. [A]

---

## 4. Costi, compensi e pagamenti

### 4.1 Come si chiama il compenso di Cleclà

**Decisione del 10/09/2026.** Il nome non è unico: si sceglie per contesto, seguendo il termine già usato nel componente. Se un componente usa «fee», nei testi nuovi dello stesso componente resta «fee». Va segnalato solo un componente che ne usa due.

Nei frame approvati convivono cinque nomi per la stessa cosa: «fee» («Fee Cleclà»), «commissione» («Con Cleclà paghi l'1%» in coda a «commissione media di un'agenzia tradizionale»; «Commissioni definite fin dall'inizio»), «provvigione» («Quietanza di pagamento della provvigione», «Fattura Cleclà per provvigione»), «costi di mediazione» («Costi di mediazione Cleclà») e «spesa di mediazione» («La tua spesa di mediazione con Cleclà»). Nessuno è stato scelto come canonico. Vedi I05. [A]

### 4.2 Percentuali, minimi e formule di calcolo

**Regole decise il 10/09/2026.** Venditore 1% con minimo 2.000 € (sotto i 200.000 € di prezzo la fee è 2.000 €). Acquirente 2% con minimo 4.000 €. Agenzia tradizionale, come termine di confronto, 4% con minimo 5.000 € (sotto i 125.000 € la spesa agenzia è 5.000 €). Resta da decidere se le percentuali si dichiarano più IVA. Gli importi d'esempio mostrati nei frame si allineano in staging quando il calcolatore funziona.

Formulazioni presenti nei frame:

[A]

- Venditore: «Con Cleclà paghi l'1%.» · «1 % del prezzo di vendita (min. €2.000)» · «1 % del prezzo di vendita (costo minimo €2.000)» · «1% del prezzo di vendita (min. €2.000)». Esistono anche occorrenze all'1,5% (I01).
- Acquirente: «Con Cleclà paghi il 2%.» (CC4). Il dettaglio dello stesso calcolatore riporta «1,5% del prezzo di vendita (min. €2.000)» (I02).
- Entrambi: «La commissione, 1% per chi vende, 2% per chi compra, si attiva solo una volta che il preliminare è andato a buon fine.» (CF5/M) · «Commissioni definite fin dall'inizio: 1% per chi vende e 2% per chi compra. Le paghi solo quando il contratto preliminare è concluso.» (CF5/D)
- Base di confronto: «Il risparmio è calcolato rispetto alla commissione media di un'agenzia tradizionale, che in Italia è tra il 3% e il 6% del prezzo di vendita.»

[PK] Venditore 1% confermato il 18/08; acquirente 2% con minimo 4.000 € più IVA nei wireframe dell'annuncio, minimo che non compare nelle pagine pubbliche.

### 4.3 Quando si paga

Le formule approvate sono sei e dicono due cose diverse: «se concludi» e «dopo il preliminare». Vedi I06. [A]

- «Paghi solo se vendi.» (EMC V) · «La pubblicazione dell'annuncio è gratuita: paghi solo se vendi.» (NAV/M)
- «Paghi solo se acquisti.» (EMC A)
- «Costi chiari. Paghi solo quando concludi.» (CF5/D)
- «Paghi solo dopo il preliminare» (CF5/M, titolo)
- «si attiva solo una volta che il preliminare è andato a buon fine» (CF5/M)
- «Le paghi solo quando il contratto preliminare è concluso.» (CF5/D)

[PK] Formula ponte fissata il 19/08 in attesa di decisione: «si paga solo se la compravendita si conclude».

### 4.4 Cosa è incluso

[A]

- «La pubblicazione dell'annuncio è gratuita.» · «Penseremo noi alla pubblicazione gratuita dell'annuncio.»
- Voci «Incluso» nel dettaglio budget: «Servizio fotografico professionale» · «Pubblicazione annuncio» · «Supporto nella raccolta documenti» (EMC V)
- CF5: «Servizio fotografico · € 200 · INCLUSO» e «Pubblicazione annuncio · € 0» (I07)

[PK] Lo studio di vendibilità «lo fa Cleclà, incluso, non si commissiona». Trova tecnico: «incluso, senza commissioni».

### 4.5 Costi che non dipendono da Cleclà

Sei etichette per lo stesso concetto (I09). [A]

«Costi non dipendenti da Cleclà» · «Costi tecnici obbligatori (non Cleclà)» · «Costi obbligatori indipendenti dalla mediazione» · «Costi dei tecnici correlati all'immobile» · «Spese obbligatorie per legge (non dipendenti da Cleclà)» · «Per la produzione dei documenti».

Voci e importi: «APE (Attestato Prestazione Energetica) · circa € 200 · Obbligatorio per legge» · «Relazione tecnica · circa € 500 · Nel caso in cui non sia disponibile la RRE» (EMC V) · «Registrazione contratto preliminare · circa €270» (CC4, EMC A; I08).

### 4.6 Il confronto con l'agenzia tradizionale

Termine stabile: «agenzia tradizionale» («agenzia immobiliare tradizionale» nelle forme estese). «Agenzia fisica» compare solo nella testimonianza. [A]

Formule del confronto: «Spesa con le agenzie tradizionali*» · «Quanto spenderesti di mediazione con un'agenzia tradizionale» · «Il tuo risparmio con Cleclà» · «4 % del prezzo di vendita (costo minimo €5.000)» (HV6; I04).

Nella tabella «Un nuovo modo di vendere e comprare casa» di CF5 la colonna agenzia usa un registro critico e fattuale: «Non sempre verificata», «Devi cercare i professionisti in autonomia o affidarti all'agenzia», «Valutazione rapida su pochi dati. Spesso ottimistica per acquisire il mandato», «Mediata dall'agenzia e spesso poco trasparente», «Firma cartacea, appuntamenti fisici, documenti da stampare e conservare», «Richiede appuntamenti, spostamenti e il coordinamento della disponibilità di tutte le parti.».

---

## 5. Identità, verifica e sicurezza

[A]

- «Sai sempre chi entra in casa tua» · «Verifichiamo l'identità delle persone interessate a vedere l'immobile prima di fissare gli appuntamenti.» (HV5)
- «Verifica identità» · «Verifichiamo l'identità di venditore e acquirente prima di ogni contatto» (CF5/M)
- «L'identità di venditore e acquirente viene verificata prima della visita.» (CF5/D)
- «Più sicurezza, fin dalla prima visita.» · «Cleclà verifica l'identità di venditore e acquirente prima dell'incontro.» (CF5/D)
- «Le persone sono sempre verificate da noi.» (HV5)
- Venditore: «Verifichi la tua identità in pochi minuti» (CFP). Acquirente: «Verifica la tua identità per confermare la prenotazione» (CFP)
- «Persone verificate, contratti chiari, documenti in ordine: ogni aspetto è curato nei minimi dettagli.» (HV5)

Il momento della verifica è detto in quattro modi diversi (I17).

[PK] Badge pubblici: «Utente verificato» (profilo), «Documentazione verificata» (annuncio, dichiara il controllo senza esporre il contenuto). Stati della verifica documento: «Da caricare», «Verifica superata», «Esito negativo».

---

## 6. Documenti, regolarità e tecnici

### 6.1 Chi fornisce cosa

Il calcolatore documentazione divide i documenti per responsabile. Le quattro etichette sono il modello da riusare ogni volta che si dice «chi se ne occupa». [A]

«Documenti che dovrai fornire tu» (in HV6 approvato: «Documenti che dovrai fornire tu come parte venditrice») · «Documenti che ti fornirà Cleclà» · «Documenti che dovrà fornirti un tecnico» · «Documenti che dovrà fornirti l'amministratore condominiale».

[PK] Stesso principio nelle etichette di responsabilità della trattativa: «Tocca a te», «In attesa di [Nome]», «Ci pensiamo noi», «Tocca a entrambi».

### 6.2 Elenco documenti approvato

Versione di HV6 ed EMC, con le differenze della versione in HV5 (I22). Le condizioni sono riportate come compaiono sotto la voce. [A]

| Chi | Documento | Condizione | Variante HV5 |
|---|---|---|---|
| Tu | Documento d'identità in corso di validità (di tutti i proprietari) | | |
| Tu | Libretto caldaia (se presente) | | «(se autonomo)» |
| Tu | Quietanza di pagamento della provvigione | | «ricevuta del bonifico di pagamento della provvigione» |
| Tu | Certificato di stato libero | | |
| Tu | Estratto per riassunto atto di matrimonio in carta libera | | |
| Tu | Certificato di stato civile | | |
| Tu | Auto-dichiarazione del regime patrimoniale | | |
| Tu | Certificato di morte del de cuius uso conservatoria | | «del proprietario deceduto» |
| Tu | Dichiarazione di successione | | |
| Tu | Atto di provenienza anteriore alla successione | | |
| Tu | Atto di provenienza | | |
| Tu | Permesso di soggiorno in corso di validità | | |
| Tu | CDU (Certificato di Destinazione Urbanistica) | | |
| Tu | RRE (Relazione di Regolarità Edilizia) | «Se la possiedi già» | |
| Tu | Certificato di conformità impianto idraulico | «Solo nel caso in cui l'immobile sia stato costruito dopo il 2008» | |
| Tu | Certificato di conformità impianto elettrico | | |
| Tu | Certificato di conformità impianto riscaldamento e climatizzazione | | «…impianto elettrico, idraulico, riscaldamento/raffrescamento» |
| Tu | Contratto di locazione | | |
| Cleclà | Visura catastale dell'immobile | | |
| Cleclà | Visura ipotecaria dell'immobile | | |
| Cleclà | Planimetria catastale dell'immobile | | |
| Cleclà | Foglio/mappa catastale | | |
| Cleclà | Contratto Preliminare di Compravendita | | |
| Cleclà | Ricevuta di registrazione del Contratto preliminare presso l'Agenzia delle Entrate | | |
| Cleclà | Ricevuta Agenzia delle Entrate di avvenuto pagamento delle imposte disse e marche da bollo | | «delle imposte e marche da bollo» |
| Cleclà | Fattura Cleclà per provvigione | | |
| Cleclà | Scheda strumenti urbanistici (gismaster) | | assente |
| Cleclà | Scheda cartografica (gismaster) | | assente |
| Cleclà | Norme tecniche di attuazione | | assente |
| Tecnico | APE (Attestato di Prestazione Energetica) | | |
| Tecnico | Titoli edilizi (provenienti dalla Relazione Tecnica Cleclà) | | «Titoli edilizi e relativi elaborati grafici che rappresentano lo stato attuale regolare dell'immobile» |
| Tecnico | Presentazione pratica sanatoria | | |
| Tecnico | Relazione Tecnica | «Se non possiedi già la RRE (Relazione di Regolarità Edilizia)» | |
| Tecnico | Relazione di calcolo della plusvalenza immobiliare | «Solo nel caso in cui l'immobile ha beneficiato di interventi agevolati fiscalmente (es. Superbonus 110%, Ecobonus, ecc.) negli ultimi 10 anni?» (I23) | |
| Amministratore | Liberatoria delle spese condominiali | | |
| Amministratore | Regolamento condominiale | | |
| Amministratore | Ultimo preventivo/consuntivo | | |
| Amministratore | Ultimi 2 verbali dell'assemblea | | «…dell'assemblea condominiale» |

Contatori dichiarati: 18 · 11 · 5 · 4.

Domande del calcolatore documentazione, nell'ordine (HV5): «Qual è il tuo stato civile?» · «In quale regime dei beni?» · «Hai la cittadinanza italiana?» · «L'immobile proviene da una successione (eredità)?» · «Nella vendita sono inclusi anche terreni?» · «Hai già una RRE (Relazione di Regolarità Edilizia) dell'immobile?» · «L'immobile si trova in un condominio?» · «L'immobile è stato costruito dopo il 2008?» · «L'immobile ha beneficiato di interventi agevolati fiscalmente (es. Superbonus 110%, Ecobonus, ecc.) negli ultimi 10 anni?» · «Hai acquistato questo immobile meno di 5anni fa e dalla data di acquisto fino a oggi, è stato il tuo domicilio principale per più della metà del tempo?» · «L'immobile è attualmente locato?». Opzioni di regime: «Separazione dei beni», «Comunione dei beni». [A]

[PK] Regole sui documenti: «Un documento caricato non si elimina, si sostituisce»; i moduli di recesso dal preliminare e di comunicazione e riconoscimento di inadempimento non compaiono in elenco perché si generano quando l'evento si verifica; la planimetria è l'unico documento dell'archivio che diventa pubblico nell'annuncio (da validare).

### 6.3 Regolarità e APE

[A]

- Definizione dell'APE, da riusare identica: «L'APE (Attestato di Prestazione Energetica) è il documento obbligatorio che certifica quanto consuma energeticamente un immobile, assegnandogli una classe dalla A4 (la più efficiente) alla G (la meno efficiente).» Titolo dell'help: «Cos'è l'APE?»
- «Un tecnico qualificato verifica la regolarità urbanistica e catastale dell'immobile.» (CF5/D) · «Un tecnico qualificato verifica urbanistica, catasto e conformità edilizia prima di procedere» (CF5/M)
- «Tecnici qualificati» · «Hai a disposizione un team di professionisti che eseguono relazioni tecniche e le verifiche necessarie.» (HV5)
- «La burocrazia ti spaventa? Nessun problema: ti indichiamo i documenti necessari e ti affianchiamo nella gestione, per arrivare al rogito senza sorprese.» (HV5 /D, versione aggiornata)
- «Nessun documento dimenticato» · «Ti guidiamo nella raccolta di tutto quello che serve, passo dopo passo. Sai tutto ciò che ti serve con ampio anticipo.»

Scelta osservata fra le versioni: NAV conteneva «L'immobile è in regola. Lo certifichiamo noi»; in HV5 la card è sostituita da «Tecnici qualificati», e nessun frame approvato dice che Cleclà «certifica» la regolarità. È una differenza di contenuto, non una decisione documentata: va confermata (I46).

### 6.4 Studio di vendibilità e prezzo

[A]

- «Studio di vendibilità su oltre 100 parametri: il prezzo consigliato è basato sul mercato reale» (CF5/M)
- «Uno studio basato su oltre 100 parametri ti aiuta a definire un prezzo consapevole e coerente con il mercato.» (CF5/D)
- «noi prepariamo una valutazione puntuale e tu decidi il prezzo» (HV5) · «Effettua una valutazione di mercato dell'immobile» (CFP)
- «Definisci il prezzo di vendita con il supporto di Cleclà.» · «Definisci il prezzo di partenza»

Tre nomi per lo stesso servizio (I25).

[PK] Decisione del 18/08: il prezzo lo decide sempre il venditore. Formulazioni di wireframe: «Il prezzo lo decidi tu: questo è provvisorio» e «Non è un prezzo imposto: è un consiglio professionale su cui ragionare».

### 6.5 Trova tecnico

Il nome della funzione compare in tre forme: «Trova tecnici» (menu bacheca, CTA), «Trova Tecnico» (CF5, tabella di confronto), «"Trova tecnico"» (EMC). Vedi I26. Descrizioni approvate: «Hai a disposizione un gruppo di professionisti e tecnici che puoi consultare in ogni momento» (CF5/M) · «Accedi a una rete di professionisti, mantenendo piena libertà di scelta.» (CF5/D) · «Ti mettiamo in contatto con tecnici partner se manca ancora qualche documento» (CFP). [A]

### 6.6 Cosa diventa pubblico

Nessun frame approvato ne parla. [PK] Si marcano i campi pubblici e il silenzio vale privato. Banner di wireframe: «Quasi niente di quello che scrivi qui diventa pubblico». Sull'annuncio non si espone quali documenti mancano.

---

## 7. Trattativa

### 7.1 Nei frame approvati

La trattativa compare solo come fase del percorso e nel contenuto dei passi di CFP. [A]

- Titolo del passo: «Gestisci la trattativa» · sottotitolo: «Quando arriva una proposta, sei tu a decidere. Puoi contare sempre sul nostro supporto»
- Cosa fai tu: «Ricevi la proposta e fai le tue valutazioni» · «Se accetti prosegui verso il preliminare» · «Se rifiuti, la trattativa rimane aperta»
- Cosa fa Cleclà: «Siamo a supporto per chiarire ogni dubbio» · «Ti affianchiamo nella valutazione della proposta» · «Teniamo traccia di tutto: gli accordi sono sempre chiari e visibili da entrambi le parti»
- CF5: «La trattativa avviene tra privati, ma sempre con il nostro supporto e la nostra guida.» · «In ogni momento puoi vedere a che punto è la trattativa, quali documenti mancano e quali passi restano da fare.»
- CHI: «Non siamo il terzo attore della compravendita. Siamo un servizio a supporto di chi vende e chi compra casa, per questo ogni persona è sempre tutelata al massimo.»
- IMP, notifica: «Trattative» · «Quando un acquirente mostra interesse a trattare o invia un'offerta»
- FAQ citata: «Come funziona la trattativa con Cleclà?»

Verbi usati per la trattativa: «Tratti direttamente con l'acquirente» (HV5), «Negozia con il venditore» (CC4), «Negozia direttamente con l'acquirente» (NAV), «Gestirai direttamente con l'acquirente la trattativa» (NAV/M).

### 7.2 Nella project knowledge

Il modello di PG2 è diverso da quello descritto in CFP (I15). [PK] Termini e label di lavoro:

- Oggetto condiviso: «documento di puntuazione», fatto di «condizioni» raggruppate in quattro gruppi: «Prezzo e pagamento», «Tempistiche e disponibilità», «Clausole sospensive», «Dichiarazioni che entrano nel preliminare» (l'ultimo è un'ipotesi).
- Azioni: «Proponi una condizione», «Rispondi», «Accetta», «Fai una controproposta», «Rifiuta» (solo sul prezzo, con motivazione facoltativa; sulle date non c'è rifiuto secco), «Invia la proposta a [Nome]», «Modifica una condizione», «Annulla la trattativa», «Vai alla trattativa in corso», «Proponi questa data», «Scarica il documento (PDF)», «Apri il documento», «Leggi prima la guida».
- Stati delle condizioni: accettata, in attesa di risposta, non ancora affrontata, non applicabile, già concordata, rifiutata, accordo da confermare, inserita dal sistema.
- Responsabilità: «Tocca a te», «In attesa di Marco Ferrero», «Tocca a entrambi».
- Traguardo: «Accordo raggiunto».
- Controparte in parallelo: «Il proprietario può trattare anche con altri» (vista acquirente).
- Mobili: «I mobili si trattano fuori da qui».

---

## 8. Contratto preliminare, firma e registrazione

### 8.1 Nei frame approvati

[A]

- Definizione: «Il compromesso è il momento in cui l'accordo diventa ufficiale.» (CFP, titolo del passo 05 «Firma il contratto preliminare»)
- «Generiamo il contratto preliminare sulla base degli accordi raggiunti in trattativa»
- «Ogni clausola è spiegata in linguaggio semplice, direttamente nel documento»
- «Registriamo il contratto all'Agenzia delle Entrate entro i termini di legge»
- «Il preliminare e gli altri atti sono redatti per tutelare venditore e acquirente, nel rispetto delle norme vigenti.» (HV5, card «Contratti chiari, senza sorprese»)
- Cosa fai tu: «Leggi il contratto generato dalla piattaforma» · «Firmi digitalmente con SPID o OTP» · «Ricevi conferma via email»
- Firma: «Firma elettronica qualificata (FEQ), con lo stesso valore legale della firma autografa.» (CF5/D) · «Firma digitale qualificata (FEQ): ha lo stesso valore legale dell'autografa, riconosciuta dall'Agenzia delle Entrate» (CF5/M). Vedi I16.

Il documento si chiama in quattro modi: «Contratto», «Contratto preliminare», «preliminare», «compromesso» (I12). Nell'elenco documenti: «Contratto Preliminare di Compravendita».

### 8.2 Nella project knowledge

[PK]

- Firma via Yousign: FEQ per il contratto, FEA per gli altri documenti, dichiarati nel testo della CTA di firma.
- «Il tuo annuncio si sospende» (callout venditore prima della firma).
- «Qualcosa non torna: chiedi una modifica» e «Fatti aiutare a leggerlo» come uscite prima della firma.
- Registrazione: 320 € più IVA, 390,40 € totali; CTA «Paga 390,40 € e registra il contratto»; «Se il contratto non viene registrato entro i 30 giorni si annulla»; terzo passo dello stepper «lo facciamo noi»; banner «Il preliminare è registrato».
- Distinzione dichiarata fra ricevuta di pagamento e ricevuta di registrazione.

---

## 9. Condizioni sospensive

### 9.1 Nei frame approvati

Termine usato: «condizioni sospensive», sempre al plurale e sempre in minuscolo. Tre occorrenze, tutte in CFP: [A]

- «Monitoriamo le scadenze: data rogito, consegna immobile, eventuali condizioni sospensive ancora aperte» (venditore, passo 06)
- «Comunichi l'avveramento delle condizioni sospensive (es. mutuo ottenuto)» (acquirente, passo rogito)
- «Monitoriamo le scadenze delle condizioni sospensive e ti avvisiamo per tempo» (acquirente)

«Avveramento» è il termine scelto per il verificarsi della condizione. Nessun frame approvato spiega che cos'è una condizione sospensiva.

### 9.2 Nella project knowledge

[PK] Le cinque condizioni previste, nella dicitura della Scheda Tecnica 2.0: mutuo · regolarità edilizia e conformità catastale · vendita dell'immobile del promissario acquirente · soluzione abitativa per il venditore · diritto di prelazione. Esempio usato nella modale: «Prelazione agraria». Il gruppo si chiama «Clausole sospensive» nella modale e «Condizioni sospensive» nella pagina trattativa (I43). La guida alla trattativa ha un callout dedicato alla condizione sospensiva il cui testo non è riportato nella project knowledge.

«Clausola sospensiva» al singolare non compare in nessuna fonte.

---

## 10. Recesso, inadempimento, inefficacia e penalità

### 10.1 Nei frame approvati

Due sole occorrenze. [A]

- EMC, email budget venditore, in coda al dettaglio costi: «Sono previsti costi aggiuntivi in caso di recesso anticipato dall'incarico o inadempimento contrattuale. Consulta i Termini e Condizioni per i dettagli completi.»
- IMP, preferenze di notifica: «Recesso, inadempienza o altro» · «Flussi che bloccano temporaneamente il contratto»

«Inadempimento» e «inadempienza» sono entrambi in uso (I36). «Inefficacia» e «caparra confirmatoria» non compaiono in nessun frame approvato né nella project knowledge.

### 10.2 Nella project knowledge

[PK] La guida alla trattativa ha una sezione «Se qualcosa va storto» con tre strade (recesso, inadempimento, inefficacia) e un callout sul fatto che, se la compravendita salta senza colpa, il costo è zero. La project knowledge descrive la sezione ma non ne riporta i testi: le formulazioni esatte vanno lette nei frame UI della guida (sezione «PG1 · Guida alla trattativa», generata dai wireframe 3559:9128 e 3559:9387), che non sono tra quelli approvati.

---

## 11. Rogito e notaio

[A]

- «Il notaio riceverà tutta la documentazione necessaria per predisporre l'atto e, se dovesse servire un'integrazione, saremo al tuo fianco fino al completamento della pratica.» (HV5, CC4)
- «Dalla scelta del notaio alla preparazione dei documenti, ti accompagniamo fino alla firma finale.» (NAV, HV5/M, CF5/D acquirente)
- «Ti aiutiamo ad arrivare al rogito con tutto quello che ti serve» (CFP, passo 06)
- Cosa fai tu (venditore): «Completa la documentazione richiesta dal notaio» · «Prepara l'immobile per la consegna» · «Fissi, in accordo con l'acquirente, la data del rogito»
- Cosa fai tu (acquirente): «Scegli il notaio, se non hai contatti puoi selezionare unon dei nostri partner» · «Comunichi l'avveramento delle condizioni sospensive (es. mutuo ottenuto)» · «Prepari la documentazione in vista dell'appuntamento»
- Cosa fa Cleclà: «Ti forniamo una checklist con tutti i documenti che il notaio ti chiederà» · «Ti accompagniamo passo, passo verso la firma del contratto»
- Esito dei calcolatori: «Tempo stimato per arrivare al rogito notarile»
- CHI: «Il nostro lavoro inizia con la pubblicazione dell'annuncio e finisce solo dopo il rogito.»

Il momento finale si chiama «rogito», «rogito notarile», «atto notarile», «firma finale», «firma dal notaio» (I13).

---

## 12. Account, profilo e impostazioni

### 12.1 Registrazione

[A] Titolo «Crea il tuo profilo». Campi: «Nome», «Cognome», «Indirizzo email», «Tipologia di profilo» (Venditore / Acquirente), «Password», «Ripeti password». Placeholder: «es. Mario», «es. Rossi», «es. mario.rossi@email.it». Nota sul ruolo: «Puoi selezionare entrambe le tipologie. Puoi aggiungere o cambiare ruolo in qualsiasi momento dal tuo profilo». Consensi, uno per riga: «Ho letto e accetto la Privacy Policy» · «Ho letto e accetto i Termini e Condizioni» · «Ho letto e accetto le clausole di cui all'Allegato 2 dei T&C». Rimando: «Hai già un account?» · «Accedi».

Conferma: «Controlla la tua email» · «Abbiamo inviato un link di conferma a mario.rossi@email.it. Clicca sul link per attivare il tuo profilo e iniziare.» · «Il link scade tra 24 ore» · «Email sbagliata?».

### 12.2 Accesso

[A] «È un piacere rivederti» · «Inserisci le credenziali e accedi al profilo» · «Ricordami» · «Password dimenticata?» · «Non hai ancora un account?». Recupero: «Inserisci l'email del tuo account. Ti invieremo un link per reimpostare la password.» · «Controlla la tua casella email» · «Abbiamo inviato un link a mario.rossi@email.it.». Nuova password: «Scegli una nuova password» · «La password deve soddisfare i requisiti indicati qui sotto.» · «Nuova password» · «Conferma password».

### 12.3 Il mio account

[A] Titolo «Il mio account», sottotitolo «Gestisci i tuoi dati personali e le impostazioni di profilo.». Blocchi: «Informazioni personali» · «Dati per la firma del contratto» con la nota «Questi dati ti verranno chiesti solo al rogito. Per adesso, puoi procedere senza.» (I18) · «Dati anagrafici» · «Residenza» · «Domicilio» con opzione «Il domicilio è uguale all'indirizzo di residenza» · «Telefono (cellulare)» · «Documento d'Identità» (campi «Tipo di documento», «Data di rilascio», «Data di scadenza», «Stato», «Allegati»; stati mostrati «SCADUTO» e «Verificato», I19). Nota ruolo: «Puoi aggiungere o cambiare ruolo in qualsiasi momento dalla tua bacheca.» (I33)

La formula «Per adesso, puoi procedere senza.» è il modello approvato per chiedere un dato che serve più avanti senza bloccare l'utente.

### 12.4 Eliminazione del profilo

Azione distruttiva, trattata con conferma, motivo facoltativo e conseguenze dichiarate. [A]

- Titolo: «Vuoi eliminare il tuo profilo?»
- Conseguenza (/M): «Cliccando su Elimina profilo, l'account verrà disattivato. I tuoi dati saranno archiviati solo per obbligo di legge e non saranno utilizzati per nessun altro scopo.»
- Conseguenza (/D): «Cliccando su Conferma eliminazione il profilo verrà disattivato definitivamente. I tuoi dati verranno archiviati per obbligo di legge, ma non saranno utilizzati per nessun altro scopo.»
- Motivo: «Ti va di dirci perché?» · «Cerchiamo di migliorare ogni giorno, per questo ogni risposta è importante.» · «Voglio cancellare il profilo perché*». Opzioni: «Ho già venduto/comprato casa tramite Cleclà» · «Ho venduto/comprato casa tramite un altro servizio» · «Pochi annunci/richieste nella mia zona» · «Non mi fido di una piattaforma online per vendere/comprare casa» · «Il servizio non è intuitivo» · «Non voglio più vendere/comprare» · «Altro:»
- Esito: vedi §2.8.

Le versioni /D e /M non coincidono (I34).

### 12.5 Notifiche

[A] Titolo «Impostazioni profilo», sottotitolo «Gestisci ruoli, notifiche e sicurezza del tuo account.». Canali: «Web», «Mail».

| Voce | Descrizione |
|---|---|
| Profilo immobile | Aggiornamenti e richieste di informazione |
| Pubblicazione annuncio | Aggiornamenti sulla pubblicazione del tuo annuncio sui diversi portali |
| Gestione visita | Quando qualcuno prenota una visita e feedback di visita avvenuta |
| Trattative | Quando un acquirente mostra interesse a trattare o invia un'offerta |
| Contratto | Modifiche a contratti e documenti |
| Recesso, inadempienza o altro | Flussi che bloccano temporaneamente il contratto |
| Finalizzazione | Documenti, aggiornamenti, notaio, next step |
| Newsletter Cleclà | Guide, news e consigli |

### 12.6 Menu e navigazione autenticata

[A] Sidebar: «Bacheca», «Profilo immobile», «Documentazione», «Calendario visite», «Trattative», «Gestione contratti», «Pagamenti», «Trova tecnici», «Il tuo calendario». Menu utente: «La tua bacheca», «Account», «Notifiche», «Impostazioni», «Esci dal tuo account». Selettore di ruolo: «Vendere» / «Comprare». Breadcrumb: «Home /».

---

## 13. Supporto e contatti

[A]

- CON: «I nostri contatti» · «Hai una domanda sul processo di vendita o di acquisto? Scrivici o chiamaci: ti risponderemo entro 48 ore dall'invio della richiesta.» · «info@clecla.it» · «Per informazioni generali sul servizio» · «Via Vignolo 117» · «12010 Cervasca (CN), Italia»
- Rimando alle FAQ: «Hai dubbi?» · «Leggi le risposte alle domande più frequenti.» · «Hai altre domande?» · «Hai una domanda specifica?» · «Vai alle FAQ»
- Domande FAQ già titolate: «Quanto costa Cleclà?» · «È sicuro vendere o comprare casa senza un'agenzia tradizionale?» · «Come funziona la trattativa con Cleclà?» · «È sicuro comprare casa con Cleclà?» · «Quanto costa comprare casa con Cleclà?» · «Gli annunci sono controllati?»
- Card di contatto: «Hai qualche dubbio o domanda?» · «Contattaci»
- «Digitale, ma mai da solo.» · «Ti guidiamo nella definizione del prezzo, nella gestione delle visite e durante la trattativa. Per gli aspetti tecnici puoi affidarti ai professionisti presenti sulla piattaforma oppure procedere in autonomia.» (CF5/D)
- «La tecnologia semplifica ogni passaggio, ma dietro Cleclà c'è un team competente. Mantieni il controllo della compravendita, con il supporto che ti serve fino al rogito.» (CHI/D)

[PK] Nelle pagine autenticate il supporto si rimanda alla chat, non all'email. Card di spalla «Hai dubbi?», floating button «Serve aiuto?». Help puntuale «?» con domanda e risposta sotto i 280 caratteri e link «Vai alla FAQ completa».

---

## 14. Calcolatori: etichette e risultati

### 14.1 Budget

[A] Input: «Inserisci il valore indicativo dell'immobile» (placeholder «es. 250.000 €»), «Quali documenti hai già a disposizione?» (APE, Relazione Tecnica). Riepilogo: «I tuoi dati», «Valore immobile», «Documenti disponibili». Risultato: «La tua spesa con Cleclà» / «La tua spesa di mediazione con Cleclà» · «Spesa con le agenzie tradizionali*» / «Quanto spenderesti di mediazione con un'agenzia tradizionale» · «Il tuo risparmio con Cleclà» · «Costi non dipendenti da Cleclà». Dettaglio: «Nel dettaglio:», «Costi Cleclà».

### 14.2 Tempistiche venditore

[A] Domande: «Hai poca esperienza nella vendita di immobili?» (Sì, ho poca esperienza / No, ho già esperienza) · «Vuoi vendere velocemente?» (Sì / Non ho fretta) · «L'immobile è regolare a livello urbanistico?» · «Pensi che l'acquirente acquisterà con mutuo?» (Sì / No / Non lo so). Riepilogo: «Prima vendita», «Tempistiche desiderate», «Immobile in regola», «Mutuo». Esiti a doppio scenario: «Se l'acquirente acquista senza mutuo» / «Se l'acquirente acquista con mutuo».

Spiegazioni dei fattori (HV5): «La mancanza di esperienza porta spesso a ponderare molto le decisioni e quindi a prenderle con più calma.» · «La volontà di vendere velocemente porterà a prendere decisioni in merito all'annuncio che porteranno l'immobile ad essere più appetibile sul mercato.» · «Dover produrre una sanatoria per mettere in regola l'immobile allunga i tempi di vendita di circa 3 mesi.» · «La richiesta del mutuo da parte dell'acquirente potrebbe allungare di circa 2 mesi le tempistiche di vendita.» Le versioni email differiscono (I39).

### 14.3 Tempistiche acquirente

[A] Domande: «Hai esperienza nella compravendita immobiliare?» · «È il primo immobile che compri?» · «Chiederai un mutuo?» · «L'immobile è regolare?». Esiti a doppio scenario: «Se l'immobile è regolare» / «Se l'immobile non è regolare». Spiegazioni: «Se è la prima volta che ti trovi ad acquistare una casa è possibile che tu abbia bisogno di più tempo per decidere.» · «La volontà o la necessità di trovare un immobile velocemente porterà a prendere decisioni più velocemente.» · «La richiesta del mutuo potrebbe allungare leggermente le tempistiche di acquisto.» · «La regolarità di un immobile è un aspetto centrale che condiziona le tempistiche di acquisto.»

---

## 15. Decisioni editoriali sui punti delicati

Per ogni tema: cosa mostrano i frame approvati, cosa è stato deciso nella project knowledge, cosa resta aperto.

### 15.1 Penalità e costi aggiuntivi

[A] Si nominano una sola volta, nell'email del calcolatore budget venditore, in una frase informativa in coda al dettaglio costi, con rimando ai Termini e Condizioni: «Sono previsti costi aggiuntivi in caso di recesso anticipato dall'incarico o inadempimento contrattuale.» La parola «penale» non compare in nessun frame approvato: si usa «costi aggiuntivi». Nelle pagine pubbliche i costi aggiuntivi non sono citati.

[PK] Principio fissato nella revisione di Sprint 2: un «decidi tu» che nasconde una penale non è un «decidi tu», quindi la fee va dichiarata vicino alla libertà di scelta sul prezzo. Punto aperto 20: i T&C non prevedono sanzioni per la registrazione tardiva; le penali riguardano il rapporto venditore-Cleclà. Importo della fee dopo un anno ancora a placeholder.

Aperto: se «costi aggiuntivi» debba comparire anche sulle pagine pubbliche dei costi, visto il principio dell'interaction model «costi, condizioni, limiti rivelati solo a fine flusso» (anti-pattern E3).

### 15.2 «Paghi solo se»

[A] La formula di rassicurazione sul pagamento è sempre condizionale e sempre legata al risultato. Le sei varianti sono al §4.3; dicono cose diverse sul momento (I06).

### 15.3 Silenzio della controparte

[A] Nessun frame approvato ne parla.

[PK] Nella guida alla trattativa c'è un callout «perché i silenzi costano»; nella variante acquirente il testo è «Il venditore potrebbe avere altre proposte sul tavolo.». In pagina trattativa: avviso di silenzio prolungato con l'azione «Manda un promemoria». Soglia: 4 giorni nel wireframe, contro le 48 ore del sollecito di pagamento (I44).

Tensione da verificare: il callout acquirente fa leva sulla possibilità di perdere l'immobile, lo stesso meccanismo che il manuale indica fra i «da evitare» («Cerca di essere disponibile, altrimenti potresti perdere l'opportunità»).

### 15.4 Esito negativo

[A] Nei flussi account: fatto, motivo e regola, uscita (§2.7). Nessuna colpa attribuita all'utente: «Il link che hai usato non è più valido.» Quando l'utente potrebbe aver già risolto da solo, lo si dice: «Se hai già reimpostato la password con questo link, accedi normalmente.»

[PK] Verifica documento: motivo specifico, «Ripeti il caricamento», «nessun dato salvato». Rifiuto di una condizione: motivazione facoltativa. Mancata registrazione entro 30 giorni: il contratto «si annulla», detto già nella schermata di pagamento e non solo alla scadenza.

### 15.5 Azioni irreversibili

[A] Unica azione irreversibile nei frame approvati: l'eliminazione del profilo. Conferma esplicita, conseguenze sui dati dichiarate, via di ritorno («Potrai riaprire un profilo con la stessa email in qualsiasi momento.»).

[PK] Prima della firma del preliminare: avviso di irreversibilità, conseguenza sull'annuncio dichiarata («Il tuo annuncio si sospende»), uscita visibile prima dell'azione («Qualcosa non torna: chiedi una modifica»).

### 15.6 Dati chiesti in anticipo

[A] «Questi dati ti verranno chiesti solo al rogito. Per adesso, puoi procedere senza.» Il dato si mostra, si dice quando servirà e non si blocca il percorso.

### 15.7 Il ruolo di Cleclà

[A] Cleclà si descrive come supporto, mai come parte: «Non siamo il terzo attore della compravendita.» · «Non vogliamo sostituirci alle persone, vogliamo supportarle.» · «Cosa non è Cleclà: Un'agenzia immobiliare tradizionale · Una piattaforma di annunci · Un algoritmo che ti lascia solo». Nessun frame dice che Cleclà media, decide o garantisce l'esito.

### 15.8 Il confronto con le agenzie

[A] Tono fattuale e a volte critico sulla colonna agenzia («Spesso ottimistica per acquisire il mandato», «spesso poco trasparente»). Il dato di confronto sulle commissioni è sempre accompagnato dalla base di calcolo o dal range di mercato. Il riferimento al fatto che siano «le agenzie a presentarsi» alle visite, presente in NAV, non compare nella versione HV5.

---

## 16. Incongruenze da verificare

Stesso concetto detto o chiamato in modo diverso. Nessuna versione è stata scelta. Le voci con [PK] mettono a confronto un frame approvato con la project knowledge.

### Costi

**I01 · Percentuale del venditore.** *Deciso: 1%, minimo 2.000 €. Da correggere le occorrenze all'1,5%.* 1%: HV5 («Con Cleclà paghi l'1%.»), HV5 dettaglio («1 % del prezzo di vendita (min. €2.000)»), HV6 («1 % del prezzo di vendita (costo minimo €2.000)»), EMC, CF5. 1,5%: NAV/M («Con Cleclà paghi l'1,5%.»), HV6 secondo frame di dettaglio («1,5% del prezzo di vendita (min. €2.000)»). [PK] 1% confermato il 18/08.

**I02 · Percentuale e minimo dell'acquirente.** *Deciso: 2%, minimo 4.000 €.* Anche l'email budget acquirente riporta la fee del venditore («1% del prezzo di vendita (min. €2.000)»). CC4 dichiara «Con Cleclà paghi il 2%.» e mostra € 4.800 su 240.000 €; il dettaglio dello stesso calcolatore riporta «Fee Cleclà · € 4.400 · 1,5% del prezzo di vendita (min. €2.000)». EMC A mostra sia € 4.800 sia € 4.400. [PK] Minimo acquirente 4.000 € più IVA, assente dai frame approvati.

**I03 · Importi d'esempio su 240.000 €.** *Si allineano in staging, nessuna correzione in Figma. Valori attesi con le regole: venditore 2.400 €, acquirente 4.800 €, agenzia 9.600 €, risparmio del venditore 7.200 €.* Spesa Cleclà del venditore: € 3.300 (HV5 risultato, HV6 «Costi di mediazione Cleclà»), € 2.400 (HV6 risultato, EMC). Spesa con agenzia: € 7.200 (HV6) e €7.100 (EMC). Risparmio: «~ € 6.800» (HV5).

**I04 · Base di confronto con l'agenzia.** *Deciso: 4%, minimo 5.000 €. Da allineare le note «3% + IVA per parte»; da verificare se il range di mercato 3-6% resta nella nota dei calcolatori.* «tra il 3% e il 6% del prezzo di vendita» (hero calcolatori), «4 % del prezzo di vendita (costo minimo €5.000)» (HV6 dettaglio), «provvigione media del 3% + IVA per parte» con «range di mercato è 3–6% + IVA» (EMC).

**I05 · Nome del compenso di Cleclà.** *Deciso: scelta per contesto (§4.1).* Restano da uniformare due componenti che usano due termini: il risultato del calcolatore budget («La tua spesa di mediazione con Cleclà» e «La tua spesa con Cleclà») e il suo dettaglio («Fee Cleclà» e «Costi di mediazione Cleclà»).

**I06 · Momento del pagamento.** «se vendi / se acquisti / quando concludi» contro «dopo il preliminare / quando il contratto preliminare è concluso» (§4.3). [PK] Formula ponte «si paga solo se la compravendita si conclude»; l'elenco documenti prevede una «Quietanza di pagamento della provvigione» senza dire quando.

**I07 · Servizio fotografico.** Prezzo: «€ 200 · INCLUSO» (CF5) contro «€ 0 · Incluso» (HV6, EMC). Nome: «servizio fotografico» (HV5, CF5), «set fotografico» (NAV, HV5/M). Chi agisce: «prenota il servizio fotografico» (HV5), «Attiva il servizio fotografico professionale nella tua zona» (CFP, colonna Cleclà). [PK] È il team Cleclà che contatta il venditore per organizzarlo.

**I08 · Registrazione del preliminare.** «Registrazione contratto preliminare · circa €270» con etichetta «Incluso» accanto (CC4) e «circa €270**» fra le «Spese obbligatorie per legge» (EMC A). [PK] 320 € più IVA, 390,40 € totali, pagati dall'acquirente.

**I09 · Etichetta dei costi non Cleclà.** Sei varianti (§4.5).

### Percorso e fasi

**I10 · Nomi e numero delle fasi.** Sei fasi con «Rogito» (HV5), sei con «Verso il rogito» (BAC, CF5/M), sei con titoli verbali (CFP), cinque per l'acquirente con «Contratto preliminare» (CC4). «Visite» (HV5) contro «Visita» (BAC, CF5, CC4). [PK] Cinque tappe venditore e quattro acquirente nell'interaction model; il punto è già aperto nelle note UI di PG1 e PG2.

**I11 · Estremi del percorso nel sottotitolo.** «dalla creazione del profilo all'atto notarile» (NAV), «dalla pubblicazione dell'immobile fino all'atto notarile» (HV5/D), «dalla creazione del profilo al rogito» (HV5/M, CC4/M), «dalla ricerca dell'immobile fino al rogito» (CC4/D).

**I12 · Nome del contratto.** «Contratto» (stepper HV5, BAC), «Contratto preliminare» (CC4, CFP), «preliminare» (HV5, CF5), «compromesso» (CFP «Il compromesso è il momento…», CC4 «Stipuliamo il compromesso»).

**I13 · Nome del momento finale.** «Rogito», «Verso il rogito», «rogito notarile», «atto notarile», «firma finale», «firma dal notaio».

**I14 · Chi pubblica l'annuncio e dove.** «Pensiamo noi a pubblicare il tuo annuncio su Cleclà e sui principali portali immobiliari.» (HV5) e «Cleclà valida e pubblica l'annuncio online.» (NAV/M) contro «Scegli tu su quali portale pubblicare l'annuncio» (CFP, «Cosa fai tu»). Il passo 02 si intitola «Crea il tuo annuncio» mentre HV5 dice che l'annuncio lo pubblica Cleclà. [PK] Pubblicazione senza CTA del venditore; titolo e descrizione li completa il team.

**I15 · Modello di trattativa.** CFP descrive una proposta unica che si accetta o si rifiuta («Se accetti prosegui verso il preliminare», «Se rifiuti, la trattativa rimane aperta»). [PK] PG2 lavora su condizioni singole con accettazione, controproposta e rifiuto per condizione.

### Firma e identità

**I16 · Firma.** «Firma elettronica qualificata (FEQ)» (CF5/D) contro «Firma digitale qualificata (FEQ)» con «riconosciuta dall'Agenzia delle Entrate» (CF5/M). «Firmi digitalmente con SPID o OTP» (CFP). [PK] Firma tramite Yousign, FEQ per il contratto e FEA per gli altri documenti.

**I17 · Momento della verifica d'identità.** «prima di fissare gli appuntamenti» (HV5), «prima di ogni contatto» (CF5/M), «prima della visita» (CF5/D), «prima dell'incontro» (CF5/D), «per confermare la prenotazione» (CFP acquirente).

**I18 · Quando servono i dati per la firma.** PRO: «Questi dati ti verranno chiesti solo al rogito.» [PK] L'anagrafica completa si raccoglie in «Preparazione alla firma» del preliminare, tramite Yousign; la memoria di progetto segnala già che la PG del Profilo utente li lega alla firma del contratto.

**I19 · Stati del documento d'identità.** PRO mostra «SCADUTO» e «Verificato». [PK] «Da caricare», «Verifica superata», «Esito negativo».

### Documenti e servizi

**I20 · Relazione tecnica.** «Relazione Tecnica» (HV5 input, elenco), «Relazione tecnica» (EMC), «Relazione tecnica urbanistica» (HV6 dettaglio), «Relazione Tecnica Cleclà» (elenco, voce titoli edilizi). Il rapporto con la RRE è detto solo in forma condizionale: «Nel caso in cui non sia disponibile la RRE», «Se non possiedi già la RRE».

**I21 · Scioglimento di APE.** «Attestato di Prestazione Energetica» (definizione, elenco) contro «Attestato Prestazione Energetica» (dettaglio budget HV6, EMC).

**I22 · Due versioni dell'elenco documenti e stato dei frame.** La versione più completa (HV6, EMC) sta in un frame il cui nome porta il marcatore di stop; quella precedente (HV5) in un frame marcato come contenitore; il solo titolo «Documenti che dovrai fornire tu come parte venditrice» sta in un frame marcato come approvato. Differenze voce per voce nella tabella del §6.2. Il contatore «11» dei documenti Cleclà corrisponde solo alla versione HV6.

**I23 · Condizione sotto la plusvalenza.** Sotto «Relazione di calcolo della plusvalenza immobiliare» compare la condizione sul Superbonus, chiusa da un punto interrogativo. Il calcolatore lega la plusvalenza a un'altra domanda (acquisto da meno di 5 anni e domicilio principale). Da verificare quale condizione va sotto quale documento.

**I24 · Numero dei documenti.** Calcolatore: 18 + 11 + 5 + 4 = 38. [PK] Archivio: 31 righe pertinenti in 8 cartelle; profilo immobile «28 di 32»; traguardi 6 · 7 · 19. Perimetri diversi o numeri da allineare: da chiarire prima di scrivere un numero in pagina.

**I25 · Nome della valutazione.** «Studio di vendibilità» (CF5, CC4), «valutazione puntuale» (HV5), «valutazione di mercato» (CFP), «VALUTAZIONE» (occhiello CF5). NAV usava ancora «uno studio di vendibilità» dove HV5 dice «una valutazione puntuale».

**I26 · Nomi delle funzioni.** «Trova tecnici», «Trova Tecnico», «Trova tecnico». «Documentazione» (sidebar) contro «Archivio documentazione» [PK].

**I27 · Incarico o mandato.** «recesso anticipato dall'incarico» (EMC, anche nell'email dell'acquirente, che l'incarico non lo firma) contro «acquisire il mandato» (CF5, colonna agenzia). [PK] «incarico di mediazione» nei wireframe, cartella d'archivio «Mandato e privacy».

### Voce e forma

**I28 · Voce di Cleclà nella colonna «Cosa fa Cleclà».** Terza persona nei passi 01-03 («Ti supporta nella creazione del profilo», «Pubblica l'annuncio su Cleclà e sugli altri portali», «Mostra agli acquirenti solo le tue disponibilità») e prima plurale nei passi 04-06 e nell'acquirente («Ti affianchiamo», «Generiamo il contratto preliminare», «Monitoriamo le scadenze»). In CF5/D e in CFP la colonna contiene anche «Inserisci dati base dell'immobile» e «Attivi il servizio fotografico professionale», alla seconda persona, ma in layer nascosti: da eliminare se sono avanzi. «Impariamo dalle tue ricerche e affina i suggerimenti» mescola le due voci nella stessa frase.

**I29 · Persona dei verbi in «Cosa fai tu».** Indicativo («Crei il profilo», «Definisci», «Controlli», «Verifichi», «Indichi», «Confermi», «Fissi», «Comunichi») e imperativo («Inserisci i dati del tuo immobile», «Completa la documentazione richiesta dal notaio», «Prepara l'immobile per la consegna», «Usa i filtri per affinare la ricerca») nella stessa lista.

**I30 · Frase di autonomia e testo dell'hero venditore.** Tre versioni del paragrafo hero (NAV/D, NAV/M, HV5/D con «Cleclà ti offre tutto il supporto di cui hai bisogno, quando serve.») e due chiuse («restano sempre le tue» / «sono sempre le tue»).

**I31 · CTA equivalenti con label diverse.** «Registrati gratis» / «Registrati (gratuito)». «Comincia subito» / «Inizia subito» / «Inizia da qui». «Usa un'email diversa» (REG) / «Prova con un altra email» (LOG). «Elimina account» / «Elimina profilo».

**I32 · Occhielli e inviti alla registrazione.** Maiuscolo e minuscolo (§2.3). «Pronto per iniziare?» / «INIZIAMO DA QUI?». «Pronto a iniziare?» esiste solo in blocchi pre-footer nascosti in tutti i frame. «Crea il tuo profilo e fai il primo passo» / «Crea il tuo profilo immobile e fai il primo passo» / «Crea il tuo profilo immobile e inizia il viaggio».

### Account

**I33 · Dove si cambia ruolo.** «dal tuo profilo» (REG), «dalla tua bacheca» (PRO, toast BAC), «Gestisci ruoli» fra le impostazioni (IMP).

**I34 · Eliminazione del profilo.** Oggetto: «account» o «profilo». CTA citata nel testo: «Elimina profilo» (/M) o «Conferma eliminazione» (/D). Effetto: «verrà disattivato» (/M), «verrà disattivato definitivamente» (/D), contro l'esito «L'eliminazione sarà confermata nei prossimi 30 giorni. Potrai riaprire un profilo con la stessa email in qualsiasi momento.».

**I35 · Uscita dall'account.** «Esci dal tuo account» (BAC) / «Logout» (PRO).

**I36 · Lessico delle notifiche.** «inadempienza» (IMP) contro «inadempimento» (EMC, [PK]). «offerta» (IMP) contro «proposta» (CFP, EMC «inizia a ricevere proposte»).

**I37 · Canali di contatto.** «Scrivici o chiamaci» senza un numero di telefono in pagina (CON). Dominio: «info@clecla.it» contro link email su «cleclà.com». [PK] Supporto in pagina tramite chat.

### Calcolatori

**I38 · Formato delle durate.** «6 mesi», «6 mesi, 3 sett», «4 mesi, 1 settimana», «2 mesi, 1 set.».

**I39 · Esito e spiegazioni del calcolatore tempistiche venditore.** Titolo del risultato: «Tempo stimato per arrivare al rogito notarile» e «Tempo stimato per concludere la vendita dell'immobile» (entrambi in HV5). Effetto del mutuo: «di circa 2 mesi» (HV5) contro «leggermente» (EMC). Tempistica: «porterà a prendere decisioni in merito all'annuncio…» (HV5) contro «predisporrà il venditore a valutazioni più elastiche…» (EMC).

**I40 · Etichette del riepilogo acquirente.** La domanda «È il primo immobile che compri?» diventa «Immobile individuato» in un risultato e «Primo immobile» in un altro. L'email acquirente spiega la regolarità con una frase sulla vendita: «Se il venditore ha già tutta la documentazione pronta, le tempistiche di vendita sono più veloci.».

**I41 · Risposta sulla fretta.** «Velocemente» (HV5) contro «Prima possibile» (EMC); la domanda offre «Sì» e «Non ho fretta».

### Numeri e prove

**I42 · Statistiche e testimonianze.** «120+ · Immobili venduti» (HV5) e «120+ · Annunci attivi» (CC4/M); «500+ · Case vendute» (CHI); «85 gg · Tempo medio di vendita» (NAV/M) accanto a stime di 4-6 mesi nei calcolatori. Su CC4 «Chi ha comprato casa con Cleclà» riporta la testimonianza di un venditore («Alla fine ho venduto in 4 mesi e mezzo.»). Molti valori sono ancora «xx» (§17).

### Trattativa [PK]

**I43 · Condizioni o clausole sospensive.** Frame approvati: «condizioni sospensive». [PK] Gruppo «Clausole sospensive» nella modale, «Condizioni sospensive» nella pagina trattativa.

**I44 · Soglia del silenzio e tono del callout.** 4 giorni (silenzio prolungato) contro 48 ore (sollecito di pagamento). Callout «Il venditore potrebbe avere altre proposte sul tavolo.» da confrontare con il «da evitare» del manuale (§15.3).

### Ruolo e versioni

**I45 · Ruolo sbagliato nella pagina acquirente.** CC4/M, frame acquirente: «Negozia con l'acquirente. Puoi contare sul nostro supporto per raggiungere un accordo chiaro e tutelante.». Il frame è nominato «Venditore – M - Venditore/1» pur contenendo la homepage acquirente.

**I46 · NAV contro HV5.** Stesso nome di frame, testi diversi: «uno studio di vendibilità» / «una valutazione puntuale»; «accordo chiaro e tutelato» / «tutelante»; «per evitare che siano le agenzie a presentarsi» presente solo in NAV; card «L'immobile è in regola. Lo certifichiamo noi» sostituita da «Tecnici qualificati». Il numero di step (2 contro 5) fa pensare che NAV sia la versione precedente, ma va confermato prima di considerarla superata.

---

## 17. Refusi e segnaposto nei frame approvati

Da correggere a prescindere dalle scelte sopra.

| Frame | Testo | Problema |
|---|---|---|
| NAV, HV5, CC4 | «Ti accompagnamo in tutte le fasi» | «accompagniamo» |
| NAV/M | «per concludere la tua trattiva» | «trattativa» |
| NAV/M | «tramite un caledario» | «calendario» |
| NAV/M | «stima indicativa delle tempistica» | concordanza |
| HV5 /D | «Cleclà ti  offre» | doppio spazio |
| HV5 | «Hai a disposizione  un team» · «Quali documenti hai già  a disposizione?» · «Tempo stimato per  concludere» | doppio spazio |
| HV5 /D | «completamento della pratica..» | doppio punto |
| HV5 | «*XXX Disclaimer tempistiche indipendenti da CLeclà» | segnaposto, «CLeclà» |
| HV5 | «*Disclaimer relativo al fatto che…» · «Fee Agenzia tradizionale · xxx» | segnaposto |
| HV5 | «meno di 5anni fa» | spazio mancante |
| HV5/M | «Placeholder» | segnaposto |
| HV6, EMC | «pagamento delle imposte disse» | refuso (probabilmente «ipocatastali» o «dirette»: da verificare) |
| HV6 | «€ xxx» | segnaposto |
| CC4 | «xx» · «xx%» (statistiche) | segnaposto |
| CC4 | «potrebbe  essere qui» | doppio spazio |
| CF5/M | «pubblicare l'annuncio .» | spazio prima del punto |
| CF5/M | «Wow!» | segnaposto |
| CF5 | nome frame «Come fuziona» | refuso nel nome |
| CFP | «Scegli tu su quali portale» | «portali» |
| CFP | «visibili da entrambi le parti» | «entrambe» |
| CFP | «puoi selezionare unon dei nostri partner» | «uno» |
| CFP | «Impariamo dalle tue ricerche e affina i suggerimenti» | concordanza |
| CFP | «passo, passo» | virgola (anche nel manuale di brand) |
| LOG | «Prova con un altra email» | «un'altra» |
| CON/M | «ti risponderemo risponde entro 48 ore» | parola doppia |
| CHI/M | «1 frase personale max 80 caratteri sulla persona.» | segnaposto |
| CHI | «nella scelta della gestione  delle compravendite» | doppio spazio |
| PRO | «Ho  venduto/comprato» · «es.Alba» | doppio spazio, spazio mancante |
| BAC/D | «Potrai passare da ruolo all'altro» | manca «un» |
| BAC | «Profilo acquirente  aggiunto» | doppio spazio |
| EMR, EMP | «https://cleclà.com/email-verification/d/…/edit?tab=t.0#heading=h.sgaek34o0qss» | URL segnaposto di un Google Doc |
| Footer | «C.F./P.IVA ______________________________» | dato mancante |

---

## 18. Cosa i frame approvati non coprono

I frame approvati coprono le pagine pubbliche, l'accesso, l'account e la bacheca vuota. Non contengono copy approvato per: visite e calendario, profilo immobile e scheda tecnica, archivio documenti, annuncio, trattativa, preparazione alla firma, pagamento della registrazione, rogito operativo.

Per i temi citati come esempio nella richiesta la situazione è questa. Condizione sospensiva: tre righe in CFP, nessuna spiegazione del concetto. Recesso: una riga nell'email del calcolatore budget e una voce di notifica. Inefficacia e caparra confirmatoria: assenti ovunque. Silenzio della controparte: solo in [PK]. Fasi del processo: presenti, con i nomi divergenti di I10.

Le formulazioni esatte di recesso, inadempimento, inefficacia e silenzi esistono nei frame UI di «PG1 · Guida alla trattativa» e «PG2 · Pagina trattativa» (pagina «UI Layouts – WIP», Sprint 3). Quando saranno approvate, vanno estratte e aggiunte qui ai §7, §9 e §10.
