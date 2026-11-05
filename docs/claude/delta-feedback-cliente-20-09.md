# Delta dal feedback cliente sulla fase Trattativa

Versione 1.0 · 22/09/2026 · lettura dei commenti sulla board FigJam «[EXT] Cleclà | Feedback», pagina «V.1 - 17/9» (`1ZS96SiXSktrMXrvLrsPA0`, node `2681:7271`), confrontati con le tavole della pagina «UI Layouts – WIP» del file «Cleclà | UI» (`0k5JkkrVwDydzvUoRHv8ye`).

## Cosa contiene il feedback

95 commenti ancorati alle tavole della pagina V.1, più un commento generale con una replica sul tono dell'interfaccia. Tutti firmati «Cleclà», scritti il 20/09. Nessuno risolto. La distribuzione dice già dove si concentra il lavoro: PG1 21 commenti, PG2 36, PG3 14, PG4 24. Sulle tavole mobile non c'è nessun commento, per scelta dichiarata: «è una conseguenza delle modifiche della versione desktop».

Altri 17 commenti sulla board riguardano pagine precedenti (landing, costi, scheda tecnica) e restano fuori da questa analisi.

Il cliente mette due riserve esplicite: i testi si valutano dopo, e il rework va riapprovato. Quindi il delta qui sotto riguarda struttura, logica e flusso, non copy.

## I due vincoli trasversali

Il primo è di contenuto: «le modifiche vengono scritte, in genere, per una pagina ma naturalmente si riferiscono a tutte». Ogni voce di questo documento va letta come regola, non come correzione puntuale.

Il secondo è visivo e pesa su tutte e quattro le priority guide: meno colore, meno avvisi, meno testo. L'esempio che portano è R4, la pagina in cui il venditore aspetta il pagamento della registrazione: «la presenza di numerosi avvisi gialli potrebbe far pensare a un problema, mentre si tratta di una normale fase della procedura». La regola che ne deriva è che l'avviso resta solo dove c'è davvero un'azione da fare o un rischio, e che quando tutto procede la pagina deve dirlo con chiarezza invece di segnalare.

Questo tocca la regola oggi in vigore su Alert e bottoni info (Complex per ciò che spiega, Default per ciò che constata, colore legato al fatto): la regola regge, cambia la soglia. Servirà una passata di censimento degli Alert sulle quattro PG con il criterio nuovo.

## Il cambio di modello, che è il delta vero

Tutto il resto discende da qui. Oggi la trattativa si svolge su un «documento di puntuazione» diviso in quattro gruppi di condizioni (Prezzo e pagamento, Condizioni sospensive, Dichiarazioni, Tempistiche e disponibilità), con una barra dell'accordo a otto segmenti e una modale che propone sei opzioni.

Il cliente chiede due contenitori al posto di quattro.

**Dichiarazioni delle parti.** Non negoziabili, informative alla controparte. Ognuno risponde alle proprie e vede l'esito di quelle dell'altro. L'acquirente dichiara se acquista con mutuo, se deve vendere il proprio immobile per finanziare l'acquisto, e in presenza di terreno agricolo pertinenziale se intende comprare anche quando il terreno va a chi ha diritto di prelazione. Il venditore dichiara se esiste la relazione tecnica e, se esiste, se l'immobile è regolare. Ogni risposta genera in automatico la condizione sospensiva corrispondente, che entra nel riepilogo e nel documento di puntuazione.

**Argomenti da trattare.** Tre soli: prezzo, data del rogito, data di consegna dell'immobile. Nient'altro si negozia.

Le conseguenze dirette:

