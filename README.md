# DL_PracticeLabAssignment_2
OCR Transfer Learning Pipeline
This project implements an OCR pipeline using transfer learning, inspired by the research paper:

Leveraging Transfer Learning and GAN Models for OCR from Engineering Documents
Wael Khallouli et al., IEEE

Overview
Objective:
Adapt a pre-trained ResNet101 model for OCR tasks by fine-tuning its top layers. This notebook demonstrates the end-to-end process—from dataset preparation to model evaluation—using the ICDAR 2015 dataset.

Dataset:
The ICDAR 2015 dataset is downloaded from Roboflow.
Link: ICDAR 2015 on Roboflow
Images are preprocessed (resized to 224×224, grayscale conversion, normalization) and augmented using Keras' ImageDataGenerator.

Model:
A pre-trained ResNet101 model is used as the backbone. Initially frozen, the top layers are later unfrozen for fine-tuning with a lower learning rate. Feature maps are visualized to inspect intermediate outputs.

Evaluation:
The model is evaluated using standard classification metrics (accuracy, precision, recall, F1-score, confusion matrix). Training and validation trends are plotted to monitor performance.
