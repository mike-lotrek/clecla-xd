# Avvisi e notifiche della fase Trattativa · censimento — e la tavola dell'acquirente in attesa

28/09/2026 · file **Cleclà | UI** (`0k5JkkrVwDydzvUoRHv8ye`), pagina `🚧 UI Layouts – WIP`, sezioni `PG2 · Pagina trattativa v2 · feedback 20/09 🚧` (`4371:29245`) e `PG2 · Pagina trattativa v2 · mobile 440 🚧` (`4435:165755`).

Nasce da due domande: se l'overlay di onboarding del venditore (`4418:165092`) debba avere altri casi simili nella fase Trattativa, e dalla mancanza della pagina dell'acquirente fra l'invio della proposta e la prima risposta del venditore.

## 1. Cosa dicono le fonti sugli avvisi

### Requirements — «Come funziona la trattativa»

Il documento non prevede **nessun** avviso e **nessuna** notifica. Descrive domande, condizioni generate, tempi tecnici e la logica della relazione tecnica. L'unico intervento attivo della piattaforma è lo **stallo** (sezione 8): dopo due proposte rifiutate Cleclà suggerisce la media. È già disegnato come T2b e T2c.

### Guide al venditore e all'acquirente (14/09)

Due eventi espliciti, entrambi non ancora disegnati in PG2:

1. **Notifica automatica 30 giorni prima della scadenza di una condizione sospensiva**, con proroga concordabile fra le parti.
2. **Avveramento della condizione segnalato in piattaforma** dalla parte che l'ha dichiarata.

### IMP · Impostazioni profilo (`2112:24863`, frame approvato)

È l'unica tassonomia approvata delle notifiche: otto categorie, ciascuna con canale Web e Mail.

| Categoria | Descrizione approvata |
|---|---|
| Profilo immobile | Aggiornamenti e richieste di informazione |
| Pubblicazione annuncio | Aggiornamenti sulla pubblicazione del tuo annuncio sui diversi portali |
| Gestione visita | Quando qualcuno prenota una visita e feedback di visita avvenuta |
| **Trattative** | **Quando un acquirente mostra interesse a trattare o invia un'offerta** |
| Contratto | Modifiche a contratti e documenti |
| **Recesso, inadempienza o altro** | **Flussi che bloccano temporaneamente il contratto** |
| Finalizzazione | Documenti, aggiornamenti, notaio, next step |
| Newsletter Cleclà | Guide, news e consigli |

### User flow

La sezione `Trattativa` della pagina Wireframe di Sprint 4 (`3559:9037`) contiene le quattro priority guides, non un diagramma di notifiche. Non esiste un documento di user story per l'epica.

## 2. Gli avvisi che esistono oggi in PG2 v2

Quindici istanze di `Alert` sulle tavole desktop, quasi tutte spente:

| Avviso | Dove | Stato |
|---|---|---|
| «Giulia Rossi ti ha fatto la prima proposta: prepara la tua risposta e inviala quando è completa.» Default/Info | D-0b, D-0c | visibile |
| «Marco Ferrero ha risposto alla tua proposta: tocca a te su tre punti.» Default/Info | D-1a / T3a | visibile |
| «Hai inviato la tua proposta a Marco Ferrero: ora tocca a lui.» Default/Info | D-0a (nuova) | visibile |
| «Vi siete fermati sul prezzo: ti suggeriamo la media» Complex/Info | D-2 / T2b | visibile |
| «Manca una tua dichiarazione: finché non la completi non potete confermare l'accordo.» Default/Warning | D-5 | visibile |
| «Accordo raggiunto» Complex/Success | D-7 / T4 | visibile |
| «Giulia Rossi aspetta la tua risposta sul prezzo da 2 giorni.» Default/Info | T2, T3, T2b, T2c, D-4, D-6, T4, T5 | **nascosto** |

Più l'overlay `Onboarding di fase (Venditore, una box)`: eyebrow «HAI RICEVUTO UNA PROPOSTA», testo «Giulia Rossi ti ha mandato una proposta: inizia la trattativa», due CTA. L'annotazione dichiara già che lato acquirente non serve, perché la trattativa la apre lui con la proposta.

## 3. Cosa manca, e di che tipo è

**Overlay come l'onboarding: un solo altro caso.** La conferma prima di «Annulla la trattativa», annotata su T2 e mai disegnata. È l'unica azione irreversibile della fase, e il pattern approvato per le azioni irreversibili (eliminazione del profilo) chiede conferma esplicita, conseguenze dichiarate e via di ritorno.

**Domanda di sistema sull'onboarding di fase.** Se è un pattern di fase, allora anche PG3 (Preparazione alla firma) e PG4 (Registrazione) ne vogliono uno al primo accesso; oggi non ce l'hanno. Se invece è un caso unico legato all'apertura della trattativa, va detto, perché il nome «Onboarding di fase» promette l'altra cosa.

