# DigiPath
A model that could generate segmented masks for the Ki-67 patches dataset obtained from real-world samples.

## Table of Contents

- [Introduction](#introduction)
- [Pre-requisites](#pre-requisites)
- [Related Work](#related-work)
- [Solution Approach](#solution-approach)
- [Detailed Discussion](#detailed-discussion)
- [Results Obtained](#results-obtained)
- [References](#references)


<a name="introduction"></a>
## Introduction

Welcome to the Ki-67 Patch Segmentation project called "DigiPath"! This repository contains code and resources for a machine-learning model that can generate segmented masks for the Ki-67 patches dataset obtained from real-world samples. Ki-67 is an essential protein associated with cell proliferation and serves as a critical biomarker in cancer research. The accurate segmentation of Ki-67 regions within the patches can provide valuable insights into tumor growth and patient prognosis.

<a name="pre-requisites"></a>
## Pre-requisites
To use the Ki-67 Patch Segmentation project, you should have the following pre-requisites in place:

1) Python: Ensure you have Python installed on your local machine. The project is developed using Python, and you will need it to run the code and Jupyter notebooks.
2) Jupyter Notebook: Install Jupyter Notebook to interact with the provided notebooks. Jupyter Notebook allows you to run code cells, modify the project, and visualize the results.
3) Tensorflow, PyTorch and TorchVision: The UNet model implementation requires Tensorflow, PyTorch and TorchVision libraries. Make sure you have installed these libraries to run the UNet model.
4) Google Colab (Optional): If you prefer using Google Colab to run the notebooks online, you can sign in to your Google account and open the provided .ipynb notebooks directly in Colab.
5) Ki-67 Patches Dataset: This project assumes you have access to the Ki-67 patches dataset sourced from real-world samples, preferably from AIIMS Raipur.

<a name="related-work"></a>
## Related Work
The project explores two different approaches to semantic segmentation:

UNet Model: This model is based on the UNet architecture proposed by Ronneberger et al. [1]. The UNet's encoder-decoder design with skip connections allows for the precise localization of objects in images, making it suitable for biomedical image segmentation tasks.

SegFormer Model: The SegFormer architecture, introduced by Xie et al. [2], utilizes transformers for semantic segmentation. Transformers have shown impressive capabilities in computer vision tasks, including capturing global context within images.

<a name="solution-approach"></a>
## Solution Approach

### Data Preprocessing
The Ki-67 patches dataset obtained from AIIMS Raipur was preprocessed to ensure standardized input for model training. The images were resized to a common resolution and normalized to a fixed pixel value range. Data augmentation techniques were applied to enhance the training dataset and improve model generalization.

### UNet Model
The UNet model was implemented using Tensorflow, leveraging its encoder-decoder architecture. Training the model involved using the annotated dataset and optimizing it with binary cross-entropy loss and Dice loss, typical choices for semantic segmentation tasks.

### SegFormer Model (Work in Progress)
While the UNet model has been successfully implemented, the exploration of the SegFormer model remains a work in progress. The implementation faces some challenges, and further research is required to resolve encountered errors and improve its performance.

<a name="detailed-discussion"></a>
## Detailed Discussion
A detailed discussion of the project's approach, data preprocessing steps, and model implementations can be found in the provided Jupyter notebooks:

- [UNet Model Implementation](UNET_digiPath.ipynb)
- [SegFormer Model Implementation](Segformer_Digipath.ipynb)

<a name="results-obtained"></a>
## Results Obtained

The UNet model achieved promising results, indicating accurate segmentation performance, effectively capturing Ki-67 regions within the patches. The generated segmented masks closely aligned with the ground truth annotations, affirming the model's effectiveness. However, since the SegFormer implementation was incomplete, no results could be obtained for this model. Further investigation and debugging are required to fully realize the potential of SegFormer for this specific task.

I hope this work contributes to advancements in cancer research and medical image analysis.


<a name="references"></a>
## References
[1] Ronneberger, O., Fischer, P., & Brox, T. (2015). U-Net: Convolutional Networks for Biomedical Image Segmentation. In Medical Image Computing and Computer-Assisted Intervention – MICCAI 2015 (pp. 234–241). Springer, Cham.

[2] Xie, L., Yuan, L., Zhao, L., Wang, Q., & Zhou, Y. (2021). SegFormer: Simple and Efficient Design for Semantic Segmentation with Transformers. In Computer Vision – ECCV 2020 (pp. 670–686). Springer, Cham.