| Cosa esiste oggi | Cosa diventa |
|---|---|
| Quattro gruppi di condizioni nel documento di puntuazione | Due sezioni: Dichiarazioni delle parti e Argomenti da trattare |
| Barra dell'accordo a otto segmenti | Indicatore sui tre argomenti, «2 di 3 concordati» |
| Modale «Proponi una condizione» con sei opzioni in due gruppi | Due blocchi: i tre argomenti negoziabili e le dichiarazioni, che non si propongono |
| Gruppo «Prezzo e pagamento» | Solo prezzo. Il pagamento non si tratta |
| Riga «Indennità forfettaria di occupazione» | Fuori, sia da «Cosa si tratta» sia dal riepilogo T4 |
| Condizioni sospensive come gruppo negoziabile | Esito automatico delle dichiarazioni, non oggetto di trattativa |
| Prima proposta con tutte le condizioni | L'acquirente propone prezzo e data del rogito. La data di consegna la introduce il venditore nella prima risposta, scegliendo se coincide con il rogito o indicandone un'altra da calendario |

La prelazione agraria prende una dipendenza nuova: la dichiarazione compare all'acquirente solo se la scheda tecnica segnala il terreno agricolo, altrimenti la domanda non esiste. Il venditore in questa fase non fa nulla; porterà la proposta agli aventi diritto dopo la firma del preliminare e tornerà in piattaforma a dichiarare l'esito dopo 30 giorni.

## PG1 · Guida alla trattativa

| Blocco | As-is | Richiesto |
|---|---|---|
| Ingresso alla pagina | Cliccando «Trattativa» si arriva qui ogni volta | Non deve essere la destinazione di default: chi ha una trattativa aperta deve trovarsi nella trattativa |
| Sidebar | Pannello chiuso con freccia di apertura da 32 px | Il click sull'icona apre la sidebar per intero, senza freccia. Vedi la controproposta sotto la tabella |
| Stepper di spalla | Quattro sotto-passi della tappa Trattativa | Da riposizionare e ripensare dopo la ristrutturazione della pagina |
| Sezione «Come funziona» | Step-walker a sei passi in accordion, con testo introduttivo | Navigazione a pallini su linea orizzontale in cima, il click apre il blocco. Via il testo introduttivo, una frase sola per passo |
| Indice «In questa pagina» | Card in spalla, su mobile tendina sticky | Dichiarato non più necessario dopo il passaggio ai pallini |
| Passo 5 dello step-walker | I dati di chi firma, lato venditore | Vale per entrambi: anche l'acquirente indica chi compra con lui |
| Sezione «Cosa si tratta» | Quattro righe: prezzo e pagamento, tempistiche, condizioni sospensive, dichiarazioni | Tre argomenti: prezzo, data del rogito, data di consegna. Il mobilio si spiega meglio: non si tratta, ma il prezzo globale può comprendere la cucina, esplicitandolo nelle note dell'offerta. Nessun modulo generato |
| Condizioni sospensive | Riga dentro «Cosa si tratta» | Sezione a sé, dopo «Cosa si tratta» e prima di «Quando fissare il rogito», con le dichiarazioni delle due parti e un popover sul diritto di prelazione (testo fornito dal cliente) |
| Data di consegna | Nessuna spiegazione dedicata | Bottone info che spiega perché può non coincidere con il rogito (testo fornito) |
| Sezione «Quando fissare il rogito» | Otto voci di tempi tecnici più il blocco «Tempistiche del rogito» | Solo cinque tempi indicativi: mutuo 3 mesi, vendita casa 6, sanatoria 6, sanatoria e mutuo 9, nessuna condizione 2. Via la lista. Del blocco resta solo la proroga. Il sottotitolo passa da «le date» a «la data» |
| Sezione «Errori da evitare» | Sette voci | Punto 3 riformulato: non c'è valutazione certificata, se si bloccano sul prezzo interviene Cleclà con un suggerimento. Punto 7 eliminato. Voce nuova: abbandonare la piattaforma e proseguire fuori, perdendo il supporto legale sul preliminare |
| Sezione «Perché non c'è la caparra» | Due card a confronto, agenzia tradizionale contro Cleclà | Via il confronto. Diventa la spiegazione del perché non si lavora con la caparra: clausola penale al 5% a carico dell'inadempiente, nessun passaggio di denaro fra sconosciuti, preliminare concludibile senza liquidità immediata. La riga di chiusura resta come concetto |
| Sezione «Cosa può succedere dopo la firma» | Tre card su recesso, inadempimento, inefficacia | Rimossa: il contenuto passa alla guida contestuale del contratto preliminare |

