# Wildfire Prediction using KAN-CNN

This repository contains the implementation of the hybrid **Kolmogorov-Arnold Network (KAN)** and **Convolutional Neural Network (CNN)** model proposed in our research paper titled "*Wildfire Prediction using Convolutional Kolmogorov-Arnold Network*," accepted at ICECE 2024 ([13th International Conference on Electrical and Computer Engineering (ICECE)](https://icece.buet.ac.bd)).

The KAN-CNN model integrates the parameter efficiency of KAN with the spatial feature extraction capability of CNN, achieving high accuracy with significantly fewer parameters. This model is designed to enable **real-time wildfire detection** from satellite imagery with **minimal computational overhead**.

---

## Overview

### Problem Statement
Wildfires pose a significant environmental challenge, causing ecological damage and threats to human life. Early and accurate detection of wildfires is crucial to mitigate these impacts. Existing models often struggle with balancing accuracy and computational efficiency for real-time applications.

### Proposed Solution
Our model combines:
- The **Kolmogorov-Arnold Network (KAN)** for learnable nonlinear activation functions and parameter efficiency.
- A traditional **Convolutional Neural Network (CNN)** for hierarchical spatial feature extraction.
  
### Key Features
- **High Accuracy**: Achieves a test accuracy of **97.32%**.
- **Efficiency**: Uses only **6,336 parameters**, significantly fewer than conventional CNN architectures.
- **Real-Time Suitability**: Faster convergence and lower computational cost make it ideal for large-scale deployment.

---

## Dataset

The dataset used for training and testing is sourced from the **Forest Fires - Open Government Portal** ([Dataset Link](https://www.kaggle.com/datasets/abdelghaniaaba/wildfire-prediction-dataset)). It contains satellite images labeled as:
- **Wildfire**: 22,710 images
- **No Wildfire**: 20,140 images

### Data Splits
- **Training**: 70%
- **Validation**: 15%
- **Testing**: 15%


## Model Architecture

The KAN-CNN architecture includes:
1. **Convolutional Layers**: Extract spatial features from satellite images.
2. **KAN Layers**: Learnable nonlinear activation functions to improve representation with fewer parameters.
3. **Fully Connected Layers**: Perform final classification.

**Key Model Statistics**:
- Total Parameters: **6,336**
- Optimizer: **AdamW**
- Learning Rate: **0.0001**
- Batch Size: **256**
- Epochs: **20**

The detailed architecture and layer-wise parameter breakdown are available in the paper.

## Citation

If you use this code or find our work helpful, please cite our paper:

@inproceedings{kan_cnn_wildfire_2024,
  title={Wildfire Prediction using Convolutional Kolmogorov-Arnold Network},
  author={Rabbi, Rawhatur and Datta, Joy and Ahmed, Shuvro and Zereen, Aniqua Nusrat},
  booktitle={Proceedings of the 13th International Conference on Electrical and Computer Engineering (ICECE)},
  year={2024},
}
