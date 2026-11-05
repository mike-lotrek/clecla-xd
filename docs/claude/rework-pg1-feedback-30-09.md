# Rework PG1 dopo il feedback del 30/09

08/10/2026 · file «Cleclà | UI», pagina Sprint 4 «🚧 UI Layouts – WIP» (44:983), sezione `PG1 · Guida alla trattativa v2 · feedback 20/09 e 30/09` (3707:110792). Backup prima delle modifiche: pagina «💿 UI Layouts – Backup 08.10» (5424:8011).

## Versione consolidata (09/10)

Giovane ha scelto un misto delle due varianti preparate per #288: slide 01, 03, 05 e 06 dalla variante A (card bianche con righe uniformi), 02 e 04 dalla variante B (righe con icona; tempi in cinque riquadri). La tavola unica è `Sezioni come slide · i sei stati` (5425:8049), di nuovo a x 1680; la sezione è tornata alla larghezza di prima. Le sei slide scartate (A 02, A 04, B 01, B 03, B 05, B 06) sono nel backup, frame `PG1 · slide non usate dopo la scelta del 09/10` (5480:8242). La slide 01 della pagina D-B è stata sostituita con la versione consolidata.

#279 · Slide 01, passo 5 «Indicate chi firma insieme a voi»: bottone (?) con popover «Chi firma insieme a voi»: «Firmano tutti i proprietari dell’immobile e tutti gli acquirenti. Se qualcuno di loro è sposato in comunione legale dei beni, firma anche il coniuge, pure se compra o vende al 100% da solo. In separazione dei beni il coniuge non firma. I documenti di tutti li carica chi gestisce la trattativa.» Anche nella slide 01 di D-B.

Mobile (09/10): le sei slide dei sei stati mobile e la slide 01 di M-B sono allineate alla versione consolidata, clonando i contenuti del desktop. Adattamenti: la card dei sei passi va su una colonna; le due card delle dichiarazioni una sotto l’altra; i cinque riquadri dei tempi su due colonne; i titoli con (?) che non stanno su una riga vanno a capo. Dalla slide 06 mobile è stata tolta la nota «La differenza è nel momento: la caparra si versa subito, la penale si paga solo se qualcuno non rispetta gli accordi.», che sul desktop non c’era.

## Le due varianti (#288), come erano state proposte

**Variante B · struttura libera.** Ogni slide tiene la sua forma: passi su due colonne, righe con icona, card affiancate, riquadri dei tempi, elenco numerato. Uniformati il blocco del titolo, le card bianche (raggio 12, padding 20/24, piena larghezza) e il testo dentro le card (Paragraph 16).

**Variante A · struttura uniforme.** Tutti i contenuti in card bianche con la stessa riga: segno a sinistra (numero o icona) quando la lista è una sequenza o un insieme di categorie, titolo Paragraph Medium 16, descrizione Paragraph small 14, bottone (?) accanto al titolo, valore a destra solo nei tempi. Sul fondo scuro restano titolo di sezione, testo introduttivo e note.

## Contenuti (versione consolidata, desktop e mobile)

- #263 · La nota sugli arredi esce dalla riga Prezzo. Il bottone (?) sta accanto a «Prezzo» e apre il popover già esistente.
- #264 · Le card «L’acquirente dichiara» e «Il venditore dichiara» coprono tutta la larghezza.
- #266 · Slide 04: frase «Tempi indicativi, contati dalla firma del contratto preliminare.» sopra i cinque riquadri dei tempi.
- #267 · Errore 3: tolta «Non esiste una valutazione certificata.»
- #268 · Bottone (?) sul terzo punto della clausola penale, con popover nuovo (testo nostro sull’esempio del cliente).
- #272 · Errore 2: «Prendere accordi a voce o fuori dalla piattaforma» con descrizione «Nel contratto preliminare entra solo quello che concordate nella pagina della trattativa.» «Documento di puntuazione» tolto anche dal testo della slide 03.
- #289 · Banner «Hai dubbi?» alleggerito su desktop e mobile: senza fondo pieno né illustrazione, bordo sottile, bottone Outline-dark «Apri la chat».

## Da confermare

- «Pagina della trattativa» non è nel glossario; «piattaforma» sì. L’errore 2 ora parla di piattaforma come l’errore 7 («Uscire dalla piattaforma e concludere fuori»): i due punti restano distinti, ma si somigliano.
- Formule nuove nei titoli di riga (slide da A): «Se c’è un terreno agricolo», «Se l’immobile è regolare» (03); «Nessun passaggio di denaro prima del rogito», «Il 5% lo paga chi non rispetta gli accordi», «Nessuna liquidità immediata» e la descrizione «Fra le parti non si versa niente, nemmeno alla firma del contratto preliminare.» (06).
- I popover della liquidità e di «Chi firma insieme a voi» sono testi nostri.
