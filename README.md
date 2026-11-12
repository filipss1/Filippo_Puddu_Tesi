# Agentic AI for Blockchain-Based Software Analysis and Implementation

Repository ufficiale del materiale e dei risultati sperimentali per la tesi di laurea in Informatica.

---

## Panoramica del Progetto

Questo repository raccoglie il materiale e i risultati sperimentali della tesi **"Agentic AI for Blockchain-Based Software Analysis and Implementation"**.

Il lavoro si propone di analizzare le capacità dei modelli linguistici di grandi dimensioni (**Large Language Models, LLM**) nell'ambito dello sviluppo software blockchain, concentrandosi su due attività principali: l'analisi del codice sorgente di progetti blockchain esistenti e la generazione di nuove applicazioni decentralizzate (**dApp**).

L'obiettivo è confrontare diversi modelli eseguiti localmente, valutandone le capacità di comprensione del codice, individuazione di problemi di sicurezza, generazione di applicazioni funzionanti e correzione degli errori prodotti durante lo sviluppo.

---

## Modelli e Ambiente di Esecuzione

Gli esperimenti sono stati condotti utilizzando tre modelli linguistici locali, operanti con una finestra di contesto pari a **131.072 token**.

| Modello | Finestra di Contesto | Strumenti di Esecuzione | Ambiente Hardware |
| :--- | :---: | :--- | :--- |
| **GPT-OSS 20B** | 131.072 token | Ollama / OpenCode CLI | Macchina virtuale universitaria / Workstation remota |
| **Qwen 3.5 9B** | 131.072 token | Ollama / OpenCode CLI | Macchina virtuale universitaria / Workstation remota |
| **Gemma 4 12B** | 131.072 token | Ollama / OpenCode CLI | Macchina virtuale universitaria / Workstation remota |

---

## Attività Sperimentali

La ricerca è stata organizzata in due principali attività sperimentali:

### Task 3 – Analisi del Codice Sorgente Blockchain
Applicazione dei modelli all'analisi del codice sorgente di tre progetti blockchain, selezionati per differenti architetture e livelli di complessità.

*   **Bitcoin Core:** Analisi dell'interprete degli script, della validazione delle transazioni e delle funzionalità Taproot.
*   **go-ethereum:** Analisi dell'Ethereum Virtual Machine (EVM), della gestione del gas e del processo di transizione dello stato.
*   **Qubic:** Analisi dell'ambiente di esecuzione degli smart contract e della sua integrazione con il meccanismo di consenso.

> **Metriche di Valutazione:** Accuratezza, completezza, latenza, utilizzo della finestra di contesto, identificazione di componenti critici per la sicurezza e potenziali vulnerabilità.

### Task 4 – Generazione di Applicazioni Decentralizzate (dApp)
Valutazione della capacità dei modelli di progettare e realizzare dApp basate su funzionalità specifiche delle piattaforme blockchain, partendo da una descrizione iniziale del progetto.

*   **Bitcoin Taproot:** Generazione di applicazioni che utilizzano il meccanismo *Script Path*.
*   **Ethereum EIP-7702:** Generazione di applicazioni basate sulla delega degli account e sull'esecuzione di codice tramite smart contract.

> **Flusso di Lavoro:** Le dApp generate sono state sottoposte a test funzionali e blockchain. In caso di errore, il modello originale è stato coinvolto in cicli di correzione iterativa per valutarne la capacità di self-debugging.

---

## Struttura del Repository

Il repository è organizzato nelle seguenti categorie:

```text
├── criteria/              # criteri di valutazione spiegati
├── README.md/                # file di spiegazione del progetto
├── prompt/              # insieme di prompt utilizzati
└── task_sourcecode/                 # link a drive per scaricare i task 3 e 4 e il codice sorgente dei codebase
