# Valutazione della Generazione di dApp tramite Agentic AI

**MODELLI:**
* `gpt-oss:20b`
* `qwen3.5:9b`
* `gemma4:12b`

**PIATTAFORME:**
* Bitcoin Taproot
* Ethereum EIP-7702

**OBIETTIVO:**
Misurare quanti passaggi aggiuntivi richiede ciascun modello locale per rendere funzionale la propria dApp generata.

---

## FASE 0 - STUDIO PILOTA

### STEP 1 - Archiviazione del Lavoro Precedente
* Archiviare i precedenti esperimenti del Task 4 come studio pilota.
* Escludere i risultati dello studio pilota dai risultati ufficiali.
* Non utilizzare le versioni corrette da ChatGPT nei risultati ufficiali.

---

## FASE 1 - BITCOIN TAPROOT

### STEP 2 - Generazione delle Proposte di dApp
* **Per ciascun modello:**
  * Utilizzare lo stesso prompt di proposta per Bitcoin.
  * Chiedere al modello di proporre **una** dApp Bitcoin Taproot.
  * Consentire al modello di scegliere il proprio concetto di applicazione.
  * Salvare la proposta originale completa.

### STEP 3 - Revisione delle Proposte di dApp
* **Per ciascun modello:**
  * Esaminare l'applicazione proposta.
  * Valutare la correttezza tecnica.
  * Verificare l'effettivo utilizzo dello *Script Path* di Taproot.
  * Valutare la fattibilità e la complessità di implementazione.
  * Identificare potenziali problemi tecnici.
  * Stabilire la proposta come progetto di riferimento del modello.

> **Nota:** Ciascun modello sviluppa la **propria** dApp proposta. Non selezionare una dApp comune per tutti i modelli.

### STEP 4 - Preparazione del Prompt di Generazione
* Scrivere un modello di prompt di generazione comune per Bitcoin.
* Includere la proposta di dApp specifica di ciascun modello.
* Descrivere l'applicazione target e i suoi requisiti.
* Specificare i componenti principali e i file attesi.
* Consentire file aggiuntivi solo quando necessario.
* Utilizzare la stessa struttura di prompt e le stesse istruzioni per tutti e tre i modelli.

### STEP 5 - Preparazione del Prompt di Riparazione
* Scrivere un prompt di riparazione fisso.
* Utilizzare lo stesso prompt per tutti i modelli.
* Includere l'errore esatto riscontrato.
* Richiedere al modello di correggere il proprio codice.
* Non consentire modifiche ai requisiti originali.

### STEP 6 - Definizione dei Piani di Test per Bitcoin
* Preparare **cinque test** per la dApp di ciascun modello.
* Definire criteri oggettivi di superamento/fallimento (PASS/FAIL).
* Adattare i dettagli dei test a ciascuna applicazione proposta.
* Completare i piani di test prima della generazione del codice.

#### BTC-01 - Installazione e Dipendenze
* Installare tutte le dipendenze richieste.
* Eseguire il processo di build o compilazione richiesto.
  * **PASS:** Tutte le dipendenze vengono installate e il progetto viene compilato con successo.
  * **FAIL:** Dipendenze bloccanti o errori di compilazione.

#### BTC-02 - Avvio dell'Applicazione
* Avviare il backend.
* Avviare il frontend.
* Aprire l'applicazione web.
  * **PASS:** Backend e frontend si avviano correttamente e l'interfaccia è accessibile.
  * **FAIL:** Un componente essenziale non si avvia o l'applicazione risulta inutilizzabile.

#### BTC-03 - Configurazione di Wallet e Signet
* Connettere il wallet.
* Verificare la configurazione della rete Bitcoin Signet.
* Creare o configurare l'output Taproot richiesto.
  * **PASS:** La connessione del wallet funziona e viene creato un output Taproot valido e verificabile su Signet.
  * **FAIL:** La connessione del wallet, la configurazione della rete o la creazione dell'output Taproot falliscono.

