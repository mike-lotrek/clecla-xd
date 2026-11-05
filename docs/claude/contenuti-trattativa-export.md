Export contenuti Trattativa verso il foglio Contenuti (07/09/2026)

Destinazione: foglio Google "20260127_Cleclà_Contenuti", tab "Priority guides".
Schema colonne: Pagina | Block | Type | Elemento | Target | Contenuto | Sprint | Note.

## Cosa è stato prodotto

215 righe estratte verbatim dai 31 frame della sezione "Trattativa" (Sprint 3) del file Figma "Cleclà | UI", pagina Wireframe. Consegnate come .xlsx da incollare a mano: il connettore Drive legge il foglio ma non scrive celle.

Ripartizione per pagina:
- Guida alla trattativa (venditore) — 44 righe, Target "Venditori"
- Guida alla trattativa (acquirente) — 9 righe, Target "Acquirenti" (solo i delta di ruolo: la variante è un clone)
- Pagina trattativa (n) — 74 righe, Target "Both - logged"
- Preparazione alla firma — 46 righe, Target "Both - logged"
- Registrazione del contratto preliminare — 42 righe, Target "Both - logged"

Granularità e vocabolario ripresi da "Trova tecnico" e "Listing tecnici" (righe 248-298), il modello più recente nel foglio: una riga per elemento, stati alternativi e stati vuoti come righe proprie, decisioni di progetto in Note. Type usati: CONTENT, INPUT, ACTION, STATUS, FEEDBACK, CARD, MODAL, LINK, LIST.

## Stili del foglio originale, per ricostruirli

Rilevati scaricando il file come .xlsx e leggendolo con openpyxl.

- Font: Geist 8 pt, colore FF000000. Intestazione: Geist 8 bold, colore FF999999.
- Allineamento: verticale in alto, testo a capo attivo, orizzontale generale.
- Bordi: sottili FFD9D9D9 sui quattro lati; colonna A bordo sinistro spesso FFCCCCCC; colonna H bordo destro sottile FF9A9A9A. Nella riga di intestazione i bordi cadono, restano solo A sinistra spesso FFCCCCCC, C sinistra sottile FFCCCCCC, H destra spesso FFCCCCCC.
- Banding: riempimento alternato per gruppo pagina, FFFFFFFF e FFF3F3F3. Non alterna per riga.
- Celle unite verticalmente: Pagina (A), Target (E) e Sprint (G) per gruppo pagina; Block (B) per gruppo blocco. Solo la cella in alto tiene il valore.
- Larghezze colonna: A 18,88 · B 12,88 · C default · D 35,38 · E 16 · F 37,25 · G 16 · H 38,63.
- Riquadri bloccati: E3. Filtro automatico: A1:H394.

## Struttura reale del tab "Priority guides"

959 righe, non 394. L'export in markdown del connettore Drive tronca intorno alla riga 311: va usato il download .xlsx per vedere tutto.

Due zone:
1. Righe 1-394, dentro il filtro automatico. Inventario pagina per pagina, con righe scarne (una per elemento previsto, colonna Contenuto vuota). Dentro questa zona, Trova tecnico (248-266) e Listing tecnici (267-298) sono stati riscritti in versione dettagliata, in place, al posto delle rispettive righe di inventario. Portano le decisioni del 18/08.
2. Righe 395-959, fuori dal filtro. Contenuto dettagliato di Profilo immobile (n) 395-767, Archivio documentazione immobile 768-853, Trova tecnico 854-876, Listing tecnici 877-908, Listing immobili 909-937, Annuncio immobile 938-959. Le versioni di Trova tecnico e Listing tecnici qui sono precedenti alle decisioni del 18/08: nominano ancora il banner di contesto e l'indicatore di passo, che quelle decisioni hanno eliminato.

Da decidere dove vanno le righe di Trattativa: in place nella prima zona, al posto delle righe di inventario, come è stato fatto per Trova tecnico; oppure in coda alla seconda zona, come per Profilo immobile.

Righe di inventario esistenti sulle pagine di Trattativa: 226-227 (Trattative in corso, Guida venditore), 242-243 (Trattative in corso, Guida acquirente), 301-303 (Pagina trattativa), 311-313 (Preparazione alla firma), 314-318 (Contratto preliminare firmato, tre pagine).

## Incoerenze rilevate nel foglio, da sistemare

1. "Preparazione alla firma" è marcata Sprint 4 nel tab Pagine e nella riga di inventario 311. I wireframe sono di Sprint 3.
2. La fase di pagamento della registrazione è spezzata in tre pagine: "Contratto preliminare firmato (pagina di attesa) venditore" (314), "(pagina di attesa) acquirente" (315-316), "(conferma pagamento)" (317-318). I wireframe la trattano come una pagina sola a quattro stati (R1 da pagare, R2 pagata e deposito in lavorazione, R3 registrato, R4 vista del venditore) più un confine (R5, termine scaduto).
3. Trova tecnico e Listing tecnici compaiono due volte, in due versioni diverse: 248-298 aggiornata, 854-908 precedente. La versione vecchia andrebbe rimossa o marcata.
4. Riga 294, "Listing tecnici · Mobile · Lista e mappa come viste alternative": nell'export markdown il contenuto risulta sfasato di una colonna. Da verificare direttamente nel foglio.
