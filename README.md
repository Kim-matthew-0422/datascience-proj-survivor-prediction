# datascience-proj-survivor-prediction
prediction survival rates of passengers in crash
predictions for Kaggle titanic competition.

models used : GaussianNB, LogisticRegression, DecisionTree, KNeighbors, RandomForest, GradientBoosting, CatBoost

Scoring results: (0.77990 3.5k~ / 50k)

6	Gradient Boosting Trees	84.85
7	CatBoost	81.82
1	Logistic Regression	80.81
5	Decision Tree	78.68
2	Naive Bayes	76.43
0	KNN	69.02
4	Linear SVC	68.01
3	Stochastic Gradient Decent	63.64

Gradient Boosting Trees ended up overfitting, was not the correct result after running the Kaggle data.

Some interesting finds: 
 [!alt text](https://github.com/Kim-matthew-0422/datascience-proj-survivor-prediction/blob/main/Factirs.png)
 
 Had initially thought gender would be the biggest factor, but it turns out age and fare had bigger impact.
 
 To improve results, deciphering Fares and Cabin would be one method. 
 
 voting classifier hard = best result 
 (voting_clf_hard = VotingClassifier(estimators = [('knn',best_knn),('rf',best_rf),('svc',best_svc),('gbt',best_gbt)], voting = 'hard')
