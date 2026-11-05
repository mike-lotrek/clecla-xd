> **LEGACY · dal 06/10/2026.** Questa trascrizione è superata da `claude/architettura-informativa-v2.md`, ricavata dalla board FigJam «[EXT] Cleclà | User Flows», sezione «Architettura» (`333:348`). Qui Trattative e Gestione contratti stanno sotto la bacheca: nella board sono figlie di Profilo immobile (n), per entrambi i ruoli. Non usare questo documento per collocare le schermate.

# Architettura informativa Cleclà

Trascrizione dello schema semplificato contenuto in `Cleclà_Architettura.pdf` (file allegato al progetto Claude).
Serve a collocare ogni schermata dei wireframe dentro l'albero del prodotto.

---

## Area pubblica

**Homepage**

**1° livello**
- Come funziona
- Chi siamo
- Annunci
- Trova casa / voglio acquistare
- Vendi casa

**2° livello**
- FAQ venditori
- Annuncio (n)
- FAQ acquirenti

**Trasversali (footer)**
- Contatti
- T&C
- Privacy Policy
- Cookie Policy

**Fuori piattaforma**
- Annuncio su piattaforma esterna

---

## Accesso

- Login
- Registrazione
- Email in attesa di verifica → Email verificata

---

## Area privata

**1° livello privato**
- Profilo utente
- Impostazioni / Sicurezza
- Trova tecnici
- Archivio documentazione (personali)
- Carrello → Checkout
- Cambia ruolo

Il profilo utente si biforca in due ruoli: **venditore** e **acquirente**.

### Ruolo venditore

- **Bacheca personale venditore**
  - Profilo immobile (n)
    - Archivio documentazione immobile (n = numero immobili)
  - Calendario visite
    - Calendario visite filtrato per immobile
    - Pagina dettaglio appuntamento
  - Trattative
    - Guida alla trattativa (venditore)
    - Trattativa (n)
  - Gestione contratti
    - Contratto (n)
  - Stato pagamenti

### Ruolo acquirente

- **Bacheca personale acquirente**
  - Preferiti
  - Profilo immobile (n)
  - Calendario visite
  - Trattative
    - Guida alla trattativa (acquirente)
  - Gestione contratti
  - Stato pagamenti

---

## Come leggerlo insieme ai wireframe

| Nodo dell'architettura | Dove sta nei wireframe |
|---|---|
| Annunci · Annuncio (n) | `ACQ / …` — sezione *Listing immobili e Annuncio immobile* |
| Bacheca personale venditore/acquirente | `BAC / …` — sezione *Bacheca venditore e acquirente* |
| Profilo immobile (n) | `S1–S8b` + `PI-ST` — sezione *Profilo immobile* |
| Archivio documentazione immobile | `ARC / …` — pagina *Archivio immobile* |
| Trova tecnici | sezione *Trova tecnico e Listing tecnici* |
| Trattative · Gestione contratti · Stato pagamenti | **fuori perimetro Sprint 2** — esistono nello stepper come ingombri dichiarati |
| Carrello · Checkout | non affrontati |

---

*Trascrizione fedele allo schema. Il PDF originale va ripreso da Drive e riallegato al nuovo progetto Claude (vedi `README.md` in questa cartella).*
