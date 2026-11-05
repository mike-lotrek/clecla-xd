# Wireframe · Finalizzazione (Sprint 5)

Versione 1.5 · 01/10/2026 · file **Cleclà | UI** (`0k5JkkrVwDydzvUoRHv8ye`), pagina `📏 Wireframe` sotto «🛑 Sprint 5 - Finalizzazione» (`71:2495`), sezione «Finalizzazione» (`4705:171330`).

Fonti: `clecla_pg_finalizzazione_v2.md` (sezioni PG 1–4), `claude/user-flow-finalizzazione.md` (board FigJam, REVIEW 16/03), decisioni successive al feedback del 20/09 (`delta-feedback-cliente-20-09.md`, `ui-pg2/pg3/pg4-v2-feedback-20-09.md`), `coerenza-firma-verifica-25-09.md` (Youtrust), `ui-contratto-lettore-guida.md` (template del contratto), glossario v1.1, interaction model. Stepper e collegamenti in UI: `claude/stepper-contratto-29-09.md`.

Stato: PG1, PG2, PG3 e PG4 completate, desktop 1440. Mobile non ancora disegnato.

## Decisioni prese con Giovane il 29/09

**Allineamento alle v2.** La PG è stata scritta prima di alcune decisioni del 20/09. I wireframe seguono le v2:

- nessun annullamento per mancata registrazione: K7 ha tre cause (recesso, inadempimento confermato, inefficacia), la riga «K1 → K7» della PG non è disegnata;
- nessun sollecito del venditore all'acquirente in K1;
- quattro condizioni sospensive con i nomi di T4 v2: mutuo, vendita dell'immobile dell'acquirente, acquisto congiunto di immobile e terreno agricolo, regolarità urbanistica e conformità catastale;
- in K1 due scadenze: pagamento entro 5 giorni dalla fattura, registrazione entro 30 giorni dall'ultima firma.

**Contenitore Contratto.** PG3 (Preparazione alla firma), PG4 (Pagamento registrazione) e la Finalizzazione stanno nella stessa tappa di percorso, Contratto. In spalla, sotto lo stepper di percorso, uno stepper «Contratto» a cinque passi: Persone e documenti · Contratto preliminare · Firme · Registrazione · Condizioni sospensive. Applicato anche a PG3 v2 e PG4 v2 in UI.

**K1 non si ridisegna.** Rimanda a R0, R1, R2, R4 della PG4 v2, presi in prestito per dare contesto a K2–K7.

**R3 diventa K3.0**, il primo stato della pagina contratto: la registrazione chiude la PG4 e apre la pagina contratto. Senza sospensive il primo stato è K2 con la stessa card in cima.

**Badge di K2: «Efficace».** La PG diceva «Attivo», uguale a K3.

## PG1 · Pagina contratto (n), desktop 1440

| Frame | Node | Vista | Cosa mostra |
|---|---|---|---|
| 0 · Legenda, fonti e punti aperti | `4705:171331` | — | Fonti, allineamento v2, convenzioni, discrepanze D1–D11, punti aperti 30, 35, 38, 36 |
| K1 · rimando a PG4 v2 | `4712:188023` | — | Link a R0 `4456:181272`, R1 `4456:179599`, R2 `4456:179718`, R4 `4456:179940`; spalla al passo 4 di 5 |
| K2 · Efficace, nessuna condizione | `4705:171881` | Venditore | Contratto già efficace, provvigione del venditore da pagare, stato delle due parti |
| K3 · Attivo, condizioni da avverare | `4705:171374` | Venditore | Pagina completa: prossima scadenza, quattro condizioni con owner e azioni, quanto costa uscire, documenti, cosa succede adesso, uscite |
| K4 · Condizione in scadenza | `4705:171588` | Acquirente, proprietaria | Avviso a 30 giorni promosso, due stati alternativi: giorno della scadenza, scadenza superata con finestra (DA VALIDARE) |
| K5 · Efficace | `4705:171975` | Acquirente | Tutte le condizioni avverate, rimando alla Conclusione (PG 4) |
| K6 · Sospeso, mediazione in corso | `4705:172091` | Venditore | Avanzamento della mediazione, scadenze congelate, stati alternativi SLA superato e azione giudiziaria |
| K7 · Annullato | `4705:172230` | Acquirente | Inefficacia a costo zero, documenti, stati alternativi recesso con multa da ricevere e inadempimento confermato |
| Gestione contratti · Listing | `4705:172354` | Venditore | Card con prossima scadenza, chiusi e annullati, empty state, regola del contratto unico |
| K3.0 · Appena registrato (ex R3) | `4712:215555` | Acquirente | Card «Il contratto è registrato» con data certa e download, prossima scadenza, condizioni; riquadro con la mappa dei contenuti di R3 |

