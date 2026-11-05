# User Flow — "Profilo immobile e pubblicazione"
Ricostruito da `EXT Cleclà _ User Flows.pdf` (board unica, 3 swimlane).

## Legenda della board
Entry/End point · User decision · System decision · Database · User action · Screen · Pagina esterna · Note · Primary path · Secondary path

---

## LANE 1 — VENDITORI

### A. Ingresso e creazione profilo immobile
1. `[SCREEN]` **Bacheca personale**
2. `[USER ACTION]` **Aggiungi immobile**
3. `[SCREEN]` **Pagina scheda immobile** — alert di contenuto: *solo Cuneo*
4. `[SYSTEM DECISION]` **Dettaglio profilo completato?**
   - NO → Step 1
   - SI → salta a Step 2
5. `[USER ACTION]` **STEP 1 — Compilazione profilo utente**: telefono (non verificato), indirizzo di residenza, altre informazioni facoltative (?)
6. `[USER DECISION]` **Compilazione corretta?**
   - NO → `[SECONDARY]` Focus campi di errore
   - SI → `[DATABASE]` Creazione e salvataggio profilo utente
7. `[USER ACTION]` **STEP 2 — Compilazione "anagrafica" immobile**
   - obbligatori: indirizzo immobile
   - facoltativi: Foglio, Particella, Subalterno
8. `[USER DECISION]` **Compilazione corretta?**
   - NO → Focus campi di errore
   - SI → prosegue
9. `[SYSTEM DECISION]` **L'immobile è in provincia di Cuneo?**
   - NO → `[SECONDARY]` **Blocca utente: notifica**
   - SI → `[DATABASE]` **Creazione e salvataggio profilo immobile con codice annuncio**
10. `[USER ACTION]` **STEP 3 — Compilazione scheda tecnica** (come indicato nelle storie)
11. `[USER DECISION]` **Compilazione corretta?**
    - NO → Focus campi di errore
    - SI → `[DATABASE]` **Creazione e salvataggio profilo immobile e creazione checklist dinamica**

### B. Verifica identità e firma incarico (Yousign)
12. `[USER ACTION]` **Carica ID utente**: Nome e Cognome · Tipo e n. ID · Data, luogo ed ente del rilascio · Data di scadenza · carica foto/scan documento
13. `[SYSTEM]` **Verifica documenti caricati**
14. `[SYSTEM DECISION]` **Documenti confermati?**
    - NON VALIDO → `[SECONDARY]` **Notifica venditore errore**
    - OK → prosegue
15. `[SYSTEM]` **Richiesta firma incarico di vendita, privacy, adeguata verifica della clientela e delega allo scaricamento della planimetria (FEA)**
    - `[DATABASE]` Settaggio documenti da firmare e destinatario — *nota: "da capire se automatizzabile"*
    - lato backoffice: `[TEAM]` Generazione dell'incarico di vendita, privacy, adeguata verifica della clientela e delega allo scaricamento della planimetria
16. `[DATABASE]` **Invio richiesta firma digitale (email)**
17. `[USER DECISION]` **L'utente ha accesso alla mail inviata?**
    - NO → `[SECONDARY]` **Richiesta di ri-invio mail**
    - SI → prosegue
18. `[PAGINA ESTERNA]` **Email** → apre il percorso Yousign
19. `[PAGINA ESTERNA]` **Richiesta verifica identità**
20. `[USER ACTION]` **Input info** — Paese di provenienza · Seleziona documento
21. `[USER ACTION]` **Foto documento** — Scattare foto · Confermare
22. `[USER ACTION]` **Video/Selfie** — Record video / Scatta foto selfie seguendo indicazioni
23. `[SYSTEM DECISION]` **Identità confermata?**
    - NO → torna al percorso di verifica
    - SI → `[DATABASE]` **Salvataggio progress**
24. `[USER ACTION]` **Accetta utilizzo della firma digitale**
25. `[USER ACTION]` **Legge e firma incarico di mediazione immobiliare**
26. `[DATABASE]` **Salvataggio documentazione firmata nella sezione Archivio documenti**
27. `[SYSTEM]` **Badge "Utente verificato" sul profilo**

