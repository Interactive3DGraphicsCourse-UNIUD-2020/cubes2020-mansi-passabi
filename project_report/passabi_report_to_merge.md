## 1 Novembre

### Passabi

- Creato modello fungo rosso e grigio + test
  - NB: per le texture abbiamo deciso di usare delle skin gratuite usate per delle mod di MineCraft 
  - TODO: la parte trasparente non dovrebbe fare ombra --> da fixare

- Riscontrato problema sulle pale del mulino
  - Se viene chiamata in Update la rotazione prima che il modello sia caricato al 100% si generano degli errori
  - Risolto con un controllo sul tipo di oggetto prima di effettuare la rotazione

- Completato il modello del mulino
- Commit su Git

---

## 2 Novembre

### Passabi

- Creato branch per sperimentare con luci e ombre
- Riscontrato problema quando vengono cambiate le impostazioni usando la funzione *onDocumentKeyDown*
  - Soluzione: implementare una GUI --> primi test con div HTML e CSS

- Implementazione GUI
  - CSS simile al contatore FPS
  - Implementato il controllo musica ON/OFF
  - Implementata la gestione della qualita della luce direzionale
  - Implementate informazioni sulla mappa e visualizzazione di Heightmap usata
  
- Modellazione alberi
  - modello albero di mele

- Creato branch per la modifica di alcuni modelli
  - perfezionato albero di mele (aggiunta trasparenza)
  - modificato il tetto del mulino
  - sistemate alcune ombre non corrette del mulino
  - aggiunte ragnatele al mulino
  - aggiunto albero tipo betulla (versione normale)
  - aggiunto albero tipo betulla (versione autunno)

- Idea: personaggio incorporeo (fantastimo) che fluttua sulla mappa e rende possibile visitare il mondo

- Idea: aggiungere occlusione ambientale
  - ricerche
  - primi test su 2 cubi (uno con AO, uno senza)
  - aggiunta dell'AO sul mulino
  - vari test sulle altre impostazioni disponibili in three js editor - fallimentari, nulla di utile al momento

## 4 Novembre

### Passabi

- Fix minori codice
- Modifiche alla GUI per quanto riguarda la gestione delle ombre
