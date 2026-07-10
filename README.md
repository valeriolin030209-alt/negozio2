# Casa Market - catalogo clienti e area admin

Questa cartella contiene un sito statico con due pagine separate:

- `index.html`: pagina clienti da collegare al QR code. Non contiene pulsanti o finestre per entrare nell'area admin.
- `admin.html`: pagina riservata all'amministratore. Mostra l'anteprima del catalogo e permette di accedere al pannello admin tramite codice.

## Funzioni clienti

- catalogo con colonna verticale delle categorie;
- categoria speciale `Offerte e sconti`, evidenziata con colore diverso, che raccoglie automaticamente tutti i prodotti in offerta;
- i prodotti in offerta restano visibili anche nella loro categoria originale;
- schede prodotto con prezzo vecchio barrato, prezzo scontato, percentuale di sconto e risparmio indicativo;
- casella informativa sopra il catalogo, modificabile dall'admin;
- messaggio in primo piano nella barra alta, modificabile dall'admin;
- filtro prodotti tramite categoria;
- ordinamento prodotti per categoria, nome, prezzo crescente e prezzo decrescente;
- scheda prodotto cliccabile con finestra dettaglio;
- prodotti con varianti/opzioni, per esempio misure, grandezze, colori o versioni diverse;
- prezzo diverso per ogni variante del prodotto;
- prezzo offerta diverso per ogni variante del prodotto;
- scelta quantita e aggiunta al carrello;
- icona in alto a destra per vedere carrello e ordini inviati;
- checkout con nome, telefono, tipo consegna/indirizzo e metodo di pagamento obbligatori;
- scelta destinazione: casa/ufficio, mercato martedi, mercato mercoledi, mercato giovedi, appartamento/residenza;
- campo indirizzo obbligatorio quando viene scelto casa/ufficio o appartamento/residenza;
- spesa minima obbligatoria, modificabile dall'admin;
- metodi di pagamento: contanti alla consegna, carta alla consegna, altro / da concordare.

## Funzioni admin

- accesso da `admin.html` con codice admin;
- aggiunta, rinomina, eliminazione e riordino categorie;
- aggiunta, modifica, eliminazione, foto, descrizione, prezzo, visibilita e riordino prodotti;
- aggiunta di varianti prodotto con nome opzione, prezzo normale e prezzo offerta specifico;
- possibilita di etichettare un prodotto come `Prodotto in offerta`;
- visualizzazione automatica dei prodotti in offerta nella categoria speciale `Offerte e sconti`;
- modifica della spesa minima necessaria per inviare l'ordine;
- modifica della casella informativa sopra il catalogo clienti;
- modifica del messaggio in primo piano nella barra alta, a sinistra del pulsante di accesso admin;
- gestione ordini ricevuti e cambio stato;
- generazione QR code per la pagina clienti `index.html`.

## Come usare le offerte

Per un prodotto senza varianti:

1. inserisci il prezzo normale;
2. seleziona `Prodotto in offerta`;
3. inserisci il `Prezzo offerta indicativo`;
4. salva il prodotto.

Per un prodotto con varianti:

1. inserisci le varianti, per esempio `20 cm`, `24 cm`, `Rosso`, `Grande`;
2. per ogni variante inserisci il prezzo normale;
3. seleziona `Prodotto in offerta`;
4. inserisci il prezzo offerta nella riga della variante interessata;
5. salva il prodotto.

Il prezzo offerta deve essere piu basso del prezzo normale. Il cliente vedra prezzo vecchio, prezzo scontato, percentuale e risparmio.

## Come provarlo subito

1. Apri `index.html` per vedere la pagina clienti.
2. Apri `admin.html` per gestire il sito.
3. Nell'area admin inserisci il codice richiesto.

Il codice admin non viene mostrato nelle pagine del sito.

## Come pubblicarlo online

Carica tutti i file su Netlify, Vercel, GitHub Pages o su uno spazio hosting.

Dopo la pubblicazione:

1. apri `admin.html`;
2. entra nell'area admin;
3. vai nella sezione `QR code`;
4. incolla il link pubblico della pagina clienti, cioe `index.html`;
5. genera e stampa il QR.

Puoi anche generare il QR da terminale:

```bash
python3 generate_qr.py https://link-pubblico-del-tuo-sito/index.html
```

## Nota importante per uso reale

Questa versione salva dati, prodotti e ordini nel browser tramite localStorage. Va bene per demo o prototipo.

Per un negozio reale con piu clienti e piu dispositivi serve collegare un backend con database, autenticazione e salvataggio ordini centralizzato.
