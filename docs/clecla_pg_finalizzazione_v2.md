# Cleclà — Priority guides · Fase Finalizzazione (Sprint 4)

> Perimetro: le quattro pagine di Sprint 4 che il foglio Pagine elenca dopo la registrazione del preliminare
> (Pagina contratti attivi, Pagina contratto annullato, Conclusione contratto, Gestione contratti), riorganizzate
> in **4 priority guide** con stati, modali e percorsi multi-passaggio. Restano fuori: il contratto preliminare in
> versione interattiva (lettura assistita, glossario contestuale), la riapertura della trattativa prima della
> firma, il rogito, che avviene fuori dalla piattaforma.
>
> Formato delle righe identico al foglio Contenuti. Sulle righe di campo la colonna Note usa la legenda già in
> uso: **Compila** (chi inserisce) · **Obbl.** (quando diventa bloccante) · **Precompilato** (da dove arriva il
> valore) · **Serve a** (uso a valle). Le righe che poggiano su un'ipotesi di lavoro sono marcate
> **DA VALIDARE**.
>
> Fonti: `MVP Functional Requirements` righe 7, 8, 17, 34–39 · `claude/user-flow-finalizzazione.md` ·
> `20260127_Cleclà_Contenuti`, fogli Pagine (righe 21, 22, 31, 32, 34–36, 40–45), Priority guides (righe 314–330)
> e Struttura backoffice (righe 49–54) · `claude/clecla_pg_trattativa.md` per la continuità · `archivio-documentazione-decisioni.md` ·
> `trova-tecnico-decisioni.md` · `/clecla-interaction-model`.
>
> La numerazione dei punti aperti continua da quella della PG Trattativa, che si è fermata a 25.

## Indice

Le quattro priority guide stanno a metà documento: **PG 1 — Pagina contratto (n)** · **PG 2 — Comunicazione
dell'esito di una condizione sospensiva** · **PG 3 — Uscita dal contratto: recesso e inadempimento** ·
**PG 4 — Conclusione del contratto**. Prima vengono le user story recuperate, il confronto con lo user flow e le
contraddizioni sciolte, che spiegano perché le PG sono queste. Dopo, i punti ancora aperti.

## Sintesi

La fase è coperta da sei righe dell'MVP che descrivono eventi isolati, mentre lo user flow la organizza in un
percorso principale più cinque rami. Le due fonti concordano sull'ossatura e divergono su tre cose sostanziali:
la caparra confirmatoria (che l'MVP usa ancora come meccanismo dell'inadempimento e che è uscita dal modello),
l'automatismo della registrazione all'Agenzia delle Entrate (manuale nei requisiti definitivi, automatico nelle
use case). La terza divergenza è fra il flow e questo documento: il flow chiama il traguardo finale
«compravendita avvenuta», quando la compravendita avviene dal notaio, mesi dopo. Servono **quattro priority guide** e **nessuna pagina nuova** oltre a quelle già
elencate nel foglio Pagine, per **203 righe di contenuto**: 56 nella PG 1, 38 nella PG 2, 62 nella PG 3, 47 nella PG 4.


## Aggiornamento del 25/09 · check sulla knowledge base

Il controllo incrociato sulla KB di progetto scioglie tre punti (26, 28, 32), riformula il 27 in modo che cambia
le cifre della PG 3 e corrobora in parte il 29. Due ipotesi di lavoro prese nella stessa giornata
chiudono il **36** (la registrazione del recesso la paga chi recede) e il **33** (la lista dei documenti per il
rogito vive nella Conclusione contratto): sono decisioni per procedere, da validare col team, e con quelle non
resta niente che blocchi la scrittura. Le fonti citate qui sotto
(`overview.md`, `delta-guide-trattativa-14-09.md`, `ui-contratto-lettore-guida.md`,
`ui-pg4-pagamento-registrazione.md`) non sono leggibili da questa sessione: le riporto come me le ha passate il
check, senza averle verificate io.

**Terminologia allineata a «inadempimento».** La terminologia bloccata in `overview.md` usa «inadempimento» e mai
«inadempienza», decisione presa dopo il glossario, che registrava le due forme come entrambe in uso. Il documento
adotta «inadempimento» in tutta la sua prosa. Le due fonti che dicono «inadempienza» restano citate con le loro
parole: la board dello user flow (ramo C) e il foglio Struttura backoffice, che etichetta la CTA del team
«attiva flusso di inadempienza». Entrambe le etichette vanno riscritte quando si toccano quei documenti.

---

## 1. Le user story della fase

Sei righe dell'MVP cadono dentro la Finalizzazione, più tre che la fase riusa dalle epiche precedenti.

| Riga | Nome | Target MVP | Cosa chiede | Ramo dello user flow |
|---|---|---|---|---|
| 34 | Registrazione contratto preliminare sul portale AdE | Both | Registrazione guidata, conferma via email, ricevuta scaricabile | A.7 |
| 35 | Controllo documentazione | Both | Check finale prima del notaio, stato per documento (ok / mancante / non leggibile), alert su file obsoleti, badge «Documentazione validata» in bacheca | Assente dal flow |
| 36 | Comunicazione avveramento / non avveramento condizione sospensiva | Both | Selezione condizione, dichiarazione avverata o non avverata, upload documento, riepilogo storico, notifica controparte, avanzamento o blocco automatico, rimando a «trova notai» | E.1 ed E.2 |
| 37 | Annullamento contratto preliminare | Both | Avviso all'avvicinarsi della scadenza e il giorno stesso, richiesta di annullamento con motivazione da lista, firma digitale del modulo, conferma della controparte, generazione dei documenti di recesso e inadempimento, archivio e download | B, C, D parzialmente |
| 38 | Checkout e pagamenti | Both | Fee Cleclà al 100% all'avveramento delle sospensive, registrazione AdE alla firma, carta o bonifico con quietanza | A.3, C.2, F.3 |
| 39 | Assistenza clienti real-time | Both | Chat in tutte le aree, FAQ suggerite, escalation a persona | Trasversale |

Le tre righe riusate: la **7** (checklist documenti) porta le due liste che servono qui, «documenti Notaio»
a 19 voci e «checklist pagamenti» a 8 voci; la **8** (trova tecnici) contiene il notaio tra i professionisti e
«rogito di compravendita» tra i filtri documento; la **17** (notifiche) elenca già i tre avvisi della fase,
reminder pagamento provvigione, reminder pagamento registrazione e aggiornamenti sullo stato delle fasi condivise.

La riga **32** (richiesta di riapertura trattativa) resta fuori: il pulsante è attivo solo prima della firma,
quindi appartiene all'epica precedente.

### Le user story, per come sono scritte

Le quattro righe con una user story esplicita dicono tutte la stessa cosa in forme diverse, e vale la pena
notarlo perché orienta il tono di tutta la fase.

- Riga 34, venditore: «voglio che il contratto preliminare venga registrato all'Agenzia delle Entrate in modo
  guidato, così da evitare errori o dimenticanze». Acquirente: «voglio assicurarmi che venga registrato
  correttamente, così da tutelarmi legalmente».
- Riga 35, venditore: «voglio che i documenti richiesti siano verificati automaticamente o da un operatore, così
  da sapere se è tutto corretto prima della stipula». Acquirente: «voglio essere certo che la documentazione
  dell'immobile sia completa e verificata, così da procedere senza rischi».
- Riga 36, venditore: «voglio sapere se l'acquirente ha rispettato la condizione sospensiva, così da sapere se
  procedere o rimettere l'immobile sul mercato». Acquirente: «voglio comunicare facilmente se la condizione è
  stata rispettata, così da evitare fraintendimenti».
- Riga 37, entrambi: «voglio ricevere una comunicazione allo scadere del contratto preliminare, per potermi
  muovere di conseguenza».

Il movente ricorrente è la **verifica**: sapere che una cosa è stata fatta bene e poterlo dimostrare. Nella
Trattativa il movente era la diffidenza verso la controparte («per evitare fregature»). Qui lo spostamento è
verso la diffidenza verso il processo, che è un problema di design diverso: la risposta sono evidenze
scaricabili, date certe e stati leggibili.

---

## 2. Il confronto con lo user flow

### Dove le due fonti concordano

Sull'ossatura, in modo verificabile riga per riga. Il pagamento della registrazione entro 30 giorni a carico
dell'acquirente (MVP 38, flow A.3), la registrazione manuale fatta dal team (MVP 34 requisiti definitivi, flow
A.7, backoffice righe 49–50), la comunicazione dell'esito delle sospensive con upload del documento e notifica
alla controparte (MVP 36, flow E.1), la generazione automatica dei documenti di recesso e inadempimento (MVP 37,
flow B.7 e C.3), l'archiviazione del contratto annullato (MVP 37, flow B.15 e C.2.10), il rimando a «trova notai»
(MVP 36 outcome, flow F.6), il pagamento della fee all'avveramento delle sospensive (MVP 38, flow F.2–F.3).

La **Struttura backoffice** conferma il flow con più precisione dell'MVP. La riga 52 elenca esattamente le
azioni del team sulla pagina contratti attivi: «attiva flusso di inadempienza» solo su richiesta ricevuta,
conferma accordo raggiunto con caricamento dell'accordo, «conferma inadempienza SI/NO», selezione della parte
inadempiente con avvio del flusso di pagamento, generazione dell'accordo di risoluzione, attiva flusso di
recesso solo su richiesta ricevuta, conferma della registrazione del recesso con caricamento della ricevuta.

### Cosa il flow aggiunge

Quattro cose che nell'MVP non esistono.

**La proroga della scadenza (ramo D).** Nessuna riga dell'MVP la prevede. Il flow la aggancia alla notifica a 30
giorni: l'utente decide se prorogare o mantenere, la controparte accetta o rifiuta, e in caso di accettazione il
sistema aggiorna le scadenze sul contratto. È l'unica interazione della fase in cui le due parti negoziano
ancora, quindi è anche l'unica che riapre un pezzo di logica della Trattativa dentro il Contratto.

**La mediazione di Cleclà nell'inadempimento (ramo C.1).** Il flow ha un bivio «Richiedi mediazione di Cleclà?»
che, se entrambe accettano, porta il contratto in stand-by e apre una gestione a cura del team, con tre esiti:
accordo che riattiva il contratto (caricamento e firma FEQ, ramo «SI, continua»), accordo che lo risolve con il
pagamento della penale (ramo «SI, risolvi», che salta direttamente alla chiusura) e azione giudiziaria, con
archiviazione della sentenza e conferma o smentita dell'inadempimento. L'MVP si ferma alla generazione del
documento.

**La registrazione del recesso e della risoluzione su AdE** (B.14, C.2.9), con un secondo pagamento di
registrazione. L'MVP non lo prevede, e il flow non dice chi lo paga: che lo paghi chi esce dal contratto è
l'ipotesi di lavoro del 25/09 sul punto 36.

**Lo scambio dei contatti diretti** (F.4). Al traguardo finale il sistema manda a ciascuna parte una mail di
recap con il contatto diretto dell'altra. È il momento in cui Cleclà esce di scena e le due persone proseguono
da sole verso il notaio. Nella Trattativa il contatto diretto era deliberatamente assente, quindi qui si apre un
regime nuovo che va progettato come tale.

### Cosa l'MVP ha e il flow non mostra

**Il controllo finale della documentazione (riga 35).** «La documentazione fornita viene controllata un'ultima
volta prima di poter essere utilizzata autonomamente dagli utenti o di essere portata dal notaio per la firma
del contratto effettivo.» Il flow non ha questo step, però la riga 7 porta la lista: 19 voci nella checklist
Notaio, contro le 7 del contratto preliminare. Fra il preliminare efficace e il rogito c'è quindi il pezzo di
raccolta documentale più grosso di tutto il percorso, e sul flow non compare.

**Gli avvisi di scadenza (riga 37).** Il flow ha la notifica a 30 giorni come innesco del ramo D. L'MVP ne chiede
due: all'avvicinarsi del termine e il giorno della scadenza. La seconda è quella che conta, perché è il momento
in cui il contratto cambia stato da sé.

**Il badge «Documentazione validata» in bacheca** per entrambi i profili (riga 35, use case).

**Lo storico dei pagamenti.** Le pagine «Stato pagamenti» esistono per i due ruoli (foglio Pagine, righe 22 e 32)
e in questa fase si riempiono: registrazione, fee, eventuali penali. Il flow non le tocca.

### Le contraddizioni da sciogliere

**26. La caparra confirmatoria è ancora dentro l'MVP.** La riga 37 descrive il meccanismo per esteso: «inadempienza
→ si attiva il meccanismo della caparra confirmatoria (se causa è compratore per la caparra, se causa è il
venditore deve restituire la caparra più un ammontare uguale alla caparra)». La caparra è uscita dal modello
(punto 14 chiuso il 03/09) e il flow usa due strumenti diversi: **clausola penale** per l'inadempimento (C.1, C.2)
e **multa penitenziale** per il recesso (B.11). Il flow è la fonte aggiornata e la riga 37 dell'MVP va considerata
superata su questo punto.

**Chiuso dal check del 25/09.** L'importo della clausola penale non lo fissa nessuno caso per caso: è un valore
fisso del template di contratto, **5% del prezzo a carico della parte inadempiente**, richiamato all'art. 1382
c.c. (`delta-guide-trattativa-14-09.md`, confermato dai numeri del caso in `ui-contratto-lettore-guida.md`, dove
la penale del 5% su 270.000 € fa 13.500 €). La domanda «dove viene concordato» cade da sé: sta nel testo del
preliminare, che le parti firmano. Per il design questo cambia due cose. Primo, l'importo è **calcolabile e
mostrabile** in anteprima dentro la modale di segnalazione, e va mostrato. Secondo, la penale va dichiarata nella
PG 1 come clausola già in vigore, non come conseguenza che si scopre al momento dell'uscita.

**27. La base di calcolo della quota proporzionale, riformulata.** Gli importi «200 € + 16 € + 3% del 5% del
prezzo dell'immobile» compaiono identici nei rami Recesso e Inadempienza, e su un immobile da 200.000 € fanno
516 €, di cui 300 € di componente proporzionale. Avevo letto il 5% come residuo della caparra eliminata. Con il
dato del punto 26 la lettura cambia e diventa più semplice: **il 5% del prezzo è esattamente l'importo della
penale e della multa penitenziale**, e nella pratica italiana l'imposta di registro proporzionale si applica anche
a penali e multe, non solo a caparra e acconti. Il 3% sarebbe quindi calcolato sulla somma effettivamente dovuta
fra le parti, e la formula regge senza caparra. La coincidenza dei due 5% è troppo precisa per essere casuale,
però resta una mia lettura: va confermata dal cliente o dal notaio prima di scrivere gli importi in schermata,
perché è la cifra che l'utente paga. Il punto scende da bloccante a da confermare.

**28. La registrazione AdE è manuale o automatica.** La descrizione della riga 34 dice «automaticamente caricato
sul sito dell'Agenzia delle Entrate utilizzando i relativi API», i requisiti definitivi dicono «(manuale da parte
del Team Cleclà)» e le use case dei due ruoli parlano ancora di caricamento automatico. Il flow (A.7) e il
backoffice (righe 49–50, «Conferma registrazione contratto preliminare», «Caricamento ricevuta della
registrazione») dicono manuale. Il design segue il manuale, con SLA dichiarato e lo stesso comportamento a SLA
superato già fissato nelle altre pagine. Le due use case dell'MVP vanno corrette.

**Chiuso dal check del 25/09.** Manuale, su fonti indipendenti dal flow: `ui-pg4-pagamento-registrazione.md`
dichiara il terzo passo dello stepper come «lo facciamo noi» per il deposito all'Agenzia delle Entrate. Il design
può poggiare sul manuale senza riserve.

**29. «Compravendita avvenuta» non è la compravendita.** L'end point del flow (F.5) si chiama «Compravendita
avvenuta e next steps» e lo step successivo (F.6) è «Trova un notaio». Quello che avviene in quel punto è
l'efficacia del contratto preliminare, cioè l'avveramento di tutte le condizioni sospensive. La compravendita
avviene al rogito, davanti al notaio, fuori dalla piattaforma e mesi dopo. Un utente che legge «compravendita
avvenuta» e subito dopo «cerca un notaio» si ferma. **Posizione presa**: lo stato si chiama «Contratto efficace»
e il traguardo dice cosa manca ancora, cioè il rogito. Vale anche per la riga «Archiviazione profilo immobile
come venduto» (F.4): in quel momento l'immobile è impegnato, e lo stato «venduto» arriva dopo il rogito.

