# Visite: consolidamento delle alternative (06/11/2026)

File Figma «Cleclà | UI», pagina Sprint 3, `UI Layouts – WIP` (3764:8875). Le versioni precedenti sono nella nuova pagina `UI Layouts – BACKUP 06.11` (6576:7030).

## Decisioni

- D-2 usa la card «Perché verificarsi» con i due badge. La stessa card passa a D-3 e D-4.
- Calendario Venditore e Calendario Acquirente usano le versioni con due tab. Le tavole con la navigazione per settimana sono tolte dal WIP.
- Prenota una visita ha due viste con lo stesso selettore a striscia:
  - modale, che si apre da «Richiedi visita» nell'annuncio
  - pagina, usata quando si parte da altri punti della piattaforma, per esempio la Bacheca

## Tavole

| Tavola | Node ID | Cosa è cambiato |
|---|---|---|
| Prenota Visite - D - 1 · Pagina | 6538:36967 | Era D-7, fuori dalla sezione. Aggiunti «Hai scelto» e «Proponi un altro orario», sottotitolo allineato alla modale, footer riposizionato |
| Prenota visita – Mobile · Pagina | 5324:196316 | Griglia sostituita con il selettore del foglio mobile, con «Hai scelto» e «Proponi» |
| Prenota Visite - D - 1 · Modale | 6421:4674 | Solo rinominata |
| Prenota visita – Mobile · Modale | 6422:5100 | Solo rinominata |
| Stato alternativo · Settimana senza orari | 6422:5013 | Invariato, vale per le due viste |
| Prenota Visite - D - 2 | 6442:6226 | Era l'alternativa badge, ora nello slot della D-2 |
| Prenota Visite - D - 3 | 5648:57268 | Card con badge. Corretto l'avatar (mostrava PH) |
| Prenota Visite - D - 4 | 5648:7459 | Card con badge |
| Modale – Proponi un nuovo orario | 5648:3626 | Aggiunti i campi Giorno e Orario, testo aggiornato. Vedi sotto |
| Calendario Visite - D - 1 · Prossime visite | 6428:5260 | Promossa |
| Calendario Visite - D - 1 · Visite passate | 6428:5917 | Promossa |
| Stato · Filtro Annullate attivo | 6428:6541 | Promosso |
| Calendario visite acquirente · Prossime visite | 6441:6076 | Promossa. Footer da utente registrato |
| Calendario visite acquirente · Immobili visitati | 6441:6573 | Promossa. Footer da utente registrato |

Tolte dal WIP (restano nel backup): Prenota Visite - D - 1 con griglia (4634:48510), D-2 base (4741:103966), Calendario Visite - D - 1 base (4535:13433), Calendario visite acquirente base (5249:193640).

Le note sotto le tavole sono state riscritte: descrivono il comportamento definitivo e non più la differenza con la versione precedente. Le sezioni sono state ricompattate e riposizionate.

## Contenuti nuovi o modificati

Modale «Proponi un nuovo orario». Con la griglia si cliccava un orario grigio e la modale partiva da quello. Il selettore a striscia non ha orari grigi, quindi giorno e ora vanno indicati nella modale.

- Testo: «Indica il giorno e l'orario che preferisci. È fuori dalle disponibilità indicate da chi vende: puoi inviare comunque la richiesta e aspettare la risposta, oppure tornare al calendario e scegliere uno degli orari disponibili.»
- Campi: «Giorno» («Scegli un giorno»), «Orario» («Scegli un orario»)

D-3 e D-4: il primo motivo diventa «La fai una volta sola: vale anche per le visite successive.», come in D-2.

## Badge di chi prenota (corretto il 06/11)

Nella card «Perché verificarsi» il badge di Giulia Rossi diceva «Identità verificata» anche prima della verifica. Ora segue lo stato: «Da verificare» in D-2 e D-3, «Verifica non riuscita» in D-4. Il badge di Marco Ferrero resta «Identità verificata».

## Punti da decidere

Col cliente:
- Le visite annullate ormai passate compaiono in «Visite passate» con il loro badge (nota già presente).
- Modale di proposta: giorno da calendario a partire da domani, orario a slot di un'ora dalle 8 alle 21. È una proposta nostra, ricavata dalla griglia precedente.
- «Cambia data» in D-2, D-3 e D-4 riporta alla vista da cui si è partiti (proposta, in nota).

