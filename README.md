# Flocking Simulation

Progetto di programmazione realizzato da **Leo, Telly e Alessio**.

## Descrizione

Il progetto consiste nella realizzazione di una **flocking simulation**, ovvero una simulazione del comportamento collettivo di uno stormo di uccelli.

Informazioni complete sono presenti in /docs/Relazione progetto.

La simulazione è basata sul modello dei **Boids**, introdotto da Craig Reynolds, in cui il comportamento complesso dello stormo emerge dall'interazione di singoli agenti che seguono semplici regole locali.

Ogni agente, chiamato **boid**, modifica la propria velocità e direzione in base alla posizione e al movimento dei boid vicini.

## Obiettivo

L'obiettivo del progetto è studiare e implementare un sistema multi-agente in cui semplici regole individuali producono un comportamento collettivo simile a quello osservabile in uno stormo.

In particolare, il programma simula l'interazione tra i boid e l'evoluzione dello stormo nel tempo.

## Flocking

Il comportamento dei boid è determinato principalmente da tre regole:

### Separation

La **separation** permette ai boid di evitare collisioni e di mantenere una certa distanza dai propri vicini.

Quando un altro boid si trova troppo vicino, l'agente tende a muoversi nella direzione opposta.

### Alignment

L'**alignment** porta ogni boid ad allineare la propria direzione e velocità con quelle dei boid presenti nelle vicinanze.

In questo modo gli agenti tendono a muoversi nella stessa direzione dello stormo.

### Cohesion

La **cohesion** permette ai boid di rimanere vicini allo stormo.

Ogni agente tende a dirigersi verso la posizione media dei propri vicini, evitando così che il gruppo si disperda.

Le tre regole vengono combinate per determinare il movimento finale di ogni boid.

## Struttura del progetto

I principali file del progetto sono:

```text
.
├── CMakeLists.txt
├── main.cpp
├── boid.cpp
├── boid.hpp
├── flock.cpp
├── flock.hpp
├── vector.cpp
├── vector.hpp
├── boid.test.cpp
├── flock.test.cpp
├── vector.test.cpp
└── DL_exercise_0.ipynb
```

### `Boid`

`boid.cpp` e `boid.hpp` contengono l'implementazione del singolo agente della simulazione.

### `Flock`

`flock.cpp` e `flock.hpp` gestiscono lo stormo e l'interazione tra i diversi boid.

### `Vector`

`vector.cpp` e `vector.hpp` implementano le operazioni matematiche necessarie per rappresentare e modificare posizione, velocità e direzione.

### Test

I file:

* `boid.test.cpp`
* `flock.test.cpp`
* `vector.test.cpp`

contengono i test delle principali componenti del progetto.

## Tecnologie

Il progetto utilizza:

* **C++**
* **CMake**
* **GoogleTest** per i test
* **Jupyter Notebook** per l'esercizio di Deep Learning incluso nel progetto

## Compilazione

Per compilare il progetto utilizzando CMake:

```bash
mkdir build
cd build
cmake ..
cmake --build .
```

Dopo la compilazione è possibile eseguire il programma tramite l'eseguibile generato da CMake.

## Testing

I test automatici permettono di verificare il corretto funzionamento delle componenti principali del progetto.

Dopo la compilazione, i test possono essere eseguiti tramite:

```bash
ctest
```

## Risultati

La simulazione mostra come il comportamento collettivo possa emergere senza la necessità di un leader centrale.

Ogni boid prende decisioni sulla base delle informazioni locali relative ai propri vicini; dalla combinazione di queste decisioni emerge il comportamento globale dello stormo.


#### Progetto realizzato per il corso di Programmazione per la Fisica nell'anno 2022/2023
