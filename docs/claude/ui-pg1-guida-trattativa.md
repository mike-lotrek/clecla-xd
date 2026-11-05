# UI — PG1 Guida alla trattativa (Sprint 4)

File Figma: **Cleclà | UI** → pagina `🚧 UI Layouts – WIP`, sezione `PG1 · Guida alla trattativa`.

**Versione scelta: le sezioni come slide numerate**, desktop `D - B` e mobile `M - B` (decisione del 24/09, presa perché è la più vicina al vincolo del cliente su meno colore, meno avvisi, meno testo a schermo). Le versioni precedenti e le tavole che documentavano l'indice a tendina sono state archiviate lo stesso giorno: nella sezione restano solo le quattro tavole qui sotto.

Storia: pagina rifatta il 22/09 sul delta del feedback cliente del 20/09, con due ritocchi tipografici lo stesso giorno; D-A e D-B impostate fra il 22 e il 24/09, M-B il 24/09. Prima, la pagina era stata riaperta il 15/09 sulle guide del 14/09, rivista il 16/09 con il componente `Passo di percorso` e ritoccata il 17/09 sulle icone dello stepper.

| Frame | Misura | Cos'è |
|---|---|---|
| `Guida alla trattativa – D - B / sezioni come slide` | 1440 × 1602 | desktop di lavoro |
| `Guida alla trattativa – M - B / sezioni come slide` | 440 × 1700 | mobile di lavoro |
| `Sezioni come slide · i sei stati` | 1515 × 5083 | le sei slide desktop con i popover a lato |
| `Mobile · sezioni come slide · i sei stati` | 2632 × 1324 | le sei slide mobile affiancate |

Archiviate: `D - 1`, `M - 1`, `D - 2 / Popover aperti`, `M - 2 / Indice aperto`, `M - 3 / Indice agganciato`, `Come funziona · i sei passi (stati)`, `D - A / pattern «Come funziona»`. I contenuti sono tutti dentro le slide, quindi restano raggiungibili anche senza quelle tavole; i quattro popover vivono ora nella tavola desktop dei sei stati.

**La vista Acquirente non è nel file.** La documentazione la dava come `D - 3` e `M - 4`: nel file `D - 3` era invece la tavola dei popover, e la variante Acquirente non è mai esistita.

## La versione a slide

### Desktop · D - B

Shell dell'area autenticata con navbar e sidebar, colonna dei contenuti a 1284 px dopo la sidebar, contenuto centrato a 1130. Sopra, il breadcrumb e l'hero centrato sul modello della pagina pubblica «Come funziona»: titolo «Guida alla trattativa» a 48 in viola, sottotitolo a 20.

**Sotto il sottotitolo sta la CTA «Vai alla trattativa in corso»**, bottone primario centrato: è l'uscita dalla guida verso la trattativa da cui si arriva. Fino al 28/09 c'era solo sul mobile, dove viveva nella barra sticky in fondo allo schermo, elemento indipendente del frame che il clone si era portato dietro; sul desktop la CTA stava nell'intestazione della versione a documento ed è caduta insieme a quel blocco quando l'hero l'ha sostituita.

Lo stepper orizzontale porta le sei sezioni (Come funziona, Argomenti, Dichiarazioni, Data del rogito, Errori, Caparra) e naviga fra le slide. Sotto si vede una slide per volta, nella card scura da 1130 con raggio 24: numero a 60 in viola, titolo della sezione a 32, sottotitolo a 16, contenuto, e le frecce avanti e indietro in basso a destra. Il banner indaco «Hai dubbi?» chiude la pagina, con la CTA «Apri la chat».

**La sidebar è quella delle altre PG**, senza varianti: contenitore da 156 × 948 a `x 0, y 97`, sidebar interna da 92 × 900 con raggio 16 su fondo indaco, e il bottone di apertura da 32 px a `x 70, y 1045`, centrato sulla sidebar e appoggiato al suo bordo inferiore. Il 24/09 il bottone era finito a metà altezza, a `x 108, y 560`: corretto sui valori di PG3 e PG4.

