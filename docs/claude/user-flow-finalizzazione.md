# User flow · Ufficializzazione del preliminare e Finalizzazione

Fonte: board FigJam «[EXT] Cleclà | User Flows» (`DXvZbuexjok4HOsLSuLiEK`), tavola «REVIEW 16/03», nodo `388:2166`. Letta il 29/09/2026.

La board è datata 16/03, quindi è precedente al feedback del cliente del 20/09. Dove le due cose divergono lo segnalo in fondo, senza correggere il flow.

## Come è organizzata la board

Tabella a tre righe (Venditori, Acquirenti, Team Cleclà backoffice) e due colonne: «Ufficializzazione contratto preliminare» e «Finalizzazione». Le sequenze sui due rail Venditore e Acquirente sono speculari: un nodo ripetuto sui due rail è lo stesso passaggio eseguito da ciascuna parte.

Legenda: ellisse = entry/end point · rombo = decisione (utente o sistema) · parallelogramma = azione utente · cilindro = database · rettangolo = schermata · fumetto = nota · linea piena = percorso primario · linea tratteggiata = percorso secondario.

La colonna Finalizzazione è divisa in cinque rami, con un titolo ciascuno:

| Ramo | Titolo sulla board |
|---|---|
| B | Recesso (può avvenire in qualsiasi momento del flusso) |
| C | Inadempienza (può avvenire in qualsiasi momento del flusso) |
| D | Proroga scadenza |
| E | Inefficacia |
| F | Avveramento |

La numerazione A–F e i numeri di passo sono miei, per poterli citare. La PG Finalizzazione usa gli stessi riferimenti.

## A · Ufficializzazione del preliminare

Ingresso: **Contratto preliminare** (entry point). Da qui tre uscite per rail.

1. **Seleziona parte del contratto** → **Riapri trattativa** → torna al **Flusso trattativa**. Ramo di riapertura, fuori perimetro Finalizzazione.
2. **Firma in quest'ordine**: adeguata verifica della clientela, privacy, contratto preliminare (tutti i proprietari).
3. Sistema: settaggio documenti da firmare e destinatario → invio richiesta firma digitale (email) → *l'utente ha accesso alla mail?* NO → richiesta di reinvio → email · SI → email → richiesta verifica identità → input info (Paese, documento) → foto documento → video o selfie → *identità confermata?* NO → torna all'input info · SI → salvataggio progress → accetta utilizzo della firma digitale → legge e firma contratto, privacy e antiriciclaggio.
4. Schermata **Contratto firmato da tutte le parti (stand-by)**.
5. Sistema: *sono presenti condizioni sospensive?*
   - **NO** → invio mail con fattura Cleclà → Venditore: pagamento fee Cleclà → (se bonifico) caricamento ricevuta. Acquirente: pagamento registrazione contratto (entro 30 gg) → pagamento fee Cleclà → (se bonifico) caricamento ricevuta.
   - **SI** → Acquirente: pagamento registrazione contratto (entro 30 gg) → (se bonifico) caricamento ricevuta.
6. Sistema: invio mail con contratto firmato a tutte le parti → notifica pagamento avvenuto.
7. Team: **registrazione contratto su AdE** → conferma caricamento → carica ricevuta di registrazione.
8. Sistema: notifica registrazione avvenuta (a entrambi) → salvataggio contratto negli archivi.
9. Schermata **Pagina contratto · stato: attivo**.

## Dalla pagina contratto attiva

Dalla schermata del passo A.9 partono tre connettori per rail: recesso (B), inadempienza (C) e la decisione di sistema *sono presenti condizioni sospensive?*

- **NO** → **Paga la fee Cleclà** (F.4).
- **SI** → notifica 30 giorni prima della scadenza (D.1) e, in parallelo, **seleziona condizione da lista** (E.1).

## B · Recesso

