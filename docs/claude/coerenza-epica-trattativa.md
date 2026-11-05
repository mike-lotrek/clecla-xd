# Controllo di coerenza — epica Trattativa (PG1-PG4)

Prima stesura 11/09/2026, aggiornata lo stesso giorno dopo la lavorazione. L'epica è lo **Sprint 4**: il file Figma la tiene sotto la pagina «🚧 Sprint 4 - Trattativa» e il foglio Contenuti la marca così. I documenti di lavorazione che dicevano Sprint 3 sono stati allineati.

Verifica condotta sui quattro documenti di lavorazione e, dove il documento non bastava, direttamente sul file **Cleclà | UI**, pagina `🫟 UI Layouts – WIP` (sezioni PG1, PG2, PG3, PG4) e sulla libreria **Cleclà | Design System (Flowbite)**. I numeri citati sono contati sul file.

Output collegato: sezione **`DS · Candidati dalla Trattativa 🧩`** (nodo `3961:9881`), sotto PG4 nella stessa pagina. Venticinque schede con un'istanza vera per componente, più un pannello «Decisioni dell'11/09» che riassume cosa è stato chiuso, cosa è rinviato al DS e cosa resta aperto.

---

## Stato al 11/09

Otto voci chiuse nel file, due rinviate al design system, cinque lasciate aperte con segnalazione.

| # | Voce | Esito |
|---|---|---|
| 1.1 | Tappe concluse disegnate come da fare | Chiusa |
| 1.2 | Badge Brand white invisibile | Rinviata al DS |
| 1.3 | Barra di percorso mobile in due versioni | Chiusa |
| 1.4 | Regola del progresso e nome della riga di responsabilità | Chiusa, regola riscritta |
| 1.5 | Alert di PG1 e PG2 prima della regola delle due famiglie | Chiusa |
| 1.6 | Cast dei nomi | Chiusa |
| 1.7 | Indirizzo dell'immobile | Chiusa |
| 1.8 | Clip content non propagato a PG1 | Rinviata al DS |
| 1.9 | Gerarchia tipografica nelle card | Chiusa |
| 1.10 | Divergenze di contenuto | Aperte, tranne la numerazione dello sprint |
| 2.4 | Il ruolo non cambia i colori | Chiusa: scelta abbandonata |

---

## 1. Cosa è stato corretto

### 1.1 Le tappe concluse ora si distinguono

La verifica ha separato due livelli che la prima stesura aveva confuso, e vale la pena registrare la differenza.

**Sotto-passi della tappa aperta.** Sono istanze di `Stepper nav link`. La variante `Completed` compariva solo in PG4, sette volte. In PG2 e PG3 i sotto-passi già conclusi erano `Initial`, cioè lo stesso segno di quelli futuri: cerchio grigio vuoto invece di cerchio brand con la spunta. Corretti 21 sotto-passi, dieci in PG2 e undici in PG3, clonando l'istanza `Completed` di PG4 invece di cambiare la variante, perché il cambio di variante non porta con sé gli override di colore. In PG1 il passo attivo è il primo, quindi non c'era niente da cambiare.

**Tappe del percorso.** Sono righe di testo dentro il blocco spalla, staccato dal componente `Stepper`. Non avevano nessuno stato: Profilo immobile, Pubblicazione, Visite e Contratto erano tutte dello stesso grigio, legato per giunta a `colors/components/button/text-disabled`, un token di bottone usato su uno stepper. Ora c'è una rampa a tre livelli, tutta su token di testo:

| Stato della tappa | Token | Opacità |
|---|---|---|
| Conclusa | `colors/text/text-onlight-medium` | 80% |
| Aperta | `colors/text/text-onlight-strong` | 100% |
| Futura | `colors/text/text-onlight-soft` | 60% |

Applicata ai 16 frame desktop delle quattro PG. La scelta del colore al posto di un'icona di spunta è reversibile in un passaggio: se il DS aggiunge un marcatore di stato per le righe di percorso, si sostituisce.

