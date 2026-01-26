# Introduction to Recommender Systems
In this repository you will learn the basics of **recommender systems** and how to build them using **content-based** and **collaborative filtering** techniques using `Scikit-Surprise`, a Python library used especially for building and analyzing recommender systems that deal with [`explicit rating`](https://mirumee.com/blog/the-difference-between-implicit-and-explicit-data-for-business) data. 


## The way to success:
Please **work together as Pair Programmers** through all the notebooks
in this particular order:

1. **`Content Based Recommender`**
   + [content based recommender](01_content_based.ipynb)
2. **`Exercise: Build a Most-Popular Movie Recommender`**
   + [Exercise: Most Popular Movie Recommender](02_exercise_most_popular.ipynb)
 
3. **`Collaborative Filtering`**
   + [Collaborative Filtering based on Similarity](03_collaborative_filtering_similarity.ipynb)
   + [Collaborative Filtering based on Matrix Factorization](03_collaborative_filtering_matrix_factorization.ipynb)
   + [Exercise: Build a Collaborative Filtering Movie Recommender System](03_exercise_collaborative_filtering.ipynb)
4. **`Recommender Evaluation`**
   + [How to Evaluate Recommenders](04_recommender_evaluation.ipynb)


## Set up your Environment

The added [requirements file](requirements.txt) contains all libraries and dependencies we need to execute the notebooks.

### **`macOS`** type the following commands : 

- Install the virtual environment and the required packages by following commands:

    ```BASH
    pyenv local 3.11.3
    python -m venv .venv
    source .venv/bin/activate
    pip install --upgrade pip
    pip install -r requirements.txt
    ```
### **`WindowsOS`** type the following commands :

- Install the virtual environment and the required packages by following commands.

   For `PowerShell` CLI :

    ```PowerShell
    pyenv local 3.11.3
    python -m venv .venv
    .venv\Scripts\Activate.ps1
    pip install --upgrade pip
    pip install -r requirements.txt
    ```

    For `Git-Bash` CLI :
    ```
    pyenv local 3.11.3
    python -m venv .venv
    source .venv/Scripts/activate
    pip install --upgrade pip
    pip install -r requirements.txt
    ```


*Note: If there are errors during environment setup, try removing the versions from the failing packages in the requirements file.*

