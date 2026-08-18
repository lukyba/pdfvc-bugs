# PDFVC — PDF Visual Composer

**PDFVC (PDF Visual Composer)** è un editor PDF visuale per **browser e desktop**, progettato per modificare, organizzare, controllare e riesportare documenti PDF preservando quanto più possibile la struttura, il contenuto vettoriale e la fedeltà della resa originale.

L'applicazione combina le funzioni di un editor di pagine PDF con strumenti di modifica visuale del contenuto, OCR, moduli, redazioni, firme digitali, accessibilità, preflight, conversione ed elaborazione batch.

> **Stato del progetto:** Beta.  
Alcune strutture PDF particolarmente complesse vengono gestite in modo conservativo: quando una modifica strutturale non può essere eseguita con sufficiente affidabilità, PDFVC evita trasformazioni distruttive e può utilizzare una materializzazione o rasterizzazione localizzata.


## Caratteristiche principali

### Editing visuale dei PDF

PDFVC dispone di una modalità **Preview / Modifica** nella quale gli elementi della pagina vengono individuati e, quando tecnicamente possibile, resi modificabili come oggetti.

L'editor riconosce e gestisce, a seconda della struttura del PDF:

- testo;

- immagini;

- forme e grafica vettoriale;

- collegamenti;

- annotazioni e commenti;

- campi modulo;

- campi firma;

- oggetti derivati dal contenuto PDF originario.

Gli oggetti possono essere selezionati direttamente sulla pagina oppure dal **pannello Oggetti**.

Le operazioni supportate comprendono, secondo il tipo di oggetto:

- spostamento;

- ridimensionamento;

- rotazione;

- modifica delle proprietà;

- opacità;

- ordine Z;

- visibilità;

- blocco/sblocco;

- raggruppamento;

- selezione multipla;

- allineamento e distribuzione;

- copia del formato;

- eliminazione.

PDFVC cerca di conservare l'identità e l'ordine di pittura del contenuto PDF originario. Preview ed export condividono geometria e semantica delle modifiche per ridurre le differenze tra ciò che viene visualizzato e il PDF finale.


## Interfaccia

L'interfaccia è organizzata in due ambienti principali:

1. **Vista documento**, dedicata alla gestione delle pagine e alle operazioni sul PDF nel suo complesso.

2. **Preview**, dedicata alla visualizzazione dettagliata e alla modifica del contenuto di una singola pagina.

### Vista documento

All'apertura dell'app viene mostrata una drop zone dalla quale è possibile trascinare un PDF oppure selezionarlo dal filesystem.

Dopo il caricamento, le pagine vengono mostrate in una **griglia di anteprime**.

La toolbar principale contiene i gruppi di comandi per:

- apertura e importazione;

- salvataggio ed esportazione;

- ottimizzazione e strumenti avanzati;

- Undo/Redo;

- ordinamento delle pagine;

- zoom;

- selezione;

- copia, taglio e incolla;

- eliminazione;

- rotazione;

- modifica delle dimensioni delle pagine;

- decorazioni e riordinamento.

La toolbar può essere utilizzata in modalità **estesa** o **compatta**.

### Barra di stato

La barra inferiore mostra informazioni e attività relative al documento, comprese operazioni in corso e possibilità di arrestare alcuni processi lunghi.

Dalla barra di stato è inoltre possibile configurare:

- toolbar estesa o compatta;

- tema chiaro o scuro;

- temi aggiuntivi;

- colori normali o invertiti.

Quando pertinenti, vengono visualizzati anche indicatori relativi a firme o conformità del PDF.


# Apertura e importazione

PDFVC può aprire normali documenti PDF e dispone inoltre di funzioni dedicate a differenti sorgenti.

## PDF

Sono disponibili:

- **Apri PDF**;

- **Apri e ripara PDF**;

- apertura dei file recenti;

- recupero degli snapshot;

- caricamento tramite drag & drop.

In presenza di PDF problematici l'app può utilizzare una pipeline di normalizzazione/riparazione prima di ricorrere a strategie più invasive.

## Inserimento di documenti

Nel documento corrente possono essere inseriti:

- altri PDF;

- immagini;

- pagine vuote.