Stepper «Contratto» per stato: K2 e K5 cinque passi completati; K3.0, K3 e K4 passo 5 attivo; K6, K7 e il recesso in corso passo 5 fermo, lo stepper non avanza; nella Conclusione «Contratto · completato».

K3.0, K4, K2, K5, K6 disegnano il delta rispetto a K3; le sezioni invariate o assenti sono dichiarate in un riquadro tratteggiato.

Dati del caso: Marco Ferrero (venditore), Giulia Rossi (acquirente), trilocale in Via Roma 12, Cuneo, 270.000 €. Ultima firma 26/09/2026, registrato il 20/10/2026. Multa penitenziale e clausola penale 13.500 €, quota del 3% 8.100 €, provvigione venditore 2.700 €, provvigione acquirente 5.400 €.

## Dove vanno i contenuti di R3

- «Il contratto è registrato», data certa, protocollo: prima card di K3.0.
- Download del contratto registrato e della ricevuta: prima card, poi «I documenti di questo contratto».
- Condizioni sospensive con scadenza e chi comunica: blocco delle condizioni.
- «La tua provvigione» e quando è dovuta: «Cosa succede adesso»; il pagamento resta alla Conclusione o in K2.
- Notaio e «Carica i documenti per il rogito» (CTA primaria di R3): **da decidere**. La PG Finalizzazione (ipotesi 33) li mette nella Conclusione, dopo l'efficacia; la Conclusione è disegnata così (PG4). In K3.0 non compaiono.

## PG2 · Comunicazione dell'esito di una condizione sospensiva, desktop 1440

Righe sotto la PG1 nella stessa sezione. Le modali seguono il pattern delle modali della Trattativa: frame 1440 con la pagina sotto oscurata, modale da 600, stati alternativi tratteggiati sotto la modale.

| Frame | Node | Vista | Cosa mostra |
|---|---|---|---|
| 0 · Legenda PG2 | `4734:215724` | — | Fonti, allineamento (come PG1), dati del caso, discrepanze D12–D16 e D1, punti aperti 30, 31, 35 |
| M1 · Comunica l'esito, condizione e bivio | `4734:215762` | Acquirente | Testo concordato in cima, «Si è avverata» primaria e «Non si avvererà» secondaria con la conseguenza sotto, uscita «Non so ancora»; popover dell'help |
| M2 · Ramo «Si è avverata» | `4734:215802` | Acquirente | Documento, data, anteprima, CTA; stati documento mancante, errori di caricamento, data non valida, testo del campo per le quattro condizioni |
| M3 · Dopo la dichiarazione di avveramento | `4734:215903` | Entrambe | Toast, riga aggiornata con «Correggi la dichiarazione» entro 48 ore, notifica alla controparte, storico aperto, modale «Tutte le condizioni sono avverate» se era l'ultima |
| M4 · Ramo «Non si avvererà» | `4734:215980` | Acquirente, mutuo | Conseguenza in cima, costo zero, motivazione da lista; stati rinuncia (causa imputabile, penale), proroga suggerita, motivazione mancante, documenti e motivazioni delle altre condizioni |
| M5 · Autocertificazione e firma FEA | `4734:216078` | Acquirente | Anteprima del documento, «Questa azione è definitiva», firma su Youtrust; stati firma in corso, firma non completata, documento non generato |
| M6 · Esito dell'inefficacia | `4734:216160` | Entrambe | Modale «Il contratto è sciolto» per chi dichiara; notifica e primo blocco di K7 per la controparte, con autocertificazione scaricabile |
| M7 · Proponi una nuova scadenza | `4734:216202` | Acquirente | Nuova data con suggerimento a +60 giorni e vincolo sul rogito, motivo facoltativo, anteprima; stati data non valida, proroga già chiesta, a scadenza superata, riga «Proroga richiesta» |
| M8 · Proroga, risposta della controparte | `4734:216284` | Venditore | Richiesta con nota, «Accetta la nuova scadenza» o «Mantieni la scadenza attuale» senza controproposta; riga d'ingresso, esiti accettata e mantenuta |
| M9 · La finestra dopo la scadenza | `4734:216347` | Entrambe | Riga «Scaduta», avvisi per chi ha la condizione e per chi aspetta, promemoria ogni 48 ore, email di sollecito, chiusura della finestra con la strada verso la segnalazione |

