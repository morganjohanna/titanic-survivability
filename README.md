# Titanic Survivability Prediction
*Predicting survivability with the Titanic dataset from [Kaggle](https://www.kaggle.com/competitions/titanic/overview)*

The objective was to predict whether or not a passenger on the Titanic survived given various information. Data (and key) are provided by Kaggle and available at the link above. The dataset was artificially split so that the selection available to create the model consists of 891 passengers, with the remaining 418 used for testing (which is done automatically by Kaggle upon upload).

I've only included the model with the best result obtained via Kaggle, a random forest model with accuracy 0.78468, and another I made with a Voting Classifier combining it with a simple logistic regression model with accuracy 0.7799.

This project was one of my earliest and took me around 2 person days to complete to its current status.

# Process
Step 1 is located in **eda.ipynb** with the rest in **titanic_pred.ipynb**
1. Basic exploratory data analysis
2. Import and split data; note that, despite the naming structure, "train.csv" is used for training and testing the model while "test.csv" is for applying the trained and tested model
3. Feature engineering with sklearn pipeline and column transformer
3. Fit and test models, calculate accuracy for split "train" dataset
4. Export and upload to Kaggle for "test"

# Next
If I dedicated more time to this project, I would use the data to come up with new variables in pursuit of a better score, like identifying family groups, and filling in missing values more reliably by segmenting into girls, boys, men, and women based on titles. I might also split it into classes to try to use cabins (mostly available for first class) as a variable, or to segment by fare and class to try to assign at least the cabin deck for missing values. 

I previously used a Voting Classifier to bring together a simple logistic regression model with the random forest model shown here, it would be interesting to use it to explore other algorithms and feature tweaking, especially if there were additional variables.