## Importazione Office

È disponibile l'importazione di:

- **DOCX**;

- **ODT**.

L'import cerca di ricostruire layout, testo e paginazione utilizzando una pipeline comune di conversione.

## Immagini e TIFF

L'app contiene importer dedicati per immagini e documenti TIFF.


# Gestione delle pagine

La vista principale consente di lavorare rapidamente anche su documenti composti da molte pagine.

Sono disponibili:

- selezione singola e multipla;

- seleziona tutto;

- deseleziona tutto;

- inverti selezione;

- seleziona pagine pari;

- seleziona pagine dispari;

- sposta pagina avanti o indietro;

- taglia;

- copia;

- incolla;

- elimina selezione;

- elimina le pagine non selezionate;

- elimina tutto;

- inserisci pagine;

- riordina le pagine;

- inverti l'ordine;

- Alternate Mix;

- Inverse Mix.

È inoltre possibile navigare direttamente indicando il numero di pagina.


# Rotazione, ritaglio e dimensioni pagina

PDFVC comprende strumenti per modificare geometria e orientamento delle pagine:

- rotazione a destra;

- rotazione a sinistra;

- rotazione di 180°;

- autorotazione;

- deskew delle scansioni;

- ritaglio;

- ridimensionamento pagina;

- uniformazione del formato;

- rasterizzazione delle pagine.

La trasformazione della pagina viene propagata, quando necessario, anche agli oggetti e ai modelli associati.


# Preview e modifica dettagliata

Facendo accesso alla Preview è possibile lavorare sulla singola pagina con un ambiente dedicato.

## Navigazione

La Preview comprende:

- pagina precedente/successiva;

- zoom numerico;

- zoom in/out;

- adatta pagina;

- adatta larghezza;

- rotazione;

- ricerca;

- Undo;

- Redo;

- ripristino;

- cronologia delle modifiche.

## Modalità Modifica

La modalità **Modifica** sovrappone al rendering PDF gli oggetti riconosciuti dall'analisi della pagina.

È possibile filtrare la visualizzazione per:

- **Testo**;

- **Immagini**;

- **Forme**;

- **Annotazioni**.

I filtri incidono anche sull'operabilità degli oggetti.

## Pannello Oggetti

Il pannello laterale Oggetti fornisce una rappresentazione strutturata del contenuto della pagina.

Può comprendere:

- blocchi di testo;

- immagini;

- grafica;

- collegamenti;

- form;

- firme;

- commenti.

Il pannello supporta:

- ricerca;

- filtri;

- selezione multipla;

- ordine Z;

- visibilità;

- lock;

- proprietà;

- centratura dell'oggetto nella viewport.

## Strumenti di precisione

La Preview comprende inoltre strumenti per il posizionamento preciso:

- righelli;

- guide;

- griglia;

- misurazione;

- snap;

- allineamento;

- distribuzione.

Questi strumenti assistono l'editing senza modificare direttamente il contenuto esportato finché non viene applicata un'operazione.


# Modifica del testo

La pipeline di analisi del testo cerca di ricostruire:

- caratteri e run;

- righe;

- blocchi;

- regioni;

- colonne;

- paragrafi;

- ordine di lettura.

Vengono considerate informazioni come:

- font;

- dimensione;

- baseline;

- avanzamento;

- colore;

- allineamento;

- indentazione;

- struttura delle righe.

Sono inoltre previsti stili come:

- apice;

- pedice;

- small caps.

Per il testo PDF originario, PDFVC distingue l'identità fisica dei glifi dal relativo contenuto Unicode e dalla possibilità effettiva di modificarli. Se una trasformazione non è sicura, l'app preferisce preservare il contenuto originario piuttosto che effettuare una sostituzione potenzialmente errata.


# Immagini e grafica vettoriale

L'editor riconosce immagini e numerose primitive grafiche PDF.

Per la grafica vettoriale vengono preservate, quando disponibili:

- curve;

- fill;

- stroke;

- fill rule;

- dash;

- opacità;

- clipping;

- bounds;

- ordine di pittura;

- Form XObject;

- gruppi di trasparenza.

La rasterizzazione non costituisce la modalità normale di editing: viene utilizzata come fallback limitato quando il contenuto non può essere trasformato strutturalmente in modo affidabile.


