# Rework PG4 dopo il feedback del 30/09

09/10/2026 · file «Cleclà | UI», Sprint 4 «🚧 UI Layouts – WIP» (44:983), sezioni `PG4 · Pagamento registrazione v2` desktop (4456:179479) e mobile (4456:184264). Backup nella pagina «💿 UI Layouts – Backup 08.10» (5424:8011): 5481:8106 desktop, 5481:8619 mobile.

- #292 · Riga «Passo successivo» di R0: già risolto in un’altra conversazione.
- #284, #285 · Dopo la registrazione i documenti nuovi sono due: ricevuta di registrazione e ricevuta di pagamento delle imposte all’Agenzia delle Entrate. Il contratto preliminare resta quello già firmato da tutti, non esiste un «contratto registrato» da scaricare.
  - R3 (desktop e mobile): «Scarica il contratto registrato» → «Scarica la ricevuta di registrazione»; il secondo bottone diventa «Scarica la ricevuta di pagamento delle imposte». Nota: «Le due ricevute finiscono nella cartella «8. Contratto e pagamenti» dell’archivio dell’immobile, e le vede anche il venditore. Il contratto preliminare non cambia: è quello che avete già firmato tutti.»
  - R2 e R4 (desktop e mobile): bottone disabilitato «Scarica la ricevuta di registrazione», nota «Si attiva quando l’Agenzia delle Entrate registra il contratto preliminare».
  - R2: la tappa «Ricevuta di registrazione e contratto registrato» diventa «Ricevuta di registrazione».
- Resta in R2 la «ricevuta di pagamento» del pagamento della registrazione fatto dall’acquirente: è un documento diverso dalla ricevuta delle imposte. Da confermare con il cliente se sono la stessa cosa.

## R1b · Pagamento con bonifico (15/10)

Il ramo bonifico di R1 si fermava alla riga del metodo; lo user flow prevede «(se bonifico) caricamento ricevuta». Ora è disegnato riusando il blocco di D-C1b della Finalizzazione (caricamento in pagina, nessuna modale). Sezione «Acquirente · 5 · Registrazione del contratto preliminare» (5785:25289).

- Desktop `5809:14789` · D-1 / R1b: radio su Bonifico; card «Paga con un bonifico» con importo 216,00 € senza IVA, intestatario e IBAN segnaposto, causale «Registrazione · fattura n. 2026/0417 · Giulia Rossi», «Copia le coordinate», zona di caricamento «Quietanza del bonifico», CTA «Ho eseguito il bonifico» disabilitata finché non c’è il file. Il bottone del footer «Paga 216,00 €» è nascosto: con il bonifico l’azione sta nella card.
- Stati alternativi sotto la tavola, clonati da D-C1b e adattati: quietanza caricata, file non valido, dopo «Ho eseguito il bonifico» (badge «Pagamento in verifica»), la quietanza non corrisponde all’importo della fattura, bonifico non ancora accreditato dopo [SLA] con il termine del 03/10/2026.
- Mobile `5811:8331` · M-1 / R1b: stessa card con le righe impilate; «Ho eseguito il bonifico» disabilitata nella barra sticky, con «Si attiva quando hai caricato la quietanza.». Gli stati alternativi esistono solo in desktop, come in Finalizzazione.
- Panoramica: box «R1b · bonifico scelto» fra R1 e R2.

Differenze rispetto alla provvigione: la fattura esiste già, quindi la quietanza collega il bonifico alla fattura e non fa partire la fattura; il pagamento sblocca il deposito all’Agenzia delle Entrate, non i contatti.

Punti aperti (in nota sotto la tavola):

- il deposito parte dalla quietanza o dall’accredito (in pagina: accredito); cosa succede se il bonifico arriva dopo il 03/10/2026;
- glossario: «quietanza» (D-C1b, elenco documenti approvato) contro «ricevuta» (user flow, Uscita dal contratto). Serve un termine unico.
