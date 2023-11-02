# Lead-Scoring-Parametric-vs-ML
Classification problem of the leads for an insurtech, in order to establish a commercial priority of them. Comparison between logistic regression and neural network classifiers.

## About the Project
The insurtech company I collaborated with is a digital broker based in Italy, intermediating between insurance companies and small and medium-sized enterprises, privates, offering a smart, full digital and customized insurance policy. New clients land in the website page, fill in the survey and a quote is available. Then they can subscribe a policy online with a full digital experience. Prospects that do not finish this procedure autonomously are managed by the sales department, deciding how to finalize the acquisition: by an intern sales consultant, by a call center or not finalizing the acquisition. In order to optimally allocate the business resources of company, a classification tool is built, using both parametric and nonparametric tequinques: a **multinomial logistic regression model** and a **neural network classifier** have been developed, comparing the performance of goodness of fit and prediction. 

## Metodology
- Preliminary analysis and outlier detection
- A **Multinomial Logistic Regression** model has been fitted, using **4 different techniques**: linearity in the covariates, first order interaction, and two different weights based on time elapsed since the last interaction with the client. The best model in terms of prediction has been chosen as the optimal one.
- In order to make the classifier more sensible with respect to the Non-managed class, the dataset has been augmented using a **synthetic data generation** algorithm oversampling that class. The target to be replicated has been identified using a clustering technique, applying a supervised dimensionality reduction to identify clusters that maximize the separation in the embedded space between labelled classes (that are the labels of the output variable in the regression).
- A **Neural network** has been designed in order to improve the prediction performance. In particular we used a fully connected NN with 2 layers and softfax output layer. In order to avoid overfitting a L2 regularitazion term is added.
- **Results**: the two different approaches show similar results in terms of prediction, reaching **68% accuracy** on the test set. The oversampling method lead to a **simultaneous increase of sensitivity and specificity** for the Non-managed class, at a little expense of Sales class, which was the most frequent in the dataset. This achievement is important in terms of **reducing unnecessary costs** for the company, avoiding to manage lead that are not commercially appealing.  