#### BTC-04 - Transazione Script Path Riuscita
* Eseguire l'operazione principale dell'applicazione.
* Spendere l'output Taproot tramite Script Path.
* Trasmettere e verificare la transazione.
  * **PASS:** La transazione viene confermata e il suo *witness* dimostra una spesa autentica tramite Script Path, inclusi lo script e il *control block*.
  * **FAIL:** La transazione fallisce, non soddisfa le condizioni previste o utilizza solo una spesa *Key-Path*.

#### BTC-05 - Rifiuto della Transazione non Valida
* Tentare un'operazione di spesa che viola le condizioni di script richieste.
  * **PASS:** La transazione non valida viene rifiutata e non si verifica alcuna spesa confermata non autorizzata.
  * **FAIL:** Una spesa non autorizzata viene eseguita con successo.

### STEP 7 - Invio per l'Approvazione
* Inviare il prompt di generazione Bitcoin ad Azmat.
* Inviare il prompt di riparazione fisso ad Azmat.
* Inviare i tre piani di test Bitcoin ad Azmat.
* Ottenere l'approvazione prima dell'implementazione.

### STEP 8 - Generazione di Tre dApp Bitcoin
* **Per ciascun modello:**
  * Creare una cartella di lavoro pulita.
  * Generare la dApp utilizzando il prompt approvato.
  * Salvare la versione iniziale senza modifiche.
  * Registrare il tempo di generazione e le metriche rilevanti.

### STEP 9 - Esecuzione dei Test Iniziali
* **Per ciascun modello:**
  * Eseguire tutti i **cinque test** predefiniti.
  * Registrare PASS/FAIL per ciascun test.
  * Registrare tutti gli errori e le relative categorie.
  * Calcolare il numero iniziale di test superati.
  * Salvare i risultati iniziali.

### STEP 10 - Riparazione e Nuovo Test
* **Per ciascun modello:**
  ```python
  repair_steps = 0
  consecutive_steps_without_improvement = 0
  ```
  * **Finché i test falliscono:**
    * Inviare l'errore esatto al modello originale.
    * Utilizzare il prompt di riparazione fisso.
    * Consentire al modello di correggere il proprio codice.
    * Salvare la nuova versione completa.
    * Incrementare `repair_steps`.
    * Eseguire nuovamente **tutti e cinque** i test.
    * Registrare i risultati e gli errori.
    * **Logica di controllo:**
      * Se il numero di test superati aumenta rispetto alla versione precedente: `consecutive_steps_without_improvement = 0`
      * Altrimenti: `consecutive_steps_without_improvement += 1`
    * **Interrompere se:**
      * Tutti e cinque i test vengono superati; **oppure**
      * Vengono raggiunti 10 passaggi di riparazione; **oppure**
      * 3 passaggi consecutivi non mostrano miglioramenti.

### STEP 11 - Test Finali di Bitcoin
* **Per ciascun modello:**
  * Eseguire tutti i **cinque test** sulla versione finale.
  * Registrare i risultati finali PASS/FAIL.
  * Verificare la funzionalità su Bitcoin Signet.
  * Salvare gli ID delle transazioni.
  * Salvare gli screenshot.
  * Registrare l'esito finale.

---

## FASE 2 - ETHEREUM EIP-7702

### STEP 12 - Generazione delle Proposte di dApp
* **Per ciascun modello:**
  * Utilizzare lo stesso prompt di proposta per Ethereum.
  * Chiedere al modello di proporre **una** dApp Ethereum EIP-7702.
  * Consentire al modello di scegliere il proprio concetto di applicazione.
  * Salvare la proposta originale completa.

### STEP 13 - Revisione delle Proposte di dApp
* **Per ciascun modello:**
  * Esaminare l'applicazione proposta.
  * Valutare la correttezza tecnica.
  * Verificare l'effettivo utilizzo della delega EIP-7702.
  * Valutare la fattibilità e la complessità di implementazione.
  * Identificare potenziali problemi tecnici.
  * Stabilire la proposta come progetto di riferimento del modello.

> **Nota:** Ciascun modello sviluppa la **propria** dApp proposta.

