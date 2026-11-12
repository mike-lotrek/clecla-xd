# Pubblicazione annuncio: integrazione dei commenti rimasti (06/11/2026)

File Figma «Cleclà | UI», sezione «Pubblicazione annuncio» (4807:60382), ora in Sprint 3, `UI Layouts – WIP` (3764:8875). Era in Sprint 2, `UI Layouts – WIP` (4807:47146). La versione precedente è in `UI Layouts – Backup 06.11` (6588:13431). Le tavole sono state modificate sul posto, quindi i commenti interni restano agganciati.

Commenti letti: board feedback V.2 del 07/10 (sezione 3206:16206) e commenti aperti sulla sezione nel file UI. Le versioni V.3 e V.4 della board non contengono questa sezione.

## Tavole

| Tavola | Node ID |
|---|---|
| Nuovo immobile – D - 19 | 4920:76919 |
| Nuovo immobile – M - 22 | 4932:77838 |
| Nuovo immobile – D - 20 | 4932:78946 |
| Nuovo immobile – D - 21 | 4932:81616 |
| Stato · Ripeti sempre disattivato (eliminato il 10/11) | 6590:13498 |
| Nuovo immobile – M - 23 (nuova) | 6593:13670 |
| Nuovo immobile – M - 24 (nuova) | 6593:14048 |
| Note · D-19, M-22, D-20, D-21 (nuove) | 6590:13480, 6590:13486, 6590:13490, 6590:13494 |

## Commenti e cosa è stato fatto

| Dove | Commento | Esito |
|---|---|---|
| D-19, blocco informazioni | «togliere» (cliente, 12/10) | Tolto, anche in M-22 |
| D-19, alert | «Si e no»: si possono richiedere visite fuori dagli orari (cliente, 12/10) | Testo della card riscritto |
| D-19, alert | «sostituire libere con disponibili» (cliente, 24/10) | «fasce libere» non compare più |
| D-19, alert | «che tu decidi se accettare o rifiutare» non è fluido (cliente, 24/10) | Riscritto |
| D-19, testo card | Deve essere identico al banner? (cliente, 24/10) | No: ora sono diversi |
| D-19, calendario | Slot 8–21 per settimana, check «ripeti sempre», notifica prima che scada l'ultimo slot (Eleonora, 12/10) | Fatto. Vedi sotto per la notifica |
| D-19, Ricorrenza | Programmazione settimanale di default (cliente, 17/10) | «Ripeti sempre» attivo di default |
| D-19, stepper | «Aggiornare le voci» (cliente, 12/10) | Le voci del WIP erano già corrette. Corretto «Mancano 1 punti» in «Manca 1 punto su 5» |
| D-19, «Carica i documenti» | «A cosa serve questo qui?» (cliente, 11/10) | Tolto anche da M-22: il caricamento resta in Archivio (deciso il 06/11) |
| D-20, prezzo | «specificare che da qui può modificare il prezzo» (cliente, 24/10) | Aggiunto il testo, anche in D-21 |
| D-20, Andamento | Togliere il blocco visualizzazioni (Marco, 08/10) | Tolto, anche in D-21 |

## Copy

- Alert: «Se non indichi le tue disponibilità, l’annuncio viene pubblicato comunque. Chi è interessato potrà proporti un orario e sarai tu a scegliere se accettarlo.»
- Testo della card: «Segna gli orari in cui puoi mostrare la casa: gli acquirenti li vedono e possono prenotare direttamente. Qualcuno potrebbe comunque proporti un orario diverso: anche in quel caso, decidi tu.»
- Check: «Ripeti sempre» · «Gli orari che hai segnato valgono per tutte le settimane, finché non li cambi. Per le assenze usa il blocco date.»
- Check disattivato: «Gli orari che hai segnato valgono solo per questa settimana.»
- Avviso: «I tuoi orari finiscono domenica 27 settembre. Aggiungine altri per continuare a ricevere prenotazioni.»
- Gestisci l'annuncio: «Da qui puoi modificare il prezzo dell’annuncio.»

## Altre modifiche

- Tolto «Ultime attività» in tutte le tavole (decisione già in CLAUDE.md).
- Footer da utente registrato su D-19, D-20, D-21: «Esci» al posto di «Accedi» e «Registrati».
- D-21: l'avviso di scadenza dell'incarico passa sotto la card «Il tuo annuncio è online».
- «Clecà» corretto in «Cleclà» nei link.
- M-22: «Sei qui: Verifica dell’identità» corretto in «Sei qui: Pubblicazione». Tolto il testo sull'indirizzo preciso, che su desktop non c'era.

## Scelte

- Calendario con il selettore a striscia, a selezione multipla: confermato il 06/11. Il commento di Eleonora è del 12/10, quando l'acquirente vedeva ancora la griglia; oggi acquirente e venditore usano lo stesso selettore.
- Tolti Durata dello slot e Fasce orarie, resi inutili dagli slot fissi di un'ora. Blocco date resta.

## Modifiche successive (06/11)

