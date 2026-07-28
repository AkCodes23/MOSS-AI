# Notebooks

Runnable Jupyter notebooks. Each one is self-contained — open it, run it top to bottom, then
change something and see what breaks.

[← Back to the README](../README.md)

---

## What's here

| Notebook | Topic | Level | Contributor |
|---|---|---|---|
| [`knn-iris.ipynb`](knn-iris.ipynb) | K-Nearest Neighbours with full EDA on Iris | Beginner | MOSS AI Chapter |
| [`random-forests.ipynb`](random-forests.ipynb) | Random Forests — compact walkthrough | Beginner | MOSS AI Chapter |
| [`random-forests-deep-dive.ipynb`](random-forests-deep-dive.ipynb) | Random Forests in depth, with diagrams | Intermediate | Keshav Krishna Singh |
| [`gradient-boosting.ipynb`](gradient-boosting.ipynb) | XGBoost, CatBoost and LightGBM compared | Intermediate | MOSS AI Chapter |
| [`perceptron.ipynb`](perceptron.ipynb) | The perceptron built from scratch in TensorFlow | Intermediate | Hrishik Patel |

Supporting images live in [`assets/`](assets/).

---

## Running them

From the repository root:

```bash
python -m venv .venv
source .venv/bin/activate          # Windows: .venv\Scripts\activate
pip install -r requirements.txt

cd notebooks
jupyter notebook
```

Or open any notebook in [Google Colab](https://colab.research.google.com/) —
**File → Open notebook → GitHub**, then paste `AkCodes23/MOSS-AI`. On Colab you'll need to
install the gradient-boosting libraries yourself:

```python
!pip install xgboost lightgbm catboost
```

---

## Suggested order

1. **[`knn-iris.ipynb`](knn-iris.ipynb)** — the gentlest start. Covers loading data, cleaning,
   visualising, and a first classifier, all on a dataset small enough to hold in your head.
2. **[`random-forests.ipynb`](random-forests.ipynb)** — your first ensemble method, and why
   combining weak models beats tuning one.
3. **[`random-forests-deep-dive.ipynb`](random-forests-deep-dive.ipynb)** — the same algorithm
   with the theory filled in: bagging, feature importance, out-of-bag error.
4. **[`gradient-boosting.ipynb`](gradient-boosting.ipynb)** — boosting instead of bagging, and a
   head-to-head of the three libraries that win most Kaggle competitions.
5. **[`perceptron.ipynb`](perceptron.ipynb)** — the jump to neural networks, one neuron at a time.
   From here, go to [`code/transformers/`](../code/transformers/).

---

## Data

| Notebook | Data it needs | Where it comes from |
|---|---|---|
| `knn-iris.ipynb` | [`../data/iris.csv`](../data/iris.csv) | In this repository |
| `random-forests.ipynb` | Iris | Loaded from `sklearn.datasets` at runtime |
| `random-forests-deep-dive.ipynb` | Loaded in-notebook | Included |
| `perceptron.ipynb` | None — synthetic | Generated in-notebook |
| `gradient-boosting.ipynb` | `train.csv`, `test.csv`, `sample_submission.csv` | **Not included** — see below |

**Known gap:** `gradient-boosting.ipynb` reads Kaggle competition files (`train.csv`, `test.csv`,
`sample_submission.csv`) for a road-accident-risk prediction task. Those files aren't in this
repository. Read the notebook for the method and the library comparison; to execute it, download
the competition data from Kaggle into this folder first. If you know the exact competition, a PR
adding the link to this table would be genuinely useful.

---

## Adding a notebook

See [CONTRIBUTING.md](../CONTRIBUTING.md). The short version:

- Lowercase, hyphen-separated file name that describes the **topic**, not the author
- Open with a markdown cell: title, one-line objective, your name
- Relative data paths only — `pd.read_csv('../data/iris.csv')`, never an absolute path from your
  own machine
- Restart and run all before committing
- Add a row to the table above and to the [main README](../README.md#notebooks)
