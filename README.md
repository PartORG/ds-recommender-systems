# ds-recommender-systems

**Build and Understand Recommender Systems with Content-Based and Collaborative Filtering**

[![Language](https://img.shields.io/github/languages/top/PartORG/ds-recommender-systems?color=blue)](https://github.com/PartORG/ds-recommender-systems)
[![Python Version](https://img.shields.io/badge/python-3.11.3-blue.svg)](https://www.python.org/downloads/release/python-3113/)
[![License](https://img.shields.io/github/license/PartORG/ds-recommender-systems?color=green)](LICENSE)
[![Package Manager](https://img.shields.io/badge/package-manager-pip-blue.svg)](https://pip.pypa.io/en/stable/installation/)
[![Framework](https://img.shields.io/badge/framework-jupyterlab-green.svg)](https://jupyter.org/)

## Introduction

Welcome to the `ds-recommender-systems` repository! This project is designed to help you learn and build recommender systems using content-based and collaborative filtering techniques. With this repository, you'll gain hands-on experience with Scikit-Surprise, a powerful Python library for building and analyzing recommender systems that deal with explicit rating data.

The primary workflow of this repository involves working through a series of Jupyter Notebooks in the specified order. Each notebook covers different aspects of recommender systems, from basic concepts to practical exercises and evaluations.

## Table of Contents

- [Features](#features)
- [How It Works](#how-it-works)
- [Technology Stack](#technology-stack)
- [Requirements](#requirements)
- [Installation](#installation)
- [Configuration](#configuration)
- [Quick Start](#quick-start)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Development](#development)
- [Limitations](#limitations)
- [License](#license)

## Features

### Recommender Systems
Learn the fundamentals of recommender systems and how to build them using content-based and collaborative filtering techniques.

### Content-Based Filtering
Explore how to recommend items based on user preferences and item attributes.

### Collaborative Filtering
Dive into collaborative filtering methods, including similarity-based and matrix factorization approaches.

## How It Works

The repository is structured around Jupyter Notebooks for learning and practicing recommender systems. Each notebook provides detailed explanations and exercises using Scikit-Surprise library. The development workflow involves setting up a virtual environment, installing dependencies, and running the notebooks in sequence.

## Technology Stack

| Technology | Purpose |
|------------|---------|
| **JupyterLab** | Interactive computing environment for data analysis, visualization, and machine learning. |
| **Numpy** | Fundamental package for scientific computing with Python. |
| **Pandas** | Data structures and operations for manipulating numerical tables and time series. |
| **Scikit-Learn** | Simple and efficient tools for predictive data analysis. |
| **Scikit-Surprise** | A Python library used especially for building and analyzing recommender systems that deal with explicit rating data. |
| **Matplotlib** | Comprehensive library for creating static, animated, and interactive visualizations in Python. |
| **Seaborn** | Statistical data visualization based on Matplotlib. |

## Requirements

- Python 3.11.3
- JupyterLab 4.3.6
- Numpy 1.26.4
- Pandas 2.2.2
- Scikit-Learn 1.6.1
- Scikit-Surprise 1.1.4
- Matplotlib 3.10.1
- Seaborn 0.13.2

## Installation

### macOS

```bash
pyenv local 3.11.3
python -m venv .venv
source .venv/bin/activate
pip install --upgrade pip
pip install -r requirements.txt
```

### WindowsOS (PowerShell)

```powershell
pyenv local 3.11.3
python -m venv .venv
.venv\Scripts\Activate.ps1
pip install --upgrade pip
pip install -r requirements.txt
```

### WindowsOS (Git-Bash)

```bash
pyenv local 3.11.3
python -m venv .venv
source .venv/Scripts/activate
pip install --upgrade pip
pip install -r requirements.txt
```

*Note: If there are errors during environment setup, try removing the versions from the failing packages in the `requirements.txt` file.*

## Configuration

No specific configuration files or environment variables are required for this project.

## Quick Start

1. **Clone the repository**:
   ```bash
   git clone https://github.com/PartORG/ds-recommender-systems.git
   cd ds-recommender-systems
   ```

2. **Set up your environment** (follow the instructions above based on your operating system).

3. **Open JupyterLab**:
   ```bash
   jupyter lab
   ```

4. **Run the notebooks in order**:
   - `01_content_based.ipynb`
   - `02_exercise_most_popular.ipynb`
   - `03_collaborative_filtering_similarity.ipynb`
   - `03_collaborative_filtering_matrix_factorization.ipynb`
   - `03_exercise_collaborative_filtering.ipynb`
   - `04_recommender_evaluation.ipynb`

## Usage

Each notebook provides detailed instructions and examples. Here are some key commands and entry points:

- **Content-Based Recommender**:
  ```python
  from surprise import Dataset, Reader, KNNWithMeans
  reader = Reader(rating_scale=(1, 5))
  data = Dataset.load_from_df(df[['user_id', 'item_id', 'rating']], reader)
  trainset = data.build_full_trainset()
  algo = KNNWithMeans(k=40, sim_options={'name': 'pearson_baseline', 'user_based': True})
  algo.fit(trainset)
  ```

- **Collaborative Filtering**:
  ```python
  from surprise import SVD
  reader = Reader(rating_scale=(1, 5))
  data = Dataset.load_from_df(df[['user_id', 'item_id', 'rating']], reader)
  trainset = data.build_full_trainset()
  algo = SVD(n_factors=100, n_epochs=20, lr_all=0.0075, reg_all=0.02)
  algo.fit(trainset)
  ```

## Project Structure

```
ds-recommender-systems/
├── .gitignore
├── 01_content_based.ipynb
├── 02_exercise_most_popular.ipynb
├── 03_collaborative_filtering_matrix_factorization.ipynb
├── 03_collaborative_filtering_similarity.ipynb
├── 03_exercise_collaborative_filtering.ipynb
├── 04_recommender_evaluation.ipynb
├── README.md
├── data/
│   ├── fish_1.csv
│   └── user_item_ratings.csv
├── images/
│   ├── KNNExampleCalc.png
│   ├── SVD_USigmaV.png
│   ├── UserItemRatingMatrix.png
│   ├── UserSimilarityMatrix.png
│   ├── book_text.png
│   ├── explode_genre.png
│   ├── fish_text.png
│   ├── movies.png
│   └── str_split_on_movies_genre.png
└── requirements.txt
```

## Development

The repository is structured around Jupyter Notebooks, making it easy to develop and test new features. Each notebook should be self-contained and clearly documented.

## Limitations

- This project focuses on explicit rating data.
- The repository does not include automated testing.

## License

This project is licensed under the [MIT License](LICENSE).