**Difetto trovato strada facendo.** La spalla di R1, R2 e R3 di PG4, che sono pagine dell'acquirente, mostrava il percorso del venditore: Profilo immobile · Pubblicazione · Visite · Trattativa · Contratto. Corretto in Ricerca · Visita · Trattativa · Contratto, coerente con PG3 F1 acquirente e con la barra mobile, che già diceva «TAPPA 4 DI 4».

### 1.3 Una sola barra di percorso mobile

Sedici istanze: sei a due righe in PG1 e PG2, dieci a tre righe in PG3 e PG4. Le sei sono state rifatte con la forma a tre righe.

| Frame | Occhiello | Passo | Segmenti pieni |
|---|---|---|---|
| PG1 M Venditore | TRATTATIVA · TAPPA 4 DI 5 | Guida alla trattativa · passo 1 di 4 | 0 |
| PG1 M Acquirente | TRATTATIVA · TAPPA 3 DI 4 | Guida alla trattativa · passo 1 di 4 | 0 |
| PG2 M T2 | TRATTATIVA · TAPPA 4 DI 5 | Risposte e controproposte · passo 3 di 4 | 2 |
| PG2 M T3 | TRATTATIVA · TAPPA 3 DI 4 | Risposte e controproposte · passo 3 di 4 | 2 |
| PG2 M T4 | TRATTATIVA · TAPPA 4 DI 5 | Accordo raggiunto · passo 4 di 4 | 3 |
| PG2 M T5 | TRATTATIVA · TAPPA 4 DI 5 | Accordo raggiunto · passo 4 di 4 | 4 |

I segmenti contano i quattro sotto-passi della trattativa, non le tappe: è la scelta di PG3, dove i segmenti contano i passi su cui l'utente può agire e la tappa resta detta a parole nell'occhiello.

**Seconda divergenza trovata qui.** PG3 e PG4 riempivano i segmenti con due convenzioni diverse: PG3 riempie i passi conclusi (passo 2 di 4 → 1 pieno), PG4 riempiva anche quello in corso (passo 2 di 4 → 2 pieni). Vale la convenzione di PG3, perché a «passo 4 di 4» riempire tutto direbbe che la fase è finita quando resta ancora da firmare. Corretti R1, R2 e R4; R3 resta a 4 pieni perché «Registrato» è un esito raggiunto, non un passo in corso.

### 1.4 La regola del progresso, riscritta in quattro casi

La regola di PG3 diceva tre forme e aveva un effetto collaterale dichiarato che il file smentiva: «su desktop non resta nessuna barra segmentata», mentre la barra dell'accordo di PG2 è su desktop. La barra resta, e la regola diventa questa.

1. **Percorso, cioè posizione dentro una sequenza di tappe.** Stepper. Uno solo per pagina, e nient'altro usa quella forma. Su desktop è la spalla, su mobile la barra di percorso.
2. **Conteggio su un insieme chiuso e omogeneo di oggetti.** Barra segmentata, un segmento per oggetto. È il caso della barra dell'accordo: otto condizioni, ordinate per step, con un totale che non cambia per tutta la trattativa.
3. **Conteggio su un insieme di persone, o su attività eterogenee.** Fatti etichettati, senza grafico. «AVANZAMENTO / 1 persona su 4 ha completato i passaggi». Un conteggio di persone non è una posizione in una sequenza, e disegnarlo come barra lo fa leggere come un secondo percorso.
4. **Sequenza dentro una riga.** Pallini a tre stati. È la catena dell'invito di PG3.

Conseguenza di naming: la riga si chiama `Riga · Responsabilità e avanzamento` ovunque. Le sei istanze di PG2 che si chiamavano `Riga · Responsabilità e progresso` sono state rinominate.

### 1.5 Gli Alert di PG1 e PG2 riletti

Regola: Complex, cioè titolo e corpo, per ciò che spiega; Default, una riga sola, per ciò che constata. Il colore segue il fatto, non il tono della pagina.

