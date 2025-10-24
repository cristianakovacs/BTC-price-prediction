# 📈 Numele Proiectului:
ANALIZĂ DE DATE ȘI ALGORITMI DE ÎNVĂȚARE AUTOMATĂ PENTRU PREDICȚIA PREȚULUI BITCOIN 🪙

# By Cristiana Kovacs 🙂
---

## Descriere
## 🎯 Obiectivul proiectului: 
Dezvoltarea și evaluarea unor modele de învățare automată pentru prognoza prețului de închidere al Bitcoin, pe baza unui set extins de date financiare, macroeconomice, și on-chain, cu scopul obținerii unei erori de predicție cât mai reduse (MAE).

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

## ▶️ Utilizare:

- Deschide fișierul Bitcoin_Prediction_Final_Presentation.ipynb în Jupyter Notebook sau Google Colab.

- Rulează celulele pentru a executa analiza și a obține predicțiile prețului Bitcoin.

- Poți modifica parametrii modelelor sau sursa de date pentru experimente proprii.

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

## 📜 Licență

Acest proiect este licențiat sub licența MIT - vezi fișierul Vezi fișierul [LICENSE](LICENSE) pentru detalii.
 pentru detalii.





   