# Ricerca e sostituzione

PDFVC dispone di un motore di ricerca testuale documentale che può utilizzare:

- testo estratto dal PDF;

- contenuto dei text operator recuperati;

- testo prodotto dalle operazioni di editing;

- OCR, quando il documento non contiene testo nativo sufficiente.

La ricerca supporta:

- Unicode;

- normalizzazione NFC;

- maiuscole/minuscole;

- parola intera;

- espressioni regolari;

- testo RTL.

È prevista anche la sostituzione del testo quando la geometria e l'identità del contenuto permettono una modifica affidabile.


# OCR

PDFVC integra una pipeline OCR basata su elaborazione locale.

Sono disponibili:

- **Riconosci tutto**;

- **OCR interattivo**;

- revisione dei risultati;

- esportazione del testo OCR;

- eliminazione del testo OCR;

- salvataggio come PDF ricercabile.

La pre-elaborazione OCR può comprendere:

- scala di grigi;

- contrasto;

- threshold;

- despeckle;

- deskew;

- rilevamento/gestione dell'orientamento.

L'OCR può essere riutilizzato nelle funzioni di ricerca e negli export.


# Moduli PDF

PDFVC gestisce i campi AcroForm presenti nei PDF.

Sono previste funzioni per:

- visualizzare e modificare i campi;

- riconoscere potenziali campi;

- mantenere le appearance;

- appiattire i campi;

- reset dei valori;

- controllo dei nomi;

- importazione dati;

- esportazione dati.

## FDF / XFDF / CSV

Dal menu **Form/FDF** è possibile:

- importare dati FDF;

- importare dati XFDF;

- importare CSV;

- esportare XFDF;

- esportare FDF;

- esportare CSV;

- controllare i nomi dei campi;

- distribuire un modulo;

- raccogliere risposte.

Sono supportati anche alcuni campi specializzati, compresi barcode.


# Annotazioni e commenti

Le annotazioni possono essere mantenute come oggetti PDF vivi oppure appiattite quando richiesto.

L'app dispone inoltre di strumenti per:

- visualizzare i commenti;

- modificare i commenti supportati;

- produrre un elenco dei commenti;

- generare pagine riepilogative dei commenti.


# Collegamenti, segnalibri e navigazione

PDFVC conserva e gestisce il sistema di navigazione del documento.

Il modello comprende:

- link;

- outline;

- segnalibri;

- destinazioni;

- Page Labels;

- Viewer Preferences.

Le destinazioni interne vengono mantenute attraverso identificatori stabili delle pagine, così da poter sopravvivere a riordino, duplicazione ed eliminazione delle pagine.


# Livelli PDF / OCG

PDFVC riconosce gli **Optional Content Groups (OCG)** e consente di gestire i livelli PDF.

Sono conservati, quando disponibili:

- stato dei livelli;

- configurazioni;

- intent;

- gerarchia;

- dipendenze OCMD.

La Preview dispone di un comando specifico per i livelli della pagina.

Le strutture OCG non deterministiche o malformate vengono gestite in modo conservativo.


# Allegati e Portfolio PDF

Dal menu di apertura/documento è possibile accedere a:

- **Allegati PDF**;

- **Portfolio PDF**.

Il modello Portfolio conserva:

- file incorporati;

- metadati;

- schema;

- ordinamento;

- modalità di visualizzazione;

- struttura logica.

Gli allegati non vengono eseguiti automaticamente.


# Proprietà e metadati

PDFVC utilizza un unico modello per i metadati documentali.

Possono essere gestiti:

- Info Dictionary;

- XMP;

- proprietà personalizzate.

Le proprietà del documento sono accessibili direttamente dal menu principale.


# Redazioni sicure

PDFVC distingue una semplice copertura grafica dalla **redazione fisica del contenuto**.

Il flusso comprende:

1. marcatura delle aree da redigere;

2. applicazione della redazione;

3. rimozione fisica del contenuto interessato;

4. verifica del PDF risultante.

Sono disponibili:

- marcatura manuale;

- **Cerca e redigi**;

- applicazione delle redazioni;

- report di redazione e verifica.

