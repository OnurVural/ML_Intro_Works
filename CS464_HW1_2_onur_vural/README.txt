N.Onur VURAL 21902330 
CS464 ML SEC2
q2main.ipynb

In this implementation:
	* the csv files are extracted as dataframe objects
	* train and val data statistics are outputted
	* components for classification and reporting accuracy is present
		piArray(dataset, label): prob estimation of given class
		thetaArray(dataset, label): word occurecy estimation for given class
		thetaArrayExtended(dataset, label, alpha): word occurecy estimation for given class for given alpha smoother

	* components for theta and pi MLE is present
		classify(allPredictions): @return correct labels
		accuracyResults(validLabels, validPredictedLabels): outputs accuracy

	* the MultinomialNBClassiffier class has following methods:
		fit(self, df_test, label): uses train data to set MLE's
		printer(self): outputs pi and theta estimated values
		predict(self, df_val): @return predicted label values
		confusionMatrix(self, df, label): @return confusion matrix 

	
	* the MultinomialNBClassiffierExtended class has following methods:
		fit(self, df_test, label, alpha): uses train data to set MLE's for given alpha smoother
		printer(self): outputs pi and theta estimated values
		predict(self, df_val): @return predicted label values
		confusionMatrix(self, df, label): @return confusion matrix

	* test results of accuracy, predicted labels and confusion matrix are outputted for both classifiers