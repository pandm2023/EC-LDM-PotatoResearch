EC-LDM: Enhanced Class-Conditioned Latent Diffusion Model for Potato Leaf Disease Classification
Overview

This repository contains the implementation of the Enhanced Class-Conditioned Latent Diffusion Model (EC-LDM) for potato leaf disease classification. The proposed framework learns disease-aware latent representations through class-conditioned latent diffusion and utilizes the learned latent features for robust disease classification.

The experiments are conducted on the publicly available Potato Leaf Disease (PLD) Dataset, containing:

Early Blight
Late Blight
Healthy
Repository Contents

1. EC_LDM512andPROPOSED1024D.ipynb

This notebook contains:

EC-LDM architecture
512-D latent representation learning
Proposed 1024-D latent representation learning
Class-conditioned latent diffusion training
Image reconstruction
Disease-aware latent feature learning
Training and validation procedures

2. 1024D_EC_LDMClassifier.ipynb

This notebook contains:

Classification using learned EC-LDM features
Frozen encoder experiments
Fine-tuned encoder experiments
Performance evaluation
ROC analysis
Confusion matrix generation
t-SNE visualization
SHAP explainability analysis


3. classifierplddataset.ipynb

This notebook contains implementations of comparative deep learning classifiers used for benchmarking:

AlexNet
VGG19
ResNet50
DenseNet201
EfficientNetB0
InceptionV4
Xception
MobileNetV1

The classifiers are trained and optimized on the same PLD dataset to provide a fair comparison with the proposed EC-LDM framework.

Proposed EC-LDM Framework

The proposed EC-LDM consists of:

Disease-Aware Encoder
Convolution Layers
Residual Blocks
Self-Attention Module
Class-Conditioned Latent Diffusion
Time Embedding
Disease Class Embedding
Latent Denoising Network
Latent Representation Learning

Two latent dimensionalities are investigated:

512-D Latent Space
1024-D Latent Space
Ablation Study

A comprehensive ablation study is performed to analyze:

Latent Dimensions
512-D EC-LDM
1024-D EC-LDM
Encoder Training Strategies
Experiment A: Frozen Encoder

The pretrained encoder is frozen and only the classifier head is trained.

Experiment B: Fine-Tuned Encoder

The encoder and classifier are jointly optimized for disease classification.


PLD-Dataset
| Class        |   Images |
| ------------ | -------: |
| Early Blight |     1628 |
| Late Blight  |     1424 |
| Healthy      |     1020 |
| **Total**    | **4072** |

Experimental requirements
pip install torch torchvision
pip install numpy pandas
pip install scikit-learn
pip install matplotlib seaborn
pip install shap
pip install scipy


Authors

Pankajkumar Thakre
Indian Institute of Information Technology Nagpur (IIIT Nagpur)

Dr. Jagdish Chakole
Indian Institute of Information Technology Nagpur (IIIT Nagpur)
