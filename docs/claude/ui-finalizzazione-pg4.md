# UI · Finalizzazione PG4 Conclusione del contratto, desktop 1440

Versione 0.2 · 05/10/2026 · file **Cleclà | UI** (`0k5JkkrVwDydzvUoRHv8ye`), pagina `🫟 UI Layouts` di Sprint 5 - Finalizzazione (`44:986`), sezione `PG4 · Conclusione del contratto · desktop 1440 🚧` (`4940:56655`), sotto la sezione della PG3.

Fonti: wireframe PG4 (`claude/wireframe-finalizzazione.md`, frame `4851:14988`–`4851:15791`), PG `clecla_pg_finalizzazione_v2.md` sezione PG 4, UI PG1 (K2, K5), UI PG3 (pagamenti, alert, percorso), Trova tecnici di Sprint 2 (`4807:62445`), glossario v1.1.

Stato: desktop completa, in review. Mobile non disegnato.

## Tavole

Codici C1–C6 come il wireframe. Etichette a 108 px come in PG1–PG3. Stati alternativi e note sotto la tavola, riquadri tratteggiati senza fondo.

| Tavola | Node | Vista | Oggi nel caso | Stati alternativi e note |
|---|---|---|---|---|
| C1 · Provvigione da pagare | `4940:56656` | Acquirente | 13/01/2027 | Popover «Perché le due percentuali sono diverse?» · Marco ha già pagato (stato senza importo) · nota sulla seconda domanda dell’help · nota D31 |
| C2 · Provvigione da pagare e annuncio | `4940:57501` | Venditore | 13/01/2027 | Nota punto 34 · nota «e se il rogito non si fa» · nota sulle righe personali di Marco |
| C3 · Provvigione pagata, contatti sbloccati | `4940:58186` | Acquirente | 15/01/2027 | Bonifico con quietanza · bonifico in verifica · carta rifiutata · scadenza vicina · scadenza superata · punto 37 · mail di recap |
| C4 · Documenti per il notaio e controllo finale | `4940:59076` | Acquirente | 18/02/2027 | Documento obsoleto, vista di Marco · documentazione validata con badge in bacheca · controllo oltre lo SLA · gruppo D prima del pagamento («A carico di Cleclà») |
| C5 · Scorciatoia «Cerca notai» | `4940:60889` | Acquirente | — | Nota da dove si arriva (blocco «Il notaio») · nota sull’unica modifica a Trova tecnici |
| C6 · Aperta da K2, senza condizioni | `4940:61491` | Acquirente | 25/10/2026 | Nota su cosa cambia rispetto a C1 |
| C1b · Provvigione da pagare con bonifico | `5055:21241` | Acquirente | 13/01/2027 | Quietanza caricata · file non valido · dopo «Ho eseguito il bonifico» · quietanza non corrispondente (da validare) · bonifico non accreditato dopo [SLA] |
| C2b · Provvigione da pagare con bonifico | `5055:21695` | Venditore | 13/01/2027 | Stessi cinque stati di C1b, con 2.700 € e la causale di Marco |

### Percorso del bonifico (C1b, C2b, aggiunto il 05/10)

«Come paghi» con il bonifico selezionato apre sotto la card «Paga con un bonifico»: importo (+ IVA, con il totale IVA inclusa in segnaposto), intestatario, IBAN, causale «Provvigione · contratto Via Roma 12, Cuneo · [nome]», «Copia le coordinate», caricamento della quietanza, CTA «Ho eseguito il bonifico» disattivata finché la quietanza non c’è. Il bottone «Paga … + IVA» del pagamento con carta non compare. Dopo l’invio la provvigione va in «Pagamento in verifica» e il passo successivo diventa «Ci pensiamo noi»; la fattura e lo sblocco dei contatti arrivano con l’accredito. Ragione sociale e IBAN di Cleclà restano segnaposto. Il controllo della quietanza contro importo e causale è un’aggiunta rispetto alla PG, DA VALIDARE.

## Dati del caso

Catena UI di PG1–PG3, non quella del wireframe. Mutuo avverato il 10/12/2026 (comunicato da Giulia, delibera-mutuo.pdf), regolarità avverata il 12/01/2027 (Marco, esito-sanatoria.pdf), efficace dal 12/01/2027, rogito entro il 15/06/2027. Provvigione Giulia 5.400 € + IVA, Marco 2.700 € + IVA. Giulia paga il 15/01/2027 con carta; Marco paga dopo (in C1 alternativo il 14/01, in C4 risulta pagata).

Lista per il notaio: niente terreno e niente successione, quindi 14 righe pertinenti su 19 (A 2, B 5, C 3, D 4). Pronte: 8 prima del pagamento, 11 dopo (le tre voci di Cleclà), 12 in C4 con lo stato libero caricato.

C6: nessuna condizione, efficace e registrato il 20/10/2026, provvigione di Giulia pagata il 24/10/2026 in K2, rogito entro il 15/06/2027 (come K2 UI).

## Shell e regole

