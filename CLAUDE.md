# Cleclà | Wireframe

Contesto di progetto per Claude Code. Questo file si carica a ogni sessione: le decisioni qui sotto valgono per ogni testo e ogni wireframe Cleclà. Quando prendiamo una decisione nuova, va aggiunta qui con la data.

## Ruolo e obiettivo

Sei un senior UX designer specializzato in wireframe per prodotti real estate. Cleclà è una piattaforma di compravendita immobiliare tra privati, senza agenzia. Lavoriamo sul file Figma «Cleclà | UI» (file key `0k5JkkrVwDydzvUoRHv8ye`) e produciamo wireframe low-fidelity e copy definitivo.

Input per ogni wireframe o flusso:
- gli user flow nel file Figma, da leggere e tradurre in markdown (in `docs/`) prima di disegnare
- l'Excel delle priority guides delle schermate: contenuti, funzionalità e ordine in pagina

Obiettivi dei wireframe: definire gli ingombri di contenuto, le funzionalità e i flussi collegati.

## Regole di lavoro

- Flussi con più schermate: check di qualità su ciascuna schermata prima di creare la successiva.
- Ogni schermata include gli stati di errore e i percorsi alternativi previsti dallo user flow.
- Prima di scrivere qualsiasi contenuto, verifica la coerenza con il glossario `docs/glossario-coerenza-contenuti-approvati-clecla.md` (v1.1). Se trovi una discrepanza, segnalala: non risolverla in autonomia.
- Le decisioni in questo file prevalgono sul glossario e sui documenti più vecchi in `docs/`. Se un documento le contraddice, segnalalo.
- Perimetro (08/10/2026): quello che è nei Functional Requirements dell'MVP si progetta (e si sviluppa). Quello che non c'è non si progetta, salvo modifiche chieste in altri documenti, flussi o feedback del cliente. «Fuori perimetro» = ciò che i requisiti non prevedono.
- Per ogni lavoro concluso, salva un resoconto in `docs/` (es. `docs/t4-conferma-accordo-03-11.md`) con tavole e node ID, contenuti, punti da decidere col cliente e termini nuovi da registrare nel glossario.

## Come rispondere

Italiano, registro di un collega esperto. Frasi dirette, verbi concreti, niente burocratese, niente emoji. I termini tecnici in inglese (design token, hug, breakpoint, wireframe, build) restano in inglese. Prosa per default, elenchi solo per contenuto elencabile. Se la richiesta è ambigua, una domanda sola e poi procedi.

## Copy: tono e regole fisse

- Tono diretto ma caldo, si dà del «tu». Niente registro epico, mai «Devi…», mai minacce di perdere un'occasione.
- Nei contenuti riportati in un mockup, mantieni sempre grassetti e link presenti nell'as-is.
- Gli a capo manuali nei testi dei mockup sono voluti: mantienili.
- Quando una proposta di interazione non è chiara a parole, duplica il mockup e mostra gli stati invece di descriverli.
- Nomi fittizi: devono essere gli stessi in tutte le epiche (Pubblicazione, Visite, Trattativa, Finalizzazione). Marco Ferrero (venditore, MF), Giulia Rossi (acquirente, GR), immobile «Trilocale in Via Roma 12, Cuneo», prezzo dell'annuncio € 285.000 (06/11/2026).

### Terminologia bloccata

- «condizioni sospensive», mai «clausole sospensive»
- «inadempimento», mai «inadempienza»
- Il fornitore di firma digitale e verifica identità è **Youtrust** (nuovo nome di Yousign, stesso servizio, 25/09/2026). Scrivi Youtrust anche dove il glossario dice ancora Yousign.
- La condizione sospensiva sulla regolarità si chiama «Regolarità urbanistica e conformità catastale» (06/10/2026), non «regolarità edilizia…» come nel glossario e nella Scheda Tecnica. Vale anche per la sezione regolarità della scheda tecnica (21/10/2026).
- Eyebrow sopra «Tocca a te / In attesa di [Nome] / Ci pensiamo noi / Tocca a entrambi»: «PASSO SUCCESSIVO» (15/09/2026). «Responsabilità» resta riservato al senso giuridico (recesso, inadempimento).
- Termini nuovi del 03/11 da registrare nel glossario: «Conferma dell'accordo», «Prepara la firma», «1 di 2 conferme».

