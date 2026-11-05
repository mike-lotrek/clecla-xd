# Memoria di progetto — Cleclà

Estratto dalla memoria persistente dell'account Claude di Matteo Banchelli, al 26/08/2026.
Sono i fatti che Claude ha accumulato lavorando su Cleclà nelle varie sessioni: valgono come **vincoli e convenzioni consolidate**, non come opinioni.

Chi riprende il progetto può incollare questo file nella knowledge base del nuovo progetto Claude: serve a far ripartire il modello con lo stesso contesto invece che da zero.

---

## Perimetro e attori

- La piattaforma è **Cleclà**. L'MVP functional requirements vive in un **Google Sheet condiviso**, gli user flow in **Figma "Cleclà | UI"** ed esportati in PDF.
- **Fase 1 limitata alla provincia di Cuneo.**
- Lotrek si appoggia a una **designer freelance esterna (Serena Micieli)** per UX/UI, design system e prototipazione.
- Il **preventivo v4 del 06/08/2026** restringe il perimetro rispetto al v3 del 30/07/2026: solo mockup desktop, un round di rework, wireframing e prototipazione solo se necessari, design system solo aggiornato sulle nuove pagine.
- Lavorazioni da concludere **entro il 31/10/2026**.

## Convenzioni sulle priority guides

- Le PG del **Profilo immobile** vanno tenute in **un'unica PG con blocchi condizionali per stato**, non spezzate per schermata.
- Le PG si consegnano **una pagina alla volta**, in un file Excel nuovo con il solo contenuto da validare. Consolidamento nel file `Contenuti` alla fine.
- Le PG Cleclà devono stare **tutte in un foglio unico**, campi e stati inclusi: niente fogli di appoggio, perché il contenuto va poi integrato nel file con le altre PG nello spazio dedicato a quella pagina.
- **Un file per area, versionato, che sostituisce il precedente.** Niente file delta separati: si integra sempre nel file completo.

## Convenzioni sui wireframe

- I wireframe Cleclà si fanno in **Desktop 1440**, con il **mobile 375 solo sui punti in cui il comportamento cambia davvero**.
- Nei wireframe la **scheda tecnica va disegnata con tutti gli 8 step in dettaglio**, non riassunta.
- **Errori e percorsi alternativi vanno inline nel frame padre**; un frame dedicato solo per le modali.
- Le **lavorazioni a carico del team Cleclà** non vanno in un blocco a parte ma **distribuite dentro la scheda tecnica in modo contestuale** (es. foto in alto come negli annunci, con hint che spiega che Cleclà contatta l'utente per il servizio fotografico), per mantenere piena trasparenza.
- Nel **listing dei tecnici la mappa va trattata come elemento primario**.
- Il **supporto in pagina** si gestisce con il rimando alla **chat**, non con un contatto email.

## Integrazioni

- **Yousign** (verifica identità e firma) va previsto come **integrazione blended** nell'esperienza ma **non progettato nel dettaglio**: non c'è possibilità di intervenire sul funzionamento dello strumento.

## Come Matteo vuole che Claude scriva (preferenza di account)

- Nei copy in italiano serve un **italiano naturale**: da evitare i calchi dall'inglese (es. «ciò che verrà dopo nella UX») e le formule gergali poco significative (es. «senso del craft»).

---

## Nota sul passaggio di consegne

- Matteo lascia il progetto Cleclà e passa la ownership a un collega.
- Ad agosto 2026 era già stato preparato l'export del precedente Claude Project **"Cleclà | Priority Guides"** (knowledge base, istruzioni, skill), caricato su Drive in
  `Agency/Progetti/Cleclà/05_Design & Develop/06_Claude Projects`.
  **Questo export — "Cleclà | Wireframe" — va nella stessa cartella**, accanto al precedente.

---

## Contesto tecnico ereditato dalle sessioni

- Dal **19/08/2026 il Figma Desktop Bridge non risponde più**: si lavora sul file con il **Figma MCP ufficiale** (`use_figma`).
  - `getPluginData` non è supportato → le librerie di helper salvate in `figma.root` non sono raggiungibili, i componenti vanno costruiti con Plugin API in chiaro.
  - La palette va campionata dai nodi esistenti: bg `#fafafa`, bianco, bordi `#e5e5e5` e `#d1d1d1`, testi `#111111` `#282828` `#434343` `#737373` `#a3a3a3`.
- I **commenti Figma non sono leggibili** dalle sessioni: serve un token valido in `FIGMA_ACCESS_TOKEN`.
- Le **annotazioni native Figma vanno scritte con la pagina in focus, una a una**: scritte in blocco fuori dalla pagina attiva ne scarta una parte senza dare errore.
- Si lavora **in place** sui frame esistenti: prima di modificare un nodo va **riletto**, e non si cancellano mai figli in blocco.