| Intervento | Prima | Dopo |
|---|---|---|
| PG1, «La data del rogito è una scadenza» (4 istanze) | Default/Info, due frasi in una riga | Complex/Info, titolo «La data del rogito è una scadenza» e corpo «Il rogito si fa entro quel giorno…» |
| PG1, «Perché conviene rispondere presto» (4 istanze) | Complex/Warning | Complex/Info |
| PG2, silenzio prolungato (2 istanze) | Complex/Info con titolo nascosto | Complex/Warning, titolo «Sono passati 4 giorni dall'ultima risposta», corpo «Marco Ferrero non ha ancora risposto. Puoi mandargli un promemoria.» |

Sul secondo: in una guida statica «perché conviene rispondere presto» spiega, non segnala un fatto che chiede attenzione ora. Il Warning aggiungeva una pressione che il manuale d'identità mette fra i «da evitare». Sul terzo, invece, il fatto c'è ed è datato, quindi Warning.

Distribuzione finale, che ora si legge come una scelta e non come un'abitudine:

| Sezione | Complex | Default |
|---|---|---|
| PG1 | Info 12, Success 4 | nessuno |
| PG2 | Info 4, Warning 2, Success 2 | Warning 4, Info 2 |
| PG3 | Info 8, Warning 2 | Danger 2, Warning 4, Success 2 |
| PG4 | Info 4, Warning 6, Success 2 | nessuno |

PG1 è una guida: tutto spiega, quindi tutto è Complex. PG4 lo stesso, per la ragione opposta — tutto ciò che dice ha due livelli di testo.

**Correzione a quanto scritto nella prima stesura.** Avevo segnalato come difetto l'assenza di `Danger` in PG1 e PG2. Verificato: non è un difetto. Danger vale per un errore, e in quelle due sezioni non ci sono errori. Il rifiuto di una condizione è un'azione voluta dall'utente, non un errore, e la modale di rifiuto non ha né deve avere un alert rosso.

### 1.6 Un cast solo

| Ruolo | Nome | Iniziali |
|---|---|---|
| Venditore | Marco Ferrero | MF |
| Coniuge del venditore, comunione legale | Elena Ferrero | EF |
| Acquirente | Giulia Rossi | GR |
| Quarta firmataria (PG3) | Sara Motta | SM |
| Trattative in parallelo (PG2) | Andrea Bianchi, Chiara Vietti | |

L'acquirente era Giulia Rossi in PG1 e PG2 e Luca Conti in PG3 e PG4: ora è Giulia Rossi ovunque. Di conseguenza il coniuge, che si chiamava Giulia Bianchi, è diventato Elena Ferrero, per non avere due Giulie sulla stessa schermata in F1 e F4. La terza trattativa in parallelo era Sara Conti, che faceva eco a Sara Motta di PG3: è diventata Chiara Vietti.

Cambiati anche i nomi dei layer, gli occhielli in maiuscolo dei pannelli Yousign («PASSAGGIO 2 DI 5 · ELENA FERRERO») e un accordo di genere che il cambio di nome aveva reso sbagliato: «gli abbiamo mandato la richiesta» è diventato «le abbiamo mandato la richiesta».

### 1.7 Un solo indirizzo

«Trilocale in Via Roma 12, Cuneo» su tutta l'epica, 32 nodi cambiati. L'incoerenza non era fra PG: era anche dentro PG3 e PG4, dove il titolo di pagina diceva «Via Roma 12» e la scheda diceva «Via Roma».

### 1.9 Tre livelli tipografici dove servivano

La regola di PG3 è che l'etichetta pesi diversamente da ciò che la segue. Verificata sezione per sezione, PG1 la rispetta già: titoli di sezione in Heading 3/Semibold, teste di elenco a 16/Medium, corpi a 14 o 16/Regular.

