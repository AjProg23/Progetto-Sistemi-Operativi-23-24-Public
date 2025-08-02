# Progetto Sistemi Operativi: Simulazione Reattore Nucleare

Progetto Sistemi Operativi (SO) UniTo anno 2023-2024

***NB! Questo repository contiene solo una descrizione del progetto.
Il codice sorgente completo non è pubblicato per rispettare le linee guida accademiche dell'Università.
Può essere condiviso privatamente su richiesta***.

## Introduzione

Il progetto consiste nello sviluppo di una simulazione 
di un reattore nucleare implementata utilizzando i meccanismi di 
Inter-Process Communication (IPC) del sistema operativo Unix/Linux. 
La simulazione gestisce diversi processi che cooperano per simulare la produzione 
di energia attraverso reazioni nucleari, la gestione degli atomi, l'alimentazione del 
reattore e l'attivazione delle reazioni.

## Tecnologie e Strumenti Usati

### Linguaggi e Tecnologie
• **C** - Linguaggio di programmazione principale
• **System V IPC** - Meccanismi di comunicazione inter-processo
• **Shared Memory** - Memoria condivisa per comunicazione tra processi
• **Message Queues** - Code di messaggi per sincronizzazione
• **Semafori** - Sincronizzazione e mutua esclusione

### Strumenti di Sviluppo
• **GCC** - Compilatore C
• **Make** - Sistema di build automation
• **Shell Unix/Linux** - Ambiente di esecuzione

### Sistema Operativo
• **Linux/Unix** - Sistema operativo target per l'esecuzione

## Contenuto Relazione Finale
La relazione finale comprende tutta la documentazione dettagliata del progetto e la sua architettura:

La simulazione è composta da quattro processi principali:

1. **Master** - Processo coordinatore che gestisce la simulazione globale
2. **Atomo** - Processi che rappresentano gli atomi nel reattore
3. **Alimentazione** - Processo che gestisce l'alimentazione del reattore
4. **Attivatore** - Processo che attiva le reazioni nucleari


## Contenuto Codice

Il codice sorgente è organizzato nella directory `src/` e include:

### File Principali
• **Master.c** - Processo coordinatore principale
• **Header.h** - Include globali e definizioni
• **Strutture.h** - Definizione delle strutture dati
• **Semafori.h** - Gestione dei semafori
• **my_sem_lib.c/h** - Libreria personalizzata per semafori

### Moduli Specializzati
• **Atomo/** - Implementazione del processo Atomo
• **Alimentazione/** - Gestione dell'alimentazione del reattore
• **Attivatore/** - Controllo dell'attivazione delle reazioni

### Caratteristiche Implementate
• **Gestione Multi-processo** - Coordinamento di processi concorrenti
• **Sincronizzazione** - Uso di semafori per controllo accessi
• **Comunicazione IPC** - Message queues e shared memory
• **Signal Handling** - Gestione corretta della terminazione
• **Statistiche Real-time** - Monitoraggio delle prestazioni del sistema
• **Memory Management** - Gestione corretta della memoria condivisa

## Compilazione ed Esecuzione

### Prerequisiti
• Sistema Unix/Linux
• Compilatore GCC
• Make utility

### Compilazione
```bash
make all
```

### Pulizia
```bash
make clean
```

### Esecuzione
```bash
make run
```

## Configurazione

Il file `Config.txt` contiene i parametri di configurazione del sistema:
• Numero di atomi iniziali
• Parametri di temporizzazione
• Soglie di energia
• Altri parametri di simulazione
