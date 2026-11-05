# UI · Lettore del contratto preliminare e guida contestuale

Versione 1.0 · 24/09/2026 · file **Cleclà | UI** (`0k5JkkrVwDydzvUoRHv8ye`), pagina `🚧 UI Layouts – WIP`. Due sezioni: `Contratto preliminare · lettore e guida · desktop 🚧` (`4456:185475`) e `Contratto preliminare · lettore e guida · mobile 440 🚧` (`4456:187889`).

Fonti: Requirements «Cleclà | MVP Functional Requirements Definition», righe «Guida contestuale per le diverse sezioni del contratto» e «Lettura del contratto»; template del contratto preliminare fornito dal cliente (Google Doc `1hK0936sAQZ4Nddiu6gQV3gu3YZ9dlC3B`).

## Decisioni del 24/09

- **Un lettore con pannello guida**, non due pagine. «Leggi il contratto» apre il testo; «Guida al contratto preliminare» apre la stessa pagina con il pannello «Come si legge».
- **Domande sì, voce lettrice dopo.** La domanda su un articolo è disegnata; la voce è un ingombro dichiarato («Ascolta» nella barra del documento).
- **Testo reale** dal template del cliente, istanziato sul caso Marco Ferrero ed Elena Ferrero / Giulia Rossi e Sara Motta, con le opzioni che il caso attiva.
- Desktop e mobile nello stesso giro.

## Cosa chiedono i Requirements e dove sta

| Requisito | Dove |
|---|---|
| Tutorial su come leggere il contratto | L1 / M2 · Come si legge |
| Icona accanto a ogni sezione, spiegazione semplice | L2 / M3 · il (?) accanto al titolo di articolo apre «In breve» con un esempio sul caso |
| Glossario contestuale | L3 / M4 · parole sottolineate, popover |
| Domande su una sezione | L4 / M5 · domanda, risposta, passaggio al team legale |
| Testo base distinto dalle condizioni definite | Riquadri «Concordato in trattativa» su indaco 050 con stroke indaco 400 |
| Navigazione interna ai paragrafi | Indice in colonna sinistra (desktop), tendina e foglio (mobile, M8) |
| Evidenziazione modifiche recenti | L5 / M6 · riquadri «Modificato nella versione 2» con stroke warning, «modificato» nell'indice |
| View recap | L6 / M7 · Riepilogo |
| Richiesta di modifica su un paragrafo (riga della riapertura) | L7 · modale con il punto del contratto precompilato |
| Voce lettrice / notaio AI | «Ascolta», ingombro da progettare |

## Tavole

**Desktop 1440**, colonne: indice 256 · documento 656 · pannello guida 400.

| Tavola | Node |
|---|---|
| L1 · Come si legge (dalla guida) | `4456:186677` |
| L2 · Spiegazione di un articolo (art. 2) | `4456:186887` |
| L3 · Parola del glossario (art. 8, «multa penitenziale») | `4456:187077` |
| L4 · Domanda su un articolo (art. 4, consegna differita) | `4456:187278` |
| L5 · Cosa è cambiato nella versione 2 | `4456:187481` |
| L6 · Riepilogo | `4456:187677` |
| L7 · Richiedi una modifica su un articolo (fondo L2) | `4456:187838` |

**Mobile 440**: M1 Lettura `4456:187890` · M2 Come si legge `4456:187994` · M3 Spiegazione `4456:188148` · M4 Glossario `4456:188395` · M5 Domanda `4456:188500` · M6 Versione 2 `4456:188647` · M7 Riepilogo `4456:188786` · M8 Indice aperto `4456:188885`. Il pannello diventa un foglio dal basso, alto al massimo 760; l'indice una tendina che apre il foglio M8.

**Ingressi**: F2 desktop, «Leggi il contratto» nella card e «Guida al contratto preliminare» in spalla. F2a, F2b e F2c mobile: aggiunto il link «Guida al contratto preliminare» nella card del contratto, dove prima mancava.

## Regole

- Barra del documento: ritorno a Preparazione alla firma, titolo, versione, scelta della vista (Testo completo / Riepilogo, con i `Radio item` Boxed già usati per sì/no), «Ascolta», «Scarica il PDF».
- Nell'indice un pallino indaco segna gli articoli con condizioni vostre (2, 4, 7), con la legenda sotto.
- Il pannello ha sempre la stessa forma: occhiello con l'articolo, titolo, «In breve», un riquadro «Nella vostra compravendita» con i numeri del caso, le azioni «Fai una domanda» e «Richiedi una modifica su questo articolo», la nota che le spiegazioni non sostituiscono una consulenza legale.
- La risposta alla domanda è dichiarata come generata dall'assistente sul testo dell'articolo, con «Scrivi al team legale» sotto.
- Il riepilogo è dal punto di vista di chi legge: mostra solo la provvigione della sua parte.

