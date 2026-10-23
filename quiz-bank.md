# Transformer Paper Quiz Bank

**Source:** "Attention Is All You Need" (Vaswani et al., 2017), arXiv:1706.03762
**Purpose:** Question bank for the graduate seminar on the Transformer. Link this from the syllabus page.

---

## Questions

1. How many identical layers are stacked in each of the encoder and decoder in the base Transformer model?
2. What is the dimension of the embeddings and all sub-layer outputs in the base model (d_model)?
3. How many parallel attention heads does the base Transformer use?
4. In the base model, what is the key/value dimension of each attention head?
5. Which optimizer was used to train the Transformer, and with what hyperparameters?
6. How many warmup steps were used in the learning-rate schedule?
7. Describe the learning-rate schedule after warmup.
8. What BLEU score did the big Transformer achieve on the WMT 2014 English-to-German task?
9. What BLEU score did the big Transformer achieve on the WMT 2014 English-to-French task?
10. What BLEU scores did the base Transformer achieve on the two WMT 2014 tasks?
11. What residual dropout rate was used for the base model?
12. For how many steps were the base models trained, and on what hardware?

---

## Answer Key (one line per fact)

1. **Stack depth:** N = 6 identical layers in each of the encoder and decoder (Section 3.1)
2. **Base model dimension:** d_model = 512 (Section 3.1 / Table 3)
3. **Attention heads:** h = 8 parallel heads (Section 3.2.2 / Table 3)
4. **Per-head dimensions:** d_k = d_v = d_model / h = 64 (Section 3.2.2)
5. **Optimizer:** Adam with beta1 = 0.9, beta2 = 0.98, epsilon = 10^-9 (Section 5.3)
6. **Warmup steps:** 4,000 (Section 5.3)
7. **LR schedule:** increases linearly for the first warmup_steps, then decreases proportionally to the inverse square root of the step number (Section 5.3)
8. **WMT 2014 EN-DE BLEU (big model):** 28.4 (Abstract / Section 6.1 / Table 2)
9. **WMT 2014 EN-FR BLEU (big model):** 41.8 (Abstract / Section 6.1 / Table 2)
10. **WMT 2014 BLEU (base model):** 27.3 EN-DE and 38.1 EN-FR (Section 6.1 / Table 2)
11. **Residual dropout:** P_drop = 0.1 (Section 5.4)
12. **Base training:** 100,000 steps, roughly 12 hours on 8 NVIDIA P100 GPUs (Section 5.2)

---

*Note: published as a repository file rather than a gist because the available GitHub token does not have gist-creation scope.*