1. User action: **Recesso · richiedi annullamento contratto**.
2. Sistema: notifica richiesta al team.
3. Team: **attiva flusso di recesso**.
4. Sistema: *condizioni sospensive avverate?* Tre uscite, tutte verso lo stesso pagamento: «SI, TUTTE», «NON CI SONO C. SOSP.», «ALTRO».
5. User action: **pagamento registrazione recesso** (200 € + 16 € + 3% del 5% del prezzo dell'immobile), bonifico o digitale. Nota: pagamenti separati.
6. User action: carica ricevuta bonifico (nota: solo se pagamento tramite bonifico).
7. Sistema: generazione documento di recesso.
8. User action: **firma FEQ**.
9. Sistema: invio documento a Cleclà e alla controparte.
10. Controparte: notifica richiesta → **inserisci IBAN per pagamento multa penitenziale**. Sulla board il nodo sta sul rail di chi esce, non di chi riceve (vedi punto 41 della PG).
11. User action: **pagamento multa penitenziale** (bonifico).
12. User action: carica ricevuta bonifico.
13. Sistema: notifica pagamento eseguito → controparte: **conferma ricezione pagamento**.
14. Team: **registrazione recesso sul portale AdE**.
15. Sistema: archiviazione contratto annullato.
16. Sistema: **riattiva annuncio e trattative in stand-by**.

## C · Inadempienza

1. User action: **Inadempienza · comunica sospetta inadempienza della controparte** (rail Venditore) o **richiedi annullamento contratto** (rail Acquirente: l'etichetta diverge fra i due rail). Lo stesso nodo è raggiunto anche dall'esito «SCADUTA» della decisione *condizione avverata?* del ramo E.
2. User action: seleziona motivazione da lista.
3. Sistema: generazione automatica documento di inadempienza.
4. Sistema: invio documento alla controparte e a Cleclà.
5. Decisione: **richiedi mediazione di Cleclà?**
   - **Entrambi accettano** → notifica richiesta → team: attiva flusso di inadempienza → contratto in stand-by → **gestione flusso di inadempienza con mediazione** → *accordo trovato?*
     - **SI, continua** → team: caricamento e invio accordo → firma FEQ di entrambi → salvataggio accordo → riattivazione del contratto in essere.
     - **SI, risolvi** → la parte inadempiente paga la clausola penale (vai a C.6).
     - **NO** → azione giudiziaria → archiviazione documento di sentenza o accordo avvocato → *inadempienza confermata?*
       - **NO** → riattiva annuncio e trattative in stand-by (vedi punto 42 della PG: in contraddizione con «contratto valido»).
       - **SI** → *chi è la parte inadempiente?* Venditore o Acquirente → vai a C.8 sul rail corrispondente.
   - **NO** → team: attiva flusso di inadempienza → contratto in stand-by → azione giudiziaria (stesso seguito del ramo NO sopra).
6. La parte inadempiente paga la clausola penale: inserisci IBAN (sul rail della parte che paga) → pagamento clausola penale → carica ricevuta bonifico.
7. Sistema: notifica richiesta → controparte: conferma ricezione pagamento.
8. Sistema: *condizioni sospensive avverate?* «SI, TUTTE» o «NON CI SONO C. SOSP.» → pagamento registrazione inadempienza (200 € + 16 € + 3% del 5%) · «ALTRO» → pagamento penale + registrazione inadempienza (stessa formula). Nota: pagamenti separati.
9. User action: carica ricevuta bonifico (solo se bonifico).
10. Sistema: generazione e invio risoluzione → firma FEQ di entrambi → notifica firma.
11. Team: registra risoluzione su AdE.
12. Sistema: archiviazione contratto annullato → riattiva annuncio e trattative in stand-by.

## D · Proroga scadenza

1. Sistema: **notifica 30 giorni prima della scadenza**.
2. Decisione dell'utente: **MANTIENI** → torna a seleziona condizione da lista (E.1) · **PROROGA** → inserisci nuova scadenza.
3. Sistema: notifica richiesta alla controparte.
4. Controparte: **accetta nuova scadenza?** SI → sistema: aggiorna scadenze sul contratto → torna a *sono presenti condizioni sospensive?* · NO → torna a *sono presenti condizioni sospensive?*

## E · Esito di una condizione (inefficacia)

1. User action: **seleziona condizione da lista**.
2. Decisione: **condizione avverata?** SI → ramo F · SCADUTA → ramo C (inadempienza) · NO → seleziona condizione da lista → *condizione avverata?* (secondo controllo).
3. Sul NO: **per regolarità e prelazione** carica documento · **per mutuo** seleziona condizione da lista.
4. Sistema: generazione automatica autocertificazione.
5. User action: **firma FEA**.
6. Database: salva clausola come non avverata.
7. User action: **segnala inefficacia contratto**.
8. Sistema: **risoluzione automatica contratto** → notifica inefficacia a entrambi.
9. Sistema: riattiva annuncio e trattative in stand-by.
10. Database: archiviazione contratto «inefficace».

## F · Avveramento e chiusura

1. Database: salva clausola come avverata.
2. User action: **allega documento (se necessario)**.
3. Sistema: *tutte le condizioni risolte?* SI → notifica compravendita avvenuta.
4. Schermata **Paga la fee Cleclà** → pagamento fee (entro TOT gg).
5. Sistema: chiusura definitiva annuncio immobile e trattative sospese → archiviazione profilo immobile come «venduto».
6. Sistema: mail di recap con contatto diretto dell'altra parte (al venditore quello dell'acquirente, all'acquirente quello del venditore).
7. End point: **Compravendita avvenuta e next steps** → schermata **Trova un notaio**.

## Cosa la board non dice

- Nessun nodo per la notifica il giorno della scadenza (la chiede l'MVP riga 37).
- Nessun nodo per il controllo finale della documentazione (MVP riga 35).
- Chi paga la registrazione del recesso e dell'inadempimento.
- Il ramo «SI» di *tutte le condizioni risolte?* esiste; il ramo «NO» non ha connettore: si presume che torni ad attendere la condizione successiva.
- Senza condizioni sospensive la fee compare due volte: pagata in A.5 insieme alla registrazione, e di nuovo come «Paga la fee Cleclà» in uscita dalla pagina contratto attiva.

## Differenze con le decisioni successive al 16/03

Segnalate, non corrette nel flow.

- **Registrazione.** La board dice «entro 30 gg» a carico dell'acquirente. Dopo il 20/09: 5 giorni dalla fattura per pagare, 30 giorni dall'ultima firma per registrare, a carico di Cleclà; il contratto non si annulla se la registrazione arriva in ritardo.
- **Condizioni sospensive.** La board cita solo regolarità, prelazione e mutuo nei rami di inefficacia. Il modello del 20/09 ne ha quattro: mutuo, vendita dell'immobile dell'acquirente, acquisto congiunto di immobile e terreno agricolo, regolarità urbanistica e conformità catastale.
- **Terminologia.** La board usa «inadempienza», «clausola» per condizione sospensiva e «compravendita avvenuta» per l'efficacia del preliminare. Glossario e decisioni bloccate: «inadempimento», «condizioni sospensive»; «Contratto efficace» è la proposta della PG (punto 29).
- **Firma.** «Adeguata verifica della clientela» e verifica identità via video/selfie: dopo il 25/09 la verifica è di Youtrust e l'identificazione antiriciclaggio si chiama «identificazione della clientela ai fini dell'antiriciclaggio».