## Contenuti

Tutte le spiegazioni, il glossario, le domande e le risposte sono **segnaposto scritti da noi** sul testo del contratto. Vanno validati dal team legale. Numeri del caso: prezzo € 270.000, rogito entro 15/06/2027, consegna 15/07/2027, penale e multa penitenziale 5% = € 13.500, 3% a Cleclà in pendenza delle condizioni = € 8.100, termine per recesso e comunicazioni sulle condizioni 16/05/2027 (30 giorni prima del rogito), provvigione venditore 1% = € 2.700 più IVA, penale per ritardata consegna € 75 al giorno.

Opzioni del template attivate dal caso: due comproprietari venditori (opzione 2 delle parti), consegna differita (art. 4 opzione 2), condizioni sospensive su mutuo (7 opz. 2.1) e regolarità (7 opz. 2.4), relazione tecnica presente con immobile non regolare (3.3.1 opz. 1.2).

## Discrepanze da segnalare

- **Scadenze delle condizioni sospensive.** In trattativa (PG2 v2, T4, sintesi di F2) sono «entro 3 mesi» e «entro 6 mesi dalla firma del preliminare». Il contratto (art. 7) le fissa tutte al trentesimo giorno prima del rogito. La sintesi di F2 e il riepilogo del lettore dicono due cose diverse: nel lettore ho seguito il contratto. Va deciso quale delle due regole vale.
- **Cleclà come «Agenzia Immobiliare» e «Mediatore Immobiliare»** (art. 6) contro il copy approvato «Non siamo il terzo attore della compravendita» (glossario §15.7). Già segnalato per «intervento mediatorio», qui è esplicito.
- **Costo del recesso.** Il contratto somma la multa penitenziale del 5% all'altra parte e il 3% (minimo € 6.000) a Cleclà, se il recesso avviene in pendenza delle condizioni. La guida alla trattativa parla solo del 5%.
- **Penale per ritardata consegna** (€ 75 al giorno, art. 4): non compare in nessuna schermata della trattativa, dove la data di consegna si concorda.
- **Provvigione di entrambe le parti nel testo** (art. 6.1), mentre il feedback su PG4 chiede che ciascuna parte veda solo la propria. Nel testo non si può nascondere; nel riepilogo sì.
- **Più acquirenti**: il template prevede un solo promissario acquirente, non ha la variante con più persone come per i venditori.
- **Refusi del template** da passare al cliente: «Promissario Venditore» in 5.2; «SUBBORDINATO»; l'opzione 2.4 dell'art. 7 ha il titolo della prelazione agraria ma parla di regolarità; 3.3.1 rimanda a un «punto b)» che non esiste; «Il Promittente» con maiuscola dopo virgola in 4.
- **L'esempio dei Requirements** («caparra confirmatoria») regge: l'art. 2.2 esclude espressamente la caparra, ed è quello che spiega L2.

## Punti aperti

- **Il cancello della dichiarazione.** Proposta: «Come si legge» e glossario consultabili anche prima della dichiarazione, testo chiuso fino all'accettazione. Non disegnato.
- **Chi risponde alle domande** e con che tempi: assistente automatico sul testo dell'articolo, team legale come secondo livello. Da confermare con il cliente, come per «Fatti aiutare a leggerlo».
- **Voce lettrice**: «Ascolta» è un segnaposto.
- **Etichette dell'indice** accorciate rispetto ai titoli del contratto (es. «Art. 8 · Penale e recesso»): da validare.
- **Modifica e benestare**: resta aperto se una richiesta partita dal lettore fa ripartire il benestare.

## Nota operativa

Le tavole sono generate da due funzioni nel plugin data di `figma.root`: `readerLib` (desktop, `reader(cfg)`) e `readerLibM` (mobile, `mreader(cfg)`, usa anche `readerLib`). Le configurazioni di ogni tavola sono in `readerCfg_L1…L6` e `readerCfg_M1…M8`: per cambiare un testo si modifica la configurazione e si rigenera la tavola. Si richiamano con `new AsyncFunction('figma','cfg', lib + 'return await reader(cfg);')`.

Trappole: il `Nav tabs` sorgente della chiusura ha opacità 0,3 e il clone la eredita; le proprietà aggiunte a un nodo Figma (`node.__x`) non persistono, serve una variabile esterna; un frame verticale creato con `resize()` resta ad altezza fissa finché non si rimette `primaryAxisSizingMode = 'AUTO'`.
