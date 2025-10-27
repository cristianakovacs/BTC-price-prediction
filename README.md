# 📈 Numele Proiectului:
ANALIZĂ DE DATE ȘI ALGORITMI DE ÎNVĂȚARE AUTOMATĂ PENTRU PREDICȚIA PREȚULUI BITCOIN 🪙

# By Cristiana Kovacs 🙂
---

## Descriere
## 🎯 Obiectivul proiectului: 
Scopul acestui proiect este dezvoltarea și evaluarea unor modele avansate de învățare automată pentru prognoza prețului de închidere al Bitcoin (BTC), utilizând un set complex de date financiare, macroeconomice și on-chain.

**Abordarea integrează pași compleți de extragere, curățare și preprocesare a datelor, feature engineering, antrenare de modele predictive (inclusiv deep learning) și evaluare a performanței prin indicatori precum MAE.**

Proiectul demonstrează capacitatea de a construi un **pipeline de predicție end-to-end**, scalabil și ușor de extins către alte active financiare. Este conceput pentru a evidenția competențele mele în **data science aplicată, modelare statistică și analiză predictivă**, cu potențial de aplicare în domenii precum **fintech, investiții și management al riscului.**

## 💡 Aplicații practice posibile:
Investitori sau traderi, ca punct suplimentar de referință în luarea deciziilor.

Analiză de scenarii (cum reacționează Bitcoin la variația altor active sau indicatori).

Monitorizarea factorilor cu cea mai mare influență (variabile importante identificate de model).

Monitorizarea automată a prețului BTC în timp real, cu alerte atunci când deviația depășește un prag (ex. ±2%).

Predicții zilnice sau pe orizont scurt (1–3 zile) pentru sisteme de risk management sau pentru ajustarea pozițiilor de tranzacționare.

Suport pentru analiza scenariilor („ce s-ar întâmpla dacă?”) prin simularea diferitelor evoluții de preț.

Integrare într-un dashboard de forecast pentru vizualizarea simultană a predicției și a deviației procentuale în timp real.

---

## ⚙️ Tehnologii folosite:

- **Limbaj de programare:** Python 🐍
- **Manipulare și analiză date:** pandas, NumPy
- **Vizualizare date:** matplotlib, seaborn, plotly, scipy
- **Machine Learning & modele statistice:** scikit-learn (LinearRegression, ElasticNet, GradientBoosting), LightGBM, CatBoost, ARIMA
- **Deep Learning:** TensorFlow / Keras (LSTM, Dense, Dropout)
- **Tool-uri și notebook:** Google Colab, Jupyter Notebook, IPython.display
- **Altele:** os, functools, itertools, warnings

---
## 🧠 Medodologie:


### 📊 1. Colectarea datelor  
Au fost integrate surse diverse:  
- 📈 **Date financiare** (preț BTC/USD, volum, volatilitate)  
- 🌍 **Indicatori macroeconomici** (inflație, rate dobândă, indici bursieri)  
- 🔗 **Date on-chain** (hash rate, adrese active, tranzacții)  
➡️ Toate datele au fost verificate pentru acuratețe și sincronizate temporal.



### 🧹 2. Preprocesare & Feature Engineering  
- Eliminarea valorilor lipsă și normalizarea datelor 📏  
- ⏳ **Lag features:** valori trecute ale prețului Bitcoin (ex: 1, 2, 3 zile înainte)  
- 📈 **Moving averages:** medii mobile pe 7, 14 și 30 de zile  
- 📉 **Volatilitate:** deviere standard a prețului pe ferestre mobile  
- 🔗 **Variabile derivate:** rapoarte BTC/SP500, BTC/AUR etc.  
- ⚙️ **Indicatori tehnici (opțional):** RSI, MACD, Bollinger Bands  
- Împărțirea setului în **train / validation / test** fără scurgere temporală 🚫



### 🤖 3. Modelare  
Au fost testate mai multe modele:  
- 🟢 **Naive Baseline:** predicție simplă: Closeₜ = Closeₜ₋₁  
- 📝 **Elastic Net Regression:** regresie liniară regularizată pentru selecția caracteristicilor și stabilitate  
- 📊 **SARIMAX / ARIMAX:** modele de serie temporală cu variabile exogene (GOLD, OIL, SP500, macroeconomice)  
- ⚡ **LightGBM Regressor:** optimizat pentru MAE (quantile loss α=0.5)  
- 🐱 **CatBoost Regressor:** alternativă robustă la LightGBM, ușor de tunat  
- ❌ **XGBoost Regressor:** folosit ca comparație cu LightGBM și CatBoost  
- 🧠 **LSTM (RNN):** pentru captarea dependențelor pe termen lung în serie temporală


### 🧾 4. Evaluare  
- Metrică principală: **MAE (Mean Absolute Error)** ✅  
- Analiză comparativă între modele și vizualizare 🔍  
- Alegerea modelului final bazată pe performanță + stabilitate 💪



### 💡 5. Interpretare & Limitări  
- Analiza importanței variabilelor 🔎  
- Modelele pot fi influențate de evenimente externe (știri, reglementări) 🌪️  
- Posibile îmbunătățiri: integrarea datelor de **sentiment** sau **online learning** 🚀
---

## 📊 Rezultate:

| Model                        | MAE       | RMSE      | Max Error   | Min Error  | Std Dev Error |
|-------------------------------|-----------|-----------|------------|------------|---------------|
| 🟢 Naive                       | 1 143.80   | 1 725.85   | 8 227.29    | 0.00       | 1 292.40       |
| 📝 ElasticNet                  | 3 147.25   | 4 080.13   | 11 668.63   | 10.74      | 2 596.58       |
| 📊 ARIMAX                      | 51 672.04  | 56 019.20  | 93 229.23   | 59.41      | 21 636.81      |
| ⚡ LightGBM                     | 15 357.06  | 22 533.54  | 56 026.47   | 0.76       | 16 490.03      |
| 🐱 CatBoost                     | 29 150.29  | 36 366.20  | 76 067.32   | 49.11      | 21 743.08      |
| 🌱 GradientBoosting             | 17 339.14  | 23 519.67  | 56 338.60   | 656.88     | 15 891.17      |
| 🧠 LSTM                        | 7 838.59   | 10 575.93  | 26 385.68   | 1.27       | 7 099.77       |
| 🔗 Stacking (Naive+ElasticNet+LSTM) | 877.42    | 1 226.64   | 5 008.30    | 1.68       | 857.19        |


### 🚀 Aplicație practică pe următoarele 7 zile :

| Date       | Pred_Naive | Pred_Stacking | BTC_Real  | Error_Stacking | Error_Naive | Error_%_Stacking | Error_%_Naive |
|------------|------------|---------------|-----------|----------------|-------------|-----------------|---------------|
| 2025-07-28 | 117 835.37  | 117 860.42     | 117 924.47 | 64.05          | 89.10       | 0.05            | 0.08          |
| 2025-07-29 | 117 475.37  | 117 755.71     | 117 922.15 | 166.44         | 446.78      | 0.14            | 0.38          |
| 2025-07-30 | 117 115.36  | 117 594.29     | 117 831.19 | 236.90         | 715.83      | 0.20            | 0.61          |
| 2025-07-31 | 116 755.36  | 117 432.87     | 115 758.20 | 1674.67        | 997.16      | 1.45            | 0.86          |
| 2025-08-01 | 116 395.35  | 117 271.45     | 113 405.34 | 3866.11        | 2990.01     | 3.41            | 2.64          |
| 2025-08-02 | 116 035.34  | 117 110.03     | 113 836.00 | 3274.03        | 2199.34     | 2.88            | 1.93          |
| 2025-08-03 | 115 675.34  | 116 948.61     | 114 017.03 | 2931.58        | 1658.31     | 2.57            | 1.45          |

---


## 🗂️ Structura proiectului:
   ```bash
BTC-price-prediction/
│
├── Bitcoin_Prediction_Final_Presentation.ipynb      # Notebook principal
├── Bitcoin_Prediction_Final_Presentation.pdf       # Prezentarea proiectului
├── data/
│   ├── raw/                  # Date brute (CSV)
│   ├── processed/            # Date prelucrate / feature engineering
│   ├── splits/               # Train / test sets
│   └── predictions/          # Rezultatele modelelor
├── requirements.txt          # Librării necesare
├── README.md
└── LICENSE
   ```
> 💾 Toate fișierele de date necesare rulării proiectului se găsesc în folderul `date/`.

---

## ⚡ Instalare:
Pași pentru a instala și rula proiectul:


1️⃣ Clonează repository-ul:

   ```bash
   git clone https://github.com/cristianakovacs/BTC-price-prediction.git
   ```

2️⃣ Navighează în directorul proiectului:
   
   ```bash
   cd BTC-price-prediction
   ```
   
3️⃣ Instalează dependințele:

  ```bash
    pip install -r requirements.txt
   ```

💡 Este recomandat să folosești un mediu virtual (virtualenv sau conda) pentru a instala dependențele, ca să nu afectezi sistemul global Python.

---

## ▶️ Utilizare:

- Deschide fișierul Bitcoin_Prediction_Final_Presentation.ipynb în Jupyter Notebook sau Google Colab.

- Rulează celulele pentru a executa analiza și a obține predicțiile prețului Bitcoin.

- Poți modifica parametrii modelelor sau sursa de date pentru experimente proprii.

---

## 🤝 Contribuții:

- 1️⃣ Fork-uieste repository-ul: Apasă pe butonul Fork din GitHub în pagina proiectului, creezi o copie a repository-ului original pe contul tău de GitHub.

- 2️⃣ Creează un branch nou: Creează un branch (o ramură) nouă numită feature-nume și te mută pe el.
   ```bash
   git checkout -b feature-nume

- 3️⃣ Realizează modificările dorite: Faci modificările în cod, adaugi fișiere noi sau corectezi bug-uri în branch-ul tău. Poți să lucrezi în Jupyter Notebook, Python, sau alte fișiere din proiect.

- 4️⃣ Comitează modificările: Salvează schimbările locale în istoria Git, cu un mesaj descriptiv.
     ```bash
     git commit -am 'Adăugat o nouă funcționalitate'
     ```
     
    -a = adaugă automat fișierele modificate (care erau deja urmărite de Git)
  
    -m = mesajul commit-ului

- 5️⃣ Trimite un pull request: Încarci modificările tale pe GitHub (în fork-ul tău) și ceri ca acestea să fie îmbinate (merge) în repository-ul original. GitHub detectează branch-ul tău nou și îți permite să creezi un Pull Request (PR).

---

## 📜 Licență

Acest proiect este licențiat sub licența MIT - vezi fișierul Vezi fișierul [LICENSE](LICENSE) pentru detalii.
 pentru detalii.

## 💼 Contact

📧 [Trimite-mi un email](mailto:cristiana15_97@yahoo.com)
- cristiana15_97@yahoo.com
  
🔗 [LinkedIn](https://www.linkedin.com/in/cristiana-kovacs-650917328)  




   