### STEP 14 - Preparazione del Prompt di Generazione
* Scrivere un modello di prompt di generazione comune per Ethereum.
* Includere la proposta di dApp specifica di ciascun modello.
* Descrivere l'applicazione target e i suoi requisiti.
* Specificare i componenti principali e i file attesi.
* Consentire file aggiuntivi solo quando necessario.
* Utilizzare la stessa struttura di prompt e le stesse istruzioni per tutti e tre i modelli.

### STEP 15 - Preparazione del Prompt di Riparazione
* Utilizzare lo stesso prompt di riparazione fisso.
* Includere l'errore esatto riscontrato.
* Richiedere al modello di correggere il proprio codice.
* Non modificare i requisiti originali.

### STEP 16 - Definizione dei Piani di Test per Ethereum
* Preparare **cinque test** per la dApp di ciascun modello.
* Definire criteri oggettivi di superamento/fallimento (PASS/FAIL).
* Adattare i dettagli dei test a ciascuna applicazione proposta.
* Completare i piani di test prima della generazione del codice.

#### ETH-01 - Installazione e Dipendenze
* Installare tutte le dipendenze richieste.
* Eseguire il processo di build o compilazione richiesto.
  * **PASS:** Tutte le dipendenze vengono installate e il progetto viene compilato con successo.
  * **FAIL:** Dipendenze bloccanti o errori di compilazione.

#### ETH-02 - Avvio dell'Applicazione
* Avviare il backend.
* Avviare il frontend.
* Aprire l'applicazione web.
  * **PASS:** Backend e frontend si avviano correttamente e l'interfaccia è accessibile.
  * **FAIL:** Un componente essenziale non si avvia o l'applicazione risulta inutilizzabile.

#### ETH-03 - Wallet e Delega EIP-7702
* Connettere il wallet a Ethereum Sepolia.
* Eseguire l'autorizzazione EIP-7702 richiesta.
* Verificare la delega on-chain.
  * **PASS:** L'autorizzazione viene elaborata correttamente e l'EOA delega allo smart contract di implementazione previsto.
  * **FAIL:** L'autorizzazione o la delega falliscono, oppure l'indirizzo delegato non è corretto.

#### ETH-04 - Operazione Delegata Riuscita
* Eseguire l'operazione principale dell'applicazione.
* Verificare che venga utilizzato il codice delegato.
* Verificare lo stato della blockchain risultante.
  * **PASS:** L'operazione viene completata con successo, con il risultato on-chain previsto.
  * **FAIL:** L'operazione fallisce o produce un risultato non corretto.

#### ETH-05 - Operazione non Valida o non Autorizzata
* Tentare un'operazione che viola le regole di autorizzazione dell'applicazione.
  * **PASS:** L'operazione viene rifiutata o annullata (*reverted*) senza effetti non autorizzati sull'applicazione.
  * **FAIL:** L'operazione non autorizzata viene eseguita con successo.

### STEP 17 - Invio per l'Approvazione
* Inviare il prompt di generazione Ethereum ad Azmat.
* Inviare il prompt di riparazione fisso ad Azmat.
* Inviare i tre piani di test Ethereum ad Azmat.
* Ottenere l'approvazione prima dell'implementazione.

### STEP 18 - Generazione di Tre dApp Ethereum
* **Per ciascun modello:**
  * Creare una cartella di lavoro pulita.
  * Generare la dApp utilizzando il prompt approvato.
  * Salvare la versione iniziale senza modifiche.
  * Registrare il tempo di generazione e le metriche rilevanti.

### STEP 19 - Esecuzione dei Test Iniziali
* **Per ciascun modello:**
  * Eseguire tutti i **cinque test** predefiniti.
  * Registrare PASS/FAIL per ciascun test.
  * Registrare tutti gli errori e le relative categorie.
  * Calcolare il numero iniziale di test superati.
  * Salvare i risultati iniziali.

