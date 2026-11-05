# Trattativa · tavole su due rail (Venditore e Acquirente)

15/10/2026, aggiornato il 19/10 · file «Cleclà | UI», Sprint 4 «🚧 UI Layouts – WIP» (44:983). Backup completo prima dello spostamento: pagina «💿 UI Layouts – Backup 15.10» (5785:8158).

Stessa organizzazione della Finalizzazione: una panoramica a box allineati per passo, poi un percorso per target diviso in fasi. Ogni fase ha le tavole desktop in una riga, le note sotto ciascuna tavola desktop e le mobile nella riga più in basso.

## Struttura della pagina, dall’alto

1. `PG1 · Guida alla trattativa v2` (3707:110792): una sola, vale per entrambi i target.
2. `Panoramica · Trattativa · Venditore e Acquirente` (5785:25291): riga Venditore e riga Acquirente, box bianchi per le tavole che esistono, box tratteggiati «DA DISEGNARE» per i buchi.
3. `Percorso Venditore · Trattativa` (5785:25251), cinque fasi:
   1. Prima proposta e prima risposta: onboarding, T1 ricevuta, modali P1–P5, T1 in preparazione, B2.
   2. Trattativa in corso: lista trattative dell’immobile (con stato vuoto e nota sotto), T2, elenco dal chip, nota lunga aperta, R1–R3, T2b, T2c.
   3. Chiusura e accordo: T3b, T4, T5, X1.
   4. Preparazione alla firma: F1, pannelli di caricamento (carta, passaporto, dati letti, segnala), F1b, F2a–F2d con la modale di modifica, F3.
   5. Registrazione del contratto preliminare: R4.
4. `Percorso Acquirente · Trattativa` (5785:25257), stesse cinque fasi: A-P1, A-P2, T1 inviata; T3a, T3, T3r, R4; F1, F3; R0, R1, R1b, R2, R3.
5. `Variante · Immobile con terreno agricolo` (5959:8249), dal 19/10.
6. `Riferimenti · contenuti dei bottoni info e note di flusso` (5785:25290): popover di PG3 e PG4, card della Bacheca acquirente (epica Visita), immagine e link al documento Google, nota sul caricamento dei documenti.

## Riepilogo degli accordi in pagina (19/10)

La pagina figlia «Riepilogo degli accordi» non esiste più. Il riepilogo sta in fondo alla pagina Trattativa, prima di «Annulla la trattativa», con titolo «Riepilogo degli accordi», una riga di introduzione e due box:

- **Argomenti · N di 3 concordati**: prezzo, data del rogito, data di consegna delle chiavi. Concordato: «Concordata» e il valore. In trattativa: «In trattativa · ultima proposta [valore]» e «Da concordare».
- **Condizioni sospensive**: nome, scadenza, «comunica: [nome] ([ruolo])», o «tu» per chi guarda.

I valori sono presi dalle righe della stessa tavola, quindi ogni stato ha il suo riepilogo coerente. Applicato a 11 tavole desktop (T1 ricevuta, T1 in preparazione, T2, elenco dal chip, T2b, T2c, T3b, T1 inviata, T3a, T3, T3r) e 10 mobile. Su mobile le righe sono impilate. Dopo l’accordo la pagina resta come T4 e T5: riepilogo e «Cosa succede dopo».

Rimossi:

- il link «Riepilogo degli accordi» nella spalla della Trattativa, di Preparazione alla firma, di Pagamento registrazione e delle pagine della Finalizzazione (98 istanze in tutto). In Preparazione alla firma la sintesi «Le vostre condizioni, in sintesi» copre lo stesso bisogno;
- «Vedi il riepilogo» in testa a «Cosa state trattando» e «Vedi il riepilogo degli accordi» in F1;
- le tavole D-6 e M-6, spostate nella pagina «💿 UI Layouts – Backup 15.10», sezione «Riepilogo degli accordi · pagina figlia rimossa il 19/10», con la nota sull’architettura;
- il segnaposto acquirente e i due box in panoramica.

Non serve più aggiungere il Riepilogo all’architettura.

## Variante · immobile con terreno agricolo (19/10)

Decisione: il terreno agricolo genera una condizione sospensiva sulla prelazione agraria, in carico al venditore. L’acquirente risponde a una domanda che decide cosa succede se la prelazione viene esercitata.

Tavole, desktop e mobile, nell’ordine del flusso:

- **A-P1t · Fai una proposta, Le tue dichiarazioni**: terza domanda «Se chi ha diritto di prelazione compra il terreno agricolo, compri comunque la casa senza il terreno?», Sì/No, con la spiegazione degli effetti. Compare solo se il venditore ha dichiarato il terreno nella scheda; si fa nella prima proposta (§4.3 del documento del cliente).
- **T1t · prima proposta ricevuta, vista venditore** (desktop `5963:8761`, mobile `5963:9142`): le dichiarazioni di Marco sono «1 di 3 completate». Il terreno è già dichiarato dalla scheda, con la condizione sulla prelazione e la riga «Per correggerla modifica la scheda dell’immobile»; relazione tecnica e regolarità sono «Da completare» con «Rispondi». Le dichiarazioni di Giulia sono 3 di 3, con la risposta sulla prelazione. Stepper e riepilogo aggiornati. Nota «STATO» sotto la tavola.
- **T3t · vista acquirente**: nelle tue dichiarazioni la risposta «Sì» con l’effetto «Se il terreno va a chi ha la prelazione, compri solo la casa». Nelle dichiarazioni di Marco «C’è un terreno agricolo nella compravendita? Sì, dalla scheda dell’immobile», la condizione «esito della prelazione agraria», scadenza «[da confermare]» e «Dopo la firma del preliminare Marco Ferrero avvisa chi ha diritto di prelazione e vi comunica l’esito». Conteggi a 3 di 3, anche nello stepper. Riepilogo con tre condizioni, la prelazione comunicata da Marco.
- **T2t · vista venditore**: stessa trattativa vista da Marco, con i testi alla seconda persona dalla sua parte.

