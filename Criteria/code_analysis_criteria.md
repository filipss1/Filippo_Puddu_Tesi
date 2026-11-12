Objective Evaluation — Code Analysis
1. Accuracy

Question: What percentage of the model's verifiable technical claims are correct?

Method: Compare each claim against the source code and trusted references. Label each claim as correct, incorrect, or unverifiable.

Metric: Correct claims / Total verifiable claims × 100

2. Completeness

Question: What percentage of the expected analysis elements are correctly covered?

Method: Create a fixed checklist for each blockchain before testing. Count an element only if the output addresses it correctly.

Metric: Correctly covered elements / Total expected elements × 100

3. Latency

Question: How long does the analysis take?

Method: Measure elapsed time from prompt submission to complete response, excluding initial model loading. Run each test at least three times.

Metric: Median completion time in seconds.

4. Context Window Usage

Question: What is the peak context usage during the analysis?

Method: Record peak context tokens and the configured context limit using runtime measurements, where available. Record any truncation.

Metric: Peak context tokens / Configured context limit × 100



Valutazione oggettiva — Code Analysis
1. Accuracy (Accuratezza)

Domanda: Quale percentuale delle affermazioni del modello è corretta?

Metodo: Confrontare le affermazioni con il codice sorgente e fonti affidabili. Classificarle come corrette, errate o non verificabili.

Formula:

Accuratezza (%) = Affermazioni corrette / Affermazioni verificabili × 100

2. Completeness (Completezza)

Domanda: Quale percentuale degli elementi richiesti è stata trattata correttamente?

Metodo: Preparare una checklist per ogni blockchain prima dei test. Contare solo gli elementi trattati correttamente.

Formula:

Completezza (%) = Elementi trattati correttamente / Elementi attesi × 100

3. Latency (Latenza)

Domanda: Quanto tempo impiega il modello a completare l'analisi?

Metodo: Misurare il tempo dal momento dell'invio del prompt al completamento della risposta, escludendo il caricamento iniziale del modello. Ripetere il test almeno tre volte.

Valore da registrare: mediana dei tempi, in secondi.

4. Context Window Usage (Utilizzo della finestra di contesto)

Domanda: Quanta parte della finestra di contesto viene utilizzata?

Metodo: Registrare il picco di token utilizzati e la dimensione massima del contesto configurata. Annotare eventuali troncamenti.

Formula:

Utilizzo (%) = Picco di token utilizzati / Dimensione del contesto configurata × 100