Sulla sidebar la richiesta non si recepisce così. La freccia in basso resta: è un comando esplicito, raggiungibile da tastiera e nominabile, e toglierla lascia l'apertura affidata a un gesto che nessun elemento dichiara. Il click su un'icona della sidebar chiusa deve portare alla destinazione di quell'icona, che è il motivo per cui l'icona è lì; se apre il pannello, la voce di menu smette di essere una voce di menu. La proposta alternativa da portare al cliente è l'apertura su hover per il desktop, che dà la stessa immediatezza senza consumare il click e senza togliere la freccia.

## PG2 · Pagina trattativa

Oltre al cambio di modello, il cliente riscrive il percorso di accesso e alleggerisce la pagina.

Accesso e navigazione. Cliccando «Trattativa» il venditore arriva a una pagina «Trattative in corso» con l'elenco degli acquirenti, solo il nome, nessuna descrizione sotto; con lo stato vuoto «Non ci sono trattative in corso». Il click sul nome apre la trattativa. L'acquirente vede la stessa cosa per immobile, con gli indirizzi al posto dei nomi. Dentro la trattativa, sotto l'indirizzo, resta il selettore per passare da una all'altra. Oggi questa pagina non esiste: c'è il popover «Elenco trattative» e il blocco «Trattative in parallelo» in fondo alla pagina, che è il modello grafico a cui il cliente rimanda.

Nota di progetto, non richiesta dal cliente: questo elenco in prospettiva sta nella Bacheca, non in una pagina a sé. L'architettura informativa lo colloca già lì, sotto il nodo «Trattative» della bacheca personale, con «Trattativa (n)» e la guida come figli; la bacheca però è organizzata per immobile e per la trattativa oggi ha solo un ingombro dichiarato, fuori perimetro Sprint 2. Quindi la schermata che serve al cliente è l'area Trattative della Bacheca, e il lavoro da fare è aggiungere quel blocco al catalogo dei blocchi, con le sue due viste per ruolo e lo stato vuoto.

Contenuto della pagina di trattativa. Vanno via tutti i blocchi che precedono il documento di puntuazione: restano intestazione essenziale, selettore e alert. All'apertura si devono vedere subito dichiarazioni e argomenti. Il pulsante «Proponi» sale sotto il titolo degli argomenti, oppure entra nei tre riquadri espandibili. Gli argomenti della box in alto a destra diventano cliccabili e portano alla guida e al riepilogo; il riepilogo deve essere accessibile in qualsiasi momento e popolarsi con gli accordi raggiunti e le condizioni sospensive derivate. «Annulla la trattativa» resta in fondo.

Regola nuova: la trattativa non si chiude finché restano dichiarazioni non completate, da una parte o dall'altra. Serve lo stato corrispondente.

