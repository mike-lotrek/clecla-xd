# UI · Finalizzazione PG2 Comunicazione dell’esito di una condizione sospensiva, desktop 1440

Versione 0.1 · 01/10/2026 · file **Cleclà | UI** (`0k5JkkrVwDydzvUoRHv8ye`), pagina `🫟 UI Layouts` di Sprint 5 - Finalizzazione (`44:986`), sezione `PG2 · Comunicazione dell’esito · desktop 1440 🚧` (`4907:20681`), sotto la sezione della PG1.

Fonti: wireframe PG2 (`claude/wireframe-finalizzazione.md`, frame M1–M9), PG `clecla_pg_finalizzazione_v2.md` sezione PG 2, UI PG1 (`claude/ui-finalizzazione-pg1.md`), modali v2 della Trattativa (`claude/ui-pg2-v2-feedback-20-09.md`), caricamento documenti (`claude/caricamento-documenti-28-09.md`), glossario v1.1.

Stato: desktop completa, in review. Mobile non disegnato.

## Tavole

Codici E1–E10 (Esito), per non confondersi con M- delle tavole mobile. Etichette a 108 px come in PG1. Stati alternativi sotto la tavola, riquadri tratteggiati senza fondo.

| Tavola | Node | Vista | Wireframe | Stati alternativi |
|---|---|---|---|---|
| E1 · Comunica l’esito, il bivio | `4907:20687` | Acquirente | M1 | Popover del (?) |
| E2 · Si è avverata | `4907:20849` | Acquirente | M2 | Documento da caricare · errori di caricamento · data non valida · campo documento per condizione |
| E3 · Dopo la dichiarazione di avveramento (pagina) | `4907:21169` | Acquirente | M3 | Vista di Marco con notifica · storico aperto |
| E4 · Era l’ultima condizione | `4907:21733` | Acquirente | M3 (alternativo) | — |
| E5 · Non si avvererà, motivazione | `4907:21794` | Acquirente | M4 | Rinuncia (penale) · pratica fuori tempo (proroga suggerita) · nessuna motivazione · regolarità con documento |
| E6 · Autocertificazione e firma FEA | `4907:22007` | Acquirente | M5 | Firma in corso · firma non completata · autocertificazione non generata |
| E7 · Contratto sciolto | `4907:22268` | Acquirente | M6 | Vista di Marco: notifica e prima card di K7 |
| E8 · Proponi una nuova scadenza | `4907:22349` | Acquirente | M7 | Data non valida · proroga già chiesta · scadenza superata · riga «Proroga richiesta» |
| E9 · Risposta alla proroga | `4907:22512` | Venditore | M8 | Riga d’ingresso con «Rispondi alla richiesta» · accettata · mantenuta (vista di Giulia) |
| E10 · Scadenza superata, finestra aperta (pagina) | `4907:23088` | Venditore | M9 | Promemoria inviato · notifica ed email a Giulia · chiusura della finestra, due viste |

## Dati del caso

Catena UI della PG1: mutuo entro il 26/12/2026 (Giulia Rossi), regolarità urbanistica e conformità catastale entro il 26/03/2027 (Marco Ferrero), rogito entro il 15/06/2027. Ramo avverata e proroga: oggi 26/11/2026 (K4, 30 giorni). Ramo non avverata: 18/12/2026, la data di K7 in PG1. Proroga chiesta al 24/02/2027 (+60 giorni). Finestra: oggi 27/12/2026. Nel caso «ultima condizione» la regolarità è avverata il 18/11/2026.

## Shell e regole

Modali: guscio di X1 della Trattativa v2. Card crema 668, raggio 16, padding 24, chiusura `Nav tabs` Primary-square, eyebrow monospaced e titolo Heading 2 centrati, sottotitolo con la scadenza. Fondo: K4 Acquirente o K3 Venditore esportati in PNG sotto lo scrim `bg-modal-bg` all’80%. Hash in plugin data `pg2fin` su `figma.root`.