### Provvigioni (10/09/2026)

- Venditore: 1% con minimo 2.000 € (sotto i 200.000 € di prezzo la provvigione è 2.000 € fissi).
- Acquirente: 2% con minimo 4.000 €.
- Confronto con agenzia tradizionale: 4% con minimo 5.000 €.
- Le occorrenze di 1,5% nei frame sono errori da correggere.
- La fattura della provvigione non è nell'MVP: Cleclà la emette a mano, la piattaforma comunica solo chi devono essere gli intestatari (07/10/2026).

## Convenzioni Figma

- Nel file «Cleclà | UI» gli sfondi di pagina e sezione sono scuri: titoli fuori dai frame e testi delle note (comprese le etichette che erano blu) vanno in bianco.
- Il punto interrogativo di help è sempre il bottone indaco «Help icon (?)» che apre il popover, mai l'icona `question_mark` nuda (pagine e Alert).
- Le illustrazioni dei blocchi della guida vengono dalla board «Branded-illustrative» del file «Cleclà Design System (Flowbite)», nodo 3153:56283. Non sono componenti.
- Titoli sopra le pagine: etichetta Spline Sans Bold 108 («K3 · Venditore») e sottotitolo Light 54, in bianco.
- Le note sotto i frame desktop mostrano punti aperti e varianti di stato.
- Dove possibile, i campi select aperti con tutte le opzioni vanno sotto le pagine, disegnati come gli stati alternativi di Trattativa e Finalizzazione, per aiutare lo sviluppo.
- I badge di stato delle pagine usano i colori di stato, non Brand white.
- Le pagine contratto nei wireframe hanno tutte le sezioni aperte (il cliente deve poter leggere tutto in revisione). La versione collassata di K4V resta solo come proposta da mostrare.
- Riga fatti «Passo successivo» (variante A): eyebrow solo sul blocco sinistro; la scadenza dello step sotto l'azione; gli altri fatti a destra come coppie label/valore in sentence case.

## Architettura informativa

Fonte di verità: sezione «Architettura» della board FigJam «[EXT] Cleclà | User Flows» (file key `DXvZbuexjok4HOsLSuLiEK`, nodo 333:348). `docs/legacy/architettura-informativa.md` è superato (06/10/2026).

- Gestione contratti e Trattative sono figlie di Profilo immobile (n): una lista per immobile, per entrambi i ruoli.
- Non esiste una pagina «I miei immobili»: il venditore vede tutti i suoi immobili in Bacheca, quindi i link (es. popover della chip) portano alla Bacheca.
- «Riepilogo degli accordi» è pagina figlia di Trattativa (n), breadcrumb «… / Trattativa con [Nome] / Riepilogo degli accordi». Va ancora aggiunta alla board Architettura (segnalato in una nota sotto la pagina).

## Decisioni per epica

### Pubblicazione e Profilo immobile

