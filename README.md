# Exoplanet Exploration thru Machine Learning     
### *An analysis of four machine learning models*

![exoplanets.jpg](Images/exoplanets.jpg)

## Background

Over a period of nine years in deep space, the NASA Kepler space telescope has been out on a planet-hunting mission to discover hidden planets outside of our solar system.

To help process this data, I have created four machine learning models capable of classifying candidate exoplanets from the raw dataset. 

## THE WORK     
#### *Four Models Created:*     
1. ``K Nearest Neighbors``
2. ``Logistic Regression``
3. ``LinearSVC``
4. ``Decision Tree``     
5. *An addition neural network model can be found [here](https://github.com/VallieTracy/machine-learning-challenge/tree/master/NeuralNetworkModel_1.ipynb "Neural Network").*     
#### *Packages/Libraries Used:* 
- [Sklearn](https://scikit-learn.org/stable/index.html "scikit-learn")
- Joblib
- Pandas
- NumPy
- Matplotlib
- TensorFlow for the neural network

#### *Tools Used to Optimize the Data:*     
  - GridSearchCV for hyperparameter tuning          
  - MinMaxScaler for preprocessing      
  - ExtraTreesClassifier for feature selection       
  
#### *General Methodology:*         
For each of the four classification models, I first created a model and only did hyperparameter tuning, no feature selection.  Then I created a second model, where I could focus on the feature selection.  I decided to take this route, thinking if I could whittle down the hyperparameters, then I could most effectively determine the best features.  NOTE: I didn't test it in the other direction.

## ANALYSIS      
As far as which model 'performed' the best, it really depends on what we're looking to accomplish.  Something that could be worth noting for stability purposes: both the SVM and Decision Tree models had consistent accuracy & precision values according to the classification_report.  When I say consistent, I mean the values didn't change from the first model of only hypertuning to the second model which included both hypertuning and feature selection.     
      
Another intersting observation: yes, SVM had the highest score after feature selection and hypertuning, at .8932.  Potentially more interesting, it had the lowest difference between the Training Data and Testing Data.  And at the other end of the spectrum, the Decision Tree model had the highest difference.

The Logistic Model had the most fluctation in the classification report from the first model to the second.  But seeing some zero values, I might have made a misstep. I've included a screen shot of the report [here](https://github.com/VallieTracy/machine-learning-challenge/tree/master/Classification_Reports/log_only_hp.PNG "Logistic Report")  Something to be looked at should this project be explored further.

The final results of the trainingg data:
1. KNN started at .8545 and ended at .8825     
2. Logistic started at .6859 and ended at .8810     
3. SVM started at .8440 and ended at .8932     
4. Decision Tree started at 1.00 and ended at .8861

If you would like to see screen shots of the final classification report for each model, you can click here or find them ....





