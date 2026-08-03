# Brain Tumor Classification Using CNN and Channel Attention
# https://alinaderiii.github.io/brain-tumor-classification-paper
Official materials and project page for our peer-reviewed article on multiclass brain tumor classification from MRI.
[![DOI](https://img.shields.io/badge/DOI-10.1155%2Fcplx%2F1644859-006699?style=for-the-badge)](https://doi.org/10.1155/cplx/1644859)
[![Open Access](https://img.shields.io/badge/Open_Access-Complexity_(Wiley)-6C4AB6?style=for-the-badge)](https://onlinelibrary.wiley.com/doi/10.1155/cplx/1644859)
[![Project Page](https://img.shields.io/badge/Project_Page-E85D4A?style=for-the-badge&logo=googlechrome&logoColor=white)](https://alinaderiii.github.io/brain-tumor-classification-paper/)
## Article
**Convolutional Neural Network and Channel Attention Mechanism for Multiclass Brain Tumor Classification**
Naderi A., Asgharzadeh-Bonab A., Ahmadi F., Kalbkhani H.
| | |
| :--- | :--- |
| Journal | Complexity (Wiley), Volume 2025 |
| Published | 30 June 2025 |
| Access | Open Access (CC BY 4.0) |
| DOI | [10.1155/cplx/1644859](https://doi.org/10.1155/cplx/1644859) |
## Abstract
This paper presents a deep learning framework combining Convolutional Neural Networks with a Channel Attention Mechanism for effective multiclass classification of brain tumors using MRI images. The proposed model comprises three components: a fine-tuned EfficientNetB7 backbone adapted through transfer learning, a channel attention module that refines extracted feature maps to emphasise clinically relevant tumour features, and a fully connected classifier optimised through grid search. Hyperparameter tuning and data augmentation further improve generalisation and robustness.
## Results
| Dataset | Task | Accuracy |
| :--- | :--- | ---: |
| Brats-4C | Four-class (glioma, meningioma, pituitary, no tumour) | **98.16%** |
| Brats-2C large | Binary | **99.4%** |
| Brats-2C small | Binary | **99.2%** |

Validated with 5-fold stratified cross-validation.
### Comparison with prior work
| Method | Architecture | Accuracy |
| :--- | :--- | ---: |
| Kang et al. (2021) | DenseNet-169 + ShuffleNet + MnasNet | 91.58% |
| Irmak (2021) | Custom CNN | 92.66% |
| Shahin et al. (2023) | MPCANet (PCANet + CNN) | 94.02% |
| Demir and Akbulut (2022) | R-CNN + SVM | 96.60% |
| **This work** | **EfficientNetB7 + CAM + FC** | **98.16%** |
## Architecture
**Transfer learning.** EfficientNetB7 pre-trained on ImageNet. The first four MBConv blocks are frozen; blocks 5 to 7 are fine-tuned for domain-specific oncological patterns.
**Channel attention module.** Exploits inter-channel relationships through average and max pooling to amplify clinically relevant tumour features before classification.
**Classifier head.** Batch normalisation, a 256-neuron dense layer selected by grid search, 45% dropout, and softmax output.
**Training.** SGDM optimiser, cross-entropy loss, L1 and L2 regularisation, and rigorous data augmentation.
## Repository contents
| File | Description |
| :--- | :--- |
| [Project page](https://alinaderiii.github.io/brain-tumor-classification-paper/) | Live summary page |
| [Complexity_2025_Naderi_Convolutional_Neural_Network_and_Channel.pdf](Complexity_2025_Naderi_Convolutional_Neural_Network_and_Channel.pdf) | Full open-access article |
| [Deep Learning & Medical Imaging.html](https://alinaderiii.github.io/brain-tumor-classification-paper/Deep%20Learning%20%26%20Medical%20Imaging.html) | Extended case study with visualisations |
| index.html | Source of the project page |
## Citation
```bibtex
@article{naderi2025cnn,
  title   = {Convolutional Neural Network and Channel Attention Mechanism for Multiclass Brain Tumor Classification},
  author  = {Naderi, Ali and Asgharzadeh-Bonab, Akbar and Ahmadi, Farid and Kalbkhani, Hashem},
  journal = {Complexity},
  volume  = {2025},
  year    = {2025},
  publisher = {Wiley},
  doi     = {10.1155/cplx/1644859}
}
```
## Authors
**Ali Naderi** - Department of Mechatronics Engineering, Urmia University of Technology
ORCID: [0009-0004-8166-5449](https://orcid.org/0009-0004-8166-5449) | [Portfolio](https://alinaderiii.github.io/) | [alinaderi119@gmail.com](mailto:alinaderi119@gmail.com)
Akbar Asgharzadeh-Bonab - Department of Electrical and Computer Engineering, Urmia University
Farid Ahmadi (corresponding author) - Department of IT and Computer Engineering, Urmia University of Technology
Hashem Kalbkhani - Department of Electrical Engineering, Urmia University of Technology
## License
The article is published Open Access under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). Please cite the paper if you build on this work.
