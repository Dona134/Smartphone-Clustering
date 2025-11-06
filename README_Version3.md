# Smartphone-Clustering

The goal of this project is to group smartphones according to their technical characteristics (e.g., CPU, RAM, storage, camera specs) and explore relationships between clusters and price.

## Table of contents
- Overview
- Features & goals
- Data
- Installation
- Usage
  - Run notebooks
  - Reproduce clustering pipeline
- Results summary
- Repository structure
- How to extend
- Contributing
- License & Contact

## Overview
This project performs EDA and unsupervised learning (clustering) on smartphone data. It shows how to preprocess heterogeneous features, apply dimensionality reduction, evaluate cluster quality, and analyze cluster relationships with price and other target variables.

## Features & goals
- Data cleaning and normalization for mixed-type features
- Feature engineering (e.g., convert string specs to numeric)
- Multiple clustering algorithms (KMeans, DBSCAN, Hierarchical, etc.)
- Dimensionality reduction (PCA, t-SNE, UMAP) for visualization
- Cluster profiling to compare price distributions and feature averages

## Data
- The dataset includes smartphone specs and prices.
- If not included in the repo, add a `data/` folder and instructions to download or provide the CSV.
- Ensure data fields are documented (columns, units).

## Installation

1. Clone the repo:
```bash
git clone https://github.com/Dona134/Smartphone-Clustering.git
cd Smartphone-Clustering
```

2. Create virtual environment and install dependencies:
```bash
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

Common dependencies: pandas, numpy, scikit-learn, matplotlib, seaborn, plotly, jupyter

## Usage

### Notebooks
Open and run notebooks to reproduce analysis:
```bash
jupyter lab
```
Notebooks typically include:
- data_preprocessing.ipynb — cleaning and feature engineering
- clustering_analysis.ipynb — algorithms and cluster evaluation
- visualization.ipynb — plots and interactive views

### Running pipeline (scripted)
If the repo includes scripts (`scripts/`), run them in order:
```bash
python scripts/preprocess.py --input data/smartphones.csv --output data/processed.csv
python scripts/cluster.py --data data/processed.csv --output results/clusters.csv
```
(Adapt commands to match your scripts.)

## Results summary
- Summarize key findings in the main notebook or README:
  - Number of clusters found
  - Main features distinguishing clusters
  - Price relationship and consumer segments

## Repository structure (example)
- notebooks/
  - data_preprocessing.ipynb
  - clustering_analysis.ipynb
  - visualization.ipynb
- data/
  - smartphones_raw.csv
  - smartphones_processed.csv
- scripts/
  - preprocess.py
  - cluster.py
- results/
- requirements.txt
- README.md

## How to extend
- Add additional features (battery, network bands).
- Try advanced clustering (spectral clustering, GaussianMixture).
- Build a small dashboard for interactive cluster exploration.

## Contributing
- File issues with suggestions or bug reports.
- Submit PRs for new algorithms, improved preprocessing, or additional analysis.

## License
Add desired license (e.g., MIT) as LICENSE file.

## Contact
Author: Dona134