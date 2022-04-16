# Projects
Programming Language: R

Models Used: Logistic regression with best subset selection, KNN Regression, Lasso Regression, Random Forest Analysis, Pruned Decision Trees.

Objective: 
The project observes a year long record of bank logs to achieve the following objectives:
  1. Differentiate between the labeled intrusions and benign sessions
  2. Develop and implement a systematic approach to detect instances of intrusions in log files. Our system will be able to take a new network_traffic log file and          determine the existence of known patterns of intrusions as well as anomalies which may be indicative of new and unknown intrusion patterns.
  3. Evaluate detection power of our system.

Source:
The network_traffic.csv file is a synopsis of logged network activity. It contains labeled examples of benign network sessions as well as examples of sessions involving intrusions. The bank observed while analyzing a year long record of logs, there were many instances of anomalous network activity that resulted in significant sums of money being siphoned from bank accounts.

Task 1:Data Cleaning 
I started data cleaning with analysing the range of values in each variable, using the summary function. There were a number of variables that had very few non zero values and for that reason we decided to drop those columns.

Task 2: Recoding variable values
All the labels were identified in two categories - an intrusion i.e error or normal.

Task 3: Data Analysis
I checked the distribution of various variables by plotting their histograms. We then plot correlation matrix and paired plots of the predictor variables in the dataset, remove atleast one of the pair of variables with high correlation.
Check for correlation between predictor variables and the resposne variable - those with high correlation are important for detectign intrusions.
Split the data set into training and test set. Train different models on the train set and then test them on the test set.

Task 5: Analysis of Methods
To evaluate each model’s ability to detect network intrusions, it is important to have high sensitivity and high negative predicted value. All the models were evaluated based on these parameters.

In conclusion, it was observed that the following variables src_bytes, service, flag, logged_in, and dst_bytes are the discerning variables that exert some degree of association on recognizing intrusions. New log files can be run using the full logistic regression model, glm.allfit, or the random forest model, traffic.rf.
