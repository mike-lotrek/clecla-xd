# PG1 · Intestazioni di sezione e allineamento delle tavole

Giovane ha rifatto le intestazioni di sezione sul desktop `D - 1`. Questo documento registra il pattern che ne risulta e il lavoro di propagazione alle altre quattro tavole di PG1.

## Il pattern nuovo

L'intestazione era una riga orizzontale: titolo a sinistra, illustrazione piccola a destra, niente altro. Ora è un blocco verticale con l'illustrazione grande che sborda dall'angolo e viene tagliata dal bordo della sezione.

| | Desktop | Mobile |
|---|---|---|
| Layout | verticale, padding 8/0/32/0, gap 16 | verticale, padding 8/0/24/0, gap 8 |
| Titolo | Spline Sans Medium 32 | Spline Sans Medium 24/30 |
| Colore del titolo | `text-fg-info` (1C06AC) | uguale |
| Sottotitolo | Regular 20, `text-onlight-strong` | Regular 16, stesso token |
| Illustrazione | 244 × 244, assoluta, x 622 y −96 | 100 × 100, assoluta, x 302 y −40 |
| Larghezza del testo | piena (802) | 280, per non finire sotto l'illustrazione |

«Errori da evitare» tiene il titolo in `text-fg-danger` (D70000): è l'unica sezione che segnala, le altre spiegano.

Due scelte che si discostano dal desktop, e il perché.

**Il titolo mobile è 24, non 28.** Sul desktop titolo di pagina e titolo di sezione sono entrambi 32, quindi la proporzione vorrebbe 28 anche su mobile, dove il titolo di pagina è 28. Ma a 28 su una colonna da 280 «Quando si annulla il contratto preliminare» va a tre righe e l'intestazione diventa più alta del primo blocco che introduce. A 24 sta su due.

**Il testo si ferma a 280 invece di andare a filo.** Sul desktop l'illustrazione si sovrappone a una colonna larga 802 senza toccare nulla, perché i titoli sono corti. Su 376 il sottotitolo finirebbe sotto il disegno.

I sottotitoli, presi dal desktop:

| Sezione | Sottotitolo |
|---|---|
| Come funziona | I sei passaggi della trattativa, dalla proposta alla firma |
| Cosa si tratta | Le condizioni da definire prima di firmare |
| Quando fissare il rogito | Cosa considerare prima di fissare le date |
| Errori da evitare | Cosa può complicare la trattativa |
| Perché non c'è la caparra? | La differenza tra caparra confirmatoria e clausola penale |
| Quando si annulla il contratto preliminare | I tre casi in cui può succedere, e cosa comporta per ciascuno |

## «Cosa si tratta»: icone e nota sui mobili

Le icone di gruppo sul desktop sono passate a 40 px allineate in alto; su mobile sono passate da 24 a 32.

La nota «I mobili non vengono trattati qui.» si è spostata: era un popover appeso al titolo del gruppo «Prezzo e pagamento», ora è una riga di testo dentro il gruppo con il bottone info accanto. Sul mobile il bottone che stava sul titolo è stato tolto, perché altrimenti lo stesso contenuto avrebbe avuto due trigger nella stessa riga.

## Testi allineati alle altre tavole

Il confronto testo per testo fra `D - 1` e le altre quattro tavole ha trovato che `D - 3` era già allineata (tranne un'etichetta di turno), mentre le tre mobili erano indietro.

**Etichette di turno accorciate** ovunque: «TOCCA AL VENDITORE» → «VENDITORE», «TOCCA ALL'ACQUIRENTE» → «ACQUIRENTE», «SUPPORTO CLECLÀ» → «SUPPORTO CLECLÀ (OPZIONALE)», «TOCCA A ENTRAMBI» → «ENTRAMBI».

**`M - 3` era la più indietro**: aveva ancora il sottotitolo di pagina della versione «senza agenzia», le card della penale intestate «Altrove» e «Con Cleclà» invece di «Agenzia tradizionale» e «Cleclà», e «Il venditore riceverebbe» al condizionale.

**`M - 2` e `M - 3` non avevano mai ricevuto il travaso del 17/09**: mancavano il settimo errore («Dichiarare le proprie condizioni a trattativa avviata») e l'ottava voce dei tempi («Fine del contratto d'affitto dell'acquirente, se è in affitto»). Aggiunti clonandoli da `M - 1`.

Dopo l'intervento le cinque tavole hanno lo stesso testo, a meno di quello che appartiene a una piattaforma sola (navbar e breadcrumb sul desktop, barra di percorso e system bar sul mobile) o a uno stato (le voci dell'indice si vedono solo in `M - 2`, dove la tendina è aperta; i testi dei popover solo in `D - 3`).

## Misure aggiornate

I frame mobili erano più corti del loro contenuto e lo tagliavano: `M - 1` dichiarava 5257 px con 5509 di contenuto, già prima di questo intervento. Ora `M - 1` e `M - 2` sono alti 5871 e la barra CTA è riancorata al fondo. `M - 3` resta 900 perché è una vista croppata dello scroll.

## Da fare

- **La tavola dei popover mobile continua a non esistere.** Era già un punto aperto e adesso pesa di più, perché con la nota sui mobili i trigger su mobile sono tre.
- **Le illustrazioni restano copie SVG scollegate dal DS.** Ridimensionarle significa rifare il `rescale` su ogni tavola: cinque volte per sei illustrazioni. Se diventassero componenti con una proprietà di taglia, questa operazione sarebbe un cambio di variante.
- **Il titolo di sezione non usa uno stile di testo.** Su desktop e mobile è impostato a mano (32 e 24 Medium): finché non c'è uno stile, ogni ritocco di scala va ripetuto a mano su cinque tavole.