### C. Documentazione e ricerca tecnici
28. `[SCREEN]` **Checklist documenti dinamica**
29. `[USER ACTION]` **Carica documenti a disposizione** — seleziona tipologia di documento · carica documento
30. `[DATABASE]` **Salva documenti nell'archivio**
31. `[SYSTEM DECISION]` **Tutti i documenti caricati?**
    - SI → prosegue verso pubblicazione
    - NO → **Trova tecnici per documentazione**
32. `[SCREEN]` **Cerca tecnici**: Localizzazione · tipologia documento · tecnico
33. `[SECONDARY]` **Contatta tecnico e richiedi documento** (fuori piattaforma)
34. `[SYSTEM DECISION]` **APE caricato?**
    - NO → resta in attesa
    - SI → prosegue
35. `[SYSTEM]` **Notifica specifica per relazione tecnica**

### D. Studio di vendibilità e prezzo
36. `[DATABASE]` **Notifica prezzo consigliato**
37. `[USER ACTION]` **Conferma di lettura dello studio**
38. `[SCREEN]` **Profilo immobile**
39. `[USER ACTION]` **Modifica prezzo immobile** (opzionale)
- *Nota sulla board: "Si può creare il contratto preliminare"*

### E. Pubblicazione
40. `[SYSTEM]` **Notifica pubblicazione avvenuta → link**
41. `[END POINT]` **Annuncio immobile**

---

## LANE 2 — ACQUIRENTI
Vuota in questa board (flusso interamente venditore).

---

## LANE 3 — TEAM CLECLÀ (BACKOFFICE)

### Ramo dati catastali (subito dopo Step 2/3)
- `[SYSTEM]` **Invio notifica al team**
- `[SYSTEM DECISION]` **Dati catastali corretti?**
  - SI → prosegue
  - NO → `[SCREEN]` Profilo immobile (backoffice) → **Modifica dati catastali** → **Notifica utente della modifica**

### Ramo generazione incarico
- `[TEAM]` **Generazione dell'incarico di vendita, privacy, adeguata verifica della clientela e delega allo scaricamento della planimetria**

### Ramo visura e planimetria
- `[TEAM]` **Scaricamento planimetria e visura catastale**
- `[SCREEN]` **Profilo immobile (backoffice)** → **Caricamento planimetria e visura catastale** → `[DATABASE]` **Salvataggio progress**

### Ramo servizio foto/video
- `[SYSTEM]` **Invio notifica al team**
- `[TEAM]` **Team Cleclà contatta venditore per organizzare servizio foto**
- `[SCREEN]` **Profilo immobile (backoffice)** → **Caricamento foto e video**
  - *Nota: "Vi forniremo dei parametri specifici di dimensione, lunghezza e formato per il caricamento"*
- `[DATABASE]` **Salvataggio progress profilo immobile**
- `[TEAM]` **Completa profilo immobile** — descrizione · titolo annuncio · modifica codice annuncio

### Ramo studio di vendibilità
- `[TEAM]` **Team Cleclà esegue studio di vendibilità**
- `[SCREEN]` **Profilo immobile (backoffice)** → **Inserisci prezzo consigliato e allega studio di vendibilità (PDF)** → **Caricamento nell'archivio del profilo immobile**

### Ramo pubblicazione
- `[SYSTEM]` **Notifica scelta venditore**
- `[SYSTEM]` **Sblocca pubblicazione immobile**
- `[TEAM]` **Pubblica immobile su Cleclà**
- `[TEAM]` **Fornisci link pubblicazioni esterne**

#### Condizioni di sblocco della pubblicazione (nota sulla board)
1. Scheda tecnica compilata dall'utente
2. Incarico di vendita immobiliare firmato dall'utente
3. Materiale multimediale caricato
4. Conferma lettura dello studio di vendibilità
5. Visura catastale e planimetria caricate da Cleclà
6. APE caricato dall'utente

---

## Non coperto dalla board (da ricostruire per assunzione)
- Definizione disponibilità visite: calendario, ricorrenze, blocchi, salvataggio
- Struttura e navigazione dell'Archivio documentazione immobile
- Pagina "Trova tecnico" (istruzioni, contesto, filtri) e listing risultati
- Stati di errore Yousign oltre a "documenti non validi" e "identità non confermata"
- Gestione della scadenza/rifiuto della richiesta di firma