**Alert in pagina, non overlay.** Due eventi delle guide non hanno ancora una schermata:

- scadenza di una condizione sospensiva a 30 giorni, con la proroga come uscita;
- avveramento della condizione dichiarato dalla parte che l'ha generata — che però cade dopo la firma del preliminare, quindi va prima collocato nell'epica giusta.

**Discrepanze trovate durante il censimento.**

- La soglia dell'avviso temporale ha tre valori: 4 giorni (silenzio prolungato, wireframe), 2 giorni (testo dell'alert in v2), 48 ore (sollecito di pagamento in PG4), contro i 30 giorni delle guide per le condizioni sospensive.
- L'alert spento in M-1 / T3 mobile dice «La data che avete fissato per il mutuo è tra 10 giorni»: è la scadenza della condizione, ma a 10 giorni invece dei 30 delle guide.
- La voce «Trattative» di IMP è scritta **solo dal lato venditore**: «quando un acquirente mostra interesse a trattare o invia un'offerta». Tutti gli eventi che riceve l'acquirente — il venditore ha risposto, l'accordo è raggiunto, la controparte ha annullato — non hanno una categoria dichiarata. Si vede proprio nella tavola nuova: la pagina promette «Ti avvisiamo appena la manda» e la tassonomia approvata non prevede quell'avviso.
- «Inadempienza» in IMP contro «inadempimento» fissato per la piattaforma (I36).
- In M-1 / T3 il primo segmento della barra dei punti è legato a `components/button/bg-primary`: la regola della v2 conosce solo verde, warning e grigio. Da correggere.

## 4. La tavola nuova · acquirente in attesa della prima risposta

### D-0a desktop (`4586:24811`), 1440 × 1867

Gemello di D-0b visto da Giulia. Nella sezione desktop sta nella quinta fila, fra A-P2 e T3a; T3a e la card della Bacheca sono scalate di una colonna a destra.

- Avviso Default/Info: «Hai inviato la tua proposta a Marco Ferrero: ora tocca a lui.»
- Argomenti, 0 di 3 concordati, tutti e tre con badge «In attesa di Marco Ferrero», cerchio vuoto, nessuno stroke: prezzo «Proposta: € 260.000 · da te, oggi · prima proposta», data del rogito «Proposta: 15/06/2027», data di consegna «Non ancora proposta · La propone Marco Ferrero con la sua prima risposta». Le prime due hanno «Vedi le proposte (1)», la terza non ha piede perché non esistono ancora proposte.
- Dichiarazioni: le tue 2 di 2 con la condizione sul mutuo, quelle di Marco 0 di 2 con badge «In attesa di Marco Ferrero» su entrambe le domande.
- Blocco «La prima risposta di Marco Ferrero», gemello senza bottone del blocco di invio del venditore: «Arriva tutta insieme: prezzo, data del rogito, data di consegna delle chiavi e le sue dichiarazioni. Ti avvisiamo appena la manda.»
- Spalla: «Mancano 4 punti su 5», un solo punto completato (le tue dichiarazioni), gli altri quattro Initial.

### M-0a mobile (`4586:25296`), 440 × 2570

Prima riga della sezione mobile, in seconda colonna dopo M-0; le altre tavole di stato sono scalate di una colonna.

- Barra dei punti: «TRATTATIVA · MANCANO 4 PUNTI SU 5», riga «In attesa di Marco Ferrero», segmenti grigio · grigio · grigio · verde · grigio secondo la regola della v2.
- **Nessuna barra sticky**: qui l'acquirente non ha azioni, come in M-6.
- Stesso avviso Default/Info e stessi contenuti della desktop.

### Trappole incontrate

Cambiare lo `State` di `Stepper nav link` da Completed o Active a Initial fa perdere gli override di colore e di stile: i testi tornano legati a `text-ondark-*` (crema su fondo chiaro, illeggibili), la forma dell'icona a un grigio, e il titolo resta Medium invece di Light. Vanno ribindati a `colors/text/text-onlight-soft`, `colors/brand/indigo/050` e `colors/brand/indigo/400`, e il peso riportato a Light. È lo stesso difetto già registrato sull'`Input field` (bind a `text-ondark-*`): candidato a una correzione in libreria.

## 5. Da decidere

- Se l'onboarding di fase è un pattern per tutte le tappe o un caso unico dell'apertura della trattativa.
- Una sola soglia per gli avvisi temporali, o tre soglie dichiarate con la loro ragione.
- La categoria di notifica per gli eventi che riceve l'acquirente: nuova voce in IMP, oppure riscrittura della descrizione di «Trattative» in forma simmetrica.
- Dove collocare l'avveramento della condizione sospensiva: resta nella Trattativa o passa all'epica successiva, visto che cade dopo la firma.
- Se la conferma prima di «Annulla la trattativa» si disegna ora o entra nel perimetro di T6.
