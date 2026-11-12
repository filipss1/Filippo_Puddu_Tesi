# Task 2: Selezione dei Modelli e degli Strumenti

Questo documento descrive le motivazioni tecniche e i criteri adottati nella scelta dei modelli linguistici e degli strumenti di sviluppo agentico impiegati per la sperimentazione e la valutazione all'interno del presente lavoro di tesi.

---

## 1. Criteri e Selezione dei Modelli Linguistici

Per condurre le attività di analisi del codice sorgente e di generazione di applicazioni decentralizzate (dApp), l'obiettivo principale è stato individuare modelli in grado di bilanciare elevate capacità di ragionamento con i vincoli hardware imposti dall'ambiente di esecuzione locale. 

La selezione si è concentrata su tre modelli specifici (`gpt-oss:20b`, `qwen3.5:9b` e `gemma4:12b`), scelti in base ai seguenti requisiti chiave:

*   **Capacità di Ragionamento (*Thinking*):** I modelli selezionati integrano avanzate capacità logiche e di pianificazione passo-passo, fondamentali per gestire compiti complessi di ingegneria del software, scomposizione dei requisiti e debug iterativo del codice.
*   **Ampia Finestra di Contesto (≥ 130.000 token):** Ciascuno dei modelli è stato configurato per operare con una finestra di contesto pari a **131.072 token**. Questa caratteristica è risultata imprescindibile per permettere agli agenti di elaborare interamente codebase estese e complesse (come parti di Bitcoin Core, go-ethereum e Qubic) in maniera completa, senza perdere i riferimenti strutturali tra i file.

---

## 2. Selezione dell'Ambiente di Sviluppo Agentico: OpenCode

Per l'interazione pratica tra i modelli linguistici e il file system del progetto, la scelta è ricaduta su **OpenCode**. 

Rispetto ad altre soluzioni valutate durante la fase preliminare, OpenCode si è dimostrato lo strumento ideale per i seguenti motivi:

*   **Esperienza d'uso intuitiva:** Offre un'interfaccia e un flusso di lavoro estremamente lineari, che riducono al minimo la curva di apprendimento e facilitano il controllo diretto sulle operazioni eseguite dall'agente.
*   **Leggerezza e installazione da terminale:** Trattandosi di uno strumento interamente gestibile via CLI (Command Line Interface) direttamente nel terminale, si integra in modo nativo con tutti gli ambienti di sviluppo, risultando estremamente veloce da configurare.
*   **Assenza di applicazioni esterne:** A differenza di ambienti dotati di interfacce grafiche pesanti o dipendenze proprietarie, OpenCode opera in autonomia sfruttando direttamente il motore di inferenza locale (Ollama) e i file di progetto, garantendo massima efficienza e totale controllo sui flussi di lavoro.