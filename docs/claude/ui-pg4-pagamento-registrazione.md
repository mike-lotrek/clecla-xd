# UI — PG4 Pagamento registrazione (Sprint 4)

File Figma: **Cleclà | UI** → pagina `🫟 UI Layouts – WIP`, sezione `PG4 · Pagamento registrazione 🚧`.
Otto frame, quattro desktop 1440 e quattro mobile 440, generati dai wireframe della sezione `PG4 · Pagamento registrazione — Desktop 1440` con i componenti della libreria **Cleclà | Design System (Flowbite)**.

| Stato | Desktop | Mobile |
|---|---|---|
| R1 · Registrazione da pagare (Acquirente) | 1440 × 1557 | 440 × 2124 |
| R2 · Pagata, deposito in lavorazione (Acquirente) | 1440 × 1387 | 440 × 1897 |
| R3 · Registrato, traguardo e passaggio al rogito (Acquirente) | 1440 × 1870 | 440 × 2526 |
| R4 · In attesa del pagamento (Venditore) | 1440 × 1117 | 440 × 1648 |

R5, il termine scaduto, resta un riquadro di confine nel wireframe: non è una pagina finché il cliente non scioglie il punto aperto 20.

Gate di libreria superato su tutti gli otto frame: da 9 a 23 istanze per frame, tutte da libreria, nessun fill o stroke fuori dalle variabili, nessun testo senza stile. Le uniche eccezioni sono il `System Bar` mobile, componente locale ereditato da PG1, e i due testi mobile fuori scala tipografica (titolo 28 ed etichetta 14), limite già registrato in PG3.

## Allineamento del 17/09 — spalla e sidebar

**La spalla mostra solo la tappa in corso.** Come PG1, PG2 e PG3: resta il blocco `Contratto` con i suoi quattro sotto-passi, sono cadute Profilo immobile, Pubblicazione, Visite e — in R4, che è la vista Venditore — anche Trattativa, con i loro separatori. `Trust inner` scende da 572-689 a 362-409 px a seconda dello stato.

**I sotto-passi hanno le loro icone.** Prima i passi ancora da fare portavano `icon/radio_button_unchecked`, cioè il segnaposto: ora sono `icon/draw` per Firma del preliminare, `icon/payments` per Pagamento della registrazione, `icon/account_balance` per Deposito all'Agenzia delle Entrate, `icon/verified` per Registrato. Prese dalla pagina Icons del design system con `figma_instantiate_component`.

**I colori passano alla scala indigo**, la stessa di PG2: cerchio `indigo/200` con icona `indigo/800` per i passi fatti, `indigo/950` con icona bianca per quello attivo, `indigo/050` con icona `indigo/400` per quelli da fare. PG4 usava `bg-target-softer`, `bg-neutral-tertiary` e `bg-surface-dark-transparent`, e i cerchi venivano grigi.

**La sidebar non è più alta quanto la pagina**: pannello da 900 px dentro un contenitore da 948, bottone di apertura da 32 sotto, centrato. È il pattern del componente `Sidebar - Chiusa` già applicato a PG2 e PG3.

**I pesi tipografici seguono ora una regola sola**, decisa in revisione e applicata a tutti i diciannove stepper del file: **Medium per Completed e Active, Light per Initial.** Completed e Active si distinguono per colore — `text-onlight-medium` contro `text-onlight-strong` — non per peso; quello che resta da fare recede. Prima era un miscuglio: in R1 «Deposito all'Agenzia delle Entrate» era Medium e «Registrato» Light pur essendo entrambi Initial, e in PG2 l'Initial era Medium e il Completed Light.

### Il punto interrogativo è il bottone blu

In R1 il `?` accanto a «Perché si paga» era l'icona nuda `Help · P7`. Ora è il `Help icon (?)`, il cerchio indaco da 18 nato in PG1: **è il trigger di un popover e nient'altro**, come già fissato per PG2 e PG3.

Nel popover va il contenuto dell'`Alert` Info che stava sotto in pagina, «Perché il pagamento sblocca l'archiviazione», che è uscito. Vale la regola di PG3: l'Alert resta solo per ciò che constata un fatto di questa pratica, la spiegazione va nel popover del titolo a cui si riferisce. R1 desktop scende da 1665 a 1557 px, il mobile da 2256 a 2124.

Il testo sta nella tavola `PG4 · Contenuti dei bottoni info`, accanto alla sezione.

**Restano otto `?` nudi in PG3 F3**, quattro su desktop e quattro su mobile, tutti sulla riga «Dichiarazione antiriciclaggio, precompilata», uno per persona. Sono il caso tenuto aperto in revisione: se il testo spiega cos'è l'antiriciclaggio va nel popover come gli altri, se constata un obbligo di questa pratica resta un Alert. Nessun altro `?` nudo nel file.

## Le tre forme, applicate a PG4

La regola di PG3 regge anche qui, e ha deciso il layout più di ogni altra cosa.

