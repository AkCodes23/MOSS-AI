# Data

Small datasets used by the [notebooks](../notebooks/). Anything larger than a few megabytes
should be downloaded at runtime rather than committed here.

[← Back to the README](../README.md)

---

## `iris.csv`

The Iris flower dataset — 150 samples, three species, four measurements each. Introduced by
Ronald Fisher in 1936 and still the standard first classification problem, because it's small
enough to plot completely and just hard enough to be interesting (two of the three species
overlap).

**Used by:** [`notebooks/knn-iris.ipynb`](../notebooks/knn-iris.ipynb)

| Column | Type | Description |
|---|---|---|
| `Id` | int | Row identifier — drop it before training |
| `SepalLengthCm` | float | Sepal length in centimetres |
| `SepalWidthCm` | float | Sepal width in centimetres |
| `PetalLengthCm` | float | Petal length in centimetres |
| `PetalWidthCm` | float | Petal width in centimetres |
| `Species` | string | Target: `Iris-setosa`, `Iris-versicolor`, `Iris-virginica` |

150 rows, 50 per species, no missing values.

```python
import pandas as pd

df = pd.read_csv('../data/iris.csv').drop(columns=['Id'])
print(df['Species'].value_counts())
```

`scikit-learn` also ships this dataset, without the `Id` column:

```python
from sklearn.datasets import load_iris
X, y = load_iris(return_X_y=True, as_frame=True)
```

**Source:** [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/53/iris)

---

## Adding a dataset

- Keep it under ~5 MB. Larger files bloat every clone, permanently
- Prefer CSV or Parquet over pickles or notebook-embedded blobs
- Add a section here: what it is, the column schema, and where it came from
- If the data is too large or licence-restricted, document the download step in the notebook
  instead of committing the file

See [CONTRIBUTING.md](../CONTRIBUTING.md).