- Tolti «Carica i documenti» da D-19 e M-22 e «Prosegui» da D-20 e D-21.
- Tolta la scritta «Questa sezione la affrontiamo più avanti con l’epica Visite» con il suo segnale.
- Nuove tavole mobile: Nuovo immobile – M - 23 (6593:13670) per D-20 e M - 24 (6593:14048) per D-21. Il blocco prezzo riparte da quello mobile di M-20 (4908:15176), con le fasce di D-20.
- Fasce di prezzo portate a tre, come chiesto dal cliente l'11/10 sulla board («Sono solo tre fasce, quindi da rimuovere "poco cosigliato"», nodo 3206:13033): Consigliato 235.000–255.000 €, Non consigliato 255.001–295.000 €, Fuori mercato oltre 295.000 €. Vale per D-20, D-21, M-23, M-24 e per il componente `State comparison`.
- La sezione è ora in Sprint 3, `UI Layouts – WIP` (3764:8875), in cima, sopra Prenota Visita. I node ID non cambiano.

## Commenti del 26/09 integrati (V.1 della board)

- Nodo 2808:27218, D-20, D-21, M-23, M-24: box «Vuoi cambiare altro?» in «Gestisci l'annuncio». Testo: «Il prezzo è l’unica cosa che puoi modificare in autonomia. Per tutto il resto, scrivici cosa vuoi cambiare: valutiamo la richiesta e ti facciamo sapere.» Campo «Cosa vuoi cambiare?», bottone «Invia la richiesta». Stato di conferma «Richiesta inviata» (6599:7173): «L’abbiamo ricevuta. Ti scriviamo appena l’abbiamo valutata.»
- Nodo 2808:27218, D-21, M-24: avviso «L’incarico scade tra 60 giorni e si rinnova in automatico. Se non vuoi proseguire, comunicacelo almeno 30 giorni prima della scadenza.»
- Nodo 2808:26943, D-19, M-22: card «Stiamo preparando il tuo annuncio», con il testo proposto da Alice nel commento.

## CTA del prezzo (06/11)

«Invia la richiesta» sembrava valere anche per il prezzo. Il blocco prezzo ha ora il suo bottone «Salva il prezzo», in D-20, D-21, M-23 e M-24. Si attiva quando la cifra cambia. Stato di conferma «Prezzo salvato» (6606:7300): «Il nuovo prezzo è già sull’annuncio. Ai portali collegati pensiamo noi.» In D-20 e D-21 il blocco `State comparison` è stato staccato dal componente per poter aggiungere il bottone: il componente resta senza.

## Settimana tipo (10/11)

Il calendario delle disponibilità di D-19 e M-22 non mostra più date vere né la navigazione per settimana: è una settimana tipo. Si sceglie un giorno della settimana, poi sotto gli orari, a slot di un'ora dalle 8 alle 21 (l'ultimo è 20:00 – 21:00). Le scelte valgono per tutte le settimane, quindi «Ripeti sempre» è tolto, e con lui lo stato «Ripeti sempre disattivato» (6590:13498, eliminato) e l'avviso sull'ultimo orario in scadenza. Tolto anche lo stato «Già prenotato» e la sua voce in legenda: in una settimana tipo un orario non è legato a una data. «Blocco date» resta com'è.

| Tavola | Node ID |
|---|---|
| Calendario D-19 | 6589:13433 |
| Calendario M-22 | 6590:13356 |
| «Ripeti sempre» nascosto | 6589:13551, 6590:13473 |

Copy:
- Testo della card: «Scegli i giorni e gli orari in cui di solito puoi mostrare la casa: valgono per tutte le settimane, finché non li cambi. Gli acquirenti li vedono e possono prenotare direttamente. Qualcuno potrebbe comunque proporti un orario diverso: anche in quel caso, decidi tu.»
- Titolo del calendario: «La tua settimana tipo». Chip: «Lun» … «Dom» con il numero di orari. Sottotitolo: «Ogni mercoledì · scegli gli orari».

Se chi vende toglie un orario in cui ha visite già confermate, le visite restano e si apre la modale «Visite fuori dai nuovi orari» (5238:2954), scritto in nota.

Gli slot restano dalle 8 alle 21, come lato acquirente (confermato il 10/11).

## Blocco date: da select a lista (09/11)

Deciso il 10/11: per l'acquirente un giorno bloccato equivale a un giorno senza orari, quindi può comunque proporre un orario.

La select aperta del 06/11 (6608:7122) è stata tolta. «Blocco date» in D-19 e M-22 è ora una lista di periodi: chi vende aggiunge e toglie periodi, non sceglie un'opzione. Tolta l'etichetta «Ferie»: il 26/09 il cliente ha detto che il blocco va bene senza giustificazione.

Comportamento:
- «+ Blocca delle date» apre un selettore a intervallo: primo e ultimo giorno, due tocchi sulla stessa data per un giorno solo. Su desktop due mesi affiancati, su mobile un foglio dal basso con un mese alla volta (solo in nota).
- «Togli» rimuove un periodo.
- Nei giorni bloccati gli orari restano segnati ma non sono prenotabili. Finito il periodo tornano validi, senza toccare la settimana tipo.
- Se nel periodo ci sono visite confermate, prima di bloccare si apre la modale delle visite fuori orario del Calendario Venditore, adattata. Le visite restano in calendario.

