# Iron Lung Navigator - AT-5 Trench

Pagina web **HTML standalone** con mappa interattiva per **Iron Lung**, pensata per aiutare la navigazione nella zona **AT-5 Trench**.

Il progetto è stato realizzato per essere:
- usato **in locale**, aprendo direttamente il file `.html` nel browser;
- pubblicato su hosting statici come **Altervista** o **GitHub Pages**;
- semplice da modificare, perché non richiede backend o dipendenze esterne.

## A cosa serve

Questa pagina permette di:
- inserire le **coordinate attuali** del sottomarino (`X` e `Y`);
- vedere la propria posizione direttamente sulla mappa;
- scegliere una **destinazione** cliccando sulla mappa;
- ottenere l'**angolo di navigazione** da tenere per dirigersi verso il punto selezionato;
- confrontare l'angolo suggerito con il proprio **angolo attuale** (`A`), se inserito manualmente.

In pratica, funziona come un piccolo navigatore dedicato alla mappa del gioco.

## Funzioni principali

- **Mappa interattiva** con posizione corrente e target visibili
- **Selettore lingua** integrato
- Lingue disponibili:
  - Italiano
  - English
  - Français
  - Español
  - Deutsch
  - Русский
  - 中文
- **Click mode** configurabile:
  - `L Click = posizione / position` 
  - `L Click = target / target`
- **R Click** sempre assegnato all'impostazione della posizione corrente
- Calcolo automatico di:
  - coordinate correnti
  - coordinate target
  - distanza in linea retta
  - heading suggerito
  - differenza rispetto all'heading attuale
- **Preset per gli angoli**, utili per adattarsi a diverse interpretazioni della convenzione X/Y e dell'orientamento nella community

## Come si usa

### 1) Apri la pagina

Apri il file HTML direttamente nel browser.
Non serve installare nulla.

### 2) Imposta la tua posizione attuale

Puoi farlo in due modi:
- scrivendo manualmente i valori nei campi **X** e **Y**;
- usando la mappa:
  - **R Click** sulla mappa = imposta sempre la posizione attuale
  - oppure selezionando il pulsante **L Click = posizione** e poi facendo click sinistro sulla mappa

### 3) Imposta la destinazione

Anche qui hai due possibilità:
- inserire manualmente le coordinate target, se previsto nella tua versione;
- oppure usare il pulsante **L Click = target** e fare click sinistro sulla mappa nel punto desiderato

### 4) Leggi il risultato

Dopo aver impostato posizione e destinazione, la pagina calcola automaticamente:
- la **distanza in linea retta**;
- l'**angolo assoluto** da tenere verso il target;
- l'eventuale **correzione di rotta** rispetto al tuo angolo attuale (`A`), se lo hai inserito.

## Controlli rapidi

- **L Click = posizione** → il click sinistro imposta la posizione attuale
- **L Click = target** → il click sinistro imposta la destinazione
- **R Click sulla mappa** → imposta sempre la posizione attuale
- **Swap** → scambia posizione corrente e target
- **Language** → cambia subito tutte le etichette della pagina

## Come funziona il calcolo

La pagina prende:
- la tua posizione corrente;
- la posizione del punto selezionato;
- la differenza tra le due coordinate.

Da questi valori ricava l'**angolo di navigazione** verso la destinazione.

### Importante

Il calcolo attuale è fatto **in linea retta** tra il punto attuale e il target.

Questa versione **non esegue pathfinding automatico** lungo i corridoi o i tunnel del trench.
Quindi:
- è perfetta come riferimento rapido di orientamento;
- non evita automaticamente pareti, curve o percorsi obbligati.

Se necessario, il progetto può essere esteso con:
- percorso guidato lungo i corridoi;
- waypoint intermedi;
- calcolo automatico del tragitto navigabile.

## Compatibilità

La pagina è compatibile con i normali browser moderni, ad esempio:
- Chrome
- Edge
- Firefox
- Opera

Non richiede:
- server backend
- database
- framework JavaScript
- installazioni aggiuntive

## Pubblicazione online

### Altervista

Puoi caricare direttamente il file HTML e gli eventuali asset associati via pannello o FTP.
Una volta caricati, la pagina funzionerà come normale sito statico.

### GitHub Pages

Puoi pubblicare il progetto anche su GitHub Pages:
1. crea un repository;
2. carica il file HTML;
3. aggiungi questo `README.md`;
4. abilita GitHub Pages nelle impostazioni del repository.

## Struttura consigliata del repository

```text
/
├─ index.html
├─ README.md
└─ eventuali asset locali
```

Se vuoi usare un nome file diverso da `index.html`, va bene lo stesso, ma per GitHub Pages `index.html` è la scelta più comoda.

## Personalizzazione

Puoi modificare facilmente:
- testi e traduzioni;
- preset angolari;
- aspetto grafico;
- dimensioni e comportamento della mappa;
- marker di posizione e destinazione.

## Limitazioni attuali

- nessun pathfinding nei corridoi;
- calcolo diretto in linea retta;
- precisione legata alla corrispondenza tra mappa visualizzata e coordinate usate nel gioco;
- convenzione degli angoli dipendente dal preset selezionato.

## Obiettivo del progetto

L'obiettivo è fornire uno strumento semplice e immediato per navigare meglio nella mappa di **Iron Lung**, senza dover calcolare a mano direzioni e orientamento ogni volta.

---

Se vuoi, questo README può essere ampliato con:
- screenshot;
- GIF dimostrative;
- sezione FAQ;
- changelog;
- istruzioni tecniche per sviluppatori.
