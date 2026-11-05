# UI · Finalizzazione PG1 Pagina contratto, desktop 1440

Versione 0.5 · 05/10/2026 · file **Cleclà | UI** (`0k5JkkrVwDydzvUoRHv8ye`), pagina `🫟 UI Layouts` di Sprint 5 - Finalizzazione (`44:986`), sezione `PG1 · Pagina contratto · desktop 1440 🚧` (`4888:58566`).

Fonti: wireframe `claude/wireframe-finalizzazione.md`, PG `clecla_pg_finalizzazione_v2.md`, regole UI di PG3 v2 e PG4 v2, glossario v1.1.

Stato: PG1 desktop completa, in review. Mobile non disegnato.

## Tavole

Ordine in sezione, da sinistra: K3.0, K3, K4, K2, K5 Acquirente, K5 Venditore, K6, K7, Listing. Etichette bianche a 108 px come in PG2 v2. Gli stati alternativi stanno sotto la tavola, in riquadri tratteggiati senza fondo.

| Tavola | Node | Vista | Oggi nel caso | Stati alternativi |
|---|---|---|---|---|
| K3.0 · Appena registrato | `4897:13019` | Acquirente | 20/10/2026 | Riquadro K1 (rimando a PG4 v2 R0, R1, R2, R4) |
| K3 · Attivo, condizioni da avverare | `4888:58567` | Venditore | 06/11/2026 | — |
| K4 · Condizione in scadenza | `4897:13572` | Acquirente | 26/11/2026 | Giorno della scadenza `4897:14028` · Scadenza superata, finestra aperta `4897:14050` · Vista del Venditore a 30 giorni `4897:14073` |
| K2 · Efficace, nessuna condizione | `4897:14086` | Venditore | 22/10/2026 | — |
| K5 · Efficace | `4897:14585` | Acquirente | 13/01/2027 | — |
| K5 · Efficace | `5029:20760` | Venditore | 13/01/2027 | — |
| K6 · Sospeso, mediazione in corso | `4897:15068` | Venditore | 20/01/2027 | SLA del team superato `4897:15541` · Azione giudiziaria `4897:15564` |
| K7 · Annullato per inefficacia | `4897:15567` | Acquirente | dopo il 18/12/2026 | Recesso del Venditore `4897:16054` · Inadempimento confermato `4897:16064` · Cosa puoi fare adesso, Venditore `4897:16073` |
| Gestione contratti · Listing | `4897:16542` | Venditore | 06/11/2026 | Nessun contratto `4897:17088` |

## Decisioni prese con Giovane

- 01/10 · **Dati del caso dalla catena UI**, non dal wireframe: due sospensive, mutuo entro il 26/12/2026 (Giulia Rossi) e regolarità urbanistica e conformità catastale entro il 26/03/2027 (Marco Ferrero), rogito entro il 15/06/2027.
- 01/10 · **Niente box con le due parti** (nome, ruolo, «Identità verificata») in nessuno stato della pagina contratto.
- 05/10 · **Fase «Rogito» nello stepper** (supera il 29/09). La fase «Contratto» si chiude con la Registrazione; da Condizioni sospensive in poi tutta la Finalizzazione (PG1–4) sta nella fase «Rogito». «Verso il rogito» resta il titolo esteso della pagina pubblica Come funziona.
- 05/10 · **Niente frasi sulle condizioni che non si applicano**: creano confusione. Tolta la riga «Non si applicano: …» da K3, K3.0, K4, K5, K6, E3, E10.
- 05/10 · **Tolto «A che punto siamo»** dalle pagine Conclusione (C1, C2, C3, C4, C6): ripeteva la sequenza dello stepper.
- 05/10 · **K4: la riga della condizione in scadenza tiene «Comunica l'esito» come CTA secondaria** (Outline), anche se la primaria sta nel blocco «La prossima scadenza».
- 05/10 · **K5 anche in vista Venditore**: efficace per condizioni avverate, CTA verso C2.

## Stepper

**Fase «Contratto»** (Preparazione alla firma, Pagamento registrazione, Sprint 4): Persone e documenti (`group`) · Contratto preliminare · Firme · Registrazione. «Condizioni sospensive» tolto il 05/10 dalle 14 tavole dello Sprint 4; R0, R1, R2, R4 hanno Registrazione attiva, R3 tutto completato.

