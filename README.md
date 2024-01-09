**COVID-19 Classification with Generative Data Augmentation**

**Introduction**
The COVID-19 pandemic has underscored the need for fast and accurate diagnostics in critical healthcare situations. Deep Learning algorithms, especially Convolutional Neural Networks 
(CNNs), have shown promise in automating accurate diagnoses. However, the scarcity of data, especially during epidemics, poses a challenge. This project addresses this concern by 
utilizing generative methods to augment small datasets, comparing the efficacy of pre-existing neural network architectures trained with both traditional and synthetic data.

**Dataset**
The COVID-19 dataset comprises MRI scans from Kaggle, categorized into three classes: Normal, Viral Pneumonia, and COVID-19. The dataset distribution is crucial for 
understanding class balance.
**Methodology**
1. **Traditional Augmentation** :  To overcome the small sample size, traditional augmentation techniques were initially employed, resulting in 1255 training samples.
The dataset was split into training (1000), validation (255), and testing (66) sets.
2. **Data Augmentation Using GANs** : Generative Adversarial Networks (GANs) were used to generate synthetic images, addressing the challenge of limited medical data.
The Conditional Generative Adversarial Network (cGAN) framework was employed to create contextually relevant images.
The training loop for the cGAN iterated 500 epochs, resulting in generated images at epoch 0 and epoch 500. These synthetic images were seamlessly integrated, expanding the dataset.

**Deep Learning Models**
Several deep-learning models were employed, including ResNet-50, Xception, MobileNet-v2, a Custom Model, and VGG16. The models were fine-tuned using both traditionally augmented 
and GAN-augmented datasets.

**Results**
Testing accuracies of the models with traditional and GANs augmented training data are summarized below.
Model	Traditional (%)	GANs (%)
ResNet-50	94	79
Xception	83	67
MobileNet-v2	95	92
Custom Model	89	85
VGG16	97	83

**Conclusion**
In conclusion, deep-learning models trained on traditionally augmented datasets outperformed those trained with synthetic images from GANs. Computational limitations
and noise introduced by GANs impacted the accuracy. Future work could focus on mitigating GAN limitations to enhance the effectiveness of generative data augmentation in 
medical image classification. 