- **Percorso → stepper.** La barra a quattro blocchi del wireframe non entra in pagina su desktop: diventa lo stepper della spalla, dentro il blocco `Contratto`, con i quattro passi della registrazione — Firma del preliminare · Pagamento della registrazione · Deposito all'Agenzia delle Entrate · Registrato. Su mobile resta la barra di percorso a tre righe, unico elemento segmentato della pagina.
- **Responsabilità, avanzamento e scadenza → fatti etichettati.** Tre occhielli affiancati su desktop, impilati su mobile: «RESPONSABILITÀ / Tocca a te», «AVANZAMENTO / Passo 2 di 4 · registrazione da pagare», «SCADENZA / 03/10/2026 · mancano 27 giorni». La scadenza compare solo dove il termine è in corso e qualcuno deve agire, cioè in R1 e R4.
- **Niente seconda barra.** L'avanzamento del deposito in R2, che nel wireframe è una timeline con i pallini, qui è una lista di fatti: tappa a sinistra, data o stima a destra, divider fra le righe. Su mobile le due parti si impilano. Il passo in corso si distingue per il peso del testo (Paragraph/Medium) e per il valore «In corso · stimato entro l'08/09/2026», non per un grafico.

Lo `Stepper nav link` ha una variante **Completed** che PG3 non aveva usato: qui serve, perché i passi già chiusi sono la metà del racconto. Il colore del testo della variante Completed arriva arancione scuro e quello della Initial creata da zero arriva crema su crema: in entrambi i casi il fill va riscritto copiandolo da un passo sano, altrimenti l'etichetta sparisce. Dal 17/09 i fill sono riscritti sistematicamente dalla mappa indigo, quindi il problema non si presenta più.

## Decisioni di contenuto

- **Le conseguenze stanno in R1, non nella schermata di scadenza.** L'annullamento del contratto dopo 30 giorni e il blocco dell'archiviazione sono due `Alert` in pagina già quando c'è ancora tempo: sono le informazioni che rendono il pagamento comprensibile invece che imposto.
- **Il terzo passo lo dichiara Cleclà.** «Deposito all'Agenzia delle Entrate · lo facciamo noi» sta nello stepper come helper del passo: senza quell'etichetta l'utente cerca un'azione che non gli spetta.
- **Il checkout non è ridisegnato.** In R1 restano i due metodi (carta e bonifico) con la differenza di tempi dichiarata; dati di fatturazione e pagamento vero sono pagina esistente, e la cosa è annotata sul frame invece che scritta in pagina.
- **La scomposizione dei 320 € tiene l'ingombro.** Due voci con importo vuoto — imposta di registro e bollo da una parte, servizio Cleclà dall'altra — sotto l'occhiello «COSA C'È DENTRO I 320 €». È il punto aperto 2: i T&C danno solo il totale.
- **Le note di servizio non entrano in pagina.** «DA VALIDARE», «INGOMBRO», «STATO ALTERNATIVO», «PUNTO APERTO» sono annotazioni native sui frame, come in PG3.
- **Gli stati alternativi di R2 e R4 sono annotati, non disegnati.** Bonifico in attesa di quietanza e SLA superato per R2; riga «Pagata» e riga «Registrata» per R4, con la nota che nello stato Registrata il footer del venditore si accende e mostra le due azioni di download di R3.

## Le due famiglie di Alert

Vale la divisione fissata in PG3. Complex — titolo e corpo — per ciò che spiega: perché il pagamento sblocca l'archiviazione, cosa succede alla scadenza, il traguardo raggiunto in R3, l'archiviazione ancora bloccata per il venditore. Il colore segue il fatto: Info per la spiegazione, Warning per l'avviso che chiede attenzione, Success per il traguardo. In PG4 non serve nessun Alert Default: tutto ciò che la pagina dice ha due livelli di testo.

## Mappatura sui componenti

Shell, navbar, sidebar, spalla, breadcrumb e barra sticky sono clonati da PG3. In più: `Button` Primary per le CTA di pagamento e di download, Primary Disabled dove l'azione dipende da altri, Outline-dark per la seconda azione di R3 e per «Trova un notaio», Link-dark Small per i rimandi. `Checkbox input` Type=Radio input per i due metodi di pagamento, dentro un frame «Casella» con padding superiore di 2 px, per il bordo esterno che altrimenti viene tagliato. `Badge` Brand blue per lo stato della fase, Success per «Pagata il 05/09/2026» e «Registrato», Warning per «In attesa dell'acquirente» e «In attesa», Brand white per il contatore «0 di 19 caricati».

| Blocco | Componente |
|---|---|
| Percorso in spalla | `Stepper nav link` Type=Icon shape & text, stati Active/Initial/Completed, una sola tappa visibile, scala indigo, testo Medium per Completed e Active e Light per Initial |
| Sidebar | pannello da 900 in un contenitore da 948, più il bottone di apertura da 32, come in PG2 e PG3 |

## Discrepanze da sciogliere

Segnalate, non risolte.

