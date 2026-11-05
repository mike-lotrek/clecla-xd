# Trattativa · risposte del cliente del 22/10 e decisioni della call del 21/10

Due fonti, lette insieme:

- le risposte scritte del cliente alle 12 domande sull’epica Trattativa (inviate il 20/10);
- il resoconto delle decisioni della call del 21/10, inviato al cliente, che precisa date, tabella dei tempi, terreno agricolo e modifica delle dichiarazioni.

Dove le due fonti si toccano, vale il resoconto della call, che è più recente e più preciso.

File «Cleclà | UI», Sprint 4 «🚧 UI Layouts – WIP» (44:983). Backup prima delle modifiche del 22/10: pagina «💿 UI Layouts – Backup 22.10» (6036:20).

## Date e scadenze: le conclusioni

**Decisione della call.** In trattativa le parti ragionano in mesi («3 mesi dal preliminare»). Nel contratto preliminare le scadenze diventano date certe (giorno, mese, anno), calcolate dalla data della firma. Tra la chiusura della trattativa e la firma può passare anche un mese: così non si fissano date che a quel punto non hanno più senso.

**Dalle risposte scritte, ancora valido:**

- nel contratto la data è un termine «entro il»: le parti possono fare il rogito prima;
- ogni condizione sospensiva deve avverarsi almeno 30 giorni prima del rogito (art. 7);
- i mesi delle condizioni servono a non fissare un rogito troppo vicino: rogito non prima di [mesi della condizione] + 1 mese per il notaio. Esempi: mutuo 3 + 1; mutuo e sanatoria insieme 8 + 1, perché la banca aspetta la sanatoria e le due condizioni hanno la stessa scadenza;
- la prelazione agraria rientra nei 3 mesi + 1: il giorno dopo la firma il venditore consegna il documento a chi ha diritto, che ha al massimo 30 giorni per rispondere; l’esito va indicato entro 30 giorni prima del rogito.

**Come lo traduco nelle tavole.**

- **Data del rogito**: si sceglie da un elenco di durate, «N mesi dalla firma del preliminare». Le durate più corte del minimo (condizione più lunga + 1 mese) non si possono scegliere.
- **Data di consegna delle chiavi**: «Coincide con il rogito» oppure «N mesi dopo il rogito».
- **Scadenze delle condizioni**: restano relative, come oggi («entro 3 mesi dalla firma del preliminare»). Il campo di A-P1 «Entro quando arriva la delibera del mutuo?» resta.
- **Righe, riepilogo e T4**: i valori del rogito e della consegna passano da date a durate.
- **Preparazione alla firma e Finalizzazione**: date certe, calcolate dalla firma.

Questo supera la conclusione scritta prima della call («date picker con data minima»): in trattativa non si sceglie una data di calendario.

**Supporto alla scelta (call).** La tabella dei tempi della Guida (punto 4) diventa visibile quando l’utente sceglie le scadenze, già filtrata sulle condizioni dichiarate (per esempio solo la riga del mutuo). Da valutare anche nella lettura del contratto, con una stima delle date reali.

## Applicato sulle tavole il 22/10 · date

Tabella provvisoria, dalle risposte scritte: mutuo 3 mesi; vendita di un immobile 6; sanatoria 6; mutuo e sanatoria insieme 8; prelazione agraria 3; nessuna condizione 3; più 1 mese per il notaio; combinazioni non indicate = la più lunga. Segnata «da confermare» in nota.

- **Valori nell’esempio** (trattativa con mutuo di Giulia e sanatoria di Marco, quindi rogito non prima di 9 mesi):
  - proposta di Giulia e rogito concordato: 15/06/2027 → «9 mesi dalla firma del preliminare»;
  - controproposta di Marco: 15/09/2027 → «12 mesi dalla firma del preliminare»;
  - consegna: 15/07/2027 e 15/10/2027 → «1 mese dopo il rogito».

  Sostituiti in 40 tavole (righe, storico, riepilogo, T3b, T4, modali, variante con terreno), 120 occorrenze, con gli stili del testo conservati. Le date del listing (annullamenti del 2026) restano.