La verifica controlla anche la possibile permanenza del contenuto in elementi quali:

- testo;

- OCR;

- metadati;

- commenti;

- allegati;

- form;

- livelli;

- contenuto fuori pagina.

Quando necessario, il fallback raster viene confinato alle sole pagine che non possono essere ripulite in modo verificabile attraverso il percorso strutturale.


# Sicurezza e pulizia documento

Il comando **Sicurezza / Pulizia documento** permette di applicare operazioni di sanitizzazione del PDF.

La pipeline produce un candidato, esegue la riscrittura necessaria e verifica le categorie di contenuto dichiarate prima del salvataggio.

Sono inoltre previste funzioni di protezione/cifratura del documento.


# Firme digitali

PDFVC comprende un sottosistema dedicato all'analisi delle firme PDF.

Il parser riconosce elementi come:

- campi firma;

- widget;

- `ByteRange`;

- contenuto CMS;

- DocMDP;

- FieldMDP;

- Lock;

- DSS;

- VRI.

La verifica mantiene separati gli aspetti relativi a:

- struttura;

- integrità;

- certificato;

- catena;

- revoca;

- timestamp;

- modifiche successive alla firma.

Il motore può utilizzare WebCrypto/PKIjs e gestisce separatamente la valutazione della fiducia e delle informazioni eIDAS quando queste possono essere determinate in modo attendibile.

Le firme già sottoscritte sono trattate come contenuto protetto/read-only durante l'editing ordinario.


# Accessibilità e PDF/UA

PDFVC contiene strumenti per l'accessibilità documentale e la produzione/analisi di PDF strutturati.

Il modello può comprendere:

- struttura logica;

- associazione degli elementi alle pagine;

- MCID;

- OBJR;

- ParentTree;

- StructTreeRoot.

È presente un dialog dedicato **Accessibilità / PDF/UA**.

La conformità strutturale e la validazione formale vengono mantenute come concetti distinti.


# Preflight

Il **Controllo preflight** analizza il documento secondo differenti profili.

Tra i profili previsti figurano:

- stampa;

- archivio;

- web;

- controllo generale;

- PDF/A-1b;

- PDF/A-2b;

- PDF/A-3b;

- PDF/A-4;

- PDF/X-1a:2001;

- PDF/X-4;

- PDF/UA.

Il preflight può analizzare, tra l'altro:

- struttura;

- font;

- form;

- appearance;

- accessibilità;

- Output Intent;

- caratteristiche incompatibili con il profilo scelto.

La validazione formale esterna, quando disponibile, viene distinta dai soli controlli strutturali interni.


# Colore e prestampa

Gli strumenti **Colore e prestampa** comprendono funzioni per il trattamento delle caratteristiche prepress del PDF, compresa la gestione degli Output Intent e delle relative trasformazioni.


# Decorazioni documento

Il sistema **Decorazioni** permette di applicare elementi ricorrenti alle pagine.

Sono previsti:

- intestazioni e piè di pagina;

- numerazione Bates;

- watermark;

- background.

Le decorazioni possono avere uno scope di pagine specifico e possono utilizzare testo, immagini o pagine PDF come risorse.

Background e foreground vengono inseriti rispettando l'ordine di composizione del documento.


# Ottimizzazione e compressione

Il comando **Ottimizza** utilizza una pipeline dedicata per ridurre o trasformare il documento.

Sono inoltre disponibili:

- **Comprimi e riduci**;

- ottimizzazione delle immagini;

- downsampling progressivo;

- scelta JPEG/PNG in funzione del contenuto;

- rasterizzazione quando esplicitamente richiesta.

Il sistema evita upscale informativo delle immagini e conserva il contenuto vettoriale quando possibile.


# Rilevamento pagine bianche

PDFVC può analizzare le pagine attraverso un rendering ridotto per individuare le pagine presumibilmente vuote.

La rimozione avviene solo dopo conferma.


# Confronto tra PDF

Il comando **Confronta documenti PDF** utilizza un motore isolato dal modello del documento aperto.

Il confronto può utilizzare:

- testo;

- raster;

- layout.

Le pagine possono essere classificate come:

- unchanged;

- modified;

- moved;