Dati del caso aggiunti: rogito entro il 31/03/2027; oggi nel caso 15/11/2026 (K4 sul mutuo); proroga richiesta al 13/02/2027.

### Scelte di struttura della PG2

- Il bivio precede i campi e i due rami hanno forma diversa: il ramo avverata è una riga di modulo, il ramo non avverata apre con la conseguenza e chiude con una firma.
- La vista della controparte è disegnata per ogni esito (M3, M6, M8, M9): chi riceve la notizia non ha agito e ha bisogno dell'evidenza.
- La risposta alla proroga è l'unico caso in cui la controparte agisce su una condizione non sua: la riga di Marco porta «Rispondi alla richiesta».
- Due aggiunte rispetto alla PG, segnalate sui nodi: in M4 il suggerimento di proroga quando la motivazione è «la pratica non si conclude entro la scadenza»; in M7 la riga «Finché non risponde vale il [data]» nell'anteprima.

## PG3 · Uscita dal contratto: recesso e inadempimento, desktop 1440

Righe sotto la PG2 nella stessa sezione. R0 e I0 sono modali (frame con due modali affiancate); gli stati successivi sono stati della pagina contratto, con il blocco «Il percorso» che elenca i passaggi, chi li fa e il loro stato per le due parti e per Cleclà. Dove servono le due viste, il frame le affianca e disegna solo il blocco principale.

| Frame | Node | Vista | Cosa mostra |
|---|---|---|---|
| 0 · Legenda PG3 | `4851:13400` | — | Fonti, dati del caso, convenzioni, discrepanze D17–D24, punti aperti 27, 34, 36, 41, 42 |
| Recesso · R0a, passaggi 1 e 2 | `4851:13441` | Venditore | Cosa stai per fare con il gradino di dialogo, motivazione da lista; stati «Altro» e popover recesso contro inadempimento |
| Recesso · R0b, passaggi 3 e 4 | `4851:13521` | Venditore | Tre voci di costo con destinatario, totale 22.221 €, «Se aspetti», conferma a tre livelli; varianti senza condizioni pendenti (niente 3%), popover multa, contratto sospeso |
| Recesso · R1–R2 | `4851:13611` | Venditore | Pagina con badge «Recesso in corso», pagamento della registrazione (621 €), riga DA DECIDERE sul 3%, «Ritira la richiesta», percorso a sette passaggi; stati R1, bonifico, vista di Giulia |
| Recesso · R3 | `4851:13828` | Venditore | Documento di recesso da rileggere, conseguenza, firma FEQ su Youtrust; stati firma in corso, firma non completata, dopo la firma |
| Recesso · R4 | `4851:14060` | Acquirente | Recesso ricevuto con documento, IBAN e intestatario per la multa; stati IBAN non valido, conto di terzi, vista di Marco |
| Recesso · R5 | `4851:14266` | Entrambe | Coordinate e ricevuta per chi paga; attesa, modifica IBAN e conferma di ricezione per chi riceve; stato «non hai ancora ricevuto» |
| Recesso · R6 e chiusura | `4851:14351` | Entrambe | Registrazione a cura del team, K7 per recesso con documenti e «Cosa puoi fare adesso»; proposta sull'annuncio del venditore che recede (D23), SLA superato |
| Inadempimento · I0 | `4851:14469` | Venditore | Tre passaggi: cosa stai per fare, cosa non è stato rispettato, cosa comporta con anteprima; stati «Altro», finestra ancora aperta, documento non generato |
| Inadempimento · I1–I2 | `4851:14583` | Entrambe | Segnalazione inviata e ricevuta, mediazione da accettare con il suo perimetro; stati «uno ha accettato», I2b rifiutata, popover |
| Inadempimento · I3–I4 | `4851:14699` | Entrambe | Cosa si congela e aggiornamento datato del team; I4 accordo che fa riprendere il contratto con le due firme; I4b accordo che lo scioglie |
| Inadempimento · I5–I7 | `4851:14763` | Entrambe | Azione giudiziaria fuori da Cleclà; I6 penale confermata; I7 smentito con il contratto che riprende (punto 42) |
| Chiusura comune | `4851:14826` | Entrambe | Percorso di chiusura, registrazione della risoluzione con le due formule DA VALIDARE, firma dell'accordo di risoluzione, K7 per inadempimento; stato K7 con pagamento aperto (D24) |

