# PG3 · Il caricamento dei documenti torna in piattaforma (28/09)

Versione 1.1 · file **Cleclà | UI** (`0k5JkkrVwDydzvUoRHv8ye`), pagina `🚧 UI Layouts – WIP`. Supera in parte `claude/coerenza-firma-verifica-25-09.md`.

## Il modello

- **Il documento d'identità si carica in piattaforma.** Ogni parte registrata aggiunge chi firma dalla sua parte e ne carica il documento. La piattaforma lo invia a Youtrust, che lo verifica ed estrae i dati.
- **La verifica non è in tempo reale.** Fra l'invio e l'esito passano i tempi tecnici di Youtrust, quindi caricamento ed esito sono due momenti separati.
- **La firma non cambia.** A ogni firmatario, registrato o no, arriva il link di Youtrust, che include anche una verifica d'identità. F2c, F2d e F3 restano come il 25/09.
- **Alla persona aggiunta** arriva l'informativa privacy e, quando il contratto è pronto, il link per firmare. Nessuna richiesta di verifica.
- **Il documento del venditore caricato per l'immobile vale**, se non è scaduto. Se scade prima del rogito va caricato di nuovo.

## Decisioni del 28/09 con Giovane

1. Il flusso è **in due tempi**. Primo tempo: il pannello di caricamento raccoglie fronte, retro e i due dati che il documento non contiene (recapito telefonico, domicilio); alla chiusura la riga passa a «Verifica in corso». Secondo tempo: quando Youtrust risponde, la riga cambia stato e arriva una notifica.
2. **L'esito si legge nella riga di F1**, non in un pannello: «Verificato» con «Vedi i dati letti», oppure «Esito negativo» con il motivo e «Carica di nuovo il documento».
3. **I dati letti non si modificano.** Il riepilogo è in sola lettura e porta «Segnala un dato sbagliato»: la segnalazione arriva al team, che controlla sull'immagine del documento e corregge prima che il dato entri nel contratto. Niente nuovo caricamento, quindi nessun nuovo uso delle API di Youtrust, e niente refusi introdotti dall'utente. È lo stesso canale delle richieste di modifica alla bozza del contratto.
4. Il documento di chi è registrato sta nella stessa riga di F1.

## Tavole

**F1, desktop e mobile.**

| Tavola | Desktop | Mobile |
|---|---|---|
| F1 · Persone e documenti (Venditore) | `4501:189580` | `4501:190002` |
| F1 · Persone e documenti (Acquirente) | `4501:189722` | `4501:190114` |
| F1b · Documenti completi (Venditore) | `4501:189865` | `4501:190227` |

- Stati del documento: Da caricare (orologio), Verifica in corso (loader), Verificato (spunta), Esito negativo (Danger). Esce «Email inviata».
- Esito negativo: motivo («Il documento risulta scaduto: caricane uno valido.») e un solo rimedio, «Carica di nuovo il documento», più «Rimuovi».
- «Vedi i dati letti» sulle righe verificate **della propria parte**: Marco nella vista Venditore, Giulia in quella Acquirente, Marco ed Elena in F1b. L'altra parte vede solo l'esito.
- Helper di «Aggiungi una persona»: «Il documento d'identità lo carichi tu, nella riga della persona, e lo verifichiamo con Youtrust. Alla persona arriva l'informativa privacy da leggere e, quando il contratto è pronto, il link per firmarlo.»
- «Vai al contratto» si sblocca quando i quattro documenti sono verificati.

**Pannelli e fogli.**

| Schermata | Desktop | Mobile |
|---|---|---|
| Carica il documento di Elena (con i due dati mancanti) | `4435:175543` | `4456:183973` |
| Dati letti dal documento di Elena (sola lettura, da «Vedi i dati letti») | `4435:175577` | `4456:184008` |
| Segnala un dato sbagliato | `4675:165432` | `4675:165558` |

- Il contatore «Passaggio n di 3» è caduto: l'occhiello dice solo di chi è il documento.
- Sotto il bottone «Carica il documento»: «Inviamo il documento a Youtrust per la verifica. L'esito non è immediato: ti avvisiamo quando arriva e lo trovi nella riga di Elena.»
- Il riepilogo ha il badge «Verificato» con la data della verifica, gli otto dati letti e i due dati aggiunti al caricamento, tutti in sola lettura, e in fondo «Segnala un dato sbagliato».
- La segnalazione chiede quale dato (tendina fra i dati letti) e come dovrebbe essere, con la nota «Non serve caricare di nuovo il documento».
- Su mobile il foglio di caricamento supera l'altezza utile: il corpo scorre, intestazione e azioni restano fisse.

**Archivio** (sezione `4501:189579`): le F1 del 25/09 con prefisso «ARCHIVIO 25/09», il pannello e il foglio «Esito negativo» con prefisso «ARCHIVIO 28/09».

## Punti aperti

- **Cosa sblocca «Vai al contratto».** Se la firma su Youtrust verifica di nuovo l'identità di tutti, il documento in piattaforma serve ai dati del contratto e all'antiriciclaggio. Va chiarito con lo sviluppo se il blocco resta sull'esito della verifica o basta il caricamento.
- **Tempi dell'esito**: nessun numero in pagina finché lo sviluppo non ne dà uno.
- **Notifica dell'esito**: canale e categoria, da agganciare alla tassonomia IMP (vedi `avvisi-trattativa-e-tavola-acquirente-28-09.md`).
- **Chi gestisce le segnalazioni** sui dati letti e in che tempi: da confermare con il cliente.
- **Scadenza del documento del venditore**: il confronto automatico con la data del rogito resta da valutare con lo sviluppo.

## Documenti da correggere

`claude/coerenza-firma-verifica-25-09.md` e `claude/ui-pg3-v2-feedback-20-09.md` descrivono F1 e pannelli nello stato precedente.