| Tavola | Richiesta |
|---|---|
| T3 · In attesa (Acquirente) | La riga di reciprocità in «Trattative in parallelo» resta |
| T4 · Riepilogo e conferma | Le condizioni concordate scendono ai tre argomenti. «Data di trasferimento del possesso» diventa «Data consegna delle chiavi dell'immobile». Escono indennità di occupazione, regolarità-sanatoria e prelazione. Le condizioni sospensive diventano quattro: mutuo, vendita dell'immobile dell'acquirente, acquisto congiunto di immobile e terreno agricolo, regolarità urbanistica e conformità catastale. Il banner «Accordo raggiunto» resta |
| T4 · «Cosa succede dopo» | Via il passo sulla verifica catastale. I documenti d'identità e la mail si chiedono solo se ci sono altri venditori o acquirenti non registrati, per mandare l'informativa privacy; la privacy si firma con il preliminare. Il passo 3 diventa «il team legale genera la bozza per vostra approvazione». Il passo 4 nomina contratto, identificazione della clientela ai fini antiriciclaggio e privacy. Il passo 5 si sdoppia: l'acquirente paga, poi Cleclà registra presso l'Agenzia delle Entrate. Serve un punto di domanda sul riconoscimento dell'intervento mediatorio di Cleclà alla conferma dell'accordo |
| T5 · Chiusura | «Mancano 2 documenti» si sposta sotto i documenti di identità. Via la riga sulla verifica catastale. I documenti d'identità e la mail solo nei casi detti sopra. La riga di responsabilità non si capisce. Da chiarire dove porta la CTA verso la documentazione |
| Onboarding di fase | Una sola box per il venditore, con il messaggio ridotto a «hai ricevuto una proposta, inizia la trattativa» e i due rimandi a trattativa e guida |
| Modale «Proponi» 1 di 3 | Aggiornata ai tre argomenti, con le dichiarazioni in blocco separato e non negoziabile. Sulla data del rogito, bottone info con i cinque tempi indicativi e rimando alla guida |
| Modale «Proponi» 3 di 3 | Via la scadenza: negli argomenti non c'è scadenza, la scadenza appartiene alle dichiarazioni e influenza la data del rogito |
| Modale «Rispondi» data del rogito | Stesso bottone info sui tempi |
| Modale «Rispondi», stato controproposta | Manca il campo nota. Vale per tutte le proposte e le controproposte |
| Modale-Confronto prezzi | Via il prezzo dello studio di vendibilità. Restano proposta e prezzo dell'annuncio, con il riferimento che si aggiorna sull'ultima proposta del venditore |
| Riferimento · Documento di puntuazione (Acquirente) | Riscrivere la nota sui mobili: non si tratta l'arredo, nel prezzo entra solo la cucina se la si vuole, e Cleclà non genera moduli |

## PG3 · Preparazione alla firma

Qui il delta è di struttura: la tappa passa da cinque momenti a tre.

«Sarebbe più intuitivo unificare le due pagine e avere un'unica schermata in cui vedo i nomi e ho la possibilità di caricare i documenti. Qui in realtà avrebbe senso ridurre a tre voci, una con elenco persone e caricamento documenti, poi il contratto preliminare e poi la pagina con il riepilogo delle firme del preliminare.» Lo ripetono due volte, su F2 e su F3.

| Stato | Esito |
|---|---|
| F1 + F2 | Una schermata sola. Tre box: la tua parte, l'aggiunta di una persona sotto la parte che la aggiunge, la controparte. L'ordine dipende dal ruolo di chi guarda. Il caricamento non resta bloccato finché mancano nomi. La CTA diventa «Vai a contratto» e si sblocca a documenti completi |
| F3 · Consensi | Eliminata. L'informativa privacy si manda per mail in presa visione; privacy e identificazione della clientela ai fini antiriciclaggio si firmano con il preliminare. Nessuna casella da spuntare in questa fase |
| F4 · Contratto | Riprogettata: box del contratto con una dichiarazione obbligatoria da accettare prima di visualizzarlo o scaricarlo, che riconosce l'intervento mediatorio di Cleclà; sotto, la richiesta di modifiche, gestite da Cleclà, con storico visibile a entrambi; la firma si sblocca solo quando entrambe le parti hanno dato il benestare sul documento, e da quel momento le modifiche si bloccano; sintesi ridotta alle sole condizioni approvate; via «Le parti coinvolte»; alert da ripensare e riposizionare. Alla CTA di firma manca la privacy |
| F5 · In attesa delle firme | Da verificare chi può sollecitare chi. Il blocco del footer vale solo per l'acquirente |
| Stepper della tappa Contratto | Da quattro passi a tre |
| Termine «responsabilità» | Da sostituire con una formula più morbida, orientata a chi deve fare cosa |
| Popover sui documenti d'identità | Si chiama «Identificazione della clientela ai fini dell'antiriciclaggio» |
| Pannello Yousign, passaggio 2 | Da chiarire: nella tavola carica Elena Ferrero, ma il modello dice che carica l'utente registrato |