L'unico punto che la violava è il blocco «Trattative in parallelo» di PG2, dove la testa era Paragraph/Medium e i nomi sotto Paragraph/Regular, cioè l'etichetta pesava meno del suo contenuto. Ora ha la stessa struttura della sezione «Documento di puntuazione» che le sta sopra: titolo «Trattative in parallelo» in Heading 3/Semibold, sotto-testa «Hai 3 trattative aperte su questo immobile» in Paragraph/Regular, nomi in Paragraph/Medium. Applicato su desktop e mobile.

Nella stessa passata 40 testi di PG1 e PG2 che erano a 16/Medium senza stile sono stati riportati su `Body/Paragraph/Medium`: i numeri degli errori da evitare, i nomi delle tre strade, le teste di elenco. I testi senza stile nella pagina, istanze escluse, scendono da 138 a 99.

---

## 2. Cosa è rinviato al design system

Segnalato, non tamponato in pagina.

**Il Badge `Brand white` non si vede.** Quaranta istanze in PG2, PG3 e PG4, tutte su fondo `#f3efe2` con riempimento `#fefbf0`, senza bordo e senza ombra: meno del 2% di differenza di luminanza. Resta leggibile il testo, sparisce la pillola, quindi sparisce il fatto che sia un badge. Riguarda gli stati neutri, cioè quelli che devono distinguersi dal testo normale senza gridare: «Non ancora affrontata», «Non applicabile», «Da caricare», «Da dare», «Non ha ancora firmato», «0 di 19 caricati». Serve un tema neutro con bordo, o un fondo distinto da `bg-surface-default`. Scheda C7 della tavola.

**`Checkbox input` e `Radio item` hanno il bordo allineato all'esterno.** Una casella dichiarata 16×16 ne occupa 18×18 e qualsiasi contenitore con Clip content la taglia. Il cerotto applicato nell'epica resta in piedi: 40 frame `Casella` con 2 px di padding e 288 frame di PG3 a cui è stato tolto Clip content. Scheda C2.

Nota su PG1: la correzione del Clip content non l'ha mai raggiunta, e la sezione ha ancora 162 frame di layout trasparenti che clippano, contro 38 in PG2, 1 in PG3 e 0 in PG4. Verificato però che oggi non taglia niente: le 32 caselle del pianificatore stanno dentro frame `Opzione` con padding 16 e 14. È un rischio latente, non un difetto aperto, e si chiude insieme al componente.

---

## 3. Cosa resta aperto

### 3.1 Divergenze di contenuto dentro l'epica

- **Le cinque condizioni sospensive.** PG2 usa l'elenco della Scheda Tecnica 2.0: mutuo, regolarità edilizia e conformità catastale, vendita dell'immobile del promissario acquirente, soluzione abitativa per il venditore, prelazione. R3 di PG4 sostituisce le ultime due con liberazione da vincoli e ipoteche e assenza di diritti di terzi. Uno dei due elenchi è sbagliato, e vanno riconciliati prima che il preliminare li citi.
- **La soglia del promemoria.** Quattro giorni per il silenzio prolungato in PG2, 48 ore per il sollecito di pagamento in PG4, nessuna attesa dichiarata in PG3. Possono restare due soglie diverse se la ragione è diversa, ma allora va detta.
- **Il nome del gruppo.** «Clausole sospensive» nella modale di PG2, «Condizioni sospensive» nella pagina e in PG4. I frame approvati dicono sempre «condizioni sospensive» (I43): la modale è l'unica fuori riga.
- **Il modello di trattativa.** Le pagine pubbliche approvate raccontano una proposta unica che si accetta o si rifiuta, PG2 lavora su condizioni singole con accettazione, controproposta e rifiuto per condizione (I15). Non è un problema di UI: è la pagina pubblica che descrive un altro prodotto.
- **Quattro, cinque o sei tappe.** Cinque nel percorso venditore, quattro nell'acquirente, sei nello stepper di «Come funziona». Su mobile si vede di più, perché l'occhiello dichiara il totale. È I10 del glossario e ricorre in tutte e quattro le PG.

