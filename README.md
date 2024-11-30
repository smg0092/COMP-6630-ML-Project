Here’s the revised version of your document with `-` added before each occurrence of "Cell" and adjusted for clarity:

---

# COMP-6630-ML-Project  
The ML Project for the Machine Learning course at Auburn University (COMP-6630)  

Here is the link to the dataset we are using (from Kaggle):  
https://www.kaggle.com/datasets/tawsifurrahman/covid19-radiography-database/data  

**FullCode.ipynb** - This is the entire code we used, including our loaded data, the algorithms and models used, and the results.  
We don't have many methods, so I'll explain each cell:  

---

### Imports for part 1  
===============================================================================================

- Cell 1 - Our various imports that involve lots of packages from the scikit-learn Python library for machine learning.  
- Cell 2 - Deprecated code.  

---

### Data Preprocessing  
================================================================================================================  

- Cell 3 - We are importing the various folders and preprocessing them by making them numerical numpy arrays. We are also taking related images and crossing them over with the other in hopes it will improve our metrics. We get our X and y this way, data and labels respectively.  
- Cell 4 - We're splitting the data into validation, training, and test sets around an 80%-20% split.  
- Cell 5 - We're making a scaled version of the test, train, and validation data for a certain run of our logistic regression.  
- Cell 6 - We're using principal component analysis (PCA) on some test, train, and validation data for another run of logistic regression.  
- Cell 7 - We're converting the PCA and scaled sets to PyTorch tensors so the models can take them.  
- Cell 8 - We've defined five model classes here:  
  1. A basic logistic regression.  
  2. A basic multi-layer perceptron (MLP).  
  3. An MLP with a dropout layer.  
  4. An MLP using the PCA sets.  
  5. The PCA MLP with extra parameters.  
- Cell 9 - A function to test and run each model made in Cell 7. It gives us the accuracy, precision, and recall.  
- Cell 10 - Prepping the test datasets and a test dataset loader (loads the dataset).  

---

### Logistic Regression  
================================================================================================================  

- Cell 11 - The training and running of our logistic regression models and its subsequent output per epoch.  
- Cell 12 - The graphing data from the results of Cell 11.  
- Cell 13 - The score table resulting from our logistic regression runs.  

---

### MLP  
================================================================================================================  

- Cell 14 - The training and running of the MLP model, with the validation loss and training loss printed out per epoch.  
- Cell 15 - The plotted data resulting from Cell 14, showing the loss and accuracy over epochs.  
- Cell 16 - The metrics and scores resulting from Cell 14.  

---

### MLP Dropout  
================================================================================================================  

- Cell 17 - The training and running of the MLP dropout model.  
- Cell 18 - The validation and accuracy plots resulting from Cell 17.  
- Cell 19 - The metrics resulting from Cell 17.  

---

### MLP PCA  
================================================================================================================  

- Cell 20 - The training and running of the MLP PCA model.  
- Cell 21 - The validation and accuracy plots resulting from the training in Cell 20.  
- Cell 22 - Loading the PCA model into the test dataset and test dataloader.  
- Cell 23 - The scores resulting from Cell 20.  

---

### MLP PCA - Extra Params  
================================================================================================================  

- Cell 24 - The training and running of the MLP PCA extra parameters model.  
- Cell 25 - The validation and accuracy plots resulting from Cell 24.  
- Cell 26 - The metrics resulting from Cell 24.  

---

### Imports for part 2  
================================================================================================================  

- Cell 27 - This is the deep learning part of the code where we import lots of deep learning libraries.  

---

### Data Preprocessing  
================================================================================================================  

- Cell 28 - The data is downloaded via Kaggle Hub and preprocessed into class files and label files, then shuffled.  

---

### CNN  
================================================================================================================  

- Cell 29 - The CNN model is imported, built, compiled, and run. The results and metrics are printed below. The model is run with only 10 epochs here versus 60 in Cell 30. This was done to see the difference between the two models.  
- Cell 30 - The CNN model being run with 60 epochs and its results.  

---

### RNN  
================================================================================================================  

- Cell 31 - The compilation, building, and fitting of the RNN model. We also import it here.  
- Cell 32 - The report and scores from the RNN model.  

---

### VGG  
================================================================================================================  

- Cell 33 - We preprocess the data for the VGG model, using a new folder that has greyscale images with 3 channels instead of 2.  
- Cell 34 - The VGG model is run and built 5 times, and we average out those scores.  

--- 