**Corroborato in parte dal check del 25/09.** `revisione-wireframe-sprint2.md` dice «annuncio venduto: non esiste,
l'immobile viene archiviato», quindi la metà della posizione che riguarda l'archiviazione ha una fonte. Il nome
dello stato «Contratto efficace» e l'etichetta «impegnato» restano una proposta di questo documento, coerente con
quella fonte e non certificata da essa.

**30. La condizione sospensiva scaduta senza esito porta direttamente all'inadempimento.** Lo dice la board:
lo stato «scaduta» è collegato all'ingresso del ramo C, «comunica sospetta inadempienza della controparte». È una
conseguenza pesante per un silenzio, e il silenzio in questa fase ha cause banali (la banca che risponde tardi,
una mail non letta). **Posizione presa**: fra la scadenza e l'inadempimento serve una finestra dichiarata, con
sollecito automatico a entrambe le parti e la possibilità di prorogare anche a scadenza superata se la controparte
è d'accordo. La soglia della finestra è da concordare.

**31. L'inefficacia è automatica e insieme richiede una segnalazione utente.** Nel flow E.2 il punto 6 è una user
action, «Segnala inefficacia contratto», e il punto 7 è una system decision, «Risoluzione automatica contratto».
Le due cose non stanno insieme come sono scritte. La lettura che regge: la dichiarazione di non avveramento,
accompagnata dall'autocertificazione firmata FEA, è l'atto dell'utente, e la risoluzione è la conseguenza
automatica di quell'atto. Va confermato, e va deciso se la segnalazione la può fare solo chi ha la condizione in
carico o entrambe le parti.

**32. Il flow è muto sull'owner dell'avveramento.** La board ripete la stessa sequenza sui due rail Venditore e
Acquirente, e la sua legenda avverte che i nodi duplicati sono lo stesso passaggio eseguito una volta per rail.
Resta quindi da stabilire chi può selezionare quale condizione, perché il flow non lo dice. Il foglio Condizioni ha una
colonna «Owner avveramento» e nella PG Trattativa le sospensive hanno un proprietario preciso. **Posizione presa**:
ciascuno comunica solo le proprie e vede lo stato di quelle dell'altro, come nella Trattativa vedeva solo le
condizioni che poteva proporre.

**Chiuso dal check del 25/09, con una correzione.** La tabella al punto 7 di «Come funziona la trattativa» mappa
gli owner e conferma l'assunzione, con uno scarto rispetto a come l'avevo scritta: mutuo e vendita di un immobile
proprio all'**Acquirente**, sanatoria e regolarità al **Venditore**, e la **prelazione a entrambi** (A.3 per
l'acquirente, V.3 per il venditore). Avevo assegnato la prelazione agraria al solo venditore. La riga della
prelazione nella PG 1 ha quindi due proprietari possibili, e l'interfaccia deve dire quale dei due la ha in carico
su quel contratto.

**33. Il contatore dei traguardi dell'Archivio è stato rimosso.** La PG Trattativa fa poggiare lo stato T5 sul
«traguardo per il preliminare» dell'Archivio documentazione e cita tre traguardi impilati (6 → 7 → 19 documenti).
Le decisioni del 18/08 sull'Archivio hanno però rimosso il pannello dei traguardi «A che punto sei», e la stessa
nota dice che l'Archivio non tiene i documenti del rogito: quelli compaiono come elenco informativo di nove voci
con accanto chi le rilascia. Il blocco documentale del rogito, che è il più grosso della fase, oggi non ha una
casa.

**Ipotesi di lavoro del 25/09: la lista vive nella Conclusione contratto.** Decisione presa per procedere, da
validare col team. Tre conseguenze, di cui una fuori da questo perimetro.

La prima: la Conclusione ospita la **checklist delle 19 voci** come blocco vero, con l'export in PDF che la riga 7
dell'MVP già prevede. La seconda: la checklist **legge dagli archivi esistenti** invece di aprire una terza
superficie di caricamento. Sei delle 19 voci sono già nell'Archivio dell'immobile (visura storica, planimetria,
APE, relazione tecnica o RRE, copia di provenienza, contratto preliminare) e si mostrano come disponibili con il
link al documento. Le voci personali (estratto per riassunto dell'atto di matrimonio, certificato di stato libero,
permesso di soggiorno, poteri di firma per società, certificato di morte per gli immobili da successione)
appartengono all'**Archivio documentazione personale**, che esiste già come pagina per i due ruoli. Le restanti
(certificato di destinazione urbanistica per i terreni, dichiarazione di inesistenza di arretrati condominiali,
mezzi di pagamento, dati del mediatore, fatture di provvigione) sono documenti che le parti portano al notaio o
che Cleclà emette, e la checklist dice chi li rilascia e come ottenerli.

La terza conseguenza sta fuori: l'Archivio dell'immobile tiene oggi un **elenco informativo di nove voci** sul
rogito. Con la lista completa nella Conclusione quelle nove voci diventano una duplicazione, e la regola
uno-e-solo-uno chiede di scegliere. La proposta: l'elenco nell'Archivio si riduce a un rimando («la lista completa
per il rogito è nella pagina del contratto, quando arriverete lì»), e la fonte canonica è la Conclusione. Va
applicato alla PG dell'Archivio, come vuole il workflow E: aggiungere un blocco implica alleggerirne un altro.

Resta da verificare che l'**Archivio personale abbia le righe** per i documenti personali del rogito. Nel foglio
Contenuti quella pagina ha due sole sezioni, ID personale e Privacy. **Punto aperto 40.**

---

## 3. La forma della fase

Lo user flow ha un percorso principale (A → F) e cinque rami. Due (Recesso, Inadempimento) la board etichetta
«può avvenire in qualsiasi momento del flusso»; gli altri tre (Proroga, Inefficacia, Avveramento) sono agganciati
al controllo sulle condizioni sospensive. Tradotto in schermate: **una pagina che regge il
contratto per tutta la sua vita**, con gli stati che cambiano sotto, più le uscite laterali sempre raggiungibili.

Questo è il punto di rottura rispetto alla Trattativa, che durava giorni. Il contratto attivo dura mesi, e per
buona parte di quei mesi l'utente non ha niente da fare: aspetta la banca, aspetta il comune, aspetta una data.
La pagina deve quindi funzionare bene soprattutto nello stato in cui non si tocca, e l'unità di misura
dell'esperienza diventa la **scadenza**, non l'azione.

### Mappa del perimetro

| Voce del foglio Pagine / elemento | Dove vive | PG |
|---|---|---|
| Pagina contratti attivi (con condizioni sospensive), riga 43 | Pagina contratto (n), stati K1–K7 | PG 1 |
| Lista condizioni sospensive, recap stato condizioni (righe 319–320) | Blocco «Le condizioni sospensive» | PG 1 |
| Gestione contratti, righe 21 e 31 | Listing dei contratti, variante per ruolo | PG 1, blocco finale |
| Comunicazione avveramento / non avveramento (MVP 36) | Modali dentro la pagina contratto | PG 2 |
| Proroga della scadenza (flow ramo D) | Modale dentro la pagina contratto | PG 2 |
| Pop-up recesso (riga 321) | Percorso di recesso, 6 passaggi | PG 3 |
| Pop-up inadempienza (riga 322) | Percorso di inadempimento, con e senza mediazione | PG 3 |
| Pagina contratto annullato, riga 44 | Stato K7 della pagina contratto + documenti allegati | PG 1 e PG 3 |
| Documento di recesso e di inadempimento allegati, richiesta di pagamento (righe 324–326) | Blocchi dello stato K7 | PG 3 |
| Conclusione contratto, riga 45 | Pagina dedicata | PG 4 |
| Pagamento fee venditore e acquirente, next steps, trova un notaio (righe 327–330) | Blocchi della Conclusione | PG 4 |
| Controllo finale della documentazione (MVP 35) | Blocco «Documenti per il rogito» | PG 4 |

Sequenza: **Pagamento registrazione** (ultima PG della Trattativa) → **Pagina contratto** (K1 → K5) →
**Conclusione contratto** → rogito, fuori piattaforma. Le uscite laterali (PG 3) staccano da K2, K3, K4 o K5 e
portano a K7. In K6 sono chiuse: finché la mediazione è aperta nessuno dei due può recedere.

---

## PG 1 — Pagina contratto (n)

**Job-to-be-done**: tenere due persone informate su un contratto che dura mesi e che per la maggior parte del
tempo non richiede niente, facendo capire in ogni momento quale scadenza sta arrivando, di chi è la prossima
mossa e cosa succede se quella mossa non arriva.

**Ruolo**: condivisa, varianti UI per ruolo · **Tappa**: Contratto (punto di convergenza) ·
**Unità atomiche**: Trattativa (il documento di puntuazione diventa contratto), Timing, Documenti.

**Posizione presa**: la pagina è un **calendario di impegni con evidenze allegate**, e la sua riga atomica è la
condizione sospensiva, con la sua scadenza, il suo proprietario e il suo esito. Questo continua il pattern della
riga di condizione già in piedi nella Trattativa: stesso componente, stato diverso. Lo storico della fase
precedente resta consultabile in sola lettura, così l'utente verifica cosa ha firmato senza uscire dalla pagina.

Le lettere degli stati partono da K perché T e F sono già usate dagli stati della Trattativa e della Preparazione
alla firma.

### Stati della pagina

| Pagina | Block | Type | Elemento | Target | Contenuto | Sprint | Note |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Pagina contratto (n) | Stati della pagina | STATUS | K1 — Firmato, registrazione da pagare | Both - logged | La pagina esiste e dichiara che il contratto è in stand-by finché l'acquirente non paga la registrazione | Sprint 4 | Ci si entra: ultima firma raccolta · Ha la palla: Acquirente · Si esce con: pagamento della registrazione, oppure con l'annullamento se i 30 giorni passano. Confine con la PG 4 della Trattativa, che contiene il pagamento. Qui la pagina c'è già, altrimenti il venditore dopo la firma non ha nessuna pagina da guardare. |
| Pagina contratto (n) | Stati della pagina | STATUS | K2 — Attivo, nessuna condizione sospensiva | Both - logged | Contratto attivo e già efficace. La fattura Cleclà è partita insieme alla registrazione | Sprint 4 | Ci si entra: registrazione pagata, zero sospensive · Ha la palla: entrambi, sul pagamento della fee · Si esce con: fee pagata → Conclusione contratto. Da flow A.2 → A.3: senza sospensive la fattura Cleclà parte subito. È l'unico stato in cui la pagina nasce già in arrivo. |
| Pagina contratto (n) | Stati della pagina | STATUS | K3 — Attivo, condizioni da avverare | Both - logged | Elenco delle sospensive con scadenza, proprietario ed esito. Nessuna azione dovuta finché una scadenza non si avvicina | Sprint 4 | Ci si entra: registrazione pagata, almeno una sospensiva · Ha la palla: chi ha in carico la prima scadenza · Si esce con: tutte le condizioni con esito positivo. Stato di lavoro della fase, e quello che dura più a lungo: mesi. |
| Pagina contratto (n) | Stati della pagina | STATUS | K4 — Condizione in scadenza | Both - logged | Variante di K3 con l'avviso in evidenza e le due azioni disponibili al proprietario | Sprint 4 | Ci si entra: 30 giorni dalla scadenza (flow D.1) · Ha la palla: il proprietario della condizione · Si esce con: esito comunicato o nuova scadenza accettata. Resta la stessa pagina, con il blocco scadenza promosso in cima. |
| Pagina contratto (n) | Stati della pagina | STATUS | K5 — Efficace | Both - logged | Tutte le sospensive avverate, con le date. Il contratto è efficace e si va al rogito | Sprint 4 | Ci si entra: ultima condizione avverata (flow E.1.5) · Ha la palla: entrambi · Si esce con: apertura della Conclusione contratto. Nome scelto contro «compravendita avvenuta» del flow: vedi punto 29. |
| Pagina contratto (n) | Stati della pagina | STATUS | K6 — Sospeso | Both - logged | Inadempimento segnalato, mediazione o azione giudiziaria in corso. Contratto sospeso, scadenze congelate | Sprint 4 | Ci si entra: attivazione del flusso di inadempimento da parte del team, con o senza mediazione (flow C.5 e C.1.7) · Ha la palla: Cleclà · Si esce con: accordo che riattiva il contratto (torna a K3), accordo che lo risolve o inadempimento confermato (va a K7), oppure inadempimento smentito (torna a K3). Copre gli stati da I2 a I5 della PG 3. Lo stato più delicato della fase: il contratto è fermo per un tempo che la piattaforma non controlla. |
| Pagina contratto (n) | Stati della pagina | STATUS | K7 — Annullato | Both - logged | Sola lettura, con causa, data, documenti allegati e l'eventuale pagamento ancora aperto | Sprint 4 | Ci si entra: recesso, inadempimento confermato, inefficacia, oppure mancata registrazione entro i 30 giorni · Ha la palla: chi deve un pagamento residuo, altrimenti nessuno · Si esce con: chiusura, annuncio e trattative riattivate. Contenuto in PG 3. |
| Pagina contratto (n) | Stati della pagina | STATUS | K1 → K7 per mancata registrazione | Both - logged | «Il contratto non è stato registrato entro i 30 giorni dalla firma e si è annullato.» | Sprint 4 | Quarta causa di annullamento, dalla PG 4 della Trattativa, punto 20 chiuso il 03/09: «il contratto si annulla se non viene registrato». È la conseguenza più pesante dell'epica precedente e la pagina che il venditore guarda mentre aspetta è questa, quindi lo stato vive qui. Il venditore può sollecitare l'acquirente ogni 48 ore, regola già fissata lì. |
| Pagina contratto (n) | Stati della pagina | STATUS | Badge stato contratto | Both - logged | In attesa di registrazione · Attivo · Condizione in scadenza · Efficace · Sospeso · Annullato | Sprint 4 | [K1–K7] Un solo badge alla volta, colore più label testuale, mai solo colore. Stessa regola del badge stato trattativa e del badge stato profilo immobile. |
| Pagina contratto (n) | Stati della pagina | CONTENT | «Pagina contratto annullato» diventa uno stato | Both - logged | — | Sprint 4 | Il foglio Pagine (riga 44) la tiene come pagina a sé. Diventa K7, per la ragione che ha portato T6 dentro la pagina trattativa: stesso contratto, stesso storico, stessi documenti. Un URL diverso fa perdere il filo di cosa si è firmato. **Riga del foglio Pagine da aggiornare.** |
| Pagina contratto (n) | Stati della pagina | CONTENT | Simmetria e asimmetria tra i ruoli | Both - logged | Stesso contratto, stesso elenco di condizioni, stesso storico e stessi stati per tutti e due. Cambiano: su quali condizioni si può agire, i testi degli avvisi, gli importi della fee | Sprint 4 | §4 dell'interaction model: nei punti di convergenza entrambe le parti vedono lo stesso stato e le azioni sono auditabili da entrambi. |

### Header e orientamento

| Pagina | Block | Type | Elemento | Target | Contenuto | Sprint | Note |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Pagina contratto (n) | Header | CONTENT | Titolo pagina | Both - logged | «Contratto · [Tipologia] in [Via], [Comune]» — es. «Contratto · Trilocale in Via Roma, Cuneo» | Sprint 4 | [K1–K7] Stessa formula del titolo della pagina trattativa e del profilo immobile. Con più contratti aperti è come l'utente riconosce quale sta guardando. |
| Pagina contratto (n) | Header | CONTENT | Le due parti | Both - logged | Nome e cognome, foto profilo, badge «Identità verificata», ruolo. La tua parte e l'altra, affiancate | Sprint 4 | [K1–K7] Stesso componente della pagina trattativa. Il contatto diretto non compare: si apre solo alla Conclusione (PG 4). |
| Pagina contratto (n) | Header | STATUS | Stepper percorso | Both - logged | V: Profilo immobile → Pubblicazione → Visite → Trattativa → **Contratto** · A: Ricerca → Visita → Trattativa → **Contratto** | Sprint 4 | [K1–K7] P3. «Sei qui: Contratto». Presidia l'anti-pattern «ruolo dichiarato ma tappa non visibile». |
| Pagina contratto (n) | Header | STATUS | Etichetta di responsabilità | Both - logged | «Tocca a te» (K4 se la condizione è tua) · «In attesa di [Nome]» (K3, K4 se la condizione è sua) · «Ci pensiamo noi» (K1 in lavorazione, K6) · «Tocca a entrambi» (K2, K5) | Sprint 4 | [K1–K7] Stesso componente delle altre pagine. È il primo elemento che l'utente cerca quando rientra dopo settimane. |
| Pagina contratto (n) | Header | STATUS | Progress delle condizioni | Both - logged | «2 condizioni su 4 avverate» + barra | Sprint 4 | [K3–K5] P3 sulla singola schermata. Il conteggio include solo le sospensive concordate in trattativa. In K2 il blocco non compare. |
| Pagina contratto (n) | Header | ACTION | Scarica il contratto registrato | Both - logged | «Scarica il contratto (PDF con marca temporale)» · «Scarica la ricevuta di registrazione» | Sprint 4 | [K1–K7] Si sbloccano al pagamento della registrazione, regola dal foglio User Stories REVIEW 16/03 già dichiarata nella PG 4 della Trattativa. In K1 le due azioni sono visibili e disattivate, con la ragione. |
| Pagina contratto (n) | Header | LINK | Torna al documento di puntuazione | Both - logged | «Vedi il riepilogo della trattativa» | Sprint 4 | [K1–K7] Sola lettura. È dove l'utente verifica cosa ha accettato, e in una fase lunga serve più di quanto sembri. |

