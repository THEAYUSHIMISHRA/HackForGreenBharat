# High-Fidelity Offroad Terrain Segmentation

An advanced, high-efficiency Semantic Segmentation pipeline leveraging the power of **Meta AI’s DINOv2** foundation model. This project achieves state-of-the-art pixel-level accuracy using self-supervised feature distillation on consumer-grade hardware.

---

## 🌟 Project Highlights
* **Backbone:** Frozen features from Meta's **DINOv2 (Vision Transformer)** for dense visual descriptors.
* **Performance:** Achieved a peak **Mean IoU of 0.7062** with stable convergence.
* **Optimization:** Optimized for **NVIDIA RTX 3050 Ti**, bringing loss down from **1.09 to 0.33**.
* **Generalization:** Robust architecture that prevents overfitting, ensuring high accuracy on unseen datasets.

---

## 📊 Performance Metrics

The model was trained for **40 epochs**. The following metrics represent the final state of the `segmentation_head.pth` model:

| Metric | Initial (Epoch 1) | Best (Epoch 34) | Final (Epoch 40) |
| :--- | :--- | :--- | :--- |
| **Training Loss** | 1.0908 | 0.3354 | **0.3347** |
| **Validation IoU** | 0.6579 | **0.7062** | 0.7058 |



---

## 🛠️ Technical Stack
* **Core Framework:** PyTorch 2.x
* **Backbone Model:** `dinov2_vits14`
* **GPU Acceleration:** CUDA on NVIDIA GeForce RTX 3050 Ti
* **Architecture:** Custom Linear/Convolutional Segmentation Head

---

## 🧠 Technical Deep-Dive
Unlike traditional supervised learning, this project utilizes **Self-Supervised Foundations**. DINOv2 provides a rich understanding of object geometry and textures without needing massive labeled data for the backbone. We engineered a custom head to map these high-dimensional features into class-specific masks, resulting in a model that understands **structural context** rather than just matching pixels.

---

## 🌟 Test Results
https://drive.google.com/file/d/1grZNTPm67QU2eLdHBzlUNYCJhoKv7I36/view?usp=sharing

---

## 🏆 Finals Visuals
https://drive.google.com/file/d/1_dU1XZWxeCZo3ea26Yut3aey3HFh1zXB/view?usp=sharing
   

   
