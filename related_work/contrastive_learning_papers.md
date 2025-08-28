# Contrastive Learning in Generative Models

## 1. CONFORM: Contrast is All You Need For High-Fidelity Text-to-Image Diffusion Models (CVPR 2024)

**Authors:** Tuna Han Salih Meral, Enis Simsar, Federico Tombari, Pınar Yanardağ
**Venue:** CVPR 2024
**URL:** https://arxiv.org/html/2312.06059v1

### Problem Addressed
Text-to-image diffusion models might not faithfully represent semantic intent, overlooking or failing to produce certain objects in complex prompts.

### Core Assumptions Made
- Attention maps can be optimized using contrastive objectives
- Segregation of objects in attention maps improves generation
- Related attributes should be kept close while objects are separated

### Novel Contribution/Insight
- Training-free method combining contrastive objective with test-time optimization
- Promotes segregation of objects while maintaining attribute relationships
- Works with both latent and pixel-based diffusion models

### Technical Approach
- Contrastive learning applied to attention maps
- Test-time optimization without model modification
- Object segregation with attribute preservation

### Impact/Significance
Demonstrates versatility across Stable Diffusion and Imagen, showing effectiveness for multi-concept generation.

---

## 2. TULIP: Towards Unified Language-Image Pretraining

**Authors:** Various (2025)
**URL:** https://arxiv.org/html/2503.15485v1

### Problem Addressed
CLIP-like models struggle with vision-centric tasks requiring high-fidelity image understanding due to prioritizing semantics over visual details.

### Core Assumptions Made
- Language alignment weakens detailed visual understanding
- Generative data augmentation can improve visual features
- Image-image and text-text contrastive learning enhances representation

### Novel Contribution/Insight
- Combines generative data augmentation with enhanced contrastive learning
- Image/text reconstruction regularization for fine-grained features
- Maintains semantic alignment while improving visual understanding

### Impact/Significance
Establishes new SOTA on ImageNet-1K, 2x improvement on RxRx1, 3x higher scores than SigLIP on MMVP.

---

## 3. CoDE: Contrastive Deepfake Embeddings

**Authors:** Lorenzo Baraldi et al. (ECCV 2024)
**URL:** https://arxiv.org/abs/2407.20337

### Problem Addressed
CLIP embedding space is optimized for global alignment, not deepfake detection, neglecting local features and tailored training benefits.

### Core Assumptions Made
- Specialized embedding space needed for deepfake detection
- Global-local similarities enhance contrastive training
- Contrastive learning can distinguish between real and generated content

### Novel Contribution/Insight
- Novel embedding space specifically for deepfake detection
- Contrastive learning with global-local similarity enforcement
- Comprehensive dataset with 9.2M images from diffusion models

### Impact/Significance
Achieves SOTA accuracy on collected dataset with excellent generalization to unseen generators.

---

## 4. Dispersive Loss: Representation Regularization for Diffusion Models

**Authors:** Runqian Wang, Kaiming He (2024)
**URL:** https://arxiv.org/html/2506.09027v2

### Problem Addressed
Diffusion models rely on regression objectives without explicit regularization on learned representations.

### Core Assumptions Made
- Internal representations should disperse in hidden space
- Contrastive-like objectives can improve generative modeling
- No positive sample pairs needed for effective regularization

### Novel Contribution/Insight
- Plug-and-play regularizer encouraging representation dispersion
- Analogous to contrastive self-supervised learning without pairs
- Bridges gap between generative modeling and representation learning

### Impact/Significance
Consistent improvements on ImageNet across range of diffusion models, demonstrating generalizability.

---

## 5. Hierarchical Text-Conditional Image Generation with CLIP Latents (DALL-E 2)

**Authors:** Aditya Ramesh et al. (OpenAI, 2022)
**URL:** https://arxiv.org/abs/2204.06125

### Problem Addressed
How to leverage CLIP's robust representations for improved image generation with text conditioning.

### Core Assumptions Made
- CLIP embeddings capture both semantics and style effectively
- Two-stage generation (prior + decoder) improves diversity
- Image representations enable better control than direct text conditioning

### Novel Contribution/Insight
- Prior generates CLIP image embedding from text
- Decoder generates image conditioned on image embedding
- Enables language-guided manipulation in zero-shot fashion

### Impact/Significance
Established hierarchical generation paradigm using contrastive representations, influencing subsequent text-to-image architectures.

---

## 6. Contrastive Learning Guided Latent Diffusion Model for Image-to-Image Translation

**Authors:** Various (2025)
**URL:** https://arxiv.org/abs/2503.20484

### Problem Addressed
Preserving reference image content while enabling desired modifications in specific regions during image-to-image translation.

### Core Assumptions Made
- Patch-wise contrastive loss can preserve content structure
- Automatic editing direction determination improves user experience
- Cross-attention guidance enhances content preservation

### Novel Contribution/Insight
- Zero-shot diffusion method with patch-wise contrastive loss
- Automatic editing direction determination in text embedding space
- Cross-attention guiding loss for structural preservation

### Impact/Significance
Demonstrates superior performance in image-to-image translation with enhanced fidelity and controllability.