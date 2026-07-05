# DS Recommender Systems

Learn how to build recommender systems using content-based and collaborative filtering techniques with Scikit-Surprise.

## Requirements

- Python 3.11.3
- jupyterlab==4.3.6
- numpy==1.26.4
- pandas==2.2.2
- scikit-learn==1.6.1
- scikit-surprise==1.1.4
- matplotlib==3.10.1
- seaborn==0.13.2

## Installation

### macOS

```bash
pyenv local 3.11.3
python -m venv .venv
source .venv/bin/activate
pip install --upgrade pip
pip install -r requirements.txt
```

### WindowsOS

#### PowerShell CLI

```powershell
pyenv local 3.11.3
python -m venv .venv
.venv\Scripts\Activate.ps1
pip install --upgrade pip
pip install -r requirements.txt
```

#### Git-Bash CLI

```bash
pyenv local 3.11.3
python -m venv .venv
source .venv/Scripts/activate
pip install --upgrade pip
pip install -r requirements.txt
```

*Note: If there are errors during environment setup, try removing the versions from the failing packages in the `requirements.txt` file.*

## Usage

1. **Content Based Recommender**
   - [content based recommender](01_content_based.ipynb)

2. **Exercise: Build a Most-Popular Movie Recommender**
   - [Exercise: Most Popular Movie Recommender](02_exercise_most_popular.ipynb)

3. **Collaborative Filtering**
   - [Collaborative Filtering based on Similarity](03_collaborative_filtering_similarity.ipynb)
   - [Collaborative Filtering based on Matrix Factorization](03_collaborative_filtering_matrix_factorization.ipynb)
   - [Exercise: Build a Collaborative Filtering Movie Recommender System](03_exercise_collaborative_filtering.ipynb)

4. **Recommender Evaluation**
   - [How to Evaluate Recommenders](04_recommender_evaluation.ipynb)