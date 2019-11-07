# Voxel Heightmap Terrain Generator - Mansi & Passabì

--> ADD: IMMAGINE(gif) DI PRESENTAZIONE

## Descrizione 

Il progetto propone un algoritmo di generazione di terreni in stile voxel.
L'algoritmo prende in input una heightmap (un'immagine in scala di grigi) e genera il terreno con una conformazione che richiama quella rappresentata dall'immagine, interpretando la gradazione di grigio di ciascun pixel come l'altezza che dovrà avere il terreno in quella determinata cordinata.

L'algoritmo di generazione permette di popolare il terreno con della vegetazione (ad esempio cespugli,rocce,alberi): questi oggetti sono posizionati randomicamente sulla superfice del terreno, e ad essi vengono applicate delle piccole trasformazioni randomiche per renderli meno ripetitivi. La loro quantità dipende dai parametri di densità scelti; anch'essi specificabili.

È inoltre possibile scegliere quale texture applicare ai blocchi superficiali, sottostanti, all'acqua etc. etc. per cambiare l'aspetto della scena.

Altri parametri forniti per controllare la generazione del terreno sono:
- altezza_max_terreno: un valore che permette di regolare l'altezza massima che deve avere il terreno. 
- sea_level: Permette di decidere il livello del mare.
- wireframe_view: permette di attivare o meno la visualizzazione del mesh finale in modalità wireframe.
- enable_vegetation: permette di attivare o disattivare la generazione di vegetazione nel terreno.

Altre caratteristiche:
- Il terreno viene generato con il numero minore di triangoli possibili. Ogni cubo è formato dalle sole facce necessarie per la sua corretta visualizzazione nel contesto di un terreno: Non vengono istanziate facce di cubi che non verrebbero visualizzate in quanto "nascoste". L'algoritmo quindi rimuove l'overhead di poligoni che si avrebbe con un approccio più naive.
- Nella scena in cui viene presentato il terreno è presente una GUI:
  - la gui permette bla bla bla AGGIUNGERE



## Screenshot dimostrative features presenti
--> ADD: 

## Screenshot terreni generati
--> ADD: 

## Idee non implementate
Segue una lista di idee che non sono stato implementate:
- GUI che permetta di modificare i paramatri di generazione del terreno e lanciare un nuovo processo di generazione (così da evitare di dover modificare le variabile nel codice ogni volta e rendere il programma interattivo con l'utente).
- Generare delle nuovole animate sopra il terreno, la cui generazione viene controllata da determinati parametri (ad es: densità,altezza,opacità).
- Aggiunta di altri modelli di vegetazione per rendere la scena più variabile.
- Aggiunta di animazioni della vegetazione (laddove sensato: alberi,cespugli) che reagiscano ad un parametro "wind_speed".
- Shader per il mesh dell'acqua


add screenshots

## Tools Utilizzati
- Three.js
- Three.js editor
- Visual studio code
- GitHub
- Chrome & Brave Browser

Hardware su cui sono state testate le performance:

- Mansi:
  - i7 9700k@5Ghz - Nvidia RTX2070
  - i5 8250U - Nvidia 940MX
- Daniele:
  - i7 9700k@4.6Ghz - Nvidia RTX2070S
  - 

Alcune considerazioni:
- L'algoritmo non pone restrizioni sulla complessità del terreno da generare: Usare un'immagine heightmap nxn comporta la generazione di un terreno nxn che avrà quindi nxn cubi superficiali più tutti quelli sottostanti in caso di presenza di dislivelli nel terreno. La complessità risulta essere quindi principalmente legata alla dimensione dell'immagine e da quanto irregolare essa sia. Sono stati effettuati alcuni test ed è stato possibile generare una scena da circa 4.5M di poligoni mantenendo un framerate di circa 60-100fps sulle configurazioni desktop citate con una heightmap di 1000x1000.