**Fase «Rogito»** (Finalizzazione PG1–4), titolo «Rogito», quattro passi:

| Passo | Icona | Helper se futuro |
|---|---|---|
| Condizioni sospensive | `edit_calendar` | — |
| Provvigione | `payments` | Quando il contratto è efficace |
| Documenti per il notaio | `description` | Dopo la provvigione |
| Firma dal notaio | `home` | Entro il 15/06/2027 |

Passo attivo per stato, helper «Sei qui»:
- Condizioni sospensive: K3.0, K3, K4, K6, K7, PG2 (E3, E10), PG3 (U4–U8, U12–U15).
- Provvigione: K5 (entrambe le viste), K2, C1, C2.
- Documenti per il notaio: C3, C4, C6.
- K2 e C6: «Condizioni sospensive» completato con helper «Nessuna».

Link sotto lo stepper invariati: Guida al contratto preliminare, Riepilogo degli accordi. Nome dell'ultimo passo «Firma dal notaio»: il glossario I13 sul momento finale è ancora aperto.

## Shell e regole

Venditore: clone di PG4 v2 R4. Acquirente: Navbar e Sidebar di R3. Spalla: stepper «Rogito», link, card «Hai dubbi?». Il listing ha solo la card «Hai dubbi?».

Righe di condizione clonate dagli argomenti di PG2 v2: icona di stato a destra (orologio tocca a te, cerchio in attesa, spunta avverata), badge senza icona tranne «Avverata» con la spunta, storico nel piede. Stroke warning sul blocco dove tocca a te, stroke success sulle condizioni avverate (K5). Un solo bottone pieno per pagina, nessun Alert.

Ordine dei blocchi di K3: titolo e badge di stato · riga dei fatti · La prossima scadenza · Le condizioni che tengono sospeso il contratto · Se una delle due parti si tira indietro · I documenti di questo contratto · Cosa succede adesso · uscite.