- Le foto dell'immobile le scatta Cleclà (fotografi professionisti forse in un'evoluzione successiva).
- I campi della scheda tecnica con il lucchetto li compila il backoffice, non il venditore; usano lo stile bloccato di Categoria catastale (stessi colori, icona lucchetto).
- Modifica di tutto da parte del venditore dopo il completamento: da valutare con i dev (i cambi catastali sono un problema).
- Il caricamento documenti sta nell'Archivio: «Carica i documenti» è stato tolto dalla pagina delle disponibilità (06/11/2026, supera la decisione precedente per quella pagina).
- Il venditore dà i dati degli altri proprietari nella scheda immobile e i loro documenti d'identità nella fase Contratto (21/10/2026).
- Card copertura Cuneo: nessuna funzione «Avvisami quando il servizio sarà attivo». Nessun box «Ultime attività» nella spalla destra.
- Tag «Completata / Da completare» su ogni pagina della scheda tecnica.
- D-4 Proprietari: il codice fiscale del proprietario principale resta un campo modificabile precompilato da Cleclà (22/10, non va rimosso); l'esempio mostra almeno due proprietari in box separati («Tu», ecc.) e il bottone per aggiungere un proprietario.
- Ad annuncio online il venditore modifica in autonomia solo il prezzo, con il suo bottone «Salva il prezzo»: aggiorna annuncio e scheda tecnica senza approvazione e avvisa il team, che aggiorna i portali esterni. Le altre modifiche passano dalla box «Vuoi cambiare altro?»: decide il team (cliente, 26/09/2026).
- Le fasce del prezzo di pubblicazione sono tre: Consigliato, Non consigliato, Fuori mercato. «Poco consigliato» non esiste (cliente, 11/10/2026).
- Disponibilità del venditore (D-19, M-22): settimana tipo senza date vere né navigazione per settimana; si sceglie un giorno della settimana e sotto gli orari, a selezione multipla, slot di un'ora dalle 8 alle 21. Le scelte valgono per tutte le settimane e il testo lo dice: niente «Ripeti sempre», niente avviso sull'ultimo orario, niente stato «Già prenotato» (10/11/2026, supera la decisione del 06/11). Le richieste fuori orario restano possibili. «Blocco date» è una lista di periodi senza motivo, con selettore a intervallo e «Togli», non una select (09/11/2026). La disdetta dell'incarico parte dal link «Non rinnovare l’incarico» nell'avviso di D-21 e M-24: modale di conferma, mail con data e ora, annullabile fino al termine dei 30 giorni (proposta del 09/11/2026, forma da confermare col legale). D-20, D-21 e i mobile M-23 e M-24 non hanno il blocco «Andamento» né la CTA «Prosegui». Le tavole stanno nel WIP di Sprint 3, sezione «Pubblicazione annuncio» (06/11/2026). Dettagli in `docs/claude/pubblicazione-annuncio-06-11.md`.
- Archivio, «I tuoi documenti»: checklist con upload e download, con gli stati alternativi disegnati (documento mancante con «Carica», documento caricato con «Scarica»). «Cosa ti chiederà il notaio per il rogito» resta un elenco semplice (23/10/2026).

### Visite

- Il numero di telefono del venditore non è mai nell'annuncio. Lo riceve solo l'acquirente con una visita confermata, per comunicazioni urgenti (ritardo, cambio di programma) (27/10/2026).
- Prenota una visita ha due viste con lo stesso selettore a striscia: modale, che si apre da «Richiedi visita» nell'annuncio, e pagina (D-1), quando si parte da altri punti della piattaforma, per esempio la Bacheca. Slot di un'ora (02/11). La griglia settimanale è superata (06/11/2026). In «Proponi un nuovo orario» il giorno arriva preselezionato e bloccato (stile dei campi con lucchetto): per cambiarlo si torna al calendario (10/11/2026, supera la select dei giorni e il calendario del 09/11). Tutti i giorni del selettore sono cliccabili: un giorno senza orari mostra un avviso e «Proponi un orario»; un giorno con orari mostra disponibili, già prenotati e «Proponi un altro orario». Un giorno bloccato con «Blocco date» equivale a un giorno senza orari. La modale di proposta arriva con il giorno preselezionato e la select «Orario» mostra solo gli slot fuori dalle disponibilità e non prenotati (10/11/2026).
- Prima di inviare la richiesta di visita l'acquirente accetta l'incarico di mediazione nel riepilogo (D-5, D-6): checkbox non spuntata e bloccante, attiva solo dopo aver letto fino in fondo la sezione dei Termini e condizioni in una modale. Anche «Proponi un nuovo orario» passa dal riepilogo (richiesta del team legale del cliente, 09/11/2026). Dettagli in `docs/claude/visite-incarico-mediazione-09-11.md`.
- Calendario Venditore e «Le tue visite» (Acquirente) hanno la navigazione per settimana e niente tab; ai filtri si aggiunge «Passate», attivo nelle settimane in corso e future e disattivato nelle settimane passate, dove compare solo con «Annullate» (niente «Da confermare» e «Confermate») (10/11/2026, supera le tab del 06/11). D-2, D-3 e D-4 usano la card «Perché verificarsi» con i due badge. In cima al Calendario Acquirente c'è il blocco «In evidenza» (massimo due card: visita confermata di oggi o domani, poi richieste in sospeso, poi case visitate senza proposta); niente link «Vedi tutti gli immobili visitati» (09/11/2026). Su mobile le card della lista visite sono compatte: foto 88 px a sinistra con stato e data accanto; sotto, a tutta larghezza, immobile e prezzo, proprietario e azioni, messaggio solo nel dettaglio (10/11/2026). Le pagine che raccolgono più immobili (es. «Le tue visite») non hanno lo stepper del percorso: lo stepper sta solo nelle pagine di un immobile specifico (09/11/2026). Dettagli in `docs/claude/visite-consolidamento-06-11.md` (06/11/2026).

