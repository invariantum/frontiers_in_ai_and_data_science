# Frontiers in AI and Data Science (6CM521): Interactive Course Materials

[!\[lite-badge](https://jupyterlite.rtfd.io/en/latest/\_static/badge.svg)](https://christsall99.github.io/frontiers_in_ai_and_data_science/lab/index.html)

This repository has all the lectures, labs, notebooks and datasets for the module **Frontiers in AI and Data Science (6CM521)**. It is published as a **JupyterLite** website, so you can open and run the notebooks **directly in your browser**. You don't need to install Python, Anaconda or Jupyter.

The site is built from the [jupyterlite/demo](https://github.com/jupyterlite/demo) template and deployed automatically to GitHub Pages.

## ✨ Open it in your browser

➡️ **https://christsall99.github.io/frontiers\_in\_ai\_and\_data\_science/lab/index.html**

The first load can take 10–30 seconds while the Python runtime (Pyodide) downloads. After that, notebooks open instantly.

## 📚 What's inside

All course material is in the [`content/`](content) folder. It shows up as the file browser on the left side of the JupyterLite site.

|Folder|Topics|
|-|-|
|`Week 1-7/Week 1`|Introduction to the module, Python crash course and exercises|
|`Week 1-7/Week 2`|Data preprocessing, Pandas (Series, DataFrames, missing data, groupby, merging, I/O)|
|`Week 1-7/Week 3`|Exploratory Data Analysis (Titanic and e-commerce examples)|
|`Week 1-7/Week 4`|Mining frequent patterns, association rules, correlation analysis|
|`Week 1-7/Week 5`|Regression problems, Python for machine learning, assessment brief|
|`Week 1-7/Week 6`|Classification and decision tree induction|
|`Week 1-7/Week 7`|Random forests and KNN, association rule mining practice|
|`Week 8-11/Week 8`|Clustering (unsupervised learning)|
|`Week 8-11/Week 9`|Generative AI and prompt engineering|
|`Week 8-11/Week 10`|Reinforcement learning|
|`Week 8-11/Week 11`|Lab session|
|`Week 13-14`|Artificial neural networks and explainable AI (XAI)|
|`Week 15-16`|Object detection (TensorFlow / YOLOv3), model explanation with SHAP, LIME, ELI5, Anchor|
|*(root of `content/`)*|Case studies: RAG + MCP + LLM, agentic AI for economics, LoRA / QLoRA fine-tuning, YOLOv8 on a custom dataset|

Lecture slides (`.pptx`, `.ppt`) and documents (`.pdf`, `.docx`) are included too. You can **download** them from the file browser (right-click → *Download*). PDFs open directly in the browser.

## ▶️ How to use the notebooks

1. Open the site link above.
2. Use the file browser on the left to go to a week's folder.
3. Double-click a `.ipynb` notebook to open it.
4. Run cells with **Shift + Enter**.

### Things to know about running in the browser

* **Your changes are saved in your browser only** (local browser storage). They are not saved to GitHub. To keep your work, right-click the notebook → *Download*.
* **Clearing your browser data deletes your edits.** The original files on the site are never changed.
* **Common libraries work out of the box:** `numpy`, `pandas`, `matplotlib`, `scikit-learn`, `scipy` and others bundled with Pyodide.
* **Extra pure-Python packages** can often be installed inside a notebook with:

```python
  %pip install mlxtend
  ```

* **Some notebooks need a real machine or GPU and will not run in the browser.** These include deep learning and fine-tuning notebooks such as `QLoRA\_customer\_support.ipynb`, `YOLOv8\_object\_detection\_on\_custom\_dataset.ipynb` and the TensorFlow object-detection demo. You can still **read** them here. To run them, use Google Colab, Kaggle or a local Jupyter installation.

## 🛠️ How this site is built

* Course files live in `content/`.
* Each push to the `main` branch runs a GitHub Actions workflow (`.github/workflows/`). It builds the JupyterLite site and deploys it to GitHub Pages.
* The JupyterLite version and kernels are set in `requirements.txt`.

### Updating the materials

1. Add, change or delete files inside `content/` (for example with GitHub Desktop).
2. Commit and push to `main`.
3. Wait about 2–5 minutes for the **Actions** tab to show a green check.
4. Hard-refresh the site (**Ctrl + F5**) to see the new version.

## 🙏 Credits

* Built with [JupyterLite](https://github.com/jupyterlite/jupyterlite) and the [jupyterlite/demo](https://github.com/jupyterlite/demo) template (BSD-3-Clause license).
* Course materials: *Frontiers in AI and Data Science (6CM521)*.