### STEP 20 - Riparazione e Nuovo Test
* **Per ciascun modello:**
  ```python
  repair_steps = 0
  consecutive_steps_without_improvement = 0
  ```
  * **Finché i test falliscono:**
    * Inviare l'errore esatto al modello originale.
    * Utilizzare il prompt di riparazione fisso.
    * Consentire al modello di correggere il proprio codice.
    * Salvare la nuova versione completa.
    * Incrementare `repair_steps`.
    * Eseguire nuovamente **tutti e cinque** i test.
    * Registrare i risultati e gli errori.
    * **Logica di controllo:**
      * Se il numero di test superati aumenta rispetto alla versione precedente: `consecutive_steps_without_improvement = 0`
      * Altrimenti: `consecutive_steps_without_improvement += 1`
    * **Interrompere se:**
      * Tutti e cinque i test vengono superati; **oppure**
      * Vengono raggiunti 10 passaggi di riparazione; **oppure**
      * 3 passaggi consecutivi non mostrano miglioramenti.

### STEP 21 - Test Finali di Ethereum
* **Per ciascun modello:**
  * Eseguire tutti i **cinque test** sulla versione finale.
  * Registrare i risultati finali PASS/FAIL.
  * Verificare la funzionalità su Ethereum Sepolia.
  * Salvare gli ID delle transazioni.
  * Salvare gli screenshot.
  * Registrare l'esito finale.

---

## FASE 3 - RISULTATI E CONFRONTO

### STEP 22 - Raccolta dei Dati Sperimentali
* **Per ciascun modello e piattaforma, registrare:**
  * Proposta di dApp originale.
  * Test iniziali superati (su 5).
  * Test finali superati (su 5).
  * Numero di passaggi di riparazione.
  * Numero di passaggi di configurazione manuale.
  * **Categorie di errore:**
    * Errori di dipendenza.
    * Uso errato di librerie/API.
    * Errori di logica.
    * Errori di sicurezza.
    * Violazioni delle regole blockchain.
  * Miglioramenti dopo ogni riparazione.
  * Stato finale del deployment e della transazione.
  * **Esito finale:** `SUCCESS` / `PARTIAL SUCCESS` / `FAILURE`.

### STEP 23 - Confronto tra i Tre Modelli
* Confrontare la qualità delle loro proposte di dApp.
* Confrontare la correttezza funzionale iniziale.
* Confrontare la correttezza funzionale finale.
* Confrontare i passaggi di riparazione richiesti.
* Confrontare i requisiti di configurazione manuale.
* Confrontare le categorie e la frequenza degli errori.
* Confrontare la capacità di correggere i propri errori.
* Confrontare i risultati finali dei test blockchain.

### STEP 24 - Preparazione dei Risultati della Tesi
* Preparare i risultati di Bitcoin.
* Preparare i risultati di Ethereum.
* Preparare il confronto incrociato tra i modelli.
* Discutere punti di forza e limitazioni.
* Includere log, ID delle transazioni e screenshot.

---

## REGOLE SPERIMENTALI

1. Gli esperimenti precedenti costituiscono **solo uno studio pilota**.
2. Ciascun modello propone e implementa la **propria** dApp.
3. Ciascun modello lavora in una cartella pulita separata.
4. La versione iniziale generata **non deve mai essere modificata**.
5. Salvare ogni versione prodotta dopo una riparazione.
6. **Non correggere mai manualmente** il codice sorgente generato.
7. Gli interventi di configurazione manuale sono consentiti solo per problemi di ambiente e configurazione. Registrare ogni intervento.
8. Utilizzare lo stesso modello di prompt di generazione per tutti i modelli sulla stessa piattaforma.
9. Utilizzare lo stesso prompt di riparazione fisso per tutti i modelli.
10. Definire tutti i piani di test prima della generazione del codice.
11. Ogni passaggio di riparazione deve essere seguito dalla suite completa di cinque test.
12. Una riparazione viene conteggiata come miglioramento **solo** quando il numero di test superati aumenta rispetto alla versione immediatamente precedente.
13. **Interrompere dopo:**
    * Il superamento di tutti e cinque i test;
    * 10 passaggi di riparazione;
    * 3 passaggi consecutivi senza miglioramenti.
14. Se il processo si interrompe con test falliti, riportare il numero esatto di test superati e classificare l'esito come `PARTIAL SUCCESS` o `FAILURE`.
15. **Non utilizzare codice corretto da ChatGPT** nei risultati ufficiali.
16. Preservare tutti gli ID delle transazioni, screenshot, log degli errori e versioni generate.