La pagina intera sta in circa 1600 px di altezza contro i 3713 della versione a documento.

**L'indice «In questa pagina» e la spalla non esistono più.** Lo stepper è l'unico indice della guida.

### Mobile · M - B

Stessa struttura. La card scende a 392 px con padding 24, numero a 48 e titolo a 24; i sei passi della prima slide stanno su una colonna sola. Il banner di chiusura è lo stesso del desktop, senza pittogramma, e sotto resta la barra sticky con la CTA «Vai alla trattativa in corso»: sul mobile la stessa uscita che il desktop mette nell'hero sta ancorata al fondo dello schermo, dove resta raggiungibile durante lo scroll.

Lo stepper è la parte che il mobile risolve diversamente: **una finestra larga quanto lo schermo dentro cui la barra scorre in orizzontale**, mostrando due o tre voci per volta con quella attiva sempre in vista. È la stessa soluzione della pagina pubblica «Come funziona» su mobile, dove lo stepper delle sei fasi trabocca allo stesso modo.

**L'affordance di scorrimento** è fatta di due segnali, su ciascun lato dove c'è altro da vedere: una sfumatura da 72 px che va dal crema del fondo al trasparente, e un chevron indaco da 16 px sulla riga della barra. Compaiono solo dove servono, quindi la prima slide ha solo il chevron avanti e le ultime due solo quello indietro. La sfumatura dice che il contenuto continua, il chevron dice che si può toccare: la sola sfumatura, su una barra già tagliata a metà parola, non bastava a suggerire il gesto.

La pagina sta in 1700 px contro i 4469 della versione a documento.

### Le sei slide

| # | Slide | Contenuto |
|---|---|---|
| 01 | Come funziona | i sei passi come elenco: due colonne su desktop, una su mobile |
| 02 | Argomenti da trattare | le tre righe: prezzo, data del rogito, data di consegna delle chiavi |
| 03 | Dichiarazioni delle parti | l'introduzione, le due card delle dichiarazioni, la nota sull'avveramento |
| 04 | Quando fissare il rogito | i cinque tempi indicativi e il blocco sulla proroga |
| 05 | Errori da evitare | le sette voci |
| 06 | Perché non c'è la caparra | l'introduzione, la card della clausola penale, la nota di chiusura |

La slide 01 è l'unica riprogettata. Conteneva a sua volta una navigazione a sei passi, e annidare pallini dentro una slide numerata avrebbe messo due numerazioni nello stesso blocco: i sei passi sono diventati un elenco con il numero in viola, il turno come occhiello e il titolo. Le altre cinque riusano i contenuti della versione a documento: le card bianche funzionano sul fondo indaco, mentre i testi sciolti, le introduzioni e le note sono stati portati in negativo e le spunte dei cinque tempi sono passate al viola dei numeri.

Il numero della slide è viola in tutte e sei. Nelle slide 02-06 era diventato bianco perché la funzione che porta i testi in negativo aveva preso anche quello: corretto il 25/09.

### I popover

Nella tavola desktop dei sei stati, a destra di ogni slide stanno i popover che si aprono dai bottoni «?» di quella sezione, con l'etichetta che dice da quale bottone arrivano.

| Slide | Popover |
|---|---|
| 02 Argomenti da trattare | I mobili si trattano fuori da qui · Perché la consegna può non coincidere con il rogito |
| 03 Dichiarazioni delle parti | Il diritto di prelazione sul terreno agricolo |
| 05 Errori da evitare | Perché conviene rispondere presto |

Le slide 01, 04 e 06 non hanno bottoni «?». Due dei quattro testi sono segnaposto: quello sulla consegna delle chiavi e quello sulla prelazione, scritto sulla regola data dal cliente ma non fornito da lui.

**Sul mobile i popover non sono riportati**, perché la forma non è decisa: popover o bottom-sheet. I testi sono gli stessi della tavola desktop.

### Cosa cambia per chi legge