### 3.2 Per il cliente

| Tema | Cosa serve sapere |
|---|---|
| **Punto aperto 20** | Cosa succede al contratto già firmato se l'acquirente non paga la registrazione, e chi risponde dei costi già sostenuti. I T&C non prevedono sanzioni per la registrazione tardiva: le penali riguardano il rapporto venditore-Cleclà. È il motivo per cui R5 non è disegnata e F5 porta un riquadro aperto. |
| **Punto aperto 2** | Come si scompongono i 320 € fra imposta di registro più bollo e servizio Cleclà. L'ingombro è tenuto in R1 con due voci a importo vuoto. |
| Importo della registrazione | Tre cifre per la stessa voce: 320 € più IVA (390,40 € totali) in PG4, «circa €270» nei frame approvati CC4 ed EMC A, 300 € stimati dal calcolatore budget. In CC4 la voce porta anche l'etichetta «Incluso», quindi non è chiaro nemmeno se sia a carico dell'acquirente (I08). |
| Coerenza col calcolatore budget | Se la stima iniziale della landing include già la voce di registrazione. Se non la include, la riga di confronto in R1 mette a fianco due cose diverse e va tolta. |
| Quando è dovuta la provvigione | R3 dice «solo a trattativa conclusa, con un contratto preliminare valido ed efficace», e aggiunge che le sospensive non ancora avverate la rinviano. È più preciso delle sei formule approvate, che oscillano fra «paghi solo se vendi» e «dopo il preliminare» (I06). Se il testo passa, va portato in glossario. |
| Dichiarazione del regime patrimoniale | Se si chiede prima della Preparazione alla firma o in F1. Se in F1, la riga «Comunione legale dei beni» diventa un input e non un avviso. |
| Secondo livello dell'assistenza | «Fatti aiutare a leggerlo» salta il chatbot e apre il team con il contesto precompilato. Se il secondo livello ha una coda o un orario, il bottone deve dichiararlo. |
| Protocollo di registrazione | Il formato usato in R3 (2026/CN/0004821) è un esempio: da confermare formato e provenienza. |
| Chi firma l'incarico con più intestatari | I cointestatari entrano davvero in F1: se l'incarico lo firma solo l'utente loggato, va deciso cosa succede quando gli altri compaiono. |
| Confronto fra scadenza del documento e data del rogito | Da valutare con i dev se il controllo è automatico (F2). |

### 3.3 Per il team di progetto e il content design

| Tema | Cosa serve decidere |
|---|---|
| **Nome della tappa e della fase** | L'header di PG3 dice «Prepara la firma», il glossario dice «Preparazione alla firma» (I18). L'header di PG4 dice «Registrazione del contratto preliminare» ma i percorsi approvati non hanno una tappa «Registrazione» (I10, I12). |
| **Breadcrumb dell'acquirente** | «Le mie trattative» è un'ipotesi annotata in PG1, PG2 e PG3, non definita da nessuna fonte. |
| Raggruppamento «Dichiarazioni che entrano nel preliminare» | Ipotesi ereditata da PG1, da confermare con content design. |
| Mappatura delle quattro domande di help P7 sui quattro gruppi | La PG elenca le domande senza abbinarle: l'abbinamento in uso è un'ipotesi annotata. |
| Scala delle fasce di prezzo | Compare «Poco consigliato», gli altri gradini non sono definiti. |
| Corpo del passo 1 dello step-walker | Ancora il placeholder della PG. |
| Stati del documento d'identità | La project knowledge registra «Da caricare / Verifica superata / Esito negativo» (I19); F1 introduce una seconda scala per la catena dell'invito (Invitato, Registrato, Dati inseriti, Documento verificato, Consensi dati) più il badge «Completo». Due scale per lo stesso oggetto. |
| Promemoria nella vista Acquirente | La riga di Elena Ferrero, coniuge del venditore, porta «Manda un promemoria» anche nella vista dell'acquirente. Se il sollecito lo manda la piattaforma il permesso può essere di entrambe le parti, altrimenti l'acquirente dovrebbe sollecitare solo la propria parte. |
| T4 e la Regolarità edilizia | Il riepilogo non la elenca fra le condizioni concordate ma la porta fra le sospensive. |
| Il tono del callout dei silenzi | «Il venditore potrebbe avere altre proposte sul tavolo» fa leva sulla possibilità di perdere l'immobile, lo stesso meccanismo che il manuale d'identità indica fra i «da evitare». |
| Rimando alla chat | La memoria di progetto fissa che il supporto in pagina si gestisce con la chat e non con l'email. Nel file UI non esiste un'icona chat istanziata: in tutta l'epica il rimando all'assistenza passa dalla card «Hai dubbi?». |
| Titolo «Trattative in parallelo» | Copy nuovo, introdotto per dare una testa al blocco. Da validare con content design. |

