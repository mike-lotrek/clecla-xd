# Revisione dei wireframe — decisioni e stato

Aggiornato al 18/08/2026. È il punto di verità su cosa è stato deciso e cosa resta aperto. **46 frame.**
Il confronto campo per campo con la Scheda Tecnica 2.0 sta in `claude/scheda-tecnica-2.0-delta.md`.

## Vincoli di lavorazione

- I frame stanno dove li ha messi Matteo: si lavora **in place**.
- Sidebar e navigazione restano **ingombri tratteggiati** nelle pagine nuove.
- I commenti Figma non sono leggibili da qui: serve un nuovo token in `FIGMA_ACCESS_TOKEN`.
- **Le annotazioni native vanno scritte con la pagina in focus**, una a una: scritte in blocco fuori dalla pagina attiva Figma ne scarta una parte senza errore.
- Riferimento ufficiale per i contenuti della scheda: **`20260331_Scheda Tecnica 2.0.xlsx`**.

## Il modello: due binari paralleli

| Binario | Sequenza |
|---|---|
| **Dati** | scheda tecnica → studio di vendibilità → conferma del prezzo |
| **Contratto** | documento d'identità → incarico di mediazione firmato |

Si incontrano solo alla pubblicazione. **Sono davvero paralleli**: dall'allegato dello studio di vendibilità risulta che la stima si calcola dai dati della scheda più le **quotazioni OMI dell'Agenzia delle Entrate**, che sono pubbliche. Nessuna dipendenza da visura o planimetria, quindi nessuna dipendenza dall'incarico.

Il punto di contatto era la **superficie commerciale**: **è stata resa un dato dichiarato dal venditore**, non derivato dalla visura. Con questa scelta i due binari restano indipendenti.

Ne segue che le frasi assolute vanno rese dipendenti dallo stato: S6 dice *«È l'ultimo requisito che manca»* e S4 *«È l'ultimo dei due requisiti»* — vere solo su un percorso. **Da fare**: tre varianti del banner dello studio (è l'ultima cosa / puoi farlo quando vuoi, intanto ti manca X / il prezzo l'hai già confermato).

## L'annuncio privato e la navigazione

Il profilo immobile **è il gemello privato dell'annuncio** e resta consultabile per sempre, anche dopo la pubblicazione. Prima non era così: da S5 in poi la scheda tecnica spariva e S8 non aveva nessun accesso ai dati dell'immobile.

**Niente tab.** Una tab che non puoi ancora usare è un vicolo cieco e costringe a disegnare N stati vuoti. Al suo posto il pannello «Cosa manca per pubblicare» è stato **promosso a indice**, si chiama **«Il tuo immobile»** e cambia ruolo lungo il viaggio:

```
IL TUO IMMOBILE                              [–]
  ▓▓░░░░  3 di 4 per pubblicare      (sparisce dopo la pubblicazione)
  ✓ Scheda tecnica            salvata il 05/09          ›
  ✓ Verifica dell'identità    confermata il 07/09       ›
  ○ Incarico di mediazione    pronto da firmare         ›
  ⊖ Prezzo di pubblicazione   arriva con lo studio          (non cliccabile)
  ──────────────────────────────────────────────
    Annuncio pubblico         online dal 20/09          ›
    Documenti dell'immobile   28 di 32                  ›
    Visite                    2 richieste in attesa     ›
    Storico attività          18 movimenti              ›
  ──────────────────────────────────────────────
    Serve per vendere         4 di 4                    ⌄
```

**Lo stato vuoto è una riga, non una schermata.** La voce non ancora disponibile è in grigio, senza chevron, e la sua sottoriga dice *perché*: «si genera a identità confermata», «arriva con lo studio di vendibilità». Non ci si atterra mai sopra, quindi non serve disegnare stati vuoti per la firma o per il prezzo.

Il secondo gruppo è **l'annuncio privato**: quello che resta raggiungibile sempre. Dopo la pubblicazione la barra di progresso sparisce e compare la riga «Annuncio pubblico», che è l'unica cosa che l'acquirente vede.

Applicato a: **10 frame desktop** del profilo immobile (S1–S8b più il frame ingombri), **5 frame dell'Archivio** — dove convive con «A che punto sei», che tiene i traguardi dell'archivio, e la riga «Documenti dell'immobile · sei qui» marca dove sei — **5 barre sticky mobile** e il **bottom-sheet**, che era rimasto sul vecchio modello a 6 requisiti (APE, lettura studio, visura, materiale multimediale).

