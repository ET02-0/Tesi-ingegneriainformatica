Tesi di Laurea Triennale: Analisi Comparativa Metodi XAI (BOCSOR, SHAP, Permutation) su Dati EEG

Questo repository raccoglie il codice Python e l'elaborato della mia Tesi di Laurea Triennale in Ingegneria Informatica presso l'Università di Pisa, sviluppata sotto la preziosa supervisione dei relatori Ing. Antonio Luca Alfeo e Prof. Mario G.C.A. Cimino.

**Panoramica del Progetto:** L'obiettivo del lavoro è affrontare il problema della "scatola nera" nei modelli di Machine Learning applicati a contesti critici. La tesi valuta e confronta l'efficienza e l'affidabilità di diverse tecniche di Explainable AI (XAI) per l'estrazione dell'importanza delle caratteristiche (feature importance). Nello specifico, il lavoro paragona i metodi standard ma computazionalmente costosi (come SHAP e Permutation Importance) con un innovativo approccio ibrido basato su controfattuali chiamato BoCSOR. L'analisi empirica è stata condotta su dati fisiologici complessi (dataset BCI_2 per il riconoscimento di movimenti immaginati da segnali EEG).

**Metodologia:**
- **Modelli utilizzati:** L'analisi è stata condotta addestrando classificatori a complessità crescente, partendo dai Decision Tree fino ad arrivare a Random Forest con un numero variabile di alberi (5, 10, 15 e 50).
- **Metriche di valutazione:** Le prestazioni dei metodi di Explainability sono state misurate confrontando il Costo Computazionale e la Fedeltà (rispetto al metodo "Intrinsic") tramite Correlazione di Pearson e p-value. È stato inoltre formulato un Indice Unificante pesato per valutare il compromesso ottimale tra tempo e affidabilità.

**Risultati Principali:**
- **Modelli Semplici (Decision Tree):** I metodi della famiglia BoCSOR garantiscono una fedeltà accettabile abbattendo drasticamente i tempi di calcolo rispetto a SHAP.
- **Modelli Complessi (Random Forest):** Aumentando la complessità (es. 50 alberi), la variante *BoCSOR Distance Original* si è rivelata il metodo più solido secondo l'indice unificante. Riesce infatti a superare SHAP e Permutation Importance per accuratezza delle spiegazioni (correlazione), confermandosi come un'alternativa altamente competitiva e flessibile per bilanciare tempi di elaborazione e qualità interpretativa nei modelli di AI.
