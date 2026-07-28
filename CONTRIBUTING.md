# Contributing

Contributions are welcome from society members and anyone else who finds this repository useful.
The bar is low: if it helps someone learn, it belongs here.

[← Back to the README](README.md)

---

## What to contribute

| Contribution | Where it goes |
|---|---|
| A new resource link | The matching section of [`README.md`](README.md) |
| A worked example or tutorial | [`notebooks/`](notebooks/) |
| A from-scratch implementation | [`code/`](code/) |
| A written explainer | [`docs/`](docs/) |
| A dataset a notebook needs | [`data/`](data/) |
| Cheat sheets, lecture notes (PDF) | [`reference/`](reference/) |
| A fix for a broken link or typo | Wherever it is — no issue needed |

---

## How to submit

```bash
# 1. Fork the repository on GitHub, then clone your fork
git clone https://github.com/<your-username>/MOSS-AI.git
cd MOSS-AI

# 2. Branch
git checkout -b add-transformer-notebook

# 3. Make your changes, then commit
git add .
git commit -m "Add notebook on positional encodings"

# 4. Push and open a pull request
git push -u origin add-transformer-notebook
```

New to this? [docs/git-and-github.md](docs/git-and-github.md) covers the basics.

---

## Conventions

### File names

- **Lowercase, hyphen-separated:** `gradient-boosting.ipynb`, not `Gradient Boosting FINAL.ipynb`
- **No spaces, no parentheses, no trailing spaces.** They break URLs, shell commands and imports
- **Always use a file extension.** A file named `notes` with no extension won't render on GitHub
- **Describe the content, not the author.** `random-forests.ipynb`, not `RF_yourname.ipynb` —
  credit goes in the notebook itself and in [`notebooks/README.md`](notebooks/README.md)

### Notebooks

- Open with a markdown cell: title, one-line objective, and your name
- Explain **why**, not just what — a wall of uncommented code teaches nothing
- **Use relative paths.** `pd.read_csv('../data/iris.csv')`, never `C:\Users\you\...`
- Restart and run all before committing, so outputs match the code
- Keep the dataset small enough to commit, or document where to download it
- Add your notebook to the table in [`notebooks/README.md`](notebooks/README.md) and in the
  [Notebooks section](README.md#notebooks) of the main README

### Code

- Python 3.9+, [PEP 8](https://peps.python.org/pep-0008/) formatting
- A module docstring saying what the file does and how to run it
- If you add a dependency, add it to [`requirements.txt`](requirements.txt)

### Resource links

- **Use the canonical URL** — the publisher's page, the arXiv abstract, the GitHub repo.
  Avoid `lnkd.in`, `bit.ly` and other shorteners: nobody can tell where they lead, and they rot
- One line per resource: `**[Title](url)** — what it is and who it's for`
- Say why it's worth someone's time. "Good course" tells the reader nothing
- **Check it isn't already listed.** Every resource should appear exactly once
- Free resources are valued most highly here — mark them if it isn't obvious

---

## Review

Pull requests are reviewed by the AI Chapter maintainers. Expect questions about scope and
duplication rather than style — those are the things that make a resource list decay.

Not sure whether something fits? [Open an issue](https://github.com/AkCodes23/MOSS-AI/issues)
and ask before you write it.

---

## Code of conduct

Be helpful and be patient. Most people reading this repository are beginners, and the point of
the whole thing is to make starting easier than it was for you.

Attribute other people's work. If you adapt a notebook, tutorial or explainer from elsewhere,
link the original.
