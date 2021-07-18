# Simple-image-calssification
This is my solution to kaggle competition: cats vs dogs classification. All relevant info can be found in their 
website: https://www.kaggle.com/c/dogs-vs-cats . my aim here is to create a very simple model and to play with hyperparameters.
Here is my short summary:

The model architechture: (((CNN - ReLU - BatchNorm) X 2) - MaxPool) X 3 - AveragePool -Flatten - (dense) x 2
Average pooling is used for the sake of reducing training parameters.
Validation accuracy ~80-85%

1. BatchNormalization is very Important. Without it the model does not train well. (~70 training accuracy) (~65% validation accuracy)
2. Normalizing and centering data is very necessary.
3. The model performs better for larger batch size (128, 64, 32 was tried: 128 performs best)
4. Effect of Weight regularizers (l2 regularizer was used) is small.
5. No difference between RMSProp and ADAM.
6. Increasing number of Convolutional filters per layer does not give noticable improvement. 