### 3.4 Stati dichiarati e non disegnati

Annotati sui frame, non dimenticanze, ma restano lavoro quando il perimetro si apre: SLA superato in T5 e in R2, verifica catastale non superata in T5, stato iniziale del bottone di conferma in T4, bonifico in attesa di quietanza in R2, righe «Pagata» e «Registrata» in R4, T0 e T6 di PG2, R5 di PG4.

---

## 4. Il design system

La tavola `DS · Candidati dalla Trattativa 🧩` raccoglie venticinque schede. Verdetti: NUOVO se non esiste in libreria, ESPORRE se esiste ma non è pubblicato o non è adottato, CORREGGERE se esiste ed è rotto o incompleto, e ora anche RISOLTA e CHIUSA per le voci sciolte l'11/09.

### 4.1 Quattro pattern esistono già

La ricognizione dei componenti parte dalle istanze presenti nel file UI, quindi trova solo ciò che qualcuno ha già usato. Tre di questi quattro stanno fra i componenti Flowbite non adottati, cioè nelle pagine con il prefisso `----`, e uno è privato, cioè ha il nome che inizia con underscore e non compare fra gli Assets.

| Costruito a mano | Cosa c'è già in libreria |
|---|---|
| Zone di caricamento tratteggiate in PG3 | `_File upload input` Type=Advanced, pagina Forms: dropzone 384×228 con bordo tratteggiato, placeholder e bottone. Va rinominata e pubblicata, non ricostruita. |
| Foglio ancorato in basso, 14 fogli fra PG2 e PG3 | `Drawer` Type=Bottom e Type=Swipeable. Swipeable porta già la maniglia 24×4, che in PG2 è registrata come punto aperto. |
| Catena a cinque pallini in PG3 | `Stepper nav link` Type=Dot, con gli stati Initial, Active, Completed, Disabled ed Error. |
| Timeline del deposito in PG4 | `Timeline`, `Timeline Item`, `Timeline dots`. |

A questi si aggiunge la variante `Danger` degli `Alert`, già scoperta in PG3 con lo stesso meccanismo.

### 4.2 Quello che manca davvero

Undici pattern, tutti ricorrenti e tutti costruiti a mano: barra di percorso mobile (A1), barra sticky con CTA (A3), barra di progresso a segmenti (A4), riga di fatti etichettati (A6), riga di condizione (A7), riga di persona (A8), anteprima del documento (A10), card «Hai dubbi?» (A12), System Bar mobile (A13), guscio di modale desktop (B1), help contestuale «?» (C6).

`A7 · Riga di condizione` e `A8 · Riga di persona` ricorrono più di tutti e costano di più a rifare a mano. `A13 · System Bar` è l'unica eccezione dichiarata in tutti e quattro i gate di libreria: finché resta un componente locale del file UI, ogni gate futuro va giustificato a mano.

### 4.3 Quello che è rotto

