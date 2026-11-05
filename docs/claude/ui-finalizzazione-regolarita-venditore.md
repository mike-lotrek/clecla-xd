# UI · Finalizzazione, condizione di regolarità del Venditore e K2 Acquirente, desktop 1440

Versione 0.2 · 06/10/2026 · file **Cleclà | UI** (`0k5JkkrVwDydzvUoRHv8ye`), pagina `UI Layouts – WIP` di Sprint 5 - Finalizzazione (`44:986`).

Fonti: UI PG1 e PG2 (`claude/ui-finalizzazione-pg1.md`, `claude/ui-finalizzazione-pg2.md`), PG `clecla_pg_finalizzazione_v2.md` sezione PG 2, «Come funziona la trattativa» 5.1 e 9.5, glossario v1.1.

## Riorganizzazione del 06/10

Le tavole della Finalizzazione non sono più divise per PG. Struttura: sezione «Panoramica» a swimlane (y 23000), poi «Percorso Venditore» e «Percorso Acquirente», ognuno con tre righe: 1 Condizioni sospensive · 2 Verso il rogito · 3 Uscita dal contratto. Le viste della controparte stanno nel percorso di chi le vede («Vista Venditore · da E3» ecc.), con una nota sulla tavola d'origine. Backup: pagina `UI Layouts – Backup 06.10`. Le vecchie sezioni PG1–PG4 sono vuote, lasciate per i commenti agganciati allo sfondo.

Titoli fuori dai frame, etichette e testi delle note in bianco (fondo scuro).

## Tavole nuove

Percorso Venditore, riga 1, dopo K3. Clonate dalle omologhe Acquirente, shell Venditore di K3.

| Tavola | Node | Clonata da | Stati alternativi |
|---|---|---|---|
| K4V · Regolarità in scadenza | `5114:5665` | K4 | Giorno della scadenza · scadenza superata · avverata con la Relazione Tecnica (da validare) + nota |
| E1V · Il bivio | `5114:7191` | E1 | Popover del (?) |
| E2V · Si è avverata | `5114:7250` | E2 | Documento da caricare · errori di caricamento · data non valida |
| E3V · Dopo la dichiarazione | `5115:6335` | E3 | Storico aperto |
| E4V · Ultima condizione, contratto efficace | `5115:7753` | E4 | — |
| E5V · Non si avvererà, documento | `5115:7849` | E5 | Zona di caricamento vuota (ex E5) · documento mancante · errori di caricamento · nota da validare |
| E6V · Autocertificazione e FEA | `5115:7963` | E6 | Firma in corso · firma non completata · autocertificazione non generata |
| E7V · Contratto sciolto | `5115:8082` | E7 | — |
| E8V · Proponi una nuova scadenza | `5115:8114` | E8 | Data non valida · proroga già chiesta · scadenza superata · riga dopo l'invio |

Percorso Acquirente, riga 1: viste di Giulia «da K4V», «da E3V», «da E7V», la modale **E9A · Proroga della sanatoria, risposta** (`5116:6292`) con lo stato «Hai accettato», e in fondo **K2 · Efficace, nessuna condizione (Acquirente)** (`5120:6256`).

K2 Acquirente: clone di K2 Venditore con shell Acquirente di K4. Provvigione 5.400 € + IVA, «2% del prezzo di acquisto, con un minimo di 4.000 €» (come C1), stato di Marco senza importo, CTA «Paga 5.400 € + IVA». Nota sotto: il pagamento segue gli stati di C1 e C1b, poi si apre C6.

## Dati del caso

Regolarità urbanistica e conformità catastale entro il 26/03/2027 (Marco Ferrero), mutuo avverato il 26/11/2026 (Giulia Rossi). K4V, E1V, E2V, E4V, E8V: oggi 24/02/2027, la regolarità è l'ultima condizione. E3V: 18/11/2026, regolarità dichiarata con il mutuo ancora aperto (data già usata in PG2). Ramo non avverata: 10/03/2027, documento `diniego-sanatoria.pdf`. Proroga al 25/05/2027 (+60 giorni), accettata il 26/02/2027. K2 Acquirente: efficace dal 20/10/2026, come K2 Venditore.

## Decisioni

- 06/10 · Nome della condizione: «Regolarità urbanistica e conformità catastale».
- 06/10 · Avveramento automatico con la Relazione Tecnica come stato alternativo di K4V, da validare.
- 06/10 · E5V resta così: il caso in cui il mancato avveramento dipende dal Venditore non si disegna per ora (nota sotto E5V).
- K4V: «Tocca a te: comunica l'esito» senza il nome della condizione, perché con «della sanatoria» la riga dei fatti non ci stava.
- E5V: documento al posto della motivazione, campo «L'esito negativo della pratica di sanatoria o il diniego del Comune» (dallo stato già disegnato in PG2).
- E8V: suggerimento «60 giorni in più» senza «il tempo tipico di una pratica»: per la sanatoria non c'è una fonte.

## Discrepanze e punti aperti

- E6V: «promittente venditore» nell'autocertificazione, in coppia con «promissaria acquirente» già da validare.
- K5 Venditore (`5029:20760`) ha date diverse (mutuo 10/12/2026, regolarità 12/01/2027) da E3/E4 e dalle tavole nuove: si vede sotto la modale E4V.
- E7V: fondo K4V, perché non esiste una K7 completa in vista Venditore.
- E9A: fondo E3 Acquirente (26/11/2026, 120 giorni), solo contesto oscurato.
- K2 Acquirente: termine di pagamento della provvigione [GG/MM] segnaposto, come in K2 Venditore.