- **Modali, desktop e mobile**:
  - A-P2 (proposta dell’acquirente) e P3 (controproposta del venditore): il campo diventa un select con chevron; sotto c’è la tabella «Tempi minimi per le vostre condizioni», filtrata. A-P2: mutuo 3 mesi, notaio 1, rogito non prima di 4 mesi dalla firma, con la riga «Marco Ferrero può dichiararne altre». P3: mutuo e sanatoria insieme 8 mesi, notaio 1, rogito non prima di 9 mesi. In fondo: «Nel contratto preliminare il rogito diventa una data precisa, calcolata dalla firma: è il termine entro cui farlo, anche prima se siete pronti. Le condizioni devono avverarsi almeno 30 giorni prima.» In P3 l’etichetta «La tua data» diventa «La tua proposta».
  - P4 (consegna): opzioni «Coincide con il rogito» e «Dopo il rogito» («Da scegliere qui sotto: 1, 2 o 3 mesi dopo il rogito»), campo «Quanto dopo il rogito» come select.
  - R4 (risposta sulla consegna): «Accetta la proposta»; testo «Un mese dopo il rogito. Nel contratto preliminare diventa una data, calcolata dalla firma.»
  - A-P1 e A-P1t: scadenza del mutuo come select, con «Il rogito si fissa almeno un mese dopo».
- **Stato alternativo** sotto P3 desktop: elenco delle durate aperto, con 4–8 mesi non disponibili, 9 come minimo, 12 selezionata.
- **Note** sotto P3 (tempi provvisori; scadenze insieme di mutuo e sanatoria) e sotto A-P2 (tempi provvisori).

Restano da fare: i fondi PNG delle modali mostrano ancora le date vecchie (e la breadcrumb «I miei immobili»); la tabella della Guida (punto 4) va allineata quando il cliente conferma i valori.

## Prezzo

- **Media in stallo**: la propone il sistema, automaticamente.
- **Media con soli rifiuti**: si usa il prezzo dell’annuncio.
- **Rifiuto al primo turno**: il resto della risposta (date e dichiarazioni) parte comunque.
- **Offerta minima**: nessun limite. Nessuna modifica alle tavole.

## Applicato sulle tavole il 29/10 · stallo sul prezzo

Il modello passa da «Cleclà suggerisce, una parte propone» a «il sistema propone, le parti accettano». Due stati per ruolo, desktop e mobile.

Vista venditore (Venditore fase 2):

- **T2b · Stallo · Cleclà propone la media**. Riga Prezzo: valore € 270.000, «Proposta da Cleclà, oggi · media fra la tua controproposta (€ 275.000) e l’ultima proposta di Giulia Rossi (€ 265.000)», badge «Media proposta». Alert: «Vi siete fermati sul prezzo: vi proponiamo la media» e «Dopo due proposte senza accordo, Cleclà propone a entrambi la media fra le vostre ultime cifre: € 275.000 (tu) e € 265.000 (Giulia Rossi). Se l’accettate tutti e due, il prezzo è concordato a € 270.000. Puoi anche continuare a trattare con una nuova proposta.» Azioni: «Accetta € 270.000» (era «Proponi € 270.000») e «Continua a trattare». Stepper: «Media proposta · tocca a entrambi»; su mobile la barra dice «Tocca a entrambi: prezzo». Proposte nello storico: 5.
- **T2c · Stallo · hai accettato la media, in attesa di Giulia**. Prima era «la media è sul tavolo», proposta da Giulia su suggerimento di Cleclà. Ora: «Proposta da Cleclà, ieri · media fra € 275.000 e € 265.000 · accettata da te oggi», badge «In attesa di Giulia Rossi», niente «Rispondi», riga senza bordo arancione, stepper «In attesa di Giulia Rossi». Su mobile la barra sticky è nascosta perché non c’è un’azione.

Vista acquirente (Acquirente fase 2, al posto del segnaposto), clonate da T3 con la riga Prezzo di T2b:

- **T3s · Stallo · Cleclà propone la media (Acquirente)**: «Proposta da Cleclà, oggi · media fra la tua ultima proposta (€ 265.000) e la controproposta di Marco Ferrero (€ 275.000)», stesso alert con le cifre dal punto di vista di Giulia, «Accetta € 270.000» e «Continua a trattare». Stepper «Media proposta · tocca a entrambi»; su mobile barra «Tocca a entrambi: prezzo» e sticky «Accetta € 270.000».
- **T3s · Stallo · Marco ha accettato la media, tocca a te (Acquirente)**: specchio di T2c. «Proposta da Cleclà, ieri · media fra € 265.000 e € 275.000 · accettata da Marco Ferrero oggi», badge «Tocca a te», alert «Marco Ferrero ha accettato la media» con «Se l’accetti anche tu, il prezzo è concordato a € 270.000 e la trattativa passa agli altri punti». Stepper e barra «Tocca a te».

Note: sotto T2b «STALLO» (regola, e la verifica di «Cleclà propone» con il copy approvato «Non siamo il terzo attore della compravendita», §15.7); sotto T2c e sotto la seconda T3s «DA CONFERMARE» (accettazione di entrambi, cosa succede se una parte rifiuta o fa una nuova proposta); sotto la prima T3s «VISTA ACQUIRENTE DELLO STALLO». Chiuse e riscritte come regole: «media con soli rifiuti» (prezzo dell’annuncio) e «rifiuto al primo turno» (il resto parte comunque). Panoramica: il box tratteggiato diventa «T3s · media proposta, vista acquirente».

