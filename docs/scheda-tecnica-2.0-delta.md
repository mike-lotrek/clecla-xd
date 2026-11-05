# Scheda Tecnica 2.0 — cosa cambia rispetto ai wireframe

Confronto campo per campo tra `20260331_Scheda Tecnica 2.0.xlsx` (foglio DATI, 253 righe piene) e il frame **PI-ST · tutti gli step aperti**. Più quello che lo **studio di vendibilità** (`20260512_Studio di vendibilità.pdf`) usa davvero per calcolare la stima.

---

## 1. Cosa serve allo studio di vendibilità

Dall'allegato «Scheda di valutazione» del PDF, la stima si costruisce così:

| Blocco | Dati usati | Da dove arrivano |
|---|---|---|
| Anagrafica | regione, comune, indirizzo, tipologia | scheda |
| **Quotazioni OMI** | zona OMI, valore min/max abitativo €/m², valore min/max box €/m² | **dato pubblico Agenzia delle Entrate** |
| Valore di riferimento | zona (centrale/periferica), trasporti entro 400 m, servizi a piedi, la zona è ordinaria/…, situazioni di degrado, adozione OMI min/medio/max | scheda |
| Fattori correttivi | FC1 tipologia, FC2 popolazione, FC3 posizione | calcolati |
| **C1** qualitative | posizione, numero di piano, ascensore, giardino o cortile di proprietà, vista principale, luminosità, camere, bagni, corrispondenza camere/bagni, corrispondenza camere/superficie, fattori ambientali, caratteristiche che aumentano o diminuiscono il valore | scheda |
| **C2** esterno | facciate, tetto, aree esterne, qualità dell'edificio rispetto alla zona | scheda |
| **C3** interno | stato manutentivo interno (intonaci, pavimento, porte, elettrico, idraulico, bagni) | scheda — la nostra matrice 5g |
| **C4** energetica e impianti | classe energetica, serramenti recenti, domotica base, domotica avanzata, raffrescamento estivo, VMC, videosorveglianza, allarme, **acque pluviali**, colonnina auto elettrica, fotovoltaico con accumulo e pompa di calore | scheda |
| **C5** giuridico | locato, tempo rimanente, nuda proprietà, età dell'usufruttuario | scheda |
| Quantitative | **superficie commerciale abitativo**, **superficie commerciale pertinenze** | scheda o visura ← *unico punto critico* |
| **C6** autorimessa | apertura automatizzata, **stato manutentivo del box**, quanti posti | scheda |
| Posti auto | **coperti (numero)**, **scoperti (numero)** | scheda |
| **Mobilio** | **armadi zona notte (numero)**, **armadi zona giorno (numero)**, dimensione media della cucina, **quante cucine** | scheda |
| Altre pertinenze | valore | scheda |

### La risposta alla domanda sulla delega

**Lo studio di vendibilità non ha bisogno né della visura né della planimetria.** Le quotazioni OMI sono un dato pubblico dell'Agenzia delle Entrate consultabile per zona, e il disclaimer del PDF lo dice esplicitamente: *«elaborato sulla base delle informazioni fornite dal venditore, dei dati di mercato disponibili al momento e dell'esperienza professionale dell'agenzia»*.

Quindi **i due binari sono davvero paralleli**: scheda tecnica → studio → prezzo da una parte, identità → incarico dall'altra. Si incontrano solo alla pubblicazione.

**L'unico punto di contatto è la superficie commerciale.** Oggi nel wireframe sta tra i «campi derivati dalla visura». Se la prendiamo dalla visura, lo studio aspetta l'incarico e il parallelismo salta. Se la dichiara il venditore — è sull'atto di provenienza, ed è il dato che useremmo comunque per l'annuncio — no. **Da decidere: è questa scelta che determina se il percorso è parallelo o sequenziale.**

---

## 2. Manca nel wireframe

### 2.1 Pertinenze — il buco più grosso
La 2.0 prevede **quattro pertinenze**, ognuna con dodici campi: indirizzo catastale, numero civico, foglio, particella, subalterno, categoria, tipologia, classe, consistenza (m²), superficie commerciale (m²), superficie (m²), rendita catastale. Nell'esempio: Pertinenza 1 = autorimessa C/6, Pertinenze 2–4 = magazzini e locali deposito C/2.

Lo studio le valorizza **separatamente** dall'abitativo («Superficie commerciale pertinenze», «STIMA Altre pertinenze», «STIMA valore autorimessa»). Nel wireframe non esiste niente: c'è solo «Box auto» come attributo dell'abitazione.

### 2.2 Terreno agricolo
Blocco assente: indirizzo catastale, civico, foglio, particella, superficie (m²), qualità, reddito dominicale, reddito agrario. **E c'è un errore da correggere**: *Reddito dominicale* e *Reddito agrario* nel wireframe stanno tra i campi derivati dalla visura dell'immobile — appartengono al terreno, non all'abitazione.

### 2.3 Dati fiscali — manca una domanda su tre
La 2.0 ne ha tre, noi due. Manca: *«Per quanto riguarda le detrazioni fiscali per ristrutturazione edilizia e/o risparmio energetico, per le quote da utilizzarsi nei rimanenti periodi di imposta permangono al venditore?»* Il contatore passa da **0 / 2** a **0 / 3**.

### 2.4 Titoli edilizi esistenti
Campo testo in 2.0 (*«Permesso di costruire n. 4448/2009; Certificato di agibilità del 07/09/2010; DIA 2985/2010…»*). Nella sezione Regolarità del wireframe ci sono solo RRE e RT.

