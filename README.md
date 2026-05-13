# security-project

An intrusion detection system capable of classifying different types of network attacks from historical data, treating the problem as a multi-class classification task.


ids_project/
├── data/                   ← NSL-KDD dataset files (4 files)
├── models/                 ← Trained models + evaluation metrics
│   ├── rf_model.joblib     ← Random Forest (accuracy 72.2%)
│   ├── knn_model.joblib    ← KNN k=5 (accuracy 70.5%)
│   ├── scaler.joblib
│   ├── encoders.joblib
│   └── metrics.json
├── src/
│   ├── preprocessing/
│   │   └── data_loader.py  ← Data loading, LabelEncoder encoding, StandardScaler preprocessing
│   ├── models/
│   │   ├── trainer.py      ← RF + KNN training, evaluation, model saving
│   │   └── predictor.py    ← IDSPredictor class for production inference
│   ├── api/
│   │   └── app.py          ← Flask REST API (7 endpoints)
│   └── utils/
│       └── visualizer.py   ← Matplotlib/Seaborn visualizations
├── static/
│   ├── css/style.css       ← Full frontend interface
│   ├── js/app.js           ← Interactive dashboard
│   └── img/                ← 5 automatically generated charts
├── templates/index.html    ← 5 tabs (Dashboard, Detection, Performance, Features, History)
├── notebooks/exploration.ipynb
├── tests/test_pipeline.py  ← 15 unit tests
├── config.py
├── train.py                ← Main entry point
└── README.md

## Installation & Usage


pip install -r requirements.txt   # Install dependencies
python train.py                   # Full model training
python src/api/app.py             # Launch web interface → http://localhost:5000
python -m pytest tests/ -v        # Run unit tests