Interni:
- Il calendario venditore non ha una tavola mobile. Il mobile di «Le tue visite» è allineato alle tab: `Le tue visite – Mobile · Prossime visite` (5720:76053) e `Le tue visite – Mobile · Immobili visitati` (6582:6004, nuova). La nota è in `Note · Le tue visite Mobile` (6582:6267).
- Quali CTA della Bacheca portano alla vista in pagina: non verificato.
- Il banner nell'annuncio per chi ha già visitato la casa (6442:6629) resta alternativa: non rientrava in questa richiesta e la nota ne segnala il dubbio di perimetro.
- Nei due calendari acquirente il footer mostrava «Accedi» e «Registrati» a un utente registrato: corretto. Lo stesso componente «Footer Cleclà» è in altre sette tavole di dettaglio, da controllare. Tavole: 5246:2456, 5720:77007, 5455:243318, 5720:77448, 5720:77857, 5455:244282, 5455:248456.
- Select aperti sotto le pagine: «Orario» (6608:7084) disegnato sotto la modale «Proponi un nuovo orario». Gli slot dalle 8 alle 21 restano da confermare.

## «Vedi tutti gli immobili visitati» tolto (09/11)

Il link sopra le tab ripeteva la tab «Immobili visitati», che riporta già il numero, e compariva anche con quella tab aperta. Nascosto in CA-1 (6441:6076, 6441:6573) e nei mobile (5720:76053, 6582:6004). Note «Note · Calendario Acquirente» e «Note · Le tue visite Mobile» aggiornate.

## Calendario Acquirente: blocco «In evidenza» (09/11)

In cima a CA-1 c'erano le ultime due case visitate «al posto delle due prossime visite», una scelta arrivata con l'alternativa promossa e mai motivata. Così la visita di oggi finiva sotto la piega. Ora il blocco si chiama «In evidenza» e mostra al massimo due card, in quest'ordine:
1. visita confermata di oggi o domani, con «Come arrivare» e «Vedi il dettaglio»;
2. qualcosa che aspetta una risposta di chi compra, per esempio un nuovo orario proposto da chi vende (regola scritta, card non disegnata);
3. casa visitata senza proposta né riscontro, con «Fai una proposta» o «Com'è andata la visita?».

Senza niente di urgente il blocco mostra le ultime due case visitate, come prima. Senza niente da mostrare non compare. La visita di oggi è ripetuta nella tab, di proposito. La logica è la stessa del blocco «Avvisi» in cima a CV-1.

| Tavola | Node ID |
|---|---|
| CA-1 · Prossime visite | 6441:6076 |
| CA-1 · Immobili visitati | 6441:6573 |
| Le tue visite – Mobile · Prossime visite | 5720:76053 |
| Le tue visite – Mobile · Immobili visitati | 6582:6004 |
| Stato · In evidenza senza visite imminenti | 6691:7131 |

Esempio: «Oggi, giovedì 18 settembre · 18:00», Bilocale in Corso Nizza, Cuneo, € 129.000, proprietario Luca Bianchi; poi «Visitata sabato 13 settembre», Bilocale in Via Savigliano. Il sottotitolo «Ti è piaciuta? Fai una proposta: è il primo passo della trattativa.» è nascosto: non vale per tutte le card.

Stepper tolto (09/11): la pagina «Le tue visite» raccoglie visite a immobili diversi, mentre lo stepper («Ecco dove eravamo rimasti», «Sei qui: Visita · tappa 1 di 3») segue le fasi di un acquisto specifico. Nascosti la card in spalla in CA-1 (6441:6263, 6441:6767) e la barra di percorso nei mobile (5720:76521, 6582:6014); in spalla resta «Hai dubbi?». Lo stepper resta nelle pagine di dettaglio della visita, che riguardano un solo immobile.

Da decidere col cliente: se la priorità alla visita imminente va bene anche dal punto di vista commerciale (la proposta scende al secondo posto il giorno della visita).

## Selettore acquirente: giorni senza orari e proposta (10/11)