- Eyebrow: «COMUNICA L’ESITO», «· SI È AVVERATA», «· NON SI AVVERERÀ», «PROPONI UNA NUOVA SCADENZA», «RISPONDI ALLA RICHIESTA», «CONTRATTO EFFICACE», «CONDIZIONE NON AVVERATA». Titolo: la condizione («Mutuo»), salvo E4, E6, E7 ed E9.
- Un solo Primary per modale. Uscite secondarie Link-dark sotto, centrate. «Cambia risposta» sta in fondo, come «Indietro» nelle modali della trattativa: esce la freccia in alto del wireframe.
- Firma dell’autocertificazione Destructive-fill, come «Annulla la trattativa»: è l’atto che scioglie il contratto.
- Conseguenze in box `bg-surface-subtle` con etichetta piccola, come «Cosa succede se annulli» di X1. Costo zero in box bianco con (?).
- Data con `Input field` e icona `icon/edit_calendar` a destra. Errori con State=Danger e testo d’aiuto nel colore del titolo dell’Alert Danger.
- File caricato: riga bianca con `icon/description`, nome, peso, «Sostituisci». Zona di caricamento clonata dal pannello documenti di PG3.
- Data protagonista in E9 a 48/Light, regola delle modali «Rispondi» del 17/09.
- Avvisi: Alert Danger per errori, Warning solo sulla rinuncia (causa imputabile), Info sul suggerimento di proroga e sulla proroga già chiesta, Success Default come toast.
- Pagine E3 ed E10 clonate da K4 e K3 della PG1: stroke success sulla condizione avverata, warning dove tocca a te, nessuno stroke dove si aspetta l’altro.

Gate di libreria superato: nessun fill o stroke senza variabile e nessun testo senza stile fuori dalle istanze, a parte le etichette delle tavole, che sono quelle della PG1.

## Scostamenti dal wireframe

- Testo concordato del mutuo da T4 v2, senza importo. Escono la frase di confronto con la cifra deliberata (M1) e «meno di 190.000 €» fra le motivazioni (M4), che diventa «un importo inferiore a quello che serviva».
- Modale dell’ultima condizione con la CTA di K5 («Vai alla provvigione e ai documenti») al posto di «Vai ai prossimi passi».
- E7: «Vedi il contratto annullato» al posto di «Vai al contratto»; per Marco l’autocertificazione resta nella notifica e nei documenti di K7, non nella card.
- E8: campo «Nota per Marco Ferrero (facoltativa)», formula delle modali di trattativa, al posto di «Perché ti serve più tempo».
- E10: pagina di chi aspetta (Marco); la vista di Giulia è già lo stato alternativo «Scadenza superata, finestra aperta» di K4 in PG1 (`4897:14050`).
- Storico della condizione: (3) dopo avviso e dichiarazione o richiesta, (4) dopo proroga o scadenza.

## Discrepanze da segnalare

- **Testo concordato del mutuo.** PG e wireframe lo scrivono con l’importo («delibera di almeno 190.000 €»); T4 v2 e la UI della PG1 dicono solo «esito della richiesta di mutuo». Senza importo, «La banca ha concesso un importo inferiore» non ha un termine di confronto scritto nel contratto. Va deciso se l’importo entra nella condizione.
- **«Condizione scaduta».** Badge nuovo, non fra i sei della PG1.
- **«Sciolto» e «annullato».** La modale E7 dice «Il contratto è sciolto» (l’evento), K7 dice «annullato» (lo stato). Entrambe le forme hanno una fonte: «si scioglie» dalle correzioni alla PG1 della trattativa, «Annullato» dal badge della PG1.
- **E9 risponde a una richiesta del 26/11, ma il fondo è K3 a 50 giorni.** Solo contesto oscurato; da rigenerare se si vuole coerente.
- Ereditate dal wireframe, non risolte: D12 (promemoria ogni 48 ore contro 4 giorni del silenzio in trattativa), D13 (correzione entro 48 ore), D14 (una proroga per condizione), D15 (motivazioni dal lato inadempimento), D16 (documento della prelazione), D1 (helper verso la guida al contratto preliminare), D2 (costo zero con la provvigione).
- Nessuno scostamento dal glossario sui termini bloccati: «condizioni sospensive», «avveramento», «inadempimento», Youtrust.

## DA VALIDARE

Punto 30 (soglia della finestra, [GG/MM] in E8 ed E10) · punto 31 (solo chi ha la condizione dichiara il mancato avveramento) · punto 35 (documento obbligatorio per tutte) · D13, D14, D15 · «promissaria acquirente» come formula dell’autocertificazione · se dopo la chiusura della finestra la proroga resta proponibile · testo dello stato «proroga già chiesta» quando Marco l’aveva mantenuta (disegnato solo il caso accettata).

## Nota operativa

Helper di sessione su `globalThis.M` (non persistono): `modal`, `fit`, `alt`, `t`, `f`, `box`, `btn`, `input`, `radio`, `fileRow`, `uploadZone`, `alertBox`, `toast`, `badge`, `setBadge`, `noArrow`. Usano anche `globalThis.UI` della PG1. La sorgente dell’input data con icona calendario era un nodo temporaneo, eliminato a fine lavoro: per rigenerare, clonare un `Input field` Filled, attivare Right Icon e fare `swapComponent` con il main di `icon/edit_calendar`. Se K4 o K3 cambiano, i fondi delle modali vanno riesportati e riassegnati a tutti i rettangoli «Pagina contratto (sotto)».
