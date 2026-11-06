# Verifica · flussi di recesso e inadempimento del cliente contro la UI attuale

05/11/2026. Verifica di sola lettura: nessuna modifica a Figma, a FigJam o ai fogli.

## Esito

I due documenti del cliente non sono compatibili con la struttura attuale di «Venditore · 3 · Uscita dal contratto» (`5107:5678`). Quattro differenze sono strutturali e vanno decise prima di rilavorare le tavole.

## Fonti

- «Procedura generale Inadempimento»: `1p8qh3bljfnHnUYnuhIpa_X9ZWgoEOnZPJwQEiet18Bk`, dal commento `1961243966` (11/10).
- «Recesso»: `1bETP2HzW945y5U2RVqkYyw89ksjd1o1_yufMjyHNl_c`, dal commento `1961118650` (10/10).
- «Bozza documento recesso»: `17TFYfJMu8NRG_6pdOf0McvJZcfh4SXuxglTrYwYRMec`, stesso commento.
- Commenti sulla board Feedback (`1ZS96SiXSktrMXrvLrsPA0`): `1959796162`, `1959741970`, `1961116918`, `1961108976`.
- Tavole lette da screenshot il 05/11: `4918:15292` (chi recede), `4918:15829` (costi), `4918:16659` (firma), `4918:19206` (cosa non è stato rispettato), `4918:19526` (mediazione), `4918:20718` (sede giudiziaria).
- Contratto preliminare v1 del 24/09/2026, art. 6.1, 8.1, 8.4.

## Differenze strutturali

1. **Atto di recesso.** UI: documento firmato con FEA su Youtrust; «Con la firma il contratto è annullato». Documento: lettera scaricata e inviata con raccomandata A.R. dal recedente; il vincolo si scioglie dopo ricezione e integrale pagamento della multa. Il commento `1959741970` chiede invece FEQ. L'art. 8.4 ammette anche la PEC, il documento cita solo la raccomandata.
2. **Ordine del recesso.** Esistono tre versioni. UI e decisione del 07/10 in CLAUDE.md: firma, registrazione, IBAN, multa. Commento del 09/10: pagamento anticipato a Cleclà e registrazione, poi documento e firma. Documento: lettera, IBAN, multa, scioglimento, poi fattura e registrazione.
3. **Sospensione durante l'inadempimento.** UI: «Il contratto è sospeso: le scadenze sono ferme e nessuno dei due può recedere». Documento: le altre condizioni vanno avanti, «non si possono sospendere i termini legali». L'art. 8.4 limita il recesso solo alla parte a cui carico si è già verificato un inadempimento dell'art. 8.1.
4. **Gestione dell'inadempimento.** UI: lista di motivi, mediazione di Cleclà accettata da entrambi, esito, sede giudiziaria dentro la pagina. Documento: testo libero, difesa, proposte e risposte senza limite, commenti di Cleclà, domanda «Avete raggiunto un accordo?», vie legali fuori dalla piattaforma. Il commento `1961108976` dice però «Noi non mediamo il recesso, solo l'inadempimento».

## Elementi mancanti in UI

Recesso:

- Registrazione con Cleclà o in autonomia.
- Caricamento dell'avviso di ricevimento della raccomandata.
- IBAN e quote per ogni beneficiario, oppure lettera firmata da tutti.
- Conferma di incasso di ogni ricevente: i cointestatari non sono utenti registrati (decisione del 07/10).
- Avviso del termine dell'art. 8.4 e della regola sulla data di ricezione (art. 1335 c.c.). Tocca il punto D18.
- Promemoria della provvigione a chi subisce il recesso, a contratto efficace.

Inadempimento:

- Tasto «Accetta inadempienza», con documento FEQ, pagamento, registrazione e risoluzione.
- Campi per difesa e proposta di soluzione; sezione dei commenti di Cleclà.
- Accordo descritto da una parte, confermato dall'altra, documento FEQ preparato da Cleclà.
- Costi distinti fra contratto non efficace e contratto efficace.
- Registrazione dell'accordo: 216 € a carico della parte inadempiente.

## Da correggere se confermato

- `4918:15292` «Basta il recesso di uno di voi»: il commento `1961116918` chiede l'unanimità della parte. Vale anche per `5275:7404` e `5275:7376`.
- `4918:15829`: mancano l'IVA sul 3% (9.882 € invece di 8.100 €) e la provvigione a contratto efficace. Il totale di 22.221 € cambia.
- `4918:20718`: la sentenza caricata e la chiusura in piattaforma non hanno riscontro nel documento.
- CLAUDE.md, «firma FEA del documento di recesso prima dei pagamenti»: superata dai documenti successivi, se confermati.

## Dubbi sui documenti del cliente

- Registrazione del recesso: 637 € (200 + 32 + 405) a inizio documento, 621 € in fondo e nel commento `1960364788`.
- Provvigione del venditore: «2.700 € > 2.000 € ok, quindi 2.000 € + IVA = 2.440 €». Sembra un errore: con il calcolo dell'acquirente sarebbero 3.294 €.
- Inadempimento accettato: il testo dice che il contratto si risolve e poi che l'inadempiente carica la quietanza. Non è chiaro se la risoluzione aspetti il pagamento, né come la controparte comunica l'IBAN.
- Accordo raggiunto: chi è «la parte inadempiente» che paga, se l'inadempimento era contestato?
- «La parte che contesta l'inadempimento»: è chi segnala o chi si difende? Può rispondere «no» da sola, e c'è un limite di tempo allo scambio?
- Nessuna soluzione: con contratto solo valido «bisognerà seguire l'evolversi della vicenda». Stato del contratto, annuncio e chiusura non sono definiti.

## Effetto sullo sviluppo

Lo scambio di risposte senza limite pone lo stesso problema di complessità sollevato sulla proroga, e i Requirements (riga 37) prevedono selezione da lista e conferma della controparte. Il documento del cliente è comunque una fonte valida per la regola di perimetro del 08/10.

## Domande al cliente

Raccolte nel documento «Parte seconda»: https://claude.ai/artifact/WwRkbr2bf4c8rQBuRmaUrS

## Non verificato

Tavole lette solo da screenshot; non ho aperto le altre tavole di uscita né il percorso Acquirente. Per quelle mi baso su `claude/ui-finalizzazione-pg3.md` e `claude/modifiche-risposte-cliente-07-10.md`. Nessuna valutazione legale.

## Termini nuovi per il glossario

Nessuno confermato. Il cliente usa «importo convenzionale pattuito» dove la UI dice «Corrispettivo a Cleclà», e alterna «inadempienza» e «inadempimento»: nei testi resta «inadempimento».