- Tutti i giorni della striscia sono selezionabili, anche quelli senza orari (prima grigi e disattivati). In D-1 · Pagina, D-1 · Modale, nei due mobile e nello stato «Settimana senza orari» i chip «Nessun orario» hanno fondo bianco e bordo leggero.
- Giorno con orari: come prima, orari disponibili e già prenotati, più il blocco «Nessuno di questi orari ti va bene?» · «Proponi tu un orario per questo giorno: chi vende può accettarlo.» con «Proponi un altro orario». Stesso testo nelle quattro viste (prima erano due versioni diverse).
- Giorno senza orari: sotto la striscia compare «Nessun orario disponibile in questo giorno» · «Chi vende non ha indicato orari per mercoledì 17 settembre. Proponine uno tu: chi vende può accettarlo.» con «Proponi un orario». Stato disegnato sotto D-1 · Pagina (6720:7079); su mobile solo in nota.
- Modale «Proponi un nuovo orario» (5648:3626): il giorno arriva preselezionato dal calendario («Sabato 20 settembre») e si può cambiare. Nuovo testo: «Il giorno è quello che hai scelto nel calendario: puoi cambiarlo. Tra gli orari trovi solo quelli fuori dalle disponibilità di chi vende e non già prenotati. Invia la richiesta e aspetta la risposta, oppure torna al calendario e scegli uno degli orari disponibili.»
- Select «Orario» aperta (6608:7084): per sabato 20 mostra solo 8–9, 12–13, 13–14, 14–15, 17–18, 18–19, 19–20, 20–21; tolti i quattro slot disponibili e quello prenotato. Cambiando giorno la lista si aggiorna e l'orario scelto si azzera.
- Campo «Giorno» (aggiornato il 10/11, supera il calendario del 09/11): select con i soli sette giorni della settimana mostrata nel calendario, da «Lunedì 15 settembre» a «Domenica 21 settembre». Per un'altra settimana si torna al calendario. Lo stato aperto (6722:7085) sostituisce il calendario 6683:7144, eliminato.
- Campo «Giorno» bloccato (10/11, supera la select qui sopra): il giorno arriva preselezionato dalla striscia e non si cambia nella modale. Stile dei campi con lucchetto (come Categoria catastale): fondo e bordo di Input field, testo al 60%, icona `icon/lock` al posto della freccia. Per cambiare giorno si torna al calendario con «Torna al calendario». Lo stato con la select aperta (6722:7085) è eliminato; lo stato «Orario» aperto (6608:7084) è spostato sotto la modale al suo posto. Testo della modale: «Il giorno è quello che hai scelto nel calendario. Tra gli orari trovi solo quelli fuori dalle disponibilità di chi vende e non già prenotati. Invia la richiesta e aspetta la risposta, oppure torna al calendario per scegliere un altro giorno o uno degli orari disponibili.» Nota sotto la modale (6578:6537) aggiornata; il bottone si attiva con l'orario scelto.
- Stato mobile del giorno senza orari (6722:7124), sotto «Prenota visita – Mobile · Pagina»: stesso avviso e «Proponi un orario» del desktop.

Per fare posto allo stato nuovo, le righe sotto D-1 · Pagina nella section Prenota Visita sono scese di 449 px, poi di altri 566 px per lo stato mobile; le section sotto sono state riposizionate con lo stacco di 1000 px.

Modale e foglio mobile allineati alla pagina (10/11):
- In D-1 · Modale (6421:4674) e nel foglio mobile (6422:5100) il blocco «Proponi un altro orario» non sta più in fondo alla modale: è dentro il calendario, sotto gli orari del giorno scelto.
- Il testo introduttivo perde «Nessuno va bene? Proponi tu data e ora.»: resta «Scegli un giorno e un orario tra quelli indicati da chi vende.»
- Stato «Settimana senza orari» (6422:5013): testo aggiornato in «Chi vende non ha indicato orari per questa settimana. Guarda la settimana successiva, oppure scegli un giorno e proponi tu un orario.»
- Nuovi stati «Giorno senza orari»: modale desktop (6723:7091, sotto «Settimana senza orari») e foglio mobile (6723:7164, sotto la sua nota). La section Prenota Visita si è allungata; le section sotto sono state riposizionate.

