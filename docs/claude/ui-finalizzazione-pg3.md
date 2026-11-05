# UI · Finalizzazione PG3 Uscita dal contratto: recesso e inadempimento, desktop 1440

Versione 0.1 · 02/10/2026 · file **Cleclà | UI** (`0k5JkkrVwDydzvUoRHv8ye`), pagina `🫟 UI Layouts` di Sprint 5 - Finalizzazione (`44:986`), sezione `PG3 · Uscita dal contratto · desktop 1440 🚧` (`4918:15192`), sotto la sezione della PG2.

Fonti: wireframe PG3 (`claude/wireframe-finalizzazione.md`, frame `4851:13400`–`4851:14826`), PG `clecla_pg_finalizzazione_v2.md` sezione PG 3, UI PG1 e PG2 (`claude/ui-finalizzazione-pg1.md`, `claude/ui-finalizzazione-pg2.md`), Pagamento registrazione v2 (R1, R2), glossario v1.1.

Stato: desktop completa, in review. Mobile non disegnato.

## Tavole

Codici U1–U15 (Uscita), per non confondersi con R0–R4 della PG4 v2 (D21). Etichette a 108 px come in PG1 e PG2. Stati alternativi sotto la tavola, riquadri tratteggiati senza fondo; le note fuori UI usano lo stesso riquadro con etichetta «Nota».

| Tavola | Node | Vista | Wireframe | Stati alternativi |
|---|---|---|---|---|
| U1 · Recesso, cosa stai per fare (modale) | `4918:15193` | Venditore | R0a, passaggio 1 | Popover recesso contro inadempimento |
| U2 · Recesso, perché (modale) | `4918:15292` | Venditore | R0a, passaggio 2 | «Altro» con testo · «Altro» senza testo |
| U3 · Recesso, quanto costa e conferma (modale) | `4918:15829` | Venditore | R0b | Da K2 o K5 senza 3% · popover multa · contratto sospeso (nota) |
| U4 · Registrazione del recesso da pagare | `4918:16038` | Venditore | R1–R2 | R1 appena inviata · bonifico · vista di Giulia · nota su cosa manca rispetto a K3 |
| U5 · Documento di recesso da firmare | `4918:16659` | Venditore | R3 | Firma in corso · firma non completata · dopo la firma |
| U6 · IBAN per ricevere la multa | `4918:17310` | Acquirente | R4 | IBAN non valido · conto non intestato · vista di Marco |
| U7 · Multa penitenziale da pagare | `4918:17894` | Venditore | R5 | Dopo il bonifico · Giulia in attesa (modifica IBAN) · Giulia conferma · bonifico non arrivato |
| U8 · Registrazione del recesso in corso | `4918:18502` | Venditore | R6 e chiusura | K7 vista di Marco · proposta D23 · oltre lo SLA · nota K7 di Giulia (PG1) |
| U9 · Inadempimento, cosa stai per fare (modale) | `4918:19119` | Venditore | I0, passaggio 1 | Nota da dove si arriva |
| U10 · Cosa non è stato rispettato (modale) | `4918:19206` | Venditore | I0, passaggio 2 | «Altro» · finestra ancora aperta |
| U11 · Cosa comporta e invio (modale) | `4918:19411` | Venditore | I0, passaggio 3 | Documento non generato |
| U12 · Mediazione da accettare | `4918:19526` | Venditore | I1–I2 | Hai accettato, l’altra no · vista di Giulia · I2b · popover · nota I3 = K6 |
| U13 · Accordo da firmare | `4918:20118` | Venditore | I3–I4 | Dopo le due firme · I4b Giulia · I4b Marco · nota I3 |
| U14 · Sede giudiziaria | `4918:20718` | Venditore | I5–I7 | I6 Giulia · I6 Marco · I7 Giulia · I7 Marco |
| U15 · Chiusura, registrazione della risoluzione | `4918:21278` | Acquirente | Chiusura comune | Firma dell’accordo di risoluzione · nota sulle due formule · K7 Marco · K7 con penale aperta (D24) · nota K7 Giulia (PG1) |

## Dati del caso

Catena UI di PG1 e PG2, non quella del wireframe. Mutuo entro il 26/12/2026 (Giulia), regolarità entro il 26/03/2027 (Marco), prezzo 270.000 €.

Recesso di Marco: richiesta 10/12/2026, attivazione 11/12, registrazione pagata 14/12, firma 15/12, IBAN di Giulia 17/12, ricevuta del bonifico 19/12, conferma di Giulia 22/12, registrazione e K7 il 29/12/2026 (date allineate a K7 recesso in PG1). Multa 13.500 €, corrispettivo a Cleclà 8.100 €, registrazione 621,00 € (200 + 16 + 405), totale 22.221 €; senza condizioni pendenti 14.121 €.

Inadempimento: mutuo scaduto il 26/12/2026, segnalazione di Marco il 12/01/2027, mediazione accettata da entrambi il 14/01 (K6 in PG1), accordo caricato il 22/01, nuova scadenza del mutuo 26/02/2027. Ramo giudiziario: verbale di mancato accordo 05/02/2027, sentenza 05/05/2027, IBAN di Marco 08/05, penale pagata 14/05 e confermata 15/05, registrazione della risoluzione pagata 18/05, accordo firmato 22/05, K7 il 30/05/2027 (allineato a K7 inadempimento in PG1).

## Shell e regole