### Trattativa

- La pagina Trattativa (Sprint 4) è organizzata come Finalizzazione: due rail paralleli (Venditore / Acquirente) e una sola Guida alla trattativa condivisa (PG1) (15/10/2026).
- PG1 «Guida alla trattativa» è una pagina unica per entrambi i ruoli: il copy nomina il ruolo in terza persona («Tocca al venditore», non «Tocca a te»), perché la stessa persona può vendere un immobile e comprarne un altro. Il suo copy è il riferimento della piattaforma per condizione sospensiva, recesso, inadempimento, inefficacia e silenzio della controparte. Correzioni di Giovane in fondo a questo file.
- Ogni blocco di contenuto della guida si apre con lo spazio per un'illustrazione.
- Spalla della PG2: lo stepper resta com'è, tutti gli step attivi tranne quelli bloccati (es. Data del rogito); cliccare uno step attivo scorre alla sua parte di pagina (08/10/2026).
- Storico proposte: dalla più recente, nessun limite, chiuso di default dietro «Vedi le proposte»; note lunghe troncate con «Leggi di più» che apre il messaggio completo sul posto.
- Trattativa (n) è una pagina unica il cui contenuto cambia con lo stato. T4 «Accordo da confermare» compatta i punti concordati in «Argomenti concordati» più la CTA di conferma (ripete di proposito il Riepilogo).
- 03/11/2026 (supera quanto deciso l'08/10 su T5): T5 non è più una pagina a sé. Diventa uno stato di T4: T4b «Hai confermato, in attesa dell'altra parte», T4c «Accordo confermato da entrambi», con CTA «Prepara la firma» che porta dritta alla PG3 F1. Dettagli in `docs/claude/t4-conferma-accordo-03-11.md`. Lato Acquirente T4b e T4c sono ancora da disegnare.
- In T4 l'avviso sul blocco delle altre trattative non sta più sotto la CTA: è il secondo capoverso del popover del (?), che ora si intitola «Cosa succede confermando» (prima «Cosa riconosci confermando») (12/11/2026).
- Nelle pagine Trattativa e Contratto non c'è il box con le due parti (nomi, ruoli, badge identità), per tenere le pagine sulla fase (01/10/2026).

### Contratto

- Lo stage «Contratto» finisce con Registrazione (Preparazione alla firma + Pagamento registrazione). Da condizioni sospensive in poi, tutto quello che è in Finalizzazione (PG1–4) è lo stage «Rogito». Label dello stepper: «Rogito»; «Verso il rogito» è il titolo esteso della pagina pubblica Come funziona. Nessuno stage «Registrazione» separato (05/10/2026, supera il 29/09).
- PG3 F2c, sezione «Firma»: niente testo sopra la CTA e niente nota FEQ sotto, resta solo la riga sull'annuncio (cliente, 12/11/2026). Dettagli in `docs/claude/pg3-firma-alleggerita-12-11.md`.
- Stepper Contratto: lo step «Persone e documenti» usa sempre l'icona `group`. I link in spalla (Guida al contratto preliminare, Riepilogo degli accordi) compaiono solo dallo step in cui diventano disponibili e rilevanti (29/09/2026).
- I cointestatari che firmano con venditore o acquirente non sono utenti registrati: nessuna pagina per i messaggi, solo notifiche via email (07/10/2026).
- La persona registrata inserisce sempre i dati di tutti gli altri cointestatari; i cointestatari si accordano fuori dalla piattaforma (09/10/2026).
- Quando le parti indicano i cointestatari per la firma, la pagina è precompilata con i dati presi da Cleclà dalla visura e l'utente inserisce solo l'email (deve essere attuale e attiva per la firma). Il precompilato avviene nello step «Persone e documenti» del Contratto (21/10/2026).

### Finalizzazione / Rogito

- Le board di Finalizzazione sono organizzate per target (percorsi Venditore / Acquirente) e non per PG; probabilmente niente prototipi Figma (06/10/2026).
- Recesso e inadempimento chiesti dall'Acquirente sono un flusso speculare (annotato, non disegnato). K2 per l'Acquirente e il flusso della condizione di regolarità del Venditore sono da disegnare.
- L'avveramento automatico tramite Relazione Tecnica è disegnato come stato alternativo della K4V del Venditore.
- Le pagine Cleclà non citano le condizioni sospensive che non si applicano al contratto (righe «Non si applicano: …» rimosse) (05/10/2026).
- Nel flusso di recesso la firma FEA del documento di recesso viene prima dei pagamenti (registrazione, multa). Nei testi di Verso il rogito il notaio lo sceglie l'acquirente (art. 4 del contratto) (07/10/2026).
- La pagina contratto della fase Rogito è sempre la stessa pagina e il suo contenuto cambia man mano. Il suo stepper traccia il percorso, non serve a navigare.

## Correzioni di Giovane al copy della PG1 (11–17/09/2026)

Da tenere presenti scrivendo le pagine successive.

- Sottotitolo (pagina unica): «Venditore e acquirente trattano direttamente, senza agenzia. Qui trovi informazioni utili su come si fa una proposta, come si risponde e cosa conviene decidere prima di partire.»
- Come funziona: «La trattativa si svolge su un documento visibile a entrambe le parti, il documento di puntuazione. Ogni punto da concordare è una condizione: il prezzo, le date, le eventuali condizioni sospensive. Quando viene trovato un accordo, si scrive lì. Generiamo il contratto preliminare sulla base degli accordi raggiunti: quello che non è scritto nel documento, non entra nel contratto.»
- Passo 2: «Si parte dal prezzo dell'annuncio: le altre condizioni iniziano quando avete trovato l'accordo. Il prezzo tiene conto del valore dell'immobile, meno eventuali lavori di sanatoria e difetti dichiarati. Se stai ancora definendo il prezzo dell'annuncio, lascia un margine per la trattativa.»
- Titoli dei passi: «3 Accetti, fai una controproposta o rifiuti» · «4. Conferma l'accordo» · «5. Firma del contratto preliminare»
- Passo 4: «Quando ogni condizione ha un accordo, rileggete il riepilogo e lo confermate entrambi. Finché manca una delle due conferme, potete ancora modificare una condizione. Dopodiché verifichiamo la documentazione dell'immobile.»
- Condizione sospensiva: «Una condizione sospensiva vincola il contratto preliminare a qualcosa che deve ancora succedere, per esempio la delibera del mutuo. Il contratto procede solo se avviene entro la data che avete fissato. Monitoriamo la scadenza e ti avvisiamo per tempo; chi ha proposto la condizione comunica se si è avverata. Se sì, proseguite verso il rogito. Se no, il contratto si scioglie. Proponi solo quelle che ti servono davvero: ognuna è una possibilità in più che la compravendita non si concluda.»
- Mobili: «I mobili non vengono trattati qui: quelli che si possono portare via non entrano nel contratto preliminare e si elencano in un modulo a parte, che compilate insieme. La cucina è compresa nel prezzo, salvo diverso accordo, e lo sono anche gli armadi a muro e gli impianti.»
- Sezione recesso/inadempimento/inefficacia (16/09): titolo «Quando si annulla il contratto preliminare», tre casi (recesso, inadempimento, inefficacia), chiude con un alert di avviso: «Se l'affare non si conclude e la responsabilità non è di nessuno, non si paga niente: né provvigione, né penali, né rimborsi.»
- «Quando fissare il rogito»: rimosso il date planner (domande, risultato live, CTA «Proponi questa data»); restano l'elenco dei tempi e un blocco «Tempistiche del rogito».
- Alcuni alert diventano bottoni info che aprono il testo lungo; la versione aperta resta come riferimento fuori dalla board UI principale.
- Errori da evitare (Venditore): «Prolungare molto la discussione sul prezzo» · «Non dichiarare i difetti noti dell'immobile»

## Documenti in `docs/`

Ordine di lettura consigliato: questo file, poi il glossario, poi il resoconto più recente dell'epica su cui lavori. I file in `docs/claude/` sono i resoconti di lavoro, datati nel nome.

Riferimenti generali
- `glossario-coerenza-contenuti-approvati-clecla.md`: glossario v1.1, da verificare prima di scrivere.
- `claude/architettura-informativa-v2.md`: architettura aggiornata al 06/10.
- `memoria-di-progetto.md`: memoria iniziale (26/08), anteriore a quasi tutte le decisioni sopra. In caso di conflitto vale questo file.
- `brand/`: Brand Strategy NIDO e Manuale d'identità Cleclà (PDF).

Profilo immobile, Pubblicazione, Archivio (Sprint 2, agosto)
- `user-flow-profilo-immobile.md`, `wireframe-profilo-immobile.md`, `revisione-wireframe-sprint2.md`
- `bacheca-blocchi-decisioni.md`, `listing-annuncio-decisioni.md`, `scheda-tecnica-2.0-delta.md`
- `archivio-documentazione-decisioni.md`, `wireframe-archivio-tecnici-acquirente.md`, `trova-tecnico-decisioni.md`
- `claude/pubblicazione-annuncio-06-11.md`

Visite
- `claude/visite-consolidamento-06-11.md`
- `claude/visite-presentazione-06-11.md`
- `claude/visite-incarico-mediazione-09-11.md`

Trattativa
- Base: `claude/contenuti-trattativa-export.md`, `claude/wireframe-trattativa.md`, `claude/coerenza-epica-trattativa.md`, `Come funziona la trattativa.md`
- Guida PG1: `claude/delta-guide-trattativa-14-09.md`, `claude/ui-pg1-guida-trattativa.md`, `claude/rework-pg1-delta-feedback-20-09.md`
- Pagina PG2: `claude/ui-pg2-pagina-trattativa.md`, `claude/switch-trattative.md`, `claude/delta-pagina-unica-17-09.md`, `claude/delta-intestazioni-sezione.md`, `claude/ui-pg2-v2-feedback-20-09.md`, `claude/avvisi-trattativa-e-tavola-acquirente-28-09.md`
- Ottobre–novembre: `claude/rail-trattativa-15-10.md`, `claude/risposte-cliente-trattativa-22-10.md`, `claude/prova-tempi-lettore-29-10.md`, `claude/t4-conferma-accordo-03-11.md`

Contratto (preparazione firma, registrazione)
- `claude/ui-pg3-preparazione-firma.md`, `claude/ui-pg4-pagamento-registrazione.md`, `claude/ui-pg3-v2-feedback-20-09.md`, `claude/ui-pg4-v2-feedback-20-09.md`
- `claude/ui-contratto-lettore-guida.md`, `claude/coerenza-firma-verifica-25-09.md`, `claude/caricamento-documenti-28-09.md`, `claude/stepper-contratto-29-09.md`, `claude/pg3-firma-alleggerita-12-11.md`

Feedback cliente trasversali
- `claude/delta-feedback-cliente-20-09.md`, `claude/feedback-cliente-v2-28-09.md`, `claude/modifiche-risposte-cliente-07-10.md`

Finalizzazione / Rogito
- `clecla_pg_finalizzazione_v2.md`, `claude/user-flow-finalizzazione.md`, `claude/wireframe-finalizzazione.md`
- `claude/ui-finalizzazione-pg1.md` … `claude/ui-finalizzazione-pg4.md`, `claude/ui-finalizzazione-regolarita-venditore.md`
- `claude/rework-pg1-feedback-30-09.md` … `claude/rework-pg4-feedback-30-09.md`

Superati
- `legacy/architettura-informativa.md`: sostituito dalla board FigJam Architettura e da `claude/architettura-informativa-v2.md`.
