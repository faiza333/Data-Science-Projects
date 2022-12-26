## Zero_deforestation Classification

### Aim of the Project: 
Data science challenge from schneider-electric-european-hackathon, creating an image classification model, predicts what type 
of deforestation appears in the image with the objective of early detection of this type of actions in protected lands.

### Dataset:
A training 'csv' files that relate the ID of the images to their features and classes.

A testing 'csv' files that relate the ID of the images to their features.

A zip file containing a few thousand training and testing images. This zip file has a weight of 309MB.

The challenge will be to create an image classification model and train it with the training images 
we provide, once you find the model that maximizes the f1-score, you will have to apply your model to classify
the testing images. Your score will depend on the F1-score of your model with the test images, the quality of your
code and the explanation of the solution you provide

### Technology: 
- Python, numpy, pandas, matplotlib, seaborn, cv2, seaborn, sklearn, tensorflow
### EDA(Exploratory Data Analysis)
#### Percentage of label
majority label of the training dataset is labeled 0 with 50.18%, the label 1 has the smallest percentage.

![download (2)](https://user-images.githubusercontent.com/68142873/209485096-0180ca67-a92c-466e-bfde-5a7cc2ad16a3.png)

we have a lot of coincides between label 0 and label 2.

![download (9)](https://user-images.githubusercontent.com/68142873/209485176-87413349-c52a-483f-ab9e-f36a981f457e.png)

from the violin plot we can observe that the distribution of label 0 and label 2 on the latitude are similar to a uniform
distribution,however, their distribution of the longitude is gathered in two mayor part.

![download (6)](https://user-images.githubusercontent.com/68142873/209485205-03f32640-4cb9-465d-96f5-a543938971a3.png)

using geopandas to plot the data on a world map so we could get a better understanding of the location of where the image was taken.

![download (7)](https://user-images.githubusercontent.com/68142873/209485229-3afc6433-1cc0-4f99-9e18-a681533ae8a8.png)

### Model Creation
The used model is EfficientNetV2S
- Input pipeline generators (class: BalanceDatasetGenerator).
- Image augmentation (class: ImageAugmentationEngine)
- Model generator (class: ModelGenerator)
Result 

- loss: 0.7323 - categorical_accuracy: 0.7135 - auc_all: 0.8719 - precision_0: 0.7845 - recall_0: 0.7679 - precision_1: 0.7845 - recall_1: 0.7679 - precision_2: 0.7845 - recall_2: 0.7679 
- val_loss: 1.2013 - val_categorical_accuracy: 0.6071 - val_auc_all: 0.7840 - val_precision_0: 0.8452 - val_recall_0: 0.5598 - val_precision_1: 0.8452 - val_recall_1: 0.5598 - val_precision_2: 0.8452 - val_recall_2: 0.5598