Per stato:
- **K3.0**: in cima la card «Il contratto è registrato» di R3, con i download. Notaio e documenti per il rogito di R3 non ci sono (D11).
- **K4**: blocco scadenza promosso con stroke e azioni («Comunica l'esito» primaria, «Proponi una nuova scadenza» link); la riga della condizione tiene stroke, badge, storico e «Comunica l'esito» secondaria (Outline); esce il caricamento in anticipo.
- **K2**: card «Il contratto è già efficace» e card «La tua provvigione» (2.700 € + IVA, stato di Giulia senza importo, «Paga 2.700 € + IVA»). Senza condizioni la provvigione si paga qui; C6 si apre dopo.
- **K5**: card «Il contratto è efficace» con «Vai alla provvigione e ai documenti»; Acquirente verso C1 (`4940:56656`), Venditore verso C2 (`4940:57501`). Nessun importo qui. Sezione condizioni rinominata «Le condizioni sospensive». Le due viste cambiano solo nell'autore delle comunicazioni e nella controparte delle uscite.
- **K2 e K5**: escono la quota del 3% e la riga «se non è colpa di nessuno».
- **K6**: card «Il contratto è sospeso» con cosa si congela e ultimo aggiornamento datato del team; righe in «Sospesa» senza azioni; esce il blocco dei costi; uscite chiuse, resta la chat.
- **K7**: card «Il contratto è annullato» con causa, costo zero e conseguenze; documenti con l'autocertificazione in cima; «Cosa puoi fare adesso». Escono condizioni, costi e documentazione dell'immobile.
- **Listing**: ordine per scadenza più vicina; ogni card dice immobile, controparte, stato e prossima scadenza con chi ha la mossa; sezione «Chiusi e annullati». Dati di Corso Nizza e Via Saluzzo inventati per il caso.

Scostamenti dal wireframe, annotati sui nodi (Dev Mode):
- badge di stato del contratto tenuto, contro la regola v2 «niente badge di fase accanto al titolo», perché lo stepper non distingue Attivo, Sospeso, Annullato;
- progress delle condizioni come fatto «0 di 2», senza barra;
- «Proponi una nuova scadenza» solo da 30 giorni prima (K4), non in K3;
- origine della condizione di regolarità riscritta sulla dichiarazione di Marco in trattativa;
- K7 recesso disegnato con la multa già ricevuta (D24), non «da ricevere»;
- CTA «Vai alle trattative» aggiunta all'empty state del listing.

## Discrepanze da segnalare

- «Mutuo dell'acquirente» (wireframe) contro «Mutuo» (T4 v2, R3): in UI «Mutuo».
- «Penale», «clausola penale», «multa penitenziale»: il glossario §15.1 registra che nei frame approvati compare solo «costi aggiuntivi». In UI resta il lessico della Guida alla trattativa.
- Data del rogito: 31/03/2027 nei wireframe PG2 e PG4, 15/06/2027 in T4 v2. In UI 15/06/2027.
- Il wireframe K3 mostra quattro condizioni, K3.0 e R3 due: il resto dei wireframe va riallineato se si tiene la catena UI.
- K6: la frase sul perimetro della mediazione («Non decidiamo noi chi ha ragione») contro il glossario §15.7 (D22).
- K6: badge di riga «Sospesa» non è fra gli stati della PG.
- K7: «né provvigione, né penali, né rimborsi» (Guida) contro «né penali, né rimborsi» (PG): D2, usata la prima.
- Nomi delle fasi (glossario I10, I13): la home venditore HV5 e lo stepper acquirente CC4 dicono «Rogito»; bacheca, CF5 mobile e Come funziona dicono «Verso il rogito». Deciso «Rogito» nello stepper, va allineato sulle altre superfici.
- PG2: due note di stato alternativo (`4907:21040`, `4907:22004`) parlano ancora delle condizioni che non si applicano. Sono note di progetto, non testo d'interfaccia: lasciate.
- Pagine C: «Le voci che non riguardano il vostro caso non compaiono» nella checklist dei documenti per il notaio. Riguarda i documenti, non le condizioni: lasciata, da confermare.

## DA VALIDARE

Aliquote e importi di multa, quota del 3% e penale (punti 26, 27, 38) · soglia della finestra dopo la scadenza, [GG/MM] segnaposto (punto 30) · termine di pagamento della provvigione in K2, [GG/MM] segnaposto · quando si chiude la card «Il contratto è registrato» in K3.0 · cosa si congela durante la mediazione · se Marco può comunicare la regolarità mentre il contratto è sospeso · SLA del team in K6 · accesso all'archivio dell'immobile dopo l'annullamento.

## Da fare

- Archiviare le tavole R3 della PG4 v2 (desktop `4456:179821`, mobile `4456:184741`): R3 ora è K3.0.
- Allineare lo stepper delle tavole mobile, se esistono, alla fase «Rogito».
- Collegare con un prototype flow le CTA di K5 a C1 (Acquirente) e C2 (Venditore).

## Nota operativa

Gate di libreria superato su tutte le tavole: nessun fill o stroke senza variabile fuori dalle istanze, nessun testo senza stile. Apostrofi tipografici (’). I frame non sono in Auto Layout: dopo ogni cambio di altezza del Main content va ridimensionato il frame.

Helper di sessione su `globalThis` (non persistono, si perdono al reload del plugin): `UI` (`clonePage`, `toAcquirente`, `card`, `txt`, `frame`, `btn`, `whiteBox`, `warnStroke`, `okStroke`, `setIcon`, `alt`, `note`, `fit`) e `applyRogito(frame, indiceAttivo, {completedHelper})`. Gli id delle sorgenti sono nel plugin data di `figma.root` (`pg1ui_src`, `rogito_src`): gli id dei modelli dello stepper in `rogito_src` puntano a un contenitore eliminato il 05/10, per riusare `applyRogito` vanno rigenerati da K3. `UI.alt` va chiamato con `node = null` se il contenuto si aggiunge dopo; `whiteBox` richiede un genitore in Auto Layout. In `Badge`, testo e icona vanno impostati in chiamate separate. Per cambiare lo stato di uno stepper nav link conviene clonare un'istanza già nello stato voluto: cambiare `State` fa perdere gli override di colore. Per passare una tavola da Acquirente a Venditore si sostituiscono Navbar e Sidebar bacheca con quelle di K3.