Dati del caso: recesso chiesto da Marco il 10/12/2026 con mutuo e regolarità ancora da avverare; multa 13.500 €, 3% a Cleclà 8.100 €, registrazione del recesso 621 € (200 + 16 + 3% di 13.500), totale 22.221 €. Inadempimento segnalato da Marco il 20/12/2026 sul mutuo scaduto; penale 13.500 €, registrazione della risoluzione 621 €.

### Scelte di struttura della PG3

- Le tre voci di costo del recesso restano separate con il loro destinatario, il totale è scritto grande una volta, e il confronto con l'attesa sta prima della conferma.
- L'IBAN lo inserisce chi riceve (punto 41) e si può modificare finché chi paga non carica la ricevuta (aggiunta).
- «Cosa si congela» si dichiara già prima dell'invio della segnalazione e a chi la riceve, perché la sospensione dipende dalla segnalazione e non dalla mediazione (aggiunta, DA VALIDARE).
- I7 è disegnato con il contratto che riprende, come la PG; il punto 42 resta aperto.
- Aggiunte rispetto alla PG, segnalate sui nodi: «Ritira la richiesta di recesso» in R1–R2, modifica dell'IBAN in R5, proposta sull'annuncio del venditore che recede in R6.

## PG4 · Conclusione del contratto, desktop 1440

Righe sotto la PG3 nella stessa sezione. C1 è la pagina completa; gli altri frame disegnano un delta o un blocco con i suoi stati.

| Frame | Node | Vista | Cosa mostra |
|---|---|---|---|
| 0 · Legenda PG4 | `4851:14988` | — | Fonti, dati del caso, discrepanze D25–D30, punti aperti 33, 34, 37, 40 |
| C1 · Pagina completa | `4851:15027` | Acquirente | Titolo «Contratto efficace», «A che punto siamo» a quattro passi, traguardo con condizioni e date, provvigione 5.400 € + IVA, documenti per il notaio (8 di 15), controllo finale, notaio, contatti bloccati, supporto |
| C2 · Delta Venditore | `4851:15252` | Venditore | Provvigione 2.700 € + IVA, annuncio chiuso, profilo immobile archiviato «impegnato, rogito da fare», punto 34, «e se il rogito non si fa» DA VALIDARE |
| C3 · Provvigione | `4851:15402` | Acquirente | Bonifico con quietanza, pagamento in verifica, pagata con fattura, carta rifiutata, reminder, scadenza superata, altra parte che ha pagato (senza importo), help |
| C4 · Documenti e controllo finale | `4851:15510` | Acquirente | I quattro gruppi aperti con i tre stati per riga e i link agli archivi; verifica in corso, esito per documento, alert su documento obsoleto, «Documentazione validata» in pagina e in bacheca, SLA superato |
| C5 · Contatti e notaio | `4851:15724` | Acquirente | Contatto di Marco sbloccato, mail di recap, variante con attesa dell'altra parte (punto 37); scorciatoia verso Trova tecnico con notai e città |
| C6 · Apertura senza condizioni | `4851:15791` | Acquirente | Pagina aperta da K2: efficace dalla registrazione, provvigione già pagata, passo attivo «Documenti per il notaio» |

