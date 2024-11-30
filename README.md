# COMP-6630-ML-Project
The ML Project for the Machine Learning course at Auburn University (COMP-6630)

Here is the link to the dataset we are using (from Kaggle):
https://www.kaggle.com/datasets/tawsifurrahman/covid19-radiography-database/data

FullCode.ipynb - This is the entire code we used, including our loaded data, the algorithmns and models used, and the results
We don't have many methods so I'll explain each cell:

Imports for part 1
================================================================================================================
  Cell 1 - our various imports that involve lots of package from the scikit learn python library for machine 
  leraring 
  Cell 2 - depricated code 

Data Preprocessing
================================================================================================================
Cell 3 - We are importing the various folders and preprocessing them by making them numerical numpy arrays. We are also taking related images and crossing them over with the other in hopes it will improve our metrics. we get our X and y this way, data and labels respectively 
Cell 4 - We're splitting the data into validation, training, and test sets around 20% 80% split 
Cell 5 - We're making a scaled version of the test, train, and val data for a certain run of our logistic progression 
Cell 6 - We're using principal component analysis on some test, train, and val data for another run of logistic regrssion 
Cell 7 - We're converting the PCA and scaled sets to pytorch tensors so the models can take them 
Cell 8 - We've defined 5 models classes here:
  1 is a basic logist regression
  2 is a basic multi layer preceptron
  3 is a MLP with a dropout layer 
  4 is a MLP where we used the PCA sets 
  5 is a the PCA MLP with extra parameters 

Cell 9 - A function to test and run each model made in cell 7. It gives us the accuracy, precision, and recalls
Cell 10 - just prepping the test datasets and a test dataseteloader (loads the dataset)

Logistic Regerssion
================================================================================================================
Cell 11 - The trianing and running of our logistic regression models and its subsequnect output per epoch 
Cell 12 - The graphing data from the results of C11
Cell 13 - The score table resulting from our Logistic regression runs

MLP
================================================================================================================
Cell 14 - The training and running of the MLP model, the valiation loss, and training loss being printed out per epoch
Cell 15 - The plotted data resulting from Cell 14. Showing the loss and accuracy over epoch 
Cell 16 - the Metrics and scores resulting from C14. 

MLP Drouput
================================================================================================================
Cell 17 - The training and running of the MLP droupout model. 
Cell 18 - the val and accuracy plots resulting from C17
Cell 19 - the metrics resulting from C17

MLP PCA
================================================================================================================
Cell 20 - The training and running of the MLP PCA model. 
Cell 21 - the val and accuracy plots resulting from the training in C20
Cell 22 - the loading of the pca model in test dataset and test dataloader 
Cell 23 - the scores resulting from C20 

MLP PCA - Extra Params
================================================================================================================
Cell 24 - The training and running of the MLP PCA extra parameters model. 
Cell 25 - the val and accuracy plots resulting from C24
Cell 26 - the metrics resulting from C24

Imports for part 2
================================================================================================================
Cell 27 - This is the Deep learining part of the code where we import lots of deep learining libraries 

Data Preprocesing
================================================================================================================
Cell 28 - The data is downloaded via kaggle hub and preprocessed into class files and label files. Shuffled as well

CNN
================================================================================================================
Cell 29 - The CNN model is imported, built, compiled, and run. The results and metrics are printed below. The model is run with only 10 epochs here vs 60 in C30. This was done in order to see the difference between the two models
Celll 30 - The CNN model being run with 60 epochs and its resutls 

RNN
================================================================================================================
Cell 31 - The compilation, building, and fitting of the rnn model. We also import it here
Cell 32 - The report and scores from the RNN model

VGG
================================================================================================================
Cell 33 - We preprocess the ddata for the Vgg model, using a new folder that has greyscale images with 3 channels instead of 2
Cell 34 - the Vgg model is run and built 5 times and we average out those scores