### 2.5 Campi che servono allo studio e non ci sono
- **Stato manutentivo del box** — usato in C6. Noi chiediamo solo l'apertura automatizzata.
- **Armadi zona notte** e **armadi zona giorno**, come numero. Noi abbiamo *«Armadi a muro?»* sì/no, che non basta per la stima del mobilio.
- **Acque pluviali** — dotazione usata in C4, assente.
- **Posti auto** vanno spezzati: coperti (numero), scoperti privati (numero), condominiali (sì/no). Oggi è un campo solo. La 2.0 ha *«Posti auto privato (numero)»* e *«Posti auto condominiale? SI/NO»*, lo studio calcola coperti e scoperti separatamente.
- **Il terrazzo ha un valore particolare** perché nella zona soluzioni così sono introvabili? — presente in 2.0, assente da noi.

### 2.6 Condizioni della compravendita
Sezione intera della 2.0, oggi nel nostro *«Cosa non chiediamo adesso»*. Contiene prezzo finale, data del rogito, consegna libera, indennità di occupazione, consegna con conduttore, **provvigione parte venditrice (+IVA)**, **provvigione parte acquirente (+IVA)**, **costi di registrazione AdE**, e **cinque condizioni sospensive**: mutuo, regolarità edilizia e conformità catastale, vendita dell'immobile del promissario acquirente (con i suoi dati catastali), soluzione abitativa per il venditore, diritto di prelazione.

**Da decidere**: restano in trattativa, come abbiamo scelto, o la 2.0 le vuole in scheda? Le tre voci sulle provvigioni si legano al punto aperto «provvigione, tre numeri diversi».

---

## 3. Dove il wireframe si è allontanato dalla 2.0

Non sono errori: sono scelte di UX. Vanno però validate perché cambiano il conteggio dei campi.

| Wireframe | 2.0 | Nota |
|---|---|---|
| Toggle + campo condizionale sulle utenze (*«allacciato alla rete acquedottistica?»* → *«modalità di approvvigionamento»*) | un campo a scelta multipla (`ACQUEDOTTO PUBBLICO` / `POZZO` / …) | il nostro contatore dice **0 / 10**, la 2.0 ha **6** campi |
| *Tipo di riscaldamento* spezzato in gestione e diffusione | un campo solo (`CENTRALIZZATO`) | noi in più |
| Descrizione dell'atto come form (notaio, sede, data, repertorio, raccolta) | testo libero | il nostro è meglio |
| Dati del titolare del diritto reale come campi (cognome, nome, CF, nascita, domicilio) | testo libero | il nostro è meglio |
| Spese condominiali: toggle + importo + periodo | solo importo €/mese | noi in più |
| Condominio spezzato tra step 1 (contesto, nome) e step 5e (spese, manutenzione) | sezione CONDOMINIO unica | da valutare se riunire |

---

## 4. Un dato che ci manca e che ci serve

In testa al foglio DATI ci sono due legende: **«informazioni che saranno presenti nell'annuncio visibile sulla piattaforma di Cleclà»** e **«Informazioni oscurate nella Brochure»**.

**Nessuna delle due è applicata a nessun campo.** Ho controllato la formattazione riga per riga: le uniche celle colorate sono le intestazioni di sezione e le fasce di vendibilità in fondo. La legenda è dichiarata e non usata.

È esattamente il dato che serve per disegnare l'annuncio pubblico e la brochure: **quali campi diventano pubblici e quali restano privati.** Senza, l'anteprima dell'annuncio resta un'ipotesi.

Nota utile già presente nel foglio, che conferma l'approccio tenuto finora: *«Le domande presenti nella colonna A sono impostate ai fini di effettuare il calcolo della stima immobiliare, dunque scritte in maniera tecnica. Per la pubblicazione sarebbe opportuno rivedere il testo.»*

---

## 5. Ordine delle sezioni

| 2.0 | Wireframe |
|---|---|
| 1. Dati catastali | 1. Dati catastali |
| 2. Situazione giuridica | 2. Situazione giuridica |
| 3. Condizioni della compravendita | *(in «cosa non chiediamo adesso»)* |
| 4. Regolarità urbanistica e catastale | 3. Regolarità urbanistica e catastale |
| 5. Dati fiscali | 7. Dati fiscali |
| 6. Prestazione energetica | 4. Prestazione energetica e impianti termici |
| 7. Condominio | *(diviso tra step 1 e step 5e)* |
| 8. Caratteristiche architettoniche e contesto | 5. Caratteristiche architettoniche |
| 9. Utenze e servizi | 6. Utenze e servizi |
| 10. Pertinenze 1–4 | **assente** |
| 11. Terreno agricolo | **assente** |
| — | 8. A quanto vorresti vendere |

L'ordine diverso non è un problema — il nostro segue la fatica dell'utente, non la logica del calcolo — ma le due sezioni assenti sì.

---

## 6. Da decidere, in ordine di impatto

1. **Superficie commerciale dichiarata o da visura** — determina se studio e incarico sono paralleli o in sequenza.
2. **Pertinenze e terreno**: quanti blocchi ripetibili, e se compaiono solo quando il venditore dichiara di averne.
3. **Condizioni della compravendita**: in scheda o in trattativa.
4. **Legenda dei campi pubblici**: quali dati vanno nell'annuncio e quali sono oscurati nella brochure.
5. Reddito dominicale e agrario spostati sul terreno.
6. I sei campi mancanti per lo studio (stato del box, armadi notte e giorno, acque pluviali, posti auto separati, valore del terrazzo) e la terza domanda fiscale.
