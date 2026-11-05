# Delta sulle 4 PG dopo le guide del 14/09

Analisi del 15/09/2026 su tre documenti del cliente: il Google Doc «Come funziona la Trattativa Cleclà» e le due guide PDF «Guida per il Venditore» e «Guida per l'Acquirente» del 14/09.

## Punto di partenza: cosa è davvero nuovo

Il Google Doc linkato è lo stesso documento già presente nella project knowledge dal 14/09 con il nome «Come funziona la trattativa»: stesse nove sezioni, stesso testo. Non cambia niente rispetto a quanto già recepito nelle PG.

Il materiale nuovo sono le due guide. Sono documenti rivolti agli utenti finali, non specifiche, ma contengono sei cose che nelle PG oggi non ci sono o ci sono diverse:

1. il percorso raccontato come **sei passi numerati**, con l'attribuzione del turno (tocca a te / tocca alla controparte / entrambi / supporto Cleclà);
2. la **clausola penale del 5%** al posto della caparra confirmatoria, presentata come «il punto più importante»;
3. il **recesso con multa penitenziale del 5%**, non cumulabile con la penale;
4. la **notifica automatica 30 giorni prima della scadenza** di una condizione, con proroga concordabile fra le parti;
5. l'**avveramento della condizione segnalato in piattaforma** dalla parte che l'ha dichiarata;
6. quattro **tempi tecnici** per la data del rogito, due dei quali in conflitto con il documento principale.

## I sei passi contro i quattro sotto-passi dello stepper

Sequenza fissata dalle guide, identica nelle due versioni tranne il ruolo che agisce:

| # | Turno | Venditore | Acquirente |
|---|---|---|---|
| 1 | Acquirente | Ricevi una proposta | Fai la tua proposta |
| 2 | Venditore | Rispondi e dichiari lo stato dell'immobile | Ricevi una risposta |
| 3 | Supporto Cleclà | In caso di stallo nella trattativa | In caso di stallo nella trattativa |
| 4 | Entrambi | Fissate la data dal notaio | Fissate la data dal notaio |
| 5 | Chi ha condotto la trattativa | Fornisci i dati di tutti i proprietari | Fornisci i tuoi dati |
| 6 | Entrambi | Guardi il contratto e firmi digitalmente | Guardi il contratto e firmi digitalmente |

Lo stepper dell'epica ha invece quattro sotto-passi dentro la tappa Trattativa: Guida alla trattativa · Proposta delle condizioni · Risposte e controproposte · Accordo raggiunto. Tre scostamenti:

- lo **stallo** è un passo numerato del racconto ma non è un'azione dell'utente, e nella UI non esiste come stato;
- i **passi 5 e 6** stanno oggi nella tappa Contratto (PG3 F1 e F4), non nella Trattativa;
- i quattro segmenti della barra di percorso mobile di PG1 e PG2 contano i quattro sotto-passi: se il racconto ufficiale diventa a sei, il conteggio non torna più con quello che l'utente ha letto nella guida.

## PG1 · Guida alla trattativa

È la PG più toccata, perché la guida PDF e la PG1 raccontano la stessa cosa a due utenti che leggeranno entrambi i documenti.

**Lo step-walker passa da cinque a sei passi**, e ogni passo acquista l'etichetta di turno. È l'informazione che la pagina oggi non dà: chi deve muoversi adesso e chi sta aspettando.

