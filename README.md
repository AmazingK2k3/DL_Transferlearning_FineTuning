# DL_CNN_TransferLearning_FineTuning
 A deep learning Project that involves the use of Keras prebuilt Convnets, using transfer learning and finetuning and integrating the performance of these models using the ensemble learning method. This project is primarily for learning purposes. The dataset used for this project is the Hutton Rock dataset from Kaggle 

 ### Models Used
 The pre-trained keras CNN Models used for Transfer Learning and Finetuining are:
 1. Model-1: InceptionResNetV2
 2. Model-2: DenseNet201
 3. Model-3: ConvNeXtTiny

### Transfer Learning
Certain Modifications were applied in each transfer learning model for learning purposes. They are:
- Model-1 → Include a Batch Normalization and Dropout layer with a 25% drop rate before the output layer.
- Model-2 → Include a Batch Normalization and Dropout layer with a 35% drop rate before the output layer.
- Model-3 → Include a Dropout layer with a 15% drop rate before the output layer.

 ### Fine Tuning
 Similarly, the Transfer Learning models including their weights were again used for fine-tuning with modifications. They are:
  - Model-1 → Set the initial 25% of the layers are non-trainable and the remaining layers as trainable.
  - Model-2 → Set the initial 35% of the layers are non-trainable and the remaining layers as trainable.
  - Model-3 → Set all the layers as trainable.

### Ensemble Learning
- The finetuned models were then combined under a user-defined Ensemble_Predict() function that yielded predictions based on these models using the majority voting method. Confusion matrix and Precision recall scores were generated for all the models in this project. 
