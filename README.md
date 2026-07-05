# ds-recommender-systems

**Build and Evaluate Recommender Systems with Content-Based and Collaborative Filtering**

[![Language](https://img.shields.io/github/languages/top/PartORG/ds-recommender-systems?color=blue)](https://github.com/PartORG/ds-recommender-systems)
[![Python Version](https://img.shields.io/badge/python-3.11.3-blue.svg)](https://www.python.org/downloads/release/python-3113/)
[![License](https://img.shields.io/github/license/PartORG/ds-recommender-systems?color=green)](LICENSE)
[![Package Manager](https://img.shields.io/badge/package-manager-pip-blue.svg)](https://pip.pypa.io/en/stable/installation/)
[![Framework](https://img.shields.io/badge/framework-jupyterlab-green.svg)](https://jupyter.org/)

Welcome to the `ds-recommender-systems` repository! This project is designed to help you understand and build recommender systems using content-based and collaborative filtering techniques. With this guide, you'll learn how to implement these methods using the `Scikit-Surprise` library in Python.

## Table of Contents
1. [Features](#features)
2. [How It Works](#how-it-works)
3. [Technology Stack](#technology-stack)
4. [Requirements](#requirements)
5. [Installation](#installation)
6. [Configuration](#configuration)
7. [Quick Start](#quick-start)
8. [Usage](#usage)
9. [Project Structure](#project-structure)
10. [Development](#development)
11. [Testing](#testing)
12. [Limitations](#limitations)
13. [License](#license)

## Features
### Content-Based Recommender
- **What it does:** Recommends items based on the similarity of their features.
- **Why it exists:** Useful when you have detailed information about users and items.
- **Why it is useful:** Provides personalized recommendations based on user preferences.

### Collaborative Filtering
- **What it does:** Recommends items to a user based on the behavior of similar users.
- **Why it exists:** Effective for large datasets where item features are not available.
- **Why it is useful:** Can handle both explicit and implicit ratings.

## How It Works
The project follows a structured approach to building recommender systems. You'll start with content-based recommendations, then move on to collaborative filtering techniques using `Scikit-Surprise`.

### Architecture Diagram
```plaintext
+-------------------+
| Content-Based     |
| Recommender       |
+---------+---------+
          |
          v
+---------+---------+
| Collaborative   |
| Filtering       |
+-------------------+
```

## Technology Stack
| Technology | Purpose |
|------------|---------|
| Jupyter Notebook | Interactive environment for data analysis and visualization. |
| Numpy | Fundamental package for scientific computing with Python. |
| Pandas | Data structures and operations for manipulating numerical tables and time series. |
| Scikit-Learn | Simple and efficient tools for predictive data analysis. |
| Scikit-Surprise | A Python library used especially for building and analyzing recommender systems that deal with explicit rating data. |
| Matplotlib | Comprehensive library for creating static, animated, and interactive visualizations in Python. |
| Seaborn | Statistical data visualization based on matplotlib. |

## Requirements
- Python 3.11.3
- Jupyter Notebook

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

## Configuration
No specific configuration files or environment variables are required.

## Quick Start
Follow these steps to get started:

1. **Clone the repository:**
   ```bash
   git clone https://github.com/PartORG/ds-recommender-systems.git
   cd ds-recommender-systems
   ```

2. **Activate your virtual environment and install dependencies:**
   - macOS/Linux:
     ```bash
     source .venv/bin/activate
     pip install -r requirements.txt
     ```
   - Windows (PowerShell):
     ```powershell
     .venv\Scripts\Activate.ps1
     pip install -r requirements.txt
     ```

3. **Run the Jupyter Notebook:**
   ```bash
   jupyter lab
   ```

## Usage
Open the Jupyter Notebook files in the order specified:

1. [Content Based Recommender](01_content_based.ipynb)
2. [Exercise: Build a Most-Popular Movie Recommender](02_exercise_most_popular.ipynb)
3. [Collaborative Filtering based on Similarity](03_collaborative_filtering_similarity.ipynb)
4. [Collaborative Filtering based on Matrix Factorization](03_collaborative_filtering_matrix_factorization.ipynb)
5. [Exercise: Build a Collaborative Filtering Movie Recommender System](03_exercise_collaborative_filtering.ipynb)
6. [How to Evaluate Recommenders](04_recommender_evaluation.ipynb)

## Project Structure
```plaintext
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
This project is open-source and contributions are welcome. Feel free to submit issues or pull requests.

## Testing
No tests are currently available for this project.

## Limitations
- The repository focuses on explicit rating data.
- No real-time recommendation capabilities are implemented.

## License
This project is licensed under the [MIT License](LICENSE).