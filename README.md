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

The Logistic Model had the most fluctation in the classification report from the first model to the second.  But seeing some zero values, I might have made a misstep. I've included a screen shot of the report [here](https://github.com/VallieTracy/machine-learning-challenge/tree/master/Classification Reports "Neural Network")  Something to be looked at should this project be explored further.

The final results of the trainingg data:
1. KNN started at .8545 and ended at .8825     
2. Logistic started at .6859 and ended at .8810     
3. SVM started at .8440 and ended at .8932     
4. Decision Tree started at 1.00 and ended at .8861

If you would like to see screen shots of the final classification report for each model, you can click here or find them ....


### Before You Begin

1. Create a new repository for this project called `machine-learning-challenge`. **Do not add this homework to an existing repository**.

2. Clone the new repository to your computer.

3. Give each model you choose their own Jupyter notebook, **do not use more than one model per notebook.**

4. Save your best model to a file. This will be the model used to test your accuracy and used for grading.

5. Commit your Jupyter notebooks and model file and push them to GitHub.

## Note

Keep in mind that this homework is optional! However, you will gain a much greater understanding of testing and tuning different Classification models if you do complete it.



In this homework assignment, you will need to:

1. [Preprocess the raw data](#Preprocessing)
2. [Tune the models](#Tune-Model-Parameters)
3. [Compare two or more models](#Evaluate-Model-Performance)

- - -

## Instructions

### Preprocess the Data

* Preprocess the dataset prior to fitting the model.
* Perform feature selection and remove unnecessary features.
* Use `MinMaxScaler` to scale the numerical data.
* Separate the data into training and testing data.

### Tune Model Parameters

* Use `GridSearch` to tune model parameters.
* Tune and compare at least two different classifiers.

### Reporting

* Create a README that reports a comparison of each model's performance as well as a summary about your findings and any assumptions you can make based on your model (is your model good enough to predict new exoplanets? Why or why not? What would make your model be better at predicting new exoplanets?).

- - -

## Resources

* [Exoplanet Data Source](https://www.kaggle.com/nasa/kepler-exoplanet-search-results)

* [Scikit-Learn Tutorial Part 1](https://www.youtube.com/watch?v=4PXAztQtoTg)

* [Scikit-Learn Tutorial Part 2](https://www.youtube.com/watch?v=gK43gtGh49o&t=5858s)

* [Grid Search](https://scikit-learn.org/stable/modules/grid_search.html)

- - -

## Hints and Considerations

* Start by cleaning the data, removing unnecessary columns, and scaling the data.

* Not all variables are significant be sure to remove any insignificant variables.

* Make sure your `sklearn` package is up to date.

* Try a simple model first, and then tune the model using `GridSearch`.

- - -

## Submission

* Create a Jupyter Notebook for each model and host the notebooks on GitHub.

* Create a file for your best model and push to GitHub

* Include a README.md file that summarizes your assumptions and findings.

* Submit the link to your GitHub project to Bootcamp Spot.

##### © 2019 Trilogy Education Services, a 2U, Inc. brand. All Rights Reserved.