La pagina non si scorre più, si sfoglia: chi arriva vede una sezione sola e deve fidarsi dello stepper per sapere che ce ne sono altre cinque. Lo stepper deve restare agganciato in alto anche mentre si scorre dentro una slide, altrimenti chi arriva in fondo alla 05, la più alta, non ha modo di passare alla 06 se non tornando su. Un contenuto stampabile o cercabile con Cmd+F non esiste più.

## I contenuti delle sezioni

### Come funziona · i sei passi

| # | Turno | Titolo | Frase |
|---|---|---|---|
| 1 | Acquirente | Si apre la trattativa | La apre l'acquirente dopo la visita, con una proposta sul prezzo |
| 2 | Venditore | Il venditore risponde e dichiara le sue condizioni | risponde al prezzo e propone la data di consegna delle chiavi |
| 3 | Supporto Cleclà (opzionale) | Se vi bloccate sul prezzo, interveniamo noi | proponiamo un riferimento, decidono loro se usarlo |
| 4 | Entrambi | Fissate la data del rogito e confermate l'accordo | la data tiene conto dei tempi delle condizioni dichiarate |
| 5 | Entrambi | Indicate chi firma insieme a voi | ognuno inserisce le altre persone che firmeranno |
| 6 | Entrambi | Firma del contratto preliminare | lo scriviamo noi sugli accordi raggiunti |

Il passo 5 era lato venditore e dal 22/09 vale per entrambi, come chiesto dal cliente. Il passo 3 non promette più una valutazione certificata.

Restano i tre scostamenti dalle guide già annotati: lo stallo è un passo del racconto e non uno stato di PG2; i passi 5 e 6 in piattaforma stanno nella tappa Contratto; data del rogito e conferma dell'accordo sono fuse nel passo 4.

### Argomenti da trattare

Tre righe: prezzo, data del rogito, data di consegna delle chiavi. La riga del prezzo porta la nota sui mobili con il suo bottone info; la riga della consegna porta il bottone info sulla data. Sono usciti l'indennità di occupazione, il gruppo delle condizioni sospensive, diventato sezione, e quello delle dichiarazioni, confluito nella stessa sezione.

Nel ritocco del 22/09 la gerarchia dei due corpi è stata invertita: il paragrafo che descrive l'argomento sta su `Body/Paragraph/Regular` (16), la nota sugli arredi su `Body/Paragraph small/Regular` (14).

Le icone delle tre righe (`chart-pie`, `map-pin`, `eye`) sono quelle dei vecchi gruppi e non dicono nulla sul contenuto: sono segnaposto.

### Dichiarazioni delle parti