**La variante Acquirente va riaperta.** È stata eliminata il 16/09 perché, tolto il pianificatore delle date, le due versioni dicevano la stessa cosa. Con i sei passi non è più vero: i passi 1, 2 e 5 cambiano di ruolo, e le condizioni dichiarate sono diverse (mutuo e vendita di un immobile per l'acquirente, sanatoria e consegna delle chiavi per il venditore).

**Serve una sezione nuova sulla clausola penale.** Le guide la trattano come il punto centrale: nessun passaggio di denaro anticipato, 5% del prezzo a carico di chi è inadempiente, art. 1382 c.c., e il confronto esplicito con la caparra confirmatoria «altrove». Oggi PG1 non nomina né la caparra né la penale, e il glossario registra che «penale» non compare in nessun frame approvato (§15.1).

**La sezione «Quando si annulla il contratto preliminare» prende i numeri.** Le tre card Recesso, Inadempimento, Inefficacia oggi sono qualitative: il recesso vale 5% a titolo di multa penitenziale, l'inadempimento 5% a titolo di penale, e le due somme non si sommano mai. L'Alert di chiusura sezione («se l'affare non si conclude e la responsabilità non è di nessuno, non si paga niente») regge e trova conferma nell'esempio della sanatoria non conclusa.

**«Quando fissare il rogito»: il corpo segnaposto dell'Alert ha finalmente un contenuto.** La notifica a 30 giorni dalla scadenza e la proroga concordabile sono esattamente quello che il blocco «Tempistiche del rogito» doveva dire. Resta da riconciliare la lista dei sette tempi della pagina con i quattro valori delle guide.

**Un blocco che oggi manca del tutto**: quando una condizione si avvera, è la parte che l'ha dichiarata a doverlo segnalare in piattaforma. La guida lo dice, PG1 si ferma alla firma.

**Conferma utile**: il raggruppamento «Dichiarazioni che entrano nel preliminare», che in PG1 era un'ipotesi, trova una formulazione del cliente — «Le tue condizioni diventano clausole».

## PG2 · Pagina trattativa

**Lo stallo diventa uno stato da disegnare.** Il documento principale dà la regola (dopo due proposte rifiutate Cleclà propone la media), le guide la promuovono a passo del percorso. Oggi PG2 non ha né uno stato né una riga per questo. Servono almeno: il momento in cui la piattaforma suggerisce il prezzo, la provenienza «suggerita da Cleclà» sulla riga di condizione — il badge «inserita dal sistema» esiste già — e le due uscite per ciascuna parte. Il conteggio delle due proposte rifiutate va reso visibile prima, altrimenti l'intervento arriva senza preavviso.

**Il modello a condizioni singole resta in tensione.** Entrambe le guide ripetono che si trattano solo prezzo e data, e che tutto il resto «sono condizioni che dichiarate, non punti su cui negoziare». La modale «Proponi una condizione» con dieci opzioni fa un'altra cosa. È l'incongruenza I15, che finora opponeva le pagine pubbliche a PG2: ora la stessa opposizione arriva da un documento che il cliente consegna agli utenti.

**Le condizioni sospensive scendono a quattro.** Le guide elencano mutuo, vendita di un immobile dell'acquirente, sanatoria urbanistica o catastale, prelazione agraria. Non compaiono la soluzione abitativa per il venditore (Scheda Tecnica 2.0), la liberazione da vincoli e ipoteche e l'assenza di diritti di terzi (R3 di PG4). La barra dell'accordo a otto segmenti va ricontata.

**La reciprocità dell'assenza di esclusiva va dichiarata a entrambi.** Le guide la scrivono in modo simmetrico: «Il Venditore non ha esclusiva su di te, e nemmeno tu su di lui». Oggi il venditore vede «Trattative in parallelo» con i nomi, l'acquirente solo «Il proprietario può trattare anche con altri». Manca, da entrambe le parti, il fatto che vale anche al contrario.

**Fra T4 e T5 si inserisce il passo 5.** La raccolta dei dati dei cointestatari, oggi in PG3 F1, nelle guide è l'ultimo passo prima della firma e lo fa chi ha condotto la trattativa. Va deciso se PG2 si chiude prima o dopo quella raccolta.

**Confermato**: sul prezzo accetta / rifiuta / controproposta, sulla data un solo giro di conferma senza rifiuto secco. La UI è già così.

## PG3 · Preparazione alla firma

**Chi carica i dati degli altri intestatari è una contraddizione aperta.** Le guide dicono che è chi ha condotto la trattativa a caricare in piattaforma i dati di tutti gli altri. F1 disegna una catena dell'invito in cinque passaggi in cui ogni persona si registra e completa i propri passaggi. Le due cose possono convivere solo se si separa quello che si carica per conto di altri (i dati anagrafici che finiscono nel contratto) da quello che resta personale (documento d'identità, consensi, firma): oggi la separazione non è dichiarata da nessuna parte.

**F4 guadagna una riga nel riepilogo.** Se il contratto contiene la clausola penale al 5%, il blocco «Le vostre condizioni, in sintesi» dovrebbe dirlo: è l'unica clausola economica che nessuno dei due ha negoziato.

**Confermato**: l'anteprima prima della firma, la FEQ con lo stesso valore della firma autografa, la firma asincrona da dispositivi diversi, e l'uscita «se qualcosa non torna, scrivi al team prima di firmare», che corrisponde a «Qualcosa non torna: chiedi una modifica».

## PG4 · Pagamento registrazione

Nessuno dei tre documenti parla di registrazione, di 320 € o dei 30 giorni. PG4 resta come è, con due avvertenze.

**L'elenco delle condizioni sospensive di R3 non è confermato da nessuna delle tre fonti.** Liberazione da vincoli e ipoteche e assenza di diritti di terzi non compaiono; la prelazione e la sanatoria sì. È la discrepanza già segnalata nel controllo di coerenza, e ora c'è un elemento in più per chiuderla.

**La penale del 5% non è la penale del punto aperto 20.** Il 5% delle guide riguarda il rapporto fra venditore e acquirente dopo la firma del preliminare; le penali dei T&C riguardano il rapporto venditore-Cleclà. Il punto aperto 20 — cosa succede al contratto firmato se l'acquirente non paga la registrazione — resta aperto, e ora va tenuto separato anche nel lessico.

**Fuori dalle quattro PG** resta un flusso che le guide introducono e nessuna schermata copre: dopo la firma del preliminare il Venditore comunica la proposta agli aventi diritto di prelazione, con il documento fornito da Cleclà, e quelli hanno 30 giorni per esercitarla. Oggi non è un compito visibile da nessuna parte.

## Discrepanze da far sciogliere al cliente

Segnalate, non risolte.

1. **Tempi tecnici invertiti.** Il documento principale dice mutuo 2 mesi e nessuna condizione 3 mesi; entrambe le guide dicono mutuo 3 mesi e nessuna condizione 2 mesi. Vendita di un immobile e sanatoria coincidono a 6 mesi. La lettura più probabile è un'inversione, ma è il numero che finisce nel validatore della data del rogito.
2. **Numero e numerazione dei passi.** I due PDF contengono tracce di due impaginazioni sovrapposte, una a nove e una a dieci pagine, che numerano diversamente lo stesso passo: la data del rogito è il passo 3 in una e il passo 4 nell'altra. Va confermato quale versione è quella buona.
3. **Lo stallo come passo.** Sta dentro una lista intitolata «I tuoi 6 passi» ma non è un'azione dell'utente. Se resta un passo, la UI deve mostrarlo nel percorso; se è un servizio, va tolto dalla numerazione.
4. **Quante sono le condizioni sospensive.** Quattro nelle guide, cinque nella Scheda Tecnica 2.0, un elenco ancora diverso in R3.
5. **La consegna delle chiavi dopo il rogito** è presentata nella tabella «Le tue condizioni diventano clausole», introdotta dalla frase «entra nel Contratto Preliminare come condizione sospensiva». Non è una condizione sospensiva: è una clausola con una data. La tabella le mescola.
6. **Il lessico della penale.** «Clausola penale», «multa penitenziale» e «5%» sono termini nuovi rispetto al glossario, dove il concetto esiste solo come «costi aggiuntivi» e dove «caparra confirmatoria» non compare. Se i testi passano, vanno portati al §10 del glossario.
7. **Chi carica i dati dei cointestatari** (vedi PG3).
