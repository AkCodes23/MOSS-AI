# MOSS AI — Manipal Open Source Society

A curated, self-contained starting point for learning **artificial intelligence and machine
learning** — maintained by the AI Chapter of the Manipal Open Source Society.

Everything here is free to read, run, and fork:

- **Explainers** you can read right now — [`docs/`](docs/)
- **Notebooks and code** you can run right now — [`notebooks/`](notebooks/), [`code/`](code/)
- **A curated index** of the best external books, courses, papers and tools — [below](#resource-library)

Maintained by **Akhil Varanasi**, Head of AI. Contributions welcome — see [Contributing](#contributing).

---

## Contents

**Getting oriented**
[What's in this repository](#whats-in-this-repository) ·
[Quick start](#quick-start) ·
[Learning roadmap](#learning-roadmap) ·
[Explainers](#explainers) ·
[Notebooks](#notebooks) ·
[Code](#code)

**Resource library**
[Books](#books) ·
[Courses](#courses) ·
[Video tutorials](#video-tutorials) ·
[YouTube channels](#youtube-channels) ·
[Research papers](#research-papers) ·
[GitHub repositories](#github-repositories) ·
[Guides & whitepapers](#guides--whitepapers)

**Specialisations**
[AI agents & LLMs](#ai-agents--llms) ·
[RAG](#rag--retrieval-augmented-generation) ·
[MLOps & production](#mlops--production) ·
[CUDA & GPU programming](#cuda--gpu-programming) ·
[Computer vision, NLP & RL](#computer-vision-nlp--reinforcement-learning)

**Practice & community**
[Tools & libraries](#tools--libraries) ·
[Datasets](#datasets) ·
[Practice platforms](#practice-platforms) ·
[Newsletters & communities](#newsletters--communities)

**Project**
[Contributing](#contributing) ·
[Contact](#contact) ·
[License](#license)

---

## What's in this repository

| Folder | What it holds | Start with |
|---|---|---|
| [`docs/`](docs/) | Written explainers on AI fundamentals, generative AI and Git | [Get Started with AI](docs/get-started-with-ai.md) |
| [`notebooks/`](notebooks/) | Runnable Jupyter notebooks with worked examples | [KNN on Iris](notebooks/knn-iris.ipynb) |
| [`code/`](code/) | Standalone from-scratch implementations | [Transformer from scratch](code/transformers/) |
| [`data/`](data/) | Small datasets the notebooks depend on | [`data/README.md`](data/README.md) |
| [`reference/`](reference/) | PDF cheat sheets and lecture notes | [ML cheat sheet](reference/ml-cheatsheet.pdf) |

---

## Quick start

You need Python 3.9 or newer. Everything here runs locally or on
[Google Colab](https://colab.research.google.com/) — no paid services required.

```bash
git clone https://github.com/AkCodes23/MOSS-AI.git
cd MOSS-AI

python -m venv .venv
source .venv/bin/activate          # Windows: .venv\Scripts\activate

pip install -r requirements.txt
jupyter notebook
```

Prefer not to install anything? Open any notebook directly in Colab —
**File → Open notebook → GitHub**, then paste `AkCodes23/MOSS-AI`.

**Setup checklist**

- [ ] Python 3.9+ installed and on your `PATH`
- [ ] Virtual environment created and activated
- [ ] `pip install -r requirements.txt` finished without errors
- [ ] [`notebooks/knn-iris.ipynb`](notebooks/knn-iris.ipynb) runs top to bottom
- [ ] Accounts created: [GitHub](https://github.com), [Kaggle](https://www.kaggle.com), [Google Colab](https://colab.research.google.com)
- [ ] Git basics understood — [docs/git-and-github.md](docs/git-and-github.md)

---

## Learning roadmap

A realistic path from zero to building things. Times assume roughly 8–10 hours a week.

| # | Stage | Time | What you learn | Start here |
|---|---|---|---|---|
| 1 | **Programming basics** | 1–2 weeks | Loops, functions, OOP in Python | [Google's Python Class](https://developers.google.com/edu/python) |
| 2 | **Mathematics** | 2–3 weeks | Linear algebra, calculus, probability | [Mathematics for Machine Learning](https://mml-book.github.io) |
| 3 | **Statistics & EDA** | 2–3 weeks | Hypothesis testing, correlation, pandas | [Kaggle: Pandas](https://www.kaggle.com/learn/pandas) |
| 4 | **Data cleaning** | 1–2 weeks | Missing data, outliers, feature scaling | [Kaggle: Data Cleaning](https://www.kaggle.com/learn/data-cleaning) |
| 5 | **Machine learning** | 3–4 weeks | Regression, KNN, trees, ensembles | [Andrew Ng's ML Specialization](https://www.coursera.org/specializations/machine-learning-introduction) |
| 6 | **Deep learning** | 4–6 weeks | Neural nets, CNNs, RNNs, transformers | [Deep Learning Specialization](https://www.coursera.org/specializations/deep-learning) |
| 7 | **Projects** | ongoing | Ship something end to end | [Kaggle Competitions](https://www.kaggle.com/competitions) |

**Practise as you go.** Each stage has a matching notebook in this repo — stage 5 maps to
[`knn-iris.ipynb`](notebooks/knn-iris.ipynb) and [`random-forests.ipynb`](notebooks/random-forests.ipynb),
stage 6 to [`perceptron.ipynb`](notebooks/perceptron.ipynb) and [`code/transformers/`](code/transformers/).

Three things that matter more than the order:

1. **Build, break, and fix.** Tutorials teach recognition; projects teach recall.
2. **Finish small things.** A working model beats a half-read textbook.
3. **Use AI tools to learn faster** — but read the code they write before you trust it.

For the full topic-by-topic breakdown, see the [AI syllabus](docs/ai-syllabus.md).

---

## Explainers

Plain-language write-ups, no setup required.

| Document | What it covers |
|---|---|
| [Get Started with AI](docs/get-started-with-ai.md) | What AI is, why it's hard to define, the four capability types |
| [Generative AI: An Overview](docs/generative-ai-overview.md) | Why ChatGPT changed things, and what LLMs can actually do |
| [Generative AI In Depth](docs/generative-ai-in-depth.md) | The tech stack, what drives progress, ethics and limitations |
| [AI Syllabus](docs/ai-syllabus.md) | Complete topic checklist, linear algebra through research methodology |
| [Git and GitHub](docs/git-and-github.md) | Version control basics every contributor needs |

---

## Notebooks

| Notebook | Topic | Level |
|---|---|---|
| [`knn-iris.ipynb`](notebooks/knn-iris.ipynb) | K-Nearest Neighbours with full EDA on the Iris dataset | Beginner |
| [`random-forests.ipynb`](notebooks/random-forests.ipynb) | Random Forests — compact, focused walkthrough | Beginner |
| [`random-forests-deep-dive.ipynb`](notebooks/random-forests-deep-dive.ipynb) | Random Forests in depth, with diagrams and theory | Intermediate |
| [`gradient-boosting.ipynb`](notebooks/gradient-boosting.ipynb) | XGBoost, CatBoost and LightGBM compared | Intermediate |
| [`perceptron.ipynb`](notebooks/perceptron.ipynb) | The perceptron, built from scratch in TensorFlow | Intermediate |

Dependencies, contributors and known gaps: [`notebooks/README.md`](notebooks/README.md).

## Code

[`code/transformers/`](code/transformers/) — a minimal GPT built from nothing but PyTorch
primitives: self-attention, multi-head attention, and a full training loop in under 200 lines.

```bash
cd code/transformers
python tiny_gpt.py
```

---
---

# Resource library

Every resource appears **once**, in the section matching what it is. Free resources are marked.

> **A note on links.** Some URLs use LinkedIn's `lnkd.in` shortener, inherited from where the
> resource was originally shared — they work, but you can't see the destination before clicking.
> When adding anything new, please use the canonical URL. See [CONTRIBUTING.md](CONTRIBUTING.md).

---

## Books

### Free and open

Start here. No purchase needed, and these are genuinely among the best available.

| Book | Author(s) | Why read it |
|---|---|---|
| [Mathematics for Machine Learning](https://mml-book.github.io) | Deisenroth, Faisal, Ong | The maths you actually need, nothing more |
| [Understanding Deep Learning](https://udlbook.github.io/udlbook/) | Simon Prince | Modern, visual, current — the best free DL text today |
| [Deep Learning](http://www.deeplearningbook.org/) | Goodfellow, Bengio, Courville | The canonical reference. Dense, but definitive |
| [Dive into Deep Learning](https://d2l.ai/) | Zhang, Lipton, Li, Smola | Every concept paired with runnable code |
| [Speech and Language Processing](https://web.stanford.edu/~jurafsky/slp3/) | Jurafsky & Martin | NLP from n-grams to transformers |
| [Pattern Recognition and Machine Learning](https://www.microsoft.com/en-us/research/publication/pattern-recognition-machine-learning/) | Christopher Bishop | The Bayesian view of ML |
| [Reinforcement Learning: An Introduction](http://incompleteideas.net/book/the-book-2nd.html) | Sutton & Barto | The RL textbook, free from the authors |

### Practical and hands-on

- **[Hands-On Machine Learning with Scikit-Learn, Keras & TensorFlow](https://lnkd.in/gxcjbJRp)** — Aurélien Géron
  The best first ML book. The whole classical pipeline, then neural networks. *Roadmap stages 4–6.*
- **[AI Engineering](https://www.oreilly.com/library/view/ai-engineering/9781098166298/)** — Chip Huyen
  Building production systems on top of foundation models.
- **[Machine Learning Book (mirror)](https://drive.google.com/file/d/1aNOunm89etXOSlpIqi_mENGtWT6pRJjp/view?usp=sharing)**
  Foundational algorithms and concepts.

### Mathematics

- **[Mathematics for Machine Learning](https://mml-book.github.io)** — see *Free and open* above
- **[45+ Mathematics Books Every Data Scientist Needs](https://lnkd.in/ghBXQfPc)** — a reference shelf, not a reading list

> **Don't** try to finish a maths textbook before starting ML. Learn linear algebra and
> probability to working depth, then come back when a model confuses you.

### LLMs and AI agents

The fastest-dating category — check publication dates before buying.

| Book | Author | Focus |
|---|---|---|
| [Build a Large Language Model (From Scratch)](https://www.manning.com/books/build-a-large-language-model-from-scratch) | Sebastian Raschka | Implementing a GPT end to end |
| [Hands-On Large Language Models](https://lnkd.in/dxaVF86w) | Alammar & Grootendorst | Using and adapting LLMs, heavily illustrated |
| [The LLM Engineering Handbook](https://lnkd.in/gWUT2EXe) | — | Deployment, evaluation and operations |
| [AI Agents: The Definitive Guide](https://lnkd.in/dJ9wFNMD) | Nicole Koenigstein | Agent architectures and design |
| [Building Applications with AI Agents](https://lnkd.in/dSs8srk5) | Michael Albada | Applied agent systems |
| [AI Agents with MCP](https://lnkd.in/dR22bEiZ) | Kyle Stratis | Model Context Protocol in practice |

**Reading order:** *Build a Large Language Model (From Scratch)* → *AI Engineering* → the agent books.

---

## Courses

### Foundations

| Course | Provider | Time | Covers |
|---|---|---|---|
| [Google's Python Class](https://developers.google.com/edu/python) | Google | ~2 weeks | Python syntax, strings, lists, files |
| [Kaggle Learn](https://www.kaggle.com/learn) | Kaggle | 3–4 hrs each | Bite-sized, interactive, free certificates |
| [Kaggle: Pandas](https://www.kaggle.com/learn/pandas) | Kaggle | 4 hrs | Data manipulation — the daily-driver skill |
| [Kaggle: Data Cleaning](https://www.kaggle.com/learn/data-cleaning) | Kaggle | 4 hrs | Missing values, scaling, dates, encodings |
| [Machine Learning Crash Course](https://developers.google.com/machine-learning/crash-course) | Google | ~15 hrs | ML fundamentals with TensorFlow |

### Core machine learning

- **[Machine Learning Specialization](https://www.coursera.org/specializations/machine-learning-introduction)** — Andrew Ng / DeepLearning.AI
  The course that taught a generation. Still the best first ML course. *Roadmap stage 5.*
- **[Machine Learning Theory (CS229)](https://www.youtube.com/watch?v=jGwO_UgTS7I&list=PLoROMvodv4rMiGQp3WXShtMGgzqpfVfbU)** — Stanford Online
  The rigorous version, with full derivations.

### Deep learning

| Course | Provider | Approach |
|---|---|---|
| [Deep Learning Specialization](https://www.coursera.org/specializations/deep-learning) | Andrew Ng / DeepLearning.AI | Bottom-up: intuition first, then models |
| [Practical Deep Learning for Coders](https://course.fast.ai/) | [fast.ai](https://www.fast.ai/) | Top-down: train a working model in lesson one |
| [Introduction to Deep Learning (6.S191)](https://youtube.com/playlist?list=PLtBw6njQRU-rwp5__7C0oIVt26ZgjG9NI) | MIT | Fast, current, lecture-style |
| [Neural Networks: Zero to Hero](https://karpathy.ai/zero-to-hero.html) | Andrej Karpathy | Build backprop, then a GPT, from scratch |
| [Language Modeling From Scratch](https://lnkd.in/g84KRW96) | — | The mechanics of training a language model |

> **Pick one and finish it.** fast.ai for fast results; Andrew Ng for theory first;
> Karpathy if you learn by watching someone type.

### Data science and interview prep

- [400+ Data Science Resources](https://lnkd.in/gv9yvfdd) — a large curated collection
- [Python Data Science Library](https://lnkd.in/gHSDtsmA) — comprehensive Python DS guide
- [Premium Data Science Interview Resources](https://lnkd.in/gPrWQ8is) — interview preparation

Agent and LLM courses are grouped under [AI agents & LLMs](#ai-agents--llms).

---

## Video tutorials

Single videos for when you need exactly one topic.

### Python and tooling

| Video | Length | Covers |
|---|---|---|
| [Python for Everybody](https://www.youtube.com/watch?v=rfscVS0vtbw) | 4 hrs | Complete Python from zero |
| [Object-Oriented Programming in Python](https://www.youtube.com/watch?v=iLRZi0Gu8Go) | 1 hr | Classes, inheritance, methods |
| [Data Structures & Algorithms](https://www.youtube.com/watch?v=pkYVOmU3MgA) | 5 hrs | The interview fundamentals |

### Data handling

| Video | Length | Covers |
|---|---|---|
| [Pandas Tutorial](https://www.youtube.com/watch?v=2uvysYbKdjM) | 1 hr | Keith Galli's practical walkthrough |
| [NumPy Tutorial](https://www.youtube.com/watch?v=QUT1VHiLmmI) | 1 hr | Arrays, broadcasting, vectorisation |
| [Matplotlib Tutorial](https://www.youtube.com/watch?v=3Xc3CA655Y4) | 1 hr | Plotting and visualisation |
| [Data Loading Techniques](https://www.youtube.com/watch?v=T23Bs75F7ZQ) | — | Reading data efficiently at scale |

### Machine learning and deep learning

Full lecture series are listed under [Courses](#courses) — Stanford's CS229 and MIT's 6.S191 are
both there, and both are free on YouTube.

---

## YouTube channels

Thirty channels, grouped by what you'd use them for. If you subscribe to only two, make them
**3Blue1Brown** and **StatQuest**.

### Start here — intuition before formalism

| Channel | Why |
|---|---|
| [3Blue1Brown](https://www.youtube.com/@3blue1brown) | The maths behind AI, made visual. Watch the neural network and linear algebra series |
| [StatQuest](https://www.youtube.com/@statquest) | Josh Starmer explains statistics and ML algorithms clearly, and makes it fun |
| [Serrano Academy](https://www.youtube.com/@SerranoAcademy) | Luis Serrano's step-by-step breakdowns — excellent when a concept won't click |
| [CodeEmporium](https://www.youtube.com/@CodeEmporium) | Algorithm explanations with clean visualisations |

### Go deeper — academic rigour

| Channel | Why |
|---|---|
| [Stanford Online](https://www.youtube.com/@stanfordonline) | Full CS229, CS231n and CS224n lectures, free |
| [MIT OpenCourseWare](https://www.youtube.com/@mitocw) | Rigorous theory across the whole curriculum |
| [Andrej Karpathy](https://www.youtube.com/@AndrejKarpathy) | Neural networks built from scratch, live. Rare clarity |
| [Steve Brunton](https://www.youtube.com/@Eigensteve) | Scientific ML, control theory, dynamical systems |

### Learn to build — code on screen

| Channel | Why |
|---|---|
| [Umar Jamil](https://www.youtube.com/@umarjamilai) | Transformers and LLMs implemented line by line |
| [Jeremy Howard](https://www.youtube.com/@howardjeremyp) | Practical deep learning, the fast.ai philosophy |
| [DeepLearning.AI](https://www.youtube.com/@Deeplearningai) | Structured paths from Andrew Ng's team |
| [Hugging Face](https://www.youtube.com/@HuggingFace) | Modern open-source tooling, from the people building it |
| [sentdex](https://www.youtube.com/@sentdex) | Python ML projects, start to finish |
| [Data School](https://www.youtube.com/@dataschool) | scikit-learn and pandas for beginners, done properly |
| [Codebasics](https://www.youtube.com/@codebasics) | Real-world use cases and career-focused projects |
| [freeCodeCamp](https://www.youtube.com/@freecodecamp) | Multi-hour complete courses, free |

### Stay current — research as it lands

| Channel | Why |
|---|---|
| [Yannic Kilcher](https://www.youtube.com/@YannicKilcher) | Paper deep dives with genuine technical criticism |
| [Two Minute Papers](https://www.youtube.com/@TwoMinutePapers) | Research summaries, fast |
| [Arxiv Insights](https://www.youtube.com/@ArxivInsights) | Beginner-friendly explanations of hard papers |
| [Machine Learning Street Talk](https://www.youtube.com/@MachineLearningStreetTalk) | Long technical debates between researchers |
| [AI Explained](https://www.youtube.com/@aiexplained-official) | Careful analysis of new models and capabilities |
| [AI Coffee Break with Letitia](https://www.youtube.com/@AICoffeeBreak) | Accessible research explainers |
| [Hamel Husain](https://lnkd.in/eSgQMg_d) | LLM evaluation, RAG and fine-tuning, from practice |

### Apply it — production and industry

| Channel | Why |
|---|---|
| [Kaggle](https://www.youtube.com/@kaggle) | Competition walkthroughs and real workflows |
| [Google Cloud Tech](https://www.youtube.com/@googlecloudtech) | Deploying and managing models at scale |
| [Matt Wolfe](https://www.youtube.com/@mreflow) | What shipped this week in AI tooling |
| [The AI Advantage](https://www.youtube.com/@aiadvantage) | Applying AI to actual business work |
| [Siraj Raval](https://www.youtube.com/@SirajRaval) | Creative, project-driven AI |

### Learn from the people building it

| Channel | Why |
|---|---|
| [Lex Fridman](https://www.youtube.com/@lexfridman) | Long-form interviews with leading researchers |
| [Tina Huang](https://www.youtube.com/@TinaHuang1) | Learning strategy and career navigation |

---

## Research papers

All links go to free arXiv or publisher pages. Read the abstract and figures first — full papers
are for the second pass.

### The foundations

| Paper | Year | Why it matters |
|---|---|---|
| [Attention Is All You Need](https://arxiv.org/abs/1706.03762) | 2017 | The transformer. Start here — everything modern descends from it |
| [Deep Residual Learning (ResNet)](https://arxiv.org/abs/1512.03385) | 2015 | Skip connections made very deep networks trainable |
| [Batch Normalization](https://arxiv.org/abs/1502.03167) | 2015 | Why training got dramatically faster and more stable |
| [Dropout](https://jmlr.org/papers/v15/srivastava14a.html) | 2014 | The regularisation idea you'll use in every model |
| [Adam: A Method for Stochastic Optimization](https://arxiv.org/abs/1412.6980) | 2014 | The default optimiser, and why |
| [Efficient Estimation of Word Representations (word2vec)](https://arxiv.org/abs/1301.3781) | 2013 | Where embeddings began |

### Language models

| Paper | Year | Why it matters |
|---|---|---|
| [BERT](https://arxiv.org/abs/1810.04805) | 2018 | Bidirectional pre-training; the encoder-only branch |
| [Language Models are Few-Shot Learners (GPT-3)](https://arxiv.org/abs/2005.14165) | 2020 | Scale as a capability unlock; in-context learning |
| [Training LMs to Follow Instructions (InstructGPT)](https://arxiv.org/abs/2203.02155) | 2022 | RLHF — how raw models became assistants |
| [LoRA: Low-Rank Adaptation](https://arxiv.org/abs/2106.09685) | 2021 | Fine-tuning large models on a single GPU |

### Vision and generative models

| Paper | Year | Why it matters |
|---|---|---|
| [Generative Adversarial Networks](https://arxiv.org/abs/1406.2661) | 2014 | The generator-vs-discriminator idea |
| [An Image is Worth 16x16 Words (ViT)](https://arxiv.org/abs/2010.11929) | 2020 | Transformers took over vision too |
| [Denoising Diffusion Probabilistic Models](https://arxiv.org/abs/2006.11239) | 2020 | The basis of Stable Diffusion and friends |

### Reinforcement learning

| Paper | Year | Why it matters |
|---|---|---|
| [Playing Atari with Deep RL (DQN)](https://arxiv.org/abs/1312.5602) | 2013 | Deep networks as value functions |
| [Proximal Policy Optimization (PPO)](https://arxiv.org/abs/1707.06347) | 2017 | The workhorse policy-gradient method, and the engine behind RLHF |

### Agents and reasoning

| Paper | Why it matters |
|---|---|
| [Chain-of-Thought Prompting](https://arxiv.org/abs/2201.11903) | Reasoning through intermediate steps |
| [ReAct: Synergizing Reasoning and Acting](https://arxiv.org/abs/2210.03629) | The think-act-observe loop nearly every agent uses |
| [Toolformer](https://arxiv.org/abs/2302.04761) | Models teaching themselves to call tools |
| [Reflexion](https://arxiv.org/abs/2303.11366) | Agents that critique and retry their own work |
| [Tree of Thoughts](https://arxiv.org/abs/2305.10601) | Searching over reasoning paths instead of one chain |
| [Generative Agents](https://arxiv.org/abs/2304.03442) | Believable simulated behaviour from LLMs |

RAG papers are grouped under [RAG](#rag--retrieval-augmented-generation).

### Finding new papers

- **[Papers with Code](https://paperswithcode.com/)** — papers paired with working implementations
- **[Connected Papers](https://www.connectedpapers.com/)** — visual maps of a research area
- **[ArXiv Sanity Preserver](http://www.arxiv-sanity.com/)** — better arXiv browsing and filtering

---

## GitHub repositories

Repos worth reading end to end, not just starring.

### Learning curricula

| Repo | What it is |
|---|---|
| [Machine Learning for Beginners](https://github.com/microsoft/ML-For-Beginners) | Microsoft's 12-week, 26-lesson ML curriculum |
| [AI Agents for Beginners](https://github.com/microsoft/ai-agents-for-beginners) | Microsoft's agent course, lesson by lesson |
| [LLM Course](https://github.com/mlabonne/llm-course) | Maxime Labonne's complete LLM roadmap with notebooks |
| [Hands-On AI Engineering](https://github.com/Sumanth077/Hands-On-AI-Engineering) | Practical AI engineering walkthroughs |

### Curated collections

| Repo | What it is |
|---|---|
| [Awesome Generative AI Guide](https://github.com/aishwaryanr/awesome-generative-ai-guide) | Papers, courses and interview prep for GenAI |
| [GenAI Agents](https://github.com/NirDiamant/GenAI_Agents) | Working agent implementations, many patterns |
| [GenAI Agents Collection](https://lnkd.in/dEt72MEy) | Further curated agent resources |
| [Designing Machine Learning Systems](https://lnkd.in/dEx8sQJK) | ML system design patterns |

### Production and practice

| Repo | What it is |
|---|---|
| [Made with ML](https://madewithml.com/) | Production ML from design through deployment |
| [Prompt Engineering Guide](https://www.promptingguide.ai/) | The reference for prompting techniques |
| [Kaggle Competitions](https://www.kaggle.com/competitions) | Real problems with real leaderboards. *Roadmap stage 7* |

---

## Guides & whitepapers

- **[Google's Agent Whitepaper](https://lnkd.in/gFvCfbSN)** — comprehensive agent design guide
- **[Google's Agent Companion](https://lnkd.in/gfmCrgAH)** — supplementary agent material
- **[Building Effective Agents by Anthropic](https://lnkd.in/gRWKANS4)** — patterns that hold up in production
- **[Claude Code Best Agentic Coding Practices](https://lnkd.in/gs99zyCf)** — agentic coding patterns
- **[OpenAI's Practical Guide to Building Agents](https://lnkd.in/guRfXsFK)** — OpenAI's agent framework

---

## AI agents & LLMs

Everything agent-related, ordered as a path rather than a pile. Prerequisites: comfortable
Python, and a working understanding of neural networks.

### 1. Understand the machine first

Don't build agents on top of a black box. Build the box.

- [Neural Networks: Zero to Hero](https://karpathy.ai/zero-to-hero.html) — backprop, then a GPT
- [Introduction to Large Language Models](https://www.youtube.com/watch?v=zjkBMFhNj_g) — what an LLM is and how it's trained
- [LLMs from Scratch](https://www.youtube.com/watch?v=9vM4p9NN0Ts) — a language model end to end
- [`code/transformers/`](code/transformers/) — **in this repo**: a working minimal GPT
- [Attention Is All You Need](https://arxiv.org/abs/1706.03762) — the paper behind all of it

### 2. Learn the agent loop

- [Agentic AI Overview (Stanford)](https://www.youtube.com/watch?v=kJLiOGle3Lw) — the landscape
- [Building an Agent from Scratch](https://www.youtube.com/watch?v=xzXdLRUyjUg) — the loop, minus the frameworks
- [Building Effective Agents](https://www.youtube.com/watch?v=D7_ipDqhtwk) — patterns that survive production
- [HuggingFace Agents Course](https://huggingface.co/learn/agents-course) — the best structured on-ramp
- [Philo Agents playlist](https://www.youtube.com/playlist?list=PLacQJwuclt_sV-tfZmpT1Ov6jldHl30NR) — a full development series
- [Learn the basics first](https://lnkd.in/gTQyc_fi) — if any of the above lost you

### 3. Give agents memory and tools

- [Agent Memory](https://lnkd.in/gNFpC542) — short- and long-term memory design
- [Building Vector Databases with Pinecone](https://lnkd.in/gCS4sd7Y) — vector storage fundamentals
- [Vector Databases: from Embeddings to Applications](https://lnkd.in/gm9HR6_2) — the fuller treatment
- [MCP with Anthropic](https://lnkd.in/geffcwdq) — the Model Context Protocol
- [Building Agents with MCP](https://www.youtube.com/watch?v=kQmXtrmQ5Zg) — MCP in practice
- [Computer Use with Anthropic](https://lnkd.in/gMUWg7Fa) — agents that drive a desktop
- [Building Browser Agents](https://lnkd.in/gsMmCifQ) — web automation

Retrieval gets its own section: [RAG](#rag--retrieval-augmented-generation).

### 4. Design for more than one agent

- [Agent Design Patterns](https://lnkd.in/gzKvx5A4) — the recurring architectures
- [Multi-Agent Use](https://lnkd.in/gU9DY9kj) — coordinating several agents
- [Multi-Agent Systems](https://lnkd.in/gUayts9s) — collaboration and delegation

### 5. Evaluate and operate

The step most people skip, and the reason most agents fail.

- [Building and Evaluating Agents](https://www.youtube.com/watch?v=d5EltXhbcfA) — construction plus measurement
- [Evaluating AI Agents](https://lnkd.in/gHJtwF5s) — how to know if your agent actually works
- [Improving LLM Accuracy](https://lnkd.in/gsE-4FvY) — prompting, tuning, grounding
- [LLMOps](https://lnkd.in/g7bHU37w) — running LLM systems in production

### 6. Go academic

- [Berkeley LLM Agents MOOC](https://lnkd.in/gqyKWE3A) — the foundational semester
- [Berkeley Advanced LLM Agents MOOC](https://lnkd.in/gydt98kW) — the follow-up

**Also relevant:** [agent books](#llms-and-ai-agents) ·
[agent papers](#agents-and-reasoning) ·
[agent repos](#curated-collections) ·
[guides & whitepapers](#guides--whitepapers)

---

## RAG — Retrieval-Augmented Generation

Giving a model access to knowledge it wasn't trained on. Work through in order.

### 1. Videos

- [What is RAG](https://lnkd.in/gYVF6CfT) — the concept in plain terms
- [How to use RAG](https://lnkd.in/g-953k9V) — the practical version
- [RAG from Scratch](https://lnkd.in/gibgTsz5) — build it yourself, no framework
- [CMU Advanced NLP: RAG](https://lnkd.in/gFXF6DZV) — the academic treatment
- [Stanford Transformers V3: RAG](https://lnkd.in/gnvPbU7X) — retrieval in the transformer context

### 2. Papers

| Paper | Why it matters |
|---|---|
| [Retrieval-Augmented Generation (Lewis et al.)](https://arxiv.org/abs/2005.11401) | The original RAG paper |
| [RAG for LLMs: A Survey](https://arxiv.org/abs/2312.10997) | The map of the whole landscape |
| [Self-RAG](https://arxiv.org/abs/2310.11511) | Models that decide when to retrieve |
| [Corrective RAG](https://arxiv.org/abs/2401.15884) | Recovering when retrieval returns junk |

### 3. Repositories

- [RAG Techniques](https://github.com/NirDiamant/RAG_Techniques) — implementations of every major variant
- [Awesome RAG](https://lnkd.in/g4ppP4-H) — curated collection
- [Awesome RAG (alternate)](https://lnkd.in/g3meT_ns) — a second, differently-scoped list

### 4. Courses

- [DeepLearning.AI: RAG](https://lnkd.in/gKCUaN7G) · [alternate link](https://lnkd.in/gy7HjASS)
- [Building and Evaluating RAG Apps](https://lnkd.in/g2qC9-mh)
- [RAG with LangChain](https://lnkd.in/gEhQJ3RC)

### 5. Keep up

- [Need the basics first?](https://lnkd.in/giV_N6KU) — start here and come back
- For weekly coverage of AI engineering and research, see
  [Newsletters](#newsletters--communities) — *Gradient Ascent* is the closest fit

---

## MLOps & production

Getting a model out of a notebook and keeping it working.

### Core practices

| Topic | Resource |
|---|---|
| CI/CD | [Continuous Integration & Deployment](https://lnkd.in/dNdq9FSn) — automated testing and release |
| Model versioning | [Model Versioning & Registry](https://lnkd.in/d-QU637Z) — managing versions and artefacts |
| Experiment tracking | [MLflow / Weights & Biases](https://lnkd.in/deFrPyHU) — track runs and hyperparameters |
| Data versioning | [DVC](https://lnkd.in/d5VQazN9) — version control for datasets |
| Monitoring | [Monitoring & Drift Detection](https://lnkd.in/dYwu-q2m) — catch degradation early |

### Building blocks

| Topic | Resource |
|---|---|
| Data pipelines | [ETL / ELT](https://lnkd.in/dhnTfFHP) |
| Feature stores | [Feast / Tecton](https://lnkd.in/dHJJ36a4) |
| Packaging | [Docker / ONNX](https://lnkd.in/dxGvWJ4w) |
| Deployment | [Batch / real-time / edge](https://lnkd.in/du7ej8p2) |
| Orchestration | [Airflow / Prefect / Kubeflow](https://lnkd.in/dDCrHszG) |
| Observability | [Prometheus / Grafana](https://lnkd.in/dYw_QQtA) |

### System design patterns

- [Batch vs online inference](https://lnkd.in/dkE4RZ23) — choosing the right pattern
- [Shadow / canary / blue-green deployments](https://lnkd.in/dZedEeWm) — shipping without breaking things
- [Retraining & continuous learning](https://lnkd.in/dEKNbTT7) — keeping models current
- [Feedback loops & drift correction](https://lnkd.in/drRXMTAd) — handling degradation

---

## CUDA & GPU programming

For when the bottleneck is the hardware and you want to write the kernel yourself.

**The book**

- **[Programming Massively Parallel Processors](https://lnkd.in/gCxbusAH)** — Kirk & Hwu.
  The standard text. Start and mostly finish here.

**Videos**

- [CUDA Crash Course](https://lnkd.in/g4u_nE9h) — NotesByNick. Real kernels, real performance
- [NVIDIA GTC on-demand](https://lnkd.in/gvaGYySz) — filter to *intermediate* to skip the sales talks

**Practice**

- [LeetGPU](https://leetgpu.com/) — kernel challenges in the browser, no GPU needed
- [GPU programming exercises](https://lnkd.in/gGRgvm7G) — where a lot of engineers start
- [Progressive CUDA exercises](https://lnkd.in/ge2TtC-i) — graduated difficulty, not toy problems

---

## Computer vision, NLP & reinforcement learning

### Computer vision

- **[OpenCV](https://opencv.org/)** — the classical CV library, still essential
- **[PyImageSearch](https://www.pyimagesearch.com/)** — practical tutorials with working code
- Papers: [ResNet](https://arxiv.org/abs/1512.03385) · [Vision Transformer](https://arxiv.org/abs/2010.11929)

### Natural language processing

- **[spaCy](https://spacy.io/)** — industrial-strength NLP pipelines
- **[NLTK](https://www.nltk.org/)** — the classic teaching toolkit
- **[Hugging Face Transformers](https://huggingface.co/docs/transformers)** — the modern default for anything pretrained
- Book: [Speech and Language Processing](https://web.stanford.edu/~jurafsky/slp3/) (free)

### Reinforcement learning

- **[Reinforcement Learning: An Introduction](http://incompleteideas.net/book/the-book-2nd.html)** — Sutton & Barto, free. The textbook
- **[Spinning Up in Deep RL](https://spinningup.openai.com/)** — OpenAI's practical companion to the theory
- **[Gymnasium](https://gymnasium.farama.org/)** — the maintained successor to OpenAI Gym
- **[Stable-Baselines3](https://stable-baselines3.readthedocs.io/)** — reliable implementations of standard algorithms
- Papers: [DQN](https://arxiv.org/abs/1312.5602) · [PPO](https://arxiv.org/abs/1707.06347)
- In this repo: [`reference/reinforcement-learning-notes.pdf`](reference/reinforcement-learning-notes.pdf)

---

## Tools & libraries

### Environments

| Tool | Use it for |
|---|---|
| [Google Colab](https://colab.research.google.com/) | Free notebooks with GPU access — no install needed |
| [Jupyter](https://jupyter.org/) | The local notebook standard |
| [VS Code](https://code.visualstudio.com/) | Editing, debugging, notebooks in one place |

### Frameworks

| Tool | Use it for |
|---|---|
| [PyTorch](https://pytorch.org/) | Research and most new work. The default in this repo |
| [TensorFlow](https://www.tensorflow.org/) | Production pipelines and mobile/edge deployment |
| [Keras](https://keras.io/) | High-level model building on top of either |
| [scikit-learn](https://scikit-learn.org/) | Everything that isn't a neural network |

### Data

| Tool | Use it for |
|---|---|
| [pandas](https://pandas.pydata.org/) | Tabular data manipulation |
| [NumPy](https://numpy.org/) | Numerical computing, the layer under everything |
| [Matplotlib](https://matplotlib.org/) | Plotting |
| [Seaborn](https://seaborn.pydata.org/) | Statistical plots with sane defaults |

### Experiment tracking & deployment

| Tool | Use it for |
|---|---|
| [Weights & Biases](https://wandb.ai/) | Experiment tracking and comparison |
| [MLflow](https://mlflow.org/) | Open-source lifecycle management |
| [DVC](https://dvc.org/) | Version control for data and models |
| [Hugging Face Hub](https://huggingface.co/) | Sharing and hosting models |
| [Docker](https://www.docker.com/) | Reproducible environments |
| [Replicate](https://replicate.com/) | Deploying a model without managing infrastructure |

### Cloud platforms

- [Google Cloud AI](https://cloud.google.com/products/ai) · [AWS Machine Learning](https://aws.amazon.com/machine-learning/) · [Azure Machine Learning](https://azure.microsoft.com/en-us/services/machine-learning/)

---

## Datasets

| Source | Best for |
|---|---|
| [Kaggle Datasets](https://www.kaggle.com/datasets) | Breadth, plus notebooks showing what others did with them |
| [Hugging Face Datasets](https://huggingface.co/datasets) | NLP, vision and multimodal, loadable in one line |
| [UCI ML Repository](https://archive.ics.uci.edu/) | The classic small benchmarks |
| [OpenML](https://www.openml.org/) | Datasets with published results to compare against |
| [Google Dataset Search](https://datasetsearch.research.google.com/) | Finding data that isn't on the usual platforms |
| [Papers with Code Datasets](https://paperswithcode.com/datasets) | Whatever a specific paper benchmarked on |

In this repo: [`data/iris.csv`](data/iris.csv) — see [`data/README.md`](data/README.md).

---

## Practice platforms

| Platform | What you get |
|---|---|
| [Kaggle](https://www.kaggle.com/) | Competitions, datasets, notebooks, free GPUs |
| [DrivenData](https://www.drivendata.org/) | Data science competitions for social-good problems |
| [HackerRank AI Track](https://www.hackerrank.com/domains/ai) | ML-specific coding challenges |
| [LeetCode](https://leetcode.com/) | The algorithm practice interviews still test |

---

## Newsletters & communities

### Newsletters

| Newsletter | Focus |
|---|---|
| [Gradient Ascent](https://lnkd.in/gZbZAeQW) | Weekly AI/ML news and analysis |
| [DecodingML](https://lnkd.in/gpZPgk7J) | Deep technical ML content, by Paul |
| [Deep (Learning) Focus](https://lnkd.in/gTUNcUVE) | Research trends, by Cameron |
| [NeoSage](https://blog.neosage.io/) | AI insights and analysis, by Shivani |
| [Jam with AI](https://lnkd.in/gQXJzuV8) | Practical applications, by Shirin and Shantanu |
| [Data Hustle](https://lnkd.in/gZpdTTYD) | Data science careers and learning, by Sai |

### Communities

| Community | Best for |
|---|---|
| [r/MachineLearning](https://www.reddit.com/r/MachineLearning/) | Research discussion and paper threads |
| [Hugging Face Forums](https://discuss.huggingface.co/) | Transformers, datasets, practical troubleshooting |
| [Kaggle Discussions](https://www.kaggle.com/discussions) | Competition tactics and what actually works |
| [AI Stack Exchange](https://ai.stackexchange.com/) | Specific technical questions with citable answers |

---

## Contributing

Contributions from society members and the wider community are welcome — new notebooks, clearer
explanations, fixed links, or resources worth adding.

Read [CONTRIBUTING.md](CONTRIBUTING.md) for file naming, notebook conventions, and how to submit a
resource. In short: fork, branch, commit, open a pull request.

Found a broken link? [Open an issue](https://github.com/AkCodes23/MOSS-AI/issues).

## Contact

**Akhil Varanasi** — Head of AI, Manipal Open Source Society
Email: [akhilvaranasi23@gmail.com](mailto:akhilvaranasi23@gmail.com)
GitHub: [@AkCodes23](https://github.com/AkCodes23)

## License

Released under the [MIT License](LICENSE). External resources linked from this repository remain
the property of their respective authors.

---

*Happy learning and building.*
