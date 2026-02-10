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

#### (a) Baseline (Single Shared)
*Severe ray artifacts and background noise due to feature misalignment.*
<video src="https://github.com/lynn1023-max/OMD-BEV/raw/main/assets/a_base.mp4" width="100%" controls></video>

#### (b) Single-Modal Only
*Specialized pathways begin to handle distinct feature distributions.*
<video src="assets/b_single_modal.mp4" width="100%"></video>

#### (c) Tri-modal Synergy
*The Balanced expert acts as a bridge to effectively suppress noise.*
<video src="assets/c_tri_modal.mp4" width="100%"></video>

#### (d) w/ Vision-Biased
*Enhanced semantic response but prone to spatial smearing.*
<video src="assets/d_vision_biased.mp4" width="100%"></video>

#### (e) w/ Geometric-Biased
*Sharper object boundaries by mitigating depth-induced distortions.*
<video src="assets/e_geometric_biased.mp4" width="100%"></video>

#### (f) Full CASR Bank (Ours)
*Optimal Synergy: Achieving the most balanced trade-off between precision and noise suppression.*
<video src="assets/f_full_model.mp4" width="100%"></video>

---


## 🚀 Key Features

* **Orthogonal Modality Decomposition (OMD):** Decouples shared cross-modal representations from modality-specific features to mitigate modality collapse.
* **Context-Adaptive Sparse Routing (CASR):** A dynamic MoE architecture that selects the optimal fusion path based on real-time environmental priors.
* **Geometric Context Prior (GCP):** Physically-grounded instructions that guide the routing process for robust multimodal perception.

## 🛠️ Installation & Usage

*(Coming Soon: Instructions for environment setup, data preparation, and training/evaluation scripts)*
