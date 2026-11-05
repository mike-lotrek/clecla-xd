# Bacheca venditore e acquirente — come si popola lungo il percorso

Creato il 18/08/2026. Nuova sezione `Bacheca venditore e acquirente` nella pagina `📏 Wireframe` dello Sprint 2, in coda alle altre.

| Frame | |
|---|---|
| `BAC / Desktop 1440 — Catalogo dei blocchi della bacheca` | ogni blocco una volta sola, con la regola di quando compare |
| `BAC / Desktop 1440 — Bacheca venditore · due immobili in momenti diversi` | + 3 stati alternativi |
| `BAC / Desktop 1440 — Bacheca acquirente · ricerche, preferiti e novità` | + 2 stati alternativi |
| `BAC / Mobile 375 — Bacheca venditore` | |
| `BAC / Mobile 375 — Bacheca acquirente` | |

## Da dove si parte

La bacheca **esiste già** come pagina Sprint 1 (`✅ Bacheca V+A`): sidebar, saluto «Ciao Mario, ecco dove eravamo rimasti» e stepper del percorso. Tutti i frame però sono fermi su **«Nessun annuncio presente»**: manca l'area contenuto. Questa sezione aggiunge solo quella. Saluto e stepper qui sono ingombri tratteggiati, non si ridisegnano.

## La regola che tiene insieme tutto

**Venditore e acquirente possono avere più immobili in ballo contemporaneamente.** Da qui discende la scelta strutturale: la bacheca si organizza **per immobile, non per tipo di attività**. Non c'è una sezione «Documenti» con dentro i documenti di tutti gli immobili: c'è una sezione per immobile, e dentro i suoi blocchi.

Ogni blocco porta sempre, in testa, **il nome dell'immobile a cui si riferisce e la tappa** in cui quell'immobile si trova. Anche quando il blocco è già dentro alla sezione di quell'immobile: la ridondanza è voluta, perché su mobile scorrendo si perde il titolo della sezione, e perché gli stessi blocchi finiscono nelle notifiche e nelle email, dove il contesto non c'è.

```
🏠  Nome dell'immobile   ·   [Tappa]                     meta
Titolo del blocco — dice cosa c'è da fare, non cosa è successo
Riga di contesto, se serve
[ Azione primaria ]   azione secondaria
```

## I blocchi

**Venditore** — Riprendi la scheda tecnica (con barra di avanzamento) · Verifica la tua identità · Firma l'incarico · È arrivato lo studio di vendibilità · Dicci quando puoi far visitare · Stiamo preparando il tuo annuncio · Il tuo annuncio è online (con visualizzazioni, salvataggi, richieste) · Mancano N documenti per il preliminare.

**Acquirente** — N nuovi immobili per questa ricerca · Il prezzo è sceso · Questo immobile non è più disponibile · Completa il profilo per prenotare.

**Comuni** — Card immobile (l'unità di base) · Aggiungi un altro immobile / Continua a cercare · ingombro delle tappe successive.

Ogni blocco nel catalogo porta sotto la propria **regola di comparsa**, che è la parte che serve davvero allo sviluppo: *«compare a scheda completa, se l'identità non è ancora confermata»*, *«sparisce a firma avvenuta»*, e così via.

## Tre scelte che vale la pena ricordare

**Lo studio di vendibilità è una notifica, non una tappa.** Compare in cima alla sezione dell'immobile, sopra il blocco della tappa corrente, e sparisce a lettura confermata. Non cambia la tappa: il venditore può riceverlo mentre sta ancora firmando l'incarico.

**«In attesa di pubblicazione» è l'unico momento senza azioni**, ed è il più rischioso: se la bacheca tace, l'utente pensa di essere stato dimenticato. Il blocco delle lavorazioni non ha CTA — è l'unico — ma accanto c'è quello dei documenti, che gli dà comunque qualcosa da fare mentre aspetta.

**Per l'acquirente l'unità non è l'immobile ma la coppia ricerca/preferito.** Il blocco porta in testa il nome della ricerca salvata o dell'immobile salvato. Le tappe successive alla ricerca compaiono solo con una visita richiesta, che ricade sull'epica successiva: resta come ingombro dichiarato.

## Perimetro

Coperti i momenti dello **Sprint 2**. Trattativa, contratto e rogito esistono nello stepper ma non hanno blocchi: restano ingombri dichiarati, non spazi vuoti. Il blocco «Visita richiesta» è disegnato ma marcato come epica successiva, per mostrare dove atterra e come muove lo stepper.

## Da fare

- **Pagina pubblica «Annunci» nello stato di default**, prima che l'utente abbia cercato: da discutere.
- Le statistiche dell'annuncio online (visualizzazioni, salvataggi) sono un'ipotesi: da validare se il dato esiste nell'MVP.
- I frame Sprint 1 della pagina `Bacheca V+A` andranno aggiornati con l'area contenuto, o dichiarati superati da questi.
