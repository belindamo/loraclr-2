# Core LoRACLR Papers

## 1. LoRACLR: Contrastive Adaptation for Customization of Diffusion Models (CVPR 2025)

**Authors:** Enis Simsar, Thomas Hofmann, Federico Tombari, Pinar Yanardag
**Venue:** CVPR 2025
**URL:** https://arxiv.org/abs/2412.09622

### Problem Addressed
Multi-concept image generation by merging multiple LoRA models while maintaining concept distinctiveness and avoiding attribute entanglement.

### Core Assumptions Made
- Individual LoRA models excel at single concepts but fail when combined
- Attention mechanisms within different LoRA models overlap, leading to concept omission or incorrect blending
- Contrastive learning can align and merge weight spaces effectively

### Novel Contribution/Insight
- Uses contrastive objective to align and merge weight spaces of multiple LoRA models
- Enforces distinct yet cohesive representations for each concept
- Training-free approach that works at test time

### Technical Approach
- Merges multiple LoRA models, each fine-tuned for distinct concepts
- Uses contrastive objective to ensure compatibility while minimizing interference
- No additional individual fine-tuning required

### Evaluation Method
- Qualitative and quantitative evaluations on multi-concept generation
- Comparison with baseline LoRA merging approaches
- Assessment of concept fidelity and attribute preservation

### Impact/Significance
Advances capabilities of personalized image generation by enabling efficient, scalable model composition for multi-concept synthesis.

---

## 2. CLoRA: Contrastive Test-Time Composition of Multiple LoRA Models (CVPR 2024)

**Authors:** Tuna Han Salih Meral, Enis Simsar, Federico Tombari, Pinar Yanardag
**Venue:** CVPR 2024
**URL:** https://arxiv.org/html/2403.19776v2

### Problem Addressed
Combining multiple LoRA models for multi-concept image generation where attention mechanisms overlap, causing concept omission or incorrect combinations.

### Core Assumptions Made
- Attention maps within different LoRA models interfere with each other
- Individual LoRA models work well for single concepts but fail in combination
- Contrastive learning can separate attention maps for distinct concepts

### Novel Contribution/Insight
- Training-free approach that updates attention maps of multiple LoRA models at test-time
- Uses attention maps to create semantic masks for fusing latent representations
- Contrastive learning to compose concept and style LoRAs simultaneously

### Technical Approach
- Revises attention maps in test-time to separate attentions associated with distinct concept LoRAs
- Creates semantic masks from attention maps for latent representation fusion
- Works with pre-trained LoRA models without additional training

### Evaluation Method
- Comprehensive qualitative and quantitative evaluations
- Comparison with existing multi-concept generation methods
- Assessment of concept preservation and text alignment

### Impact/Significance
Demonstrates superior performance in multi-concept image generation, providing a scalable solution for combining multiple LoRA adaptations.