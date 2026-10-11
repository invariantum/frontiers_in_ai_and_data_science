# Frontiers in AI and Data Science (6CM521): Interactive Course Materials

This repository holds the lectures, labs, notebooks and datasets for the module **Frontiers in AI and Data Science (6CM521)** at Mediterranean College. It is published as a **JupyterLite** website, so students open and run the notebooks **directly in the browser**, with nothing to install.

## Open it in your browser

➡️ **https://invariantum.github.io/frontiers_in_ai_and_data_science/lab/index.html**

The first load takes 10–30 seconds while Python downloads into the browser. After that, it opens in a few seconds.

Use a normal (not private/incognito) Chrome, Edge or Firefox window: in a private window the notebooks cannot see their data files.

## What's inside

All course material is in the [`content/`](content) folder, which appears as the file browser on the left of the site.

| Folder | Topics |
|-|-|
| `00_start_here` | Environment check notebook, assessment brief, useful links |
| `week01_introduction` | Introduction to the module; Python crash course and exercises |
| `week02_data_preprocessing` | Data preprocessing with Pandas: Series, DataFrames, missing data, groupby, merging, input/output |
| `week03_exploratory_data_analysis` | Exploratory data analysis (e-commerce and Titanic examples) |
| `week04_frequent_patterns` | Frequent patterns, association rules, correlation analysis |
| `week05_regression` | Regression; machine learning lab (used in Weeks 5–8) |
| `week06_classification_decision_trees` | Classification and decision tree induction |
| `week07_random_forests_knn` | Random forests and KNN (association rule practice: Week 4 lab) |
| `week08_clustering` | Clustering (unsupervised learning) |
| `week09_generative_ai_prompting` | Generative AI and prompt engineering; LLM APIs lab |
| `week10_reinforcement_learning` | Reinforcement learning |
| `week11_reinforcement_learning_lab` | Reinforcement learning lab (FrozenLake) |
| `week13-14_neural_networks_xai` | Artificial neural networks and explainable AI; fine-tuning and evaluation lab |
| `week15-16_object_detection_explainability` | Object detection; explaining models with SHAP, LIME, ELI5 and Anchor |
| `extras` | Case studies: RAG + MCP + LLMs, agentic AI for economics, LoRA / QLoRA fine-tuning, YOLOv8 |

Every week folder uses the same layout: `lecture/` (slides as PDF to view in the browser, plus the PowerPoint), `lab/` (notebooks in the order to work through them, their data files and lab sheets) and, where needed, `reading/`.

### Naming conventions

* Lowercase, underscores, no spaces: the name typed in code always matches the file.
* Two-digit week numbers (`week02`, `week10`) so folders sort correctly everywhere.
* Notebooks are numbered in the order to do them (`01_`, `02_`, …).
* Slides and lab sheets carry their week in the name (`week05_regression.pdf`), so they stay identifiable after download.
* Data files sit next to the notebooks that use them, and notebooks read them by file name only.
* `_readonly` marks notebooks that need a GPU or libraries that cannot run in a browser. They open with a notice at the top and are meant to be read.

## How to use the notebooks

1. Open the site link above.
2. First time only: open `00_start_here/00_environment_check.ipynb` and choose **Run → Run All Cells**. Every line should say **OK**.
3. Open a week's `lab` folder and double-click a notebook (`.ipynb`).
4. Run a cell with **Shift + Enter**, or all cells with **Run → Run All Cells**.

### Things to know about running in the browser

* **Your changes are saved in your browser only.** To keep your work, right-click the notebook → **Download**. Clearing your browser data deletes your edits; the original files on the site never change.
* **If a notebook looks out of date**, your browser is showing your own older saved copy. Download it if you want to keep your changes, then right-click it → **Delete** and reload the page.
* **Pre-installed libraries:** numpy, pandas, scipy, scikit-learn, statsmodels, matplotlib, seaborn, plotly, ipywidgets, mlxtend, sympy, networkx, pillow, missingno, openpyxl, xlrd, beautifulsoup4, html5lib and tabulate. SQL lessons use Python's built-in `sqlite3`.
* **No internet access from code.** Notebooks cannot download files from websites; every dataset is stored next to its notebook.

## How this site is built

* Course files live in `content/`.
* Each push to `main` runs the GitHub Actions workflow in `.github/workflows/deploy.yml`, which builds the JupyterLite site and deploys it to GitHub Pages.
* The browser Python kernel is **xeus-python**. Its packages and their exact versions are listed in [`environment.yml`](environment.yml); the build tools are in `.github/build-environment.yml`.
* Only pure-Python packages may go under `pip:` in `environment.yml`; anything with compiled code makes the build fail.

### Updating the materials

1. In GitHub Desktop, click **Fetch origin** (and **Pull origin** if it appears) before changing anything.
2. Add, change or delete files inside `content/`, following the naming conventions above.
3. Commit and push to `main`.
4. Wait 2–5 minutes for the **Actions** tab to show a green check, then hard-refresh the site (**Ctrl + F5**).
5. After changing `environment.yml`, run `00_start_here/00_environment_check.ipynb` on the site again.

To upgrade libraries between terms, change the version numbers in `environment.yml`, push, then rerun the environment check and the course notebooks before students use the site.

## Credits

* Built with [JupyterLite](https://github.com/jupyterlite/jupyterlite), [jupyterlite-xeus](https://github.com/jupyterlite/xeus) and the [jupyterlite/demo](https://github.com/jupyterlite/demo) template (BSD-3-Clause license).
* Course materials: *Frontiers in AI and Data Science (6CM521)*.