Punti aperti, in nota:

- **Prezzo**: se il terreno va a chi ha la prelazione e l’acquirente compra solo la casa, di quanto scende il prezzo? Da verificare con il team legale se l’avviso a chi ha la prelazione deve indicare il prezzo del terreno.
- **Tempi**: i tempi minimi del rogito (fase 3) non includono la prelazione. Va deciso se il tempo per rispondere di chi ha la prelazione entra nel calcolo e nella scadenza della condizione.
- **Glossario**: «prelazione agraria» (Finalizzazione) contro «esito del diritto di prelazione sul terreno agricolo» (documento del cliente). La PG della Finalizzazione assegna la condizione ad acquirente o venditore: va allineata al venditore.
- Esempio sullo stesso immobile delle altre tavole (Trilocale in Via Roma 12) per coerenza: va valutato se usare un immobile più verosimile con terreno.

## Note sotto le tavole desktop (15/10)

Stesso componente visivo delle note della Finalizzazione (bordo bianco, occhiello «NOTA · …», testo). Le note dicono punti aperti, regole di comportamento e varianti di stato:

- Venditore 1 · T1 in preparazione: invio unico nel primo turno. P1: rifiuto del prezzo al primo turno, da confermare se il resto dell’invio parte lo stesso.
- Venditore 2 · T2: comportamento dello stepper di spalla (#291); regole dello storico e del «Leggi di più» (#287); il popover del chip chiude con «Vai alla bacheca». R1: turni successivi senza B2. T2b: vista acquirente da disegnare; media quando una parte ha solo rifiutato, da confermare. Lista trattative: stato vuoto e nota già presenti.
- Venditore 3 · T3b: specchio acquirente da disegnare. T4: blocco delle altre trattative (#276, da decidere se si riaprono) e modello della pagina. T5: chip «Altre 2 trattative bloccate». X1: nuova trattativa dopo l’annullamento (#277) e annullamento chiesto dall’acquirente, da disegnare.
- Venditore 4 · F1: chi inserisce i dati dei cointestatari; breadcrumb di PG3 e PG4 da confermare. Pannello di caricamento: termini fuori glossario, opzioni dell’attività lavorativa, scelta carta/passaporto da confermare. F2a: tutto in FEQ. F2b: risposte scritte di Cleclà senza nuova versione. F2d (nota 5807:183): da confermare con lo sviluppo se Cleclà sa che il firmatario ha completato la firma su Youtrust o solo che l’ha avviata.
- Acquirente 2 · T3: blocco informativo sulle trattative in parallelo. T3r: come si legge il rifiuto. Acquirente 4 · F1: comunione legale anche con acquisto al 100%. Acquirente 5 · R1b: deposito da quietanza o da accredito, glossario quietanza/ricevuta. R2: ricevuta di pagamento contro ricevuta delle imposte, da confermare; R3: documenti dopo la registrazione.

## Rifiuto del prezzo (15/10)

- **Gerarchia.** In P1 e R1, desktop e mobile, «Rifiuta» è un link secondario (Link-dark, Small) centrato sotto «Fai una controproposta».
- **Vista di chi riceve.** T3r · Prezzo rifiutato da Marco (Acquirente), desktop `5846:8405` e mobile `5846:211203`: badge «Rifiutata», motivazione di Marco, «Il prezzo resta da concordare: puoi fare una nuova proposta a Marco Ferrero.» e CTA «Fai una nuova proposta».
- **Da confermare**: la media dello stallo quando una parte ha solo rifiutato (proposta: prezzo dell’annuncio); il rifiuto del prezzo nella prima risposta a invio unico.

Da rigenerare: i fondi PNG delle modali di prezzo mostrano ancora la breadcrumb «I miei immobili».

## F2d e «Riapri la firma su Youtrust» (15/10)

F2d mescola firma aperta ma non completata e firma completata in attesa di validazione. Domanda aperta allo sviluppo, in nota sotto la tavola: se Cleclà distingue i due casi, F2d diventa due stati (con «Riprendi la firma su Youtrust» e senza bottone); se no, il bottone resta secondario con una riga che dice a chi serve. Si lega al punto aperto sulla pagina di rientro da Youtrust.

## «I miei immobili» non è una pagina (15/10)

Chi vende vede tutti i suoi immobili nella Bacheca. Il link finale del popover del chip è «Vai alla bacheca». I link di ritorno mobile sono allineati al livello sopra nella breadcrumb desktop: «‹ Trattative» per le pagine trattativa del venditore e la Guida; «‹ Trilocale in Via Roma 12, Cuneo» per Preparazione alla firma e Pagamento registrazione.

## Buchi del flusso (segnaposto tratteggiati nel percorso Acquirente)

Lato acquirente:

- Fase 2 · T2b/T2c vista acquirente: come vede il suggerimento della media e la media proposta.
- Fase 3 · T3b chiusura bloccata; T4 accordo da confermare; T5 trattativa chiusa.
- Fase 3 · Trattativa annullata dal venditore, con la possibilità di aprire una nuova trattativa (#277).
- Fase 3 · Trattativa bloccata perché il venditore ha confermato un altro accordo (#276).
- Fase 4 · F1b documenti completi; F2a–F2d contratto preliminare, benestare e firma.

Lato venditore: trattativa annullata dall’acquirente.

I segnaposto sono solo desktop: le versioni mobile vanno aggiunte quando le tavole si disegnano.