## PG4 · Pagamento registrazione

Tre cambi sostanziali e una lunga lista di correzioni di merito.

Il primo: l'importo non è più fisso. Varia con il tipo di contratto preliminare, lo inserisce Cleclà quando tutti hanno firmato, ed è senza IVA perché è un'imposta dell'Agenzia delle Entrate e non un servizio. Dentro la cifra ci sono solo imposta di registro e marche da bollo, dichiarate senza importo per riga. La voce «Servizio Cleclà — deposito e registrazione» esce dalla scomposizione.

Il secondo: le scadenze sono due e oggi in pagina ce n'è una. 30 giorni dall'ultima firma sono il tempo di Cleclà per registrare; 5 giorni dall'emissione della fattura sono il tempo dell'acquirente per pagare. La CTA di pagamento si attiva alla ricezione della fattura.

Il terzo: il contratto non si annulla se non viene registrato in tempo. Gli avvisi che lo dicono vanno rimossi o sostituiti, in R1 e in R4.

| Tavola | Richiesta |
|---|---|
| R1 | «Perché si paga» riscritto: l'opponibilità ai terzi discende dalla trascrizione, non dalla registrazione. Il concetto da rendere in forma breve è data certa, prova dell'accordo, adempimento fiscale, tutela in caso di controversia. Via «Perché tocca a te» o sostituirlo. Via l'avviso sui 30 giorni. La registrazione parte dal primo giorno lavorativo dopo il pagamento e richiede fino a 30 giorni di calendario, perché un rifiuto della registrazione telematica obbliga alla registrazione fisica con appuntamento a circa 15 giorni. Un blocco duplicato da eliminare |
| R2 | Stessa precisazione sui 30 giorni di calendario, in due punti. Da chiarire se le date sono automatiche o le inserisce Cleclà |
| R3 | Il contratto non è opponibile a terzi, lo è la data di registrazione. Condizioni sospensive da riallineare al nuovo modello: escono le ultime due, entra la vendita dell'immobile dell'acquirente se presente. Il notaio porta accanto al nome la città in cui lavora, senza il riferimento a Cuneo. I documenti per il rogito diventano un rimando alla cartella. Ciascuna parte vede solo la propria provvigione. La CTA finale non si capisce dove porti |
| R4 | Allineata alle modifiche lato acquirente. Via il promemoria del venditore all'acquirente. L'avviso sull'archiviazione diventa un pagamento che non tocca al venditore. La box sui 30 giorni esce. È la pagina citata come esempio di interfaccia troppo allarmante |

## Decisioni già registrate che il feedback ribalta

Sono i punti su cui il rework contraddice qualcosa che era stato chiuso, e che vale la pena nominare prima di rimettere mano alle tavole.

La sidebar chiusa con bottone di apertura da 32 px, fissata per PG1, PG2, PG3 e PG4, è l'unico punto su cui controproponiamo invece di recepire: la freccia resta e il click sull'icona continua a portare alla sua destinazione, con l'apertura su hover come alternativa da discutere.

La regola «vale la condizione più lunga» sui tempi del rogito, dichiarata nel blocco «Tempistiche del rogito», non regge con i numeri nuovi: sanatoria e mutuo insieme danno 9 mesi, cioè la somma di 6 e 3.

Il confronto con l'agenzia tradizionale nella sezione sulla caparra esce, dopo essere stato costruito sul modello del confronto già approvato nelle pagine pubbliche.

Lo switch fra trattative era stato chiuso come chip che apre un popover, presente solo lato venditore perché solo lì esiste il blocco delle trattative in parallelo. Ora serve una pagina indice per entrambi i ruoli, e il chip resta come selettore interno.

