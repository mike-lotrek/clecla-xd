# Fase Rogito · modifiche dopo le risposte del cliente del 07/10

File «Cleclà | UI», pagina «🚧 UI Layouts – WIP» di Sprint 5 (44:986) e PG3 v2 della Trattativa. Backup prima delle modifiche: pagina «💿 UI Layouts – Backup 07.10» (5273:6367), che contiene anche la sezione PG3 v2.

Scelte di Giovane: firma del recesso prima dei pagamenti; notaio scelto dall'acquirente (art. 4); si disegna solo la ripartizione della fattura, il resto va in nota; backup e modifica in place.

## Recesso (Venditore · 3 · Uscita dal contratto)

- U2 `4918:15292` diventa «Chi recede, e perché»: Marco bloccato come recedente, Elena Ferrero spuntabile, link di firma via email. Nota `5275:7404` sui punti aperti.
- U4 e U5 scambiati. U4 `4918:16659` è la firma FEA del documento, U5 `4918:16038` la registrazione. Stato nuovo in U4 «Recede anche Elena Ferrero» `5275:7376`. In U5 sparisce «Ritira la richiesta», compare «Documento di recesso firmato» fra i documenti.
- U3: «Fino alla firma del documento di recesso puoi ancora fermarti» (chiude D19).
- Percorsi riordinati (Firma prima di Registrazione) e FEQ → FEA in U6, U7, U8 e nel K7 dopo la registrazione.
- FEQ resta sull'accordo di risoluzione dell'inadempimento (U13, U15): il cliente non ne parla.

## Condizioni sospensive

- E6 ed E6V (autocertificazione con firma FEA) tolte, al loro posto le note `5275:7430` e `5275:7433`. Il ramo «Non si avvererà» porta direttamente a E7/E7V, rinominate «Contratto sciolto».
- E5 `4907:21794`: campo «La comunicazione della banca» con il documento, anteprima, CTA Destructive-fill «Dichiara che il mutuo non si avvera». E5V: stessa CTA. K7 ed E7/E7V citano il documento caricato invece dell'autocertificazione.
- Proroga: in E8/E8V il motivo è obbligatorio ed entra nel documento di proroga. In E9/E9A, dopo «Accetta» si prepara il documento e lo firmano tutti con FEA. Stato nuovo «Hai accettato: documento di proroga da firmare» `5275:7436`; lo stato «Prorogata» arriva solo a firme complete.
- Promemoria ogni 15 giorni in K3.0 e K3.
- Nota da disegnare sulla proroga della data del rogito `5275:7457`.

## Provvigione (Verso il rogito)

- C1 e C2: card «Fattura e pagamento» con tre opzioni (fattura intestata a te, intestata al cointestatario, una a testa) e solo bonifico. CTA «Paga [X] € + IVA con bonifico». Carta tolta anche da C1b e C2b; «Con carta» → «Con bonifico» in C3, C4, C6; stato «Pagamento con carta non riuscito» tolto.
- Nota `5275:7506` sui punti aperti della ripartizione.
- Aggiornamento del 07/10 sera: la generazione della fattura non è nell'MVP, Cleclà la emette a mano. La piattaforma comunica solo gli intestatari. Da sistemare quando si sa come Cleclà consegna la fattura (caricata in piattaforma o solo email): le frasi «La fattura arriva quando riceviamo la quietanza», «Ti mandiamo la fattura», «Scarica la fattura» e la voce «Fattura di provvigione» del gruppo D.

## Notaio

- C1–C6: «Il notaio lo scegli tu, come prevede il contratto…» per l'acquirente; per il venditore «Il notaio lo sceglie Giulia Rossi…» e «Cerca notai» nascosto.
- Nota da disegnare `5275:7509`: notaio indicato, cartella «Notaio» (oggi assente nell'Archivio), invio, controllo finale, D31, K2 e K5.

## Proposta del 08/10 · stepper a tre tappe e «Notaio e documenti»

Sezione `5344:6103` su Sprint 5 (x 33000). Lo stepper della pagina contratto traccia il percorso e non è cliccabile (la pagina è sempre la stessa). Tiene solo le tappe che si sbloccano a vicenda: condizioni sospensive, provvigione, firma dal notaio.

- Copia di K3.0 `5344:6104` con la sezione «Notaio e documenti» dopo le condizioni sospensive; «Cosa succede adesso» non promette più la lista dopo la provvigione.
- Copia di C1 `5344:6305`: la sezione sostituisce le card «I documenti che il notaio vi chiederà» e «Il notaio»; dopo il pagamento si sblocca solo il contatto diretto.
- Stati della sezione: da iniziare, notaio indicato, documenti quasi pronti, pronti da mandare, vista del venditore.
- Da disegnare: modale «Indica il notaio» e cartella Notaio. Da chiarire: invio dalla piattaforma o download, controllo finale di Cleclà.

## Altro

- PG3 v2 Trattativa, F2c: il testo della card «Firma» spiega le due sezioni di firma (accettazione del preliminare e approvazione specifica delle clausole vessatorie).
- Sprint 2, «Incarico di mediazione»: nota da disegnare sul recesso dall'incarico `5275:26601`.
- Panoramica aggiornata: E6/E6V spente, E7/E7V, U4/U5, E5 rinominate.

## Da segnalare sul glossario

«Multa penitenziale», «clausole vessatorie» e «documento di proroga» non sono nel glossario. Nel caso di Fase Rogito entrano due cointestatari, Elena Ferrero (venditori) e Sara Motta (acquirenti), presi dal caso della PG3 v2.