Pagine: clone di K5 (Acquirente) della PG1; per C2 Navbar e Sidebar di K2 (Venditore). Spalla: stepper «Rogito» (Condizioni sospensive · Provvigione · Documenti per il notaio · Firma dal notaio) (trovato così il 05/10 al posto dello stepper Contratto); card «Hai dubbi?». C5 è la pagina Trova tecnici di Sprint 2 con Navbar e Sidebar di Giulia.

Ordine dei blocchi: titolo «Contratto efficace · …» e badge «Efficace» · link «Vedi il contratto e le condizioni» · riga dei fatti (passo successivo, efficace dal, rogito entro) · Dove siete arrivati (condizioni con data, chi l’ha comunicata, documento; cosa manca ancora) · (la card «A che punto siamo» non c’è più: i quattro passi stanno nello stepper Rogito in spalla) · La tua provvigione (stroke warning finché è da pagare) · Come paghi e CTA · I documenti che il notaio vi chiederà · Il controllo finale · Il notaio · I vostri contatti · Il tuo annuncio (solo Venditore) · supporto.

- I quattro gruppi della lista sono righe apribili con il contatore per gruppo; tre stati di riga come badge: «Già in piattaforma» (con spunta), «Da richiedere», «A carico di Cleclà».
- Quando il controllo finale chiede un’azione (C4), la card passa sopra la lista con lo stroke warning e la CTA.
- Pagamenti come PG3: «Come paghi» clonata, CTA che nomina la cifra, bonifico con coordinate e quietanza nello stato alternativo.
- Un solo bottone pieno per pagina. Alert solo negli stati alternativi: Danger per la carta rifiutata, Warning per le scadenze della provvigione e il documento obsoleto, Info per SLA e attese, Success per la documentazione validata.
- Niente box con le due parti (decisione del 01/10).

Gate di libreria: superato su C1–C4 e C6. In C5 restano 9 fill e stroke non legati a variabili, ereditati dalla pagina Trova tecnici di Sprint 2 e non toccati. Annotazioni Dev Mode: 40, sulle decisioni e discrepanze; quelle ereditate dai cloni sono state tolte.

## Scostamenti dal wireframe

- Dati della catena UI: due condizioni invece di tre, rogito 15/06/2027 invece di 31/03/2027, niente CDU nella lista.
- Titolo della card «La tua provvigione» come K2 UI (PG e wireframe: «La nostra provvigione»).
- «Pagamento ed esiti» del wireframe C3 diventano stati alternativi della tavola con la provvigione pagata, che porta anche i contatti sbloccati (ex C5).
- C5 è la pagina di Trova tecnici con i filtri impostati; il blocco «Il notaio» sta in C1.
- Nella vista di Marco (C2) il gruppo A è chiuso: il suo stato civile non è nel caso.

## Discrepanze da segnalare

Ereditate dal wireframe e non risolte: D25, D26, D27, D28, D29, D30, D11, punti 33, 34, 37, 40.

Nuove:

- **D31 · Quando arriva la lista per il notaio.** Wireframe e UI la mostrano da subito; K2 e K5 UI dicono «Quando hai pagato ti diamo la lista dei documenti per il notaio». Una delle due versioni va cambiata.
- **D32 · Esiti del controllo.** «Verificati · Da rifare · Non leggibile» (PG, MVP 35) contro gli stati di verifica documento del glossario [PK], «Verifica superata» ed «Esito negativo».
- **D33 · Chi rifà la visura.** Il wireframe la fa rifare a Marco; il glossario §6.2 mette la visura catastale fra i «Documenti che ti fornirà Cleclà».
- **D34 · Il notaio.** Glossario §11 [A]: «se non hai contatti puoi selezionare uno dei nostri partner»; la PG dice «l’elenco di chi lavora nella zona, senza commissioni».
- **Etichette della lista.** «A carico di Cleclà» contro il modello §6.1 «Documenti che ti fornirà Cleclà»; «Fattura di provvigione» contro §6.2 «Fattura Cleclà per provvigione».
- Nessuno scostamento sui termini bloccati.

## DA VALIDARE

Termine di pagamento della provvigione, [GG/MM] in segnaposto · IVA (glossario §4.2) · risposta a «Cosa succede se non pago?» · cosa succede dopo la scadenza · SLA del controllo finale, [SLA] in segnaposto · chi paga il notaio · etichetta «impegnato, rogito da fare» · cosa succede se il rogito non si fa · se i contatti aspettano anche il pagamento dell’altra parte (punto 37) · ragione sociale e IBAN di Cleclà per il bonifico.

## Nota operativa

Helper di sessione su `globalThis.P4` (non persistono): `page`, `card`, `row`, `group`, `step`, `badge`, `btn`, `alert`, `alt`, `pop`, `noteF`, `stack`, `fit`, `note`. Sorgenti in `P4.S`: nodi di K2, K5 (PG1) e U4, U7, U8 (PG3). Id di sezione, tavole e stati alternativi nel plugin data di `figma.root`, chiave `pg4ui`. I frame pagina non sono in Auto Layout: dopo un cambio di altezza del Main content va ridimensionato il frame.
