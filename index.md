# Brain Tumor Radiogenomic Classification

WPI CS 539 ML Final Project

Felipe Mejias, Jose Raul Gamez Carias, Shreedhar Kodate, Khatera Alizada, Nicholas Josselyn

### <ins>Project Goal</ins>: Determine methylation status of brain tumors using magnetic resonance imaging (MRI)

## Introduction

Automated identification of brain tumors in MRI has many profound clinical applications in surgical treatment planning, image-guided interventions, monitoring tumor growth, and the generation of radiotherapy maps for treatment plans. However, manual identification of brain tumors on MRI is time-consuming, tedious, and subjective and at times it can require invasive follow-up surgeries [1]. Radiologists perform a manual, qualitative approach to identify tumors on MRI, which becomes impractical when dealing with a large number of patients. The automated solution will expedite the process and will decrease the cost of the procedure. The patients, who would otherwise have to wait for longer periods of time because of manual identification procedures by radiologists, could be diagnosed in a timely manner and start their treatment sooner, saving precious time that could extend their lives.


## Background

There is an existing work that ensembles multiple architectures trained on the BraTS data set, however, they do so in order to generate high quality segmentations of brain tumors. In our work, we intend to ensemble architectures, across various MRI scan types, for the classification of methylation status of the tumor. The promise of using ensemble techniques is shown as this implementation won the BraTS competition for segmentation in 2017 [2]. Additionally, work has been done using traditional machine learning to extract features and ensemble methods for classification [3]. However, we propose to remove the manual feature extraction step and employ deep learning models to learn the features to extract and ensemble them to build a reliable classifier. There also exists a work that uses a different MRI dataset with deep learning and ensemble methods for assessing MRI image quality. This work tunes a CNN by adapting and adjusting the VGG architecture to fit their data and ensembles models that were trained on one MRI scan type, but across different scan orientations (coronal, sagittal, and axial) [4].


## Methodology

### Data

We will use the MRI scans of patients from the BraTS 2021 dataset that labels the MGMT status of the patients. The BraTS 2021 dataset is a comprehensive collection of brain tumor MRI scans of patients from various institutions that use different equipment and imaging protocols that represent heterogeneous image quality and diverse clinical practices from different institutions [1,5]. The dataset we will use consists of 585 cases/patients. The data is essentially balanced with 47% being labeled ‘0’ (unmethylated) and 53% being labeled ‘1’ (methylated). The dataset will be divided into training, validation and testing data sets. As part of the BraTS 2021 data set, the participants are provided with binary class labels denoting their tumor methylation status. Each patient has 4 different scan types (T1w, T2w, FLAIR, and T1wCE) each of which captures unique information of the tumors.

### 3D Convolutional Neural Network

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.

### VGG 16

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/fmejias/CS539MachineLearningProject/settings/pages). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

## Results

These were the results:

## References

[1] Baid, U. et al., “The RSNA-ASNR-MICCAI BraTS 2021 Benchmark on Brain Tumor Segmentation and Radiogenomic Classification”, arXiv:2107.02314 (2021)

[2] Kamnitsas, K. et al., “Ensembles of Multiple Models and Architectures for Robust Brain Tumor Segmentation”, International MICCAI brain lesion workshop (2017)

[3] Gupta, N. et al., “Glioma detection on brain MRIs using texture and morphological features with ensemble learning”, Biomedical Signal Processing and Control (2019)

[4] Sujit, S. et al., “Automated image quality evaluation of structural brain MRI using an ensemble of deep learning networks”, Journal of Magnetic Resonance Imaging (2019)

[5] RSNA-MICCAI Brain Tumor Radiogenomic Classification | Kaggle 

[6] https://github.com/hasibzunair/3D-image-classification-tutorial 