### La prossima scadenza

| Pagina | Block | Type | Elemento | Target | Contenuto | Sprint | Note |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Pagina contratto (n) | Prossima scadenza | CONTENT | Il blocco che regge la pagina | Both - logged | «Entro il [GG/MM]: [cosa deve succedere]. Tocca a [te / Nome].» + «Mancano [X] giorni» | Sprint 4 | [K3–K4] Quattro informazioni e niente altro: data, cosa, chi, quanto manca. In una fase che dura mesi il progresso lo misura il calendario, quindi P3 qui prende la forma di un conto alla rovescia. |
| Pagina contratto (n) | Prossima scadenza | CONTENT | Cosa succede se la data passa | Both - logged | «Se la [condizione] non si avvera entro quella data, il contratto si scioglie e l'immobile torna disponibile.» | Sprint 4 | [K3–K4] E3 + E4. È la frase che dà senso alla data: senza, la scadenza sembra burocrazia. Testo diverso per condizione, perché le conseguenze sono diverse. |
| Pagina contratto (n) | Prossima scadenza | FEEDBACK | Avviso a 30 giorni | Both - logged | «La [condizione] scade il [GG/MM], fra 30 giorni. Se ti serve più tempo, puoi proporre una nuova data a [Nome].» | Sprint 4 | [K4] Innesco del ramo D del flow. Il copilota parla quando serve: questo è uno dei tre momenti in cui parla. Compare a entrambe le parti, con le azioni solo al proprietario. |
| Pagina contratto (n) | Prossima scadenza | FEEDBACK | Avviso il giorno della scadenza | Both - logged | «Oggi scade la [condizione]. Se l'esito c'è, comunicalo adesso.» | Sprint 4 | [K4] Da MVP riga 37, che chiede due avvisi: all'avvicinarsi del termine e il giorno della scadenza. Il flow ha solo il primo. Il secondo è quello che conta, perché è il giorno in cui il contratto può cambiare stato da sé. |
| Pagina contratto (n) | Prossima scadenza | FEEDBACK | Scadenza superata senza esito | Both - logged | «La [condizione] è scaduta il [GG/MM] senza una comunicazione. Avete tempo fino al [GG/MM] per comunicare l'esito o concordare una nuova data.» | Sprint 4 | [K3–K4] Blocco nuovo, nasce dal punto 30: la board collega «scaduta» direttamente all'inadempimento, che per un silenzio è sproporzionato. La finestra è dichiarata a entrambi. **DA VALIDARE**: soglia della finestra. |
| Pagina contratto (n) | Prossima scadenza | CONTENT | Nessuna scadenza imminente | Both - logged | «La prossima scadenza è il [GG/MM], fra [X] giorni. Per ora non c'è niente da fare.» | Sprint 4 | [K3] Stato di attesa dichiarato. Dirlo è meglio che lasciare la pagina muta: l'utente che rientra e non trova niente pensa di aver perso una notifica. |
| Pagina contratto (n) | Prossima scadenza | ACTION | Carica il documento in anticipo | Both - logged | «Hai già la [certificazione]? Caricala adesso» | Sprint 4 | [K3] E1 in uno stato di attesa: l'unica cosa che l'utente può fare prima della scadenza è portarsi avanti. Visibile solo al proprietario della condizione. |

### Le condizioni sospensive

| Pagina | Block | Type | Elemento | Target | Contenuto | Sprint | Note |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Pagina contratto (n) | Condizioni sospensive | CONTENT | Titolo e ruolo del blocco | Both - logged | «Le condizioni che tengono sospeso il contratto» | Sprint 4 | [K3–K5] Il nome dice la funzione. Il termine tecnico «condizione sospensiva» resta nella riga, spiegato da un helper P7 la cui fonte canonica è la Guida alla trattativa. |
| Pagina contratto (n) | Condizioni sospensive | LIST | Riga di condizione — struttura | Both - logged | Nome della condizione · scadenza · chi la ha in carico · badge di stato · documento allegato se c'è · azione contestuale | Sprint 4 | [K3–K5] Unità atomica della pagina. Stesso componente della riga di condizione della trattativa, con la scadenza al posto del valore in discussione. P2: lo storico si apre, non è visibile di default. |
| Pagina contratto (n) | Condizioni sospensive | STATUS | Stati della riga | Both - logged | Da comunicare · Proroga richiesta · Prorogata · Avverata · Non avverata · Scaduta · Non applicabile | Sprint 4 | [K3–K7] «Prorogata» porta con sé la data vecchia e quella nuova. «Non applicabile» copre le condizioni che non si attivano, come la prelazione fuori dai terreni agricoli: dichiararle assenti è più chiaro che nasconderle, stessa regola della trattativa. |
| Pagina contratto (n) | Condizioni sospensive | LIST | Le cinque condizioni e il loro proprietario | Both - logged | Mutuo — Acquirente · Vendita di un immobile dell'acquirente — Acquirente · Acquisto o soluzione abitativa del venditore — Venditore · Regolarità edilizia e conformità catastale — Venditore · Prelazione agraria — Acquirente o Venditore | Sprint 4 | [K3–K5] Owner dalla tabella al punto 7 di «Come funziona la trattativa» (check KB del 25/09). La prelazione ha **due proprietari possibili** (A.3 / V.3): la riga dichiara quale dei due la ha in carico su questo contratto. Correzione rispetto alla prima stesura, che la assegnava al solo venditore. |
| Pagina contratto (n) | Condizioni sospensive | ACTION | Azione sulla riga, solo al proprietario | Both - logged | «Comunica l'esito» (primaria) · «Proponi una nuova scadenza» (secondaria) | Sprint 4 | [K3–K4] P5. Aprono le modali della PG 2. Sulle condizioni dell'altra parte non compare nessuna azione, e la riga dice «In attesa di [Nome]». Punto 32 applicato. |
| Pagina contratto (n) | Condizioni sospensive | CONTENT | Perché vedi anche le condizioni dell'altro | Both - logged | «Vedi tutte le condizioni, comprese quelle che deve avverare [Nome]: il contratto dipende da tutte.» | Sprint 4 | [K3–K5] Auditabilità P2P. Presidia l'anti-pattern dell'anonimizzazione della controparte: sapere cosa sta aspettando l'altro fa parte del contratto condiviso. |
| Pagina contratto (n) | Condizioni sospensive | ACTION | Storico della singola condizione | Both - logged | «Vedi cosa è successo su questa condizione (3)» → elenco cronologico: proroghe richieste e accettate, solleciti inviati, esito comunicato, documento allegato, con data e autore | Sprint 4 | [K3–K7] P2 e auditabilità. Chiuso di default. In una fase di mesi è l'unico modo per ricostruire perché una data è cambiata. |
| Pagina contratto (n) | Condizioni sospensive | STATUS | Documento allegato all'esito | Both - logged | Nome del file, data di caricamento, chi lo ha caricato, link all'Archivio | Sprint 4 | [K3–K5] Il documento è l'evidenza che l'altra parte aspetta. Da MVP riga 36: «upload eventuale documentazione (es. mutuo approvato)». **DA VALIDARE**: per quali condizioni è obbligatorio (punto 35). |
| Pagina contratto (n) | Condizioni sospensive | CONTENT | La condizione Regolarità arriva dalla trattativa | Venditori | «Questa condizione l'ha inserita il sistema perché la relazione tecnica [mancava / ha rilevato irregolarità]. Si avvera quando la sanatoria è conclusa.» | Sprint 4 | [K3–K5] Continuità con la regola della PG 2 della Trattativa, dove la condizione la mette il sistema e le parti trattano chi sana ed entro quando. Qui si avvera, e l'evidenza è l'esito della pratica in comune. |

### Quanto costa uscire

| Pagina | Block | Type | Elemento | Target | Contenuto | Sprint | Note |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Pagina contratto (n) | Quanto costa uscire | CONTENT | Titolo e ragione del blocco | Both - logged | «Se una delle due parti si tira indietro» | Sprint 4 | [K2–K5] Blocco aggiunto dopo il check KB del 25/09. Penale e multa sono clausole già in vigore nel contratto firmato, quindi la loro esistenza appartiene alla pagina del contratto, dove si legge senza aver deciso niente. La PG 3 fa un lavoro diverso sullo stesso dato: calcola il totale effettivo di questa uscita, registrazione inclusa, e lo confronta con l'alternativa di aspettare. Qui si sa quanto costerebbe, lì si sa quanto costa adesso. |
| Pagina contratto (n) | Quanto costa uscire | CONTENT | Recesso — multa penitenziale | Both - logged | «Chi si tira indietro paga all'altra parte una multa penitenziale del 5% del prezzo: **[X] €** su questo contratto.» | Sprint 4 | [K2–K5] 5% del prezzo, dal template di contratto (check KB). Cifra calcolata sul prezzo concordato: su 270.000 € fa 13.500 €. **DA VALIDARE**: aliquota ed esistenza della clausola, perché il documento che la riporta non è leggibile da questa sessione. |
| Pagina contratto (n) | Quanto costa uscire | CONTENT | Recesso in pendenza delle condizioni — il 3% a Cleclà | Both - logged | «Se il recesso arriva mentre ci sono ancora condizioni da avverare, a Cleclà è dovuto anche il 3% del prezzo, con un minimo di 6.000 €: **[Y] €** su questo contratto.» | Sprint 4 | [K3–K5] Dal template di contratto (check KB). **Punto 38**: la Guida alla trattativa spiega il recesso nominando solo la multa penitenziale, e questa voce manca. Chi legge la Guida stima il costo di un'uscita per difetto, di almeno 6.000 €. Qui la riga esiste; la correzione va fatta nell'epica Trattativa. |
| Pagina contratto (n) | Quanto costa uscire | CONTENT | Inadempimento — clausola penale | Both - logged | «Chi non rispetta il contratto paga all'altra parte una clausola penale del 5% del prezzo: **[X] €**. Penale e multa penitenziale non si sommano mai.» | Sprint 4 | [K2–K5] 5% del prezzo, art. 1382 c.c., valore fisso del template (punto 26), **DA VALIDARE** come la voce sopra. L'ultima frase serve: la domanda «le pago entrambe?» arriva sempre. |
| Pagina contratto (n) | Quanto costa uscire | CONTENT | E se non è colpa di nessuno | Both - logged | «Se una condizione sospensiva non si avvera e non dipende da nessuno dei due, il contratto si scioglie e non si paga niente: né penali, né rimborsi.» | Sprint 4 | [K3–K5] Verbatim dal Capitolo 4 dei Termini e Condizioni, «€ 0,00 a qualsiasi titolo». È la riga che rende il blocco leggibile invece che minaccioso: le tre cifre sopra valgono solo quando qualcuno si tira indietro. |
| Pagina contratto (n) | Quanto costa uscire | CONTENT | Help contestuale (P7) | Both - logged | «Che differenza c'è fra recesso e inadempimento?» · «Cosa vuol dire multa penitenziale?» | Sprint 4 | [K2–K7] Due «?» per il blocco, non uno per riga: regola delle schermate autenticate dense fissata nella revisione dei wireframe di Sprint 2. Fonte canonica nella Guida alla trattativa, blocco «Se qualcosa va storto». |

### Il contratto e i suoi documenti

| Pagina | Block | Type | Elemento | Target | Contenuto | Sprint | Note |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Pagina contratto (n) | Documenti | LIST | I documenti di questo contratto | Both - logged | Contratto preliminare firmato (PDF con marca temporale) · ricevuta di registrazione all'Agenzia delle Entrate · documento di puntuazione della trattativa · documenti allegati agli esiti delle condizioni | Sprint 4 | [K2–K7] Una selezione: le quattro cose che servono su questa pagina. Il resto vive nell'Archivio dell'immobile, cartella 8 «Contratto e pagamenti», che esiste già. Regola uno-e-solo-uno. |
| Pagina contratto (n) | Documenti | LINK | Tutti i documenti dell'immobile | Both - logged | «Vedi la documentazione dell'immobile» → Archivio documentazione immobile | Sprint 4 | [K2–K7] A contratto firmato l'acquirente vede i documenti oltre la planimetria, regola già fissata nell'Archivio. |
| Pagina contratto (n) | Documenti | STATUS | In K1 i download sono bloccati | Both - logged | «Il contratto firmato viene archiviato con marca temporale quando la registrazione è pagata.» | Sprint 4 | [K1] Dipendenza dal foglio User Stories REVIEW 16/03, già dichiarata nella PG 3 e nella PG 4 della Trattativa. Visibile a entrambi, perché il venditore la subisce senza poter agire. |

### Cosa succede adesso

| Pagina | Block | Type | Elemento | Target | Contenuto | Sprint | Note |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Pagina contratto (n) | Cosa succede adesso | LIST | Le tre strade | Both - logged | Tutte le condizioni si avverano: il contratto diventa efficace e si va dal notaio · Una condizione non si avvera: il contratto si scioglie da sé e l'immobile torna disponibile · Una parte si tira indietro o non rispetta il contratto: si apre il percorso di recesso o di inadempimento | Sprint 4 | [K2–K5] Tre righe, una per strada. Stesse tre frasi del blocco «Se qualcosa va storto» della Guida alla trattativa, che resta la fonte canonica: qui si richiamano, con il link. |
| Pagina contratto (n) | Cosa succede adesso | CONTENT | Cosa arriva dopo il contratto efficace | Both - logged | «Quando tutte le condizioni sono avverate: pagate la nostra provvigione, vi diamo la lista dei documenti per il notaio e i vostri contatti diretti, e da lì proseguite voi.» | Sprint 4 | [K3–K5] E3, ponte verso la PG 4. Toglie la domanda «e poi?» prima che nasca, e prepara il cambio di regime sul contatto diretto. |
| Pagina contratto (n) | Cosa succede adesso | LINK | Il rogito avviene fuori da Cleclà | Both - logged | «Il rogito si fa dal notaio. Noi vi accompagniamo fino a lì.» | Sprint 4 | [K2–K5] Perimetro dichiarato presto, così l'utente non si mette a cercare in piattaforma una funzione che non c'è. |

### Le uscite laterali

| Pagina | Block | Type | Elemento | Target | Contenuto | Sprint | Note |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Pagina contratto (n) | Uscite | ACTION | Chiedi l'annullamento del contratto | Both - logged | «Chiedi l'annullamento del contratto» | Sprint 4 | [K2–K5] Azione terziaria, sempre raggiungibile, mai in evidenza. Il flow la etichetta «può avvenire in qualsiasi momento del flusso». Apre il percorso di recesso (PG 3). P4: anteprima degli importi prima di qualunque conferma. |
| Pagina contratto (n) | Uscite | ACTION | Segnala un inadempimento | Both - logged | «Segnala che [Nome] non sta rispettando il contratto» | Sprint 4 | [K2–K5] Azione terziaria. P5: la label dice cosa fa, invece del termine giuridico da solo. Apre il percorso di inadempimento (PG 3). |
| Pagina contratto (n) | Uscite | CONTENT | Prima di uscire, prova a parlarne | Both - logged | «Prima di avviare una procedura: parlarne con [Nome] o con noi costa niente e risolve la maggior parte dei casi.» + accesso all'assistenza | Sprint 4 | [K2–K5] E4 nella forma della prevenzione. Il costo di un recesso parte dal 5% del prezzo, quindi vale la pena mettere un gradino prima. È anche l'unico punto della fase in cui l'escalation al team è la risposta giusta. |

### Gestione contratti

