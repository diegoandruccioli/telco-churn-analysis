# 📊 Telco Customer Churn Analysis & Prediction

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Libraries](https://img.shields.io/badge/Libraries-Pandas%20%7C%20Scikit--Learn%20%7C%20Seaborn-green)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)

## 📖 Abstract
Questo progetto universitario analizza il fenomeno del **Customer Churn** (abbandono dei clienti) in un'azienda di telecomunicazioni. Attraverso un approccio data-driven, l'analisi mira a identificare i fattori di rischio, segmentare la clientela in profili comportamentali e costruire un modello predittivo per anticipare futuri abbandoni.

---

## 🎯 Motivazione e Obiettivi
Il settore delle telecomunicazioni è caratterizzato da un'elevata competizione e da costi di acquisizione clienti significativamente più alti rispetto ai costi di mantenimento. 
**L'obiettivo di questo progetto è duplice:**
1.  **Analitico:** Comprendere *perché* i clienti se ne vanno. È un problema di prezzo? Di servizio? Di contratto?
2.  **Strategico:** Fornire strumenti (cluster e modelli predittivi) per permettere all'azienda di intervenire *prima* che il cliente abbandoni.

---

## 📂 Struttura del Progetto

```
telco-churn-analysis/
├── data/
│   └── WA_Fn-UseC_-Telco-Customer-Churn.csv  # Dataset originale (Kaggle/IBM)
├── notebooks/
│   └── churn_analysis.ipynb                  # Notebook principale con l'intera analisi
├── requirements.txt                          # Dipendenze Python
└── README.md                                 # Documentazione del progetto
```

---

## ⚙️ Metodologia

Il progetto segue un flusso di lavoro strutturato in 4 fasi principali:

### 1. Data Cleaning & Preprocessing
-   Gestione dei valori mancanti e conversione dei tipi di dato (es. `TotalCharges`).
-   Encoding delle variabili categoriche (Label Encoding e One-Hot Encoding).
-   Feature Scaling per normalizzare le variabili numeriche.

### 2. Exploratory Data Analysis (EDA)
-   Analisi della distribuzione del Churn (sbilanciamento delle classi).
-   Correlazione tra variabili demografiche/contrattuali e tasso di abbandono.
-   Visualizzazione avanzata con `seaborn` e `matplotlib`.

### 3. Customer Segmentation (Clustering)
-   Utilizzo dell'algoritmo **K-Means** per identificare gruppi di clienti omogenei.
-   Determinazione del numero ottimale di cluster tramite **Elbow Method**.
-   Profilazione dei cluster basata su *Tenure* (fedeltà) e *Monthly Charges* (spesa).

### 4. Modellazione Predittiva (Classification)
-   Addestramento di un modello di **Logistic Regression**.
-   Valutazione tramite **Accuracy**, **Confusion Matrix**, **Precision** e **Recall**.
-   Analisi della **Feature Importance** per identificare i driver del churn.

---

## 🔑 Risultati Chiave

Dall'analisi sono emersi i seguenti insight:

*   **Tasso di Abbandono:** Il 26.6% dei clienti ha abbandonato il servizio.
*   **Fattore Tempo:** Il rischio di abbandono è massimo nei primi **6 mesi**.
*   **Fattore Contratto:** I contratti mensili (*Month-to-month*) sono il principale fattore di rischio. I contratti a 1-2 anni riducono drasticamente il churn.
*   **Segmentazione:** È stato individuato un cluster critico di **"Nuovi Alto-Spendenti"** con un tasso di abbandono >50%, che richiede azioni di retention immediate.
*   **Performance Modello:** La Logistic Regression prevede il churn con un'accuratezza del **~79%**.

---

## 🚀 Installazione e Utilizzo

Per eseguire il progetto in locale:

1.  **Clona la repository** (o scarica la cartella):
    ```bash
    git clone <repository-url>
    cd telco-churn-analysis
    ```

2.  **Crea un ambiente virtuale (opzionale ma consigliato):**
    ```bash
    python -m venv venv
    # Windows
    venv\Scripts\activate
    # Mac/Linux
    source venv/bin/activate
    ```

3.  **Installa le dipendenze:**
    ```bash
    pip install -r requirements.txt
    ```

4.  **Avvia Jupyter Notebook:**
    ```bash
    jupyter notebook
    ```
    Apri il file `notebooks/churn_analysis.ipynb` ed esegui le celle sequenzialmente.

---

## 🛠️ Tecnologie Utilizzate
-   **Python**: Linguaggio principale.
-   **Pandas & NumPy**: Manipolazione e analisi dati.
-   **Matplotlib & Seaborn**: Visualizzazione dati.
-   **Scikit-Learn**: Machine Learning (K-Means, Logistic Regression, Preprocessing).

---

**Autore:** Diego Andruccioli
**Corso:** Laboratorio di Big Data, Data Mining e Data Analytics
**Anno Accademico:** 2025/2026