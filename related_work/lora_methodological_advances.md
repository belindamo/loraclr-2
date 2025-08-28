# LoRA Methodological Advances

## 1. QR-LoRA: Efficient and Disentangled Fine-tuning via QR Decomposition

**Authors:** Various (2025)
**URL:** https://arxiv.org/abs/2507.04599

### Problem/Assumption
Standard LoRA methods lead to unstructured weight matrix modifications causing feature entanglement between content and style attributes.

### Insight/Contribution
- Leverages QR decomposition for structured parameter updates
- Orthogonal Q matrix minimizes interference between visual features
- Upper triangular R matrix efficiently encodes attribute-specific transformations

### Impact
Reduces trainable parameters to half of conventional LoRA while supporting effective merging without cross-contamination.

---

## 2. T-LoRA: Timestep-Dependent Low-Rank Adaptation

**Authors:** Various (2025)
**URL:** https://arxiv.org/abs/2507.05964

### Problem/Assumption
Higher diffusion timesteps are more prone to overfitting than lower ones, necessitating timestep-sensitive fine-tuning.

### Insight/Contribution
- Dynamic fine-tuning strategy that adjusts rank-constrained updates based on diffusion timesteps
- Weight parametrization ensuring independence between adapter components
- Orthogonal initialization for better performance

### Impact
Superior balance between concept fidelity and text alignment in single-image customization scenarios.

---

## 3. RiemannLoRA: Unified Riemannian Framework for Ambiguity-Free LoRA Optimization

**Authors:** Vladimir Bogachev et al. (2025)
**URL:** https://arxiv.org/abs/2507.12142

### Problem/Assumption
LoRA faces challenges in optimal initialization and overparametrization in low-rank matrix factorization.

### Insight/Contribution
- Treats fixed-rank LoRA matrices as a smooth manifold
- Removes overparametrization while determining optimal initialization direction
- Numerically stable implementation using Riemannian optimization

### Impact
Consistently improves convergence speed and final performance over standard LoRA across LLM and diffusion architectures.

---

## 4. LoFT: Low-Rank Adaptation That Behaves Like Full Fine-Tuning

**Authors:** Nurbek Tastan et al. (2025)
**URL:** https://arxiv.org/abs/2505.21289

### Problem/Assumption
LoRA underperforms full fine-tuning in accuracy and converges more slowly due to misaligned optimizer dynamics.

### Insight/Contribution
- Aligns optimizer's internal dynamics with full-model updates
- Projects optimizer's first and second moments into the same low-rank subspace
- Eliminates need for tuning LoRA scaling factor α

### Impact
Narrows performance gap between adapter-based tuning and full fine-tuning without increasing inference cost.

---

## 5. ARD-LoRA: Dynamic Rank Allocation for Parameter-Efficient Fine-Tuning

**Authors:** Haseeb Ullah Khan Shinwari, Muhammad Usama (2025)
**URL:** https://arxiv.org/abs/2506.18267

### Problem/Assumption
Conventional LoRA employs fixed rank, imposing uniform adaptation despite heterogeneous learning dynamics across layers.

### Insight/Contribution
- Automates rank allocation through learnable scaling factors
- Balances task performance and parameter efficiency
- Incorporates L1 sparsity and Total Variation regularization

### Impact
Achieves 99.3% of full fine-tuning performance with only 0.32% trainable parameters, reducing multimodal adaptation memory by 41%.

---

## 6. Block-wise LoRA: Fine-grained LoRA for Effective Personalization

**Authors:** Various (2024)
**URL:** https://arxiv.org/abs/2403.07500

### Problem/Assumption
Existing efficient fine-tuning methods struggle to achieve effective personalization and stylization in T2I generation.

### Insight/Contribution
- Performs fine-grained fine-tuning for different blocks of Stable Diffusion
- Generates images faithful to input prompts and target identity with desired style
- Block-specific adaptation for better control

### Impact
Demonstrates effectiveness in personalization tasks requiring precise control over different aspects of generation.

---

## 7. TimeStep Master: Asymmetrical Mixture of Timestep LoRA Experts

**Authors:** Various (2025)
**URL:** https://arxiv.org/abs/2503.07416

### Problem/Assumption
Same LoRA used for different timesteps limits capabilities since different timesteps require different noise level modeling.

### Insight/Contribution
- Different LoRAs for different timestep intervals (TimeStep LoRA experts)
- Asymmetrical mixture via core-context collaboration at multi-scale intervals
- Time-dependent gating for context experts

### Impact
Achieves state-of-the-art results across domain adaptation, post-pretraining, and model distillation tasks.

---

## 8. MoSLoRA: Mixture-of-Subspaces in Low-Rank Adaptation

**Authors:** Various (2024)
**URL:** https://arxiv.org/abs/2406.11909

### Problem/Assumption
Standard LoRA weights can be decomposed into subspaces, and mixing them can enhance performance.

### Insight/Contribution
- Equivalently decomposes LoRA weights into two subspaces
- Jointly learns mixer with original LoRA weights
- Flexible subspace fusion approach

### Impact
Consistently outperforms LoRA across commonsense reasoning, visual instruction tuning, and text-to-image generation tasks.