- **Importo della registrazione.** PG4 dice 320 € + IVA, 390,40 € totali. I frame approvati dicono «Registrazione contratto preliminare · circa €270» (CC4, EMC A), e in CC4 la voce porta l'etichetta «Incluso». Il wireframe stesso cita una terza cifra, i 300 € stimati dal calcolatore budget. Tre numeri per la stessa voce, più il dubbio se sia a carico dell'acquirente o inclusa (I08).
- **Coerenza col calcolatore budget.** Prima di mostrare in pagina il confronto fra stima e importo effettivo serve sapere se la stima iniziale include già questa voce, altrimenti la riga confronta due cose diverse. Tenuta fuori dalla pagina e annotata.
- **Le condizioni sospensive di R3.** L'elenco del wireframe — mutuo, regolarità edilizia e conformità catastale, prelazione agraria, liberazione da vincoli e ipoteche, assenza di diritti di terzi — non coincide con le cinque della Scheda Tecnica 2.0, dove al posto delle ultime due ci sono la vendita dell'immobile del promissario acquirente e la soluzione abitativa per il venditore. Né con le quattro delle guide del 14/09, che hanno fatto scendere a quattro anche l'elenco di PG2. Testo tenuto come nel wireframe e annotato sul frame.
- **Nome del compenso.** In PG4 è sempre «provvigione», coerente con la decisione del 10/09 di scegliere per contesto, ma diverso da «fee» e «costi di mediazione» usati altrove (I05).
- **Quando è dovuta la provvigione.** R3 dice «solo a trattativa conclusa, con un contratto preliminare valido ed efficace» e aggiunge che le sospensive non ancora avverate la rinviano. È più preciso delle sei formule approvate, che oscillano fra «paghi solo se vendi» e «dopo il preliminare» (I06): se il testo passa, va portato in glossario.
- **Soglia del promemoria.** 48 ore in R4, quattro giorni per il silenzio prolungato in PG2 (I44).
- **«Trova un notaio».** Nuova funzione a livello di label: il glossario conosce solo «Trova tecnici» nelle sue tre grafie (I26).
- **Nome della tappa.** L'header dice «Registrazione del contratto preliminare», la spalla la tiene dentro `Contratto`, i percorsi approvati non hanno una tappa «Registrazione» (I10, I12).
- **Quattro o cinque tappe.** La barra mobile dichiara «TAPPA 4 DI 4» all'acquirente e «TAPPA 5 DI 5» al venditore: eredità di PG3, punto ancora aperto. Con la spalla ridotta alla sola tappa in corso la domanda resta solo sulla barra mobile, che il conteggio lo dichiara.

## Punti aperti

- **Punto aperto 2.** Manca la scomposizione dei 320 € fra imposta e servizio Cleclà.
- **Punto aperto 20, residuo.** I T&C non prevedono sanzioni per la registrazione tardiva: le penali riguardano il rapporto venditore–Cleclà. Resta aperto cosa succede al contratto già firmato se l'acquirente non paga, e chi risponde dei costi già sostenuti. È il motivo per cui R5 non è stata disegnata.
- **Protocollo di registrazione.** In R3 è un esempio (2026/CN/0004821): da confermare formato e provenienza.

## Note operative

Confermato quanto scritto per PG2 e PG3, con tre trappole nuove.

- **Il target del bridge si sposta da solo.** A metà lavorazione le chiamate sono finite su un altro file aperto con il plugin. Conviene fissare il file con `figma_navigate` e `lock: true` prima di iniziare.
- **Le esecuzioni lunghe vanno spezzate.** Oltre i trenta secondi lo script viene interrotto a metà e lascia nodi parziali: dalla lavorazione sono usciti un blocco «Perché tocca a te» duplicato, una riga di timeline doppia e una data ripetuta, tutti trovati solo rileggendo i figli. Meglio dieci script corti e una verifica dopo ognuno.
- **Un frame clonato porta con sé le altezze fisse.** Dopo aver sostituito il contenuto vanno rimessi `layoutSizingVertical = HUG` sulle card e ricalcolate altezza del frame, altezza della sidebar e posizione della barra sticky mobile.
- **`swapComponent()` riporta l'icona al fill di default.** In PG4 i colori dello stepper erano stati riscritti prima dello scambio delle icone, e lo scambio li ha cancellati: i vettori sono tornati a `text-fg-brand`, che su un cerchio indigo/950 dà un'icona indaco su indaco. Prima si scambia l'icona, poi si ricolora.
- **Su mobile le righe etichetta-valore si impilano a mano**, e dopo il cambio di direzione va rimesso l'hug verticale sulla riga, altrimenti resta alta quanto una riga sola e i due testi si sovrappongono.
- **Le icone del design system si prendono per chiave.** `importComponentByKeyAsync` non risponde entro il timeout del bridge, ma `figma_execute_across_files` sul file del DS restituisce la `key` del componente e `figma_instantiate_component` lo porta nel file. Da lì `swapComponent()` lo distribuisce su tutte le istanze che servono.