| Pagina | Block | Type | Elemento | Target | Contenuto | Sprint | Note |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Gestione contratti | Listing | LIST | I contratti in cui sei coinvolto | Both - logged | Una card per contratto: immobile, controparte, badge di stato, prossima scadenza con data e proprietario | Sprint 4 | Foglio Pagine righe 21 e 31, foglio Priority guides righe 228 e 244. La prossima scadenza sulla card è quello che rende la lista utile: senza, è un elenco di titoli. |
| Gestione contratti | Listing | CONTENT | Con un contratto solo | Both - logged | — | Sprint 4 | La voce di menu porta direttamente alla pagina del contratto. Una lista di un elemento è un passaggio in più senza informazione: E2. |
| Gestione contratti | Listing | STATUS | Empty state | Both - logged | V: «Non hai contratti attivi. Un contratto nasce quando una trattativa si chiude e firmate il preliminare.» · A: stesso testo | Sprint 4 | La voce di menu esiste prima che esista un contratto, quindi l'empty state deve dire da dove arriva, altrimenti sembra una funzione che non trova. Stessa regola dell'empty state delle trattative. |
| Gestione contratti | Listing | LIST | Contratti chiusi e annullati | Both - logged | Sezione separata, in coda: immobile, esito, data, documenti scaricabili | Sprint 4 | Un contratto annullato o concluso resta consultabile. I documenti sono l'unica ragione per cui un utente torna su questa pagina dopo mesi. |

### Supporto

| Pagina | Block | Type | Elemento | Target | Contenuto | Sprint | Note |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Pagina contratto (n) | Supporto | LINK | Rimando alle FAQ | Both - logged | «Altre domande sul contratto preliminare» → FAQ, tema «Contratto» pre-filtrato | Sprint 4 | P6. Il tema «Contratto» va aggiunto ai chip della pagina FAQ: oggi ci sono quelli fino alla Trattativa. |
| Pagina contratto (n) | Supporto | LINK | Contatto umano | Both - logged | Floating button di assistenza | Sprint 4 | E5. Coerente con le altre pagine loggate. Da MVP riga 39. |
| Pagina contratto (n) | Supporto | FEEDBACK | SLA superato sulle righe a carico di Cleclà | Both - logged | «Ci stiamo mettendo più del previsto» + apertura dell'assistenza | Sprint 4 | [K2, K6] Stessa regola della PG Profilo immobile e della PG Trattativa. Vale sulla registrazione all'AdE, che il team esegue dopo il pagamento, e sulla mediazione. |

**Checklist Appendice A** — Ruolo sì · Tappa sì · Azione richiesta sì, con una nota: per settimane non c'è niente
da fare, e la risposta sono il blocco prossima scadenza come elemento attivo, le due azioni sempre disponibili al
proprietario e il caricamento in anticipo · Quantità proporzionata sì (storico chiuso di default, documenti come
selezione) · Perché chiaro sì · Errori prevenuti sì (due avvisi di scadenza, finestra prima dell'inadempimento,
gradino di dialogo prima delle uscite) · Supporto sì · Pattern P2, P3, P4, P5, P6, P7 · Stato visibile sì · CTA
specifici sì. **10/10**.

---

## PG 2 — Comunicazione dell'esito di una condizione sospensiva

**Job-to-be-done**: far dichiarare a chi ha in carico una condizione che si è avverata o che non si avvererà, con
l'evidenza allegata, capendo che nel secondo caso il contratto si scioglie.

**Ruolo**: condivisa, asimmetrica per proprietario della condizione · **Tappa**: Contratto ·
**Unità atomiche**: Documenti, Timing.

**Posizione presa**: tre modali dentro la pagina contratto. La ragione sta nel peso delle due azioni: comunicare
un avveramento è una riga di modulo, comunicare un mancato avveramento scioglie un contratto firmato. Portarle
sulla stessa schermata con lo stesso peso visivo sarebbe l'errore più grosso possibile qui, quindi il bivio arriva
al primo passaggio e i due rami hanno forma diversa. La terza modale, la proroga, esiste perché la scadenza è
l'unica cosa che le parti possono ancora negoziare.

### Modale «Comunica l'esito» — ingresso e bivio

| Pagina | Block | Type | Elemento | Target | Contenuto | Sprint | Note |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Pagina contratto (n) | Modale esito | CONTENT | Passaggio 1 — La condizione | Both - logged | «[Nome della condizione] · scadenza [GG/MM]» + il testo esatto concordato in trattativa | Sprint 4 | Precompilata quando si arriva dalla riga. Il testo concordato sta in cima perché è quello che l'utente deve confrontare con la realtà: «ottenimento del mutuo per almeno X €» si avvera o no in base a quella cifra. |
| Pagina contratto (n) | Modale esito | ACTION | Passaggio 2 — Il bivio | Both - logged | «Si è avverata» · «Non si avvererà» | Sprint 4 | E1: si entra con una decisione. Le due uscite hanno peso visivo diverso e la seconda dichiara la conseguenza già qui, sotto il bottone: «scioglie il contratto». P4: l'utente sa dove sta andando prima di andarci. P2: il bivio precede i campi, che compaiono solo nel ramo scelto. |
| Pagina contratto (n) | Modale esito | CONTENT | Chi può aprire questa modale | Both - logged | — | Sprint 4 | Solo il proprietario della condizione (punto 32). Sulle condizioni dell'altra parte la riga non ha azioni. Per la prelazione, che ha due proprietari possibili, la apre quello indicato sul contratto. |
| Pagina contratto (n) | Modale esito | CONTENT | Non ancora deciso | Both - logged | «Non so ancora: torna indietro» | Sprint 4 | Uscita senza conseguenze, dichiarata. Con una scadenza addosso l'utente può aprire la modale per capire cosa comporta, e deve poter uscire senza aver dichiarato niente. |

### Ramo «Si è avverata»

| Pagina | Block | Type | Elemento | Target | Contenuto | Sprint | Note |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Pagina contratto (n) | Esito avverata | INPUT | Il documento che lo dimostra | Both - logged | Upload, pdf jpg png. Testo del campo diverso per condizione: mutuo → «la delibera della banca» · vendita di un immobile → «l'atto di vendita o il preliminare registrato» · prelazione → «la rinuncia del confinante o la scadenza dei termini» · regolarità → «l'esito della pratica di sanatoria» · acquisto o soluzione abitativa del venditore → «il preliminare o il contratto della nuova casa» | Sprint 4 | P1: il documento richiesto è l'output della condizione scelta al passaggio 1, e il testo del campo cambia con essa. Compila: il proprietario della condizione · Obbl.: **DA VALIDARE** (punto 35, il flow dice «se necessario» senza specificare) · Precompilato: — · Serve a: evidenza per la controparte, Archivio dell'immobile, fascicolo notaio. Da MVP riga 36. Formati coerenti con il resto della piattaforma. |
| Pagina contratto (n) | Esito avverata | CONTENT | A cosa serve il documento e chi lo vede | Both - logged | «Lo vede [Nome] e lo vediamo noi. È l'unica prova che la condizione si è avverata, e serve anche al notaio.» | Sprint 4 | E3 + P5. Presidia l'anti-pattern «caricamento di documenti senza spiegare a cosa servono e chi li vedrà». In un P2P la domanda «chi vede questo?» arriva sempre. |
| Pagina contratto (n) | Esito avverata | INPUT | Data dell'avveramento | Both - logged | Campo data, precompilato a oggi | Sprint 4 | Compila: il proprietario · Obbl.: sì · Precompilato: data odierna · Serve a: storico, conteggio delle condizioni, calcolo del momento in cui il contratto diventa efficace. Modificabile, perché l'evento può essere di qualche giorno prima. |
| Pagina contratto (n) | Esito avverata | CONTENT | Anteprima | Both - logged | «Stai dichiarando a [Nome]: [condizione] avverata il [GG/MM], con [nome del documento] allegato.» | Sprint 4 | P4. È il testo che vedrà l'altra parte, mostrato prima dell'invio. |
| Pagina contratto (n) | Esito avverata | ACTION | Dichiara | Both - logged | «Dichiara la condizione avverata» | Sprint 4 | P5. [tap] → [riga aggiornata ad «Avverata», notifica e email a [Nome], contatore avanzato, documento salvato in Archivio]. Se era l'ultima condizione la pagina passa in K5 e si apre la Conclusione. |
| Pagina contratto (n) | Esito avverata | FEEDBACK | Esito dopo l'ultima condizione | Both - logged | «Tutte le condizioni sono avverate. Il contratto è efficace: vi abbiamo aperto la pagina con i prossimi passi.» | Sprint 4 | Il momento che l'utente aspetta da mesi. Dichiarato nella modale, senza fargli cercare il cambiamento in pagina. Da flow E.1.5 → ramo F. |
| Pagina contratto (n) | Esito avverata | ACTION | Correggere una dichiarazione | Both - logged | «Correggi la dichiarazione» sulla riga, entro 48 ore e prima che il contratto diventi efficace | Sprint 4 | P4, reversibilità. La dichiarazione è un atto con conseguenze contrattuali, quindi la finestra è corta e la correzione resta nello storico. **DA VALIDARE** con il team: la finestra esiste o la dichiarazione è definitiva. |

### Ramo «Non si avvererà» — inefficacia

| Pagina | Block | Type | Elemento | Target | Contenuto | Sprint | Note |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Pagina contratto (n) | Esito non avverata | CONTENT | Cosa comporta, prima di tutto il resto | Both - logged | «Dichiarando che la [condizione] non si avvera, il contratto si scioglie. Non è una scelta che si annulla: l'immobile torna disponibile e le altre trattative si riaprono.» | Sprint 4 | P4 su un'azione irreversibile: la conseguenza sta in cima, non sotto il bottone. Il ramo cambia registro rispetto all'avveramento, e deve vedersi dal primo elemento. |
| Pagina contratto (n) | Esito non avverata | CONTENT | E quanto costa | Both - logged | «Se la condizione non si avvera e non dipende da nessuno dei due, non si paga niente: né penali, né rimborsi.» | Sprint 4 | Verbatim dai Termini e Condizioni, Capitolo 4, «€ 0,00 a qualsiasi titolo». È la cosa che l'utente in questo momento ha più bisogno di sapere, e toglie la paura che blocca la dichiarazione. |
| Pagina contratto (n) | Esito non avverata | INPUT | Per regolarità e prelazione — il documento | Both - logged | Upload del documento che attesta il mancato avveramento | Sprint 4 | Compila: il proprietario · Obbl.: sì · Serve a: autocertificazione, archivio. Da flow E.2: la board distingue due tipologie con lo stesso schema, e questa è la prima. |
| Pagina contratto (n) | Esito non avverata | INPUT | Per vendita e acquisto di un altro immobile — la motivazione | Both - logged | Selezione da lista: trattativa non conclusa · acquirente o venditore ritirato · tempi non compatibili con la scadenza · rinuncia alla ricerca | Sprint 4 | Compila: il proprietario della condizione · Obbl.: sì · Serve a: autocertificazione, storico. Il flow dettaglia solo regolarità, prelazione e mutuo, però le cinque condizioni della PG 1 includono anche la vendita di un immobile dell'acquirente e l'acquisto del venditore, che sono fra le più probabili a non avverarsi. Lo schema è lo stesso delle altre. |
| Pagina contratto (n) | Esito non avverata | INPUT | Per il mutuo — la motivazione | Acquirenti | Selezione da lista: mutuo rifiutato · importo concesso inferiore a quello necessario · pratica non conclusa entro la scadenza · rinuncia alla richiesta | Sprint 4 | Compila: Acquirente · Obbl.: sì · Serve a: autocertificazione, storico. Da flow E.2, ramo mutuo: «seleziona condizione da lista». L'ultima voce è la sola in cui il mancato avveramento dipende dall'utente, e ha una conseguenza diversa: vedi riga sotto. |
| Pagina contratto (n) | Esito non avverata | FEEDBACK | Se la causa dipende da te | Both - logged | «Hai indicato che hai rinunciato alla richiesta. In questo caso il mancato avveramento dipende da te, e [Nome] può chiedere la clausola penale del 5%.» | Sprint 4 | E3 + E4. La distinzione fra «non si è avverata» e «non l'ho fatta avverare» è la linea fra inefficacia e inadempimento, e va detta nel punto in cui l'utente sceglie la motivazione. **DA VALIDARE** con il cliente: quali motivazioni cadono da questo lato. |
| Pagina contratto (n) | Esito non avverata | STATUS | L'autocertificazione generata | Both - logged | Documento precompilato con i dati del contratto, la condizione, la motivazione e la data. Da rileggere prima di firmare | Sprint 4 | Da flow E.2.3: «generazione automatica autocertificazione». Precompilato: dati anagrafici, contratto, condizione, motivazione. All'utente resta da rileggere. |
| Pagina contratto (n) | Esito non avverata | ACTION | Firma FEA | Both - logged | «Firma l'autocertificazione» | Sprint 4 | Firma elettronica avanzata, da flow E.2.4. FEA e non FEQ, coerente con i Termini e Condizioni, dove la FEQ è riservata al preliminare perché la legge impone la forma scritta. Noi disegniamo il contorno e gli stati di esito, la procedura è del provider. |
| Pagina contratto (n) | Esito non avverata | CONTENT | Questa azione è definitiva | Both - logged | «Con la firma il contratto si scioglie. Non serve il consenso di [Nome]: la condizione era nel contratto che avete firmato.» | Sprint 4 | P4. La seconda frase previene la domanda più probabile, e insieme spiega perché il flow chiama la risoluzione «automatica»: non c'è una controparte da convincere. Punto 31, nella lettura adottata. |
| Pagina contratto (n) | Esito non avverata | FEEDBACK | Esito | Both - logged | «Il contratto è sciolto. Abbiamo avvisato [Nome], l'annuncio è tornato online e le trattative in stand-by si sono riaperte.» | Sprint 4 | Da flow E.2.8 e E.2.9. Le tre conseguenze dichiarate insieme, perché sono tre cose che l'utente si chiederebbe una per una. Pagina in K7. |
| Pagina contratto (n) | Esito non avverata | CONTENT | Vista della controparte | Both - logged | «[Nome] ha dichiarato che la [condizione] non si è avverata. Il contratto è sciolto.» + autocertificazione allegata e scaricabile | Sprint 4 | Chi riceve la notizia non ha agito, quindi ha bisogno dell'evidenza più di chi ha dichiarato. Da MVP riga 37: notifica con la motivazione, in piattaforma e via email. |
| Pagina contratto (n) | Esito non avverata | CONTENT | Chi può dichiarare l'inefficacia | Both - logged | — | Sprint 4 | **DA VALIDARE**, punto 31. Qui la modale è del proprietario della condizione, che è la lettura coerente con il punto 32. Se il cliente decide che entrambe le parti possono dichiararla, cambia chi vede la CTA, non la struttura della modale. |

### Modale «Proponi una nuova scadenza»

| Pagina | Block | Type | Elemento | Target | Contenuto | Sprint | Note |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Pagina contratto (n) | Modale proroga | CONTENT | Da dove si arriva | Both - logged | «[Condizione] · scadenza attuale [GG/MM]» | Sprint 4 | Ramo D del flow. Disponibile dall'avviso a 30 giorni e dentro la finestra a scadenza superata. Fuori da quelle due situazioni la CTA non compare: una proroga chiesta con quattro mesi di anticipo non ha senso. |
| Pagina contratto (n) | Modale proroga | INPUT | La nuova data | Both - logged | Campo data, con il vincolo che non superi la data del rogito concordata | Sprint 4 | Compila: il proprietario della condizione · Obbl.: sì · Precompilato: suggerimento in base al tipo, mutuo +60 giorni · Serve a: aggiornamento delle scadenze sul contratto. E4: la validazione previene la proroga che sfonda il rogito, che è l'errore probabile. |
| Pagina contratto (n) | Modale proroga | INPUT | Perché ti serve più tempo | Both - logged | Campo testo facoltativo, max 300 caratteri | Sprint 4 | Compila: chi propone · Obbl.: no · Serve a: decisione della controparte, storico. Facoltativo, con il testo di supporto «Dirlo aiuta [Nome] a decidere»: suggerimento, non obbligo, come la motivazione del rifiuto in trattativa. |
| Pagina contratto (n) | Modale proroga | CONTENT | Anteprima | Both - logged | «Stai chiedendo a [Nome] di spostare la scadenza della [condizione] dal [GG/MM] al [GG/MM].» | Sprint 4 | P4. |
| Pagina contratto (n) | Modale proroga | ACTION | Invia | Both - logged | «Chiedi la proroga a [Nome]» | Sprint 4 | P5. [tap] → [riga in «Proroga richiesta», notifica e email alla controparte]. |
| Pagina contratto (n) | Modale proroga | ACTION | Risposta della controparte | Both - logged | «Accetta la nuova scadenza» · «Mantieni la scadenza attuale» | Sprint 4 | Due azioni, senza controproposta: la proroga è una richiesta secca. Il flow (D.4) prevede solo sì o no, e aprire una negoziazione sulle date dentro il contratto riaprirebbe la Trattativa. |
| Pagina contratto (n) | Modale proroga | FEEDBACK | Se accetta | Both - logged | «La scadenza della [condizione] è spostata al [GG/MM]. Il contratto è aggiornato.» | Sprint 4 | Da flow D: «aggiorna scadenze sul contratto». Notifica a entrambi, riga in «Prorogata» con la data vecchia visibile nello storico. |
| Pagina contratto (n) | Modale proroga | FEEDBACK | Se mantiene | Both - logged | «[Nome] preferisce mantenere la scadenza del [GG/MM]. La condizione va avverata entro quella data.» | Sprint 4 | Lettura del loop del flow verso il punto A.2: il rifiuto lascia in piedi la scadenza originale, non annulla niente. Dirlo esplicitamente evita che l'utente pensi che il contratto sia a rischio. |
| Pagina contratto (n) | Modale proroga | CONTENT | Un solo rilancio per condizione | Both - logged | «Su questa condizione hai già chiesto una proroga.» | Sprint 4 | Limite di design, non del flow. Senza limite la proroga diventa una trattativa parallela dentro il contratto. **DA VALIDARE** con il team. |

