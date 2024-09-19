# Deepfake Image Detection Using VGG16 and Channel Attention

This project focuses on detecting deepfake images using the **140k Real and Fake Faces** dataset from Kaggle. We leverage **VGG16** with channel attention to enhance the performance of the model, improving accuracy by focusing on the most relevant feature channels. We also perform an ablation study with **ResNet50** to compare feature extraction performance.

## Dataset

The dataset consists of 140,000 images:  
- **70,000 Real Faces**: From the Flickr dataset collected by Nvidia  
- **70,000 Fake Faces**: Generated using StyleGAN by Bojan.

We utilized the given train, validation, and test sets from [Kaggle Dataset](https://www.kaggle.com/datasets/xhlulu/140k-real-and-fake-faces/data), but Images have been resized to 224px by 224px.

## Methodology

We implemented the **VGG16** deep learning model for classification, enhanced by a **channel attention mechanism** to prioritize relevant feature channels and suppress less useful ones. This attention mechanism helps the model focus on critical features, improving overall classification accuracy.

### Models Used:
1. **VGG16**: 
   - Accuracy: **99.64%**
   - **VGG16 with Channel Attention**: Accuracy improved to **99.80%**.

2. **ResNet50** (Ablation Study):
   - Accuracy: **96.65%**
   - **ResNet50 with Channel Attention**: Accuracy improved to **98.41%**.

## Results

| Model                | Accuracy  |
|----------------------|-----------|
| ResNet50             | 96.65%    |
| ResNet50 + Attention | 98.41%    |
| VGG16                | 99.64%    |
| VGG16 + Attention    | 99.80%    |

The addition of channel attention enhanced the model's performance by focusing on the most relevant features. The **VGG16 with Channel Attention** model outperformed all other configurations, achieving an accuracy of **99.80%**.
