## Autor
**Benaia J. Heinze**  
Data del projecte: 06/12/2025  


# League of Legends SOLO-Q Ranked Games - Anàlisi Cas Kaggle

Es busca predir l'equip guanyador en les partides classificatòries del videojoc League of Legends utilitzant estadístiques de partides del 2019.


## Estructura del projecte
```
├── data/               # Dataset utilitzat
├── models/             # Models o imatges utilizats al notebook
├── kaggle.ipynb        # Notebook principal d'anàlisi
├── kaggle.html         # Notebook en html per més llegibilitat
└── README.md           # Documentació del projecte
```

## Objectiu

L'objectiu principal d'aquest anàlisi es predir la probabilitat de que l'equip blau guanyi la partida, utilitzant les estadistiques recollides al dataset.

Dataset original: https://www.kaggle.com/datasets/bobbyscience/league-of-legends-soloq-ranked-games/data.

Cal mencionar que donat que el videojoc evoluciona constantment, aquestes dades no representen l'estat actual del joc. El dataset conté dades unicament de l'any 2019.

## Metodologia i aproximament

1. Introducció al Cas Kaggle
2. Explicació del Gameplay
    * Necessaria per entendre el significat de les variables del dataset
3. Dependències
    * Llibreries utilitzades al notebook
4. Anàlisi exploratori del dataset (EDA)
    * 4.1. Informació bàsica del dataset
    * 4.2. Estadístiques descriptives
    * 4.3. Distribucio de la variable objectiu
    * 4.4. Correlació entre variables i la variable objectiu
    * 4.5. Anàlisi per trams temporals (frames)
    * 4.6. Evolució de les estadístiques de joc per frame
    * 4.7. Anàlisi d'objectius épics (Dracsm Baron Nashor, Rift Herald)
    * 4.8. Análisi de destrucció d'estructures
    * 4.9. Anàlisi de Visió (Wards)
5. Processament de dades i selecció de variables
6. Models de classificació i predicció
    * 6.1. Matrius de confusió i corbes ROC
7. Conclusions


## Models utilitzats

* Regresió logística: Model lineal que serveix com a sòlida línia base. Ha proporcionat resultats sorprenentment bons.
* Random Forest: Model d’arbres aleatoris capaç de capturar interaccions no lineals. En aquest dataset, el seu rendiment és lleugerament inferior als models de boosting.
* HistGradientBoosting: Model de gradient boosting dissenyat per a grans volums de dades. Ha estat el model amb millor ROC AUC.
* XGBoost: Un dels models més utilitzats per competició tabular. En el dataset analitzat obté resultats pràcticament idèntics a HistGradientBoosting.

Les mètriques finals són aproximadament:
```
| Model                 | Accuracy | ROC AUC |
|-----------------------|----------|---------|
| Logistic Regression   | ~0.786   | ~0.871  |
| Random Forest         | ~0.775   | ~0.858  |
| HistGradientBoosting  | ~0.786   | ~0.873  |
| XGBoost               | ~0.786   | ~0.871  |
```