- moved + modified;

- replaced;

- added;

- deleted.

È possibile produrre un report HTML autosufficiente del confronto.


# Salvataggio ed esportazione

PDFVC offre differenti modalità di output.

## PDF standard

Il pulsante **Salva** produce il normale output PDF.

La pipeline cerca di preservare il contenuto vettoriale e applica le modifiche secondo un ordine deterministico.

## Salva avanzato

Il menu:

**Salva → Salva tutti come… → Salva avanzato…**

permette di utilizzare le opzioni avanzate di esportazione.

Un corrispondente comando **Salva avanzato…** è disponibile anche per la selezione di pagine.

## Salvataggio selezione

È possibile esportare soltanto le pagine selezionate come:

- PDF;

- PDF/A;

- immagini;

- PDF rasterizzato;

- output avanzato.

## PDF/A

Sono disponibili output dedicati alla famiglia PDF/A, in funzione delle capacità del profilo scelto.

## Immagini

Le pagine possono essere esportate come immagini, utilizzando JPEG o PNG in base al tipo di contenuto.

## Raster

È possibile produrre deliberatamente un PDF completamente rasterizzato.

## PDF ricercabile

L'OCR può essere incorporato per produrre un PDF ricercabile.

## Office

Il comando **Esporta HTML / DOCX / RTF** permette di esportare il contenuto verso:

- HTML;

- DOCX;

- RTF.

## Dividi PDF

Il comando **Dividi PDF** permette di generare più documenti a partire dal PDF corrente.


# Progetti `.vcp`

PDFVC dispone di un proprio formato progetto:

**`.vcp`**

Il progetto può conservare il modello di lavoro e gli asset necessari a proseguire una sessione di editing.

Sono disponibili:

- **Apri progetto .vcp**;

- **Salva progetto .vcp**.


# Recovery e autosalvataggio

La versione desktop utilizza un sistema di recovery basato sul runtime Neutralino.

Sono previste:

- persistenza dello stato;

- snapshot;

- riapertura degli ultimi snapshot;

- journal delle scritture;

- recovery dopo interruzioni;

- gestione sicura della pubblicazione dei file.

I file recenti memorizzano percorso e metadati, non una copia completa dei byte del documento.


# Elaborazione batch

PDFVC comprende una modalità di **conversione batch** per elaborare più file attraverso le pipeline dell'app.

Tra le azioni utilizzabili nel batch figurano:

- PDF ricercabile;

- compressione;

- ottimizzazione;

- decorazioni/stamper;

- rimozione pagine bianche;

- deskew.

Gli errori vengono isolati per singolo file, evitando che un documento problematico interrompa necessariamente l'intero batch.


# Interfaccia multilingua

La UI è predisposta per:

- **Italiano**;

- **English**.

Testo visibile, tooltip e attributi ARIA sono gestiti insieme dal sistema di internazionalizzazione.


# Web e Desktop

PDFVC condivide la stessa applicazione tra i due ambienti.

## Web

La versione browser è una applicazione statica JavaScript.

Il filesystem e lo storage utilizzano le API disponibili nel browser.

## Desktop

La versione desktop utilizza **Neutralino** e aggiunge funzionalità native come:

- filesystem;

- file picker;

- storage persistente;

- recovery;

- gestione sicura delle scritture;

- CLI;

- elaborazione batch;

- single-instance handling.


# Tecnologia

PDFVC è sviluppato principalmente in **JavaScript ESM**, senza framework applicativo e senza TypeScript.

Tra le librerie utilizzate figurano:

- **PDF.js** — rendering e analisi PDF;

- **pdf-lib** — manipolazione PDF;

- **MuPDF.js** — normalizzazione e trasformazioni PDF;

- **Tesseract.js** — OCR;

- **PKIjs** — infrastruttura crittografica e certificati;

- **fontkit** — gestione font;

- **JSZip** — archivi;

- **docx-preview** — supporto DOCX;

- **odf-kit** — supporto ODT;

- **bwip-js** — barcode;

- **html2canvas** — rendering ausiliario.

Il runtime desktop utilizza **Neutralino**.


# Architettura

L'applicazione utilizza un modello documento centrale.