Dati del caso: efficace dal 12/01/2027, rogito entro il 31/03/2027. Giulia nubile, c'è un terreno agricolo (compare il CDU): 15 righe pertinenti su 19. In C6 contratto senza condizioni, efficace dal 20/10/2026, rogito entro il 31/01/2027.

### Scelte di struttura della PG4

- La pagina è un passaggio di consegne: traguardo, provvigione, documenti, controllo, notaio, contatti. Il rogito compare come quarto passo tratteggiato, fuori da Cleclà.
- Ciascuna parte vede la propria provvigione; dell'altra parte solo lo stato, senza importo (D26).
- I contatti si sbloccano dopo il pagamento della propria provvigione (D27, punto 37).
- La checklist conta come pronte solo le righe già in piattaforma; le tre righe a carico di Cleclà diventano pronte con il pagamento della provvigione.
- La scorciatoia al notaio non nomina Cuneo; ogni notaio porta la città in cui lavora (feedback cliente 20/09 su R3).
- «Tocca a voi due» della PG non è usato: vale «Tocca a entrambi» (D28).

## Discrepanze

Aperte:

- D1 · La PG rimanda al blocco «Se qualcosa va storto» della Guida alla trattativa, rimosso il 20/09: i link e gli helper puntano alla guida del contratto preliminare.
- D2 · «né penali, né rimborsi» (PG) contro «né provvigione, né penali, né rimborsi» (Guida alla trattativa). Applicata la seconda anche in PG2 (M4, M6).
- D3 · «Identità verificata» contro «Utente verificato» (glossario).
- D5 · «Vedi il riepilogo della trattativa» contro «Riepilogo degli accordi». In UI PG3 chiuso il 29/09 («Vedi il riepilogo degli accordi» solo in F1 e F1b).
- D6 · La PG dice Sprint 4, Figma Sprint 5.
- D7 · Owner della prelazione: la PG dice acquirente o venditore, la regola del cliente del 20/09 la dà al venditore. Vale anche in PG2.
- D8 · Importi di multa, penale e quota del 3% DA VALIDARE (punti 26, 27, 38). In PG2 la penale compare nell'avviso di causa imputabile (M4); in PG3 in tutti i passaggi di pagamento.
- D11 · Notaio e documenti per il rogito: subito alla registrazione (R3 v2) o alla Conclusione (PG, ipotesi 33).
- D12 · Promemoria nella finestra ogni 48 ore (PG) contro 4 giorni per il silenzio in trattativa (glossario I44).
- D13 · Finestra di correzione di 48 ore sulla dichiarazione di avveramento: proposta della PG, DA VALIDARE.
- D14 · Una sola proroga per condizione: limite di design della PG, DA VALIDARE.
- D15 · Motivazioni del mancato avveramento: quali cadono dal lato dell'inadempimento («rinuncia alla richiesta», «rinuncia a vendere»). La lista della vendita è adattata perché la PG la condivideva con la condizione del venditore uscita in T4 v2.
- D16 · Documento di mancato avveramento per l'acquisto congiunto di immobile e terreno agricolo: comunicazione di esercizio della prelazione, testo di lavoro.
- D17 · Il 3% a Cleclà sul recesso non ha un passaggio di pagamento: la PG lo mette fra i costi di R0, nessuno stato R1–R6 e nessun nodo della board lo incassa.
- D18 · Termine per recedere: il template del contratto lo fissa 30 giorni prima del rogito, board e PG dicono «in qualsiasi momento». Manca lo stato dopo il termine.
- D19 · Punto di non ritorno: la PG lo mette al pagamento della registrazione, l'atto che annulla è la firma FEQ (R3).
- D20 · Badge durante il recesso: «Recesso in corso» proposto, i sei badge della PG1 non lo coprono.
- D21 · Nomi R0–R4 uguali a quelli della PG4 v2: frame con prefisso «Recesso ·» e «Inadempimento ·».
- D22 · Cleclà presentata come parte che media (PG, contratto art. 6) contro il glossario §15.7.
- D23 · Riattivazione automatica dell'annuncio quando recede il venditore: proposta alternativa disegnata in R6.
- D24 · K7 con un pagamento aperto: nella sequenza del flow non si verifica.
- D25 · Documenti per il rogito: checklist delle 19 voci nella Conclusione (PG, ipotesi 33) contro la richiesta del cliente del 20/09 su R3 di un rimando alla cartella dell'archivio.
- D26 · Provvigione dell'altra parte: la PG ne mostra lo stato, il cliente ha chiesto che ciascuna parte veda solo la propria. Disegnato lo stato senza importo.
- D27 · Quando arrivano i contatti: la PG1 li lega al pagamento della provvigione, la PG4 li mostra senza condizioni. Disegnati bloccati fino al pagamento della propria.
- D28 · «Tocca a voi due» (PG) ha lo stesso senso di «Tocca a entrambi»: usato il secondo.
- D29 · «Documentazione validata» (PG, MVP 35) contro «Documentazione verificata» (glossario, annuncio).
- D30 · Chi porta i documenti al notaio: copy approvato «Il notaio riceverà tutta la documentazione necessaria» e «Il nostro lavoro finisce solo dopo il rogito» contro la PG («la lista è da portare», «da qui in avanti vi coordinate voi due»).

