![Visitors](https://api.visitorbadge.io/api/visitors?path=https%3A%2F%2Fgithub.com%2Fpvtien96%2FSIIM-COVID-19-Detection&countColor=%23dce775)
# 👩‍⚕️ Identification and Localization COVID-19 Abnormalities on Chest Radiographs
<div>
<div align="center">
    <a href='https://github.com/pvtien96' target='_blank'>Van Tien PHAM<sup>1,&#x2709</sup></a>&emsp;
    <a href='http://tpnguyen.univ-tln.fr/' target='_blank'>Thanh Phuong NGUYEN<sup>1</sup></a>&emsp;
</div>
<div>

<div align="center">
    <sup>1</sup><em>Université de Toulon, Aix Marseille Université, CNRS, LIS, UMR 7020, France</em>&emsp;
    <sup>&#x2709</sup><em>Corresponding Author</em>
</div>

<div style="text-align: justify"> Solutions to screen and diagnose positive patients for SARS-CoV-2 promptly and efficiently are critical in the context of the COVID-19 pandemic’s complex evolution. Recent researches have demonstrated the efficiency of deep learning and particularly convolutional neural networks (CNNs) in classifying and detecting lung disease-related lesions from radiographs. This paper presents a solution using ensemble learning techniques on advanced CNNs to classify as well as localize COVID-19-related abnormalities in radiographs. Two classifiers including EfficientNetV2 and NFNet are combined with three detectors, DETR, Yolov7, and EfficientDet. Along with gathering and training the model on a large number of datasets, image augmentation, and cross-validation are also addressed. Since then, this study has shown promising results and has received excellent marks in the Society for Imaging Informatics in Medicine’s competition. The analysis in model selection for the trade-off between speed and accuracy is also given.

<div>
  <img class="image" src="readme\ProposedFramework.png" width="100%" height="100%">
</div>


## 📋 News
- **[2023.01.02]** Paper is accepted to [AICV 2023](http://egyptscience.net/AICV2023/home.html).
- **[2022.09.06]** Create baseline.


## 🦠 Main results
<p align="center" width="100%">
    <img src="readme/ClassificationPerformance.png" width="50%" height="50%">
</p>

Evaluation of the COVID-19 lesion detector on the SIIM test set:

| Detector            | Accuracy (mAP@ IoU 0.5:0.95) |                |                       |         Performance         |                 |
|---------------------|:----------------------------:|:--------------:|:---------------------:|:---------------------------:|:---------------:|
|                     |        Discrete model        | Lung localized | Inference speed (FPS) | GPU memory requirement (MB) | Model size (MB) |
| DETR                |             0.542            |      0.587     |           25          |             2683            |       232       |
| Yolov7              |             0.563            |      0.591     |           34          |             3520            |       290       |
| EfficientDet        |             0.499            |      0.574     |           19          |             1903            |       187       |
| Weighted Box Fusion |             0.605            |      0.612     |           8           |             8106            |       709       |

## 💉 Installation

Please refer to [INSTALL.md](readme/INSTALL.md) for installation instructions.

## 🧬 Model zoo

Trained models are available in the [MODEL_ZOO.md](readme/MODEL_ZOO.md).

## 💻 Dataset zoo

Please see [DATASET_ZOO.md](readme/DATASET_ZOO.md) for detailed description of the training/evaluation datasets.

## 🔍 Getting Started

Follow the aforementioned instructions to install environments and download models and datasets.

[GETTING_STARTED.md](readme/GETTING_STARTED.md) provides a brief intro of the usage of builtin command-line tools.


## 🔬 Citing

If you use this work in your research or wish to refer to the results, please use the following BibTeX entry.

```BibTeX
@inproceedings{pham2023identification,
  title={Identification and localization COVID-19 abnormalities on chest radiographs},
  author={Pham, Van Tien and Nguyen, Thanh Phuong},
  booktitle={The International Conference on Artificial Intelligence and Computer Vision},
  pages={251--261},
  year={2023},
  organization={Springer}
}
```
