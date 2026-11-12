# Criteri di Valutazione — Code Analysis

La valutazione dell'attività di analisi del codice sorgente blockchain (Task 3) si basa su quattro metriche quantitative e qualitative fondamentali: **Accuracy**, **Completeness**, **Latency** e **Context Token Usage**.

---

### 1. Accuracy (Accuratezza)

* **Domanda:** Quale percentuale delle affermazioni del modello è corretta?
* **Metodo:** Confrontare le affermazioni prodotte dal modello con il codice sorgente originale e fonti autorevoli. Classificare ogni affermazione come *corretta*, *errata* o *non verificabile*.
* **Formula:**

$$\text{Accuracy (\%)} = \left( \frac{\text{Affermazioni corrette}}{\text{Affermazioni verificabili}} \right) \times 100$$

* **Categorie di Classificazione:**
  * **Corretta:** L'affermazione rispecchia fedelmente la logica del codice o le specifiche tecniche.
  * **Errata:** L'affermazione contiene incomprensioni architetturali o descrizioni errate del comportamento del codice.
  * **Non verificabile:** L'affermazione non può essere confermata o smentita in modo definitivo tramite il codice sorgente esaminato.

---

### 2. Completeness (Completezza)

* **Domanda:** Quale percentuale degli elementi richiesti è stata trattata correttamente?
* **Metodo:** Preparare una checklist dettagliata per ciascun progetto blockchain prima di avviare l'analisi. Contare esclusivamente gli elementi effettivamente trattati e spiegati in modo corretto.
* **Formula:**

$$\text{Completeness (\%)} = \left( \frac{\text{Elementi trattati correttamente}}{\text{Elementi attesi}} \right) \times 100$$

* **Parametri di Verifica per Progetto:**
  * **Bitcoin Core:** Interprete degli script, validazione delle transazioni, funzionalità Taproot (Script Path / Key Path).
  * **go-ethereum:** EVM (Ethereum Virtual Machine), gestione del gas, transizione dello stato (State Transition).
  * **Qubic:** Ambiente di esecuzione degli smart contract, integrazione con il meccanismo di consenso.

---

### 3. Latency (Latenza)

* **Domanda:** Quanto tempo impiega il modello a completare l'analisi?
* **Metodo:** Misurare il tempo trascorso dall'invio del prompt fino al completamento della risposta generata, escludendo il tempo di caricamento iniziale del modello in memoria. Ripetere il test almeno **tre volte** per ciascun modello e calcolarne la mediana.
* **Valore da Registrare:** Mediana dei tempi di risposta, espressa in secondi (s).

---

### 4. Context Token Usage (Somma dei Token Utilizzati)

* **Domanda:** Quanti token vengono complessivamente consumati dal modello per completare l'analisi?
* **Metodo:** Estrarre dai log di esecuzione la somma totale dei token impiegati (inclusi i token di input/prompt e i token di output generati).
* **Valore da Registrare:** Somma totale dei token utilizzati (Token Totali = Token di Prompt + Token di Generazione).

---

### Tabella Riassuntiva delle Metriche di Code Analysis

| Metrica | Obiettivo di Misurazione | Metodo di Calcolo / Valutazione | Output Atteso |
| :--- | :--- | :--- | :--- |
| **1. Accuracy** | Affidabilità delle descrizioni tecniche | (Affermazioni corrette / Verificabili) $\times 100$ | Percentuale (%) |
| **2. Completeness** | Copertura dei requisiti di analisi | (Elementi trattati / Elementi attesi) $\times 100$ | Percentuale (%) |
| **3. Latency** | Efficienza temporale di risposta | Mediana su 3 esecuzioni (escluso warm-up) | Secondi (s) |
| **4. Context Token Usage** | Consumo complessivo di risorse testuali | Somma di token di input e di output | Numero totale di token |
