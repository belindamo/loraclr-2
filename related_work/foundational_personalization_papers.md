# Foundational Personalization Papers

## 1. DreamBooth: Fine Tuning Text-to-Image Diffusion Models for Subject-Driven Generation (CVPR 2023)

**Authors:** Nataniel Ruiz, Yuanzhen Li, Varun Jampani, Yael Pritch, Michael Rubinstein, Kfir Aberman
**Venue:** CVPR 2023 (Award Candidate)
**URL:** https://arxiv.org/abs/2208.12242

### Problem Addressed
Large text-to-image models lack the ability to mimic specific subjects from reference images and synthesize them in different contexts.

### Core Assumptions Made
- Pre-trained models have strong semantic priors that can be leveraged
- Few images (3-5) are sufficient to learn subject binding
- Class-specific prior preservation prevents overfitting

### Novel Contribution/Insight
- Binds unique identifier with specific subject through fine-tuning
- Introduces autogenous class-specific prior preservation loss
- Enables subject synthesis in diverse scenes not in reference images

### Technical Approach
- Fine-tunes entire pre-trained text-to-image model
- Uses unique identifier token for subject
- Prior preservation loss maintains model's general knowledge

### Evaluation Method
- New dataset and evaluation protocol for subject-driven generation
- Qualitative assessment across multiple tasks
- Comparison with existing personalization approaches

### Impact/Significance
Seminal work that established the field of subject-driven image generation and inspired numerous follow-up works.

---

## 2. An Image is Worth One Word: Personalizing Text-to-Image Generation using Textual Inversion (ICLR 2023)

**Authors:** Rinon Gal, Yuval Alaluf, Yuval Atzmon, Or Patashnik, Amit H. Bermano, Gal Chechik, Daniel Cohen-Or
**URL:** https://arxiv.org/abs/2208.01618

### Problem Addressed
How to represent specific unique concepts through language-guided models for creative personalization.

### Core Assumptions Made
- Frozen text-to-image models can learn new concepts in embedding space
- Single word embedding is sufficient for capturing varied concepts
- 3-5 images provide adequate supervision

### Novel Contribution/Insight
- Learns new "words" in embedding space of frozen model
- Represents concepts through pseudo-word tokens
- Compositional approach using natural language

### Technical Approach
- Optimizes embedding vectors while keeping model frozen
- Uses reconstruction loss on provided images
- Integrates learned embeddings into text prompts

### Evaluation Method
- Comparison across range of applications and tasks
- Assessment of concept fidelity and composition ability
- Baseline comparisons with existing approaches

### Impact/Significance
Established textual inversion as fundamental technique for parameter-efficient personalization.

---

## 3. HyperDreamBooth: HyperNetworks for Fast Personalization (CVPR 2024)

**Authors:** Nataniel Ruiz et al.
**URL:** https://openaccess.thecvf.com/content/CVPR2024/papers/Ruiz_HyperDreamBooth_HyperNetworks_for_Fast_Personalization_of_Text-to-Image_Models_CVPR_2024_paper.pdf

### Problem Addressed
DreamBooth requires considerable GPU time and storage for each personalized model.

### Core Assumptions Made
- HyperNetworks can predict personalized weights from single image
- Fast fine-tuning can refine initial predictions
- Weight prediction is more efficient than full fine-tuning

### Novel Contribution/Insight
- Uses HyperNetwork to generate subset of personalized weights
- 25x faster than DreamBooth, 125x faster than Textual Inversion
- Produces 10,000x smaller models than DreamBooth

### Technical Approach
- HyperNetwork predicts initial weights from single image
- Fast fine-tuning refines predictions for high fidelity
- Composed weights integrate into diffusion model

### Impact/Significance
Addresses scalability challenges of personalization, enabling practical deployment scenarios.

---

## 4. AttnDreamBooth: Towards Text-Aligned Personalized Text-to-Image Generation

**Authors:** Various (2024)
**URL:** https://arxiv.org/abs/2406.05000

### Problem Addressed
Textual Inversion tends to overfit concepts while DreamBooth often overlooks them due to incorrect embedding alignment.

### Core Assumptions Made
- Embedding alignment, attention maps, and subject identity can be learned separately
- Cross-attention regularization enhances attention map learning
- Staged training improves both identity preservation and text alignment

### Novel Contribution/Insight
- Separate learning of embedding alignment, attention maps, and subject identity
- Cross-attention map regularization term
- Multi-stage training strategy

### Impact/Significance
Demonstrates significant improvements in identity preservation and text alignment compared to baseline methods.