# Stepper «Contratto» su PG3 v2 e PG4 v2 · 29/09/2026

File **Cleclà | UI** (`0k5JkkrVwDydzvUoRHv8ye`), pagina `🚧 UI Layouts – WIP` di Sprint 4. Decisione presa con Giovane il 29/09 (vedi `claude/wireframe-finalizzazione.md`).

## La regola

Preparazione alla firma (PG3), Pagamento registrazione (PG4) e la Finalizzazione stanno nella stessa tappa di percorso, Contratto. Lo stepper di spalla ha cinque passi:

Persone e documenti · Contratto preliminare · Firme · Registrazione · Condizioni sospensive

La registrazione è un passo solo. I suoi stati interni (pagamento, deposito all'Agenzia delle Entrate, registrato) restano nella pagina, nella riga dei fatti e nell'avanzamento. La tappa «Registrazione» della PG4 v2 del 24/09 non esiste più.

Icone: `group` · `fact_check` · `draw` · `account_balance` · `edit_calendar`. «Persone e documenti» usa sempre `group` (deciso con Giovane il 29/09).

## Collegamenti

Regola decisa con Giovane il 29/09: i collegamenti compaiono solo dal passo in cui diventano disponibili e rilevanti.

- **F1 e F1b**: nessun link in spalla. Nell'intestazione c'è «Vedi il riepilogo degli accordi» (prima «Vedi il riepilogo della trattativa»), perché è l'unico rimando utile prima che esista il contratto.
- **Da F2a in poi e in PG4**: «Guida al contratto preliminare» e «Riepilogo degli accordi» in spalla; il link nell'intestazione non c'è più. Su mobile i due link stanno in un blocco «Collegamenti» sopra la card «Hai dubbi?».

## Cosa è cambiato

**PG3 v2 desktop, 9 tavole** (F1 V e A, F1b, F2a, F2b, F2c, F2d, F3 V e A): aggiunti i passi Registrazione e Condizioni sospensive, stato Initial. Le nuove istanze sono cloni di un nav link Initial già presente, non istanze con la variante cambiata: il cambio di variante non porta con sé gli override di colore e il testo risultava quasi invisibile. In F1 V, F1 A e F1b l'icona del primo passo passa da `badge` a `group`.

**PG4 v2 desktop, R0–R4**: il blocco «Registrazione (aperto)» diventa «Contratto (aperto)» con i cinque passi. R0, R1, R2, R4: passi 1–3 Completed, Registrazione Active «Sei qui», Condizioni sospensive Initial. R3: passi 1–4 Completed, Condizioni sospensive Active. Si perde l'etichetta «lo facciamo noi» che stava sul sotto-passo del deposito: la stessa informazione resta nella riga «REGISTRAZIONE ENTRO · CLECLÀ».

**Mobile, 14 tavole** (9 PG3, 5 PG4): barra di percorso a cinque segmenti, contatore «passo n di 5», segmenti arancio fino al passo in corso compreso (convenzione già in uso in entrambe). Occhiello della PG4 allineato alla PG3: da «REGISTRAZIONE DEL CONTRATTO» a «CONTRATTO · TAPPA 4 DI 4» per l'acquirente e «CONTRATTO · TAPPA 5 DI 5» per il venditore (R4). Etichetta PG4: «Sei qui: Registrazione», in R3 «Sei qui: Condizioni sospensive».

**Mobile PG3, F2a–F2d e F3 V/A**: aggiunto il blocco «Collegamenti» (clonato da M-0 R0) sopra «Hai dubbi?». In F2a–F2d è stato tolto il link «Guida al contratto preliminare» che stava dentro la sezione «Contratto preliminare», per non averlo due volte; su desktop sta solo in spalla. F3 mobile prima non aveva nessuno dei due link.

**Intestazione PG3**: in F1 V, F1 A, F1b (desktop e mobile) il link diventa «Vedi il riepilogo degli accordi»; in F2a–F2d e F3 V/A (desktop e mobile) è rimosso. 18 tavole.

## R3 esce dalla PG4

Deciso con Giovane il 29/09: R3 («Registrato») diventa il primo stato della pagina contratto, K3.0 nei wireframe della Finalizzazione (`4712:215555`). La PG4 finisce con R2 (acquirente) e R4 (venditore). Le tavole R3 desktop (`4456:179821`) e mobile (`4456:184741`) sono ancora nella sezione PG4 v2 in UI: da spostare o archiviare quando si disegna la UI della pagina contratto.

Resta da decidere dove stanno notaio e «Carica i documenti per il rogito», che R3 proponeva subito e la PG Finalizzazione mette nella Conclusione, dopo l'efficacia.
