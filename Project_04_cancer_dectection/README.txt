1. This purpose if this project is to use Covolutional Neural Network in order to detect if the slide images of Breast Cancer (BCa) specimens are IDC negative or IDC positive. 

2. Dataset: 
- The dataset can be downloaded from: https://www.kaggle.com/paultimothymooney/breast-histopathology-images
- The original dataset consisted of 162 whole mount slide images of Breast Cancer (BCa) specimens scanned at 40x. From that, 277,524 patches of size 50 x 50 were extracted (198,738 IDC negative and 78,786 IDC positive). Each patch’s file name is of the format: u_xX_yY_classC.png — > example 10253_idx5_x1351_y1101_class0.png . Where u is the patient ID (10253_idx5), X is the x-coordinate of where this patch was cropped from, Y is the y-coordinate of where this patch was cropped from, and C indicates the class where 0 is non-IDC and 1 is IDC

3. Approach:
- Train, test and validated split
- Convolutional Neural Network with 2 layers, loss= Categorical crossentropy, optimizer=Adadelta, metrics=Accuracy(validation) , epochs = 20

4. Results: 
- Best model at Epoch 19: val_accuracy = 0.85475
- Confustion metric: ([[34452,  5224],
                      [ 3177, 12652]])
- f1 score: 0.7507491470108292
  precision score: 0.7077646005817856
  recall score: 0.799292437930381