### La finestra prima dell'inadempimento

| Pagina | Block | Type | Elemento | Target | Contenuto | Sprint | Note |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Pagina contratto (n) | Finestra | STATUS | La riga passa in «Scaduta» | Both - logged | «Scaduta il [GG/MM], in attesa di comunicazione» | Sprint 4 | È uno stato della riga: il contratto resta in K3. La board collega «scaduta» direttamente all'ingresso dell'inadempimento, e questa finestra è il gradino che ci metto in mezzo (punto 30). |
| Pagina contratto (n) | Finestra | FEEDBACK | Sollecito automatico a entrambi | Both - logged | «La [condizione] è scaduta senza comunicazione. Fino al [GG/MM] si può ancora comunicare l'esito o concordare una nuova data.» | Sprint 4 | Notifica e email a entrambe le parti. Il copilota parla quando serve, e questo è il momento in cui il silenzio costa più caro. **DA VALIDARE**: soglia della finestra. In KB esistono soglie analoghe per la Trattativa (3 giorni di silenzio, 48 ore fra solleciti) che non si riusano senza conferma. |
| Pagina contratto (n) | Finestra | ACTION | Sollecita la controparte | Both - logged | «Manda un promemoria a [Nome]» | Sprint 4 | Ripetibile ogni 48 ore, come gli altri solleciti della piattaforma. Visibile alla parte che aspetta. |
| Pagina contratto (n) | Finestra | ACTION | La proroga resta disponibile | Both - logged | «Proponi una nuova scadenza» | Sprint 4 | Dentro la finestra, anche a scadenza superata. È l'uscita che evita l'inadempimento nella maggior parte dei casi reali, dove il ritardo è della banca o del comune. |
| Pagina contratto (n) | Finestra | FEEDBACK | Alla chiusura della finestra | Both - logged | «La finestra è chiusa. [Nome] può segnalare un inadempimento, oppure potete ancora accordarvi.» | Sprint 4 | E3: la conseguenza si apre come possibilità. La segnalazione resta un'azione dell'utente, coerente con il flow C.1, dove il ramo parte da una user action. Il volante resta all'utente. |

### Help contestuale

| Pagina | Block | Type | Elemento | Target | Contenuto | Sprint | Note |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Pagina contratto (n) | Help | CONTENT | Gli helper P7 della fase | Both - logged | «Cosa vuol dire che il contratto si scioglie?» · «Cos'è un'autocertificazione e perché la firmo io?» · «Che differenza c'è fra recesso e inadempimento?» · «Posso spostare una scadenza dopo che è passata?» | Sprint 4 | Quattro helper, uno per momento di dubbio quasi certo. Un «?» per blocco e non per campo, regola delle schermate autenticate dense. Max 280 caratteri più link alla FAQ, tema «Contratto». Fonte canonica nella Guida alla trattativa dove esiste già. |

