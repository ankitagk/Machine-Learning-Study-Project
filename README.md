# Machine-Learning-Study-Project



Problem Statment:-
Many studies are being conducted for cancer treatment and the research shows that precision medicine and especially genetic testing is bringing innovative ways in which cancer can be treated. Once sequenced, a cancer tumor can have thousands of genetic mutations. But the challenge is distinguishing the mutations that contribute to tumor growth (drivers) from the neutral mutations (passengers). The problem we are facing that most of the genetic testing is done manually. This is a very time-consuming task where a clinical pathologist has to manually review and classify every single genetic mutation based on evidence from text-based clinical literature.
We need to develop a Machine Learning algorithm that, using this knowledge base as a baseline, automatically classifies genetic variations.

Resource:-
This problem statement is taken from Kaggle:
https://www.kaggle.com/c/msk-redefining-cancer-treatment
The following data set can be downloaded from Kaggle
training_variants.zip and training_text.zip

Approach:-

Understood the data set provided and using the dataset tried to understand the above problem in Machine Learning world. Since, the dataset is huge I loaded it using python itself by including all the packages shown in the Juypter note book shared by me.

In the data set  there are mainly  4 fields
•	ID : row id used to link the mutation to the clinical evidence
•	Gene : the gene where this genetic mutation is located
•	Variation : the aminoacid change for this mutations
•	Class : class value 1-9, this genetic mutation has been classified on
On analysis we found that this is discrete data so it is classification problem and since there are multiple discrete output possible so we can call it Multi class classification problem.
This is medical related problem so correct results are very important. Error can be really costly here so we would like to have result for each class in terms of Probability. We might not be much bothered about time taken by ML algorithm as far as it is reasonable.
We also want our model to be highly interpretable because a medical practitioner want to also give proper reasoning on why ML algorithm is predicting any class.

Steps :-

Kindly follow the juypter notebook to get the complete details and code analysis for each step-

1)	Analysis of the Problem Statement:
2)	Creating Training, Test and Validation Data
3)	Building a Random Model
4)	Confusion Matrix
5)	Precision
6)	Recall
7)	Evaluating Gene Column
8)	Evaluating Variation Column
9)	Evaluating Text Column
10)	Data Preparation for Machine Learning Models
11)	Building Machine Learning Model – Naïve Bayes
12)	Building Machine Learning Model – KNN
13)	Building Machine Learning Model – Logistic Regression
14)	Building Machine Learning Model – Random Forest Classifier


Result:-

For each model we can see the accuracy in the training data, cross validation and test data and even the missclassification %


Naïve Bayes (One Hot Encoding) - Training Data(%)	0.84	Cross Validation Data (%)1.24	Test Data (%)	1.25 Misclassification Error (%)	37.78
K Nearest Neighbour ( Response Encoding)	Training Data(%)0.65	Cross Validation Data (%) 11.01	Test Data (%) 1.07	 Misclassification Error (%)33.83
Logistic Regression ( With Balance One Hot Encoding) Training Data(%)	0.61	Cross Validation Data (%) 1.1 Test Data (%)	1.06	 Misclassification Error (%)35.33
Logistic Regression ( Without Balance One Hot Encoding) Training Data(%)	0.61 Cross Validation Data (%)	1.09 Test Data (%)	1.07	 Misclassification Error (%)34.77
Linear SVM	Training Data(%)0.74	Cross Validation Data (%)1.13	Test Data (%) 1.14  Misclassification Error (%)	34.21
Random Forest (One Hot Encoding)	Training Data(%)0.71 Cross Validation Data (%)	1.14 Test Data (%)	1.12  Misclassification Error (%)	38
Random Forest ( Response Encoding)	Training Data(%) 0.05	Cross Validation Data (%) 1.2 Test Data (%)	1.3  Misclassification Error (%)	48.86



Conclusion:-
•	Analyzed discrete data to interpret the genetic mutations and defined the Multi-class classification problem. Developed six different ML algorithm (KNN, Naïve Bayes, Decision Tree, Random Forest, Logistic Regression SVM) in Python and evaluated the model accuracy by Multi class log-loss and found KNN to be the best fit having log loss value of 0.65 and least misclassification error of 33.83%







