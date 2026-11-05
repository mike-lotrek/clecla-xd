# Trova tecnico e Listing tecnici — decisioni e stato

Aggiornato al 18/08/2026. Priority guides: `20260818_Clecla_PG_Trovatecnico_2.xlsx` — 51 righe su due pagine più il foglio «Modifiche v2».

## Il principio: qui non c'è dietrologia

Trova tecnico è un servizio che Cleclà dà senza ricavarci nulla — nessuna commissione sui tecnici, nessun ruolo nell'accordo. Da questo discende tutto il resto: **non serve difendere il servizio, serve farlo usare**. La pagina si è ridotta da **2660 a 900 px** e i due campi sono la prima cosa che si vede.

## Cosa è stato tolto dall'apertura

| Blocco | Perché è caduto |
|---|---|
| Banner «Stai cercando un tecnico per: APE» | Diceva a parole quello che i campi già mostrano. |
| Indicatore di passo «1 di 2» | Cerimonia. Due campi e un bottone non sono un wizard. Tolto anche dal listing. |
| Blocchi «CHI LO PRODUCE» e «COSTO E TEMPO INDICATIVI» | Due card per un'informazione che sta in una riga sotto al campo. |
| P7 «Che differenza c'è tra RRE e relazione tecnica?» | Diventa l'annotazione del «?» sul campo documento: la risposta serve mentre scegli. |
| P7 «Devo pagare Cleclà per questo?» | Già risposto dal badge «incluso, senza commissioni». |
| Sezione «Dove sei nel percorso» | Spiegava che Trova tecnico non è una tappa del viaggio. Vero, ma non serve mentre cerchi un geometra. |
| Ricerche recenti, ALT «Non so cosa mi serve» | Tolti da Matteo nella semplificazione successiva. |

## La ricerca parte sempre vuota

**Nessuna precompilazione, mai.** Anche arrivando da una voce di checklist i due campi partono vuoti, il contatore dice «Compila i due campi» e la CTA è disabilitata. Cade così lo stato alternativo «arrivo dal menu, senza contesto»: non ci sono più due aperture diverse, ce n'è una sola.

Le **scorciatoie ai documenti mancanti** restano, e non sono una precompilazione: sono una proposta che si attiva al tap — *«Ti mancano per Trilocale in Via Roma: [APE] [Relazione tecnica] — un tap imposta documento e zona»*. È la cosa più action-first della pagina.

```
Ti mancano per Trilocale in Via Roma:  [APE] [Relazione tecnica]     un tap imposta documento e zona
Che documento ti serve (?)          Dove              Raggio
[ Scegli dall'elenco           ⌄ ]  [ Comune o CAP 🔍]  [ 25 km ⌄ ]
ⓘ Scegli il documento e ti diciamo chi lo produce, quanto costa e quanto ci vuole
────────────────────────────────────────────────────────────────
ⓘ Compila i due campi   il numero di tecnici compare qui   Non so cosa mi serve   [ Vedi i tecnici ]
```

Il **raggio a 25 km** è l'unico valore preimpostato, ed è un default di sistema, non un contesto dell'utente: tiene conto della conformazione della provincia, dove in valle il tecnico più vicino in linea d'aria non è quello che arriva prima.

Il **contatore live** che compare a campi pieni è l'invito a scoprire il risultato: dice che dall'altra parte c'è qualcosa, e quanto.

## I campi vivono anche nella pagina dei risultati

I chip «Stai cercando: APE ✕ Cuneo ✕ 25 km ✕» erano un riepilogo che costringeva a tornare indietro per cambiare una cosa. Al loro posto c'è **lo stesso blocco di campi**, in versione compatta, in testa ai risultati: si modifica da lì e la lista si ricarica mantenendo la posizione della mappa.

È il pattern standard (Booking, Airbnb, Idealista): la pagina dei risultati diventa autosufficiente. Su mobile lo stesso blocco è una **barra compatta** — «APE · Cuneo · 25 km / tocca per modificare» — che al tap si apre con gli stessi due campi.

## La ricerca resta a raggio

La proposta di sostituire il raggio con le **isocrone** (aree per tempo di percorrenza: entro 20 minuti, entro 40, oltre) **è caduta**. In un territorio montano il tempo di percorrenza è il dato che conta davvero, ma sta bene dove sta — **su ogni card, accanto alla distanza**: «1,2 km · 5 min» — senza cambiare il modello di ricerca né aggiungere un calcolo da validare col team tech.

## Mobile: lista e mappa come viste alternative

Prima la mappa occupava un terzo di schermo *sopra* la lista, tutto in un unico scroll. Ora sono **due viste della stessa ricerca**, pattern Booking e Airbnb:

- il **toggle Lista / Mappa** sta accanto alla barra di ricerca e resta raggiungibile in entrambe
- default **Lista**: card a tutta larghezza, nessuna mappa a rubare spazio
- **Mappa** a tutto schermo: pin numerati, filtri in overlay, e la lista ridotta a una **card in peek** che scorre in orizzontale — tocchi un pin e salti alla sua card

Le azioni della card stanno su due righe: a 375 px quattro bottoni su una riga sfondavano. Contatto sopra (Chiama, Scrivi), secondarie sotto (L'ho contattato, Salva).

## Niente recensioni

**Rimosse da tutti i layout**: voto in stelle e numero di recensioni sulle card, «Nessuna recensione ancora» per i nuovi, il blocco recensioni nella modale di dettaglio, «Valutazione» tra i criteri di ordinamento, e lo stato vuoto «Nessun tecnico con almeno 4 stelle entro 10 km» — riscritto sul raggio.

⚠️ **Nota di onestà**: la riga «Da MVP: recensioni del tecnico» nelle priority guide l'ho scritta io in una sessione precedente. Non ho in questa sessione il documento MVP che la giustificherebbe, quindi non posso confermare che ci fosse davvero. In ogni caso non si raccolgono in prima battuta e sono state tolte.

Il pulsante **«Salva»** sulle card resta: serve a confrontare due o tre tecnici prima di decidere, e non ha niente a che fare con le recensioni.

## Punti aperti

- **DA VALIDARE con il team**: la regola reale di ingresso nell'elenco dei tecnici. È l'informazione che rende l'elenco credibile invece che una pagina gialla.
- I costi indicativi per documento (150–250 € per l'APE) sono placeholder: servono medie reali del Cuneese.
- «Tempo di risposta dichiarato» come criterio di ordinamento regge solo se il dato esiste.
- Le righe delle priority guide su recensioni, ordinamento per valutazione e stato vuoto a stelle (foglio Contenuti, righe 852, 862, 868, 872) vanno riscritte.