## Terreno agricolo (call)

Il valore del terreno lo calcola Cleclà con i VAM (valori agricoli medi) quando redige il preliminare, e lo scorpora dal prezzo totale concordato. Se la prelazione viene esercitata, il prezzo scende esattamente di quel valore; il documento per chi ha la prelazione lo contiene. Le parti possono chiederne la correzione quando leggono la bozza. Il flusso della trattativa resta invariato.

Allineato il 29/10 nella sezione della variante:

- la nota sul prezzo diventa «PREZZO DEL TERRENO» (VAM, scorporo, correzione sulla bozza, nessuna cifra in trattativa);
- la nota sui tempi diventa «TEMPI DELLA PRELAZIONE» (3 mesi + 1, 30 giorni per rispondere, esito almeno 30 giorni prima del rogito);
- la scadenza della condizione passa da «[da confermare]» a «entro 3 mesi dalla firma del preliminare», nelle dichiarazioni e nel riepilogo di T1t, T3t, T2t, desktop e mobile;
- la riga sotto la condizione dice «Il giorno dopo la firma del preliminare […] avvisa chi ha diritto di prelazione, che ha 30 giorni per rispondere, e […] comunica l’esito».

## Chiusura e annullamento

- **Trattative bloccate (#276)**: si bloccano quando entrambi confermano, perché partono preliminare, verifica dei documenti e attività di Cleclà. Si riaprono se l’accordo non va a buon fine.
- **Riapertura dopo un annullamento (#277)**: può chiederla sia il venditore sia l’acquirente, per qualsiasi motivo. L’altra parte vede un messaggio come «Il venditore vorrebbe riaprire la trattativa».
- **Modifica di una dichiarazione**: possibile fino al preliminare (call). Per esempio un acquirente che non ha più bisogno del mutuo. Cambia solo quella condizione, con effetto sulla data del rogito; la trattativa non riparte da capo.

## Applicato sulle tavole il 29/10 · chiusura e annullamento

Stesso schema per i tre stati di pagina: un blocco in cima con titolo, testo e azione (bordo arancione quando c’è un’azione), il resto della pagina in sola lettura (sezioni al 45% di opacità, bottoni nascosti, «Annulla la trattativa» tolto), intestazione dello stepper con lo stato, su mobile barra di percorso e barra sticky aggiornate.

- **X2 · Trattativa annullata dal venditore (Acquirente)**, desktop e mobile, al posto del segnaposto in Acquirente fase 3. Blocco «Marco Ferrero ha annullato la trattativa»: «L’ha annullata il 28/10. Le proposte e le dichiarazioni fatte finora decadono: nessuno dei due è vincolato. Se cambi idea, puoi chiedere a Marco Ferrero di riaprirla.», CTA «Chiedi di riaprire la trattativa». Stato alternativo sotto: «Hai chiesto di riaprire la trattativa». Nota «DA CONFERMARE · RIAPERTURA (#277)».
- **X3 · Trattativa bloccata per un altro accordo (Acquirente, #276)**, desktop e mobile, al posto del segnaposto. Blocco «Marco Ferrero ha confermato un accordo con un altro acquirente»: la trattativa è bloccata, se l’accordo non va a buon fine si riapre e arriva un avviso. Nessuna azione. Stato alternativo sotto: «La trattativa è di nuovo aperta», con «Torna alla trattativa». Nota «#276».
- **X2 · Richiesta di riapertura ricevuta (Venditore, #277)**, desktop e mobile, in Venditore fase 3 dopo X1. Blocco «Giulia Rossi vorrebbe riaprire la trattativa», con «Riapri la trattativa» e «Lascia chiusa». Stato alternativo sotto: «Giulia Rossi ha annullato la trattativa», con «Chiedi di riaprire la trattativa» (il caso dell’annullamento chiesto dall’acquirente, che mancava). Nota «RIAPERTURA (#277)».
- **X1 · Annulla la trattativa**, desktop e mobile: la frase finale diventa «Se in futuro uno dei due cambia idea, può chiedere all’altro di riaprirla.»
- **Modifica di una dichiarazione**: link «Modifica» sulle righe di «Le tue dichiarazioni» in T3 (desktop e mobile); modale e foglio **A-M1 · Modifica una dichiarazione (Acquirente)** in Acquirente fase 2. Esempio: il mutuo passa da Sì a No. Riquadro «Cosa cambia se rispondi No»: la condizione sul mutuo esce dal contratto preliminare, il rogito minimo passa da 9 a 7 mesi, il rogito concordato (9 mesi) resta valido, Marco Ferrero riceve un avviso. CTA «Salva la modifica», link «Annulla». Nota «MODIFICA DELLE DICHIARAZIONI».
- **Note aggiornate**: #276 sotto T4 (decisione presa), #277 e «annullata dall’acquirente» sotto X1.
- **Panoramica**: i box tratteggiati diventano «X2 · annullata dal venditore · richiesta di riapertura», «X3 · bloccata da un altro accordo (#276)» e, lato venditore, «X2 · richiesta di riapertura ricevuta · annullata dall’acquirente».

Il fondo PNG della modale A-M1 desktop è quello della Bacheca, ereditato da A-P1: da rigenerare con gli altri.

## Contratto

- **Penale per ritardata consegna**: non compare in trattativa. Sta solo nel contratto e decorre dal giorno dopo la data di consegna concordata.

## Discrepanze da segnalare

- **Tabella dei tempi della Guida (punto 4)** contro le risposte del 22/10. La Guida, dal feedback del 20/09, dice: mutuo 3, vendita della casa 6, sanatoria 6, sanatoria e mutuo 9, nessuna condizione 2. Le risposte dicono mutuo 3 + 1 = 4 al rogito, mutuo e sanatoria 8 + 1 = 9 al rogito. Nella Guida «mutuo 3» sembra il tempo della condizione, «sanatoria e mutuo 9» il tempo del rogito. Serve una sola lettura.
- **Documento «Come funziona la trattativa»**: mutuo «non meno di 2 mesi», nessuna condizione 3 mesi, più condizioni «il tempo più lungo». Va allineato. Al §8 dice ancora che Cleclà «suggerisce» un prezzo di accordo.
- **Scadenze insieme**: il cliente dice che mutuo e sanatoria insieme hanno la stessa scadenza (8 mesi); in piattaforma le scadenze si dichiarano una per volta (3 e 6).
- **Annullamento e riapertura**: X1 dice che con l’annullamento proposte e dichiarazioni decadono; con la riapertura non è chiaro se tornano valide.
- **Glossario**: «VAM»; la formula «N mesi dalla firma del preliminare» (nella call «3 mesi dal preliminare»: in pagina ho usato la forma lunga, già in uso per le condizioni); il nome della condizione sul terreno resta da confermare; voci nuove «Cleclà propone la media», «Media proposta», «Trattativa bloccata», «Chiedi di riaprire la trattativa», «Lascia chiusa».

## Domande che restano per il cliente

1. **Valori della tabella dei tempi**: la Guida indica il tempo della condizione o quello del rogito? Servono anche le combinazioni che mancano: mutuo con vendita, vendita con sanatoria, tutte e tre.
2. **Da che data si calcolano le date del contratto.** Il contratto si genera prima della firma e i firmatari possono firmare in giorni diversi. Si calcola dal giorno in cui si apre la firma, o dall’ultima firma con un contratto che riporta le durate?
3. **Media proposta dal sistema**: nelle tavole la devono accettare entrambi (ipotesi). Se una parte la rifiuta o fa una nuova proposta, la trattativa riprende dalle ultime cifre?
4. **Riapertura dopo un annullamento**: l’altra parte sceglie fra «Riapri la trattativa» e «Lascia chiusa» (ipotesi)? Riaprendo, proposte e dichiarazioni di prima tornano valide o si riparte da zero?
5. **Modifica di una dichiarazione**: se la nuova condizione richiede più tempo del rogito già concordato (per esempio si aggiunge il mutuo), la data del rogito torna da concordare?
6. **Trattative riaperte dopo un accordo saltato**: tornano allo stato in cui erano, con le proposte già fatte?
7. **Scadenze di mutuo e sanatoria insieme**: la piattaforma le allinea da sola alla stessa scadenza?

## Lavoro sulle tavole che ne segue

1. ~~Date: rogito e consegna come durate~~ fatto il 22/10.
2. ~~Note chiuse: P1, T2b, terreno (prezzo e tempi)~~ fatto il 29/10.
3. ~~Stallo: T2b/T2c con la media proposta dal sistema~~ fatto il 29/10, con l’accettazione di entrambi come ipotesi (domanda 3).
4. ~~Chiusura e annullamento: annullata, bloccata, richiesta di riapertura, modifica di una dichiarazione~~ fatto il 29/10.
5. ~~Vista acquirente dello stallo~~ fatto il 29/10 (due tavole T3s, desktop e mobile).
6. Da valutare: tabella dei tempi con stima delle date nella lettura del contratto.
7. Fondi PNG delle modali e tabella della Guida da rigenerare.
