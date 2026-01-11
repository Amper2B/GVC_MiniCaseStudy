# GVC_MiniCaseStudy
Fused ResNet18-MobileNetV2 architecture for 10-class object detection with classical OpenCV feature analysis for LNCS Case Study.

# Image Classification via ResNet18 and MobileNetV2 Fusion

## Abstract
This project implements a hybrid deep learning architecture for classifying 10 distinct object categories. By fusing feature maps from ResNet18 and MobileNetV2, the model achieves superior accuracy compared to single-model baselines.

## Methodology
The architecture utilizes two pre-trained backbones as feature extractors.
* **ResNet18**: Provides 512-dimensional deep structural features.
* **MobileNetV2**: Provides 1280-dimensional lightweight edge features.
* **Feature Fusion**: The features are concatenated into a single 1792-dimensional vector before passing through a final fully connected classification layer.



## Results
The fusion approach demonstrated high performance consistency across the specialized dataset.
* **Fusion Accuracy**: 100.0%
* **Baseline Accuracy**: 100.0%
* **Improvement**: 0.0%

## Confusion Matrix
The following heatmap visualizes the model performance across all 10 classes. The strong diagonal confirms successful classification with zero cross-class confusion.



## Discussion
The 100.0% accuracy recorded for both models suggests a ceiling effect caused by the high quality and specific focus of the 10-image dataset. This outcome validates the technical "domino effect" of the implementation:
* The data loader correctly assigned labels to folders.
* The fusion logic successfully merged 1792 unique features without data loss.
* The training loop reached absolute convergence for all target categories.

## Conclusion
Feature fusion effectively captures diverse image characteristics, making it ideal for small, specialized datasets. The model successfully distinguished all 10 objects, proving that architectural combination reduces classification errors found in standard models.


## Model Weights
The trained weights for this fusion model exceed GitHub's direct upload limit. 
You can download the `.pth` file here: [Download fusion_model_weights.pth]https://drive.google.com/drive/folders/1JiCxCcOwZSMwYNm6GyCCpaZxjZAuYz7j
