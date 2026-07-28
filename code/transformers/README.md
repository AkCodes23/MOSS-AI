# Transformer from Scratch

A minimal GPT built from PyTorch primitives — no `nn.Transformer`, no Hugging Face. Under 200
lines total, small enough to read in one sitting and train on a laptop CPU.

[← Back to the README](../../README.md)

---

## Files

| File | What it defines |
|---|---|
| [`transformer_blocks.py`](transformer_blocks.py) | `SelfAttentionHead`, `MultiHeadAttention`, `FeedForward`, `Block` |
| [`tiny_gpt.py`](tiny_gpt.py) | `TinyGPT` — token/position embeddings, the training loop, and generation |

`tiny_gpt.py` imports from `transformer_blocks.py`, so run it from inside this directory.

---

## Running it

```bash
cd code/transformers
python tiny_gpt.py
```

Trains for 1500 steps on a ten-sentence corpus and prints generated text. Takes well under a
minute on CPU. It will report whether CUDA is available, but doesn't need it.

Expected output — loss falling, then a short generated sequence:

```
Step 0, loss=3.4...
Step 300, loss=1.8...
...
Generated text:

hello friends how are you <END> ...
```

The corpus is ten sentences, so the model memorises rather than generalises. That's the point:
you can verify it learned by reading the output.

---

## Reading order

Read `transformer_blocks.py` bottom-up — the pieces build on each other.

1. **`SelfAttentionHead`** — the whole idea in fifteen lines. Project the input into queries,
   keys and values; score every token against every other; mask out the future with a lower
   triangular matrix so position *t* can't see *t+1*; softmax the scores into weights; take the
   weighted sum of values.
2. **`MultiHeadAttention`** — run several heads in parallel and concatenate. Each head learns a
   different relationship (syntax, position, topic) rather than one head averaging them all.
3. **`FeedForward`** — a two-layer MLP applied to each position independently. Attention moves
   information between tokens; this layer does the thinking on it.
4. **`Block`** — attention plus feed-forward, each wrapped in a residual connection with
   pre-normalisation (`x + sublayer(norm(x))`). Residuals are what make depth trainable.

Then `tiny_gpt.py`:

5. **Embeddings** — token identity plus position, summed. Attention has no inherent notion of
   order, so position has to be added explicitly.
6. **`forward`** — embed, stack blocks, normalise, project to vocabulary logits, cross-entropy
   against the next token.
7. **`generate`** — crop to the last `block_size` tokens, take the final position's logits,
   softmax, sample, append, repeat.

---

## Configuration

Set at the top of `tiny_gpt.py`. Change them and watch what happens — this is the fastest way to
build intuition.

| Parameter | Default | What it controls |
|---|---|---|
| `block_size` | 6 | Context window — how far back the model can see |
| `embedding_dim` | 32 | Width of the residual stream |
| `n_heads` | 2 | Attention heads per block |
| `n_layers` | 2 | Stacked transformer blocks |
| `lr` | 1e-3 | Learning rate for AdamW |
| `epochs` | 1500 | Training steps |

---

## Where to go next

- **Read the paper:** [Attention Is All You Need](https://arxiv.org/abs/1706.03762)
- **Watch it built:** [Neural Networks: Zero to Hero](https://karpathy.ai/zero-to-hero.html) —
  this code follows the same structure
- **Go bigger:** [Build a Large Language Model (From Scratch)](https://www.manning.com/books/build-a-large-language-model-from-scratch)
- **Try changing something:** swap `ReLU` for `GELU`; add dropout; scale the corpus up to a real
  text file and switch to character-level tokenisation; increase `n_layers` and see where it
  stops helping
