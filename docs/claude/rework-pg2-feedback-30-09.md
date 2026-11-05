# Rework PG2 dopo il feedback del 30/09

08/10/2026 · file «Cleclà | UI», Sprint 4 «🚧 UI Layouts – WIP» (44:983), sezioni `PG2 · Pagina trattativa v2` desktop (4371:29245) e mobile (4435:165755). Backup prima delle modifiche nella pagina «💿 UI Layouts – Backup 08.10» (5424:8011): 5434:8600 desktop, 5434:14520 mobile.

## Risposte di Giovane

- #290: la pagina Trattative (elenco per immobile) esiste già, `Trattative dell’immobile – D · Listing (Venditore)` 5131:7921.
- #291: lo stepper di spalla resta com’è. Tutti i passi sono attivi, salvo quelli bloccati (per esempio la data del rogito): il clic su un passo attivo porta con lo scroll al punto della pagina che ne parla.
- #287: storico dal più recente; nessun limite al numero di proposte (lo storico è chiuso di default, si apre con «Vedi le proposte»); le note lunghe si troncano con «Leggi di più», che apre il messaggio intero sul posto.
- Riepilogo degli accordi (08/10): è una pagina figlia di Trattativa (n). Va aggiunto all’architettura.
- Modello della pagina (08/10): la trattativa è una pagina sola il cui contenuto cambia con lo stato, come la pagina contratto. T4 e T5 sono stati della pagina Trattativa, non il Riepilogo. In T4 le card si compattano nell’elenco «Argomenti concordati» con la CTA di conferma; l’elenco ripete il Riepilogo, ed è voluto: chi conferma rilegge senza cambiare pagina.

## Modifiche

- #269 · Nelle 51 card degli argomenti (desktop e mobile) il valore è su una riga sua in Heading 3 Semibold: «€ 270.000», «15/06/2027». Lo stato si sposta nella riga sotto, insieme all’autore: «Controproposta da Giulia Rossi, 2 giorni fa · terza proposta», «Concordata · proposta da Giulia Rossi, accettata da te il 14/09». Le card «Non ancora proposta» restano com’erano.
- #290 · Tolto il blocco «Trattative in parallelo» da tutte le pagine del venditore (13 tavole fra desktop e mobile). Resta il chip «1 di 3 su questo immobile», che apre l’elenco. Resta anche il blocco informativo dell’acquirente («Si possono avere più trattative aperte in parallelo?»), che non elenca altre trattative.
- #287 · Storico del prezzo dal più recente in T2, D-4 e M-1. In T2 e M-1 la nota della proposta da € 280.000 è lunga e troncata, con «Leggi di più». Stato aperto disegnato a destra della sezione: `Stato · Nota lunga aperta (dopo «Leggi di più»)` 5434:17741.
- #270 · Tolto il blocco «Non applicabili» da D-6, T4, M-6, M-7.
- #271, #273, #274, #275 · «contratto preliminare» per esteso nel testo delle condizioni sospensive (D-6, T4 e mobile) e nei passi 4, 5 e 6 di «Cosa succede dopo».
- #276 · In T4 (desktop e mobile), sotto la CTA «Conferma l’accordo»: «Quando confermate entrambi, le altre trattative su questo immobile si bloccano e chi le aveva aperte riceve un avviso.» In T5 il chip dice «Altre 2 trattative bloccate».
- #277 · Modale e foglio X1, conseguenza 2: «Le proposte e le dichiarazioni di questa trattativa decadono senza vincoli. Se Giulia Rossi ci ripensa, può aprire una nuova trattativa su questo immobile.»
- Riepilogo degli accordi · D-6: breadcrumb a quattro livelli «Trilocale in Via Roma 12, Cuneo / Trattative / Trattativa con Giulia Rossi / Riepilogo degli accordi» (istanza staccata, il componente ne mostra tre). Tolto il link «Torna alla trattativa», che era una copia di «Annulla la trattativa» con l’icona del cestino. M-6: il ritorno in testa diventa «‹ Trattativa con Giulia Rossi» (era «‹ I miei immobili»), tolto lo stesso link. Sotto D-6 e M-6 una nota chiede di aggiungere il nodo alla board Architettura.
- Nomi: D-6/M-6 «Riepilogo degli accordi … · pagina figlia della trattativa»; D-7/M-7 «T4 · Accordo da confermare»; D-8/M-8 «T5 · Trattativa chiusa». Etichette aggiornate. Banner di T4: «Rileggete gli accordi qui sotto e confermateli entrambi.»

## Da disegnare o decidere

- #276: lo stato «trattativa bloccata» per l’acquirente delle altre trattative, il testo dell’avviso, e cosa succede se l’accordo poi salta (le trattative bloccate si riaprono o no).
- #277: il percorso dell’acquirente che riapre una trattativa sullo stesso immobile dopo un annullamento non è nello user flow.
- Il troncamento delle note: il limite di caratteri va fissato con lo sviluppo (nel mockup la nota è tagliata a circa 130 caratteri).
- Board Architettura: aggiungere «Riepilogo degli accordi» come figlia di Trattativa (n), per entrambi i ruoli.
- Il componente Breadcrumb in libreria ha quattro voci ma l’istanza ne espone tre: va controllato in libreria, così D-6 può tornare un’istanza.
