# security-project

An intrusion detection system capable of classifying different types of network attacks from historical data, treating the problem as a multi-class classification task.



## Installation & Usage


pip install -r requirements.txt   # Install dependencies

python train.py                   # Full model training

python src/api/app.py             # Launch web interface 

python -m pytest tests/ -v        # Run unit tests