Chiuse il 29/09: D4 (stepper, con il contenitore Contratto; resta I10 sul numero delle tappe di percorso), D9 (K1 rimanda a PG4 v2), D10 (badge di K2 «Efficace»).

Altre note agganciate ai nodi: SLA della mediazione («entro 3 giorni lavorativi») è un segnaposto; lo stato di riga «Sospesa» in K6 non è fra quelli della PG; quando si chiude la card «Il contratto è registrato» in K3.0 è DA VALIDARE; in M6 da decidere se alla controparte va offerta la strada della segnalazione; in M9 da decidere se la proroga resta proponibile dopo la chiusura della finestra.

## Punti aperti della PG

- 30 · Soglia della finestra fra scadenza superata e inadempimento. In PG2 la data è in segnaposto [GG/MM].
- 31 · Chi può dichiarare il mancato avveramento. In PG2 solo chi ha la condizione in carico.
- 35 · Per quali condizioni il documento allegato è obbligatorio. In PG2 obbligatorio per tutte, con l'etichetta DA VALIDARE.
- 38 · La Guida alla trattativa non nomina la quota del 3% a Cleclà.
- 27 · Base della quota proporzionale della registrazione: letta come 3% della multa o della penale.
- 34 · Notifica alle controparti delle trattative riattivate o chiuse: non disegnata.
- 36 · La registrazione del recesso la paga chi recede: ipotesi di lavoro.
- 41 · IBAN su chi riceve, al contrario della board.
- 42 · Inadempimento smentito: disegnato con il contratto che riprende.
- 33 · La lista dei documenti del rogito vive nella Conclusione: ipotesi di lavoro, in tensione con D25.
- 37 · Dipendenza fra i pagamenti della provvigione delle due parti.
- 40 · L'Archivio personale non ha le righe per i documenti personali del rogito.
- Altri DA VALIDARE della PG3: SLA del team, scadenza dei pagamenti, cosa succede se la multa non viene pagata, cosa distingue le due formule di registrazione dell'inadempimento, chi paga la registrazione della risoluzione in mediazione, se le scadenze corrono durante il recesso.
- Altri DA VALIDARE della PG4: termine di pagamento della provvigione, risposta a «Cosa succede se non pago?», IVA, chi paga il notaio, etichetta «impegnato, rogito da fare», cosa succede se il rogito non si fa.

## Nota operativa

I frame sono costruiti con Auto Layout e helper definiti su `globalThis.WF` nella sessione del plugin (compresi `WF.contractStepper`, `WF.modal`, `WF.field`, `WF.upload`, `WF.radio`, `WF.altCard`, `WF.screen2`, `WF.percorso`, `WF.twoViews`, `WF.modalPair`, `WF.mbox`, `WF.costRow`, `WF.conclScreen`): non persistono dopo il riavvio del plugin. Annotazioni native visibili in Dev Mode (Shift+D): 28 sui frame della PG2, 36 sui frame della PG3, 18 sui frame della PG4.
