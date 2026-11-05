# Rework PG1 dopo il feedback del 20/09

Versione 2.0 · 22/09/2026 · rework eseguito sulle tavole della pagina `🚧 UI Layouts – WIP`, sezione `PG1 · Guida alla trattativa`, file **Cleclà | UI** (`0k5JkkrVwDydzvUoRHv8ye`).

Il cliente ha sciolto i cinque punti che bloccavano il rework, quindi le modifiche sono state applicate. Restano tre segnaposto dichiarati, elencati in fondo.

## Le risposte del cliente

La navigazione a pallini vale **solo per la sezione «Come funziona»**, non per tutta la guida. L'indice «In questa pagina» resta quindi in spalla sul desktop e come barra a tendina sul mobile: perde la voce «Dopo la firma» e guadagna «Condizioni sospensive». Le tavole M-2 e M-3, che documentano gli stati dell'indice mobile, restano in perimetro.

Sul diritto di prelazione il cliente ha dato la regola, non il testo: se la scheda tecnica segnala il terreno, all'acquirente si chiede se compra anche quando il terreno va a chi ha diritto di prelazione; il venditore in questa fase non fa nulla e porterà la proposta agli aventi diritto dopo la firma del preliminare, dichiarando l'esito dopo 30 giorni; se il terreno non c'è, la domanda non compare. Il popover in pagina riporta questa regola ed è dichiarato segnaposto.

Il popover sulla data di consegna è anch'esso un segnaposto scritto da noi. L'illustrazione della sezione sulla penale resta quella attuale.

Le trattative partono dalla Bacheca: è lì che l'acquirente salva gli immobili cercati, visitati e in trattativa, e dopo la visita decide se aprirne una. Questo chiude la prima delle sei domande aperte del delta e vale per PG2, non per PG1.

## Cosa è cambiato in pagina

**Come funziona.** Lo step-walker a sei card in accordion è sostituito da una linea orizzontale di sei pallini numerati con sotto il blocco del passo selezionato. Il testo introduttivo è uscito. Il bottone +/− dentro la card è nascosto: il comando ora è il pallino, e due comandi per la stessa cosa sarebbero uno di troppo. Il titolo del passo ha perso la numerazione, che sta nel pallino. Ogni passo porta una frase sola.

Due contenuti cambiano oltre alla forma. Il passo 5 passa da «Il venditore indica chi vende insieme a lui» a «Indicate chi firma insieme a voi», con turno ENTRAMBI, come chiesto. Il passo 3 non promette più una valutazione certificata.

**Cosa si tratta.** Da quattro righe a tre argomenti: prezzo, data del rogito, data di consegna delle chiavi. Escono l'indennità di occupazione, le condizioni sospensive (che diventano sezione) e le dichiarazioni (che confluiscono nella stessa sezione). Sul mobile sono spariti i bottoni di apertura: tre righe brevi non hanno bisogno di essere espandibili, e i testi che erano nascosti nelle righe chiuse ora si leggono. Il bottone info sulla data di consegna è in entrambe le versioni.

La nota sui mobili è riscritta come chiesto: arredi ed elettrodomestici non si trattano, la cucina entra nel prezzo se la si vuole, basta scriverlo nelle note della proposta, e nessun modulo viene generato.

**Condizioni sospensive.** Sezione nuova fra «Cosa si tratta» e «Quando fissare il rogito». Spiega cos'è una condizione sospensiva, poi due card affiancate con le dichiarazioni delle due parti: tre per l'acquirente (mutuo, vendita di un proprio immobile, terreno agricolo), due per il venditore (esistenza della relazione tecnica, regolarità). Chiude con l'avveramento e con la regola sulla prelazione. Il bottone info sul terzo punto dell'acquirente apre il popover sulla prelazione.

**Quando fissare il rogito.** Otto voci diventano cinque tempi indicativi: nessuna condizione due mesi, mutuo tre, vendita della casa dell'acquirente sei, sanatoria sei, sanatoria e mutuo insieme nove. Il sottotitolo dice «la data» e non più «le date». Del blocco informativo resta la sola proroga, sotto il titolo «Se servisse più tempo»; la regola «vale la condizione più lunga» è uscita perché con i numeri nuovi non regge, dato che sanatoria e mutuo insieme fanno la somma dei due.

