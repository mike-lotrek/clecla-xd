# Visite: accettazione dell'incarico di mediazione da parte dell'acquirente (09/11/2026)

File Figma «Cleclà | UI», Sprint 3, `UI Layouts – WIP` (3764:8875), section «Prenota Visita (A)».

## Perché

Oggi chi prenota una visita riceve una mail di riepilogo che lo avvisa: accettando la visita accetta anche un incarico di mediazione con una provvigione percentuale. Secondo il team legale del cliente non basta, perché è un obbligo di pagamento e l'incarico è dentro i Termini e condizioni, che nessuno legge. La mail resta, ma prima della conferma serve un'accettazione esplicita:
- una checkbox dedicata, non spuntata e bloccante;
- idealmente, la lettura della sezione dei Termini e condizioni sull'incarico prima che la spunta venga registrata. Il modo lo scegliamo noi.

## Soluzione

L'accettazione sta nel riepilogo «Controlla e invia la richiesta» (D-5, D-6). Ci passano tutti i percorsi: modale sull'annuncio, pagina dalla Bacheca, registrazione e verifica. Anche «Proponi un nuovo orario» ora porta lì («Continua» al posto di «Proponi nuovo orario»), così l'accettazione è in un punto solo.

Sequenza:
1. Il blocco «Incarico di mediazione» spiega l'impegno e la percentuale. La checkbox è vuota e disattivata, «Invia la richiesta» è disattivato e accanto dice perché.
2. «Leggi l'incarico di mediazione» apre una modale con la sezione dei Termini e condizioni. «Ho letto l'incarico» si attiva solo dopo aver scorso il testo fino in fondo. «Apri i Termini e condizioni» porta alla pagina completa.
3. Tornato al riepilogo, la checkbox è attiva ma ancora vuota.
4. Con la spunta si attiva «Invia la richiesta».

Ho scelto la lettura obbligata in modale e non l'ancora alla pagina dei Termini e condizioni: tiene l'utente nella prenotazione e lascia una prova che la sezione è stata vista per intero.

## Tavole e node ID

| Tavola | Node ID |
|---|---|
| Prenota Visite - D - 6 · blocco «Incarico di mediazione» | 6628:7067 (frame 5648:58017) |
| Prenota Visite - D - 5 · stesso blocco | 6628:7090 (frame 5648:58337) |
| Stato · Incarico letto, da accettare | 6630:7232 |
| Stato · Incarico accettato | 6630:7251 |
| Modale · Incarico di mediazione · da leggere | 6630:7075 |
| Modale · Incarico di mediazione · letto | 6630:7152 |
| Note · D-6 Incarico di mediazione | 6630:7227 |
| Modale – Proponi un nuovo orario (CTA «Continua») | 5648:3626 |

D-7 «Richiesta inviata» e le tavole alla sua destra sono state spostate per fare posto alle due modali.

## Contenuti

- Titolo: «Incarico di mediazione»
- Testo: «Prenotando la visita, affidi a Cleclà un incarico di mediazione per questa casa. Se la compri, ci riconosci una provvigione del 2% sul prezzo, con un minimo di 4.000 € più IVA. È dovuta solo a trattativa conclusa, con un contratto preliminare valido ed efficace.»
- Nessun importo calcolato: la frase «Al prezzo dell’annuncio, € 285.000, la provvigione è di 5.700 € più IVA.» è stata tolta il 09/11, perché il prezzo finale quasi mai coincide con quello dell'annuncio e la cifra sarebbe fuorviante.
- Link: «Leggi l’incarico di mediazione»
- Checkbox: «Ho letto l’incarico di mediazione e lo accetto». Sotto, prima della lettura: «Per accettarlo, aprilo e leggilo fino in fondo.» Dopo: «Accettandolo, ti impegni a riconoscere la provvigione se compri questa casa.»
- Accanto alla CTA disattivata: «Per inviare la richiesta, accetta l’incarico di mediazione.»
- Modale: titolo «Incarico di mediazione», intro «È la parte dei Termini e condizioni che riguarda l’incarico. Leggila fino in fondo: dopo potrai accettarla.», aiuto «Scorri fino in fondo per continuare.» poi «Hai letto tutta la sezione.», bottoni «Apri i Termini e condizioni» e «Ho letto l’incarico».

Le formule sulla provvigione vengono da Trattativa («dovuta a trattativa conclusa, con un contratto preliminare valido ed efficace»). Percentuale e minimo da CLAUDE.md.

## Punti da decidere

Col team legale e col cliente:
- Testo della sezione dei Termini e condizioni nella modale: oggi è un segnaposto.
- Testo del blocco: è una bozza. In particolare «più IVA» (il glossario lo riporta solo dai wireframe dell'annuncio) e il momento in cui la provvigione è dovuta.
- Accettazione a ogni prenotazione o una volta per immobile.
- Se la mail di riepilogo deve riportare data e ora dell'accettazione.

Interni:
- Il riepilogo D-6 con un orario proposto, invece che scelto tra le disponibilità, è da disegnare.
- Mobile: il riepilogo non ha una tavola mobile. La modale su mobile diventa un foglio dal basso con la stessa regola.
- D-7 «Richiesta inviata» potrebbe ricordare che l'incarico è stato accettato e dove trovarlo: non disegnato.

## Discrepanze con il glossario

- I27 dice che l'acquirente l'incarico «non lo firma». Con questa modifica l'acquirente accetta un incarico di mediazione: la voce va aggiornata. Non l'ho risolto io.

## Termini da registrare nel glossario

«Incarico di mediazione» anche per l'acquirente, «Leggi l’incarico di mediazione», «Ho letto l’incarico».
