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

---

## Troubleshooting

### Windows: scikit-surprise Installation Error

If you encounter errors when installing `scikit-surprise` on Windows, such as:
- `"Failed building wheel"`
- `"Microsoft Visual C++ 14.0 is required"`
- `"Unable to find vcvarsall.bat"`
- `"distutils.errors.DistutilsError"`

This happens because `scikit-surprise` requires C++ build tools to compile from source.

#### Solution:

0. **Open Visual Studio 2022 Installer:**
   - If not installed yet, see step 1 to download and install it first

1. **Download Visual Studio Build Tools:**
   - Go to: https://visualstudio.microsoft.com/downloads/
   - Scroll down to **"All Downloads"**
   - Under **"Tools for Visual Studio"**, download **"Build Tools for Visual Studio"** (latest version)

2. **Run the Installer:**
   - Launch the downloaded installer
   - When the Visual Studio Installer opens, you'll see the **"Workloads"** tab

3. **Select the Required Components:**
   - ✅ **ONLY check:** **"Desktop development with C++"**
   - ⚠️ **Important:** Do NOT select all options - this will install unnecessary components and take up significant disk space
   - (Optional) You may also check **"Python development"** under "Web & Cloud"

4. **Install:**
   - Click **"Install"** and wait for the installation to complete (this may take several minutes)

6. **Restart your machine**

7. **Package Installation:**
   - **open** your terminal/command prompt (important: this refreshes environment variables)
   - Run: `pip3 install misaka`
   - Navigate to your project directory
   - Reactivate your virtual environment
   - Run: `pip install -r requirements.txt`

The installation should now complete successfully!

**Additional Resources:** If you continue to experience issues, see [this Stack Overflow discussion](https://stackoverflow.com/questions/48541801/microsoft-visual-c-14-0-is-required-get-it-with-microsoft-visual-c-build-t) for more solutions.