Pagine: clone di K6 (Venditore) e K4 (Acquirente) della PG1, con Navbar, Sidebar, spalla Contratto a cinque passi e card «Hai dubbi?». Modali: guscio di E9 (fondo K3 Venditore) della PG2.

- Ordine dei blocchi nelle pagine del percorso: titolo e badge · riga dei fatti · card di contesto · card con l’azione (stroke warning a sinistra) · eventuale «Come paghi» e CTA · «Il percorso» · «I documenti di questo contratto».
- «Il percorso del recesso», «Il percorso dell’inadempimento», «La chiusura»: una riga per passaggio con l’icona di stato a sinistra (spunta fatto, orologio dove tocca a qualcuno, cerchio da fare), chi lo fa e la data nella riga secondaria, badge solo sul passaggio corrente.
- Pagamenti: «Cosa paghi» con importo, «senza IVA» e scomposizione; «Come paghi» clonata dalla PG4 v2; CTA che nomina la cifra.
- Firme: documento in box bianco con le voci, conseguenza in box bianco «Questa azione è definitiva», firma del recesso Destructive-fill; accordi di mediazione e risoluzione Primary, con lo stato di firma per persona.
- Un solo bottone pieno per pagina e per modale. Alert solo negli stati alternativi: Danger per errori, Info per attese e SLA, Warning per la penale ancora aperta, Success come conferma.
- Niente box con le due parti (decisione del 01/10).

Gate di libreria superato: nessun fill o stroke senza variabile e nessun testo senza stile fuori dalle istanze, salvo le etichette delle tavole, come in PG1 e PG2. Annotazioni Dev Mode: 16, sulle decisioni e discrepanze; quelle ereditate dai cloni sono state tolte.

## Scostamenti dal wireframe

- Richiesta di recesso in tre passaggi invece di quattro: la conferma sta nella modale dei costi.
- Box delle due parti tolto da tutte le pagine.
- Date riallineate alla catena UI (il wireframe usava mutuo al 15/12/2026 e segnalazione al 20/12/2026).
- Nella card di contesto del recesso e dell’IBAN niente riga documento duplicata: il documento sta nell’elenco dei documenti. L’accordo di mediazione entra nell’elenco solo quando è firmato.
- Corrispettivo a Cleclà fuori dalla pagina di pagamento (resta nel documento di recesso e in U3), con D17 in annotazione al posto della riga «DA DECIDERE».
- Riga «Imposta sulla multa/clausola penale, 3% di 13.500 €» nella scomposizione della registrazione: rende leggibile la formula del punto 27.

## Discrepanze da segnalare

- **«Corrispettivo a Cleclà».** Termine nuovo per il 3% sul recesso; il glossario (§4.1) registra cinque nomi per il compenso di Cleclà e nessuno per questa voce. Da confermare che sia una voce distinta dalla provvigione.
- **«Documento di recesso» e «Segnalazione di inadempimento».** Il glossario [PK] chiama i due atti «moduli di recesso dal preliminare e di comunicazione e riconoscimento di inadempimento». In UI la forma della PG.
- **Multa, penale, clausola penale.** Il glossario (§15.1) registra solo «costi aggiuntivi» nei frame approvati. In UI il lessico della guida al contratto, come in PG1.
- **Mediazione di Cleclà (D22).** Contro §15.7, che non presenta mai Cleclà come parte che media.
- **Badge.** «Recesso in corso» (D20) e «Sospeso» durante la chiusura dell’inadempimento non sono fra i sei della PG1.
- **Punto di non ritorno (D19).** «Fino al pagamento della registrazione puoi ancora fermarti», ma il contratto si annulla con la firma.
- **Spalla.** Durante recesso e inadempimento il quinto passo resta «Condizioni sospensive · Sei qui», come K6 UI; il wireframe diceva «Fermo».
- Ereditate e non risolte: D17, D18 (termine per recedere 30 giorni prima del rogito), D23, D24, punti 27, 34, 36, 41, 42.
- Nessuno scostamento sui termini bloccati: «condizioni sospensive», «inadempimento», Youtrust.

## DA VALIDARE

Aliquote e importi di multa, corrispettivo e penale · base della registrazione (punto 27) · chi paga la registrazione (36, anche in mediazione) · SLA del team e scadenze dei pagamenti, [SLA] e [GG/MM] in segnaposto · conto di terzi per la multa · cosa succede se la multa non viene pagata · se le scadenze corrono durante il recesso · sospensione all’invio della segnalazione · quando la mancata risposta sulla mediazione vale come no · voci della lista di inadempimento oltre al mutuo · le due formule della registrazione dell’inadempimento · ragione sociale e IBAN di Cleclà per il bonifico.

## Nota operativa

Helper di sessione su `globalThis.P3` (non persistono): `page`, `modal`, `card`, `percorso`, `step`, `cosaPaghi`, `comePaghi`, `docs`, `docRow`, `docBox`, `box`, `field`, `radios`, `upload`, `fileRow`, `firme`, `medBlock`, `alert`, `alt`, `note`, `stack`. Usano come sorgenti nodi di PG1, PG2 e PG4 v2 (id in `figma.root` plugin data `pg3ui`, insieme agli id delle tavole). `clone()` dei nodi sorgente mette il clone alla radice della pagina: in caso di errore va cercato e rimosso lì. I frame pagina non sono in Auto Layout: dopo un cambio di altezza del Main content va ridimensionato il frame.
