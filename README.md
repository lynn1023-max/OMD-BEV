# OMD-BEV: Orthogonal Modality Decomposition with Context-Adaptive Sparse Routing for Multi-Modal BEV Perception

This is the official implementation of **OMD-BEV**. Our framework addresses feature interference and modality imbalance in autonomous driving BEV semantic segmentation through orthogonal decomposition and a dynamic Mixture-of-Experts (MoE) bank.

## 🌟 Expert Bank Ablation Visualization

To investigate the rationale behind the Expert Bank design, we visualize the BEV feature activation maps across different expert compositions. These videos demonstrate how the model evolves from a noisy baseline to a precise, synergized perception system.

### Configuration Overview

| Variant | Composition | Description |
| :--- | :--- | :--- |
| **(a) Base** | Single Shared | Standard convolutional fusion suffering from severe ray artifacts and background noise. |
| **(b) Single-Modal** | V + G | Specialized pathways that handle distinct feature distributions for vision and geometry. |
| **(c) Tri-modal** | V + G + B | Inclusion of the Balanced expert as a bridge to significantly suppress scattered noise. |
| **(d) Vision-Biased** | + VB | Enhances semantic response but may introduce spatial smearing during projection. |
| **(e) Geometric-Biased** | + GB | Sharpens object boundaries and effectively mitigates depth-induced geometric distortions. |
| **(f) Full Model** | **All Experts** | Achieves the optimal trade-off between precision and noise suppression via diverse synergy. |

---

### Qualitative Demo Videos

The following demonstrations visualize the evolution of BEV feature activation maps. We recommend viewing in full screen to observe the mitigation of geometric distortions.

### Qualitative Demo Videos

The following demonstrations visualize the evolution of BEV feature activation maps. We recommend viewing in full screen to observe the mitigation of geometric distortions.

#### (a) Baseline (Single Shared)
<img src="assets/a_base.gif" style="width: 100%; max-width: 840px; height: auto;">
*Severe ray artifacts and background noise due to feature misalignment.*

#### (b) Single-Modal Only
<img src="assets/b_single_modal.gif" style="width: 100%; max-width: 840px; height: auto;">
*Specialized pathways begin to handle distinct feature distributions.*

#### (c) Tri-modal Synergy
<img src="assets/c_tri_modal.gif" style="width: 100%; max-width: 840px; height: auto;">
*The Balanced expert acts as a bridge to effectively suppress noise.*

#### (d) w/ Vision-Biased
<img src="assets/d_vision_biased.gif" style="width: 100%; max-width: 840px; height: auto;">
*Enhanced semantic response but prone to spatial smearing.*

#### (e) w/ Geometric-Biased
<img src="assets/e_geometric_biased.gif" style="width: 100%; max-width: 840px; height: auto;">
*Sharper object boundaries by mitigating depth-induced distortions.*

#### (f) Full CASR Bank (Ours)
<img src="assets/f_full_model.gif" style="width: 100%; max-width: 840px; height: auto;">
*Optimal Synergy: Achieving the most balanced trade-off between precision and noise suppression.*

---


## 🚀 Key Features

* **Orthogonal Modality Decomposition (OMD):** Decouples shared cross-modal representations from modality-specific features to mitigate modality collapse.
* **Context-Adaptive Sparse Routing (CASR):** A dynamic MoE architecture that selects the optimal fusion path based on real-time environmental priors.
* **Geometric Context Prior (GCP):** Physically-grounded instructions that guide the routing process for robust multimodal perception.

## 🛠️ Installation & Usage

*(Coming Soon: Instructions for environment setup, data preparation, and training/evaluation scripts)*
