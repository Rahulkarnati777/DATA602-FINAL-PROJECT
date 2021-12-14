# DATA602-FINAL-PROJECT
ABSTRACT:
According to the dataset considered, this situation deals with violation of laws 
and the features related to citations in court from different areas for different people. Most of the times when there is violation of law, the authorities settle it using charges. Few times there are cases where people are charged without committing any violations or there are cases where people resist the charges
for an inevitable reason. so in this work, for a citation, we are going to find if the hearing Status is issued or not meaning we are trying to understand how features of citations are affecting people who face any hearing status and people who don't have one. This helps us to know better about the current mindset of people and the mistakes made by them and in-turn provide an analysis for jurisdiction for easy flow of their work. 
![image](https://user-images.githubusercontent.com/91164843/146068869-995be7ac-e50d-4ee2-8b14-e42125a9f3be.png)


Proposed Work:
Trying to produce an intelligent, analytic solution for above discussed problem
Using machine Learning techniques.
 


Explanation:
Data Acquisition: converting the normal data like csv file etc. into python understandable data such as nd-array object of numpy or DataFrame object of pandas. 
Data Analysis: understanding the basics of the data loaded. To have knowledge of number of columns, number of rows, their statistics, correlations etc. So that we can perform Data pre-processing step. 
Data pre-processing: cleaning the data like removing the empty values, removing insignificant columns, removing outliers, encoding the data or filtering high correlation. preparing the data for giving it as input to the algorithm etc.   

Summary of Data Analysis and Data Pre-Processing:
1.	The original dataset has 204161 rows and 30 columns
2.	We are considering only first 50000 rows and 30 columns as population for the research.
3.	As the population has many columns, missing values and outliers. We will  be processing the population with many different dimensionality reduction steps as follows
a.	First removal of the columns with large number of categorical values as both one-hot encoding or label encoding will not reduce the dimension or will add bias to data.
b.	Second handling the missing values, as in the population we have missing values in only 2 columns and they are only 0.0044%  of the total data. So we will remove the rows with missing values.
c.	In few columns with continuous data, there were outliers which are being removed using Isolation Forest algorithm.
d.	Now object type of data has to be vectorized. Here we are using label encoder to handle columns with moderately high columns 

Setting the Features and Labels:
•	selecting the Hearing-Status as label.
•	so as to predict in which instance people can got to that extent for violation charges.
•	if a citation has Hearing or not is only considered.





Data Splitting: creating the training set and testing set so that we can train the algorithm and understand the performance of that model. 
We are going with random samples for Training and Testing sets.
As in population, we have very less positive values
•	93.49377704420752% negative values
•	6.506222955792479% positive values
when random state '7' was used for splitting, it has more instances in minority class i.e. more positive values which helps in testing more on minority class
In training set, we are having
•	93.61251289486158% negative values
•	6.387487105138429% positive values
In testing set, we are having
•	93.0188468830155% negative values
•	6.9811531169844985% positive values
it is observed that both the training and testing set are following the ratios of the population.
Minimum Performance level that classifiers should have to be useable:
93.0188468830155 %

Instantiating: Creating the object of Algorithm to train, test and evaluate.
Selecting Algorithms based on the immune or in-sensitive to outliers 
1. Decision Tree classifier
2. Random Forest Classifier
And considering few more algorithm to understand the effect of outliers
1. Logistic Regression
2. Support Vector Machine

Training: Making the particular algorithm understand the relation between training inputs and training outputs and become intelligent in that concept.  

Validation: data sample used to understand the performance of ML model while Training. 

Testing: process used to predict the outputs for the inputs in the test set.   

Grid Search: After selecting the most promising models we fine tune their parameters to perform even better. 

comparing the metrics: process used to measure performance of all the algorithms and to obtain a conclusion

selected metric system
* Accuracy Score
* Precision Score
* Recall
* f1-Score
* Confusion Matrix
* ROC curve
out of all the above metrics, 'accuracy' helped the most in many cases like Decision tree, Random Forest, Logistic Regression where rest of the metrics like Recall, F1-score, precision were are 100% except for SVM Algorithm. Confusion matrix and ROC curve helped to understand the model better.

Results
we were able to classify the instances as having a hearing or not having with a very good performance of 99.96+ % even when there were few outliers were left in the data. Random Forest was best and decision tree, Logistic Regression was also performing close to best and SVM had many difficulties in classification as it is sensitive to the outliers. 

Next steps
1. we have only considered a sample data from the population. for the complete data the procedure for data pre-processing may change
2. all the outliers were not removed, few were left in the dataset. further understanding of the data in better way is possible.
3. much better algorithms can be researched on that can handle the outliers like voting classifier.
4. research can be done in finding a better representative sample. for training, validation and testing purposes by understanding the distributions of different random sample. And etc.