Un giorno bloccato con «Blocco date» equivale a un giorno senza orari: avviso e proposta possibile (deciso il 10/11).

## Calendario Venditore: settimane e filtro «Passate» (10/11)

Supera la versione con le tab del 06/11 per il solo calendario venditore. Tornano la navigazione per settimana della versione nel backup e la lista cronologica della settimana; le tab sono nascoste. Ai filtri si aggiunge «Passate».

- Settimana in corso (6428:5260, ex «Prossime visite»): 15–21 settembre, oggi giovedì 18. Filtri attivi di default «Da confermare» e «Confermate»; «Annullate» e «Passate» spenti. Le visite di lunedì 22 e domenica 28 sono nascoste: stanno nella settimana dopo.
- Settimana passata (6428:5917, ex «Visite passate»): 8–14 settembre, visite in ordine cronologico. Il filtro «Passate» è disattivato (opacità 40%), perché la settimana contiene solo visite passate.
- Stato «Filtro Passate attivo» (6725:13984): settimana in corso con «Passate» acceso, compare la visita già fatta di martedì 16 settembre (Irene Viale, «Com'è andata la visita?») prima di quella di oggi.
- Stato «Filtro Annullate attivo» (6428:6541): tab tolte, chip «Passate» aggiunto, data della visita annullata spostata a sabato 20 settembre per stare nella settimana.
- Sottotitoli sopra le tavole e nota «Note · Calendario Venditore» riscritti.

Nelle settimane passate i filtri «Da confermare» e «Confermate» non compaiono: restano «Annullate» e «Passate» disattivato (deciso il 10/11).

## Le tue visite (Acquirente): settimane e filtro «Passate» (10/11)

Stesso trattamento del Calendario Venditore: niente tab, navigazione per settimana, filtro «Passate».

| Tavola | Node ID | Cosa mostra |
|---|---|---|
| Calendario visite acquirente · Settimana in corso | 6441:6076 | 15–21 settembre: oggi 18 (Corso Nizza) e sabato 20 (Via Roma 12). Domenica 28 nascosta, è nella settimana dopo |
| Calendario visite acquirente · Settimana passata | 6441:6573 | 8–14 settembre: giovedì 11 (Corso Giolitti) e sabato 13 (Via Savigliano). Filtri: solo «Annullate» e «Passate» disattivato |
| Le tue visite – Mobile · Settimana in corso | 5720:76053 | Come il desktop, con la navigazione per settimana aggiunta |
| Le tue visite – Mobile · Settimana passata | 6582:6004 | Come il desktop |
| Stato · Filtro Passate attivo | 6727:7190 | Settimana in corso con la visita già fatta di martedì 16 settembre in cima |

Il blocco «In evidenza» resta in cima. Con le tab sparisce «Immobili visitati»: le case visitate si ritrovano nelle settimane passate e, se serve agire, nel blocco «In evidenza». Note e sottotitoli sopra le tavole riscritti.

## Card della lista visite su mobile: due proposte (10/11)

Le card della lista in «Le tue visite» mobile sono alte circa 560 px. Le card di «In evidenza» restano come sono. Due proposte disegnate sotto i mobile, da scegliere col cliente:

| Proposta | Node ID | Cosa resta visibile |
|---|---|---|
| A · Card compatta (scelta) | tolta dopo l'applicazione | Foto 88 px a sinistra, accanto stato, data, immobile e prezzo; sotto proprietario e azioni. Il messaggio va nel dettaglio. Circa 200–260 px |
| B · Card chiuse | tolta | Foto 56 px, stato, data, immobile e prezzo, chevron. Circa 150 px |
| B · Card aperta | tolta | La card si apre sul posto con proprietario, messaggio e azioni; una aperta alla volta |

Indirizzo sotto la riga principale (10/11): in alto foto 88 px a sinistra con stato e data accanto, sotto a tutta larghezza immobile e prezzo, poi proprietario e azioni. La foto è stata provata a destra e poi riportata a sinistra, come su desktop e in «In evidenza». Scelta la proposta A (10/11) e applicata alle card della lista nei due mobile (5720:76053, 6582:6004), comprese le card nascoste. Le tavole delle proposte e la loro nota sono state tolte. Nelle visite passate stato «Passata» in alto nella colonna e azioni «Com'è andata la visita?» / «Fai una proposta» sotto. La stessa card varrà per il calendario venditore se avrà una tavola mobile.

## Pulizia dei livelli nascosti in «Le tue visite» (10/11)

Eliminati i livelli nascosti nelle quattro tavole (desktop e mobile, settimana in corso e passata): barre delle tab, card di altre settimane, chip dei filtri non più usati, stepper e barra di percorso tolti il 09/11, link «Vedi tutti gli immobili visitati», sottotitolo di «In evidenza», messaggio e «In attesa che Marco confermi la visita» nelle card compatte del mobile. Restano solo i livelli nascosti interni ai componenti.

La card annullata del 9 settembre è diventata lo stato «Settimana passata con filtro Annullate attivo» (6734:7107), sotto la tavola della settimana passata, con «Fissa un altro appuntamento». Nel mobile il bottone «Riparti dalla ricerca» della card annullata, nascosto per errore, era stato ripristinato prima della pulizia; la card è stata poi eliminata con le altre nascoste.

## Pulizia dei livelli nascosti nel Calendario Venditore (10/11)

Eliminati i livelli nascosti in settimana in corso (6428:5260), settimana passata (6428:5917) e nei due stati dei filtri: tab, card di altre settimane, chip non più usati, «Conteggio» e «Ultime attività» nello stepper, un bottone e la riga «Davide ha confermato il suo interesse» nella card del 13 settembre.

Prima della pulizia, le card utili sono diventate stati sotto «Filtro Passate attivo»:
- «Settimana passata con filtro Annullate attivo» (6736:7408): la visita annullata di martedì 9 settembre in cima, poi l'11 e il 13.
- «Settimana successiva» (6736:7673): 22–28 settembre, con la proposta fuori orario di Matteo Bo (lunedì 22) e la visita di Laura Bruno (domenica 28).

Nota e sottotitolo della colonna degli stati aggiornati.

## Titolo dello stepper (10/11)

Il titolo dello stepper in spalla ripeteva il primo step («Prenota una visita»). Ora è «Visite» in D-1 · Pagina, D-2, D-3, D-4, D-5, D-6 e D-7 (Richiesta visita inviata). Gli step restano «Prenota una visita», «Verifica identità», «Riepilogo». La barra mobile («Sei qui: Prenota una visita · tappa 1 di 3») non mostra il titolo e resta com'è. Da registrare nel glossario.

## Giorno della proposta: calendario invece della select (09/11, superato il 10/11)

La select «Giorno» elencava solo la settimana in corso (15–21 settembre), compresi giorni già passati, mentre la nota diceva «a partire da domani». Il campo «Giorno» della modale (6577:7089) è ora un campo data con icona calendario. Lo stato aperto (6683:7144) sostituisce la select aperta 6608:7058 e mostra due mesi: settembre con i giorni fino a oggi disattivati, ottobre fino al 15. Selezionato venerdì 2 ottobre.

Copy: «Puoi proporre un giorno da domani fino al 15 ottobre.» · «Il calendario si chiude appena scegli un giorno.»

Da decidere col cliente:
- Orizzonte di 4 settimane: è una nostra proposta, per non ricevere proposte per date in cui l'annuncio potrebbe non essere più online.
- Giorni bloccati dal venditore disattivati anche qui: dipende dalla decisione su «Blocco date» (vedi `pubblicazione-annuncio-06-11.md`).

Su mobile il calendario si apre in un foglio dal basso, un mese alla volta: non disegnato.

## Discrepanze segnalate, non risolte

- Nomi fittizi: risolto il 06/11, vedi `visite-presentazione-06-11.md`. Restano da allineare prezzo e titolo dell'immobile.
- Etichette della proposta: «Proponi un altro orario» (bottone), «Proponi un nuovo orario» (titolo modale), «Proponi nuovo orario» (CTA).
- Etichette d'ingresso: «Richiedi visita» nell'annuncio, «Prenota una visita» nello stepper.

## Termini da registrare nel glossario

Il glossario non ha copy approvato per le visite. Da registrare: «Hai scelto», «Nessun orario va bene?», «Proponi un altro orario», «Prossime visite», «Visite passate», «Immobili visitati».