Le principali autorità dello stato comprendono:

- pagine e sorgenti;

- moduli;

- commenti;

- OCR;

- navigazione;

- livelli;

- accessibilità;

- allegati;

- metadati;

- firme;

- decorazioni;

- report preflight.

Le azioni condivise da toolbar, menu, hotkey e test passano attraverso un command registry/controller comune.

La cronologia utilizza transazioni in modo che una singola azione dell'utente generi, per quanto possibile, un solo gruppo Undo/Redo.


# Fedeltà di rendering

Uno degli obiettivi principali di PDFVC è mantenere la corrispondenza fra:

1. PDF sorgente;

2. rendering iniziale;

3. Preview modificata;

4. PDF esportato.

Il rendering iniziale del PDF sorgente viene considerato l'autorità visiva.

Per questo motivo l'app cerca di:

- conservare il vettoriale;

- riutilizzare geometria e metriche originarie;

- identificare gli operatori PDF coinvolti;

- sopprimere soltanto il paint sostituito;

- preservare il contenuto vicino all'oggetto modificato;

- utilizzare un fallback raster soltanto quando il percorso strutturale non è sufficientemente sicuro.


# Limitazioni note

PDF è un formato di presentazione, non un formato sorgente pensato per l'editing. Alcuni documenti contengono programmi grafici estremamente complessi o ambigui.

Nella versione corrente esistono pertanto limitazioni note in aree quali:

- pattern PDF complessi;

- shading non deterministici;

- soft mask con programmi grafici arbitrari;

- alcuni font Type 3;

- casi nei quali non è disponibile una identità strutturale univoca dell'operatore PDF;

- OCG/livelli malformati o ciclici;

- reflow quando non può essere dimostrata una materializzazione completa e reversibile;

- immagini per le quali il PDF non conserva informazioni sufficienti per ricostruire il contenuto originario;

- raggruppamenti visuali intrinsecamente ambigui;

- campi modulo privi di una appearance originaria valida.

In questi casi PDFVC privilegia una strategia **fail-closed**, la conservazione del contenuto o un fallback localizzato rispetto a una modifica distruttiva non verificabile.

Per i dettagli tecnici aggiornati vedere `OPEN\_ISSUES.md`.


# Avvio in sviluppo

## Requisiti

- Node.js;

- npm;

- PowerShell per gli script Windows del progetto.

Installare le dipendenze:

```
`npm install`
```

Avviare il server di sviluppo:

```
`npm start`
```

Quindi aprire:

```
`http://127.0.0.1:4173`
```

È disponibile anche:

```
`npm run serve`
```


# Build desktop

Per sincronizzare le risorse Neutralino:

```
`npm run neutralino:sync`
```

Per creare la build Windows:

```
`npm run neutralino:build`
```

Sono inoltre presenti script `.bat` dedicati alla build e al deploy dell'eseguibile.


# Test e QA

Il progetto utilizza principalmente:

- **Vitest** per i test unitari;

- **Playwright** per i test end-to-end.

Sono inoltre disponibili audit e strumenti specifici per alcune aree, compresi i controlli i18n e la diagnostica degli export.

Esempio:

```
`npm run test:i18n`
```

Per analizzare una traccia diagnostica di export:

```
`npm run pdfvc:export-replacement-trace -- \<trace.json\>`
```


# Principi del progetto

PDFVC segue alcuni principi fondamentali:

- preservare il contenuto vettoriale quando possibile;

- evitare modifiche distruttive non dimostrabili;

- mantenere Preview ed export coerenti;

- utilizzare un solo modello documento;

- mantenere Undo/Redo transazionale;

- preferire modifiche localizzate alle riscritture integrali;

- utilizzare rasterizzazione solo come fallback esplicito;

- verificare il PDF dopo le trasformazioni critiche;

- mantenere le operazioni lunghe cancellabili e responsive quando possibile;

- evitare dipendenze o complessità non necessarie.


## PDF Visual Composer

**PDFVC** è pensato come un ambiente unico per passare dalla semplice organizzazione delle pagine alla modifica visuale, all'OCR, alla gestione strutturale e alla verifica tecnica del PDF, mantenendo come priorità la fedeltà al documento originale.

