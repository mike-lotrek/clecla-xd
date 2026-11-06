# Verifica · proroga di una condizione sospensiva: data negoziata o richiesta secca

05/11/2026, aggiornato dopo la lettura dei commenti del cliente. Verifica di sola lettura: nessuna modifica a Figma, a FigJam o ai fogli.

## Esito

Nessun requisito obbliga a negoziare la nuova data: i Requirements non citano la proroga. La richiesta arriva però in modo esplicito dal feedback del cliente, e per la regola di perimetro del 08/10 il feedback è una fonte valida. La decisione va quindi presa col cliente.

## Commenti del cliente

Board «[EXT] Cleclà | Feedback» (`1ZS96SiXSktrMXrvLrsPA0`), tutti aperti:

- 08/10, `3231:16435`, commento `1958283101`: «si potrebbe inserire la possibilità di fare una controporoposta per quanto riguarda la tempistica, cioè che non sia poprio bloccato o accetti la data proposta o rifiuti».
- 10/10, `3231:17733`, risposta `1961060722`: «Questo vale per tutte le condizioni sospensive: quando si propone una nuova data, permettere alla controparte di rispondere con una controproposta di data». Il commento padre `1961059471` chiede, per la sola regolarità, una nota visibile con la clausola sulla buona fede: un invito a non rifiutare la proroga.
- 10/10, `3231:17281`, commento `1961039630`, a scadenza superata: «può solo proporre una nuova data e l'altra parte può accettare o rifiutare oppure segnalare l'inadempienza». Stesso giorno, ma senza controproposta.
- 08/10, `3231:16495`, commento `1958287286`: dopo la scadenza l'altra parte «potrà accettare o andare nel flusso inadempienza».

Stessa fonte, punti collegati:

- 10/10, `3231:16435`, `1961063006`: «Con la proroga della scadenza della condizione si accetta la proroga dello stesso tempo del rogito».
- 10/10, `3231:16201`, `1961055582`: la scadenza di tutte le condizioni è il trentesimo giorno prima del rogito.
- 10/10, `3231:17073`, `1961035327`: richiesta di nuova scadenza possibile «fin da subito», non solo a ridosso della scadenza. Contraddice `clecla_pg_finalizzazione_v2.md:496`.
- 08/10, `3231:17733`, `1958221777`: «un'eventuale modifica ad un contratto preliminare deve essere fatta con FEQ non FEA». Contraddice `claude/modifiche-risposte-cliente-07-10.md:19`.

Board «[EXT] Cleclà | User Flows» (`DXvZbuexjok4HOsLSuLiEK`), 14/03, `310:5025`, commento `1674303919`, risolto: la controparte «dovrà accettare o rifiutare». «Nel caso di rifiuto si rimane in attesa fino alla scadenza della data già prestabilita». È la specifica da cui nasce il ramo D.

## Altre fonti

- **MVP Functional Requirements (versione del 16/10/2026):** nessuna occorrenza di proroga, rinvio o nuova scadenza. La riga 27, «Fai controproposta», riguarda la Trattativa.
- **User Stories, «Finalizzazione - REVIEW 16/03», e Contenuti:** nessuna occorrenza di «proroga».
- **Board User Flows, ramo D (`388:2166`):** «Inserisci nuova scadenza» (`391:2129`, `392:2297`), poi «Accetta nuova scadenza?» (`391:2189`, `392:2311`) con SI o NO.
- **Guida venditore del 14/09:** «tu e l'Acquirente potete accordarvi per una proroga»; senza accordo, o superato il tempo massimo, il contratto diventa inefficace.
- **Contratto preliminare v1 (24/09/2026):** art. 10, modifiche valide «solo se approvate e sottoscritte da tutte le Parti»; art. 3.3.1, buona fede sui ritardi non imputabili al venditore; art. 7, esito entro il trentesimo giorno prima del rogito.

## Punti da decidere col cliente

1. Proposta: richiesta con accetta o rifiuta; chi rifiuta può indicare in una nota la data che accetterebbe; dopo un rifiuto si può fare una nuova richiesta. Cade il limite D14 (`clecla_pg_finalizzazione_v2.md:504`). Se il cliente vuole una vera controproposta, ripiego: una sola, poi accetta o rifiuta e il ciclo finisce.
2. Effetto a catena: se il rogito si sposta dello stesso tempo, si spostano anche le scadenze delle altre condizioni ancora aperte?

Le domande su proroga e archivio sono nel documento per il cliente: https://claude.ai/artifact/AV6hrRdQCPAEaihByWMDbv

## Da riallineare

Se confermato dal cliente, in PG e tavole: vincolo della nuova data (`clecla_pg_finalizzazione_v2.md:497`), proroga disponibile da subito (`:496`), firma FEQ del documento di proroga. Da verificare nelle tavole: non ho controllato se questi commenti sono già stati recepiti.

## Non verificato

Sulla board Feedback ho letto i 291 thread con attività dal 01/10/2026, non quelli precedenti. La Finalizzazione è stata presentata al cliente il 07/10. Nessuna valutazione legale sul testo del contratto.

## Termini nuovi per il glossario

Nessuno. «Documento di proroga» è già segnalato come assente (`claude/modifiche-risposte-cliente-07-10.md:51`).
