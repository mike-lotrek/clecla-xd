# PG2 · Passare da una trattativa all'altra

Prima di questo intervento il passaggio da una trattativa all'altra esisteva in un punto solo: il `Blocco · Trattative in parallelo`, in fondo alla pagina, sotto il documento di puntuazione. Su mobile sono circa 2000 px di scroll. In cima c'era un `Chip · trattative` che diceva «Trattativa 1 di 3», presente solo su mobile e solo in due frame su cinque, senza nessuna tavola del suo stato aperto: non era definito cosa aprisse.

Ora il chip apre l'elenco, e il chip c'è su entrambe le piattaforme.

## Cosa è stato fatto

**Nuovo frame `Foglio · Le tue trattative su questo immobile – M`** (`4185:75934`), costruito sul guscio dei fogli mobili già in uso in PG2: pagina sotto in immagine, `Dim` a `bg-surface-dark` 80%, foglio ancorato al fondo con angoli superiori a 16 e bottone di chiusura in alto a destra. Occhiello «PASSA A UN'ALTRA TRATTATIVA», titolo con l'indirizzo dell'immobile, l'elenco delle tre trattative, e in fondo il link «Vai a tutte le tue trattative».

**Nuovo frame `Pagina trattativa – D - 4 / Elenco trattative (popover aperto)`** (`4185:75993`), con lo stesso elenco dentro un popover ancorato sotto il chip, freccia allineata al centro del chip.

**Il chip è ora anche su desktop**, sotto il titolo di pagina, in `D - 1 / T2` e `D - 2 / T2b`. Le tre pagine desktop toccate sono cresciute di 46 px e sono state ridimensionate di conseguenza.

**Copy del chip cambiato**: da «Trattativa 1 di 3» a «1 di 3 su questo immobile». L'ordinale da solo non aiutava a ritrovarsi, perché l'elenco che si apre è per nome; e non diceva su cosa fossero aperte quelle tre, mentre chi vende un immobile e ne compra un altro ha trattative anche altrove.

## Dove sta il chip e dove no

Il chip compare dove esiste il blocco delle trattative in parallelo, cioè solo dal lato venditore: `T2` e `T2b`. In `T3` il blocco è ridotto alla sola frase per l'acquirente, che non vede le altre trattative del venditore, e in `T4` e `T5` l'accordo è raggiunto e il blocco non c'è. Questa regola è una conseguenza di com'erano già fatte le pagine, non una decisione presa ora: se cambia il modello (per esempio se l'acquirente deve sapere quante altre trattative ci sono, senza vedere chi), cambia anche dove sta il chip.

## Le due cose che restano decisioni aperte

**Tre nomi per la stessa destinazione.** Il breadcrumb dice «I miei immobili», il nuovo link dice «Vai a tutte le tue trattative», e nell'architettura informativa quella vista è la Bacheca. Sono la stessa pagina chiamata in tre modi. Il delta del 17/09 aveva già aperto il punto sul breadcrumb; il link del foglio lo allarga. Va scelto un nome solo, e il glossario non contiene ancora copy approvato per la trattativa, quindi la scelta è da fare, non da recuperare.

**Trattative sullo stesso immobile e trattative su immobili diversi restano separate.** Il chip e il foglio coprono solo le prime. Per le seconde c'è il link in fondo, che porta fuori. Se il caso della persona che vende e compra insieme conta, il foglio potrebbe avere due gruppi invece di uno.

## Debito tecnico

Il popover desktop è un'istanza **detached**. Il motivo: la variante `Type=Vertical items` del `Popover` è ancora quella Flowbite originale, con item da 32 px, icona social e una riga di testo, mentre qui serve un item a due righe (nome e stato) con la freccia a destra. La variante `Type=Default` ha un `Popover content` che accetta solo testo, quindi non poteva ospitare l'elenco. Quando la variante `Vertical items` verrà tematizzata nel design system, questo popover torna a essere un'istanza.

Stessa nota, già aperta altrove, per il foglio mobile: nel DS c'è `Drawer` con `Type=Bottom` e `Type=Swipeable`, non ancora adottato. Finché non lo è, i fogli di PG2 restano frame costruiti a mano.