Apre spiegando che cos'è una condizione sospensiva, cosa che nessun frame approvato faceva. Due card: `L'acquirente dichiara` con tre punti (mutuo, vendita di un proprio immobile, terreno agricolo) e `Il venditore dichiara` con due (esistenza della relazione tecnica, regolarità). Il terzo punto dell'acquirente porta il bottone info sulla prelazione. Chiude una riga sull'avveramento e sul fatto che sul terreno agricolo il venditore agisce dopo la firma del preliminare, dichiarando l'esito dopo 30 giorni.

### Quando fissare il rogito

Nessuna condizione due mesi, mutuo tre, vendita della casa dell'acquirente sei, sanatoria sei, sanatoria e mutuo insieme nove. Del blocco `Alert` resta la sola proroga, sotto il titolo «Se servisse più tempo».

**La regola «vale la condizione più lunga» è uscita**: con i numeri nuovi sanatoria e mutuo insieme danno la somma dei due, non il massimo.

### Errori da evitare

Il punto 3 dice che una valutazione certificata non esiste e che il riferimento sul prezzo lo proponiamo noi. Il punto 7 non parla più di condizioni dichiarate a trattativa avviata, che nel modello nuovo la piattaforma impedisce per costruzione, ma di uscire dalla piattaforma e concludere fuori.

Il fondo `bg-danger-soft` con bordo rosso è caduto con la versione a documento: ora la sezione è una slide come le altre. In linea con il vincolo su meno colore, meno riconoscibile come sezione di attenzione.

### Perché non c'è la caparra

Il confronto con l'agenzia tradizionale è uscito. Resta una card con tre punti: nessun passaggio di denaro prima del rogito, 5% a carico di chi non rispetta gli accordi, preliminare concludibile senza liquidità immediata. La riga di chiusura tiene il concetto del momento in cui si versa la somma.

Il glossario non copre questo contenuto: la parola «penale» non compare in nessun frame approvato, che parlano di «costi aggiuntivi» (§15.1).

## Componenti e libreria

| Blocco | Componente |
|---|---|
| Navbar | `Navbar` Device=Desktop/Mobile, User=User |
| Sidebar dell'area autenticata | stessa di PG2, PG3 e PG4, senza varianti |
| Stepper orizzontale | `Stepper nav link` Type=Dot, State=Active/Initial |
| Finestra scorrevole dello stepper mobile | frame costruito a mano, con sfumature e chevron |
| Card della slide | frame costruito a mano, clonato dal pattern pubblico |
| Righe dei tre argomenti | `List item` Type=With right icon senza right icon |
| Proroga della data | `Alert` Type=Complex, Color=Info |
| Contenuto dei bottoni info | `Popover` Type=Default |
| Card delle dichiarazioni e della penale | frame costruiti a mano |
| Banner di chiusura | frame clonato dal banner «Iniziamo da qui?» della pagina pubblica |
| CTA | `Button` Primary / Outline-orange / Link-orange |

Candidati da portare in libreria: la card della slide e la finestra scorrevole dello stepper mobile, se il pattern regge anche su altre pagine.

## Punti aperti

- **Lo stepper deve restare agganciato** in alto durante lo scroll della slide: da dichiarare come comportamento, su desktop e su mobile.
- **La CTA «Vai alla trattativa in corso» sul desktop non è sticky**: sta nell'hero e scorre via. Da decidere se basta o se serve anche lì un'ancora persistente.
- **La forma dei popover su mobile** non è decisa: popover o bottom-sheet.
- **La vista Acquirente non esiste**: va deciso se ricostruirla e con quale delta.
- **Lo stepper della tappa Trattativa** stava in spalla e nella versione a slide non c'è: la pagina non dichiara più a che punto sei nel percorso.
- **Due popover portano testi segnaposto**, consegna delle chiavi e prelazione.
- **«Argomenti da trattare» e «Dichiarazioni delle parti» non sono in glossario.**
- **«Data di consegna delle chiavi» è una scelta fra tre forme** usate dal cliente, da confermare.
- **La clausola penale al 5% non è coperta dal glossario.**
- **Le icone dei tre argomenti sono segnaposto.**
- **Le illustrazioni di sezione non ci sono più**: da decidere se servono.
- **«Spline Sans Mono» non rende la À maiuscola**: l'occhiello «SUPPORTO CLECLÀ» si legge senza accento.
- **`text-onlight-soft` e `text-onlight-strong` hanno lo stesso valore** nel file (201650).

## Note operative

**Quando desktop e mobile nascono da cloni diversi, gli elementi fuori dal flusso si perdono.** La CTA verso la trattativa è sopravvissuta sul mobile perché lì viveva in una barra sticky, figlia diretta del frame in posizione assoluta, e sul desktop no perché stava dentro l'intestazione che è stata sostituita. Dopo una ristrutturazione conviene confrontare l'elenco dei figli di primo livello delle due tavole.

**La shell dell'area autenticata ha coordinate fisse in tutte le PG**: sidebar a `x 0, y 97` (156 × 948), bottone di apertura a `x 70, y 1045` con constraints MIN/MIN. Quando si costruisce una tavola nuova clonando la shell, quelle due posizioni vanno verificate sul riferimento di PG3 o PG4 invece che a occhio.

**`resize()` su un frame in auto layout spegne l'AUTO.** L'AUTO va rimesso dopo il resize, altrimenti i figli aggiunti non lo fanno crescere. Vale per entrambi gli assi: su un frame orizzontale l'altezza a hug è `counterAxisSizingMode = 'AUTO'`, non `primaryAxisSizingMode`. È l'errore che si ripete più spesso.

**`layoutGrow = 1` su un figlio blocca l'altezza del contenitore** quando il contenitore cambia direzione: ruotando il blocco dei sei passi da orizzontale a verticale, la colonna restava a `FILL` e tagliava il sesto passo. Va rimesso a `layoutGrow = 0` e `layoutSizingVertical = 'HUG'`.

**Lo stepper mobile scorre dentro una finestra**: il contenitore va a `layoutMode = 'NONE'` con `clipsContent = true` e larghezza dello schermo, e lo stepper si posiziona con `x` negativa per portare in vista il link attivo. Se il contenitore resta in auto layout, il figlio non si può spostare.

**Una funzione che porta i testi in negativo prende anche quelli che erano già a posto**: il numero della slide, viola per scelta, è finito bianco nelle slide 02-06. Dopo una passata del genere conviene ricontrollare gli elementi che avevano un colore proprio.

**Un'istanza di icona clonata dentro un frame nuovo può non renderizzare**, pur risultando visibile e con il fill corretto: `resize` su un'istanza non scala il contenuto e il vettore resta fuori squadra. Per segni piccoli e indipendenti conviene `figma.createNodeFromSvg`, che dà un nodo autonomo e prevedibile. È così che sono fatti i chevron dell'affordance.

**`createFrame()` nasce con `clipsContent` attivo**: ombre e code dei popover vengono tagliate se il contenitore non viene messo a `clipsContent = false`.

**`createText()` nasce con Inter Regular**: va caricato quel font, oppure impostato `fontName` prima di scrivere `characters`, altrimenti l'esecuzione fallisce e lascia nodi orfani sulla pagina, da ripulire a mano.

**`loadFontAsync` fallisce con «Cannot unwrap symbol»** quando il testo ha più font nello stesso nodo: `fontName` vale `figma.mixed`. Va caricato il font di ogni range con `getRangeFontName` prima di scrivere.

**Il font «Spline Sans» non ha lo stile Semi Bold** in questo file: dichiararlo fa fallire l'intera esecuzione. Conviene caricare il font leggendolo dal nodo o dallo stile di testo.

**Cambiare variante a un'istanza si fa con `setProperties({ State: 'Active' })`**, e gli override di colore che l'istanza portava restano attaccati al nodo, non alla variante: dopo il cambio, etichette e pallini vanno riallineati copiando i fill da un'istanza corretta. Nello `Stepper nav link` il colore sta su due nodi diversi, `Shape` per il pieno e `Frame 1` per l'anello: vanno allineati tutti e due, altrimenti resta un anello arancione attorno a un pieno viola.

**Un paint legato a variabile non sopravvive sempre a un clone ricostruito da codice.** Ricreare il paint con `setBoundVariableForPaint` dentro un ciclo su nodi clonati ha prodotto fill neri: il modo che funziona è copiare l'array `fills` da un nodo già corretto (`JSON.parse(JSON.stringify(nodo.fills))`) e assegnarlo.

**Per portare contenuti chiari su fondo scuro** conviene una funzione che risale i parent di ogni testo e lo schiarisce solo se non sta dentro un contenitore con fill chiaro: così le card bianche restano intatte e cambiano solo i testi sciolti.

**Clonare un blocco desktop dentro un frame mobile lascia larghezze fisse**: dopo il clone vanno rimessi a `FILL` i frame e a `HEIGHT` + `FILL` i testi, in profondità, altrimenti il copy esce dai bordi.

**Le card affiancate con altezza fissa tagliano il testo.** Figli a HUG, si legge la più alta, si fissa la riga a quell'altezza e si rimettono i figli a FILL.

**Le coordinate di un frame dentro una SECTION sono relative alla sezione.** La SECTION non si adatta ai figli: va ridimensionata leggendo il bounding box dei figli.

**`figma.getNodeById` non funziona** con `documentAccess: dynamic-page`: va usato `getNodeByIdAsync`.
