# BactériAI — Détection de bactéries avec YOLOv8

Projet de vision par ordinateur : détection et classification de 4 types de bactéries
(Bacillus, Coccus, Spirillum, Vibrio) sur des images microscopiques, avec YOLOv8 et une
interface Streamlit.

## Contenu du dépôt

| Fichier | Rôle |
|---|---|
| `notebooks/mlproject_colab.py` | Export Colab : exploration des données, entraînement, évaluation |
| `app.py` | Application Streamlit de détection |
| `requirements.txt` | Dépendances Python |

## Installation

```bash
git clone https://github.com/<ton-pseudo>/bacteria-detection-yolov8.git
cd bacteria-detection-yolov8
python -m venv .venv
source .venv/bin/activate        # Windows : .venv\Scripts\activate
pip install -r requirements.txt
```

## Modèle entraîné

Les poids (`best.pt`) ne sont pas versionnés (fichier trop lourd).
Place-les dans `weights/best.pt`, puis vérifie le chemin utilisé dans `app.py`.

## Lancer l'application

```bash
streamlit run app.py
```

## Entraînement (Google Colab)

- Modèle : YOLOv8l, 40 epochs, imgsz 640, batch 8, optimiseur AdamW (lr0 = 0.001)
- Jeu de données : `Bacteria_Balanced_yolov8.zip` (non inclus)
- Métriques évaluées : précision, rappel, F1, mAP@50, mAP@50-95

## Auteure

Aya Moujoud — Master Big Data & Data Science, FSBM, Université Hassan II de Casablanca
