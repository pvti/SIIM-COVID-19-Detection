# SIIM-COVID-19-Detection
> [**Identification and localization COVID-19 abnormalities on chest radiographs via ensemble of convolutional neural networks**](https://drive.google.com/file/d/1tgmOoJpSYjiDAOTYwTCjrQMP4Fylq3uh/view?usp=sharing),            
> Van-Tien Pham;        

![](readme/ProposedFramework.png)

> Contact: [pvtien96@gmail.com](mailto:pvtien96@gmail.com). Discussions are welcome!

## Abstract
Solutions to screen and diagnose patients positive for the SARS-CoV-2 promptly and efficiently are critical in the context of the COVID-19 pandemic's complex evolution. Recent researches have demonstrated the efficiency of deep learning and convolutional neural networks (CNNs) in classifying and detecting lung disease-related lesions from radiographs. This paper presents a solution using ensemble learning techniques on advanced CNNs to classify as well as localize COVID-19-related abnormalities in radiographs. Two classifiers including EfficientNetV2 and NFNet are combined with three detectors, DETR, Yolov7 and EfficientDet. Along with gathering and training the model on a large number of datasets, image augmentation and cross validation are used. Since then, this study has shown extremely promising results and has received excellent marks in the Society for Imaging Informatics in Medicine's competition. The analysis in model selection for the trade-off between speed and accuracy is also given as a basis for practical applications.

## News
- **[2022.09.06]** Create baseline.


## Main results

F1 score of the COVID-19 abnormalities classifiers on the SIIM test set:

|   Classifier   |        F1 score        |                    |                          |                     |
|----------------|:----------------------:|:------------------:|:------------------------:|:-------------------:|
|                | Negative for Pneumonia | Typical Appearance | Indeterminate Appearance | Atypical Appearance |
| NFNet          |          0.79          |        0.56        |           0.59           |         0.72        |
| EfficientNetv2 |          0.83          |        0.54        |           0.61           |         0.75        |

Evaluation of the COVID-19 lesion detector on the SIIM test set:

| Detector            | Accuracy (mAP@ IoU 0.5:0.95) |                |                       |         Performance         |                 |
|---------------------|:----------------------------:|:--------------:|:---------------------:|:---------------------------:|:---------------:|
|                     |        Discrete model        | Lung localized | Inference speed (FPS) | GPU memory requirement (MB) | Model size (MB) |
| DETR                |             0.542            |      0.587     |           25          |             2683            |       232       |
| Yolov7              |             0.563            |      0.591     |           34          |             3520            |       290       |
| EfficientDet        |             0.499            |      0.574     |           19          |             1903            |       187       |
| Weighted Box Fusion |             0.605            |      0.612     |           8           |             8106            |       709       |

## Installation

Please refer to [INSTALL.md](readme/INSTALL.md) for installation instructions.

## Model zoo

Trained models are available in the [MODEL_ZOO.md](readme/MODEL_ZOO.md).

## Dataset zoo

Please see [DATASET_ZOO.md](readme/DATASET_ZOO.md) for detailed description of the training/evaluation datasets.

## Getting Started

Follow the aforementioned instructions to install environments and download models and datasets.

[GETTING_STARTED.md](readme/GETTING_STARTED.md) provides a brief intro of the usage of builtin command-line tools.

## License

Code is released under the [Apache 2.0 license](LICENSE).

## Citing

If you use this work in your research or wish to refer to the results, please use the following BibTeX entry.

```BibTeX
@misc{tien2022COVID,
  author =       {Van-Tien Pham},
  title =        {Identification and localization COVID-19 abnormalities on chest radiographs via ensemble of convolutional neural networks},
  howpublished = {\url{https://github.com/pvtien96/SIIM-COVID-19-Detection}},
  year =         {2022}
}
```
