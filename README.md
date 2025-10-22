# 🪙 Bitcoin Price Prediction  
**Predicția prețului Bitcoin folosind modele de învățare automată**  
Autor: **Cristiana Kovacs**

---

## 🎯 Descriere
Acest proiect aplică metode de **machine learning** pentru a prezice prețul de închidere al Bitcoin.  
Modelul folosește un set divers de date — **financiare, macroeconomice, on-chain și de sentiment** — pentru a identifica factorii care influențează evoluția BTC.

---

## 🧾 Date utilizate
Surse principale:
- **Yahoo Finance:** prețuri BTC, indici bursieri, aur, petrol  
- **FRED:** indicatori macro (CPI, dobânzi, șomaj)  
- **Blockchain.com API:** date on-chain (hash rate, difficulty, tranzacții)  
- **Reddit & CoinDesk:** scoruri de sentiment  

Setul final: `3967 rânduri × 19 coloane` (2014–2025)

---

## 🧠 Modele testate
| Model | Tip | Observație |
|--------|-----|-------------|
| Naive Baseline | Simplu, rapid | Bază de comparație |
| ElasticNet | Regressie liniară regularizată | Interpretabil |
| ARIMAX | Serii temporale cu variabile exogene | Captură relații temporale |
| LightGBM / CatBoost / GradientBoosting | Boosting | Precizie mare |
| LSTM | Rețea neuronală recurentă | Pattern-uri complexe |

**Modelul final:** `Stacking (Naive + ElasticNet + LSTM)`  
📉 **MAE: 877 USD**, **RMSE: 1226 USD**, eroare medie ≈ **1.5%**

---

## ⚙️ Cum folosești proiectul

### 1️⃣ Instalare
```bash
git clone https://github.com/<username>/BTC-price-prediction.git
cd BTC-price-prediction
pip install -r requirements.txt

BTC-price-prediction/
│
├── Bitcoin_Prediction_Final_Presentation.ipynb      # Notebook principal
├── data/
│   ├── raw/                  # Date brute (CSV)
│   ├── processed/            # Date prelucrate / feature engineering
│   ├── splits/               # Train / test sets
│   └── predictions/          # Rezultatele modelelor
└── Bitcoin_Prediction_Final_Presentation.pdf    # Prezentarea proiectului


