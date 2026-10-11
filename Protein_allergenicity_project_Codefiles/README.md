# Allergenicity Prediction — Project Bundle

Predicts whether a protein is an **allergen** or **non-allergen** from its amino-acid
sequence, using AAC + DPC + physicochemical features and a Random Forest model.

## Contents
- `allergenicity_prediction.ipynb` — full, executed pipeline (open and re-run top to bottom)
- `data/allergen_dataset.fasta` — labelled benchmark (allergen/non-allergen, train/test)
- `models/allergenicity_rf.joblib` — trained Random Forest + scaler + feature spec
- `figures/` — all generated figures
- `requirements.txt` — exact dependencies

## Run
```bash
pip install -r requirements.txt
jupyter notebook allergenicity_prediction.ipynb
```

## Headline result (held-out test set)
Random Forest — accuracy 0.933, sensitivity 0.934, specificity 0.932, MCC 0.866, ROC-AUC 0.981.

## Predict a new sequence
```python
from joblib import load
# see notebook section 9 for predict_sequence(); returns probability + ALLERGEN/NON-ALLERGEN
```
