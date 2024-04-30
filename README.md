# apai3010

## Abstract

The paper “StableRep: Synthetic Images from Text-to-Image Models Make Strong Visual Representation Learners” (abbreviated as: “The Original Paper”)  has shown that (a) synthetic training data, with proper guidance scale (w), can achieve similar accuracy performance or even outperform the real world training data. (b) StableRep, a multi-positive contrastive learning method that treat multiple images from the same text prompts as positive for each other, can achieve a better performance than the two benchmark models, SimCLR and CLIP, with the same text prompts and real images. Our research seeks to replicate these experiments to validate their results and explore the potential of synthetic images in training robust visual representation models.

Due to computational constraints, a full replication of the original study was not feasible. Instead, our research focuses on assessing the efficacy of synthetic images in training models for downstream tasks. We hypothesized that classifiers trained on synthetic images could potentially outperform those trained on real images. To test this, we conducted experiments using two types of neural network architectures: Convolutional Neural Network (CNN) and Vision Transformer (ViT). The results from both architectures indicated that models trained with real images consistently outperformed those trained with synthetic images. This suggests that while synthetic images may be advantageous for pretraining phases, real images are crucial for achieving optimal performance in downstream tasks. Our findings highlight the essential role of authentic data in the fine-tuning stages of model training.

## Data

To reproduce the results of this project, please download the CIFAKE dataset and place it into `data/`.

With kaggle installed, you may do it using the following code snippet:
```bash
cd data
kaggle datasets download -d birdy654/cifake-real-and-ai-generated-synthetic-images
unzip cifake-real-and-ai-generated-synthetic-images.zip -d cifake
```
