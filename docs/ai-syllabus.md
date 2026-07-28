# AI Syllabus

Every topic worth knowing, from linear algebra to research methodology. Use it as a **checklist**,
not a reading order — the [roadmap](../README.md#learning-roadmap) tells you what order to meet
these in.

Tick things off honestly. "I've heard of it" and "I could implement it" are different states.

[← Back to docs](README.md) · [← Back to the README](../README.md)

---

## Contents

[1. Mathematics & foundations](#1-mathematics--foundations) ·
[2. Classical machine learning](#2-classical-machine-learning) ·
[3. Deep learning](#3-deep-learning-foundations) ·
[4. Computer vision](#4-computer-vision) ·
[5. Natural language processing](#5-natural-language-processing) ·
[6. Reinforcement learning](#6-reinforcement-learning) ·
[7. Generative AI](#7-generative-ai) ·
[8. Research methodology](#8-research-methodology)

---

## 1. Mathematics & foundations

*Roadmap stage 2. Companion: [Mathematics for Machine Learning](https://mml-book.github.io) (free).*

### Linear algebra

- [ ] Scalars, vectors, matrices, tensors
- [ ] Matrix operations — transpose, inverse, trace, determinant
- [ ] Dot product, cross product, Hadamard product
- [ ] Eigenvalues and eigenvectors (spectral theory)
- [ ] Singular Value Decomposition (SVD)

### Calculus

- [ ] Derivatives and gradients
- [ ] Partial derivatives and Jacobians
- [ ] The chain rule — *the foundation of backpropagation*
- [ ] Hessian matrices and second-order optimisation

### Probability & statistics

- [ ] Random variables — discrete vs. continuous
- [ ] Distributions — Gaussian, Bernoulli, Binomial, Poisson
- [ ] Bayes' theorem — prior, likelihood, posterior
- [ ] Expectation, variance, covariance
- [ ] Maximum Likelihood Estimation (MLE) vs. Maximum A Posteriori (MAP)

### Information theory

- [ ] Shannon entropy
- [ ] Cross-entropy loss — *the loss function you'll use most often*
- [ ] Kullback–Leibler (KL) divergence

---

## 2. Classical machine learning

*Roadmap stage 5. Companions: [`knn-iris.ipynb`](../notebooks/knn-iris.ipynb),
[`random-forests.ipynb`](../notebooks/random-forests.ipynb),
[`gradient-boosting.ipynb`](../notebooks/gradient-boosting.ipynb).*

### Supervised learning

- [ ] Linear regression (ordinary least squares)
- [ ] Logistic regression and the sigmoid
- [ ] Support Vector Machines and kernels
- [ ] Decision trees and pruning
- [ ] K-Nearest Neighbours — *[notebook](../notebooks/knn-iris.ipynb)*
- [ ] Naive Bayes classifiers

### Ensemble methods

- [ ] Bagging — Random Forests — *[notebook](../notebooks/random-forests.ipynb)*
- [ ] Boosting — AdaBoost, XGBoost, LightGBM, CatBoost — *[notebook](../notebooks/gradient-boosting.ipynb)*

### Unsupervised learning

- [ ] Clustering — K-Means, DBSCAN, hierarchical
- [ ] Dimensionality reduction — PCA, t-SNE, UMAP

### Optimisation

- [ ] Gradient descent — batch, stochastic (SGD), mini-batch
- [ ] Loss functions — MSE, MAE, Huber, binary cross-entropy

---

## 3. Deep learning foundations

*Roadmap stage 6. Companion: [`perceptron.ipynb`](../notebooks/perceptron.ipynb).*

### Core architectures

- [ ] Perceptron and Multi-Layer Perceptron (MLP) — *[notebook](../notebooks/perceptron.ipynb)*
- [ ] Activation functions — ReLU, Leaky ReLU, Sigmoid, Tanh, Softmax, GELU, Swish

### Training dynamics

- [ ] Backpropagation
- [ ] Weight initialisation — Xavier/Glorot, He
- [ ] Optimisers — SGD with momentum, RMSProp, [Adam](https://arxiv.org/abs/1412.6980), AdamW
- [ ] Learning rate schedules — cosine annealing, step decay

### Regularisation

- [ ] L1 and L2 regularisation (weight decay)
- [ ] [Dropout](https://jmlr.org/papers/v15/srivastava14a.html)
- [ ] [Batch normalisation](https://arxiv.org/abs/1502.03167) vs. layer normalisation
- [ ] Early stopping

---

## 4. Computer vision

### Foundations

- [ ] Convolutions — kernels, stride, padding
- [ ] Pooling — max, average, global average

### Architectures, in historical order

- [ ] LeNet-5, AlexNet, VGG-16
- [ ] [ResNet](https://arxiv.org/abs/1512.03385) — residual connections
- [ ] Inception (GoogLeNet)
- [ ] MobileNet — depthwise separable convolutions

### Advanced tasks

- [ ] Object detection — YOLO, SSD, Faster R-CNN
- [ ] Segmentation — U-Net, Mask R-CNN
- [ ] [Vision Transformers (ViT)](https://arxiv.org/abs/2010.11929)

---

## 5. Natural language processing

*Companions: [`code/transformers/`](../code/transformers/),
[Speech and Language Processing](https://web.stanford.edu/~jurafsky/slp3/) (free).*

### Text representation

- [ ] Tokenisation — BPE, WordPiece, SentencePiece
- [ ] Embeddings — one-hot, TF-IDF, [Word2Vec](https://arxiv.org/abs/1301.3781) (skip-gram, CBOW), GloVe

### Sequence models

- [ ] Recurrent Neural Networks (RNNs)
- [ ] LSTMs and GRUs
- [ ] Seq2Seq encoder-decoder models

### The transformer

*Everything below is implemented in [`code/transformers/`](../code/transformers/) — read the code
alongside this list.*

- [ ] Attention — scaled dot-product
- [ ] Self-attention and multi-head attention
- [ ] Positional encodings — sinusoidal vs. learnable
- [ ] LayerNorm and residual connections
- [ ] [BERT](https://arxiv.org/abs/1810.04805) — encoder-only, masked LM
- [ ] [GPT](https://arxiv.org/abs/2005.14165) — decoder-only, causal LM
- [ ] T5 — encoder-decoder

---

## 6. Reinforcement learning

*Companions: [Sutton & Barto](http://incompleteideas.net/book/the-book-2nd.html) (free),
[`reference/reinforcement-learning-notes.pdf`](../reference/reinforcement-learning-notes.pdf).*

### Basics

- [ ] Markov Decision Process — state, action, reward, policy
- [ ] Exploration vs. exploitation, epsilon-greedy
- [ ] Discount factor (gamma)

### Algorithms

- [ ] Value-based — Q-learning, [Deep Q-Networks](https://arxiv.org/abs/1312.5602)
- [ ] Policy-based — REINFORCE, policy gradients
- [ ] Actor-critic — A2C, A3C
- [ ] Advanced — [PPO](https://arxiv.org/abs/1707.06347), TRPO
- [ ] Reward modelling and [RLHF](https://arxiv.org/abs/2203.02155)

---

## 7. Generative AI

### Generative models

- [ ] Autoencoders and Variational Autoencoders (VAEs)
- [ ] [Generative Adversarial Networks](https://arxiv.org/abs/1406.2661) — generator vs. discriminator

### Diffusion models

- [ ] Forward process — adding noise
- [ ] Reverse process — [denoising](https://arxiv.org/abs/2006.11239)
- [ ] The U-Net backbone
- [ ] Latent diffusion (Stable Diffusion)

### Large language models

- [ ] Pre-training vs. fine-tuning
- [ ] Instruction tuning — Alpaca, Vicuna
- [ ] Parameter-efficient fine-tuning — [LoRA](https://arxiv.org/abs/2106.09685), QLoRA
- [ ] [Retrieval-Augmented Generation](https://arxiv.org/abs/2005.11401) — *[full path](../README.md#rag--retrieval-augmented-generation)*
- [ ] Vector databases — ChromaDB, Pinecone, FAISS

---

## 8. Research methodology

The section juniors skip and later wish they hadn't. Knowing algorithms makes you useful; knowing
how to run an experiment makes you a researcher.

### Tools

- [ ] [PyTorch](https://pytorch.org/) — the research standard
- [ ] [Hugging Face](https://huggingface.co/) — Transformers, Datasets, Accelerate
- [ ] [Weights & Biases](https://wandb.ai/) — experiment tracking
- [ ] LaTeX / [Overleaf](https://www.overleaf.com/) — writing papers

### Skills

- [ ] Reading arXiv papers efficiently — abstract, figures, conclusion, *then* the method
- [ ] Ablation studies — remove one part at a time to find out what actually mattered
- [ ] Reproducibility — fix random seeds, pin versions, log configurations
- [ ] Benchmarking and metrics — precision, recall, F1, AUC-ROC, BLEU, ROUGE, perplexity

---

## What next

- Follow the [roadmap](../README.md#learning-roadmap) for a schedule
- Run the [notebooks](../notebooks/) as you reach each topic
- Read the [landmark papers](../README.md#research-papers) for anything you want beyond a
  working understanding
