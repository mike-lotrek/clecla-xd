# PG1 · Pagina unica per i due ruoli — delta del 17/09

Decisione: **una sola guida alla trattativa**, valida per venditore e acquirente. Il copy non si rivolge più al venditore dandogli del tu, ma nomina il ruolo in terza persona — «Tocca al venditore» invece di «Tocca a te». La ragione: la stessa persona può vendere un immobile e comprarne un altro, e due pagine distinte la confonderebbero.

Il «tu» resta dove vale per chiunque legga («Qui trovi informazioni utili»); è caduto solo dove implicava un ruolo.

## Le differenze fra i due ruoli non erano solo in «Come funziona»

Il confronto testo per testo fra `D - 1` (venditore) e `D - 3 / Acquirente` ha trovato differenze in quattro sezioni su sei.

| Sezione | Cosa cambiava |
|---|---|
| Come funziona | etichette di turno, titolo dei passi 2 e 5, corpo del passo 1 |
| Quando fissare il rogito | **tutta la lista dei tempi**, scritta dal punto di vista di chi legge, più una voce che esisteva solo nell'acquirente: il contratto d'affitto |
| Errori da evitare | il venditore aveva «Non dichiarare i difetti noti dell'immobile», l'acquirente aveva **«Dichiarare le proprie condizioni a trattativa avviata»** |
| Perché non c'è la caparra | le sei righe delle due card, rovesciate fra chi versa e chi riceve |
| Quando si annulla il contratto | l'inefficacia: «il tuo annuncio torna online» vale solo per il venditore |

## Cosa è stato fatto sul copy

**Neutralizzati 17 testi** su `D - 1` e altrettanti su `M - 1`, più le tre tavole di stato. I principali:

- sottotitolo: «Venditore e acquirente trattano direttamente, senza agenzia. Qui trovi informazioni utili su come si fa una proposta, come si risponde e cosa conviene decidere prima di partire.»
- passo 1: «…Avvisiamo il venditore appena arriva: da lì in poi si tratta direttamente fra le due parti.»
- passo 2: «Il venditore risponde al prezzo e dichiara le sue condizioni» · passo 5: «Il venditore indica chi vende insieme a lui»
- etichetta di turno: «TOCCA AL VENDITORE»
- lista tempi: «Consegna della nuova casa del venditore», «Rogito di acquisto della nuova casa del venditore, se ne compra una», «Sanatoria sulla casa in vendita»
- caparra: «Il venditore riceverebbe la somma dall'acquirente, subito alla firma» · «Se l'acquirente non rispetta gli accordi, il venditore la trattiene» · «Se è il venditore a non rispettarli, deve restituirla raddoppiata» · «Se l'acquirente non rispetta gli accordi, paga il 5% del prezzo al venditore» · «Se è il venditore a non rispettarli, paga il 5% all'acquirente»
- inefficacia: «…le parti sono libere e l'annuncio torna online»
- inadempimento: «Prepariamo il modulo per comunicarlo e vi guidiamo nei passi successivi»

**Travasati i due contenuti che esistevano solo nella variante Acquirente**, riscritti in terza persona e aggiunti a `D - 1` e `M - 1`:

- lista tempi, ottava voce: «Fine del contratto d'affitto dell'acquirente, se è in affitto»
- errori, settima voce: «Dichiarare le proprie condizioni a trattativa avviata», con la nota «Mutuo, vendita di un immobile dell'acquirente e prelazione vanno dichiarati con la prima proposta: cambiano la data del rogito.»

I frame si chiamano ora `Guida alla trattativa – D - 1` e `– M - 1`, senza suffisso di ruolo.

## Allineamento a PG2: sidebar e stepper

**Sidebar.** In PG1 la barra scura era stirata per tutta l'altezza della pagina (4107 px). In PG2 è alta **900**, dentro un wrapper da 948, e sotto ha un **`Bottone · apri sidebar`** da 32 con `icon/keyboard_arrow_right` su `bg-surface-dark`, a x 70 e y 1045. PG1 ora ha la stessa misura e lo stesso bottone, clonato da PG2.