L'importo della registrazione a 320 € più IVA, 390,40 € totali, con la CTA «Paga 390,40 € e registra il contratto», decade.

## Discrepanze da segnalare al cliente

Per istruzione di progetto le segnalo invece di risolverle.

Il cliente scrive «documento di puntazione»; in pagina, nei documenti e nel glossario la forma è «documento di puntuazione». Serve la forma buona, anche perché nel nuovo modello il documento resta come output ma sparisce come titolo di sezione, sostituito da «Argomenti da trattare».

«Argomenti da trattare» e «Dichiarazioni delle parti» sono termini nuovi. Oggi i doc dicono «gruppi di condizioni» e «Dichiarazioni che entrano nel preliminare», e il glossario non conosce nessuno dei due.

La data di consegna ha tre nomi nello stesso feedback: «data consegna immobile», «data di consegna delle chiavi», «Data consegna delle chiavi dell'immobile». In pagina oggi è «Data di trasferimento del possesso», nei frame approvati «consegna immobile».

La prelazione agraria compare in T4 come «Acquisto congiunto dell'immobile e del terreno agricolo» e altrove come «prelazione agraria». È lo stesso oggetto.

«Identificazione della clientela ai fini dell'antiriciclaggio» sostituisce «dichiarazione antiriciclaggio» in tutte le occorrenze, glossario compreso.

L'elenco delle trattative si sovrappone a una destinazione che ha già tre nomi: «I miei immobili» nel breadcrumb, «Vai a tutte le tue trattative» nel link, Bacheca nell'architettura informativa. Visto che la destinazione è il nodo «Trattative» della Bacheca, il nome va scelto ora, prima di disegnare il blocco.

Sulla registrazione tardiva, il testo oggi in pagina e la project knowledge dicono che il contratto si annulla; il cliente dice che non si annulla e che c'è una piccola penale. Il punto aperto 20 sui T&C resta il posto dove questo si chiude.

## Domande aperte che bloccano il rework

Sono le sei che vanno risolte prima di ridisegnare, non dopo.

Da dove parte fisicamente la prima proposta dell'acquirente. Il cliente lo chiede esplicitamente sull'onboarding, e nelle tavole quella schermata non c'è.

Se la navigazione a pallini vale per la sola sezione «Come funziona» o per tutta la guida, perché da questo dipende se l'indice in spalla sparisce del tutto o solo in parte.

Dove vive la guida contestuale alle sezioni del contratto preliminare. È nei requirements, il cliente la reclama su F4, e PG1 perde una sezione in suo favore.

Come il sistema sa che la fattura è stata emessa, visto che da quel momento partono i 5 giorni e si sblocca il pagamento.

Se i tempi del deposito in R2 sono automatici o li aggiorna Cleclà a mano.

Chi carica i documenti d'identità degli altri, che è una regola già fissata ma che la tavola del pannello Yousign sembra contraddire.

## Impatto sulle tavole

Il rework non è una passata di correzioni. PG2 e PG3 vanno rifatte nella struttura, PG1 nella sequenza delle sezioni e nel pattern di navigazione, PG4 nel contenuto di R1 e nel tono di R4.

Schermate nuove da disegnare: riepilogo come destinazione accessibile in ogni momento, stato di chiusura bloccata per dichiarazioni incomplete, storico delle richieste di modifica al preliminare con il doppio benestare.

Fuori da PG2, nella Bacheca: il blocco «Trattative» con la vista venditore per nome, la vista acquirente per immobile e lo stato vuoto. Va nel catalogo dei blocchi della bacheca, che per la trattativa oggi porta solo un ingombro.

Schermate che escono: F3 Consensi, la sezione «Cosa può succedere dopo la firma» di PG1, e le due tavole mobile dell'indice della guida se l'indice cade.

Schermate che si fondono: F1 e F2 in una sola.

Il mobile segue, come dichiarato dal cliente, ma è comunque un secondo giro completo su quattro priority guide.
