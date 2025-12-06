# League of Legends SOLO-Q Ranked Games - Anàlisi Cas Kaggle

Es busca predir l'equip guanyador en les partides classificatòries del videojoc League of Legends utilitzant estadístiques de partides del 2019.


## Estructura del projecte
```
├── data/               # Dataset utilitzat
├── models/             # Models o imatges utilizats al notebook
├── kaggle.ipynb        # Notebook principal d'anàlisi
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
7. Conclusions


## Models utilitzats