1. **`Checkbox input` e `Radio item`, bordo allineato all'esterno.** Vedi §2. Da sistemare anche la taglia, che si chiama `base` per il checkbox e `Default` per il radio.
2. **`Stepper nav link` pensato per fondo scuro.** La variante Initial lega il testo a `text-ondark-medium` e su fondo chiaro sparisce, la Completed arriva arancione scuro. Ogni passo va corretto a mano, ed è successo anche nella correzione di oggi. Serve una variante on-light. Il set ha anche `State=Error`, mai usata in tutta l'epica.
3. **`Button` senza taglia Small sui pieni e sugli outline.** Verificato sulle 48 varianti: `Size=Small` esiste solo per Link-orange, Link-neg e Link-dark.
4. **`Badge` non manda il testo a capo.** Il testo ha autoresize su larghezza e altezza. L'epica ha risposto due volte in due modi diversi: in PG2 convertendo il badge del prezzo in una riga con icona, in PG3 mandando il badge sotto il nome.
5. **`Badge` senza tema neutro visibile.** Vedi §2.
6. **`Alert` Complex con bottone incorporato senza booleano.** Serve `Show button`. Secondo punto sullo stesso set: Complex scrive su `Body text` e Default su `Text`, e scrivere sulla proprietà sbagliata non dà errore, lascia il testo di default.
7. **Il colore degli Alert.** Lilla, giallo acido e verde menta sono i pastelli Flowbite di serie e stonano con il crema e l'indaco. Intervento a sé, rimandato l'8/09.

### 4.4 Le foundations

**Mancano i token di progresso.** Servono in quattro posti: barra di percorso mobile, barra dell'accordo, pallini della catena, e prima ancora la barra requisiti del Profilo immobile di Sprint 2. Oggi il segmento pieno è legato al fill del bottone primario e quello vuoto al testo primario al 15%. Servono tre token di stato, e sopra di essi i due componenti distinti che la regola a quattro casi richiede: uno stepper segmentato e una fila di pallini.

**Manca la scala tipografica mobile.** Dopo la passata di oggi restano 99 nodi di testo senza stile, istanze escluse, e le taglie dicono esattamente cosa manca: 14/Medium (28 nodi), 22/SemiBold (24), 28/Medium (16), 22/Medium (11). Sono i titoli di pagina, i titoli di sezione e le righe di etichetta del mobile.

**Il ruolo non cambia i colori, e va bene così.** Decisione dell'11/09: la distinzione cromatica per ruolo era una scelta vecchia, abbandonata. Il file è già coerente: la collezione si chiama `Alias`, ha un solo modo `Value` (`1146:2`), e Venditore e Acquirente puntano agli stessi arancioni. La skill `clecla-ds-process` descrive ancora due temi per ruolo e due mode ID, di cui uno (`3153:2`) appartiene in realtà alla collezione `Frames`: la skill va corretta, il DS no. Il ruolo continua a distinguersi per contenuto, percorso e avatar, non per colore.

---

## Nota di metodo

Tre cose da portarsi dietro.

La ricognizione dei componenti per istanze presenti nel file non è l'inventario della libreria. Ha fatto dare per mancante il colore Danger degli Alert, la dropzone di caricamento, il Drawer, i pallini e la Timeline. Per sapere cosa c'è davvero si legge il `COMPONENT_SET` e si elencano i suoi figli, e si guardano anche le pagine con il prefisso `----` e i componenti con l'underscore.

Una regola presa a metà epica non torna indietro da sola. Le tre forme del progresso, le due famiglie di Alert e la gerarchia tipografica sono nate tutte dopo che PG1 e PG2 erano chiuse, e nessuna delle tre era stata riportata all'indietro. Conviene che l'ultimo passo di ogni PG sia un giro sulle precedenti.

Quando una regola e il file non vanno d'accordo, non è detto che abbia ragione la regola. La barra dell'accordo di PG2 violava le tre forme di PG3 ed è la regola che è stata riscritta, non il disegno.