**Errori da evitare.** Il punto 3 dice che una valutazione certificata non esiste e che se la distanza sul prezzo resta siamo noi a proporre un riferimento. Il punto 7 non parla più di condizioni dichiarate a trattativa avviata, cosa che nel modello nuovo la piattaforma impedisce per costruzione, ma di uscire dalla piattaforma e concludere fuori, perdendo il supporto legale sul preliminare.

**Perché non c'è la caparra.** Le due card a confronto con l'agenzia tradizionale sono uscite. Resta una card sola con i tre punti chiesti: nessun passaggio di denaro prima del rogito, 5% a carico di chi non rispetta gli accordi, preliminare concludibile senza liquidità immediata. La riga di chiusura tiene il concetto del momento in cui si versa la somma.

**Cosa può succedere dopo la firma.** Sezione rimossa da desktop e mobile. Il contenuto su recesso, inadempimento e inefficacia va nella guida contestuale del preliminare, in PG3 F4. La sua illustrazione, la busta, è passata alla sezione sulle condizioni sospensive, così le due sezioni non condividono più la spunta.

## Le tavole

| Tavola | Misura | Stato |
|---|---|---|
| `Guida alla trattativa – D - 1` | 1440 × 3713 | desktop di lavoro, era 4555 |
| `Guida alla trattativa – M - 1` | 440 × 4469 | mobile di lavoro, era 5871 |
| `Guida alla trattativa – D - 2 / Popover aperti` | 1440 × 3713 | rifatta da D-1, quattro popover |
| `Guida alla trattativa – M - 2 / Indice aperto` | 440 × 4469 | rifatta da M-1, tendina a sei voci |
| `Guida alla trattativa – M - 3 / Indice agganciato` | 440 × 900 | rifatta da M-1 |
| `Come funziona · i sei passi (stati)` | 914 × 1801 | tavola nuova, i sei stati dei pallini |

La tavola dei popover si chiamava D-3 e portava quel nome pur essendo lo stato dei popover: ora si chiama D-2, come la documentazione dichiarava. I popover sono quattro: mobili, consegna delle chiavi, prelazione agraria, risposta in tempi ragionevoli.

La tavola dei sei stati serve a leggere in una volta i sei testi e a vedere come si comporta la navigazione, visto che in pagina se ne vede uno per volta.

## Quello che non è stato fatto

**La vista Acquirente non esiste più nella sezione.** La documentazione la dava come `D - 3` e `M - 4`; nel file quei frame non ci sono e il nome D-3 era usato dalla tavola dei popover. Il rework è quindi solo sulla vista Venditore. Va deciso se ricostruire la vista Acquirente, e in quel caso il delta da applicare è quello già descritto: ruoli ribaltati nei passi 1, 2 e 5, lista dei tempi dal lato di chi compra, breadcrumb «Le mie trattative».

**Lo stepper di spalla non è stato toccato.** Il cliente chiede di ripensarlo dopo la ristrutturazione della pagina: ora che la pagina è più corta di un quinto, la spalla ha proporzioni diverse e la richiesta si può affrontare.

**La sidebar resta com'è**, con la freccia di apertura. È il punto su cui controproponiamo, come già scritto nel delta.

## Segnaposto e discrepanze da chiudere

I due popover nuovi portano testi scritti da noi sulla regola data dal cliente, non testi del cliente. La nota sopra la tavola D-2 lo dichiara.

Tre discrepanze di glossario restano aperte e non le abbiamo risolte in autonomia. «Argomenti da trattare» e «Dichiarazioni delle parti» sono termini nuovi che il glossario non conosce: in pagina sono usati come nomi dei contenitori. Per la data di consegna abbiamo scelto «Data di consegna delle chiavi», che sta fra le tre forme usate dal cliente e quella dei frame approvati: va confermata, anche perché in T4 di PG2 il cliente scrive «Data consegna delle chiavi dell'immobile». La clausola penale al 5% resta un contenuto che il glossario non copre: nei frame approvati la parola «penale» non compare e si parla di «costi aggiuntivi».

Restano vere due cose già note: le icone dei tre argomenti sono segnaposto e non dicono nulla sul contenuto della riga, e le illustrazioni di sezione non sono state scelte per significato.