| Tavola | Node ID |
|---|---|
| Blocco date in D-19 · lista con un periodo | 4920:77755 |
| Blocco date in M-22 | 4932:78169 |
| Stato · Nessuna data bloccata | 6678:7099 |
| Stato · Scegli le date (selettore a intervallo) | 6678:7111 |
| Modale · Visite nelle date bloccate (da 5238:2954) | 6678:7309 |

Copy:
- Titolo «Blocco date», testo «Nei giorni bloccati non ricevi prenotazioni. Finito il periodo, tornano validi gli orari che hai segnato.»
- Riga «Dal 24 dicembre al 6 gennaio», link «Togli». Vuoto: «Nessuna data bloccata.» Link «+ Blocca delle date».
- Selettore: «Scegli il primo e l’ultimo giorno in cui non puoi mostrare la casa. Per un giorno solo, tocca due volte la stessa data.» Riepilogo «Dal 24 dicembre al 6 gennaio · 14 giorni», bottoni «Annulla» e «Blocca queste date».
- Modale: «2 visite sono nelle date che vuoi bloccare» · «Le hai già confermate. Bloccando le date restano in calendario: puoi spostarle, disdirle oppure mantenerle.» · «Blocca le date e mantieni le visite».

D-19 si è allungata di 57 px, la section di 1.287 px; le section sotto sono state riposizionate con lo stacco di 1000 px.

## Disdetta dell'incarico (09/11)

L'avviso di D-21 e M-24 chiedeva di comunicare la disdetta senza dire come. Ora contiene il link «Non rinnovare l’incarico», che apre una modale di conferma. Dopo la conferma Cleclà manda una mail con data e ora, che fa da prova scritta. Fino al termine dei 30 giorni la disdetta si può annullare; dopo, il link sparisce.

| Tavola | Node ID |
|---|---|
| Avviso in D-21 | 4932:81640 |
| Avviso in M-24 | I6593:14247 |
| Stato · Incarico disdetto (alert Info) | 6681:7124 |
| Stato · Termine per la disdetta passato | 6681:7132 |
| Modale · Non rinnovare l’incarico (da 5238:2954) | 6681:7147 |

Copy (date di esempio: scadenza 15 gennaio 2027, termine 16 dicembre):
- Avviso: «L’incarico scade tra 60 giorni, il 15 gennaio 2027, e si rinnova in automatico. Se non vuoi proseguire, puoi disdirlo entro il 16 dicembre. **Non rinnovare l’incarico**»
- Modale: «Non vuoi rinnovare l’incarico?» · «L’incarico di mediazione scade il 15 gennaio 2027. Se non lo rinnovi:» · «l’annuncio resta online fino a quella data, poi lo togliamo da Cleclà e dai portali collegati;» · «le visite e le trattative in corso proseguono fino alla scadenza;» · «puoi cambiare idea fino al 16 dicembre.» · «Ti mandiamo una mail con la conferma della disdetta.» · bottoni «Mantieni l’incarico» e «Non rinnovare».
- Disdetto: «Hai disdetto l’incarico: scade il 15 gennaio 2027 e non verrà rinnovato. Ti abbiamo mandato una mail di conferma. **Annulla la disdetta**»
- Termine passato: «L’incarico scade il 15 gennaio 2027 e si rinnova in automatico. Il termine per disdirlo è passato: se vuoi parlarne, **scrivici**»

Da decidere col cliente e col legale:
- Se basta la disdetta in piattaforma o l'incarico chiede una forma precisa (PEC, raccomandata).
- Cosa succede a visite, trattative in corso e provvigione dopo la disdetta: le righe della modale sono una proposta.
- Se la disdetta è nei Functional Requirements dell'MVP: l'avviso viene da un commento del cliente del 26/09, il canale no.
- Dove porta «scrivici».

Non disegnati: la mail di conferma, il foglio mobile della modale.

## Punti da decidere

Superati il 10/11 dalla settimana tipo: la notifica sull'ultimo orario e «Ripeti sempre» attivo di default.

Col cliente:
- Visite confermate in un periodo bloccato: oggi restano in calendario, la modale propone di spostarle o disdirle.

Da definire:
- «Vuoi cambiare altro?»: quali modifiche sono ammesse e in quanto tempo il team risponde. In CLAUDE.md la modifica dopo il completamento è ancora «da valutare con i dev».
- Avviso dei 60 giorni: proposta disegnata il 09/11 (vedi «Disdetta dell'incarico»), forma e effetti da confermare.

Interni:
- Se togliere il blocco Andamento vale anche per eventuali dati simili in Bacheca: non verificato.

## Termini da registrare nel glossario

«La tua settimana tipo», «Ogni [giorno] · scegli gli orari», «Blocco date». «Ripeti sempre» non serve più (10/11). Il glossario non ha copy approvato per le disponibilità del venditore.
