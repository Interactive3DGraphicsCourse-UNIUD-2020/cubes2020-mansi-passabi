## 2 Novembre

### Mansi

- Obiettivi del giorno: analisi del codice, refactoring & ottimizzazione.

  - aggiunta misurazione tempo di generazione del terreno.
  - ottimizzazione fase di generazione del terreno:
    - tramite piccoli accorgimenti sul codice è stato possibile velocizzare la fase di generazione del terreno. Per testare il risultato è stata utilizzata una heightmap di 750x750 la quale è stata generata prima in 14555ms e poi, con le ottimizzazioni effettuate in 8440ms portando a un miglioramento circa pari al 42%.
    Le misurazioni sono frutto della media di diverse misurazioni.
  - Eseguito test di performance dopo l'ottimizzazione del codice: utilizzando un'img in input 1250x1250 il codice è riuscito a generare e visualizzare su schermo in 30.5sec un terreno da 1562500 blocchi superficiali (esclusi quelli delle penedenze) portando la CPU (i7 9700K) costantemente al 100%, un utilizzo della GPU di circa 40% (RTX 2070), e un utilizzo di circa 9GB di memoria primaria.
  - I 4 lati agli estremi del terreno ora non sono più "vuoti" ma viene generata una parete in modo da rendere più piacevole la visione del terreno da distanze elevate; è stato inoltre aggiunto un piano su cui poggia il terreno.
  - è stato fixato un problema che generava erroneamente le "pareti" nei blocchi ai bordi del terreno.

Aggiornata la ROADMAP:

| n° | Features TODO List | Priorita' |
| :---        |    :----:   |          ---: |
| 1 | Fixing dell'algoritmo di generazione/spawning della vegetazione nel terreno: Capire come mergare i mesh e ottimizzare la presenta di un elevato numero di oggetti! | Alta |
| 2 | Idea: Aggiunta di un sistema di generazione di superfici d’acqua. | Bassa |
| 3 | La telecamera si posiziona automaticamente in una posizione coerente in base alle dimensioni del terreno generato (si adatta alle varie dimensioni). | Bassa |



## 3 Novembre

### Mansi:

- rilettura e piccole sistemazioni del codice.
- sistemazione di alcune texture.
- alcune sperimentazioni con l'ottimizzazione degli oggetti caricati tramite ObjectLoader senza alcun risultato.
- visione della lezione sugli shaders.


## 4 Novembre

### Mansi & Passabì:

- Colloquio con il professore a fine lezione relativa alla problematica riscontrata (basse performance con un'alto numero di istanze di oggeti caricati tramite Objectloader).
  - Soluzioni possibili:
    - Eseguire il merge dei vari mesh come effettuato con i cubi(facce) (il mesh del terreno).
    - Condividere geometria e materiale per ciascuna istanza dell'oggeto, al fine di ridurre drasticamente i cambi di contesto effettuati dalla gpu. (in astratto "passare da n oggetti diversi a n istanze di un solo oggetto").


### Mansi:

- Rilettura del codice & aggiornamento del report.
- Aggiornamento della ROADMAP:

| n° | Features TODO List | Priorita' |
| :---        |    :----:   |          ---: |
| 1 | Fixing dell'algoritmo di generazione/spawning della vegetazione nel terreno: Sperimentare le soluzioni proposte precedentemente. | Alta |
| 2 | Introdurre l'entità cespuglio da posizionare randomicamente nella scena (idea: parametro dimensione che varia randomicamente) | Alta |
| 3 | Commentare e fare il refactoring del codice prima della consegna | Obbligatoria |
| 4 | Creazione della scena finale da presentare come lavoro concluso | Obbligatoria | 
| 5 | Valutare come sostituire l'erba billboard non consentita dal progetto in quanto "non fatta a cubi" | Bassa |
| 6 | Implementazione dell'ambient occlusion | Bassa |
| 7 | Aggiunta di qualche shader? sperimentare ed eventualemte aggiungere dove sensato. | Bassa |
| 8 | Idea: Aggiunta di un sistema di generazione di superfici d’acqua. | Bassa |
| 9 | La telecamera si posiziona automaticamente in una posizione coerente in base alle dimensioni del terreno generato (si adatta alle varie dimensioni). | Bassa |

### 5 Novembre

### Mansi:

- Introdotta l'entità cespuglio e completata l'implementazione della sua generazione e posizionamento randomico nel terreno. (Non si è verificato il problema di performance, i cespugli vengono mergiati in un unico mesh alla fine della loro generazione.)
- Pulizia e Commento del codice.
- screenshots, aggiornamento report.md, commit su git.

### 6 Novembre

add meet di gruppo

### Mansi:

- Preparazione del codice e aggiunta della GUI nella scena insieme a Daniele.
- Piccoli ritocchi in varie parti del codice. Aggiunta di piccole features minori.

### 7 Novembre

- Ideazione e implementazione della generazione dell'acqua
- Lavoro sul report e sul readme (presentazione del progetto)
- screenshot, debugging, commento e sistemazione del codice.
- definizione degli obbiettivi finali: concludere entro 08/11 sera.