**Checklist Appendice A** — Ruolo sì · Tappa sì · Azione richiesta sì · Quantità proporzionata sì · Perché chiaro
sì · Errori prevenuti sì (bivio e conseguenze in cima al ramo irreversibile, validazione della data sul rogito,
finestra prima dell'inadempimento, distinzione fra inefficacia e causa imputabile) · Supporto sì · Pattern P1, P2,
P4, P5, P7 · Stato visibile sì · CTA specifici sì. **10/10**.

---

## PG 3 — Uscita dal contratto: recesso e inadempimento

**Job-to-be-done**: portare a termine un'uscita dal contratto in modo che entrambe le parti sappiano quanto costa,
chi paga chi, cosa devono firmare e quando l'immobile torna disponibile.

**Ruolo**: condivisa, con ruoli asimmetrici che si invertono (chi esce, chi riceve) · **Tappa**: Contratto ·
**Unità atomiche**: Budget, Documenti.

**Posizione presa**: sono i due rami più lunghi della fase, 16 passaggi il recesso e una ventina l'inadempimento
con mediazione, e sono anche i due che l'utente affronta nel momento peggiore. Il modo di tenerli leggibili è una
**sequenza a passaggi con stato per parte**, come la catena dell'invito della Preparazione alla firma: ogni persona
vede a che punto è il percorso, cosa tocca a lei e cosa si sta aspettando dall'altra. È P3 applicato alle persone
invece che alle schermate, e P2 sui passaggi, che si aprono uno alla volta. Entrambi i rami convergono sullo stesso
schema di chiusura, quindi la parte finale si disegna una volta sola.

Il percorso vive come **sequenza dentro la pagina contratto**, che resta il posto dove il contratto abita. Il foglio Priority guides lo chiama «pop-up recesso» e «pop-up inadempienza» (righe 321–322), e
una modale regge il primo passaggio ma non sei passaggi con pagamenti e firme di due persone in giorni diversi.

### Il percorso di recesso — stati

| Pagina | Block | Type | Elemento | Target | Contenuto | Sprint | Note |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Pagina contratto (n) | Recesso · stati | STATUS | R0 — Richiesta da confermare | Both - logged | I quattro passaggi della richiesta: cosa stai per fare, perché, quanto costa, conferma | Sprint 4 | Ci si entra: CTA «Chiedi l'annullamento del contratto» da K2–K5 · Ha la palla: chi recede · Si esce con: la conferma, oppure con l'uscita dalla sequenza, che qui è ancora senza conseguenze. È l'unico stato del percorso che vive come modale. |
| Pagina contratto (n) | Recesso · stati | STATUS | R1 — Richiesta inviata | Both - logged | «Abbiamo ricevuto la tua richiesta di annullamento. Ti diciamo entro [SLA] come procedere.» | Sprint 4 | Ci si entra: conferma della richiesta · Ha la palla: Cleclà · Si esce con: attivazione del flusso da parte del team. Da flow B.2–B.3 e backoffice riga 52, «CtA attiva flusso di recesso, solo se viene ricevuta richiesta». |
| Pagina contratto (n) | Recesso · stati | STATUS | R2 — Registrazione da pagare | Both - logged | Importo, destinatario, scadenza e metodo | Sprint 4 | Ci si entra: flusso attivato · Ha la palla: chi recede · Si esce con: pagamento e, se per bonifico, caricamento della ricevuta. Da flow B.4–B.5. |
| Pagina contratto (n) | Recesso · stati | STATUS | R3 — Modulo da firmare | Both - logged | Documento di recesso generato, da rileggere e firmare in FEQ | Sprint 4 | Ci si entra: pagamento confermato · Ha la palla: chi recede · Si esce con: firma. Da flow B.6–B.8: alla firma il documento parte verso Cleclà e la controparte. |
| Pagina contratto (n) | Recesso · stati | STATUS | R4 — In attesa dell'IBAN della controparte | Both - logged | «[Nome] deve dirci dove ricevere la multa penitenziale.» | Sprint 4 | Ci si entra: documento inviato · Ha la palla: la controparte · Si esce con: IBAN inserito. Da flow B.9–B.10. Vedi punto 41 sulla direzione del pagamento. |
| Pagina contratto (n) | Recesso · stati | STATUS | R5 — Multa penitenziale da pagare | Both - logged | Importo, IBAN del destinatario, scadenza | Sprint 4 | Ci si entra: IBAN ricevuto · Ha la palla: chi recede · Si esce con: pagamento, caricamento della ricevuta e conferma di ricezione della controparte. Da flow B.11–B.13. |
| Pagina contratto (n) | Recesso · stati | STATUS | R6 — Registrazione del recesso in corso | Both - logged | «Registriamo il recesso all'Agenzia delle Entrate e archiviamo il contratto.» + SLA | Sprint 4 | Ci si entra: pagamento confermato da entrambi · Ha la palla: Cleclà · Si esce con: contratto in K7. Da flow B.14–B.16 e backoffice riga 52. |
| Pagina contratto (n) | Recesso · stati | STATUS | Vista della controparte, in ogni stato | Both - logged | Stesso percorso, con l'etichetta di responsabilità invertita: «In attesa di [Nome]» dove tocca a chi recede, «Tocca a te» su R4 e sulla conferma di ricezione | Sprint 4 | [R1–R6] Auditabilità P2P. Chi subisce il recesso vede tutto il percorso, perché sta aspettando dei soldi e ha diritto di sapere a che punto è la pratica. |

### Recesso — la richiesta e i suoi costi

| Pagina | Block | Type | Elemento | Target | Contenuto | Sprint | Note |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Pagina contratto (n) | Recesso · richiesta | CONTENT | Passaggio 1 — Cosa stai per fare | Both - logged | «Stai chiedendo di annullare il contratto preliminare su [Tipologia] in [Via], [Comune]. Il recesso è un tuo diritto e non richiede il consenso di [Nome]. Ha un costo, e te lo diciamo prima.» | Sprint 4 | [R0] Apre dichiarando tre cose: cosa, che si può fare, che costa. La terza frase è quella che tiene la persona in pagina invece di farla chiamare l'assistenza. |
| Pagina contratto (n) | Recesso · richiesta | INPUT | Passaggio 2 — Perché | Both - logged | Selezione da lista: ho cambiato idea · non ho più le condizioni economiche · ho trovato un'altra soluzione · problemi emersi sull'immobile · altro, con campo testo | Sprint 4 | [R0] Compila: chi recede · Obbl.: sì · Serve a: documento di recesso, storico, statistiche del team. Da MVP riga 37, «richiesta annullamento con selezione motivazione da lista». La voce «problemi emersi sull'immobile» esiste perché i T&C, Capitolo 4, elencano fra le cause l'impossibilità sopravvenuta a seguito della relazione tecnica. |
| Pagina contratto (n) | Recesso · richiesta | CONTENT | Passaggio 3 — Quanto costa, in tre voci | Both - logged | Vedi le tre righe sotto, presentate insieme con il totale in fondo | Sprint 4 | [R0] **È la schermata più importante della PG.** P4 nella sua forma più letterale: anteprima completa prima di un'azione irreversibile e costosa. Le tre voci hanno destinatari diversi, quindi vanno separate: un totale unico sarebbe un costo opaco, cioè l'anti-pattern dei costi rivelati a fine flusso. |
| Pagina contratto (n) | Recesso · richiesta | CONTENT | Voce 1 — Multa penitenziale a [Nome] | Both - logged | «**[X] €** — 5% del prezzo concordato ([prezzo] €). Va a [Nome], come previsto dal contratto che avete firmato.» | Sprint 4 | 5% dal template di contratto (check KB del 25/09). Su 270.000 € fa 13.500 €. Il rimando al contratto firmato è quello che rende la cifra accettabile: non è una penale della piattaforma. **DA VALIDARE** l'aliquota. |
| Pagina contratto (n) | Recesso · richiesta | CONTENT | Voce 2 — Corrispettivo a Cleclà | Both - logged | «**[Y] €** — 3% del prezzo, minimo 6.000 €. Dovuto solo perché ci sono ancora condizioni da avverare.» | Sprint 4 | Dal template di contratto (check KB). **DA VALIDARE**, aliquota e minimo, e l'esistenza della clausola: il documento che la riporta non è leggibile da questa sessione, e questa è la voce più pesante della schermata. Compare **solo** con sospensive pendenti: in K2 e K5 la voce non c'è, e va detto perché, altrimenti sembra arbitraria. **Punto 38**: la Guida alla trattativa nomina la multa penitenziale del recesso e non nomina questa voce. Correzione da fare nell'epica Trattativa. |
| Pagina contratto (n) | Recesso · richiesta | CONTENT | Voce 3 — Registrazione del recesso | Both - logged | «**[Z] €** — imposta e bollo per registrare il recesso all'Agenzia delle Entrate. La paghi tu, che eserciti il recesso.» | Sprint 4 | Formula dal flow B.4: 200 € + 16 € + 3% del 5% del prezzo. **Ipotesi di lavoro del 25/09**: la paga chi recede (punto 36). **DA VALIDARE** anche la base della quota proporzionale (punto 27): la lettura adottata è che il 3% si calcoli sulla multa penitenziale, che è appunto il 5% del prezzo. |
| Pagina contratto (n) | Recesso · richiesta | CONTENT | Il totale | Both - logged | «In tutto: **[X+Y+Z] €**» + «Su un contratto da [prezzo] €» | Sprint 4 | [R0] Su 270.000 € con sospensive pendenti il totale è intorno ai 22.000 €. È la cifra più alta che un utente incontra in tutta la piattaforma: va scritta grande, una volta, con le tre voci sopra. |
| Pagina contratto (n) | Recesso · richiesta | CONTENT | Se aspetti che le condizioni si avverino | Both - logged | «Se aspetti e una condizione non si avvera, il contratto si scioglie da sé e non paghi niente. Recedere adesso costa [X+Y+Z] €.» | Sprint 4 | [R0] E4, prevenzione dell'errore costoso. È l'informazione che cambia la decisione, e arriva all'utente solo se gliela diamo: la differenza fra le due strade sono decine di migliaia di euro. Il copilota suggerisce, la scelta resta all'utente. |
| Pagina contratto (n) | Recesso · richiesta | ACTION | Passaggio 4 — Conferma | Both - logged | «Ho capito i costi, procedi» (primaria) · «Torna al contratto» (secondaria) · «Parla con noi prima di decidere» (terziaria) | Sprint 4 | [R0] P5 ed E4: la primaria nomina il costo, che è l'informazione su cui si decide. La terza uscita esiste perché a queste cifre una telefonata conviene a tutti. |
| Pagina contratto (n) | Recesso · richiesta | CONTENT | Questa richiesta è ancora annullabile | Both - logged | «Fino al pagamento puoi ancora fermarti.» | Sprint 4 | [R0] P4, reversibilità dichiarata finché esiste. Il punto di non ritorno è il pagamento della registrazione, e va detto dove si trova. |

### Recesso — pagamenti, firma, documento

| Pagina | Block | Type | Elemento | Target | Contenuto | Sprint | Note |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Pagina contratto (n) | Recesso · pagamenti | ACTION | Paga la registrazione | Both - logged | «Paga [Z] € e registra il recesso» | Sprint 4 | [R2] P5. → Checkout esistente, carta o bonifico. Nessun carrello: è una voce unica e obbligatoria, stessa impostazione della PG 4 della Trattativa. |
| Pagina contratto (n) | Recesso · pagamenti | INPUT | Ricevuta del bonifico | Both - logged | Upload, solo se il pagamento è per bonifico | Sprint 4 | Compila: chi paga · Obbl.: sì con bonifico · Serve a: codice transazione, archivio. Da MVP riga 38 e nota della board «solo se pagamento eseguito tramite bonifico». Con carta il passaggio non compare. |
| Pagina contratto (n) | Recesso · pagamenti | CONTENT | Pagamenti separati | Both - logged | «Registrazione e multa penitenziale sono due pagamenti distinti, con destinatari diversi.» | Sprint 4 | Nota a margine della board su questo step. La registrazione va allo Stato tramite Cleclà, la multa va alla controparte con un bonifico diretto: due canali, e la confusione fra i due genererebbe ticket. |
| Pagina contratto (n) | Recesso · pagamenti | STATUS | Il documento di recesso generato | Both - logged | Documento precompilato con le parti, l'immobile, il contratto, la motivazione e gli importi. Da rileggere | Sprint 4 | [R3] Da flow B.7 e MVP riga 37, «generazione documento di recesso». All'utente resta da rileggere. Il documento non compare nell'elenco dell'Archivio, regola del 18/08: si genera dentro al percorso quando l'evento si verifica. |
| Pagina contratto (n) | Recesso · pagamenti | ACTION | Firma il recesso | Both - logged | «Firma il documento di recesso» | Sprint 4 | [R3] FEQ, da flow B.6. Sopra il bottone: «Con la firma il contratto è annullato. [Nome] riceve il documento e le istruzioni per ricevere la multa.» P4 su azione irreversibile. |
| Pagina contratto (n) | Recesso · pagamenti | INPUT | IBAN per ricevere la multa | Both - logged | Campo IBAN e intestatario, alla parte che riceve | Sprint 4 | [R4] Compila: la controparte · Obbl.: sì · Precompilato: — · Serve a: bonifico della multa penitenziale. **L'IBAN entra in piattaforma qui e solo qui**, come deciso il 03/09 al punto 16: la Trattativa non lo chiede più. |
| Pagina contratto (n) | Recesso · pagamenti | ACTION | Paga la multa penitenziale | Both - logged | «Ho eseguito il bonifico» + upload della ricevuta | Sprint 4 | [R5] Bonifico diretto fra le parti, fuori dal checkout: Cleclà non incassa la multa. Da flow B.11–B.12. |
| Pagina contratto (n) | Recesso · pagamenti | ACTION | Conferma di ricezione | Both - logged | «Confermo di aver ricevuto [X] €» | Sprint 4 | [R5] Alla parte che riceve. Chiude il pagamento senza che il team debba verificare due conti bancari. Da flow B.13. |
| Pagina contratto (n) | Recesso · pagamenti | FEEDBACK | Se il pagamento non arriva | Both - logged | «Non hai ancora ricevuto il bonifico? Scrivici.» dopo [SLA] dalla ricevuta caricata | Sprint 4 | [R5] Il caso in cui la ricevuta è caricata e i soldi non arrivano esiste, e la piattaforma non può risolverlo da sola. **DA VALIDARE** con il team: cosa succede se la multa non viene pagata. |

### Il percorso di inadempimento — stati

| Pagina | Block | Type | Elemento | Target | Contenuto | Sprint | Note |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Pagina contratto (n) | Inadempimento · stati | STATUS | I0 — Segnalazione da confermare | Both - logged | I tre passaggi della segnalazione: cosa stai per fare, cosa non è stato rispettato, cosa comporta | Sprint 4 | Ci si entra: CTA «Segnala che [Nome] non sta rispettando il contratto» da K2–K5 · Ha la palla: chi segnala · Si esce con: l'invio, oppure con l'uscita dalla sequenza. Come R0, è una modale. |
| Pagina contratto (n) | Inadempimento · stati | STATUS | I1 — Segnalazione inviata | Both - logged | «Abbiamo inviato la segnalazione a [Nome] e la stiamo esaminando.» | Sprint 4 | Ci si entra: conferma della segnalazione · Ha la palla: la controparte e Cleclà · Si esce con: la risposta sulla mediazione. Da flow C.1–C.4. |
| Pagina contratto (n) | Inadempimento · stati | STATUS | I2 — Mediazione da accettare | Both - logged | «Possiamo provare a mediare fra voi. Serve il sì di tutti e due.» | Sprint 4 | Ci si entra: documento inviato · Ha la palla: entrambi · Si esce con: due sì (va a I3) oppure un no (il team attiva comunque il flusso). Da flow C.5: la mediazione richiede l'accordo di entrambi. |
| Pagina contratto (n) | Inadempimento · stati | STATUS | I2b — Mediazione rifiutata | Both - logged | «Uno di voi ha preferito procedere senza mediazione. Ce ne stiamo occupando comunque.» | Sprint 4 | Ci si entra: un no sulla mediazione (flow C.5, ramo NO: «attiva flusso di inadempienza») · Ha la palla: Cleclà · Si esce con: la gestione del team, che riporta il percorso su I5 o I6. Il contratto passa comunque in K6: la sospensione dipende dalla segnalazione, non dalla mediazione. **DA VALIDARE** con il team. |
| Pagina contratto (n) | Inadempimento · stati | STATUS | I3 — Contratto sospeso, mediazione in corso | Both - logged | «Il contratto è sospeso e le scadenze sono congelate finché la mediazione è aperta.» + SLA | Sprint 4 | Corrisponde a K6. Ci si entra: mediazione accettata · Ha la palla: Cleclà · Si esce con: accordo trovato o azione giudiziaria. Da flow C.1.6–C.1.8 e backoffice riga 52. |
| Pagina contratto (n) | Inadempimento · stati | STATUS | I4 — Accordo da firmare | Both - logged | Accordo caricato dal team, da rileggere e firmare in FEQ da entrambe le parti | Sprint 4 | Ci si entra: accordo trovato · Ha la palla: entrambi · Si esce con: due firme → il contratto torna in K3 con le scadenze riattivate. Da flow C.1.9, ramo «SI, continua». |
| Pagina contratto (n) | Inadempimento · stati | STATUS | I4b — Accordo che risolve il contratto | Both - logged | «Avete trovato un accordo: il contratto si scioglie e [Nome] paga la clausola penale.» | Sprint 4 | Ci si entra: accordo in mediazione sul ramo «SI, risolvi» del flow C.1.9 · Ha la palla: la parte inadempiente · Si esce con: pagamento → blocco Chiusura. È il terzo esito della mediazione, distinto da I4 perché lì il contratto riprende e qui finisce, e distinto da I6 perché ci si arriva senza passare da un giudice. |
| Pagina contratto (n) | Inadempimento · stati | STATUS | I5 — Azione giudiziaria in corso | Both - logged | «La mediazione non ha trovato un accordo. La vicenda è passata in sede giudiziaria e il contratto resta sospeso.» | Sprint 4 | Ci si entra: mediazione senza accordo · Ha la palla: fuori dalla piattaforma · Si esce con: sentenza o accordo fra avvocati archiviato. Da flow C.1.9, ramo «NO». Lo stato più lungo e meno controllabile: la pagina dichiara che non c'è niente da fare qui e dove si trovano i documenti. |
| Pagina contratto (n) | Inadempimento · stati | STATUS | I6 — Inadempimento confermato, penale da pagare | Both - logged | Parte inadempiente, importo, destinatario | Sprint 4 | Ci si entra: conferma dell'inadempimento con individuazione della parte · Ha la palla: la parte inadempiente · Si esce con: pagamento confermato. Da flow C.1.9 e C.2. Backoffice riga 52: «conferma inadempienza SI/NO», «seleziona parte inadempiente». |
| Pagina contratto (n) | Inadempimento · stati | STATUS | I7 — Inadempimento smentito | Both - logged | «La segnalazione non è stata confermata. Il contratto resta valido.» | Sprint 4 | Da flow C.1.9, ramo «Inadempienza confermata? NO». Qui la board manda a «riattiva annuncio e trattative», che contraddice «contratto valido»: se l'inadempimento è smentito il contratto dovrebbe riprendere, non sciogliersi. **Punto aperto 42.** |

### Inadempimento — segnalazione e mediazione

| Pagina | Block | Type | Elemento | Target | Contenuto | Sprint | Note |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Pagina contratto (n) | Inadempimento · segnalazione | CONTENT | Passaggio 1 — Cosa stai per fare | Both - logged | «Stai segnalando che [Nome] non sta rispettando il contratto. È una segnalazione formale: genera un documento che riceve anche [Nome].» | Sprint 4 | [I0] La differenza con il recesso va detta subito: qui si accusa qualcuno, e la parola «formale» è quella che fa fermare chi stava solo sfogandosi. |
| Pagina contratto (n) | Inadempimento · segnalazione | INPUT | Passaggio 2 — Cosa non è stato rispettato | Both - logged | Selezione da lista, costruita sulle condizioni di questo contratto: scadenza di una condizione sospensiva superata senza comunicazione · sanatoria non avviata entro la data concordata · possesso non trasferito alla data concordata · rifiuto di procedere al rogito · altro, con campo testo | Sprint 4 | [I0] Compila: chi segnala · Obbl.: sì · Serve a: documento di inadempimento, mediazione. Da flow C.2, «seleziona motivazione da lista». La lista si costruisce sulle condizioni effettivamente presenti nel contratto: E2, niente voci che non possono capitare. |
| Pagina contratto (n) | Inadempimento · segnalazione | CONTENT | Passaggio 3 — Cosa comporta | Both - logged | «Se l'inadempimento viene confermato, [Nome] ti paga la clausola penale del 5% del prezzo: **[X] €**. Se non viene confermato, il contratto resta valido.» | Sprint 4 | [I0] P4 e simmetria: chi segnala sa cosa sta chiedendo, e sa che può non ottenerlo. 5% dal template, art. 1382 c.c. (punto 26). |
| Pagina contratto (n) | Inadempimento · segnalazione | ACTION | Invia la segnalazione | Both - logged | «Invia la segnalazione a [Nome]» | Sprint 4 | [I0] P5. [tap] → [generazione automatica del documento, invio alla controparte e a Cleclà, pagina in I1]. Da flow C.3–C.4. |
| Pagina contratto (n) | Inadempimento · segnalazione | CONTENT | Vista di chi riceve la segnalazione | Both - logged | «[Nome] ha segnalato che non stai rispettando il contratto, per questo motivo: [motivazione]. Il documento è allegato.» + «Se ti sembra un malinteso, la mediazione serve esattamente a questo.» | Sprint 4 | [I1] Il momento più teso della piattaforma. Il tono resta descrittivo e apre subito l'uscita costruttiva, senza toni paternalistici. |
| Pagina contratto (n) | Inadempimento · segnalazione | ACTION | La mediazione | Both - logged | «Accetta la mediazione di Cleclà» · «Preferisco procedere senza» | Sprint 4 | [I2] Da flow C.5. Serve il sì di entrambi: la riga lo dice, altrimenti chi accetta non capisce perché non parte niente. |
| Pagina contratto (n) | Inadempimento · segnalazione | CONTENT | Cosa fa la mediazione, e cosa non fa | Both - logged | «Proviamo a farvi trovare un accordo. Non decidiamo noi chi ha ragione: se l'accordo non arriva, la vicenda va davanti a un giudice.» | Sprint 4 | [I2] E3, e coerenza con i T&C: la provvigione include il coordinamento della mediazione, non attività consulenziali specialistiche. Il perimetro del servizio va detto prima, non scoperto dopo. |
| Pagina contratto (n) | Inadempimento · segnalazione | CONTENT | Cosa si congela | Both - logged | «Finché la mediazione è aperta: le scadenze delle condizioni sospensive sono sospese, l'annuncio resta fuori dai risultati, e nessuno dei due può recedere.» | Sprint 4 | [I3] E3 sullo stato più delicato della fase. La terza conseguenza è la più importante e la meno ovvia: la sospensione chiude anche l'uscita laterale. **DA VALIDARE** con il team. |
| Pagina contratto (n) | Inadempimento · segnalazione | STATUS | Chi ha la palla durante la mediazione | Both - logged | «Ci pensiamo noi» + ultimo aggiornamento del team con data | Sprint 4 | [I3] L'aggiornamento datato è quello che evita la telefonata settimanale. Senza, uno stato che dura settimane sembra uno stato dimenticato. |
| Pagina contratto (n) | Inadempimento · segnalazione | STATUS | Documenti della vicenda | Both - logged | Documento di inadempimento · accordo di mediazione, se raggiunto · sentenza o accordo fra avvocati, se si è arrivati lì | Sprint 4 | [I1–I7] Da flow C.1.9, «archiviazione documento di sentenza o accordo avvocato». Scaricabili da entrambe le parti: sono gli atti della loro vicenda. |

### Chiusura, comune ai due rami

| Pagina | Block | Type | Elemento | Target | Contenuto | Sprint | Note |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Pagina contratto (n) | Chiusura | INPUT | IBAN della parte che riceve | Both - logged | Campo IBAN e intestatario | Sprint 4 | [R5, I4b, I6] Compila: chi riceve · Obbl.: sì · Serve a: bonifico. **Punto 41**: la board mette l'inserimento dell'IBAN sul rail della parte che paga, in entrambi i rami. La sequenza che regge è l'opposta, chi riceve dà l'IBAN, e l'ho disegnata così. Da confermare. |
| Pagina contratto (n) | Chiusura | ACTION | Pagamento e ricevuta | Both - logged | «Ho eseguito il bonifico» + upload della ricevuta | Sprint 4 | [R5, I4b, I6] Da flow C.2.2. Bonifico diretto fra le parti. |
| Pagina contratto (n) | Chiusura | ACTION | Conferma di ricezione | Both - logged | «Confermo di aver ricevuto [X] €» | Sprint 4 | [R5, I4b, I6] Da flow C.2.3. |
| Pagina contratto (n) | Chiusura | CONTENT | Le due formule di registrazione | Both - logged | Con tutte le condizioni avverate (o nessuna condizione): «registrazione dell'inadempimento, [Z] €» · Con condizioni ancora pendenti: «penale più registrazione dell'inadempimento, [Z] €» | Sprint 4 | [I4b, I6] Da flow C.2.4, che prevede due percorsi con gli stessi importi. La differenza va spiegata dove si paga, perché è il punto che genera il ticket: due voci con lo stesso totale e nomi diversi sembrano un errore. **DA VALIDARE** cosa distingue davvero le due formule. |
| Pagina contratto (n) | Chiusura | STATUS | La risoluzione generata | Both - logged | Documento generato dal team, da rileggere e firmare in FEQ da entrambe le parti | Sprint 4 | [I4b, I6] Da flow C.2.6–C.2.7 e backoffice riga 52, «genera accordo di risoluzione». Due firme: chiude la vicenda per entrambi. |
| Pagina contratto (n) | Chiusura | STATUS | Registrazione e archiviazione | Both - logged | «Registriamo la risoluzione all'Agenzia delle Entrate e archiviamo il contratto.» + SLA | Sprint 4 | [R6, I6] Da flow C.2.9–C.2.10. Ha la palla Cleclà. Stesso comportamento a SLA superato delle altre pagine. |
| Pagina contratto (n) | Chiusura | FEEDBACK | L'immobile torna disponibile | Venditori | «Il tuo annuncio è tornato online e le trattative che erano in stand-by si sono riaperte.» | Sprint 4 | [K7] Da flow B.16 e C.2.11. Aggancio allo stato S6b del profilo immobile, dove la sospensione era scattata alla firma. |
| Pagina contratto (n) | Chiusura | FEEDBACK | L'immobile torna disponibile | Acquirenti | «L'immobile è tornato disponibile per altri acquirenti.» | Sprint 4 | [K7] La stessa notizia dal lato di chi non ce l'ha più. Detta senza giri di parole. |
| Pagina contratto (n) | Chiusura | CONTENT | Le controparti delle trattative riattivate | Both - logged | — | Sprint 4 | [K7] **Punto 34.** Le trattative in stand-by hanno una controparte dall'altro lato, che si vede riaprire una trattativa senza sapere perché. Serve una notifica dedicata, e nel flow non c'è. Contenuto da scrivere quando il punto si chiude. |

### Lo stato annullato (K7)

| Pagina | Block | Type | Elemento | Target | Contenuto | Sprint | Note |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Pagina contratto (n) | K7 | STATUS | Causa e data | Both - logged | «Contratto annullato il [GG/MM] per [recesso di [Nome] / inadempimento di [Nome] / mancato avveramento della [condizione]]» | Sprint 4 | [K7] Foglio Priority guides riga 323, «motivazioni annullamento». Quattro cause possibili, dette con il nome della persona dove c'è una persona: l'auditabilità vale anche nella chiusura. Il flow archivia l'inefficacia con un nodo suo, distinto da quelli di recesso e inadempimento (E.2.10 contro B.15 e C.2.10): qui i tre confluiscono in K7 e la causa resta scritta sulla riga, perché per l'utente la pagina da guardare è la stessa e cambia solo perché il contratto è caduto. |
| Pagina contratto (n) | K7 | LIST | Documenti allegati | Both - logged | Documento di recesso · documento di inadempimento · autocertificazione di mancato avveramento · accordo di risoluzione · ricevuta di registrazione · contratto preliminare originale | Sprint 4 | [K7] Righe 324–325 del foglio Priority guides. Tutti scaricabili, da entrambe le parti, senza scadenza: sono gli atti di una vicenda che può avere seguiti legali. |
| Pagina contratto (n) | K7 | ACTION | Pagamento ancora aperto | Both - logged | «Devi ancora pagare [X] € a [Nome]» + azione | Sprint 4 | [K7] Riga 326 del foglio Priority guides, «richiesta di pagamento». È il punto in cui uno stato terminale contiene ancora un'azione: K7 diventa di sola lettura quando l'ultimo pagamento è confermato. |
| Pagina contratto (n) | K7 | CONTENT | Cosa puoi fare adesso | Venditori | «Il tuo annuncio è online. Se vuoi, aggiorna il prezzo o le condizioni prima di ricevere nuove richieste.» | Sprint 4 | [K7] E1 in uno stato terminale: un'uscita utile invece di un vicolo cieco. Porta al profilo immobile. |
| Pagina contratto (n) | K7 | CONTENT | Cosa puoi fare adesso | Acquirenti | «Le tue ricerche salvate sono ancora attive. Riprendi da lì.» | Sprint 4 | [K7] Porta ai Preferiti. Stessa logica dal lato acquirente. |
| Pagina contratto (n) | K7 | LINK | Supporto | Both - logged | «Hai bisogno di chiarimenti su come è andata?» → assistenza | Sprint 4 | [K7] E5 nel punto in cui il rapporto con la piattaforma può essere finito male. |

**Checklist Appendice A** — Ruolo sì · Tappa sì · Azione richiesta sì · Quantità proporzionata: presidiata con la
sequenza a stati, che mostra un passaggio alla volta invece di tutto il percorso · Perché chiaro sì · Errori
prevenuti sì (scomposizione dei costi prima della conferma, confronto con l'attesa, punto di non ritorno
dichiarato, gradino di dialogo prima di iniziare) · Supporto sì, ed è l'unico punto della fase in cui
l'escalation al team è la risposta giusta · Pattern P2, P3, P4, P5 · Stato visibile sì · CTA specifici sì.
**10/10**.

---

## PG 4 — Conclusione del contratto

**Job-to-be-done**: far capire alle due parti che il preliminare è efficace, far pagare la fee Cleclà, consegnare
la lista dei documenti che servono al notaio e il contatto diretto dell'altra parte, e accompagnarle fuori dalla
piattaforma.

**Ruolo**: condivisa, con importi diversi per ruolo · **Tappa**: Contratto, in uscita ·
**Unità atomiche**: Budget, Documenti.

**Posizione presa**: è la pagina in cui Cleclà chiude il suo servizio, quindi la sua forma è un **passaggio di
consegne**: cosa è stato fatto, cosa resta da fare, con chi, con quali documenti. Il rischio da presidiare è la
pagina di festeggiamento con un pagamento dentro, che lascerebbe l'utente senza le informazioni operative che gli
servono per i mesi successivi. Lo stato si chiama «Contratto efficace», per la ragione del punto 29.

### Header e stato

| Pagina | Block | Type | Elemento | Target | Contenuto | Sprint | Note |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Conclusione contratto | Header | CONTENT | Titolo pagina | Both - logged | «Contratto efficace · [Tipologia] in [Via], [Comune]» | Sprint 4 | Foglio Pagine riga 45: la pagina «si genera all'avveramento di tutte le condizioni sospensive». Il titolo dice lo stato giuridico raggiunto, invece di «compravendita avvenuta», che non è ancora vero (punto 29). |
| Conclusione contratto | Header | STATUS | Stepper percorso | Both - logged | «Sei qui: Contratto» con la tappa in chiusura | Sprint 4 | P3. Il rogito compare come passaggio successivo fuori dalla piattaforma, dichiarato, in sola lettura. |
| Conclusione contratto | Header | STATUS | A che punto siamo | Both - logged | Condizioni avverate ✓ → **Provvigione da pagare** → Documenti per il notaio → Rogito, fuori da Cleclà | Sprint 4 | Quattro passi, di cui l'ultimo fuori perimetro. Dichiararlo evita che l'utente cerchi in piattaforma una funzione che non esiste. |
| Conclusione contratto | Header | STATUS | Etichetta di responsabilità | Both - logged | «Tocca a entrambi» (provvigione) · «Ci pensiamo noi» (controllo della documentazione) · «Tocca a voi due» (rogito) | Sprint 4 | Stesso componente delle altre pagine. L'ultima variante è nuova e serve: dalla fine di questa pagina in poi la responsabilità è delle due parti insieme, fuori dalla piattaforma. |
| Conclusione contratto | Header | LINK | Torna al contratto | Both - logged | «Vedi il contratto e le condizioni» → Pagina contratto (n), stato K5 | Sprint 4 | La pagina contratto resta la fonte dello storico. Questa è la pagina delle azioni finali. |

### Dove siete arrivati

| Pagina | Block | Type | Elemento | Target | Contenuto | Sprint | Note |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Conclusione contratto | Traguardo | CONTENT | Cosa è appena successo | Both - logged | «Tutte le condizioni sospensive sono avverate. Il contratto preliminare è efficace e vincolante per entrambi.» | Sprint 4 | Da flow F.1. Detto una volta, in tono asciutto: la persona ha appena passato mesi ad aspettare, e quello che vuole sapere è cosa cambia. |
| Conclusione contratto | Traguardo | LIST | Le condizioni avverate, con le date | Both - logged | Una riga per condizione: nome, data dell'avveramento, chi l'ha comunicata, documento allegato | Sprint 4 | La prova che il traguardo è reale. È anche quello che l'utente porta al notaio per dimostrare l'efficacia, quindi va esportabile insieme alla checklist. |
| Conclusione contratto | Traguardo | CONTENT | Cosa manca ancora | Both - logged | «Manca il rogito: l'atto definitivo che si firma dal notaio, entro il [data del rogito concordata]. Da qui in avanti vi coordinate voi due, noi restiamo a disposizione per i documenti.» | Sprint 4 | Il cuore del punto 29. La data del rogito arriva dalle condizioni concordate in trattativa, dove era dichiarata come «un entro, non un appuntamento fisso»: la riga lo ripete, perché a distanza di mesi il fraintendimento torna. |

### La provvigione Cleclà

| Pagina | Block | Type | Elemento | Target | Contenuto | Sprint | Note |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Conclusione contratto | Provvigione | CONTENT | Quanto devi | Venditori | «**[X] €** + IVA — 1% del prezzo di vendita, con un minimo di 2.000 €» | Sprint 4 | Tabella dei costi dei Termini e Condizioni, allegato 1. Cifra calcolata sul prezzo concordato. Foglio Priority guides riga 327, «pagamento fee venditore». |
| Conclusione contratto | Provvigione | CONTENT | Quanto devi | Acquirenti | «**[Y] €** + IVA — 2% del prezzo di acquisto, con un minimo di 4.000 €» | Sprint 4 | Stessa fonte. Riga 328, «pagamento fee acquirente». Le due percentuali sono diverse e va detto senza giustificarlo qui: il dettaglio sta nei T&C, che l'utente ha accettato. |
| Conclusione contratto | Provvigione | CONTENT | Perché la paghi adesso | Both - logged | «La nostra provvigione è dovuta a trattativa conclusa, con un contratto preliminare valido ed efficace. Da oggi lo è.» | Sprint 4 | E3. Riconcilia le due fonti che sembravano dire cose diverse: i T&C, Capitolo 2 punto 3, dicono «valido ed efficace», il foglio User Stories dice «all'avveramento delle condizioni sospensive». Un preliminare con sospensive pendenti non è efficace, quindi le due frasi indicano lo stesso momento. |
| Conclusione contratto | Provvigione | CONTENT | Cosa include | Both - logged | «Include tutto quello che abbiamo fatto fino a qui e il coordinamento fino al rogito. Non include perizie, consulenze tecniche o l'atto notarile.» | Sprint 4 | T&C, Capitolo 2 punto 3: la provvigione «non include compensi per attività tecniche, peritali o consulenziali specialistiche». Il perimetro va detto qui, dove l'utente paga. |
| Conclusione contratto | Provvigione | ACTION | Paga | Both - logged | V: «Paga [X] € + IVA» · A: «Paga [Y] € + IVA» | Sprint 4 | P5. → Checkout esistente (foglio Pagine riga 36, Stripe), carta o bonifico. Da MVP riga 38: pagamento del 100% all'avveramento delle sospensive. |
| Conclusione contratto | Provvigione | CONTENT | Bonifico | Both - logged | «Con bonifico la fattura arriva quando riceviamo la quietanza, di solito 2–3 giorni lavorativi.» | Sprint 4 | Da MVP riga 38: con bonifico serve la quietanza per il codice transazione. Stessa riga già usata nella PG 4 della Trattativa: dire il ritardo prima evita il ticket. |
| Conclusione contratto | Provvigione | STATUS | Scadenza e reminder | Both - logged | «Da pagare entro il [GG/MM]. Mancano [X] giorni.» | Sprint 4 | E4. Reminder automatico via email da MVP riga 17, «reminder pagamento provvigione». **DA VALIDARE**: il termine di pagamento. |
| Conclusione contratto | Provvigione | STATUS | Lo stato dell'altra parte | Both - logged | «[Nome]: provvigione pagata il [GG/MM]» oppure «[Nome] non ha ancora pagato» | Sprint 4 | Trasparenza dei punti di convergenza, come in tutta la fase. **Punto 37**: va deciso se il pagamento di una parte ha una dipendenza con quello dell'altra. Nel flow F.3 compaiono in parallelo senza dipendenze dichiarate, e questa riga assume che siano indipendenti. |
| Conclusione contratto | Provvigione | ACTION | Fattura | Both - logged | «Scarica la fattura» | Sprint 4 | Da MVP riga 7, checklist pagamenti: la fattura di provvigione è una delle voci che il notaio chiede. Finisce anche nella checklist del rogito, gruppo D. |
| Conclusione contratto | Provvigione | CONTENT | Il caso senza condizioni sospensive | Both - logged | La pagina si apre con la provvigione già pagata e senza il blocco delle condizioni | Sprint 4 | Da flow A.2 → A.3: senza sospensive la fattura Cleclà parte insieme alla registrazione, quindi mesi prima. Due aperture della stessa pagina. Lo stato di partenza è K2. |
| Conclusione contratto | Provvigione | CONTENT | Help contestuale (P7) | Both - logged | «Perché le due percentuali sono diverse?» · «Cosa succede se non pago?» | Sprint 4 | Due helper, max 280 caratteri più link alla FAQ. Il secondo è la domanda che nessuno fa e che tutti si pongono. **DA VALIDARE** la risposta con il team. |

### I documenti per il notaio

| Pagina | Block | Type | Elemento | Target | Contenuto | Sprint | Note |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Conclusione contratto | Documenti notaio | CONTENT | Titolo e ruolo del blocco | Both - logged | «I documenti che il notaio vi chiederà» + «[N] di 19 già pronti» | Sprint 4 | **Ipotesi di lavoro del 25/09 sul punto 33**: la lista vive qui. Contatore sulle righe pertinenti, come nell'Archivio: fatti = disponibili, denominatore = righe pertinenti. |
| Conclusione contratto | Documenti notaio | CONTENT | Come funziona questa lista | Both - logged | «Non serve caricare niente qui. Quello che è già in piattaforma lo trovi col link, per il resto ti diciamo chi lo rilascia.» | Sprint 4 | E3, e presidia il rischio della terza superficie di caricamento. Il rogito avviene fuori da Cleclà, quindi la lista è una checklist da spuntare e portare, non un archivio nuovo. |
| Conclusione contratto | Documenti notaio | STATUS | Tre stati per riga | Both - logged | Già in piattaforma, con il link · Da richiedere, con chi lo rilascia e dove · A carico di Cleclà | Sprint 4 | Tre stati al posto di «ok / mancante»: su un certificato che si chiede in comune, «da richiedere» descrive un passaggio da fare, mentre «mancante» suonerebbe come una colpa dell'utente. |
| Conclusione contratto | Documenti notaio | LIST | Gruppo A — Identità e stato civile (5 voci) | Both - logged | Carta d'identità e codice fiscale di tutti i venditori e acquirenti · estratto per riassunto dell'atto di matrimonio, in carta libera, dal comune di celebrazione · certificato di stato libero, in carta libera · permesso di soggiorno non scaduto, se straniero residente in Italia · poteri di firma, se compra o vende una società | Sprint 4 | P2: quattro gruppi chiusi, si apre quello che serve. Da MVP riga 7, checklist Notaio. Le carte d'identità sono già in piattaforma dalla Preparazione alla firma. Le altre quattro sono documenti personali: vanno nell'**Archivio documentazione personale**, che oggi ha due sole sezioni (ID e Privacy). **Punto 40.** |
| Conclusione contratto | Documenti notaio | LIST | Gruppo B — L'immobile (7 voci) | Both - logged | Visura storica catastale · planimetria · APE · copia di provenienza (atto di acquisto, divisione, dichiarazione di successione) · relazione tecnica della due diligence o RRE · certificato di morte a uso conservatoria, se l'immobile arriva da una successione · certificato di destinazione urbanistica, solo per i terreni | Sprint 4 | Le prime cinque sono già nell'Archivio dell'immobile e la riga porta lì. Le ultime due sono condizionali e compaiono solo nei casi che le richiedono: E2, niente righe che non possono capitare. |
| Conclusione contratto | Documenti notaio | LIST | Gruppo C — Contratto (3 voci) | Both - logged | Contratto preliminare firmato · documento di avvenuta registrazione · dichiarazione di inesistenza di arretrati condominiali | Sprint 4 | Le prime due sono in piattaforma dalla fine della Trattativa. La terza la rilascia l'amministratore di condominio, e la riga lo dice: è la voce che in pratica arriva per ultima. |
| Conclusione contratto | Documenti notaio | LIST | Gruppo D — Pagamenti e mediatore (4 voci) | Both - logged | Mezzi di pagamento del prezzo (assegni o bonifico) · dati del mediatore · mezzi di pagamento al mediatore, con la contabile in caso di bonifico · fattura di provvigione | Sprint 4 | Da MVP riga 7, checklist pagamenti. I dati del mediatore e la fattura li fornisce Cleclà e si compilano da sé: la riga nasce già verde. I mezzi di pagamento del prezzo li predispongono le parti con la banca. |
| Conclusione contratto | Documenti notaio | ACTION | Esporta la lista | Both - logged | «Scarica la lista (PDF)» | Sprint 4 | Da MVP riga 7, «export riepilogo in PDF». È la lista che l'utente stampa, porta dal notaio e usa come promemoria per le telefonate al comune: l'export è l'azione principale del blocco. |
| Conclusione contratto | Documenti notaio | LINK | Dove sono i documenti | Both - logged | «Documentazione dell'immobile» · «I tuoi documenti personali» | Sprint 4 | I due archivi restano le case dei documenti. Regola uno-e-solo-uno: qui vive la lista, lì vivono i file. |
| Conclusione contratto | Documenti notaio | CONTENT | Cosa cambia nell'Archivio | Both - logged | — | Sprint 4 | Conseguenza dell'ipotesi sul 33: l'Archivio dell'immobile tiene oggi un elenco informativo di nove voci sul rogito, che diventa una duplicazione. Si riduce a un rimando a questa pagina. **Da applicare alla PG dell'Archivio**, come vuole il workflow E. |

### Il controllo finale di Cleclà

| Pagina | Block | Type | Elemento | Target | Contenuto | Sprint | Note |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Conclusione contratto | Controllo finale | STATUS | Verifica in corso | Both - logged | «Controlliamo un'ultima volta la documentazione prima che la portiate dal notaio.» + SLA | Sprint 4 | Da MVP riga 35, che è l'unica fonte di questo passaggio: sul flow non compare. Ha la palla Cleclà. Check manuale, come dice la riga stessa. |
| Conclusione contratto | Controllo finale | STATUS | Esito per documento | Both - logged | Verificato · da rifare, con il motivo · non leggibile, con la richiesta di ricaricarlo | Sprint 4 | Da MVP riga 35: «evidenza stato documenti (ok / mancante / non leggibile)». E4: l'esito negativo dice il motivo specifico e l'uscita, non solo che qualcosa non va. |
| Conclusione contratto | Controllo finale | FEEDBACK | Alert su documenti obsoleti | Both - logged | «La [visura] è del [data]: il notaio ne chiede una recente. Conviene rifarla adesso.» | Sprint 4 | Da MVP riga 35, «alert + notifica per file obsoleti o incompleti». Qui il dato c'è: la data di caricamento è nell'Archivio e la data del rogito è una condizione concordata. È lo stesso alert che l'Archivio aveva lasciato aperto per mancanza di quei due dati. |
| Conclusione contratto | Controllo finale | STATUS | Badge «Documentazione validata» | Both - logged | Badge in pagina e in bacheca, per entrambi i profili | Sprint 4 | Da MVP riga 35, use case: «un badge Documentazione validata appare nella dashboard per entrambi i profili». È il blocco di bacheca nuovo che questa PG richiede. |
| Conclusione contratto | Controllo finale | FEEDBACK | SLA superato | Both - logged | «Ci stiamo mettendo più del previsto» + apertura dell'assistenza | Sprint 4 | Stessa regola delle altre pagine sulle righe a carico di Cleclà. |

### Trova un notaio

| Pagina | Block | Type | Elemento | Target | Contenuto | Sprint | Note |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Conclusione contratto | Notaio | ACTION | Scorciatoia a Trova tecnico | Both - logged | «Vi serve un notaio per [Comune]? [Cerca notai]» (un tap imposta documento e zona) | Sprint 4 | Foglio Priority guides riga 330, «trova un notaio». È Trova tecnico con il documento «rogito di compravendita», già fra i filtri della riga 8 dell'MVP. La regola del 18/08 dice che la ricerca parte sempre vuota, quindi il rimando prende la forma della scorciatoia, che è l'unica precompilazione ammessa. **Unica aggiunta alla PG Trova tecnico esistente.** |
| Conclusione contratto | Notaio | CONTENT | Il notaio lo scegliete voi | Both - logged | «Il notaio lo scegliete voi due, insieme. Noi vi diamo l'elenco di chi lavora nella zona, senza commissioni.» | Sprint 4 | Metafora del copilota: il volante resta all'utente. La seconda frase è il principio già fissato per Trova tecnico, dove Cleclà non prende commissioni sui professionisti. |
| Conclusione contratto | Notaio | CONTENT | Chi paga il notaio | Both - logged | «L'atto notarile lo paga chi compra, salvo diverso accordo fra voi.» | Sprint 4 | **DA VALIDARE**: non compare né nei T&C che ho letto né nel flow. È la domanda che arriva subito dopo «cerca un notaio», quindi la riga va scritta, con la risposta del cliente. |

### Il contatto diretto

| Pagina | Block | Type | Elemento | Target | Contenuto | Sprint | Note |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Conclusione contratto | Contatti | CONTENT | Cosa cambia da adesso | Both - logged | «Da qui in avanti vi coordinate direttamente. Vi diamo i vostri contatti: da organizzare insieme ci sono il notaio, la data del rogito e la consegna delle chiavi.» | Sprint 4 | Da flow F.4, dove è una mail di recap. È un **cambio di regime**: in tutta la trattativa il contatto diretto era deliberatamente assente, e il passaggio va dichiarato a entrambi invece di comparire. |
| Conclusione contratto | Contatti | CONTENT | Il contatto dell'altra parte | Both - logged | Nome e cognome, telefono, email | Sprint 4 | In pagina oltre che via mail: una mail si perde e questo dato serve per settimane. Da flow F.4, dove arriva a entrambe le parti. |
| Conclusione contratto | Contatti | CONTENT | Perché ve li diamo adesso | Both - logged | «Fino a qui tutto passava dalla piattaforma, per tenere traccia degli accordi. Adesso gli accordi sono firmati e il resto si organizza meglio parlandosi.» | Sprint 4 | E3. Spiega la regola precedente invece di smentirla in silenzio, che è quello che farebbe perdere fiducia a chi si era fidato della mediazione. |
| Conclusione contratto | Contatti | STATUS | Mail di recap | Both - logged | Email a entrambe le parti con contatto, condizioni avverate, lista dei documenti e link alla pagina | Sprint 4 | Da flow F.4, che prevede la mail per ruolo. Contenuto identico per i due, cambia solo il contatto riportato. |

### Cosa succede all'annuncio

| Pagina | Block | Type | Elemento | Target | Contenuto | Sprint | Note |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Conclusione contratto | Annuncio | STATUS | Chiusura definitiva | Venditori | «Il tuo annuncio è chiuso definitivamente e le trattative che erano in stand-by si sono chiuse con lui.» | Sprint 4 | Da flow F.4, «chiusura definitiva annuncio immobile e trattative sospese». La sospensione era scattata alla firma (stato S6b del profilo immobile), qui diventa definitiva. |
| Conclusione contratto | Annuncio | STATUS | Come finisce il profilo immobile | Venditori | Archiviato, con lo stato «impegnato, rogito da fare» | Sprint 4 | Punto 29. Il flow dice «archiviazione profilo immobile come venduto», e «venduto» arriva dopo il rogito. `revisione-wireframe-sprint2.md` conferma che «annuncio venduto non esiste, l'immobile viene archiviato». **DA VALIDARE** l'etichetta dello stato. |
| Conclusione contratto | Annuncio | CONTENT | Le altre trattative | Venditori | — | Sprint 4 | **Punto 34.** Le trattative in stand-by hanno una controparte che si vede chiudere una trattativa senza sapere perché. Serve una notifica dedicata a quelle persone, e nel flow non c'è. Contenuto da scrivere quando il punto si chiude. |
| Conclusione contratto | Annuncio | CONTENT | E se il rogito non si fa | Both - logged | — | Sprint 4 | **DA VALIDARE.** Il preliminare è efficace, la provvigione è pagata, l'annuncio è chiuso: se poi il rogito non avviene, oggi non è definito cosa succede all'immobile né alla provvigione. Il flow finisce prima. Domanda per il cliente. |

### Supporto

| Pagina | Block | Type | Elemento | Target | Contenuto | Sprint | Note |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Conclusione contratto | Supporto | CONTENT | Restiamo per i documenti | Both - logged | «Anche dopo il rogito trovate qui tutti i documenti della compravendita.» | Sprint 4 | L'archivio è la ragione per cui un utente torna sulla piattaforma dopo mesi, e dirlo adesso è quello che lo fa tornare. |
| Conclusione contratto | Supporto | LINK | FAQ e assistenza | Both - logged | «Domande sul rogito» → FAQ, tema «Contratto» · floating button di assistenza | Sprint 4 | P6 ed E5. |

**Checklist Appendice A** — Ruolo sì · Tappa sì · Azione richiesta sì (pagamento, documenti, ricerca del notaio) ·
Quantità proporzionata sì (19 voci in quattro gruppi, righe condizionali nascoste quando non pertinenti) · Perché
chiaro sì (perché si paga adesso, perché i contatti arrivano adesso) · Errori prevenuti sì (alert su documenti
obsoleti, scadenza della provvigione) · Supporto sì · Pattern P2, P3, P5, P7 · Stato visibile sì · CTA specifici
sì. **10/10**.

---

## Cosa non diventa una pagina nuova

**Trova un notaio.** È Trova tecnico con il documento «rogito di compravendita» tra i filtri già previsti dalla
riga 8. Serve solo la scorciatoia dalla Conclusione.

**Una guida al contratto.** La Guida alla trattativa contiene già il blocco «Se qualcosa va storto» con recesso,
inadempimento e inefficacia spiegati in una riga ciascuno, ed è dichiarata fonte canonica di quelle spiegazioni.
Aggiungere una guida al contratto duplicherebbe quel contenuto, e la regola del workflow E dice che aggiungere
una pagina implica alleggerirne altre. La proposta: le spiegazioni restano nella guida, la pagina contratto le
richiama con P7 e la pagina FAQ apre un tema «Contratto». Se il team preferisce una pagina, il modo giusto è
estendere la guida esistente a «Guida alla trattativa e al contratto», non affiancarne una seconda.

**Un archivio dei documenti del rogito.** Con l'ipotesi del 25/09 la lista delle 19 voci vive nella Conclusione
contratto e legge dai due archivi esistenti, quello dell'immobile e quello personale. Nessuna superficie di
caricamento nuova, e l'Archivio dell'immobile resta com'è, con una riduzione: il suo elenco informativo di nove
voci sul rogito diventa un rimando alla Conclusione.

---

## Cosa serve fuori da queste PG

**I blocchi di bacheca della fase.** La PG Trattativa ha già segnalato che il catalogo dei blocchi copre lo
Sprint 2 e che trattativa, contratto e rogito sono ingombri dichiarati nello stepper. Per la Finalizzazione
servono almeno: «Comunica l'esito di [condizione]», «[Condizione] scade fra X giorni», «In attesa di [Nome] su
[condizione]», «Contratto efficace: paga la provvigione», «Mancano N documenti per il rogito», «Inadempimento
segnalato: ci stiamo occupando noi», «Contratto annullato». Il pattern è fissato (nome dell'immobile più tappa in
testa, titolo che dice cosa fare, una azione primaria), quindi è lavoro di compilazione.

**Il badge «Documentazione validata» in dashboard.** Da MVP riga 35, use case: compare a entrambi i profili quando
il controllo finale ha esito positivo. È l'unico elemento di questa fase che vive in bacheca come stato e non come
blocco d'azione, quindi va aggiunto al catalogo come componente a sé.

**La scorciatoia notaio su Trova tecnico.** Una chip in più nel blocco delle scorciatoie della pagina Trova
tecnico, che al tap imposta documento «rogito di compravendita» e il comune dell'immobile. Unica modifica a una PG
già chiusa.

**Tre citazioni da correggere nella PG Trattativa.** Verificate sul file MVP: la riga 32 è «Richiesta di
riapertura trattativa», la 34 è «Registrazione contratto preliminare sul portale AdE» e la 36 è «Comunicazione
avveramento / non avveramento condizione sospensiva». Quindi: «Da MVP riga 32: la registrazione è manuale, la fa il
team Cleclà» va corretto in riga 34, che nei requisiti definitivi dice «(manuale da parte del Team Cleclà)»;
«Visibili a entrambe le parti, da MVP riga 32» va corretto in riga 34, la cui use case dice che entrambi ricevono
conferma e possono scaricare la ricevuta; «Il rimando a "Trova notai" è previsto da MVP riga 34» va corretto in
riga 36, che lo elenca fra i propri outcome. Il punto 28 poggia sulla riga 34, non sulla 32.

**Le correzioni al foglio Contenuti e all'MVP.** «Pagina contratto annullato» diventa uno stato e la riga va
aggiornata. Le use case della riga 34 dell'MVP parlano di registrazione automatica e vanno riscritte sul manuale.
La riga 37 dell'MVP descrive la caparra confirmatoria e va riscritta su clausola penale al 5% e multa
penitenziale al 5%. Le etichette «Pop-up inadempienza» (foglio Priority guides, riga 322) e «attiva flusso di
inadempienza» (Struttura backoffice, riga 52) vanno allineate a «inadempimento», insieme ai nodi omonimi della
board dello user flow.

**La discrepanza sul 3% dovuto a Cleclà.** Punto 38. Riguarda la Guida alla trattativa e la PG 3 della Trattativa,
quindi si chiude fuori da questo perimetro. Va messa in coda alle correzioni di quell'epica, con priorità alta:
è un costo di migliaia di euro che oggi l'utente non legge prima di firmare.

**Lo storico dei pagamenti.** Le pagine «Stato pagamenti» dei due ruoli (righe 22 e 32) in questa fase si
riempiono con registrazione, fee ed eventuali penali. Sono a Sprint 2 nel foglio: va verificato che la struttura
regga le voci della Finalizzazione.

---

## Punti aperti

Stato dopo il check sulla KB del 25/09.

| # | Punto | Stato |
|---|---|---|
| 26 | Importo e sede della clausola penale | **Chiuso sul check KB**, con una riserva: 5% del prezzo, valore fisso del template, art. 1382 c.c., e sta nel testo del preliminare invece di concordarsi. Le fonti che lo dicono non sono leggibili da questa sessione, quindi le righe di schermata che riportano la cifra restano DA VALIDARE |
| 27 | Base di calcolo della quota proporzionale della registrazione | **Da confermare**, con una lettura che regge: la base è il 5% di penale o multa. Era bloccante, ora no |
| 28 | Registrazione AdE manuale o automatica | **Chiuso.** Manuale. Restano da correggere le use case dell'MVP |
| 29 | Nome del traguardo finale e stato del profilo immobile | **Corroborato in parte.** L'archiviazione ha una fonte, i due nomi restano una proposta |
| 30 | Finestra fra scadenza di una condizione e segnalazione di inadempimento | Aperto. In KB ci sono soglie analoghe per la Trattativa (3 giorni di silenzio, 48 ore fra solleciti) che non si riusano senza conferma |
| 31 | Chi può segnalare l'inefficacia | Aperto |
| 32 | Owner dell'avveramento | **Chiuso, con una correzione.** La prelazione ha due owner possibili |
| 33 | Dove vivono i documenti del rogito | **Ipotesi di lavoro del 25/09**: nella Conclusione contratto, che legge dai due archivi esistenti. Da validare. L'elenco di nove voci nell'Archivio si riduce a un rimando |
| 34 | Chi avvisa le controparti delle trattative in stand-by alla chiusura definitiva | Aperto |
| 35 | Per quali condizioni il documento di avveramento è obbligatorio | Aperto |
| 36 | Registrazione del recesso e multa penitenziale | **Chiuso.** La multa è il 5% del prezzo (check KB). La registrazione la paga la parte che recede, Acquirente o Venditore secondo chi esercita: **ipotesi di lavoro del 25/09**, da validare |
| 37 | Dipendenza fra il pagamento della fee delle due parti | Aperto |
| 38 | Il 3% con minimo 6.000 € dovuto a Cleclà sul recesso in pendenza delle sospensive non è dichiarato nella guida alla trattativa | **Nuovo.** Da chiudere nella Guida e nella PG 3 della Trattativa, prima della firma del preliminare |
| 39 | Terminologia: «inadempimento» per tutta la PG, come in `overview.md` | **Applicato**, da confermare. Board dello user flow e foglio backoffice usano ancora «inadempienza» |
| 40 | L'Archivio personale ha le righe per i documenti personali del rogito (stato libero, atto di matrimonio, permesso di soggiorno, poteri di firma, certificato di morte) | **Nuovo**, derivato dall'ipotesi sul 33. Nel foglio Contenuti quella pagina ha due sole sezioni |
| 41 | Chi inserisce l'IBAN nei pagamenti fra le parti | **Nuovo**, emerso scrivendo la PG 3. La board mette l'inserimento dell'IBAN sul rail di chi paga, in entrambi i rami (B.10 e C.2.1). La sequenza che regge è l'opposta: chi riceve dà l'IBAN, chi paga esegue il bonifico e carica la ricevuta, chi riceve conferma. Disegnata così, da confermare |
| 42 | Inadempimento smentito: il contratto riprende o si scioglie | **Nuovo**, emerso scrivendo la PG 3. Il flow C.1.9, ramo «inadempienza confermata? NO», manda a «riattiva annuncio e trattative in stand-by», che è quello che succede quando il contratto cade. Se la segnalazione non è confermata il contratto dovrebbe tornare attivo |

Le voci marcate «ipotesi di lavoro» sono decisioni prese per sbloccare la scrittura, non risposte del cliente. Ogni
riga di contenuto che ci poggia sopra è marcata **DA VALIDARE** nella colonna Note, così se l'ipotesi cade si
trova cosa cambiare. Oltre a quelle, sono marcate DA VALIDARE le righe che aprono una domanda emersa scrivendo:
la finestra di sollecito e le sue soglie, la finestra di correzione di una dichiarazione di avveramento, il limite
di una proroga per condizione, cosa succede se la multa penitenziale non viene pagata, cosa distingue le due
formule di registrazione dell'inadempimento, il termine di pagamento della provvigione, chi paga il notaio, e
cosa succede se il rogito non si fa dopo che la provvigione è stata pagata.

## Cosa serve prima dei wireframe

I contenuti delle quattro PG sono scritti. Le righe marcate DA VALIDARE sono disegnabili con il valore
provvisorio: nessuna di esse cambia la struttura di un blocco, cambiano una cifra, una soglia o chi vede una CTA.

Tre cose vanno chiuse prima di posare i wireframe, e sono tutte domande per il cliente.

Il **27** e la parte del **36** sull'aliquota decidono le cifre della schermata di scomposizione dei costi del
recesso, che è la schermata più delicata dell'epica. Si può disegnare con i valori calcolati sul 5%, a patto di
tenere la conferma come gate prima della consegna.

Il **38** ha priorità su tutto il resto, e non riguarda questa epica: la Guida alla trattativa spiega il recesso
nominando solo la multa penitenziale, quindi chi la legge stima il costo di un'uscita per difetto di almeno
6.000 €. Va corretto lì, prima della firma del preliminare.

Il **42** decide uno stato della PG 3, e se la risposta fosse che il contratto si scioglie anche con
l'inadempimento smentito, il ramo I7 va riscritto.

Sull'ordine di lavorazione: conviene partire dalla **PG 1**, che fissa i componenti riusati da tutte le altre
(riga di condizione con scadenza, blocco prossima scadenza, etichetta di responsabilità, badge di stato). La
**PG 3** pesa più delle altre tre messe insieme: due percorsi multi-passaggio con stato per parte, e una schermata
di anteprima dei costi che vale da sola una sessione di wireframe.

Va aggiunto al conto quello che nasce fuori da queste PG: i sette blocchi di bacheca, il badge «Documentazione
validata» in dashboard per entrambi i profili, la scorciatoia notaio su Trova tecnico, le due righe dell'Archivio
personale e la riduzione dell'elenco rogito nell'Archivio dell'immobile.
