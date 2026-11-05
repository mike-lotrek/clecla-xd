# Rework PG3 dopo il feedback del 30/09

09/10/2026 · file «Cleclà | UI», Sprint 4 «🚧 UI Layouts – WIP» (44:983), sezioni `PG3 · Preparazione alla firma v2` desktop (4435:172035) e mobile (4456:181570). Backup nella pagina «💿 UI Layouts – Backup 08.10» (5424:8011): 5479:8136 desktop, 5479:15716 mobile.

## Risposte di Giovane

- #279: un «?» anche sul titolo della parte acquirenti, come per i venditori. Il concetto si spiega anche nella guida: scelta la prima proposta (bottone (?) sul passo 5 della slide 01, fatto il 09/10, vedi `claude/rework-pg1-feedback-30-09.md`).
- #280: i dati di tutti li inserisce sempre la persona registrata (il venditore o l’acquirente che gestisce la sua parte). I cointestatari si accordano e si scambiano le informazioni fuori dalla piattaforma.

## Modifiche

- #278, #279 · Bottone (?) su tutti i titoli di parte («Venditori · …», «Acquirenti · …») in F1, F1b e F1 acquirente, desktop e mobile. Due popover nella tavola «PG3 v2 · Contenuti dei bottoni info»: comunione legale dei venditori (vale per ogni proprietario; in separazione dei beni non serve) e degli acquirenti (vale anche se uno dei due compra al 100%). Testi in terza persona, perché ogni popover si vede da entrambe le parti.
- #280 · Pannello «Carica il documento di Elena» (desktop) e foglio mobile: scelta «Carta d’identità / Passaporto»; gruppo «Dati che il documento non contiene» con recapito, domicilio, attività lavorativa (select), domanda PEP con (?) e Sì/No; nota «Questi dati li inserisci tu per Elena: se non li conosci, chiediglieli prima di caricare il documento.» Popover PEP con la definizione del cliente. Stato con passaporto: desktop `Pannello v2 · … · passaporto` (5479:17613, a destra della sezione), mobile `Foglio v2 · … – M · passaporto (contenuto intero)` (5482:9509): una sola zona di caricamento, residenza in quattro campi, codice fiscale, PEP «Sì» con «Carica ricoperta». Mobile: anche lo stato di scorrimento del foglio con carta d’identità. (Superato il 03/11, vedi sotto.)
- #281 · Nota di firma in F2a–F2d, desktop e mobile: «Il contratto preliminare, l’informativa privacy e l’identificazione ai fini dell’antiriciclaggio si firmano tutti con firma elettronica qualificata (FEQ).»
- #282 · Modale e foglio «Richiedi una modifica»: «Scrivi cosa non torna nel contratto preliminare.»
- #283 · Storico delle richieste di modifica (F2b, F2c, F2d, desktop e mobile): terza richiesta con una risposta scritta di Cleclà senza nuova versione: «Aggiungere una caparra di 10.000 € alla firma» → «Risposta: non la aggiungiamo. Il contratto preliminare prevede la clausola penale al posto della caparra: vi tutela allo stesso modo, senza versare denaro alla firma. Il contratto resta alla versione 2.»

## Da segnalare

- «Persona politicamente esposta (PEP)», «attività lavorativa» e «carica ricoperta» non sono nel glossario.
- Le otto opzioni dell’attività lavorativa (dalla risposta del cliente) vanno nel select: nel mockup c’è solo il campo chiuso. Le opzioni: lavoratore dipendente; libero professionista / lavoratore autonomo; imprenditore / titolare d’impresa; pensionato; studente; casalinga/o; disoccupato; altro.
- Il pannello non diceva come si scopre che il documento è un passaporto: abbiamo messo la scelta esplicita in testa al pannello. Da confermare.

## Semplificazione di F1 (03/11)

Decisione di Giovane del 03/11. Tolti i sotto-step dei dati letti dal documento e della segnalazione di un errore: niente più «Vedi i dati letti» né «Segnala un errore». Il venditore non aggiunge proprietari, perché Cleclà li verifica in pubblicazione; l’aggiunta resta solo all’acquirente, per i futuri cointestatari.

- Desktop venditore (F1, F1b): fatto da Giovane.
- Mobile venditore F1 (4501:190002) e F1b (4501:190227): tolti «Vedi i dati letti», il blocco «Aggiungi una persona dalla tua parte» con il divider sopra e «Rimuovi» sotto Elena, come nel desktop.
- Acquirente F1 desktop (4501:189722) e mobile (4501:190114): tolto «Vedi i dati letti». «Aggiungi una persona dalla tua parte» e «Rimuovi» restano.
- Le tavole dei sotto-step tolti sono fuori dalla sezione, a sinistra della pagina: pannello desktop 4435:175577 e modale 4675:165432 (spostati da Giovane), fogli mobile 4456:184008 e 4675:165558 accanto.
- Copy del desktop venditore allineato al mobile: sottotitolo della sezione in F1 e F1b, titoli di parte «Venditori · la tua parte» / «Acquirenti · l’altra parte», «coniuge in comunione legale» in F1b.

## Maschera «Carica il documento» semplificata (03/11)

Decisione di Giovane del 03/11, applicata a modale carta d’identità (4435:175543), modale passaporto (5479:17613) e ai tre fogli mobile (4456:183973, 5479:200541, 5482:9509).

- La scelta carta d’identità / passaporto resta e cambia solo le zone di caricamento (fronte e retro, oppure la pagina con la foto).
- Stessi dati in tutti e due i casi, con lo schema della Verifica dell’identità in Pubblicazione (4908:38365): indirizzo di residenza (indirizzo e numero civico, comune, provincia, paese), indirizzo di domicilio con la casella «Il domicilio è uguale all’indirizzo di residenza», codice fiscale e contatti (codice fiscale, telefono, email), attività lavorativa, PEP con «Carica ricoperta» se Sì.
- Precompilati codice fiscale ed email, che il venditore ha già inserito per il secondo proprietario in Pubblicazione (D-PI-4, accordion «Proprietari», 4860:86016). Riga: «Codice fiscale ed email di Elena li hai già inseriti nella scheda dell’immobile, in «Proprietari»: li trovi compilati e puoi modificarli qui.»
- Tolti «Dati che il documento non contiene», «Domicilio, se diverso dalla residenza» come campo unico e la nota del passaporto su residenza e codice fiscale. La nota «Questi dati li inserisci tu per Elena…» apre il blocco dei dati.
- Occhiello unico «VERIFICA DELL’IDENTITÀ» anche nella variante passaporto.
- Mobile: telefono ed email uno sotto l’altro. Lo stato di scorrimento mostra la parte da codice fiscale in giù.
- La variante passaporto mostra PEP «Sì» con «Carica ricoperta», la carta d’identità PEP «No».

Da verificare:
- In Pubblicazione l’email del secondo proprietario è obbligatoria, il codice fiscale no: se manca, il campo qui arriva vuoto.
- Residenza e telefono di Elena non si chiedono in Pubblicazione: vanno inseriti qui.
- Le immagini di sfondo delle modali mostrano ancora la pagina con «Aggiungi una persona» e «Vedi i dati letti»: da rigenerare.