## Prezzo e valutazione: decide il venditore

**Il prezzo lo decide sempre e comunque il venditore.** Quello in scheda è **provvisorio**, resta modificabile e non è la cifra che finisce nell'annuncio. Lo **studio di vendibilità è un consiglio professionale**, non una regola.

Riscritti: il banner (era «Questa cifra non compare mai nell'annuncio» → **«Il prezzo lo decidi tu: questo è provvisorio»**), l'intro della sezione, il testo dello studio, le annotazioni, e in S6 desktop e mobile «Non è un prezzo imposto: è un consiglio professionale su cui ragionare».

Due «?» distinti: quello sul titolo del blocco risponde sul prezzo, quello accanto a «Studio di vendibilità» risponde sulla valutazione. L'annotazione dichiara la **fee**, perché un «decidi tu» che nasconde una penale non è un «decidi tu».

## Cosa diventa pubblico

Tre opzioni valutate. **Il generico da solo no**: «non tutte le informazioni verranno mostrate» dice che qualcosa sarà pubblico senza dire cosa, e aumenta l'ansia invece di ridurla. **Marcare i non pubblicati no**: il silenzio significherebbe «pubblico», che è il default sbagliato per chi vende casa, e sono comunque **il gruppo più grande** — su 174 campi, quelli che finiscono in un annuncio immobiliare sono una ventina.

**Si marcano i pubblici.** Silenzio uguale privato, che è il default sicuro. Concretamente:

- un banner in testa alla scheda — **«Quasi niente di quello che scrivi qui diventa pubblico»** — che nomina il perimetro e porta all'anteprima dell'annuncio
- l'**icona dell'occhio** sui campi pubblici (25 posati) e una nuova voce di legenda
- il resto resta senza marcatore

**Manca il dato definitivo.** Nel foglio 2.0 le due legende in testa — «informazioni presenti nell'annuncio» e «informazioni oscurate nella Brochure» — **non sono applicate a nessun campo**: le uniche celle colorate sono le intestazioni di sezione e le fasce di prezzo. La lista deve arrivare da lì.

## Scheda tecnica: allineamento alla 2.0

**Da 121 a 174 campi.** Aggiunto:

- **Superficie commerciale** come dato dichiarato dal venditore, con il gruppo «Quanto è grande»
- **Pertinenze accatastate separatamente** — blocco condizionale attivato da una spunta, fino a 4, con foglio/particella/subalterno chiesti e il resto letto dalla visura
- **Terreno agricolo** — blocco condizionale attivato da «L'immobile include un terreno agricolo»
- **Titoli edilizi esistenti** nella sezione Regolarità
- **Detrazioni fiscali residue** — la terza domanda dello step fiscale, che mancava
- **Stato manutentivo del box**, **armadi zona notte e zona giorno come numero**, **acque pluviali**, **posti auto** separati tra coperti, scoperti di proprietà e condominiali, **valore particolare del terrazzo**

Corretto: **reddito dominicale e agrario** stavano tra i campi derivati dell'abitazione, appartengono al terreno.

Contatori aggiornati ovunque: 36/36 · 0/25 · 0/8 · 7/15 · 42/74 · 0/11 · 0/3 · 0/2. Totale **85 di 174 campi**, **9 obbligatori mancanti in 3 step**.

**Resta da decidere** (vedi il delta): le condizioni della compravendita — provvigioni, costi di registrazione, cinque condizioni sospensive — oggi in «cosa non chiediamo adesso», in 2.0 dentro la scheda.

## Documento d'identità e verifica

**Il controllo Yousign è in tempo reale**: caricamento e stato della verifica non convivono più, sono due stati della stessa sezione — *Da caricare* (default), *Verifica superata*, *Esito negativo*. Caduti il tracker a tre passi e il badge «in corso · 2-3 giorni».

**Eliminato** lo stato alternativo «Più intestatari o titolare di un diritto reale di godimento»: si procede con il documento di un solo proprietario. Resta aperta la domanda gemella su S4 — se l'incarico lo firma solo l'utente loggato o tutti gli intestatari.

Confermato: caricamento in pagina, solo jpg e png, dati nel Profilo utente, campi anagrafici non compilabili, identità già confermata al momento della firma.

## Dati personali del venditore

Si raccolgono **prima della scheda immobile**, subito dopo i dati di contatto: come ti contattiamo → dove risiedi → dove si trova l'immobile. Solo **l'indirizzo di residenza**, e di quello un campo solo: comune e provincia via geocoding. Il resto vive nel **Profilo utente**. La sezione «I tuoi dati» è stata eliminata dalla scheda tecnica.

## Help contestuale: un «?» per blocco

Nelle schermate **autenticate e dense di form** l'help diventa **«?» più annotazione nativa**; nelle **schermate pubbliche o di conversione** resta visibile in pagina, perché lì è copy di fiducia. **13 «?» posati**, uno per blocco, nessuno replicato tra frame — nel frame ingombri resta solo quello sullo Studio di vendibilità.

Restano in pagina **9 blocchi P7 da valutare**: *E se poi non vendo?* (S4), *Devo esserci per forza io?* (S5), *Chi ha fatto questa valutazione?* (S6 ×2), *Dove trovo i dati catastali?*, *Perché mi servono tutti questi documenti?* (A2), *Che differenza c'è tra RRE e relazione tecnica?* e *Devo pagare Cleclà per questo?* (Trova tecnico), *Chi controlla i documenti?* e *Devo pagare per visitare?* (Annuncio — questi due li terrei visibili).

## Ridondanza: cosa è stato tagliato e cosa regge

| Gruppo | Sovrapposizione | Verdetto |
|---|---|---|
| Scheda tecnica · stato di default vs S2 | 7 stringhe uniche su 99 | **Eliminato** |
| Trova tecnico con/senza contesto | **77%** | **Assorbito** come due stati alternativi |
| Archivio A1–A5 | 27–54% | **Reggono** — la sovrapposizione è chrome, ognuno ha 25–73 stringhe proprie |
| Listing tecnici / Listing immobili / Annuncio | 19–33% | **Reggono** |

## Menu azioni immobile (i tre puntini)

Rinomina riferimento · Duplica scheda tecnica **(da validare)** · Sospendi temporaneamente e Ritira l'annuncio (disabilitate finché non è online) · Archivia immobile (distruttiva). Due punti aperti: *Rinomina* sovrascriverebbe il titolo composto — meglio un'etichetta aggiuntiva; *Duplica* riporta le risposte da cui si genera la lista documenti, con il rischio di una lista sbagliata non riletta.

## Progresso e salvataggio della scheda

Un blocco solo in coda alla scheda, che porta la CTA **«Salva e riprendi quando vuoi»** — azione più promessa, e vera visto che l'autosave gira a ogni cambio step. Il bottone non è più disabilitato: salvare un parziale è sempre possibile.

## Altre decisioni applicate

- **Blocco incarico**: un blocco, una CTA; a firma avvenuta diventa «Scarica l'incarico firmato». Da chiarire chi firma.
- **Studio di vendibilità**: lo fa Cleclà, incluso, non si commissiona.
- **Relazione tecnica**: non serve a pubblicare, serve a vendere.
- **Salvataggio, non invio**: la scheda si salva sul profilo immobile.
- **Fee dopo un anno**: importo a placeholder.
- **Stato di pausa**: due origini da distinguere anche in priority guide.
- **Annuncio venduto**: non esiste, l'immobile viene archiviato.
- **Archivio**: progresso nella sidebar, documenti dentro le cartelle. Ancora da applicare su A2.
- **Fuori perimetro**: tre modali con il nastro che spiega il motivo.

## Da fare

1. Le tre varianti del banner dello studio di vendibilità, ora che i binari sono paralleli
2. L'handoff nella modale di salvataggio: «Ho finito per ora» è un vicolo cieco, va sostituito con il passaggio al requisito successivo — e vanno separati il salvataggio parziale (toast) dal completamento (modale)
3. Restructure di A2
4. Condizioni della compravendita: in scheda o in trattativa
5. Legenda dei campi pubblici dal foglio 2.0

## Punti aperti

Rinomina riferimento · Duplica scheda tecnica · chi firma l'incarico · APE e conformità dell'annuncio · importo della fee · pausa per preliminare in PG · immobile archiviato · provvigione (tre numeri diversi) · le 8 cartelle dell'archivio · accesso dei tecnici · costo per l'acquirente nell'annuncio · delega della visita · i 9 blocchi P7 rimasti in pagina · nome della sezione «Profilo immobile — 8 step».
