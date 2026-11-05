# Architettura informativa Cleclà · v2

Versione 2.1 · 06/10/2026. Trascrizione della sezione «Architettura» (`333:348`) della board FigJam **[EXT] Cleclà | User Flows** (`DXvZbuexjok4HOsLSuLiEK`). Sostituisce `architettura-informativa.md`, che resta in KB come legacy.

Le relazioni sono quelle dei connettori della board. Il tipo di pagina segue la legenda della board: contenuto (bordo nero), funzionalità (bordo blu), funzionalità della pagina (tratteggio blu), stati della pagina (tratteggio giallo), esterna (grigio).

---

## Area pubblica

- **Homepage**
  - **Landing venditori** (connettore «voglio vendere»)
    - FAQ
  - **Landing acquirenti** (connettore «voglio acquistare»)
    - Listing immobili
      - Annuncio (n)
    - FAQ
  - **Chi siamo**
  - Footer: Contatti · T&C · Privacy Policy · Cookie Policy
- **Annuncio su piattaforma esterna** (pagina esterna) → porta ad Annuncio (n)

Nella board non c'è un nodo «Come funziona»: la vecchia trascrizione lo metteva al primo livello.

## Accesso

- Homepage → **Login** e Homepage → **Registrazione**, collegati fra loro nei due sensi.
- Registrazione → «Email in attesa di verifica» → torna alla Homepage.
- Registrazione → «Email verificata» → Profilo utente.
- Login → Profilo utente.

## Area privata

**Profilo utente** (tratteggiato), con figli:

- Trova tecnici (funzionalità)
- Impostazioni / Sicurezza
- Carrello → Checkout (funzionalità)
- Archivio documentazione personali (funzionalità)
- Bacheca personale venditore (connettore «Ruolo: venditore»)
- Bacheca personale acquirente (connettore «Ruolo: acquirente»)

**Cambia ruolo** collega le due bacheche, nei due sensi.

### Ruolo venditore

- **Bacheca personale venditore**
  - **Profilo immobile (n)**
    - Archivio documentazione immobile (n = numero di immobili) (funzionalità)
    - Calendario visite filtrato per immobile (funzionalità)
    - **Trattative**
      - Guida alla trattativa (venditore)
      - Trattativa (n) (funzionalità, condivisa con l'acquirente)
    - **Gestione contratti**
      - Contratto (n) (funzionalità, condivisa con l'acquirente)
  - Calendario visite (funzionalità)
  - Stato pagamenti

### Ruolo acquirente

- **Bacheca personale acquirente**
  - Preferiti
  - Calendario visite (funzionalità)
    - Pagina dettaglio appuntamento
  - **Profilo immobile (n)**
    - **Trattative**
      - Guida alla trattativa (acquirente)
      - Trattativa (n) (condivisa)
    - **Gestione contratti**
      - Contratto (n) (condivisa)
  - Stato pagamenti

Trattativa (n) e Contratto (n) sono un nodo solo, raggiunto dai due rami con connettori tratteggiati: la stessa pagina vista dai due ruoli.

---

## Differenze rispetto alla trascrizione legacy

- Trattative e Gestione contratti sono figlie di **Profilo immobile (n)**, per entrambi i ruoli, non della bacheca. Le liste sono per immobile.
- L'acquirente ha un Profilo immobile (n) con figli (Trattative, Gestione contratti).
- Calendario visite filtrato per immobile è figlio di Profilo immobile, non del Calendario visite.
- Pagina dettaglio appuntamento sta sotto il Calendario visite dell'acquirente, non del venditore.
- Area pubblica: Landing venditori e Landing acquirenti con le rispettive FAQ, Listing immobili sotto la Landing acquirenti; «Come funziona» non compare.

## Regola delle breadcrumb

La breadcrumb parte dal Profilo immobile («Trilocale in Via Roma 12, Cuneo»). Il livello della lista («Trattative», «Contratti») compare solo quando la lista esiste: con un elemento solo la lista si salta e il link porta dritto alla pagina (regola della PG Finalizzazione, estesa alle trattative). L'ultima voce nomina la controparte: «Trattativa con [Nome]», «Contratto con [Nome]».

## Conseguenze applicate (06/10/2026)

**Finalizzazione** (`Cleclà | UI`, pagina `44:986`):

- lista «Contratti dell'immobile», breadcrumb «Trilocale in Via Roma 12, Cuneo / Contratti»;
- pagine contratto: «Trilocale in Via Roma 12, Cuneo / Contratto con [controparte]» (caso con un contratto solo);
- sidebar con «I miei immobili» attiva al posto della Bacheca.

**Trattativa, Sprint 4** (pagina `44:983`, 28 tavole desktop):

- pagina trattativa, Venditore (10): «Trilocale in Via Roma 12, Cuneo / Trattative / Trattativa con Giulia Rossi». Il venditore ha tre trattative aperte sull'immobile, quindi la lista c'è;
- pagina trattativa, Acquirente (3): «Trilocale in Via Roma 12, Cuneo / Trattativa con Marco Ferrero»;
- Guida alla trattativa (1): «Trilocale in Via Roma 12, Cuneo / Trattative / Guida alla trattativa»;
- Preparazione alla firma e Pagamento registrazione (14): «Trilocale in Via Roma 12, Cuneo / Contratto con [controparte]», perché stanno nella fase «Contratto» dello stepper e R3 è diventata K3.0. Scelta da confermare;
- sidebar con «I miei immobili» attiva;
- pagina nuova **Trattative dell'immobile – D · Listing (Venditore)** (`5131:7921`), nella sezione PG2 dopo il popover D-4: tre trattative aperte (Giulia Rossi, Andrea Bianchi, Chiara Vietti, con il passo successivo del popover), due chiuse con accordo (Paolo Gallo e Luca Bianchi, i cui contratti compaiono come annullati nella lista contratti), link «Guida alla trattativa», empty state e nota. Senza PG dedicata: l'inventario ha solo le righe 226-227 e 242-243.

## Punti aperti

- Il popover D-4 e il foglio mobile chiudono con «Vai ai tuoi immobili». Con la lista nuova il link più utile sarebbe verso «Trattative dell'immobile». Da decidere insieme al nome unico della destinazione (punto già aperto in `claude/switch-trattative.md`).
- Le modali hanno come fondo PNG esportati prima del cambio di breadcrumb e sidebar.