**Stepper della spalla.** Struttura e icone erano già allineate; a divergere erano i colori, perché PG1 aveva override locali di fill. Prima li ho riportati ai valori di PG2 (pastiglia `bg-target-softer` arancio chiaro, icona `text-fg-brand`), poi l'intera scala è passata all'indaco.

## Stepper: tre stati sulla scala indaco

Il vecchio schema usava l'arancio del brand per attivo e completato e un grigio trasparente per i futuri: due stati su tre condividevano lo stesso colore, quindi lo stepper non diceva a che punto sei. Ora i tre stati stanno sulla stessa scala indaco, dal più scuro al più chiaro, e la posizione si legge dal contrasto.

| Stato | Pastiglia | Icona |
|---|---|---|
| Corrente | `indigo/950` (201650), piena | `text-ondark-strong` (FEFBF0) |
| Compiuto | `indigo/200` (C2C8FF) | `indigo/800` (3C25AE) |
| Futuro | `indigo/050` (ECEFFF) | `indigo/400` (7775FF) |

Le variabili arrivano dalla collezione **Primitives** del DS, importate con `importVariableByKeyAsync`; l'`Icon Shape` non ha una variante Color indaco, quindi i fill sono override locali sull'istanza e sul vettore dell'icona. Applicato a tutte le **32 istanze** di `Stepper nav link` presenti nelle due sezioni: 12 in PG1 (`3707:110792`), 20 in PG2 (`3847:95665`).

Sistemato nello stesso passaggio un residuo di PG2: il testo del passo corrente era `text-fg-brand`, cioè rosso mattone, mentre in PG1 era indaco. Ora entrambi usano `text-onlight-strong` per il titolo e `text-onlight-soft` al 60% per l'«Sei qui».

Quando l'`Icon Shape` prenderà una variante Color indaco nel DS, questi override vanno tolti e sostituiti dalla variante.

**Ogni passo tiene la sua icona, anche quando è quello corrente.** Nell'allineamento a PG2 avevo sostituito l'icona del passo corrente di PG1 con `radio_button_unchecked`, leggendo il cerchio vuoto come il modo in cui PG2 segnala «sei qui». Era una lettura sbagliata: in PG2 i passi correnti mostrano la loro icona (`compare_arrows`, `handshake`), e con i tre toni indaco il colore basta a dire dove sei. Il passo corrente di PG1 è tornato a `icon/description`; scambiare l'icona costava un'informazione senza aggiungerne.

Una cosa che PG1 non usa ancora: lo stato **Completed**. In PG2 i passi già fatti lo hanno, in PG1 siamo al primo passo e non serve, ma quando la guida verrà aperta da un punto più avanti della trattativa i passi precedenti dovranno mostrarlo.

## Da decidere

- **Le due varianti Acquirente (`D - 3`, `M - 4`) sono ancora nella tavola.** Tutto quello che contenevano è stato travasato o neutralizzato: si possono eliminare, ma la cancellazione non è stata fatta senza conferma.
- **Il breadcrumb.** Il venditore aveva «I miei immobili», l'acquirente «Le mie trattative». Su una pagina sola serve una voce che valga per entrambi: «Le mie trattative» funziona, «I miei immobili» no, perché un acquirente non ha immobili. Oggi la pagina porta ancora «I miei immobili». Il punto si è allargato: vedi `claude/switch-trattative.md`, dove lo stesso posto viene chiamato in tre modi.
- **L'ordine degli errori.** Il nuovo errore è in coda come settimo: sta vicino a «Non dichiarare i difetti» ma parla d'altro. Probabilmente sale accanto al secondo, che riguarda anch'esso cosa va messo per iscritto e quando.
- **La lista dei tempi è lunga otto voci** e mescola cose del venditore e dell'acquirente. Se diventa faticosa si può spezzare in due gruppi.
- **L'avatar e il nome in navbar** restano quelli del venditore (MR, Mario): segnaposto da dichiarare.
- **Il mobile non ha l'equivalente del bottone apri sidebar**, perché lì la sidebar non c'è: il confronto con PG2 mobile non è stato fatto.

Chiuso: l'«Sei qui» invisibile in PG2 era un frame spento, riacceso da Giovane.
