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



