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
